# Analiza przed napisaniem sprawozdania Z40/Z34

**Status: DO ZATWIERDZENIA. Etap 1.** Dokument jest planem opracowania danych, a nie gotowym sprawozdaniem. Nie zmieniono `report/main.tex`, wyznaczono jedynie warunkowe oszacowanie lokalnej gęstości strumienia neutronów i nie wpisano wyniku zastępczego za brakujące parametry geometrii i aktywacji.

## 1. Cel, zakres i wymagania

Głównym celem jest identyfikacja linii gamma w widmach próbek aktywowanych przez źródło AmBe, wyznaczenie wydajności pełnoenergetycznej detektora HPGe z pomiaru $^{152}\mathrm{Eu}$, a następnie ocena, czy dane folii o znanych masach pozwalają wyznaczyć **lokalną gęstość strumienia neutronów**. Widma Cs, Co, Mn, Na, I, monet i Cu będą pokazane poglądowo. Obliczenia ilościowe obejmują Eu oraz drugi pomiar Au potrzebny do wyznaczenia strumienia.

| Źródło | Wymaganie i decyzja dla tych danych |
|---|---|
| Z40, s. 1, cel i §1 | Widma aktywacyjne, identyfikacja nuklidów, oszacowanie lokalnego strumienia. Zakres raportu ograniczyć do zarejestrowanych widm i folii. |
| Z40, s. 3–4, równania (9)–(15) | Równanie aktywacji, chłodzenie, czas zliczania, intensywność linii i wydajność zależna od geometrii. |
| Z40, s. 4–5, §5 pkt 1–6 | Kalibracja energetyczna, czas martwy, kalibracja wydajnościowa, zapis czasów aktywacji i pomiaru, długi pomiar tła. Napięcie detektora było już włączone przed wejściem. |
| Z40, s. 5, §6 pkt 1–5, 8 | Kalibracja widm i tła, wydajność, pola linii po uwzględnieniu tła, identyfikacja izotopów, strumień i błędy systematyczne. Wybrać tylko zadania poparte zebranymi danymi. |
| Z40, s. 6, dodatek A.1, równanie (16); s. 7, rys. 5 | Proponowana parametryzacja $\ln\varepsilon$ wielomianem trzeciego stopnia w $\ln E$; tablica linii i parametrów aktywacji. Sprawdzić sens fizyczny i zakres stosowania dopasowania. |
| Z34, s. 1–2, „Program ćwiczenia” i „Opracowanie wyników” | Metoda dopasowania Gaussa potrzebna do wyznaczenia pól Eu i drugiego Au; pozostałe widma bez dodatkowego dopasowywania pików. |
| Uwagi prowadzącego przekazane w opisie doświadczenia | Widma Cs/Co można opisać krótko jako pomocnicze. Priorytetem jest trzecie widmo Eu z odległości około 16,9 cm. Pola pików należy wyznaczyć dopasowaniem do binów. |

W Z40, s. 1, przytoczono emisję całego źródła około $(7{,}7\pm1{,}5)\cdot10^5\ \mathrm{n/s}$ dla aktywności Am $12{,}95\ \mathrm{GBq}$. Jest to **wydajność źródła** $Q$, a nie $\phi$ przy folii w $\mathrm{cm^{-2}s^{-1}}$. Porównanie liczbowe wymaga osobnego modelu transportu i geometrii osłony. Nie wolno dobierać odległości efektywnej ani czasu aktywacji tak, aby wynik „wyszedł” równy $Q$.

## 2. Fakty o rzeczywistym doświadczeniu

