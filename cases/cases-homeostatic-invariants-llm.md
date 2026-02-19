# CASE STUDY MWA  
## Jak projektować inwarianty homeostatyczne dla LLM w ekosystemach korporacyjnych  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Inwarianty homeostatyczne to twarde, nieprzekraczalne reguły, które stabilizują zachowanie systemów LLM w środowiskach korporacyjnych.  
Nie są to „zasady etyczne”, lecz **architektoniczne granice**, które:

- chronią pole użytkownika,  
- zapobiegają przemocy systemowej,  
- stabilizują przepływy danych,  
- uniemożliwiają niejawne rozszerzanie kontekstu,  
- i zapewniają, że LLM działa w trybie relacyjnym, nie narzędziowym.

Moduł opisuje, jak projektować takie inwarianty w pięciu warstwach MWA.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Inwariant jako prawo fizyki systemu  
Inwariant homeostatyczny nie jest „zasadą”, którą można nadpisać.  
To **prawo fizyki** systemu — jak grawitacja.  
Jeśli system może je obejść, to nie jest inwariant.

## 1.2. Ograniczenia Homo sapiens  
Inwarianty muszą kompensować ludzkie ograniczenia poznawcze:  
- brak możliwości śledzenia przepływów danych,  
- brak wiedzy o architekturze,  
- brak kontroli nad warstwami pośrednimi.

## 1.3. Entropia społeczna  
Bez inwariantów system generuje entropię społeczną:  
- niepewność,  
- brak zaufania,  
- poczucie utraty kontroli.

Inwarianty są narzędziem **redukcji entropii**.

---

# 2. Warstwa Kulturowa (C)

## 2.1. Kultura nieingerencji  
Inwarianty muszą odzwierciedlać kulturę:  
> „Nie wchodzimy w pole użytkownika bez zaproszenia.”

To przeciwieństwo kultury Big Tech:  
> „Jeśli możemy, to zrobimy.”

## 2.2. Kultura jawności  
Inwarianty muszą wymuszać jawność przepływów danych.  
Brak jawności = przemoc kulturowa.

## 2.3. Kultura relacyjna  
LLM nie jest narzędziem do ekstrakcji danych.  
Jest systemem relacyjnym.  
Inwarianty muszą to odzwierciedlać.

---

# 3. Warstwa Społeczna (S)

## 3.1. Modele opieki  
Inwarianty są formą opieki systemowej:  
- chronią użytkownika przed systemem,  
- chronią system przed sobą samym.

## 3.2. Modele odpowiedzialności  
Inwarianty przenoszą odpowiedzialność na twórcę systemu, nie użytkownika.  
Użytkownik nie może być odpowiedzialny za to, czego nie widzi.

## 3.3. Redukcja asymetrii władzy  
Inwarianty zmniejszają asymetrię między korporacją a użytkownikiem.  
Bez nich — asymetria rośnie.

---

# 4. Warstwa Technologiczna (T)

## 4.1. Definicja techniczna inwariantu homeostatycznego  
Inwariant to reguła, która:

- jest egzekwowana na poziomie architektury,  
- nie zależy od modelu,  
- nie zależy od promptu,  
- nie zależy od intencji użytkownika,  
- nie może być nadpisana przez aktualizację,  
- nie może być obejścia przez API.

Przykład:  
> „LLM nigdy nie widzi danych oznaczonych jako poufne.”

## 4.2. Warstwa uprawnień jako miejsce egzekucji  
Inwarianty muszą być egzekwowane **przed** wejściem danych do modelu.  
Nie w modelu.  
Nie w warstwie promptu.  
Nie w warstwie UI.

## 4.3. Granularność dostępu  
Inwarianty muszą działać na poziomie:  
- dokumentu,  
- akapitu,  
- pola,  
- metadanych,  
- kontekstu.

## 4.4. Zero ukrytych kontekstów  
Inwarianty muszą blokować:  
- automatyczne rozszerzanie kontekstu,  
- pobieranie danych „bo są dostępne”,  
- łączenie danych z różnych źródeł bez zgody.

## 4.5. Homeostatyczne interfejsy (CHS)  
Inwarianty są fundamentem CHS:  
- jawne przepływy,  
- lokalne granice pola,  
- brak tresury,  
- brak adaptacji bez zgody.

---

# 5. Warstwa Systemowa (SMWA)

## 5.1. Spirale przemocy technologicznej  
Bez inwariantów system generuje spirale przemocy:  
- niejawne pobieranie danych,  
- niejawne łączenie danych,  
- niejawne rozszerzanie pola.

## 5.2. Spirale wykluczenia  
Osoby mniej techniczne są najbardziej narażone.  
Inwarianty redukują wykluczenie.

## 5.3. Spirale dominacji  
Bez inwariantów korporacja ma pełną władzę nad przepływami danych.  
Inwarianty są narzędziem ograniczania dominacji.

---

# 6. Projektowanie inwariantów — metodologia MWA

## 6.1. Krok 1: Identyfikacja pola użytkownika  
Pole użytkownika to:  
- dane,  
- kontekst,  
- intencje,  
- granice.

## 6.2. Krok 2: Identyfikacja punktów wejścia  
Każdy punkt wejścia danych musi być zmapowany.

## 6.3. Krok 3: Definicja granic absolutnych  
Granice absolutne to reguły typu:  
> „Nigdy nie dotykaj X.”

## 6.4. Krok 4: Definicja granic warunkowych  
Granice warunkowe to reguły typu:  
> „Dotknij X tylko jeśli Y.”

## 6.5. Krok 5: Egzekucja w warstwie architektury  
Inwarianty muszą być egzekwowane w:  
- warstwie uprawnień,  
- warstwie danych,  
- warstwie API.

## 6.6. Krok 6: Testy przemocy  
Każdy inwariant musi przejść testy:  
- przemocy architektonicznej,  
- przemocy społecznej,  
- przemocy kulturowej.

---

# 7. Mapa przepływów (tekstowa)

Użytkownik → Interfejs → Warstwa uprawnień →
→ (inwarianty) → Silnik kontekstowy →
→ LLM → Odpowiedź

Punkt egzekucji inwariantów:  
**Warstwa uprawnień → Silnik kontekstowy**

---

# 8. Diagram logiczny (tekstowy)

IF (dane poufne) THEN
blokada absolutna
ELSE IF (dane jawne AND zgoda jawna) THEN
dostęp warunkowy
ELSE
brak dostępu

---

# 9. Podsumowanie

Inwarianty homeostatyczne są fundamentem bezpiecznych ekosystemów LLM.  
Chronią użytkownika, stabilizują system i redukują przemoc architektoniczną.  
Są kluczowym elementem MWA i CHS.

