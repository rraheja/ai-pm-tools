# Installation Guide for AI PM Tools

This guide covers installation across multiple AI platforms to support different Product Manager workflows and tool preferences.

---

## 🚀 Quick Navigation - Choose Your Tool

**Select your platform to jump directly to installation instructions:**

### Installation Options
- 💻 [Claude Code (CLI)](#-claude-code-cli) - Command-line with full plugin support
- 🖥️ [Claude Projects (Paid Plans)](#️-claude-projects-paid-plans) - Desktop/Web with Project Knowledge
- 🤖 [ChatGPT Custom GPT (Paid Plans)](#-chatgpt-custom-gpt-paid-plans) - Custom GPT with knowledge base
- 📓 [Google NotebookLM](#-google-notebooklm) - Document synthesis with notebooks
- 🆓 [Free AI Tools](#-free-ai-tools) - Claude, ChatGPT, Perplexity, Gemini, etc.

### Additional Resources
- [📋 Universal Testing Commands](#-universal-testing-commands) - Verify your installation
- [🔧 Troubleshooting](#-troubleshooting) - Common issues and solutions
- [📞 Support](#-support) - Get help

---

## 💻 Claude Code (CLI)

*Best for: Technical Product Managers comfortable with command-line interfaces*

Claude Code supports the full plugin/marketplace experience with automatic detection of agents, skills, and commands.

**Prerequisites:**
- Claude Code CLI installed
- Cursor or VS Code with Claude Code extension (optional)
- Git access

### Method 1: Plugin Installation (Coming Soon)

Once available in the Claude Code marketplace:

```bash
# Add AI PM Tools from marketplace
/plugin marketplace add rraheja/ai-pm-tools

# Install the plugin
/plugin install ai-pm-tools

# Verify installation
/help
```

### Method 2: Git Clone (for Development purposes)

**Step 1: Clone the Repository**

```bash
# Clone to your project or workspace
git clone https://github.com/rraheja/ai-pm-tools.git
cd ai-pm-tools
```

**Step 2: Automatic Detection**

Claude Code automatically detects:
- **Agents** in `.claude/agents/` 
- **Skills** in `.claude/skills/` 
- **Commands** in `.claude/commands/`

**Step 3: Test Installation**

```bash
# Verify agents are detected
/agents

# Verify skills are detected
/skills

# List available commands
/help
```

### How to Use in Claude Code

**Referencing Agents:**
```
Act as the Product Strategy Agent and help me create a market sizing analysis.
```

**Using Commands:**
```
/write-requirements

Product: AI-powered code review tool
```

**Leveraging Skills:**
Skills are automatically invoked when relevant. Just describe your task:
```
I need to prioritize 5 AI use cases for my portfolio.
```

---

## 🖥️ Claude Projects (Paid Plans)

*Best for: Product Managers using Claude Desktop or claude.ai with Paid plans*

Claude Projects provide a dedicated workspace with persistent knowledge base.

**Prerequisites:**
- Claude Desktop app ([Download here](https://claude.com/download)) OR claude.ai access with a paid plan

### Installation Steps

**1. Download Repository Files**
```bash
# Option A: Git clone
git clone https://github.com/rraheja/ai-pm-tools.git

# Option B: Download ZIP
# Go to https://github.com/rraheja/ai-pm-tools
# Click "Code" → "Download ZIP"
# Extract to local folder
```

**2. Create AI PM Tools Project**
- **Desktop:** Open Claude Desktop → Click "New Project" → Name: "AI PM Tools"
- **Web:** Go to [claude.ai](https://claude.ai) → Click "Create Project" → Name: "AI PM Tools"

**3. Upload Folders to Project Knowledge**

Click **"Add Content"** or **"Project Knowledge"** and upload these folders:

**Priority 1 - Agents (Essential):**
- Upload **all files** from the `/agents/` folder

**Priority 2 - Skills (Recommended):**
- Upload **all files** from the `/skills/` folder (including subdirectories)

**Priority 3 - Commands (As Needed):**
- Upload command files from the `/commands/` folder that you use most frequently
- Choose from discovery, planning, execution, and launch categories based on your needs

**Storage Note:** Projects support ~200K tokens (~500 pages). You can typically upload all agents, all skills, and your most-used command templates within this limit.

**4. Set Project Instructions**

In Project Settings, add custom instructions:

```
You are an AI Product Management assistant with access to specialized agent personas, skills, and command templates.

When I request help, identify which agent persona is most appropriate (Product Strategy, Product Manager, Product Design, etc.) and respond using that agent's expertise and communication style from the uploaded knowledge base.

Use the uploaded skills (like AI use case prioritization) and command templates (like lean canvas, PRD, roadmap) to structure your responses.

Always reference the uploaded files to ensure consistency with the framework.
```

**5. Test Installation**

Start a new chat in the project:

```
What agents and skills do you have access to in this project?
```

**Expected:** Claude lists the agents and skills from the uploaded files in Project Knowledge.

### How to Use

**Every conversation in the Project has access to:**
- All agent personas from `/agents/`
- Skills frameworks from `/skills/`
- Command templates you uploaded from `/commands/`

**Example requests:**
```
Act as the [appropriate agent persona] to help me write requirements for a new feature

Follow the lean canvas command template to build a canvas for my product

Apply the use case prioritization skill to evaluate these projects
```

---

## 🤖 ChatGPT Custom GPT (Paid Plans)

*Best for: Product Managers using ChatGPT paid plans*

**Prerequisites:**
- ChatGPT paid plans with access to GPT Builder

### Installation Steps

**1. Download Repository Files**
```bash
# Clone or download
git clone https://github.com/rraheja/ai-pm-tools.git
```

**2. Create Custom GPT**
- Go to [chatgpt.com/create](https://chatgpt.com/create)
- Click **"Create a GPT"**

**3. Configure GPT Settings**

**Name:** "AI PM Tools Assistant"

**Description:** "Complete product management toolkit with specialized agents, skills, and command templates covering the entire product lifecycle."

**Instructions:**
```
You are a comprehensive Product Management AI assistant with access to specialized agent personas and PM frameworks from the uploaded knowledge base.

Review the uploaded files from the /agents/ folder to identify all available agent personas and their areas of expertise. Each agent has specific capabilities in different PM domains (strategy, execution, design, marketing, engineering, operations, etc.).

When users ask for help:
1. Identify which agent persona from the uploaded files is most appropriate for their request
2. Respond using that agent's expertise and communication style as defined in their file
3. Reference the uploaded command templates and skills for structured outputs
4. Ask clarifying questions when context is needed

Use the uploaded knowledge base files to ensure consistent, high-quality PM deliverables.
```

**4. Upload Knowledge Base**

Under **"Knowledge"**, upload files (max 20 files):

**Priority 1 - Agents (Essential):**
- All agent files from the `/agents/` folder

**Priority 2 - Skills (Recommended):**
- Key skill files from the `/skills/` folder

**Priority 3 - Commands (As Needed):**
- Most frequently used command files from the `/commands/` folder
- Choose based on your typical workflows (discovery, planning, execution, launch, operations)

**5. Configure Capabilities**
- ✅ Web Browsing (for market research)
- ✅ DALL-E Image Generation (for mockups/diagrams)
- ✅ Code Interpreter (for data analysis)

**6. Save and Test**

Click **"Create"** then test:
```
What agents and skills do you have access to?
```

**Expected:** GPT lists all agent personas and available skills from the uploaded knowledge base.

### How to Use

Start any conversation with:
```
I need help from the [Agent Name] to [specific task]
```

Examples:
```
Act as the [agent persona] and help me write requirements for a new feature

Use the lean canvas template to build a canvas for an AI analytics platform

Act as the [agile coach persona] and help me plan our next sprint
```

---

## 📓 Google NotebookLM

*Best for: Product Managers who need document synthesis, research notes, and knowledge base creation*

**Prerequisites:**
- Google account with access to NotebookLM ([notebooklm.google.com](https://notebooklm.google.com))

### Installation Steps

**1. Download Repository Files**
```bash
# Clone or download
git clone https://github.com/rraheja/ai-pm-tools.git
```

**2. Create AI PM Tools Notebook**
- Go to [notebooklm.google.com](https://notebooklm.google.com)
- Click **"New notebook"** or **"+ Create"**
- Name: "AI PM Tools Knowledge Base"

**3. Upload Agent Files (Priority)**

Click **"Add Source"** → **"Upload"** and upload:
- **All files** from the `/agents/` folder

**4. Upload Skills Documentation**

- **All files** from the `/skills/` folder (including subdirectories)

**5. Upload Command Templates**

- Upload your most frequently used command files from the `/commands/` folder
- Choose from discovery, planning, execution, go-to-market, and operations categories based on your needs

**Note:** NotebookLM supports up to 50 sources per notebook.

**6. Test Installation**

```
What agents and skills do you have access to from the uploaded sources?
```

**Expected:** NotebookLM lists the agents and skills from the uploaded files, with source citations.

### How to Use NotebookLM

**Query Examples:**
```
Based on the strategy agent's expertise, help me create a competitive positioning strategy for an AI-powered CRM.

Using the lean canvas template, help me build a lean canvas for a mobile inventory management app.

Using the use case prioritization skill, help me evaluate these projects: chatbot, code review tool, analytics dashboard.

Combine insights from multiple agent personas to develop a go-to-market strategy.
```

**Unique Features:**
- **Audio Overviews:** Generate podcast-style discussions about PM strategies
- **Study Guide:** Create structured learning materials from frameworks
- **Timeline View:** Track chronological development of ideas
- **Source Citations:** Responses include citations to uploaded documents
- **Notebook Guide:** AI-generated summaries and suggested questions

**Limitations:**
- No file generation (download Excel templates separately from GitHub)
- 50 source limit (prioritize most-used agents and commands)
- Best for research and synthesis, not real-time collaboration
- Cannot execute code or create interactive tools

---

## 🆓 Free AI Tools

*For: Claude Free, ChatGPT Free, Perplexity Free, Gemini Free, and other free-tier AI chat interfaces without project/spaces capabilities*

This universal approach works across all free AI tools that don't support persistent Projects or Custom GPTs.

**Prerequisites:**
- Free account on your preferred AI platform (Claude, ChatGPT, Perplexity, Gemini, etc.)

### Installation Steps

**1. Download Repository Files**
```bash
# Option A: Git clone
git clone https://github.com/rraheja/ai-pm-tools.git

# Option B: Download ZIP
# Go to https://github.com/rraheja/ai-pm-tools
# Click "Code" → "Download ZIP" → Extract to local folder
```

**2. Prepare Files for Your Task**

Identify which agent(s), skills, and commands you need for your specific task:

**For strategy work:**
- Agents: Browse `/agents/` for strategy-related personas
- Commands: From `/commands/discovery-strategy/`

**For requirements/features:**
- Agents: Browse `/agents/` for execution-focused personas
- Commands: From `/commands/planning-requirements/` or `/commands/design-development/`

**For team management:**
- Agents: Browse `/agents/` for team-focused personas
- Commands: From `/commands/agile-coaching/`

**For other domains:**
- Browse `/agents/` for appropriate persona
- Browse `/commands/` for relevant templates
- Include `/skills/` files if using frameworks

**3. Use Based on Platform Capability**

### If Your Platform Supports File Upload:

**Examples:** 

1. Start a new conversation
2. Upload relevant files (agent + skill + commands as needed)
3. Set context in your first message:
   ```
   [After uploading files]

   Act as the [Agent Name] and use the uploaded command templates and skills to help me with [your specific task].
   ```

### If Your Platform Only Supports Text (No File Upload):

**Examples:** ChatGPT Free, basic AI interfaces

1. Open relevant agent/command files in a text editor
2. Copy the content
3. Paste into conversation with instructions:
   ```
   [Paste agent definition]

   Using this persona and the following template:

   [Paste command template]

   Help me with: [your specific request]
   ```

**4. Test Installation**

Try this query to verify access to uploaded/provided content:

```
What agents, skills, and command templates do you have access to from the files I've uploaded/provided?
```

**Expected:** The AI lists all agents, skills, and commands from the uploaded or pasted content.

### Example Workflows

**Strategy Session:**
```
[Upload: strategy agent file, lean canvas command]

Act as the uploaded agent persona and help me create a lean canvas for my new mobile app idea.
```

**Requirements Writing:**
```
[Upload: product manager agent file, requirements and user stories commands]

Act as the uploaded agent persona and help me write requirements for a new user authentication feature.
```

**Sprint Planning:**
```
[Upload: agile coach agent file, sprint planning command]

Act as the uploaded agent persona and help me plan our next 2-week sprint.
```

### Limitations
- No persistent knowledge base (upload/paste files each conversation)
- Limited file uploads per conversation (varies by platform)
- Need to re-establish context for each new conversation
- May require copy-paste on platforms without file upload support

### Tips for Free Tiers
- **Bookmark frequently used agents/commands** for quick access
- **Combine related files** before uploading to maximize usage
- **Start with the agent definition** to establish persona before adding commands
- **Be explicit** in referencing uploaded/pasted content to ensure it's used

---

## 📋 Universal Testing Commands

Try these across platforms to verify your installation:

### For Claude Code (CLI)
```bash
# Verify agents are detected
/agents

# Verify skills are detected
/skills

# List available commands
/help
```

### For All Other Platforms
```
What agents, skills, and command templates do you have access to?
```

**Expected Response Should Include:**
- List of agent personas from the `/agents/` folder
- Available skills from the `/skills/` folder
- Command templates uploaded from the `/commands/` folder
- Source citations (for platforms like NotebookLM)

**If the response lists the expected content, your installation is successful!**

---

## 🔧 Troubleshooting

### Claude Projects Issues
- **Project not accessible:** Verify subscription status, check project permissions
- **Files not uploading:** Check file size, verify Pro/Team subscription, ensure .md format
- **Agent not responding correctly:** Explicitly reference agent name in your prompt

### Claude Code Issues
- **Commands not found:** Run `/help` to verify command detection
- **Skills not working:** Check `.claude/skills/` folder structure
- **Repository not detected:** Ensure you're in the correct directory

### ChatGPT Custom GPT Issues
- **Knowledge not used:** Ensure files uploaded successfully, verify file count limit
- **Agent persona not followed:** Be more explicit: "Act as the [Agent Name]"
- **File limit reached:** Prioritize agents over commands, upload only most-used files

### NotebookLM Issues
- **Sources not uploading:** Check file format (.md supported), verify source count limit
- **Responses not using uploaded knowledge:** Explicitly mention agent or template name
- **Audio overview not generating:** Ensure sufficient sources uploaded

### Free AI Tools Issues
- **File uploads failing:** Check platform file size limits and supported formats (.md usually supported)
- **Context not maintained:** Re-upload files or copy-paste agent definitions for each conversation
- **Inconsistent responses:** Be more explicit - reference agent name and template in every query
- **Platform doesn't support files:** Use copy-paste method instead

---

## 📞 Support

- **Issues:** [GitHub Issues](https://github.com/rraheja/ai-pm-tools/issues)
- **Discussions:** [GitHub Discussions](https://github.com/rraheja/ai-pm-tools/discussions)
- **Documentation:** [README.md](README.md)
- **Updates:** Watch the repository for new releases

---

**Installation Guide Version:** 3.0
**Last Updated:** October 2025