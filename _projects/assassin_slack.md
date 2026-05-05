---
layout: project
title: "Assassin Slack webhook"
description: "A Slack slash command for anonymous taunting during an office assassin game."
tech: [Go, Slack API, Heroku]
status: "🟢 Archive"
link: "https://github.com/aliking/assassin-slack"
featured: true
---

I organized an office assassins game. If you're not familiar: all players are assassins. Each person is assigned one of the other players as a target, and their goal is to "assassinate" their target (the rules around this were elaborate, but it was something like - catch the alone without witnesses and hit them with a ball-pit ball). Once a player successfully assassinates their target, they get their target's target as their new target. Eventually there is only one player left, and they are the winner.

I wanted place for gossip, smacktalk and game updates, and that was the Slack channel #assassins. This project is effectively a Slack bot that listens for a registered / command message and then relays the message under an alias to the channel.

Registered players each had an alias name and an avatar. When one of them used the slash command, the bot would post their message with their alias and avatar. When I used it, it would post as 'The Director' and if anyone else used it, it would post as 'Civilian'.

{% picture "/assets/media/assassin_slack/citizen.png" alt="Example of a message posted by the bot as 'Civilian'" %}
