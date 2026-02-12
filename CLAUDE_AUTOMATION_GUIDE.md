# Claude Automated Weekly Briefing Publishing Guide

## Overview
This guide enables Claude to automatically generate and publish weekly data management briefings to GitHub.

## How It Works

### Option 1: Using GitHub Actions Web UI (Recommended for now)

1. **Generate your briefing** using your Claude task in Perplexity
2. **Copy the briefing content** to your clipboard
3. **Go to GitHub Actions**: https://github.com/srjbridge/data-management-briefing/actions
4. **Select "Publish Weekly Briefing" workflow**
5. **Click "Run workflow"**
6. **Paste your briefing content** into the "Briefing Content" field
7. **Click "Run workflow"** to publish

### Option 2: Claude Native Integration (Coming Soon)

When Claude can directly access GitHub APIs, it will:
1. Generate the briefing
2. Automatically create a dated post file
3. Commit it to the repository
4. Trigger site rebuild
5. Publish to https://srjbridge.github.io/data-management-briefing/

## Briefing Format

Your Claude task should generate briefings in this markdown format:

```markdown
## What's New
Developments and trends in data management

### [Headline](link)
Brief description of the development.

**Why it matters:** Impact and relevance.

---

## What's Innovative
New tools and approaches in data management

### [Headline](link)
Description of the innovation.

**Why it matters:** Importance and use cases.

---

## What's Controversial
Debates and disagreements in the field

### [Headline](link)
Description of the controversy.

**Why it matters:** Why this matters to practitioners.

---

## What's in the Lab
Announcements from research and government

### [Headline](link)
Description of research or announcement.

**Why it matters:** Relevance and impact.

---

## What's in Academe
New research and academic developments

### [Headline](link)
Description of academic work.

**Why it matters:** Significance for the field.
```

## Perplexity Task Configuration (Claude)

### Current Setup
- **Space**: Daily Briefing
- **Schedule**: Every Monday at 8:00 AM ET
- **Model**: [Change from ChatGPT to Claude]
- **Prompt**: Generate weekly data management briefing

### To Change to Claude:
1. Go to: https://www.perplexity.ai/spaces/daily-briefing-[your-space-id]
2. Click the model selector (currently shows GPT-5.2)
3. Select "Claude 3.5 Sonnet" or latest Claude model
4. Save changes
5. Task will now run with Claude

## Key Information for Claude

### Data Sources to Monitor
- Canadian Government data initiatives
- Open Data portals
- Data management research papers
- Industry news and trends
- Government announcements

### Briefing Sections
- **What's New**: 2-3 recent developments
- **What's Innovative**: 2-3 new tools/approaches
- **What's Controversial**: 1-2 active debates
- **What's in the Lab**: 1-2 research announcements
- **What's in Academe**: 1-2 academic papers

### Formatting Requirements
- Use markdown format
- Include links to sources
- Add "Why it matters" section for each item
- Keep descriptions concise (2-3 sentences max)
- Use consistent structure across sections

## Publishing Instructions for Claude

### Step 1: Generate Briefing
Your Perplexity task generates the briefing every Monday at 8:00 AM ET.

### Step 2: Trigger Publishing
Unce you have the briefing content:

1. Navigate to: https://github.com/srjbridge/data-management-briefing/actions
2. Click on "Publish Weekly Briefing" in the left sidebar
3. Click "Run workflow" button
4. In the dialog:
   - **Briefing Title**: (optional) Leave blank for auto-generated date-based title
   - **Briefing Content**: Paste your complete briefing in markdown format
5. Click "Run workflow"

### Step 3: Site Updates
- GitHub Actions creates a dated post file
- Jekyll rebuilds the site automatically
- Content goes live at https://srjbridge.github.io/data-management-briefing/

## Troubleshooting

### Workflow fails
- Check content is valid markdown
- Ensure no special characters break YAML formatting
- Verify briefing content is not empty

### Site doesn't update
- Wait 2-3 minutes for GitHub Pages rebuild
- Clear browser cache (Ctrl+Shift+R)
- Check: https://github.com/srjbridge/data-management-briefing/actions for deployment status

### Content formatting issues
- Wrap multi-line content in proper markdown
- Use `**bold**` for emphasis
- Use `[text](url)` for links
- Use `---` for section breaks

## Next Steps

1. **Change Perplexity task to Claude** (see instructions above)
2. **Test the workflow** with sample briefing content
3. **Verify publication** at the live site
4. **Optional**: Set up scheduled publishing to GitHub

## Files Involved

- `.github/workflows/publish-briefing.yml` - The automation workflow
- `_posts/` - Where weekly briefings are stored
- `_config.yml` - Jekyll configuration
- `assets/style.css` - Site styling

## Support

For issues or questions, check:
- GitHub Actions logs: https://github.com/srjbridge/data-management-briefing/actions
- Site status: https://github.com/srjbridge/data-management-briefing/deployments
