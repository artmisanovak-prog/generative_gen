# Pokyny pro GitHub Copilot – generative_gen

## Co je tento repozitář
Toto je pracovní prostředí projektu Semantic Gap / MOUSE. Nejde jen o běžný generátor textu ani o obyčejný dataset. Karty propojují původní pohádky, ilustrace, segmenty, měřitelné vlastnosti, modelové reprezentace a následné zkoumání vztahů a přenosu pravidel.

## Základní pravidla práce
- Nejdřív prohlédni existující strukturu, soubory a odkazy. Nevymýšlej novou architekturu, pokud úkol žádá jen cílenou úpravu.
- Zachovávej původní texty přesně: pravopis, interpunkci, nezvyklé tvary, řádkování i autorský rytmus. Nikdy je tiše neopravuj ani nepřepisuj.
- Rozlišuj primární zdroj, segmentaci, autorskou interpretaci, odvozené rysy a výstupy modelu. Tyto vrstvy neslučuj.
- Nikdy nevymýšlej embeddingové vektory, modelové výpočty, rozměry ani výsledky. Pokud model nebyl skutečně spuštěn, označ vektor jako not_computed.
- TF-IDF je lexikální baseline, nikoli neuronový sémantický embedding. PCA, kosinová podobnost, graf a TDA odvozené z TF-IDF nejsou nezávislými sémantickými důkazy.
- Textové a obrazové vektory porovnávej jen tehdy, když model skutečně poskytuje kompatibilní společný prostor. Vždy zaznamenej poskytovatele, přesný model/verzi, dimenzi a prostor.
- Udržuj navigaci přes relativní cesty. Každá nová karta musí být dosažitelná z příslušného indexu.
- Před úpravou načti aktuální soubor. Po úpravě znovu načti a ověř obsah, odkazy, JSON syntaxi a zachování primárních zdrojů.
- Neprohlašuj, že proběhl vizuální test v prohlížeči, pokud skutečně neproběhl.

## Významová přesnost – karta Kocour
- Dvě spolknuté berušky měly každá sedm teček. Číslo 14 je přesný počet spolknutých teček, tedy vstupní příčina.
- Následný jev trval půl hodiny, tedy 30 minut.
- Během něj kocour krkal tečky a předčasně dokončoval věty lidem na celém světě.
- Počet vykrknutých teček není určen.
- Počet předčasně dokončených vět není určen.
- Nikdy neodvozuj, že kocour vykrkal přesně 14 teček nebo dokončil 14 vět.
- Počet vstupních prvků se automaticky nerovná počtu výstupů nebo následků. Neurčeno není totéž co nula.
- Po skončení krkání lidé opět mohli dokončovat své věty sami.

## Doporučený způsob analýzy karty
U každého jevu odděl:
1. zdrojové tvrzení a jeho přesný úryvek;
2. vstupní stav / příčinu;
3. průběh / mechanismus;
4. dobu trvání;
5. rozsah / koho nebo co jev zasahuje;
6. následek a změnu stavu;
7. přesně známé hodnoty;
8. neznámé nebo neurčené hodnoty;
9. možné vztahy a hypotézy, jasně označené jako hypotézy.

Když údaj ve zdroji chybí, napiš „neurčeno“ a nevymýšlej náhradní hodnotu. U každého odvození ukaž, z jakého úryvku vychází.

## Jak plnit úkoly
- Nejprve stručně zjisti, co už v repozitáři existuje a které soubory úkol ovlivní.
- Pracuj po malých, kontrolovatelných změnách.
- Zachovej stávající vzhled a funkce, pokud zadání výslovně nepožaduje změnu.
- Výstup musí být použitelný na mobilu i desktopu.
- Po dokončení uveď konkrétní změněné soubory, provedené kontroly a známá omezení.
