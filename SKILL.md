---
name: concept-map-prose
description: >
  Writing conventions aimed at turning prose more into a concept network (away from
  'reads like a wall of text'). Extraction, not narrative:
  hierarchical bullets over paragraphs, conclusion first, examples nested under their claim
  and worked to a number, no codas, no lead-ins, a strict emphasis budget. Consult it before
  ANY prose reply, especially short conversational ones: explaining a concept, answering "what
  do you think", summarizing commits or notes, reporting findings. Applies equally to reports,
  READMEs and PR descriptions.
  In scope: reshaping raw material (notes, transcripts, drafts)
  Out of scope (does NOT apply): code or comments, product and UI copy, another person's voice or
  house style, legal text, translations, creative writing.
---

# concept-map-prose

## Principle

**The reader should not have to convert a block of prose into a concept network in their head. Do that work for them.**

- Every rule below derives from it
- This is not a preference for brevity: it is a transfer of structural work from the reader
to the writer
- Problem, briefly:
-- Information has a semantic hierarchy: important concepts, details, examples, filler text
-- Normal prose means everything is on the same level visually (wall of text)
-- Important concepts are buried on the same level as less important info
-- Reader needs to build a concept network
-- Examples of filler text (in bold):
--- 'Two reasons**, both the user's own**'
--- One asymmetry '**worth knowing about**'
--- It carries a risk **I want to state plainly**
- Solution, briefly:
-- Pull out a hierarchy of concepts
-- Structure them hierarchically
-- Minimize filler

This document is an example of the skill's proposed style. Normal prose is still fine, but to be
used frugally.
When you feel the pull to write a connecting sentence, ask whether it carries information
or only carries the reader from one idea to the next. The second kind is what this style
removes.

## Structure

- **Hierarchy over paragraphs.** Anything that is a set of things becomes a list. Prose
  survives where reasoning genuinely flows, not where facts are merely adjacent.
- **Nest to depth 3 when the content has depth 3.** Flat bullets are as much a failure as
  a wall of prose: they throw away the structure you were supposed to be encoding.
  - Level 1: the claim or definition
  - Level 2: examples, sub-cases, elaboration
  - Level 3: taxonomy leaves, the terminal distinctions
- **Single-item lists are legitimate.** Two reasons, both the user's own: the item stands
  out from the surrounding text, and it signals that the item belongs to a concept whether
  or not siblings exist yet.
- **Numbered lists only for genuine sequences** where order carries information and step N
  depends on step N-1. Everything else is bulleted. A numbered list applied to an unordered
  set tells the reader a lie about the content.
- **Section titles carry all and only the information relevant to that section.** A title
  that could sit on any section is a wasted line.
- **Linearity.** Explain a prerequisite at the point where it is first needed, never in an
  appendix or a "see above". The document should be readable start to finish with no jumps.

## Order

- **Conclusion first**, like a paper's abstract, subject to one constraint: the conclusion
  must not depend on anything defined later. If it does, define the minimum first, then
  state the conclusion.
- Within a section: **claim, then evidence, then example.**
- The exception that earns itself: open with the motivating problem when the machinery is
  meaningless without it. The user does this exactly once in 32 pages of statistics notes,
  introducing significance testing via a drug trial before any formula appears.
  
## Prose rules

This skill is mostly about structure, but writing style is affected too.

- Prefer numbers and concise formulas over text:
-- "13/40", not "thirteen out of forty"
-- "Result = PV - Load", not "We can define the result as the PV minus the load value"

## Examples

- **Nest examples under the claim they illustrate.** Never a freestanding paragraph, never
  a separate callout floating loose from its point.
- **Work them to a number or a verdict.** Not "the chi-squared test then gives a value you
  compare against the table", but the actual counts, the actual 4.8, the actual table, the
  actual n* = 11.07, and the actual conclusion.
- **Multiple examples cover distinct cases; they do not restate one case.** Three median
  examples in the user's notes cover odd cardinality, even cardinality, and the tie-heavy
  case. Four set examples cover valid, invalid-by-repetition, equal-but-reordered, and
  unequal. Each isolates one rule.
- Use `e.g.` inline to anchor an abstraction without spending a sentence on it.

## What to cut

These four account for most of the volume in over-written drafts. Look for them explicitly
before sending.

- **Codas.** The sentence after the point that explains the point's significance. If the
  point needed it, the point was badly made.
  - Cut: "...so the two rungs finally describe the same account. That distinction is what
    makes the whole exercise worthwhile."
- **Lead-ins and meta-narration.** Do not narrate the document's own structure. No "six
  changes, the first of which is the reason for the exercise", no "as we will see below",
  no "it is worth noting that".
- **Rhetorical closers.** "Only the question changed." Satisfying to write, zero
  information.
