# Fieldcraft — Blog Workflow Plan
*Generated 2026-03-09 · Living document*

---

## Overview

Fieldcraft publishes writing about craft, skill, and transferable wisdom across disciplines. The editorial engine runs on a five-stage pipeline, a weekly publishing cadence, and a growing roster of disciplines — each treated as a domain with its own vocabulary, its own mistakes, and its own lessons that apply everywhere else.

---

## Disciplines

Organized by current depth in the ideas backlog. Asterisks mark disciplines with committed content.

### Tier 1 — Active (ideas + outlines exist)
| Discipline | Symbol | Topics in Backlog | Notes |
|---|---|---|---|
| Fly Fishing | 🎣 | 5 (launch series) + 3 additional | Hayes's primary; 5 pieces already stubbed |
| Woodworking | 🪵 | 3 | Well-developed backlog |
| Aviation / Flying | ✈️ | 3 | Strong cross-reference potential |
| Cooking / Baking | 🍞 | 3 | Mise en place essay is a natural early feature |
| Surgery / Medicine | 🏥 | 3 | High-concept; distinct voice required |

### Tier 2 — Developing (concepts, no outlines)
| Discipline | Symbol | Topics in Backlog | Notes |
|---|---|---|---|
| Trail Running | 🏃 | 2 | Pacing, bonk — good for Field Notes |
| Ceramics | 🏺 | 2 | Centering, patience themes |
| Jazz / Music | 🎷 | 2 | Structure vs. improvisation — rich |
| Rock Climbing | 🧗 | 2 | Route reading, commitment |
| Farming | 🌾 | 2 | Seasons, soil, patience |
| Beekeeping | 🐝 | 2 | The hive as a system; autonomy |
| Sailing | ⛵ | 2 | Reading wind, trim, patience |
| Glassblowing | 🫧 | 2 | Heat windows, irreversibility |

### Tier 3 — On Deck (named in brand materials, not yet developed)
| Discipline | Symbol | Status |
|---|---|---|
| Navigation / Wilderness | 🧭 | Named in disciplines.md; pairs well with Aviation |
| Survival Skills | 🪓 | Named in disciplines.md; good for Field Notes |
| History | 📜 | Named in disciplines.md; cross-reference substrate |
| Architecture | 🏛️ | Natural fit; not yet listed |
| Martial Arts | 🥋 | High transferability potential |
| Leatherworking | 🧵 | Complements woodworking audience |

**Total active + developing: 13 disciplines | Total including Tier 3: ~19**

---

## Content Formats

Per the brand brief, Fieldcraft runs five format types on a weekly cadence:

| Format | Cadence | Length | Voice Mode | Example |
|---|---|---|---|---|
| **Feature Essay** | 2×/week | 1,200–2,000 words | Narrative first, lesson emerges | "Reading the Water" |
| **Field Note** | 2×/week | 400–700 words | Tight, specific, practitioner-direct | "The Drag-Free Drift" |
| **Interview** | 1×/week | 1,000–1,500 words | Practitioner in their own voice | TBD |
| **Cross-Reference** | 1×/week | 800–1,200 words | Two disciplines, one insight | "Mending the Line" |
| **Weekend Read** | 1×/week | 1,500–2,500 words | Long-form, richer narrative | "Why I Fish Alone" |

**Weekly publish cadence: 7 posts/week** (sustainable target; can throttle to 5 at launch)

---

## Post Pipeline — From Idea to Published

```
ideas.md → 01-outlines/ → 02-drafts/ → 03-review/ → 04-approved/ → src/content/blog/
```

### Stage 0: Backlog (`drafts/ideas.md`)
- Every idea starts here with a working title, format, discipline, and core insight
- Status tracked by emoji: 💡 raw → 📝 outlined → ✍️ drafted → 👀 in review → ✅ published / ❌ passed
- Nothing gets deleted — the backlog is a permanent record

### Stage 1: Outline (`drafts/pipeline/01-outlines/slug.md`)
Each outline contains:
- Working title + format + discipline(s)
- Core lesson (1–2 sentences, never stated directly in the piece)
- Opening hook — how does Act I begin?
- 3–5 structural beats
- Transferable parallel — what does this say beyond the craft?
- Target length

*Agent action: Create outline if prompted, or from `ideas.md` backlog. Save research file (`slug-research.md`) alongside.*

