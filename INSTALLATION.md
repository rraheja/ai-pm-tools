# Installation Guide for AI PM Tools

This comprehensive guide covers installation across multiple AI platforms to support different Product Manager personas and technical comfort levels.

---

## 🖥️ Claude Desktop Pro
*Best for: UI-focused Product Managers who prefer settings-driven installation*

**Prerequisites:**
- Claude Desktop app installed ([Download here](https://claude.com/download))
- Claude Pro/Team/Enterprise subscription

**Installation Steps:**

1. **Access Plugin Marketplace**
   - Open Claude Desktop app
   - Navigate to **Settings** → **Plugins & Marketplace**
   - Click **"Browse Marketplace"**

2. **Search and Install**
   - Search for "AI PM Tools"
   - Look for the package with 📊 icon
   - Author: Product Management Community
   - Click **"Install"** and accept permissions

3. **Activate Components**
   - In Plugin settings, enable:
     - ✅ All 12 Agents (recommended)
     - ✅ All 38 Commands
     - ✅ AI Use Case Prioritization skill
   - Click **"Apply Changes"**

4. **Verify Installation**
   ```
   Hello Claude! I just installed AI PM Tools. Can you list the available agents?
   ```

### Alternate Method: Local Installation for Skills Development

**For developers wanting to modify or extend the toolkit:**

1. **Clone Repository**
   ```bash
   git clone https://github.com/rraheja/ai-pm-tools.git
   cd ai-pm-tools
   ```

2. **Add to Claude Desktop**
   - Open Claude Desktop app
   - Go to **Settings** → **Skills & Plugins**
   - Click **"Add Local Plugin"**
   - Navigate to and select the `ai-pm-tools` folder
   - Click **"Add"**

3. **Configure Components**
   - Select agents to activate (recommend all 12)
   - Enable all commands
   - Skill will auto-activate

---

## 🖥️ Claude Desktop Free
*Best for: Product Managers on free tier who want basic PM assistance*

**Prerequisites:**
- Claude Desktop app installed ([Download here](https://claude.com/download))
- Free Claude account

**Installation Steps:**

1. **Download Repository Files**
   - Go to [GitHub Repository](https://github.com/rraheja/ai-pm-tools)
   - Click **"Code"** → **"Download ZIP"**
   - Extract to a local folder

2. **Manual File Upload**
   - Start a new conversation in Claude Desktop
   - Upload 2-3 agent files most relevant to your work:
     - `agents/product-strategy.md` (for strategy work)
     - `agents/product-manager.md` (for requirements/features)
     - `agents/agile-coach.md` (for team management)

3. **Set Context**
   ```
   [Upload the agent files]
   
   Claude, I've uploaded Product Management agent personas. Please act as the 
   appropriate agent based on my requests and use the uploaded knowledge.
   ```

4. **Test Installation**
   ```
   Act as the Product Strategy Agent and help me understand market sizing approaches.
   ```

---

## 🌐 Claude.ai Pro
*Best for: Product Managers using web interface who prefer browser-based workflows*

**Prerequisites:**
- Claude account ([claude.ai](https://claude.ai))
- Claude Pro/Team subscription for Projects feature

**Installation Steps:**

1. **Create AI PM Tools Project**
   - Go to [claude.ai](https://claude.ai)
   - Click **"Create Project"**
   - Name: "AI PM Tools"
   - Description: "Complete PM toolkit with agents, commands, and skills"

2. **Upload Knowledge Base**
   - In Project settings, go to **"Project Knowledge"**
   - Upload these files (Max 20 files, 512MB each):
     - **Priority uploads:** All 12 agent files from `/agents/` folder
     - **Core skill:** `/skills/ai-usecase-prioritization/SKILL.md`
     - **Frequently used commands:** Select 7-8 most relevant from `/commands/`

3. **Set Project Instructions**
   ```
   You are an AI Product Management Assistant with access to 12 specialized agents:
   - Product Strategy Agent, Product Manager Agent, Product Design Agent
   - Product Marketing Agent, Engineering Architect Agent, Quality Assurance Agent
   - SRE Operations Agent, Product Operations Agent, Customer Success Agent
   - Sales and Marketing Agent, Technical Program Manager Agent, Agile Coach Agent
   
   Use the appropriate agent persona based on the user's request. Reference the uploaded 
   command templates and AI use case prioritization skill when needed.
   ```

4. **Test Installation**
   ```
   I need help with product strategy. Can you act as the Product Strategy Agent and 
   help me understand market sizing approaches?
   ```

---

## 🌐 Claude.ai Free
*Best for: Product Managers on free tier who want ad-hoc PM assistance*

**Prerequisites:**
- Claude account ([claude.ai](https://claude.ai))
- Free Claude account

**Installation Steps:**

1. **Download Repository Files**
   - Go to [GitHub Repository](https://github.com/rraheja/ai-pm-tools)
   - Click **"Code"** → **"Download ZIP"**
   - Extract to a local folder

2. **Upload Relevant Files per Conversation**
   - Start new conversation
   - Upload 1-2 agent files relevant to your task
   - Upload specific command file you need
   - Upload skill file if doing AI prioritization

3. **Give Context**
   ```
   [Upload product-strategy.md and create-lean-canvas.md]
   
   Claude, please act as the Product Strategy Agent and follow the 
   create-lean-canvas command structure to help me build a lean canvas.
   ```

4. **Test Installation**
   ```
   Help me create a lean canvas for a new AI-powered project management tool.
   ```

---

## 💻 Claude Code
*Best for: Technical Product Managers comfortable with command-line interfaces*

**Prerequisites:**
- Claude Code CLI installed
- VS Code with Claude Code extension (optional)
- Git access

**Installation Steps:**

```bash
# Add our marketplace
/plugin marketplace add rraheja/ai-pm-tools

# Install the plugin
/plugin install ai-pm-tools@rraheja

# Verify installation
/help

# Test a command
/prioritize-ai-usecases

# I have 3 AI projects: chatbot, code assistant, recommendation engine
```

### Alternate Method: Repository-Level Setup for Teams

**For team-wide automatic installation:**

1. **Add to Project Settings**
   Create `.claude/settings.json` in your project:
   ```json
   {
     "marketplaces": ["rraheja/ai-pm-tools"],
     "plugins": {
       "ai-pm-tools@rraheja": "enabled"
     }
   }
   ```

2. **Team Auto-Installation**
   When team members trust the repository, plugins install automatically.

---

## 🤖 ChatGPT Plus/Team/Enterprise
*Best for: Product Managers using OpenAI ecosystem with paid subscriptions*

**Prerequisites:**
- ChatGPT Plus, Team, or Enterprise subscription
- Access to GPT Builder

**Installation Steps:**

1. **Create AI PM Tools GPT**
   - Go to [chatgpt.com/create](https://chatgpt.com/create)
   - **Name:** "AI PM Tools Assistant"
   - **Description:** "Complete product management toolkit with 12 specialized agents"
   - **Instructions:**
     ```
     You are a comprehensive Product Management AI with access to 12 specialized agent personas:
     
     1. Product Strategy Agent - Market analysis, competitive positioning
     2. Product Manager Agent - Requirements, features, delivery
     3. Product Design Agent - UX research, user journeys
     4. Product Marketing Agent - GTM strategy, positioning  
     5. Engineering Architect Agent - Technical feasibility, architecture
     6. Quality Assurance Agent - Testing strategy, quality metrics
     7. SRE Operations Agent - Site reliability, incident management
     8. Product Operations Agent - Metrics, experimentation, data
     9. Customer Success Agent - User feedback, adoption metrics
     10. Sales and Marketing Agent - Sales enablement, competitive intelligence
     11. Technical Program Manager Agent - Program coordination, dependencies
     12. Agile Coach Agent - Sprint planning, team health, retrospectives
     
     When users ask for help, first ask which agent role would be most appropriate, 
     then respond in that agent's persona using the uploaded knowledge base.
     ```

2. **Upload Knowledge Base**
   - **Knowledge Base (Max 20 files):**
     - All 12 agent files from `/agents/` folder (priority - upload all)
     - `/skills/ai-usecase-prioritization/SKILL.md`
     - Remaining 7 slots: Most frequently used command files from `/commands/`

3. **Test Installation**
   ```
   I need help with product strategy. Which agent should I use and can you help me 
   understand market sizing approaches?
   ```

---

## 🤖 ChatGPT Free
*Best for: Product Managers using OpenAI free tier for ad-hoc assistance*

**Prerequisites:**
- ChatGPT free account

**Installation Steps:**

1. **Download Repository Files**
   - Go to [GitHub Repository](https://github.com/rraheja/ai-pm-tools)
   - Click **"Code"** → **"Download ZIP"**
   - Extract and keep files handy

2. **Copy-Paste Agent Instructions**
   ```
   Please act as a Product Strategy Agent with 15+ years of experience leading 
   product strategy across B2B SaaS and enterprise software.
   
   [Copy-paste relevant sections from agents/product-strategy.md]
   
   Now help me with: [your specific request]
   ```

3. **Reference Command Templates**
   ```
   I need to create a lean canvas. Here's the template structure I want to follow:
   
   [Copy-paste from commands/discovery-strategy/create-lean-canvas.md]
   
   Product: [describe your product]
   ```

4. **Test Installation**
   ```
   Help me understand the difference between TAM, SAM, and SOM for market sizing.
   ```

---

## 🔍 Perplexity Pro/Enterprise
*Best for: Product Managers who need research-focused AI with web access*

**Prerequisites:**
- Perplexity Pro or Enterprise subscription
- Access to Spaces feature

**Installation Steps:**

1. **Create PM Toolkit Space**
   - Click **"Spaces"** in left menu
   - Click **"Create a Space"**
   - **Name:** "AI PM Tools"
   - **Custom Instructions:**
     ```
     You are a comprehensive Product Management AI assistant. Draw from the uploaded 
     PM knowledge base and combine with web research. Always cite sources and provide 
     actionable insights. Focus on practical, executable recommendations.
     ```

2. **Upload Knowledge Base**
   - Click **"Add Sources"**
   - Upload key files (Max 50 files, 25MB each):
     - All 12 agent files (priority)
     - AI prioritization skill file
     - Top 10 command templates you use most
     - Any company-specific PM templates

3. **Set Custom Model** (Optional)
   - Select preferred AI model (Claude, GPT-4, etc.)
   - Adjust for your use case

4. **Test Installation**
   ```
   Using my uploaded product strategy knowledge, help me analyze the competitive 
   landscape for our new AI-powered analytics platform. Include market sizing 
   and positioning recommendations.
   ```

### Alternate Method: Individual Project Spaces

**For specialized PM domains:**

1. **Product Strategy Space**
   - Upload: Product Strategy Agent + strategy commands
   - Instructions: "Focus on market analysis and strategic planning"

2. **Agile Coaching Space**  
   - Upload: Agile Coach Agent + agile commands
   - Instructions: "Help with sprint planning and team facilitation"

3. **Technical Program Management Space**
   - Upload: Technical PM Agent + program management commands
   - Instructions: "Focus on dependencies and cross-team coordination"

---

## 🔍 Perplexity Free
*Best for: Product Managers on free tier who want research assistance*

**Prerequisites:**
- Perplexity free account

**Installation Steps:**

1. **Download Repository Files**
   - Go to [GitHub Repository](https://github.com/rraheja/ai-pm-tools)
   - Click **"Code"** → **"Download ZIP"**
   - Extract and keep files handy

2. **Reference Agent Knowledge in Queries**
   ```
   Based on product management best practices for strategic planning, help me analyze 
   the competitive landscape for AI-powered analytics platforms. Include market sizing 
   approaches and positioning strategies.
   
   Context: I'm acting as a Product Strategy Agent with focus on B2B SaaS markets.
   ```

3. **Use Command Templates**
   ```
   Help me create a lean canvas framework for a new product. I need to cover:
   - Problem, Solution, Key Metrics
   - Unique Value Proposition, Unfair Advantage
   - Channels, Customer Segments, Cost Structure, Revenue Streams
   
   Format this as a structured template I can fill out.
   ```

4. **Test Installation**
   ```
   Research current market sizing methodologies (TAM/SAM/SOM) and provide examples 
   for AI-powered project management tools.
   ```

---

## 📱 Slack with Claude Integration
*Best for: Product Managers wanting AI assistance in team communication workflows*

**Prerequisites:**
- Slack workspace on paid plan
- Claude Team/Enterprise subscription
- Admin permissions to install apps

**Installation Steps:**

1. **Install Claude App**
   - Admin goes to Slack App Directory
   - Search for "Claude" 
   - Click **"Add to Slack"**
   - Approve installation

2. **Configure PM Bot Persona**
   - In Claude settings, add instructions:
     ```
     You are an AI Product Management assistant integrated into our team's Slack. 
     Respond as the appropriate PM agent based on the request:
     - Strategy questions → Product Strategy Agent
     - Requirements → Product Manager Agent  
     - Team issues → Agile Coach Agent
     - Technical concerns → Engineering Architect Agent
     
     Keep responses concise for Slack format. Use threads for longer responses.
     ```

3. **Create PM Shortcuts**
   - Set up custom slash commands in Slack:
     ```
     /pm-strategy - Product strategy assistance
     /pm-requirements - Requirements writing help  
     /pm-roadmap - Roadmap planning
     /pm-prioritize - AI use case prioritization
     ```

4. **Test Installation**
   ```
   @claude act as Product Strategy Agent and help with competitive analysis
   
   @claude /pm-prioritize 
   I have 3 AI projects: chatbot, code assistant, recommendation engine
   ```

### Alternate Method: Custom Claude-Slack Bot

**For advanced customization:**

1. **Deploy Custom Bot**
   - Use [claude-slack-app](https://github.com/sumansm/claude-slack-app)
   - Configure with your agent instructions
   - Add PM command shortcuts

2. **Configure PM Workflows**
   ```
   @claude-pm act as Agile Coach and help plan our sprint
   @claude-pm prioritize these AI use cases with VALUE/RISK+COST framework
   ```

---

## 🚀 Quick Start Guide by Persona

### **UI-Focused Product Managers**
**Recommended:** Claude Desktop Pro → Plugin Marketplace → Test with Product Strategy Agent

### **Web-First Product Managers** 
**Recommended:** Claude.ai Pro → Projects → Upload all agents → Create comprehensive project

### **Technical Product Managers**
**Recommended:** Claude Code → Plugin installation → Repository-level setup

### **Budget-Conscious Product Managers**
**Recommended:** Claude.ai Free → Direct file upload → Focus on 2-3 core agents

### **Research-Heavy Product Managers**
**Recommended:** Perplexity Pro → Spaces → Upload knowledge base → Combine with web research

### **Team-Collaboration Focused**
**Recommended:** Slack with Claude → Official app → Custom PM commands

---

## 📋 Universal Testing Commands

Try these across any platform to verify your installation:

1. **Agent Test**
   ```
   Act as the Product Strategy Agent and explain the difference between TAM, SAM, and SOM.
   ```

2. **Command Test**
   ```
   Help me create a lean canvas for a new AI-powered project management tool.
   ```

3. **Skill Test**
   ```
   Use the AI use case prioritization framework to evaluate these 3 projects:
   1. Chatbot for customer support
   2. Code assistant for developers  
   3. Recommendation engine for ecommerce
   ```

### Expected Responses
- Agent should respond in character with appropriate expertise
- Commands should follow structured templates
- Skills should reference specific methodologies and frameworks

---

## 🔧 Troubleshooting

### Claude Desktop Issues
- **Plugins not appearing:** Restart app, check subscription status
- **Commands not working:** Verify plugin is enabled in settings
- **File generation fails:** Grant file system access

### Claude.ai Issues  
- **Projects not working:** Verify Pro subscription, check upload limits (20 files max)
- **Agents not responding correctly:** Re-upload agent files, clarify project instructions

### ChatGPT Issues
- **Knowledge not accessible:** Check file upload success, verify instructions reference uploaded files
- **Responses too generic:** Be more specific about which agent persona to use

### Perplexity Issues
- **Files not uploading:** Check file size (25MB limit), verify Pro subscription
- **Custom instructions ignored:** Ensure instructions are saved in Space settings

### Slack Issues
- **Bot not responding:** Check app permissions, verify Claude subscription
- **Commands not working:** Ensure proper slash command setup, check bot configuration

---

## 📞 Support

- **Issues:** [GitHub Issues](https://github.com/rraheja/ai-pm-tools/issues)
- **Discussions:** [GitHub Discussions](https://github.com/rraheja/ai-pm-tools/discussions)  
- **Documentation:** [README.md](README.md)
- **Updates:** Watch the repository for new releases

---

**Installation Guide Version:** 2.0  
**Last Updated:** October 2025  
**Compatible with:** AI PM Tools v1.0.0