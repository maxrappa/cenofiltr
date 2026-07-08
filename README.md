# Jak z ventus_filter.py udělat .exe

Potřebuješ Windows PC s nainstalovaným Pythonem (stačí jednou, jen pro sestavení — na cílových PC už Python nebude potřeba).

## 1. Instalace nástrojů (jednorázově)
Otevři příkazovou řádku (cmd) a spusť:
```
pip install openpyxl pyinstaller
```

## 2. Sestavení .exe
V příkazové řádce přejdi do složky, kde je `ventus_filter.py`, a spusť:
```
pyinstaller --onefile --noconsole --name VentusFilter ventus_filter.py
```

- `--onefile` = vše zabalí do jednoho .exe souboru
- `--noconsole` = nebude se otevírat černé okno konzole, jen dialogová okna

## 3. Výsledek
Hotový soubor najdeš v: `dist\VentusFilter.exe`

Tento soubor už funguje samostatně na jakémkoliv Windows PC (i bez Pythonu) — stačí ho zkopírovat a spustit.

## Jak program funguje
1. Spustíš `VentusFilter.exe`
2. Otevře se dialog pro výběr souboru — vybereš svůj Excel export z Ventusu
3. Program očekává v souboru:
   - **1. list** – data z Ventusu (sloupce: Kód sortimentu, Cena, Název, Nákupní smluvený ceník - platnosti.Název)
   - **2. list** – tvůj seznam kódů (Kód sortimentu), po jednom v každém řádku, sloupec A
4. Program vytvoří/přepíše **3. list** s názvem "Vyfiltrovano", kde budou všechny řádky odpovídající zadaným kódům (včetně více řádků pro stejný kód, např. různí výrobci)
5. Kódy, které se v datech nenajdou, se do výsledku přidají s poznámkou "POLOŽKA NENALEZENA"
6. Na konci se zobrazí okno s výsledkem (počet nalezených řádků, počet nenalezených kódů) nebo chybová hláška

Soubor se ukládá **do stejného souboru**, který jsi vybral (přidá/přepíše 3. list).
