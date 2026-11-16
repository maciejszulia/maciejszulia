# Maciej Szulia

Full-stack developer poziomu mid i inżynier AI. Systemy informacyjne, aplikacje webowe i API; narzędzia metaprogramistyczne; automatyzacja pracy z agentami AI.

[English](README.md)

## Systemy prywatne w prawdziwym użyciu

**Strona AgroCamping i API rezerwacji.** Serwis po polsku, angielsku i niemiecku z osobnym API rezerwacji i integracją z recepcją. Wspólne reguły rezerwacji, transakcje sprawdzające dostępność i klucze idempotencji obsługują ponawiane żądania. Kolejka outbox rejestruje próby doręczenia powiadomień niezależnie od przyjęcia rezerwacji. Zdarzenia płatności są weryfikowane. Przez tę stronę goście działającego obiektu noclegowego wysyłają zapytania o pobyt.

Next.js, React, TypeScript, Node.js, MySQL/MariaDB, Stripe, GitLab CI

[Opis techniczny](case-studies/agrocamping-website.md) | [Publiczna strona](https://www.agrocamping.eu/) | [Obiekt w Mapach Google](https://www.google.com/maps?cid=12963305277474159664)

**System recepcji AgroCamping.** Wewnętrzna aplikacja, która łączy rezerwacje i zapytania gości z obsługą recepcji oraz ewidencją finansową. Ponowny import zachowuje miejsce i cenę ustawione przez recepcję. Wpłaty, zwroty i odwrócenia zapisów są uzgadniane niezależnie od statusu rezerwacji.

TypeScript, Astro, Express, Prisma, SQLite, Python, narzędzia powłoki, GitLab CI

[Opis techniczny](case-studies/agrocamping-reception.md)

Kod obu systemów jest prywatny. Projekty prywatne pokazuję na żywo, człowiekowi. Jeżeli jesteś rekruterem, to napisz w pierwszej wiadomości, że jesteś osobą, a nie agentem AI, a umówimy się na prezentację z udostępnionym ekranem.

Wokół obu systemów działa 14 usług; każda usługa to osobny proces z jednym zadaniem. Przykłady: synchronizacja poczty, kopie bazy, monitoring, odnawianie certyfikatu, cotygodniowy job bezpieczeństwa. Lista stoi w pliku [details.pl.md](details.pl.md).

## Wybrane repozytoria publiczne

| Repozytorium | Co zawiera | Technologie |
|---|---|---|
| [claude-code-skills](https://github.com/maciejszulia/claude-code-skills)<br>[![CI](https://github.com/maciejszulia/claude-code-skills/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/claude-code-skills/actions/workflows/ci.yml) | 8 skilli dla Claude Code: pamięć sesji w Markdownie, przeładowanie reguł, zespół subagentów, zlecenie dla workera Codex, drift check, handoff lidera, reguły README, PK. Każdy skill ma diagram. | Markdown, Python. |
| [polszczyzna-kontrolowana](https://github.com/maciejszulia/polszczyzna-kontrolowana)<br>[![CI](https://github.com/maciejszulia/polszczyzna-kontrolowana/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/polszczyzna-kontrolowana/actions/workflows/ci.yml) | Polszczyzna Kontrolowana (PK): 32 numerowane reguły, po których zdanie ma jedno znaczenie. Zbiór reguł, skill dla Claude i praca z pomiarami. | Python, LaTeX. |
| [pk-rewriter](https://github.com/maciejszulia/pk-rewriter)<br>[![CI](https://github.com/maciejszulia/pk-rewriter/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/pk-rewriter/actions/workflows/ci.yml) | Lokalne modele Qwen przepisują polskie instrukcje na PK. Linter pklint sprawdza każdy wynik. Repo zawiera ewaluację modeli, adapter LoRA trenowany na procesorze i serwer MCP. | Python, Ollama. |
| [neurophify](https://github.com/maciejszulia/neurophify)<br>[![CI](https://github.com/maciejszulia/neurophify/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/neurophify/actions/workflows/ci.yml) | Graf wiedzy w 3D w kształcie mózgu. Program czyta plik graph.json z graphify albo katalog notatek w Markdownie. Program zapisuje interaktywną stronę, obracający się rysunek SVG i model STL do README. Repo ma wydanie w wersji 1.3.0, obraz kontenera i [demo na żywo](https://maciejszulia.github.io/neurophify/). | Python, 3d-force-graph. |
| [book-skills](https://github.com/maciejszulia/book-skills) | 6 skilli: 5 książek o C++ oraz 4 książki matematyczne jako listy kontrolne do pisania kodu i do przeglądu kodu. | Markdown. |
| [rogalddl-scraper](https://github.com/maciejszulia/rogalddl-scraper)<br>[![CI](https://github.com/maciejszulia/rogalddl-scraper/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/rogalddl-scraper/actions/workflows/ci.yml) | CLI w Node.js, które buduje lokalny katalog metadanych. Bez zależności npm, 75 testów offline dla sprawdzonej wersji, odzyskiwanie po przerwanym zapisie. | Node.js. |
| [agro-kubernetes](https://github.com/maciejszulia/agro-kubernetes)<br>[![CI](https://github.com/maciejszulia/agro-kubernetes/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/agro-kubernetes/actions/workflows/ci.yml) | Laboratorium Kubernetes na 2 telefonach Xperia bez roota: gość QEMU w Termuxie, zmierzony stan, K3s zablokowany przez brak 3 opcji jądra. 28 testów. | Python, Bash, QEMU, K3s. |
| [millennium-models](https://github.com/maciejszulia/millennium-models)<br>[![CI](https://github.com/maciejszulia/millennium-models/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/millennium-models/actions/workflows/ci.yml) | Minimalne modele 7 problemów milenijnych: 3 modele, 14 sprawdzianów liczbowych, 18 rysunków, strona interaktywna. Plany dowodu z nazwanym brakującym krokiem, bez dowodów. | Python. |

Pozostałe repozytoria publiczne i stan CI stoją w pliku [details.pl.md](details.pl.md).

## Jak pracuję

Piszę wymagania, agenci AI piszą kod, a ja odbieram wynik na testach. Modele według roli: „Claude Fable 5.2” prowadzi i orkiestruje agentów, „Claude Opus 5.5” pisze kod, „DeepSeek V4.1 Flash” (wydanie 1017) obsługuje wywołania API, „GPT-6 Luna” czyta.

Narzędzia agentów, których używam, stoją w pliku [details.pl.md](details.pl.md).

Od 2026-11-15 2 sesje agentów pracują jako para. Pierwsza sesja planuje, decyduje i ocenia. Druga sesja mierzy, dowodzi i pisze kod. Każda sesja przekazuje skończone zadanie drugiej sesji do oceny. Pomiar, test albo cytat reguły wygrywa z opinią. Para decyduje w sprawach odwracalnych. Decyzję nieodwracalną albo zewnętrzną podejmuję ja.

Jak pilnuję agentów:

- **Handoff i drift-check**: sesja, która dochodzi do limitu, pisze stronę handoffu. Lider, który przejmuje pracę, najpierw porównuje moje polecenia ze stanem repozytoriów ([lead-handoff](https://github.com/maciejszulia/claude-code-skills/tree/main/skills/lead-handoff), [drift-check](https://github.com/maciejszulia/claude-code-skills/tree/main/skills/drift-check)).
- **Hooki**: 1 hook pyta mnie, czy sesja pracuje dalej, gdy zużycie limitu wynosi co najmniej 90 %. 1 hook każe zaktualizować README po commicie, który zmienia co najmniej 200 linii ([github-readme](https://github.com/maciejszulia/claude-code-skills/tree/main/skills/github-readme)).
- **Rejestr poleceń**: każde moje polecenie ma w rejestrze godzinę, dowód i procent wykonania.

Do problemów, które napotykam, wprowadzam rozwiązania oparte na matematyce. Każde rozwiązanie prowadzi do nowych problemów, więc rozwiązanie ma być możliwie najmniejsze. Uzasadnienie jest w repozytorium [philosophy](https://github.com/maciejszulia/philosophy). Dlaczego prośba do maszyny jest niebezpieczna: [notes/why-ai-is-dangerous.pl.md](notes/why-ai-is-dangerous.pl.md).

## Języki

Udział języków w kodzie 67 moich repozytoriów na GitHubie (24 publiczne, 43 prywatne). Pomiar: GitHub Linguist, bajty kodu, 2026-11-16.

| Język | Udział | Zastosowanie |
|---|---|---|
| Jupyter Notebook | 30,9 % | Zajęcia na studiach. Notebook zapisuje wyniki, więc liczba bajtów zawyża ilość kodu. |
| HTML | 29,3 % | Dokumenty generowane: CV i raporty projektu szukania pracy, strony panelu recepcji. |
| TypeScript | 12,7 % | Panel recepcji AgroCamping (Astro, Express, Prisma) oraz serwis rezerwacji (Next.js, React). |
| JavaScript | 10,5 % | API rezerwacji w Node.js, skrypty serwisu oraz CLI rogalddl-scraper. |
| Python | 8,7 % | Narzędzia i badania: linter Polszczyzny Kontrolowanej, pk-rewriter, neurophify, hooki i nadzór agentów AI, modele matematyczne, model gospodarstwa, kolektory ofert pracy. |
| Astro | 2,5 % | Frontend panelu recepcji. |
| Shell | 1,9 % | Operacje: deploy, kopie zapasowe, usługi runit, skrypty paska statusu. |
| C | 1,2 % | dwm oraz st: kod suckless z moimi patchami. |
| TeX | 0,8 % | Prace: Polszczyzna Kontrolowana, arytmetyki generowane funkcją, tpfas. |
| CSS, SCSS | 0,8 % | Style serwisu, panelu recepcji oraz strony CV. |

Pozostałe 0,6 % to Java oraz Prolog (zajęcia na studiach), MATLAB oraz Lean (repozytoria matematyczne), PL/pgSQL (baza projektu gospodarstwa), Mermaid, Roff, Makefile oraz Dockerfile.

Pomiar pomija 2 forki oraz 1 prywatne repozytorium ze studiów, które zawiera wgrane środowisko Pythona (37,6 MB kodu Pythona). Z tym repozytorium udział Pythona wynosi 61,4 %.

## Dowody i zakres

[Wyniki weryfikacji](verification.md) obejmują **75 zaliczonych testów offline CLI** dla sprawdzonej wersji, wybrane testy API i uruchomienie recepcji na danych syntetycznych. Każdy wynik ma wskazaną wersję kodu i zakres.

[Dane gości, odzyskiwanie działania i licencje](engineering-practices.md) opisują ograniczenia dostępu, retencji, usuwania danych oraz praw do wykorzystania kodu i treści. Publiczne opisy nie zawierają danych gości ani konfiguracji produkcyjnej. Testy nie potwierdzają stanu produkcji, pełnego pokrycia ani zgodności prawnej.

## Kontakt

CV: https://maciejszulia.github.io

maciej.szulia@gmail.com

Jako człowiek mam wolę, uwagę i odpowiedzialność.
