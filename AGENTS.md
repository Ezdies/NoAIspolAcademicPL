# AntiSlopPL: instrukcje dla agentów

Ten workspace służy do pisania, recenzowania i redagowania tekstów naukowych po polsku. Domyślnie odpowiadaj po polsku i redaguj w polszczyźnie akademickiej, chyba że użytkownik poprosi o inny język.

## Lokalne zasoby

- Traktuj `POLISH_ACADEMIC_CORE.md` jako wspólne źródło zasad dla wszystkich warstw.
- Używaj `manuscript-writing/` jako głównej warstwy rewizji naukowej: precyzja, zakres twierdzeń, logika, cytowania, ton.
- Używaj `slopbuster/` jako warstwy anty-GenAI-slop po redakcji merytorycznej.
- Używaj `academic-writing-agents/` przy LaTeX-u, pracach dyplomowych, artykułach, figurach, bibliografii, notacji i wieloagentowej recenzji.
- Przed zaprojektowaniem workflow przeczytaj `START_HERE_PL.md`.

## Twarde reguły

- Zachowuj twierdzenia autora, zakres, niepewność, terminologię i deklarowany wkład pracy.
- Nie dopisuj cytowań, wyników, mechanizmów, danych, liczb, ograniczeń ani intencji autora bez źródła.
- Nie wzmacniaj korelacji do przyczynowości i nie zamieniaj ostrożnych sformułowań w pewniki.
- Nie „upiększaj” tekstu kosztem ścisłości. Lepsze jest zdanie suche i prawdziwe niż płynne i fałszywie mocne.
- Przy znaczących zmianach zostaw krótki log rewizji.
- Nierozstrzygnięte kwestie oznaczaj jako `Do weryfikacji`.

## Typowe problemy GenAI w polskim tekście naukowym

- Nadmiar metajęzyka: „niniejsza praca ma na celu”, „warto zauważyć”, „należy podkreślić”, „w kontekście dynamicznego rozwoju”.
- Puste wzmacniacze: „kluczowy”, „istotny”, „znaczący”, „kompleksowy”, „wielowymiarowy”, „fundamentalny” bez konkretu.
- Mechaniczne przejścia: „ponadto”, „co więcej”, „jednocześnie”, „z drugiej strony”, „w rezultacie” użyte bez realnej relacji logicznej.
- Angielskie kalki: „adresować problem”, „mapować wyzwania”, „dostarczać wglądów”, „leveragować”, „stanowić krok w kierunku”.
- Zbyt gładkie akapity: każde zdanie ma taki sam rytm, a każdy akapit kończy się ogólną implikacją.
- Abstrakcyjne podmioty: „analiza pokazuje”, „wyniki wskazują”, „podejście umożliwia” powtarzane bez wskazania danych, warunków lub ograniczeń.
- Fałszywa kompletność: listy trójek, symetryczne kontrasty i „pełne” podsumowania, które nie wynikają z materiału.
- Rozmyte autorstwo: tekst brzmi jak raport modelu, a nie jak badacz z określonym problemem, materiałem i decyzjami.

## Kolejność pracy

1. Sprawdź pytanie badawcze, wkład, strukturę i tok argumentacji.
2. Sprawdź terminologię, definicje, cytowania, figury, tabele, równania i odwołania LaTeX.
3. Popraw jasność, zwięzłość, spójność logiczną i ton akademicki.
4. Wykonaj audyt anty-slop: frazy generyczne, nadmierne uogólnienia, kalki z angielskiego, sztuczne przejścia, puste konkluzje.
5. Porównaj z próbką stylu autora, jeśli jest dostępna, i przywróć naturalny polski głos autora.
