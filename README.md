# The HTML report system

A way to make Claude hand you a **page** instead of a wall of text.

You ask a question that deserves a real answer — compare these five options, is this actually
fixed, explain how this works, here is where the project stands. Instead of six screens of chat
prose, Claude writes an HTML page: the answer at the top, the evidence beside the claims it proves,
your open questions in an amber panel you cannot skim past. One stylesheet, no build step, no
libraries. Open it in a browser, dark or light, desktop or phone.

It was built for one person over two days, by rejecting drafts until the rules held. This copy is
the same system with that person taken out of it — every rule they measured for themselves is now a
default you can overrule.

A 31-second tour of the blocks: [`demo/html-report-demo.mp4`](demo/html-report-demo.mp4)

---

## Start here

**Hand this whole folder to your Claude and say: "read ONBOARD.md and run it."**

`ONBOARD.md` is written for Claude, not for you. It tells it to read the system, look at the
examples, then present the whole thing to you and ask what you want to change *before* installing
anything. About twenty minutes, and it ends with one real page built from something you actually
needed.

If you would rather look first:

```bash
cd <this folder> && python3 -m http.server 8181
```

Then open `http://localhost:8181/examples/system.html` — every block in the system, drawn live,
with what it is for and what it must never hold beside it.

*(Serve it over http rather than double-clicking the file. Opened directly, the stylesheet and the
table controls will not load and the page looks broken.)*

---

## What is in the box

| | |
|---|---|
| `ONBOARD.md` | the first conversation, for Claude to run. Start here |
| `README.md` | this file |
| `CUSTOMIZE.md` | every knob, and which file to turn it in |
| `skill/READER.md` | **the one file that is about you.** Onboarding fills it in |
| `skill/html-report.md` | the method, the six kinds of page, the rules, the self-check |
| `skill/BLOCKS.md` | the catalog — every block, what it claims, what it must never hold |
| `skill/SKILL.md` | the `/html` runner: the steps, in order, every time |
| `skill/report.css` | the one stylesheet. Every block, light and dark |
| `skill/report-table.js` | search, sorting, filters and phone card mode for long tables |
| `examples/` | eight worked pages — the shelf, plus one per kind of page |

---

## The idea in five lines

1. **Say it out loud first.** The speech is the draft. It expands into blocks, never paragraphs.
2. **Name the job by what you have to DO** — decide, don't lose track, go find out, show me it
   works, help me understand, show me the screen.
3. **Form follows function.** Arrows say "then", a grid says "and". If the shape's sentence is a
   lie, the shape is wrong.
4. **Build only from the sheet.** A new block goes into the stylesheet, never inline on one page.
5. **Look at the render before you send it.** At 1440 and at 390.

---

## What you are agreeing to

Some of this is structural and some of it is one person's taste. Claude will walk you through the
split during onboarding, but the short version:

**Structural** — the speech-first method, form follows function, the four drawing laws, one
stylesheet, answer before teaching, look at it before sending.

**Taste, change freely** — dark by default, the color meanings, no emoji, US spellings, and the
writing register, which was measured from 13,002 of one person's own messages and is not yours. The
six kinds of page stay as the starting set; add a seventh if something you ask for is missing.

---

## The examples

| Page | Shows |
|---|---|
| `system.html` | the shelf — every block, live, with its rules |
| `decision.html` | a choice, answerable in one word from a phone |
| `findings.html` | go find out and tell me what to do — with the long-table controls |
| `explainer.html` | one metaphor carried the whole way down |
| `mission.html` | a big project you must not lose track of |
| `proof.html` | claim, what was seen, how to get there, the capture |
| `thing.html` | the actual screen, framed, with numbered notes |
| `drift.html` | why the spacing rules exist — the same page before and after |

The content is invented. The shapes and the rules are the real ones.
