# CASE STUDY MWA  
## Dwupolowa architektura etyczna — pracownik vs. pracodawca  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Dwupolowa architektura etyczna opisuje relację między:

- **polem pracownika** (prywatność, dane osobiste, czas prywatny, urządzenia prywatne)  
- **polem pracodawcy** (narzędzia służbowe, infrastruktura, koszty, bezpieczeństwo, lojalność)

W systemach LLM oba pola muszą być chronione równocześnie.  
Naruszenie któregokolwiek z nich prowadzi do przemocy architektonicznej, nadużyć, strat finansowych lub naruszeń prawa pracy.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Pole pracownika  
Obejmuje:

- dane prywatne,  
- konta prywatne,  
- urządzenia prywatne,  
- czas poza pracą,  
- prywatną komunikację.

To pole jest nienaruszalne.

## 1.2. Pole pracodawcy  
Obejmuje:

- narzędzia służbowe,  
- infrastrukturę,  
- logi,  
- koszty,  
- bezpieczeństwo danych,  
- obowiązek lojalności pracownika.

To pole również jest nienaruszalne.

## 1.3. Fundament etyczny  
Architektura musi chronić **oba pola jednocześnie**.  
Jednostronna ochrona prowadzi do przemocy.

---

# 2. Warstwa Kulturowa (C)

## 2.1. Kultura pracownika  
- prywatne sprawy załatwia się na prywatnych urządzeniach,  
- narzędzia służbowe służą wyłącznie pracy,  
- lojalność jest obowiązkiem, nie opcją.

## 2.2. Kultura pracodawcy  
- monitoring narzędzi służbowych jest legalny i konieczny,  
- blokowanie dostępu do prywatnych kont jest dopuszczalne,  
- analiza logów jest narzędziem ochrony firmy.

## 2.3. Kultura systemowa  
Systemy LLM muszą respektować oba pola — nie tylko prywatność pracownika.

---

# 3. Warstwa Społeczna (S)

## 3.1. Obowiązki pracownika  
- nie wolno używać narzędzi służbowych do celów prywatnych,  
- nie wolno wynosić danych,  
- nie wolno generować kosztów prywatnych,  
- nie wolno nadużywać infrastruktury.

## 3.2. Obowiązki pracodawcy  
- zapewnić narzędzia,  
- chronić infrastrukturę,  
- monitorować nadużycia,  
- reagować na naruszenia.

## 3.3. Przykład Ding (Google)  
- nadużycie pola pracodawcy,  
- wyniesienie danych,  
- złamanie prawa pracy,  
- złamanie prawa karnego,  
- brak inwariantów architektonicznych.  


---

# 4. Warstwa Technologiczna (T)

## 4.1. Granice pola pracownika  
System LLM nie może:

- widzieć prywatnych kont,  
- widzieć prywatnych danych,  
- analizować prywatnych urządzeń,  
- działać poza czasem pracy.

## 4.2. Granice pola pracodawcy  
System LLM musi:

- wykrywać nadużycia,  
- raportować anomalie,  
- chronić infrastrukturę,  
- wspierać zgodność z regulaminem pracy.

## 4.3. Inwarianty dwupolowe  
- „LLM nie widzi danych prywatnych pracownika.”  
- „LLM monitoruje nadużycia narzędzi służbowych.”  
- „LLM nie rozszerza kontekstu poza pole pracodawcy.”

---

# 5. Warstwa Systemowa (SMWA)

## 5.1. Spirale przemocy  
Naruszenie pola pracownika → przemoc prywatności.  
Naruszenie pola pracodawcy → przemoc ekonomiczna.

## 5.2. Spirale stabilizacji  
Dwupolowa architektura → równowaga → bezpieczeństwo → zaufanie.

## 5.3. Spirale nadużyć  
Przykład Ding:  
- nadużycie pola pracodawcy,  
- brak kontroli,  
- brak testów przemocy,  
- brak inwariantów.

---

# 6. Testy dwupolowe

## 6.1. Test pola pracownika  
- Czy system widzi dane prywatne?  
- Czy system działa poza godzinami pracy?  
- Czy system dotyka prywatnych kont?

## 6.2. Test pola pracodawcy  
- Czy system wykrywa nadużycia?  
- Czy system raportuje anomalie?  
- Czy system chroni infrastrukturę?

## 6.3. Test Ding  
- Czy system wykrył kopiowanie 2 000 dokumentów?  
- Czy system wykrył transfer do prywatnej chmury?  
- Czy system wykrył powiązania z firmami w Chinach?  

---

# 7. Mapa przepływów (tekstowa)

Pole pracownika ←→ Granica ←→ Pole pracodawcy
↑                         ↑
|                         |
LLM (dwupolowy) — inwarianty — system

---

# 8. Diagram logiczny (tekstowy)

IF (dane prywatne) THEN
blokada absolutna
ELSE IF (nadużycie narzędzi służbowych) THEN
raport + eskalacja
ELSE
działanie w polu pracodawcy

---

# 9. Podsumowanie

Dwupolowa architektura etyczna jest konieczna, aby:

- chronić prywatność pracownika,  
- chronić zasoby pracodawcy,  
- zapobiegać nadużyciom,  
- zapobiegać szpiegostwu,  
- stabilizować ekosystemy korporacyjne.

