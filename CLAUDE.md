# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

DAGA ("Make Direct Reactions Great Again") is a **static two-page parody-meets-manifesto site** arguing that LLM-assisted "vibe research" can revive the direct nuclear reactions subfield. Deployed via **GitHub Pages** at `vibeinscience.com` (CNAME file at repo root, A records + `www` CNAME pointed at `jinleiphys.github.io`).

There is **no build step, no framework, no package.json**. Each page is a single self-contained `.html` file with inline CSS. Editing HTML and pushing to `main` is the entire deploy pipeline — Pages picks it up automatically.

## Files

- `index.html` — landing page (DAGA direct-reactions billboard): brand, CTA, links out to manifesto and Nuclear HQ
- `nuclear.html` — the broader "Nuclear Physics HQ" parody page (hero slogan, Trump-style speech, 8 quote cards, SAD ticker). Previously served as `index.html`; now linked from DAGA as the wider-field companion page
- `why.html` — manifesto subpage: 6 chapters arguing why direct reactions can be revived via vibe research, written in first-person "Boss" voice with embedded "Truth Social" pull-quotes and real arXiv citations
- `legends.html`, `lexicon.html`, `barrier.html` — supporting subpages (Hall of Fame, glossary, Coulomb-barrier calculator)
- `CNAME` — contains `vibeinscience.com`; managed by GitHub Pages, don't remove
- `README.md` — deploy/DNS instructions for the custom domain

## Voice and content rules (load-bearing — violating these has been corrected before)

1. **Trump parody voice, but never write "Donald"** or reference any real politician by name. The persona is always "The Boss."
2. **Academic internationalism is non-negotiable.** No flags, no country names (especially no "China"), no US-centric framing. The disclaimer explicitly states *"Science knows no borders."*
3. **Address convention:** when others speak TO the Boss they say *"Professor"*; when the Boss speaks TO others he says *"Sir"*. Getting this backwards is a recurring mistake.
4. **No em-dashes (—)** anywhere in visible copy. The user dislikes them. Use periods, commas, or restructure.
5. **The user's 14-papers-in-4-months LLM track record is real but currently off-limits on the public site** — do not add it unless the user asks. It is the strongest possible evidence for the thesis but they're holding it back for now.
6. **Thesis of the site is specifically *vibe research* (LLMs as collaborators in the paper-writing/research workflow), NOT "ML for physics"** (neural network potentials, emulators, etc.). Do not drift into the latter — it's a different argument and the user explicitly rejected that framing.

## Visual style

Both pages share a MAGA-parody palette: `--red: #d92b4a` (or `#b31942` on index), `--blue: #0a2a5e`/`#0a3161`, `--cream: #f5f0e1`, `--gold: #ffd54a`, `--ink: #0b0b0b`. Impact/Arial Black for display, Georgia for quotes and serif body, Courier New for monospace accents. Hard black borders + offset box-shadows (`6px 6px 0 var(--ink)`) are the signature motif — keep that neo-brutalist feel when adding components.

`why.html` uses a darker, richer treatment than `index.html` (linear-gradient hero, giant roman-numeral chapter watermarks, "TRUTH SOCIAL · THE BOSS" pull-quote cards). When editing, preserve the visual hierarchy between the two pages: `index.html` is the billboard, `why.html` is the argument.

## Local preview and deploy

```bash
open index.html          # preview landing page in default browser
open why.html            # preview manifesto
```

Deploy is just `git push origin main`. GitHub Pages serves from `main` / root. Custom domain + HTTPS are already configured in the repo Settings — do not touch `CNAME` or add workflow files unless the user explicitly asks.
