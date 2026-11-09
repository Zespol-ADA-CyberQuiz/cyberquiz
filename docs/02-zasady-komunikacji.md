# Zasady komunikacji (Working Agreement)

**Status:** obowiązujące · **Data przyjęcia:** 09.11.2026 · **Właściciel dokumentu:** koordynator zespołu

## 1. Gdzie co piszemy

| Miejsce | Do czego służy |
|---|---|
| Teams → kanał **Ogólny** | ogłoszenia, organizacja zespołu, terminy, check-iny |
| Teams → kanał **Produkt** | implementacja quizu, treść pytań, pytania techniczne |
| Teams → kanał **Jakość** | prośby o review, wyniki testów, decyzje o wydaniu |
| GitHub **Issues + Projects** | oficjalny stan pracy: każde zadanie, właściciel, status, blokady |
| GitHub **Pull Requests** | propozycje zmian i review |
| `docs/04-dziennik-decyzji.md` | ostateczne decyzje zespołu |
| Wiadomości prywatne | tylko krótka koordynacja („dzwonię za 5 min”) |

**Zasada:** jeśli ustalenie wpływa na projekt, ląduje we wspólnym miejscu (kanał, Issue, dziennik decyzji), a nie zostaje w prywatnej wiadomości ani w czyjejś pamięci.

Każdy kanał ma przypiętą wiadomość z linkami do repozytorium, tablicy i działającego quizu.

## 2. Czas odpowiedzi

- Na **pytania bezpośrednie** (z @wzmianką) odpowiadamy **w ciągu 24 godzin**, także krótko: „widzę, odpiszę jutro”.
- Na **prośbę o review** odpowiadamy **w ciągu 48 godzin**.
- Wiadomość wysłana **po 21:00 lub w weekend** nie wymaga natychmiastowej odpowiedzi. Termin liczymy od następnego dnia roboczego.
- Nie oczekujemy stałej dostępności. Jeśli wiemy, że nie będzie nas kilka dni, piszemy o tym na kanale **Ogólny** z wyprzedzeniem i informujemy zastępcę roli.

## 3. Asynchronicznie czy spotkanie?

**Domyślnie piszemy asynchronicznie.** Status jest na tablicy, materiały w repozytorium, a rutynowe pytania na kanale.

**Krótkie spotkanie na Teams (do 20 minut)** robimy, gdy:

- trzeba rozwiązać niejasność, której nie da się szybko wyjaśnić w wiadomościach,
- trzeba wybrać między kilkoma opcjami,
- jest konflikt (o zakres, jakość albo odpowiedzialność),
- dyskusja w wątku przekroczyła ok. 10 wiadomości bez rozstrzygnięcia.

**Po spotkaniu** osoba prowadząca w ciągu 24 godzin:

1. zapisuje decyzję w dzienniku decyzji,
2. aktualizuje lub tworzy zadania na tablicy, z właścicielami,
3. wrzuca krótkie podsumowanie na odpowiedni kanał.

## 4. Check-in

Raz w tygodniu (po zajęciach lub w środę wieczorem) każdy pisze na kanale **Ogólny** trzy krótkie punkty:

```
✅ Zrobione: …
➡️ Następne: …
⛔ Blokady: … (albo „brak”)
```

To nie jest raport z każdej czynności. Szczegóły są na tablicy i w repozytorium.

## 5. Zasada eskalacji (zablokowana praca)

Gdy nie możesz skończyć zadania, nie rozumiesz, co ma być wynikiem, albo czekasz na cudzą pracę:

1. **Przesuń zadanie do kolumny „Blocked”** i dodaj etykietę `blocked`.
2. **Dopisz komentarz w zadaniu:** co blokuje, od czego zależy i czego potrzebujesz.
3. **Oznacz koordynatora** (@) na kanale **Produkt** lub **Jakość**.
4. Koordynator w ciągu 24 godzin decyduje razem z zespołem, czy:
   - doprecyzować zadanie,
   - zmienić właściciela,
   - zmniejszyć zakres,
   - dać pomoc (np. praca w parze).
5. Decyzję zapisujemy w komentarzu zadania, a jeśli dotyczy zakresu, także w dzienniku decyzji.

**Milczenie nie jest sposobem na zarządzanie opóźnieniem.** Jeśli zadanie stoi w „In progress” dłużej niż 3 dni bez żadnego ruchu, koordynator pyta właściciela o stan.

Jeśli zespół nie może sam rozwiązać problemu zagrażającego projektowi, opisujemy fakty i możliwe opcje i prosimy prowadzącego o decyzję.

## 6. Jak rozmawiamy o pracy

- Komentarz w review: **co** jest nie tak, **dlaczego** i **propozycja** poprawki.
- Odpowiadamy na treść uwagi, a nie na ton.
- Przy sporze wracamy do karty zespołu, kryteriów akceptacji zadania i zapisanych dowodów.
- Niedopuszczalne: osobista krytyka, przerywanie, ignorowanie wiadomości, ciche wycofanie się z pracy.
