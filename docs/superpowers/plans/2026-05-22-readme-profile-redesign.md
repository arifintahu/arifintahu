# README Profile Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite the GitHub profile README to match the terminal-minimal aesthetic of arifintahu-web, and update the email to `miftahul97@gmail.com`.

**Architecture:** Single-file edit to `README.md`. Replace emoji section headers with terminal prompt labels, remove the tech stack badge grid and TypeScript code block, update writing tone to match the web (direct, no buzzwords), keep social badge buttons and GitHub contribution chart, update email.

**Tech Stack:** Markdown, GitHub Shields.io badges (existing), ghchart.rshah.org (existing)

---

### Task 1: Create feature branch

**Files:**
- No files changed — git operation only

- [ ] **Step 1: Create and switch to feature branch**

Run:
```bash
git checkout -b feature/readme-redesign
```
Expected output:
```
Switched to a new branch 'feature/readme-redesign'
```

- [ ] **Step 2: Verify branch**

Run:
```bash
git branch
```
Expected: `* feature/readme-redesign` shown as active.

---

### Task 2: Rewrite README.md

**Files:**
- Modify: `README.md` (full rewrite)

This replaces the entire file content. The new content below is the complete README.

- [ ] **Step 1: Replace README.md with the following content**

Write the entire file `README.md`:

```markdown
<div align="center">

`~/arifin $ whoami`

# Miftahul Arifin

**Backend and blockchain engineer.** Six years across Cosmos SDK chains, EVM contracts, and Go backends.

</div>

---

`~/arifin $ cat about.md`

I build distributed systems that are correct, maintainable, and understandable. When I'm not writing code, I'm writing about how it works. Currently focused on cross-chain infrastructure and DeFi protocols.

---

`~/arifin $ ls projects/`

| Project | Description | Stars |
|---------|-------------|-------|
| [**Project Structure API**](https://github.com/arifintahu/project-structure-api) | Production-ready TypeScript REST API template — adopted by 138+ developers and 21 forks | ![Stars](https://img.shields.io/github/stars/arifintahu/project-structure-api?style=flat-square) |
| [**Dexplorer**](https://github.com/arifintahu/dexplorer) | Lightweight Cosmos chain explorer with real-time validator dashboard. Used for quick chain debugging without spinning up full infra | ![Stars](https://img.shields.io/github/stars/arifintahu/dexplorer?style=flat-square) |
| [**Vault Strategy**](https://github.com/arifintahu/vault-strategy) | Automated EMA-based leverage vaults for Bitcoin — self-custody with configurable risk tiers | ![Stars](https://img.shields.io/github/stars/arifintahu/vault-strategy?style=flat-square) |
| [**QuickLend**](https://github.com/arifintahu/quicklend) | Decentralized non-custodial lending protocol — pooled liquidity and algorithmic interest rates | ![Stars](https://img.shields.io/github/stars/arifintahu/quicklend?style=flat-square) |
| [**PR-Please**](https://github.com/arifintahu/pr-please) | Chrome extension that generates structured GitHub PR titles and descriptions using AI | ![Stars](https://img.shields.io/github/stars/arifintahu/pr-please?style=flat-square) |
| [**Earn Aggregator**](https://github.com/arifintahu/earn-aggregator) | High-performance API aggregating flexible earn product APYs from major crypto exchanges | ![Stars](https://img.shields.io/github/stars/arifintahu/earn-aggregator?style=flat-square) |
| [**Astral**](https://github.com/arifintahu/astral) | Ultra-lightweight server monitoring dashboard — single binary with built-in alerting | ![Stars](https://img.shields.io/github/stars/arifintahu/astral?style=flat-square) |
| [**Xylem**](https://github.com/arifintahu/xylem) | Stateless EVM blockchain explorer — zero backend required, connects directly to RPC nodes | ![Stars](https://img.shields.io/github/stars/arifintahu/xylem?style=flat-square) |

---

`~/arifin $ ls writing/`

<!-- BLOG-POST-LIST:START -->
- [How Reentrancy Exploits Drain Smart Contracts](https://arifintahu.com/blog/how-reentrancy-exploits-drain-smart-contract)
- [The Odyssey of Consensus: From Byzantine](https://arifintahu.com/blog/the-odyssey-of-consensus-from-byzantine)
- [How Merkle Trees Secure Blockchain](https://arifintahu.com/blog/how-merkle-trees-secure-blockchain)
<!-- BLOG-POST-LIST:END -->

[More...](https://arifintahu.com/blog)

---

`~/arifin $ git log --oneline`

<div align="center">

![GitHub Contribution Graph](https://ghchart.rshah.org/arifintahu)

</div>

---

<div align="center">

`~/arifin $ contact`

[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://twitter.com/arifintahu)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/miftahul-arifin/)
[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/arifintahu)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:miftahul97@gmail.com)
[![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/users/arifintahu)
[![GitHub Follow](https://img.shields.io/github/followers/arifintahu?style=for-the-badge&logo=github&label=Follow)](https://github.com/arifintahu)

</div>
```

- [ ] **Step 2: Verify email is updated**

Run:
```bash
grep "gmail.com" README.md
```
Expected:
```
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:miftahul97@gmail.com)
```
`arifintahu11@gmail.com` must NOT appear anywhere in the output.

- [ ] **Step 3: Verify old emoji headers are gone**

Run:
```bash
grep -E "🚀|🛠️|⭐|📝|📊|💬|👋" README.md
```
Expected: no output (no matches).

- [ ] **Step 4: Commit**

```bash
git add README.md
git commit -m "feat: redesign README with terminal-minimal aesthetic

- Replace emoji section headers with terminal prompt labels
- Remove tech stack badge grid
- Remove TypeScript code block persona
- Update writing tone to match arifintahu-web
- Update email to miftahul97@gmail.com"
```
