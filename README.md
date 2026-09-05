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


## Instruction

```markdown
Search web to find hot finance and technology news yesterday.
Then create a markdown file and write it.

File path: <year>/<MM>-<month>/<day>.md (relative to this folder).
- <year>: 4-digit year.
- <MM>-<month>: 2-digit month, dash, full month name in lowercase.
- <day>: day of month without leading zero.
- Example for 4 September 2026: 2026/09-september/4.md

Create the year and month folders if they do not exist.
Title inside the file: # Daily News — <day> <Month> <year>
Example: # Daily News — 4 September 2026

After the file is written, commit and push it:
1. Run: git add <the new file path>
   Do not add any other file.
2. If git status shows nothing staged, stop here. Do not commit or push.
3. Run: git commit -m "Add daily news for <day> <Month> <year>"
   Example: git commit -m "Add daily news for 5 September 2026"
4. Run: git push origin main
5. If push fails, run `git pull --rebase origin main` and push again.
Do not change git config or the remote.
```
