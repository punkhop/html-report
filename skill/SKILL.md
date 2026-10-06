---
name: html
description: "Build an HTML page for a human reader — a report, brief, plan, decision, mission map, proof, explainer or mockup. Runs the report system: ask what you are presenting, pick blocks by what the content IS, build from the one stylesheet, screenshot before serving. Use when the user says \"/html\", \"make me a page\", \"show me this as a page\", \"write it up\", or any output that would otherwise be a wall of markdown."
---

# /html — build the page

**The split is by reader, not by document type.**

| Who reads it | Format |
|---|---|
| **A human** — a brief, plan, decision, status page, digest, findings, proof, mission map, explainer, mockup, anything they open | **an HTML page**, served as a link |
| **Only agents** — session notes, handoffs between Claude sessions, skill and rule files, catalogs | markdown |

If a person is going to look at it, it is a page. Nobody reads markdown for anything substantial —
a status page and a digest are for a human, so they are pages. Markdown is what one Claude leaves
for the next one.

## The canon lives in four files. Read them, don't restate them.

| File | What it holds |
|---|---|
| `READER.md` | **who this is for** — their register, their locale, where pages get served, their component kit |
| `html-report.md` | the method, the six jobs, the rules, the self-check |
| `BLOCKS.md` | every block: for / holds / never / which kinds it is at home on |
| `report.css` | the one stylesheet. Every block, both modes, the drift knobs |

`html-report.md` auto-loads on these triggers, so it is usually already in context. If it is not,
read it before writing a line of markup. **This file is a runner, not a second copy of the rules.**
Any rule that needs changing gets changed in `html-report.md`, never here. Anything about the
*person* gets changed in `READER.md`.

## Run it in this order

### 1 · Say the whole thing out loud first

Plain sentences, the way you would tell them across a desk. What happened. What it means for them.
What they have to decide. A page that cannot be said out loud becomes an essay, and essays get
skimmed to death. **The speech is the draft — it expands into blocks, never into paragraphs.**

**The title and every heading name the subject.** A page about invoicing has "invoicing" in its
title. Evocative and naming nothing gets rejected.

### 2 · Ask what you are presenting

Name the job by what **the reader has to DO**:

- they must answer something → **decision**
- they must not lose track of a big project → **mission map**
- they asked you to go find out → **findings**
- they asked whether it works → **proof**
- they asked how something works → **explainer**
- the subject IS a screen → **the thing itself**

Most pages are two jobs. The dominant job owns the spine; take the union of required blocks, never
the union of spines; the page answers once. Mixing rules are in `html-report.md` §2.

### 3 · Shop the shelf

Open `BLOCKS.md`, and open `examples/system.html` in a browser if a block is unfamiliar — every
block is drawn live there with its rules beside it. Blocks are tagged by the kind they are at home
on — **a starting shelf, not a fence.** Any block goes on any page when the connector test passes.

**Before drawing anything, say the relationship aloud.** Arrows say "then". A rail says "happened".
Nested boxes say "inside". Stations growing say "becomes". A grid says "and". **If the sentence is
a lie, the shape is wrong.** Peers want "and", so peers want a grid, never arrows.

Then: size means importance · position means order · nesting means containment · color keeps its
four meanings and a color without its meaning is a bug.

### 3b · If one of your own screens appears on the page, draw it for real

A screen is never described in a paragraph and never a gray placeholder box. It is a real HTML file:
framed full size in `.r-frame` on a thing-itself page, or scaled inside `.r-scale` as a miniature
(set `--r-w` and `--r-tall`, leave `--r-zoom` alone so it shrinks rather than clips on a phone).

- **Nothing drawn yet?** That is the normal case. The screen you need becomes the first file in a
  folder of its own, with its own small stylesheet. `examples/mocks/` is the worked example.
- **Something already drawn?** Frame that file. Never redraw it — two drawings of one screen will
  disagree. Check the folder named in `READER.md` §4 first, and say what you found.
