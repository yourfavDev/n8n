# Raport de Analiză a Documentului

**Data:** 4 Februarie 2024
**Tip Document:** Examen (Contabilitate Financiară)

## 1. Rezumat Executiv
Documentul reprezintă un set de subiecte de examen pentru disciplina **Contabilitate Financiară**, conform reglementărilor europene (OMFP 1802/2014). Acesta conține două variante de examen (NR 1 și NR 2) și baremul de corectare aferent. Subiectele acoperă teme fundamentale precum: gestiunea stocurilor la preț de vânzare cu amănuntul, operațiuni în valută și creanțe incerte, imobilizări corporale (achiziție, amortizare și reevaluare) și operațiuni de finanțare (credite bancare și acțiuni proprii).

---

## 2. Defalcare Conținut și Soluții (Varianta NR 1)

Vom rezolva în detaliu **Varianta NR 1**, deoarece structura este identică pentru ambele variante, diferind doar valorile numerice.

### Subiectul 1: Gestiunea Stocurilor (Retail)
**Cerință:** Înregistrarea achiziției, plății, vânzării și determinarea valorii stocului final în bilanț la 31.12.N.

**Rezolvare și Explicații:**

*   **a) Achiziția de mărfuri (12.12.N):**
    *   Preț cumpărare net: $220.000 - 20.000 (rabat) = 200.000 \text{ lei}$
    *   TVA deductibilă (19%): $200.000 \times 19\% = 38.000 \text{ lei}$
    *   Adaos comercial (30%): $200.000 \times 30\% = 60.000 \text{ lei}$
    *   TVA neexigibilă: $(200.000 + 60.000) \times 19\% = 49.400 \text{ lei}$
    *   Valoare totală în 371: $200.000 + 60.000 + 49.400 = 309.400 \text{ lei}$

    **Articol contabil:**
    ```
    %           = 401        238.000 (Cost + TVA deductibila)
    371                      200.000
    4426                      38.000
    
    371         = %           109.400
                  378          60.000
                  4428         49.400
    ```

*   **b) Plata furnizorului (17.12.N):**
    `401 = 5121 238.000 lei`

*   **c) Vânzarea și descărcarea din gestiune (23.12.N):**
    *   Vânzare: `5311 = % (707: 325.000, 4427: 61.750) Total: 386.750 lei`
    *   Descărcarea (Calcul coeficient K):
        $K = \frac{\text{Sold inițial } 378 + \text{Rulaj creditor } 378}{(\text{Sold inițial } 371 + \text{Rulaj debitor } 371) - (\text{Sold inițial } 4428 + \text{Rulaj creditor } 4428)}$
        $K = \frac{90.000 + 60.000}{(464.100 + 309.400) - (74.100 + 49.400)} = \frac{150.000}{650.000} \approx 0,230769$
    *   Adaos aferent vânzării: $325.000 \times K = 75.000 \text{ lei}$
    *   TVA neexigibilă aferentă: $61.750 \text{ lei}$

    **Articol descărcare:**
    ```
    607         = 371        250.000 (386.750 - 75.000 - 61.750)
    378         = 371         75.000
    4428        = 371         61.750
    ```

*   **d) Valoarea în bilanț:**
    Stocul se prezintă la cost de achiziție.
    $\text{Stoc Final } 371 = 464.100 + 309.400 - 386.750 = 386.750 \text{ lei}$
    $\text{Valoare bilanț} = \text{Sold } 371 - \text{Sold } 378 - \text{Sold } 4428 = 250.000 \text{ lei}$

---

### Subiectul 2: Valută și Creanțe
**Cerință:** Înregistrarea operațiunilor de avans, vânzare, diferențe de curs și depreciere.

**Rezolvare și Explicații (Selecție):**
*   **e) Plata datoriei externe (17.12.N):**
    *   Datorie veche: $5.000 \text{ EUR} \times 4,90 = 24.500 \text{ lei}$
    *   Plata efectivă: $5.000 \text{ EUR} \times 5,00 = 25.000 \text{ lei}$
    *   Diferență nefavorabilă: $500 \text{ lei}$
    `% (401: 24.500, 665: 500) = 5124 25.000 lei`
*   **f) Client incert:** `4118 = 4111 150.000 lei`
*   **g) Ajustare depreciere:** `6814 = 491 100.000 lei`
*   **h) Reevaluare datorie (31.12):** Rest $15.000 \text{ EUR}$. Curs nou $4,80$ vs $4,90$. Câștig: $15.000 \times 0,10 = 1.500 \text{ lei}$.
    `401 = 765 1.500 lei`

---

### Subiectul 3: Imobilizări Corporale
**Cerință:** Achiziție, montaj, amortizare și reevaluare.

**Explicație pas cu pas:**
1.  **Cost Intrare:** Achiziție netă ($400.000$) + Montaj ($30.000$) = $430.000 \text{ lei}$.
2.  **Amortizare Anul N:** Punere în funcțiune 17.06.N. Începe amortizarea în iulie.
    $\text{Amortizare lunară} = 430.000 / (5 \text{ ani} \times 12 \text{ luni}) = 7.166,67 \text{ lei/lună}$.
    $\text{Amortizare N (6 luni)} = 43.000 \text{ lei}$.
3.  **Reevaluare (31.12.N):**
    *   $\text{Valoare Contabilă Netă (VCN)} = 430.000 - 43.000 = 387.000 \text{ lei}$.
    *   $\text{Valoare Justă} = 420.000 \text{ lei}$.
    *   $\text{Surplus Reevaluare} = 420.000 - 387.000 = 33.000 \text{ lei}$.
    *   **Articol contabil (anulare amortizare):** `2813 = 2131 43.000 lei`.
    *   **Articol contabil (creștere valoare):** `2131 = 105 33.000 lei`.

---

### Subiectul 4: Finanțare
**Cerință:** Credit bancar și acțiuni proprii.

**Rezolvare (Selecție):**
*   **a) Credit:** `5121 = 1621 2.500.000 lei`.
*   **b) Dobândă (01.05-31.12):** $2.500.000 \times 8\% \times 8/12 = 133.333,33 \text{ lei}$.
    `666 = 1682`.
*   **f) Răscumpărare acțiuni:** $20.000 \times 120 = 2.400.000 \text{ lei}$.
    `109 = 5121`.
*   **g) Anulare acțiuni:** Valoare nominală $2.000.000$, pierdere $400.000$ (din rezerve/rezultat reportat).
    `% (1012: 2.000.000, 149: 400.000) = 109 2.400.000`.

---

## 3. Note și Observații
*   **Precizie Calcul:** La Subiectul 1, utilizarea coeficientului K cu mai multe zecimale este esențială pentru a evita erori de rotunjire semnificative în bilanț.
*   **Reglementări:** Documentul respectă OMFP 1802/2014, în special în ceea ce privește tratamentul reducerilor comerciale (rabatul reduce costul de achiziție dacă apare pe factura inițială).
*   **Reevaluare:** Procedeul utilizat în Subiectul 3 este cel al anulării amortizării cumulate ("net basis"), una din cele două metode permise de standarde.