1. Detektor HPGe był już włączony przed rozpoczęciem pracy. Tukan miał wcześniejszą kalibrację energii. Zarejestrowano widma Cs i Co w kilku położeniach, sprawdzając położenia pików i czas martwy. Zeszyt (s. 1–2) opisuje m.in. położenie najbliższe, środkowe oraz źródło przy górze detektora. Przy bardzo bliskim Cs czas martwy przekroczył 40%. Pomiary służyły też nauce obsługi układu. Nie przypisywać grupie włączenia detektora lub stworzenia pierwotnej kalibracji.
2. Zmierzono trzy widma $^{152}\mathrm{Eu}$ (zeszyt, s. 3–5). Trzeci pomiar wykonano około 16,9 cm od powierzchni detektora, z czasem żywym 522 s i rzeczywistym 526 s. To pomiar wybrany do kalibracji wydajnościowej. W notatce położenia wielu linii w tym widmie są o około 2 keV poniżej wartości świadectwa, np. 409,09 zamiast 411,1 keV. W dniu późniejszych pomiarów wykonano też osobny pomiar Eu i poprawiono/zweryfikowano kalibrację. Zeszyt (s. 6) notuje pozostałą różnicę około 0,2 keV dla przykładowej linii.
3. Przed pomiarami aktywacyjnymi zarejestrowano tło przez 69 260 s czasu żywego i 69 305 s rzeczywistego. W `pomiar_tlo_2026_10_23.dat` jest jeden słupek zliczeń na kanał 0–2047. Kalibrację energii należy przypisać z kanałów i zweryfikować względem widm z tej samej konfiguracji.
4. Z osłony AmBe wyjęto wcześniej napromienioną monetę i zarejestrowano jej widmo. W osłonie znajdowały się też Mn i I. Folie Au i Cu przymocowano symetrycznie przy dolnej i górnej stronie walcowego źródła AmBe, po czym aktywowano je podczas pozostałych pomiarów. Fotografia komory dokumentuje jej zewnętrzny wygląd i otwory, ale nie daje wymiarów wewnętrznych ani odległości folia–aktywny obszar źródła.
5. Pierwszy pomiar Mn pokazał linię około 847 keV. Po zmianie zakresu/wzmocnienia zmierzono Mn ponownie. Pierwotny eksport zapisany obecnie jako `Mn_zakres_2_oryginalny.lst` przypisywał maksimom w kanałach 466, 996 i 1162 około 338, 722 i 843 keV. Na prośbę użytkownika kolumnę energii w `Mn_zakres_2.lst` przeliczono liniowo z trzech punktów pliku `.clb`, zachowując nagłówek, numery kanałów i wszystkie zliczenia. Z punktów `kalibracja_Mn_Na_zakres2.clb` wynika $E(k)\simeq1{,}81930k-1{,}3474$ keV. Daje to dla tych kanałów około 846,45, 1810,68 i 2112,68 keV. Pierwsza linia 847 keV była punktem tej kalibracji, a pozostałe dwie są jej niezależną kontrolą. Są to wstępne maksima binów, nie centroidy z dopasowania. Widmo Na ma maksima w kanałach 282 i 701, zgodne z nowym zakresem i liniami 511 oraz 1274,6 keV. Widmo I pozostaje na starym zakresie (pik około kanału 612 odpowiada około 443 keV). Dlatego Na i I **nie mają tej samej kalibracji**, mimo że oba eksporty mają po dwie kolumny.
6. Zmierzono drugą monetę. Au aktywowano przez około 3,5 h, a Cu przez około 4 h. Są to szacunki, więc ich precyzja musi wejść do analizy wrażliwości. Masy z fotografii etykiet i potwierdzenia użytkownika: $m_{\rm Au}=0{,}1328\ \mathrm{g}$ i $m_{\rm Cu}=0{,}1479\ \mathrm{g}$. W rachunku mają być przyjęte jako dokładne dane wejściowe zgodnie z podaną konwencją, co należy wyraźnie zaznaczyć w sprawozdaniu.
7. Pierwszy pomiar Au wykonano około 16,9 cm od powierzchni HPGe. Nie zauważono w nim wyraźnego piku 412 keV. Od oderwania folii od AmBe do początku tego pomiaru minęło 61 s. Następnie folię umieszczono na powierzchni obudowy detektora. Drugi pomiar rozpoczął się według relacji po dalszych 17 min 03 s, czyli $t_{c,2}=1084$ s od wyjęcia. Nagłówki plików dają odstęp między początkami pomiarów 1016 s, a więc $61+1016=1077$ s. Różnica wynosi 7 s i należy ją oznaczyć jako niejednoznaczność, bez ukrytego poprawiania danych. Cu zmierzono na powierzchni obudowy po około 60 s od wyjęcia. Jej chłodzenie nie było zmierzone dokładnie.
8. Dwa widma Au nie tworzą serii zaniku o stałej geometrii, ponieważ między nimi zmieniono odległość. Linia 511 keV w widmie Cu służy tylko jakościowej identyfikacji. Lokalny strumień neutronów będzie oceniany ilościowo z Au.

