# **Podstawowe wzory całek nieoznaczonych**  

Całka nieoznaczona funkcji $ f(x) $ to zbiór wszystkich funkcji pierwotnych $ F(x) $, których pochodna daje $ f(x) $. Oznaczamy ją jako:

$
\int f(x) \, dx = F(x) + C
$

gdzie $ C $ to stała całkowania.  

## **1. Całki podstawowe**
$
\int a \, dx = ax + C
$

$
\int x^n \, dx = \frac{x^{n+1}}{n+1} + C, \quad n \neq -1
$

$
\int \frac{1}{x} \, dx = \ln |x| + C
$

$
\int e^x \, dx = e^x + C
$

$
\int a^x \, dx = \frac{a^x}{\ln a} + C, \quad a > 0, a \neq 1
$

$
\int \ln x \, dx = x \ln x - x + C
$

## **2. Całki funkcji trygonometrycznych**
$
\int \sin x \, dx = -\cos x + C
$

$
\int \cos x \, dx = \sin x + C
$

$
\int \tan x \, dx = -\ln |\cos x| + C
$

$
\int \cot x \, dx = \ln |\sin x| + C
$

$
\int \sec x \, dx = \ln |\sec x + \tan x| + C
$

$
\int \csc x \, dx = -\ln |\csc x + \cot x| + C
$

## **3. Całki funkcji hiperbolicznych**
$
\int \sinh x \, dx = \cosh x + C
$

$
\int \cosh x \, dx = \sinh x + C
$

$
\int \tanh x \, dx = \ln |\cosh x| + C
$

$
\int \coth x \, dx = \ln |\sinh x| + C
$

## **4. Całki odwrotności funkcji trygonometrycznych**
$
\int \frac{dx}{\sqrt{1 - x^2}} = \arcsin x + C
$

$
\int \frac{dx}{1 + x^2} = \arctan x + C
$

$
\int \frac{dx}{|x|\sqrt{x^2 - 1}} = \text{arcosh} \, x + C, \quad x > 1
$

## **5. Całki przez części**  
Jeśli $ u = f(x) $ i $ dv = g(x)dx $, to:

$
\int u \, dv = u v - \int v \, du
$

## **6. Całki przez podstawienie**  
Dla podstawienia $ t = g(x) $:

$
\int f(g(x)) g'(x) \, dx = \int f(t) \, dt
$

### **Zastosowania i techniki obliczania całek oznaczonych i nieoznaczonych**  

---

## **1. Zastosowania całek**
Całki znajdują szerokie zastosowanie w matematyce, fizyce, inżynierii i ekonomii.  

### **Całki nieoznaczone** $(int f(x) \, dx$)  
Służą do znajdowania funkcji pierwotnych oraz modelowania procesów dynamicznych.  
**Zastosowania:**  
- **Obliczanie prędkości i drogi** – jeśli znamy przyspieszenie $ a(t) $, to prędkość $ v(t) $ i położenie $ s(t) $ uzyskujemy przez całkowanie.  
- **Równania różniczkowe** – kluczowe w modelowaniu zjawisk fizycznych i ekonomicznych.  
- **Obliczenia w elektronice** – np. wyznaczanie ładunku elektrycznego $ q(t) $ ze wzoru $ i(t) = \frac{dq}{dt} $.  

### **Całki oznaczone** $(int_a^b f(x) \, dx$)  
Służą do obliczania wartości liczbowych (np. pola powierzchni, objętości, sumy).  
**Zastosowania:**  
- **Obliczanie pól pod wykresem funkcji** – np. pole pod wykresem prędkości daje przebyta drogę.  
- **Obliczanie objętości brył obrotowych** – metoda Pappusa, metoda walcowa.  
- **Średnie wartości funkcji** – np. średnia temperatura w czasie.  
- **Zastosowania w probabilistyce** – obliczanie wartości oczekiwanej i wariancji w teorii prawdopodobieństwa.  

