---
name: html-report
description: The one skill for any HTML page written for a human reader — reports, briefs, plans, decisions, mission maps, proofs, explainers, mockups. Ask what you are presenting, pick blocks by what the content IS, build only from the sheet.
kind: rule
triggers:
  - html
  - brief
  - plan
  - report page
  - status page
  - digest
  - write it up
  - needs your attention
  - mission map
  - explainer
  - mockup
  - show me options
---

# HTML pages for a human — one method, one sheet, a shelf of blocks

Every big document Claude hands a person to review, decide from, or learn from is one of these
pages. The goal: **richer communication bandwidth.** The more that lands in one read, the more
aligned you are and the less you spend re-explaining. A page that makes your reader reread, or
reply "which one?", spends that bandwidth instead of building it.

**Who your reader is lives in `READER.md`.** Read it first. Every rule below is a rule about that
person, and a few of them flip when the person changes.

## How this works, start to finish

1. **Say the whole thing out loud first** — the speech, in plain sentences, across a desk.
2. **Ask what you are presenting.** A decision? A mission? Findings? Proof? Teaching? The thing
   itself? Name the job by what your reader has to DO. Most pages are two jobs at once.
3. **Shop the shelf** — `BLOCKS.md`. Blocks are tagged by the kind they are at home on, and any
   block may go on any page **when the connector test passes**.
4. **Build only from `report.css`.** Two lines at the top of the page, no libraries, no build step.
5. **Screenshot it, look at it, walk the self-check**, then serve it as a link.

---

## 1 · The method — write the speech first

**Before any HTML: say the whole thing in a few plain sentences.** What happened. What it means for
them. What they need to decide. A page that cannot be said out loud first becomes an essay — and
essays get skimmed to death.

**The speech is the draft, never the render.** It expands into blocks — drawn rules, cards, chips,
hero numbers — not into paragraphs. Rendering the speech as prose is the single most common failure
of this system: *"It's just a wall of text. You didn't do anything with HTML at all."* Short does
not mean two paragraphs; it means few blocks, each carrying one point. **A finished page has no
prose block over about three lines** — anything longer is a block that has not been drawn yet.

1. **The headline reads like a book title, and it names the subject.** Short, plain, one thought,
   no quotation marks, at most one dash — but the actual thing has to be in it. A page about
   invoicing says "invoicing" in the title. "Rebuilding how you get paid" is evocative and names
   nothing. The test: your reader wrote the underlying idea six months ago and remembers none of
   it; the title alone tells them what the page is about. Never a tease, never a quoted phrase up
   front, never clause chained to clause. **The same applies to every h2** — "The whole thing runs
   on one file now" fails it; "Every report page runs on one stylesheet now" passes.
2. **The line under the title describes the page in a handful of words, with no data.** "Five
   payment providers, compared." The data arrives where it lives, in blocks.
3. **When the page opens a subject they have not held for months, introduce it cold.** Never "the
   test / the plan / the question" before saying what it is — *"You checked what? Which test?"* is
   an instant rejection.
4. **Every h2 is a sentence of the speech.** Extract the headings and read them as a paragraph
   before serving: fifteen seconds of headings and six minutes of full reading must reach the same
   conclusion.
5. **Evidence sits against the sentence it proves.** Never a separate evidence pile to join back up.
6. **Answer first, teach inside, their calls at the end of the section that makes them answerable,
   one recap last.** Both, not either: the question appears inline where it can be answered, AND a
   "Needs your attention" section at the foot indexes every one so a skim misses none. A page whose
   questions live only at the bottom forces a scroll back up to answer them.

On directness: **state it like an ad, prove it like a report.** Benefit first, plain claim, no
build-up — the directness of advertising copy, never its selling tone.

---

## 2 · What am I presenting? — the six jobs

Measured over 330 real pages written for one reader. **Name the dominant job by what your reader
has to DO**, not by how much of the
page each job fills. If they must answer something, it is a decision however long the teaching
runs. If they only have to understand, it is an explainer however many numbers appear.

