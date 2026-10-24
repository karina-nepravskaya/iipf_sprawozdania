# Styl Kariny i wymagania Pracowni dla sprawozdań

Ten dokument łączy trzy źródła, w tej kolejności:

1. **wymagania formalne Pracowni Fizycznej UJ** z dokumentu „Kilka wskazówek dotyczących przygotowywania sprawozdań” (Tomasz Kawalec, październik 2021);
2. **formatka** z `FORMATKA.tex`, zgodna z układem dokumentu `raport_praktyka_Nepravskaya_Karina.pdf`;
3. styl językowy Kariny, wyprowadzony z `main.tex`, `raport_praktyka_Nepravskaya_Karina.pdf` i `Dlugosc_fali_Nepravskaya_Karina.pdf`.

Gdy styl i formalne zalecenie są sprzeczne, obowiązuje zalecenie Pracowni. Nie negocjuj tego z własnym gustem: fizyka eksperymentalna ma dość losowych formatowań.

## Formatka dokumentu

Nowy raport rozpoczynaj od `FORMATKA.tex`. Zachowaj:

- A4, `12pt`, marginesy `2.5 cm`, język polski i kodowanie UTF-8;
- pakiety i ustawienie `siunitx` z przecinkiem dziesiętnym;
- tytuł, autora „Karina Nepravskaya” i datę „Kraków …”;
- streszczenie po tytule;
- podpis **nad tabelą** i **pod rysunkiem**;
- tabelaryczne linie `booktabs`, bez pionowych kresek;
- grafikę wektorową, gdy jest dostępna; grafikę rastrową o rozdzielczości co najmniej 300 DPI, jeśli raport będzie drukowany.

Spis treści dodawaj tylko, gdy raport jest na tyle długi albo instrukcja prowadzącego wyraźnie go wymaga. Nie upychaj tabel przez `\small` tylko po to, żeby „się zmieściło”; najpierw skróć nagłówki, przeorganizuj tabelę albo podziel ją logicznie.

## Streszczenie

Streszczenie zawiera wyłącznie:

1. cel pomiaru,
2. zastosowaną metodę,
3. główne wyniki liczbowe razem z niepewnościami i warunkami istotnymi dla wyniku.

Nie opisuj w nim montowania układu, kolejnych kliknięć w programie, faktu uczestnictwa w ćwiczeniu ani odnośników do literatury, równań, rysunków i tabel. Musi dać się przeczytać osobno. Wzorzec:

> Metodą … wyznaczono … . Dla … otrzymano … .

## Ton i składnia

- Polski techniczny, prosty, konkretny i spokojny.
- Zdania raczej krótkie; jeden akapit rozwija jedną myśl.
- Bez patosu, marketingu i ozdobników: nie używaj „kluczowy”, „fascynujący”, „niewątpliwie”, „bardzo istotny” ani „znacząco” bez liczbowego uzasadnienia.
- Nie udawaj pewności, której nie dają dane. Zamiast „udowodniono” używaj „otrzymano”, „porównanie wskazuje” albo „wynik jest zgodny w granicach niepewności”.
- Teoria służy metodzie i interpretacji. Nie jest streszczeniem podręcznika.

Preferowane konstrukcje:

- „Celem ćwiczenia jest wyznaczenie…”
- „Do pomiaru wykorzystano…”
- „Układ eksperymentalny przedstawiono na rys. …”
- „Ustawiono…, a następnie…”
- „Dla każdej serii pomiarów wyznaczono…”
- „Z otrzymanych punktów sporządzono wykres…”
- „Do danych dopasowano…”
- „Z równania (…) wynika, że…”
- „Ostatecznie otrzymano…”
- „Porównując …, stwierdzono zgodność w granicach …”
- „Na tej podstawie można stwierdzić, że…”

Opis procedury ma czas przeszły i formę bezosobową: „zmierzono”, „zamocowano”, „wykonano zdjęcie”, „przeanalizowano”. Wyniki również opisuj w czasie przeszłym.

