# concept-map-prose

A [Claude Code](https://claude.com/claude-code) skill that makes Claude write prose you read by extraction rather than by narrative: hierarchical bullets over paragraphs, conclusion first, examples worked through to a number, no codas or lead-ins, a bounded emphasis budget.

The governing principle, from `SKILL.md`:

> The reader should not have to convert a block of prose into a concept network in their head. Do that work for them.

This is not a brevity rule. A long document in this style is fine; what it removes is the sentence that only carries the reader from one idea to the next.

## What it changes

- **Structure.** Sets of things become nested lists, to depth 3 where the content has depth 3. Prose survives only where reasoning genuinely flows.
- **Order.** Conclusion before justification, subject to the constraint that the conclusion cannot depend on anything defined later.
- **Examples.** Nested under the claim they illustrate and worked to an actual value, not "you then compare against the table".
- **Cuts.** Codas, meta-narration, rhetorical closers, and prose that restates a table.
- **Emphasis.** Bold marks a term being defined or a section's single load-bearing claim, budgeted at roughly 5-7% of body text.

## Scope

- **Applies to:** any prose reply, including short conversational ones, plus reports, READMEs and PR descriptions.
- **Does not apply to:** code and comments, product and UI copy, another person's voice or house style, legal text, translations, creative writing.

## Install

Clone into your personal skills directory, with the directory name matching the skill name:

```bash
git clone https://github.com/DvD12/claude-skill-concept-map-prose.git ~/.claude/skills/concept-map-prose
```

On Windows (PowerShell):

```powershell
git clone https://github.com/DvD12/claude-skill-concept-map-prose.git "$env:USERPROFILE\.claude\skills\concept-map-prose"
```

Claude Code discovers the skill on next start. Invoke it explicitly with `/concept-map-prose`, or add a line to `~/.claude/CLAUDE.md` so it is consulted without being asked:

```markdown
- Use the "concept-map-prose" skill if available.
```

For a project-scoped install, clone into `.claude/skills/concept-map-prose` inside the repository instead.

## Adapting it

The conventions are one person's, derived from roughly a decade of technical writing (2016-2024), and the worked transformations in `SKILL.md` use that person's own edits. Fork and change the rules rather than the examples: the examples exist to show what each rule does to a real paragraph, so a rule edited without its example loses its calibration.

## License

MIT. See [LICENSE](LICENSE).
