---
title: 11ty - Instalace
date: 2025-03-21
tags: eleventy
eleventyExcludeFromCollections: ["post"]
eleventyNavigation:
  key: 11ty - Instalace
  parent: Eleventy 
  order: 2
---
V tomto článku vytvoříme první jednoduchou webovou stránku pomocí 11ty. Nebude zatím dostupná nikde na internetu a půjde zobrazit pouze lokálně na našem počítači. Takže pojďme na to. 
<!-- excerpt -->

#### 1. Vytvoření souboru package.json
```bash
npm init -y
```
#### 2. ESM místo commonJS
```bash
npm pkg set type="module"
```
#### 3. Instalace 11ty
```bash
npm install @11ty/eleventy
```
#### 4. Vytvoření prvního obsahu
```bash
echo '# Můj první Eleventy projekt' > index.md
```
#### 5. Generování stránek
```bash
npx @11ty/eleventy --serve
```