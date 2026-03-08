# HTML to Image Skill for Agent

This skill allows AI agents to convert local HTML files into high-quality PNG images using the system's installed Google Chrome browser via `puppeteer-core`. This lightweight approach avoids the need to download a separate Chromium binary.

## Features

- 📸 **High-Quality Screenshots**: Captures full-page screenshots of any local HTML file.
- 🚀 **Lightweight**: Uses `puppeteer-core` and connects to your existing Chrome installation.
- 🤖 **Agent-Ready**: Designed to be easily invoked by AI agents (like Trae, Claude, etc.) via the Skills protocol.

## Installation

You can install this skill into your agent workspace using the `skills` CLI:

```bash
npx skills add Zevi-zzy/html-to-image-skills
```

## Prerequisites

1.  **Google Chrome**: Must be installed in the standard location.
    *   macOS: `/Applications/Google Chrome.app`
    *   (The script can be modified for Windows/Linux paths if needed)
2.  **Node.js**: The environment must support running Node.js scripts.

## Usage

Once installed, you can ask your agent to:

> "Convert report.html to an image."
> "Take a screenshot of dashboard.html."

The agent will use the `html-to-image` skill to:
1.  Verify `puppeteer-core` is installed.
2.  Generate a temporary Node.js script.
3.  Launch a headless Chrome instance.
4.  Render the HTML file.
5.  Save it as a PNG image in the same directory.

## Skill Definition

The skill is defined in `SKILL.md`, which provides the prompt engineering instructions for the agent to generate the correct Puppeteer script.

## License

MIT
