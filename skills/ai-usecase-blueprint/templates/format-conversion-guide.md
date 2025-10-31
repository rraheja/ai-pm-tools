# Format Conversion Guide

> **Converting existing blueprint markdown to PDF, DOCX, or PPTX formats**
> Use this guide when user already has markdown and wants alternative formats

---

## Purpose

This guide enables **format conversion WITHOUT re-running the entire ai-usecase-blueprint skill**. If a user already has a completed blueprint in markdown, use the instructions here to convert it to PDF, DOCX, or PPTX without regenerating the content.

**When to use this guide:**
- User has existing blueprint markdown file
- User requests PDF, Word, or PowerPoint version
- Goal: Save tokens and time by skipping content regeneration

---

## Markdown to PDF Conversion

### Option 1: Pandoc (Recommended)

**Installation**:
```bash
# macOS
brew install pandoc
brew install basictex  # For LaTeX support

# Ubuntu/Debian
sudo apt-get install pandoc texlive
```

**Conversion Command**:
```bash
pandoc blueprint.md -o blueprint.pdf \
  --pdf-engine=xelatex \
  --toc \
  --toc-depth=2 \
  --number-sections \
  -V geometry:margin=1in \
  -V fontsize=11pt \
  -V documentclass=article
```

**With Custom Styling**:
```bash
pandoc blueprint.md -o blueprint.pdf \
  --pdf-engine=xelatex \
  --toc \
  --template=custom-template.tex \
  --highlight-style=tango \
  -V colorlinks=true
```

**Output**: Professional PDF with table of contents, page numbers, headers

---

### Option 2: Markdown to HTML to PDF

**Step 1: Convert to HTML**:
```bash
pandoc blueprint.md -o blueprint.html \
  --standalone \
  --css=styles.css \
  --toc
```

**Step 2: HTML to PDF** (using wkhtmltopdf or Chrome):
```bash
# Using wkhtmltopdf
wkhtmltopdf blueprint.html blueprint.pdf

# Using Chrome headless
chrome --headless --print-to-pdf=blueprint.pdf blueprint.html
```

---

### Option 3: Online Tools (No Installation)

**Tools**:
- **Dillinger** (dillinger.io): Markdown editor with PDF export
- **Markdown PDF** (VS Code extension): Right-click → Export to PDF
- **Typora**: Markdown editor with built-in PDF export

**Process**:
1. Open blueprint.md in tool
2. Click Export → PDF
3. Download generated PDF

---

## Markdown to DOCX (Microsoft Word)

### Option 1: Pandoc (Recommended)

**Basic Conversion**:
```bash
pandoc blueprint.md -o blueprint.docx \
  --toc \
  --toc-depth=2 \
  --reference-doc=template.docx
```

**With Custom Template**:
1. Create `template.docx` with desired styles (heading fonts, colors, logo)
2. Run conversion:
```bash
pandoc blueprint.md -o blueprint.docx --reference-doc=template.docx
```

**Output**: Word document with proper headings, formatting, table of contents

---

### Option 2: Copy-Paste with Formatting

**Tools**:
- **Typora**: Open markdown, File → Export → Word (.docx)
- **MacDown** (macOS): Export to Word
- **VS Code**: Use Markdown Preview Enhanced extension

**Manual Process**:
1. Preview markdown in tool
2. Copy formatted content
3. Paste into Word
4. Adjust styling as needed

---

## Markdown to PPTX (PowerPoint)

### Approach: Section-Based Slide Conversion

Markdown is linear text, PowerPoint is slide-based. Need to convert sections to slides.

**Option 1: Pandoc Slide Conversion**

```bash
pandoc blueprint.md -o blueprint.pptx \
  --slide-level=2 \
  --reference-doc=template.pptx
```

**Slide-Level Logic**:
- `#` (H1) = Title slide
- `##` (H2) = New slide
- `###` (H3) = Bullet point or sub-section

**Limitations**:
- Tables and complex formatting may not convert well
- Manual cleanup usually needed
- Best for simple, bullet-heavy content

---

### Option 2: Manual Slide Creation (Recommended for Executive Decks)

**Process**:
1. **Extract Key Sections** from markdown:
   - Executive Summary → Slide 1-2
   - Business & Monetization → Slides 3-5
   - Technical Architecture (diagram) → Slide 6
   - Economics & Cost → Slide 7
   - Responsible AI → Slide 8
   - Execution Roadmap → Slide 9
   - Recommendation → Slide 10

2. **Create Slide Template**:
   - Corporate branding
   - Consistent fonts and colors
   - Slide numbers and footers

3. **Populate Slides**:
   - Copy-paste content from markdown
   - Simplify text (slides are visual, not text-heavy)
   - Add charts, diagrams, and visuals
   - Use bullet points over paragraphs

