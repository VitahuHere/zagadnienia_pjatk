**Zasada indukcji matematycznej** to metoda dowodzenia twierdzeń dotyczących liczb naturalnych. Polega na wykazaniu, że pewna własność $ P(n) $ jest prawdziwa dla wszystkich liczb naturalnych $ n $, począwszy od pewnej liczby początkowej (zwykle $ n = 1 $ lub $ n = 0 $).  

Indukcja matematyczna składa się z dwóch kroków:  

1. **Krok bazowy** – pokazujemy, że własność $ P(n) $ jest prawdziwa dla najmniejszej wartości $ n $ (np. $ P(1) $).  
2. **Krok indukcyjny** – zakładamy, że $ P(k) $ jest prawdziwe dla pewnej liczby naturalnej $ k $ (założenie indukcyjne), i na tej podstawie dowodzimy, że $ P(k+1) $ również jest prawdziwe.  

Jeśli oba kroki są spełnione, to na podstawie zasady indukcji matematycznej własność $ P(n) $ jest prawdziwa dla wszystkich $ n \geq n_0 $.  

### Przykład: suma pierwszych $ n $ liczb naturalnych  
Twierdzenie:  
$
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$  

#### Dowód indukcyjny:  
1. **Krok bazowy:** dla $ n = 1 $:  
   $
   1 = \frac{1(1+1)}{2} = 1
   $  
   Równość jest spełniona.  

2. **Krok indukcyjny:** zakładamy, że dla pewnego $ k $ obowiązuje:  
   $
   \sum_{i=1}^{k} i = \frac{k(k+1)}{2}
   $  
   Musimy wykazać, że własność ta jest prawdziwa dla $ k+1 $:  
   $
   \sum_{i=1}^{k+1} i = \sum_{i=1}^{k} i + (k+1)
   $  
   Podstawiając założenie indukcyjne:  
   $
   \frac{k(k+1)}{2} + (k+1)
   $  
   Wyłączamy $ (k+1) $ przed nawias:  
   $
   \frac{k(k+1) + 2(k+1)}{2} = \frac{(k+1)(k+2)}{2}
   $  
   Otrzymujemy wzór dla $ k+1 $, co kończy dowód.  

W ten sposób wykazaliśmy, że wzór jest prawdziwy dla wszystkich $ n \geq 1 $.