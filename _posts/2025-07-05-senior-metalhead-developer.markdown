---
layout: post
title: Senior Metalhead Developer
date: 2025-07-04 10:00:00 +0300
description:
  No recuerdo exactamente cuando fue el momento en que me empecé a escuchar música y tampoco me recuerdo escuchando nada
  diferente al género que más me gusta, el **METAL** 🤘
img: senior-metalhead-developer.webp
img-cover: senior-metalhead-developer.webp
tags: [ metal,música,conciertos ]
category: IRL
---

No recuerdo exactamente cuando fue el momento en que me empecé a escuchar música y tampoco me recuerdo escuchando nada
diferente al género que más me gusta, el **METAL** 🤘.

El proceso de descubrimiento músical siempre va de los más mainstream o lo más extremo, yo no sería la excepción. El
primer album original que recuerdo haber tenido fue el "Californication" (1999) de Red hot Chilli Peppers y lo compré
con algún dinero que me regalaron un mi cumpleaños.

En esa época la forma de encontrar música era a través de un rudimentario internet a traves de AudioGalaxy, Napster,
etc. (P2P) u otros medios más convencionales, la radio o la TV (MTV, cuando era bueno). Soñaba con ver a mis bandas
favoritas en vivo y aunque asistí a varios festivales gratuitos, el cartel nunca fue completamente de mi agrado.

Para ser sincero no recuerdo cuál fue mi primer concierto y justamente por eso hoy quiero compartir una línea de tiempo
con todos los concierto a los que he asistido:

<div class="timeline" id="timeline">
  <!-- Aquí JS insertará los eventos -->
</div>

