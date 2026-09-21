# Maciej Szulia

Wsparcie techniczne · wdrożenia · aplikacje webowe · Linux  
Olsztyn · Szukam pracy na pełny etat, zdalnie lub hybrydowo

[Strona i API rezerwacji](case-studies/agrocamping-website.md)
· [System recepcji](case-studies/agrocamping-reception.md)
· [CLI](https://gitlab.com/maciejszulia/rogalddl-scraper)

Pomagam przy rezerwacjach i korespondencji z gośćmi w AgroCamping Olsztyn,
kempingu moich rodziców. Koordynuję też rozwój strony i aplikacji recepcji.
Oba projekty AgroCamping powstały z potrzeby obsługi rezerwacji,
uporządkowania danych i rozwiązywania problemów z integracjami.

Mam również doświadczenie komercyjne na stanowiskach juniorskich we frontendzie,
e-commerce i systemach CMS. Pracowałem między innymi z PrestaShop i InsERT Sello.

[English](README.md) · [LinkedIn](https://www.linkedin.com/in/maciej-szulia)
· [Strona AgroCamping](https://www.agrocamping.eu/)

## Projekty

- [Strona AgroCamping i API rezerwacji](case-studies/agrocamping-website.md).
  Serwis po polsku, angielsku i niemiecku, z osobnym API. W opisie pokazuję drogę
  rezerwacji do recepcji, obsługę awarii powiadomień oraz ograniczanie danych
  zapisywanych przez formularz i analitykę.
- [System recepcji](case-studies/agrocamping-reception.md).
  Aplikacja do codziennej pracy z rezerwacjami. Opis obejmuje między innymi
  ponowny import rezerwacji bez nadpisywania zmian pracownika, uprawnienia
  użytkowników i przywracanie działania po nieudanym wdrożeniu.
- [Lokalny katalog metadanych, CLI](https://gitlab.com/maciejszulia/rogalddl-scraper).
  Mniejszy projekt w Node.js, bez zależności npm. Można pobrać kod i sprawdzić,
  dlaczego wpis został zachowany, połączony z innym albo odrzucony. Testy działają
  offline, a README opisuje instalację i sprawdzanie danych wejściowych.

Kod systemów firmowych pozostaje prywatny. Publiczne opisy pokazują ich budowę
i ograniczenia, bez danych gości ani konfiguracji używanej w firmie. Projekt CLI
można samodzielnie uruchomić.

## Jak pracuję

W projektach kempingu opisuję potrzeby recepcji, ustalam kolejność zmian i sprawdzam
wynik względem przyjętych wymagań. Korzystam z Claude Code i Codex przy implementacji
oraz weryfikacji. Mój udział w tych projektach obejmuje kierowanie pracą wspieraną
przez AI i odbiór tego, co powstało.

Przy szukaniu przyczyny błędu trzeba czasem przejść od ekranu przez API i bazę danych
aż do skryptu importu albo ustawień wdrożenia. Zmiany sprawdzam testami i powtarzalnym
procesem budowania aplikacji. W dokumentacji zostawiam instrukcje uruchomienia,
opis znanych problemów i informację o tym, czego jeszcze nie sprawdzono.

Opisuję też rozwiązania dotyczące danych gości: dobrowolne zgody, czas przechowywania,
uprawnienia i usuwanie danych. W [notatkach o ochronie danych](engineering-practices.md)
można przeczytać, co robi kod i jakie są granice tych zabezpieczeń. To opis
konkretnych mechanizmów, bez deklarowania pełnego audytu prawnego.
