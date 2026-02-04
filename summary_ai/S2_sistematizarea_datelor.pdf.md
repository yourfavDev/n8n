Iată raportul detaliat bazat pe documentul furnizat, structurat ca o resursă educațională cu soluții și explicații.

# Raport de Analiză a Documentului
**Data:** 2026-02-04
**Tip Document:** Material Didactic / Temă de Seminar - Sistematizarea Datelor (Statistică)

## 1. Rezumat Executiv
Documentul prezintă concepte fundamentale de statistică descriptivă, concentrându-se pe **gruparea statistică** (după caracteristici calitative și cantitative). Include metodologia pas cu pas pentru crearea intervalelor de grupare (formula lui Sturges), utilizarea funcțiilor Excel (`COUNTIF`, `FREQUENCY`) și exemple rezolvate. Partea finală conține aplicații propuse pentru rezolvare și o serie de teste grilă pentru verificarea cunoștințelor.

---

## 2. Descompunere Conținut și Soluții

Mai jos sunt prezentate rezolvările pentru **Aplicațiile Propuse** (pagina 4-5) și **Testele Grilă** (paginile 5-7).

### APLICAȚII PROPUSE (Pagina 4)

#### Aplicația 1: Calculul centrelor de interval

**Cerință:** Pentru distribuțiile date, scrieți grupele sub formă de intervale și calculați centrele de interval.
*Notă: Centrul de interval ($x_i$) se calculează ca media aritmetică a limitelor intervalului: $x_i = \frac{Limita_{inf} + Limita_{sup}}{2}$. Pentru intervalele deschise ("Sub X", "Peste Y"), se asumă de regulă aceeași mărime a intervalului ($h$) ca a celorlalte grupe.*

**Tabel 1: Înălțimea (cm)**
Presupunem mărimea intervalului $h = 10$ cm (dedusă din intervalele 150-160, 160-170).

| Intervale (scrise formal) | Centre de interval ($x_i$) | Explicație Calcul |
| :--- | :---: | :--- |
| $[140, 150)$ (Sub 150) | **145** | $(140+150)/2$ (asumând $h=10$) |
| $[150, 160)$ | **155** | $(150+160)/2$ |
| $[160, 170)$ | **165** | $(160+170)/2$ |
| $[170, 180]$ (Peste 170) | **175** | $(170+180)/2$ (asumând $h=10$) |

**Tabel 2: Greutatea (kg)**
Presupunem mărimea intervalului $h = 10$ kg (dedusă din intervalele 50-60, etc.).

| Intervale (scrise formal) | Centre de interval ($x_i$) | Explicație Calcul |
| :--- | :---: | :--- |
| $[40, 50)$ (Sub 50) | **45** | $(40+50)/2$ (asumând $h=10$) |
| $[50, 60)$ | **55** | $(50+60)/2$ |
| $[60, 70)$ | **65** | $(60+70)/2$ |
| $[70, 80)$ | **75** | $(70+80)/2$ |
| $[80, 90]$ (Peste 80) | **85** | $(80+90)/2$ (asumând $h=10$) |

---

#### Aplicația 2: Completarea tabelului de frecvențe (Pagina 5)

**Date cunoscute:**
*   Grupa 1 [10-40]: Frecv. Relativă ($f_i\%$) = 6%, Frecv. Absolută ($n_i$) = 30.
    *   *Deducție:* Dacă 6% corespunde la 30 unități, atunci 1% = 5 unități. Totalul populației ($N$) = $30 / 0.06 = 500$.
*   Grupa 2 (40-70]: Frecv. Relativă ($f_i\%$) = 20%.
*   Grupa 3 (70-100]: Frecv. Relativă Cumulată Crescător ($F_i\%$) = 45%.
*   Grupa 4 (100-130]: Frecv. Relativă Cumulată Crescător ($F_i\%$) = 81%.

