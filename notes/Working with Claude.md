---
tags: [valley-life, help]
---
# Working with Claude

Back to [[Home]]

## How changes happen
1. Tell Claude what you want, for example "make the boar slower" or "fix the bugs in [[Bugs and Ideas]]".
2. Claude changes the game, tests it, and pushes to GitHub.
3. Within a couple of minutes the website and the `.exe` on Releases update by themselves.
4. In GitHub Desktop, click **Fetch origin**, then **Pull**, to get the new files and notes on your computer.

> [!warning] Before you write notes
> Always **Pull** first in GitHub Desktop, then write, then **Commit and Push**.
> That way your notes and Claude's changes don't bump into each other.

> [!caution] This repo is public
> Anyone can read these notes on GitHub. Don't write anything private here.

## Where things are
| What | File |
|---|---|
| The game (Python, used for the `.exe`) | `valley_life.py` |
| All the art | `valley_art.py` |
| Browser version | `web/template.html` |
| Builds the browser version | `build_web.py` |
| The website GitHub Pages shows | `docs/index.html` |
| itch.io files and guide | `itch/` |
| These notes | `notes/` |
