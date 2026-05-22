# Push the AAOIFI SME skill to GitHub — setup steps

This file contains the exact commands to (a) clean up a half-created `.git/` folder, (b) initialize a fresh git repository, (c) commit everything, and (d) push to GitHub.

## 0. One-time cleanup (only once)

A half-initialized `.git/` folder was created during the build by the sandbox and could not be cleaned up due to a cross-OS file-permission issue. Delete it once before you start:

**PowerShell (run as your normal user, not admin):**

```powershell
Remove-Item -Path "D:\AWA\AAOIFI\.git" -Recurse -Force
```

**Or in File Explorer:** show hidden items (View → Show → Hidden items), then delete the `.git` folder inside `D:\AWA\AAOIFI`.

## 1. Create an empty public repository on GitHub

1. Open https://github.com/new
2. **Repository name**: `aaoifi-sme-skill` (or any name you prefer — adjust the commands below to match)
3. **Description**: *"Claude skill — Senior SME on AAOIFI standards for Islamic Financial Institutions"*
4. **Public** (per your choice in chat)
5. Do **not** initialize with a README, .gitignore, or license — this repo already has those.
6. Click **Create repository**
7. Copy the HTTPS URL — it will look like `https://github.com/<your-username>/aaoifi-sme-skill.git`

## 2. Initialize, commit, and push (PowerShell or Git Bash)

Run these from `D:\AWA\AAOIFI`. Replace `<your-username>` with your actual GitHub username (or replace the whole URL with the one GitHub gave you in step 1).

```powershell
cd D:\AWA\AAOIFI

git init -b main
git config user.email "amir.wahmed@gmail.com"
git config user.name  "Amir W. Ahmed"

git add .
git commit -m "feat: initial release of AAOIFI SME skill v1.0"

git remote add origin https://github.com/<your-username>/aaoifi-sme-skill.git
git push -u origin main
```

GitHub will prompt for authentication on the `git push` step. Three options:

- **GitHub CLI (recommended)** — install [GitHub CLI](https://cli.github.com/), then run `gh auth login` once before `git push`. After that, all pushes are seamless.
- **Personal Access Token (PAT)** — when prompted for password, paste a PAT scoped to `repo` (create one at https://github.com/settings/tokens). Save the credential via Windows Credential Manager.
- **SSH** — if you already have SSH keys set up, use the SSH URL `git@github.com:<your-username>/aaoifi-sme-skill.git` instead of HTTPS.

## 3. Verify

After the push succeeds:

```powershell
git log --oneline
git remote -v
start https://github.com/<your-username>/aaoifi-sme-skill
```

The repo page should show:

- `README.md` rendered at the bottom
- The folder layout `aaoifi-sme/`, `source-materials/`, `SETUP.md`, `LICENSE`, `.gitignore`
- A single initial commit by Amir W. Ahmed

## 4. Optional next steps

- **Add a topic tag** on GitHub: `claude-skill`, `islamic-finance`, `aaoifi`, `islamic-banking`, `shariah` — helps discovery.
- **Pin a release**: tag this commit as `v1.0` via `git tag v1.0 && git push origin v1.0`, then create a Release on GitHub with the changelog from the commit message.
- **Enable GitHub Pages** off the README for a public landing page (optional).
- **Add a `CONTRIBUTING.md`** if you plan to accept PRs.
- **Add a `.github/workflows/`** CI workflow that validates the SKILL.md frontmatter on every push (e.g., description length, reference resolution) — there's a draft of these checks in the `python3` validation block we ran during the build.

## What's already in the repo

```
D:\AWA\AAOIFI\
├── README.md                                ← public-facing repo intro
├── LICENSE                                  ← proprietary educational/professional licence
├── .gitignore
├── SETUP.md                                 ← this file
├── aaoifi-sme\                              ← the installable skill
│   ├── SKILL.md                             ← entrypoint, 1023-char description, 129 lines body
│   └── references\
│       ├── standards-catalogue.md           ← all 117+ standards numbered
│       ├── fas-deep-dive.md                 ← FAS 1, 28, 30, 32, 33, 35, 39, 40, 42, 43, 44, 53
│       ├── shariah-standards-deep-dive.md   ← SS 5, 8, 9, 17, 23, 26, 30, 40, 49, 57, 59
│       ├── audit-governance-ethics.md       ← ASIFI 1-8, GSIFI 1-14, Codes of Ethics
│       ├── jurisdictional-overlay.md        ← Pakistan, GCC, Malaysia, Indonesia, UK
│       ├── decision-frameworks.md           ← Shari'ah gate, ECL stages, Sukuk classification
│       └── deliverable-templates.md         ← DOCX, XLSX, PPTX, PDF templates
└── source-materials\
    └── ED-of-FAS-__-Direct-Costs-Determination-Attribution-and-Reimbursement.pdf
```

All set. You should be able to run the four commands in section 2 above and have the repo live in under a minute.