**Rezolvare pas cu pas:**
1.  **Total ($N$):** 500.
2.  **Grupa 2:** $f_2\% = 20\%$. $n_2 = 20\% \times 500 = 100$. Frecv. cumulate: $6\% + 20\% = 26\%$.
3.  **Grupa 3:** $F_3\% = 45\%$. Deci $f_3\% = 45\% - 26\% = 19\%$. $n_3 = 19\% \times 500 = 95$.
4.  **Grupa 4:** $F_4\% = 81\%$. Deci $f_4\% = 81\% - 45\% = 36\%$. $n_4 = 36\% \times 500 = 180$.
5.  **Grupa 5 (130-160]:** Restul până la 100%. $f_5\% = 100\% - 81\% = 19\%$. $n_5 = 19\% \times 500 = 95$.

**Tabel Completat:**

| Grupe | Centre de interval | Frecvențe relative (%) $n_i^*$ | Frecvențe relative cumulate crescător (%) | Frecvențe absolute $n_i$ | Frecv abs cum desc | Frecv abs cum crescător |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| [10-40] | 25 | 6 | 6 | 30 | 500 | 30 |
| (40-70] | 55 | 20 | 26 | 100 | 470 | 130 |
| (70-100] | 85 | 19 | 45 | 95 | 370 | 225 |
| (100-130] | 115 | 36 | 81 | 180 | 275 | 405 |
| (130-160] | 145 | 19 | 100 | 95 | 95 | 500 |
| **Total** | - | **100** | - | **500** | - | - |

---

#### Aplicația 3 (Pagina 5)

**Date:** Centre de interval: 60, 64, 68, 72, 76.
**Rezolvare:**
*   **a) Mărimea intervalului ($h$):** Este diferența dintre două centre consecutive.
    $h = 64 - 60 = 4$. **Răspuns: 4.**
*   **b) Limitele intervalelor:** Limitele sunt $Centru \pm \frac{h}{2}$. Deci $Centru \pm 2$.
    *   Grupa 1: $60 \pm 2 \rightarrow [58, 62)$
    *   Grupa 2: $64 \pm 2 \rightarrow [62, 66)$
    *   Grupa 3: $68 \pm 2 \rightarrow [66, 70)$
    *   Grupa 4: $72 \pm 2 \rightarrow [70, 74)$
    *   Grupa 5: $76 \pm 2 \rightarrow [74, 78]$

---

### TESTE GRILĂ (Paginile 5-7)

**1. Suma frecvenţelor relative pentru toate grupele unei colectivităţi este:**
*   **Răspuns: a) 1**
*   *Explicație:* Frecvențele relative sunt proporții ($n_i/N$). Suma lor este întotdeauna 1 (sau 100%).

**2. Frecvenţa relativă pentru o grupă (un interval) se calculează:**
*   **Răspuns: d) împărţind frecvenţa absolută corespunzătoare respectivului interval la volumul eşantionului.**
*   *Explicație:* Formula este $f_i = \frac{n_i}{N}$.

**3. Suma frecvenţelor absolute pentru toate grupele unui eşantion este:**
*   **Răspuns: a) egală cu volumul eşantionului;**
*   *Explicație:* Suma numărului de unități din fiecare grupă dă totalul populației/eșantionului ($\sum n_i = N$).

**4. Într-o distribuţie de frecvenţe relative cumulate crescător, ultima grupă va avea o frecvenţă relativă cumulată crescător egală cu:**
*   **Răspuns: b) unu;**
*   *Explicație:* Cumularea tuturor proporțiilor ajunge la 1 (sau 100%).

**5. Într-o distribuţie de frecvenţe relative cumulate descrescător, prima grupă va avea o frecvenţă relativă cumulată egală cu:**
*   **Răspuns: a) unu;**
*   *Explicație:* Cumularea descrescătoare pornește de la total (toți indivizii au valoarea mai mare sau egală cu minimul), deci proporția este 1.

**6. Într-o distribuţie de frecvenţe relative cumulate crescător, prima grupă va avea o frecvenţă relativă cumulată egală cu:**
*   **Răspuns: b) frecvenţa relativă a grupei;**
*   *Explicație:* Pentru prima grupă, nu există nimic anterior de adunat, deci cumulatul este egal cu valoarea simplă a grupei.

