# 🏆 Auto GitHub Achievements

An automated GitHub Actions tool designed to help you farm GitHub profile badges—specifically **Pull Shark**, **YOLO**, and **Quickdraw**—without manual effort. 

By utilizing GitHub Actions and the GitHub CLI (`gh`), this workflow automatically creates dummy branches, commits, opens Pull Requests, and immediately merges them to fulfill the achievement requirements.

## ✨ Achievements Targeted
*   🦈 **Pull Shark:** Opened a pull request that has been merged. (Farms up to the Gold tier: 1024 PRs).
*   🚀 **YOLO:** Merged a pull request without a code review.
*   🤠 **Quickdraw:** Closed/merged an issue or pull request within 5 minutes of opening.

## ⚙️ How It Works
When triggered (either manually or via a cron schedule), the workflow will:
1. Check out the repository.
2. Create a unique branch based on the current timestamp.
3. Append a timestamp log to `badge-farm-log.txt` and commit the change.
4. Open a Pull Request from the new branch to `main`.
5. Instantly squash-merge the PR (satisfying YOLO and Quickdraw conditions).
6. Delete the temporary branch to keep the repository clean.

## 🚀 Setup Instructions

**Step 1: Enable GitHub Actions Permissions**
By default, GitHub Actions cannot create or merge PRs. You must grant it permission:
1. Go to your repository's **Settings**.
2. Navigate to **Actions** > **General** on the left sidebar.
3. Scroll down to **Workflow permissions**.
4. Select **Read and write permissions**.
5. Check the box for **Allow GitHub Actions to create and approve pull requests**.
6. Click **Save**.

**Step 2: Add the Workflow**
1. Create a directory structure `.github/workflows/` in your repository.
2. Add the `badge-farm.yml` file generated for this tool.
3. Update the `user.name` and `user.email` in the YAML file to match your GitHub account details.

## 🕹️ Usage
*   **Manual Run:** Go to the **Actions** tab, select the workflow, click **Run workflow**, and input the number of PR loops you want to execute (if configured).
*   **Automated Run:** Uncomment the `schedule` (cron) section in the YAML file to let it run daily in the background.

## ⚠️ Disclaimer & Anti-Spam Warning
GitHub has rate limits and abuse detection mechanisms. **Do not** spam hundreds of PRs in a matter of minutes manually. It is highly recommended to run this action at a reasonable pace (e.g., a few times a day or via the daily cron job) to keep your account safe and ensure your achievements are recorded properly.

---
*Inspired by the quest for the Gold Pull Shark badge!*