# Contributing

Thanks for wanting to make this better. It's a set of Markdown files, so
you don't need to be a developer to help.

## Fixing or improving the text

If a step is unclear, wrong for you, or you have a sharper way to put it,
edit the relevant file under `docs/en/` (or `docs/ru/`) and open a pull
request. Small fixes — a typo, an awkward sentence — don't need an issue
first; just send the PR.

A few notes on the writing, so edits stay in the same voice:

- Plain and direct. Second person ("you"), short sentences, no jargon.
- Honest over motivational. No hype, no guilt-tripping, no "just do it."
- If you add a claim about how the brain or behaviour works, back it with
  a real source and add it to `docs/en/11_sources.md` (and the Russian
  page) with a link to the original study.

## Previewing your changes

```bash
pip install -r requirements.txt
mkdocs serve
```

Open `http://127.0.0.1:8000`. Files under `docs/` reload as you save.
Before opening a PR, run a strict build to catch broken links and config
problems:

```bash
mkdocs build --strict
```

## Adding a translation

Open an issue first so we can agree on the language code and split the
work. The mechanics:

1. Copy `docs/en/` to `docs/<lang>/` (for example `docs/de/`) and
   translate the files. Keep the filenames identical — the language
   switcher and the internal links depend on them matching.
2. In `mkdocs.yml`, add the language under `plugins → i18n → languages`,
   and translate the navigation labels under that language's
   `nav_translations`.
3. Run `mkdocs build --strict` to confirm both the new language and the
   existing ones still build cleanly.

## Ground rule

Keep it free and open. This exists so people can get out of a habit that
costs them time, not so anyone can sell it back to them.
