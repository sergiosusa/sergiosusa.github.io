---
layout: post
title: Como automatizar procesos repetitivos e incómodos en el navegador
date: 2025-03-29 10:00:00 +0300
description: Han pasado años desde que empecé a usar los userscripts, primero, como hobby, al automatizar cosas que quería hacer en
  el navegador de forma diaria con el objetivo de simplificar su ejecución a un simple clic.
img: como-automatizar-procesos-repetitivos-e-incomodos-en-el-navegador.webp
img-cover: como-automatizar-procesos-repetitivos-e-incomodos-en-el-navegador-cover.webp
tags: [ programación,userscript,javascript ]
category: Desarrollo de Software
---

Han pasado años desde que empecé a usar los userscripts, primero, como hobby, al automatizar cosas que quería hacer en
el navegador de forma diaria con el objetivo de simplificar su ejecución a un simple clic o, agregando alguna funcionalidad
que yo creía que era indispensable. Pronto, me di cuenta de que esta herramienta es útil en entornos laborales, por este motivo, creo que
todos aquellos que usáis algún navegador podréis sacar provecho de esta tecnología.

Lo primero que tenéis que saber es que el lenguaje utilizado es javascript, por lo cual, la extensión de estos archivos
serán: `.user.js`, lo segundo, es instalar una extensión para que el contenido de estos archivos sean
inyectados. Acá os dejo una lista para los navegadores más usados:

- <a href="https://tampermonkey.net" target="_blank">Tampermonkey (Chrome)</a>
- <a href="https://www.greasespot.net" target="_blank">Greasemonkey (Firefox)</a>
- <a href="https://addons.opera.com/sk/extensions/details/violent-monkey/" target="_blank">Violent monkey (Opera)</a>

La idea detrás de la extensión es la inyección del script en las páginas donde se necesiten para que sean
ejecutadas luego de su carga.

Una vez instalado, se debe crear el primer userscript haciendo clic derecho en el icono de la extensión donde se
desplegará un menú contextual con la opción de "Agregar nuevo script...".

<div class="center-text">
    <img height="350px" alt="menú contextual del tampermonkey" src="{{site.baseurl}}/assets/images/blog/como-automatizar-procesos-repetitivos-e-incomodos-en-el-navegador-2.webp" />
</div>
<br />
Una nueva ventana se abrirá con un editor de texto y un modelo vacío del script.

``` javascript
// ==UserScript==
// @name         New Userscript
// @namespace    https://sergiosusa.com
// @version      0.1
// @description  try to take over the world!
// @author       You
// @match        https://sergiosusa.com
// @grant        none
// ==/UserScript==

(function() {
    'use strict';
    // Your code here...
})();
```

Explicaré detalladamente las dos partes que dividen este modelo:

1. Metadatos:
    - `@name`: nombre del script.
    - `@namespace`: un identificador único.
    - `@version`: versión del script, necesaría para lanzar actualizaciones.
    - `@description`: descripción corta de la funcionalidad del script.
    - `@author`: el autor del script.
    - `@match`: define en qué sitios se ejecutará el script.
    - `@grant`: indica que el script requiere o no permisos especiales.
2. Código principal:
    - `(function() { ... })();`: esto es una IIFE (Immediately Invoked Function Expression), es decir, una función que
      se ejecuta inmediatamente después de definirse. En este caso se ejecutará luego que finalice la carga de la
      página, aunque se puede modificar de ser necesario.
    - `'use strict'`: activa el modo estricto de JavaScript para prevenir errores comunes y malas prácticas.
    - `// Your code here... `: nuestro código empezará acá.

Para ejemplificar, a continuación se presenta un código muy simple reemplazando el comentario descrito anteriormente:

``` javascript
   const navbarBrand = document.querySelector(".navbar-brand img");
   if (navbarBrand) {
       navbarBrand.style.transition = "transform 0.8s ease";
       navbarBrand.style.transform = "rotate(180deg)";
   }
```

Si se guarda y ahora entras a la dirección que aparece en el tag `@match` la extensión mostrará un número en rojo, estos
son los scripts que han sido inyectados en la página actual.

Si probáis este ejemplo, veréis que he modificado, en este caso, el aspecto de uno de los elementos presentes en la
página web.

Desde ahora, el límite es la imaginación. Para ayudaros a ejemplificar el potencial que tienen estos scripts os pongo
otro caso práctico real:

✨ Steam Enhanced ✨
[![GitHub Repo](https://img.shields.io/badge/GitHub-Repo-black?style=for-the-badge&logo=github)](https://github.com/sergiosusa/steam-enhanced){:
target="_blank"}

Este script agrega botones, gráficas y algún comportamiento en el marketplace de videojuegos más famoso del mundo:
Steam.

No quiero repetirme explicando el código o que hace, esto lo podéis ver en la descripción y en el código del proyecto,
que es público.

Lo que sí quiero compartir y explicar es un esqueleto que he creado para organizar el código de los scripts basado en
las URLs, en la cuales, se inyectan elementos o comportamientos, yo recomiendo su uso, cuando:

- hay que inyectar comportamientos completamente diferentes en más de una página y requieran mucho código.
- se tienen que inyectar comportamientos que aplican a todo el sitio web junto con los scripts que se aplican a cada
  página de manera individual.

Si, por el contrario, son scripts sencillos y muy puntales, no creo que sea necesario utilizar ese extra de complejidad.

## Userscript Skeleton

[![GitHub Repo](https://img.shields.io/badge/GitHub-Repo-black?style=for-the-badge&logo=github)](https://github.com/sergiosusa/userscript-skeleton){:
target="_blank"}

- Función principal:
  ``` javascript
  
  (function () {
    'use strict';
    try {
        let siteImproved = new SiteImproved();
        siteImproved.render();
    } catch (exception) {
        alert(exception);
    }
   })();
  ```
  Crea una instancia de la clase/función `SiteImproved` que hereda de `Renderer` y llama al método `render` para empezar
  la inyección de código para ese sitio en concreto.
- Clase `SiteImproved` tiene dos atributos heredados de clase `Renderer` donde se tienen que declarar nuevas instancias
  de clases que hereden de `Renderable` (que se puede renderizar):
    - rendererList: Lista de clases que modificarán páginas específicas.
    - globalRenderList: Lista de funciones que se aplicarán globalmente.
- Clase `RenderableExampleFunction` hereda de `Renderable` por lo que hay que completar el atributo `handlePage`, con
  una expresión regular que concuerde con la(s) página(s) donde se ejecutará e implementar la función `render`, donde
  estará el código encargado de realizar las modificaciones.
- Clase `Renderer` tiene toda la lógica de renderización configurada en la clase que la hereda, en el ejemplo es la
  clase `SiteImproved`.
- Clase `Renderable` implementa la lógica para verificar que una clase se puede renderizar en una página concreta
  mediante una expresión regular.

Este diseño permite agregar múltiples funciones de renderizado sin modificar el código base de una forma modular y
organizada.

Resumiendo, el script está estructurado como un **marco de renderizado** (o **rendering framework**) que busca funciones
específicas para modificar la página y su propósito es organizar la ejecución de elementos visuales y lógicos en función
de ciertas reglas.
