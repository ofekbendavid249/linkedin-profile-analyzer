# 🔍 LinkedIn Profile Analyzer — Claude Code Skill

> A Claude Code skill that reads your LinkedIn profile export and gives you an **honest, scored critique** with specific improvements. No sugarcoating.

---

## 💡 What it does

- Reads your `Profile.csv` exported directly from LinkedIn
- Asks you a few quick questions to fill in the gaps (experience, skills, photo)
- Scores 5 categories: Headline, Summary, Experience, Skills, Profile completeness
- Returns direct feedback + a suggested improved headline written for you
- Lists the **top 3 fixes** to do immediately

---

## ⚡ Quick start

**Step 1 — Export your LinkedIn profile**

1. Go to LinkedIn → **Settings & Privacy** → **Data Privacy**
2. Click **"Get a copy of your data"**
3. Select **"Profile"**
4. Click **"Request archive"** — arrives by email within 10–30 minutes
5. Extract the ZIP and copy `Profile.csv` to your working directory

**Step 2 — Add the skill to your project**

Download `SKILL.md` from this repository and place it in the same directory as your `Profile.csv`.

**Step 3 — Run it**

Open Claude Code in that directory and run:

```
read the file SKILL.md in this directory and then analyze my LinkedIn profile using the Profile.csv file here
```

That's it. Claude Code will read your profile, ask a few questions, and return a full analysis.

---

## 📊 Example output

```
## LinkedIn Profile Analysis — Ofek Ben David

Overall score: 58/100

> Your summary is completely empty and your headline
> doesn't differentiate you from any other CS student.

### Headline — 55/100
The current headline tells a recruiter your title and company,
but nothing about what you actually build or what makes you different.

Current: "Software Developer Intern at LeadSpotting | CS Student"
Suggested: "Building AI-powered dev tools | CS Final Year |
            React · Python · Claude Code"

### Summary — 10/100
No summary exists. This is the single biggest missed opportunity
on your profile — recruiters read this first.

Suggested summary:
"Final-year CS student with hands-on experience building
production systems. Currently interning at LeadSpotting
where I work on data labeling infrastructure using React
and Flask. Passionate about AI tooling and automation —
I build things, ship them, and share what I learn."

...

## Top 3 fixes
1. Write a summary — even 3 sentences beats nothing
2. Rewrite your headline to show what you build, not just where you are
3. Add at least 8 specific technical skills
```

---

## 📁 Files in this repo

| File | Description |
|------|-------------|
| `SKILL.md` | The skill file — place this in your working directory |
| `README.md` | This file |

---

## 🤔 Who is this for?

Anyone who uses **Claude Code** and wants honest feedback on their LinkedIn profile. Especially useful for:
- Students about to enter the job market
- Developers updating their profile after a new role
- Anyone who hasn't touched their LinkedIn in over a year

---

## 🌐 Want a web version anyone can use?

This skill requires Claude Code. If you'd like a version that works directly in the browser — no installation needed — drop a comment or reaction. If there's enough interest, I'll build it.

---

## ⭐ If this helped you

Give the repo a star — it helps others find it.

---

*Built by Ofek Ben David · CS Student & AI tooling enthusiast*
*(www.linkedin.com/in/ofek-ben-david)*
