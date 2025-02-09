### **Problem szeregowania procesów i wątków w systemach operacyjnych**  

#### **1. Wprowadzenie do szeregowania**  
Szeregowanie procesów i wątków to kluczowy aspekt działania systemów operacyjnych, który wpływa na **wydajność, responsywność i sprawiedliwy podział zasobów**. Polega na decydowaniu, **który proces lub wątek otrzyma dostęp do procesora**, pamięci i innych zasobów w danym momencie.  

#### **2. Rodzaje szeregowania**  
Wyróżniamy trzy główne poziomy szeregowania w systemach operacyjnych:  

1. **Szeregowanie długoterminowe (Long-Term Scheduling)**  
   - Decyduje, **które procesy są wprowadzane do systemu** (przejście ze stanu "nowy" do "gotowy").  
   - Spotykane w systemach wsadowych i serwerowych, gdzie ogranicza się liczbę jednocześnie działających procesów.  

2. **Szeregowanie krótkoterminowe (Short-Term Scheduling, CPU Scheduling)**  
   - Wybiera proces do wykonania na procesorze spośród procesów w stanie "gotowy".  
   - Działa bardzo szybko (milisekundy) i jest krytyczne dla wydajności systemu.  

3. **Szeregowanie średnioterminowe (Medium-Term Scheduling)**  
   - Decyduje o **wstrzymaniu i wznowieniu procesów** (przejście między "gotowy" i "wstrzymany").  
   - Stosowane w systemach wielozadaniowych dla optymalizacji użycia pamięci.  

#### **3. Kryteria oceny algorytmów szeregowania**  
Dobry algorytm szeregowania powinien spełniać następujące kryteria:  
- **Sprawiedliwość** – każdy proces powinien mieć dostęp do CPU.  
- **Efektywność** – maksymalne wykorzystanie CPU.  
- **Czas odpowiedzi** – minimalizacja czasu reakcji dla procesów interaktywnych.  
- **Przepustowość** – liczba zakończonych procesów na jednostkę czasu.  
- **Czas oczekiwania** – minimalizacja czasu w kolejce do CPU.  
- **Czas realizacji (turnaround time)** – czas od zgłoszenia procesu do jego zakończenia.  

#### **4. Popularne algorytmy szeregowania procesów**  
Systemy operacyjne wykorzystują różne algorytmy planowania procesów, zależnie od typu systemu i wymagań użytkownika.  

1. **FCFS (First-Come, First-Served)**  
   - Najprostszy algorytm – procesy wykonują się w kolejności przyjścia.  
   - **Zalety**: Łatwy w implementacji.  
   - **Wady**: Może powodować efekt **"konwoju"** – długi proces blokuje krótsze.  

2. **SJF (Shortest Job First)**  
   - Wybiera proces o najkrótszym czasie wykonywania.  
   - **Zalety**: Minimalizuje średni czas oczekiwania.  
   - **Wady**: Wymaga znajomości czasu wykonania procesu (trudne do oszacowania).  

3. **Round Robin (RR)**  
   - Każdy proces dostaje **kwant czasu**, po czym jest przełączany.  
   - **Zalety**: Dobre dla systemów interaktywnych, zapewnia sprawiedliwość.  
   - **Wady**: Zbyt krótki kwant zwiększa narzut przełączeń kontekstu, zbyt długi upodabnia RR do FCFS.  

4. **Priorytetowe (Priority Scheduling)**  
   - Procesy mają przypisane priorytety – wyższy priorytet oznacza szybsze wykonanie.  
   - **Zalety**: Umożliwia obsługę krytycznych zadań.  
   - **Wady**: Może prowadzić do **zagłodzenia** niskopriorytetowych procesów (rozwiązanie: technika **starzenia** – zwiększanie priorytetu w czasie).  

5. **Multilevel Queue Scheduling**  
   - Procesy dzielone na klasy (np. systemowe, użytkowe, wsadowe), każda klasa ma własną kolejkę.  
   - **Zalety**: Umożliwia obsługę różnych typów zadań.  
   - **Wady**: Może prowadzić do głodzenia niższych kolejek.  

6. **Multilevel Feedback Queue (MLFQ)**  
   - Udoskonalona wersja multilevel queue – procesy mogą zmieniać kolejki w zależności od ich zachowania.  
   - **Zalety**: Adaptacyjność, dynamiczne dostosowanie priorytetów.  
   - **Wady**: Skomplikowana implementacja.  

#### **5. Szeregowanie w systemach wielowątkowych**  
W systemach wielowątkowych oprócz procesów należy planować wykonanie wątków. Popularne strategie obejmują:  
- **Wątki o równej priorytetyzacji** – obsługiwane według tych samych algorytmów co procesy.  
- **Wątki o różnym priorytecie** – wyższy priorytet może prowadzić do problemu **inwersji priorytetów** (np. gdy wątek o niskim priorytecie blokuje zasób dla ważniejszego wątku).  
- **Planowanie współdzielone (Thread Pooling)** – ograniczenie liczby jednocześnie działających wątków w celu poprawy wydajności.  

#### **6. Wyzwania w szeregowaniu**  
- **Starvation (zagłodzenie)** – procesy o niskim priorytecie mogą nigdy nie otrzymać dostępu do CPU.  
- **Inwersja priorytetów** – proces o wysokim priorytecie może być blokowany przez proces o niższym priorytecie.  
- **Overhead przełączenia kontekstu** – częste przełączanie procesów zwiększa narzut systemowy.  
- **Real-time scheduling** – w systemach czasu rzeczywistego procesy muszą być wykonane w określonym czasie (stosuje się np. RM – Rate Monotonic, EDF – Earliest Deadline First).  

#### **7. Podsumowanie**  
Szeregowanie procesów i wątków jest kluczowym zadaniem systemu operacyjnego, mającym wpływ na **wydajność, responsywność i równomierność podziału zasobów**. Wybór algorytmu zależy od specyfiki systemu – w systemach interaktywnych często stosuje się **Round Robin**, w systemach wsadowych **SJF** lub **FCFS**, a w systemach czasu rzeczywistego algorytmy oparte na terminach wykonania.