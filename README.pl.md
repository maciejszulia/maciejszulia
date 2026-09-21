# Dokumentacja projektów

Opisy techniczne, mechanizmy ochrony danych i wyniki weryfikacji aplikacji
AgroCamping oraz lokalnego katalogu metadanych obsługiwanego z terminala.

[English](README.md)

## Projekty

| Projekt | Zakres | Technologie |
| --- | --- | --- |
| [Strona AgroCamping i API rezerwacji](case-studies/agrocamping-website.md) | Serwis po polsku, angielsku i niemiecku; reguły rezerwacji, obsługa zdarzeń płatności, ponawianie powiadomień i ochrona danych gości. | Next.js, React, TypeScript, Node.js, MySQL/MariaDB, Stripe, GitLab CI |
| [System recepcji](case-studies/agrocamping-reception.md) | Import rezerwacji, ewidencja finansowa, uprawnienia i przywracanie działania po nieudanym wdrożeniu. Ponowny import zachowuje przydział miejsca i cenę ustawione przez pracownika recepcji. | TypeScript, Astro, Express, Prisma, SQLite, Python, narzędzia powłoki, GitLab CI |
| [Lokalny katalog metadanych, CLI](https://gitlab.com/maciejszulia/rogalddl-scraper) | Zapisuje, dlaczego wpis został zachowany, połączony z innym albo odrzucony. Repozytorium opisuje instalację i sprawdzanie danych wejściowych oraz zawiera testy offline na danych syntetycznych. | Node.js, bez zależności npm |

Publiczna strona: [agrocamping.eu](https://www.agrocamping.eu/).

## Dokumentacja uzupełniająca

- [Dane gości, odzyskiwanie działania i licencje](engineering-practices.md): zgody, retencja, uprawnienia, usuwanie danych i ograniczenia praw do wykorzystania kodu oraz treści.
- [Wyniki weryfikacji](verification.md): sprawdzone wersje kodu, polecenia, wyniki testów i niewykonane sprawdzenia.

## Dostęp do kodu i zakres weryfikacji

Repozytoria strony i systemu recepcji są prywatne. Publiczne opisy przedstawiają
implementację bez publikowania danych gości ani konfiguracji produkcyjnej.
Kod CLI jest publiczny i można go uruchomić lokalnie.

Wyniki weryfikacji dotyczą zapisanych wersji kodu i wybranych sprawdzeń. Nie
potwierdzają stanu produkcji, pełnego pokrycia testami ani zgodności prawnej.
Do implementacji i weryfikacji projektów AgroCamping służą narzędzia AI,
w tym Claude Code i Codex.
