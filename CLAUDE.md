# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a DSA (Data Structures & Algorithms) learning repo focused on LeetCode preparation. It contains interactive HTML "lecture board" visualizations that explain algorithm patterns — styled to look like a chalkboard with handwritten fonts.

## Structure

- `DSA/<topic>/` — HTML lecture boards organized by topic (currently `linked-lists/`)
- `TODO.md` — Tracks which patterns still need lecture boards, organized by difficulty level

## Lecture Board Format

Each HTML file is a **self-contained, single-file** lecture board (no external JS/CSS beyond Google Fonts). They share a consistent visual design:

- **Chalkboard theme**: dark green background (`#2d5016`), wooden border, chalk-style text
- **Google Fonts**: Caveat (body chalk), Patrick Hand (subtitles), Permanent Marker (headings), Gloria Hallelujah (code/pointers)
- **Color palette**: yellow `#ffe066` (titles/emphasis), pink `#ff9ecf` (keywords/highlights), cyan `#7fd4ff` (section labels/code functions), green `#90ee90` (solutions/success), orange `#ffb347` (step titles/warnings), red `#ff6b6b` (problems/errors)
- **Responsive sizing**: all font sizes use `clamp()` for mobile compatibility, board max-width is `520px`

### Common CSS Classes

- `.board` — main container; `.title`, `.subtitle` — header
- `.section-label` — blue underlined section headings
- `.chalk` — body text; supports `.pink`, `.green`, `.cyan`, `.orange` color spans and `<strong>` for yellow emphasis
- `.ll-row`, `.node`, `.arrow`, `.null-node` — linked list diagram elements
- `.node` variants: `.dummy`, `.head`, `.active`, `.deleted`, `.slow`, `.fast`, `.both`, `.dim`, `.cycle-target`
- `.code-block` — code display with `.kw` (pink keywords), `.fn` (cyan functions), `.cm` (dim comments), `.num` (orange numbers), `.str` (green strings)
- `.step-box`, `.problem-box`, `.solution-box`, `.insight` — callout containers
- `.pill`, `.use-cases` — tag-style labels; `.badge` — complexity badges

### Content Structure Pattern

Each board follows: Title → Problem statement → Visual diagram → Solution explanation → Code template → When to use → Key insights

## Creating New Boards

When creating new lecture boards, copy the style/theme from existing files (e.g., `slow-fast-pointers.html` is the most comprehensive template). The files in `TODO.md` list remaining patterns to build, organized in dependency levels. Code examples are in JavaScript.

Note: Some existing files (`dummy-head-node.html`, `reverse-iterative.html`) are UTF-16 encoded with wide spacing between characters. The newest file (`slow-fast-pointers.html`) uses standard UTF-8 — prefer UTF-8 for new files.
