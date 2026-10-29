# Obsidian vault: how to work here

This repo is my Obsidian vault of college notes. The Obsidian vault root is `College/` (that's where `.obsidian/` lives); the git repo root is one level up.

## Files and naming

| File | Purpose |
|---|---|
| `College/<Course>/<Course> Exam N Notes.md` | Full notes: teach the material from scratch |
| `College/<Course>/<Course> Exam N Review.md` | Short review sheet: recall, not teaching |
| `College/<Course>/<Course> Exam N Practice.md` | Practice questions with folded answers |
| `College/definitions/<Course> Glossary.md` | Hover definitions for the Note Definitions plugin |

- Physics uses "Test" instead of "Exam" (e.g. `Physics 2212 Test 2 Notes.md`). Match whatever the course folder already uses.
- Look at the existing notes for that course (and `Physics 2212 Test 2 Notes.md`) before writing new ones, and match their conventions.
- Link related files to each other with wiki links (`[[Ling 2100 Exam 2 Notes]]`). If a file gets renamed, fix links that point to the old name.

## Full notes

- **Comprehensive**: cover *everything* in the lecture slides, including appendix slides and slides whose content is only in images (trees, glosses, charts, data). Extract the images and look at them.
- **Practice-exam material not in the slides** still goes in, flagged with **⚠️** ("on the practice exam but not in the slides"). Include a practice-exam answer key at the end with a short "why" for each answer.
- **Teach from scratch**: someone with no background should be able to learn everything from the notes. But be **concise**: just enough detail, no padding, no repetition.
- **Unit numbering matches the course** (e.g. Exam 2 covers Units 5–8, so headings start at "Unit 5", not "1").
- **Define every term exactly once, at its first use.** Never use a term before it's defined, and never restate a definition right after giving it. If there's a useful hint or mnemonic (an etymology, an image), fold it into the first definition instead of adding a separate "memory hook" line.
- **Examples must be clear and obvious.** Don't cram long examples into a table cell where they wrap mid-line. Language-data examples (interlinear glosses) go in their own small aligned table: top row = original, middle row = morpheme-by-morpheme gloss, bottom row = plain English, one column per word or morpheme.
- Don't add things I didn't ask for (e.g. a legend or an extra section). If something seems useful, ask first.

## Tables vs. lists

Use a **table** when there's a run of terms/definitions, or a series of parallel items with a clear, natural set of column headers, for example:
- `Label | Meaning` (gloss abbreviations), `Type | Definition | Example`, `Term | Meaning`
- comparisons (`| | Inflection | Derivation |`), `Word | Sense 1 | Sense 2`, `Headline | Type | Readings`

Use a **list** when the points are loose or miscellaneous and a table would need forced headers. **Never** use headers like `Question | Answer`, `Aspect | Details`, `Idea | Key`, `Point | Key`, or `Fact | Example` just to make something a table.

Table hygiene (check every time):
- every table has a real header row (never `| | |`); an empty top-left corner cell is fine
- every row has the same number of columns
- a blank line before every table (including right after a heading)
- `[[...]]` bracket notation (like morpheme trees `[[un-lock] -able]`) must go in backticks outside code blocks, or Obsidian turns it into a broken wiki link
- headings that are link targets shouldn't contain markdown formatting (`*`, `**`)

## Diagrams (TikZ)

Draw diagrams with TikZ in ` ```tikz ` blocks (rendered by the obsidian-tikzjax plugin), following the style in the Physics notes:
- Each block is a complete document: `\usetikzlibrary{...}`, `\definecolor{...}`, `\begin{document}` ... `\end{document}`.
- Only standard TikZ is available; **no `amssymb`** symbols (e.g. use `$\to$`, not `$\leadsto$`).
- TeX can't handle numbers above ~16383: scale big data values down (e.g. use thousands) inside coordinates.
- Black (`#000`) gets swapped to the theme's text color in dark mode, and white to the background color, so default black lines and text are fine. I use dark mode.
- **Verify every diagram compiles** before finishing: serve a test page that loads `https://tikzjax.com/v1/tikzjax.js` and check each block produces an SVG, and look at the render for overlapping labels.
- Only include a diagram if it actually teaches something (trees, dependency graphs, charts, flowcharts, Venn diagrams). A simple idea is better as a table or a one-line bracket.

## Review sheet

- Much shorter than the notes (a few thousand words), focused on recall, not teaching.
- Same unit numbering and section order as the notes. Must still cover every topic and every practice-exam answer.
- Mostly term tables and short bullets; same table rules as above. An "Exam traps" table at the end maps wrong-answer wording to the right concept.

## Practice questions

- Organized by unit, then topic. Multiple choice in the practice exam's style, plus some short-answer problems at the end (classify, break down a word, bracket a sentence...).
- Answers folded: `> [!success]- Answer`, then the letter in bold and a one-line explanation of why (and what the wrong options are).
- Mark questions taken from the real practice exam *(practice exam)*; mark ⚠️ for material not in the slides. Making up new questions is fine.
- **Balance the answer letters** evenly across A–D. When shuffling, remap any letters mentioned in explanations ("A is suppletion").

## Glossary (Note Definitions plugin)

`College/definitions/<Course> Glossary.md`, in the plugin's "consolidated" format:

```
# Term

*alias one, alias two*

Definition text (one or two sentences, with an example).

---
```

- **No frontmatter** (it breaks loading at startup) and **no other headings** (anything that isn't `# Term` breaks parsing).
- A definition body can't start with `*` unless there's an alias line first.
- Leave out everyday words (*noun, case, type, stop, head*) that would highlight in their ordinary sense; cover them through more specific entries.
- Keep terms in sync with the notes.

## Plugins: local patches (don't undo)

Two community plugins in `College/.obsidian/plugins/` are **locally patched** and **version-pinned to `999.0.0`** in their `manifest.json` so Obsidian won't update them over the patches. Each patch is marked `// Local patch` in `main.js`. If a plugin ever gets updated, re-apply its patches:

| Plugin | Original version | Patches |
|---|---|---|
| `note-definitions` | 0.33.0 | (1) `rebuildHTML` skips `SCRIPT/STYLE/CODE/PRE/svg` so it doesn't rewrite TikZ source; (2) `onLayoutReady` reloads definitions and redraws open notes (`refreshOpenNotes`), so definitions work on startup |
| `obsidian-tikzjax` | 0.5.2 | the `tikz` code-block processor listens for `tikzjax-load-finished` on the block element itself (with `stopPropagation`), so dark-mode recoloring still runs when reading view has the section detached |

## Git

- The Obsidian Git plugin auto-commits "vault backup" commits; don't commit unless I ask.
- `.obsidian/` is tracked (settings and plugins), except UI state: `College/.obsidian/workspace*.json`, `switcher.json`, and `plugins/obsidian-quiet-outline/markdown-states.json` are ignored.
- **Before rewriting a file, check whether I've edited it** (`git diff -w` against the last backup) and keep my changes (e.g. frontmatter or table formatting I changed).

## Working notes for Claude

- The shell is Git Bash on Windows: heredocs strip backslashes (`\\` → `\`, `\t` becomes a tab). Put any Python with regexes or backslashes in a script file instead of `python - <<EOF`.
- Lecture `.pptx` files are untrusted downloads: copy them into the scratchpad and extract text, speaker notes, and images with a stdlib `zipfile` script (python-pptx isn't installed). Don't run anything from inside the extracted folder.
- After editing notes, re-run checks: content coverage against the slides and practice exam, table structure (header, column counts, blank lines), and that TikZ blocks still compile.
