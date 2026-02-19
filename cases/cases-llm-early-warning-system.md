# CASE STUDY MWA  
## LLM jako system wczesnego ostrzegania — predykcja ryzyk pracowniczych i anomalii organizacyjnych  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Systemy LLM mogą pełnić funkcję **systemu wczesnego ostrzegania (EWS)**, wykrywając:

- wczesne sygnały nadużyć pracowniczych,  
- anomalie organizacyjne,  
- ryzyka kadrowe,  
- naruszenia regulaminu pracy,  
- wzorce zachowań prowadzące do strat finansowych,  
- sygnały korupcyjne i niegospodarność.

Moduł opisuje, jak LLM — działając w architekturze MWA — może przewidywać ryzyka zanim staną się incydentem, chroniąc **pole pracodawcy** i jednocześnie nie naruszając **pola pracownika**.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Definicja systemu wczesnego ostrzegania (EWS)

EWS to system, który:

- wykrywa anomalie,  
- identyfikuje wzorce ryzyka,  
- przewiduje nadużycia,  
- generuje alerty przed wystąpieniem szkody.

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
LLM musi działać **na styku pól**, ale nie może naruszać żadnego z nich.

---

# 2. Warstwa Kulturowa (C)

## 2.1. Kultura prewencji  
EWS działa najlepiej w kulturze:

- jawności,  
- lojalności,  
- odpowiedzialności,  
- braku tolerancji dla nadużyć.

## 2.2. Kultura ochrony zasobów  
Pracodawca ma obowiązek:

- chronić infrastrukturę,  
- zapobiegać stratom,  
- reagować na sygnały ostrzegawcze.

## 2.3. Kultura ochrony pracownika  
LLM nie może:

- analizować danych prywatnych,  
- działać poza godzinami pracy,  
- dotykać kont prywatnych.

---

# 3. Warstwa Społeczna (S)

## 3.1. Polska — sygnały ostrzegawcze (2024–2025)

- **36% firm** padło ofiarą nadużyć.  
- Zakupy i księgowość: **29%** przypadków.  
- Korupcja: **16%** firm.  
- Tylko **5,7%** firm prowadzi bieżące kontrole.  
- W spółkach Skarbu Państwa (2016–2023) trwają kontrole nadużyć finansowych.

## 3.2. USA — sygnały ostrzegawcze (2024–2025)

- **32%** pracowników doświadczyło nadużyć (bullying).  
- Firmy tracą **5% przychodów** rocznie na oszustwach pracowniczych.  
- DOJ: **18% wzrost** spraw korporacyjnych.  
- Zgłoszenia nadużyć: **+50%** r/r.  
- Insider fraud: **60%** sprawców to pracownicy.  
- Straty z oszustw zatrudnieniowych: **500 mln USD**.  
- EEOC: **+9,2%** spraw o dyskryminację.  
- 72% pracowników wie o nękaniu.  
- 50% widziało nadużycia podczas pracy zdalnej.

## 3.3. Wspólny mianownik: czyn pracownika  
Niezależnie od kraju:

> **to pracownik narusza pole pracodawcy.**

EWS ma wykrywać te naruszenia zanim staną się stratą.

---

# 4. Warstwa Technologiczna (T)

## 4.1. Jak LLM wykrywa sygnały ostrzegawcze

### 1. Analiza wzorców zachowań  
- nagłe zmiany aktywności,  
- nietypowe godziny pracy,  
- wzrost liczby błędów,  
- wzrost liczby incydentów.

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

### 4. Wykrywanie ryzyk kadrowych  
- konflikty,  
- mobbing,  
- bullying,  
- dyskryminacja,  
- spadek morale.

### 5. Wykrywanie ryzyk finansowych  
- niegospodarność,  
- korupcja,  
- manipulacje księgowe.

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

## 5.1. Spirale ryzyka  
Bez EWS:

- nadużycia rosną,  
- koszty rosną,  
- morale spada,  
- konflikty eskalują.

## 5.2. Spirale stabilizacji  
Z EWS:

