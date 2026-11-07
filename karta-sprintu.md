# Karta sprintu 1

Wypełnia zespół na zajęciach 2, krok po kroku. Można ją prowadzić w tym pliku albo od razu w GitHub Projects (patrz krok 5).

**Zespół:** NoName5  **Temat projektu:** PanBilecik, platforma z biletami na wydarzenia kulturalne

---

## Krok 1. Role Scrum

| Rola | Osoba | Za co odpowiada w naszym zespole |
|---|---|---|
| Product Owner (PO) | Bartłomiej Pisarek | ustala kolejność w backlogu, decyduje o MoSCoW, akceptuje „zrobione” po sprawdzeniu kryteriów akceptacji |
| Scrum Master (SM) | Jakub Kierklo | pilnuje zasad i terminów, usuwa przeszkody, prowadzi planowanie i przegląd sprintu, dba o aktualną tablicę |
| Developerzy | Bartłomiej Pisarek, Jakub Kierklo, Jakub Kuśmierski, Zbigniew Czarnecki, Tomasz Nowak | wszyscy (PO i SM też programują), każdy bierze zadania z tablicy i wpisuje się przy nich |

Role z karty zespołu (koordynator, opiekun repozytorium, opiekun jakości) zostają jako dodatkowe obowiązki:

| Dodatkowa rola | Osoba |
|---|---|
| Koordynator | Bartłomiej Pisarek |
| Opiekun repozytorium | Zbigniew Czarnecki |
| Opiekun jakości | Jakub Kierklo |

Kanał komunikacji: Discord, odpowiadamy w ciągu 24 h w dni robocze. Stałe spotkanie zespołu: środa 19:00.

## Krok 2. Wizja produktu

> Dla **mieszkańców miasta**, którzy **chcą pójść na koncert, spektakl albo wystawę, ale repertuar i bilety są rozrzucone po stronach wielu instytucji**, **PanBilecik** to **aplikacja webowa**, która **w jednym miejscu pokazuje nadchodzące wydarzenia kulturalne i pozwala od razu kupić na nie bilet**. W odróżnieniu od **szukania wydarzeń i kupowania biletów osobno na stronie każdego teatru, klubu czy galerii** nasz produkt **zbiera ofertę wielu organizatorów i daje jeden prosty sposób zakupu z biletem w telefonie**.

Użytkownicy (min. 2 typy):
1. Widz: szuka wydarzenia, kupuje bilet, pokazuje go przy wejściu.
2. Organizator: dodaje wydarzenia, ustala pulę biletów i cenę, sprawdza sprzedaż.
3. Bileter (obsługa wejścia): sprawdza bilety przy drzwiach.

## Krok 3. Product backlog

Format: **Jako** [użytkownik] **chcę** [funkcja], **aby** [korzyść]. Do każdej historyjki min. 2 kryteria akceptacji.

Kolejność w tabeli to kolejność priorytetów ustalona przez PO.

| ID | Historyjka | Kryteria akceptacji | MoSCoW | Punkty |
|---|---|---|---|---|
| H1 | Jako widz chcę przeglądać listę nadchodzących wydarzeń, aby wybrać coś dla siebie. | 1. Lista jest posortowana od najbliższej daty i pokazuje nazwę, datę, miejsce i cenę. 2. Wydarzenia, które już się odbyły, nie pojawiają się na liście. | M | 2 |
| H2 | Jako widz chcę zobaczyć szczegóły wydarzenia, aby zdecydować, czy kupić bilet. | 1. Widzę opis, adres, godzinę, cenę i liczbę wolnych biletów. 2. Gdy biletów nie ma, widzę napis „Wyprzedane”, a przycisk „Kup” jest nieaktywny. | M | 1 |
| H3 | Jako organizator chcę dodać wydarzenie z ceną i liczbą biletów, aby sprzedawać je przez platformę. | 1. Formularz nie przyjmie wydarzenia bez nazwy, miejsca, ceny i liczby biletów ani z datą z przeszłości. 2. Po zapisaniu wydarzenie od razu pojawia się na liście dla widzów. | M | 3 |
| H4 | Jako widz chcę kupić bilety na wybrane wydarzenie, aby mieć pewność, że wejdę. | 1. Po wybraniu liczby biletów, podaniu e-maila i potwierdzeniu widzę podsumowanie zamówienia, a liczba wolnych biletów maleje. 2. Nie mogę kupić więcej biletów, niż zostało, ani więcej niż 6 w jednym zamówieniu. 3. Płatność w sprincie 1 jest symulowana (przycisk „Zapłać”). | M | 5 |
| H5 | Jako widz chcę dostać bilet z kodem QR, aby pokazać go przy wejściu z telefonu. | 1. Każdy kupiony bilet ma unikalny kod QR. 2. Bilet przychodzi na e-mail podany przy zakupie. | M | 3 |
| H6 | Jako widz chcę założyć konto, aby mieć wszystkie swoje bilety w jednym miejscu. | 1. Nie da się założyć drugiego konta na ten sam e-mail. 2. Po zalogowaniu w zakładce „Moje bilety” widzę bilety kupione na ten adres. | S | 3 |
| H7 | Jako widz chcę filtrować wydarzenia po kategorii i dacie, aby szybciej znaleźć to, co mnie interesuje. | 1. Wybór kategorii (koncert, teatr, kino, wystawa) i zakresu dat zawęża listę. 2. Gdy nic nie pasuje, widzę komunikat „Brak wydarzeń” i przycisk czyszczenia filtrów. | S | 3 |
| H8 | Jako bileter chcę zeskanować kod QR biletu, aby wpuścić tylko osoby z ważnym biletem. | 1. Ważny bilet daje zielony komunikat i zostaje oznaczony jako wykorzystany. 2. Ponowny skan tego samego biletu pokazuje „Bilet już użyty”. | S | 5 |
| H9 | Jako widz chcę zwrócić bilet do 48 godzin przed wydarzeniem, aby nie tracić pieniędzy, gdy nie mogę przyjść. | 1. Przycisk „Zwróć” jest aktywny tylko do 48 h przed startem. 2. Po zwrocie bilet jest nieważny, a liczba wolnych biletów rośnie. | C | 5 |
| H10 | Jako organizator chcę widzieć, ile biletów sprzedałem, aby wiedzieć, czy promować wydarzenie. | 1. Przy każdym wydarzeniu widzę liczbę sprzedanych i wolnych biletów. 2. Dane zgadzają się z liczbą zamówień w systemie. | C | 2 |
| H11 | Jako widz chcę wybrać konkretne miejsce na planie sali, aby siedzieć tam, gdzie chcę. | 1. Zajęte miejsca są wyszarzone i nie da się ich kliknąć. 2. Dwie osoby nie mogą kupić tego samego miejsca. | C | 13 |
| H12 | Jako widz chcę zapłacić kartą lub BLIKIEM, aby kupić bilet bez wychodzenia z aplikacji. | 1. Po udanej płatności zamówienie dostaje status „Opłacone”. 2. Po nieudanej płatności bilet wraca do puli. | W | 8 |

