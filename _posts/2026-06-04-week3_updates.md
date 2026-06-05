---
title: "Week 3 Updates: June 4, 2026"
date: 2026-06-04 23:30:30 +0800
categories: [CSPB, Weekly Updates]
tags: [game-dev, cspb]     # TAG names should always be lowercase
---

### What I have done

#### Data Structures & Algorithms

In the past week, I worked on the infrastructure of my game. I designed a grid system to manage cards on the board. It has two aspects: two-dimensional arrays (data structures) and coordinates (visual representation). I'm following the convention of computer graphics, so the arrays *grid[y][x]* and the coordinates *(x, y)* are arranged in opposite ways.

I designed an algorithm to quickly evaluate a poker hand. Part of my algorithm is as follows:

For five cards:

Preparatory work
- Count ranks
- Count suits
- Check if this hand is a straight
- Check if this hand is a flush

Evaluation
- If straight and flush -> straight flush
- Else if a rank appears 4 times -> four of a kind
- Else if a rank appears 3 times and another rank appears 2 times -> full house
- Else if flush -> flush
- Else if straight -> straight
- Else if two ranks both appear twice -> two pair
- Else -> invalid

I evaluate hands following a standard poker hierarchy. I reject hands that would make my game too easy, such as high cards.

This function is just used for evaluating poker hands. I will create another function for evaluating the strength and score of a poker hand. According to the SOLID principles, decoupling functions is probably the best practice because each will have a clear and single responsibility.

#### Seeding System

I also read about pseudo procedural generation and designed an algorithm to use a seed (a large integer) to deterministically shuffle a card deck. For shuffling, I use the Fisher-Yates algorithm. I implemented the algorithm on a Google Sheet with Javascript to make sure that a seed always generates the same board layout.

### What I am doing

#### Software Architecture & Design Patterns

I have been studying the SOLID principles for software architecture, and I have been studying design patterns, including Singleton pattern, Command pattern, Factory pattern, Observer pattern, State Machine, and Model-View-Presenter (MVP). They are eye-opening. Some also look promising. But I still need to read more and think about how to apply these ideas to my game.

#### Unity & C#

I am going to studying Unity and C# in the next few days. I will give myself a crash course on Unity to learn the essential concepts and techniques that are needed for my game. Since my game will be 2D, I will entirely focus on 2D and skip all the technical details of a 3D game for the time being. For C#, I will learn all the basic syntax. Since it's a language in the C family, and since it has more syntactic sugar than C/C++, it should be more straightforward. C# is a general-purpose language, but I will just focus on its application on Unity.
