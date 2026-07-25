# AGENTS.md

## Cursor Cloud specific instructions

This repository (`Web-search`) is **documentation-only**. It contains D365
Finance & Operations and Power Automate documentation (Markdown guides, a
Power Automate flow-definition JSON, and office documents) — not an
application code base.

Key durable facts for future agents:

- There is **no runnable application, no dependency manifest** (no
  `package.json`, `requirements.txt`, `*.sln`, `*.rnrproj`, `Dockerfile`,
  `Makefile`, etc.), **no build system, and no automated test suite** on any
  branch. There is therefore nothing to install, lint, build, or run in this
  Linux Cloud Agent VM, and no update script is needed.
- The associated D365 F&O X++ work described in the project rules
  (`CLAUDE.md` user rules, `/d365fo.compile`, `xppc.exe`) targets **Windows +
  Visual Studio + Microsoft proprietary tooling** and **cannot be compiled or
  run in this Linux environment**. Do not attempt to set up a D365FO/X++
  toolchain here.
- Power Automate flow definitions (e.g. `docs/power-automate-flow-definition.json`
  on feature branches) execute in Microsoft's cloud, not locally.
- Work in this repo is authoring/reviewing documentation. Validate changes by
  reading the Markdown and checking links/formatting; there is no dev server or
  test command to run.
