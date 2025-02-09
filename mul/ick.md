### **Zasady interakcji człowiek-komputer: heurystyki Nielsena-Molicha**  

Heurystyki użyteczności opracowane przez **Jakoba Nielsena i Rolfa Molicha** to zbiór 10 zasad projektowania interfejsów użytkownika. Stanowią one podstawę do oceny użyteczności systemów i aplikacji, pomagając identyfikować problemy z interakcją człowieka z komputerem.  

---

## **1. Widoczność statusu systemu (Visibility of System Status)**  
### 🔹 Opis  
System powinien zawsze informować użytkownika o swoim stanie poprzez **czytelne komunikaty zwrotne** w odpowiednim czasie.  

### ✅ Przykład dobrej praktyki  
- Po wysłaniu formularza użytkownik otrzymuje komunikat „Twoja wiadomość została wysłana.”  
- Podczas ładowania treści wyświetlany jest pasek postępu lub animacja.  

### ❌ Przykład złej praktyki  
- Użytkownik klika przycisk „Zapisz” i nic się nie dzieje – brak informacji zwrotnej.  

---

## **2. Zgodność systemu ze światem rzeczywistym (Match Between System and the Real World)**  
### 🔹 Opis  
Interfejs powinien używać **znanych metafor**, naturalnego języka i terminologii zrozumiałej dla użytkownika, zamiast technicznych określeń.  

### ✅ Przykład dobrej praktyki  
- Ikona 🗑️ (kosza na śmieci) zamiast tekstu „Usuń plik.”  
- Użycie jednostek „kg”, „cm” zamiast „float64.”  

### ❌ Przykład złej praktyki  
- Komunikat błędu: „Błąd 0xE1000021 – błąd alokacji pamięci.”  

---

## **3. Kontrola użytkownika i swoboda (User Control and Freedom)**  
### 🔹 Opis  
Użytkownik powinien mieć możliwość **łatwego cofania i poprawiania działań**, szczególnie w przypadku błędów.  

### ✅ Przykład dobrej praktyki  
- Przycisk „Cofnij” w edytorze tekstu.  
- Możliwość anulowania przypadkowego usunięcia pliku („Przywróć” w koszu).  

### ❌ Przykład złej praktyki  
- Brak opcji „Cofnij” po omyłkowym usunięciu ważnego dokumentu.  

---

## **4. Spójność i standardy (Consistency and Standards)**  
### 🔹 Opis  
Interfejs powinien być **spójny** – użytkownicy nie powinni się zastanawiać, czy różne słowa, ikony lub elementy oznaczają to samo.  

### ✅ Przykład dobrej praktyki  
- Stałe miejsce dla przycisku „Zaloguj się” w górnym prawym rogu strony.  
- Jednolite nazewnictwo (np. „Plik → Zapisz” w różnych aplikacjach).  

### ❌ Przykład złej praktyki  
- W jednym miejscu przycisk „Usuń”, a w innym „Kasuj” dla tej samej funkcji.  

---

## **5. Zapobieganie błędom (Error Prevention)**  
### 🔹 Opis  
System powinien **minimalizować ryzyko popełnienia błędów** poprzez odpowiednie mechanizmy ostrzegawcze i walidacje.  

### ✅ Przykład dobrej praktyki  
- Formularz nie pozwala wysłać wiadomości bez wypełnienia wymaganych pól.  
- Potwierdzenie przed usunięciem pliku: „Czy na pewno chcesz usunąć ten plik?”  

### ❌ Przykład złej praktyki  
- Brak ostrzeżenia przed zamknięciem aplikacji bez zapisania zmian.  

---

## **6. Rozpoznawanie zamiast przypominania (Recognition Rather Than Recall)**  
### 🔹 Opis  
Interfejs powinien ograniczać konieczność pamiętania informacji – użytkownik powinien mieć **widoczne opcje i podpowiedzi**.  

### ✅ Przykład dobrej praktyki  
- Lista ostatnio otwieranych dokumentów w edytorze tekstu.  
- Sugestie haseł i podpowiedzi w polach wyszukiwania.  

### ❌ Przykład złej praktyki  
- Wymaganie od użytkownika ręcznego wpisania kodu kategorii produktu zamiast wyboru z listy.  

---

## **7. Elastyczność i efektywność użytkowania (Flexibility and Efficiency of Use)**  
### 🔹 Opis  
System powinien oferować zarówno **opcje dla początkujących, jak i zaawansowanych użytkowników** (np. skróty klawiszowe).  

### ✅ Przykład dobrej praktyki  
- Skróty klawiaturowe (Ctrl + C, Ctrl + V) dla bardziej zaawansowanych użytkowników.  
- Możliwość dostosowania interfejsu (np. układ paneli w Photoshopie).  

### ❌ Przykład złej praktyki  
- Brak skrótów klawiaturowych w edytorze tekstu, zmuszający do klikania wszystkiego myszką.  

---

## **8. Estetyka i minimalizm (Aesthetic and Minimalist Design)**  
### 🔹 Opis  
Interfejs powinien unikać zbędnych elementów – **im mniej rozpraszających detali, tym łatwiej skupić się na treści.**  

### ✅ Przykład dobrej praktyki  
- Prosty, czytelny interfejs Gmaila.  
- Unikanie nadmiaru reklam i wyskakujących okienek.  

### ❌ Przykład złej praktyki  
- Strona główna aplikacji z mnóstwem przycisków, banerów i reklam.  

---

## **9. Pomoc w rozpoznawaniu, diagnozowaniu i naprawianiu błędów (Help Users Recognize, Diagnose, and Recover from Errors)**  
### 🔹 Opis  
Komunikaty błędów powinny być **czytelne, konkretne i oferować rozwiązania**.  

### ✅ Przykład dobrej praktyki  
- „Hasło jest nieprawidłowe. Spróbuj ponownie lub użyj opcji odzyskiwania hasła.”  

### ❌ Przykład złej praktyki  
- Komunikat „Błąd 404” bez żadnej wskazówki, co zrobić dalej.  

---

## **10. Pomoc i dokumentacja (Help and Documentation)**  
### 🔹 Opis  
System powinien oferować **łatwo dostępną pomoc** w razie problemów.  

### ✅ Przykład dobrej praktyki  
- Sekcja „Pomoc” w aplikacji z instrukcjami krok po kroku.  
- Możliwość kontaktu z pomocą techniczną.  

### ❌ Przykład złej praktyki  
- Brak instrukcji obsługi dla skomplikowanego narzędzia.  

---

## **Podsumowanie**  
Heurystyki Nielsena-Molicha pomagają projektować intuicyjne, efektywne i przyjazne użytkownikowi interfejsy. Stosowanie ich w procesie tworzenia interakcji człowiek-komputer pozwala unikać błędów UX i poprawia komfort korzystania z systemów.  

Jeśli chcesz ocenić użyteczność dowolnej aplikacji, **przeprowadzenie heurystycznej ewaluacji** w oparciu o te zasady może pomóc wykryć kluczowe problemy i usprawnić projekt. 🚀