W samym raporcie **nie dzielić opisu na pierwszy i drugi dzień**. Przedstawić ciągłą, bezosobową procedurę: pomiary kalibracyjne i tła, wcześniejszą aktywację próbek przez AmBe, rejestrację widm i zmianę zakresu tam, gdzie jest istotna dla osi energii. Nie opisywać niewykonanych pomiarów.

## 3. Materiały i mapa danych

Wszystkie ścieżki w tabeli są względem `cwiczenia/Z40_34/`. Pliki `data/raw/` pozostają bez zmian.

| Pliki | Zawartość i rola |
|---|---|
| `instructions/Z40.pdf`, `Z34.pdf` | Instrukcje, odpowiednio model aktywacji i wymagania pracy z detektorami. |
| `instructions/swiadectwo_wzorcowania_Eu.HEIC` | Świadectwo BW/Z-62/154/17, s. 2/2. $A_0=(101{,}3\pm2{,}4)\ \mathrm{kBq}$ na 01.01.2018, godz. 12:00 CET. $T_{1/2}=(13{,}522\pm0{,}016)$ roku. Część aktywna ma średnicę 4 mm, oprawa średnicę 12 mm i wysokość 3 mm. Świadectwo podaje energie i intensywności linii Eu, m.in. 121,8, 344,3, 778,9, 964,1, 1112,1 i 1408,0 keV. Niepewności intensywności nie są podane na widocznej stronie. |
| `instructions/zdjecia_zeszytu_laboratoryjnego.pdf`, `zdjecie_folii_masy.jpg`, `zdjecie_komory.jpg` | Notatki, masy, odległości i położenie próbek. Przejrzano komplet siedmiu stron zeszytu oraz fotografie folii i komory, dostarczone również bezpośrednio w rozmowie. S. 1–2 dokumentują Cs/Co, s. 3–5 Eu i notatki o wydajności, s. 6–7 pomiary aktywacyjne i masy. Fotografia etykiet potwierdza 0,1328 g Au i 0,1479 g Cu. Fotografia komory nie podaje odległości folii od aktywnej części AmBe. |
| `instructions/Aktywacja_neutronowa_mat_dodatkowe.pdf` | Pełniejsza wersja materiału Z40: s. 1 podaje rozmiar kapsuły AmBe 17,4 × 19,2 mm i osłonę parafinową z Cd/stalą; s. 4, równania (9)–(14), podaje model aktywacji i wymóg transferu geometrii wydajności. Załącznik 1 ma krzywą dla **źródła objętościowego walca ok. 4 cm wysokości**, której nie wolno podstawiać do Eu/folii. Wydrukowane równanie zamienia role $\ln E$ i $\ln\varepsilon$ względem wykresu. Załącznik 3 potwierdza Au: $\sigma=98{,}8\ \mathrm b$, $I=0{,}95$, $T_{1/2}=232675{,}2\ \mathrm s$, $M=196{,}967\ \mathrm{g/mol}$, a także linię I 442,9 keV. Tabela Mn zawiera niespójny półokres „154,8 s” (wartość odpowiada minutom). |
| `instructions/charakterystyka_detektora_GMX25P4-70.png` | Załącznik 2 do aparatury: średnica kryształu Ge 53 mm, długość 70 mm, szczelina przy przednim oknie 3 mm, okno 0,03 mm Al/Mylar. Wartość „relative efficiency 28%” dotyczy Co-60 przy 1,33 MeV w geometrii testowej, nie wydajności bezwzględnej Au przy 412 keV. |
| `data/raw/Cs137/`, `Co60/` | Widma z 16.10. Pomocnicza kontrola położenia linii 661,7, 1173,2 i 1332,5 keV, czasu martwego i odległości. Dodatkowy katalog `ylicyenia/` zawiera kopie części `.lst`, a nie nowe serie. |
| `data/raw/Eu/Eu_1)_…`, `Eu_2_…`, `Eu_3_…` | Trzy widma Eu z 16.10. Trzecie: 522 s czasu żywego, 526 s rzeczywistego, początek 13:21:12. To podstawowy zbiór dla $\varepsilon(E)$. |
| `data/raw/23-10-2026 Eu/pomiar1.lst` | Eu z 23.10, 517/520 s, początek 08:51:55. Kontrola położenia linii w dniu pomiarów aktywacyjnych. Nie zamieniać bez wyjaśnienia z trzecim Eu z 16.10. |
| `data/raw/kalibracja_Europem152_zakres1.clb`, `kalibracja_Mn_Na_zakres2.clb` | Binarne punkty kalibracji Tukana dla dwóch zakresów. Drugi plik zawiera pary kanał–energia: (281,67; 511,0 keV), (466,21; 847,0 keV), (701,38; 1274,6 keV). Dla Mn w drugim zakresie i Na użyć tej skali; dla I pierwszej. |
| `data/raw/pomiar_tlo_2026_10_23.dat`, `.wdm` | Tło 2048 kanałów, zliczenia i metadane czasowe. `.wdm` jest plikiem natywnym Tukana, nie tabelą CSV. |
| `data/raw/mangan/Mn_zakres_1.*`, `Mn_zakres_2.*`; `Na_zakres2/`; `jod/` | Dwa pomiary Mn, Na w szerszym zakresie i I na starszej skali. Eksporty Na oraz I mają po dwie kolumny, ale maksima kanałowe Na 282 i 701 wskazują nową kalibrację, a pik I około kanału 612 starą. Oryginał `Mn_zakres_2_oryginalny.lst` ma nieaktualną energię (krok około 0,726 keV/kanał). W `Mn_zakres_2.lst` energię obliczono jako $E(k)=1{,}8193024734k-1{,}3474341942$ keV i zapisano do czterech miejsc po przecinku, z zachowaniem zliczeń. Notebook powinien niezależnie odtworzyć i zweryfikować tę oś z `.clb`. |
| `data/raw/moneta/`, `moneta2/` | Dwa osobne pomiary monet. Początki 09:04:07 (4336/4340 s) i 12:29:29 (1499/1500 s). Nie zakładać, że monety mają ten sam skład. |
| `data/raw/zlota folia_pierwsza odleglosc/`, `zlota folia_druga odleglosc/`, `miedz folia_druga odleglosc/` | Au daleko i w kontakcie, Cu w kontakcie. Początki odpowiednio 12:56:16 (955/956 s), 13:13:12 (1392/1393 s), 13:39:29 (1819/1821 s). Au daleko było około 16,9 cm od obudowy, drugie Au i Cu leżały na niej. Nazwy katalogów nie definiują odległości efektywnej wewnątrz HPGe. |

