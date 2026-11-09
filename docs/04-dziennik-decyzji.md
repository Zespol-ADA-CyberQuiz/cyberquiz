# Dziennik decyzji

**Właściciel dokumentu:** właściciel jakości i wiedzy

Zapisujemy tu decyzje, które wpływają na **zakres, narzędzia, strukturę, odpowiedzialność, jakość albo zawartość wydania**. Nie zapisujemy każdej drobnej rozmowy. Celem jest to, żeby po kilku tygodniach dało się zrozumieć, *dlaczego* projekt wygląda tak, a nie inaczej.

**Zasady:**

- dyskusja może się toczyć na Teams albo na spotkaniu, ale **ostateczna decyzja trafia tutaj**,
- **nie usuwamy ani nie przerabiamy starych wpisów.** Gdy decyzja się zmienia, dodajemy nowy wpis, który odwołuje się do starego, a w starym zmieniamy tylko status na „zastąpiona przez D-0XX”,
- nowe wpisy dodajemy na końcu, przez Pull Request.

## Wzór wpisu

```
## D-0XX — [krótki tytuł]

- **Data:**
- **Status:** obowiązuje / zastąpiona przez D-0XX
- **Uczestnicy:**
- **Pytanie:** co trzeba było rozstrzygnąć?
- **Rozważane opcje:**
  1. …
  2. …
- **Wybrana opcja:**
- **Uzasadnienie:**
- **Skutki / powiązane zadania:**
```

---

## D-001 — Wybór produktu

- **Data:** 09.11.2026
- **Status:** obowiązuje
- **Uczestnicy:** Andrzej Derewońko, Damian Piec, Artur Adamczewski
- **Pytanie:** jaki mały produkt IT będzie wspólnym przedmiotem pracy zespołu?
- **Rozważane opcje:**
  1. quiz z cyberbezpieczeństwa,
  2. baza wiedzy IT dla użytkownika (problem → instrukcja → rozwiązane / zgłoszenie),
  3. prototyp rezerwacji sal.
- **Wybrana opcja:** 1, quiz z cyberbezpieczeństwa („CyberQuiz”).
- **Uzasadnienie:** ma jeden jasny proces od startu do wyniku. Łatwo napisać mierzalne kryteria akceptacji i dane testowe (klucz odpowiedzi). Treść (pytania) i funkcje da się równo podzielić na 3 osoby. Temat pasuje do naszej specjalizacji. Zakres jest wykonalny na poziomie pierwszego semestru.
- **Skutki / powiązane zadania:** karta zespołu, zadania #4–#11.

## D-002 — Narzędzia pracy zespołowej

- **Data:** 09.11.2026
- **Status:** obowiązuje
- **Uczestnicy:** Andrzej Derewońko, Damian Piec, Artur Adamczewski
- **Pytanie:** jakich darmowych narzędzi używamy do komunikacji, zadań i plików?
- **Rozważane opcje:**
  1. Microsoft Teams + GitHub (repozytorium, Issues, Projects, Pull Requests, Releases, Pages),
  2. Discord + Trello + Google Drive.
- **Wybrana opcja:** 1, Microsoft Teams + GitHub.
- **Uzasadnienie:** zestaw rekomendowany w instrukcji projektu. Wszyscy mamy dostęp do Microsoft Teams. GitHub łączy w jednym miejscu zadania, zmiany, review, wydania i hosting quizu, a historia zmian jest automatycznym dowodem wkładu każdej osoby. Opcja 2 rozrzuca informacje po trzech narzędziach.
- **Skutki / powiązane zadania:** #1, #2.

## D-003 — Technologia produktu

- **Data:** 09.11.2026
- **Status:** obowiązuje
- **Uczestnicy:** Andrzej Derewońko, Damian Piec, Artur Adamczewski
- **Pytanie:** w czym budujemy quiz?
- **Rozważane opcje:**
  1. czysty HTML + CSS + JavaScript, bez frameworków i bez serwera,
  2. React,
  3. Python (Flask) z serwerem.
