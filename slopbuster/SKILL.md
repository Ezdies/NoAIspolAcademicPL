---
name: slopbuster
description: |
  Anti-GenAI-slop reviewer for prose, code, and academic writing, with Polish
  academic writing support. Use when editing or reviewing text to remove
  AI-generated patterns, preserve author voice, catch inflated claims, reduce
  generic phrasing, and improve Polish scientific prose without changing facts.
license: MIT
metadata:
  author: gabelul
  version: "1.0.0"
  tags: [ai-humanizer, text-humanization, ai-slop, deslop, ai-text-humanizer, code-quality, writing-tools, anti-slop, ai-patterns]
allowed-tools:
  - Read
  - Write
  - Edit
  - Grep
  - Glob
  - AskUserQuestion
---

# Slopbuster: usuń GenAI-slop, zachowaj autora

Usuwaj wzorce typowe dla tekstu generowanego przez modele. To nie jest zwykła korekta językowa ani „humanizacja” pod detektory. Celem jest tekst bardziej ścisły, konkretny i autorski.

Działa na prozie, kodzie, commitach, docstringach i tekstach akademickich. W tym workspace domyślnie traktuj tryb akademicki jako tryb dla polskiego tekstu naukowego.

Przy tekście akademickim po polsku najpierw przeczytaj `/home/ezdies/AntiSlopPL/POLISH_ACADEMIC_CORE.md`. Ten plik ma pierwszeństwo przed ogólnymi regułami humanizacji i scoringu.

## How This Works

Audyt ma dwa przejścia. Pierwsze znajduje wzorce GenAI. Drugie sprawdza, czy po usunięciu tych wzorców tekst nie stał się sterylny, bezosobowy albo zbyt gładki.

## Quick Start

```
/slopbuster <file_or_text>                    # Auto-detect mode, standard depth
/slopbuster <file> --mode text|code|academic  # Force specific mode
/slopbuster <file> --depth quick|standard|deep
/slopbuster <file> --score-only               # Just score, don't rewrite
```

## Modes

Detect automatically from file extension and content, or specify explicitly.

| Mode | Targets | Rule files loaded |
|------|---------|-------------------|
| `text` | Prose, marketing, blog posts, docs, emails | text-content, text-language, text-style, text-communication, text-structure |
| `code` | Source files, comments, naming, commits, docstrings | code-comments, code-naming, code-commits, code-docstrings, code-quality, code-llm-tells |
| `academic` | Research papers, theses, abstracts | academic (49 rules, section-specific) |
| `auto` | Detects from context | Loads relevant rule files |

## Depth Levels

| Depth | What happens | Best for |
|-------|-------------|----------|
| `quick` | Single pass, obvious patterns only, no scoring | Fast edits, social copy |
| `standard` | Full pattern scan + two-pass audit + score + changelog | Anything going public |
| `deep` | Full scan + voice calibration against writer's sample + style guide generation | Ghostwriting, brand voice matching |

**Default: `standard`**

## Proces

### Krok 1: Diagnoza
Przeczytaj wejście. Wczytaj reguły dla wybranego trybu. Wskaż wzorce GenAI, ryzyka znaczeniowe i miejsca wymagające weryfikacji.

For text mode, read these rule files:
- `rules/text-content.md` — significance inflation, promotional language, vague attributions, formulaic challenges
- `rules/text-language.md` — AI vocabulary, copula avoidance, synonym cycling, false ranges, negative parallelisms, rule of three
- `rules/text-style.md` — em dashes, boldface, inline-header lists, title case, emojis, curly quotes
- `rules/text-communication.md` — chatbot artifacts, sycophancy, disclaimers, filler phrases, hedging, generic conclusions
- `rules/text-structure.md` — structural anti-patterns and how to fix them

For code mode, read these rule files:
- `rules/code-comments.md` — 18 comment anti-patterns
- `rules/code-naming.md` — 14 naming anti-patterns
- `rules/code-commits.md` — 10 commit message anti-patterns
- `rules/code-docstrings.md` — 8 docstring anti-patterns
- `rules/code-quality.md` — error handling, API design, test anti-patterns
- `rules/code-llm-tells.md` — 16 structural code tells

For academic mode, read:
- `/home/ezdies/AntiSlopPL/POLISH_ACADEMIC_CORE.md` — shared Polish academic constraints and anti-GenAI rules
- `rules/academic.md` — Polish academic anti-GenAI rules with section-specific guidance

For voice and soul guidance (all modes), read:
- `guides/voice-and-soul.md` — how to inject personality, not just strip patterns
- `guides/style-template.md` — if deep mode, use this to build a custom voice profile