## Równania, symbole i odnośniki

Najpierw napisz, co jest wyznaczane. Następnie wprowadź równanie i zdefiniuj każdy nowy symbol. Każde równanie jest częścią zdania, więc kończy się przecinkiem albo kropką. Stosuj `\left(\right)`, `\left[\right]` i `\left\lvert\right\rvert`, gdy rozmiar nawiasów powinien dopasować się do wyrażenia.

Symbole zapisuj w trybie matematycznym również w zdaniu, np. `czas $t$`, `pęd $p$`. Symbol w tekście ma wyglądać dokładnie tak jak w równaniu.

Odwołania zapisuj konsekwentnie:

- równanie: „z równania (6) wynika…”;
- literatura: „w pracy [1]…”;
- rysunek: „na rys. 1…” — bez nawiasów wokół numeru.

## Liczby, jednostki i niepewności

Obliczenia prowadź z pełną dostępną precyzją. Zaokrąglaj **dopiero wynik końcowy**:

1. niepewność zaokrąglij w górę do dwóch cyfr znaczących;
2. wartość zaokrąglij zwyczajnie do tego samego miejsca dziesiętnego;
3. nie usuwaj końcowego zera, jeżeli informuje ono o precyzji, np. (51{,}0 \pm 0{,}1), a nie (51 \pm 0{,}1).

Zapisuj liczbę i jednostkę ze spacją nierozdzielającą, prostą czcionką dla jednostki, np. `\SI{10}{\metre\per\second\squared}` albo `\num{10}~\mathrm{m/s^2}`. Nie zapisuj `10m/s^2`.

Oddziel niepewności statystyczne i systematyczne przed ich połączeniem. Każdy wynik musi mieć jednostkę oraz jasno opisaną definicję niepewności. Jeżeli porównujesz wynik z referencją, pokaż kryterium zgodności i liczby.

## Dopasowania, tabele i wykresy

- W tekście lub podpisie podaj pełną postać dopasowanej funkcji.
- Podaj parametry dopasowania wraz z prawidłowo zaokrągloną niepewnością i jednostką.
- Nie wklejaj surowej tabelki z Origin, Excelu ani innego programu. Taka tabela zwykle nie ma jednostek, kontekstu i sensownego zaokrąglenia.
- Osie, legenda, liczby i czcionki na wykresie muszą być czytelne w PDF.
- Zestawy danych muszą różnić się także w skali szarości: używaj symboli, stylów linii lub grubości, nie tylko koloru.
- Każdy rysunek i każda tabela muszą zostać omówione w tekście oraz odpowiadać na pytanie analizy.

Podpis powinien mówić, co przedstawiono, jakie wielkości porównano i dla jakiego przypadku, np. „Zależność … od … dla …”.

## Polska typografia LaTeX

- Łącznik w nazwie złożonej: `-`, np. Fabry'ego-Pérota.
- Zakres liczbowy: `--` bez spacji, np. `123--456`.
- Myślnik w zdaniu: `---` ze spacjami po obu stronach.
- Polski cudzysłów: `,,tekst''`. Angielski: ```text''`. Nie stosuj prostych `"tekst"`.
- Stosuj `~` między liczbą i jednostką, po jednoliterowym przyimku oraz tam, gdzie rozdzielenie na końcu wiersza byłoby błędne.

## Końcowa kontrola

Przed oddaniem PDF sprawdź:

- czy streszczenie zawiera cel, metodę i wyniki z niepewnościami;
- czy wszystkie liczby, jednostki, niepewności i oznaczenia są spójne;
- czy wykresy są czytelne także po wydruku;
- czy w PDF są polskie znaki, litery greckie i poprawnie złożone wzory;
- czy odnośniki, podpisy i bibliografia działają;
- czy dane w raporcie mają źródło w `data/raw/` albo w zatwierdzonej analizie;
- czy nie wprowadzono wyniku tylko dlatego, że „ładnie wygląda”.
