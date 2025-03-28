---
title: 11ty - Instalace
date: 2025-03-27
tags: eleventy
eleventyNavigation:
  key: 11ty - Instalace
  parent: Eleventy 
  order: 2
---
K vytvoření první webové stránky s Eleventy stačí velmi málo. Kdekoli v počítači si založte nový adresář. V něm budeme vytvářet náš Eleventy projekt. Adresář si otevřete ve Visual Studio Code a stejně tak si v něm otevřete i terminál. 
<!-- excerpt --> V terminálu postupně spusťte následujících 5 příkazů: 


### 1. Vytvoření souboru package.json
```bash
npm init -y
```
<details>
  <summary>Doplňující informace</summary>
  <p>Dojde k vytvoření souboru <em>package.json</em> ve vašem adresáři. Soubor slouží jako základní konfigurace Node.js projektu. Zde se budou zapisovat například závislosti na instalovaných knihovnách, které se rozhodnete v projektu použít. Jednou z takových knihoven bude právě Eleventy.</p>
</details>

### 2. ESM místo CommonJS
```bash
npm pkg set type="module"
```
<details>
  <summary>Doplňující informace</summary>
  <p>Příkaz přidá do package.json extra řádek <em>"type": "module"</em>, který definuje použití modulů v ESM formátu, což je novější způsob psaní JavaScriptu (proti předchozímu CommonJS). Tenhle příkaz není nezbytný. Pokud ale chcete používat moje zápisky, spusťte ho.</p>
</details>

### 3. Instalace 11ty
```bash
npm install @11ty/eleventy
```
<details>
  <summary>Doplňující informace</summary>
  <p>Do adresáře vašeho projektu se nainstaluje Eleventy. Její instalace se propíše do package.json (do objektu dependencies). Pokud přesunete obsah vašeho Eleventy projektu někam jinam, lze jedním příkazem (npm install) nainstalovat všechny knihovny zapsané v package.json znovu. S instalací Eleventy dojde také k vytvoření souboru <em>package-lock.json</em> a adresáře <em>node_modules</em>.</p>
</details>

### 4. Vytvoření prvního obsahu
```bash
echo '# Můj první Eleventy projekt' > index.md
```
<details>
  <summary>Doplňující informace</summary>
  <p>Vytvoří jednoduchý Markdown soubor s nadpisem „Můj první Eleventy projekt“. Eleventy z něj při generování (viz níže) vytvoří HTML stránku. Jde v podstatě o soubor s obsahem, který chcete na stránce zobrazit. Soubor by se měl jmenovat <em>index.md</em>, protože představuje výchozí stránku webu. Mohl by mít i jiný formát, například <em>index.html</em>, ale psaní obsahu v Markdownu je obecně považováno za jednu z hlavních výhod statických generátorů.</p>
</details>

### 5. Generování stránek
```bash
npx @11ty/eleventy --serve
```
<details>
  <summary>Doplňující informace</summary>
  <p>Eleventy vezme náš Markdown soubor (index.md), převede jeho obsah do HTML formátu a uloží výsledek do nového adresáře <em>_site</em>. Zároveň spustí lokální server a HTML výstup se stane dostupný na <em>http://localhost:8080</em>. Obsah adresáře <em>_site</em> se navíc automaticky přegeneruje pokaždé, když uložíte v Eleventy projektu jakoukoli změnu. A právě tenhle obsah představuje finální produkt celého našeho snažení - výstupní HTML soubory, které můžete teoreticky vzít a nahrát kamkoli, kde budete svoje stránky chtít hostovat. Btw. běh serveru ukončíte zkratkou Ctrl + C v terminálu.</p>
</details>

A to je opravdu všechno. Gratuluji! Svoji první stránku si můžete prohlédnout na adrese [http://localhost:8080](http://localhost:8080).


