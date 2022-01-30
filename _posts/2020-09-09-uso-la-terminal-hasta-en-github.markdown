---
layout: post
title: Uso la terminal hasta en github
date: 2020-09-09 10:00:00 +0300
description: Cuando empecé a usar entornos Linux me encantó su terminal, su potencia, versatilidad, rapidez, entre otras características. Razón por la cual siempre intentaré buscar una solución por línea de comandos y no por el entorno gráfico. 
img: uso-la-terminal-hasta-en-github.webp
img-cover: uso-la-terminal-hasta-en-github-cover.webp
tags: [github, git, terminal, cli]
category: Tecnología
---

Cuando empecé a usar entornos Linux me encantó su terminal, su potencia, versatilidad, rapidez, entre otras características. Razón por la cual siempre intentaré buscar una solución por línea de comandos y no por el entorno gráfico. 

En esta ocasión os contaré mi último descubrimiento. En realidad la instalé por recomendación de <a href="https://twitter.com/dant3dmc" target="blank">@dant3dmc</a>. Hablo de “GitHub CLI”, la herramienta oficial para línea de comandos de Github (¡claro!). Actualmente está en su versión beta y disponible solo para github.com, no para repositorios self hosted o “GitHub Enterprise Server”, según fuentes oficiales estas opciones estarán disponibles en un futuro.

La instalación es sencilla y está muy bien explicada en el README del proyecto en github así que no me detendré en este punto.

Lo que voy a detallar es cómo se crea un PR desde la herramienta, como ejemplo de su uso: 

1. Tener una rama diferente a master con commits, para nuestro ejemplo usaremos una con el nombre “20200909_uso-la-terminal-hasta-en-github” que es la rama que usaré para subir este artículo al blog.

   <div class="center-text"><img src="https://i.ibb.co/MPTv0Hm/giphy.webp" alt="mind blow!" border="0"></div>

2. Hay que ejecutar el siguiente comando: 

    <div class="center-text"><img alt="gh pr create" src="{{site.baseurl}}/assets/images/blog/uso-la-terminal-hasta-en-github-2.webp" /></div>

    En mi caso, el repositorio es un fork de otro por lo que tengo que especificar el repositorio en el cual quiero hacer el PR, luego solo hay que rellenar lo que nos va pidiendo la terminal hasta llegar al punto donde nos pregunta qué queremos hacer. 

3. Desde este punto, podemos terminar (“Submit”), cancelar (“Cancel”), continuar la creación desde el navegador (“Continue in browser”) o más interesante agregar todos los datos adicionales que nos faltan, como puede ser los “Reviewers”, “Assignees”, etc. 

    <div class="center-text"><img alt="add metatags github cli" src="{{site.baseurl}}/assets/images/blog/uso-la-terminal-hasta-en-github-3.webp" /></div>

    Para el ejemplo vamos a agregar algún “Reviewer”, las opciones se seleccionan con la tecla “espacio” porque se pueden hacer varias selecciones simultáneas y, para terminar, procedemos con el “Enter”. 

4. Seleccionamos el/los “Reviewers” y damos a”Enter” para continuar.

En este punto solo tenemos la opción de Completar (“submit”) para terminar el proceso.

Al completarlo la herramienta nos dará la URL del PR recién creado.

<div class="center-text"><img alt="resultado pull request" src="{{site.baseurl}}/assets/images/blog/uso-la-terminal-hasta-en-github-4.webp" /></div>

Este es solo un ejemplo de la potencia que tiene la herramienta “GitHub CLI” que mejora constantemente. Actualmente podemos interactuar con los Pull Request, las issues y repositorios casi en todas sus casuísticas. 

Como soy un friki de la consola, este tipo de herramientas me alegran y facilitan mi día y espero que a vosotros también.