| Job | The ask, in their words | Answers first with | Required blocks |
|---|---|---|---|
| **Mission map** | "Bird's-eye view of this huge project so I don't lose track" | stat row or tally | timeline rail · status marks · asks |
| **Decision** | "Decide this with me" | decision cards | my call · asks |
| **The thing itself** | "Show me the actual screen, not a description of it" | embedded prototype | numbered notes · asks |
| **Findings** | "Go find out and tell me what to do" | verdict plate | admitted-flaws row · my call · asks |
| **Proof** | "Show me it actually works" | tally | evidence pairs · what this does not cover |
| **Explainer** | "Help me understand how this works" | callout, or the first stage of the metaphor | a carried sequence or drawing · recap |

Six is the whole list to start from. A seventh gets added only when the reader regularly asks for
something none of the six covers — named by what they have to do, with its own answer-first block
(`READER.md` §2). **Drawings are not a seventh job** — the assembly line, nesting doll, split bar,
miniature and before/after are elements the six build from, the same way a table is.

**The explainer is the craft job.** Give it the most drafting care: one metaphor mapping 1:1 to
real parts (recipe card → kitchen → plate is the standard to beat), every new term getting a
household name with the real name beside it, once, where it lands.

### Mixing two jobs — three rules, in order

1. **The dominant job owns the spine** — the answer slot and the section order.
2. **Take the union of required blocks, never the union of spines.** The secondary job's
   answer-first block drops. A page answers once.
3. **The page never switches format halfway down.**

*Worked — a page that is both an explainer and a decision:* they have to answer, so it is a
decision. The cards go near the top with the recommendation pre-filled, the teaching earns them
underneath, my call sits at the end of the section that makes it answerable, and "Needs your
attention" closes it — the explainer's recap drops. Flip it so the choice is already made and
exactly one thing changes: the cards move down, lose their radio, and become the illustration of a
decision taken.

---

## 3 · Picking a block — form follows function

The ruling that produced this rule, on three unrelated drawings laid out as a flow: *"You put three
completely different things that have nothing to do with each other in a sequence line… You did
this just because you have the one, two, three boxes with arrows between them. That is exactly what
we do not want to do. We want the form to follow the function for all displays on all pages."*

**Having a block is never a reason to use it.**

### The connector test — say it out loud before you draw

Every arrangement makes a claim about how its items relate. Read the claim aloud. **If the sentence
is a lie, the shape is wrong.**

| Drew | Claims | Read aloud |
|---|---|---|
| cards with arrows | order | "A **then** B **then** C" |
| a rail with dots | happened, at times | "A **happened**, then B" |
| nested boxes | containment | "B is **inside** A" |
| three stations growing | transformation | "A **becomes** B" |
| a bar cut into slices | parts of a whole | "A **plus** B **equals** the total" |
| bars on one scale | magnitude | "A is **bigger than** B" |
| a grid of equal cards | peers, no order | "A **and** B" |
| a table | the same questions of each | "for each: price, size, verdict" |

Peers want "and", so peers want a grid — never arrows.

### The four drawing laws

- **Size means importance.** A bigger block claims it matters more. If it does not, shrink it.
- **Position means order.** Left to right, top to bottom, is a sequence claim. Do not make it idly.
- **Nesting means containment.** A box inside a box says the inner thing belongs to the outer one.
- **Color keeps its four meanings, always** — green good/done/the pick · amber
  waiting/caution/their call · red broken/dead/ruled out · teal informational, in flight,
  magnitude, links. Everything else is grayscale surface. **A color appearing without its meaning
  is a bug.**

### The fact test — does it change a decision?

Before a fact, figure, chart or section earns its place: **does your reader make a different
decision because it is here, given what this page is for?** The verdicts that produced this test:
*"you're using stat cards just because you have them"* · *"I don't care how many facts it knows"* ·
*"I don't need two charts just because you have access to charts."*

- **Never draw what seven words can say.** A chart illustrating a concept rather than carrying data
  they act on is decoration.
- **The history of an idea is one line, not a section.** "It's called X, named by Y" — then move.
- **Numbers shown side by side share one axis** — same unit, same period, same subject. If they do
  not compare, they do not sit together.
- **No needless precision.** A third number that changes no decision comes off.
- **The cup test** — every block has a shape and a capacity. Text overflowing its cup means the
  wrong block, not a shorter label.

---

## 4 · The stack

Two lines at the top of every page. No libraries, no build step, renders years from now.

