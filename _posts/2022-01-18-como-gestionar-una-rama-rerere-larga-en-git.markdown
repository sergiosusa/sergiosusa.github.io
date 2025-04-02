---
layout: post
title: ¿Cómo gestionar una Rama Rerere-larga en Git?
date: 2022-04-18 10:00:00 +0300
description: Cuando empecé a usar entornos Linux me encantó su terminal, su potencia, versatilidad, rapidez, entre otras características. Razón por la cual siempre intentaré buscar una solución por línea de comandos y no por el entorno gráfico.
img: como-gestionar-una-rama-rerere-larga-en-git.webp
img-cover: como-gestionar-una-rama-rerere-larga-en-git-cover.webp
tags: [ git, rerere ]
category: Desarrollo de Software
---


Los proyectos de software de gran envergadura con cientos de desarrolladores aportando nuevos desarrollo y corrección de
“bugs” afrontan no solo retos a nivel de desarrollo. Hoy hablaré del gran olvidado, la gestión de GIT durante los
“releases” de versión de larga duración.

Imaginemos como escenario inicial una “feature branch”, que lleva un par de semanas siendo desarrollada con algunas
funcionalidades ya implementadas y una rama “master” donde se han ido subiendo correcciones y arreglos como se ve en el
siguiente gráfico:

<div style="width: 100%; text-align: center; margin-bottom: 1rem;" class="push-right"><img style="min-width: 350px;max-width: 700px; width: 100%;" alt="Ejemplo de long term branch" src="{{site.baseurl}}/assets/images/blog/como-gestionar-una-rama-rerere-larga-en-git-2.webp"/></div>

A este punto el cómo unir la “feature branch” a “master” sería fácil, aunque puede que tengamos que resolver unos
cuantos conflictos. Imaginemos ahora que la “feature” es un cambio estructural profundo y toma cerca de 10 meses en
completar, mientras la rama “master” sigue recibiendo actualizaciones y correcciones de errores.

Somos las personas encargadas de realizar el lanzamiento de la nueva versión y nos enfrentamos a un “merge” de 10 meses
de bifurcación entre las ramas. ¿Veis el problema que nos espera? Seguramente serán cientos de conflictos a arreglar, un
proceso extremadamente tedioso, aunque posible.

Ahora la pregunta sería: ¿Podemos evitar esta situación de alguna forma? La primera idea que nos viene a la cabeza sería
ir haciendo “merge” a la rama “master” en “feature” lo que ocasionará cientos de “commits” extras. La segunda sería ir
haciendo “rebase” sobre las ramas nombradas anteriormente, lo cual es totalmente inviable porque cambiaría la historia
pública, romperíamos la regla de oro de GIT.

Ya sin ideas es donde os traigo una buena noticia: GIT nos da una herramienta no muy conocida que simplifica este
escenario haciéndolo “trivial”.

La opción mágica —que no es tan mágica— se llama "reuse recorded resolution" más conocida por sus siglas “rerere”. Para
activarla hay que cambiar la siguiente configuración:

{% highlight bash %}
$ git config --global rerere.enabled true
{% endhighlight %}

Al activar esta opción GIT guardará y reutilizará las resoluciones de conflictos de forma automática, el procedimiento
entonces para arreglar la problemática planteada es:

- Unir ocasionalmente las ramas “features” y “master” (git merge)
- Resolver los conflictos (quedarán guardados).
- Revertir la unión de las ramas. ($ git reset --hard HEAD^)

Ahora imaginemos que es hora de hacer el merge final, siguiendo con el procedimiento normal, el rerere sería capaz de
aplicar las resoluciones antes realizadas durante meses y completar la que antes era una tarea interminable y riesgosa
en cuestión de minutos.




