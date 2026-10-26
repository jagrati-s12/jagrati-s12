# Setup — Jagrati Sharma's GitHub profile

This is the customized version of the original profile template. The layout and section structure are retained, with Jagrati's links, skill radar, project cards, and profile portrait.

## 1. Repository

Create/use the **public** repository named exactly `jagrati-s12` at https://github.com/jagrati-s12/jagrati-s12. Copy the contents of this folder into that repository; do not copy the outer folder as an extra nested directory. Preserve `.github/workflows/`.

## 2. Check your details

- GitHub: https://github.com/jagrati-s12
- LinkedIn: https://www.linkedin.com/in/jagrati-sharma-6a2b5a2ab/
- Email: sjagrati822@gmail.com
- LeetCode: https://leetcode.com/u/jag_281/

Check the repository names in `assets/projects.json` and the project links in `README.md` before publishing. If a repo has a different spelling or is not public, update it. The `assets/skills.json` values are illustrative self-ratings; edit them to reflect your own comfort level.

## 3. Generate local assets (optional)

Install Python 3.10+ if needed, then from this folder run:

```powershell
python scripts\radar.py --data assets/skills.json -o assets/radar
python scripts\cards.py --user jagrati-s12 --projects assets/projects.json --out assets
```

The charts script uses your public GitHub repository language data. If API rate limits prevent it from running locally, the GitHub Actions workflow can regenerate the charts after upload.

## 4. GitHub Actions permissions

In the repository, go to **Settings → Actions → General → Workflow permissions**, select **Read and write permissions**, and save. The workflows need permission to commit generated SVGs and publish the snake to the `output` branch.

## 5. Token setup (no personal token required)

This version uses GitHub Actions' built-in `GITHUB_TOKEN`; you do **not** need to create or store a personal access token. The workflows only request repository write access to publish generated SVG assets. Public-profile metrics are generated from information GitHub makes available to the workflow. Some Metrics plugins may return reduced data with the built-in token; if a plugin specifically reports an authorization/rate-limit error, the rest of the profile can still work without adding a personal token.

Never paste tokens or passwords into tracked files.

## 6. Run the workflows

Open **Actions** and run each workflow manually if the option is available:

| Workflow | Purpose |
|---|---|
| Metrics | Refreshes the contribution calendar, language statistics, habits, and achievements |
| Snake | Generates snake SVGs and publishes them to the `output` branch |
| Charts and cards | Refreshes the skill radar, language radar, and project/stat cards |

The snake image will be unavailable until its workflow successfully creates the `output` branch. The metrics cards in the ZIP are safe starter placeholders and will be replaced by live, account-specific results after a successful run.

## 7. Before publishing

- Do not upload `.env` files, API tokens, private keys, or passwords.
- Keep `.github/workflows/`; those files are essential.
- Verify every featured project link is yours and public.
- Do not claim a GPA or achievement unless you want it displayed and it is accurate.
