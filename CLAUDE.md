# CLAUDE.md — KIT-Tools

This file provides context for AI assistants (e.g. Claude Code) working in this repository.

---

## Project Overview

**KIT-Tools** (also referred to as *K-IT Tools*) is a Windows desktop utility that bundles
[yt-dlp](https://github.com/yt-dlp/yt-dlp) and exposes it through a custom interface.
The compiled application is distributed as `KiT_Tools.exe`.

### Known History

| Version | Notes |
|---------|-------|
| Initial | `yt-dlp.exe` added as standalone binary |
| v2.1 / v2.2 | `KiT_Tools.exe` (~66 MB) replaced the raw yt-dlp binary — yt-dlp was bundled inside |
| v2.2.1 | `KiT_Tools.exe` deleted from the repository |

Tags in this repo: `K-IT`, `v2.1`, `v2.2`, `v2.2.1`.

---

## Current Repository State

> **The repository currently contains no source files.**

The working tree is empty. Only the `.git/` directory is present.
All previously tracked files were compiled Windows executables, not source code.

This means:
- There is no build system to run.
- There are no tests to execute.
- There are no dependencies to install.

If source code is being added to this repository, update this file accordingly
(see the *Adding Source Code* section below).

---

## Repository Structure (Expected / Target)

When source code is introduced, the recommended layout is:

```
KIT-Tools/
├── CLAUDE.md          # This file
├── README.md          # User-facing documentation
├── src/               # Application source code
├── assets/            # Icons, resources, UI assets
├── dist/              # Build output (gitignored)
├── scripts/           # Build / release helper scripts
└── .gitignore
```

---

## Development Conventions

### Binaries and Build Artifacts

- **Do not commit compiled executables or large binaries** to the repository directly.
  Use GitHub Releases to distribute `KiT_Tools.exe` builds.
- Add a `.gitignore` that excludes `dist/`, `*.exe`, `*.pyd`, and other build artifacts
  before committing source code.

### Commit Style

Current commits are minimal (`"1"`, `"deleted"`). Prefer descriptive messages:

```
feat: add download queue UI
fix: handle missing yt-dlp dependency on first run
chore: bump yt-dlp to 2026.03.15
```

### Branching

- `main` — stable / release branch
- Feature work goes on short-lived branches (e.g. `feature/<description>`)
- Documentation / tooling branches follow `claude/<description>` for AI-assisted work

---

## Working with yt-dlp

`yt-dlp` is a dependency of this project. Key facts for AI assistants:

- The bundled `yt-dlp.exe` was ~18 MB at the time it appeared in this repo.
- `KiT_Tools.exe` (~66 MB) likely embeds yt-dlp via PyInstaller or a similar bundler.
- When updating yt-dlp, download the latest release binary from the official yt-dlp
  GitHub releases page and replace the bundled copy before rebuilding.
- yt-dlp's Python API can be used directly if the project is built from Python source.

---

## Adding Source Code

If you are adding source code to this repository for the first time:

1. Identify the language / framework used (Python + PyInstaller is the most likely
   candidate given the binary size and yt-dlp dependency).
2. Add a `README.md` explaining what the tool does and how to build it.
3. Add a `.gitignore` appropriate to the language.
4. Update this `CLAUDE.md` with:
   - How to install dependencies
   - How to run the application in development mode
   - How to build the release executable
   - How to run tests (if any)

---

## AI Assistant Guidelines

- **Do not assume source files exist.** Always verify with `ls` or `Glob` before
  attempting to read or edit files.
- **Do not push to `main` directly.** Open a PR from a feature branch.
- **Large binary files** (`.exe`, compiled artifacts) should not be committed; direct
  the user to use GitHub Releases instead.
- **Preserve the existing tag history** (`K-IT`, `v2.1`, `v2.2`, `v2.2.1`) — do not
  delete or move tags without explicit user instruction.
- When in doubt about the project's intent, ask the user rather than guessing.
