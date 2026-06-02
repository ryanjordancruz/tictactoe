# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A self-contained browser-based Tic Tac Toe game in a single file: `tictactoe.html`. No build step, no dependencies, no package manager.

## Running the App

Open `tictactoe.html` directly in a browser. No server required.

## Git Workflow

Commit and push to `origin master` after every meaningful change — not just at the end of a task. Each commit should have a clean, descriptive message reflecting what changed and why. Push frequently so there is always an up-to-date remote copy and any state can be recovered or reverted.

## Architecture

Everything lives in `tictactoe.html`:

- **CSS** (inline `<style>`) — dark-themed layout using CSS Grid for the 3×3 board.
- **HTML** — static board of 9 `.cell` divs, a score display, and a reset button.
- **JS** (inline `<script>`) — pure vanilla JS. Key globals: `board` (9-element array), `current` (active player `'X'`/`'O'`), `scores` (win/draw counters). Win detection iterates the `WINS` constant (all 8 winning index triples). No frameworks, no modules.
