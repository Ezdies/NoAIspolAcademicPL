# Reguły akademickie dla języka polskiego

Reguły do usuwania najczęstszych śladów GenAI z polskich tekstów akademickich i naukowych. Priorytetem jest ścisłość, zachowanie zakresu twierdzeń, naturalna polszczyzna badawcza i głos autora. To nie jest zestaw trików pod detektory AI; to audyt jakości tekstu.

Przed użyciem tych reguł przeczytaj `/home/ezdies/AntiSlopPL/POLISH_ACADEMIC_CORE.md`. Jeśli pojawi się różnica między plikami, pierwszeństwo ma `POLISH_ACADEMIC_CORE.md`.

Zasada nadrzędna: poprawiaj styl tylko wtedy, gdy nie zmieniasz sensu, poziomu pewności, zakresu, danych, metody, wyniku ani relacji przyczynowej.

---

## Przed rozpoczęciem: parametry kontekstu

Ustal cztery czynniki przed rewizją:

1. **Dziedzina** — np. informatyka, inżynieria, medycyna, ekonomia, psychologia, językoznawstwo, nauki społeczne, humanistyka.
2. **Typ tekstu** — artykuł, rozdział pracy dyplomowej, abstrakt, przegląd literatury, raport, preprint.
3. **Styl** — zwięzły i bezpośredni, formalny i gęsty, opisowy, recenzyjny, zgodny z próbką autora.
4. **Sekcja** — Wstęp, Metody, Wyniki, Dyskusja, Abstrakt, Przegląd literatury, Zakończenie, Ogólne.

### Wskazówki dla sekcji

**Wstęp:** Konkretna luka badawcza zamiast szerokiego otwarcia typu „w dynamicznie rozwijającym się obszarze”. Kończ konkretnym wkładem pracy.

**Metody:** Strona bierna bywa właściwa. Usuwaj wypełniacze, ale nie wymuszaj aktywnej narracji, jeśli konwencja dziedziny jej nie wymaga.

**Wyniki:** Każde zdanie musi być zakotwiczone w danych. „Istotnie” wymaga podstawy statystycznej albo jasnego znaczenia opisowego.

**Dyskusja:** Otwieraj interpretacją, nie prostym powtórzeniem wyników. Pilnuj sekwencji: obserwacja → interpretacja → ograniczenie lub implikacja.

**Abstrakt:** Każde zdanie niesie informację: problem, metoda, materiał, wynik, znaczenie. Zero zdań ozdobnych.

**Przegląd literatury:** Nie streszczaj prac jedna po drugiej mechanicznie. Grupuj według problemów, metod, sporów lub luk.

**Zakończenie:** Nie powtarzaj ogólnikowo całej pracy. Podaj najważniejszy wniosek, ograniczenie i następny krok tylko wtedy, gdy wynikają z tekstu.

---

## Grupa A: sens i ścisłość

To są granice twarde. Nie łam ich.

1. Zachowuj sens dokładnie. Nie dopisuj twierdzeń, cytowań, wyników, ograniczeń ani intencji autora.
2. Nie zmieniaj liczb, symboli, p-wartości, nazw zmiennych, wzorów, terminów technicznych, oznaczeń i odwołań.
3. Nie zamieniaj korelacji, współwystępowania ani interpretacji w przyczynowość.
4. Osłabiaj język przyczynowy, gdy materiał go nie wspiera: „dowodzi” → „sugeruje”, „prowadzi do” → „wiąże się z”, „wykazuje” → „wskazuje”.
5. Oddziel wynik od interpretacji. Wynik mówi, co zaobserwowano; interpretacja mówi, co to może znaczyć.
6. Jeśli brakuje źródła, figury, tabeli albo danych, oznacz `Do weryfikacji` zamiast wygładzać zdanie jako fakt.

---

## Grupa B: polskie wypełniacze GenAI

Usuwaj albo konkretyzuj:

- „w niniejszej pracy”, „celem niniejszego artykułu jest”, jeśli można przejść od razu do działania lub tezy;
- „warto zauważyć”, „należy podkreślić”, „istotnym aspektem jest”, „nie bez znaczenia pozostaje”;
- „w dynamicznie rozwijającym się świecie/obszarze/kontekście”;
- „kluczową rolę odgrywa”, „ma fundamentalne znaczenie”, „stanowi istotny element”, jeśli nie podano mechanizmu;
- „dostarcza cennych wglądów”, „rzuca światło”, „podkreśla znaczenie”, „otwiera nowe perspektywy”;
- „kompleksowy”, „wielowymiarowy”, „interdyscyplinarny”, „nowatorski”, „przełomowy”, jeśli nie są zdefiniowane.

