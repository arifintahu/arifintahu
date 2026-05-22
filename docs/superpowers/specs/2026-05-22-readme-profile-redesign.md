# README Profile Redesign

**Date:** 2026-05-22  
**Status:** Approved

## Goal

Rewrite the GitHub profile README to match the terminal-minimal aesthetic of arifintahu-web. Update email from `arifintahu11@gmail.com` to `miftahul97@gmail.com`.

## Design

**Approach:** Hybrid minimal — terminal prompt section labels, updated writing tone, no emoji headers, no tech stack section. Keep social badge buttons and GitHub contribution chart.

### Section Map

| Current | New |
|---------|-----|
| `# Hey there! I'm Arifin 👋` | `~/arifin $ whoami` + `# Miftahul Arifin` |
| TypeScript code block persona | Removed |
| `## 🚀 About Me` | `` `~/arifin $ cat about.md` `` |
| `## 🛠️ Tech Stack` | Removed entirely |
| `## ⭐ Featured Projects` | `` `~/arifin $ ls projects/` `` |
| `## 📝 Latest Blog Posts` | `` `~/arifin $ ls writing/` `` |
| `## 📊 GitHub Stats` | `` `~/arifin $ git log` `` (contribution chart only) |
| `### 💬 Let's Connect!` | `` `~/arifin $ contact` `` |
| Email: `arifintahu11@gmail.com` | Email: `miftahul97@gmail.com` |
| Footer `*From arifintahu*` | Removed |

### Writing Tone

Match the web:
- Direct, factual sentences. No buzzwords or empty modifiers.
- "Six years building distributed systems" not "6+ years of experience building"
- "I care about systems that are correct, maintainable, and understandable." not "I specialize in..."
- No `!` enthusiasm punctuation outside natural use

### Header Copy

```markdown
~/arifin $ whoami

# Miftahul Arifin

Backend and blockchain engineer. Six years across Cosmos SDK chains, EVM contracts, and Go backends.
```

### About Copy

```markdown
~/arifin $ cat about.md

I build distributed systems that are correct, maintainable, and understandable.
Currently focused on cross-chain infrastructure and DeFi protocols.
```

## Implementation

1. Create branch `feature/readme-redesign` from `master`
2. Edit `README.md` in place — rewrite all sections per the section map above
3. Keep all project links, GitHub stars badges, and blog post links unchanged
4. Keep social badge buttons (X, LinkedIn, Telegram, Discord, GitHub Follow) — update email badge to `miftahul97@gmail.com`
5. Keep GitHub contribution chart (`ghchart.rshah.org/arifintahu`)
6. Commit on the new branch