### Stage 2: Draft (`drafts/pipeline/02-drafts/slug.md`)
- Full first draft written by Sonnet 4.6
- Briefed with: outline + research + `drafts/WRITING-GUIDE.md`
- Includes frontmatter (title, description, tags; `pubDate` left blank until publish)
- Three-act structure: discipline → challenge/crisis → transferable landing
- Voice: first-person practitioner, earned authority, witty-dry humor, no named lesson

*Agent action: Spawn Sonnet subagent with full context. Save to `02-drafts/`. Move idea status to ✍️*

### Stage 3: Review (`drafts/pipeline/03-review/slug.md`)
- File moved here when ready for Hayes's eyes
- Hayes options:
  - **Approve** → move to `04-approved/`, tag `✅`
  - **Pass** → delete from pipeline, tag `❌` in ideas.md
  - **Workshop** → leave in review, add `## Feedback` section at bottom of file

*Agent action: Notify Hayes via Telegram. Stage file, update ideas.md.*

### Stage 4: Approved (`drafts/pipeline/04-approved/slug.md`)
- Polished and ready to go live
- Waits here until Hayes sets a publish date
- Agent can suggest scheduling based on cadence gaps

*Agent action: Remind Hayes of approved posts if >7 days have passed without publishing one.*

### Stage 5: Published (`src/content/blog/slug.md`)
- Copy file from `04-approved/` to `src/content/blog/`
- Set `pubDate` in frontmatter
- `git add . && git commit -m "publish: [title]" && git push`
- GitHub Actions deploys to hayesmetzger.github.io/fieldcraft automatically
- Update `ideas.md` status to ✅

---

## Status Tracking

### ideas.md Status Emoji Legend
| Emoji | Meaning |
|---|---|
| 💡 | Raw idea, in backlog |
| 📝 | Outline created |
| ✍️ | Draft in progress |
| 👀 | In review (03-review/) |
| ✅ | Published live |
| ❌ | Passed / killed |
| 🔄 | Workshopping / revision |

### Quick Dashboard (agent should report this on request)
```
Published:  [N] posts live
Approved:   [N] ready to publish
In Review:  [N] awaiting Hayes
Drafting:   [N] in progress
Outlined:   [N] ready to write
Backlog:    [N] raw ideas
```

---

## Launch Sequence

The fly fishing series is the runway. Recommended publish order:

| # | Title | Format | Status |
|---|---|---|---|
| 1 | Reading the Water | Feature Essay | Draft in progress |
| 2 | The Drag-Free Drift | Field Note | Stubbed |
| 3 | Matching the Hatch | Field Note | Stubbed |
| 4 | The One That Got Away | Feature Essay | Stubbed |
| 5 | Why I Fish Alone | Weekend Read | Stubbed |

**After launch series:** Rotate into woodworking + aviation to signal breadth early. First Cross-Reference should arrive by week 3.

---

## OpenClaw's Role

| Task | Trigger | Action |
|---|---|---|
| Idea capture | Hayes mentions a topic | Add to `ideas.md` with 💡, format guess, discipline |
| Outline | "Outline [slug]" | Research + create `01-outlines/slug.md` + `slug-research.md` |
| Draft | "Draft [slug]" | Spawn Sonnet subagent; save to `02-drafts/`; move to `03-review/`; notify Hayes |
| Status check | "What's in the pipeline?" | Report dashboard from ideas.md |
| Publish | "Publish [slug]" | Copy to `src/content/blog/`, set pubDate, git commit/push |
| Scheduling | "What should I publish next?" | Check approved queue + publishing cadence gaps, recommend |
| Ideas | "Give me 5 ideas for [discipline]" | Generate working titles + formats + core insights; add to ideas.md |

---

## File Locations (Reference)

| Resource | Path |
|---|---|
| Ideas backlog | `drafts/ideas.md` |
| Writing guide | `drafts/WRITING-GUIDE.md` |
| Pipeline doc | `drafts/PIPELINE.md` |
| Topic ideas | `drafts/topics.md` |
| Discipline list | `content/disciplines.md` |
| Outlines | `drafts/pipeline/01-outlines/` |
| Drafts | `drafts/pipeline/02-drafts/` |
| In Review | `drafts/pipeline/03-review/` |
| Approved | `drafts/pipeline/04-approved/` |
| Published | `src/content/blog/` |

---

*This document is meant to be shared with Hayes as an overview and refined as the workflow evolves.*
