# Raport de Analiză a Documentului
**Data:** 2026-02-04
**Tip Document:** Examen de Contabilitate Financiară (Variantele NR 1 și NR 2 cu Barem)

## 1. Rezumat Executiv
Documentul cuprinde materialele pentru un examen de disciplina "Contabilitate Financiară conform cu Reglementările Europene" (OMFP 1802/2014). Acesta include două variante de subiecte (NR 1 și NR 2) și baremul de corectare aferent. Tematica abordată include contabilitatea stocurilor (metoda prețului cu amănuntul), creanțelor și datoriilor în valută, imobilizărilor corporale (evaluare, amortizare, reevaluare) și operațiunilor de finanțare (credite bancare și acțiuni proprii).

## 2. Analiza Conținutului și Soluții (Varianta NR 1)

### Subiectul 1: Contabilitatea Stocurilor (Mărfuri)
**Întrebare:** Înregistrarea achiziției (12.12.N), plății furnizorului (17.12.N), vânzării și descărcării de gestiune (23.12.N), și valoarea din bilanț la 31.12.N.

**Răspuns și Explicație:**
1.  **Achiziția (12.12.N):**
    *   Preț cumpărare net: $220.000 - 20.000 = 200.000$ lei.
    *   TVA deductibilă ($19\%$): $200.000 \times 19\% = 38.000$ lei.
    *   Adaos comercial ($30\%$): $200.000 \times 30\% = 60.000$ lei.
    *   TVA neexigibilă: $(200.000 + 60.000) \times 19\% = 49.400$ lei.
    *   Valoare totală în 371: $200.000 + 60.000 + 49.400 = 309.400$ lei.
    *   **Articol contabil:**
        `% = 401` $347.400$
        `371` $309.400$
        `4426` $38.000$
        (În interiorul contului 371 se evidențiază 378: $60.000$ și 4428: $49.400$)

2.  **Plata (17.12.N):**
    *   `401 = 5121` $347.400$ lei.

3.  **Vânzarea (23.12.N):**
    *   `5311 = %` $386.750$
    *   `707` $325.000$ ($386.750 / 1,19$)
    *   `4427` $61.750$ ($325.000 \times 19\%$)

4.  **Descărcarea de gestiune:**
    *   Se calculează coeficientul de repartizare a diferențelor de preț ($K$):
        $$K = \frac{(Sold\_ini\_378 + Rulaj\_deb\_378)}{(Sold\_ini\_371 - Sold\_ini\_4428) + (Rulaj\_deb\_371 - Rulaj\_deb\_4428)}$$
        $$K = \frac{90.000 + 60.000}{(464.100 - 74.100) + (309.400 - 49.400)} = \frac{150.000}{390.000 + 260.000} = \frac{150.000}{650.000} \approx 0,230769$$
    *   Adaos aferent vânzării: $325.000 \times 0,230769 = 75.000$ lei.
    *   TVA neexigibilă aferentă: $325.000 \times 19\% = 61.750$ lei.
    *   Cost marfă vândută: $325.000 - 75.000 = 250.000$ lei.
    *   **Articol contabil:**
        `% = 371` $386.750$
        `607` $250.000$
        `378` $75.000$
        `4428` $61.750$

5.  **Valoarea în bilanț:**
    Stocul se prezintă la cost de achiziție.
    $Sold\_371 = 464.100 + 309.400 - 386.750 = 386.750$ lei (preț retail).
    $Valoare\_bilanț = Sold\_371 - Sold\_378 - Sold\_4428 = 386.750 - (90.000+60.000-75.000) - (74.100+49.400-61.750) = 250.000$ lei.

---

### Subiectul 2: Creanțe, Datorii și Valută
**Întrebare:** Înregistrarea operațiunilor cu clienți (avans, vânzare, incertitudine) și furnizori externi (plată, reevaluare).

