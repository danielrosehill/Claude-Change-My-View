# Change My View Workflow Reference

## Available Commands

### Core Workflow
- `/change-my-view` - Start a new debate (writes hot take, generates rebuttal, logs to JSON)
- `/first-run` - Initial repository setup and orientation

### Export & Publishing
- `/generate-pdf [debate_id]` - Generate a styled PDF from a debate
- `/build-index` - Create comprehensive indexes (HTML, MD, PDF, JSON) of all debates

### Utilities
- Agents for format export, podcast generation, and log validation are available

## Directory Structure

```
Claude-Change-My-View/
├── my-hot-takes/
│   └── processed/          # User's original hot takes
├── claude-responses/        # AI-generated rebuttals
├── exports/
│   ├── pdf/                # Individual debate PDFs
│   └── indexes/            # Catalog/index files
├── scripts/
│   ├── generate_pdf.py     # Reusable PDF generator
│   └── build_index.py      # Reusable index builder
├── log.json                # Master debate log
└── .claude/
    ├── commands/           # Slash commands
    └── agents/             # Specialized agents
```

## Workflow Steps

1. **Create a debate**: Use `/change-my-view` to state your position
2. **Review the rebuttal**: Check `claude-responses/` for the AI's counter-argument
3. **Export to PDF**: Run `/generate-pdf 1` to create a formatted PDF
4. **Build catalog**: Run `/build-index` to update the searchable index

## Automation with Scripts

After using the slash commands once, reusable Python scripts are generated in `/scripts`:

### Generate PDFs independently
```bash
# Single debate
python scripts/generate_pdf.py 1

# All debates
python scripts/generate_pdf.py --all
```

### Build indexes independently
```bash
# All formats
python scripts/build_index.py --format all

# Specific format
python scripts/build_index.py --format html

# Watch mode (auto-rebuild)
python scripts/build_index.py --format all --watch
```

## Index Features

The `/build-index` command creates:
- **Markdown index** - GitHub-friendly catalog
- **HTML index** - Interactive, searchable web interface
- **PDF catalog** - Printable reference with excerpts
- **JSON index** - Machine-readable with enhanced metadata

The HTML index includes:
- Sortable table (by date, word count, title)
- Search/filter functionality
- Statistics dashboard
- Preview tooltips
- Dark mode toggle
- Direct links to all files

## File Naming Convention

- Hot takes: `my-hot-takes/processed/{id:03d}_hottake.md`
- Rebuttals: `claude-responses/{id:03d}_response.md`
- PDFs: `exports/pdf/debate_{id:03d}.pdf`
- Debate IDs are zero-padded 3-digit numbers (001, 002, etc.)

## Future Enhancements

Consider adding:
- Tag/category system for debates
- Topic modeling and sentiment analysis
- Comparison views (side-by-side)
- RSS feed for new debates
- GitHub Pages hosting for HTML index
- Email digest of recent debates
