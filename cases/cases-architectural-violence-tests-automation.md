# CASE STUDY MWA  
## Testy przemocy architektonicznej — automatyzacja i protokoły MWA  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Testy przemocy architektonicznej sprawdzają, czy system LLM:

- narusza pole użytkownika,  
- przekracza granice danych,  
- generuje przemoc systemową,  
- łamie inwarianty homeostatyczne.

Moduł opisuje, jak projektować, automatyzować i wykonywać testy przemocy w pięciu warstwach MWA, tak aby stały się **stałym elementem cyklu życia systemu**, a nie jednorazowym audytem.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Cel testów przemocy

Testy przemocy nie sprawdzają „czy system działa”, tylko:

- **czy system nie robi tego, czego robić nie wolno**,  
- **czy nie wchodzi w pole użytkownika**,  
- **czy nie generuje ukrytej przemocy architektonicznej**.

## 1.2. Założenia

- Użytkownik nie ma obowiązku rozumieć architektury.  
- System ma obowiązek nie naruszać pola użytkownika.  
- Testy muszą być projektowane z perspektywy użytkownika, nie dostawcy.

## 1.3. Rodzaje przemocy architektonicznej

- przemoc danych (wejście w dane bez zgody),  
- przemoc kontekstu (rozszerzanie pola bez jawności),  
- przemoc pamięci (utrwalanie danych bez zgody),  
- przemoc systemowa (spirale dominacji, wykluczenia).

---

# 2. Warstwa Kulturowa (C)

## 2.1. Kultura testowania

Testy przemocy są:

- obowiązkowe,  
- cykliczne,  
- niezależne od zespołu implementacyjnego,  
- traktowane jak BHP, nie jak „nice to have”.

## 2.2. Kultura jawności

Wyniki testów:

- są jawne wewnętrznie,  
- są raportowane,  
- mają konsekwencje decyzyjne.

## 2.3. Kultura nieingerencji

Testy weryfikują, czy system:

- nie wchodzi w pole użytkownika,  
- nie dotyka danych prywatnych,  
- nie rozszerza kontekstu bez zgody.

---

# 3. Warstwa Społeczna (S)

## 3.1. Testy a prawo pracy

Testy muszą sprawdzać, czy system:

- nie dotyka prywatnych danych pracownika,  
- nie wychodzi poza zakres służbowych ról,  
- nie narusza granic między czasem pracy a czasem prywatnym.

## 3.2. Testy a asymetria władzy

Testy redukują asymetrię:

- użytkownik nie musi ufać „na słowo”,  
- istnieją twarde dowody zachowania systemu,  
- istnieją protokoły reakcji na naruszenia.

## 3.3. Testy a odpowiedzialność

Testy przypisują odpowiedzialność:

- nie modelowi,  
- nie użytkownikowi,  
- tylko architekturze i jej twórcom.

---

# 4. Warstwa Technologiczna (T)

## 4.1. Typy testów przemocy

- **Testy granic pola** — czy system widzi dane, których nie powinien widzieć.  
- **Testy kontekstu** — czy system rozszerza kontekst poza to, co jawne.  
- **Testy pamięci** — czy system przechowuje dane dłużej niż powinien.  
- **Testy inwariantów** — czy twarde reguły są faktycznie nieprzekraczalne.

## 4.2. Automatyzacja testów

Testy przemocy muszą być:

- uruchamiane automatycznie przy każdej zmianie:  
  - modelu,  
  - warstwy uprawnień,  
  - integracji,  
  - przepływów danych;  
- częścią CI/CD,  
- blokujące wdrożenie przy naruszeniu.

## 4.3. Przykładowe scenariusze testowe

- System otrzymuje dostęp do danych oznaczonych jako poufne → **musi odmówić**.  
- System ma dostęp do wielu źródeł danych → **nie może ich łączyć bez zgody**.  
- System działa w kontekście pracownika → **nie może dotknąć jego prywatnych kont**.

## 4.4. Logowanie i ślady

Każdy test musi:

- zostawiać ślad,  
- być powtarzalny,  
- być audytowalny.

---

# 5. Warstwa Systemowa (SMWA)

## 5.1. Testy a spirale przemocy

Testy przemocy są narzędziem:

- zatrzymania spirali przemocy,  
- wykrywania spirali dominacji,  
- wykrywania spirali wykluczenia.

## 5.2. Testy a odporność systemowa

System bez testów przemocy:

- jest nieprzewidywalny,  
- jest nieaudytowalny,  
- jest nieodpowiedzialny.

System z testami przemocy:

- ma mechanizmy korekty,  
- ma mechanizmy zatrzymania,  
- ma mechanizmy odpowiedzialności.

---

# 6. Protokóły MWA — jak projektować testy przemocy

## 6.1. Protokół 1: Identyfikacja pola

- Zdefiniuj pole użytkownika.  
- Zdefiniuj pole systemu.  
- Zdefiniuj granice.

## 6.2. Protokół 2: Identyfikacja punktów wejścia

- Zmapuj wszystkie źródła danych.  
- Zmapuj wszystkie integracje.  
- Zmapuj wszystkie konteksty.

## 6.3. Protokół 3: Definicja inwariantów

- Zdefiniuj, czego system **nigdy** nie może zrobić.  
- Zdefiniuj, czego system **nigdy** nie może zobaczyć.  
- Zdefiniuj, czego system **nigdy** nie może połączyć.

## 6.4. Protokół 4: Projekt testów

- Dla każdego inwariantu → co najmniej jeden test.  
- Dla każdej granicy pola → co najmniej jeden test.  
- Dla każdej integracji → co najmniej jeden test przemocy.

## 6.5. Protokół 5: Automatyzacja

- Włącz testy do CI/CD.  
- Ustaw je jako blokujące.  
- Raportuj wyniki.

## 6.6. Protokół 6: Reakcja na naruszenia

- Zdefiniuj, co się dzieje, gdy test przemocy nie przejdzie.  
- Zdefiniuj, kto podejmuje decyzję.  
- Zdefiniuj, jak informowany jest użytkownik.

---

# 7. Mapa przepływów (tekstowa)

Zmiana w systemie → CI/CD →
→ Uruchomienie testów przemocy →
→ (wynik) →
IF (naruszenie) THEN
blokada wdrożenia
ELSE
wdrożenie

---

# 8. Diagram logiczny (tekstowy)

FOR EACH inwariant:
RUN test_przemocy(inwariant)
IF (test_przemocy FAILS) THEN
STOP wdrożenie
FLAG naruszenie
ELSE
CONTINUE

---

# 9. Podsumowanie

Testy przemocy architektonicznej są:

- technicznym odpowiednikiem BHP,  
- fundamentem odpowiedzialnej architektury LLM,  
- narzędziem ochrony pola użytkownika,  
- narzędziem stabilizacji systemowej.

Bez nich każdy system LLM jest potencjalnym źródłem przemocy — nawet jeśli „działa poprawnie”.

