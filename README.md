# divi — Award-Level Animated Website Builder (Claude skill)

**divi** is a Claude Code / Claude.ai skill that generates **Awwwards / Site-of-the-Day-grade animated websites** in React (Next.js or Nuxt) from just two files you provide per project: `design.md` (visual system) and `brief.md` (content + scope). The skill supplies everything else — the motion vocabulary, transitions, build rules, and the framework decision.

## What you provide
- **design.md** — palette, typography, spacing, tokens, components, feel
- **brief.md** — name, type, audience, pages, sections, real copy, goals

## What the skill provides
- **Animation library** — 25 categories, ~180 effects, each a compressed prompt with exact params
- **Transitions library** — 53 page / section / overlay / loader / media transitions
- **Master build prompt** + 6 vertical **scenario prompts** (insurance, e-commerce, real estate, crypto, gaming, general)
- **Rules baked in** — anti-slop, 60fps (transform/opacity only), SSR-safe, accessibility (prefers-reduced-motion, WCAG AA)
- **Framework decision** — Next.js vs Nuxt chosen per project complexity

## Install
Download **`divi-skill-package.skill`** (or **`.zip`**) from this repo, then either:
- **Claude.ai** → Settings → Capabilities → Skills → **Upload skill** (use the `.zip`), or
- Unzip into your project at **`.claude/skills/divi/`**

The package contains:
```
SKILL.md
references/   animation-library · transitions-library · master-prompt · scenario-prompts · teardowns/
templates/    design.template.md · brief.template.md
examples/     5 worked design.md + brief.md pairs + a studio prompt
```

## Usage
1. Put `design.md` and `brief.md` in your repo (copy from `templates/` if starting fresh).
2. Invoke the skill: **`/divi`** — or say *"build the site from design.md and brief.md."*
3. It picks Next.js or Nuxt, states the design brief + technique IDs per section, then builds — preloader → hero → scroll → section/page transitions — anti-slop and 60fps.

## License
MIT — use freely. The example briefs are fictional placeholders.
