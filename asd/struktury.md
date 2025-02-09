## Charakterystyka i zastosowania podstawowych struktur danych

Oto charakterystyka i zastosowania podstawowych struktur danych: stos, kolejka, kolejka priorytetowa, struktura Find-Union i słownik.

## 1. Stos (Stack)

*   **Charakterystyka**:*
    *   LIFO (Last In, First Out) - ostatni element dodany do stosu jest pierwszym elementem pobranym.
    *   Operacje:
        *   push(element) - dodaje element na wierzch stosu.
        *   pop() - usuwa i zwraca element z wierzchu stosu.
        *   peek() lub top() - zwraca element z wierzchu stosu, nie usuwając go.
        *   isEmpty() - sprawdza, czy stos jest pusty.
*   **Zastosowania**:*
    *   Przechowywanie historii przeglądania stron internetowych (przycisk "wstecz").
    *   Wywoływanie funkcji w programowaniu (stos wywołań).
    *   Wyrównywanie nawiasów w wyrażeniach algebraicznych lub kodzie programistycznym.
    *   Implementacja algorytmów, takich jak przeszukiwanie w głąb (DFS).

## 2. Kolejka (Queue)

*   **Charakterystyka**:*
    *   FIFO (First In, First Out) - pierwszy element dodany do kolejki jest pierwszym elementem pobranym.
    *   Operacje:
        *   enqueue(element) - dodaje element na koniec kolejki.
        *   dequeue() - usuwa i zwraca element z początku kolejki.
        *   peek() lub front() - zwraca element z początku kolejki, nie usuwając go.
        *   isEmpty() - sprawdza, czy kolejka jest pusta.
*   **Zastosowania**:*
    *   Obsługa zadań w systemach operacyjnych (kolejka procesów).
    *   Buforowanie danych w komunikacji sieciowej.
    *   Przeszukiwanie wszerz (BFS) w grafach.
    *   Symulacje (np. kolejka klientów w sklepie).

## 3. Kolejka priorytetowa (Priority Queue)

*   **Charakterystyka**:*
    *   Elementy mają przypisane priorytety.
    *   Element o najwyższym priorytecie jest pobierany jako pierwszy.
    *   Operacje:
        *   insert(element, priorytet) - dodaje element z określonym priorytetem.
        *   removeMin() lub removeMax() - usuwa i zwraca element z najniższym lub najwyższym priorytetem.
        *   peekMin() lub peekMax() - zwraca element z najniższym lub najwyższym priorytetem, nie usuwając go.
*   **Zastosowania**:*
    *   Planowanie zadań w systemach operacyjnych (zadania o wyższym priorytecie są wykonywane jako pierwsze).
    *   Algorytm Dijkstry znajdowania najkrótszej ścieżki w grafie.
    *   Kompresja danych (algorytm Huffmana).

## 4. Struktura Find-Union (Disjoint Set Union)

*   **Charakterystyka**:*
    *   Przechowuje zbiór rozłącznych (nieprzecinających się) podzbiorów.
    *   Umożliwia szybkie sprawdzanie, czy dwa elementy należą do tego samego podzbioru (operacja find).
    *   Umożliwia łączenie dwóch podzbiorów w jeden (operacja union).
*   **Zastosowania**:*
    *   Algorytm Kruskala znajdowania minimalnego drzewa rozpinającego w grafie.
    *   Wykrywanie cykli w grafach.
    *   Implementacja algorytmów grupowania danych (clustering).

## 5. Słownik (Dictionary)

*   **Charakterystyka**:*
    *   Przechowuje pary klucz-wartość.
    *   Umożliwia szybkie wyszukiwanie wartości na podstawie klucza.
    *   Klucze muszą być unikalne.
*   **Zastosowania**:*
    *   Implementacja baz danych (indeksy).
    *   Przechowywanie konfiguracji aplikacji.
    *   Tłumaczenie nazw na wartości (np. słownik językowy).
    *   Implementacja tablic asocjacyjnych w językach programowania.

## Podsumowanie

Wybór odpowiedniej struktury danych zależy od specyfiki problemu, który chcemy rozwiązać. Znajomość charakterystyki i zastosowań podstawowych struktur danych jest kluczowa dla efektywnego projektowania algorytmów i programów.
