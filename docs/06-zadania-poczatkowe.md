# Zadania początkowe

Pierwsza paczka zadań, przyjęta 09.11.2026. Każde zadanie zakładamy jako osobne **Issue** z szablonu „Zadanie”, kopiując treść z tej listy, i dodajemy je do tablicy. Numery Issues powinny zgadzać się z numerami poniżej, więc zakładamy je po kolei i **wszystkie przed pierwszym Pull Requestem**, bo Issues i Pull Requesty na GitHubie mają wspólną numerację. Oficjalny stan zadań jest na tablicy, nie w tym pliku.

## Podział pracy

Każdy ma pracę przy produkcie, dokumentacji i review. Nikt nie jest „tylko od pisania” ani „tylko od zarządzania”.

| Osoba | Właściciel zadań | Reviewer zadań |
|---|---|---|
| Andrzej Derewońko | #2, #7, #9, #12 | #1, #5, #6, #10, #13 |
| Damian Piec | #1, #4, #6, #10, #14 | #3, #7, #8, #11 |
| Artur Adamczewski | #3, #5, #8, #11, #13 | #2, #4, #9, #12 |

| Rodzaj pracy | Andrzej | Damian | Artur |
|---|---|---|---|
| Produkt (kod) | #7 | #6 | #5, #8 |
| Produkt (treść pytań) | #9 | #10 | #11 |
| Dokumentacja | #12 | #4, #14 | #3, #13 |
| Środowisko / proces | #2 | #1, #14 | — |

**Kolejność:** dziś #1 → #2 → #3, potem #4 i #5, następnie #6, #8, #9–#11 równolegle, na końcu #7, #12, #13 i #14.

Etykiety do utworzenia w repozytorium: `srodowisko`, `produkt`, `tresc`, `dokumentacja`, `testy`, `wydanie`, `blocked`, `defekt`.

---

## #1 Utworzyć organizację GitHub, repozytorium i tablicę zadań

**Etykiety:** `srodowisko` · **Właściciel:** Damian Piec · **Reviewer:** Andrzej Derewońko · **Zależności:** brak

**Oczekiwany wynik:** darmowa organizacja GitHub z publicznym repozytorium `cyberquiz` zawierającym pliki startowe, chronioną gałęzią `main` i tablicą Projects „CyberQuiz”.

**Kryteria akceptacji:**
- [ ] KA1: Organizacja istnieje i wszyscy trzej członkowie mają w niej rolę *Owner*. Sprawdzenie: każdy widzi zakładkę *Settings* organizacji.
- [ ] KA2: Repozytorium `cyberquiz` jest publiczne. Otwarte w oknie incognito (bez logowania) pokazuje README.
- [ ] KA3: Gałąź `main` ma regułę ochrony „Require a pull request before merging” z co najmniej 1 zatwierdzeniem. Próba bezpośredniego commita na `main` z poziomu przeglądarki jest zablokowana.
- [ ] KA4: Tablica Projects ma kolumny: Backlog, Ready, In progress, In review, Done, Blocked, i jest połączona z repozytorium.
- [ ] KA5: W repozytorium są etykiety wymienione na początku tego pliku.

**Powiązane:** D-004, D-005, `docs/03-proces-pracy.md`

---

## #2 Utworzyć zespół w Microsoft Teams z trzema kanałami

**Etykiety:** `srodowisko` · **Właściciel:** Andrzej Derewońko · **Reviewer:** Artur Adamczewski · **Zależności:** #1 (linki)

**Oczekiwany wynik:** zespół „Zespół ADA – CyberQuiz” z kanałami Ogólny, Produkt, Jakość.

**Kryteria akceptacji:**
- [ ] KA1: Wszyscy trzej są członkami zespołu, a każdy potwierdza na kanale Ogólny, że widzi wszystkie trzy kanały.
- [ ] KA2: Każdy kanał ma w opisie jedno zdanie o przeznaczeniu, zgodne z `docs/02-zasady-komunikacji.md`.
- [ ] KA3: Na kanale Ogólny jest przypięta wiadomość z linkami do repozytorium i tablicy. Reviewer klika oba linki i oba się otwierają.

**Powiązane:** D-002, `docs/02-zasady-komunikacji.md`

---

## #3 Uzupełnić README o linki i sprawdzić opis celu (pierwszy pełny cykl współpracy)

**Etykiety:** `dokumentacja` · **Właściciel (autor):** Artur Adamczewski · **Reviewer:** Damian Piec · **Potwierdzenie stanu:** Andrzej Derewońko · **Zależności:** #1, #2