---

## **2. Techniki obliczania całek**
W zależności od funkcji, stosuje się różne metody całkowania.

### **A) Techniki obliczania całek nieoznaczonych**  
1. **Całkowanie przez podstawienie** (metoda zamiany zmiennej)  
   - Jeśli $ I = \int f(g(x)) g'(x) \, dx $, to podstawiamy $ t = g(x) $, $ dt = g'(x)dx $, co upraszcza obliczenia.  
   - **Przykład:**  
     $
     \int 2x e^{x^2} \, dx
     $
     Podstawiamy $ t = x^2 $, wtedy $ dt = 2x \, dx $, co prowadzi do:
     $
     \int e^t \, dt = e^t + C = e^{x^2} + C
     $

2. **Całkowanie przez części** (dla iloczynu funkcji)  
   - Jeśli $ u = f(x) $, $ dv = g(x) dx $, to stosujemy wzór:  
     $
     \int u \, dv = u v - \int v \, du
     $
   - **Przykład:**  
     $
     \int x e^x \, dx
     $
     Wybieramy $ u = x $, $ dv = e^x dx $, wtedy $ du = dx $, $ v = e^x $, co daje:
     $
     \int x e^x \, dx = x e^x - \int e^x \, dx = x e^x - e^x + C
     $

3. **Rozkład na ułamki proste**  
   - Stosowane do całkowania funkcji wymiernych, np.  
     $
     \int \frac{1}{x^2 - 1} \, dx
     $
     Rozkładamy:  
     $
     \frac{1}{x^2 - 1} = \frac{A}{x - 1} + \frac{B}{x + 1}
     $
     Wyznaczamy $ A $ i $ B $, a następnie całkujemy.  

4. **Całkowanie funkcji trygonometrycznych**  
   - Stosuje się podstawienia trygonometryczne, np.  
     $
     \int \frac{dx}{\sqrt{1 - x^2}} = \arcsin x + C
     $

---

### **B) Techniki obliczania całek oznaczonych**  
1. **Metoda podstawienia**  
   - Podobna do podstawienia w całkach nieoznaczonych, ale trzeba pamiętać o zmianie granic.  

2. **Całkowanie przez części**  
   - Stosuje się do obliczania całek oznaczonych funkcji, które są iloczynem dwóch wyrażeń.  

3. **Całkowanie numeryczne** (dla funkcji, których nie można całkować analitycznie)  
   - **Metoda trapezów:**  
     Przybliżamy pole pod wykresem sumą trapezów:  
     $
     I \approx \sum_{i=1}^{n} \frac{f(x_i) + f(x_{i-1})}{2} \cdot \Delta x
     $
   - **Metoda Simpsona:**  
     Przybliża całkę parabolą zamiast trapezami, co daje lepszą dokładność.  

4. **Twierdzenie o wartości średniej dla całek oznaczonych**  
   - Jeśli $ f(x) $ jest ciągła na $ [a, b] $, to istnieje $ c \in (a, b) $ takie, że:
     $
     \int_a^b f(x) \, dx = f(c)(b - a)
     $

5. **Obliczanie pól i objętości**  
   - **Pole między dwiema funkcjami:**  
     $
     A = \int_a^b (f(x) - g(x)) \, dx
     $
   - **Objętość bryły obrotowej (metoda dysków):**  
     $
     V = \pi \int_a^b [f(x)]^2 \, dx
     $

---

## **Podsumowanie**  
### **Całki nieoznaczone**  
🔹 Pozwalają znaleźć funkcję pierwotną.  
🔹 Stosuje się metody: **podstawienia, części, ułamków prostych**.  
🔹 Zastosowania: kinematyka, ekonomia, elektronika.  

### **Całki oznaczone**  
🔹 Dają konkretną wartość liczbową.  
🔹 Stosuje się **podstawienie, numeryczne metody, części**.  
🔹 Zastosowania: pola, objętości, probabilistyka.  