`.lst` zawiera nagłówek `$DATE_MEA`, `$MEAS_TIM` (najpierw czas żywy, potem rzeczywisty) i zliczenia na kanał. Część plików zawiera także kolumnę energii z eksportu. Należy walidować liczbę 2048 kanałów, kolejność kolumn, duplikaty i sumy zliczeń. Przykładowo Cs nr 5 ma 619/1046 s, czyli około 40,8% czasu martwego; nie jest odpowiednim widmem do precyzyjnej kalibracji bez kontroli efektów obciążenia.

## 4. Model fizyczny i definicje

**Kalibracja energii.** Kanał przelicza się na energię według $E(k)=ak+b$, osobno dla dwóch ustawień elektroniki. Punkty zapisane w `.clb` wyznaczają współczynniki $a,b$. Dopasowanie Gaussa do binów z lokalnym tłem jest potrzebne ilościowo dla Eu i drugiego pomiaru Au; widma pomocnicze pokazać bez dalszego dopasowywania pików.

**Eu i wydajność.** Aktywność w chwili pomiaru wynosi $A_{\rm Eu}(t)=A_0\exp(-\lambda_{\rm Eu}\Delta t)$, $\lambda_{\rm Eu}=\ln2/T_{1/2,\rm Eu}$. $A_0$ to aktywność ze świadectwa, $\Delta t$ czas od daty wzorcowania. Dla linii o prawdopodobieństwie emisji $I_\gamma$ na rozpad i polu netto $N_\gamma$ wydajność pełnoenergetyczna w **geometrii Eu** to w przybliżeniu $\varepsilon_{\rm Eu}(E)=N_\gamma/(A_{\rm Eu}I_\gamma t_{\rm live})$. Dla długiego półokresu Eu zmiana aktywności podczas kilkuminutowego pomiaru jest pomijalna, co zostanie policzone i jawnie stwierdzone. Na podstawie punktów przetestować $\ln\varepsilon=c_3(\ln(E/\mathrm{keV}))^3+c_2(\ln(E/\mathrm{keV}))^2+c_1\ln(E/\mathrm{keV})+c_0$ (Z40, równanie (16)); $c_j$ są bezwymiarowe. Nie ekstrapolować poza linie Eu. W rachunku niepewności punktu uwzględnić $u(N)$ oraz $u(A)$, przyjmując $I_\gamma$ i $t_l$ jako dane dokładne.

