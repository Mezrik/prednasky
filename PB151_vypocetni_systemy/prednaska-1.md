# Pojmy, číselné soustavy

## Základní Pojmy
**Byte (slabika)** - 8 bitů, 128 kombinací (7 bitů stačí na ASCI + 1 navíc na zabezpečení paritou, paritní bit, umí ale najít jen lichý počet chyb), např. na děrném pásku, horní řada paritní

![Děrná páska](https://i.imgur.com/qFU9lE3.gif)

dnes je zabezpečení mimo data, ne paritním bitem

* **Word (slovo)** - několik slabik (2, 4, 6, 8)
* **Paměť** - Uchovává informace, operační, vnější…
* **Adresa v paměti** - číselné označení místa v paměti
* **Nejmenší adresovatelná jednotka** - kapacita místa v paměti, které má vlastní adresu (slabika, slovo)

#### Adresace v paměti
**Adresový registr = n-tice bitů** - 3-bitový registr může mít hodnotu max, 7 (2<sup>2</sup> + 2<sup>1</sup> + 2<sup>0</sup>) | 2<sup>10</sup> = 1 KB, 2<sup>20</sup> = 1 GB…

**Střádač**, registr sčítající přijaté hodnoty, **Adresový registr**, **Datový registr**

#### Typy paměti
* _RAM_ pro čtení a zápis
* _ROM_ pouze čtení, permanentní paměť 
* _Paměť s přímým nebo sekvenčním přístupem_
* _Vnitřní_ (operační) a _vnější_ (periferní)
* _Registry_
* _V / V zařízení_ vstup a výstup
* _Řadič_
