# Checklist rewizji polskiego tekstu akademickiego

Używaj tej checklisty ściśle i sekwencyjnie przy rewizji lub recenzji tekstów naukowych. W tym workspace domyślny język pracy to polska proza akademicka. Celem jest precyzja, zwięzłość, spójność logiczna, rygor naukowy i naturalna polszczyzna przy zachowaniu zweryfikowanego sensu.

Przed redakcją polskiego tekstu akademickiego przeczytaj `/home/ezdies/AntiSlopPL/POLISH_ACADEMIC_CORE.md`. To wspólne źródło reguł anty-GenAI-slop i ma pierwszeństwo przed lokalnymi przykładami, jeśli pojawi się konflikt.

Przykłady w tej checklistcie pokazują wzorce redakcyjne. Nie traktuj ich treści technicznej jako zweryfikowanych faktów i nie wstawiaj ich do pracy, jeśli nie wynikają z materiału autora lub cytowanego źródła.

## Phase 0: Revision Scope Setup

- [ ] **Load Polish Academic Core**

Przeczytaj `/home/ezdies/AntiSlopPL/POLISH_ACADEMIC_CORE.md`, gdy tekst jest po polsku albo ma zostać przepisany na polski.

- [ ] **Identify Revision Constraints**

Identify the target audience, journal or proposal format, word limit, and required tone before revising.

- [ ] **Preserve Technical Meaning**

Preserve the author's intended technical meaning. Do not improve style by changing claims beyond the available evidence.

Decision rule: If a revision changes the scope, certainty, mechanism, temperature range, material system, or causal relationship of the original claim, flag it instead of silently rewriting it.

Przed: "Wyniki dowodzą, że zastosowana metoda eliminuje problem niezależnie od warunków."

Po: "W badanych warunkach zastosowana metoda zmniejszyła skalę problemu."

## Phase 1: Precision and Clarity Verification

- [ ] **Remove Polish GenAI Fillers**

Scan for Polish filler formulas such as "w niniejszej pracy", "warto zauważyć", "należy podkreślić", "istotnym aspektem jest", and "w dynamicznie rozwijającym się obszarze". Delete them or replace them with the concrete claim they obscure.

- [ ] **Remove English Calques**

Replace English-influenced Polish such as "adresować problem", "dostarczać wglądów", "mapować wyzwania", "krajobraz badawczy", and "leveragować" with natural Polish academic wording.

- [ ] **Specify Vague Language**

Scan for open-ended statements and replace them with exact parameters or specific context.

Przed: "Jest to nadal nierozwiązany problem."

Po: "W literaturze nie określono dotąd, jak ten parametr zmienia się przy większej liczbie użytkowników systemu."

- [ ] **Resolve Ambiguous Adjectives**

Identify multi-meaning modifiers, such as "fragile" or "strong", and replace them with precise scientific descriptions.

Przykład: zamiast pisać, że układ jest "wrażliwy", doprecyzuj, czy chodzi o podatność na zakłócenia pomiarowe, niestabilność przy zmianie parametrów wejściowych, czy brak odporności na dane spoza rozkładu.

- [ ] **Quantify Qualitative Adverbs ("Show, Don't Tell")**

Replace qualitative descriptors with exact metrics, percentages, or mathematical orders of magnitude when those values are provided.

Przed: "Wydajność modelu znacząco spada dla krótkich sekwencji wejściowych."

Po: "Dla sekwencji krótszych niż [zweryfikowana długość] dokładność modelu spada z [wartość] do [wartość]."

- [ ] **Standardize Terminology**

Verify that a single technical term is used consistently throughout the text. Remove "elegant variation", meaning synonyms used for technical terms only to vary vocabulary.

- [ ] **Delete Redundant Modifiers (Tautologies)**

Remove modifiers that duplicate the meaning of the core word.

Przed: "całkowicie wyeliminować", "absolutnie niezbędny", "przyszły potencjał", "nowa innowacja".

Po: "wyeliminować", "niezbędny", "potencjał", "innowacja".

- [ ] **Explain Niche Jargon**

Identify highly domain-specific jargon. Provide a brief, seamless, in-line explanation for readers outside the immediate sub-field.

- [ ] **Remove Orphan Abbreviations**

Delete acronyms or defined concepts if the term only appears once in the entire text.

## Phase 2: Conciseness and Flow Engineering

- [ ] **Convert Nominalizations to Strong Verbs**

Find core actions hidden inside nouns and convert them to direct verbs to propel the sentence forward.

Przed: "Dokonano przeprowadzenia analizy wpływu parametru X na skuteczność klasyfikacji."

Po: "Przeanalizowano wpływ parametru X na skuteczność klasyfikacji."

- [ ] **Combine into "Property/Action -> Consequence" Structures**

Merge fragmented sentences and remove excessive bridging phrases. Combine statements of fact directly with their resulting impact.

Przed: "Metoda wykorzystuje próbkowanie warstwowe. Ta cecha poprawia stabilność wyników."

