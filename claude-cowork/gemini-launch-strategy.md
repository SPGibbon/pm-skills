# Go-to-Market Plan: PM Skills on Gemini CLI

**Launch date:** Target first public install path in Q4 2026 (ship when one-command install works, not on a calendar date).
**Type:** Market expansion — same marketplace, new agent surface.
**Stage:** Pre-launch. Claude Code and Claude Cowork already ship; Gemini CLI is documented as copy-skills-only.
**Sources used:** `/plan-launch` plus `beachhead-segment`, `ideal-customer-profile`, `gtm-strategy`, `gtm-motions`, `growth-loops`, `positioning-ideas`, `value-prop-statements`, `north-star-metric`, and `competitive-battlecard`. Cowork analog is the install path in the repo README (Customize → Browse plugins → Add marketplace from GitHub → `phuryn/pm-skills`), because a local folder named "Claude cowork" was not attached to this environment.

---

## Why this launch exists

Cowork already has the winning distribution pattern: a non-developer adds a GitHub marketplace once and gets all nine plugins, skills, and slash workflows. Gemini users get the same skill files, but the path is a `cp` loop into `~/.gemini/skills/`. That is not a launch. It is a footnote.

Gemini CLI now supports Agent Skills (`SKILL.md` + description-triggered load), `gemini skills install`, and extensions that bundle a `skills/` tree behind `gemini-extension.json`. It still does **not** install from `.claude-plugin/marketplace.json` (open request: [google-gemini/gemini-cli#28428](https://github.com/google-gemini/gemini-cli/issues/28428)). Slash commands remain Claude-specific.

The launch is therefore two bets:

1. **Distribution bet:** Make Gemini as close as possible to the Cowork one-step install without waiting for native marketplace support.
2. **Workflow bet:** Translate the 42 command workflows into Gemini-native invocations so PMs do not lose `/discover`, `/plan-launch`, and `/write-prd` just because they switched harnesses.

---

## Beachhead segment

### Candidates scored (1–5)

| Segment | Burning pain | Willingness to pay | Winnable | Referral | Total |
|---------|-------------|--------------------|----------|----------|-------|
| **A. Dual-harness PMs** — already use Cowork/Code for PM work and Gemini CLI for Google-stack engineering | 5 | 4 | 5 | 5 | **19** |
| B. Gemini-native PMs at Google Cloud / Firebase / Android shops who never installed Cowork | 4 | 4 | 4 | 4 | 16 |
| C. "Everyone on Gemini CLI" (engineers, hobbyists, students) | 2 | 2 | 2 | 3 | 9 |
| D. Enterprise PM orgs standardizing one agent across the company | 4 | 5 | 2 | 3 | 14 |

### Primary beachhead: Segment A — dual-harness PMs

**Who:** Individual product managers and product-minded engineers who already trust PM Skills on Cowork or Claude Code, and who already have Gemini CLI on the machine because their team ships on Google Cloud, Firebase, Android, or Gemini APIs.

**Why them first:**

- **Burning pain:** They already know the workflows. The gap is context switching — discovery in Cowork, implementation in Gemini — so PRDs and assumption maps never land in the repo the engineer is actually using.
- **Willingness to pay:** Time, not license. They have already paid the install cost once. A second install that feels like Cowork is an easy yes; a 69-folder copy script is an easy no.
- **Winnable:** Unique access via the existing Cowork user base and README. Competitors on Gemini are coding-skill packs, not a PM operating system. You do not need 60% of all Gemini users; you need most of the people who already starred or installed PM Skills and also run Gemini CLI.
- **Referral:** They sit between PM communities (Product Compass, Cowork) and engineering communities (Gemini CLI, Firebase, internal Google-stack Slack). One successful install becomes a team default via `.gemini/skills` or a workspace extension in the repo.

**Size (order-of-magnitude, unvalidated):**

- **TAM:** PMs and founders using any agent CLI or Cowork-class tool for product work.
- **SAM:** That group who also use Gemini CLI at least monthly.
- **SOM (90 days):** Dual-harness users already in the PM Skills / Product Compass orbit. Aim to *dominate this niche* (majority of known dual-harness installs), not Gemini CLI as a whole.

### Adjacent expansion (after beachhead)

1. Segment B — Gemini-only PMs in Google-stack companies (same motion, new proof: "works without Claude").
2. Workspace-level install (checked-in `.gemini/skills` or extension) so a whole product trio shares the same PM OS.
3. If/when Gemini ships marketplace catalogs, promote the existing `marketplace.json` rather than maintaining a parallel catalog forever.

---

## Ideal customer profile

| Attribute | Definition |
|-----------|-----------|
| Company size | 20–2,000 people; product org exists; not a solo weekend hacker |
| Industry | B2B SaaS, developer tools, Google Cloud / Firebase / Android product teams |
| Geography | English-first; remote-friendly; already in GitHub + CLI workflows |
| Decision maker | The PM themselves (install is personal or repo-level). Engineering manager is influencer, not buyer. |
| Key JTBD | "When I am in Gemini CLI doing product work, help me run the same structured PM process I already trust — discovery, strategy, PRD, launch — without switching apps or inventing a prompt." |
| Current solution | Generic Gemini prompts; coding skills (Firebase, security, code-review); copy-paste from Cowork chats; Notion PM templates |
| Qualification signal | Has Gemini CLI installed **and** can name a recent PRD, experiment, or launch they ran with an LLM. Bonus: already added `phuryn/pm-skills` in Cowork. |
| Disqualify | People who want Gemini to write code faster, or who expect `/slash` commands on day one with zero translation. Also disqualify "install all AI skills on earth" collectors — they will not retain. |

### JTBD (detail)

- **Functional:** Produce a defensible PM artifact (PRD, GTM plan, interview script) inside the same CLI as the codebase.
- **Emotional:** Feel like a rigorous PM, not someone who got lucky with a prompt.
- **Social:** Share a markdown plan in GitHub that engineering will actually read.

### Behaviors

- Discover via GitHub README, Product Compass, or a teammate's `gemini extensions install` line.
- Evaluate in one afternoon: install → `/skills list` → run discovery or a PRD on a real idea.
- Buy = keep the extension auto-updating. No procurement.
- Adoption is high if the first workflow completes without reading plugin architecture.

---

## Positioning and messaging

### Positioning statement

For product managers who already run Gemini CLI (and often Cowork too) and need structured product decisions in the same place they ship, **PM Skills** is the PM operating system for agents — 69 skills and 42 workflows from discovery through launch. Unlike generic Gemini coding skills or a `cp` of markdown files, it is the same curated marketplace that Cowork installs in one step, adapted to Gemini's skill and extension model.

### Positioning options considered

| Idea | Statement | Verdict |
|------|-----------|---------|
| **1. Same OS, new harness** | The PM operating system Cowork users already have, now native to Gemini CLI. | **Primary.** Lowest education cost for the beachhead. |
| 2. Anti-vibes PM | The only Gemini skill pack that refuses to skip discovery, assumptions, and GTM. | Strong supporting message; too negative as the headline. |
| 3. Google-stack PM | Built for PMs whose engineers live in Gemini, Firebase, and Cloud. | Use for Segment B later; too narrow for dual-harness launch. |
| 4. Marketplace, not a gist | A versioned, tested catalog — not a random `SKILL.md` dump. | Proof point, not positioning. |
| 5. Commands without slashes | Full PM workflows on Gemini even though `/plan-launch` is Claude-only. | Feature positioning for the workflow-translation workstream. |

### Key messages by stakeholder

| Audience | Message | Proof point |
|----------|---------|-------------|
| Dual-harness PM | Stop splitting product thinking across Cowork and Gemini. Same skills, in the CLI your engineers already have open. | Cowork marketplace install vs. one Gemini extension command. |
| Gemini-only PM | Gemini is excellent at building. These skills make it excellent at deciding what to build. | `/discover` → `/write-prd` → `/plan-launch` chain, invoked in plain language. |
| Eng manager / tech lead | Check this into the repo so PMs and engineers argue from the same PRD, not two chat logs. | Workspace skills under `.gemini/skills` or `.agents/skills`. |
| Product Compass / Cowork user | You already know the plugins. Gemini was the missing surface, not a new methodology. | Identical `SKILL.md` files; README already lists Gemini. |

### Value proposition statements

1. **Marketing (beachhead):** PM Skills on Gemini CLI gives dual-harness product managers the same discovery-to-launch system they use in Cowork, without leaving the CLI their engineering team already runs.
2. **Sales / advocacy:** Teams get a shared, versioned PM skill catalog — beachhead, ICP, GTM, PRDs, shipping audits — instead of each person prompting Gemini from scratch.
3. **Onboarding:** After one extension install, ask Gemini to run product discovery on your idea; it should load the discovery skills and pause between steps the way `/discover` does on Cowork.

---

## Channel strategy and GTM motions

### Motion scores (1–10)

| Motion | Score | Why |
|--------|-------|-----|
| **Community** | 9 | Gemini CLI GitHub, Cowork users, Product Compass, r/ProductManagement, AI PM Discords. Lowest CAC. |
| **PLG** | 9 | Install is the product. Time-to-value is one workflow. Auto-update extensions are the "subscription." |
| **Inbound** | 8 | README + a Gemini-specific install section + one worked example (`/plan-launch` analog). SEO for "Gemini CLI PM skills". |
| **Partners** | 7 | Gemini CLI extension gallery / example repos; Firebase/agent-skills adjacency; Agent Skills standard (`.agents/skills`). |
| Outbound | 3 | No sales team; ACV is zero. |
| Paid | 2 | Wrong economics for an MIT catalog. |
| ABM | 2 | No named enterprise motion yet. |

**Motion stack:** PLG (install) + Community (proof) + Inbound (findability). Partners as a 60-day add-on (get listed wherever Gemini shows official/example extensions).

### Channel tactics

| Channel | Tactic | Reach | Cost | Priority |
|---------|--------|-------|------|----------|
| GitHub README | Promote Gemini from "other assistants / copy loop" to a first-class install next to Cowork | All visitors | Low | P0 |
| Gemini extension install | `gemini extensions install <url>` (or documented `gemini skills install` once a flattened path exists) | CLI users | Eng time | P0 |
| Product Compass / existing Cowork users | "If you use Gemini CLI at work, here is the one-step port" | Existing audience | Low | P0 |
| Gemini CLI community (GitHub discussions, Discord) | Show a real `/plan-launch`-style session, not a skill dump | High-intent | Low | P1 |
| Workspace default | PR that adds the extension or `.agents/skills` to an internal product repo | Team expansion | Low | P1 |
| Extension directories / example lists | Submit once install is one command | Discovery | Low | P2 |

---

## Product work that *is* the launch (do this before announcing)

Cowork's GTM works because install is a product feature. Gemini launch fails if we only write docs.

| Workstream | Outcome | Notes |
|------------|---------|--------|
| **1. One-command install** | A Gemini user runs one command and gets all skills | Root `gemini-extension.json` plus a flattened `skills/` tree (build step from `pm-*/skills/`), **or** a thin companion repo. Do not ask people to copy 69 folders. Track [gemini-cli#28428](https://github.com/google-gemini/gemini-cli/issues/28428) so a future marketplace add can replace the shim. |
| **2. Workflow skills** | The 42 commands are usable without Claude `/slash` | Highest-traffic workflows first: discover, write-prd, plan-launch, strategy, north-star, ship-check. Each becomes a Gemini-activatable skill (or a single `pm-workflows` skill that lists the chains). Codex README already describes this pattern in prose — Gemini needs it as loadable skills. |
| **3. README parity** | Gemini sits beside Cowork, not under "other AI assistants" | Same promise: all plugins, then honest delta ("skills auto-load; workflows via named skills, not `/commands`"). |
| **4. Smoke path** | A 10-minute script: install → list skills → run one discovery prompt → confirm a skill loaded | Treat install like a product. If Gemini does not activate `gtm-strategy` on "launch strategy for X", the launch is broken. |
| **5. Name collision pass** | Skill `name` values stay unique and Gemini-safe | Gemini forbids some characters in names; last-wins if duplicates exist across plugins. |

Keep plugins independent for Claude. The Gemini shim is an *export*, not a tenth plugin that other plugins import.

---

## Launch timeline

| Phase | Timing | Actions | Owner |
|-------|--------|---------|-------|
| **Pre-launch** | Until one-command install + 6 workflow skills pass smoke | Build extension/flatten script; convert discover, write-prd, plan-launch, strategy, north-star, ship-check; README draft on a branch; 5 dual-harness users dogfood | Maintainer + anyone shipping the Gemini shim |
| **Launch week** | When smoke path is green | Merge README; pin a release note under Unreleased then version bump when ready; post to Product Compass / GitHub; reply in Gemini CLI community with the install command and one recorded workflow | Same |
| **Post-launch (days 1–30)** | | Collect install failures; watch whether skills auto-load; convert next command tier (interview, competitive-analysis, red-team-prd); invite one partner listing | Same |
| **Post-launch (days 31–90)** | | Workspace install guide for teams; Segment B messaging ("no Claude required"); drop the copy-loop as the primary Gemini path; revisit native marketplace if 28428 ships | Same |

### Launch-week narrative (keep it small)

1. Dual-harness PM installs the extension.
2. Asks Gemini: "Run product discovery on [their real idea]: brainstorm, map assumptions, prioritize, design experiments — pause between steps."
3. Gets a structured artifact in the repo, not a chat they cannot share.

That is the demo. Not a feature matrix.

---

## Success metrics

**Business game:** Productivity (complete better product work faster, in-flow).

**North Star:** Number of Gemini sessions per week in which a PM Skills skill is actually activated (not merely installed).

Why this one: customer-centric, leading, actionable (install UX + description quality + workflow skills all move it), not vanity stars.

| Input metric | 30-day target | 90-day target |
|--------------|---------------|---------------|
| Successful one-command installs (self-reported + Git clone/extension telemetry if available) | 25 beachhead users | 100 |
| Skill-activated sessions (proxy: GitHub issues/discussions + 10 qualitative interviews if no telemetry) | 15 people completed ≥1 real workflow | 50 people completed ≥1; 20 completed ≥3 |
| Dual-harness conversion (Cowork users who also install Gemini path) | 10 from existing audience | 40 |
| Time-to-first-workflow (install → first saved markdown artifact) | < 15 minutes median in dogfood | < 10 minutes |
| README Gemini path is copy-loop | Must be **false** at launch | Stay false |

Awareness (stars, impressions) is a hygiene metric, not the North Star.

---

## Growth loops (post-install)

| Loop | Fit | How it would work |
|------|-----|-------------------|
| **Usage (primary)** | High | User runs a workflow → writes `docs/prd.md` or a GTM plan into the repo → reviewers see structured PM output → they install the same extension. |
| **Collaboration (secondary)** | High | Workspace skills in git mean inviting a teammate to the repo *is* the invite to the product. |
| Viral | Medium | Shareable artifacts (PRDs, battlecards) are markdown, not Gemini-proprietary. Good, but not a consumer social graph. |
| Referral | Low | No credits to give. Status ("we run PM Skills") is enough if the artifact quality is visible. |
| UGC | Low until people publish their own PM skills into the marketplace. | Later. |

**30–60–90 for loops:** 30 = make the artifact the share object (default "save as markdown" already in `/plan-launch`). 60 = workspace install snippet in the README. 90 = one public example repo with PM Skills + a real (sanitized) discovery/PRD trail.

---

## Competitive notes (not a full battlecard)

| Alternative | They win when | We win when |
|-------------|---------------|-------------|
| Generic Gemini prompts | User wants a one-off paragraph | User wants a repeatable PM system |
| Firebase / Google agent-skills | User is implementing Google products | User is deciding product strategy |
| Coding skill packs (security, PR, tests) | The job is the codebase | The job is the market, the user, the launch |
| Staying on Cowork only | User never opens a CLI | The work has to live next to `git` and Gemini |
| Copying `SKILL.md` files by hand | Maintainer does not ship an extension | User expects Cowork-like install |

**Landmine questions for dogfood interviews:** "When you last wrote a PRD in Gemini, which skill or template did it load?" If the answer is "none," the current README path has already failed.

---

## Risks and mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Gemini still cannot install a multi-plugin marketplace | High (today) | High | Ship an extension/flatten shim; do not block launch on 28428 |
| Skills exist but never auto-load (weak descriptions) | Medium | High | Smoke-test trigger phrases; keep frontmatter trigger-rich as CLAUDE.md already requires |
| Users expect `/plan-launch` and bounce | High | Medium | Launch copy states the delta; ship workflow skills on day one |
| Flattened `skills/` diverges from plugin directories | Medium | High | Generate from source in CI; do not hand-edit the Gemini tree |
| Cross-plugin command references leak into Gemini workflows | Medium | Medium | Same rule as CLAUDE.md: natural language follow-ups only |
| "Launch Gemini" is misread as launching Google Gemini the consumer app | Low | Low | Title every artifact "PM Skills on Gemini CLI" |
| Dogfood sample is too Claude-centric | Medium | Medium | Include at least two Gemini-only PMs before public launch |

---

## Pricing alignment

MIT, GitHub-distributed, no seat license. GTM motion is PLG + community. "Price" is install friction and context-window cost. The Cowork analog already proved people will install nine plugins when friction is near zero. Charge nothing; spend the budget on making Gemini friction match Cowork.

---

## Expansion plan

After the beachhead is clearly using Gemini for real PM artifacts:

1. **Gemini-only PMs** in Google-stack companies — message: you do not need Claude to get the OS.
2. **Team workspace default** — one `gemini extensions install` in the engineering README.
3. **Native marketplace** — collapse the shim if Gemini adds catalog install.
4. **Command parity** — remaining workflows as skills, not a promise of Claude `/` syntax.

---

## Assumptions to validate before calling it launched

1. Dual-harness PMs will install a Gemini extension if it is one command (not if it is a script in a gist).
2. Gemini will activate `gtm-strategy` / discovery skills from conversation, not only from `/skills`.
3. Six translated workflows cover 80% of first-week usage.
4. The Cowork audience will redistribute the Gemini path without paid amplification.

If (1) or (2) fails in dogfood, do not announce. Fix install or descriptions.

---

## Further reading (from the skills used)

- [5 GTM Principles You Should Know as a PM](https://www.productcompass.pm/p/5-gtm-principles-with-frameworks-templates)
- [OpenAI’s Product Leader Shares 3-Layer Distribution Framework To Win Mind & Market Share in the AI World](https://www.productcompass.pm/p/distribution-framework-ai-products)
- [Product-Led Growth 101, Part 1/2](https://www.productcompass.pm/p/product-led-growth-101-12)
- [How to Design a Value Proposition Customers Can't Resist?](https://www.productcompass.pm/p/how-to-design-value-proposition-template)
- [The North Star Framework 101](https://www.productcompass.pm/p/the-north-star-framework-101)