For scoring reference, read:
- `scoring.md` — unified scoring system

### Krok 2: Rewizja
Usuń lub przebuduj wzorce GenAI. W polskim tekście naukowym dodawaj konkret, rytm i głos autora tylko wtedy, gdy nie narusza to ścisłości. Zachowaj sens, fakty, cytowania, wyniki i kluczowe argumenty.

### Krok 3: Drugie przejście
Zadaj pytanie: *„Co nadal brzmi jak tekst z GenAI?”*
Wypisz pozostałe ślady w krótkich punktach.
Popraw je bez wzmacniania twierdzeń i bez dopisywania źródeł.

To ważny etap. Samo usunięcie fraz modelowych często tworzy tekst sterylny. W polskim artykule naukowym celem jest naturalna precyzja, nie potoczność.

### Krok 4: Raport
Zwróć diagnozę, poprawiony tekst, log zmian i `Do weryfikacji`. Ocena liczbowa jest pomocnicza; priorytetem jest jakość merytoryczna.

## Output Format

### For Text Mode

```
ORIGINAL SCORE: 3.8/10 (AI-heavy)
MODE: text | DEPTH: standard

--- DRAFT REWRITE ---
[first pass rewrite]

--- WHAT'S STILL AI ABOUT THIS? ---
- [remaining tells as brief bullets]

--- FINAL VERSION ---
[second pass rewrite]

FINAL SCORE: 8.4/10 (human-like)

CHANGES MADE:
- Removed 7 hedging phrases ("It's important to note", "arguably")
- Replaced 4 corporate buzzwords ("leverage" -> "use")
- Fixed 3 robotic patterns (parallel structure overuse)
- Added 5 specific examples (replaced vague references)
- Shortened 8 sentences (>40 words -> 15-25 words)

FLAGS FOR MANUAL REVIEW:
- Paragraph 3: Still uses "various" — suggest specific companies
- Paragraph 7: Transition feels abrupt — consider adding context

FILE SAVED: example-HUMAN.md
```

### For Code Mode

```
MODE: code | DEPTH: standard
FILES SCANNED: 3

--- CHANGES ---
src/auth.ts:
  L12: Comment "// Initialize authentication" -> deleted (tautological)
  L34: Variable `userDataObject` -> `user` (verbose compound name)
  L67: Comment "// We validate the input" -> "// Reject expired tokens — see #1234"

COMMIT MSG REWRITE:
  "Enhanced authentication flow with improved error handling"
  -> "reject expired OAuth tokens at middleware boundary"

SCORE: 4.2 -> 8.1
```

### For Academic Mode

```
MODE: academic | DEPTH: standard
JĘZYK: polski
DZIEDZINA: [wykryta lub podana]
SEKCJA: [wykryta lub podana]

--- NAJWAŻNIEJSZE RYZYKA ---
- [sens, cytowania, przyczynowość, zakres, dane]

--- ŚLADY GENAI ---
- "warto zauważyć" — pusty metajęzyk
- "kluczową rolę" — inflacja znaczenia bez mechanizmu
- "ponadto" — mechaniczne przejście bez relacji logicznej

--- POPRAWIONY TEKST ---
[wersja po rewizji]

--- LOG REWIZJI ---
- [3-6 zmian z uzasadnieniem]

--- DO WERYFIKACJI ---
- [brakujące źródła, dane, figury, liczby, ograniczenia]
```

## What Gets Killed (Pattern Summary)

### Text: 24 Core Patterns
1. Significance inflation ("pivotal moment", "testament to")
2. Notability name-dropping (listing outlets without context)
3. Superficial -ing analyses ("highlighting", "showcasing", "ensuring")
4. Promotional language ("vibrant", "nestled", "groundbreaking", "breathtaking")
5. Vague attributions ("experts argue", "industry reports suggest")
6. Formulaic challenges ("Despite X... continues to thrive")
7. AI vocabulary (delve, tapestry, landscape, interplay, foster, garner, pivotal)
8. Copula avoidance ("serves as" instead of "is")
9. Negative parallelisms ("not just X, it's Y")
10. Rule of three (forcing everything into triads)
11. Synonym cycling (rotating words for the same thing)
12. False ranges ("from X to Y" without meaningful scale)
13. Em dash overuse
14. Boldface overuse
15. Inline-header vertical lists
16. Title case in headings
17. Emoji as structure
18. Curly quotation marks
19. Chatbot artifacts ("I hope this helps!", "Let me know if...")
20. Knowledge-cutoff disclaimers
21. Sycophantic tone ("Great question!")
22. Filler phrases ("in order to", "it is important to note")
23. Excessive hedging
24. Generic positive conclusions ("the future looks bright")