**7. Într-o distribuţie de frecvenţe relative cumulate descrescător, ultima grupă va avea o frecvenţă relativă cumulată egala cu:**
*   **Răspuns: b) frecvenţa relativă a grupei;**
*   *Explicație:* La descrescător, ultima grupă conține doar elementele din ea însăși (elementele "mai mari sau egale" cu limita inferioară a ultimei grupe).

**8. O histogramă este:**
*   **Răspuns: a) o reprezentare grafică a unei distribuţii de frecvenţe absolute sau relative pentru o variabilă numerică continuă;**

**9. Pentru reprezentarea grafică a unei distribuţii de frecvenţe pentru o variabilă calitativă se utilizează:**
*   **Răspuns: b) diagrama prin coloane;**
*   *Explicație:* Histogramele sunt pentru variabile continue (intervale lipite), în timp ce diagramele cu bare (coloane) spațiate sunt pentru variabile calitative sau discrete.

**Analiză Tabel (pentru întrebările 10-16):**
Total locuitori ($N$) = $18 + 44 + 68 + 54 + 42 + 36 + 16 + 10 = 288$.

**10. Limita inferioară a primului interval este:**
*   **Răspuns: c) 0;**
*   *Explicație:* Intervalul este 0 – 10.

**11. Dacă vom cumula crescător frecvenţele (absolute), ultima grupă va avea o frecvenţă cumulată egală cu:**
*   **Răspuns: d) 288;**
*   *Explicație:* Frecvența cumulată absolută finală este egală cu totalul populației ($N$).

**12. Dacă vom cumula descrescător frecvenţele, ultima grupă va avea o frecvenţă cumulată egală cu:**
*   **Răspuns: c) 10;**
*   *Explicație:* Ultima grupă (70-80) are 10 locuitori. Cumularea descrescătoare la ultimul pas include doar această grupă.

**13. Dacă vom cumula crescător frecvenţele relative... ultima grupă va avea o frecvenţă relativă egală cu:**
*   **Răspuns: c) 1;**
*   *Explicație:* Similar cu întrebarea 4. Suma proporțiilor este 1.

**14. Procentul locuitorilor cu vârsta mai mică sau egală cu 30 ani este:**
*   **Răspuns: c) 45,13%;**
*   *Calcul:* Grupele implicate: 0-10 (18), 10-20 (44), 20-30 (68).
    Suma = $18 + 44 + 68 = 130$.
    Procent = $130 / 288 = 0,45138... \approx 45,13\%$.

**15. Numărul locuitorilor cu vârsta mai mare cu 50 de ani este:**
*   **Răspuns: a) 62** (Notă: În grilă opțiunea a) pare a fi 62, deși calculul e mai jos).
*   *Calcul:* Grupele implicate: 50-60 (36), 60-70 (16), 70-80 (10).
    Suma = $36 + 16 + 10 = 62$.

**16. Mărimea celui de-al treilea interval este egală cu:**
*   **Răspuns: b) 10;**
*   *Explicație:* Intervalul este 20–30. Mărimea = $30 - 20 = 10$.

**17. Dacă construim mai multe distribuţii... distribuţia cu cea mai mică mărime a grupei (h) va avea:**
*   **Răspuns: b) cele mai multe grupe;**
*   *Explicație:* Relația este invers proporțională. $h = \frac{Amplitudine}{r}$. Dacă $h$ scade, numărul de grupe $r$ trebuie să crească.

**18. Tabelul utilizat pentru prezentarea simultană a datelor referitoare la două variabile se numeşte:**
*   **Răspuns: d) tabel combinat.**
*   *Explicație:* Se mai numește și tabel de contingență.

## 3. Note și Observații
*   Documentul este bine structurat, acoperind atât teoria cât și practica.
*   La exercițiile grilă, întrebarea 15 are opțiunile ușor decalate sau neclare în OCR, dar calculul matematic confirmă varianta a) ca fiind 62.
*   Formulele matematice din partea teoretică (ex: Sturges) au fost transcrise cu mici erori de formatare în textul original (ex: `1 3,322lg` în loc de $1 + 3,322 \lg n$), dar contextul este clar.