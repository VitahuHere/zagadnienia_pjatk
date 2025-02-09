Relacyjne bazy danych są fundamentem wielu aplikacji i systemów, które przetwarzają dane. Oto ich kluczowe cechy:

1. **Model relacyjny:** Dane są przechowywane w tabelach, które składają się z wierszy (rekordów) i kolumn (atrybutów). Tabele są powiązane ze sobą relacjami, co umożliwia efektywne zarządzanie danymi i unikanie duplikatów.

2. **ACID:** Transakcje w relacyjnych bazach danych spełniają zasady ACID:
   - **Atomicity (niepodzielność):** Transakcja jest traktowana jako niepodzielna całość. Albo wszystkie operacje w transakcji są wykonane, albo żadna z nich.
   - **Consistency (spójność):** Transakcja zachowuje spójność danych, tzn. dane po transakcji nadal spełniają określone reguły.
   - **Isolation (izolacja):** Transakcje są odizolowane od siebie, tzn. jedna transakcja nie wpływa na drugą.
   - **Durability (trwałość):** Zmiany dokonane przez transakcję są trwałe i nie są tracone nawet w przypadku awarii systemu.

3. **Język SQL:** SQL (Structured Query Language) to standardowy język do komunikacji z relacyjnymi bazami danych. Umożliwia tworzenie tabel, wstawianie, aktualizowanie i usuwanie danych oraz wykonywanie zapytań.

4. **Klucze:**
   - **Klucz główny (primary key):** Unikalny identyfikator każdego rekordu w tabeli.
   - **Klucz obcy (foreign key):** Odwołuje się do klucza głównego w innej tabeli, tworząc relację między tabelami.

5. **Integralność danych:** Relacyjne bazy danych zapewniają integralność danych poprzez:
   - **Integralność encji:** Każdy rekord w tabeli musi mieć unikalny klucz główny.
   - **Integralność referencyjna:** Wartość klucza obcego musi istnieć w tabeli, do której się odwołuje.
   - **Ograniczenia (constraints):** Dodatkowe reguły, które określają, jakie dane mogą być przechowywane w tabeli (np. typ danych, zakres wartości).

6. **Normalizacja:** Proces projektowania bazy danych, który minimalizuje redundancję danych i poprawia ich spójność.

7. **Bezpieczeństwo:** Relacyjne bazy danych oferują mechanizmy kontroli dostępu, które umożliwiają ograniczenie uprawnień użytkowników do określonych danych.

8. **Skalowalność:** Relacyjne bazy danych mogą być skalowane w celu obsługi dużych ilości danych i dużej liczby użytkowników.

9. **Wydajność:** Relacyjne bazy danych oferują mechanizmy optymalizacji zapytań, które pozwalają na szybkie wyszukiwanie i przetwarzanie danych.

Relacyjne bazy danych są szeroko stosowane w różnych aplikacjach, takich jak systemy zarządzania relacjami z klientami (CRM), systemy ERP, aplikacje internetowe i wiele innych.
