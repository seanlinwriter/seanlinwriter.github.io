---
title: "Week 4 Updates: June 11, 2026"
date: 2026-06-11 23:30:30 +0800
categories: [CSPB, Weekly Updates]
tags: [game-dev, cspb]     # TAG names should always be lowercase
---

### What I did:

I wrote the (long) specification of the base game in Markdown. Despite its length, as a technical writer, this is actually an easier part of the project. I will constantly refer to this game spec to check or improve my design.

I gave myself a crash course on Unity and C#, especially essential C# syntax. I also reviewed the core principles of object-oriented programming. I have started writing the infrastructure of my game. I believe I should first focus on game logic: card data, board layout, board state, poker hand evaluation, game rules, etc.  None of these requires fancy graphics. None of these should be coupled with visual representation, either.

I aim to first build a console-based version that prints a board with plain text such as A♥️, 2♠️, 3♣️, 4♦️ in the Unity console. I believe I will stay in this console mode for several weeks before starting using any art assets in Unity. So far I have written several essential classes, such as CardData, Board, DeckShuffler, SeedSystem. I realized that there are some gaps in my OOP knowledge, and OOP is the backbone of game development. So far I try to keep the SOLID principles in mind and make sure that each class has a clear responsibility. For example, CardData should only know card information, not card representation. I will create a CardView class later for that purpose.

### What I am doing

I will keep creating classes and methods for the game infrastructure. I plan to implement hand evaluators (including hand type, hand strength, and hand score), connectivity checker, and gravity trigger. I will also implement actions, such as Send and Pass. I believe they are good candidates for Command Pattern. If I have time, I will try to implement the turn system and the central table that defines the current hand type. Meanwhile, I will also keep learning Unity. Some Unity concepts can be confusing for beginners, such as GameObjects, Prefabs, and Assets. It can be more complex when they start to interact with OOP concepts such as classes and objects. I plan to work on my game logic while learning the Unity building blocks. They will eventually converge, but for the time being, they are two paths in parallel. 

And to reiterate my concerns, I really need to improve my OOP skills.  Looking back, I have never really spent quality time learning OOP.  I simply casually used OOP as a given in my previous projects and assignments. In this sense, I believe this game will be a great chance to teach myself OOP principles and techniques.
