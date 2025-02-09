# **Układy równań liniowych – metody rozwiązywania i liczba rozwiązań**  

## **1. Definicja układu równań liniowych**  
Układ równań liniowych składa się z równań postaci:  

$
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n = b_1
$

$
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n = b_2
$

$
\vdots
$

$
a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n = b_m
$

gdzie:
- $ a_{ij} $ to współczynniki macierzy współczynników,  
- $ x_1, x_2, \dots, x_n $ to niewiadome,  
- $ b_1, b_2, \dots, b_m $ to wyrazy wolne.  

## **2. Liczba rozwiązań układu równań**  
Układ równań liniowych może mieć:  

✅ **Jedno rozwiązanie** (układ oznaczony) – gdy macierz współczynników ma pełną rangę ($ \text{rang}(A) = n $).  

✅ **Brak rozwiązań** (układ sprzeczny) – gdy równania są ze sobą sprzeczne, np.:  
$
x + y = 2
$
$
x + y = 5
$
Dwa równania są równoległe i nie przecinają się.  

✅ **Nieskończenie wiele rozwiązań** (układ nieoznaczony) – gdy równania są liniowo zależne (np. jedno jest wielokrotnością drugiego).  

## **3. Metody rozwiązywania układów równań liniowych**  
W zależności od wielkości układu stosuje się różne metody:  

### **A) Metody algebraiczne (dla małych układów)**
1. **Metoda podstawiania**  
   - Wyznaczamy jedną niewiadomą z jednego równania,  
   - Podstawiamy do pozostałych równań, aż uzyskamy rozwiązania.  
   - **Przykład:**  
     $
     x + y = 5
     $
     $
     2x - y = 1
     $
     Z pierwszego: $ y = 5 - x $.  
     Podstawiamy do drugiego:  
     $
     2x - (5 - x) = 1 \Rightarrow 3x = 6 \Rightarrow x = 2
     $
     Podstawiamy $ x = 2 $ do $ y = 5 - x $, więc $ y = 3 $.  

2. **Metoda przeciwnych współczynników (eliminacji)**  
   - Przekształcamy układ tak, aby eliminować jedną zmienną przez dodawanie/różnicę równań.  
   - **Przykład:**  
     $
     3x + 2y = 5
     $
     $
     6x - 2y = 4
     $
     Dodajemy równania:
     $
     (3x + 2y) + (6x - 2y) = 5 + 4
     $
     $
     9x = 9 \Rightarrow x = 1
     $
     Podstawiamy $ x = 1 $ do pierwszego równania:
     $
     3(1) + 2y = 5 \Rightarrow 2y = 2 \Rightarrow y = 1
     $

### **B) Metody macierzowe (dla większych układów)**  
3. **Metoda macierzy odwrotnej**  
   Jeśli układ można zapisać w postaci $ AX = B $, gdzie:  
   $
   A =
   \begin{bmatrix}
   a_{11} & a_{12} \\
   a_{21} & a_{22}
   \end{bmatrix},
   \quad
   X =
   \begin{bmatrix}
   x_1 \\
   x_2
   \end{bmatrix},
   \quad
   B =
   \begin{bmatrix}
   b_1 \\
   b_2
   \end{bmatrix}
   $
   To rozwiązanie uzyskujemy jako:
   $
   X = A^{-1} B
   $
   gdzie $ A^{-1} $ to macierz odwrotna.  

4. **Metoda Cramera (dla układów kwadratowych)**  
   - Stosowana, gdy $ \det(A) \neq 0 $.  
   - Rozwiązania dane są wzorem:
     $
     x_i = \frac{\det(A_i)}{\det(A)}
     $
     gdzie $ A_i $ to macierz $ A $, w której $ i $-ta kolumna została zastąpiona wektorem $ B $.  

5. **Metoda eliminacji Gaussa**  
   - Polega na sprowadzeniu macierzy do postaci trójkątnej i rozwiązaniu przez podstawienie wsteczne.  

6. **Metoda Gaussa-Jordana**  
   - Ulepszona wersja eliminacji Gaussa, gdzie macierz doprowadza się do postaci jednostkowej.  

### **C) Metody numeryczne (dla bardzo dużych układów)**  
7. **Metoda iteracyjna Jacobiego**  
   - Przybliżeniowa metoda dla rzadkich układów równań, gdzie kolejne wartości niewiadomych są iteracyjnie poprawiane.  

8. **Metoda Gaussa-Seidela**  
   - Ulepszona metoda Jacobiego, szybciej zbieżna, ale wymaga specjalnych warunków dla zbieżności.  

---

## **Podsumowanie**  
✅ **Liczba rozwiązań:**  
- **Jedno rozwiązanie** – układ oznaczony.  
- **Brak rozwiązań** – układ sprzeczny.  
- **Nieskończenie wiele rozwiązań** – układ nieoznaczony.  

✅ **Metody rozwiązywania:**  
- **Podstawianie i przeciwnych współczynników** – dobre dla małych układów.  
- **Macierzowe (Cramer, odwrotność, Gauss, Gauss-Jordan)** – dla większych układów.  
- **Numeryczne (Jacobi, Gauss-Seidel)** – dla bardzo dużych układów w obliczeniach komputerowych.  

Jeśli masz konkretne równania do rozwiązania, mogę pomóc! 😊