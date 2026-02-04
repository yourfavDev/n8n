# Titlu: Analiza Documentului: Curs - Circuite Liniare de Microunde
**Dată:** 2026-02-04T21:52:37.285+02:00
**Tip:** Notițe Curs Universitar / Teorie Inginerească
**Limbă:** Română

## 1. Rezumat
Acest document reprezintă un suport de curs detaliat pentru "Circuite liniare de microunde", predat de Ș.l. Dr. Ing. Diana Brînaru. Conținutul acoperă tranziția de la teoria clasică a circuitelor la teoria microundelor, definind tensiuni și curenți echivalenți, unde de putere ($a$ și $b$), și introducând matricea de repartiție ($[S]$) ca instrument fundamental pentru analiza multiporturilor, inclusiv proprietățile acesteia (reciprocitate, pasivitate, pierderi) și relația cu matricea de impedanță ($[Z]$).

## 2. Reconstrucția și Analiza Datelor Teoretice

Deoarece documentul este un suport teoretic și nu conține date statistice brute, această secțiune sistematizează formulele fundamentale și definițiile prezentate în curs sub formă tabelară pentru o consultare rapidă.

### Tabel Sinoptic: Mărimi și Relații Fundamentale

| Concept | Formula / Relație Matematică | Descriere |
| :--- | :--- | :--- |
| **Unde de Putere** | $a = \frac{1}{2\sqrt{Z_0}}(U + Z_0 I)$ | Unda incidentă (transportă putere spre sarcină). |
| | $b = \frac{1}{2\sqrt{Z_0}}(U - Z_0 I)$ | Unda reflectată (transportă putere dinspre sarcină). |
| **Inversare (U, I)** | $U = \sqrt{Z_0}(a + b)$ | Tensiunea exprimată prin unde de putere. |
| | $I = \frac{1}{\sqrt{Z_0}}(a - b)$ | Curentul exprimat prin unde de putere. |
| **Puterea** | $P = \frac{1}{2}(|a|^2 - |b|^2)$ | Puterea activă netă într-o secțiune. |
| **Coef. Reflexie ($\Gamma$)** | $\Gamma = \frac{b}{a} = \frac{Z - Z_0}{Z + Z_0}$ | Raportul dintre unda reflectată și cea incidentă. |
| **Matricea [S]** | $[b] = [S][a]$ | Relația liniară dintre undele incidente și cele reflectate la un multiport. |
| **Transformare [Z] $\leftrightarrow$ [S]** | $[S] = ([Z] - [Z_0])([Z] + [Z_0])^{-1}$ | Relația dintre matricea de impedanță și cea de repartiție (pentru $Z_0$ egal la toate porțile). |
| **Schimbare plan ref.** | $[S'] = [\Phi][S][\Phi]$ | $[\Phi]$ este matrice diagonală de defazaj $e^{-j\beta l_i}$. |

## 3. Soluții Pas-cu-Pas pentru Temele Propuse

Documentul conține mai multe secțiuni marcate ca "Temă" sau deducții implicite. Mai jos sunt prezentate rezolvările detaliate bazate pe teoria expusă.

### Problema 1: Transferul Maxim de Putere (Slide 9)
**Cerință:** Să se determine condiția pentru $\Gamma_S$ astfel încât puterea $P$ să fie maximă, unde $P = f(a_G, \Gamma_G, \Gamma_S)$.

**Rezolvare:**
Expresia puterii livrate sarcinii este:
$$P = \frac{|a_G|^2}{2} \frac{1 - |\Gamma_S|^2}{|1 - \Gamma_G \Gamma_S|^2}$$
Pentru a maximiza puterea, trebuie minimizat numitorul și maximizat numărătorul în contextul adaptării conjugate. Matematic, maximul se obține atunci când reflexiile se anulează reciproc conjugat.

Condiția de adaptare conjugată este:
$$\Gamma_S = \Gamma_G^*$$
unde $\Gamma_G^*$ este complex conjugatul coeficientului de reflexie al generatorului.

În acest caz, puterea maximă disponibilă ($P_{max,d}$) devine:
$$P_{max,d} = \frac{|a_G|^2}{2} \frac{1}{1 - |\Gamma_G|^2}$$
*(Notă: Această relație este validă pentru $|a_G|$ constant și sursă pasivă stabilă).*

---

### Problema 2: Schimbarea Planelor de Referință (Slide 14)
**Cerință:** Să se determine elementele matricei $[S']$ pentru un diport, știind că $[S'] = [\Phi][S][\Phi]$, unde $[\Phi]$ descrie propagarea pe liniile de acces de lungimi $l_1$ și $l_2$.

**Date:**
Matricea de defazaj este:
$$[\Phi] = \begin{bmatrix} e^{-j\beta l_1} & 0 \\ 0 & e^{-j\beta l_2} \end{bmatrix}$$

**Calcul:**
Operația matriceală este:
$$[S'] = \begin{bmatrix} e^{-j\beta l_1} & 0 \\ 0 & e^{-j\beta l_2} \end{bmatrix} \begin{bmatrix} S_{11} & S_{12} \\ S_{21} & S_{22} \end{bmatrix} \begin{bmatrix} e^{-j\beta l_1} & 0 \\ 0 & e^{-j\beta l_2} \end{bmatrix}$$

1.  Înmulțirea primelor două matrici (înmulțirea la stânga cu o matrice diagonală scalează rândurile):
    $$[\Phi][S] = \begin{bmatrix} S_{11}e^{-j\beta l_1} & S_{12}e^{-j\beta l_1} \\ S_{21}e^{-j\beta l_2} & S_{22}e^{-j\beta l_2} \end{bmatrix}$$

2.  Înmulțirea cu a treia matrice (înmulțirea la dreapta cu o matrice diagonală scalează coloanele):
    $$[S'] = \begin{bmatrix} S_{11}e^{-j\beta l_1} \cdot e^{-j\beta l_1} & S_{12}e^{-j\beta l_1} \cdot e^{-j\beta l_2} \\ S_{21}e^{-j\beta l_2} \cdot e^{-j\beta l_1} & S_{22}e^{-j\beta l_2} \cdot e^{-j\beta l_2} \end{bmatrix}$$

**Rezultat Final (Elementele matricei):**
*   $S'_{11} = S_{11} e^{-j2\beta l_1}$ (Faza se rotește cu drumul dus-întors pe linia 1)
*   $S'_{12} = S_{12} e^{-j\beta (l_1 + l_2)}$ (Faza se adaugă pentru tranzitarea ambelor linii)
*   $S'_{21} = S_{21} e^{-j\beta (l_2 + l_1)}$
*   $S'_{22} = S_{22} e^{-j2\beta l_2}$

---

### Problema 3: Multiport Pasiv și Nedisipativ (Slide 18)
**Cerință:** Determinarea relațiilor care rezultă din condiția $[S]^*[S] = [1]$ (Matrice unitară).

**Analiză:**
Pentru o matrice unitară, produsul dintre transpusa conjugată și matricea însăși este matricea identitate ($\delta_{ij}$).
Elementul generic al produsului este: $\sum_{k=1}^n S_{ki}^* S_{kj} = \delta_{ij}$.

Aceasta implică două seturi de ecuații:

1.  **Pentru elementele de pe diagonală ($i=j$):**
    Suma pătratelor modulelor elementelor de pe o coloană (sau linie, pentru reciproce) este 1. Aceasta reflectă **conservarea puterii** (energia care intră pe o poartă trebuie să iasă integral pe celelalte porți).
    $$\sum_{k=1}^n |S_{ki}|^2 = 1$$

2.  **Pentru elementele din afara diagonalei ($i \neq j$):**
    Produsul scalar al coloanelor matricei $S$ este nul. Aceasta reprezintă o relație de ortogonalitate (relație de fază între parametri).
    $$\sum_{k=1}^n S_{ki}^* S_{kj} = 0, \quad \text{pentru } i \neq j$$

## 4. Concluzii și Observații

*   **Importanța Matricei S:** În domeniul microundelor, tensiunile și curenții totali sunt greu de măsurat direct din cauza variației spațiale rapide. Undele de putere și parametrii S sunt preferați deoarece se leagă direct de fluxul de putere și reflexii, fiind măsurabili cu analizoare vectoriale de rețea (VNA).
*   **Normalizarea:** Toate definițiile parametrilor S depind de impedanța de normare ($Z_0$). Modificarea $Z_0$ (renormalizarea) schimbă valorile parametrilor S, chiar dacă componenta fizică rămâne neschimbată (Slide 15).
*   **Reciprocitatea:** Pentru componente pasive uzuale (fără ferite polarizate sau elemente active), matricea S este simetrică ($S_{ij} = S_{ji}$), ceea ce simplifică proiectarea și măsurătorile.
*   **Validarea Datelor:** Relațiile deduse pentru rețelele fără pierderi (Slide 18) sunt cruciale pentru verificarea validității numerice a simulărilor sau măsurătorilor; dacă suma pătratelor modulelor nu este 1 (cu o toleranță mică), există erori de calcul sau pierderi necontabilizate.