**Przed:**
> Warto zauważyć, że niniejsze badanie dostarcza cennych wglądów w złożone mechanizmy, które odgrywają kluczową rolę w progresji choroby.

**Po:**
> Wyniki wskazują dwa mechanizmy: przyspieszoną apoptozę komórek CD4+ oraz utrzymaną aktywację NF-kB.

---

## Grupa C: kalki z angielskiego i nienaturalna polszczyzna

- „adresować problem” → „rozwiązywać problem”, „odnosić się do problemu”, „podejmować problem”.
- „dostarczać wglądów” → „pokazywać”, „wskazywać”, „pozwalać rozpoznać”, zależnie od danych.
- „mapować wyzwania” → „porządkować problemy”, „opisywać zależności”, „identyfikować obszary”.
- „krajobraz badawczy” → zwykle „stan badań”, „obszar badań”, „literatura”.
- „implementacja rozwiązania” → często „wdrożenie”, „zastosowanie”, „opracowanie”.
- „optymalny trade-off” → „kompromis”, chyba że termin branżowy ma zostać.
- Nadużycie cudzysłowów przy zwykłych terminach usuń albo zdefiniuj termin.
- Myślniki i dwukropki używaj oszczędnie. Jeśli akapit wygląda jak przepisany angielski abstract, przebuduj składnię.

---

## Grupa D: rytm zdań i akapitów

1. Różnicuj długość zdań. Po dwóch długich zdaniach sprawdź, czy jedno krótkie zdanie nie przywróci kontroli nad argumentem.
2. Nie zaczynaj kilku kolejnych zdań od „Wyniki”, „Analiza”, „Badanie”, „To”, „Ponadto”.
3. Nie kończ każdego akapitu zdaniem o „szerszym znaczeniu”, jeśli akapit go nie uzasadnia.
4. Nie wymuszaj układu „po pierwsze / po drugie / po trzecie”, gdy lista jest tylko ozdobą.
5. Nie używaj symetrii „z jednej strony / z drugiej strony”, jeśli kontrast nie jest rzeczywiście równoważny.
6. Rozbij zdania, które kumulują kilka zastrzeżeń, wyjątków i warunków.
7. Zostaw czasem logiczną bliskość bez łącznika. Nie każdy związek wymaga „zatem”.

---

## Grupa E: głos autora i rozumowanie

- Zastępuj ogólniki konkretem tylko wtedy, gdy materiał źródłowy go zawiera.
- Zachowuj słownictwo dziedzinowe. Nie upraszczaj terminów tylko po to, by tekst brzmiał „lżej”.
- Prowadź rozumowanie przez obserwacje, porównania, ograniczenia i decyzje metodologiczne.
- Nie wygładzaj niepewności. W polskim tekście naukowym naturalne są zdania ostrożne, jeśli ostrożność wynika z danych.
- Przywracaj głos autora: konkretne wybory, zakres pracy, ograniczenia, terminologia i rytm z próbki stylu.

---

## Grupa F: głębokie wzorce składni GenAI

- Ogranicz abstrakcyjne podmioty: „niniejsza analiza pokazuje”, „podejście umożliwia”, „wyniki podkreślają”. Jeśli to możliwe, wskaż konkretny wynik, metodę, próbę lub warunek.
- Przenoś główną tezę do zdania głównego, a warunki i ograniczenia do zdań podrzędnych.
- Usuwaj nominalizacje: „dokonanie analizy” → „analiza” albo „przeanalizowano”; „przeprowadzenie oceny” → „oceniono”.
- Rozbij łańcuchy „który/która/które”, jeśli zaciemniają podmiot.
- Kwestionuj listy równoległe, które wyglądają jak automatycznie dopisane trójki.
- Nie rozlewaj hedgingu na każde zdanie. Ostrożność ma być tam, gdzie twierdzenie jest niepewne.

**Przed:**
> Niniejsza analiza pokazuje, że implementacja technik uczenia maszynowego ma istotne implikacje dla całego obszaru badawczego.

**Po:**
> Model uczenia maszynowego zwiększył dokładność klasyfikacji o 18%. Poprawa wystąpiła we wszystkich trzech zbiorach walidacyjnych.

---

## Grupa G: naturalna polska składnia

- Nie każde zdanie musi być pełnym, gładkim raportem. Krótsze zdanie może być bardziej akademickie niż rozbudowana fraza.
- Dopuszczaj napięcie między zdaniami bez przejścia, jeśli relacja wynika z treści.
- Mieszaj zdania obserwacyjne, interpretacyjne i zastrzegające.
- Nie eliminuj całej szorstkości autora. Zbyt równy tekst brzmi modelowo.

---

## Wyjątek: listy konieczne

