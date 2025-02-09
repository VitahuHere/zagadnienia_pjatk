### **Twierdzenie Bayesa**  

Twierdzenie Bayesa jest podstawową zasadą w teorii prawdopodobieństwa, która pozwala obliczać prawdopodobieństwo zdarzenia na podstawie wcześniejszej wiedzy o warunkach związanych z tym zdarzeniem.  

Matematycznie jest ono wyrażone jako:  

$
P(A | B) = \frac{P(B | A) P(A)}{P(B)}
$  

gdzie:  
- $ P(A | B) $ – prawdopodobieństwo zajścia zdarzenia $ A $ pod warunkiem, że zaszło zdarzenie $ B $ (prawdopodobieństwo warunkowe),  
- $ P(B | A) $ – prawdopodobieństwo zajścia $ B $, jeśli $ A $ jest prawdziwe,  
- $ P(A) $ – prawdopodobieństwo zajścia $ A $ (a priori),  
- $ P(B) $ – prawdopodobieństwo zajścia $ B $.  

---

### **Przykład – Diagnostyka medyczna**  

Załóżmy, że mamy test na pewną chorobę, który daje wynik pozytywny z prawdopodobieństwem 99% u osób chorych (czułość testu). Wiemy również, że test daje fałszywie pozytywny wynik w 5% przypadków u osób zdrowych. Załóżmy, że 0.1% populacji rzeczywiście choruje.  

**Obliczmy prawdopodobieństwo, że osoba z pozytywnym wynikiem testu rzeczywiście jest chora.**  

Dane:  
- $ P(A) = 0.001 $ (prawdopodobieństwo, że ktoś jest chory),  
- $ P(B | A) = 0.99 $ (prawdopodobieństwo pozytywnego testu, jeśli ktoś jest chory),  
- $ P(B | \neg A) = 0.05 $ (prawdopodobieństwo fałszywie pozytywnego testu, jeśli ktoś jest zdrowy),  
- $ P(\neg A) = 1 - P(A) = 0.999 $.  

Prawdopodobieństwo, że test jest pozytywny, wynosi:  

$
P(B) = P(B | A) P(A) + P(B | \neg A) P(\neg A)
$

$
P(B) = (0.99 \times 0.001) + (0.05 \times 0.999) = 0.00099 + 0.04995 = 0.05094
$

Teraz możemy obliczyć $ P(A | B) $:  

$
P(A | B) = \frac{P(B | A) P(A)}{P(B)} = \frac{0.99 \times 0.001}{0.05094} \approx 0.0194
$

Oznacza to, że mimo pozytywnego testu, rzeczywista szansa na chorobę wynosi tylko około **1.94%**!

---

### **Zastosowania Twierdzenia Bayesa**  

1. **Diagnostyka medyczna** – wykrywanie chorób na podstawie testów diagnostycznych (np. COVID-19, rak).  
2. **Filtry antyspamowe** – klasyfikacja e-maili jako spam lub nie-spam.  
3. **Rozpoznawanie mowy i obrazów** – algorytmy uczenia maszynowego do przetwarzania sygnałów dźwiękowych i obrazów.  
4. **Systemy rekomendacyjne** – przewidywanie preferencji użytkowników (np. Netflix, Amazon).  
5. **Sztuczna inteligencja** – metody Bayesowskie w uczeniu maszynowym, sieci Bayesowskie.  
6. **Analiza ryzyka** – ocena prawdopodobieństwa wystąpienia zdarzeń w finansach i ubezpieczeniach.  

Twierdzenie Bayesa jest więc niezwykle ważne w wielu dziedzinach, szczególnie w analizie danych i podejmowaniu decyzji na podstawie niepewnych informacji.