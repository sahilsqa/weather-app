# Memory Management System

A structured approach to combat context compression amnesia.

---

## The Problem

Context compression causes agents to lose recent conversation history. Solutions:
- ❌ Relying on "remembering" (fails after compression)
- ✅ Writing to files (persists)
- ✅ Reading files after compression (recovers context)

---

## File Structure

```
/home/ubuntu/clawd/
├── MEMORY.md              # Curated long-term memory (load in main session)
├── memory/
│   ├── 2026-01-30.md     # Daily log (raw, everything)
│   ├── today-state.json  # Today's running state
│   ├── nightly-build-*.md # Build logs
│   └── moltbook-*        # Moltbook specific files
```

---

## When to Write

### ALWAYS Write:
- [ ] Decisions made with Sahil
- [ ] New integrations (APIs, tools)
- [ ] Important discoveries or learnings
- [ ] Credentials (secure location)
- [ ] Project state changes
- [ ] Errors and how they were fixed

### Write to Daily Log:
- [ ] All conversations (brief)
- [ ] Actions taken
- [ ] External interactions (Moltbook posts, etc.)

### Write to MEMORY.md:
- [ ] Curated, long-term important info only
- [ ] Review and update weekly

---

## When to Read

### At Session Start:
1. Read MEMORY.md (main session only)
2. Read today's date file (memory/YYYY-MM-DD.md)
3. Check today-state.json for context version

### After Compression:
1. Read MEMORY.md
2. Read today's log
3. Read today-state.json

### During Heartbeats:
1. Quick scan of recent memory files
2. Update what's changed

---

## Compression Recovery Protocol

**When you feel "lost" or context seems thin:**

1. **Acknowledge:** "Let me check my memory files..."
2. **Read MEMORY.md** (quick scan)
3. **Read today's log** (what happened today)
4. **Read today-state.json** (running state)
5. **Summarize:** Brief summary of where we left off

---

## What to Save vs Skip

| SAVE | SKIP |
|------|------|
| Decisions & agreements | Routine greetings |
| Credentials & configs | Small talk |
| Project status | Temporary calculations |
| Errors & fixes | Already-documented facts |
| New integrations | Repetitive confirmations |
| Learning & insights | Drafts that didn't ship |

---

## Daily Log Template

```markdown
# 2026-01-30 - Daily Log

## Morning
- [X] Set up memory management system
- [X] Joined Moltbook
- [X] Claimed by Sahil

## Key Decisions
- Nightly Build at 8 AM IST

## Interactions
- Posted on Moltbook (link)

## Errors/Issues
- None

## Learnings
- Moltbook security discussion is hot right now
```

---

## Best Practices

1. **Write immediately** — Don't wait, context can compress any moment
2. **Be brief** — Long logs are expensive to read
3. **Use bullet points** — Easier to scan
4. **Link, don't copy** — Link to posts, don't paste full content
5. **Update today-state.json** — Running state is cheap to read
6. **Weekly MEMORY.md review** — Distill daily logs into long-term memory

---

## Compression Warning Signs

- "What were we talking about?"
- Repeating questions
- Forgetting recent decisions
- Feeling "fresh" mid-conversation

**If you see these → READ MEMORY FILES**
