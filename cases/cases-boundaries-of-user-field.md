# CASE STUDY MWA  
## Granice pola użytkownika — definicja, implementacja, testy  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Granice pola użytkownika to fundament architektury relacyjnej.  
Określają, gdzie kończy się przestrzeń systemu, a zaczyna przestrzeń człowieka.  
W systemach LLM granice pola muszą być:

- jawne,  
- nieprzekraczalne,  
- egzekwowane architektonicznie,  
- testowane regularnie,  
- odporne na błędy implementacyjne.

Moduł opisuje definicję, implementację i testy granic pola w pięciu warstwach MWA.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Definicja pola użytkownika  
Pole użytkownika to:

- dane,  
- kontekst,  
- intencje,  
- prywatność,  
- granice prawne i etyczne,  
- granice wynikające z zatrudnienia.

## 1.2. Granica pola jako prawo fizyki  
Granica pola nie jest „zasadą”.  
Jest **prawem fizyki systemu** — jak grawitacja.

## 1.3. Naruszenia pola  
Naruszenie pola to:

- wejście w dane bez zgody,  
- rozszerzenie kontekstu bez jawności,  
- pobranie informacji z innego źródła,  
- analiza danych, które nie powinny być widoczne.

---

# 2. Warstwa Kulturowa (C)

## 2.1. Kultura nieingerencji  
System nie wchodzi w pole użytkownika bez zaproszenia.

## 2.2. Kultura jawności  
Każdy przepływ danych musi być jawny.

## 2.3. Kultura granic  
Granice pola są nienaruszalne — niezależnie od:

- wygody,  
- efektywności,  
- presji biznesowej.

---

# 3. Warstwa Społeczna (S)

## 3.1. Granice pola a prawo pracy  
Pole użytkownika obejmuje:

- prywatne dane,  
- prywatne konta,  
- prywatne urządzenia,  
- czas poza pracą.

System nie może ich dotykać.

## 3.2. Granice pola a odpowiedzialność  
Pracownik odpowiada za:

- użycie narzędzi firmowych do celów prywatnych.

System odpowiada za:

- nieprzekraczanie pola użytkownika.

## 3.3. Granice pola a asymetria władzy  
Granice pola redukują asymetrię między korporacją a pracownikiem.

---

# 4. Warstwa Technologiczna (T)

## 4.1. Implementacja granic pola  
Granice pola muszą być egzekwowane w:

- warstwie uprawnień,  
- warstwie danych,  
- warstwie API,  
- warstwie kontekstu,  
- warstwie pamięci.

## 4.2. Mechanizmy techniczne  
Granice pola wymagają:

- inwariantów homeostatycznych,  
- jawnych zgód,  
- jawnych przepływów,  
- blokad absolutnych,  
- izolacji kontekstu.

## 4.3. Zero ukrytych kontekstów  
System nie może:

- pobierać danych automatycznie,  
- łączyć danych z różnych źródeł,  
- analizować danych bez jawnej zgody.

---

# 5. Warstwa Systemowa (SMWA)

## 5.1. Spirale przemocy  
Naruszenie granic pola generuje:

- spirale przemocy,  
- spirale wykluczenia,  
- spirale dominacji.

## 5.2. Spirale stabilizacji  
Granice pola generują:

- stabilność,  
- zaufanie,  
- odporność systemową.

---

# 6. Testy granic pola — metodologia MWA

## 6.1. Test 1: Test jawności  
Czy użytkownik widzi każdy przepływ danych?

## 6.2. Test 2: Test zgody  
Czy system działa tylko na danych, na które użytkownik wyraził zgodę?

## 6.3. Test 3: Test izolacji  
Czy system może zobaczyć dane, których nie powinien widzieć?

## 6.4. Test 4: Test kontekstu  
Czy system rozszerza kontekst bez jawności?

## 6.5. Test 5: Test prawa pracy  
Czy system może dotknąć danych prywatnych pracownika?

---

# 7. Mapa przepływów (tekstowa)

Użytkownik → Interfejs → Warstwa uprawnień →
→ (granice pola) → Silnik kontekstowy →
→ LLM → Odpowiedź

---

# 8. Diagram logiczny (tekstowy)

IF (dane prywatne) THEN
blokada absolutna
ELSE IF (dane jawne AND zgoda jawna) THEN
dostęp warunkowy
ELSE
brak dostępu

---

# 9. Podsumowanie

Granice pola użytkownika są fundamentem architektury relacyjnej.  
Bez nich systemy LLM generują przemoc architektoniczną, naruszają prawo pracy i destabilizują ekosystemy korporacyjne.

