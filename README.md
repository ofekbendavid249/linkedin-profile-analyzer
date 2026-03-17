# LinkedIn Profile Analyzer — Claude Code Skill

A Claude Code skill that reads your LinkedIn profile export and gives you an honest, scored critique with actionable improvements.

## What it does

- Reads your `Profile.csv` exported from LinkedIn
- Scores 5 categories: Headline, Summary, Experience, Skills, Overall presence
- Gives direct feedback — no sugarcoating
- Suggests specific improvements including a rewritten headline

## Installation

1. Clone or download this repository
2. Place `SKILL.md` in your project directory (or in `~/.claude/skills/`)
3. Done — Claude Code will detect it automatically

## How to export your LinkedIn profile

1. Go to **LinkedIn → Settings → Data Privacy**
2. Click **"Get a copy of your data"**
3. Select **"Profile"** only
4. Click **"Request archive"**
5. You'll receive an email with a ZIP file — extract `Profile.csv`

## Usage

Place `Profile.csv` in the same directory, then run Claude Code and say:

```
analyze my LinkedIn profile
```

## Example output

```
## LinkedIn Profile Analysis — Ofek Levi

Overall score: 61/100

> Your headline is a missed opportunity and your summary doesn't exist.

### Headline — 55/100
"Computer Science Student at Bar-Ilan University" tells a recruiter nothing 
about what you actually do or what value you bring...
```

## Built by

Ofek Levi — CS student building AI tools.
Follow on LinkedIn: [your LinkedIn URL]

