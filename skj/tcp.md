Warstwa transportu to jedna z kluczowych warstw w modelu OSI (Open Systems Interconnection) lub TCP/IP, która znajduje się pomiędzy warstwą sieciową a warstwą aplikacji. Jej głównym zadaniem jest **dostarczenie niezawodnej i efektywnej transmisji danych pomiędzy aplikacjami działającymi na różnych hostach (komputerach) w sieci.**

## Usługi warstwy transportu

Warstwa transportu oferuje szereg usług, które ułatwiają komunikację między aplikacjami. Najważniejsze z nich to:

1.  **Segmentacja i składanie danych:** Warstwa transportu dzieli dane z warstwy aplikacji na mniejsze jednostki, zwane segmentami (w przypadku protokołu TCP) lub datagramami (w przypadku protokołu UDP). Na odbiorze segmenty są ponownie składane w całość, tworząc oryginalne dane.

2.  **Adresowanie aplikacji:** Każda aplikacja, która chce komunikować się w sieci, ma przypisany unikalny numer portu. Warstwa transportu, dodając numery portów do segmentów, identyfikuje, do której aplikacji na danym hoście mają trafić dane.

3.  **Nawiązywanie i zamykanie połączeń:** Niektóre protokoły warstwy transportu (np. TCP) oferują usługi nawiązywania i zamykania połączeń między aplikacjami. Pozwala to na logiczne powiązanie dwóch aplikacji i wymianę danych w ramach "sesji".

4.  **Kontrola przepływu:** Warstwa transportu dba o to, aby nadawca nie wysyłał danych szybciej, niż odbiorca jest w stanie je przetworzyć. Mechanizmy kontroli przepływu zapobiegają przeciążeniu sieci i utracie danych.

5.  **Kontrola błędów:** Warstwa transportu może oferować mechanizmy kontroli błędów, takie jak sumy kontrolne, które pozwalają na wykrycie uszkodzonych danych podczas transmisji. W przypadku wykrycia błędu, dane mogą być retransmitowane.

6.  **Multipleksowanie i demultipleksowanie:** Warstwa transportu umożliwia wielu aplikacjom korzystanie z tego samego łącza fizycznego (multipleksowanie). Na odbiorze, na podstawie numerów portów, segmenty są kierowane do odpowiednich aplikacji (demultipleksowanie).

## Protokół TCP jako przykład

TCP (Transmission Control Protocol) to jeden z najpopularniejszych protokołów warstwy transportu. Oferuje on **niezawodną, strumieniową transmisję danych z potwierdzeniami.** Oznacza to, że:

*   **Niezawodność:** TCP dba o to, aby wszystkie dane dotarły do odbiorcy w całości i w odpowiedniej kolejności. W przypadku utraty danych, TCP retransmituje je.
*   **Strumieniowość:** TCP traktuje dane jako ciąg bajtów (strumień), a nie jako oddzielne wiadomości.
*   **Potwierdzenia:** Odbiorca potwierdza odbiór każdego segmentu, co pozwala nadawcy upewnić się, że dane dotarły bez problemów.

**Protokół TCP jest szeroko stosowany w Internecie do przesyłania danych, które wymagają niezawodności, np. strony internetowe (HTTP), poczta elektroniczna (SMTP), przesyłanie plików (FTP).**

## Podsumowanie

Warstwa transportu odgrywa kluczową rolę w komunikacji sieciowej, oferując szeroki zakres usług, które ułatwiają aplikacjom wymianę danych. Protokół TCP jest przykładem protokołu warstwy transportu, który zapewnia niezawodną transmisję danych i jest szeroko stosowany w Internecie.
