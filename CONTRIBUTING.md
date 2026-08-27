# Contributing

Thanks for helping make these skills better. Contributions we love:

- **Corrections** — a rule that changed in this year's final rule, a deadline that
  moved, a term of art used wrong. Open an issue with a citation (CMS final rule,
  RAI manual section, MLN article) and we'll fix it fast.
- **New workflows** — a checklist or template your facility actually uses that a
  skill should produce. Open an issue describing the input → output.
- **New packs** — propose the pack in an issue first so we can agree on scope.

## Ground rules for skill content

1. **Public knowledge only.** CMS methodology, published manuals, general industry
   practice. Never paste content from commercial products, proprietary payer
   documents, or anything under NDA.
2. **No PHI, ever.** Examples use fictional patients ("Patient A") and fictional
   organizations ("Example Hospital", "Sample Health Plan").
3. **No year-specific dollar figures.** Rates and thresholds change every fiscal
   year. Skills should instruct Claude to ask for or look up current figures, not
   hardcode them.
4. **Accurate capture, never upcoding.** Anything touching coding or billing must
   reinforce that codes and claims reflect what is genuinely documented.
5. **Keep the skill format.** Each skill lives at
   `plugins/<pack>/skills/<skill-name>/SKILL.md` with YAML frontmatter
   (`name` in kebab-case matching the directory, `description` under 1024
   characters, `license`), an imperative workflow body under ~450 lines, long
   reference tables in a `references/` folder beside it, and a closing
   `## Disclaimer` section. This is the open
   [Agent Skills](https://agentskills.io) format, so the repo stays
   installable both as Claude Code plugins and via `npx skills add` — don't
   add frontmatter fields outside that spec.
6. **Skills must stand alone.** Users can install a single skill without the
   rest of the repo (e.g. via the skills CLI), so refer to other skills as
   "the companion `<skill-name>` skill (if installed)" — never assume the
   whole marketplace is present.

## Testing a change

From a checkout, add the local marketplace and install your pack:

```
/plugin marketplace add ./snf-skills
/plugin install <pack>@snf-skills
```

Then run a realistic prompt against it (a fictional referral packet, a sample
contract) and check the output. `claude plugin validate ./plugins/<pack>` catches
manifest problems, and `npx skills add . --list` from the repo root confirms
every skill is still discoverable by the open-format skills CLI.

## License

By contributing you agree your contribution is licensed under the repository's
MIT license.
