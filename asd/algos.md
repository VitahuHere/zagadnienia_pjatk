### **Najważniejsze algorytmy wyszukiwania i sortowania – przegląd i zastosowania**  

Algorytmy wyszukiwania i sortowania odgrywają kluczową rolę w informatyce, umożliwiając efektywne przetwarzanie danych.  

---

## **1. Algorytmy wyszukiwania**  

Algorytmy wyszukiwania służą do odnajdywania określonego elementu w zbiorze danych. Można je podzielić na dwa główne typy: **liniowe** i **binarne**.  

### **1.1 Wyszukiwanie liniowe (Linear Search)**  
- **Opis:** Sprawdza każdy element tablicy, aż znajdzie szukany element lub przejdzie przez cały zbiór.  
- **Złożoność czasowa:**  
  - Średnio: $ O(n) $  
  - Najlepiej: $ O(1) $ (jeśli element jest na początku)  
  - Najgorzej: $ O(n) $ (jeśli elementu nie ma w zbiorze)  
- **Zastosowania:**  
  - Wyszukiwanie w małych i nieposortowanych zbiorach.  
  - Proste aplikacje, gdy dane nie są uporządkowane.  

### **1.2 Wyszukiwanie binarne (Binary Search)**  
- **Opis:** Działa na posortowanych zbiorach, dzieląc dane na połowy i eliminując połowę, w której element nie może się znajdować.  
- **Złożoność czasowa:**  
  - Średnio: $ O(\log n) $  
  - Najgorzej: $ O(\log n) $  
  - Najlepiej: $ O(1) $ (jeśli element jest na środku)  
- **Zastosowania:**  
  - Szybkie wyszukiwanie w posortowanych zbiorach, np. w bazach danych, drzewach BST.  
  - Wyszukiwanie w słownikach, katalogach.  

---

## **2. Algorytmy sortowania**  

Sortowanie pozwala uporządkować dane, co jest kluczowe dla szybkiego wyszukiwania i optymalizacji operacji na zbiorach danych.  

### **2.1 Sortowanie bąbelkowe (Bubble Sort)**  
- **Opis:** Porównuje sąsiednie elementy i zamienia je miejscami, jeśli są w złej kolejności. Proces powtarza się, aż zbiór będzie posortowany.  
- **Złożoność czasowa:**  
  - Średnio i najgorzej: $ O(n^2) $  
  - Najlepiej: $ O(n) $ (dla już posortowanych danych)  
- **Zastosowania:**  
  - Proste implementacje edukacyjne.  
  - Niewielkie zbiory danych, gdzie wydajność nie jest kluczowa.  

### **2.2 Sortowanie przez wstawianie (Insertion Sort)**  
- **Opis:** Dzieli zbiór na część posortowaną i nieposortowaną, a następnie wstawia elementy z części nieposortowanej w odpowiednie miejsce.  
- **Złożoność czasowa:**  
  - Średnio i najgorzej: $ O(n^2) $  
  - Najlepiej: $ O(n) $ (dla posortowanych danych)  
- **Zastosowania:**  
  - Sortowanie małych zbiorów.  
  - Wstawianie nowych elementów do już posortowanej listy.  

### **2.3 Sortowanie przez wybór (Selection Sort)**  
- **Opis:** W każdej iteracji wybiera najmniejszy element i zamienia go z pierwszym elementem nieposortowanej części tablicy.  
- **Złożoność czasowa:**  
  - Zawsze: $ O(n^2) $  
- **Zastosowania:**  
  - Proste implementacje.  
  - Gdy liczba zamian elementów jest kluczowa (np. sortowanie na dyskach).  

### **2.4 Sortowanie szybkie (QuickSort)**  
- **Opis:** Wybiera element zwany pivotem, a następnie dzieli zbiór na dwie części – mniejsze i większe od pivota, po czym rekurencyjnie sortuje obie części.  
- **Złożoność czasowa:**  
  - Średnio: $ O(n \log n) $  
  - Najgorzej: $ O(n^2) $ (gdy pivot jest zawsze najgorszym możliwym wyborem)  
  - Najlepiej: $ O(n \log n) $  
- **Zastosowania:**  
  - Efektywne sortowanie dużych zbiorów danych.  
  - Algorytmy baz danych, kompresja danych.  

### **2.5 Sortowanie przez scalanie (Merge Sort)**  
- **Opis:** Dzieli tablicę na mniejsze części, sortuje je, a następnie scala w posortowaną całość.  
- **Złożoność czasowa:**  
  - Zawsze: $ O(n \log n) $  
- **Zastosowania:**  
  - Sortowanie dużych zbiorów na dyskach (z powodu stabilności).  
  - Algorytmy wymagające stabilnego sortowania.  

### **2.6 Sortowanie kubełkowe (Bucket Sort)**  
- **Opis:** Dzieli dane na przedziały (kubełki), sortuje je indywidualnie, a następnie scala.  
- **Złożoność czasowa:**  
  - Średnio: $ O(n + k) $, gdzie $ k $ to liczba kubełków  
- **Zastosowania:**  
  - Sortowanie liczb zmiennoprzecinkowych.  
  - Sortowanie dużych zbiorów o znanym rozkładzie wartości.  

---

## **Podsumowanie**  

| Algorytm           | Średnia złożoność | Najlepsza złożoność | Najgorsza złożoność | Stabilność | Zastosowanie |
|--------------------|-----------------|-----------------|-----------------|-----------|----------------|
| **Bubble Sort**    | $ O(n^2) $     | $ O(n) $      | $ O(n^2) $    | Tak       | Edukacja, małe zbiory |
| **Insertion Sort** | $ O(n^2) $     | $ O(n) $      | $ O(n^2) $    | Tak       | Małe, prawie posortowane zbiory |
| **Selection Sort** | $ O(n^2) $     | $ O(n^2) $    | $ O(n^2) $    | Nie       | Proste implementacje |
| **QuickSort**      | $ O(n \log n) $ | $ O(n \log n) $ | $ O(n^2) $ | Nie       | Duże zbiory, optymalizacja baz danych |
| **Merge Sort**     | $ O(n \log n) $ | $ O(n \log n) $ | $ O(n \log n) $ | Tak       | Algorytmy stabilne, sortowanie plików |
| **Bucket Sort**    | $ O(n + k) $   | $ O(n) $      | $ O(n^2) $    | Tak       | Liczby zmiennoprzecinkowe, duże zbiory |

Wybór algorytmu zależy od konkretnych wymagań – dla małych zbiorów sprawdzają się proste algorytmy jak **Insertion Sort**, natomiast dla dużych zbiorów najlepsze są **QuickSort** lub **Merge Sort**.