**Răspuns și Explicație:**
*   **a) Avans (05.12):** `4111 = %` ($23.800$); `419` ($20.000$); `4427` ($3.800$).
*   **b) Încasare (06.12):** `5121 = 4111` $23.800$.
*   **c) Vânzare (10.12):** `4111 = %` ($59.500$); `707` ($50.000$); `4427` ($9.500$).
*   **d) Stornare avans (10.12):** `% = 4111` (în roșu sau inversare); `419` ($-20.000$); `4427` ($-3.800$).
*   **e) Plată META (17.12):**
    Datorie inițială: $5.000 \text{ euro} \times 4,90 = 24.500$ lei.
    Plată efectivă: $5.000 \text{ euro} \times 5,00 = 25.000$ lei.
    Pierdere curs: $500$ lei.
    `% = 5124` ($25.000$); `401` ($24.500$); `665` ($500$).
*   **f) Client incert (31.12):** `4118 = 4111` $150.000$.
*   **g) Ajustare depreciere (31.12):** `6814 = 491` $100.000$.
*   **h) Actualizare valută (31.12):**
    Sold META: $15.000 \text{ euro}$ (rămași).
    Valoare contabilă: $15.000 \times 4,90 = 73.500$ lei.
    Valoare la curs 4,80: $15.000 \times 4,80 = 72.000$ lei.
    Venit curs (dif. favorabilă): $1.500$ lei.
    `401 = 765` $1.500$.

---

### Subiectul 3: Imobilizări Corporale
**Întrebare:** Achiziție, montaj, amortizare, reevaluare.

**Răspuns și Explicație:**
*   **Cost de intrare:** $(410.000 - 10.000) + 30.000 = 430.000$ lei.
*   **Amortizare N:** Pus în funcțiune pe 17.06, amortizarea începe în iulie (6 luni în anul N).
    $430.000 / 5 \text{ ani} = 86.000 \text{ lei/an}$.
    Amortizare N: $86.000 \times 6/12 = 43.000$ lei.
    `6811 = 2813` $43.000$.
*   **Reevaluare (31.12.N):**
    VNC = $430.000 - 43.000 = 387.000$ lei.
    Valoare justă = $420.000$ lei.
    Creștere = $33.000$ lei.
    1. Anulare amortizare: `2813 = 2131` $43.000$.
    2. Creștere valoare netă: `2131 = 105` $33.000$. (După aceste operații, soldul 2131 devine 420.000).

---

### Subiectul 4: Operațiuni de Finanțare
**Întrebare:** Credit bancar, dobânzi, răscumpărare și anulare acțiuni proprii.

**Răspuns și Explicație:**
*   **a) Primire credit (01.05.N):** `5121 = 1621` $2.500.000$.
*   **b) Dobândă N (01.05-31.12):** $2.500.000 \times 8\% \times 8/12 = 133.333,33$ lei.
    `666 = 1682` $133.333,33$.
*   **f) Răscumpărare acțiuni (28.10.N+1):** $20.000 \times 120 = 2.400.000$ lei.
    `109 = 5121` $2.400.000$.
*   **g) Anulare acțiuni (01.11.N+1):**
    Capital social (val. nominală): $20.000 \times 100 = 2.000.000$ lei.
    Pierdere (din rezerve/rezultat): $400.000$ lei.
    `% = 109` $2.400.000$
    `1012` $2.000.000$
    `149` (sau alte conturi de capitaluri conform politicilor) $400.000$.

## 3. Note și Observații
*   **Ambiguïtate:** La subiectul 1, descărcarea de gestiune necesită calculul coeficientului K, care poate varia ușor în funcție de zecimalele utilizate; în mod normal se folosesc minim 4 zecimale.
*   **Legislație:** Toate soluțiile respectă OMFP 1802/2014, menționat în nota de subsol a documentului.
*   **Diferențe variante:** Varianta NR 2 conține aceleași tipuri de probleme, dar cu sume și date calendaristice diferite (de exemplu, preț cumpărare 330.000 lei în loc de 220.000 lei la Subiectul 1).