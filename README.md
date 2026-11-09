# CyberQuiz — sprawdź swoją czujność

Projekt semestralny z przedmiotu **Technologie pracy grupowej** (Akademia Finansów i Biznesu Vistula).
Zespół: **Zespół ADA**.

| Członek zespołu | Nr albumu | Rola (od 09.11.2026) |
|---|---|---|
| Andrzej Derewońko | [nr albumu] | Koordynator zespołu |
| Damian Piec | 71654 | Właściciel repozytorium i integracji |
| Artur Adamczewski | [nr albumu] | Właściciel jakości i wiedzy |

## Cel projektu

CyberQuiz to prosta strona internetowa z quizem o podstawach cyberbezpieczeństwa (phishing, hasła, uwierzytelnianie wieloskładnikowe, aktualizacje). Użytkownik odpowiada na 10 pytań, po każdej odpowiedzi dowiaduje się, czy była poprawna i dlaczego, a na końcu widzi swój wynik.

Produkt jest celowo mały. Głównym celem projektu jest przećwiczenie pracy zespołu IT: podziału odpowiedzialności, review, zapisywania decyzji, kontroli zmian i dzielenia się wiedzą.

## Główny proces

Użytkownik otwiera stronę quizu i klika „Rozpocznij”. Widzi kolejno 10 pytań jednokrotnego wyboru. Przy każdym pytaniu zaznacza jedną odpowiedź i klika „Zatwierdź”. Strona pokazuje, czy odpowiedź jest poprawna, wraz z krótkim wyjaśnieniem, a przycisk „Dalej” przechodzi do następnego pytania. Bez zaznaczonej odpowiedzi nie można przejść dalej. Po 10. pytaniu użytkownik widzi wynik (np. 7/10), ocenę słowną i listę pytań, na które odpowiedział błędnie. Przycisk „Zagraj ponownie” uruchamia quiz od początku.

## Aktualny stan

- **Etap:** start projektu (09.11.2026), przed pierwszym wydaniem.
- **Aktualna wersja:** brak. Pierwsze wydanie to `v0.1`.
- **Historia zmian:** [CHANGELOG.md](CHANGELOG.md)

## Linki

| Zasób | Link |
|---|---|
| Repozytorium | [uzupełnić po utworzeniu] |
| Tablica zadań (GitHub Projects) | [uzupełnić po utworzeniu] |
| Zespół w Microsoft Teams | [uzupełnić po utworzeniu] |
| Działający quiz (GitHub Pages) | [uzupełnić po włączeniu Pages] |

## Gdzie co jest

| Czego szukasz | Gdzie |
|---|---|
| Cel, zakres, role, zastępstwa | [docs/01-karta-zespolu.md](docs/01-karta-zespolu.md) |
| Zasady komunikacji i eskalacji | [docs/02-zasady-komunikacji.md](docs/02-zasady-komunikacji.md) |
| Jak pracujemy: tablica, Definition of Done, review, kryteria akceptacji | [docs/03-proces-pracy.md](docs/03-proces-pracy.md) |
| Decyzje zespołu | [docs/04-dziennik-decyzji.md](docs/04-dziennik-decyzji.md) |
| Historia ról i przekazań | [docs/05-historia-rol.md](docs/05-historia-rol.md) |
| Zadania początkowe (wzór do Issues) | [docs/06-zadania-poczatkowe.md](docs/06-zadania-poczatkowe.md) |
| Zapisy testów | [docs/testy/](docs/testy/) |
| Pliki produktu (quiz) | [quiz/](quiz/) |
| Bieżące zadania | zakładka **Issues** i tablica w **Projects** |
| Wydania | zakładka **Releases** oraz [CHANGELOG.md](CHANGELOG.md) |

## Jak uruchomić

Instrukcja powstanie w zadaniu #12 i będzie w pliku `docs/instrukcja-uruchomienia.md`. W skrócie quiz będzie można otworzyć na dwa sposoby:

1. przez link GitHub Pages (tabela „Linki” powyżej),
2. lokalnie: pobrać repozytorium i otworzyć `quiz/index.html` w przeglądarce. Nie trzeba niczego instalować.

## Jak zgłosić zadanie lub błąd

Nowe zadanie lub błąd zakładamy w zakładce **Issues** z szablonu „Zadanie” albo „Defekt”. Każda zmiana w plikach przechodzi przez Pull Request i review innej osoby. Szczegóły: [docs/03-proces-pracy.md](docs/03-proces-pracy.md).