- **A real component library or Storybook?** Point at that instead; the real component beats a mock
  of it every time.

### 3c · Measuring behavior across states? Use the matrix

When the subject is "what does each action do in each state", the block is the **state matrix** —
rows are actions, columns are states, every cell a mark plus what happened. The shape of the answer
is the finding: a row green all the way across behaves, one red square in a field of green is the
bug. Never leave a square blank; untested and unchanged are different answers.

### 4 · Build

The page lives in a dated folder per topic, e.g. `reports/YYYY-MM-DD-topic/<name>.html`. Two lines
at the top:

```html
<link rel="stylesheet" href="../skill/report.css">
<script src="../skill/report-table.js"></script>  <!-- only for 8+ row tables -->
```

Point those at wherever `skill/` actually lives, relative to the page or as an absolute URL.

Copy the theme toggle script from the foot of `examples/system.html`, and the page skeleton with
it: nav row + toggle · title · dek · the answer · teaching sections whose headings are sentences ·
their questions at the end of the section that makes them answerable · "Needs your attention" last,
or a recap when nothing is open.

**Only blocks from the sheet.** A genuinely new block gets built into `report.css` and listed in
`BLOCKS.md` the same turn — never inline on one page.

### 5 · Look at it before they do

Non-negotiable, and the source of every correction that has ever landed on these pages:

1. Screenshot the real render at **1440 and at 390**. Never serve unseen pixels.
2. Read every arrangement's connector aloud. A shape claiming something the content does not
   support is a defect, not a style choice.
3. Extract the h2s and read them as a paragraph — do they carry the argument alone?
4. Follow-up test on every noun: could they reply "which one?"
5. Walk the rest of the self-check in `html-report.md` §6.

Headless Chrome is the cheapest way to see your own render:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --disable-gpu \
  --hide-scrollbars --window-size=1440,1100 --screenshot=out.png --virtual-time-budget=6000 URL
```

Then look at `out.png`.

**For the phone, `--window-size=390` is a trap.** Headless Chrome lays the page out wider than that
and crops the screenshot to 390, so you see a desktop layout with its right side cut off and you
will "fix" defects that do not exist. Load the page in a real 390px iframe instead:

```bash
cat > /tmp/phone.html <<EOF
<!doctype html><meta charset="utf-8"><style>html,body{margin:0;background:#000}
iframe{width:390px;height:2200px;border:0;display:block}</style>
<iframe src="PAGE_URL"></iframe>
EOF
```

Then screenshot `/tmp/phone.html` at `--window-size=390,2200`. That gives a true 390 viewport, so
the phone rules in the sheet actually fire.

### 6 · Serve it

The command is in `READER.md` §3. Never a bare `file://` — most people will not open a path. A
**sources line** closes findings, proof and mission pages only.

## Standing traps

- **Never `overflow-x:hidden` on `html` or `body`** — it breaks scrolling in Chrome. Containment
  comes from `minmax(0,1fr)` on grids and `.r-tablebox` on wide tables.
- **A recommendation is an opinion and never wears a badge.** It uses `.r-mycall`.
- **Never dim or strike a ruled-out row.** They are still comparing against it.
- **A sequence carries no numerals.** Numerals only where something must be cited — proof claims
  and asks.
- **Small multiples and stat rows shrink on a phone, never stack.** Side by side IS the component.
- **Namespace every class `r-`.** A bare modifier name once matched a component and threw a panel
  off the page.
- **After editing `report.css`, reload with the cache bypassed before believing what you see.** A
  plain static server sends no cache headers, so Chrome holds the old stylesheet and you will
  screenshot a fix that did not apply. A `?v=N` on the page URL does not help — the stylesheet is a
  separate request.

## The page that shows all of it

`examples/system.html` — every block rendered live with what it is for, what it holds and what it
never does. Read it before composing anything unfamiliar.
