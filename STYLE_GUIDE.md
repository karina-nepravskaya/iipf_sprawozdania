# Styl Kariny oraz wymagania IIPF/PFMB

Ten dokument łączy trzy źródła, w tej kolejności:

1. **oficjalny układ raportu:** \`Szablon_TEX_IIPF_PFMB.tex\`;
2. **zalecenia Pracowni Fizycznej UJ:** „Kilka wskazówek dotyczących przygotowywania sprawozdań”, Tomasz Kawalec, październik 2021;
3. styl językowy Kariny z \`main.tex\`, \`raport_praktyka_Nepravskaya_Karina.pdf\` i \`Dlugosc_fali_Nepravskaya_Karina.pdf\`.

Jeżeli styl osobisty jest sprzeczny z formatką albo zaleceniami Pracowni, obowiązuje formatka i zalecenia. Nie improwizuj layoutu.

## Obowiązująca formatka

Punktem wyjścia dla każdego raportu jest \`FORMATKA.tex\`, która zachowuje układ dostarczonego szablonu IIPF/PFMB:

- A4, \`10 pt\`, układ **dwukolumnowy**;
- marginesy: po \`2 cm\` z lewej i prawej, \`1.5 cm\` od góry i \`3 cm\` od dołu;
- pierwszy blok nad dwiema kolumnami: tytuł, autorka z przypisem e-mail, opiekun, nazwa pracowni i data rozpoczęcia;
- streszczenie w wydzielonym bloku na pierwszej stronie;
- strona z numerem na dole, skróconym nazwiskiem w prawym dolnym rogu;
- struktura: **Wprowadzenie**, **Opis eksperymentu**, **Wyniki i ich dyskusja**, **Podsumowanie i wnioski**, **Literatura**, a rachunek niepewności w **Dodatku**;
- maksymalnie **6 stron**, o ile prowadzący nie postanowi inaczej.

Nie dodawaj strony tytułowej ani spisu treści. To nie praca licencjacka, więc nie trzeba robić z sześciostronicowego sprawozdania małej rozprawy.

Dla szerokiego rysunku w dwóch kolumnach użyj środowiska \`figure*\`. Podpis tabeli umieszczaj nad tabelą, a podpis rysunku pod rysunkiem. Każdy rysunek, wykres i tabela muszą mieć odwołanie w tekście głównym albo dodatku.

## Streszczenie

Streszczenie ma najwyżej **200 słów** i zawiera wyłącznie:

1. cel pomiaru;
2. zastosowaną metodę;
3. główne wyniki liczbowe z niepewnościami;
4. opcjonalnie jeden krótki wniosek.

Nie opisuj montowania układu, przebiegu zajęć, kolejnych kliknięć w programie ani tego, że był to eksperyment studencki. Nie zamieszczaj w streszczeniu cytowań ani odnośników do równań, rysunków i tabel.

## Ton i składnia

- Polski techniczny, prosty, konkretny i spokojny.
- Zdania raczej krótkie; jeden akapit rozwija jedną myśl.
- Preferuj dwa pełne zdania zamiast jednego zdania sklejonego średnikiem albo dwukropkiem. Dwukropek stosuj wyłącznie przed rzeczywistym wyliczeniem, definicją albo wyjaśnieniem bezpośrednio wynikającym z poprzedniej części zdania. Średnik stosuj wyjątkowo, gdy dwie części muszą pozostać w jednym zdaniu; w zwykłym opisie zastąp go kropką albo przecinkiem.
- Nie wstawiaj znaku przestankowego w środku myśli tylko po to, aby zdanie brzmiało „bardziej naukowo”. Najpierw sprawdź, czy treść nie będzie jaśniejsza po rozdzieleniu na dwa zdania.
- Bez patosu, marketingu i ozdobników: nie używaj „kluczowy”, „fascynujący”, „niewątpliwie”, „bardzo istotny” ani „znacząco” bez liczbowego uzasadnienia.
- Nie udawaj pewności, której nie dają dane. Zamiast „udowodniono” używaj „otrzymano”, „porównanie wskazuje” albo „wynik jest zgodny w granicach niepewności”.
- Teoria we Wprowadzeniu służy metodzie i interpretacji; nie jest przepisanym fragmentem instrukcji, Wikipedii lub podręcznika.

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

Najpierw napisz, co jest wyznaczane. Następnie wprowadź równanie i zdefiniuj każdy nowy symbol. Każde równanie jest częścią zdania, więc kończy się przecinkiem albo kropką. Stosuj \`\left(\right)\`, \`\left[\right]\` i \`\left\lvert\right\rvert\`, gdy rozmiar nawiasów powinien dopasować się do wyrażenia.

Symbole zapisuj w trybie matematycznym również w zdaniu, np. \`czas $t$\`, \`pęd $p$\`. Symbol w tekście ma wyglądać dokładnie tak jak w równaniu.

Odwołania zapisuj konsekwentnie:

- równanie: „z równania (6) wynika…”;
- literatura: „w pracy [1]…”;
- rysunek: „na rys. 1…” lub \`na rys.~\ref{...}\` — bez nawiasów wokół numeru.

## Liczby, jednostki i niepewności

Obliczenia prowadź z pełną dostępną precyzją. Zaokrąglaj **dopiero wynik końcowy**:

1. niepewność zaokrąglij w górę do dwóch cyfr znaczących;
2. wartość zaokrąglij zwyczajnie do tego samego miejsca dziesiętnego;
3. nie usuwaj końcowego zera, jeżeli informuje ono o precyzji, np. \(51{,}0 \pm 0{,}1\), a nie \(51 \pm 0{,}1\).

Zapisuj liczbę i jednostkę ze spacją nierozdzielającą, prostą czcionką dla jednostki, np. \`\SI{10}{\metre\per\second\squared}\` albo \`\num{10}~\mathrm{m/s^2}\`. Nie zapisuj \`10m/s^2\`.

Oddziel niepewności statystyczne i systematyczne przed ich połączeniem. Szczegółowy rachunek niepewności umieść w Dodatku. Każdy wynik musi mieć jednostkę oraz jasno opisaną definicję niepewności. Jeżeli porównujesz wynik z referencją, pokaż kryterium zgodności i liczby.

## Dopasowania, tabele i wykresy

- W tekście lub podpisie podaj pełną postać dopasowanej funkcji.
- Podaj parametry dopasowania wraz z prawidłowo zaokrągloną niepewnością i jednostką.
- Nie wklejaj surowej tabelki z Origin, Excelu ani innego programu.
- Osie, legenda, liczby i czcionki na wykresie muszą być czytelne w PDF.
- Zestawy danych muszą różnić się także w skali szarości: używaj symboli, stylów linii lub grubości, nie tylko koloru.
- Każdy rysunek i każda tabela muszą zostać omówione w tekście.

## Polska typografia LaTeX

- Łącznik w nazwie złożonej: \`-\`, np. Fabry'ego-Pérota.
- Zakres liczbowy: \`--\` bez spacji, np. \`123--456\`.
- Myślnik w zdaniu: \`---\` ze spacjami po obu stronach.
- Polski cudzysłów: \`,,tekst''\`. Angielski: \`\`text''\`. Nie stosuj prostych \`"tekst"\`.
- Stosuj \`~\` między liczbą i jednostką, po jednoliterowym przyimku oraz tam, gdzie rozdzielenie na końcu wiersza byłoby błędne.

## Końcowa kontrola

Przed oddaniem PDF sprawdź:

- czy dokument mieści się w limicie 6 stron;
- czy streszczenie ma maksymalnie 200 słów i zawiera cel, metodę oraz wyniki z niepewnościami;
- czy wszystkie liczby, jednostki, niepewności i oznaczenia są spójne;
- czy wykresy są czytelne także po wydruku;
- czy w PDF są polskie znaki, litery greckie i poprawnie złożone wzory;
- czy odnośniki, podpisy i bibliografia działają;
- czy dane w raporcie mają źródło w \`data/raw/\` albo w zatwierdzonej analizie;
- czy nie wprowadzono wyniku tylko dlatego, że „ładnie wygląda”.