Po: "Próbkowanie warstwowe zmniejsza zmienność wyników między uruchomieniami w eksperymentach z [zweryfikowany warunek]."

- [ ] **Verify Sentence Purpose**

Evaluate every sentence individually. Delete "orphan facts", even if technically true, if they do not actively advance the core argument or provide immediate, necessary context.

Decision rule: A sentence should define the problem, justify the approach, explain evidence, interpret results, state a limitation, or advance the conclusion. If it does none of these, delete or relocate it.

Przykład: informację o historii danej metody usuń, jeśli nie wyjaśnia bezpośrednio wyboru procedury, luki badawczej, konstrukcji eksperymentu albo interpretacji wyników.

- [ ] **Remove Argument Echoing**

Check for repetitive looping of the exact same argument across a paragraph or section. Make the point clearly once and advance the narrative.

- [ ] **Use Transitions Only for Clear Logical Relationships**

Dopuszczaj spójniki i operatory logiczne, takie jak "ponadto", "co więcej", "jednocześnie", "zatem" i "w konsekwencji", tylko wtedy, gdy dokładnie oznaczają relację między zdaniami. Usuwaj je, gdy jedynie dekorują tekst albo maskują słabe połączenie. Jeśli to możliwe, łącz zdania przez powiązanie tematu nowego zdania z informacją z poprzedniego.

Przed: "Ponadto model osiąga większą stabilność. Co więcej, ten wynik potwierdza zasadność przyjętej architektury."

Po: "Większa stabilność wyników wspiera wybór tej architektury."

Akceptowalne: "Po usunięciu przykładów odstających wzrosła precyzja klasyfikacji. Dlatego w dalszej analizie traktujemy odstające obserwacje jako osobne źródło błędu, a nie jako neutralny składnik zbioru."

Reguła dla polszczyzny: "ponadto", "co więcej", "jednocześnie", "zatem" i "w konsekwencji" zostają tylko wtedy, gdy oznaczają rzeczywistą relację logiczną. Jeśli tylko wygładzają akapit, usuń je.

## Phase 3: Tone and Formatting Calibration

- [ ] **Strip Hyperbole**

Delete subjective, exaggerated, or non-scientific adjectives, such as "exceptional", "first-ever", "unprecedented", and "perfect".

Polish examples: "kluczowy", "fundamentalny", "przełomowy", "kompleksowy", "wielowymiarowy", and "nowatorski" require evidence or definition. Otherwise, delete or weaken them.

- [ ] **Calibrate Scientific Certainty (Hedging)**

Replace absolute verbs, such as "proves" and "guarantees", with precise, empirically appropriate verbs, such as "demonstrates", "indicates", and "suggests", unless dealing with pure mathematical certainty.

Przed: "Wyniki dowodzą, że mechanizm X powoduje obserwowany wzrost skuteczności."

Po: "Wyniki wskazują, że mechanizm X może częściowo wyjaśniać obserwowany wzrost skuteczności."

- [ ] **Enforce Objective Active Voice**

Avoid clunky passive voice, such as "It was demonstrated that". Make the data, the model, or the literature the subject where this improves clarity.

Polish exception: do not force active voice in methods or formal Polish academic prose. Impersonal forms such as "przeanalizowano", "zastosowano", and "porównano" are often natural and should remain if clear.

Przed: "Zostało pokazane, że warunek X pogarsza działanie algorytmu."

Przed: "Pokazaliśmy, że warunek X pogarsza działanie algorytmu."

Po: "W eksperymentach warunek X obniżył skuteczność algorytmu."

- [ ] **Convert Bullets to Natural Prose**

Transform bullet-heavy explanations into cohesive paragraph flow where prose is expected by the venue.

- [ ] **Remove Endless Dashes and Hyphens**

Break up long, disjointed clauses bridged by dashes into clear, properly punctuated, separate sentences.

## Phase 4: Scientific Rigor and Structural Integrity Verification

- [ ] **Validate Problem Statements**

Ensure the core research gap is rooted in established physics or documented literature. Flag and rewrite any contrived, "strawman" problems that do not reflect actual scientific or engineering challenges.

Decision rule: A valid problem statement should identify what remains unknown, why existing methods do not resolve it, and why the gap matters scientifically or technically.

Przed: "Dotychczas nikt dokładnie nie zbadał tego problemu."

Po: "Dotychczasowe prace opisują [znany aspekt problemu], ale nie określają, jak [konkretna własność] zmienia się w warunkach [badany kontekst]."

- [ ] **Verify Citation Coverage**

Check all factual claims, baseline metrics, and novelty statements to ensure they are anchored by appropriate references.

Działanie: jeśli autor twierdzi, że metoda jest "nowa", "pierwsza" albo "nowatorska", sprawdź, czy wcześniejsza literatura jest dokładnie przywołana i czy rzeczywiście uzasadnia lukę badawczą. Sprawdź też lata publikacji cytowanych prac, aby porównanie nie opierało się wyłącznie na przestarzałej literaturze.

