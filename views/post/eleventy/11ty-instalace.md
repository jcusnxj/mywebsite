---
title: 11ty - Instalace
date: 2025-03-27
tags: eleventy
eleventyNavigation:
  key: 11ty - Instalace
  parent: Eleventy 
  order: 2
---
K vytvoření první statické webové stránky s pomocí Eleventy stačí velmi málo. Kdekoli v počítači si založte nový adresář. V něm budeme vytvářet náš Eleventy projekt. Adresář si otevřete ve Visual Studio Code a stejně tak si v něm otevřete i terminál. 
<!-- excerpt --> V terminálu postupně spusťte následujících 5 příkazů: 


### 1. Vytvoření souboru package.json
```bash
npm init -y
```
<details>
  <summary>Doplňující informace</summary>
  <p>Dojde k vytvoření souboru package.json ve vašem adresáři. Soubor slouží jako základní konfigurace Node.js projektu. Zde se budou zapisovat například závislosti na instalovaných knihovnách, které se rozhodnete v projektu použít. Jednou z takových knihoven bude právě Eleventy.</p>
</details>

### 2. ESM místo CommonJS
```bash
npm pkg set type="module"
```
<details>
  <summary>Doplňující informace</summary>
  <p>Přidá do package.json extra řádek ("type": "module"), který definuje použití modulů v ESM formátu, což je novější způsob psaní JavaScriptu (proti předchozímu CommonJS). Tenhle příkaz není ani nutný. Pokud ale chcete používat moje zápisky, spusťte ho.</p>
</details>

### 3. Instalace 11ty
```bash
npm install @11ty/eleventy
```
<details>
  <summary>Doplňující informace</summary>
  <p>Do vašeho adresáře se nainstaluje Eleventy. Její instalace se propíše do package.json (do objektu dependencies). Díky tomu můžete například přesunout obsah vašeho Eleventy projektu do jiného adresáře a jedním příkazem (npm install) nainstalovat všechny knihovny zapsané v package.json znovu. S instalací Eleventy dojde také k vytvoření souboru package-lock.json a adresáře node_modules.</p>
</details>

### 4. Vytvoření prvního obsahu
```bash
echo '# Můj první Eleventy projekt' > index.md
```
<details>
  <summary>Doplňující informace</summary>
  <p>Vytvoří jednoduchý Markdown soubor s nadpisem „Můj první Eleventy projekt“. Eleventy z něj při generování (viz níže) vytvoří HTML stránku. Jde v podstatě o soubor s obsahem, který chcete na stránce zobrazit. Soubor by se měl jmenovat index.md, protože představuje výchozí stránku webu. Mohl by mít i jiný formát, například index.html, ale psaní obsahu v Markdownu je obecně považováno za jednu z hlavních výhod statických generátorů.</p>
</details>

### 5. Generování stránek
```bash
npx @11ty/eleventy --serve
```
<details>
  <summary>Doplňující informace</summary>
  <p>Eleventy vygeneruje HTML stránky a spustí lokální server. Stránky budou dostupné na http://localhost:8080. HTML výstup se navíc automaticky přegeneruje pokaždé, když uložíte ve vašem Eleventy projektu jakoukoli změnu. HTML výstup se ukládá do nového "_site" adresáře. Právě tento adresář obsahuje finální produkt celého našeho snažení - výstupní soubory, které můžete teoreticky vzít a nahrát kamkoli, kde budete svoje stránky hostovat. Btw. běh serveru ukončíte zkratkou Ctrl + C v terminálu.</p>
</details>

A to je opravdu všechno. Gratuluji! Svoji první stránku si můžete prohlédnout na adrese [http://localhost:8080](http://localhost:8080).


