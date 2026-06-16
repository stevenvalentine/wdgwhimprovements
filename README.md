# wdgwhimprovements

Notes !
Publishing Your Second GitHub Repository to GitHub Pages
Step-by-Step Fix
Step 1 — Check Your Repository Settings
1. Go to your second repository on GitHub
   e.g. https://github.com/YOUR-USERNAME/REPO-NAME

2. Click the "Settings" tab
   (gear icon — top right of repository)

3. In the LEFT sidebar scroll down and click "Pages"
4. Step 2 — Enable GitHub Pages
5. You will see this screen under Settings → Pages:

┌─────────────────────────────────────────────────────────┐
│  GitHub Pages                                           │
│                                                         │
│  Source                                                 │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Deploy from a branch              ▼             │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  Branch                                                 │
│  ┌──────────────┐    ┌──────────────┐                  │
│  │  main    ▼  │    │  / (root) ▼  │   [ Save ]       │
│  └──────────────┘    └──────────────┘                  │
│                                                         │
└─────────────────────────────────────────────────────────┘

Set EXACTLY:
  Source:  Deploy from a branch
  Branch:  main
  Folder:  / (root)

Then click SAVE
Step 3 — Verify Your File Structure
Your repository MUST have index.html
in the ROOT folder (not inside a subfolder)

CORRECT ✅                    WRONG ✗
──────────────────────────    ──────────────────────────
repo-name/                    repo-name/
├── index.html                ├── src/
├── data/                     │   └── index.html
│   └── tasks.csv             ├── data/
└── README.md                 │   └── tasks.csv
                              └── README.md

If index.html is inside a subfolder
GitHub Pages cannot find it.
Step 4 — Check Repository is Public
GitHub Pages REQUIRES a public repository
on the free plan.

To check:
1. Settings → General
2. Scroll to bottom → "Danger Zone"
3. Look for "Change repository visibility"
4. If it says "Make public" → repository is PRIVATE
   Click it → Type repo name → Confirm

┌─────────────────────────────────────────────────────────┐
│ Danger Zone                                             │
│                                                         │
│ Change repository visibility                            │
│ This repository is currently PRIVATE                    │
│ [ Make public ]   ← click this if showing              │
└─────────────────────────────────────────────────────────┘

Your Daily Workflow (30 Seconds)
Every morning:

1. Open Microsoft Planner
   → Click ⋯ menu → Export plan to Excel → Save file

2. Open the saved Excel file
   → File → Save As → Browse → choose CSV (Comma delimited)
   → Name it exactly:  tasks.csv
   → Click Save

3. Go to your GitHub repository
   → Click the  data  folder
   → Click  tasks.csv
   → Click the pencil icon ✏️  OR  drag new file to upload
   → If uploading: Add file → Upload files → drag tasks.csv
   → Commit message: "Update tasks DD/MM/YYYY"
   → Click Commit changes

4. Wait 60 seconds

5. Refresh your dashboard URL
   → All numbers, charts and tables update automatically ✅
Final Repository Structure
warehouse-dashboard/
├── index.html          ← Updated dashboard (reads CSV on load)
├── data/
│   └── tasks.csv       ← Your daily Excel export goes here
├── README.md
├── LICENSE
└── .gitignore

Daily Excel Upload → Auto-Update Dashboard on GitHub
How It Works
You export Excel → Upload to GitHub → Dashboard reads it → Numbers update automatically
        ↓                  ↓                    ↓                      ↓
  Microsoft Planner   Drag & drop file     JavaScript fetches      All charts & KPIs
  exports .xlsx       to GitHub repo       the CSV on load         refresh instantly
  Step 1 — Add This File to Your Repository
  data/tasks.csv
Create a folder called data in your repository and add this file.
This is your sample starting CSV — replace it each time with your export.
