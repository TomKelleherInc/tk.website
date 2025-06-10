---
layout: post
title: AI-Assisted Game Creation
description: >
  How I went too far, too fast...
image: /assets/img/blog/diagnostic-game.jpg
sitemap: false
---

Trying to use AI to assist me with coding a medical diagnostic game. Having huge fun with it, but I think I get why no one has made one for real life yet! {sad trombone}

The effort was to see what I could make that would be:
* Non-trivial
* As close to zero-keyboarding as I could manage (let the AI do the coding)
* Leverage Harper's database, pub/sub and possibly caching

Started with [Claude.ai](https://claude.ai), my first deep effort using it. I spent a lovely evening on the back porch with my wife while she read a book, and I chatted with Claude, getting the specs thought through. For me, it was a great brainstorming buddy -- though about on par with ChatGPT in that regard.

Hit a wall: After a while, Claude tells you "That prompt is too long." Couldn't get it to do anything. Much confusing and fussing. Discovered that Claude appends your whole conversation to each new prompt...so what you think is your teeny tiny next prompt is a *BIG HONKING PROMPT!*...and Claude sez no-can-do. 

Weirdly, I could still save the entire conversation to a markdown file, append the two other markdowns (a PRD in BDD/gherkin format and an initial DB schema) that Claude had created, and start a NEW chat, upload those, and say "Create a complete prompt that I can bring to Lovable/Bolt." And it did.

Started with Lovable but started too deep: It of course wanted to build out the UI -- and admittedly, it was a *nice* UI. I might come back to that in time. 

Changed to Bolt.new, and I liked the speed gain I got from it -- though that was maybe because I had become more decisive/articulate from my Lovable session. Anyway, again, realized I was starting too deep.

The shimmering magic I need at the center of this game would be what I'm humbly calling the "Clinical State Engine." The idea is that as the patient presents with X, Y and Z symptoms, and as the players run tests and try treatments, the patient's status should react in sensible ways. If they are dehydrated and we give them an IV, the thirst and other symptoms should abate. The aim of the game is to correctly diagnose the malady.

So yeah, shimmering magic will be needed. Dumped my two UIs and I'm deep in conversation with ChatGPT on how to build this iteratively, keeping to small testing steps, to keep the complexity bounded as we proceed. 

More news as it happens...