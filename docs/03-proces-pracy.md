# Proces pracy

**Status:** obowiązujący · **Data przyjęcia:** 09.11.2026 · **Właściciel dokumentu:** właściciel repozytorium i integracji

Ten dokument opisuje, jak zadanie przechodzi od pomysłu do zaakceptowanego wyniku.

---

## 1. Tablica zadań

Oficjalny stan pracy jest na tablicy **GitHub Projects „CyberQuiz”**. Jeśli tablica i rozmowa na Teams się nie zgadzają, obowiązuje tablica, a rozbieżność trzeba poprawić.

| Kolumna | Znaczenie |
|---|---|
| **Backlog** | zadanie zapisane, czeka (brak kryteriów albo nie teraz) |
| **Ready** | ma kryteria akceptacji i właściciela, zależności są spełnione, można zaczynać |
| **In progress** | właściciel naprawdę nad tym pracuje |
| **In review** | wynik jest gotowy, otwarty Pull Request czeka na review innej osoby |
| **Done** | spełnia [Definition of Done](#3-definition-of-done) |
| **Blocked** | stoi, w komentarzu jest opisane, co blokuje i czego potrzeba |

**Zasady:**

- każde aktywne zadanie ma **jednego właściciela** (pole *Assignees*). Inni mogą pomagać, ale za ruch do przodu odpowiada właściciel,
- w zadaniu wpisujemy też **reviewera** (w treści zadania),
- jedna osoba ma naraz maksymalnie **2 zadania w „In progress”**,
- koordynator co tydzień sprawdza, czy tablica odpowiada rzeczywistości i czy praca jest równo rozłożona.

---

## 2. Zadanie: jak je napisać

Każde zadanie opisuje **jeden wynik**, który da się skończyć i sprawdzić. Zadania typu „zrobić aplikację” albo „napisać dokumentację” są za duże i trzeba je podzielić.

Zadanie zakładamy z szablonu **Zadanie** (zakładka Issues → New issue). Musi zawierać:

1. **Oczekiwany wynik:** co konkretnie powstanie (plik, ekran, zapis),
2. **Kryteria akceptacji:** spisane *przed* rozpoczęciem pracy,
3. **Właściciela i reviewera,**
4. **Powiązane pliki lub wymagania,**
5. **Zależności:** od jakich zadań zależy (np. „zależy od #4”).

### Kryteria akceptacji: zasady

Każde kryterium opisuje **obserwowalny wynik**, który da się ocenić jako *spełnione / niespełnione* bez zgadywania, co autor miał na myśli. Używamy schematu:

> **Warunek początkowy** → **Akcja** → **Oczekiwany wynik** (+ przypadek brzegowy lub błędny)

| ❌ Niedopuszczalne | ✅ Dobre |
|---|---|
| „Strona ma ładnie wyglądać” | „Na ekranie o szerokości 375 px (telefon) treść pytania i 4 odpowiedzi mieszczą się bez przewijania w poziomie” |
| „Quiz ma działać poprawnie” | „Po zaznaczeniu poprawnych odpowiedzi według klucza testowego we wszystkich 10 pytaniach ekran wyniku pokazuje 10/10 i ocenę »Świetnie!«” |
| „Instrukcja ma być kompletna” | „Osoba, która nie pisała instrukcji, zaczynając od pustego folderu, otwiera quiz w mniej niż 5 minut tylko na podstawie instrukcji” |

- **Produkt:** podajemy dane testowe, akcję użytkownika, oczekiwany wynik i co ma się stać przy braku lub błędnych danych.
- **Dokumentacja:** podajemy, kto ma umieć wykonać instrukcję, od jakiego stanu wyjściowego i co dowodzi, że instrukcja wystarcza.
- **Proces zespołu:** podajemy, jaki zapis ma istnieć, gdzie, kto go sprawdza i jak potwierdzamy, że wszyscy trzej potrafią z niego korzystać.

Kryteria możemy **doprecyzować przed rozpoczęciem pracy**, ale **nie wolno ich osłabiać po fakcie**, żeby niekompletny wynik wyglądał na zaakceptowany. Istotna zmiana kryteriów wymaga decyzji w dzienniku decyzji i aktualizacji zadania.

---

## 3. Definition of Done

Zadanie jest **Done** dopiero wtedy, gdy **wszystkie** punkty są spełnione:

1. ☐ oczekiwany wynik istnieje w repozytorium (albo we wskazanym wspólnym miejscu),
2. ☐ każde kryterium akceptacji zostało sprawdzone i oznaczone jako ✅ spełnione, ❌ niespełnione albo ⚠️ nie dało się sprawdzić,
3. ☐ review wykonała **inna osoba niż autor**,
4. ☐ wymagane poprawki zostały naniesione, a kryteria, których dotyczyły, sprawdzone ponownie,
5. ☐ powiązana dokumentacja jest aktualna (w tym samym Pull Requeście),
6. ☐ Pull Request jest scalony do `main`, a zadanie zamknięte i przeniesione do **Done**,
7. ☐ jest dowód sprawdzenia (patrz punkt 5).

Zadanie z kryterium ❌ albo ⚠️ **nie trafia do Done**. Wraca do „In progress”.

---

## 4. Zmiany w plikach i review

### Przebieg zmiany

1. Bierzesz zadanie z „Ready”, przypisujesz siebie i przesuwasz do „In progress”.
2. Tworzysz gałąź o nazwie `nr-zadania-krotki-opis`, np. `6-wyswietlanie-pytan`.
3. Robisz zmiany w małych commitach z opisem, np. `#6 Dodano przycisk Zatwierdź`.
4. Otwierasz **Pull Request** do `main`. W opisie piszesz `Closes #6`, wypełniasz szablon i wskazujesz reviewera.
5. Przesuwasz zadanie do „In review” i piszesz na kanale **Jakość**.
6. Reviewer sprawdza wynik względem zadania i zakresu, a potem zatwierdza albo prosi o zmiany.
7. Autor nanosi poprawki i odpowiada na komentarze.
8. Po zatwierdzeniu PR scala **autor albo właściciel repozytorium**.

Gałąź `main` jest chroniona: **nie da się scalić zmiany bez zatwierdzenia przez inną osobę**.

### Zasady review

- Autor ważnego wyniku **nie może być jego jedynym reviewerem**.
- Reviewer porównuje wynik z **zadaniem, kryteriami akceptacji i zakresem projektu**.
- Komentarz wskazuje, co jest **niejasne, błędne, brakujące albo ryzykowne**, i podaje **powód** prośby o zmianę.
- Samo „LGTM” albo „ok” nie wystarcza. Nawet przy braku uwag reviewer pisze, **co sprawdził**, np. „Otworzyłem lokalnie w Chrome i Edge, przeszedłem pytania 1–4, wyjaśnienia zgadzają się ze źródłami, bez uwag”.
- Reviewer w komentarzu do PR oznacza każde kryterium akceptacji jako ✅ / ❌ / ⚠️.

---

## 5. Dowody akceptacji

Każde zakończone zadanie zostawia dowód, że kryteria sprawdzono. Dowodem może być:

- zatwierdzony Pull Request z komentarzami reviewera,
- zapis testu w `docs/testy/` (wzór: [docs/testy/WZOR-zapis-testu.md](testy/WZOR-zapis-testu.md)),
- zrzut ekranu widocznego wyniku (bez danych osobowych, prywatnych wiadomości i niezwiązanych kart przeglądarki),
- przykładowe wejście i wynik,
- wpis w historii repozytorium albo link do wydania.

Dowód musi wskazywać: **zadanie, sprawdzaną wersję lub commit, reviewera, wynik dla każdego kryterium i pozostałe ograniczenia**. Musi być zrozumiały po kilku tygodniach i nie może zależeć od prywatnych wiadomości ani tymczasowych linków. Zdanie „wszystko przetestowaliśmy” nie jest dowodem.

---

## 6. Wersje i wydania

- Wersje oznaczamy tagami: `v0.1` (pierwsze wydanie), `v1.0` (drugie, końcowe wydanie). Ewentualne poprawki: `v0.1.1`.
- Numer wersji jest widoczny w stopce strony quizu.
- Każde wydanie ma wpis w [CHANGELOG.md](../CHANGELOG.md) i w GitHub Releases. Wpis zawiera nowe funkcje, zmiany zachowania, poprawione błędy i znane ograniczenia.
- **Przy wydaniu:** jedna osoba je przygotowuje, druga przechodzi instrukcję od zera, a trzecia sprawdza, czy repozytorium, tablica i CHANGELOG opisują tę samą wersję.

---

## 7. Odtworzenie ostatniego dobrego stanu

Ostatni zaakceptowany stan to **ostatni tag wydania** albo ostatni scalony i zatwierdzony PR na `main`. Szczegółową procedurę odtworzenia dopisze właściciel repozytorium przy ćwiczeniu odtwarzania stanu (Part Two). Do tego czasu nikt nie wykonuje `git push --force` na `main`.
