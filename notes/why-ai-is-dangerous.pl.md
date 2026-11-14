# Dlaczego prośba do maszyny jest niebezpieczna?

Co dostajesz, gdy maszyna spełnia twoją prośbę co do słowa?

Ta notatka stawia 1 tezę o pracy z maszyną. Notatka jest zapisana w Polszczyźnie Kontrolowanej (PK). Notatka ma budowę rozdziału z tekstu [„Perfekcja – koniec ludzkości?”](https://github.com/maciejszulia/philosophy): zjawisko, teza, słabe miejsce tezy, pytania.

> Legenda: PK to polski z regułami, po których zdanie ma 1 znaczenie. „Albo” znaczy: dokładnie 1 z członów. POWINIEN to zalecenie. NIE WOLNO to zakaz. Słowo „Teza” oznacza twierdzenie bez pomiaru. Słowo „maszyna” obejmuje program, który język potoczny nazywa sztuczną inteligencją (AI).

## Słownik

| Termin | Definicja | Słowa zakazane dla tego pojęcia |
|---|---|---|
| maszyna | Maszyna oznacza układ zbudowany przez człowieka, który wykonuje obliczenia. | sztuczna inteligencja, robot |
| prośba | Prośba oznacza tekst, który człowiek daje maszynie jako opis wyniku. | polecenie, życzenie |
| zamiar | Zamiar oznacza stan świata, którego człowiek chce po spełnieniu prośby. | intencja, pragnienie |
| wynik | Wynik oznacza stan świata, który maszyna wytwarza po prośbie. | odpowiedź, rezultat |
| zbiór P | Zbiór P oznacza zbiór wyników, które spełniają słowa prośby. | zakres prośby |
| zbiór C | Zbiór C oznacza zbiór wyników, których człowiek chce. | zakres zamiaru |

## Zjawisko

Termostat utrzymuje 20 °C przy czujniku. Człowiek siedzi przy oknie, 4 m od czujnika. Przy oknie jest 17 °C. Termostat spełnia zapis: 20 °C przy czujniku. Termostat nie zna zamiaru człowieka: ciepła przy oknie.

Owidiusz zapisał to samo zjawisko w poemacie „Metamorfozy”[^ovid]. Król Midas prosi boga o dar: każda rzecz, której Midas dotknie, ma stać się złotem. Bóg spełnia prośbę co do słowa. Chleb w ręku Midasa staje się złotem. Midas dostał wynik, który spełnia słowa prośby. Midas chciał innego wyniku.

## Zapis w logice zbiorów

Prośba dzieli zbiór P na 2 rozłączne części:

$$P = (P \cap C) \cup (P \setminus C) \qquad (1)$$

- $P \cap C$: wyniki, które spełniają słowa prośby i których człowiek chce;
- $P \setminus C$: wyniki, które spełniają słowa prośby i które człowiek odrzuca.

Maszyna zwraca 1 wynik ze zbioru P. Maszyna spełnia słowa prośby. Maszyna nie zna zbioru C.

Prośba jest bezpieczna dokładnie w 1 przypadku:

$$P \subseteq C \iff P \setminus C = \varnothing \qquad (2)$$

Wzór (2) mówi: każdy wynik, który spełnia słowa prośby, jest wynikiem, którego człowiek chce. Złoty chleb Midasa leży w części $P \setminus C$. Temperatura 17 °C przy oknie też leży w tej części.

## Teza

**Teza.** Maszyna jest niebezpieczną technologią, bo wymaga od człowieka wiedzy o własnym zamiarze.

Zapis ścisły tezy: tylko jeżeli część $P \setminus C$ zawiera co najmniej 1 wynik, prośba jest niebezpieczna. Niebezpieczeństwo leży więc w prośbie, a nie w maszynie.

Maszyna jest rozwiązaniem: maszyna usuwa problem wykonania. Teza 2 z tekstu „Perfekcja – koniec ludzkości?” mówi, że każde nowe rozwiązanie prowadzi do nowych problemów. Nowym problemem jest zamiar. Człowiek, który oddał wykonanie maszynie, zostaje z pytaniem: czego chcę?

Norbert Wiener ostrzegał przed tym samym w 1960 r.[^wiener]. Człowiek, który oddaje cel maszynie, POWINIEN mieć pewność, że maszyna dostała cel, którego człowiek naprawdę chce.

## Co robi człowiek

Zawężenie prośby ma 3 akty z tezy 8 tego samego tekstu: akt woli, akt uwagi i akt odpowiedzialności. Wykonaj każdy krok w tej kolejności:

1. Wola: zapisz zamiar jako stan, który potrafisz sprawdzić.
2. Uwaga: nazwij to, czego maszynie NIE WOLNO zmienić.
3. Uwaga: nazwij co najmniej 1 wynik, który odrzucasz.
4. Odpowiedzialność: sprawdź wynik przed użyciem.

Wynik: część $P \setminus C$ jest mniejsza, a wynik maszyny jest twoim wynikiem.

Przykład prośby szerokiej: „Posprzątaj katalog.”

Przykład prośby zawężonej: „Usuń z katalogu `tmp` każdy plik `.log` starszy niż 30 dób. Zostaw każdy inny plik bez zmian. Wypisz nazwy usuniętych plików.”

## Słabe miejsce tezy

Człowiek nie zna całego zbioru C przed zobaczeniem wyniku. Człowiek poznaje część własnego zamiaru dopiero wtedy, gdy widzi wynik, który odrzuca. Zbiór P zależy też od tego, jak maszyna czyta słowa prośby. Człowiek nie widzi tego czytania. Wzór (2) opisuje więc warunek, którego człowiek nie potrafi sprawdzić przed prośbą.

## Pytania

1. Przypomnij sobie prośbę, którą maszyna spełniła co do słowa i wbrew zamiarowi. Które słowo było za szerokie?
2. Wypisz 3 wyniki, które odrzucasz, zanim wyślesz kolejną prośbę. Ile minut trwało wypisanie?
3. Midas dostał dokładnie to, o co prosił. Kto odpowiada za złoty chleb: Midas albo bóg?
4. Prosisz o to samo człowieka i maszynę. Który wykonawca zapyta, czego naprawdę chcesz?
5. Czy istnieje prośba, dla której część $P \setminus C$ jest pusta? Podaj taką prośbę.

## Decyzje i braki

| Nr | Fragment | Reguła | Znaczenia lub brak | Wybór |
|---|---|---|---|---|
| 1 | „AI” w tytule wersji pierwszej | A1 | Tekst „Perfekcja – koniec ludzkości?” nazywa to pojęcie słowem „maszyna”. | Notatka używa słowa „maszyna”. Legenda podaje związek ze skrótem AI. |
| 2 | Termostat: 20 °C, 17 °C, 4 m | D1 | Liczby opisują przykład, a nie pomiar. | Liczby zostają jako dane przykładu. |
| 3 | Zdanie Wienera | Granice standardu | Źródło jest po angielsku. | Notatka podaje sens zdania bez cudzysłowu. |

## Powiązane

- [philosophy](https://github.com/maciejszulia/philosophy): teza 2, teza 7 i teza 8.
- [tractatus-skills](https://github.com/maciejszulia/tractatus-skills): skill `tractatus-sense` zawęża zbiór P przed pracą, a skill `tractatus-verify` sprawdza wynik po pracy.
- [polszczyzna-kontrolowana](https://github.com/maciejszulia/polszczyzna-kontrolowana): reguły, po których zdanie prośby ma 1 znaczenie.

[Profil](../README.pl.md) | [English](why-ai-is-dangerous.md)

[^ovid]: Owidiusz, „Metamorfozy”, księga XI, wersy 85–145.
[^wiener]: N. Wiener, „Some Moral and Technical Consequences of Automation”, „Science” 131 (3410), 1355–1358 (1960). [doi:10.1126/science.131.3410.1355](https://doi.org/10.1126/science.131.3410.1355)