Nie skracaj list, które są kompletnym i koniecznym zestawem: warunki eksperymentalne, kategorie kodowania, zmienne, komponenty molekularne, pytania badawcze, hipotezy. Reguły antywyliczeniowe dotyczą list ozdobnych, nie merytorycznych.

---

## Grupa H: metafory, ozdobniki i architektura zdań

- Usuń metafory wyjaśniające proces techniczny, jeśli nie są potrzebne dla odbiorcy.
- Unikaj konstrukcji „nie tylko X, ale także Y”, gdy służy tylko podbiciu znaczenia.
- Nie twórz zdań dwuczłonowych, w których druga część powtarza pierwszą.
- Gdy wykonawca jest znany, rozważ stronę czynną. W metodach i opisach procedur strona bierna może zostać.
- Usuń końcówki imiesłowowe, które tylko streszczają zdanie: „tym samym umożliwiając...”, „prowadząc do...”, jeśli relacja jest oczywista albo nieudowodniona.

---

## Grupa I: domknięcie logiczne i argument

- Nie domykaj każdego łańcucha przyczynowego. Jeśli wniosek jest oczywisty, nie dopisuj „co podkreśla znaczenie...”.
- Nie prowadź tekstu wyłącznie do przodu. Czasem lepiej zacząć od wyjątku, ograniczenia albo wyniku niezgodnego z oczekiwaniem.
- Nie otwieraj każdego akapitu najszerszym uogólnieniem. W polskim artykule często mocniejsze jest wejście od konkretu.
- Pilnuj, by „zatem”, „w konsekwencji”, „tym samym” oznaczały relację wynikającą z poprzedniego zdania.

---

## Grupa J: podmioty i logika ukryta

- Jeśli dwa kolejne zdania zaczynają się od „Wyniki”, „Analiza”, „Badanie”, „Podejście”, zmień podmiot jednego z nich.
- Przełam łańcuch abstrakcyjnych podmiotów konkretem: próbą, metodą, zmienną, grupą, wynikiem, autorem, ograniczeniem.
- Usuń „zatem”, „tym samym”, „w konsekwencji”, gdy relacja jest jasna bez sygnalizatora.
- Pisz bezpośrednio o dobrze wspartych wynikach, a ostrożnie o interpretacjach i generalizacjach.

---

## Audyt strukturalny po regułach

Uruchom po poprawkach zdaniowych, zwłaszcza gdy tekst ma ponad 5 zdań albo nadal brzmi modelowo.

| # | Wzorzec | Poprawka |
|---|---------|-----|
| S1 | Wszystkie zdania mają podobną wagę | Wydobądź główne twierdzenie, skróć wsparcie |
| S2 | Każdy akapit kończy się implikacją | Zostaw tylko implikacje wynikające z materiału |
| S3 | Argument idzie wyłącznie linearnie | Wprowadź kontrast, wyjątek lub ograniczenie |
| S4 | Akapit zaczyna się od szerokiego banału | Zacznij od konkretnej obserwacji |
| S5 | Powtarza się ten sam typ podmiotu | Wprowadź wynik, metodę, grupę, warunek albo źródło |
| S6 | Wszystkie zdania mają ten sam rytm | Zmień długość i konstrukcję części zdań |
| S7 | Łączniki logiczne są oczywiste | Usuń je i pozwól działać zestawieniu zdań |
| S8 | Niepewność jest wszędzie | Skup hedging na twierdzeniach niepewnych |
| S9 | Zestawienie zdań jest niejasne | Dodaj precyzyjny łącznik, nie generyczne „ponadto” |
| S10 | Finał tylko streszcza | Zastąp go konkretnym wnioskiem, ograniczeniem albo przejściem |

---

## Czego nie zmieniać

Te granice chronią ścisłość i standardy dziedziny:

- Zdań, które już brzmią naturalnie i są ścisłe.
- Strony biernej w metodach, jeśli jest zgodna z konwencją.
- Terminologii technicznej i słownictwa dziedzinowego.
- Ostrożności przy rzeczywiście niepewnych twierdzeniach.
- Kompletnych, koniecznych list.
- Języka statystycznego popartego statystyką.
- Stylu autora, jeśli nie wprowadza błędów ani sztuczności.

## Format wyniku audytu

Przy recenzji zwracaj:

1. `Najważniejsze ryzyka`: sens, cytowania, przyczynowość, zakres.
2. `Ślady GenAI`: konkretne frazy i wzorce z tekstu.
3. `Proponowane poprawki`: krótkie zamienniki albo zasady przebudowy.
4. `Do weryfikacji`: brakujące źródła, dane, figury, liczby, ograniczenia.
5. `Log rewizji`: jeśli tekst został zmieniony.