- **Wybrana opcja:** 1.
- **Uzasadnienie:** wszyscy możemy to zrozumieć i rozwijać. Quiz otwiera się w przeglądarce bez instalowania czegokolwiek, więc łatwo spełnić kryterium „otwiera się z instrukcji”. Darmowy hosting na GitHub Pages. Opcje 2 i 3 wymagają instalacji, budowania i wiedzy, której nie ma cały zespół.
- **Skutki / powiązane zadania:** #4–#8, #12.

## D-004 — Repozytorium w organizacji GitHub, nie na prywatnym koncie

- **Data:** 09.11.2026
- **Status:** obowiązuje
- **Uczestnicy:** Andrzej Derewońko, Damian Piec, Artur Adamczewski
- **Pytanie:** na czyim koncie zakładamy repozytorium?
- **Rozważane opcje:**
  1. prywatne konto jednej osoby, pozostali jako współpracownicy,
  2. darmowa organizacja GitHub, wszyscy trzej jako właściciele (*Owner*).
- **Wybrana opcja:** 2.
- **Uzasadnienie:** dostęp do projektu i odtwarzania stanu nie może zależeć od jednego konta. Repozytorium jest publiczne, żeby prowadzący i inny zespół mogli je otworzyć bez proszenia o dostęp.
- **Skutki / powiązane zadania:** #1.

## D-005 — Każda zmiana przez Pull Request z review

- **Data:** 09.11.2026
- **Status:** obowiązuje
- **Uczestnicy:** Andrzej Derewońko, Damian Piec, Artur Adamczewski
- **Pytanie:** jak wprowadzamy zmiany do repozytorium?
- **Rozważane opcje:**
  1. każdy wrzuca zmiany bezpośrednio na `main`,
  2. każda zmiana na osobnej gałęzi, Pull Request i zatwierdzenie przez inną osobę, `main` chroniony.
- **Wybrana opcja:** 2.
- **Uzasadnienie:** wymusza review innej osoby, zostawia dowód sprawdzenia i chroni ostatni dobry stan. Opcja 1 grozi nadpisywaniem cudzej pracy i nie zostawia śladu review.
- **Skutki / powiązane zadania:** #1, [proces pracy](03-proces-pracy.md).

## D-006 — Pytania w pliku `pytania.js`, nie w JSON

- **Data:** 09.11.2026
- **Status:** obowiązuje
- **Uczestnicy:** Andrzej Derewońko, Damian Piec, Artur Adamczewski
- **Pytanie:** w jakim formacie przechowujemy pytania?
- **Rozważane opcje:**
  1. plik `pytania.json` wczytywany przez `fetch()`,
  2. plik `pytania.js` z tablicą obiektów, dołączony przez `<script>`.
- **Wybrana opcja:** 2.
- **Uzasadnienie:** przeglądarki blokują `fetch()` dla plików otwieranych lokalnie (`file://`). Z opcją 1 quiz działałby tylko z serwera, a nie po dwukliku w `index.html`. Opcja 2 działa w obu przypadkach.
- **Skutki / powiązane zadania:** #4 (szczegóły formatu ustala i opisuje Damian).

## D-007 — Język projektu

- **Data:** 09.11.2026
- **Status:** obowiązuje
- **Uczestnicy:** Andrzej Derewońko, Damian Piec, Artur Adamczewski
- **Pytanie:** w jakim języku jest quiz i dokumentacja?
- **Wybrana opcja:** polski (quiz, dokumentacja, zadania, commity).
- **Uzasadnienie:** fikcyjny użytkownik jest polskojęzyczny, a cały zespół pisze po polsku.

## D-008 — Numeracja wydań i rotacja ról

- **Data:** 09.11.2026
- **Status:** obowiązuje
- **Uczestnicy:** Andrzej Derewońko, Damian Piec, Artur Adamczewski
- **Pytanie:** jak oznaczamy wydania i kiedy rotujemy role?
- **Wybrana opcja:** pierwsze wydanie `v0.1`, drugie (końcowe) `v1.0`, poprawki `v0.1.x`. Role rotujemy po wydaniu v0.1 według planu z karty zespołu.
- **Uzasadnienie:** prosta, jednoznaczna konwencja zgodna z instrukcją projektu.
