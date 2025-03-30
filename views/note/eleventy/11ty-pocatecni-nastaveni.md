---
title: 11ty - Počáteční nastavení
date: 2025-03-27
tags: eleventy
eleventyNavigation:
  key: 11ty - Počáteční nastavení
  parent: Eleventy 
  order: 1
---
### 1. Vytvoření souboru package.json
```bash
npm init -y
```

### 2. ESM místo CommonJS
```bash
npm pkg set type="module"
```

### 3. Instalace 11ty
```bash
npm install @11ty/eleventy
```

### 4. Vytvoření index.md
```bash
echo '# Můj první Eleventy projekt' > index.md
```

### 5. Generování stránek
```bash
npx @11ty/eleventy --serve
```


