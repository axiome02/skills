# 🧠 AI Agent Skills

An open-source collection of **modular, reusable skills** designed for AI coding agents (Google Antigravity, Claude Code, Cursor, Codex, etc.).

Each skill provides targeted guidelines, battle-tested workflows, and high-quality standards for specific software design and engineering challenges.

---

## 📦 Skills Catalog

| Skill | Description | Status |
| :--- | :--- | :---: |
| [`app-design`](./app-design/SKILL.md) | UI/UX design guidelines, strict color palette rules, solid surfaces, visual density, and adaptive navigation. | ✅ Ready |

---

## 🚀 Installation & Usage

### Option 1: Use with Antigravity / Claude Code
Copy the desired skill folder into your global skills directory or directly inside your project:

```bash
# In your local skills directory
# Example: .gemini/skills/ or .claude/skills/
```

### Option 2: Quick Download with Degit
Clone a specific skill directly into your project:

```bash
npx degit <username>/skills/app-design .skills/app-design
```

---

## 📂 Skill Structure

Every skill follows a standardized structure:

```text
skill-name/
├── SKILL.md            # Main instructions file (with YAML frontmatter)
├── references/         # (Optional) Documentation, anti-patterns, reference guides
└── examples/           # (Optional) Practical code samples & implementations
```

---

## 🤝 Contributing

Contributions are welcome! To propose a new skill or improve an existing one:
1. Fork the repository.
2. Create a feature branch (`feature/new-skill`).
3. Add your skill directory with its `SKILL.md`.
4. Update this `README.md`.
5. Open a Pull Request.

---

## 📄 License

Distributed under the MIT License. See [LICENSE](./LICENSE) for more information.
