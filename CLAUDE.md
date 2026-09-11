# 🧠 Agent Skills Repository

## 🎯 Project Goal
This repository is an open-source public catalog providing **modular and reusable skills** for AI coding assistants (Google Antigravity, Claude Code, etc.).

Each skill addresses a specific problem or enforces high standards across recurring software engineering workflows.

---

## 📂 Repository Architecture
```text
skills/
├── CLAUDE.md                     # General context and guidelines for AI agents
├── README.md                     # GitHub showcase with skills catalog and installation guide
├── .gitignore                    # Git exclusions
├── LICENSE                       # MIT License
│
├── app-design/                   # ✅ Validated and complete skill
│   └── SKILL.md                  # 16 UI/UX golden rules, component standards, and checklist
│
└── [future-skills]/              # New skills to be added later
    └── SKILL.md
```

---

## 📋 Available Skills
- **`app-design`** (✅ Ready) : Strict UI/UX standards (16 golden rules: strict user palette adherence, zero gradients/transparency, 1px subtle borders, no parasite arrows, zero fake reviews/testimonials, optimal space density, native responsive & adaptive navigation, zero emojis, local real assets only, 1 primary button per view, destructive action guards, actionable empty states, touch targets ≥ 44px, clean overflow & truncation, keyboard shortcuts & navigation, concise microcopy).

---

## 📌 Next Steps: Git Initialization & GitHub Publication
1. **Initialize Git locally**:
   ```bash
   git init
   git add .
   git commit -m "feat: initial commit with app-design skill and documentation"
   ```
2. **Link to remote GitHub repository**:
   ```bash
   git branch -M main
   git remote add origin https://github.com/axiome02/skills.git
   git push -u origin main
   ```

---

## 🛠️ Contribution Guidelines for Agents
- Each skill must reside in its own dedicated subfolder with a documented `SKILL.md` (YAML frontmatter containing `name` and `description`).
- Keep the root `README.md` up to date with the skills catalog table and quick installation commands (`npx degit`, etc.).
