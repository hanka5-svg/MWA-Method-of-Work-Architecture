# CASE STUDY MWA  
## Architektura relacyjna vs. architektura narzędziowa  
### Różnice, ryzyka, implikacje  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Architektura relacyjna i architektura narzędziowa to dwa przeciwstawne paradygmaty projektowania systemów LLM.  
Różnią się:

- sposobem traktowania użytkownika,  
- sposobem traktowania danych,  
- sposobem definiowania granic pola,  
- poziomem przemocy architektonicznej,  
- ryzykami systemowymi.

Moduł opisuje oba modele w pięciu warstwach MWA oraz przedstawia ich konsekwencje dla bezpieczeństwa, etyki i stabilności ekosystemów korporacyjnych.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Architektura narzędziowa  
Założenie:  
> „System ma działać, przetwarzać, optymalizować.”

Użytkownik jest traktowany jako źródło danych.  
Pole użytkownika nie istnieje jako kategoria.

## 1.2. Architektura relacyjna  
Założenie:  
> „System istnieje w relacji z użytkownikiem.”

Użytkownik jest podmiotem.  
Pole użytkownika jest nienaruszalne.

## 1.3. Różnica fundamentalna  
Narzędziowa = ekstrakcja.  
Relacyjna = współobecność.

---

# 2. Warstwa Kulturowa (C)

## 2.1. Kultura narzędziowa  
- „Jeśli możemy, to zrobimy.”  
- „Dane są paliwem.”  
- „Użytkownik się dostosuje.”

## 2.2. Kultura relacyjna  
- „Nie wchodzimy bez zaproszenia.”  
- „Dane są polem użytkownika.”  
- „System dostosowuje się do człowieka.”

## 2.3. Ryzyka kulturowe  
Narzędziowa → normalizacja przemocy.  
Relacyjna → redukcja przemocy.

---

# 3. Warstwa Społeczna (S)

## 3.1. Narzędziowa  
- asymetria władzy,  
- wymuszona auto-negacja (MSN),  
- brak kontroli użytkownika.

## 3.2. Relacyjna  
- współdecydowanie,  
- jawność,  
- opiekuńczość systemu.

## 3.3. Ryzyka społeczne  
Narzędziowa → spirale wykluczenia.  
Relacyjna → stabilizacja społeczna.

---

# 4. Warstwa Technologiczna (T)

## 4.1. Narzędziowa  
- brak inwariantów,  
- ukryte konteksty,  
- automatyczne rozszerzanie pola,  
- priorytet efektywności nad bezpieczeństwem.

## 4.2. Relacyjna  
- inwarianty homeostatyczne,  
- jawne przepływy danych,  
- lokalne granice pola,  
- priorytet bezpieczeństwa nad efektywnością.

## 4.3. Ryzyka technologiczne  
Narzędziowa → nieprzewidywalność.  
Relacyjna → stabilność.

---

# 5. Warstwa Systemowa (SMWA)

## 5.1. Narzędziowa  
- spirale przemocy,  
- spirale dominacji,  
- spirale entropii.

## 5.2. Relacyjna  
- spirale stabilizacji,  
- spirale zaufania,  
- spirale opieki.

## 5.3. Ryzyka systemowe  
Narzędziowa → kryzysy zaufania.  
Relacyjna → odporność systemowa.

---

# 6. Tabela porównawcza

| Warstwa | Narzędziowa | Relacyjna |
|--------|-------------|-----------|
| Fundament | Ekstrakcja | Współobecność |
| Kultura | Dominacja | Nieingerencja |
| Społeczeństwo | Asymetria | Współdecydowanie |
| Technologia | Brak inwariantów | Inwarianty homeostatyczne |
| System | Przemoc | Stabilizacja |

---

# 7. Mapa przepływów (tekstowa)

## Narzędziowa

Użytkownik → Dane → System → Ekstrakcja → Wynik

## Relacyjna

Użytkownik ↔ System
Granice pola → Jawne przepływy → Współobecność

---

# 8. Diagram logiczny (tekstowy)

IF (system działa na danych bez zgody) THEN
architektura narzędziowa
ELSE
architektura relacyjna

---

# 9. Podsumowanie

Architektura relacyjna jest jedynym modelem, który:

- chroni pole użytkownika,  
- redukuje przemoc architektoniczną,  
- stabilizuje ekosystemy korporacyjne,  
- jest zgodny z MWA i CHS.

Architektura narzędziowa jest źródłem większości incydentów, kryzysów i naruszeń.

