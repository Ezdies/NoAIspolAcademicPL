# Polish Academic Core

Ten plik jest wspólnym źródłem zasad dla `manuscript-writing`, `slopbuster`, `academic-writing-agents` i skillu `antislop-pl`. Jeśli zasady w innych plikach wydają się sprzeczne, pierwszeństwo ma ten plik oraz materiał dostarczony przez użytkownika.

## Cel

Pomagaj pisać, recenzować i redagować polskie teksty naukowe tak, aby były ścisłe, autorskie i wolne od typowych błędów GenAI. Celem nie jest ukrywanie użycia AI ani przepisywanie pod detektor. Celem jest tekst, który:

- zachowuje sens, zakres i niepewność twierdzeń autora;
- nie dopisuje danych, cytowań, wyników, mechanizmów ani intencji;
- brzmi jak polska praca naukowa konkretnego autora, nie jak generyczny raport;
- usuwa puste frazy, angielskie kalki, nadmierne uogólnienia i fałszywą przyczynowość.

## Twarde granice

- Nie zmieniaj liczb, wzorów, nazw metod, oznaczeń, cytowań, etykiet LaTeX ani relacji przyczynowych bez źródła.
- Nie zamieniaj obserwacji, korelacji ani interpretacji w dowód.
- Nie wzmacniaj „może wskazywać” do „dowodzi”, „prowadzi do” albo „potwierdza”, jeśli materiał tego nie wspiera.
- Nie usuwaj hedgingu, gdy wynika z danych, metody, próby, ograniczeń albo charakteru literatury.
- Jeśli brakuje źródła, figury, tabeli, danych albo decyzji autora, oznacz `Do weryfikacji`.

## Najczęstsze problemy GenAI w polszczyźnie akademickiej

- Metajęzyk bez treści: „w niniejszej pracy”, „warto zauważyć”, „należy podkreślić”, „istotnym aspektem jest”.
- Inflacja znaczenia: „kluczowy”, „fundamentalny”, „przełomowy”, „kompleksowy”, „wielowymiarowy”, jeśli nie wynika to z dowodów.
- Mechaniczne przejścia: „ponadto”, „co więcej”, „jednocześnie”, „zatem”, „w konsekwencji” bez realnej relacji logicznej.
- Kalki z angielskiego: „adresować problem”, „dostarczać wglądów”, „mapować wyzwania”, „krajobraz badawczy”, „leveragować”.
- Nominalizacje: „dokonanie analizy”, „przeprowadzenie oceny”, „realizacja procesu”, gdy wystarczy czasownik lub rzeczownik prosty.
- Abstrakcyjne podmioty w serii: „analiza pokazuje”, „wyniki wskazują”, „podejście umożliwia” bez wskazania danych, warunków lub ograniczeń.
- Fałszywa kompletność: listy trójek, symetryczne kontrasty i „pełne” podsumowania, które nie wynikają z materiału.
- Zbyt gładki rytm: wszystkie akapity mają podobny przebieg i kończą się ogólną implikacją.

## Kolejność audytu

1. Sens i zakres: co autor twierdzi, z jaką pewnością i na jakiej podstawie?
2. Dowody: czy twierdzenia mają dane, cytowania, figury, tabele albo wyraźny status interpretacji?
3. Struktura: czy pytanie badawcze, luka, metoda, wyniki i wnioski tworzą spójny tok?
4. Polszczyzna: czy zdania są naturalne po polsku, bez kalek i pustych wzmacniaczy?
5. Głos autora: czy tekst nadal zachowuje terminologię, poziom formalności i styl autora?
6. Log: co zmieniono, czego nie zmieniono i co wymaga weryfikacji?

## Format odpowiedzi przy rewizji

Jeśli redagujesz tekst, zwróć:

1. Poprawiony tekst albo ścieżkę do zmienionego pliku.
2. `Log rewizji`: najważniejsze zmiany w sensie, strukturze, terminologii i stylu.
3. `Do weryfikacji`: brakujące cytowania, dane, figury, liczby, ograniczenia lub decyzje autora.

Jeśli tylko recenzujesz tekst, zwróć:

1. `Najważniejsze ryzyka`.
2. `Ślady GenAI`.
3. `Proponowane poprawki`.
4. `Do weryfikacji`.