### Code: 80+ Patterns Across 6 Domains
- **Comments**: tautological, section headers, narrating obvious intent, hedge TODOs, "we" language, changelog comments, philosophical prose
- **Naming**: verbose compounds, Manager/Handler suffix abuse, Enhanced/Advanced prefixes, process/handle verbs, acronym avoidance, result catch-all
- **Commits**: vague verbs, "various/several", passive voice, past tense, misleading bodies
- **Docstrings**: tautological summaries, type redundancy, weak openings, filler phrases, happy-path only
- **Quality**: broad exception catches, generic error messages, boolean parameters, god functions, mock-heavy tests, happy-path-only tests
- **LLM tells**: commented-out alternatives, symmetrical code, placeholder values, defensive null-checks, tutorial-style comments

### Academic: polskie reguły akademickie
- Grupy A-J obejmują: zachowanie sensu, usuwanie polskich wypełniaczy GenAI, kalki z angielskiego, rytm zdań, głos autora, nominalizacje, metafory, domknięcie logiczne i różnicowanie podmiotów.

## What Gets Added

Not just subtraction. For Polish academic prose, add only what improves precision, logic, or author voice without changing claims.

Read `guides/voice-and-soul.md` for the full guide. For Polish academic text, apply it conservatively:
- **Rytm zdań** — mieszaj krótsze zdania kontrolne z dłuższymi zdaniami analitycznymi.
- **Konkret** — zastępuj ogólnik danymi, metodą, warunkiem albo ograniczeniem, jeśli są dostępne.
- **Głos autora** — zachowuj terminologię, poziom formalności i sposób argumentowania z próbki stylu.
- **Uczciwa niepewność** — nie usuwaj hedgingu, gdy wynika z danych.
- **Kontrolowana szorstkość** — nie wygładzaj każdego akapitu do identycznego rytmu.
- **Bez potoczności na siłę** — nie dodawaj kolokwializmów, skrótów ani „ludzkich reakcji” do tekstu naukowego.

## Configuration

### Preserve Mode
```
/slopbuster document.md --preserve-formal
```
Keeps formal language. Removes obvious cliches only. Target: 7+/10. For white papers, case studies, business docs.

### Academic Mode
```
/slopbuster paper.md --mode academic --field biomedical --section discussion
```
Zachowuje konwencje dziedziny. W metodach strona bierna może zostać. W polskim tekście priorytetem jest ścisłość, naturalna składnia i usunięcie typowych fraz GenAI.

### Code Mode
```
/slopbuster src/ --mode code
```
Scans all source files. Rewrites comments, flags naming issues, suggests commit message fixes.

### Voice Calibration (Deep Mode)
```
/slopbuster doc.md --depth deep --voice-sample author-sample.md
```
Analyzes the voice sample first, builds a style profile, then matches the rewrite to that voice.

## Scoring

See `scoring.md` for the full system. Quick reference:

**Skala jakości anty-GenAI (0-10):**
- **0-3:** Tekst silnie modelowy: ogólniki, puste przejścia, inflacja znaczenia, brak konkretu.
- **4-5:** Tekst mieszany: część zdań działa, ale nadal widać automatyczne wzorce.
- **6-7:** Tekst akceptowalny: sens zachowany, lecz wymaga dopracowania głosu autora.
- **8-9:** Tekst naturalny akademicko: konkretny, ścisły, z minimalną liczbą wzorców GenAI.
- **10:** Tekst brzmi jak praca kompetentnego autora w danej dziedzinie.

**Scoring uses three tiers:**
- Tier 1 (3 pts each): AI-specific tells — "delve into", "tapestry of", sycophancy
- Tier 2 (2 pts each): Corporate/formal buzzwords — "synergy", "leverage", "circle back"
- Tier 3 (1 pt each): Weak signals — generic transitions, mild hedging, marketing language

Silniejsze sygnały waż więcej, ale nigdy nie poprawiaj wyniku kosztem prawdziwości lub stylu autora.

## Sources and Attribution

Built from analyzing 1,000+ AI vs human content samples across marketing, technical, creative, and academic writing. Cross-referenced against peer-reviewed LLM detection research (Kobak et al. 2025, Liang et al. 2024, Juzek & Ward COLING 2025) and Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) (CC BY-SA 4.0).

---

**Usuwa GenAI-slop z prozy, kodu i tekstów naukowych bez poświęcania sensu.**