**Executive Deck Structure**:
```
Slide 1: Title (Use Case Name, Date, Author)
Slide 2: Executive Summary (Problem, Solution, ROI)
Slide 3: Strategic Positioning (Quadrant, Value Prop, Moat)
Slide 4: Target Market & Segments (TAM/SAM/SOM)
Slide 5: Pricing Strategy (Recommended model + tiers)
Slide 6: Technical Architecture (Diagram)
Slide 7: Unit Economics & ROI (Cost breakdown, break-even)
Slide 8: Responsible AI (Principles + Compliance)
Slide 9: Execution Roadmap (Q1-Q4 milestones)
Slide 10: Go/No-Go Recommendation (Next steps)
```

---

### Option 3: Use AI to Convert Markdown to Slides

**Process**:
1. Provide blueprint markdown to AI
2. Ask: "Convert this markdown into 10 PowerPoint slides. For each slide, provide: Title, bullet points (max 5), and notes."
3. AI outputs slide-by-slide content
4. Manually create slides in PowerPoint using AI's structure

**Prompt Example**:
```
Convert the following AI blueprint markdown into a 10-slide executive
presentation. For each slide, provide:
- Slide title
- 3-5 bullet points (concise, executive-friendly)
- Speaker notes (2-3 sentences)

Focus on: Executive Summary, Business Model, Architecture, Economics,
Roadmap, and Recommendation.

[Paste blueprint markdown here]
```

---

## Lean Canvas to One-Page PDF

### Specialized Conversion for Lean Canvas

The lean-canvas-template.md is designed to be a **one-page document**. Convert it differently from the full blueprint.

**Option 1: Landscape PDF**

```bash
pandoc lean-canvas.md -o lean-canvas.pdf \
  --pdf-engine=xelatex \
  -V geometry:paperheight=8.5in \
  -V geometry:paperwidth=11in \
  -V geometry:margin=0.5in \
  -V fontsize=9pt
```

**Option 2: Fit to One Page**

```bash
pandoc lean-canvas.md -o lean-canvas.pdf \
  --pdf-engine=xelatex \
  -V geometry:margin=0.4in \
  -V fontsize=8pt \
  -V linestretch=0.9
```

**Result**: Single-page Lean Canvas PDF suitable for printing or sharing

---

## Best Practices

### For PDF Conversion

**Do**:
- Use pandoc with LaTeX for professional output
- Include table of contents for long documents
- Set reasonable margins (1 inch) and font size (11pt)
- Add page numbers and headers/footers

**Don't**:
- Convert without testing (always review output)
- Use tiny fonts to fit content (reduce content instead)
- Forget to check diagrams render correctly

---

### For DOCX Conversion

**Do**:
- Use custom template.docx for branding
- Set proper heading styles (Heading 1, 2, 3)
- Include table of contents
- Test on Windows and Mac

**Don't**:
- Assume formatting will be perfect (always review)
- Use complex markdown tables (simplify first)
- Forget to enable track changes for collaborative editing

---

### For PPTX Conversion

**Do**:
- Simplify content for slides (bullets, not paragraphs)
- Use visuals (diagrams, charts, icons)
- Follow corporate slide template
- Limit to 10-15 slides for executive decks

**Don't**:
- Auto-convert without review (slides need manual cleanup)
- Use dense text (slides are visual, not documents)
- Forget speaker notes (add context for presenters)

---

## Troubleshooting

### Pandoc Not Installed

**Error**: `pandoc: command not found`

**Solution**:
```bash
# macOS
brew install pandoc

# Windows
choco install pandoc

# Linux
sudo apt-get install pandoc
```

---

### LaTeX Not Installed (PDF Generation Fails)

**Error**: `pdflatex not found`

**Solution**:
```bash
# macOS
brew install basictex

# Windows
# Download MiKTeX from miktex.org

# Linux
sudo apt-get install texlive
```

---

### Diagrams Don't Render

**Issue**: Mermaid or ASCII diagrams don't convert well to PDF/DOCX

**Solution**:
- **Mermaid**: Use https://mermaid.live to render diagrams to images, then insert images
- **ASCII**: Convert to plain text or use image screenshots
- **Tables**: Simplify complex tables before conversion

---

### Formatting Lost in Conversion

**Issue**: Markdown formatting doesn't match output

**Solution**:
- Use custom templates (template.docx, template.pptx)
- Manually adjust after conversion
- Use styles consistently (Heading 1, 2, 3 for hierarchy)

---

## Summary

**Quick Reference**:

| Format | Recommended Tool | Command |
|--------|------------------|---------|
| PDF | Pandoc | `pandoc blueprint.md -o blueprint.pdf --pdf-engine=xelatex --toc` |
| DOCX | Pandoc | `pandoc blueprint.md -o blueprint.docx --reference-doc=template.docx` |
| PPTX | Manual | Extract key sections, create slides manually or use AI assist |
| Lean Canvas PDF | Pandoc | `pandoc lean-canvas.md -o lean-canvas.pdf -V geometry:margin=0.5in` |

**When to skip conversion and regenerate**:
- User requests significant content changes
- Original markdown is incomplete or outdated
- User wants to add new sections not in existing markdown

**When to convert existing markdown**:
- Content is complete and accurate
- User just needs different format (PDF, Word, PowerPoint)
- Goal is to save time and tokens

---

**Version**: 1.0
**Last Updated**: October 2025
