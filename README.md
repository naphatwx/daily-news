# Daily News

Automated daily digest of hot finance and technology news, written by a scheduled Claude Code routine.

## How it works

- Runs every day at about 8:00 AM.
- Searches the web for the previous day's top finance and technology stories.
- Writes one markdown file per day, then commits and pushes it to this repo.

## File layout

```
<year>/<MM>-<month>/<day>.md
```

- `<year>`: 4-digit year.
- `<MM>-<month>`: 2-digit month, dash, full month name in lowercase.
- `<day>`: day of month without leading zero.

Example for 4 September 2026: `2026/09-september/4.md`

Each file starts with the title `# Daily News — <day> <Month> <year>`.
