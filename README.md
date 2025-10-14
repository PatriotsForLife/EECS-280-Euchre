# Euchre![card-20257_256](https://github.com/user-attachments/assets/4a416298-2b99-403a-a208-0c630be178ed)


# EECS 280 — **Euchre** (University of Michigan)
[![build](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/yourname/eecs280-euchre) [![license](https://img.shields.io/badge/license-MIT-blue.svg)](#license) [![coverage](https://img.shields.io/badge/coverage-85%25-yellow.svg)](#tests)

> A compact, well-tested C++ implementation of the card game **Euchre** built for EECS 280 (UMich). Play human vs. human, human vs. AI
---

## Table of contents
- [Project Overview](#project-overview)
- [Architecture](#architecture)
- [Quickstart (Install & Run)](#quickstart--install--run)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Build (CMake)](#build-cmake)
- [Run examples (CLI)](#run-examples-cli)
- [Usage Examples](#usage-examples)
- [FAQ](#faq)



---

# Project overview
**EECS 280 Euchre** is a classic example of Object-Oriented Programming (OOP), leveraging C++ to simulate a complex card game. Its core function is to manage game state, enforce rules, and facilitate interaction between different player types through a modular, class-based architecture.

The system is built on four primary Abstract Data Types (ADTs) that encapsulate distinct responsibilities:
    
    - Card: Represents a single playing card. It consists of the complex logic for determining a card's value based on the current Trump suit and Led suit using specialized comparison functions.
    - Pack: Represents the deck of 24 cards. It manages the card order, handles the shuffling algorithm, and facilitates the dealing of cards to players.
    - Player: An abstract base class that defines the interface for all player actions (e.g., make_trump, play_card).
    - Simple/Human Player: Derived classes that inherit from Player. Polymorphism allows the main game loop to treat both an AI player (Simple) and an interactive user (Human) identically when requesting an action.
The **EECS 280 Euchre** program operates as a game driver, initialized by validating command-line arguments and setting up four players, which are dynamically allocated as either Simple (AI) or Human types, leveraging polymorphism. The software enters a main Game Loop that continues until a team reaches the POINTS_TO_WIN threshold, with the dealer position rotating each hand. Each hand cycles through several phases: the Pack is shuffled and cards are dealt; the Making Trump phase uses a two-round, polymorphic call to the players' make_trump method to set the trump suit; and the Trick Taking phase proceeds through five tricks, where the software enforces the follow suit rule.

The core complexity of the game is encapsulated within its ADTs. The Card object manages the most complex logic, as its value is determined by a complex system involving the Trump suit and the Led suit. This comparison logic must correctly handle Bower Mechanics (Right and Left Bowers), Trump Dominance over all other cards, and the elevated importance of the Led Suit for non-trump cards. Meanwhile, the Player objects, especially the Simple Player, encapsulate their specific AI strategy for Ordering Up and Playing Cards. By defining the player interface through an abstract base class, the main game loop remains clean and can seamlessly interact with both AI and human input, effectively separating the game's flow control from the decision-making logic.
**Who is this for?**
- EECS 280 students 
- Anyone learning data structures  by building an Euchre Program


**Why does it exist?**
- Teaching exercise to practice ADTs, pointers/references, copy semantics, and unit testing.
- A compact but complete example of game-engine design in C++.

---
# Architecture
- <img width="1470" height="890" alt="euchre-flowchart" src="https://github.com/user-attachments/assets/dabd0cc9-42da-428c-9d30-646ae05a4352" />
- <img width="592" height="517" alt="Screenshot 2025-10-14 at 4 21 18 PM" src="https://github.com/user-attachments/assets/6beabc47-74c2-491b-835b-40cab73715e4" />

# Quickstart — Install & Run

> Works on macOS, Linux, and WSL. Build via **CMake** (recommended) or **Makefile**.
> Download the euchre folder and navigate to the location of the euchre folder in your CLI (Command Line Interface) and run ```gcc euchre.cpp -o euchre```
> Run ```make euchre```  and play the game. [Rules of Euchre](https://bicyclecards.com/how-to-play/euchre)


![a93nho](https://github.com/user-attachments/assets/cd3fca29-951e-4b53-9a93-259e7cb4a39a)


![a93pri](https://github.com/user-attachments/assets/f8bdd762-7e20-4f34-a5bb-d26629a326af)



# Features
- Multiplayer ![poker](https://github.com/user-attachments/assets/701e2d19-e523-4b91-94da-4a0cc89c864b)
Euchre Game

- Play Euchre against the computer
- ![artificial-intelligence-22071_256](https://github.com/user-attachments/assets/c893df5a-60b2-489b-8d7b-944dbbc73b13)

## Prerequisites
- **Compiler:** `g++` or `clang++` (C++17)
- **Build tools:** `cmake` >= 3.10 or `make`

Ubuntu:
```bash
sudo apt update
sudo apt install -y build-essential cmake git libSDL2-dev
```
# Usage Examples
- Learning how to use data structures in C++ to build complex programs
- A casual game to play for fun
# FAQ
- What is Euchre?
    - Euchre is a card game played by 4 players with the objective of taking tricks and winning hands.
- Is it necessary to use data structures to build this game?
    -  Yes, it is absolutely essential to use data structures like classes to build this Euchre program.
- How can I keep track of the rules?
    - You can use the Euchre flowchart to help you figure out the rules and order of the game.