**Oczekiwany wynik:** README z działającymi linkami do repozytorium, tablicy i Teams, zaakceptowane w Pull Requeście.

**Kryteria akceptacji:**
- [ ] KA1: W tabeli „Linki” w README nie ma już tekstu „[uzupełnić po utworzeniu]” przy repozytorium, tablicy i Teams. Link do GitHub Pages może zostać pusty do #12.
- [ ] KA2: Reviewer klika każdy link z README i każdy prowadzi do właściwego miejsca.
- [ ] KA3: Reviewer zostawia w PR co najmniej jeden merytoryczny komentarz o opisie celu lub procesu, a autor na niego odpowiada albo nanosi poprawkę.
- [ ] KA4: Po scaleniu Andrzej potwierdza w komentarzu zadania, że README na `main` zawiera zmianę, a zadanie jest w kolumnie Done.

**Powiązane:** `README.md`

---

## #4 Ustalić format pytania i dodać jedno przykładowe pytanie

**Etykiety:** `produkt` `dokumentacja` · **Właściciel:** Damian Piec · **Reviewer:** Artur Adamczewski · **Zależności:** brak

**Oczekiwany wynik:** plik `quiz/pytania.js` z tablicą `PYTANIA` zawierającą 1 przykładowe pytanie oraz opis formatu w `quiz/README.md`.

**Kryteria akceptacji:**
- [ ] KA1: Każde pytanie ma pola: `id` (liczba), `kategoria` (`phishing` / `hasla` / `mfa`), `tresc`, `odpowiedzi` (tablica 4 tekstów), `poprawna` (indeks 0–3), `wyjasnienie`, `zrodlo` (adres URL).
- [ ] KA2: `quiz/README.md` opisuje każde pole jednym zdaniem i pokazuje przykład.
- [ ] KA3: Po otwarciu w przeglądarce pustej strony z dołączonym `pytania.js` i wpisaniu w konsoli `PYTANIA.length` wynik to `1`, bez błędów w konsoli.

**Powiązane:** D-006, `quiz/README.md`

---

## #5 Ekran startowy quizu

**Etykiety:** `produkt` · **Właściciel:** Artur Adamczewski · **Reviewer:** Andrzej Derewońko · **Zależności:** brak

**Oczekiwany wynik:** plik `quiz/index.html` z ekranem startowym i stopką.

**Kryteria akceptacji:**
- [ ] KA1: Po otwarciu `quiz/index.html` widać tytuł „CyberQuiz”, jedno- lub dwuzdaniowy opis („10 pytań, ok. 5 minut”) i przycisk „Rozpocznij”.
- [ ] KA2: W stopce widać tekst „CyberQuiz v0.1 · Zespół ADA”.
- [ ] KA3: Strona ma `lang="pl"` i polskie znaki (ą, ę, ł, ó, ś, ż) wyświetlają się poprawnie w Chrome i Edge.
- [ ] KA4: Strona zawiera puste kontenery na ekran pytania i ekran wyniku (z `id`, które wpisujemy w `quiz/README.md`), ukryte na starcie.

**Powiązane:** `quiz/README.md`

---

## #6 Wyświetlanie pytań, zatwierdzanie odpowiedzi i przejście dalej

**Etykiety:** `produkt` · **Właściciel:** Damian Piec · **Reviewer:** Andrzej Derewońko · **Zależności:** #4, #5

**Oczekiwany wynik:** plik `quiz/quiz.js` obsługujący przejście przez wszystkie pytania z `PYTANIA`.

