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
- **Color scheme**: Use flat red (#c0392b) as the primary accent color for consistency across all tools
- **Responsiveness**: Tools should be responsive and work well on both desktop and mobile devices
- **HTML**: Use semantic HTML5 elements where appropriate
- **CSS**: Use inline styles for tool-specific styles; avoid external stylesheets
- **JavaScript**: Use vanilla JavaScript; avoid libraries or frameworks
- **Documentation**: Each tool should have a brief description at the top of the HTML file, explaining its purpose and usage
- **Fonts**: Use JetBrains Mono (from google fonts)
- **Title**: At the top, each tool should have a big header with style "/tool-name" in smaller case
- **UI Patterns**: 
  - Use consistent copy buttons with red accent color and success feedback
  - Include line numbers for code/text editors
  - Use syntax highlighting with GitHub-style colors for code display
  - Implement collapsible/expandable sections for complex data structures

## Required Components
Every tool must include these standardized elements:

### Navigation
- **Home link**: Add a "← home" link in the top-left that goes back to ../index.html
- Use this CSS styling:
```css
.home-link {
    color: #888;
    text-decoration: none;
    font-size: 14px;
    transition: color 0.2s ease;
}

.home-link:hover {
    color: #c0392b;
}
```
- Place in a flex container with the title centered

### Footer
- **Attribution footer**: Include "made with ❤️ by nuwandavek" footer at the bottom
- **GitHub source link**: Include a "view source" link pointing to the specific tool file on GitHub
- Use this CSS styling:
```css
.footer {
    text-align: center;
    margin-top: 40px;
    padding-top: 20px;
    border-top: 1px solid #444;
    color: #888;
    font-size: 14px;
}

.footer a {
    color: #c0392b;
    text-decoration: none;
}

.footer a:hover {
    text-decoration: underline;
}
```
- Link format: `made with ❤️ by <a href="https://github.com/nuwandavek">nuwandavek</a> | <a href="https://github.com/nuwandavek/llm-tools/blob/master/tool/[TOOL-NAME].html">view source</a>`

## Development Workflow

Since this is a static site with no build process:
- Create new tools as standalone HTML files
- Update `index.html` to list new tools
- Deploy by pushing to the main branch (GitHub Pages auto-deploys)

## File Structure

- `index.html` - Main entry point that lists all tools
- Individual tool files - Self-contained HTML files with embedded CSS/JS
- `README.md` - Project documentation