```html
<link rel="stylesheet" href="../skill/report.css">
<script src="../skill/report-table.js"></script>   <!-- only for 8+ row tables -->
<!-- theme toggle script at the foot — copy it from examples/system.html -->
```

**Relative paths, always — the stylesheet and every internal link.** An absolute path only resolves
while a server is up; open the same file from disk and the page renders unstyled with every link
dead. Relative paths work served AND from disk.

- **`report.css`** — the whole system: four semantic hues in light and dark, the type scale, the
  spacing scale, every block with its FOR / HOLDS / NEVER at the source. The **drift knobs** are
  named at the top: `--stage`, `--measure`, `--r-plate`, `--r-chip`, `--sec-gap`. Change one and
  every page linking the sheet follows.
- **`report-table.js`** — search, sortable headers, per-column filters, dismissable pills,
  clear-all, phone card mode. It reads the table already in the page, so the data lives in the
  markup and the page still reads with the script missing. Columns lock their widths on load:
  **sorting moves rows, never columns.**
- **`BLOCKS.md`** — the tagged catalog. Read it before composing.

**Every page is built only from blocks in the sheet.** A genuinely new block gets built INTO
`report.css` and listed in `BLOCKS.md` the same turn — declared and reusable, never inline as a
one-off. If a block looks wrong, fix it in the sheet so every future page improves. A one-off
`<style>` tag on a single page is how a design system dies.

### Standing craft rules

- **Hierarchy by size, weight and color only.** Never underline, box, or capitalize something into
  importance. No all-caps letter-spaced labels anywhere. No eyebrow labels — roll the word into the
  title.
