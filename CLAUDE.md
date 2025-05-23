# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains simple tools written entirely by LLMs. Each tool is a self-contained HTML file that includes vanilla JavaScript and CSS. The tools are deployed on GitHub Pages.

## Architecture

- **Single-file tools**: Each tool is contained in one HTML file with embedded CSS and JavaScript, inside the tool directory.
- **No build process**: Tools use vanilla web technologies without compilation or bundling (especially no React, Vue, etc.)
- **GitHub Pages deployment**: Static files are served directly from the repository
- **Entry point**: `index.html` serves as the main directory listing all available tools

## Style Guide
- **Appearance**: Dark theme, clean and minimalistic design, flat colors, developer look
- **Responsiveness**: Tools should be responsive and work well on both desktop and mobile devices
- **HTML**: Use semantic HTML5 elements where appropriate
- **CSS**: Use inline styles for tool-specific styles; avoid external stylesheets
- **JavaScript**: Use vanilla JavaScript; avoid libraries or frameworks
- **Documentation**: Each tool should have a brief description at the top of the HTML file, explaining its purpose and usage
- **Fonts**: Use JetBrains Mono (from google fonts)
- **Title**: At the top, each tool should have a big header with style "/tool-name" in smaller case

## Development Workflow

Since this is a static site with no build process:
- Create new tools as standalone HTML files
- Update `index.html` to list new tools
- Deploy by pushing to the main branch (GitHub Pages auto-deploys)

## File Structure

- `index.html` - Main entry point that lists all tools
- Individual tool files - Self-contained HTML files with embedded CSS/JS
- `README.md` - Project documentation