---
title: PMSpecKit - Enterprise AI-Native Product Management Framework
version: 2.0
short_prefix: pmsk
last_updated: 2025-10-29
audience: Enterprise Product Managers, AI-Native Teams
framework_compatibility: GitHub Spec Kit, Enterprise Agile, Modern AI Tools
---

# PMSpecKit
## Enterprise AI-Native Product Management Framework

**Status**: Production Ready | **Version**: 2.0 | **Short Form**: pmsk

---

## Executive Summary

**PMSpecKit** (pmsk) is an enterprise-grade AI-native product management framework combining:
- **GitHub Spec Kit** principles (spec-driven development, constitution-based governance)
- **Modern AI tooling** (multiple AI platforms supported)
- **Enterprise PM practices** (full product lifecycle from strategy to feedback)

PMSpecKit enables product managers to:
- **Increase productivity** with AI-powered artifact creation/review/analysis
- **Maintain governance** through spec-driven, constitution-based approach
- **Work with preferred tools** (Claude, ChatGPT, Perplexity, NotebookLM - no IDE required)
- **Enable reproducibility** through structured markdown-first workflows
- **Scale across organizations** with minimal overhead and maximum clarity

---

## Core Fundamentals

PMSpecKit is built on five fundamental principles that make it production-ready for enterprise teams:

### 1. 📁 9-Phase Folder Structure
Predictable, standardized organization from strategy to feedback:
```
01_Strategy/ 02_Planning/ 03_Design/ 04_Requirements/ 05_Backlog/
06_Prototype/ 07_Quality/ 08_Launch/ 09_Feedback/
```

