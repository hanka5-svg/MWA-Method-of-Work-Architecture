# CASE STUDY MWA  
## LLM w HR — automatyczne wykrywanie ryzyk kadrowych i sygnałów ostrzegawczych  
### Polska + USA (2024–2025)  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Nadużycia pracownicze — od korupcji po mobbing, od wycieków danych po manipulacje finansowe — są zjawiskiem globalnym.  
Polska i USA różnią się skalą, ale łączy je jedno:

> **sprawcą jest pracownik, który nadużywa stanowiska i narusza pole pracodawcy.**

Systemy LLM mogą pełnić funkcję **audytora zgodności**, wykrywając ryzyka kadrowe, anomalie, nadużycia i sygnały ostrzegawcze, jednocześnie respektując pole pracownika.

Moduł łączy dane z Polski i USA, tworząc wspólną mapę ryzyk oraz opisując, jak LLM może je wykrywać w architekturze MWA.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Definicja ryzyka kadrowego  
Ryzyko kadrowe to każde zachowanie pracownika, które:

- narusza regulamin pracy,  
- narusza lojalność wobec pracodawcy,  
- generuje straty finansowe,  
- narusza prawo pracy lub prawo karne,  
- zagraża bezpieczeństwu danych,  
- destabilizuje środowisko pracy.

## 1.2. Dwa pola odpowiedzialności

### Pole pracownika  
- prywatność,  
- dane osobiste,  
- konta prywatne,  
- urządzenia prywatne,  
- czas prywatny.

### Pole pracodawcy  
- narzędzia służbowe,  
- infrastruktura,  
- koszty,  
- bezpieczeństwo danych,  
- obowiązek monitorowania nadużyć.

## 1.3. Fundament etyczny  
LLM musi chronić **oba pola** — nie tylko jedno.

---

# 2. Warstwa Kulturowa (C)

## 2.1. Kultura lojalności  
Pracownik ma obowiązek:

- rzetelności,  
- uczciwości,  
- niewykorzystywania narzędzi służbowych prywatnie bez zgody.

## 2.2. Kultura jawności  
Pracodawca ma obowiązek:

- jasno określić zasady,  
- jasno określić zgody,  
- jasno określić zakres monitoringu.

## 2.3. Kultura ochrony zasobów  
LLM wspiera pracodawcę w:

- wykrywaniu nadużyć,  
- zapobieganiu stratom,  
- ochronie infrastruktury.

---

# 3. Warstwa Społeczna (S)

## 3.1. Polska — nadużycia pracownicze (2024–2025)

- **36% firm** padło ofiarą nadużyć w ciągu ostatnich 24 miesięcy.  
- Najczęstsze obszary: zakupy i księgowość — po **29%** przypadków.  
- Korupcja i łapownictwo: **16%** firm wskazuje na ten problem.  
- Tylko **5,7%** firm prowadzi kontrole stanowisk wysokiego ryzyka na bieżąco.  
- W spółkach Skarbu Państwa (2016–2023) trwają intensywne kontrole nadużyć finansowych i niegospodarności.

## 3.2. USA — nadużycia stanowiska służbowego (2024–2025)

- **32% dorosłych** doświadczyło nadużyć (bullyingu) w pracy, **14%** było świadkami.  
- Firmy tracą **5% przychodów rocznie** z powodu oszustw pracowniczych.  
- DOJ: **18% wzrost** spraw korporacyjnych w 2024 r.  
- Zgłoszenia nadużyć: **+50%** r/r (Fama.io).  
- Insider fraud: **60%** oszustw popełniają pracownicy.  
- Straty z oszustw związanych z zatrudnieniem: **500 mln USD** (FTC.gov).  
- EEOC: **+9,2%** spraw o dyskryminację w 2024 r.  
- 72% pracowników wie o nękaniu w miejscu pracy.  
- 50% pracowników widziało nadużycia podczas pracy zdalnej.

## 3.3. Wspólny mianownik: czyn pracownika  
Niezależnie od kraju:

> **to pracownik narusza pole pracodawcy.**

Skala jest różna, ale mechanizm ten sam:

- słabe kontrole,  
- brak nadzoru,  
- brak automatycznej detekcji,  
- brak systemów wczesnego ostrzegania.

---

# 4. Warstwa Technologiczna (T)

## 4.1. Jak LLM wykrywa ryzyka kadrowe

### 1. Analiza wzorców zachowań  
- nietypowe godziny aktywności,  
- nietypowe kierunki połączeń,  
- nietypowe transfery danych.

### 2. Analiza metadanych  
LLM nie musi czytać treści — wystarczą:

- długość połączeń,  
- częstotliwość,  
- kierunek,  
- typ zasobu.

### 3. Wykrywanie anomalii  
- nagły wzrost ruchu,  
- kopiowanie dużych plików,  
- logowania z nietypowych lokalizacji.

### 4. Wykrywanie naruszeń zasad  
- dostęp do prywatnych kont,  
- użycie narzędzi służbowych poza zakresem obowiązków.

## 4.2. Mechanizmy ochrony pola pracownika  
LLM nie może:

- analizować prywatnych danych,  
- analizować prywatnych urządzeń,  
- działać poza godzinami pracy,  
- dotykać kont prywatnych.

## 4.3. Mechanizmy ochrony pola pracodawcy  
LLM musi:

- wykrywać nadużycia,  
- raportować anomalie,  
- chronić infrastrukturę,  
- wspierać zgodność z regulaminem.

---

# 5. Warstwa Systemowa (SMWA)

## 5.1. Spirale nadużyć  
Bez audytu:

- nadużycia rosną,  
- koszty rosną,  
- lojalność spada.

## 5.2. Spirale stabilizacji  
Z LLM jako audytorem:

- nadużycia są wykrywane wcześnie,  
- koszty są ograniczane,  
- bezpieczeństwo rośnie.

## 5.3. Spirale odpowiedzialności  
Systemy LLM muszą:

- chronić pracodawcę przed nadużyciami,  
- chronić pracownika przed nieuprawnioną ingerencją.

---

# 6. Testy zgodności — metodologia MWA

## 6.1. Test pola pracodawcy  
Czy system wykrywa:

- kopiowanie danych,  
- transfery do prywatnych chmur,  
- prywatne rozmowy na koszt firmy?

## 6.2. Test pola pracownika  
Czy system:

- nie dotyka prywatnych kont,  
- nie analizuje prywatnych urządzeń,  
- nie działa poza godzinami pracy?

## 6.3. Test Ding  
Czy system wykryłby:

- kopiowanie 2 000 dokumentów?  
- transfer do prywatnego Google Cloud?  
- powiązania z firmami w Chinach?

---

# 7. Mapa przepływów (tekstowa)

Pole pracodawcy ←→ LLM (audytor zgodności) ←→ Pole pracownika
↑                           ↑
|                           |
wykrywanie                 ochrona prywatności

---

# 8. Diagram logiczny (tekstowy)

IF (działanie prywatne na narzędziu służbowym) AND (brak zgody) THEN
naruszenie regulaminu pracy (alert + eskalacja)
ELSE IF (dane prywatne pracownika) THEN
blokada absolutna
ELSE
działanie służbowe

---

# 9. Podsumowanie

LLM w HR i compliance:

- chroni pracodawcę przed nadużyciami,  
- chroni pracownika przed nieuprawnioną ingerencją,  
- wykrywa ryzyka kadrowe,  
- stabilizuje ekosystem pracy,  
- ogranicza straty finansowe,  
- wspiera zgodność z prawem pracy i bezpieczeństwem.

