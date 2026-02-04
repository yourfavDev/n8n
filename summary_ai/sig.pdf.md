# [Titlu: Analiză și Soluționare Examen Baze de Date]
**[Etichetă: Data]:** 2026-02-04T21:06:37.795+02:00
**[Etichetă: Tip]:** Examen / Quiz (SQL, Normalizare, Modelare Date)
**[Etichetă: Limbă]:** Română

## 1. [Titlu: Rezumat / Concept Cheie]
Acest document reprezintă o serie de întrebări de tip grilă și exerciții practice dintr-un examen de Baze de Date. Subiectele acoperite includ terminologia bazelor de date relaționale, interogări SQL (sintaxă specifică Microsoft Access), normalizarea datelor (FN1, FN2, FN3), modelarea entitate-relație și algebra relațională.

## 2. [Titlu: Reconstrucția Datelor și Analiza]
Mai jos sunt prezentate datele reconstruite din capturile de ecran, organizate pe categorii tematice, împreună cu răspunsurile selectate sau soluțiile corecte deduse.

### A. Terminologie și Concepte Fundamentale
**Asociere definiții (Pagina 1):**
| Definiție | Termen Asociat |
| :--- | :--- |
| 1. Coloană a unui tabel | Câmp (atribut) |
| 2. Linie a unui tabel | Înregistrare (tuplu) |
| 3. Mulțimea valorilor unui câmp | Domeniu |
| 4. Câmp (altul decât cheia primară) ce poate fi cheie primară | Cheie candidată |
| 5. Câmp ce servește la realizarea legăturii cu un alt tabel | Cheie externă |

**Proprietăți Cheie Primară (Pagina 4):**
Într-un tabel, câmpul cheie primară trebuie obligatoriu:
*   [x] **b.** Să conțină valori unice.
*   [x] **e.** Să nu conțină valori nule.

### B. Interogări SQL (Data Manipulation Language)

#### 1. Construcție Interogare Simplă (Pagina 2)
**Cerință:** Afișarea numelor primilor 5 angajați cu cele mai mari salarii.
**Soluție (Drag & Drop):**
```sql
SELECT TOP 5 NUME
FROM ANGAJATI
ORDER BY SALARIU DESC
```

#### 2. Interogări cu Jonctiuni și Agregări (Pagina 3)
**Cerință:** Calcul număr conturi bancare pentru fiecare furnizor din categoria "SA".
**Soluție completată:**
```sql
SELECT Count(CONT.NrCont) AS Nr_Conturi, Cont.CodFiscal -- (Notă: sintaxa exactă depinde de blocurile disponibile)
FROM FURNIZOR INNER JOIN CONT ON
URNIZOR.CodFiscal = Cont.CodFiscal
WHERE FURNIZOR.Categorie="SA" AND FURNIZOR.Denumire=[Introduceți numele furnizorului]
GROUP BY CONT.CodFiscal;
```

#### 3. Interogare Grupări și Having (Pagina 11)
**Cerință:** Județele cu mai mult de 4 orașe.
**Soluție completată:**
```sql
SELECT CodJudet, Count(CodOras) AS NrOrase
FROM Oras
GROUP BY CodJudet
HAVING Count(CodOras) > 4;
```

#### 4. Interogare Complexă (Pagina 12)
**Cerință:** Județele cu mai mult de 4 orașe care au peste 20000 locuitori.
**Soluție completată:**
```sql
SELECT Judet.DenumireJudet, Count(Oras.[CodOras]) AS NrOrase
FROM Judet INNER JOIN Oras ON Judet.CodJudet = Oras.CodJudet
WHERE Oras.NumarLocuitori > 20000
GROUP BY Judet.DenumireJudet
HAVING Count(*) > 4;
```

#### 5. Execuție SQL (Pagina 13)
**Date:** Tabelul `Plata` conține date din anii 2019 (2 înreg.), 2020 (2 înreg.), 2021 (2 înreg.).
**Interogare:** `SELECT YEAR(DataPlata)... GROUP BY YEAR(DataPlata)`
**Rezultat:** Interogarea va returna **3** rânduri (câte un rând pentru fiecare an distinct: 2019, 2020, 2021).

#### 6. Sintaxă Update (Pagina 14)
**Cerință:** Diminuarea cu 10% a valorii facturilor din 2015 pentru anumiți clienți.
**Soluție:**
```sql
UPDATE facturi
SET ValoareFacturata = 0.9 * ValoareFacturata
WHERE year(DataFactura) = 2015 and CodClient in (100, 105, 107)
```

#### 7. Sintaxă Delete (Pagina 18)
**Cerință:** Ștergerea salariaților angajați în ultimele 60 de zile din anumite departamente.
**Răspuns Selectat:**
*   [x] **a.** `DELETE FROM SALARIATI WHERE Departament IN SELECT("Contabilitate", "Financiar", "Marketing") AND DataAngajare > Today()-60`
    *(Notă: Sintaxa `IN SELECT(...)` este neobișnuită aici, de obicei este `IN (...)`, dar opțiunea a fost selectată ca fiind corectă în contextul dat).*

### C. Normalizare și Modelare Date

