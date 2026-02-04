# [Titlu: Raport de Analiză a Documentului]

**Dată:** 2024-05-22
**Tip Detectat:** Examen (Contabilitate Financiară)

## 1. Rezumat Executiv
Acest document reprezintă două variante de examen (NR 1 și NR 2) pentru disciplina „Contabilitate Financiară”, conform reglementărilor europene (OMFP 1802/2014). Examenul evaluează cunoștințele studenților în domenii cheie: contabilitatea stocurilor (metoda prețului cu amănuntul), operațiuni în valută și creanțe incerte, imobilizări corporale (achiziție, montaj, reevaluare) și operațiuni de finanțare (credite bancare și acțiuni proprii). Documentul include și baremul de corectare detaliat pe puncte pentru fiecare subpunct.

## 2. Analiza Conținutului și Soluții (Varianta NR 1)

În cele ce urmează sunt prezentate rezolvările pentru **Varianta NR 1**. Varianta NR 2 urmează aceeași logică contabilă, având doar valori numerice diferite.

---

### Subiectul 1: Contabilitatea Stocurilor (Mărfuri)

**Întrebare:** Înregistrarea achiziției, plății, vânzării și determinarea valorii stocului în bilanț pentru entitatea ALFA.

**Răspuns și Explicație:**

*   **a) Achiziția de mărfuri (12.12.N):**
    *   Preț de cumpărare net: $220.000 - 20.000 (rabat) = 200.000$ lei.
    *   Adaos comercial (30%): $200.000 \times 30\% = 60.000$ lei.
    *   TVA neexigibilă: $(200.000 + 60.000) \times 19\% = 49.400$ lei.
    *   Preț de vânzare cu amănuntul: $200.000 + 60.000 + 49.400 = 309.400$ lei.
    *   **Articol contabil:**
        ```
        %       = 401 Furnizori               238.000
        371 Mărfuri                           309.400
        4426 TVA deductibilă                   38.000 (19% din 200.000)
                = 378 Diferențe de preț        60.000
                = 4428 TVA neexigibilă         49.400
        ```

*   **b) Plata furnizorului (17.12.N):**
    ```
    401 Furnizori = 5121 Conturi la bănci în lei  238.000
    ```

*   **c) Vânzarea și scoaterea din evidență (23.12.N):**
    *   Vânzare:
        ```
        5311 Casa în lei = %                  386.750
                         707 Venituri mărfuri 325.000
                         4427 TVA colectată    61.750
        ```
    *   Scoaterea din evidență (Calcul Coeficient K):
        $K = \frac{Sold\_Ini\_378 + Rd\_378}{(Sold\_Ini\_371 - Sold\_Ini\_4428) + (Rd\_371 - Rd\_4428)} = \frac{90.000 + 60.000}{(464.100 - 74.100) + (309.400 - 49.400)} = \frac{150.000}{390.000 + 260.000} = 0,230769$
        Adaos aferent vânzării: $325.000 \times 0,230769 = 75.000$ lei.
        ```
        %                = 371 Mărfuri        386.750
        607 Chelt. mărfuri                    250.000 (325.000 - 75.000)
        378 Dif. de preț                       75.000
        4428 TVA neexigibilă                   61.750
        ```

*   **d) Valoarea în bilanț (31.12.N):**
    *   Sold Final 371: $464.100 + 309.400 - 386.750 = 386.750$ lei.
    *   Sold Final 378: $90.000 + 60.000 - 75.000 = 75.000$ lei.
    *   Sold Final 4428: $74.100 + 49.400 - 61.750 = 61.750$ lei.
    *   **Valoare bilanțieră (Cost de achiziție):** $386.750 - 75.000 - 61.750 = \mathbf{250.000}$ lei.

---

### Subiectul 2: Creanțe, Datorii în Valută și Ajustări

**Întrebare:** Înregistrarea tranzacțiilor cu clienții și furnizorii externi pentru entitatea BETA.

**Răspuns și Explicație (Selectiv):**

*   **a) Factură avans (05.12.N):** $23.800 / 1,19 = 20.000$ net.
    ```
    4111 Clienți = %                        23.800
                   419 Clienți-avansuri      20.000
                   4427 TVA colectată         3.800
    ```
*   **e) Plata datoriei externe (17.12.N):** 5.000 EUR. Curs istoric: 4,90. Curs plată: 5,00.
    *   Datorie stinsă: $5.000 \times 4,90 = 24.500$ lei.
    *   Plată bancă: $5.000 \times 5,00 = 25.000$ lei.
    ```
    %                      = 5124 Conturi bănci valută 25.000
    401 Furnizori (META)                               24.500
    665 Chelt. dif. curs                                  500
    ```
*   **f) Client incert GAMA (31.12.N):**
    ```
    4118 Clienți incerți = 4111 Clienți                150.000
    ```
*   **g) Ajustare depreciere (31.12.N):** Pierdere estimată de 100.000 lei (TVA inclus în creanță, dar ajustarea se face pe valoarea netă sau brută conform politicii; aici se cere pe 100.000).
    ```
    6814 Ch. expl. ajust. creanțe = 491 Ajust. depr. creanțe  100.000
    ```

---

### Subiectul 3: Imobilizări Corporale (Echipament)

**Răspuns și Explicație:**

*   **Cost achiziție:** $(410.000 - 10.000) + 30.000 = 430.000$ lei.
*   **Amortizare an N:** Punere în funcțiune 17.06.N. Amortizarea începe din iulie.
    $430.000 / 5 \text{ ani} \times (6 / 12) = 43.000$ lei.
*   **Reevaluare (31.12.N):**
    *   Valoare contabilă netă (VNC): $430.000 - 43.000 = 387.000$ lei.
    *   Valoare justă: $420.000$ lei.
    *   Plus din reevaluare: $420.000 - 387.000 = 33.000$ lei.
    *   Anulare amortizare: `2813 = 2131 43.000`
    *   Înregistrare creștere: `2131 = 105 33.000`
*   **Amortizare N+1:** $420.000 / 4,5 \text{ ani rămași} = 93.333$ lei.

---

### Subiectul 4: Finanțare (Credit și Acțiuni)

**Răspuns și Explicație:**

*   **a) Primire credit (01.05.N):** `5121 = 1621 2.500.000`.
*   **b) Dobândă an N (8 luni):** $2.500.000 \times 8\% \times (8/12) = 133.333$ lei.
    ```
    666 Chelt. dobânzi = 1682 Dobânzi aferente creditelor 133.333
    ```
*   **f) Răscumpărare acțiuni (28.10.N+1):** $20.000 \text{ acțiuni} \times 120 = 2.400.000$ lei.
    ```
    109 Acțiuni proprii = 5121 Conturi bănci 2.400.000
    ```
*   **g) Anulare acțiuni (01.11.N+1):** Valoare nominală $20.000 \times 100 = 2.000.000$.
    ```
    %                  = 109 Acțiuni proprii 2.400.000
    1012 Capital subscris vărsat             2.000.000
    149 Pierderi leg. de instrum. capital      400.000
    ```

## 3. Note și Observații
*   **Varianta NR 2:** Toate calculele pentru NR 2 urmează aceiași pași, dar cu datele de intrare modificate (ex: credit 1.800.000, dobândă 10%).
*   **Precizie:** La Subiectul 1, coeficientul K a fost rotunjit pentru exemplificare; în practică se recomandă utilizarea a cel puțin 4-6 zecimale.
*   **Reglementări:** Soluțiile respectă OMFP 1802/2014, inclusiv tratamentul fiscal al reevaluării și al creanțelor incerte.