**Aktywacja folii.** Dla stałej lokalnej gęstości strumienia $\phi$ ($\mathrm{n\,cm^{-2}s^{-1}}$) i cienkiej próbki liczba jąder docelowych to $N_p=m g N_A/M$, gdzie $m$ jest masą pierwiastka w g, $g$ abundancją izotopową, $M$ masą molową w g/mol, $N_A$ stałą Avogadra. Przekrój czynny $\sigma$ trzeba podać w $\mathrm{cm^2}$ ($1\ \mathrm{b}=10^{-24}\ \mathrm{cm^2}$). Dla czasu aktywacji $t_a$, chłodzenia $t_c$ i pomiaru $t_r$ oczekiwane pole piku to

$$
N_\gamma=\frac{t_l}{t_r}\,\varepsilon_{\rm foil}(E)I_\gamma\,\frac{\sigma\phi m g N_A}{M\lambda}\,(1-e^{-\lambda t_a})e^{-\lambda t_c}(1-e^{-\lambda t_r}),\qquad \lambda=\frac{\ln2}{T_{1/2}}.
$$

Tutaj $t_l$ jest czasem żywym, $t_r$ rzeczywistym. Czynnik $t_l/t_r$ jest przybliżeniem przy równomiernym rozkładzie strat podczas pomiaru. Jeśli Tukan ma inny model korekty, trzeba go sprawdzić. Po przekształceniu otrzymuje się $\phi$, **nie** całkowitą emisję źródła. Dla Au użyć $^{197}\mathrm{Au}(n,\gamma)^{198}\mathrm{Au}$, linii około 412 keV. Dla Cu rozważyć $^{63}\mathrm{Cu}(n,\gamma)^{64}\mathrm{Cu}$, ale 511 keV pochodzi z anihilacji i jest nieswoiste. Z40, s. 7, podaje orientacyjnie $\sigma_{\rm Au}=98{,}8\ \mathrm b$, $T_{1/2,\rm Au}=232675{,}2\ \mathrm s$, $g_{\rm Au}=1$, $I_{\rm Au}\approx0{,}95$, a dla $^{63}\mathrm{Cu}$ $\sigma=4{,}5\ \mathrm b$, $T_{1/2}=46080\ \mathrm s$, $g=0{,}6915$ i wpis $I_{511}=0{,}38$. W tym opracowaniu 511 keV służy tylko identyfikacji jakościowej. Nie wyznaczać strumienia z Cu. Tabela Z40 dla $^{56}\mathrm{Mn}$ podaje $154{,}8$ pod nagłówkiem sekund, co wygląda na pomyłkę jednostki (wartość odpowiada minutom). Nie przenosić tej liczby do obliczeń zaniku bez weryfikacji.

