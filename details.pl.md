# Szczegóły

Pełne listy do krótkiego README profilu.

## Repozytoria publiczne

### Agenci AI i modele językowe

| Repozytorium | Co zawiera | Technologie |
|---|---|---|
| [claude-code-skills](https://github.com/maciejszulia/claude-code-skills)<br>[![CI](https://github.com/maciejszulia/claude-code-skills/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/claude-code-skills/actions/workflows/ci.yml) | 8 skilli dla Claude Code: pamięć sesji w Markdownie, przeładowanie reguł, zespół subagentów, zlecenie dla workera Codex, drift check, handoff lidera, reguły README, PK. Każdy skill ma diagram. | Markdown, Python. |
| [job-search-agent](https://github.com/maciejszulia/job-search-agent)<br>[![CI](https://github.com/maciejszulia/job-search-agent/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/job-search-agent/actions/workflows/ci.yml) | Narzędzia i metoda szukania pracy z agentem AI: zbieranie ofert, dla każdej oferty 1 CV i 1 wiadomość, ledger zgłoszeń, statystyki bez nazw. Dokumentacja jest w PK. | Python. |
| [pk-rewriter](https://github.com/maciejszulia/pk-rewriter)<br>[![CI](https://github.com/maciejszulia/pk-rewriter/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/pk-rewriter/actions/workflows/ci.yml) | Lokalne modele Qwen przepisują polskie instrukcje na PK. Linter pklint sprawdza każdy wynik. Repo zawiera ewaluację modeli, adapter LoRA trenowany na procesorze i serwer MCP. | Python, Ollama. |
| [polszczyzna-kontrolowana](https://github.com/maciejszulia/polszczyzna-kontrolowana)<br>[![CI](https://github.com/maciejszulia/polszczyzna-kontrolowana/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/polszczyzna-kontrolowana/actions/workflows/ci.yml) | Polszczyzna Kontrolowana (PK): 32 numerowane reguły, po których zdanie ma jedno znaczenie. Zbiór reguł, skill dla Claude i praca z pomiarami. | Python, LaTeX. |
| [neurophify](https://github.com/maciejszulia/neurophify)<br>[![CI](https://github.com/maciejszulia/neurophify/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/neurophify/actions/workflows/ci.yml) | Graf wiedzy w 3D w kształcie mózgu. Program czyta plik graph.json z graphify albo katalog notatek w Markdownie. Program zapisuje interaktywną stronę, obracający się rysunek SVG i model STL do README. Repo ma wydanie w wersji 1.3.0, obraz kontenera i [demo na żywo](https://maciejszulia.github.io/neurophify/). | Python, 3d-force-graph. |
| [tractatus-skills](https://github.com/maciejszulia/tractatus-skills) | Dwa skille na podstawie „Traktatu” Wittgensteina: warunki prawdziwości prośby i tabela prawdy dla twierdzenia. | Markdown. |
| [controlled-english](https://github.com/maciejszulia/controlled-english) | Controlled English (CE): angielski odpowiednik PK z modułem S dla claimów, findingów, raportów z testów i opisów pull requestów w ruchliwych repozytoriach. Skill dla Claude. | Markdown. |
| [pullrequest-sandbox](https://github.com/maciejszulia/pullrequest-sandbox) | Uruchamia kod niezaufanego repozytorium i testuje otwarte pull requesty scalone z `main` w kontenerach Docker bez sieci. | Python, Bash, Docker. |
| [book-skills](https://github.com/maciejszulia/book-skills) | 6 skilli: 5 książek o C++ oraz 4 książki matematyczne jako listy kontrolne do pisania kodu i do przeglądu kodu. | Markdown. |
| [silverbullet](https://github.com/maciejszulia/silverbullet) | Fork SilverBulleta z 2 bibliotekami Space Lua: „Decision Inbox” dodaje przycisk odpowiedzi, a „Local AI” zawiera konfigurację dla Ollamy. | Space Lua. |

### Systemy i narzędzia

| Repozytorium | Co zawiera | Technologie |
|---|---|---|
| [rogalddl-scraper](https://github.com/maciejszulia/rogalddl-scraper)<br>[![CI](https://github.com/maciejszulia/rogalddl-scraper/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/rogalddl-scraper/actions/workflows/ci.yml) | CLI w Node.js, które buduje lokalny katalog metadanych. Bez zależności npm, 75 testów offline dla sprawdzonej wersji, odzyskiwanie po przerwanym zapisie. | Node.js. |
| [agro-kubernetes](https://github.com/maciejszulia/agro-kubernetes)<br>[![CI](https://github.com/maciejszulia/agro-kubernetes/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/agro-kubernetes/actions/workflows/ci.yml) | Laboratorium Kubernetes na 2 telefonach Xperia bez roota: gość QEMU w Termuxie, zmierzony stan, K3s zablokowany przez brak 3 opcji jądra. 28 testów. | Python, Bash, QEMU, K3s. |
| [dwm](https://github.com/maciejszulia/dwm), [dwmblocks](https://github.com/maciejszulia/dwmblocks), [dwm-bar-scripts](https://github.com/maciejszulia/dwm-bar-scripts), [st](https://github.com/maciejszulia/st)<br>[![dwm CI](https://github.com/maciejszulia/dwm/actions/workflows/ci.yml/badge.svg?branch=master)](https://github.com/maciejszulia/dwm/actions/workflows/ci.yml) [![dwm-bar-scripts CI](https://github.com/maciejszulia/dwm-bar-scripts/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/dwm-bar-scripts/actions/workflows/ci.yml) | Mój pulpit X11: forki suckless dwm w wersji 6.8 i st w wersji 0.9.3. Klikalny zwijany pasek stanu i skrypty paska (alerty pogodowe, CPU, GPU, limity AI). | C, Shell. |

### Matematyka

| Repozytorium | Co zawiera | Technologie |
|---|---|---|
| [millennium-models](https://github.com/maciejszulia/millennium-models)<br>[![CI](https://github.com/maciejszulia/millennium-models/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/millennium-models/actions/workflows/ci.yml) | Minimalne modele 7 problemów milenijnych: 3 modele, 14 sprawdzianów liczbowych, 18 rysunków, strona interaktywna. Plany dowodu z nazwanym brakującym krokiem, bez dowodów. | Python. |
| [function-generated-arithmetics](https://github.com/maciejszulia/function-generated-arithmetics)<br>[![CI](https://github.com/maciejszulia/function-generated-arithmetics/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/function-generated-arithmetics/actions/workflows/ci.yml) | Arytmetyki generowane funkcją: dziesięć generatorów, klasyfikacja na grupę, monoid albo półgrupę, weryfikacja liczbowa, jeden wynik negatywny. Prace po polsku i po angielsku. | Python, LaTeX. |
| [arytmetyki-generowane-funkcyjnie](https://github.com/maciejszulia/arytmetyki-generowane-funkcyjnie)<br>[![CI](https://github.com/maciejszulia/arytmetyki-generowane-funkcyjnie/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/arytmetyki-generowane-funkcyjnie/actions/workflows/ci.yml) | Arytmetyki generowane funkcyjnie (rachunek nie-Newtonowski): modele w Pythonie, testy aksjomatów, wykresy, artykuł w LaTeX, demo w MATLAB-ie. | Python, LaTeX, MATLAB. |
| [nowe-dzialania-matematyczne](https://github.com/maciejszulia/nowe-dzialania-matematyczne)<br>[![CI](https://github.com/maciejszulia/nowe-dzialania-matematyczne/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/nowe-dzialania-matematyczne/actions/workflows/ci.yml) | p-dodawanie: 1 działanie z parametrem p daje sumę, połączenie równoległe, przeciwprostokątną, minimum i maksimum. 39 testów. | Python. |
| [tpfas](https://github.com/maciejszulia/tpfas) | Notatka o arytmetyce nie-Newtonowskiej z członem synergii: operator przemienny i niełączny; źródło LaTeX i PDF. | LaTeX. |

### Teksty i projekty

| Repozytorium | Co zawiera | Technologie |
|---|---|---|
| [philosophy](https://github.com/maciejszulia/philosophy) | Tekst filozoficzny w polszczyźnie kontrolowanej: rozwiązania i problemy, spokój i chaos, człowiek i maszyna. | Markdown. |
| [traktat-ludzko-sztuczno-inteligencyjny](https://github.com/maciejszulia/traktat-ludzko-sztuczno-inteligencyjny) | 145 tez o granicy między człowiekiem a maszyną, w numeracji „Traktatu”. | Markdown, LaTeX. |
| [samowystarczalny-system-do-zycia](https://github.com/maciejszulia/samowystarczalny-system-do-zycia)<br>[![CI](https://github.com/maciejszulia/samowystarczalny-system-do-zycia/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/maciejszulia/samowystarczalny-system-do-zycia/actions/workflows/ci.yml) | Projekt samowystarczalnego gospodarstwa o powierzchni 4,27 ha: żywność, ciepło, woda, energia off-grid, model 3D. | Python. |

### Kod pisany ręcznie na studiach (2020–2024)

| Repozytorium | Co zawiera | Technologie |
|---|---|---|
| [AiSD](https://github.com/maciejszulia/AiSD) | Algorytmy i struktury danych: lista jednokierunkowa, kolejka, stos, drzewo, drzewo BST, z testami. 49 commitów, 2021–2022. | Python. |
| [po-bitbucket-copy](https://github.com/maciejszulia/po-bitbucket-copy) | Programowanie obiektowe: 5 list zadań, kolokwium i zadania egzaminacyjne. 63 commity, 2021–2022. | Java. |
| [C-prace-domowa](https://github.com/maciejszulia/C-prace-domowa) | Programowanie strukturalne: zadania w 3 rozdziałach, w tym wskaźniki. 2021. | C. |
| [ProgDekl](https://github.com/maciejszulia/ProgDekl) | Programowanie deklaratywne: 10 laboratoriów i projekt zespołowy. 2023. | Prolog. |
| [python-uwm](https://github.com/maciejszulia/python-uwm) | Prace domowe: funkcje i moduły, pliki, klasy, NumPy, pandas. 33 commity, 2021. | Python. |
| [Simple-Password-Generator](https://github.com/maciejszulia/Simple-Password-Generator) | Mały własny projekt: generator haseł z interfejsem graficznym. 2021–2023. | Python, Tkinter. |

18 kolejnych repozytoriów z czasów studiów jest publicznych na [moim profilu](https://github.com/maciejszulia?tab=repositories).

## Usługi wokół tych systemów

Każda usługa to osobny proces z jednym zadaniem.

Recepcja, usługi pod runit:

- **Backend panelu, gateway i sonda zdrowia**: trzy usługi; sonda sprawdza panel co 30 sekund.
- **Synchronizacja poczty**: importuje pocztę gości z Gmaila do panelu i liczy kolejne błędy każdego kroku.
- **Powiadomienia o przyjazdach**: wysyła powiadomienie push o przyjazdach przez ntfy.
- **Konserwacja**: okresowa kopia bazy danych.
- **Watcher**: sprawdza zdrowie panelu, wolne miejsce na dysku, API strony, wiek kopii bazy i ważność certyfikatu; powiadamia tylko przy zmianie stanu.
- **Odnawianie certyfikatu**: dzienna pętla odnawia certyfikat TLS panelu.
- **Pogoda**: pobiera dane pogodowe do cache.

Strona, GitLab CI i Docker:

- **Cotygodniowy job bezpieczeństwa**: audyt zależności (npm audit, osv-scanner), skan sekretów (gitleaks), test TLS (testssl), test nagłówków HTTP (MDN Observatory) i test linków (lychee).
- **Podgląd wdrożenia**: job CI wdraża statyczny podgląd strony do lokalnego klastra Kubernetes (k3d).
- **Monitoring dostępności**: Gatus w Dockerze z własną konfiguracją i alertami.

Stacja robocza:

- **Sterowanie wiatrakiem**: krzywa obrotów z histerezą dla laptopa.
- **Watchdog zasobów**: mierzy zasoby systemu i zapisuje raport; nie zabija żadnego procesu.
- **Front TLS dla lokalnej instancji SearXNG**: usługa w Node.js.
- **Kopia poza maszyną**: szyfruje najnowszą kopię bazy przez GPG (AES-256) i zapisuje ją poza maszyną.

## Narzędzia agentów

- **Claude Code** (Anthropic): agent programistyczny w terminalu. Czyta repozytorium, planuje, pisze i testuje kod, prowadzi subagentów.
- **OMX, oh-my-codex**: orkiestracja nad Codex CLI od OpenAI. Planowanie, zespoły agentów, każdy w osobnym git worktree, bramki jakości na końcu.
- **OMC, oh-my-claudecode**: orkiestracja agentów dla Claude Code, uruchamiana w osobnej instancji.
- **Hermes Agent** (Nous Research): autonomiczny agent z pamięcią, zadaniami według harmonogramu i tablicą Kanban. Prowadzi codzienny przegląd prasy.
- **oh-my-pi** (`omp`): agent programistyczny w terminalu z osobnymi modelami do planowania, szybkich poprawek i głębokiego rozumowania, u różnych dostawców.
- **OMH, oh-my-hermes**: skille i role dla Hermesa, w ocenie.

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
