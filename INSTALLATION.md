# Installation Instructions for AI PM Tools

## Method 1: Install via Claude Marketplace (Recommended)

### Prerequisites
- Claude AI account (Desktop, Web, or Mobile app)
- Claude 4.0 or later

### Steps

1. **Open Claude Marketplace**
   - In Claude AI, click on your profile icon (top right)
   - Select "Settings" → "Plugins & Marketplace"
   - Or navigate directly to the Marketplace tab

2. **Search for AI PM Tools**
   - In the search bar, type "AI PM Tools"
   - Look for the package with 📊 icon
   - Author: Product Management Community

3. **Install the Plugin**
   - Click on "AI PM Tools Core Package"
   - Review the description and features
   - Click "Install" button
   - Accept permissions for file system access (needed for generating documents)

4. **Activate Desired Components**
   After installation, you can selectively activate:
   - **All Agents** (recommended for full experience)
   - **Specific Agents** (if you only need certain roles)
   - **All Commands** (recommended)
   - **Skills** (ai-usecase-prioritization is auto-enabled)

5. **Verify Installation**
   ```
   Hey Claude, I just installed AI PM Tools. Can you list the available agents?
   ```
   
   You should see all 12 agents listed.

6. **Try Your First Command**
   ```
   /create-team-charter
   
   I'm forming a new 6-person product team (4 engineers, 1 designer, 1 PM) 
   distributed across 2 time zones.
   ```

## Method 2: Install via Git Clone (For Development/Customization)

### Prerequisites
- Git installed on your machine
- Claude AI Desktop app (recommended for local file access)
- Basic command line familiarity

### Steps

1. **Clone the Repository**
   ```bash
   cd ~/Developer  # or your preferred directory
   git clone https://github.com/rraheja/ai-pm-tools.git
   cd ai-pm-tools
   ```

2. **Configure Claude Plugin**
   The repository includes `.claude-plugin/plugin.json` which Claude Desktop will auto-detect.

3. **Enable in Claude Desktop**
   - Open Claude AI Desktop app
   - Go to Settings → Skills & Plugins
   - Click "Add Local Plugin/Skill"
   - Navigate to and select the `ai-pm-tools` folder
   - Click "Add"

4. **Activate Components**
   - Select which agents to activate (recommend starting with all)
   - Enable all commands
   - The ai-usecase-prioritization skill will auto-activate

5. **Verify Installation**
   ```
   Hey Claude, show me the agents from AI PM Tools
   ```

6. **Keep Updated**
   ```bash
   cd ~/Developer/ai-pm-tools
   git pull origin main
   ```
   
   Claude Desktop will automatically reload updated files.

## Method 3: Manual Installation (Web Claude)

### For Claude Web Users

1. **Download the Repository**
   - Go to https://github.com/rraheja/ai-pm-tools
   - Click "Code" → "Download ZIP"
   - Extract to a local folder

2. **Upload Agents and Skills to Projects**
   Since web Claude doesn't support local plugins, you can:
   
   **Option A: Add to a Claude Project**
   - Create a new Claude Project
   - Name it "AI PM Tools"
   - In Project Knowledge, upload:
     - All agent files from `/agents/` folder
     - Skill files from `/skills/ai-usecase-prioritization/`
     - Select command files you'll use frequently from `/commands/`

   **Option B: Reference in Conversation**
   - Upload agent and skill files at the start of each conversation
   - Example:
     ```
     [Upload agile-coach.md and agile-ceremonies SKILL.md]
     
     Claude, please act as the Agile Coach Agent and use the 
     agile-ceremonies skill to help me create a team charter.
     ```

3. **Using Commands in Web**
   Commands work differently in web:
   - You won't have `/command` syntax
   - Instead, reference the command file:
     ```
     [Upload create-team-charter.md]
     
     Claude, please follow the create-team-charter command structure 
     to help me build a charter for my new team.
     ```

## Post-Installation Setup

### Recommended Configuration

1. **Set Up File Permissions** (Desktop App Only)
   - Grant Claude access to a working directory for documents
   - Recommended: `~/Documents/Claude-Workspace/`
   - This allows Claude to save generated files directly

2. **Configure Skills Folder** (Optional)
   If you want to add more skills later:
   - Create `~/Claude/skills/` directory
   - Claude will auto-detect new skills you add here

3. **Customize for Your Organization**
   - Edit agent files to reflect your company's terminology
   - Update command templates with your standards
   - Add company-specific skills

### Testing Your Installation

Try these commands to verify everything works:

1. **Test an Agent**
   ```
   Hey Claude, use the Product Strategy Agent to help me understand 
   the difference between TAM, SAM, and SOM.
   ```

2. **Test a Command**
   ```
   /prioritize-ai-usecases
   
   I have 3 AI projects: chatbot, code assistant, and recommendation engine
   ```

3. **Test a Skill**
   ```
   Can you show me the ai-usecase-prioritization framework details?
   ```

## Troubleshooting

### Issue: Agents not appearing

**Solution:**
- Desktop: Restart Claude Desktop app
- Web: Re-upload agent files to your project
- Verify plugin.json is in `.claude-plugin/` directory

### Issue: Commands not working

**Solution:**
- Ensure you're using forward slash: `/command-name`
- Check that the command is activated in Settings
- Try restarting the conversation

### Issue: Can't generate Excel files

**Solution:**
- Grant file system permissions in Settings
- Ensure you're using Claude Desktop (Excel generation limited in web)
- Check that you have write permissions to the output directory

### Issue: Skill not loading

**Solution:**
- Verify skill folder has `SKILL.md` file
- Check that skill is referenced in plugin.json
- Restart Claude to reload skills

## Updating AI PM Tools

### For Marketplace Installation
- Updates are automatic
- You'll see a notification when new versions are available
- Click "Update" in the Plugins section

### For Git Clone Installation
```bash
cd ~/Developer/ai-pm-tools
git pull origin main
```
Claude Desktop will auto-reload the updated files.

## Getting Help

- **Issues**: https://github.com/rraheja/ai-pm-tools/issues
- **Discussions**: https://github.com/rraheja/ai-pm-tools/discussions
- **Documentation**: See README.md in the repository

## Next Steps

After installation:
1. Review the [README.md](../README.md) for full feature list
2. Explore example workflows
3. Try different agents for various PM tasks
4. Customize agents and commands for your team
5. Contribute improvements back to the community!

---

*Installation Guide Version: 1.0*  
*Last Updated: October 2025*  
*For: AI PM Tools v1.0.0*
