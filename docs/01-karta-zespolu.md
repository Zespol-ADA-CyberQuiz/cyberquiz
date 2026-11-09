# Karta zespołu (Team Charter)

**Status:** obowiązująca · **Wersja karty:** 1.0 · **Data przyjęcia:** 09.11.2026
**Właściciel dokumentu:** koordynator zespołu · **Następny przegląd:** po wydaniu v0.1

Karta to pierwsze wspólne porozumienie zespołu. Zmieniamy ją tylko decyzją zapisaną w [dzienniku decyzji](04-dziennik-decyzji.md).

---

## 1. Zespół

**Nazwa zespołu:** Zespół ADA (od pierwszych liter imion: **A**ndrzej, **D**amian, **A**rtur)

| Imię i nazwisko | Nr albumu |
|---|---|
| Andrzej Derewońko | [nr albumu] |
| Damian Piec | [nr albumu] |
| Artur Adamczewski | [nr albumu] |

### Umiejętności, które już mamy

| Osoba | Umiejętności przydatne w projekcie |
|---|---|
| Andrzej Derewońko | wsparcie IT (helpdesk), Microsoft 365 i Teams, podstawy programowania, [do uzupełnienia] |
| Damian Piec | [do uzupełnienia] |
| Artur Adamczewski | [do uzupełnienia] |

Brakujące umiejętności (np. JavaScript, Git) zdobywamy w trakcie projektu i zapisujemy wiedzę w dokumentacji. Nie oddajemy całej pracy jednej osobie, bo „ona umie najlepiej”.

---

## 2. Produkt

**Tytuł projektu:** CyberQuiz — sprawdź swoją czujność

**Cel:** prosta strona z quizem, która w kilka minut sprawdza podstawową wiedzę użytkownika o bezpiecznym korzystaniu z komputera i internetu, i wyjaśnia błędy.

**Użytkownik (fikcyjny):** student lub pracownik biurowy bez wykształcenia technicznego, który chce sprawdzić, czy rozpozna phishing i czy dobrze dba o hasła i konta.

**Główny proces (od początku do wyniku):**
Użytkownik otwiera stronę i klika „Rozpocznij”. Odpowiada kolejno na 10 pytań jednokrotnego wyboru: zaznacza odpowiedź, klika „Zatwierdź”, widzi, czy odpowiedź jest poprawna, wraz z wyjaśnieniem, i przechodzi „Dalej”. Bez zaznaczonej odpowiedzi nie można przejść dalej. Po ostatnim pytaniu widzi wynik (np. 7/10), ocenę słowną i listę błędnych odpowiedzi, a potem może zagrać ponownie.

### Minimalny działający wynik (wersja v0.1)

- strona otwiera się z linku GitHub Pages i lokalnie z pliku `quiz/index.html`, bez instalowania czegokolwiek,
- 10 pytań w 3 tematach: phishing (4), hasła (3), MFA i aktualizacje (3),
- każde pytanie ma 4 odpowiedzi, dokładnie jedna jest poprawna, każde ma wyjaśnienie i źródło,
- blokada przejścia dalej bez zaznaczonej odpowiedzi,
- ekran wyniku: wynik liczbowy, ocena słowna, lista błędnych odpowiedzi, przycisk „Zagraj ponownie”,
- numer wersji widoczny w stopce strony,
- instrukcja uruchomienia, scenariusze testowe z wynikami, notatki do wydania ze znanymi ograniczeniami.

### Poza zakresem (nie robimy)

- logowanie, konta użytkowników, zapisywanie wyników na serwerze, ranking online,
- backend, baza danych, serwer własny, infrastruktura produkcyjna,
- płatności, prawdziwe dane osobowe, integracja z systemami uczelni,
- funkcje wymagające wiedzy, której zespół nie ma (np. frameworki, których nikt nie zna).

### Pomysły na przyszłość (nie wchodzą do bieżącego zakresu)

- losowa kolejność pytań i odpowiedzi,
- wybór kategorii przed startem,
- licznik czasu na pytanie,
- zapamiętanie najlepszego wyniku w przeglądarce (localStorage),
- tryb ciemny,
- większa baza pytań.

Jeden z tych pomysłów może zostać naszą kontrolowaną zmianą wymagań po wydaniu v0.1.

---

## 3. Co uznajemy za sukces

