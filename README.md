# IIPF — sprawozdania

Repozytorium do przygotowywania sprawozdań laboratoryjnych na kierunku **Fizyka dla Firm, UJ**.

Każde ćwiczenie ma niezależny katalog w `cwiczenia/`. Punkt startowy to `cwiczenia/00_szablon_cwiczenia/`. Należy go skopiować i zmienić nazwę, np. na `01_dlugosc_fali`.

## Zasada pracy: dwa etapy

1. **Analiza.** Agent czyta instrukcję prowadzącego, rzeczywisty przebieg doświadczenia, dane i wymagania. Następnie tworzy `analysis/ANALIZA.md`. Dokument wskazuje fakty, obliczenia, niepewności, plan wykresów, strukturę raportu oraz braki danych. Na tym etapie agent **nie pisze raportu**.
2. **Raport.** Dopiero po wpisaniu `ZATWIERDZONE` w `analysis/DECYZJA.md` agent przygotowuje `report/main.tex`, tworzy wykresy i kompiluje PDF.

Pełne reguły są w [AGENTS.md](AGENTS.md). Styl polszczyzny jest opisany w [STYLE_GUIDE.md](STYLE_GUIDE.md).

## Układ ćwiczenia

- `brief/` — opis rzeczywistego przebiegu oraz wymagania prowadzącego zapisane własnymi słowami;
- `instructions/` — oryginalne instrukcje, najczęściej PDF;
- `data/raw/` — niezmieniane dane pomiarowe i zdjęcia;
- `data/processed/` — dane po obróbce oraz skrypty obliczeń;
- `figures/` — wykresy i fotografie użyte w raporcie;
- `analysis/` — analiza przed zatwierdzeniem;
- `report/` — źródła LaTeX i końcowy PDF;
- `notes/` — robocze notatki, pytania i komunikacja po zajęciach.

Nie wpisuj ręcznie wartości do `report/main.tex`, jeśli mają źródło w tabeli lub obliczeniu. Wyniki muszą dać się prześledzić do `data/raw/` albo do opisanego faktu z przebiegu doświadczenia.
