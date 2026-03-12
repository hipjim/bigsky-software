# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the website for **Big Sky Software** — a single-file static site (`index.html`) with no build step, no dependencies, and no frameworks.

## Development

No build, test, or lint tooling. To preview the site, open `index.html` directly in a browser or use a local static server:

```sh
python3 -m http.server 8000
```

## Architecture

The entire site lives in `index.html` with embedded `<style>` and `<script>` blocks.

**CSS** uses custom properties (CSS variables), CSS Grid/Flexbox, and CSS animations. Respects `prefers-reduced-motion`.

**JavaScript** is vanilla with no dependencies. Key behaviors:
- Typewriter animation on the heading at page load
- Staggered fade-in for content sections
- Mouse-tracking parallax on the background
- Scroll-based parallax
- "Skip animation" button for accessibility

All interactivity is self-contained — no external fetches, no bundler, no transpilation needed.
