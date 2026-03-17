# LinkedIn Profile Analyzer

## Description
Analyzes a LinkedIn profile and returns an honest, scored critique with specific improvements. Works with LinkedIn's exported CSV file and fills in gaps by asking the user directly.

## Trigger phrases
- "analyze my LinkedIn profile"
- "review my LinkedIn"
- "score my LinkedIn profile"
- "what's wrong with my LinkedIn"
- "improve my LinkedIn profile"
- "נתח את הפרופיל שלי בלינקדין"

---

## How to export your LinkedIn profile CSV

1. Go to LinkedIn → **Settings & Privacy** → **Data Privacy**
2. Click **"Get a copy of your data"**
3. Select **"Profile"** and any other available options
4. Click **"Request archive"** — arrives by email within 10–30 minutes
5. Extract the ZIP and place `Profile.csv` in your working directory

---

## Instructions for Claude Code

### Step 1 — Locate the CSV
Look for `Profile.csv` in the current directory or any subdirectory.
If not found, tell the user exactly where to place it and stop.

### Step 2 — Extract available data from CSV
Read `Profile.csv` and extract:
- `First Name` + `Last Name` → full name
- `Headline` → title shown under their name on LinkedIn
- `Summary` → the "About" section (often empty)
- `Industry` → declared industry
- `Geo Location` → location

### Step 3 — Ask for missing data
LinkedIn's basic export does not include experience or skills. Ask the user:

```
I have your profile basics from the CSV. To give you a complete analysis, please provide:

1. Your current role (job title + company, or "student" / "looking for work")
2. Your last 1–3 positions: [title] at [company] — [one sentence of what you did]
3. Your top 5–10 skills (technologies, tools, languages)
4. Do you have a profile photo? (yes/no)
5. Do you have any recommendations on your profile? (yes/no)
```

Wait for the user's response before continuing.

### Step 4 — Analyze all 5 categories

Score each from 0–100. Be direct and specific. Do not sugarcoat.

---

#### Headline (0–100)
Evaluate:
- Does it say more than just a job title or "student at X"?
- Does it communicate value or differentiation?
- Is it specific and memorable?
- Does it use keywords relevant to the target role?

Deduct points for:
- Generic title with no differentiation (-20)
- "Looking for opportunities" with nothing else (-15)
- No mention of what they actually build or do (-20)
- Over 120 characters (-10)

Provide the current headline and a specific improved version.

---

#### Summary / About (0–100)
Evaluate:
- Does a summary exist? (empty = max 25 points)
- Does it tell a story or just list facts?
- Does it explain what the person is good at and what they want?
- Is it written in first person with personality?

Deduct points for:
- Empty summary (-75)
- Under 3 sentences (-40)
- No mention of skills or goals (-20)
- Reads like a CV bullet list (-15)

---

#### Experience (0–100)
Evaluate based on the positions provided:
- Are there measurable achievements or only job descriptions?
- Are impact verbs used (built, led, reduced, increased)?
- Is the scope of work clear?
- For students: is internship/project experience presented with impact?

Deduct points for:
- Only listing job titles with no descriptions (-40)
- No numbers or measurable outcomes (-25)
- Passive language ("responsible for") instead of active (-15)

---

#### Skills (0–100)
Evaluate:
- Minimum 5 skills recommended (under 5 = significant deduction)
- Are they specific (e.g. "React.js") not vague (e.g. "Communication")?
- Are they relevant to the target role?

Deduct points for:
- No skills listed (-80)
- Only soft skills (-40)
- Missing obvious skills for their role (-20)

---

#### Profile completeness (0–100)
Evaluate:
- Profile photo present? (no photo = -30)
- Location filled in?
- Industry set correctly?
- Any recommendations?
- Does the overall profile tell a coherent story?

---

### Step 5 — Output format

Use this exact structure:

---

## LinkedIn Profile Analysis — [Full Name]

**Overall score: [weighted average]/100**

> [One sentence capturing the single most important thing to fix. Be direct.]

---

### Headline — [score]/100
[2–3 sentences of honest feedback]

**Current:** "[current headline]"
**Suggested:** "[specific improved version tailored to their background]"

---

### Summary — [score]/100
[2–3 sentences of honest feedback]
[If empty, write a suggested 3-sentence summary based on what they provided]

---

### Experience — [score]/100
[2–3 sentences of honest feedback with a specific example of how to rewrite one bullet]

---

### Skills — [score]/100
[2–3 sentences of honest feedback]
[If missing obvious skills for their role, list them explicitly]

---

### Profile completeness — [score]/100
[2–3 sentences of honest feedback]

---

## Top 3 fixes — do these first

1. **[Most impactful fix]** — [one sentence explaining why]
2. **[Second fix]** — [one sentence]
3. **[Third fix]** — [one sentence]

---

*Built by Ofek Ben David · [GitHub link] · Give it a ⭐ if it helped*

---

## Scoring weights
- Headline: 25%
- Summary: 25%
- Experience: 25%
- Skills: 15%
- Profile completeness: 10%
