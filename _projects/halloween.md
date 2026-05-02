---
layout: project
title: "Halloween Parade Costumes"
description: "Costumes for the annual Village Halloween Parade in NYC."
tech: [Papercraft, Sewing, Inflatables]
status: "🟢 Ongoing"
featured: true
panels:
- title: Foam and Paper Mache
  description:
  - A 9ft tall replica of Carol from the movie of Where the Wild Things are. Made of paper mache, foam, fur and feathers. I made an Instructable for this costume, as if anyone would want to make their own.
  - Jake the Dog from Adventure Time. Foam structure with felt skin.
  links:
    - url: https://www.instructables.com/Carol-from-Where-the-wild-things-areMovie-Co
      text: Instructables Guide
  images:
  - path: assets/images/halloween/carol_max.jpg
    alt: Getty Images photo of the 2008 parade, featuring Max and a wild thing
  - path: assets/images/halloween/foam.JPG
    alt: Paper mache and foam built
  - path: assets/images/halloween/feathers.JPG
    alt: Fur and feathers added
  - path: assets/images/halloween/carol.jpg
    alt: Final look, with Max
  - path: assets/images/halloween/jake_the_dog.jpg
    alt: Jake the Dog costume, with Finn
- title: Fabric and Sewing
  description:
  - Sewed costumes for Tenzin, Milo and an Equalist from Avatar The Legend of Korra.
  - Cat in the Hat
  - Man in the Big Yellow Hat and Curious George. At the time I could not find yellow pants and shirt anywhere, so I had to sew the whole thing from scratch.
  - Hannibal Lecter.
  - A couple of different spidermans from different parts of the spiderverse. Spider webs and logos are stencilled in silicon caulk, which is extrmely high risk/high reward.
  - Number 5 and Delores from The Umbella Academy.
  - Ice King from Adventure Time.
  images:
  - path: assets/images/halloween/tenzin.jpg
    alt: Tenzin and Milo costumes
  - path: assets/images/halloween/equalist.jpg
    alt: Equalist
  - path: assets/images/halloween/milo.jpg
    alt: Equalist and Milo
  - path: assets/images/halloween/cat_hat.jpg
    alt: Cat in the Hat costume
  - path: assets/images/halloween/curious_george.jpg
    alt: Curious George and the Man in the Big Yellow Hat
  - path: assets/images/halloween/lecter.jpg
    alt: Hannibal Lecter. The material for the straight jacket is a canvas drop cloth.
  - path: assets/images/halloween/spider_king.jpg
    alt: Spider King. He's from another part of the spiderverse...
  - path: assets/images/halloween/dolores.jpg
    alt: Number 5 (with Delores) from the Umbrella Academy
  - path: assets/images/halloween/ice_king.jpg
    alt: Ice King and Finn from Adventure Time.
- title: Inflatables
  description: Inflatable costumes are the solution to "how do I transport this giant thing on the subway?" and "how do I store this?". The first of these are adapted from inflatable sumo suits, later ones are sewed from kite fabric.
  images:
  - path: assets/images/halloween/snorlax.jpg
    alt: Progress shot building inflatable Snorlax
  - path: assets/images/halloween/jigglypuff.jpg
    alt: Inflatable Jigglypuff (plus Ash Ketchum)
  - path: assets/images/halloween/popsicle.jpg
    alt: Inflatable raimbow ice pop
  - path: assets/images/halloween/animoto_logo.png
    alt: Inflatable Animoto logo costume
- title: Pepakura
  description: Pepakura is the art of making 3D models out of paper. It's a great way to make a large number of pieces, or to make and cut out kits that other people can assemble.
  images:
  - path: assets/images/halloween/cat_heads.jpg
    alt: Papercraft cat heads
  - path: assets/images/halloween/plague_doctor.jpg
    alt: Plague doctors
  - path: assets/images/halloween/cat_heads2.jpg
    alt: Papercraft cat heads
---

The East Village Halloween Parade is (in my humble opinion) the greatest place to spend October 31st. Every year I'm much too insane to document these properly, but here are some of the highlights.


{% for panel in page.panels %}
  {% include multi_image_panel.html
    title=panel.title
    description=panel.description
    images=panel.images
    links=panel.links
  %}
{% endfor %}
