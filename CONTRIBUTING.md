Contributing
===========

Thanks for your interest in improving zx_debate! This is a small static project that embeds a ZX Spectrum emulator to load classroom debate prompts.

How to contribute
- Propose: Open an issue describing the improvement (docs, code, UI, accessibility, etc.).
- Discuss: Share context, screenshots, or small repro steps if relevant.
- Implement: Fork, create a feature branch, and submit a focused pull request.

Project setup
- No build step is required to run: it’s a static site.
- Run locally by serving the folder, e.g. `python3 -m http.server 8000` and navigate to `http://localhost:8000`.
- To switch the tape, edit `index.html` and change `loadFile` (e.g. `ernesto.tap` → `juanbe.tap`).

Rebuilding TAP files
- If you change a `.bas`, regenerate the corresponding `.tap` using the ZX Basic compiler (`zxb`).
- Example: `zxb -o ernesto.tap -t -B -a ernesto.bas`

Guidelines
- Keep changes minimal and focused; avoid unrelated edits.
- Prefer clear, concise documentation (Spanish is welcome; adding an English summary helps).
- Match the existing style and formatting.

License
- By contributing, you agree that your changes are licensed under GPL-3.0 (see `LICENSE`).

