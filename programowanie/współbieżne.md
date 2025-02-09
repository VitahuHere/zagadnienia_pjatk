### **Programowanie współbieżne w języku Java: Mechanizmy i narzędzia**

Programowanie współbieżne w języku Java polega na tworzeniu aplikacji, które mogą wykonywać więcej niż jedno zadanie w tym samym czasie, umożliwiając wykorzystanie wielu rdzeni procesora i poprawiając wydajność aplikacji, szczególnie w środowiskach wielowątkowych. Java oferuje szereg narzędzi i mechanizmów, które wspierają tworzenie aplikacji współbieżnych.

---

### **1. Mechanizmy współbieżności w Javie**

#### **1.1. Wątki (Threads)**
- **Opis**: Wątek to jednostka wykonawcza, która wykonuje fragment kodu w ramach procesu. Każdy proces w systemie może mieć jeden lub więcej wątków, które współdzielą zasoby procesora.
- **Wykorzystanie w Javie**:
  - Można tworzyć wątki za pomocą klasy `Thread` lub implementując interfejs `Runnable`.
  - Klasa `Thread` pozwala na tworzenie wątków, zarządzanie nimi, a także na synchronizowanie dostępu do współdzielonych zasobów.
  
  **Przykład**:
  ```java
  class MyThread extends Thread {
      public void run() {
          System.out.println("Wątek działa!");
      }
  }

  public class Main {
      public static void main(String[] args) {
          MyThread t = new MyThread();
          t.start(); // Uruchamia nowy wątek
      }
  }
  ```

#### **1.2. Interfejs `Runnable`**
- **Opis**: Jest to alternatywna metoda tworzenia wątków. `Runnable` to interfejs, którego implementacja dostarcza metodę `run()`, którą należy wykonać w nowym wątku.
- **Zalety**: Umożliwia lepsze rozdzielenie logiki wątków od samego zarządzania wątkami. Może być używane do uruchomienia wątków w ramach różnych mechanizmów, jak np. w poolach wątków.
  
  **Przykład**:
  ```java
  class MyRunnable implements Runnable {
      public void run() {
          System.out.println("Wątek działający w ramach Runnable!");
      }
  }

  public class Main {
      public static void main(String[] args) {
          MyRunnable runnable = new MyRunnable();
          Thread t = new Thread(runnable);
          t.start(); // Uruchamia wątek
      }
  }
  ```

---

### **2. Narzędzia wspierające programowanie współbieżne**

#### **2.1. Executor Service**
- **Opis**: `ExecutorService` to interfejs w Javie, który pozwala na zarządzanie pulami wątków i efektywne zarządzanie wątkami. Jest to bardziej zaawansowane narzędzie w porównaniu do tradycyjnego używania klasy `Thread` czy `Runnable`.
- **Wykorzystanie**: Można używać takich klas jak `FixedThreadPool`, `CachedThreadPool`, `SingleThreadExecutor`, aby zarządzać pulami wątków.
  
  **Przykład**:
  ```java
  import java.util.concurrent.*;

  public class Main {
      public static void main(String[] args) {
          ExecutorService executor = Executors.newFixedThreadPool(4);
          
          Runnable task = () -> {
              System.out.println("Wątek działający w puli!");
          };

          for (int i = 0; i < 10; i++) {
              executor.submit(task); // Przekazywanie zadań do wykonania
          }

          executor.shutdown(); // Zamknięcie ExecutorService
      }
  }
  ```

