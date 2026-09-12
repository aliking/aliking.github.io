---
layout: project
title: "Big Red Button"
description: "Prototyped spectacular installation for product launch"
tech: [Arduino, IOT, WebSockets, Vanilla JavaScript, PVC]
status: "🟠 Prototype"
link: "https://github.com/aliking/confetti_cannon"
featured: true
panel:
  images:
  - path: assets/media/big-red-button/thismachinekillsfascists.png
    alt: This confetti cannon kills fascists
  - path: assets/media/big-red-button/confetti.png
    alt: Confetti from the cannon
  - path: assets/media/big-red-button/cannon.jpg
    alt: The confetti cannon prototype
---

Prototype installation for a deliberately elaborate product launch. The orginal spec was something like: "Something spectacular for the Facebook Live launch. A big red button or a confetti cannon".

{% include multi_image_panel.html
    images=page.panel.images
  %}

The final product was much more restrained than the prototype: just a pneumatic confetti cannon, fired remotely over the internet. There was a _quite_ large red button.


However, initially, there was a vision.
{% page_asset image controlbox.png alt="The control box for the launch system" %}
A control box (with a big red button), two key switches and a status light, all hooked up to a particle.io microcontroller. The microcontroller could register events from the controls and set the status light.

{% page_asset image panel.png alt="Display panel" %}
A retro inspired status display with a main information panel surrounded by technical looking nonsense. This is unfinished in prototype form, but each of the sections could have had different important looking status updating. This is scaled to look good at 4:3 and be displayed on a large CRT monitor using a raspberry pi.

The display panel is a web page that uses websockets to update it remotely, so that the panel can be loaded, and then react to events from the control box. It's a fairly fragile system, the server has an internal state machine and is waiting for events in a particular sequence from the control box.

The web server also serves a backup control panel, so that if the control box fails, the events can still be triggered using a phone or laptop.

This video shows the prototype in action using the web backup controls. The controls correspond to control box switches:
 * 0000 - Turn the small key
 * 1100 - Turn the big key ( this triggers twice, turning in the other direction)
 * 1110 - Unlock the big red button
 * 1111 - Press the big red button

<video style="width: 100%; height: auto;" controls muted>
  <source src="{{ '/assets/media/big-red-button/display_panel.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

