# DATASCI 350 - Data Science Computing

## Quiz 01 - Forking and improving an existing GitHub repository

### The scenario

This repository holds a small climate-station project: sensor readings, three Python scripts, and some notes. You take over as its maintainer. Your job is to reorganise it from the command line and record everything you do.

### Instructions

This quiz is worth 6% of the final grade. Complete the tasks below with command-line operations and Git commands, as covered in lectures 02 to 07. The quiz is open-book and open-notes. It is an individual assessment: do not discuss the questions with your colleagues during class. You have 75 minutes.

You may use AI tools on the same terms as the rest of the course: they are allowed, and you must be able to explain every command you submit. The instructor may ask any student to walk through part of their work, during the quiz or right after it. An answer you cannot explain earns no marks.

Record every command in a file named `commands.txt` (or a Jupyter notebook named `commands.ipynb`) in the repository's root directory. The final repository on GitHub must reflect all changes, and `commands.txt` must list every command you used.

Work from the command line throughout. Files created or uploaded through the GitHub website lose points: the grader checks your commit history.

When you finish, post the link to your repository on Canvas, in the "Assignments" tab under Quiz 01.

### If `git push` asks for credentials

Your machine should already be logged in to GitHub (see the lecture 08 review). If a push still fails with an authentication error, do not waste time creating tokens: run `gh auth login`, choose GitHub.com, then HTTPS, and log in with the browser. After that, `git push` works normally.

### Setup

1. Fork this repository to your GitHub account.
2. Clone your fork to your machine with the command line.
3. Change directory into the cloned repository.
4. Create `commands.txt` (or `commands.ipynb`) in the root of the repository.

### Tasks

1. Create and switch to a new branch named `station-upgrade` in a single command.
2. Create a new directory named `results` in the repository.
3. Create an empty file `results/summary.md`, then append this exact line to it from the command line: `Analysis of the first field season.`
4. Stage the `results` directory and commit with the message "Add results directory".
5. Rename `data/sensor-readings.csv` to `data/station-data.csv` from the command line.
6. Create a directory named `archive` inside `scripts`, then copy every `.py` file from `scripts` into it. *Use a wildcard for the copy and chain both commands in a single line.*
7. Delete the file `docs/notes.md` from the command line.
8. Stage all changes and commit with the message "Update station files".
9. Create a `.gitignore` file in the root of the repository and append these two lines to it from the command line:

    ```text
    temp/
    log?.txt
    ```

10. Display the contents of `.gitignore` from the command line.
11. Stage and commit `.gitignore` with the message "Add gitignore". *Use a single line for both steps.*
12. Create four empty files `log1.txt` through `log4.txt` in the root of the repository *with a single brace-expansion command*.
13. Run `git status`. The log files must not appear in the output. Paste the output into `commands.txt` and add one sentence explaining why they do not appear.
14. Count the lines of `data/station-data.csv` with a single command and append the resulting number to `results/summary.md` from the command line.
15. Open `scripts/03-plot.py` and add this exact comment as a new line at the top of the file: `# Reviewed for the field season report`. Then run `git diff`, paste the output into `commands.txt`, and add one sentence explaining what the lines starting with `+` mean.
16. Stage all changes and commit with the message "Update analyss" (with this exact typo).
17. Fix the last commit message with a single command so it reads "Update analysis".
18. Switch back to the `main` branch and merge `station-upgrade` into it.
19. Show the history with `git log --oneline` and paste the output into `commands.txt`.
20. Update `commands.txt` with all commands used, stage it, commit with the message "Add command log", and push everything to your fork. Done! 😊

### Bonus tasks

Attempt these only after finishing the main tasks, if you still have time (and like challenges). Document every step in `commands.txt`.

1. Open a pull request from your fork to the original repository (this one). Document each step of the process.
2. Perform an interactive rebase to squash the last two commits into a single commit.

Best of luck!