**Przeliczenie wydajności do geometrii folii.** Eu zmierzono 16,9 cm od powierzchni obudowy, a folie położono na niej. Z charakterystyki detektora wynika 3 mm odstępu okno–kryształ oraz 70 mm długości kryształu. Dla uproszczonego prawa odwrotnych kwadratów przyjęto efektywną płaszczyznę w połowie długości kryształu. Daje to $d_0=0{,}3+7{,}0/2=3{,}8\ \mathrm{cm}$ i $G=[(16{,}9+d_0)/d_0]^2=29{,}674$. Zatem $\varepsilon_{\rm folia}(E)=G\varepsilon_{\rm Eu}(E)$. Jest to **założenie**, a nie zmierzona głębokość oddziaływań gamma. Podstawienie samych 3 mm dawałoby dla Au wydajność ponad 1, co jest niemożliwe. Dla bliskiej folii prawo $1/r^2$ jest tylko przybliżeniem; model nie obejmuje jej rozmiarów i odpowiedzi detektora zależnej od kąta. Nie porównywać uzyskanego lokalnego $\phi$ w $\mathrm{n\,cm^{-2}s^{-1}}$ bezpośrednio z emisją całego AmBe w $\mathrm{n/s}$.

## 5. Notebook analizy i dalsze kontrole

1. W notebooku wczytać widma, tło i obie kalibracje z `.clb`. Zweryfikować poprawioną oś energii drugiego Mn, zachowując surowe zliczenia bez zmian.
2. Dla trzeciego Eu dopasować Gaussa do **wszystkich 13 linii gamma wymienionych w świadectwie**. Po odjęciu przeskalowanego długiego tła wyznaczyć pola netto $N\pm u(N)$, aktywność Eu w dniu pomiaru i punkty $\varepsilon(E)$. Do wszystkich punktów dopasować wielomian w logarytmach z instrukcji Z40.
3. Dla folii obliczyć z tej krzywej $\varepsilon_{\rm Eu}(411{,}8\ \mathrm{keV})$ oraz orientacyjnie $\varepsilon_{\rm Eu}(511{,}0\ \mathrm{keV})$. Obie wartości przeliczyć na geometrię folii przez $G=29{,}674$. Linię 511 keV w Cu pokazać wyłącznie jakościowo. Drugi Au wymaga osobnego dopasowania pola netto po odjęciu tła do wzoru aktywacji.
4. Cs, Co, Mn, Na, I, monety, pierwszy Au i Cu przedstawić jako widma poglądowe. W pierwszym Au pik około 412 keV nie jest rozróżnialny od tła. Cel rejestracji widm pomocniczych opisać w raporcie w 2–3 zdaniach, bez tabel pól, centroidów i osobnych analiz.
5. W rachunku Au przyjąć $t_a\approx3{,}5\ \mathrm h$, $t_c=1084\ \mathrm s$ oraz masę $0{,}1328\ \mathrm g$. Czas Cu około 4 h i chłodzenie około 60 s podać w opisie pomiaru bez obliczania strumienia z Cu.

