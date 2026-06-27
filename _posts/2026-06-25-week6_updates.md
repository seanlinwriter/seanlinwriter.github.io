---
title: "Week 6 Updates: June 25, 2026"
date: 2026-06-25 23:30:30 +0800
categories: [CSPB, Weekly Updates]
tags: [game-dev, cspb]     # TAG names should always be lowercase
---

### What I did last week

I added the ability to select cards, check connectivity, and evaluate hand types.

To select cards in terminal, I designed a console-only helper class that allows me to enter a string that uses card short hands (for example, AS = Ace of spades, TD = ten of diamonds, and 3H = three of hearts). This helper function can parse the input string (order doesn't matter), translate it into card data, and send data to the board object. 

I created a card connectivity checker that runs breadth-first search to check orthogonal connectivity. This is because all the selected cards must be orthogonally connected to be considered valid in my game. Think of selected cards as nodes on a graph. If you can reach every card via BFS, it means they are all connected. 

Lastly, I created a hand type evaluator that takes selected (and connected) cards and identifies their hand type.

To track the "selected / not selected" state of cards, I use a second 2D array of cards behind the scenes. This array consists of 6x6 Boolean values. It helps me map the state of cards into card data. I feel this may be a clearer implementation than adding an extra state to each card object. A 2D array of Boolean values is very lightweight. If I had to check every card object to check their selected state, it could be slower. I may be wrong, though. 

Due to the limitations of a console-based app, I've decided to use square brackets to enclose a selected card. The screenshot below shows an initial board, my card input, and an updated board with selected cards.

In this case, I have a straight:

Ten of Spades
Jack of Diamonds
Queen of Hearts
King of Diamonds
Ace of Diamonds

![console card selector]((../assets/img/screenshot_console_card_selector.png))


### What I am doing

I plan to add gravity in the next step. Now that a valid hand has been selected, I need to remove cards from the board and apply gravity to update the board. I will also add a hand score evaluator to add up scores. I will be using an infinite loop to keep the game running until I remove all the cards from the board.

So far the game is in solo mode. I will first focus on all the features that a solo player needs and then expand it into two player mode, which can be quite challenging to implement in terminal, but I will see what I can do. 


