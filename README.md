# mockup-apply

Claude Code skill for applying HTML mockup designs to existing web pages.

## What it does

Takes an HTML mockup file and systematically applies it to your existing codebase:

1. **Analyze** - Compares mockup vs current code, classifies changes as ADD/CHANGE/KEEP
2. **Design Sync** - Updates design tokens (DESIGN.md) and common CSS classes
3. **Implement** - Applies changes one by one, preserving all existing functionality
4. **Verify** - Console error check, screenshot, user confirmation

## Key principle

```
ADD:    In mockup, not in code     → Implement
CHANGE: In both, but different     → Modify
KEEP:   In code, not in mockup     → Never remove
```

Existing features (dark mode, language toggle, data loading, APIs) are always preserved, even if the mockup doesn't include them.

## Install

```bash
# Clone to Claude Code skills directory
git clone https://github.com/<your-username>/mockup-apply.git ~/.claude/skills/mockup-apply
```

## Usage

```
/mockup-apply path/to/mockup.html
/mockup-apply path/to/mockup.html --page dashboard
/mockup-apply path/to/mockup.html --analyze-only
```

## Requirements

- [Claude Code](https://claude.com/claude-code)
- Playwright MCP (for verification screenshots)

## License

MIT