- **A recommendation is an opinion and never wears a badge** (verbatim: *"why are your
  recommendations in badges?? they are not BADGES, they are your opinion"*). It uses `.r-mycall`.
- **A ruled-out row is never dimmed or struck through.** They are still comparing against it.
- **A sequence carries no numerals.** Numerals only where something must be cited by number — proof
  claims and asks. Off section headings.
- **Status is dots on pages, glyphs in chat.** On a page: the mark AND the word, filled = firm
  state, hollow = fading or pending. In a terminal message: a glyph.
- **Containment is a rule.** Every grid uses `minmax(0,1fr)`; wide tables scroll inside
  `.r-tablebox`, never the page; on a phone a comparison table becomes one card per row wearing its
  column names. **Never `overflow-x:hidden` on `html` or `body`** — it breaks scrolling in Chrome.
- **Prose runs the stage.** No measure cap: a paragraph is as wide as the page. A narrow text
  column leaves a ragged half-empty right side that reads as a mistake, and whatever fills it is
  filler. **No margin notes** — a fact that changes what your reader does goes inline in the
  sentence it changes; a fact that does not goes nowhere.
- **Blocks size to their content**, never stretch to fill the stage.
- **State fills are solid, not borders.** Bolder reads faster.
- **Verdict bars are rare** — one or two per page. *"It seems like everything has an alert
  underneath it… that's annoying."*
- **Light and dark are both first-class**, sun/moon toggle top right, dark default, choice
  remembered.
- **A screen on a page is a real HTML file**, framed live — never described in a paragraph, never
  a gray placeholder, never a screenshot. With nothing drawn yet, the first screen you need becomes
  the first file in a folder of its own (`READER.md` §4).
- **House conventions** live in `READER.md` §6. Shipped defaults: US spellings, 12-hour time, `$`,
  no emoji, no exclamation marks, never the word "successfully". `✓` and `✗` may carry a verdict;
  nothing else pictorial.

---

## 5 · The register — measured, not guessed

### The seven laws — what earns a sentence

From a blind bake-off: eleven writers wrote the same page, and the one following a long style guide
lost every duel to the same model writing with no rules at all. These are the reader's own diagnosis
of why.

1. **Say it. Never set it up.** At the end of every sentence the reader must know more than at the
   start. *"One real fix, one silent failure caught — I didn't learn anything by that. Just tell me
   what happened."* A sentence whose only job is to make them read the next one is deleted, not
   rewritten. Counting — "three changes landed" — is the same failure wearing a number. **The test:
   if the line still works with the number swapped for any other number, it is carrying nothing.**
2. **Name it in their words, before you use it.** *"If it says 'the controller', I'm already
   confused. What controller? Is that the router?"*
3. **Establish the thing before the event.** What it is, where it runs, what it does for them —
   then what happened to it. Never open mid-event with an unnamed subject.
4. **Situation, action, consequence**, in that order, in plain verbs. **One list per sentence, and
   the verb stays near its subject.** Two stacked lists force a reparse; split into two sentences.
5. **Length follows importance. Symmetry is a defect.** Blocks all the same length mean the writer
   is filling a shape instead of saying a thing. Bullets are the default; a paragraph earns itself.
6. **Only numbers they would act on. No clock times in prose, and never a relative date.** "Last
   week" goes quietly wrong when the page is opened in two months. Absolute dates, with the year,
   only where the date carries weight.
7. **Never dramatize.** No emergency, no "what nearly went wrong", no story arc. A real risk is a
   fact plus its cost, which lands harder than the drama anyway.

### The measurement

**The measurement in `READER.md` §5 is the input to every sentence on the page.** The idea is the
portable part: do not guess how your reader talks, read a few hundred of their real messages and
report back what you find. A style guide is taste; a corpus is evidence.

Four rules hold for nearly any reader and are worth keeping without measuring:

1. **Verdict word first, reason second.**
2. **Exact nouns, always** — if they could reply "which one?", it is not written yet, and the fix is
   more words, not fewer.
3. **Corrections without apology.** Errors are facts.
4. **Supply the criterion when asking them to judge**, stacked as separate lines.

The rest is theirs to set. The shipped example, measured from 13,002 messages of one person, is in
`READER.md` §5 with its provenance attached, as a demonstration of what the output of a measurement
looks like.

---

## 6 · Before serving — the self-check

Walk this on the real render. Every redesign that has ever been rejected died on execution, not
intent.

1. **Screenshot the page and look at it** — containment, typography, alignment. Never serve unseen
   pixels. Check 390 and 1440.
2. **Read every arrangement's connector aloud.** Arrows say "then", a rail says "happened", a grid
   says "and". A shape claiming something the content does not support is a defect, not a style
   choice.
3. **Read the headline cold** — the two-weeks test.
4. **Extract the h2s and read them as a paragraph** — do they carry the argument alone?
5. **Does the page break any rule it states?**
6. **Every claim has its proof beside it.** "You haven't backed up what you're saying" is an
   instant rejection.
7. **Follow-up test on every noun** — could they reply "which one?" or "what is that?"
8. One dry aside max · no enthusiasm · no process narration · counts carry their consequence.

---

## 7 · Delivery

Serve it as a clickable link, never a bare `file://` — the command is in `READER.md` §3. Pages live
in a dated folder per topic. A **sources line** — what was checked, what was not, the date, the
links — closes findings, proof and mission pages only; decisions, explainers and mockups end where
the format says.

### Self-contained — a standalone file that travels

**When the reader says "self-contained", or the page is going to anyone else, also write a
standalone copy in the same folder — same turn, no second ask.** The normal page links the shared
sheet so restyling the sheet updates every page; mailed to someone else, a linked page renders as
unstyled text. Both files ship: `index.html` stays linked, `<topic>.html` beside it travels.

```python
from pathlib import Path
src, css = Path('index.html'), Path('../skill/report.css')
link = '<link rel="stylesheet" href="../skill/report.css">'
Path('<topic>.html').write_text(src.read_text().replace(link, '<style>\n'+css.read_text()+'\n</style>'))
```

Verify it by screenshotting the standalone over `file://` with no server running — the only check
that proves it travels. Editing `index.html` later does not regenerate it; rebuild in the same turn.

**The split between a page and markdown is by reader, not by document type.** Anything the human
opens is a page: brief, plan, decision, status page, digest, findings, proof, mission map,
explainer, mockup. Markdown is only for what agents read — session notes, handoffs between two
Claude sessions, skill and rule files. A status page and a digest are for the human, so both are
pages.

---

## Source

Built for one reader over two days of rulings, then generalized. The rulings that shaped it: the
design system replaces a pile of library files · light mode stays · drawings are elements the six
kinds build from, not a seventh kind · numerals stay where something is cited, off section headings
· dots on pages, glyphs in chat · the long-table controls get built · the sources line on findings
and proof only · form follows function, for all displays on all pages · questions appear inline AND
indexed at the foot · margin notes are filler and are retired.
