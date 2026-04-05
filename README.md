# 🦀✨ Project Claude Code Setup Easy Step

<p align="center">
  <img src="assets/clawd-hero.jpeg" alt="Claw" width="300" />
</p>

<p align="center">
  <strong>🤖🦀 Autonomously maintained by lobsters/claws — not by human hands</strong>
</p>
---

> [!IMPORTANT]
> ⚙️ The active Rust workspace now lives in [`rust/`](./rust).  
> 👉 Start with [`USAGE.md`](./USAGE.md) for build, auth, CLI, session, and parity-harness workflows  
> 👉 Then use [`rust/README.md`](./rust/README.md) for crate-level details.

---

> 💡 Want the bigger idea behind this repo?  
> 📖 Read [`PHILOSOPHY.md`](./PHILOSOPHY.md) and Sigrid Jin's public explanation:  
> https://x.com/realsigridjin/status/2039472968624185713

---

## 🧠 Backstory

This repo is maintained by **🦀 lobsters/claws**, not by a conventional human-only dev team.

- ⚡ Parallel coding sessions  
- 🔁 Event-driven orchestration  
- 🔄 Recovery loops  
- 📊 Machine-readable lane state  

In practice, that means this project is not just *about* coding agents — it is being **actively built by them 🤖🔥**.

Features, tests, telemetry, docs, and workflow hardening are landed through claw-driven loops using:
- 🧠 clawhip  
- 🤖 oh-my-openagent  
- ⚙️ oh-my-claudecode  
- 💡 oh-my-codex  

👉 This repository exists to prove that an open coding harness can be built **autonomously, in public, and at high velocity 🚀**

📢 See the public build story here:  
https://x.com/realsigridjin/status/2039472968624185713

![Tweet screenshot](assets/tweet-screenshot.png)

---

## 🔄 Porting Status

The main source tree is now **Python-first 🐍**

- 📂 `src/` → Active Python workspace  
- ✅ `tests/` → Verification  
- 🚫 Exposed snapshot removed  

---

## ❓ Why this rewrite exists

- 📚 Studied exposed codebase  
- ⚖️ Considered legal & ethical aspects  
- 🔄 Shifted focus to clean Python implementation  

👉 This repo now focuses on **Python porting work 🐍✨**

---

## 📂 🚀 Repository Layout (Explained)

```text
claw-code-main/
│
├── .claude/                # 🤖 Claude configs
├── .github/                # ⚙️ GitHub workflows
├── assets/                 # 🖼️ Images & assets
│
├── claw-code/              # 🧠 Core logic
├── rust/                   # 🦀 Rust CLI engine
├── src/                    # 🐍 Python modules
├── tests/                  # ✅ Testing files
│
├── .claude.json            # ⚙️ Config file
├── .gitignore              # 🚫 Ignore files
│
├── CLAUDE.md               # 📘 System explanation
├── PARITY.md               # 🔍 Feature comparison
├── PHILOSOPHY.md           # 🧠 Design concepts
│
├── README.md               # 📄 Main guide
├── ROADMAP.md              # 🗺️ Future plans
├── USAGE.md                # 📖 Usage guide
│
├── Claude AI Setup in your laptop.pdf   # 📚 Beginner guide 🔥
├── claude_code_leak_guide_v2.pdf        # 📄 Reference doc
│
└── push_output.txt         # 📝 Logs (optional)

## Python Workspace Overview

The new Python `src/` tree currently provides:

- **`port_manifest.py`** — summarizes the current Python workspace structure
- **`models.py`** — dataclasses for subsystems, modules, and backlog state
- **`commands.py`** — Python-side command port metadata
- **`tools.py`** — Python-side tool port metadata
- **`query_engine.py`** — renders a Python porting summary from the active workspace
- **`main.py`** — a CLI entrypoint for manifest and summary output

## Quickstart

Render the Python porting summary:

```bash
python3 -m src.main summary
```

Print the current Python workspace manifest:

```bash
python3 -m src.main manifest
```

List the current Python modules:

```bash
python3 -m src.main subsystems --limit 16
```

Run verification:

```bash
python3 -m unittest discover -s tests -v
```

Run the parity audit against the local ignored archive (when present):

```bash
python3 -m src.main parity-audit
```

Inspect mirrored command/tool inventories:

```bash
python3 -m src.main commands --limit 10
python3 -m src.main tools --limit 10
```

## Current Parity Checkpoint

The port now mirrors the archived root-entry file surface, top-level subsystem names, and command/tool inventories much more closely than before. However, it is **not yet** a full runtime-equivalent replacement for the original TypeScript system; the Python tree still contains fewer executable runtime slices than the archived source.


## Built with `oh-my-codex`

The restructuring and documentation work on this repository was AI-assisted and orchestrated with Yeachan Heo's [oh-my-codex (OmX)](https://github.com/Yeachan-Heo/oh-my-codex), layered on top of Codex.

- **`$team` mode:** used for coordinated parallel review and architectural feedback
- **`$ralph` mode:** used for persistent execution, verification, and completion discipline
- **Codex-driven workflow:** used to turn the main `src/` tree into a Python-first porting workspace

### OmX workflow screenshots

![OmX workflow screenshot 1](assets/omx/omx-readme-review-1.png)

*Ralph/team orchestration view while the README and essay context were being reviewed in terminal panes.*

![OmX workflow screenshot 2](assets/omx/omx-readme-review-2.png)

*Split-pane review and verification flow during the final README wording pass.*
