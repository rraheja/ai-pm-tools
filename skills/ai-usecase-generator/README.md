# AI Use Case Generator Skill

**Version**: 1.0.0  
**License**: Apache 2.0  
**Compatible with**: Claude AI Projects

## What This Skill Does

This skill helps organizations identify AI opportunities by:
1. Analyzing organizational documents (vision, strategy, customer feedback)
2. Researching industry trends and competitor capabilities
3. Generating 5 strategic AI use case ideas
4. Mapping to the Strategic Pillars Quadrant
5. Outputting high-level summaries in multiple formats

## How to Install

### For Claude Projects (claude.ai)

1. **Upload to Project**:
   - Create or open a Claude Project
   - Upload the entire `ai-usecase-generator` folder (this folder)
   - Or upload just `SKILL.md` and the `templates/` folder

2. **That's it!** Claude will automatically detect and use the skill.

### What to Upload

You only need these files:
```
ai-usecase-generator/
├── SKILL.md              # Main skill instructions (self-contained)
└── templates/
    ├── use-case-template.md     # Output template
    └── industry-examples.md     # Detailed examples (loaded as needed)
```

## Quick Start

Once uploaded, simply say:
```
"Help me identify AI opportunities for my company"
```

Claude will:
1. Ask for your industry (if not clear)
2. Request key documents or work with what you provide
3. Perform automatic web research
4. Generate 5 AI use cases mapped to strategic quadrants
5. Offer outputs in your preferred format

## Strategic Pillars Quadrant

The skill maps AI use cases to this framework:

```
              AUTONOMOUS
                  |
      Q2          |          Q4
  (In-context)    |    (Autonomous)
                  |
KNOW-HOW ──────────────── ACTIONABLE
                  |
      Q1          |          Q3
  (Diagnostic)    |     (Workflows)
                  |
         HUMAN INTERVENTION
```

**Quadrants**:
- **Q1**: BI/Analytics - Insights with human review
- **Q2**: Automated Insights - Self-service predictions
- **Q3**: Assisted Workflows - AI drafts, human approves  
- **Q4**: Autonomous Agents - Fully automated

## Output Examples

### 1. Comparison Table
| # | Use Case | Quadrant | Target Market | Customer | Problem | Value | Cost |
|---|----------|----------|---------------|----------|---------|-------|------|

### 2. Individual Markdown Files
- `usecase_01_[name].md`
- `usecase_02_[name].md`
- etc.

### 3. Visual Quadrant Map
Shows all 5 use cases positioned in the 2x2 matrix

### 4. Executive Formats
- Word (.docx) - consolidated report
- PDF - presentation format
- PowerPoint (.pptx) - slide deck

## What This Skill Does NOT Do

❌ **Prioritization** - Use `ai-usecase-prioritization` skill for scoring  
❌ **Detailed Specs** - Use `ai-usecase-blueprint` skill for requirements  
❌ **Implementation** - This is discovery only

## Next Steps After Using This Skill

1. **Prioritize**: Use `ai-usecase-prioritization` to score opportunities
2. **Plan**: Use `ai-usecase-blueprint` for detailed specifications
3. **Execute**: Implement your top-priority use cases

## File Structure

```
ai-usecase-generator/
│
├── README.md                          # This file
├── SKILL.md                           # Main skill instructions (self-contained, required)
│
└── templates/                         # Template files
    ├── use-case-template.md          # Markdown output template (always used)
    └── industry-examples.md          # Detailed examples (loaded as needed)
```

## Key Features

✅ **Automated Web Research** - Searches trends and competitors  
✅ **Document Analysis** - Extracts strategic goals and pain points  
✅ **Industry Agnostic** - Works for any sector  
✅ **High-Level Focus** - Portfolio view, not detailed specs  
✅ **Multiple Outputs** - Markdown, tables, visuals, executive formats  
✅ **Skill Integration** - Works with other AI PM Tools skills

## Technical Details

**Main Instruction File**: `SKILL.md` (~400 lines, self-contained)
- Includes: Quadrant framework, analysis methodology, process guidance
- Core framework and methodology built-in

**Reference Files** (loaded conditionally):
- `use-case-template.md` (~146 lines) - Output template (always used)
- `industry-examples.md` (~300 lines) - Detailed examples (loaded when user needs deeper context)

## Usage Tips

✅ **Provide Context**: Share strategic documents if available  
✅ **Be Specific**: Mention industry and key challenges  
✅ **Review Quadrants**: Ensure balanced portfolio  
✅ **Save Markdown**: Files can be used by other skills  
✅ **Iterate**: Regenerate with more information if needed

## Support

- **Core Framework**: Built into SKILL.md (self-contained)
- **Industry Examples**: See `templates/industry-examples.md`
- **Template Format**: See `templates/use-case-template.md`

## License

Apache License 2.0 - Free for commercial and personal use

## Version History

**v1.0.0** (October 2025)
- Initial release
- Strategic Pillars Quadrant framework
- Automated web research
- Multiple output formats
- Integration with ai-usecase-prioritization and ai-usecase-blueprint

---

Made with ❤️ for AI Product Managers