#### 1. Forme Normale
*   **FN3 (Pagina 5):** Un tabel respectă FN3 dacă respectă FN2 și nu există dependențe tranzitive față de cheia primară. (Răspuns: **a**)
*   **Analiză Tabel BACALAUREAT (Pagina 6):** Tabelul `(CNPElev, Nume, Prenume, MedieBAC, CodLiceu, NumeLiceu, OrasLiceu)` încalcă FN3 deoarece există dependența tranzitivă: `CodLiceu` -> `NumeLiceu`, `OrasLiceu`. De obicei, un astfel de tabel este considerat în **FN2** (presupunând cheie simplă `CNPElev`). Răspuns selectat: **d. FN2**.
*   **Analiză Tabel CONCEDII (Pagina 19):** Tabelul conține date despre concediu și datele angajatului (`CNP` -> `Nume`, `Prenume`). Deoarece atributele angajatului depind de CNP (care nu este cheia primară a concediului, ci o cheie externă sau parte dintr-o dependență tranzitivă), tabelul încalcă FN3. Răspunsul selectat este **c. Tabelul respecta FN1** (deoarece valorile sunt atomice).

#### 2. Modelare Relațională (Diagrama ER -> Tabele)
*   **Relație 1-la-N (Pagina 9):** Un contract are un singur angajat responsabil.
    *   Tabel `Contract` trebuie să conțină cheia externă `CodAngajat`.
*   **Relație N-la-M (Pagina 10):** Un contract are mai mulți angajați responsabili.
    *   Este necesară o tabelă de legătură `AngajatContract(CodAngajat, NrContract)`.
*   **Relație N-la-M cu Atribute (Pagina 20):** Clienții au coduri CAEN, cu anul obținerii specific perechii.
    *   Soluția corectă este **d**:
        *   `Client (CUIClient, ...)`
        *   `CAEN (CodCAEN, ...)`
        *   `ClientCAEN (CUIClient, CodCAEN, AnObtinereCAEN)`

### D. Algebra Relațională și Seturi

#### 1. Operația Diferență (Pagina 8)
*   **Tabel Clienti:** {ABC, XYZ, ABA}
*   **Tabel Furnizori:** {ABC, DDE}
*   **Rezultat:** {XYZ, ABA}
*   **Analiză:** Rezultatul conține elementele din Clienti care NU sunt în Furnizori ($A - B$).
*   **Răspuns:** a. Diferența dintre tabelele Clienti și Furnizori.

#### 2. Operația Intersecție (Pagina 21)
*   **Tabel Clienti:** {ABC, XYZ, ABA}
*   **Tabel Furnizori:** {ABC}
*   **Rezultat:** {ABC}
*   **Analiză:** Rezultatul conține elementele comune ($A \cap B$).
*   **Răspuns:** a. Intersecția dintre tabelele Furnizori și Clienti.

## 3. [Titlu: Soluție Pas-cu-Pas pentru Probleme Specifice]

### Analiza Integrității Referențiale (Pagina 16)
Se dau tabelele `Client` și `Factura`.
*   **Chei:** `CodClient` în tabelul `Client` (PK), `NrFactura` în `Factura` (PK), `CodClient` în `Factura` (FK).
*   **Date:**
    *   `Client`: Codurile 1, 2, 3, 4.
    *   `Factura`: Conține `CodClient` 1 și **44**.
*   **Concluzie:** Deoarece valoarea **44** din tabelul copil (`Factura`) nu există în tabelul părinte (`Client`), integritatea referențială **nu** este respectată.
*   **Răspunsuri corecte bifate:**
    *   [x] b. Nu este respectata integritatea referentiala a datelor.
    *   [x] c. In model se pot identifica 2 chei primare si o cheie externa.
    *   [x] d. In cele 2 tabele sunt, in total, 7 inregistrari (4 clienți + 3 facturi).

### Logică SQL Specifică Access (Pagina 7)
Analiza afirmațiilor corecte:
1.  **Between:** `WHERE Salariu BETWEEN 1000 AND 2000` este metoda corectă pentru intervale inclusive. (Bifat **b**).
2.  **Date():** Funcția `Date()` returnează data curentă în Access. Pentru "ultimele 10 zile", condiția este ca data facturii să fie mai mare decât data curentă minus 10 zile.
    *   Corect: `DataFactura > Date()-10` (Bifat **f**).

### Logică Booleană Complexă (Pagina 17)
**Cerință:**
1.  (Februarie 2014 AND Valoare > 1000)
    **SAU**
2.  (Martie 2014 AND Valoare < 200)

**Sintaxa corectă:**
Necesită paranteze pentru a separa cele două condiții majore reunite prin OR.
Răspunsul **d** este corect:
$$ (Month(...) = 2 \land Year(...) = 2014 \land Val > 1000) \lor (Month(...) = 3 \land Year(...) = 2014 \land Val < 200) $$

## 4. [Titlu: Concluzii și Note]
*   **Tipul de SQL:** Întrebările sunt specifice dialectului SQL folosit în **Microsoft Access** (utilizarea `TOP`, `Date()`, `YEAR()`, wildcards `*` în loc de `%` pentru `LIKE`, delimitatori `#` sau funcții specifice de dată).
*   **Capcane:** La problemele de algebră relațională, este crucial să se observe dacă rezultatul reprezintă elemente comune (Intersecție) sau elemente unice primului tabel (Diferență). Imaginile 8 și 21 ilustrează exact aceste două cazuri distincte.
*   **Normalizare:** Un punct recurent este identificarea dependențelor tranzitive (atribute non-cheie care depind de alte atribute non-cheie), ceea ce indică încălcarea Formei Normale 3.