<script>
  const events = [
    {
      name: "Rock Fest Barcelona 2025",
      date: new Date("2025-06-26T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20250626-rock-fest-barcelona.webp",
      type: "festival",
    },    
    {
      name: "Eluveitie + Amorphis + Dark Tranquility + Nailed To Obscurity",
      date: new Date("2022-11-17T15:30:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20221117-eluveitie-amorphis.jpg",
      type: "concert",
    },
    {
      name: "Saurom",
      date: new Date("2023-10-07T10:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20231007-saurom.jpg",
      type: "concert",
    },
    {
      name: "Tierra Santa",
      date: new Date("2025-04-12T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20250412-tierra-santa.webp",
      type: "concert",
    },
    {
      name: "Tierra Santa",
      date: new Date("2013-03-15T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20130315-tierra-santa.jpg",
      type: "concert",
    },
    {
      name: "Gigatron",
      date: new Date("2017-06-02T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20170602-gigatron.jpg",
      type: "concert",
    },
    {
      name: "Rhapsody + Beast In Black + Scarlet Aura",
      date: new Date("2018-03-18T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20180320-rhapsody.jpg",
      type: "concert",
    },
    {
      name: "Powerwolf + Beast In Black + Serenity",
      date: new Date("2016-04-03T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20160403-powerwolf.webp",
      type: "concert",
    },
    {
      name: "Sabaton + Apocalyptica + Amaranthe",
      date: new Date("2020-02-04T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20200204-sabaton.jpg",
      type: "concert",
    },
    {
      name: "Therion + Imperial Age",
      date: new Date("2018-02-25T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20180225-therion.jpg",
      type: "concert",
    },
    {
      name: "Iron Maiden",
      date: new Date("2009-03-07T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20090307-ironmaiden.jpg",
      type: "concert",
    },
    {
      name: "Kiss",
      date: new Date("2009-04-11T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20090411-kiss.jpeg",
      type: "concert",
    },
    {
      name: "Metallica",
      date: new Date("2010-03-10T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20100310-metallica.jpg",
      type: "concert",
    },
    {
      name: "Dark Tranquillity",
      date: new Date("2005-05-19T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20050519_dark-tranquillity.jpg",
      type: "concert",
    },
    {
      name: "Therion",
      date: new Date("2004-08-22T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20040722-therion.jpg",
      type: "concert",
    },
    {
      name: "Therion",
      date: new Date("2010-10-09T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20101009-therion.webp",
      type: "concert",
    },
    {
      name: "Lacrimosa",
      date: new Date("2010-10-07T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20101007-lacrimosa.jpg",
      type: "concert",
    },
    {
      name: "Nightwish",
      date: new Date("2004-12-08T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20041208-nightwish.jpg",
      type: "concert",
    },
    {
      name: "Lacuna Coil",
      date: new Date("2010-06-12T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20100612-lacuna-coil.jpg",
      type: "concert",
    },
    {
      name: "Angra",
      date: new Date("2010-05-16T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20100516-angra.jpg",
      type: "concert",
    },
    {
      name: "Angra",
      date: new Date("2007-05-13T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20070513-angra.jpg",
      type: "concert",
    },
    {
      name: "Metallica + Ghost",
      date: new Date("2019-05-05T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20190505-metallica.webp",
      type: "concert",
    },
    {
      name: "Epica",
      date: new Date("2008-09-13T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20080913-epica.jpg",
      type: "concert",
    },
    {
      name: "Stratovarius + Amaranthe + Seven Kingdoms",
      date: new Date("2013-04-05T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20130405-stratovariuos.jpg",
      type: "concert",
    },
    {
      name: "Children of Bodom + Decapitated + Medeia",
      date: new Date("2013-10-26T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20131026-children-of-bodom.jpg",
      type: "concert",
    },
    {
      name: "God Save The Queen",
      date: new Date("2014-10-24T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20141024-god-save-the-queen.jpg",
      type: "concert",
    },
    {
      name: "Tierra Santa",
      date: new Date("2014-12-27T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20141227-tierra-santa.webp",
      type: "concert",
    },
    {
      name: "Avantasia",
      date: new Date("2016-03-11T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20160311_avantasia.jpg",
      type: "concert",
    },
    {
      name: "Rhapsody",
      date: new Date("2001-07-22T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20010722-rhapsody.jpg",
      type: "concert",
    },
    {
      name: "Amon Amarth",
      date: new Date("2009-05-14T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20090514-amon-amarth.jpg",
      type: "concert",
    },
    {
      name: "Kamelot + Xandria + Triosphere + Blackguard",
      date: new Date("2012-11-11T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20121111-kamelot.jpg",
      type: "concert",
    },
    {
      name: "Helloween + Gammaray + Shadowside",
      date: new Date("2013-02-28T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20130228-helloween.jpg",
      type: "concert",
    },
    {
      name: "Dark Moor + Sinheresy + Mindfeeder + Menzia",
      date: new Date("2014-02-21T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20140221-dark-moor.webp",
      type: "concert",
    },
    {
      name: "Dragonforce",
      date: new Date("2009-05-19T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20090519-dragonforce.jpg",
      type: "concert",
    },
    {
      name: "Judas Priest",
      date: new Date("2009-11-03T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20081103-judas-priest.jpg",
      type: "concert",
    },
    {
      name: "Belphegor + God Dethroned + Elexorien",
      date: new Date("2009-09-20T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20090920-belphegor.jpg",
      type: "concert",
    },
    {
      name: "Testament",
      date: new Date("2008-05-25T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20080525-testament.jpg",
      type: "concert",
    },
    {
      name: "Iron Maiden",
      date: new Date("2008-02-28T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20080228-iron-maiden.webp",
      type: "concert",
    },
    {
      name: "Kreator + Exodus",
      date: new Date("2009-10-11T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20091011-kreator.jpg",
      type: "concert",
    },
    {
      name: "Mägo de Oz + Rata Blanca + Kraken",
      date: new Date("2009-10-11T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20041128-mago-de-oz.jpg",
      type: "concert",
    },
    {
      name: "Wacken Open Air 2015",
      date: new Date("2015-07-30T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20150730-wacken.jpg",
      type: "festival",
    },
    {
      name: "Rock Fest Barcelona 2014",
      date: new Date("2014-07-04T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20140704-rock-fest-barcelona.webp",
      type: "festival",
    },
    {
      name: "Rock Fest Barcelona 2015",
      date: new Date("2015-07-23T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20150723-rock-fest-barcelona.webp",
      type: "festival",
    },
    {
      name: "Rock Fest Barcelona 2016",
      date: new Date("2016-07-15T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20160715-rock-fest-barcelona.webp",
      type: "festival",
    },
    {
      name: "Rock Fest Barcelona 2017",
      date: new Date("2017-06-30T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20170630-rock-fest-barcelona.webp",
      type: "festival",
    },
    {
      name: "Rock Fest Barcelona 2018",
      date: new Date("2018-07-05T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20180705-rock-fest-barcelona.webp",
      type: "festival",
    },
    {
      name: "Rock Fest Barcelona 2022",
      date: new Date("2022-06-30T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20220630-rock-fest-barcelona.webp",
      type: "festival",
    },
    {
      name: "Rock Fest Barcelona 2024",
      date: new Date("2024-07-07T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20240707-rock-fest-barcelona.webp",
      type: "festival",
    },
    {
      name: "Sonisphere",
      date: new Date("2013-06-01T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20130601-sonisphere.webp",
      type: "festival",
    },
    {
      name: "Leyendas del Rock 2013",
      date: new Date("2013-08-08T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20130808-leyendas-del-rock.png",
      type: "festival",
    },
    {
      name: "Leyendas del Rock 2015",
      date: new Date("2015-08-05T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20150805-leyendas-del-rock.jpg",
      type: "festival",
    },
    {
      name: "Leyendas del Rock 2016",
      date: new Date("2016-08-10T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20160810-leyendas-del-rock.jpg",
      type: "festival",
    },
    {
      name: "Leyendas del Rock 2017",
      date: new Date("2017-08-09T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20170809-leyendas-del-rock.jpg",
      type: "festival",
    },
    {
      name: "Leyendas del Rock 2018",
      date: new Date("2018-08-08T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20180808-leyendas-del-rock.jpg",
      type: "festival",
    },
    {
      name: "Leyendas del Rock 2022",
      date: new Date("2022-08-03T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20220803-leyendas-del-rock.jpg",
      type: "festival",
    },
    {
      name: "Leyendas del Rock 2024",
      date: new Date("2024-08-07T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20240807-leyendas-del-rock.jpg",
      type: "festival",
    },
    {
      name: "Hellfest 2016",
      date: new Date("2016-06-20T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20140620-hellfest.jpg",
      type: "festival",
    },
    {
      name: "Metaldays 2013",
      date: new Date("2013-07-21T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20130721-metaldays.webp",
      type: "festival",
    },
    {
      name: "Rock al Parque 2011",
      date: new Date("2011-06-01T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20110601-rock-al-parque.jpg",
      type: "festival",
    },
    {
      name: "Rock al Parque 2010",
      date: new Date("2010-07-03T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20100703-rock-al-parque.jpg",
      type: "festival",
    },
    {
      name: "Rock al Parque 2009",
      date: new Date("2009-06-27T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20090627-rock-al-parque.jpg",
      type: "festival",
    },
    {
      name: "Rock al Parque 2008",
      date: new Date("2008-11-01T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20081101-rock-al-parque.jpg",
      type: "festival",
    },
    {
      name: "Rock al Parque 2006",
      date: new Date("2006-10-14T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20061014-rock-al-parque.jpg",
      type: "festival",
    },
    {
      name: "Rock al Parque 2005",
      date: new Date("2005-10-15T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20051015-rock-al-parque.jpg",
      type: "festival",
    },
    {
      name: "Rock al Parque 2004",
      date: new Date("2004-10-30T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20041030-rock-al-parque.jpg",
      type: "festival",
    },
    {
      name: "Nargaroth",
      date: new Date("2009-04-26T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20090426-nargaroth.jpg",
      type: "concert",
    },
    {
      name: "Congregation Fest 3",
      date: new Date("2010-05-22T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20100522-congregation-fest-3.jpeg",
      type: "festival",
    },
    {
      name: "Metalmania Colombia 2007",
      date: new Date("2007-06-30T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20070630-metalmania.jpeg",
      type: "festival",
    },
    {
      name: "Evocación A Símbolos del Rock Nacional",
      date: new Date("2006-11-19T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20061119-evocacion.jpg",
      type: "festival",
    },
    {
      name: "After Forever",
      date: new Date("2005-07-06T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20050706-after-forever.jpg",
      type: "concert",
    },
    {
      name: "Destruction",
      date: new Date("2006-04-14T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20060414-destruction.jpg",
      type: "concert",
    },
    {
      name: "Rata Blanca + Krönös",
      date: new Date("2004-07-31T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/image-not-found.jpg",
      type: "concert",
    },
    {
      name: "Tierra Santa",
      date: new Date("2024-01-12T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20240112-tierra-santa.jpg",
      type: "concert",
    },
    {
      name: "Rafael Bittencourt",
      date: new Date("2008-12-06T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/image-not-found.jpg",
      type: "concert",
    },
    {
      name: "Metalmania Colombia 2006",
      date: new Date("2006-06-24T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/image-not-found.jpg",
      type: "festival",
    },
    {
      name: "Dark Tranquillity",
      date: new Date("2008-06-16T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/image-not-found.jpg",
      type: "concert",
    },
    {
      name: "The Offspring",
      date: new Date("2004-10-29T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20041029-the-offspring.jpg",
      type: "concert",
    },
    {
      name: "Magö de Oz",
      date: new Date("2004-03-21T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/image-not-found.jpg",
      type: "concert",
    },
    {
      name: "Sagar Fest",
      date: new Date("2009-12-04T00:00:00"),
      image: "/assets/images/blog/senior-metalhead-developer/20091204-sagarfest.jpg",
      type: "concert",
    }
  ].sort((a, b) => new Date(a.date) - new Date(b.date));

  function formatDateYMD(date) {
    const y = date.getFullYear();
    const m = String(date.getMonth() + 1).padStart(2, '0');
    const d = String(date.getDate()).padStart(2, '0');
    return `${y}-${m}-${d}`;
  }

  const timeline = document.getElementById("timeline");

  events.forEach(event => {
    const el = document.createElement("div");
    el.className = "event " + event.type;
    el.innerHTML = `
      <div class="event-content">
        <img loading="lazy" class="expandible" src="${event.image}" alt="${event.name}">
        <div class="event-details">
          <h3>${event.name}</h3>
          <time>${formatDateYMD(event.date)}</time>
        </div>
      </div>
    `;
    timeline.appendChild(el);
  });
</script>




<script type="text/javascript">

document.addEventListener("DOMContentLoaded", function () {
  
 const modal = document.getElementById("modal");
const modalImg = document.getElementById("modal-img");

  // Al hacer click en cualquier imagen con clase "expandible"
  document.addEventListener("click", function(e) {
    if (e.target.classList.contains("expandible")) {
      modalImg.src = e.target.src;
      modal.classList.add("show");
    } else if (e.target === modal) {
      modal.classList.remove("show");
    }
  });

  // Cerrar con tecla ESC
  document.addEventListener("keydown", function(e) {
    if (e.key === "Escape") {
      modal.classList.remove("show");
    }
  });

  });

function formatDateToYMD(date) {
  const year = date.getFullYear();
  const month = String(date.getMonth() + 1).padStart(2, '0'); // Mes comienza en 0
  const day = String(date.getDate()).padStart(2, '0');

  return `${year}-${month}-${day}`;
}

</script>

<div class="image-modal" id="modal">
  <img id="modal-img" src="" alt="Afiche ampliado">
</div>