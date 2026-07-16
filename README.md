# ScrollStop

A free, open method for getting off short-form video — Reels, Shorts,
TikTok. It comes out of my own experience with the problem and leans on
published research instead of the usual "just delete the app" advice.

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](#license)
[![Deploy](https://github.com/DenisDrobyshev/ScrollStop/actions/workflows/deploy.yml/badge.svg)](https://github.com/DenisDrobyshev/ScrollStop/actions/workflows/deploy.yml)
[![Built with Material for MkDocs](https://img.shields.io/badge/built%20with-Material%20for%20MkDocs-526cfe.svg)](https://squidfunk.github.io/mkdocs-material/)

**Read it online:** https://denisdrobyshev.github.io/ScrollStop/
&nbsp;·&nbsp; English (default) &nbsp;·&nbsp; [Русская версия](https://denisdrobyshev.github.io/ScrollStop/ru/)

## Why this exists

For a while I couldn't sit through a three-minute video without wanting
to skip ahead. I'd open an app to check one thing and look up forty
minutes later with no memory of what I'd watched, and reading a book
had started to feel like hard physical work. Instead of guessing at
willpower fixes, I went and read what the research actually says about
what short-form video does to attention, and turned it into a plan I
could follow. This is that plan, cleaned up so someone else can use it.

It's not a product and there's nothing to buy. It's a set of documents
you can read, follow, fork, or send fixes to.

## What's inside

- What's actually going on in your brain while you scroll, explained
  through the real research — dopamine as anticipation, variable reward,
  opponent-process theory.
- A plain checklist to gauge how far into it you are.
- A concrete three-week program: first observe your patterns, then add
  friction, then replace the habit with something that meets the same
  need.
- A separate, honest chapter on relapses, because they happen to
  everyone and that's where most people quit.
- Sources for every claim, linked to the original studies so you can
  check them yourself.

## The method in brief

If you only want the actions, the whole thing lives on one page:
[The Plan](https://denisdrobyshev.github.io/ScrollStop/protocol/).

| Stage    | What you do                                                        |
| -------- | ------------------------------------------------------------------ |
| Week 1   | Count every time you open the app. Change nothing. Find your triggers. |
| Week 2   | Kill notifications, hide the app, add a few seconds of friction.   |
| Week 3   | Decide your replacements in advance and reach for them first.      |
| Ongoing  | Treat slips as data, not failure. Keep the phone out of the bedroom at night. |

## How to read it

It's written to be read in order — each chapter builds on the last, so
skimming it out of sequence loses most of the point. If you want to
start doing before you finish reading, go straight to The Plan and use
the chapter links from there.

The raw Markdown lives in `docs/en/` and `docs/ru/` if you'd rather read
it in your editor. The [hosted site](https://denisdrobyshev.github.io/ScrollStop/)
is the same content with search and a language switcher.

## Running it locally

The site is Markdown rendered with MkDocs. To preview changes before
opening a PR:

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open `http://127.0.0.1:8000`. Anything you edit under `docs/`
reloads live.

## Contributing

If a step didn't work for you or you have a better version of it, open a
PR. To add a translation into another language, open an issue first so
we can sort out the folder layout together.

## Disclaimer

This is not a replacement for therapy. If short-form video is seriously
getting in the way of your work, your relationships, or your daily life,
talk to a professional as well as reading any of this.

## License

MIT. Use it however you like — just don't pass off the underlying
research as your own.
