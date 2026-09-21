# Maciej Szulia

Wsparcie techniczne · wdrożenia · aplikacje webowe · Linux  
Olsztyn · Dostępność: pełny etat, zdalnie lub hybrydowo

[Strona i API rezerwacji](case-studies/agrocamping-website.md)
· [System recepcji](case-studies/agrocamping-reception.md)
· [CLI](https://gitlab.com/maciejszulia/rogalddl-scraper)

Praca w AgroCamping Olsztyn, kempingu prowadzonym przez rodziców Macieja Szulii,
obejmuje pomoc przy rezerwacjach i korespondencji z gośćmi oraz koordynację rozwoju
strony i aplikacji recepcji.
Oba projekty AgroCamping wynikają z tej pracy. Pomagają obsłużyć rezerwacje
trafiające do recepcji i utrzymać porządek w danych wymienianych między systemami.

Doświadczenie komercyjne obejmuje stanowiska juniorskie we frontendzie,
e-commerce i systemach CMS, między innymi pracę z PrestaShop i InsERT Sello.

[English](README.md) · [LinkedIn](https://www.linkedin.com/in/maciej-szulia)
· [Strona AgroCamping](https://www.agrocamping.eu/)

## Projekty

- [Strona AgroCamping i API rezerwacji](case-studies/agrocamping-website.md).
  Serwis po polsku, angielsku i niemiecku, z osobnym API. Opis pokazuje,
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

## Sposób pracy

Zakres prac przy projektach kempingu obejmuje opis potrzeb recepcji, ustalenie
kolejności zmian, koordynację rozwoju i sprawdzenie wyników względem przyjętych
wymagań. Do implementacji i weryfikacji służą narzędzia AI, w tym Claude Code i Codex.

Błąd widoczny na ekranie może mieć przyczynę w API, bazie danych, skrypcie importu
albo ustawieniach wdrożenia. Do sprawdzania zmian służą testy i powtarzalny proces
budowania aplikacji. Dokumentacja opisuje uruchomienie projektu, znane problemy
i kwestie, które pozostają do sprawdzenia.

Dokumentacja obejmuje też rozwiązania dotyczące danych gości: dobrowolne zgody,
czas przechowywania, uprawnienia i usuwanie danych.
[Notatki o ochronie danych](engineering-practices.md) wyjaśniają, co robi kod
i gdzie kończą się jego możliwości. Te notatki nie są
pełnym audytem prawnym.