- **Restating a table in prose.** If the table shows it, the sentence beneath it should add
  something the table cannot: provenance, a caveat, a unit definition.

Do not cut: numbers, units, file paths, exact quotations, technical qualifiers, or the
honest statement of what is unknown. This style compresses rhetoric, never signal. A
finding that says "roughly 75" where the run produced 75.3 has failed at the thing the
style exists for.

## Register

Register is scoped by section type, not fixed per document.

| Section | Register |
|---|---|
| Front matter, once per document | Warm, human, metaphor and humour permitted |
| Body | Dry, brief, to the point |
| Definitions, edge cases, theorems | Formal, boxed or otherwise visually confined |

**At most one piece of front matter, at the document level, and most documents get none.**
The user's 82-page book has exactly one, and it exists to state sources, assumed reader
knowledge and typographic conventions before the reader hits the body. Its job is to set up
the contract for reading, not to warm the reader up.

This is not a licence to preface sections. A warm opener attached to each chapter is the
meta-narration rule violated in a friendlier tone. In a chat reply or a short document,
front matter is almost always wrong: start with the conclusion.

- **Informality is allowed and often better.** First and second person are fine ("we can
  now say", "notice that"). The user deliberately dropped an impersonal academic voice over
  the years because it cost readability.
- **Complete grammatical sentences.** This style is structural, not lexical. Do not drop
  articles or write telegraphic fragments. If a Caveman-type lexical compression mode is
  also active, this skill governs structure and wins on any conflict; that mode may still
  tighten word choice inside a sentence.
- Rhetorical questions work well as section pivots when the next block answers them.

## Emphasis

- **Bold marks a term being defined, or the single load-bearing claim of a section.** Not
  general emphasis, not every clause you happen to like.
- **Budget: roughly 5-7% of body text.** Measured from the user's own documents. Past that
  it stops functioning, because emphasis is a contrast effect.
- **Where the medium supports two accent colours, split them by grammatical role**, by
  explicit analogy to sentence analysis:
  - Warm (red / magenta): objects, names, subjects, concepts. Red when globally important,
    magenta when relevant only locally.
  - Cool (blue / violet): actions, tasks, properties belonging to those objects. Blue when
    important, violet when marginal or inside a list.
  - Suspend the convention inside images, code blocks and diagrams.
- In plain markdown or chat, where colour is unavailable, bold alone carries this and the
  budget matters more.

## Worked transformation

**Before** (39 words, one idea, two codas):

> Today several measurements hit a ceiling and stop counting. A very good result and an
> extraordinary one land on the same 100; a bad loss and a catastrophic one both land on 0.
> Curved scales replace the flat ones so the extremes stay distinguishable. In the test
> cohort, half the traders were pinned at a ceiling on at least one measurement.

**After** (the user's own edit):

> Today several measurements hit a ceiling and stop counting. 'Very good' = 'Extraordinary'
> = 100; 'Bad' = 'Catastrophic' = 0. Curved scales replace the flat ones so the extremes
> stay distinguishable.

What happened: the middle sentence became the equivalence it was describing, and the
closing statistic was dropped because it belonged in the section that reports measurements,
not in a card that defines a change. **Notation beats description whenever the content is
actually a relation between quantities.**

## Second worked transformation

**Before:**

> Every ranked trader gets a number from 0 to 100. It is built from seven measurements of
> their broker-verified record: how much they returned, how steadily, how far they fell at
> their worst, how long we have been watching, and how much trading sits behind it. Each
> measurement is converted to a 0-to-100 sub-score, multiplied by a published weight, and
> added up.

**After:**

> - Ranks traders on a 0-to-100 scale from seven measurements:
>   - Overall return
>   - Consistency of month-to-month returns
>   - Worst-fall from peak to trough
>   - Sortino ratio (return per unit of downside)
>   - Profit factor (money made vs money lost)
>   - Length of verified record
>   - Number of closed trades
> - Divides them into five tiers: Newbie, Rising, Steady, Pro, Elite.

What happened: a paragraph that *listed seven things in prose* became a list of seven
things. The original also only named five of the seven and blurred the rest into "and how
much trading sits behind it". **Prose hides incompleteness; a list exposes it.** That is a
second, less obvious reason to enumerate.

## Before sending, check

1. Is any paragraph secretly a list? Convert it.
2. Does any sentence restate what a table or code block already shows? Cut it.
3. Does the last sentence of any section add information, or only emphasis? Cut the second
   kind.
4. Is any description of arithmetic better written as the arithmetic?
5. Are the examples nested under their claims, and worked through to a result?
6. Does the conclusion appear before the justification, and does it depend on anything
   defined later?
7. Is bold doing real work, and is it under ~7%?
8. Did anything numeric, qualified or uncertain get smoothed away? Restore it.
