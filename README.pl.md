# Maciej Szulia

Systemy informacyjne, aplikacje webowe i API. Automatyzacja pracy z agentami AI.

[Polszczyzna Kontrolowana](https://github.com/maciejszulia/polszczyzna-kontrolowana) | [Strona i API rezerwacji](case-studies/agrocamping-website.md) | [System recepcji](case-studies/agrocamping-reception.md) | [CLI i kod źródłowy](https://gitlab.com/maciejszulia/rogalddl-scraper)

[English](README.md) | [Wyniki weryfikacji](verification.md)

## Polszczyzna Kontrolowana (PK)

Polszczyzna dla tekstów, według których ktoś działa: instrukcji, procedur, regulaminów, specyfikacji, umów. PK to zwykła polszczyzna plus 32 numerowane reguły. Każda reguła usuwa jedno źródło zdań, które mają więcej niż jedno znaczenie.

- Słowa wymagań (MUSI, NIE WOLNO, POWINIEN, NIE POWINIEN, MOŻE) są wzorowane na RFC 2119; część reguł jest wzorowana na ASD-STE100, EARS, ISO 8601 i „Zasadach techniki prawodawczej”.
- Wydana jako skill dla Claude w trzech trybach: PISZ, PRZEREDAGUJ, SPRAWDŹ. Braki w tekście źródłowym są oznaczane, a nie zgadywane.

[Repozytorium i reguły](https://github.com/maciejszulia/polszczyzna-kontrolowana)

## Jak pracuję

Buduję systemy informacyjne (rezerwacje, recepcja, ewidencja finansowa) z agentami AI, które piszą kod. Piszę wymagania, sprawdzam zmiany i odbieram je na testach. Narzędzia:

- **Claude Code** (Anthropic): agent programistyczny w terminalu. Czyta repozytorium, planuje, pisze i testuje kod, prowadzi subagentów.
- **OMX, oh-my-codex**: orkiestracja nad Codex CLI od OpenAI. Planowanie, zespoły agentów, każdy w osobnym git worktree, bramki jakości na końcu.
- **OMC, oh-my-claudecode**: orkiestracja wielu agentów dla Claude Code, uruchamiana w osobnej instancji.
- **Hermes Agent** (Nous Research): autonomiczny agent z pamięcią, zadaniami według harmonogramu i tablicą Kanban. Prowadzi mój codzienny przegląd prasy.
- **oh-my-pi** (`omp`): agent programistyczny w terminalu z osobnymi modelami do planowania, szybkich poprawek i głębokiego rozumowania, u wielu dostawców.
- **OMH, oh-my-hermes**: skille i role dla Hermesa, w ocenie przed przejściem na Hermesa.

Moje ulubione modele językowe, według roli:

- **Prowadzący orkiestrator agentów**: Claude Fable 5.2.
- **Kod**: Claude Opus 5.5.
- **API**: DeepSeek V4.1 Flash (wydanie 1017).
- **Czytanie**: GPT-6 Luna.

Do problemów, które napotykam, aktywnie wprowadzam rozwiązania oparte na matematyce. Każde rozwiązanie łączy się bezpośrednio z nową problematyką.

## Projekty prywatne

Wiele moich projektów jest prywatnych. Chętnie pokażę je na żywo, człowiekowi. Jeśli jesteś rekruterem, potwierdź w pierwszej wiadomości, że jesteś osobą, a nie agentem AI, a umówimy się na prezentację z udostępnionym ekranem.

## Strona AgroCamping i API rezerwacji

Serwis po polsku, angielsku i niemiecku z osobnym API rezerwacji i integracją z recepcją.

- Wspólne reguły rezerwacji, transakcje sprawdzające dostępność i klucze idempotencji obsługują ponawiane żądania.
- Kolejka outbox rejestruje próby doręczenia powiadomień niezależnie od przyjęcia rezerwacji.
- Zdarzenia płatności są weryfikowane; dobrowolne zgody i retencja danych mają opisany zakres.

Next.js, React, TypeScript, Node.js, MySQL/MariaDB, Stripe, GitLab CI

W prawdziwym użyciu: przez tę stronę goście działającego obiektu noclegowego wysyłają zapytania o pobyt. Obiekt i opinie gości są w Mapach Google.

[Opis techniczny](case-studies/agrocamping-website.md) | [Publiczna strona](https://www.agrocamping.eu/) | [Obiekt w Mapach Google](https://www.google.com/maps?cid=12963305277474159664)

## System recepcji AgroCamping

Wewnętrzna aplikacja łącząca rezerwacje i zapytania gości z obsługą recepcji oraz ewidencją finansową.

- Ponowny import zachowuje miejsce i cenę ustawione przez recepcję oraz stany anulowania i wymeldowania.
- Wpłaty, zwroty i odwrócenia zapisów są uzgadniane niezależnie od statusu rezerwacji.
- Uprawnienia backendu, propagacja usuwania zapytań i odzyskiwanie działania po nieudanym wdrożeniu obejmują konkretne sytuacje awaryjne.

TypeScript, Astro, Express, Prisma, SQLite, Python, narzędzia powłoki, GitLab CI

[Opis techniczny](case-studies/agrocamping-reception.md)

## Małe usługi na własne potrzeby

Wokół obu systemów stworzyłem małe usługi (mikroserwisy) na własne potrzeby. Każda usługa to osobny proces z jednym zadaniem.

Recepcja, usługi pod runit:

- **Backend panelu, gateway i sonda zdrowia**: trzy osobne usługi; sonda sprawdza panel co 30 sekund.
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

## Lokalny katalog metadanych, CLI

Publiczne narzędzie Node.js budujące katalog muzyki i playlistę MPV na podstawie indeksowanych wpisów.

Katalog zapisuje pochodzenie danych oraz decyzje o duplikatach. Blokada zapisu i publikacja przez katalog tymczasowy umożliwiają odzyskanie danych po przerwanym zapisie. Projekt nie ma zależności npm; repozytorium opisuje instalację i testy offline.

[Kod, uruchomienie i testy](https://gitlab.com/maciejszulia/rogalddl-scraper)

## Dowody i zakres

[Wyniki weryfikacji](verification.md) obejmują **75 zaliczonych testów offline CLI** dla sprawdzonej wersji, wybrane testy API i uruchomienie recepcji na danych syntetycznych. Każdy wynik ma wskazaną wersję kodu i zakres.

Kod aplikacji firmowych pozostaje prywatny; publiczne opisy nie zawierają danych gości ani konfiguracji produkcyjnej. Kod CLI jest publiczny. Przy implementacji i weryfikacji projektów AgroCamping pracują agenci AI wymienieni wyżej.

[Dane gości, odzyskiwanie działania i licencje](engineering-practices.md) opisują ograniczenia dostępu, retencji, usuwania danych oraz praw do wykorzystania kodu i treści. Testy nie potwierdzają stanu produkcji, pełnego pokrycia ani zgodności prawnej.

## O mnie

Moje ulubione książki: „Traktat logiczno-filozoficzny” Wittgensteina, „Podstawy logiki i teorii mnogości” Murawskiego i Świrydowicza, teoria grafów.