Projekt jest udany, gdy:

1. quiz da się otworzyć wyłącznie na podstawie spisanej instrukcji,
2. główny proces da się przejść od początku do wyniku na danych testowych i wynik zgadza się z oczekiwanym,
3. aktualna wersja jest jednoznaczna: ten sam numer widać na stronie, w Releases, w CHANGELOG i na tablicy,
4. ważne decyzje są zapisane w dzienniku decyzji razem z uzasadnieniem,
5. inny zespół rozumie projekt bez prywatnych wyjaśnień,
6. każdy z nas ma widoczny wkład w produkt, dokumentację, review, testy i koordynację.

---

## 4. Czego oczekujemy od siebie nawzajem

- **Praca jest widoczna.** Co robimy, widać na tablicy. Zadanie „W toku” jest naprawdę w toku.
- **Problemy zgłaszamy wcześnie**, zanim zrobią się pilne. Ukryte opóźnienie szkodzi bardziej niż szybka informacja „mam problem”.
- **Deklaracje są realne.** Lepiej wziąć mniej i dowieźć niż obiecać dużo.
- **Prośba o pomoc jest w porządku.** Nikt nie musi wszystkiego umieć.
- **Krytykujemy pracę, nie osobę.** Komentarz w review mówi, co jest nie tak, dlaczego i jak to poprawić.
- **Odpowiadamy na merytoryczną treść review**, a nie traktujemy go jak oceny osoby.
- **Ustalenia z prywatnych wiadomości przenosimy** do wspólnego kanału lub na GitHub.

---

## 5. Role i zastępstwa

Role oznaczają odpowiedzialność za „zdrowie” procesu, a nie własność kawałka projektu. Każdy, niezależnie od roli, robi część produktu, dokumentacji i review.

| Rola | Osoba (od 09.11.2026) | Zastępca | Za co odpowiada |
|---|---|---|---|
| Koordynator zespołu | Andrzej Derewońko | Artur Adamczewski | utrzymuje tablicę zgodną z rzeczywistością, wyłapuje zablokowane zadania, pilnuje zakresu, prowadzi krótkie check-iny |
| Właściciel repozytorium i integracji | Damian Piec | Andrzej Derewońko | struktura plików, proces zmian (gałęzie, Pull Requesty), zaakceptowane wersje i tagi, procedura odtworzenia stanu |
| Właściciel jakości i wiedzy | Artur Adamczewski | Damian Piec | pilnuje review i testów, dziennika decyzji, instrukcji i materiałów potrzebnych do przejęcia pracy przez inną osobę |

**Zasada zastępstwa:** jeśli właściciel roli jest niedostępny dłużej niż 48 godzin albo zgłosi niedostępność, zastępca przejmuje bieżące obowiązki roli. Żadna ważna czynność nie może zależeć od tego, że jedna konkretna osoba jest akurat online.

**Rotacja ról:** po wydaniu v0.1 role przesuwają się o jedną pozycję, tak by każdy przeszedł przez każdą rolę. Przekazanie zapisujemy w [historii ról](05-historia-rol.md).

| Okres | Koordynator | Repozytorium i integracja | Jakość i wiedza |
|---|---|---|---|
| start → v0.1 | Andrzej | Damian | Artur |
| v0.1 → rotacja 2 | Artur | Andrzej | Damian |
| rotacja 2 → koniec semestru | Damian | Artur | Andrzej |

---

## 6. Gdzie jest wszystko

| Co | Gdzie |
|---|---|
| Komunikacja | Microsoft Teams, zespół „Zespół ADA – CyberQuiz” ([zasady](02-zasady-komunikacji.md)) |
| Zadania (oficjalny stan pracy) | GitHub Projects, tablica „CyberQuiz” |
| Pliki produktu i dokumentacja | repozytorium GitHub `cyberquiz` |
| Decyzje | [docs/04-dziennik-decyzji.md](04-dziennik-decyzji.md) |
| Wydania | GitHub Releases + [CHANGELOG.md](../CHANGELOG.md) |

---

## 7. Akceptacja karty

Każdy członek potwierdza, że przeczytał kartę i się z nią zgadza, zatwierdzając Pull Request z tą kartą albo dopisując się poniżej.

- [ ] Andrzej Derewońko — data:
- [ ] Damian Piec — data:
- [ ] Artur Adamczewski — data:
