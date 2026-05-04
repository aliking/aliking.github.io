---
layout: project
title: "Card Stack Challenge App"
description: "A physical computing challenge and app for recruiting fairs"
tech: [Ruby, Sinatra, Heroku, Punchcards]
status: "🟢 Archive"
link: "https://github.com/aliking/card_stack"
featured: true
---

I got interested in [Edge-notched cards](https://en.wikipedia.org/wiki/Edge-notched_card): a system for encoding data in physical cards with holes and notches at the edges.

We were running a table at a recruiting fair, and I thought this could be a way to attract the kind of candidates who might find this a weird and fun challenge.
{% picture "/assets/media/card_stack/back.jpg" alt="The back of a card, showing the notches and holes" %}
Back of a card, with explaination. The circles along the edges were pre-punched, so it was easy enough for a candidate to rip along the lines to create a notch. As the example says, if we get a stack of cards back and we want all the card with github profiles, we insert a needle through all of the github holes and lift out any cards that are not notched. Any cards remaining were notched and therefore have github profiles.

{% picture "/assets/media/card_stack/front.jpg" alt="The front of a card, showing the punchcard holes and challenge instructions" %}

The other side of the card had this obscure challenge which... honestly was a bit too obscure.

This is what someone attempting this would have to work out:
1. The sorting procedure itself, writte in weird pseudocode. Basically, given a stack of the cards, you insert a needle through all of them at hole 1, lift out and cards that will come, and put them all at the front. Then you repeat for hole 2, then hole 3, etc.
2. In order for that to sort the cards, lower numbers must get lifted out and put to the front _more_ that higher numbers. 0, the first card, must be lifted out the most - it must get lifted out every time, so it must have NO NOTCHES. A theoretical last card in the stack has every hole notched, so it never gets lifted out and always stays at the back.
3. Then the key insight is that the holes and notches are binary digits. Hole = 0, Notch = 1.
4. Then you just convert the number on the card to binary, and notch the holes that correspond to 1s. This card, 31, is `11111` in binary, so it should have the first 5 holes notched.

All that while walking around a recruiting fair? Yeah, it was a bit much.

This also came with a companion web app to test if a card was punched correctly, so that anyone at the table could quickly check if a card had the right answer. The app was deployed to Heroku, and took a target number in the url. It just converted the number to a series of needle instructions. Given a stack of cards, if you followed the instructions and the card was notched correctly, it should be the only card left at the end.

`<app url>/31`
{% picture "/assets/media/card_stack/app.png" alt="Screenshot of the app, showing the instructions for card 31" %}
