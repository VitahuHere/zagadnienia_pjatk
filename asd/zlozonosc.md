Złożoność algorytmów to miara ilości zasobów (czasu i pamięci) potrzebnych do wykonania algorytmu w zależności od rozmiaru danych wejściowych. Szacowanie złożoności algorytmów jest kluczowe dla wyboru najefektywniejszego algorytmu do rozwiązania danego problemu.

## Sposoby szacowania złożoności algorytmów

1. **Analiza liczby operacji dominujących:**
   - Skupiamy się na operacjach, które są wykonywane najczęściej w algorytmie.
   - Określamy, jak liczba tych operacji rośnie wraz ze wzrostem rozmiaru danych wejściowych (n).
   - Ignorujemy stałe współczynniki i mniej znaczące operacje.

2. **Notacja Big O:**
   - Używamy notacji Big O do opisywania asymptotycznej złożoności algorytmu.
   - Notacja Big O określa górne ograniczenie na wzrost funkcji złożoności.
   - Przykłady: O(1) - złożoność stała, O(log n) - logarytmiczna, O(n) - liniowa, O(n log n) - liniowo-logarytmiczna, O(n^2) - kwadratowa, O(2^n) - wykładnicza.

3. **Analiza przypadków:**
   - Rozważamy różne przypadki danych wejściowych:
     - Przypadek pesymistyczny: Najgorszy możliwy przypadek, w którym algorytm działa najdłużej.
     - Przypadek średni: Uśredniony czas działania algorytmu dla różnych danych wejściowych.
     - Przypadek optymistyczny: Najlepszy możliwy przypadek, w którym algorytm działa najkrócej.

## Klasy złożoności problemów algorytmicznych

Problemy algorytmiczne można podzielić na klasy złożoności w zależności od zasobów potrzebnych do ich rozwiązania:

1. **Klasa P:** Problemy, które można rozwiązać w czasie wielomianowym (np. O(n), O(n^2), O(n^3)). Są to problemy "łatwe" do rozwiązania.

2. **Klasa NP:** Problemy, dla których istnieje algorytm weryfikujący rozwiązanie w czasie wielomianowym. Nie wiadomo, czy problemy te można rozwiązać w czasie wielomianowym (czy P = NP?). Wiele ważnych problemów praktycznych należy do tej klasy.

3. **Klasa NP-trudne:** Problemy co najmniej tak trudne, jak najtrudniejsze problemy w klasie NP. Jeśli udałoby się rozwiązać którykolwiek problem NP-trudny w czasie wielomianowym, to wszystkie problemy z klasy NP również można by rozwiązać w czasie wielomianowym.

4. **Klasa NP-zupełne:** Problemy, które należą zarówno do klasy NP, jak i do klasy NP-trudnych. Są to "najtrudniejsze" problemy w klasie NP.

## Znaczenie szacowania złożoności algorytmów

- **Wybór optymalnego algorytmu:** Pozwala na porównanie różnych algorytmów i wybór tego, który jest najbardziej efektywny dla danego problemu.
- **Przewidywanie czasu działania algorytmu:** Umożliwia oszacowanie, jak długo będzie działał algorytm dla danych wejściowych o określonym rozmiarze.
- **Projektowanie efektywnych algorytmów:** Pomaga w projektowaniu algorytmów, które minimalizują zużycie zasobów (czasu i pamięci).
- **Zrozumienie granic możliwości obliczeniowych:** Pozwala na zrozumienie, które problemy są "łatwe" do rozwiązania, a które są "trudne" lub wręcz niemożliwe do rozwiązania w rozsądnym czasie.

Szacowanie złożoności algorytmów i klasyfikacja problemów algorytmicznych to ważne narzędzia w informatyce, które pozwalają na tworzenie efektywnych i skalowalnych rozwiązań problemów.

## Przykład szacowania złożoności algorytmu

Rozważmy problem wyszukiwania elementu w posortowanej tablicy. Mamy tablicę `A` o rozmiarze `n` i chcemy znaleźć indeks elementu `x` w tej tablicy.

### Algorytm liniowy

Najprostszy algorytm to przeszukanie liniowe, które polega na przeglądaniu kolejnych elementów tablicy i porównywaniu ich z `x`.

```python
def szukaj_liniowo(A, x):
  for i in range(len(A)):
    if A[i] == x:
      return i
  return -1 # element nie znaleziony
```

W najgorszym przypadku (gdy `x` jest ostatnim elementem w tablicy lub nie występuje wcale), algorytm ten będzie musiał porównać `x` z każdym elementem tablicy. Zatem liczba operacji dominujących (porównań) będzie równa `n`.

Złożoność czasowa tego algorytmu wynosi **O(n)**, czyli jest liniowa.

### Algorytm binarny

Ponieważ tablica jest posortowana, możemy zastosować algorytm binarny, który jest znacznie szybszy. Algorytm ten polega na dzieleniu tablicy na pół w każdym kroku i porównywaniu `x` z środkowym elementem. Jeśli `x` jest mniejszy od środkowego elementu, to szukamy go w lewej połowie tablicy, a jeśli jest większy, to w prawej połowie.

```python
def szukaj_binarnie(A, x):
  lewy = 0
  prawy = len(A) - 1
  while lewy <= prawy:
    srodek = (lewy + prawy) // 2
    if A[srodek] == x:
      return srodek
    elif A[srodek] < x:
      lewy = srodek + 1
    else:
      prawy = srodek - 1
  return -1 # element nie znaleziony
```

W najgorszym przypadku algorytm binarny będzie musiał podzielić tablicę na pół logarytmicznie wiele razy, zanim znajdzie element `x` lub stwierdzi, że go nie ma. Zatem liczba operacji dominujących (porównań) będzie równa **log₂(n)**.

Złożoność czasowa tego algorytmu wynosi **O(log n)**, czyli jest logarytmiczna.

### Porównanie

Jak widać, algorytm binarny jest znacznie szybszy od algorytmu liniowego, zwłaszcza dla dużych tablic. Na przykład, dla tablicy o rozmiarze 1000 elementów, algorytm liniowy w najgorszym przypadku wykona 1000 porównań, a algorytm binarny tylko około 10 porównań.

### Podsumowanie

Szacowanie złożoności algorytmów pozwala na porównywanie różnych algorytmów i wybór tego, który jest najbardziej efektywny dla danego problemu. W tym przypadku algorytm binarny jest znacznie lepszy od algorytmu liniowego dla posortowanych tablic.
