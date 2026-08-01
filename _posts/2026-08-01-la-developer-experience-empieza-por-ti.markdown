---
layout: post
title: La “Developer Experience” empieza por TI
date: 2026-08-01 10:00:00 +0300
description: 'La eficiencia no es solo usar la IA, el uso de las herramientas correctas puede marcar la diferencia.'
img: la-developer-experience-empieza-por-ti.webp
img-cover: la-developer-experience-empieza-por-ti-cover.webp
tags: [ Developer ]
category: Desarrollo de Software
---

Llevo años escuchando a equipos, departamentos y empresas hablar de cómo mejorar la “Developer Experience”, para quienes
no sepan qué es, os pongo la definición moderna:

<blockquote class="blockquote mt-3 p-3">
    <p class="text-muted mb-0 font-italic">
    "Developer Experience refers to the lived experience of developers as they interact with the tools, processes, and 
    environment necessary to build software."
<br/>
<br/>
— ACM / DX Core Framework
</p>
</blockquote>

La definición intenta englobar problemáticas que van desde el trato con las personas de negocio hasta el entorno donde
ocurren estas interacciones durante el proceso de creación de software. Hay un punto en el cual cada desarrollador tiene
el control total, hablo del uso de la herramienta fundamental a la hora de desarrollar software (no es la IA, se que
muchos esperaban que fuera esa), hablo de tu máquina local.

Dominar el entorno de desarrollo que usas día tras día es posiblemente donde menos atención se presta y donde se pierde
más tiempo. No voy a entrar a discutir la tecnología usar, porque es un tema que no ayuda a nadie, pero lo que sí voy a
enfatizar es que hay que buscar siempre: el mejor y más eficiente uso.

Después de estar presente en cientos de horas de desarrollo puedo enfatizar que los siguientes puntos son los que
encuentro más críticos y simples de optimizar:

### Ausencia en el uso de atajos de teclado:

Todo sistema operativo e IDEs cuentan con cientos de atajos que permiten hacer tareas de forma eficiente (si no, quizás
sea hora de cambiar). Por ejemplo, formatear una clase, crear una interfaz e implementar el esqueleto, eliminar
“imports” no usados, etc. Son procesos que deberían tomar segundos, pero si en cambio tienes que buscar estás opciones
en los menús, que no suelen estar fácilmente accesibles y pierdes dos o tres minutos, a la larga, serán horas perdidas a
nivel de productividad.

Para Mac por ejemplo, existe una aplicación que convierte el “Bloq Mayús” (tecla que no sé por qué existe aún) en una
tecla mágica con la cual puedes jugar y tener todo un conjunto de atajos asociados, por debajo lo que hace es simular
que estás presionando ctrl + command + option + function (casi imposible de hacerlo con una mano) por lo que no existen
conflictos con atajos pre-existentes. La aplicación se llama [Hyperkey](https://hyperkey.app/){:target="_blank" rel="noopener"}.

En mi caso, he configurado esta nueva tecla para organizar mis ventanas (usando otro programa que citaré más adelante):

<div class="center-text">
    <img height="600px" alt="Atajos de teclado" src="{{site.baseurl}}/assets/images/blog/la-developer-experience-empieza-por-ti-1.webp" />
</div>
<br/>
Llegados a este punto el límite es tu imaginación.

### Uso excesivo del ratón (o peor, del panel táctil).

El ratón posiblemente es el mejor periférico jamás creado cuando tienes que realizar tareas que no tengan que ver con
escribir, lamentablemente, los desarrolladores basamos nuestro trabajo en la escritura, por lo que cada momento que
gastas moviendo tu mano al ratón es tiempo que pierdes, todo lo que tienes que hacer en tu día seguramente se puede
hacer con el teclado de forma más eficiente, si no es el caso, es porque el primer punto citado arriba no se está
cumpliendo.

Por ejemplo, IntelliJ IDEA (IDE para java de Jetbrains) tiene un panel para mostrar los archivos del proyecto, el típico
explorador en forma de árbol. Hay personas que cada vez que quieren ocultarlo usan el ratón para hacer click en el guión
que colapsa la sección y para desplegarlo de nuevo hacen clic en el ícono. Este gesto parece insignificante pero si lo
haces doscientas veces en un día, deja de serlo.

La solución es simplemente usar el atajo de teclado cmd + 1 (en el caso de Mac).

### Falta de herramientas que ayudan con procesos cotidianos: gestor de portapapeles, gestor de contraseñas, gestor de ventanas, entre muchos otros.

Este punto lo puedo reducir a un nombre si eres usuario de Mac (también hay versión para Windows): [Raycast](https://www.raycast.com/){:target="_blank" rel="noopener"}

Mac tiene un lanzador de aplicaciones y búsqueda de archivos que es de lo peor que he visto (Spotlight) y trata de
complementar al “Finder”, que es el gestor de archivos, que también es terrible y al final tienes un sistema cojo
ayudando a otro ciego.

Raycast es un programa que transforma el “Spotlight” en algo útil, tiene todo un sistema de manejo de ventanas, gestor
de portapapeles, incluso puedes crear scripts para automatizar tareas en varios lenguajes, notación de texto
reemplazables (por ejemplo: si escribes #tarea automáticamente te reemplaza eso por una plantilla de texto para la
creación de una tarea), en realidad las opciones son ilimitadas, ya que tiene un sistema de plugins para extenderlo.

Hay en el mercado otras opciones similares, pero lo importante es que uses alguna que te solucione estas limitaciones y
agilice estos procesos.

### Uso de herramientas de comunicación ineficientes.

Todas las herramientas para realizar reuniones permiten compartir pantalla, enviar archivos, tener conversaciones, etc,
por lo que doy por sentado estas funcionalidades como las mínimas en una herramienta de comunicación.

Nosotros, en SEAT CODE, acostumbramos a hacer por defecto programación en parejas o “pair programming” y no hay nada más
cómodo que la herramienta de comunicación que usamos tenga como mínimo la capacidad de realizar anotaciones en la
pantalla del “driver” de la sesión, esto ahorra mucho tiempo cuando hay que señalar puntos concretos y no hay que
describirlos y localizarlos usando el lenguaje.

Cito esta característica porque curiosamente, no es muy común. Solo conozco dos herramientas que la tienen de fábrica:
Zoom y los “huddles” de Slack.

#### Conclusión

Probablemente, para cada caso particular existan otros puntos que se puede mejorar, la idea de este artículo es dar
ejemplos comunes donde se pierde eficiencia por el uso inadecuado o ausencia de las herramientas disponibles e intentar
fomentar ese espíritu crítico que producirá el cambio en la forma de trabajar mejor y mas a gusto.