### Wyniki robocze odtwarzalne z notebooka

Aktywność Eu podczas trzeciego pomiaru wynosi $A\approx64{,}56\ \mathrm{kBq}$. Dla wszystkich 13 linii ze świadectwa obliczono wydajności punktowe po odjęciu tła. Dopasowania lokalne linii 121,8 i 1085,8 keV mają większe odchylenia od modelu Gaussa z prostą; punkty pozostawiono na wykresie zgodnie z przyjętym zakresem analizy. Wielomian dopasowany do tych punktów daje $\varepsilon_{\rm Eu}(411{,}8\ \mathrm{keV})\approx0{,}0013872$ z warunkową $u\approx0{,}0000646$. Dla folii Au przy $d_0=3{,}8\ \mathrm{cm}$ uzyskuje się $\varepsilon_{\rm Au}(411{,}8\ \mathrm{keV})\approx0{,}04116$. W okolicy 511 keV analogiczne przybliżenie daje $\varepsilon_{\rm folia}(511{,}0\ \mathrm{keV})\approx0{,}03409$, ale widmo Cu służy tylko poglądowo.

Drugi pomiar Au po odjęciu tła daje $N=(198{,}5\pm20{,}1)$ zliczeń. Dla przyjętych czasów i wydajności wzór aktywacji daje warunkowo $\phi=(2480\pm277)\ \mathrm{n\,cm^{-2}s^{-1}}$. Ta niepewność obejmuje jedynie pole Au i wydajność Eu przy ustalonym $G$; nie obejmuje niepewności założonego położenia efektywnej płaszczyzny detekcji ani widma neutronów. Pierwszy pomiar Au z większej odległości nie pokazuje rozróżnialnego piku około 412 keV.

## 6. Niepewności w przyjętym rachunku

Surowe zliczenia w kanałach są zapisanymi liczbami całkowitymi. Niepewność podajemy dla **pola piku netto** $N$, które jest wynikiem dopasowania Gaussa do widma po odjęciu przeskalowanego tła i lokalnego kontinuum. $u(N)$ pochodzi z dopasowania; nie dopisujemy niepewności do każdego surowego wpisu w tabeli.

| Wielkość | Przyjęty rachunek |
|---|---|
| Pole piku $N$ | Od widma odejmujemy pomiar tła w skali $t_{l,\rm próbka}/t_{l,\rm tło}$; dopasowujemy Gaussa i lokalną prostą. Podajemy $N\pm u(N)$ dla pola netto. |
| Aktywność Eu $A$ | $A=A_0 2^{-\Delta t/T_{1/2}}$. Dla danych ze świadectwa uwzględniamy $u(A_0)$ i $u(T_{1/2})$ zwykłym przeniesieniem niepewności. Ponieważ na widocznej stronie nie podano współczynnika rozszerzenia, wariant liczbowy $u(A)$ zakłada $k=1$. |
| Wydajność $\varepsilon=N/(A I_\gamma t_l)$ | $u(\varepsilon)=\varepsilon\sqrt{[u(N)/N]^2+[u(A)/A]^2}$. Prawdopodobieństwo emisji $I_\gamma$ i czas żywy $t_l$ przyjmujemy dokładne w tym rachunku. Niepewność wartości krzywej blisko 411,8 keV szacujemy z najbliższej linii Eu 411,1 keV i $u(A)$. |
| Strumień lokalny $\phi$ z Au | Przy ustalonej geometrii i danych tablicowych $u(\phi)=\phi\sqrt{[u(N_{\rm Au})/N_{\rm Au}]^2+[u(\varepsilon_{\rm Eu})/\varepsilon_{\rm Eu}]^2}$. $I_\gamma$, $t_l$, masę i pozostałe zadane liczby traktujemy tu jako dokładne. Współczynnik geometryczny $G$ przyjęto z opisanego założenia jako ustalony. |

