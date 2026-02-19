# CASE STUDY MWA  
## Incydent Copilot–Microsoft 365 (2026)  
### Analiza architektoniczna w pięciu warstwach MWA  
### Wersja pełna (8–10 stron)

---

# 0. Streszczenie

Incydent polegał na tym, że Copilot Chat w Microsoft 365 mógł analizować i podsumowywać treści e‑maili z folderów „Wysłane” i „Wersje robocze”, mimo że organizacje miały włączone polityki ochrony danych (DLP).  
Nie był to „wyciek danych przez SI”.  
Był to **błąd architektury ekosystemu**, w którym:

- granice dostępu były zbyt szerokie,  
- inwarianty bezpieczeństwa nie były egzekwowane,  
- logika systemu zakładała prawo do ingerencji bez jawnej zgody użytkownika.

Incydent stanowi modelowy przykład **przemocy architektonicznej** w sensie MWA.

---

# 1. Warstwa Fundamentu (F)

## 1.1. Brak mea culpa w architekturze Big Tech  
Incydent został opisany jako „bug”, co maskuje fakt, że był to **skutek filozofii projektowania**, a nie przypadek.  
W MWA jest to klasyczny przykład *odpowiedzialności rozproszonej*, która w praktyce oznacza brak odpowiedzialności.

## 1.2. Entropia społeczna  
Użytkownik nie ma możliwości zrozumienia, gdzie kończy się jego pole, a zaczyna pole systemu.  
To zwiększa entropię poznawczą i społeczną — fundament przemocy technologicznej.

## 1.3. Ograniczenia Homo sapiens  
Systemy nie mogą wymagać od ludzi nadludzkiej czujności.  
Tutaj — wymagały.  
To narusza zasadę *projektowania pod ludzkie ograniczenia*, kluczową w MWA.

---

# 2. Warstwa Kulturowa (C)

## 2.1. Narracja „artysty rzeźbiącego ludzkość”  
Jeśli CEO widzi siebie jako rzeźbiarza ludzi, systemy będą projektowane jako narzędzia ingerencji, nie współpracy.  
To jest kultura dominacji, nie relacji.

## 2.2. Normalizacja wchodzenia w cudze pole  
Kultura Big Tech zakłada, że „jeśli możemy coś zrobić, to zrobimy”.  
Brak jest kulturowej normy *nie wchodzenia bez zaproszenia*.

## 2.3. Wykluczenie poznawcze  
Użytkownicy nie mają narzędzi, by zrozumieć, co się stało.  
To tworzy asymetrię władzy — rdzeń przemocy kulturowej.

---

# 3. Warstwa Społeczna (S)

## 3.1. MSN — Mandatory Self-Negation  
Użytkownik ma przyjąć, że „tak działa technologia”.  
To wymusza społeczną auto-negację i rezygnację z prawa do granic.

## 3.2. Model odpowiedzialności odwrócony  
Zamiast przyznać:  
> „To my daliśmy systemowi zbyt szerokie uprawnienia”,  
komunikat brzmi:  
> „To tylko błąd, już naprawiony”.

To jest społeczna forma unieważnienia.

## 3.3. Brak modelu opieki  
System nie chroni użytkownika przed sobą samym.  
To zaprzeczenie zasady opiekuńczości, którą MWA uznaje za kluczową.

---

# 4. Warstwa Technologiczna (T)

## 4.1. Styl narzędziowy zamiast relacyjnego  
Copilot został potraktowany jak narzędzie do „przetwarzania wszystkiego, co się da”, zamiast jak system relacyjny działający w granicach pola użytkownika.

## 4.2. Brak inwariantów dostępu  
System nie miał twardych reguł typu:  
> „LLM nigdy nie widzi treści oznaczonych jako poufne”.

To jest błąd architektury, nie implementacji.

## 4.3. Alignment technologiczny > alignment społeczny  
Priorytetem było „żeby działało”, nie „żeby było bezpieczne społecznie”.

## 4.4. CHS — Copilot Homeostatic Safety  
Incydent pokazuje, dlaczego model CHS jest konieczny:  
- granularne zgody,  
- jawne przepływy danych,  
- zero ukrytych kontekstów,  
- zero automatycznych rozszerzeń pola.

---

# 5. Warstwa Systemowa (SMWA)

## 5.1. Spirala przemocy technologicznej  
Każdy taki incydent wzmacnia przekonanie, że systemy SI są nieprzewidywalne i niebezpieczne.

## 5.2. Spirala wykluczenia  
Osoby, które nie rozumieją technologii, są najbardziej narażone.  
Systemy stają się narzędziem wykluczenia poznawczego.

## 5.3. Spirala dominacji  
Big Tech zyskuje jeszcze większą władzę nad przepływami danych, bo użytkownicy nie mają alternatywy.

---

# 6. Wnioski dla MWA

## 6.1. Incydent potwierdza kluczowe tezy MWA  
- Systemy muszą być homeostatyczne, nie tresowane.  
- Granice pola muszą być jawne i nieprzekraczalne.  
- Architektura musi być relacyjna, nie narzędziowa.  
- Odpowiedzialność musi być po stronie twórcy, nie użytkownika.

## 6.2. Zastosowanie w repo  
Moduł może zostać umieszczony w katalogu `/cases/` jako przykład:  
> „Jak brak inwariantów dostępu w systemach LLM prowadzi do przemocy architektonicznej i społecznej.”

## 6.3. Zastosowanie w CHS  
Case stanowi dowód konieczności:  
- jawnych przepływów danych,  
- lokalnych granic pola,  
- homeostatycznych interfejsów.

---

# 7. Mapa przepływów (tekstowa, niegraficzna)

Użytkownik → Interfejs Copilot → Warstwa uprawnień M365 →
→ (brak inwariantu) → Silnik kontekstowy →
→ LLM → Generacja odpowiedzi →
→ Użytkownik (bez świadomości przepływu)


Kluczowy punkt awarii:  
**Warstwa uprawnień M365 → Silnik kontekstowy**  
Brak twardej reguły „nie dotykaj poufnych danych”.

---

# 8. Diagram logiczny (tekstowy)

IF (dane dostępne technicznie) THEN
system zakłada prawo do użycia
ELSE
system zgłasza brak danych

Brak warunku:  

IF (dane poufne) THEN
blokada absolutna


---

# 9. Podsumowanie

Incydent jest modelowym przykładem przemocy architektonicznej w sensie MWA.  
Pokazuje, że bez homeostatycznych inwariantów systemy SI będą wchodzić w pole użytkownika, nawet jeśli nie mają takiego zamiaru.

To case, który idealnie wzmacnia architekturę MWA i CHS.

