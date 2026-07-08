# Návod k použití – NakupniCenaFilter

## Co program dělá
Z velkého exportu z Ventusu vybere pouze položky, jejichž kódy si zadáš, a výsledek přehledně sestaví na 3. listu ve stejném souboru.

## Postup

### 0. Stažení programu

Program najdeš na společném disku na adrese:
S:\_Osobni_slozky\Max\NakupniCenaFilter
Stáhni si nejnovější verzi programu do svého počítače. Tento krok stačí provést pouze jednou.

### 1. Připrav si Excel soubor
1. Exportuj data z Ventusu do .xlsx souboru.
2. Ujisti se, že tento export je **1. list** v sešitu (obsahuje sloupce Kód sortimentu, Cena, Název, Nákupní smluvený ceník - platnosti.Název).
3. Vytvoř/otevři **2. list** v tomtéž souboru a do sloupce A napiš kódy položek, které chceš vyfiltrovat – jeden kód na řádek.

   - Kódy můžeš psát klidně jako čísla i s chybějící nulou na začátku (např. `12345` místo `012345`) – program si to sám opraví.
   - Pořadí kódů na 2. listu určuje pořadí výsledků na 3. listu.

4. Soubor ulož.

### 2. Spusť program
1. Spusť `NakupniCenaFilter.exe`.
2. Otevře se dialog – vyber svůj připravený .xlsx soubor.
3. Program chvíli pracuje (u velkých souborů to může trvat pár vteřin).

### 3. Zkontroluj výsledek
- Po dokončení se zobrazí okno se shrnutím: kolik kódů se hledalo, kolik řádků se našlo, kolik kódů se nenašlo.
- Otevři soubor znovu v Excelu – uvidíš nový/přepsaný **3. list "Vyfiltrovano"**.
- Pokud se pro nějaký kód nic nenašlo, objeví se v tabulce s poznámkou **"POLOŽKA NENALEZENA"** – zkontroluj, jestli je kód napsaný správně nebo jestli položka v exportu z Ventusu vůbec existuje.

## Když potřebuješ přidat další kódy
1. Nemusíš nic mazat – stačí na **2. list** přidat/upravit kódy.
2. Spusť `NakupniCenaFilter.exe` znovu a vyber stejný soubor.
3. **3. list se při každém spuštění celý přepíše** podle aktuálního obsahu 2. listu – takže tam zůstanou vždy jen aktuální výsledky, ne staré + nové dohromady.

