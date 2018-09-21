# 1. Úvod

## 1.1. Nevýhody používání souborových systémů k ukládání dat
* data nebyly přistoupitelná
  * tvorba nových programů pro přístup k datům
* velká **rendundance** dat (seznam studentů x studenti koleje)
* nutnost **zapojení programátora** při vytvoření jakéhokoliv požadavku
* problémy s **integritou**, akce zakódované ve vlastním programu (nalezení a změna v programu)

### 1.1.1 Hlubší problémy
* jakékoliv zpracování logické transakce se musí chovat konsistetním způsobem (musí se vykonat celá nebo se nevykoná vůbec)
* přístup více uživatelů
  - souběžné zpracování dat více uživateli
  - nekonzistentní (stav účtu 100, aktualizovaný souběžně dvěma lidmi, například vybráním 50)
* bezpečnostní problémy

## 1.2. Datové modely
* soubor nástrojů umožňující popisovat data, jejich sémantiku a omezení
* **relační datový model** (nejpoužívanější)
* **ERD** (Entity-Relationship data models) design databází
* Object-based datový model (v současné době méně používaný)
* Semistrukturované datové modely (XML) - vznik na základě přenosu dat mezi jednotlivými systémy (až tak se neujalo)
* Další starší modely
  - Síťové modely
  - Hierarchické modely

## 1.3. Relační datový model
* fast, simple and relevant (koncept jednoduchý, blízký lidem)
* laicky - relace je tabulka (sloupce - **atributy** a řádky - **n-tice**)
* první sloupec **ID** - primární klíč, unikátní, slouží k identifikaci n-tice
* relace - tabulka (vztah je v datech)

## 1.4. Data Definition Language (DDL)
* co nejjednodušší pro lidi (např. **create table instructor(..)**)
* vytváří sadu vzorů pro tabulky, ukládá do **datového adresáře** (obsahuje i informace o integritních omezeních)
  - integritní omezení - primární klíč, referenční integrita (závislosti)

## 1.5. SQL
* **hlavní komunikační prostředek pro relační databáze**
* rozšířený neprocedurální jazyk

## 1.6 Design databáze
* vyvarování se redundanci - každá informace by měla existovat pouze jednou (riziko inkonzistence)
* normalizační teorie - formulace zásad
* ERM (Entity Relationship Model) - navrhuje datovou realitu jako množinu entit a jejich vztahů
  * entita je v zásadě cokoliv, jež jsme schopni rozpoznat v reálném světě
  * entita popisována podle určité množiny atributů
  * např. my tvoříme entitní množinu lidé

## 1.7. Storage management
* hlavní problémy
  - přístup k úložišti
  - organizace souborů
  - indexování a hashování

## 1.8. Zpracování dotazu (Query processing)
* viz prezentace
* v první řadě analyzace dotazu, sytaktický, sémantická analýza (parser and translator)
* původní dotaz přeložen do **relační algebry**
* v relační algebře systém provede **optimalizaci**
* vytvoření execution plánu, poslání do evaluation engine jež podá výstup pro query

## 1.9. Management transakcí
* tansakce je kolekce operací, které vykonává jedna funkce v databázové aplikaci
* zajištení práce více uživatelů najednou, Transaction-management component (konzistence)