#### **2.2. Synchronizacja (Synchronize)**
- **Opis**: Synchronizacja w Javie jest kluczowa w programowaniu współbieżnym, aby zapewnić, że tylko jeden wątek na raz będzie miał dostęp do danej sekcji kodu. Java oferuje dwa główne mechanizmy synchronizacji:
  1. **Blokada synchronizowana** – użycie słowa kluczowego `synchronized` przy metodach lub blokach kodu.
  2. **ReentrantLock** – bardziej elastyczna alternatywa pozwalająca na precyzyjne zarządzanie blokadami.
  
  **Przykład (Synchronize)**:
  ```java
  public class Counter {
      private int count = 0;

      public synchronized void increment() {
          count++;
      }

      public int getCount() {
          return count;
      }
  }
  ```

  **Przykład (ReentrantLock)**:
  ```java
  import java.util.concurrent.locks.Lock;
  import java.util.concurrent.locks.ReentrantLock;

  public class Counter {
      private int count = 0;
      private final Lock lock = new ReentrantLock();

      public void increment() {
          lock.lock(); // Zajmowanie blokady
          try {
              count++;
          } finally {
              lock.unlock(); // Zwolnienie blokady
          }
      }

      public int getCount() {
          return count;
      }
  }
  ```

#### **2.3. Semafory**
- **Opis**: Semafory to mechanizmy synchronizacji pozwalające na kontrolowanie dostępu do zasobów współdzielonych w systemie. Są one wykorzystywane, aby ograniczyć liczbę wątków, które mogą jednocześnie korzystać z jakiegoś zasobu.
- **Wykorzystanie**: Java dostarcza klasę `Semaphore` do zarządzania liczbą dostępnych zasobów.

  **Przykład**:
  ```java
  import java.util.concurrent.*;

  public class Main {
      public static void main(String[] args) throws InterruptedException {
          Semaphore semaphore = new Semaphore(3); // Zezwala na 3 wątki jednocześnie

          Runnable task = () -> {
              try {
                  semaphore.acquire(); // Zajmowanie semafora
                  System.out.println(Thread.currentThread().getName() + " zaczyna pracę");
                  Thread.sleep(1000);
                  System.out.println(Thread.currentThread().getName() + " kończy pracę");
              } catch (InterruptedException e) {
                  Thread.currentThread().interrupt();
              } finally {
                  semaphore.release(); // Zwolnienie semafora
              }
          };

          for (int i = 0; i < 5; i++) {
              new Thread(task).start();
          }
      }
  }
  ```

#### **2.4. CountDownLatch i CyclicBarrier**
- **Opis**: Są to mechanizmy synchronizacji pozwalające na synchronizację wątków w oparciu o liczbę oczekiwań.
  - **CountDownLatch**: Używany, gdy wątki muszą poczekać na zakończenie innych wątków przed kontynuowaniem swojej pracy.
  - **CyclicBarrier**: Umożliwia synchronizację wątków w taki sposób, że mogą one czekać na siebie nawzajem w określonych punktach.
  
  **Przykład (CountDownLatch)**:
  ```java
  import java.util.concurrent.*;

  public class Main {
      public static void main(String[] args) throws InterruptedException {
          CountDownLatch latch = new CountDownLatch(3); // Czeka na 3 wątki

          Runnable task = () -> {
              try {
                  Thread.sleep(1000);
                  System.out.println(Thread.currentThread().getName() + " wykonane!");
              } catch (InterruptedException e) {
                  Thread.currentThread().interrupt();
              } finally {
                  latch.countDown(); // Zmniejsza licznik
              }
          };

          for (int i = 0; i < 3; i++) {
              new Thread(task).start();
          }

          latch.await(); // Czeka na zakończenie wszystkich wątków
          System.out.println("Wszystkie wątki zakończone!");
      }
  }
  ```

---

### **3. Podsumowanie**

Programowanie współbieżne w Javie jest wspierane przez szeroki zestaw narzędzi, które pozwalają na efektywne zarządzanie wątkami, synchronizowanie dostępu do zasobów oraz kontrolowanie równoczesnych zadań. Dzięki mechanizmom takim jak `ExecutorService`, `synchronized`, `Semaphore`, czy `CountDownLatch`, Java umożliwia tworzenie wydajnych aplikacji wielowątkowych, które mogą w pełni wykorzystać możliwości nowoczesnych procesorów.