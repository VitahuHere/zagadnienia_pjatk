# **Grafy – typy i metody reprezentacji**  

## **1. Definicja grafu**  
Graf to struktura matematyczna składająca się z **wierzchołków** (ang. *vertices*, oznaczanych jako $ V $) oraz **krawędzi** (ang. *edges*, oznaczanych jako $ E $), które łączą pary wierzchołków. Graf zapisujemy jako:  

$
G = (V, E)
$

gdzie:  
- $ V $ – zbiór wierzchołków,  
- $ E $ – zbiór krawędzi.  

---

## **2. Typy grafów**  

### **A) Ze względu na rodzaj krawędzi**  
1. **Graf nieskierowany** – krawędzie nie mają kierunku, czyli jeśli istnieje krawędź $ (u, v) $, to można przejść z $ u $ do $ v $ i odwrotnie.  
2. **Graf skierowany (digraf)** – krawędzie mają kierunek, zapisane jako $ (u, v) $, oznaczają przejście tylko od $ u $ do $ v $.  

### **B) Ze względu na wagę krawędzi**  
3. **Graf ważony** – każda krawędź ma przypisaną wagę (np. koszt, odległość, czas).  
4. **Graf nieważony** – wszystkie krawędzie są równoważne, bez dodatkowych wartości.  

### **C) Ze względu na liczbę krawędzi**  
5. **Graf rzadki** – liczba krawędzi jest niewielka względem liczby wierzchołków ($ |E| \approx |V| $).  
6. **Graf gęsty** – liczba krawędzi jest bliska maksymalnej możliwej liczby krawędzi ($ |E| \approx |V|^2 $).  

### **D) Ze względu na strukturę**  
7. **Graf spójny** – istnieje ścieżka między każdą parą wierzchołków.  
8. **Graf niespójny** – istnieją wierzchołki, między którymi nie ma ścieżki.  
9. **Drzewo** – graf acykliczny (bez cykli), w którym każdy wierzchołek jest osiągalny z dowolnego innego.  
10. **Graf cykliczny** – zawiera co najmniej jeden cykl.  

### **E) Specjalne rodzaje grafów**  
11. **Graf pełny** – każdy wierzchołek jest połączony z każdym innym.  
12. **Graf dwudzielny** – zbiór wierzchołków można podzielić na dwie grupy, takie że krawędzie istnieją tylko między grupami (np. relacja uczniowie – nauczyciele).  

---

## **3. Reprezentacje grafów**  

### **A) Macierz sąsiedztwa**  
Macierz $ A $ rozmiaru $ |V| \times |V| $, gdzie:  
- $ A[i][j] = 1 $, jeśli istnieje krawędź $ (i, j) $  
- $ A[i][j] = 0 $, jeśli krawędzi nie ma  

**Przykład dla grafu nieskierowanego:**  

$
G =
\begin{array}{c|ccc}
 & A & B & C \\
\hline
A & 0 & 1 & 1 \\
B & 1 & 0 & 1 \\
C & 1 & 1 & 0 \\
\end{array}
$

✅ **Zalety:** szybkie sprawdzanie, czy istnieje krawędź $ O(1) $  
❌ **Wady:** zajmuje $ O(|V|^2) $ pamięci  

---

### **B) Lista sąsiedztwa**  
Lista, w której każdy wierzchołek przechowuje listę sąsiadów.  

**Przykład:**  
$
A: B, C  
B: A, C  
C: A, B  
$

✅ **Zalety:** oszczędność pamięci dla grafów rzadkich $ O(|V| + |E|) $  
❌ **Wady:** wolniejsze sprawdzanie obecności krawędzi $ O(\deg(V)) $  

---

### **C) Lista krawędzi**  
Zbiór par $ (u, v) $, np.:  

$
E = \{ (A, B), (A, C), (B, C) \}
$

✅ **Zalety:** kompaktowe dla małych grafów  
❌ **Wady:** wymaga przeszukiwania dla sprawdzenia krawędzi  

---

## **4. Wybór metody reprezentacji**  
✅ **Macierz sąsiedztwa** – dla gęstych grafów, szybkie sprawdzanie krawędzi  
✅ **Lista sąsiedztwa** – dla rzadkich grafów, oszczędność pamięci  
✅ **Lista krawędzi** – gdy potrzebujemy iterować po wszystkich krawędziach  

Chcesz zobaczyć implementację w Pythonie? 😊