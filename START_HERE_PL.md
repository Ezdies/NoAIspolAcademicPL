# AntiSlopPL: start dla agentów pisania naukowego po polsku

Ten katalog zbiera narzędzia do pracy nad artykułem naukowym, pracą dyplomową albo rozdziałem w stylu akademickim. Celem nie jest „humanizacja” dla samej humanizacji, tylko usunięcie najczęstszych błędów GenAI: zmyślonych lub wzmocnionych twierdzeń, pustych ogólników, angielskich kalek, sztucznego rytmu i tekstu, który brzmi jak wygenerowany raport zamiast pracy konkretnego autora.

Wspólne zasady są w `POLISH_ACADEMIC_CORE.md`. Pozostałe instrukcje powinny odsyłać do tego pliku, żeby nie dublować reguł i nie tworzyć sprzecznych wersji checklisty.

## Warstwy

1. `manuscript-writing`
   - Główna warstwa do academic/scientific writing.
   - Najpierw czytaj `manuscript-writing/SKILL.md`.
   - Przy rewizji tekstu używaj `manuscript-writing/references/revision-checklist.md`.
   - Tryb `review` nadaje się do diagnozy, a `revision` do bezpośredniej redakcji.
   - W polskim tekście pilnuj szczególnie zakresu twierdzeń, cytowań i tego, czy zdanie nie dodaje pewności, której nie ma w danych.

2. `slopbuster`
   - Warstwa anty-GenAI-slop.
   - Dla tekstu naukowego używaj trybu akademickiego i próby głosu autora.
   - Dobre miejsce na końcowy audyt po merytorycznej redakcji.
   - W polszczyźnie szukaj zwłaszcza: „niniejsza praca”, „warto zauważyć”, „kluczowe znaczenie”, „w dynamicznie rozwijającym się obszarze”, mechanicznych „ponadto/co więcej”, angielskich kalek i pustych konkluzji.

3. `academic-writing-agents`
   - Warstwa szczególnie przydatna dla LaTeX-a, paperów i prac dyplomowych.
   - Zawiera agentów od logiki, stylu, spójności terminologii, bibliografii, figur i układu LaTeX.
   - Najpierw stosuj agentów recenzenckich, dopiero potem agentów edytujących.

## Proponowany pipeline dla artykułu po polsku

1. Zdefiniuj plik stylu autora: próbka Twojego tekstu, preferencje terminologiczne, poziom formalności, zakazane frazy.
2. Uruchom diagnozę struktury i argumentacji na szkicu.
3. Popraw tekst merytorycznie bez zmiany zakresu twierdzeń.
4. Zrób audyt cytowań, definicji, tabel, figur i odnośników.
5. Przepuść tekst przez warstwę anty-GenAI-slop.
6. Na końcu wykonaj recenzję „czy to nadal brzmi jak autor”, szczególnie przy pracy dyplomowej albo paperze.

## Lokalny profil autora

Dla prac Maksymiliana Dudziaka używaj profilu
`author-profiles/maksymilian-dudziak.md`. Profil ma pierwszeństwo tylko w sprawach
tonu, rytmu i sposobu objaśniania. Nie wolno używać go do dopisywania faktów,
wyników, cytowań ani decyzji implementacyjnych.

## Minimalny audyt anty-GenAI dla polszczyzny

- Czy każde mocne twierdzenie ma podstawę w danych, literaturze albo materiale użytkownika?
- Czy tekst nie zamienia „może wskazywać” w „dowodzi” albo „prowadzi do”?
- Czy usunięto frazy-wypełniacze: „warto zauważyć”, „należy podkreślić”, „istotnym aspektem jest”, „w ramach niniejszej pracy”?
- Czy przejścia logiczne oznaczają realną relację, a nie tylko wygładzają akapit?
- Czy polski styl nie jest kalką angielskiego abstractu?
- Czy każde podsumowanie coś wnosi, zamiast kończyć akapit pustą implikacją?
- Czy po redakcji został log zmian i lista `Do weryfikacji`?

## Lokalny revision guard

Nie znalazłem jednoznacznego publicznego repozytorium GitHub o nazwie `ai-revision-guard` po samej nazwie. Jeśli masz dokładny adres `owner/repo`, można je sklonować obok pozostałych projektów:

```bash
git clone https://github.com/OWNER/ai-revision-guard.git
```

Do czasu znalezienia konkretnego repo jego rolę pełni lokalna zasada z `POLISH_ACADEMIC_CORE.md`: każda większa rewizja musi mieć `Log rewizji`, elementy `Do weryfikacji` oraz sprawdzenie zgodności z próbką stylu autora.
