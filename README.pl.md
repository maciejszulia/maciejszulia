# Maciej Szulia

Systemy informacyjne, aplikacje webowe i API. Automatyzacja pracy z agentami AI.

[English](README.md)

## Repozytoria publiczne

| Repozytorium | Co zawiera | Technologie |
|---|---|---|
| [polszczyzna-kontrolowana](https://github.com/maciejszulia/polszczyzna-kontrolowana) | Polszczyzna Kontrolowana (PK): 32 numerowane reguły, po których zdanie ma jedno znaczenie. Zbiór reguł, skill dla Claude i praca z pomiarami. | Python, LaTeX |
| [claude-code-skills](https://github.com/maciejszulia/claude-code-skills) | Sześć skilli dla Claude Code, każdy z diagramem: pamięć sesji w Markdownie, przeładowanie reguł, zespół subagentów, zlecenie dla workera Codex, drift check, PK. | Markdown, Python |
| [tractatus-skills](https://github.com/maciejszulia/tractatus-skills) | Dwa skille na podstawie „Traktatu” Wittgensteina: warunki prawdziwości prośby i tabela prawdy dla twierdzenia. | Markdown |
| [millennium-models](https://github.com/maciejszulia/millennium-models) | Minimalne modele 7 problemów milenijnych: 3 modele, 14 sprawdzianów liczbowych, 18 rysunków, strona interaktywna. Plany dowodu z nazwanym brakującym krokiem, bez dowodów. | Python |
| [function-generated-arithmetics](https://github.com/maciejszulia/function-generated-arithmetics) | Arytmetyki generowane funkcją: dziesięć generatorów, klasyfikacja na grupę, monoid albo półgrupę, weryfikacja liczbowa, jeden wynik negatywny. Prace po polsku i po angielsku. | Python, LaTeX |
| [rogalddl-scraper](https://github.com/maciejszulia/rogalddl-scraper) | CLI w Node.js, które buduje lokalny katalog metadanych. Bez zależności npm, 75 testów offline dla sprawdzonej wersji, odzyskiwanie po przerwanym zapisie. | Node.js |
| [philosophy](https://github.com/maciejszulia/philosophy) | Tekst filozoficzny w polszczyźnie kontrolowanej: rozwiązania i problemy, spokój i chaos, człowiek i maszyna. | Markdown |
| [traktat-ludzko-sztuczno-inteligencyjny](https://github.com/maciejszulia/traktat-ludzko-sztuczno-inteligencyjny) | 145 tez o granicy między człowiekiem a maszyną, w numeracji „Traktatu”. | Markdown, LaTeX |
| [samowystarczalny-system-do-zycia](https://github.com/maciejszulia/samowystarczalny-system-do-zycia) | Projekt samowystarczalnego gospodarstwa o powierzchni 4,27 ha: żywność, ciepło, woda, energia off-grid, model 3D. | Python |

## Systemy prywatne w prawdziwym użyciu

**Strona AgroCamping i API rezerwacji.** Serwis po polsku, angielsku i niemiecku z osobnym API rezerwacji i integracją z recepcją. Wspólne reguły rezerwacji, transakcje sprawdzające dostępność i klucze idempotencji obsługują ponawiane żądania. Kolejka outbox rejestruje próby doręczenia powiadomień niezależnie od przyjęcia rezerwacji. Zdarzenia płatności są weryfikowane. Przez tę stronę goście działającego obiektu noclegowego wysyłają zapytania o pobyt.

Next.js, React, TypeScript, Node.js, MySQL/MariaDB, Stripe, GitLab CI

[Opis techniczny](case-studies/agrocamping-website.md) | [Publiczna strona](https://www.agrocamping.eu/) | [Obiekt w Mapach Google](https://www.google.com/maps?cid=12963305277474159664)

**System recepcji AgroCamping.** Wewnętrzna aplikacja, która łączy rezerwacje i zapytania gości z obsługą recepcji oraz ewidencją finansową. Ponowny import zachowuje miejsce i cenę ustawione przez recepcję. Wpłaty, zwroty i odwrócenia zapisów są uzgadniane niezależnie od statusu rezerwacji.

TypeScript, Astro, Express, Prisma, SQLite, Python, narzędzia powłoki, GitLab CI

[Opis techniczny](case-studies/agrocamping-reception.md)

Kod obu systemów jest prywatny. Projekty prywatne pokazuję na żywo, człowiekowi. Jeśli jesteś rekruterem, napisz w pierwszej wiadomości, że jesteś osobą, a nie agentem AI, a umówimy się na prezentację z udostępnionym ekranem.

## Małe usługi wokół tych systemów

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
- **Front TLS dla lokalnej instancji SearXNG**: mała usługa w Node.js.
- **Kopia poza maszyną**: szyfruje najnowszą kopię bazy przez GPG (AES-256) i zapisuje ją poza maszyną.

## Jak pracuję

Piszę wymagania, agenci AI piszą kod, a ja odbieram wynik na testach.

- **Claude Code** (Anthropic): agent programistyczny w terminalu. Czyta repozytorium, planuje, pisze i testuje kod, prowadzi subagentów.
- **OMX, oh-my-codex**: orkiestracja nad Codex CLI od OpenAI. Planowanie, zespoły agentów, każdy w osobnym git worktree, bramki jakości na końcu.
- **OMC, oh-my-claudecode**: orkiestracja wielu agentów dla Claude Code, uruchamiana w osobnej instancji.
- **Hermes Agent** (Nous Research): autonomiczny agent z pamięcią, zadaniami według harmonogramu i tablicą Kanban. Prowadzi codzienny przegląd prasy.
- **oh-my-pi** (`omp`): agent programistyczny w terminalu z osobnymi modelami do planowania, szybkich poprawek i głębokiego rozumowania, u wielu dostawców.
- **OMH, oh-my-hermes**: skille i role dla Hermesa, w ocenie.

Modele według roli: Claude Fable 5.2 prowadzi i orkiestruje agentów, Claude Opus 5.5 pisze kod, DeepSeek V4.1 Flash (wydanie 1017) obsługuje wywołania API, GPT-6 Luna czyta.

Do problemów, które napotykam, wprowadzam rozwiązania oparte na matematyce. Każde rozwiązanie prowadzi do nowych problemów, więc rozwiązanie ma być tak małe, jak się da. Uzasadnienie jest w repozytorium [philosophy](https://github.com/maciejszulia/philosophy). Dlaczego prośba do maszyny jest niebezpieczna: [notes/why-ai-is-dangerous.pl.md](notes/why-ai-is-dangerous.pl.md).

## Dowody i zakres

[Wyniki weryfikacji](verification.md) obejmują **75 zaliczonych testów offline CLI** dla sprawdzonej wersji, wybrane testy API i uruchomienie recepcji na danych syntetycznych. Każdy wynik ma wskazaną wersję kodu i zakres.

[Dane gości, odzyskiwanie działania i licencje](engineering-practices.md) opisują ograniczenia dostępu, retencji, usuwania danych oraz praw do wykorzystania kodu i treści. Publiczne opisy nie zawierają danych gości ani konfiguracji produkcyjnej. Testy nie potwierdzają stanu produkcji, pełnego pokrycia ani zgodności prawnej.

## Kontakt

maciej.szulia@gmail.com

Jako człowiek mam wolę, uwagę i odpowiedzialność.