**Kryteria akceptacji:**
- [ ] KA1: Po kliknięciu „Rozpocznij” ekran startowy znika i widać pytanie nr 1, jego 4 odpowiedzi do wyboru (jednokrotny wybór) oraz licznik „Pytanie 1 z N”, gdzie N = `PYTANIA.length`.
- [ ] KA2: Kliknięcie „Zatwierdź” **bez** zaznaczonej odpowiedzi nie zmienia pytania i pokazuje komunikat „Zaznacz odpowiedź, aby przejść dalej”.
- [ ] KA3: Po zaznaczeniu poprawnej odpowiedzi i kliknięciu „Zatwierdź” widać „Dobrze!” i treść `wyjasnienie`. Po zaznaczeniu błędnej widać „Niestety, poprawna odpowiedź to: [tekst]” i `wyjasnienie`.
- [ ] KA4: Po zatwierdzeniu nie da się zmienić odpowiedzi, a pojawia się przycisk „Dalej”, który pokazuje następne pytanie.
- [ ] KA5: Po zatwierdzeniu ostatniego pytania „Dalej” przechodzi do ekranu wyniku (#7). Kod przekazuje liczbę poprawnych odpowiedzi i listę błędnych.

**Powiązane:** D-006, `quiz/README.md`

---

## #7 Ekran wyniku i „Zagraj ponownie”

**Etykiety:** `produkt` · **Właściciel:** Andrzej Derewońko · **Reviewer:** Damian Piec · **Zależności:** #6

**Oczekiwany wynik:** ekran wyniku w `quiz/index.html` + obsługa w `quiz/quiz.js`.

**Kryteria akceptacji:**
- [ ] KA1: Po odpowiedzeniu poprawnie na wszystkie pytania według klucza testowego ekran pokazuje „Twój wynik: 10/10”. Po odpowiedzeniu błędnie na wszystkie pokazuje „0/10”.
- [ ] KA2: Ocena słowna zależy od wyniku: 0–4 → „Uważaj, łatwo Cię oszukać”, 5–7 → „Nieźle, ale jest co poprawić”, 8–10 → „Świetnie!”. Sprawdzić na granicach: 4, 5, 7, 8.
- [ ] KA3: Pod wynikiem jest lista pytań z błędną odpowiedzią (treść pytania i poprawna odpowiedź). Przy wyniku 10/10 zamiast listy jest komunikat „Brak błędów”.
- [ ] KA4: Kliknięcie „Zagraj ponownie” pokazuje pytanie 1 z licznikiem „Pytanie 1 z N”, bez zaznaczonej odpowiedzi, a następny wynik liczy się od zera.

**Powiązane:** `docs/testy/` (klucz testowy z #13)

---

## #8 Styl CSS i czytelność na komputerze i telefonie

**Etykiety:** `produkt` · **Właściciel:** Artur Adamczewski · **Reviewer:** Damian Piec · **Zależności:** #5

**Oczekiwany wynik:** plik `quiz/styl.css` dołączony do `index.html`.

**Kryteria akceptacji:**
- [ ] KA1: Przy szerokości okna 375 px (tryb urządzenia w narzędziach deweloperskich) pytanie, 4 odpowiedzi i przyciski mieszczą się bez przewijania w poziomie.
- [ ] KA2: Przy szerokości 1280 px treść jest wyśrodkowana i ma maksymalnie 800 px szerokości.
- [ ] KA3: Tekst ma rozmiar co najmniej 16 px, a każdą odpowiedź da się wybrać kliknięciem w cały jej wiersz, nie tylko w kółeczko.
- [ ] KA4: Komunikaty „Dobrze!” i „Niestety…” różnią się nie tylko kolorem, ale też tekstem lub ikoną, więc da się je odróżnić bez rozróżniania kolorów.

**Powiązane:** `quiz/index.html`

---

## #9 Pytania 1–4: phishing

**Etykiety:** `tresc` · **Właściciel:** Andrzej Derewońko · **Reviewer:** Artur Adamczewski · **Zależności:** #4

**Oczekiwany wynik:** 4 pytania (`id` 1–4, `kategoria: "phishing"`) w `quiz/pytania.js`.

**Kryteria akceptacji:**
- [ ] KA1: Są 4 pytania zgodne z formatem z #4. Konsola przeglądarki nie pokazuje błędów.
- [ ] KA2: Każde pytanie ma dokładnie jedną poprawną odpowiedź. Reviewer, czytając tylko treść i odpowiedzi, wybiera tę samą poprawną odpowiedź co autor, a każdą rozbieżność omawiamy w PR.
- [ ] KA3: Każde wyjaśnienie ma 1–3 zdania i podaje źródło z wiarygodnej strony (np. CERT Polska, NASK, gov.pl), które reviewer otworzył i potwierdził.
- [ ] KA4: Pytania nie zawierają prawdziwych danych osobowych ani prawdziwych adresów e-mail. Przykłady są fikcyjne.

**Powiązane:** D-006

---

## #10 Pytania 5–7: hasła

**Etykiety:** `tresc` · **Właściciel:** Damian Piec · **Reviewer:** Andrzej Derewońko · **Zależności:** #4

**Oczekiwany wynik:** 3 pytania (`id` 5–7, `kategoria: "hasla"`) w `quiz/pytania.js`.

**Kryteria akceptacji:** jak w #9 (KA1–KA4), dla 3 pytań o hasłach i menedżerach haseł.

**Powiązane:** D-006

---

## #11 Pytania 8–10: MFA i aktualizacje

**Etykiety:** `tresc` · **Właściciel:** Artur Adamczewski · **Reviewer:** Damian Piec · **Zależności:** #4

**Oczekiwany wynik:** 3 pytania (`id` 8–10, `kategoria: "mfa"`) w `quiz/pytania.js`.

**Kryteria akceptacji:** jak w #9 (KA1–KA4), dla 3 pytań o uwierzytelnianiu wieloskładnikowym i aktualizacjach oprogramowania.

**Powiązane:** D-006

---

## #12 Instrukcja uruchomienia i włączenie GitHub Pages

**Etykiety:** `dokumentacja` `srodowisko` · **Właściciel:** Andrzej Derewońko · **Reviewer:** Artur Adamczewski · **Zależności:** #5

**Oczekiwany wynik:** działający adres GitHub Pages i plik `docs/instrukcja-uruchomienia.md`.

**Kryteria akceptacji:**
- [ ] KA1: GitHub Pages jest włączone (gałąź `main`, folder `/`), a adres `https://[organizacja].github.io/cyberquiz/quiz/` otwiera ekran startowy quizu.
- [ ] KA2: Instrukcja opisuje dwa sposoby: (a) przez link, (b) lokalnie, czyli pobranie ZIP z GitHuba, rozpakowanie i otwarcie `quiz/index.html`.
- [ ] KA3: Reviewer, zaczynając od pustego folderu i znając tylko adres repozytorium, otwiera quiz oboma sposobami wyłącznie według instrukcji. Każde miejsce, w którym się zawahał, zapisuje w PR, a autor je poprawia.
- [ ] KA4: Link do GitHub Pages jest w tabeli „Linki” w README.

**Powiązane:** `README.md`

---

## #13 Scenariusze testowe głównego procesu (v0.1)

**Etykiety:** `testy` `dokumentacja` · **Właściciel:** Artur Adamczewski · **Reviewer:** Andrzej Derewońko · **Zależności:** brak (piszemy przed implementacją). Wykonanie testów zależy od #6–#11.

**Oczekiwany wynik:** plik `docs/testy/scenariusze-v0.1.md` z kluczem odpowiedzi i scenariuszami.

**Kryteria akceptacji:**
- [ ] KA1: Plik zawiera klucz testowy: dla każdego z 10 pytań numer poprawnej odpowiedzi (A–D).
- [ ] KA2: Są co najmniej te scenariusze, każdy z danymi wejściowymi i oczekiwanym wynikiem:
  - TS-01: wszystkie poprawne → 10/10, „Świetnie!”, „Brak błędów”,
  - TS-02: wszystkie błędne → 0/10 i lista 10 pytań,
  - TS-03: poprawne tylko 1–5 → 5/10, „Nieźle…”,
  - TS-04: „Zatwierdź” bez zaznaczenia → komunikat, pytanie się nie zmienia,
  - TS-05: „Zagraj ponownie” → pytanie 1, wynik od zera,
  - TS-06: otwarcie lokalne i przez GitHub Pages → ekran startowy, wersja v0.1 w stopce.
- [ ] KA3: Reviewer wykonuje TS-04 na bieżącej wersji (albo potwierdza, że da się go wykonać bez dopytywania autora) i zapisuje wynik w PR.

**Powiązane:** `docs/testy/WZOR-zapis-testu.md`, #6, #7

---

## #14 Wydanie v0.1

**Etykiety:** `wydanie` · **Właściciel (przygotowuje):** Damian Piec · **Przechodzi instrukcję od zera:** Andrzej Derewońko · **Sprawdza spójność:** Artur Adamczewski · **Zależności:** #1–#13

**Oczekiwany wynik:** tag `v0.1`, GitHub Release „CyberQuiz v0.1”, wpis w CHANGELOG, zapis testów v0.1.

**Kryteria akceptacji:**
- [ ] KA1: Andrzej, który nie przygotowywał wydania, otwiera quiz tylko według instrukcji, wykonuje TS-01 do TS-06 i zapisuje wyniki w `docs/testy/` (wszystkie ✅ albo opisane jako znane ograniczenie, które zespół świadomie zaakceptował).
- [ ] KA2: Żaden znany defekt nie blokuje głównego procesu.
- [ ] KA3: Tag `v0.1`, Release, CHANGELOG i stopka strony pokazują tę samą wersję. Release zawiera opis funkcji, znane ograniczenia i hash commita.
- [ ] KA4: Artur potwierdza w komentarzu zadania, że tablica (zadania #1–#13 w Done), CHANGELOG i Release opisują ten sam stan.
- [ ] KA5: Jeśli któreś kryterium nie przejdzie, zapisujemy nieudane sprawdzenie, wracamy z zadaniem do pracy z właścicielem i powtarzamy sprawdzenia przed wydaniem.

**Powiązane:** `CHANGELOG.md`, `docs/03-proces-pracy.md` (punkt 6)
