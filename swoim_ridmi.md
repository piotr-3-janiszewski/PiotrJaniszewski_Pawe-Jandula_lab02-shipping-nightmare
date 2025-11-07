📘 **Różnice między plikami – skrót**

1. **Struktura kodu:**

   * **Zmodyfikowany plik** używa wzorca **Strategy** – każdy typ wysyłki ma własną klasę (`ShippingStandard`, `ShippingExpress` itd.).
   * **Oryginalny plik** zawiera wszystko w jednej klasie (`ShippingCalculator`) i dużym łańcuchu `if-elif`.

2. **Rozszerzalność:**

   * W **zmodyfikowanym pliku** łatwo dodać nowy typ wysyłki – wystarczy nowa klasa.
   * W **oryginalnym pliku** trzeba dopisać kolejną sekcję `if`.

3. **Czytelność i utrzymanie:**

   * **Zmodyfikowany plik** jest bardziej uporządkowany – każda metoda dostawy ma własną logikę.
   * **Oryginalny plik** jest trudniejszy w utrzymaniu i mniej przejrzysty.

4. **Różnice w danych:**

   * W **oryginalnym pliku** pojawia się dodatkowa stawka `"international_express"`, ale nie jest używana.
   * **Zmodyfikowany plik** korzysta z listy strategii, **oryginalny** – z jednego słownika z cenami bazowymi.

5. **Cel refaktoryzacji:**

   * **Oryginalny plik** pokazuje „spaghetti code” przed zastosowaniem wzorca.
   * **Zmodyfikowany plik** to zrefaktoryzowana, modularna wersja gotowa do rozbudowy.
