### **Popularne interfejsy komunikacyjne w mikrokontrolerach**  

Mikrokontrolery wykorzystują różne interfejsy komunikacyjne do wymiany danych z innymi urządzeniami, takimi jak czujniki, pamięci, wyświetlacze czy moduły komunikacyjne. Można je podzielić na interfejsy **szeregowe** i **równoległe**, przy czym te pierwsze są częściej stosowane ze względu na prostsze okablowanie i mniejsze zapotrzebowanie na piny.  

---

### **1. Interfejsy szeregowe**  
Są powszechnie stosowane ze względu na oszczędność linii transmisyjnych i możliwość komunikacji na większe odległości.  

#### **1.1. UART (Universal Asynchronous Receiver-Transmitter)**  
- **Typ**: Asynchroniczny  
- **Liczba linii**: 2 (TX – nadajnik, RX – odbiornik)  
- **Sposób działania**: Brak sygnału zegarowego, dane przesyłane są w postaci ramek (start bit, dane, bit parzystości, stop bit).  
- **Zastosowanie**: Moduły komunikacyjne (np. Bluetooth, GPS), debugowanie, komunikacja między mikrokontrolerami.  

#### **1.2. SPI (Serial Peripheral Interface)**  
- **Typ**: Synchroniczny, pełnodupleksowy  
- **Liczba linii**: 4 (MOSI – dane do urządzenia, MISO – dane od urządzenia, SCK – zegar, SS/CS – wybór urządzenia)  
- **Sposób działania**: Master generuje sygnał zegarowy i steruje transmisją, urządzenia Slave odbierają i wysyłają dane.  
- **Zastosowanie**: Karty pamięci SD, wyświetlacze, przetworniki ADC/DAC, szybka wymiana danych.  

#### **1.3. I²C (Inter-Integrated Circuit)**  
- **Typ**: Synchroniczny, półdupleksowy  
- **Liczba linii**: 2 (SDA – dane, SCL – zegar)  
- **Sposób działania**: Magistrala wielourządzeniowa, jedno urządzenie Master może komunikować się z wieloma Slave. Adresacja urządzeń umożliwia ich identyfikację.  
- **Zastosowanie**: Czujniki, EEPROM, zegary RTC, interfejsy z układami peryferyjnymi.  

#### **1.4. CAN (Controller Area Network)**  
- **Typ**: Synchroniczny, wielopunktowy  
- **Liczba linii**: 2 (CAN_H, CAN_L)  
- **Sposób działania**: Ramki danych przesyłane w sieci wielu urządzeń, odporne na zakłócenia, system priorytetów wiadomości.  
- **Zastosowanie**: Motoryzacja (ECU, ABS), automatyka przemysłowa, robotyka.  

#### **1.5. USB (Universal Serial Bus)**  
- **Typ**: Synchroniczny, pełnodupleksowy  
- **Liczba linii**: 4 (VCC, GND, D+, D-)  
- **Sposób działania**: Magistrala host-device, umożliwia szybki transfer danych i zasilanie urządzeń.  
- **Zastosowanie**: Połączenie mikrokontrolera z komputerem, pamięci USB, urządzenia HID (klawiatury, myszki).  

#### **1.6. 1-Wire**  
- **Typ**: Asynchroniczny, jednoliniowy  
- **Liczba linii**: 1 (+ masa)  
- **Sposób działania**: Komunikacja przez jedną linię danych, każde urządzenie ma unikalny adres.  
- **Zastosowanie**: Czujniki temperatury (np. DS18B20), identyfikatory elektroniczne.  

---

### **2. Interfejsy równoległe**  
Wymagają większej liczby przewodów, ale umożliwiają szybszą transmisję danych.  

#### **2.1. GPIO (General Purpose Input/Output)**  
- **Sposób działania**: Proste linie wejścia/wyjścia sterujące stanami logicznymi.  
- **Zastosowanie**: Sterowanie diodami LED, przyciskami, przekaźnikami.  

#### **2.2. Interfejs równoległy (Parallel Bus, np. 8080, 6800)**  
- **Sposób działania**: Dane przesyłane wielobitowo (8-, 16-, 32-bitowe magistrale).  
- **Zastosowanie**: Wyświetlacze LCD TFT, szybkie transfery danych w układach pamięci.  

---

### **Podsumowanie**  
Wybór interfejsu zależy od **zastosowania** i **wymagań projektowych**.  
- **Do komunikacji z komputerem**: USB, UART  
- **Do czujników i pamięci**: I²C, SPI, 1-Wire  
- **Do aplikacji motoryzacyjnych i przemysłowych**: CAN  
- **Do szybkiego przesyłu danych**: SPI, równoległy interfejs danych  

Każdy z interfejsów ma swoje **zalety i ograniczenia**, dlatego dobór odpowiedniego rozwiązania powinien uwzględniać **przepustowość, liczbę przewodów i odporność na zakłócenia**.