### Przegląd INVEST (robi zespół sąsiedni)

Recenzent wpisuje numer historyjki przy literze, której ona **nie spełnia**, i jedno zdanie, jak ją poprawić.

| Litera | Znaczenie | Uwagi recenzenta |
|---|---|---|
| I | Independent: niezależna od innych | |
| N | Negotiable: opisuje potrzebę, nie gotowe rozwiązanie | |
| V | Valuable: daje wartość użytkownikowi | |
| E | Estimable: da się ją oszacować | |
| S | Small: mieści się w jednym sprincie | |
| T | Testable: wiadomo, jak sprawdzić, że działa | |

## Krok 4. Estymacja (Planning Poker)

- Karty: 0, 1, 2, 3, 5, 8, 13, 20, ?, ☕
- Historyjka wzorcowa (2 punkty): H1, lista nadchodzących wydarzeń.
- Historyjki z największym rozrzutem głosów i co ustaliliście:
  - H11 (wybór miejsca na planie sali), głosy od 5 do 20. Każdy inaczej wyobrażał sobie plan sali. Zostaje 13 i trafia do Could have, a przed wzięciem do sprintu trzeba ją podzielić na „widz widzi plan sali” i „widz rezerwuje miejsce bez ryzyka, że ktoś kupi je w tym samym momencie”.
  - H4 (zakup biletów), głosy od 2 do 8. Część osób liczyła prawdziwą płatność online. Ustaliliśmy, że w sprincie 1 płatność jest symulowana, a prawdziwa to osobna historyjka H12. Po drugim głosowaniu 5 punktów.

## Krok 5. Plan sprintu 1

**Cel sprintu** (jedno zdanie, co użytkownik będzie mógł zrobić po sprincie): Widz może znaleźć wydarzenie dodane przez organizatora i kupić na nie bilet.

**Ile punktów bierzemy:** 11 (H1, H2, H3, H4)

| Historyjka | Zadania techniczne | Kto |
|---|---|---|
| H3 Organizator dodaje wydarzenie (3) | model danych wydarzenia, formularz dodawania, walidacja pól i daty | Jakub Kuśmierski |
| H1 Lista wydarzeń (2) | widok listy, sortowanie po dacie, ukrywanie minionych wydarzeń | Tomasz Nowak |
| H2 Szczegóły wydarzenia (1) | strona szczegółów, stan „Wyprzedane” i nieaktywny przycisk „Kup” | Zbigniew Czarnecki |
| H4 Zakup biletów (5) | model zamówienia, formularz zakupu z e-mailem, zmniejszanie puli biletów, limit 6 sztuk i blokada zakupu ponad pulę, symulowana płatność, test limitu biletów | Bartłomiej Pisarek (model zamówienia, limity), Jakub Kierklo (formularz zakupu, symulowana płatność, test) |

**Tablica:** link do GitHub Projects (albo zdjęcie tablicy papierowej): …

Kolumny: `Backlog` → `Do zrobienia` → `W toku` → `Przegląd` → `Zrobione`

**Definition of Done** (z karty zespołu, poprawiona):
1. Kod działa i spełnia kryteria akceptacji historyjki.
2. Testy jednostkowe przechodzą, a historyjka ma co najmniej jeden test do swoich kryteriów.
3. Kod przejrzała i zatwierdziła w pull requeście inna osoba z zespołu.
4. README opisuje, jak uruchomić nową funkcję, a w kodzie są komentarze tam, gdzie logika nie jest oczywista.
5. Zadanie jest w kolumnie „Zrobione”, a Product Owner zaakceptował historyjkę.
