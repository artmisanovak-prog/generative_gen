# MOUSE CORE

Samostatné offline-first pracovní prostředí v repozitáři `generative_gen`.

## Nástroje

- [MOUSE CORE – rozcestník](index.html)
- [Gap Workspace](workspace.html) – zápis vztahů mezi fenomény, pozorováním, interpretací a mezerou.
- [Vector Lab](vectors.html) – import skutečných embeddingových vektorů a výpočet kosinové podobnosti.
- [Experience Store](experience.html) – lokální archiv zkušeností, pravidel, hypotéz a neúspěšných pokusů.
- [Transfer Bench](transfer.html) – evidence experimentů s přenosem pravidel mezi doménami.

- [Pilot Results](results.html) – načtení a zobrazení výstupního JSON z Kaggle: strukturální měření, kontexty a vektorová geometrie.
- [BGE-M3 Pilot notebook](BGE_M3_Pilot.ipynb) – Kaggle notebook pro výpočet embeddingů celých pohádek, opakování slov a interpunkce, kontextů výskytů a párové geometrie tří vektorů.

## Stav a technické hranice

- Nástroje jsou samostatné HTML/CSS/JavaScript stránky bez backendu.
- Záznamy se ukládají do `localStorage` konkrétního prohlížeče a zařízení. Pro přenos mezi zařízeními použij JSON export/import.
- Vector Lab načítá již vypočtené embeddingy. Neobsahuje samotný embeddingový model a negeneruje vektory.
- Pro smysluplné porovnávání musí být vektory vytvořeny kompatibilním modelem a stejným postupem.
- Textové a obrazové embeddingy nelze míchat, pokud model výslovně neposkytuje společný multimodální prostor.
- MOUSE CORE neprovádí automatické uvažování jazykového modelu. Slouží jako pracovní a evidenční vrstva pro experimenty.

## Formát vektorů

```json
[
  {
    "id": "mys-01",
    "text": "Popis zdrojového úseku",
    "model": "BAAI/bge-m3",
    "vector": [0.12, -0.04, 0.88]
  }
]
```

Všechny vektory v jednom porovnání musí mít stejný počet dimenzí a pocházet z kompatibilního embeddingového prostoru.
