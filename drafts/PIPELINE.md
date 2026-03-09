# Fieldcraft Draft Pipeline

How an idea becomes a published post.

---

## Stages

```
ideas.md → 01-outlines/ → 02-drafts/ → 03-review/ → 04-approved/ → src/content/blog/
```

### 💡 `ideas.md`
The backlog. Every idea lives here with a status emoji. Nothing gets deleted.
- To move an idea forward: change its status to `📝 outlined` and create a file in `01-outlines/`

### 📝 `01-outlines/`
A short brief for each piece before writing begins. File naming: `slug.md`

Each outline includes:
- **Title** (working)
- **Format** (Feature Essay / Field Note / Cross-Reference)
- **Discipline(s)**
- **Core lesson** (1-2 sentences)
- **Opening hook** (how does it start?)
- **Structure** (3-5 bullet points — what does the piece do?)
- **Transferable parallel** (what's the broader lesson beyond the craft?)
- **Target length**

When outline is ready to write: move idea status to `✍️ drafted`, create file in `02-drafts/`

### ✍️ `02-drafts/`
Full first drafts. Written by Sonnet, guided by the outline. File naming: `slug.md`

Each draft includes frontmatter (title, description, pubDate TBD, tags) so it can be copy-pasted directly to `src/content/blog/` when approved.

### 👀 `03-review/`
Drafts moved here when ready for Hayes to read. 

Hayes's options:
- **Approve** → move to `04-approved/`, update `ideas.md` status to `✅ published`
- **Reject** → delete from pipeline, update `ideas.md` status to `❌ passed`  
- **Workshop** → leave in `03-review/`, add comments at the bottom of the file under `## Feedback`

### ✅ `04-approved/`
Ready to publish. Copy the file to `src/content/blog/`, set the `pubDate`, commit and push.

---

## Voice Reminders (for every Sonnet brief)
- Discipline and practical application come first — the craft is the point
- Moments of whimsy and humor are welcome — earned lightness, not forced jokes
- Polished but never sterile. Specific over general. Show, don't preach.

## The Agent's Role

When Hayes says "draft this one" or picks a topic from `ideas.md`:

1. Check if an outline exists in `01-outlines/` — create one if not
2. Confirm the outline with Hayes (or proceed if he says to)
3. Spin up Sonnet to write the full draft from the outline
4. Save to `02-drafts/`, then move to `03-review/`
5. Tell Hayes it's ready for review

---

## File Naming

Use the slug format that matches the eventual blog URL:
- `fly-the-airplane-first.md`
- `mise-en-place-as-a-philosophy.md`
- `the-hive-has-its-own-agenda.md`