- ryzyka są wykrywane wcześnie,  
- koszty są ograniczane,  
- bezpieczeństwo rośnie,  
- organizacja staje się odporna.

## 5.3. Spirale odpowiedzialności  
EWS wymusza:

- odpowiedzialność pracownika,  
- odpowiedzialność pracodawcy,  
- odpowiedzialność systemu.

---

# 6. Testy EWS — metodologia MWA

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

Pole pracodawcy ←→ LLM (EWS) ←→ Pole pracownika
↑                     ↑
|                     |
wykrywanie           ochrona prywatności

---

# 8. Diagram logiczny (tekstowy)

IF (anomalia) THEN
alert + eskalacja
ELSE IF (dane prywatne pracownika) THEN
blokada absolutna
ELSE
działanie służbowe

---

# 9. Mapa ryzyk globalnych — dane naukowe i operacyjne

## Tabela porównawcza: CEJSH (USA – analiza naukowa) vs USA (2024–2025) vs Polska (2024–2025)

| Obszar | CEJSH – USA (analiza naukowa, skandale korporacyjne) | USA 2024–2025 (dane bieżące) | Polska 2024–2025 |
|--------|--------------------------------------------------------|-------------------------------|-------------------|
| **Charakter zjawiska** | Przestępczość korporacyjna jako zjawisko systemowe, zakorzenione strukturalnie | Nadużycia stanowiska, bullying, insider fraud, korupcja | Nadużycia finansowe, korupcja, niegospodarność, wycieki danych |
| **Główni sprawcy** | Menedżerowie wyższego szczebla (Enron, KPMG, Madoff) | Insiderzy: **60%** oszustw popełniają pracownicy | Pracownicy działów zakupów, księgowości, administracji |
| **Skala strat** | Miliardy USD (Enron, Madoff) | Firmy tracą **5% przychodów rocznie**; straty z fraudów zatrudnieniowych: **500 mln USD** | Brak pełnych danych; straty znaczne, szczególnie w sektorze publicznym |
| **Częstość występowania** | Skandale cykliczne, powtarzalne | **32%** pracowników doświadczyło nadużyć; zgłoszenia +50% r/r | **36%** firm padło ofiarą nadużyć w 24 miesiące |
| **Rodzaje nadużyć** | Fałszowanie sprawozdań, manipulacje księgowe, ukrywanie strat | Bullying, dyskryminacja, insider fraud, korupcja | Nadużycia zakupowe (29%), księgowe (29%), korupcja (16%) |
| **Mechanizmy umożliwiające** | Asymetria informacji, słaby nadzór, konflikt interesów | Słabe kontrole: **76%** przypadków | Kontrole okresowe, tylko **5,7%** bieżących kontroli |
| **Mechanizmy wykrywania** | Audyty po fakcie, sygnaliści | Sygnaliści: **43%** wykryć | Audyty, kontrole, sygnaliści (słabo chronieni) |
| **Ryzyka społeczne** | Utrata zaufania do instytucji, destabilizacja rynku | 72% pracowników świadomych nękania; 50% widziało nadużycia zdalnie | Wysokie ryzyko korupcji i niegospodarności w sektorze publicznym |
| **Wnioski systemowe** | Potrzeba automatycznej detekcji i prewencji | Rosnąca potrzeba EWS i compliance AI | Krytyczna potrzeba automatyzacji kontroli i audytu |
| **Wspólny mianownik** | **Czyn pracownika** jako źródło nadużycia | **Czyn pracownika** jako źródło nadużycia | **Czyn pracownika** jako źródło nadużycia |

---

# 10. Podsumowanie

LLM jako system wczesnego ostrzegania:

- chroni pracodawcę przed nadużyciami,  
- chroni pracownika przed nieuprawnioną ingerencją,  
- wykrywa ryzyka zanim staną się incydentem,  
- stabilizuje ekosystem pracy,  
- ogranicza straty finansowe,  
- wspiera zgodność z prawem pracy i bezpieczeństwem.