### 2. 📝 Fixed Filename Standards
Every skill outputs predictable files with lowercase, hyphen-separated naming:
- `market-overview.md`, `swot-analysis.md`, `usecase-01-{slug}.md`
- Auto-generated slugs by LLM (e.g., "fraud-detection", "customer-support")
- See [Filename Standards](#filename-standards) for complete reference

### 3. 🎯 Spec-Driven Full-Stack PM
Product Managers orchestrate the entire AI product lifecycle:
- Constitution.md as project source of truth
- Markdown files are source; PDF/PPTX/DOCX are exports
- Outputs from one phase flow into the next (optional but optimal)

### 4. 🔧 AI-Agnostic Toolchain
Tools are recommendations, not requirements:
- **Strategy**: Perplexity + NotebookLM (web research + synthesis)
- **Planning**: ChatGPT OR Claude (use case generation)
- **Design/Requirements**: Claude Desktop or IDE
- **Prototype/Quality**: Claude in IDE (Cursor/VS Code)
- Pattern: `analyze-*` (collect) → `synthesize-*` (process, any tool)

### 5. 🔄 Re-run & Archive System
Skills prompt when existing files found:
- **Use as input**: Update with new insights, show what changed
- **Start fresh**: Auto-archive to `_archive/{timestamp}/`
- **Review only**: Summarize existing content

---

## Unified Phase Model: 9 Phases

| Phase | Name | Purpose | Skills | Primary Tools | Outputs |
|-------|------|---------|--------|---------------|---------|
| **01** | Strategy | Market analysis, competitive context | ai-market-trends | Perplexity + NotebookLM | market-overview.md, swot-analysis.md, five-forces-analysis.md, market-sources.md |
| **02** | Planning | Use case generation, prioritization, roadmap | ai-usecase-generator, ai-usecase-prioritization | ChatGPT OR Claude | usecases-summary.md, usecase-NN-{slug}.md (01-05), prioritization-scores.xlsx |
| **03** | Design | Product blueprint, lean canvas, architecture | ai-usecase-blueprint | Claude (Desktop or IDE) | blueprint-{name}.md, lean-canvas-{name}.md |
| **04** | Requirements | PRD, technical specs, PR/FAQ | (future skills) | Claude (Desktop or IDE) | prd.md, prfaq.md, functional-requirements.md |
| **05** | Backlog | Epics, stories, dependency tracking | (future skills) | Claude (IDE: Cursor/VS Code) | epic-NN-{slug}.md, story-NN-{slug}.md, dependencies.md |
| **06** | Prototype | PM-created prototypes, POCs, demos | (future skills) | Claude (IDE: Cursor/VS Code) | prototype-{name}.md, poc-{name}.md, demo-script.md |
| **07** | Quality | Test plans, evals, quality metrics | (future skills) | Claude + Eval frameworks | test-plan.md, eval-framework.md, quality-metrics.md |
| **08** | Launch | GTM strategy, release planning, sales enablement | (future skills) | Claude/ChatGPT | gtm-strategy.md, launch-checklist.md, release-notes.md, battlecard.md |
| **09** | Feedback | Customer feedback, VOC, win-loss analysis | (future skills) | NotebookLM + Analytics | feedback-synthesis.md, win-loss-analysis.md, iterations.md |

---

## Filename Standards

All skills follow standardized naming conventions to enable predictable workflows and cross-skill integration.

### Naming Patterns

1. **Phase outputs**: `{descriptor}.md` (e.g., `market-overview.md`, `swot-analysis.md`)
2. **Use cases**: `usecase-{NN}-{slug}.md` (e.g., `usecase-01-fraud-detection.md`, `usecase-02-customer-support.md`)
3. **Blueprints**: `blueprint-{name}.md` (e.g., `blueprint-ai-customer-support.md`)
4. **Lean Canvas**: `lean-canvas-{name}.md`
5. **Epics/Stories**: `epic-{NN}-{slug}.md`, `story-{NN}-{slug}.md`
6. **Excel files**: `{descriptor}.xlsx` (e.g., `prioritization-scores.xlsx`)

### Naming Rules

- **Lowercase**: All filenames use lowercase
- **Hyphens**: Use hyphens for word separation (not underscores or spaces)
- **Descriptive**: Filenames should be self-documenting
- **Sequential**: Use zero-padded numbers for ordered items (01, 02, ..., 10)
- **Auto-generated slugs**: LLM generates two-word slugs from content (e.g., "fraud-detection", "content-generation")

### Filename Reference by Phase

**01_Strategy** (ai-market-trends):
- `market-overview.md` - Company + Industry + Competitive Landscape
- `swot-analysis.md` - SWOT matrix
- `five-forces-analysis.md` - Porter's Five Forces
- `market-sources.md` - Bibliography

**02_Planning** (ai-usecase-generator, ai-usecase-prioritization):
- `usecases-summary.md` - Portfolio overview
- `usecase-01-{slug}.md` through `usecase-05-{slug}.md` - Individual use cases
- `usecases-quadrant.md` - Strategic pillars visualization
- `prioritization-scores.xlsx` - Scoring matrix
- `prioritization-comparison.md` - Side-by-side comparison
- `prioritization-justification.md` - Scoring rationale

**03_Design** (ai-usecase-blueprint):
- `blueprint-{name}.md` - Comprehensive specification
- `lean-canvas-{name}.md` - Optional one-pager

**04_Requirements** (future):
- `prd.md` - Product Requirements Document
- `prfaq.md` - PR/FAQ document
- `functional-requirements.md` - Detailed specs

**05_Backlog** (future):
- `epic-{NN}-{slug}.md` - Epic-level requirements
- `story-{NN}-{slug}.md` - User stories
- `dependencies.md` - Cross-team dependencies

**06_Prototype** (future):
- `prototype-{name}.md` - Prototype documentation
- `poc-{name}.md` - Proof of concept specs

**07_Quality** (future):
- `test-plan.md` - Testing strategy
- `eval-framework.md` - AI evaluation methodology

**08_Launch** (future):
- `gtm-strategy.md` - Go-to-market strategy
- `launch-checklist.md` - Launch readiness
- `release-notes.md` - Version release notes
- `battlecard.md` - Sales enablement

**09_Feedback** (future):
- `feedback-synthesis.md` - Aggregated feedback
- `win-loss-analysis.md` - Win-loss insights
- `iterations.md` - Planned improvements

### Re-run Behavior

When skills detect existing output files, they prompt the user with options:

1. **Use as input**: Read existing files, incorporate new insights, update with new analysis
2. **Start fresh**: Move existing files to `_archive/{timestamp}/` directory, generate from scratch
3. **Review only**: Summarize existing content, no changes

**What the user sees:**
```
I found these existing files:
- market-overview.md (last updated: 2024-10-29)
- swot-analysis.md (last updated: 2024-10-29)

Would you like me to:
A. Use existing files as input for additional analysis
B. Start fresh (archive old files)
C. Review existing files only (no changes)
```

**If option A selected, skill will show:**
```
I will update:
- market-overview.md (add new competitive intelligence)
- market-sources.md (add new research sources)

These will remain unchanged:
- swot-analysis.md
- five-forces-analysis.md
```

### Archive System

When re-running with "Start fresh" option, old files are automatically archived:

```
02_Planning/
├── usecase-01-fraud-detection.md          # Current version
├── usecase-02-content-generation.md
└── _archive/
    └── 2024-10-29-143022/                 # Timestamp: YYYY-MM-DD-HHMMSS
        ├── usecase-01-fraud-detection.md  # Previous version
        └── usecase-02-content-generation.md
```

---

## Phase Details

### 01_Strategy

**Purpose**: Analyze company, market, and competitive context.

**Key Outputs**:
- `market-overview.md` - Company + Industry + Competitive Landscape (8-12 pages consolidated)
- `swot-analysis.md` - SWOT matrix with strategic implications
- `five-forces-analysis.md` - Porter's Five Forces analysis
- `market-sources.md` - Source bibliography with reliability ratings

**Skills**: `ai-market-trends` - See [skills/ai-market-trends/SKILL.md](skills/ai-market-trends/SKILL.md) for complete methodology

**Tool Recommendations**:
- **Perplexity**: Live web research for current trends, competitor data, market sizing
- **NotebookLM**: Synthesis across multiple research sources (5+ documents)
  - Upload: Research files + synthesis prompt
  - Ask: Cross-cutting analysis questions
  - Export: Insights and audio briefings for stakeholders

**Workflow**:
1. Use Perplexity to research competitors, industry trends, market sizing
2. Save outputs as markdown files in 01_Strategy/
3. (Optional) For synthesis: Concatenate files, upload to NotebookLM for cross-document analysis
4. Export selected files to PDF/PPTX for stakeholder review

**Duration**: 1-2 weeks

**Feeds Into**: 02_Planning (use case generation uses market context)

---

### 02_Planning

**Purpose**: Generate use cases, research users, prioritize opportunities.

**Key Outputs**:
- `usecases-summary.md` - Portfolio overview with quadrant mapping
- `usecase-01-{slug}.md` through `usecase-05-{slug}.md` - Individual use cases (auto-generated slug)
- `usecases-quadrant.md` - Strategic Pillars Quadrant visualization
- `prioritization-scores.xlsx` - VALUE/(RISK+COST) scoring with dashboard
- `prioritization-comparison.md` - Side-by-side comparison matrix
- `prioritization-justification.md` - Detailed scoring rationale

**Skills**:
- `ai-usecase-generator` - See [skills/ai-usecase-generator/SKILL.md](skills/ai-usecase-generator/SKILL.md)
- `ai-usecase-prioritization` - See [skills/ai-usecase-prioritization/SKILL.md](skills/ai-usecase-prioritization/SKILL.md)

**Tool Recommendations**:
- **ChatGPT**: Better for creative brainstorming and use case ideation
- **Claude**: Better for structured analysis and prioritization logic
- Choose based on your company's license and task focus
- **NotebookLM** (optional): For synthesizing feedback from multiple user research sources

**Workflow**:
1. Use ChatGPT or Claude to generate use cases based on 01_Strategy outputs
2. Create individual use case files with standard structure
3. Generate prioritization framework and scoring (Excel with VALUE/(RISK+COST) formula)
4. Identify top use cases for development
5. Create roadmap

**Duration**: 2-3 weeks

**Feeds Into**: 03_Design (product blueprint), 05_Backlog (epic creation)

---

### 03_Design

**Purpose**: Define product blueprint, architecture, and UX approach.

**Key Outputs**:
- `blueprint-{usecase-name}.md` - Comprehensive 14-16 page product specification
- `lean-canvas-{usecase-name}.md` - Optional one-page strategic overview

**Skills**: `ai-usecase-blueprint` - See [skills/ai-usecase-blueprint/SKILL.md](skills/ai-usecase-blueprint/SKILL.md)

**Tool Recommendations**:
- **Claude** (via Desktop or IDE: Cursor/VS Code)
- Use IDE for iterative design refinement and agent collaboration

**Workflow**:
1. Input: 02_Planning outputs (use cases, prioritization)
2. Use Claude Desktop or IDE to generate product blueprint
3. Iterate on architecture and UX approach
4. Document design rationale directly in files
5. Export to PDF for design review

**Duration**: 1-2 weeks

**Feeds Into**: 04_Requirements (PRD generation), 05_Backlog (epic breakdown)

---

### 04_Requirements

**Purpose**: Define PRD, technical specs, and success metrics.

**Key Outputs**:
- `prd.md` - Full Product Requirements Document
- `plan.md` - Technical implementation plan
- `functional-requirements.md` - Detailed functional specs
- `non-functional-requirements.md` - Performance, security, scalability
- `success-metrics.md` - KPIs, OKRs, success criteria

**Skills**: `requirements-engineering` (planned)

**Tool Recommendations**:
- **Claude** (via Desktop or IDE: Cursor/VS Code)
- Use IDE for comprehensive PRD generation and refinement

**Workflow**:
1. Input: 03_Design outputs (blueprint, architecture)
2. Use Claude to generate comprehensive PRD
3. Include success metrics and acceptance criteria
4. Iterate for clarity and completeness
5. Export to PDF and DOCX for stakeholder distribution

**Duration**: 1-2 weeks

**Feeds Into**: 05_Backlog (epic and story generation), 06_Quality (test case generation)

---

### 05_Backlog

**Purpose**: Break down requirements into epics, stories, and tasks.

**Key Outputs**:
- `epics/epic-###-{title}.md` - Epic-level requirements
- `stories/{epic-###}/story-###-{title}.md` - User stories
- `stories/story-999-{title}.md` - Independent stories
- `tasks/task-###-{title}.md` - Implementation tasks
- `acceptance-criteria/acceptance-criteria-template.md` - AC templates

**Skills**: `requirements-epics-stories` (planned)

**Tool Recommendations**:
- **Claude** (via IDE: Cursor/VS Code)
- IDE recommended for collaborative refinement and story quality

**Workflow**:
1. Input: 04_Requirements/prd.md
2. Use Claude to generate epics based on PRD features
3. Generate user stories for each epic
4. Create tasks for complex stories
5. Define acceptance criteria for each story
6. Iterate for clarity and completeness

**Duration**: 1-2 weeks

**Feeds Into**: 06_Quality (test case generation), 07_Launch (release planning)

---

### 06_Prototype

**Purpose**: Create PM-led prototypes, POCs, and technical demos.

**Key Outputs**:
- `prototype-{name}.md` - Prototype documentation and learnings
- `poc-{name}.md` - Proof of concept specifications
- `demo-script.md` - Demo walkthrough scripts

**Skills**: (future skills)

**Tool Recommendations**:
- **Claude** (via IDE: Cursor/VS Code)
- Modern PMs use AI-powered IDEs to create quick prototypes and POCs
- Validate technical feasibility before full development

**Workflow**:
1. Input: 03_Design/blueprint outputs
2. Use Claude with IDE to generate prototype code
3. Create POC to validate key assumptions
4. Document learnings and technical decisions
5. Share demos with stakeholders

**Duration**: 1-2 weeks (parallel to requirements)

**Feeds Into**: 05_Backlog (technical constraints), 07_Quality (test scenarios)

---

### 07_Quality

**Purpose**: Define tests, evaluations, and safety guardrails.

**Key Outputs**:
- `test-plan.md` - Overall testing strategy
- `test-cases.md` - Functional test cases
- `eval-framework.md` - AI model evaluation methodology
- `ai-model-evals.md` - Model performance metrics
- `agent-performance-evals.md` - Agent behavior tests
- `guardrails.md` - Safety constraints and policies
- `use-case-evals/eval-use-case-###.md` - Per-use-case evaluation results

**Skills**: `qa-framework` (planned)

**Tool Recommendations**:
- **Claude**: For test case and eval framework generation
- **Specialized eval frameworks**: Patronus AI, Giskard, etc. for AI-specific evals
- **IDE** (Cursor/VS Code): For automation scripts

**Workflow**:
1. Input: 05_Backlog/acceptance-criteria
2. Use Claude to generate test cases and eval frameworks
3. Generate model and agent performance evaluations
4. Define safety guardrails
5. Create per-use-case evaluation reports
6. Document results and recommendations

**Duration**: Parallel to development; ongoing refinement

**Feeds Into**: 08_Launch (quality gates), 09_Feedback (monitoring)

---

### 08_Launch

**Purpose**: Prepare go-to-market strategy and release planning.

**Key Outputs**:
- `gtm-strategy.md` - GTM approach, positioning, launch channels
- `launch-checklist.md` - Sign-offs, testing, deployment readiness
- `release-notes/release-v###.md` - Version-specific release notes
- `communications/launch-announcement.md` - Customer announcements

**Skills**: `gtm-planning` (planned)

**Tool Recommendations**:
- **Claude**: For GTM strategy, competitive positioning, detailed go-to-market planning
- **ChatGPT**: For messaging, launch copy, announcement content, social media
- Choose tool based on task: Claude for strategy, ChatGPT for messaging
- Can use both for different components

**Workflow**:
1. Input: 04_Requirements/prd.md, 05_Backlog (final deliverables)
2. Use Claude OR ChatGPT (based on task) to generate GTM strategy
3. Create launch checklist and sign-off documentation
4. Generate release notes for version release
5. Draft customer/stakeholder communications
6. Export for stakeholder distribution

**Duration**: 2-4 weeks before launch

**Feeds Into**: 09_Feedback (post-launch monitoring)

---

### 09_Feedback

**Purpose**: Track metrics, synthesize user feedback, and plan iterations.

**Key Outputs**:
- `kpi-dashboard.md` - Current metric values and trends
- `metrics.md` - Metric definitions and targets
- `user-feedback.md` - Aggregated user feedback and insights
- `persona-feedback.md` - Feedback segmented by persona
- `retrospectives/sprint-01-retro.md` - Sprint retrospectives
- `iterations/iteration-01.md` - Planned improvements and bug fixes

**Skills**: `feedback-synthesis` (planned)

**Tool Recommendations**:
- **NotebookLM**: For feedback synthesis from customer data, support tickets, surveys
  - Concatenate feedback documents
  - Upload to NotebookLM
  - Ask: "What are the top 5 user concerns?" "What improvements are most requested?"
- **Analytics tools**: For metric aggregation and KPI dashboards
- **Claude**: For iteration planning and insights synthesis

**Workflow**:
1. Aggregate user feedback from support, surveys, analytics
2. Concatenate feedback documents
3. Upload to NotebookLM for cross-source analysis
4. Ask NotebookLM for insights: pain points, requested features, trends
5. Use Claude to synthesize NotebookLM output into iteration plans
6. Document sprint retrospectives and planned improvements
7. Create persona-specific feedback analysis

**Duration**: Ongoing; weekly reviews during initial launch, monthly after stabilization

**Loops Back To**: 01_Strategy (market updates), 02_Planning (new use cases), 05_Backlog (new epics/stories)

---

## Configuration

### Root-Level Governance

**constitution.md** (Project Root):
```yaml
---
type: Constitution
project-name: [Your Project Name]
created: 2025-10-29
updated: 2025-10-29
---

# Project Constitution

## Vision
[Concise vision statement]

## Key Stakeholders
- Product Manager: [Name] ([Email])
- Engineering Lead: [Name] ([Email])
- Design Lead: [Name] ([Email])
- Executive Sponsor: [Name] ([Email])

## Core Principles
1. [Principle]
2. [Principle]
3. [Principle]

## Success Criteria
1. [Metric 1]
2. [Metric 2]

## Constraints
- Budget: $[Amount]
- Timeline: [Duration]
- Tech Stack: [Technologies]
```

### PMSpecKit Configuration (.pmsk/config.yaml)

Configuration file locations (XDG standard):
1. **Project-level** (highest priority): `<project_root>/.pmsk/config.yaml`
2. **User-level** (fallback): `~/.config/pmsk/config.yaml`
3. **Hardcoded defaults**: Built into skills if no config found

**Minimal configuration**:
```yaml
# PROJECT METADATA
project-name: "My AI Product"
framework: "PMSpecKit"

# PHASE DIRECTORIES
STRATEGY_DIR: "01_Strategy"
PLANNING_DIR: "02_Planning"
DESIGN_DIR: "03_Design"
REQUIREMENTS_DIR: "04_Requirements"
BACKLOG_DIR: "05_Backlog"
PROTOTYPE_DIR: "06_Prototype"
QUALITY_DIR: "07_Quality"
LAUNCH_DIR: "08_Launch"
FEEDBACK_DIR: "09_Feedback"

# BEHAVIOR
archive-existing: true        # Move old files to _archive/{timestamp}/ on re-run
```

See `.pmsk/config.yaml` in this repository for complete configuration reference with filename overrides.

**How skills use configuration**:
1. Check for config file in project root (`.pmsk/config.yaml`) or user home (`~/.config/pmsk/config.yaml`)
2. Read appropriate phase directory variable (e.g., `STRATEGY_DIR` for ai-market-trends)
3. If directory exists, write outputs there
4. If directory doesn't exist, notify user and write to current directory
5. If no config found, write to current directory

**Skill behavior (always enabled)**:
- **Re-run prompts**: Always prompt when existing files detected, always show what will be updated
- **Export formats**: All formats (PDF, DOCX, PPTX) available - user chooses at export time
- **Archive**: Controlled by `archive-existing` config option (default: true)

---

## Integration Points

### Skill Dependencies (Input → Output Flow)

```
01_Strategy (ai-market-trends)
  ↓ OUTPUTS: market-overview.md, swot-analysis.md, five-forces-analysis.md, market-sources.md
  ↓ (optional inputs)
02_Planning (ai-usecase-generator, ai-usecase-prioritization)
  ↓ OUTPUTS: usecases-summary.md, usecase-NN-{slug}.md (01-10), prioritization-scores.xlsx
  ↓ (optional inputs)
03_Design (ai-usecase-blueprint)
  ↓ OUTPUTS: blueprint-{name}.md, lean-canvas-{name}.md
  ↓ (inputs for next phases)
04_Requirements → 05_Backlog → 06_Prototype → 07_Quality → 08_Launch → 09_Feedback
  ↓ (loops back)
01_Strategy (market updates), 02_Planning (new use cases), 05_Backlog (iterations)
```

**Cross-Phase Data Flow:**
- Strategy outputs inform Planning (market context for use case generation)
- Planning outputs inform Design (prioritized use cases for blueprints)
- Design outputs inform Requirements (blueprint details for PRDs)
- Feedback loops back to Strategy, Planning, and Backlog for continuous improvement

See "Re-run Behavior" section under "Filename Standards" for details on handling existing files.

### Tool Selection by Phase

| Phase | Research | Analysis | Synthesis | Collaboration |
|-------|----------|----------|-----------|---------------|
| 01_Strategy | Perplexity | — | NotebookLM | — |
| 02_Planning | ChatGPT/Claude | ChatGPT/Claude | NotebookLM (optional) | — |
| 03_Design | — | Claude | — | IDE (Cursor/VS Code) |
| 04_Requirements | — | Claude | — | IDE (Cursor/VS Code) |
| 05_Backlog | — | Claude | — | IDE (Cursor/VS Code) |
| 06_Prototype | — | Claude | — | IDE (Cursor/VS Code) |
| 07_Quality | — | Claude | — | IDE + Eval frameworks |
| 08_Launch | — | Claude/ChatGPT | — | — |
| 09_Feedback | — | Claude | NotebookLM | Analytics tools |

**Decision Logic**:
1. **Large volumes of source documents?** → NotebookLM for synthesis
2. **Strategic planning or creative brainstorming?** → Claude (structured) or ChatGPT (creative)
3. **Need IDE integration?** → Claude Desktop or IDE
4. **AI-specific evaluation needs?** → Specialized frameworks + Claude

---

## Getting Started

### Quick Start Checklist

- [ ] **Create project folder** and 9 phase directories (01_Strategy through 09_Feedback)
- [ ] **Create root files**: `constitution.md`, `README.md`
- [ ] **Copy `.pmsk/config.yaml`**: Configure phase directories for your project
- [ ] **Initialize Git**: `git init`, create `.gitignore`
- [ ] **Install AI PM Tools**: Follow [INSTALLATION.md](INSTALLATION.md) for your preferred platform
- [ ] **Start with 01_Strategy**: Use `ai-market-trends` skill or `/analyze-market` command
- [ ] **Generate first artifacts**: Markdown files with consistent naming
- [ ] **Export for stakeholders**: PDF or PPTX as needed
- [ ] **Commit to Git**: Track all changes
- [ ] **Share constitution.md** with team for governance alignment

### Example Project Structure

```
project-name/
├── README.md
├── constitution.md
├── .pmsk/
│   └── config.yaml
│
├── 01_Strategy/
│   ├── market-overview.md
│   ├── swot-analysis.md
│   ├── five-forces-analysis.md
│   └── market-sources.md
│
├── 02_Planning/
│   ├── usecases-summary.md
│   ├── usecase-01-customer-support.md
│   ├── usecase-02-fraud-detection.md
│   ├── ...
│   ├── usecase-05-content-generation.md
│   ├── usecases-quadrant.md
│   ├── prioritization-scores.xlsx
│   ├── prioritization-comparison.md
│   └── prioritization-justification.md
│
├── 03_Design/
│   ├── blueprint-customer-support.md
│   └── lean-canvas-customer-support.md
│
├── 04_Requirements/
│   ├── prd.md
│   └── prfaq.md
│
├── 05_Backlog/
│   ├── epic-01-authentication.md
│   ├── story-01-user-login.md
│   └── dependencies.md
│
├── 06_Prototype/
│   ├── prototype-chatbot-poc.md
│   └── demo-script.md
│
├── 07_Quality/
│   ├── test-plan.md
│   └── eval-framework.md
│
├── 08_Launch/
│   ├── gtm-strategy.md
│   ├── launch-checklist.md
│   ├── release-notes.md
│   └── battlecard.md
│
└── 09_Feedback/
    ├── feedback-synthesis.md
    └── win-loss-analysis.md
```

---

## Extending PMSpecKit

### Custom Skills
- Add new skills to `skills/` directory
- Follow structure: `SKILL.md`, `README.md`, `/templates/`, `/assets/`
- Configure output folder in `.aipmconfig`

### Custom Commands
- Add to `commands/` directory
- Reference existing skills or agents
- Keep commands concise (30-50 lines)
- Detailed methodology goes in skills

### Custom Agents
- Add to `agents/` directory
- Define persona, capabilities, operating principles
- Reference from commands

---

## Framework Information

**Framework Name**: PMSpecKit (pmsk)
**Version**: 2.0
**Last Updated**: 2025-10-29
**Audience**: Enterprise Product Managers, AI-Native Teams
**License**: CC-BY-4.0 (Creative Commons Attribution 4.0)

**For detailed skill methodologies**, see:
- [ai-market-trends](skills/ai-market-trends/SKILL.md) - Market and competitive intelligence
- [ai-usecase-generator](skills/ai-usecase-generator/SKILL.md) - Use case generation
- [ai-usecase-prioritization](skills/ai-usecase-prioritization/SKILL.md) - AI initiative prioritization
- [ai-usecase-blueprint](skills/ai-usecase-blueprint/SKILL.md) - Product blueprint creation

**For installation and setup**, see:
- [INSTALLATION.md](INSTALLATION.md) - Multi-platform installation guide
- [README.md](README.md) - Project overview
- [CLAUDE.md](CLAUDE.md) - Claude Code-specific guidance

---

*PMSpecKit v2.0 - Enterprise AI-Native Product Management Framework*
*Last Updated: 2025-10-29*
