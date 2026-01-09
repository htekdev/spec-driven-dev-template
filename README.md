# Spec-Driven Development Template

A GitHub repository template that enforces **specification-first development** through intelligent GitHub Copilot instructions. This template ensures that all changes are documented before implementation, creating a living specification that evolves with your codebase.

## 🎯 What is Spec-Driven Development?

Spec-Driven Development is a methodology where:
1. **Documentation comes first** - Before writing any code, you update the Product Requirements Document (PRD)
2. **PRD is the source of truth** - All features, changes, and decisions are tracked in PRD.md
3. **No exceptions** - GitHub Copilot is configured to refuse code changes until PRD.md is updated
4. **Living documentation** - Your spec evolves alongside your code, never becoming stale

## 🚀 Why Use This Template?

- **Prevents undocumented changes** - Every feature and fix is recorded
- **Improves team communication** - Everyone knows what's being built and why
- **Facilitates code reviews** - Reviewers can reference the PRD for context
- **Creates audit trail** - Historical record of all decisions and changes
- **Reduces technical debt** - Forces intentional, documented decisions
- **Onboarding made easy** - New team members can read the PRD to understand the project

## 📋 The PRD-First Workflow

### The Golden Rule

```
Every change = PRD.md update FIRST. No exceptions.
```

### How It Works

1. **You ask Copilot to make a change**
   - "Add user authentication"
   - "Fix the login bug"
   - "Refactor the database layer"

2. **Copilot updates PRD.md FIRST**
   - Documents the requirement
   - Explains the rationale
   - Lists acceptance criteria

3. **Then Copilot implements the change**
   - With the spec as a guide
   - Ensuring alignment with documented requirements

4. **PRD.md stays current**
   - Acts as living documentation
   - Never falls out of sync with code

## 🛠️ Setup Instructions

### Using This Template

1. **Click "Use this template"** on GitHub
2. **Clone your new repository**
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

3. **Initialize your project**
   - PRD.md will be created automatically on first Copilot interaction
   - Or create it manually using the structure below

4. **Start developing**
   - Just ask GitHub Copilot to implement features
   - Copilot will automatically update PRD.md first

### PRD.md Options

This template offers **two PRD approaches** depending on your project needs:

#### Option 1: Lightweight Change Log (for templates/libraries)
Best for: Open-source projects, templates, utility libraries

Use PRD.md as a simple change log:
```markdown
# PRD: Your Project Name

## Overview
Brief project description

**Core Principle**: Update PRD.md BEFORE any code changes.

---

## Changes

### [YYYY-MM-DD] Feature Name
**Type**: Feature|Bug|Docs | **Status**: 🔄 | ✅ | ⏸️
**Goal**: What you're building
**Why**: Business/user value
**What**: 
- [ ] Task 1
- [ ] Task 2
```

#### Option 2: Full-Stack Product PRD (for applications)
Best for: Full-stack apps, SaaS products, user-facing applications

Use the comprehensive [prd-template.md](prd-template.md) based on the [VibeCoding PRD Guide](https://github.com/cpjet64/vibecoding/blob/main/prd-guide.md). This template includes:

- **Product Overview**: Vision, users, objectives, metrics
- **User Personas**: Demographics, goals, pain points, journeys
- **Feature Requirements**: Detailed table with priorities
- **User Flows**: Step-by-step interaction paths
- **Non-Functional Requirements**: Performance, security, accessibility
- **Technical Specifications**: Frontend, backend, infrastructure
- **Analytics & Monitoring**: Metrics and dashboards
- **Release Planning**: MVP and future releases
- **AI Conversation Insights**: Document AI-assisted design decisions

**When to use which**:
- **Lightweight**: Template repositories, tools, proof-of-concepts
- **Full-Stack**: Production apps with users, complex features, team collaboration

**Both approaches follow the same rule**: Document BEFORE implementing.

## 💡 Example Workflow

### Scenario: Adding a new feature

**You**: "Add a user profile page"

**Copilot**: 
1. ✅ First updates PRD.md with:
   - Feature requirements
   - Design decisions
   - Acceptance criteria

2. ✅ Then implements:
   - Creates profile page component
   - Adds routing
   - Implements API endpoints
   - Writes tests

**Result**: You have both working code AND complete documentation of what was built and why.

## 🔒 How Enforcement Works

This template uses `.github/copilot-instructions.md` to configure GitHub Copilot with strict rules:

- ❌ Refuses to write code before updating PRD.md
- ❌ Won't skip documentation "just this once"
- ✅ Always updates PRD.md as the first action
- ✅ Treats PRD.md as the source of truth

The instructions are loaded automatically when GitHub Copilot is active in your repository.

## 📚 Best Practices

1. **Be specific in PRD entries** - Include enough detail for future reference
2. **Update status as you go** - Mark items as Completed when done
3. **Include rationale** - Explain WHY decisions were made
4. **Link to related items** - Reference related PRD entries or issues
5. **Keep it organized** - Use clear headings and consistent formatting
6. **Review PRD in code reviews** - Ensure documentation matches implementation

## 🤝 Contributing

This is a template repository. Feel free to:
- Fork and customize for your needs
- Submit issues for suggestions
- Create pull requests for improvements

## 📄 License

[MIT License](LICENSE)

## 🙋 FAQ

**Q: What if I need to make a quick fix?**  
A: Even quick fixes get documented in PRD.md first. It takes seconds and prevents undocumented changes.

**Q: Can I disable this for certain changes?**  
A: You can manually edit files without Copilot, but that defeats the purpose. The value is in the discipline.

**Q: What if my PRD.md gets too large?**  
A: Archive completed items to a `docs/history/` folder periodically, keeping only active/recent items in PRD.md.

**Q: Does this work with other AI coding assistants?**  
A: The instructions are designed for GitHub Copilot, but the PRD-first principle can be applied manually with any tool.

---

**Start building with intention. Start with spec-driven development.** 🚀
