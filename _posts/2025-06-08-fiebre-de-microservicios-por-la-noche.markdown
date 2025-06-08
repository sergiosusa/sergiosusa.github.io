---
layout: post
title: Fiebre de microservicios por la noche
date: 2025-06-08 10:00:00 +0300
description:
  Durante la Spring I/O del 2025 celebrada en Barcelona, en el curso de una entrevista, una preguntas me recordó uno de los conflictos más grandes que tiene la industria del desarrollo de software: ¿Monolito o microservicio?
img: fiebre-de-microservicios-por-la-noche.webp
img-cover: fiebre-de-microservicios-por-la-noche-cover.webp
tags: [ programación,microservicio,monolito ]
category: Desarrollo de Software
---

Durante la Spring I/O del 2025 celebrada en Barcelona, en el curso de una entrevista, una pregunta me recordó uno de
los conflictos más grandes que tiene la industria del desarrollo de software: ¿Monolito o microservicio?

Esa inocente pregunta me hizo rememorar cientos de horas que invertí en acaloradas discusiones sobre si era o no
necesario un nuevo microservicio. Teniendo solo una frase y un minuto para resumirlo todo, respondí con la vieja
confiable: "Depende” y lo complementé con otra frase lapidaria y ambigua: "Si nace de forma orgánica, entonces la
respuesta es microservicio”. La cara de la entrevistadora entre confundida y sorprendida me indicó que había sorteado el
dilema de forma elegante.

Regresando a la vida real, en el proyecto donde estoy actualmente en Seat Code, se han heredado cerca de veinticuatro
microservicios de dos equipos externos. En la transferencia de uno de ellos, los desarrolladores dijeron que muchos de
esos microservicios no debían haberse separado. Mi pregunta fue obvia: ¿porque entonces se separaron los microservicios?
Un silencio incómodo y miradas cruzadas terminaron en un: "porque era como se hacía”.

Aunque la teoría de los microservicios se remonta al 2005, su popularidad se alcanzó en el 2014 cuando James Lewis y
Martin Fowler escribieron el artículo [Microservices](https://martinfowler.com/articles/microservices.html). En aquel
momento se comenzó a utilizarse de forma desenfrenada. Ese hecho, me hizo pensar en la **Ley de Maslow:**

> "Si la única herramienta que tienes es un martillo, todo te parecerá un clavo.”

En un entorno de malas praxis y sistemas legado por doquier, este modelo arquitectural prometía el paraíso y, si ha esto
le sumamos la masificación de DDD, encontraremos una simple y mortal fórmula:

Bounded context = microservicio (no confundir con microservicio = Bounded context).

A partir de aquí, se perdió el control de la situación. Proyectos que antes eran un monolito, ahora son veinte
microservicios y un monolito.

<div class="center-text">
    <img height="200px" alt="shrek meme" src="{{site.baseurl}}/assets/images/blog/fiebre-de-microservicios-por-la-noche-1.webp" />
</div>
<br />

Entonces, ¿Están todos estos nuevos microservicios mal? La respuesta, es la esperada para todos los problemas complejos
y preguntas incomodas : “depende”.

Para llegar a una decisión argumentada, he creado una lista de preguntas para ayudar identificar si un microservicio
tiene sentido o no:

- ¿La existencia del microservicio ayudaría al escalabilidad de sistema?
- ¿La lógica de negocio del microservicio puede vivir separadamente del resto?
- ¿El microservicio necesita o no compartir base de datos? (si tiene)

(Para efectos prácticos del articulo voy a ignorar las limitaciones relacionadas con el equipo de desarrollo).

Ahora os contaré un caso real. Hace unos años estaba en una empresa que tenía su sistema de facturación dentro de un
ERP (EKON), generalmente, estos sistemas tienen unos modelos estándar para emitir facturas simples a proveedores y,
quizás a algunos clientes, pero en el caso de querer algo más complejo seguramente se tendrían que hacer algunos
movimientos circenses. Para que os hagáis una idea, la factura era de una comercializadora de electricidad, muchas
hojas, muchos gráficos, infinidad de letras pequeñas, varias tablas de resumen etc. Todo para cumplir la normativa
exigida por el gobierno (este es un sector fuertemente regulado).

La situación empezó a volverse crítica cuando el proceso de facturación se degradó hasta llegar a durar tres días para
completar un total de 300.000 facturas.

Lo primero fue analizar cual parte del proceso era el causante de la degradación: el cálculo de los datos, la creación
del PDF, la copia del PDF a un gestor de archivos o algún otro punto.

La respuesta fue, para mi sorpresa, la creación del PDF. Entré a las entrañas del ERP y me encontré con una magia arcana
muy antigua, como el sistema solo era capaz de crear una página por factura, lo que se hacía era crear N facturas y
luego unían lo trozos dando lugar al documento final, Facturastein.

<div class="center-text">
    <img height="200px" alt="shrek meme" src="{{site.baseurl}}/assets/images/blog/fiebre-de-microservicios-por-la-noche-2.webp" />
</div>
<br />

Claramente, se tenía que reemplazar esta pieza del proceso. A este punto existían dos soluciones: 1) agregar esta
funcionalidad al monolito o, 2) crear un microservicio de impresión de facturas (o documentos). A esta situación, se le
puede aplicar las tres preguntas que se han propuesto anteriormente:

- ¿La existencia del microservicio ayudaría al escalabilidad de sistema?
    - Definitivamente, la posibilidad de escalar horizontalmente y de tener el control del proceso garantiza este punto.
- ¿La lógica de negocio del microservicio puede vivir separadamente del resto?
    - Totalmente, solo tendría lógica de impresión.
- ¿El microservicio necesita o no compartir base de datos?
    - No comparte, porque no tiene.

El camino a seguir estaba claro. En este artículo no entraré en los detalles de la implementación, que seguro en algún
futuro cercano los contaré, lo que si diré es que fue un éxito rotundo en todo sentido.

El tiempo de facturación ya no eran tres días, eran seis horas con una sola máquina muy pequeña, no llegamos a bajarlo
más porque el cuello de botella estaba ahora en otro parte del sistema.

Volviendo al tema y, para concluir, lo importante a la hora de crear o no un microservicio es que sea a partir de una
necesidad y un análisis concienzudo y no porque está de moda, porque me gustan o porque quiero hacer uno para mi
currículum.
