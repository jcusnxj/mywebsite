---
title: 11ty - Nastavení
date: 2025-04-01
templateEngineOverride: md
eleventyNavigation:
  key: 11ty - Nastavení
  parent: Zápisky
  order: 1
---
### package.json
```bash
npm init -y
```
### ESM místo CommonJS
```bash
npm pkg set type="module"
```
### Instalace 11ty
```bash
npm install @11ty/eleventy
```
### index.md
```bash
echo '# My Eleventy Project' > index.md
```
### .gitignore
```txt
dist          
node_modules
.DS_Store
.vscode
.env
```
`/.gitignore`
### eleventy.config.js
```js
export default function(eleventyConfig) {
	// Configure Eleventy
};
```
`/eleventy.config.js`
### Override výchozích adresářů
```js
export default function(eleventyConfig) {
	// Configure Eleventy
};

export const config = {
    dir: {
      input: "views",  
      layouts: "_layouts",
      output: "dist"
    }
  };
```
`/eleventy.config.js`
### package.json - skripty
```json
"scripts": {
     "start": "eleventy --serve",
     "build": "eleventy"
}
```
`/package.json`
### njk - výchozí template engine
```js
export default function(eleventyConfig) {
	// Configure Eleventy
};

export const config = {
  markdownTemplateEngine: "njk",
  htmlTemplateEngine: "njk",
};
```
`/eleventy.config.js`
### Adresářová struktura
```txt
└── views                   // custom override of default folder 
│    ├── _data              // global data folder
│    │     └── site.js      
│    ├── _includes
│    │     └── partials   
│    ├── _layouts           // custom override of default folder 
│    │     └── base.njk     // base layout
│    ├── assets             // custom folder
│    │     ├── css          
│    │     ├── img          
│    │     └── js           
│    ├── note               // custom folder
│    │     └── note.json    // default Front Matter Data 
│    ├── post               // custom folder
│    │     └── post.json    // default Front Matter Data 
│    └── index.md           
├── .eleventy.config.js            
├── .gitignore              
├── package.json            
└── package-lock.json       
```
### addPassthroughCopy metoda
```js
export default function(eleventyConfig) {

    // method creates a file/folder copy in the output directory
	eleventyConfig.addPassthroughCopy("views/assets/css");
    eleventyConfig.addPassthroughCopy("views/assets/img");
    eleventyConfig.addPassthroughCopy("views/assets/js");
};
```
`/eleventy.config.js`
### Základní layout
```html
<!DOCTYPE html>
<html lang="cs">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>{{ title }}</title> 
  </head>
  <body>
    <main>
      {% block content %}
      {{ content | safe }}
      {% endblock %}    
    </main>
  </body>
</html>
```
`/views/_layouts/base.njk`
### Defaultní Front Matter Data
```json
{
    "layout": "base" 
  }
```
`/views/notes/notes.json`
### CSS stylesheets
```html
<head>
   <link href="/assets/css/style.css" rel="stylesheet"> 
</head>
```
`/views/_layouts/base.njk`
### Permalink (příklad)
```yaml
---
permalink: "/index.html"
---
```


