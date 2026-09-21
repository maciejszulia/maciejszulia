# Maciej Szulia

Wsparcie techniczne · wdrożenia · aplikacje webowe · Linux  
Olsztyn · Szukam pracy na pełny etat, zdalnie lub hybrydowo

[Strona i API rezerwacji](case-studies/agrocamping-website.md)
· [System recepcji](case-studies/agrocamping-reception.md)
· [CLI](https://gitlab.com/maciejszulia/rogalddl-scraper)

Pomagam przy rezerwacjach i korespondencji z gośćmi w AgroCamping Olsztyn,
kempingu moich rodziców. Koordynuję też rozwój strony i aplikacji recepcji.
Oba projekty AgroCamping wynikają z tej pracy. Pomagają obsłużyć rezerwacje
trafiające do recepcji i utrzymać porządek w danych wymienianych między systemami.

Mam również doświadczenie komercyjne na stanowiskach juniorskich we frontendzie,
e-commerce i systemach CMS. Pracowałem między innymi z PrestaShop i InsERT Sello.

[English](README.md) · [LinkedIn](https://www.linkedin.com/in/maciej-szulia)
· [Strona AgroCamping](https://www.agrocamping.eu/)

## Projekty

- [Strona AgroCamping i API rezerwacji](case-studies/agrocamping-website.md).
  Serwis po polsku, angielsku i niemiecku, z osobnym API. W opisie pokazuję,
  jak rezerwacja trafia do recepcji, co się dzieje po awarii powiadomienia
  i jakie dane zapisują formularze oraz analityka.
- [System recepcji](case-studies/agrocamping-reception.md).
  Aplikacja do codziennej pracy z rezerwacjami. Ponowny import zachowuje przydział
  miejsca i cenę ustawione przez pracownika recepcji. Opis pokazuje też uprawnienia
  użytkowników i przywracanie działania po nieudanym wdrożeniu.
- [Lokalny katalog metadanych, CLI](https://gitlab.com/maciejszulia/rogalddl-scraper).
  Niewielki projekt w Node.js, bez zależności npm. Można pobrać kod i sprawdzić,
  dlaczego wpis został zachowany, połączony z innym albo odrzucony. Testy działają
  offline, a README opisuje instalację i sprawdzanie danych wejściowych.

Kod systemów firmowych pozostaje prywatny. Publiczne opisy pokazują ich budowę
i ograniczenia, bez danych gości ani konfiguracji używanej w firmie. Projekt CLI
można samodzielnie uruchomić.

## Jak pracuję

W projektach kempingu odpowiadam za opis potrzeb recepcji, ustalenie kolejności
zmian i sprawdzenie, czy wynik odpowiada przyjętym wymaganiom. Koordynuję rozwój
z pomocą narzędzi AI, w tym Claude Code i Codex, których używam do implementacji
i weryfikacji.

Błąd widoczny na ekranie może mieć przyczynę w API, bazie danych, skrypcie importu
albo ustawieniach wdrożenia. Sprawdzam zmiany testami i powtarzalnym procesem
budowania aplikacji. Zapisuję też, jak uruchomić projekt, jakie problemy są już
znane i co pozostaje do sprawdzenia.

Opisuję też rozwiązania dotyczące danych gości: dobrowolne zgody, czas przechowywania,
uprawnienia i usuwanie danych. W [notatkach o ochronie danych](engineering-practices.md)
wyjaśniam, co robi kod i gdzie kończą się jego możliwości. Te notatki nie są
pełnym audytem prawnym.
