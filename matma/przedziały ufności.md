Przedział ufności to zakres wartości, który z określonym prawdopodobieństwem zawiera nieznany parametr populacji. Innymi słowy, jest to oszacowanie przedziałowe, które pozwala nam określić, z jaką pewnością prawdziwa wartość parametru populacji znajduje się wewnątrz tego przedziału.

## Jak obliczyć przedział ufności?

1. **Ustal wielkość próby (n)**: Im większa próba, tym mniejszy błąd standardowy i węższy przedział ufności.
2. **Znajdź średnią wartość swojej próbki (x̄)**: Jest to punkt centralny przedziału ufności.
3. **Wyznacz odchylenie standardowe próby (s)**: Mierzy ono rozproszenie danych w próbie.
4. **Wybierz poziom ufności (1-α)**: Najczęściej stosuje się 95% (0,95), co oznacza, że istnieje 95% szans, że prawdziwy parametr populacji znajduje się w przedziale.
5. **Znajdź wartość krytyczną (z lub t)**: Zależy to od rozkładu i wielkości próby. Dla dużych prób (n > 30) zazwyczaj stosuje się rozkład normalny (z). Dla małych prób stosuje się rozkład t-Studenta.
6. **Oblicz błąd standardowy (SE)**: SE = s / √n
7. **Oblicz margines błędu (ME)**: ME = wartość krytyczna * SE
8. **Wyznacz przedział ufności**: (x̄ - ME, x̄ + ME)

## Interpretacja przedziału ufności

Przedział ufności (np. 95%) oznacza, że jeśli wielokrotnie pobieralibyśmy próby i obliczali dla nich przedziały ufności, to 95% z tych przedziałów zawierałoby prawdziwy parametr populacji.

## Przykład

Chcemy oszacować średni wzrost Polaków. Pobieramy próbę 100 osób i obliczamy średni wzrost w próbie (x̄ = 175 cm) oraz odchylenie standardowe (s = 10 cm). Wybieramy poziom ufności 95%.

1. **Wielkość próby**: n = 100
2. **Średnia z próby**: x̄ = 175 cm
3. **Odchylenie standardowe**: s = 10 cm
4. **Poziom ufności**: 1-α = 0,95
5. **Wartość krytyczna**: z = 1,96 (dla rozkładu normalnego i 95% ufności)
6. **Błąd standardowy**: SE = 10 / √100 = 1 cm
7. **Margines błędu**: ME = 1,96 * 1 = 1,96 cm
8. **Przedział ufności**: (175 - 1,96; 175 + 1,96) = (173,04; 176,96)

Możemy więc powiedzieć, że z 95% pewnością średni wzrost Polaków mieści się w przedziale od 173,04 cm do 176,96 cm.

## Dodatkowe informacje

* Przedziały ufności mogą być jednostronne (górny lub dolny).
* Szerokość przedziału ufności zależy od wielkości próby, poziomu ufności i odchylenia standardowego.
* Im węższy przedział ufności, tym dokładniejsze oszacowanie.

Mam nadzieję, że to wyjaśnienie jest pomocne. Jeśli masz jakieś pytania, nie wahaj się pytać.
