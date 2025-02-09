### **Wielomian Taylora i szereg Taylora funkcji rzeczywistej**  

#### **1. Wielomian Taylora**  
Wielomian Taylora funkcji $ f(x) $ to przybliżenie tej funkcji za pomocą wielomianu wokół punktu $ x_0 $. Jest on skonstruowany tak, aby wartość funkcji oraz jej pochodne w punkcie $ x_0 $ były zgodne z wartościami odpowiadających pochodnych funkcji rzeczywistej.

Wielomian Taylora stopnia $ n $ w rozwinięciu funkcji $ f(x) $ wokół punktu $ x_0 $ ma postać:
$
P_n(x) = f(x_0) + f'(x_0)(x - x_0) + \frac{f''(x_0)}{2!} (x - x_0)^2 + \dots + \frac{f^{(n)}(x_0)}{n!} (x - x_0)^n
$
gdzie $f^{(k)}(x_0)$ oznacza $ k $-tą pochodną funkcji $ f(x) $ obliczoną w punkcie $ x_0 $.

#### **2. Szereg Taylora**  
Szereg Taylora to nieskończone rozwinięcie funkcji w szereg potęgowy, którego suma dąży do wartości funkcji w otoczeniu punktu $ x_0 $, pod warunkiem, że szereg ten jest zbieżny. Szereg Taylora funkcji $ f(x) $ wokół punktu $ x_0 $ zapisujemy jako:

$
f(x) = \sum_{k=0}^{\infty} \frac{f^{(k)}(x_0)}{k!} (x - x_0)^k
$

Jeśli rozwinięcie odbywa się wokół punktu $ x_0 = 0 $, to taki szereg nazywamy **szeregiem Maclaurina**:

$
f(x) = \sum_{k=0}^{\infty} \frac{f^{(k)}(0)}{k!} x^k
$

#### **3. Przykład rozwinięcia funkcji w szereg Taylora**  
Rozważmy funkcję $ f(x) = e^x $. Wszystkie jej pochodne wynoszą $ f^{(k)}(x) = e^x $, więc w punkcie $ x_0 = 0 $ mamy $ f^{(k)}(0) = 1 $. Szereg Maclaurina dla tej funkcji to:

$
e^x = \sum_{k=0}^{\infty} \frac{x^k}{k!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \dots
$

Szereg Taylora pozwala na przybliżenie funkcji rzeczywistych za pomocą wielomianów, co ma zastosowanie m.in. w analizie numerycznej, fizyce i ekonomii.