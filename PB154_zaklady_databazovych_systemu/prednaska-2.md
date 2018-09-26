# 2. Relační modely

## 2.1. Základní pojmy
* *doména (D)* = množina hodnot, kterých nabývá atribut, null je prázdná hodnota součástí každé domény, např. doména dnů v týdnu = pondělí, úterý…
* *atributy (A)* = sloupce tabulky, atomické (dále se nedělí, nerozkláda)
* *n-tice* = řádky, z hlediska uložení databáze nezáleží na pořadí
* *relace (r)* = "tabulka", podmnožina kartézského součinu D1 x D2  x…x Dn
  - při definici určujeme, jaké má relační schéma a relační výskyty  např. instructor(INSTRUCTOR) nebo instructor(ID, name, salary)
* *relační schéma (R)* = schéma s atributy A a vlastními doménami D1, D2…Dn
  - např. R = (A1, A2….An); INSTRUCTOR = (ID, name, salary)
* *výskyt relace (instance)* = počet n-tic obsažených v **daném časovém momentu**
* *databáze* = množina relací
  - např instructor (ID, name…), student (ID, name…), advisor (ID, name…)

<hr>

**super/klíč (K)** = množina atributů, která umožňuje poznat libovolnou n-tici v relaci (např. {ID} nebo {ID, name}
**kandidátský klíč** = minimální množina atributů (např. {ID})
vybere se z nich 1, který se stane primárním klíčem

![schéma](https://i.imgur.com/2aamu2Z.png)

## 2.2. Relační query jazyky

* obsahuje uživatelské dotazy
* **PROCEDURÁLNÍ JAZYKY**: říkají co chci a jakým způsobem postupovat, abychom se k tomu dostali
* **DEKLARATIVNÍ (neprocedurální) JAZYKY**: neříkají, jakým způsobem dosáhnout výsledku
* **ČISTÉ JAZYKY**: relační algebra (proc. jazyk, jednoduchá, málo operátorů)

SQL (Structured Queary Language, umí definovat požadavky na databázi, požadavky se zpracují do relační algebry a zpracuje se, jak informaci vyhodnotit)

### 2.2.1. Relační algebra
* 6 operátorů: select, project, union, set difference, Cartesian product, rename
* po použití operátoru vzniknou další relace

>O<sub>p</sub>(r) = {t; t náleží relaci a jsou splněné predikáty p}

<hr>

**[σ] select, odstranění řádků**
A=B a zároveň D>5

![select](https://i.imgur.com/eLCaplw.png)

<hr>

**[π] project, odstranění sloupců**
π<sub>A,B</sub> (r); r = A, B, C
(po = se odstraní nově vzniklé duplicity, protože jsme odstranili B, primární klíč)

![project](https://i.imgur.com/SLVpmey.png)

<hr>

**[u] union, sjednocení**
r u s
(obě relace musí mít stejnou aritu = množství atributů)

![union](https://i.imgur.com/y19Gkqh.png)

<hr>

**[-] difference, rozdíl**
r - s
(obě relace musí mít stejnou aritu = množství atributů)

![difference](https://i.imgur.com/Uwn8eps.png)

<hr>

**[x] kartézský součin**
r x s

![součin](https://i.imgur.com/qE61Tw9.png)
