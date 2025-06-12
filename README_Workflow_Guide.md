# RStudio Project Workflow Guide (Team Version)

This guide helps all team members collaborate using RStudio + GitHub, with correct Git practices.

---

## 1. Open the RStudio Project

- Double-click the file `CarAccidents.Rproj`  
  **OR**  
- In RStudio: `File -> Open Project -> CarAccidents`

> This sets your working directory correctly and loads Git, files, and Git integration.

---

## 2. Pull the Latest Code from `main` Branch

Always pull the most recent version of the project before starting your work:

In RStudio Git tab:
- Click the `Pull` button

Or in the Terminal tab in RStudio:
```bash
git checkout main
git pull origin main
```

---

## 3. Create Your Own Branch (Per Task or Feature)

To avoid conflicts, every teammate should work on a **separate branch**.

### Where to run this:
- Open the **Terminal** tab at the bottom of RStudio  
  (or go to `Tools -> Terminal -> New Terminal`)

Then run:
```bash
git checkout -b feature-yourname-task
```

Examples:
```bash
git checkout -b feature-ohad-eda
git checkout -b bugfix-daniel-import
```

You are now working in your own copy of the project.

---

## 4. Open Your Script

- Open the file you’re working on (e.g. `scripts/analyze_accidents.R`)
- Or create a new `.R` file and save it inside the project folder

---

## 5. Load Your Data (if needed)

Use one of the following methods to load your data:

```r
library(readr)
accidents <- read_csv("data/accidents.csv")
```

> ⚠️ If the file is too large to be stored on GitHub, download it manually from the shared folder (Google Drive, Dropbox, etc.) and place it in the `data/` folder.

---

## 6. Save, Stage, Commit and Push (Using RStudio Buttons)

Once you’ve made changes:

1. Go to the **Git tab** in RStudio
2. Check the boxes next to the files you changed
3. Click **Commit**
4. Write a short description (e.g., `"Added EDA script for crashes"`)
5. Click **Commit**
6. Then click **Push** to upload your branch to GitHub

---

## 7. Open a Pull Request (PR) on GitHub

1. Go to your repository on GitHub
2. Switch to your branch (top-left dropdown)
3. Click **"Compare & pull request"**
4. Describe your changes and click **Create pull request**

> Your teammates can now review and merge your work into `main`.

---

## 8. After Merge: Pull `main` Again

Once your branch is merged into `main`, update your local copy:

In the **Terminal** tab:
```bash
git checkout main
git pull origin main
```

---

## ✅ Daily Checklist

| Step           | Description                            |
|----------------|----------------------------------------|
| Open project   | Open `CarAccidents.Rproj`              |
| Pull main      | Click `Pull` or run `git pull origin main` |
| Create branch  | `git checkout -b feature-name-task` in Terminal |
| Work           | Write and save code                    |
| Commit + Push  | Use Git tab buttons in RStudio         |
| PR             | Open a pull request on GitHub          |
| Update main    | Pull again after merging               |

---

## 🧠 Pro Tips

- **Never work directly on `main`**
- **Name branches clearly**: `feature-`, `bugfix-`, `doc-` etc.
- **Always pull `main` before starting new work**
