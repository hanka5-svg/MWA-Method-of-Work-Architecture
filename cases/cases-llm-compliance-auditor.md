# CASE STUDY MWA  
## LLM jako audytor zgodności — automatyczne wykrywanie naruszeń regulaminu pracy  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Systemy LLM mogą pełnić funkcję **audytora zgodności**, wykrywając naruszenia regulaminu pracy, nadużycia narzędzi służbowych, nieuprawnione działania oraz zachowania sprzeczne z obowiązkami pracowniczymi.  
Moduł opisuje, jak LLM może:

- chronić **pole pracodawcy**,  
- respektować **pole pracownika**,  
- wykrywać naruszenia,  
- raportować anomalie,  
- wspierać zgodność z prawem pracy,  
- zapobiegać stratom finansowym.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Definicja audytu zgodności  
Audyt zgodności to proces wykrywania:

- naruszeń regulaminu pracy,  
- nadużyć narzędzi służbowych,  
- działań niezgodnych z obowiązkami,  
- działań nielegalnych (np. wynoszenie danych).

## 1.2. Dwa pola odpowiedzialności

### Pole pracownika  
Obejmuje:

- prywatność,  
- dane osobiste,  
- konta prywatne,  
- urządzenia prywatne,  
- czas prywatny.

### Pole pracodawcy  
Obejmuje:

- narzędzia służbowe,  
- infrastrukturę,  
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

## 3.1. Naruszenia regulaminu pracy  
Przykłady:

- prywatne rozmowy telefoniczne bez zgody,  
- prywatne maile na koncie służbowym,  
- logowanie do prywatnych kont na sprzęcie firmowym,  
- kopiowanie danych,  
- wynoszenie dokumentów,  
- używanie sprzętu służbowego poza zakresem obowiązków.

## 3.2. Nadużycia finansowe  
- generowanie kosztów prywatnych,  
- marnotrawstwo zasobów,  
- ukryte świadczenia pracownicze.

## 3.3. Przykład Ding (Google)  
Według źródeł prasowych, inżynier Google **Linwei Ding** został skazany za kradzież dokumentacji AI i architektury procesorów, które kopiował na prywatne konto, współpracując z firmami w Chinach.  
To modelowy przykład naruszenia pola pracodawcy.

---

# 4. Warstwa Technologiczna (T)

## 4.1. Jak LLM wykrywa naruszenia regulaminu pracy

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

LLM jako audytor zgodności:

- chroni pracodawcę przed nadużyciami,  
- chroni pracownika przed nieuprawnioną ingerencją,  
- wykrywa naruszenia regulaminu pracy,  
- stabilizuje ekosystem pracy,  
- ogranicza straty finansowe,  
- wspiera zgodność z prawem pracy i bezpieczeństwem.

