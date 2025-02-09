### **Przetwarzanie strumieniowe w Javie (java.util.stream)**

Przetwarzanie strumieniowe w Javie to podejście do operowania na kolekcjach danych, które umożliwia eleganckie i efektywne przetwarzanie danych w sposób deklaratywny. Strumienie (ang. *streams*) pozwalają na wykonywanie operacji na danych w sposób funkcyjny, umożliwiając przetwarzanie elementów kolekcji bez konieczności używania tradycyjnych pętli. Są one częścią pakietu `java.util.stream`, wprowadzonego w Javie 8, i pozwalają na użycie operacji takich jak filtrowanie, mapowanie, redukcja i inne.

### **1. Czym są strumienie?**

Strumień w Javie to sekwencyjna lub równoległa kolekcja elementów, na której można wykonywać różne operacje. Strumień nie przechowuje danych, lecz przetwarza je na bieżąco. Każda operacja na strumieniu jest lazily evaluated, co oznacza, że operacje są wykonywane dopiero w momencie, gdy dane są rzeczywiście potrzebne (np. przy zakończeniu strumienia lub jego kolejnym przetworzeniu).

### **2. Podstawowe elementy przetwarzania strumieniowego**

#### **2.1. Tworzenie strumieni**
Strumienie można tworzyć na kilka sposobów, na przykład z kolekcji, tablic czy generatorów.

**Przykłady tworzenia strumieni:**

- Z kolekcji:
  ```java
  List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
  Stream<Integer> stream = numbers.stream();
  ```

- Z tablicy:
  ```java
  String[] names = {"Anna", "Bartek", "Czesław"};
  Stream<String> stream = Arrays.stream(names);
  ```

- Z generatora:
  ```java
  Stream<Integer> infiniteStream = Stream.iterate(0, n -> n + 2);
  ```

#### **2.2. Operacje na strumieniach**

Strumienie oferują dwa rodzaje operacji: **operacje pośrednie** (intermediate) oraz **operacje terminalne** (terminal).

- **Operacje pośrednie**: Przetwarzają strumień, ale nie zwracają ostatecznego wyniku. Zamiast tego zwracają nowy strumień, który może być przetwarzany dalej.
  - **Przykłady**:
    - `filter()` – filtruje elementy na podstawie warunku.
    - `map()` – przekształca elementy w inny typ lub zmienia je według określonego wzorca.
    - `distinct()` – usuwa duplikaty.
    - `sorted()` – sortuje elementy.

    **Przykład**:
    ```java
    List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9);
    List<Integer> evenNumbers = numbers.stream()
                                       .filter(n -> n % 2 == 0)  // Filtrujemy liczby parzyste
                                       .collect(Collectors.toList());  // Zbieramy wynik w liście
    System.out.println(evenNumbers);  // [2, 4, 6, 8]
    ```

- **Operacje terminalne**: Kończą operacje na strumieniu, zwracając wynik lub wywołując efekt uboczny. Po wykonaniu operacji terminalnej strumień nie może być już używany.
  - **Przykłady**:
    - `collect()` – zbiera wyniki w formie kolekcji.
    - `forEach()` – wykonuje operację na każdym elemencie.
    - `reduce()` – redukuje strumień do jednej wartości.
    - `count()` – zlicza elementy strumienia.
    - `anyMatch()` – sprawdza, czy przynajmniej jeden element spełnia warunek.

    **Przykład**:
    ```java
    List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
    int sum = numbers.stream()
                     .filter(n -> n % 2 != 0)  // Filtrujemy liczby nieparzyste
                     .reduce(0, Integer::sum);  // Redukujemy je do sumy
    System.out.println(sum);  // 9 (1 + 3 + 5)
    ```

---

### **3. Przykłady operacji strumieniowych**

#### **3.1. `map()`**
Operacja `map()` pozwala na przekształcenie każdego elementu strumienia.

**Przykład**:
```java
List<String> words = Arrays.asList("apple", "banana", "cherry");
List<Integer> lengths = words.stream()
                             .map(String::length)  // Przekształcamy słowa na ich długości
                             .collect(Collectors.toList());
System.out.println(lengths);  // [5, 6, 6]
```

#### **3.2. `filter()`**
Operacja `filter()` filtruje elementy strumienia na podstawie zadanego warunku.

**Przykład**:
```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6);
List<Integer> evenNumbers = numbers.stream()
                                   .filter(n -> n % 2 == 0)  // Wybieramy liczby parzyste
                                   .collect(Collectors.toList());
System.out.println(evenNumbers);  // [2, 4, 6]
```

#### **3.3. `reduce()`**
Operacja `reduce()` pozwala na zredukowanie strumienia do jednej wartości, wykonując operację na wszystkich jego elementach.

**Przykład**:
```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
int result = numbers.stream()
                    .reduce(0, (a, b) -> a + b);  // Sumowanie elementów
System.out.println(result);  // 15
```

#### **3.4. `forEach()`**
Operacja `forEach()` umożliwia wykonanie operacji na każdym elemencie strumienia.

**Przykład**:
```java
List<String> names = Arrays.asList("Anna", "Bartek", "Czesław");
names.stream()
     .forEach(name -> System.out.println(name));  // Wypisuje każdą nazwę
```

---

### **4. Strumienie równoległe (Parallel Streams)**

Java pozwala na równoległe przetwarzanie strumieni za pomocą metody `parallelStream()`. Strumienie równoległe dzielą dane na mniejsze fragmenty, które są przetwarzane na różnych rdzeniach procesora, co może przyspieszyć operacje na dużych zbiorach danych.

**Przykład**:
```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
int sum = numbers.parallelStream()
                 .reduce(0, Integer::sum);  // Suma liczb przy użyciu strumienia równoległego
System.out.println(sum);  // 55
```

Należy pamiętać, że strumienie równoległe nie zawsze są szybsze niż strumienie sekwencyjne, ponieważ ich użycie wiąże się z pewnymi kosztami związanymi z zarządzaniem równoległym przetwarzaniem.

---

### **5. Podsumowanie**

Strumienie w Javie oferują elastyczny i funkcjonalny sposób przetwarzania danych. Umożliwiają one wykonywanie złożonych operacji na kolekcjach danych w sposób deklaratywny, co zwiększa czytelność i skraca kod. Dzięki takim operacjom jak `filter()`, `map()`, `reduce()`, `forEach()` oraz wsparciu dla strumieni równoległych, Java 8 wprowadza nowoczesne podejście do przetwarzania danych. Programowanie strumieniowe jest szczególnie przydatne w przypadkach, gdzie chcemy wykonywać operacje na dużych zbiorach danych w sposób bardziej efektywny i przejrzysty.