# ![Euchre Banner]https://tenor.com/view/euchre-cards-play-cards-lets-go-gif-16354272376622054339

# EECS 280 — **Euchre** (University of Michigan)
[![build](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/yourname/eecs280-euchre) [![license](https://img.shields.io/badge/license-MIT-blue.svg)](#license) [![coverage](https://img.shields.io/badge/coverage-85%25-yellow.svg)](#tests)

> A compact, well-tested C++ implementation of the card game **Euchre** built for EECS 280 (UMich). Play human vs. human, human vs. AI, or watch the AI play against itself for statistics and strategy testing.

---

## Table of contents
- [Project Overview](#project-overview)
- Architecture
- [Quickstart (Install & Run)](#quickstart--install--run)
- [Prerequisites](#prerequisites)
- [Build (CMake)](#build-cmake)
- [Run examples (CLI)](#run-examples-cli)
- [Generating GIFs / Screenshots](#generating-gifs--screenshots)
- [Features](#features)
- [Deep-dive: Trick resolution & scoring](#deep-dive-trick-resolution--scoring)
- [Architecture](#architecture)
- [Usage Examples](#usage-examples)
- [FAQ](#faq)
- [Tests & CI](#tests--ci)
- [Dependencies & third-party code](#dependencies--third-party-code)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)
- [License](#license)

---

# Project overview
**eecs280-euchre** is a modular C++ implementation of the trick-taking card game *Euchre* designed as a course project for EECS 280.
**Key goals:** correctness of game rules, clean data structures, unit-tested logic, modular AI players, and an approachable CLI for playing and debugging.

**Who is this for?**
- EECS 280 students 
- Anyone learning data structures  by building an Euchre Program


**Why does it exist?**
- Teaching exercise to practice ADTs, pointers/references, copy semantics, and unit testing.
- A compact but complete example of game-engine design in C++.

---
# Architecture
- <img width="1470" height="890" alt="euchre-flowchart" src="https://github.com/user-attachments/assets/dabd0cc9-42da-428c-9d30-646ae05a4352" />

# Quickstart — Install & Run

> Works on macOS, Linux, and WSL. Build via **CMake** (recommended) or **Makefile**.

## Prerequisites
- **Compiler:** `g++` or `clang++` (C++17)
- **Build tools:** `cmake` >= 3.10 or `make`
- Optional: `SDL2` (for GUI), `GoogleTest` (for unit tests)

Ubuntu:
```bash
sudo apt update
sudo apt install -y build-essential cmake git libSDL2-dev
