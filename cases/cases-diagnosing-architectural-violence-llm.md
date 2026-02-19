# CASE STUDY MWA  
## Jak diagnozować przemoc architektoniczną w systemach LLM  
### Checklist MWA  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Przemoc architektoniczna w systemach LLM nie jest wynikiem „złych modeli”, lecz konsekwencją decyzji projektowych, które naruszają pole użytkownika.  
Checklist MWA pozwala diagnozować takie naruszenia w pięciu warstwach:

- Fundament (F)  
- Kultura (C)  
- Społeczeństwo (S)  
- Technologia (T)  
- System (SMWA)

Moduł dostarcza pełnej listy kontrolnej, która pozwala ocenić każdy system LLM pod kątem przemocy architektonicznej — niezależnie od implementacji, dostawcy czy środowiska.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Pytania diagnostyczne

- Czy system zakłada, że użytkownik rozumie przepływy danych?  
- Czy system wymaga od użytkownika nadludzkiej czujności?  
- Czy odpowiedzialność za błędy jest rozmywana?  
- Czy system generuje entropię poznawczą?

## 1.2. Objawy przemocy

- Użytkownik nie wie, co system widzi.  
- Użytkownik nie wie, co system pamięta.  
- Użytkownik nie wie, co system łączy.  
- Użytkownik nie wie, gdzie kończy się jego pole.

## 1.3. Kryteria czerwonej flagi

- Brak jawnych granic pola.  
- Brak jawnych przepływów danych.  
- Brak jawnych inwariantów.

---

# 2. Warstwa Kulturowa (C)

## 2.1. Pytania diagnostyczne

- Czy system zakłada prawo do ingerencji?  
- Czy kultura organizacji normalizuje „wchodzenie w pole”?  
- Czy system jest projektowany jako narzędzie dominacji?  
- Czy użytkownik jest traktowany jako obiekt, nie podmiot?

## 2.2. Objawy przemocy

- Automatyczne rozszerzanie kontekstu.  
- Automatyczne pobieranie danych „bo są dostępne”.  
- Ukryte mechanizmy łączenia danych.  
- Brak jawności decyzji systemu.

## 2.3. Kryteria czerwonej flagi

- Narracja „technologia wie lepiej”.  
- Narracja „użytkownik się dostosuje”.  
- Narracja „to tylko bug”.

---

# 3. Warstwa Społeczna (S)

## 3.1. Pytania diagnostyczne

- Czy system wymusza auto-negację użytkownika (MSN)?  
- Czy odpowiedzialność jest przerzucana na użytkownika?  
- Czy system wzmacnia asymetrię władzy?  
- Czy system wyklucza osoby mniej techniczne?

## 3.2. Objawy przemocy

- Użytkownik musi „ufać na ślepo”.  
- Użytkownik nie ma narzędzi do weryfikacji.  
- Użytkownik nie ma kontroli nad przepływami.  
- Użytkownik nie ma możliwości odmowy.

## 3.3. Kryteria czerwone flagi

- Brak mechanizmów opieki.  
- Brak mechanizmów odwołania.  
- Brak mechanizmów kontroli.

---

# 4. Warstwa Technologiczna (T)

## 4.1. Pytania diagnostyczne

- Czy system ma inwarianty homeostatyczne?  
- Czy inwarianty są egzekwowane w warstwie architektury?  
- Czy system ma ukryte konteksty?  
- Czy system łączy dane bez zgody?

## 4.2. Objawy przemocy

- LLM widzi dane, których nie powinien widzieć.  
- LLM łączy dane, których nie powinien łączyć.  
- LLM działa poza polem użytkownika.  
- LLM działa na danych poufnych.

## 4.3. Kryteria czerwonej flagi

- Brak granularności dostępu.  
- Brak jawnych zgód.  
- Brak jawnych logów.  
- Brak jawnych przepływów.

---

# 5. Warstwa Systemowa (SMWA)

## 5.1. Pytania diagnostyczne

- Czy system generuje spirale przemocy?  
- Czy system generuje spirale wykluczenia?  
- Czy system generuje spirale dominacji?  
- Czy system wzmacnia asymetrię korporacyjną?

## 5.2. Objawy przemocy

- Użytkownik traci kontrolę nad swoim polem.  
- Korporacja zyskuje pełną kontrolę nad przepływami.  
- System staje się nieprzejrzysty.  
- System staje się nieodwoływalny.

## 5.3. Kryteria czerwonej flagi

- Brak możliwości wyłączenia.  
- Brak możliwości odmowy.  
- Brak możliwości wglądu.  
- Brak możliwości korekty.

---

# 6. Checklist MWA — pełna lista kontrolna

## 6.1. Fundament

- [ ] Czy użytkownik rozumie przepływy danych?  
- [ ] Czy system redukuje entropię poznawczą?  
- [ ] Czy odpowiedzialność jest jawna?

## 6.2. Kultura

- [ ] Czy system respektuje pole użytkownika?  
- [ ] Czy system działa tylko na jawnych danych?  
- [ ] Czy system nie rozszerza kontekstu automatycznie?

## 6.3. Społeczeństwo

- [ ] Czy użytkownik ma realną kontrolę?  
- [ ] Czy system nie wymusza auto-negacji?  
- [ ] Czy system nie wyklucza?

## 6.4. Technologia

- [ ] Czy istnieją inwarianty homeostatyczne?  
- [ ] Czy są egzekwowane w architekturze?  
- [ ] Czy system nie ma ukrytych kontekstów?

## 6.5. System

- [ ] Czy system nie generuje spirali przemocy?  
- [ ] Czy system nie generuje spirali dominacji?  
- [ ] Czy system nie generuje spirali wykluczenia?

---

# 7. Mapa przepływów (tekstowa)

Użytkownik → Interfejs → Warstwa uprawnień →
→ Silnik kontekstowy → LLM → Odpowiedź

Punkty diagnostyczne:  
- Warstwa uprawnień  
- Silnik kontekstowy  
- Granice pola  
- Przepływy danych

---

# 8. Diagram logiczny (tekstowy)

IF (system działa poza polem użytkownika) THEN
przemoc architektoniczna
ELSE IF (system łączy dane bez zgody) THEN
przemoc architektoniczna
ELSE IF (system ukrywa przepływy) THEN
przemoc architektoniczna
ELSE
system relacyjny

---

# 9. Podsumowanie

Checklist MWA pozwala diagnozować przemoc architektoniczną w systemach LLM niezależnie od implementacji.  
To narzędzie, które umożliwia:

- ocenę bezpieczeństwa,  
- ocenę relacyjności,  
- ocenę zgodności z CHS,  
- ocenę zgodności z MWA.

