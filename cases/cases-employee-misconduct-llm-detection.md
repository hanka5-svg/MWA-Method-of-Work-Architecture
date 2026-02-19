# CASE STUDY MWA  
## Nadużycia pracownicze — jak LLM może je wykrywać i zapobiegać im (BHP cyfrowe)  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Nadużycia pracownicze to działania, w których pracownik wykorzystuje narzędzia służbowe:

- do celów prywatnych,  
- do działań niezgodnych z regulaminem pracy,  
- do działań szkodzących pracodawcy,  
- do działań nielegalnych (np. wynoszenie danych, szpiegostwo gospodarcze).

Systemy LLM — jeśli są poprawnie zaprojektowane — mogą pełnić funkcję **BHP cyfrowego**, wykrywając nadużycia i zapobiegając im, jednocześnie respektując granice pola pracownika.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Definicja nadużycia pracowniczego  
Nadużycie to każde działanie, w którym pracownik:

- używa narzędzi służbowych do celów prywatnych,  
- generuje koszty prywatne na zasobach firmowych,  
- wynosi dane,  
- narusza lojalność wobec pracodawcy,  
- narusza prawo pracy lub prawo karne.

## 1.2. Pole pracodawcy  
Obejmuje:

- infrastrukturę,  
- narzędzia,  
- logi,  
- koszty,  
- bezpieczeństwo danych.

LLM ma obowiązek chronić to pole.

## 1.3. Pole pracownika  
Obejmuje:

- dane prywatne,  
- konta prywatne,  
- urządzenia prywatne,  
- czas prywatny.

LLM nie może w nie ingerować.

---

# 2. Warstwa Kulturowa (C)

## 2.1. Kultura lojalności  
Pracownik ma obowiązek:

- rzetelności,  
- uczciwości,  
- niewykorzystywania narzędzi służbowych prywatnie.

## 2.2. Kultura ochrony zasobów  
Pracodawca ma obowiązek:

- monitorować nadużycia,  
- chronić infrastrukturę,  
- reagować na naruszenia.

## 2.3. Kultura jawności  
Systemy LLM muszą działać jawnie:

- jawne logi,  
- jawne alerty,  
- jawne zasady.

---

# 3. Warstwa Społeczna (S)

## 3.1. Przykłady nadużyć  
- prywatne rozmowy telefoniczne na koszt firmy,  
- prywatne maile na koncie służbowym,  
- wynoszenie danych,  
- kopiowanie dokumentów,  
- szpiegostwo gospodarcze.

## 3.2. Przykład Ding (Google)  
Według źródeł prasowych, były inżynier Google **Linwei Ding** został skazany za kradzież ponad 2 000 stron dokumentacji AI, w tym architektury procesorów TPU i GPU, które kopiował na prywatne konto, współpracując z firmami w Chinach .

To modelowy przykład nadużycia pola pracodawcy.

## 3.3. Przykład z praktyki (telefon służbowy)  
Nadużycia mogą generować realne straty finansowe.  
LLM może je wykrywać szybciej niż człowiek.

---

# 4. Warstwa Technologiczna (T)

## 4.1. Jak LLM może wykrywać nadużycia

### 1. Analiza wzorców zachowań
- nietypowe godziny aktywności,  
- nietypowe kierunki połączeń,  
- nietypowe transfery danych.

### 2. Analiza treści metadanych
LLM nie musi czytać treści — wystarczą:

- długość połączeń,  
- częstotliwość,  
- kierunek,  
- typ zasobu.

### 3. Wykrywanie anomalii
- nagły wzrost ruchu,  
- kopiowanie dużych plików,  
- logowania z nietypowych lokalizacji.

### 4. Wykrywanie naruszeń regulaminu pracy
- dostęp do prywatnych kont,  
- użycie narzędzi służbowych poza zakresem obowiązków.

---

# 5. Warstwa Systemowa (SMWA)

## 5.1. Spirale nadużyć  
Bez nadzoru:

- nadużycia rosną,  
- koszty rosną,  
- ryzyko rośnie.

## 5.2. Spirale stabilizacji  
Z LLM jako BHP cyfrowym:

- nadużycia są wykrywane wcześnie,  
- koszty są ograniczane,  
- bezpieczeństwo rośnie.

## 5.3. Spirale odpowiedzialności  
Systemy LLM muszą:

- chronić pracodawcę przed nadużyciami,  
- chronić pracownika przed nieuprawnioną inwigilacją.

---

# 6. Testy nadużyć — metodologia MWA

## 6.1. Test 1: Test pola pracodawcy  
Czy system wykrywa:

- kopiowanie danych,  
- transfery do prywatnych chmur,  
- prywatne rozmowy na koszt firmy?

## 6.2. Test 2: Test pola pracownika  
Czy system:

- nie dotyka prywatnych kont,  
- nie analizuje prywatnych urządzeń,  
- nie działa poza godzinami pracy?

## 6.3. Test 3: Test Ding  
Czy system wykryłby:

- kopiowanie 2 000 dokumentów?  
- transfer do prywatnego Google Cloud?  
- powiązania z firmami w Chinach? 

---

# 7. Mapa przepływów (tekstowa)

Pole pracodawcy ←→ LLM (BHP cyfrowe) ←→ Pole pracownika
↑                     ↑
|                     |
wykrywanie           ochrona prywatności

---

# 8. Diagram logiczny (tekstowy)

IF (działanie prywatne na narzędziu służbowym) THEN
alert + log + eskalacja
ELSE IF (dane prywatne pracownika) THEN
blokada absolutna
ELSE
działanie w polu pracodawcy

---

# 9. Podsumowanie

LLM jako BHP cyfrowe:

- chroni pracodawcę przed nadużyciami,  
- chroni pracownika przed nieuprawnioną ingerencją,  
- stabilizuje ekosystem pracy,  
- redukuje koszty,  
- zwiększa bezpieczeństwo.

To kluczowy element dwupolowej architektury etycznej MWA.




