# **Algorytmy rekurencyjne vs algorytmy iteracyjne – porównanie i omówienie**  

Algorytmy można implementować na dwa sposoby: **rekurencyjnie** i **iteracyjnie**. Wybór odpowiedniego podejścia zależy od problemu oraz dostępnych zasobów obliczeniowych.  

---

## **1. Algorytmy rekurencyjne**  

### **Definicja**  
Rekurencja to technika, w której funkcja wywołuje samą siebie z mniejszymi podproblemami, aż do osiągnięcia warunku zakończenia.  

### **Podstawowe założenia**  
- **Warunek stopu** – konieczny, aby uniknąć nieskończonego wywoływania funkcji.  
- **Podział problemu** – duży problem jest dzielony na mniejsze instancje tego samego problemu.  
- **Zasobochłonność** – każde wywołanie funkcji zajmuje dodatkową pamięć na stosie.  

### **Przykład – silnia (\( n! \))**
```python
def silnia(n):
    if n == 0:
        return 1
    return n * silnia(n - 1)

print(silnia(5))  # Wynik: 120
```

### **Zalety rekurencji**  
✔ Elegancka, czytelna i naturalna dla problemów podzielnych na mniejsze podproblemy.  
✔ Ułatwia implementację algorytmów takich jak przeszukiwanie drzew czy algorytmy podziału (np. QuickSort, MergeSort).  

### **Wady rekurencji**  
✖ Zajmuje więcej pamięci (stos rekurencyjny).  
✖ Może prowadzić do przepełnienia stosu (Stack Overflow) dla dużych wartości wejściowych.  
✖ Czasami mniej efektywna niż iteracja (np. przy wielokrotnym powtarzaniu tych samych obliczeń – rozwiązanie: programowanie dynamiczne).  

---

## **2. Algorytmy iteracyjne**  

### **Definicja**  
Iteracja to proces powtarzania zestawu instrukcji przy użyciu pętli (**for, while**) zamiast wywołań rekurencyjnych.  

### **Podstawowe założenia**  
- **Korzystanie z pętli** – powtarzanie operacji bez dodatkowych wywołań funkcji.  
- **Brak przepełnienia stosu** – zmienne są przechowywane w pamięci operacyjnej zamiast na stosie wywołań.  
- **Efektywność pamięciowa** – nie wymaga dodatkowego miejsca na stosie.  

### **Przykład – silnia (\( n! \)) w wersji iteracyjnej**
```python
def silnia_iter(n):
    wynik = 1
    for i in range(2, n + 1):
        wynik *= i
    return wynik

print(silnia_iter(5))  # Wynik: 120
```

### **Zalety iteracji**  
✔ Zwykle bardziej efektywna pod względem zużycia pamięci.  
✔ Mniejsze ryzyko przepełnienia stosu.  
✔ Łatwiejsza do debugowania, ponieważ nie ma zagnieżdżonych wywołań funkcji.  

### **Wady iteracji**  
✖ Czasami mniej intuicyjna i trudniejsza do implementacji dla problemów naturalnie rekurencyjnych (np. drzewa, algorytmy podziałowe).  
✖ W niektórych przypadkach mniej czytelna niż podejście rekurencyjne.  

---

## **3. Porównanie rekurencji i iteracji**  

| **Kryterium**         | **Rekurencja**                               | **Iteracja**                              |
|-----------------------|---------------------------------------------|------------------------------------------|
| **Definicja**        | Funkcja wywołuje samą siebie                | Użycie pętli do powtarzania operacji    |
| **Warunek stopu**    | Tak (w przeciwnym razie Stack Overflow)      | Pętla kończy się przy spełnionym warunku |
| **Wydajność**        | Może być mniej wydajna (zależy od problemu) | Zazwyczaj bardziej wydajna pamięciowo   |
| **Złożoność pamięciowa** | Większe użycie stosu wywołań            | Mniejsze zużycie pamięci                |
| **Czytelność kodu**  | Czytelniejsza dla problemów podzielnych     | Może być mniej intuicyjna               |
| **Przykłady użycia** | Drzewa, algorytmy podziałowe (QuickSort, DFS) | Sortowanie, operacje matematyczne       |

---

## **4. Kiedy stosować rekurencję, a kiedy iterację?**  

🔹 **Użyj rekurencji, gdy:**  
✅ Problem można podzielić na mniejsze podproblemy tego samego typu (np. drzewa, algorytmy podziałowe).  
✅ Algorytm jest naturalnie rekurencyjny (np. DFS w grafach, QuickSort, MergeSort).  
✅ Liczba wywołań nie jest zbyt duża (uniknięcie Stack Overflow).  

🔹 **Użyj iteracji, gdy:**  
✅ Potrzebna jest optymalizacja pamięciowa i czasowa.  
✅ Problem można rozwiązać pętlą bez potrzeby dzielenia na podproblemy.  
✅ Potrzebujemy większej kontroli nad przebiegiem algorytmu.  

---

## **Podsumowanie**  

- **Rekurencja** jest bardziej elegancka i intuicyjna dla problemów podzielnych na mniejsze części, ale może prowadzić do nadmiernego użycia pamięci.  
- **Iteracja** jest bardziej efektywna, ale może być mniej czytelna dla problemów rekurencyjnych.  

W praktyce często **rekurencyjne algorytmy optymalizuje się poprzez zamianę na iteracyjne**, np. użycie stosu zamiast wywołań rekurencyjnych (rekurencja ogonowa, programowanie dynamiczne).