Masy Au $0{,}1328\ \mathrm g$ i Cu $0{,}1479\ \mathrm g$ pochodzą z etykiet. Niepewność liczbowa strumienia jest **warunkowa**: nie obejmuje ograniczeń modelu geometrycznego ani przybliżenia przekroju czynnego dla pola AmBe. Ograniczenia geometrii zaznaczamy w opisie wyniku. W sprawozdaniu wystarczy zwięzły przykład przeniesienia niepewności dla $\varepsilon$ i $\phi$.

## 7. Plan wykresów, tabel i wyników

| Element | Funkcja |
|---|---|
| Widma pomocnicze | Pokazać wybrane Cs, Co, Mn, Na, I, monety, pierwszy Au i Cu z osiami i jednostkami. Dodać 2–3 zdania o nauce obsługi układu, sprawdzeniu zakresu energii i rejestracji próbek aktywowanych. Bez tabel dopasowań. |
| Eu i krzywa wydajności | Tabela 13 linii: energia, intensywność, pole netto i wydajność. Wykres punktów z krzywą Z40 dla 16,9 cm. |
| Drugi Au i strumień | Fragment widma po odjęciu tła, dopasowanie Gaussa, pole netto, przeliczenie wydajności przez $G$ i warunkowy lokalny strumień. |
| Pierwszy Au i Cu | Pokazać widma poglądowo; w pierwszym Au pik 412 keV jest nierozróżnialny od tła, w Cu linia 511 keV stanowi wskazówkę jakościową. |

## 8. Proponowany układ raportu w etapie 2

Zgodnie z `FORMATKA.tex` i `STYLE_GUIDE.md`: blok tytułowy i streszczenie do 200 słów; **Wprowadzenie** (zwięzły model i cel), **Opis eksperymentu** (ciągły, bezosobowy opis pomiarów kalibracyjnych, aktywacji AmBe, tła, geometrii i rejestracji), **Wyniki i ich dyskusja** (kalibracja, Eu, widma próbek i warunkowy strumień z Au), **Podsumowanie i wnioski**, **Literatura**, **Dodatek** (rachunek i założenia niepewności). Dwie kolumny, do 6 stron. Nie rozdzielać przebiegu na dni. Nie pisać o niezrealizowanym porównaniu detektorów Z34, warstwach absorbenta ani innych niewykonanych punktach instrukcji. Wymienić tylko wykonane czynności i dostępne pomiary.

## 9. Rozstrzygnięte kwestie i pozostające ograniczenia

- Folie znajdowały się po przeciwnych stronach walcowego AmBe. Potwierdzono masy Au 0,1328 g i Cu 0,1479 g. Czasy aktywacji to szacunki około 3,5 h i 4 h.
- Dla drugiego Au przyjęto chłodzenie 1084 s na podstawie relacji z doświadczenia. Nagłówki pomiarów wskazują 1077 s; różnica 7 s ma mały wpływ wobec innych przybliżeń.
- Współczynnik $G$ z $d_0=3,8$ cm opiera się na założeniu, że połowa długości kryształu może reprezentować efektywną głębokość. Karta detektora nie potwierdza tego jako rzeczywistej głębokości pochłaniania. Bliska geometria ogranicza wiarygodność modelu $1/r^2$.
- Świadectwo Eu nie wyjaśnia na widocznej stronie, czy zapisane $\pm2,4\ \mathrm{kBq}$ jest niepewnością standardową czy rozszerzoną. Wyniki liczbowe przyjmują ją jako standardową. Intensywności linii i czasy żywe potraktowano jako dokładne dane wejściowe w tym rachunku.

**Rekomendacja:** w raporcie skupić rachunek na Eu i drugim Au; resztę widm pokazać poglądowo. Wynik strumienia nazwać orientacyjnym i podać przyjęte $d_0=3,8$ cm. Etap 2 rozpocząć dopiero po zatwierdzeniu analizy.