Decision rule: Claims about prior work, performance benchmarks, material properties, mechanisms, and novelty require citations unless they are directly supported by data presented in the same text.

- [ ] **Classify Claims Correctly**

Verify that each claim is classified correctly as evidence, interpretation, limitation, or implication.

Przykład:

  - Dowód: "Średnia wartość F1 wzrosła z 0,71 do 0,78 po zastosowaniu ważenia klas."
  - Interpretacja: "Ten wzrost jest zgodny z hipotezą, że ważenie klas ogranicza wpływ niezbalansowania zbioru."
  - Ograniczenie: "Eksperyment nie oddziela wpływu ważenia klas od wpływu doboru progu decyzyjnego."
  - Implikacja: "Wynik sugeruje, że sposób obsługi niezbalansowanych klas może istotnie wpływać na ocenę modelu."

- [ ] **State Limitations and Boundary Conditions**

Check that limitations and boundary conditions are stated where the evidence does not support general conclusions.

Decision rule: When a conclusion depends on a specific temperature range, bias condition, geometry, sample size, measurement setup, or model assumption, state that boundary explicitly.

Przed: "Model jest odporny na szum w danych."

Po: "Model zachował dokładność powyżej [wartość] dla poziomów szumu od [wartość] do [wartość] w badanym zbiorze testowym."

- [ ] **Confirm Citation Specificity**

Confirm that citations support the specific claim being made, not just the general topic.

Przed: "Uczenie kontrastowe poprawia jakość reprezentacji [1]." Źródło [1] opisuje wyłącznie procedurę trenowania modeli kontrastowych.

Po: "Uczenie kontrastowe wymaga odpowiedniego doboru par dodatnich i ujemnych [1]."

- [ ] **Cross-Examine Data Consistency**

Cross-reference all numerical values, percentages, and metrics mentioned in the text against the data presented in the accompanying figures and tables to guarantee exact alignment. Verify that mathematical logic is strictly sound, particularly regarding baselines.

Przykład: sprawdź mianownik w porównaniach procentowych. Jeśli metoda B uzyskała 100 punktów, a metoda A 120 punktów, to A ma wynik o 20% wyższy od B. Nie oznacza to jednak, że B ma wynik o 20% niższy od A, bo spadek z 120 do 100 wynosi 16,7%.

- [ ] **Audit Figure/Table Sequencing**

Sprawdź, czy wszystkie ryciny i tabele są numerowane kolejno, np. "Rycina 1", "Rycina 2", "Tabela 1", oraz czy każda z nich jest przywołana i omówiona w tekście głównym.

- [ ] **Define Equation Variables**

Audit every mathematical equation. Ensure every variable is clearly defined immediately before or after the equation appears.

- [ ] **Evaluate Evidence Presentation**

Verify that logical leaps are avoided. Ensure that empirical evidence directly and logically supports the subsequent conclusions without overextending the data's implications.

Decision rule: Do not convert correlation into causation, limited measurements into general laws, or a single device result into a technology-wide conclusion.

Przed: "Spadek błędu dowodzi, że dodany moduł odpowiada za poprawę generalizacji."

Po: "Spadek błędu jest zgodny z interpretacją, że dodany moduł wspiera generalizację w badanej konfiguracji."

- [ ] **Audit Multi-Level Flow and Logic**

Perform a final logic-flow pass at the sentence, paragraph, and section levels. Ensure each sentence connects to the preceding and following context rather than reading as an isolated fact. Confirm that each paragraph has a clear internal progression, and that each section advances the larger argument in a coherent order.

Decision rule: A technically correct sentence should still be revised or relocated if its relationship to the surrounding argument is unclear.

Przed: "Model trenowano na danych z 2022 roku. Zbiór zawiera teksty urzędowe. Usunięto duplikaty."

Po: "Model trenowano na tekstach urzędowych z 2022 roku, ponieważ taki materiał odpowiada docelowemu zastosowaniu systemu. Przed treningiem usunięto duplikaty, aby ograniczyć ryzyko zawyżenia wyników ewaluacji."

## Phase 5: Final Output Audit

- [ ] **Produce a Revision Log**

Produce a concise `Log rewizji` identifying major changes to claims, structure, terminology, and evidence support.

Przykładowy log rewizji:

  - Doprecyzowano lukę badawczą przez wskazanie badanego zakresu danych.
  - Zastąpiono nieuzasadnione twierdzenie o nowości ostrożnym porównaniem z literaturą.
  - Dodano warunki brzegowe, aby nie uogólniać wyniku poza przebadany materiał.

- [ ] **Perform Final Accuracy and Prose Review**

Re-read the revised text once for scientific accuracy and once for prose quality.

- [ ] **Produce Do weryfikacji**

List unresolved citation needs, missing data, unclear author intent, unsupported numerical claims, figure/table mismatches, or style decisions that require the author's approval under `Do weryfikacji`.
