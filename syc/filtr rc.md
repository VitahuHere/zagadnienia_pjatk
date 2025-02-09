### **Filtr dolnoprzepustowy RC – częstotliwość graniczna i pasmo przenoszenia**  

#### **Filtr dolnoprzepustowy RC**  
Filtr dolnoprzepustowy RC to układ elektroniczny składający się z rezystora (**R**) i kondensatora (**C**), którego zadaniem jest **przepuszczanie sygnałów o niskich częstotliwościach** i **tłumienie sygnałów o częstotliwościach wyższych** od określonej wartości.  

W najprostszym układzie filtr ten może być zrealizowany jako:  
- **Filtr pierwszego rzędu** – zawierający pojedynczy rezystor i kondensator.  
- **Filtr pasywny** – ponieważ nie zawiera elementów aktywnych, takich jak tranzystory czy wzmacniacze operacyjne.  

#### **Częstotliwość graniczna ($ f_c $)**  
Częstotliwość graniczna to wartość częstotliwości, przy której sygnał wyjściowy filtru zostaje **stłumiony do poziomu 70,7% wartości początkowej** (czyli o **-3 dB** w stosunku do amplitudy maksymalnej). Dla filtru RC pierwszego rzędu częstotliwość graniczna wyrażona jest wzorem:  

$
f_c = \frac{1}{2\pi RC}
$

Gdzie:  
- $ R $ – wartość rezystancji w omach [Ω],  
- $ C $ – pojemność kondensatora w faradach [F],  
- $ \pi $ – stała matematyczna (≈ 3,1416).  

Powyższy wzór pokazuje, że im większa wartość rezystancji i pojemności, tym niższa częstotliwość graniczna, co oznacza, że filtr będzie tłumił wyższe częstotliwości bardziej efektywnie.  

#### **Pasmo przenoszenia filtru**  
Pasmo przenoszenia to zakres częstotliwości, dla którego sygnał przechodzi przez filtr **bez znacznego tłumienia**. Dla filtru dolnoprzepustowego RC pasmo przenoszenia obejmuje **wszystkie częstotliwości niższe od częstotliwości granicznej** ($ f_c $).  

W praktyce oznacza to, że sygnały o częstotliwościach **mniejszych niż $ f_c $** przechodzą niemal bez zmian, natomiast sygnały o częstotliwościach wyższych od $ f_c $ są stopniowo tłumione (ze spadkiem $ -20 $ dB na dekadę dla filtru pierwszego rzędu).  

### **Podsumowanie**  
- **Częstotliwość graniczna** to wartość częstotliwości, przy której sygnał jest tłumiony do 70,7% swojej początkowej wartości.  
- **Pasmo przenoszenia** filtru dolnoprzepustowego RC obejmuje zakres częstotliwości niższych od częstotliwości granicznej.  
- Filtr RC znajduje zastosowanie w eliminacji zakłóceń wysokoczęstotliwościowych, wygładzaniu sygnałów i w systemach audio.