# 🏆 Auto GitHub Achievements & Comprehensive Badge Guide

Welcome to the ultimate repository for GitHub Achievements! This project serves two purposes:
1. 🤖 **An Automated Tool (GitHub Action)** to effortlessly farm specific badges (Pull Shark, YOLO, Quickdraw).
2. 📚 **A Comprehensive Guide** explaining every GitHub badge available, how to earn them, and what they mean.

---

## 🤖 PART 1: The Automation Tool (Badge Farm)

An automated GitHub Actions workflow designed to help you farm specific GitHub profile badges without manual effort. By utilizing GitHub Actions and the GitHub CLI (`gh`), this workflow automatically creates dummy branches, commits, opens Pull Requests, and immediately merges them.

### ✨ Targeted Achievements
*   🦈 **Pull Shark:** Opened a pull request that has been merged. (Farms up to the Gold tier: 1024 PRs).
*   🚀 **YOLO:** Merged a pull request without a code review.
*   🤠 **Quickdraw:** Closed/merged an issue or pull request within 5 minutes of opening.

### ⚙️ How It Works
When triggered (either manually or via a cron schedule), the workflow will:
1. Check out the repository and pull the latest code to prevent conflicts.
2. Create a unique branch based on the current timestamp.
3. Overwrite the `badge-farm-log.txt` file with a new timestamp and commit the change.
4. Open a Pull Request from the new branch to `main`.
5. Instantly squash-merge the PR using its specific URL.
6. Delete the temporary branch to keep the repository clean.

### 🚀 Setup Instructions
**Step 1: Enable GitHub Actions Permissions**
1. Go to your repository's **Settings** > **Actions** > **General**.
2. Scroll down to **Workflow permissions**.
3. Select **Read and write permissions**.
4. Check the box for **Allow GitHub Actions to create and approve pull requests**.
5. Click **Save**.

**Step 2: Add the Workflow**
1. Create a directory structure `.github/workflows/` in your repository.
2. Add the `badge-farm.yml` file generated for this tool.
3. Update the `user.name` and `user.email` in the YAML file to match your GitHub account details.

### 🕹️ Usage
*   **Manual Run:** Go to the **Actions** tab, select the workflow, click **Run workflow**, and input the number of PR loops you want to execute (1, 5, 10, 20, or 50 PRs per run).
*   **Automated Run:** The workflow runs automatically daily at 00:00 UTC (approximately 7:00 AM Vietnam time). You can modify the cron schedule in the YAML file if needed.

### 📊 Execution Details
**Schedule (Automatic):**
- **1 PR per day** at 00:00 UTC
- Time per PR: ~22-37 seconds (including delays to avoid rate limit)

**Manual Run:**
- Choose from 1, 5, 10, 20, or 50 PRs per run
- Each PR takes ~22-37 seconds
- 50 PRs run takes approximately 15-25 minutes

### ⏱️ Time Estimates for Pull Shark Tiers
Based on your running frequency:
| Tier | Required PRs | 1 PR/day | 5 PR/day | 10 PR/day | 20 PR/day |
|------|--------------|----------|----------|-----------|------------|
| Default | 2 | 2 days | <1 day | <1 day | <1 day |
| Bronze | 16 | 16 days | 3-4 days | 2 days | 1 day |
| Silver | 128 | ~4 months | ~26 days | ~13 days | ~6 days |
| Gold | 1024 | ~2.8 years | ~7 months | ~3.5 months | ~2 months |

> **⚠️ Anti-Spam Warning:** GitHub has rate limits and abuse detection mechanisms. Do not spam hundreds of PRs in a matter of minutes manually. Run this action at a reasonable pace.

---

## 📚 PART 2: GitHub Achievements & Badges Guide

GitHub offers a variety of badges to celebrate your contributions, engagement, and community-building efforts. These badges can be displayed on your GitHub profile and are available based on different activities.

### 🏅 Displaying Achievements
You can opt to **show or hide** these achievements on your GitHub profile. By default, they are visible to anyone who visits your public profile. If you prefer not to display them, you can modify this setting in your [GitHub Profile Settings](https://github.com/settings).

### 📃 Achievement List
Below is a list of some of the key **GitHub Badges** you can earn and how to get them:

| Badge | Name | How to get |
| :---: | --- | --- |
| ![Achievement badge Heart On Your Sleeve](https://github.githubassets.com/images/modules/profile/achievements/heart-on-your-sleeve-default.png) | **Heart On Your Sleeve** | React to something on GitHub with a ❤️ emoji **(Being tested - now unable to earn)** |
| ![Achievement badge Open Sourcerer](https://github.githubassets.com/images/modules/profile/achievements/open-sourcerer-default.png) | **Open Sourcerer** | User had PRs merged in multiple public repositories **(Being tested - now unable to earn)** |
| ![Achievement badge Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-default.png) | **Starstruck** | Created a repository that has **16 stars** or [more](#badge-tiers).                                                                                              |
| ![Achievement badge Quickdraw](https://github.githubassets.com/images/modules/profile/achievements/quickdraw-default.png) | **Quickdraw** | Closed an issue or a pull request within 5 min of opening.                                                                                                       |
| ![Achievement badge Pair Extraordinaire](https://github.githubassets.com/images/modules/profile/achievements/pair-extraordinaire-default.png) | **Pair Extraordinaire** | Coauthored in **one** or [more](#badge-tiers) merged pull requests.                                                                                             |
| ![Achievement badge Pull Shark](https://github.githubassets.com/images/modules/profile/achievements/pull-shark-default.png) | **Pull Shark** | **2 pull requests** merged (or [more](#badge-tiers)).                                                                                                            |
| ![Achievement badge Galaxy Brain](https://github.githubassets.com/images/modules/profile/achievements/galaxy-brain-default.png) | **Galaxy Brain** | 2 accepted answers or [more](#badge-tiers). <br> *Now unable to earn via [Community discussions](https://github.com/orgs/community/discussions/), for more information see [here](https://github.com/orgs/community/discussions/106536).*                                                                                                                       |
| ![Achievement badge YOLO](https://github.githubassets.com/images/modules/profile/achievements/yolo-default.png) | **YOLO** | Merged **at least one** pull request without code review.                                                                                                       |
| ![Achievement badge Public Sponsor](https://github.githubassets.com/images/modules/profile/achievements/public-sponsor-default.png) | **Public Sponsor** | Sponsoring open source work via [GitHub Sponsors](https://github.com/sponsors).                                                                                  |
| ![Achievement badge Mars 2020 Contributor](https://github.githubassets.com/images/modules/profile/achievements/mars-2020-contributor-default.png) | **Mars 2020 Contributor** | Contributed code to repositories used in the [Mars 2020 Helicopter Mission](https://github.com/readme/featured/nasa-ingenuity-helicopter). *Now unable to earn.* |
| ![Achievement badge 2020 GitHub Archive Program](https://github.githubassets.com/images/modules/profile/achievements/arctic-code-vault-contributor-default.png) | **Arctic Code Vault Contributor** | Contributed code to a repository in the [2020 GitHub Archive Program](https://archiveprogram.github.com/). *Now unable to earn.*                                 |

<br>

## Badge Tiers

Some Achievements not only have the base version, but also tiers.

| Achievement | Default | Bronze | Silver | Gold |
| --- | :---: | :---: | :---: | :---: |
| **Starstruck** | ![Achievement badge Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-default.png) | ![Bronze badge Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-bronze.png) | ![Silver badge Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-silver.png) | ![Gold badge Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-gold.png) |
| | 16 stars | 128 stars | 512 stars | 4096 stars |
| **Pair Extraordinaire** | ![Achievement badge Pair Extraordinaire][pe-default] | ![Bronze badge Pair Extraordinaire][pe-bronze] | ![Silver badge Pair Extraordinaire][pe-silver] | ![Gold badge Pair Extraordinaire][pe-gold] |
| | 1 pull request | 10 pull requests | 24 pull requests  | 48 pull requests |
| **Pull Shark** | ![Achievement badge Pull Shark][ps-default] | ![Bronze badge Pull Shark][ps-bronze] | ![Silver badge Pull Shark][ps-silver] | ![Gold badge Pull Shark][ps-gold] |
| | 2 pull requests | 16 pull requests | 128 pull requests | 1024 pull requests |
| **Galaxy Brain** | ![Achievement badge Galaxy Brain][gb-default] | ![Bronze badge Galaxy Brain][gb-bronze] | ![Silver badge Galaxy Brain][gb-silver] | ![Gold badge Galaxy Brain][gb-gold] |
| | 2 answers | 8 answers | 16 answers | 32 answers |
| **Heart On Your Sleeve** | ![Achievement badge Heart On Your Sleeve](https://github.githubassets.com/images/modules/profile/achievements/heart-on-your-sleeve-default.png) | ![Bronze badge Heart On Your Sleeve](https://github.githubassets.com/images/modules/profile/achievements/heart-on-your-sleeve-bronze.png) | ![Silver badge Heart On Your Sleeve](https://github.githubassets.com/images/modules/profile/achievements/heart-on-your-sleeve-silver.png) | ![Gold badge Heart On Your Sleeve](https://github.githubassets.com/images/modules/profile/achievements/heart-on-your-sleeve-gold.png) |
| | ??? | ??? | ??? | ??? |
| **Open Sourcerer** | ![Achievement badge Open Sourcerer](https://github.githubassets.com/images/modules/profile/achievements/open-sourcerer-default.png) | ![Bronze badge Open Sourcerer](https://github.githubassets.com/images/modules/profile/achievements/open-sourcerer-bronze.png) | ![Silver badge Open Sourcerer](https://github.githubassets.com/images/modules/profile/achievements/open-sourcerer-silver.png) | ![Gold badge Open Sourcerer](https://github.githubassets.com/images/modules/profile/achievements/open-sourcerer-gold.png) |
| | ??? | ??? | ??? | ??? |


[ss-bronze]: https://github.githubassets.com/images/modules/profile/achievements/starstruck-bronze.png
[ss-silver]: https://github.githubassets.com/images/modules/profile/achievements/starstruck-silver.png
[ss-gold]: https://github.githubassets.com/images/modules/profile/achievements/starstruck-gold.png

[pe-default]: https://github.githubassets.com/images/modules/profile/achievements/pair-extraordinaire-default.png
[pe-bronze]: https://github.githubassets.com/images/modules/profile/achievements/pair-extraordinaire-bronze.png
[pe-silver]: https://github.githubassets.com/images/modules/profile/achievements/pair-extraordinaire-silver.png
[pe-gold]: https://github.githubassets.com/images/modules/profile/achievements/pair-extraordinaire-gold.png

[ps-default]: https://github.githubassets.com/images/modules/profile/achievements/pull-shark-default.png
[ps-bronze]: https://github.githubassets.com/images/modules/profile/achievements/pull-shark-bronze.png
[ps-silver]: https://github.githubassets.com/images/modules/profile/achievements/pull-shark-silver.png
[ps-gold]: https://github.githubassets.com/images/modules/profile/achievements/pull-shark-gold.png

[gb-default]: https://github.githubassets.com/images/modules/profile/achievements/galaxy-brain-default.png
[gb-bronze]: https://github.githubassets.com/images/modules/profile/achievements/galaxy-brain-bronze.png
[gb-silver]: https://github.githubassets.com/images/modules/profile/achievements/galaxy-brain-silver.png
[gb-gold]: https://github.githubassets.com/images/modules/profile/achievements/galaxy-brain-gold.png

<br>

## Achievement Skin Tone

The appearance of some achievements depends on your Emoji Skin Tone Preference.

You can change your preferred Skin Tone by going to [appearance settings](https://github.com/settings/appearance).

<br>

| **Badge** | 👋 | 👋🏻 | 👋🏼 | 👋🏽 | 👋🏾 | 👋🏿 |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Starstruck** | ![Default skin tone of Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-default.png) | ![Light skin tone of Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-default--light.png) | ![Light-medium skin tone of Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-default--light-medium.png) | ![Medium skin tone of Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-default--medium.png) | ![Medium-dark skin tone of Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-default--medium-dark.png) | ![Dark skin tone of Starstruck](https://github.githubassets.com/images/modules/profile/achievements/starstruck-default--dark.png) |
| **Quickdraw** | ![Default skin tone of Quickdraw][q-default] | ![Light skin tone of Quickdraw][q-light] | ![Light-medium skin tone of Quickdraw][q-light-medium] | ![Medium skin tone of Quickdraw][q-medium] | ![Medium-dark skin tone of Quickdraw][q-medium-dark] | ![Dark skin tone of Quickdraw][q-dark] |

[s-light]: https://github.githubassets.com/images/modules/profile/achievements/starstruck-default--light.png
[s-light-medium]: https://github.githubassets.com/images/modules/profile/achievements/starstruck-default--light-medium.png
[s-medium]: https://github.githubassets.com/images/modules/profile/achievements/starstruck-default--medium.png
[s-medium-dark]: https://github.githubassets.com/images/modules/profile/achievements/starstruck-default--medium-dark.png
[s-dark]: https://github.githubassets.com/images/modules/profile/achievements/starstruck-default--dark.png

[q-default]: https://github.githubassets.com/images/modules/profile/achievements/quickdraw-default.png
[q-light]: https://github.githubassets.com/images/modules/profile/achievements/quickdraw-default--light.png
[q-light-medium]: https://github.githubassets.com/images/modules/profile/achievements/quickdraw-default--light-medium.png
[q-medium]: https://github.githubassets.com/images/modules/profile/achievements/quickdraw-default--medium.png
[q-medium-dark]: https://github.githubassets.com/images/modules/profile/achievements/quickdraw-default--medium-dark.png
[q-dark]: https://github.githubassets.com/images/modules/profile/achievements/quickdraw-default--dark.png

<br>

## Highlights Badges

| Badge | Name | Is it possible to get? | How to achieve |
| --- | --- | --- | --- |
| ![White badge GitHub Pro](https://user-images.githubusercontent.com/65187002/173065531-57dbf8b1-7eb7-4d46-81bf-f2d18c7c9112.svg#gh-dark-mode-only)![Black badge GitHub Pro](https://user-images.githubusercontent.com/65187002/173065669-d1fdb5a7-8895-43cc-8dea-72a511a37e86.svg#gh-light-mode-only) | **Pro** | Yes | Use [GitHub Pro](https://docs.github.com/en/get-started/learning-about-github/githubs-products#github-pro) |
| ![Dark badge Developer Program Member](https://user-images.githubusercontent.com/65187002/173079579-3c393d22-7a13-4e7d-87b8-341fb613d52b.svg#gh-dark-mode-only)![Light badge Developer Program Member](https://user-images.githubusercontent.com/65187002/173079614-33f43a97-1cc2-4228-85e3-ef43836e17c2.svg#gh-light-mode-only) | **Developer Program Member** | Yes | Be a registered member of the [GitHub Developer Program](https://docs.github.com/en/developers/overview/github-developer-program) |
| ![security-bug-bounty-hunter-dark](https://user-images.githubusercontent.com/65187002/173081624-93e3cf1f-50b7-45a4-82b7-1954f66368b9.svg#gh-dark-mode-only)![security-bug-bounty-hunter-light](https://user-images.githubusercontent.com/65187002/173081657-e500d72c-9247-44c2-a3d3-2deff30e1ae7.svg#gh-light-mode-only) | **Security Bug Bounty Hunter** | Yes | Helped out hunting down security vulnerabilities at [GitHub Security](https://bounty.github.com/) |
| ![Light badge GitHub Campus Expert][gce-dark]![Dark badge GitHub Campus Expert][gce-light] | **GitHub Campus Expert** | Yes | Participate in the [GitHub Campus Program](https://education.github.com/experts) (Open [in August 2024](https://education.github.com/campus_experts)) |
| ![Dark badge Security advisory credit][SAC-dark]![Light badge Security advisory credit][SAC-light] | **Security Advisory Credit** | Yes | Have your security advisory submitted to the [GitHub Advisory Database](https://github.com/advisories) accepted |
|  | **GitHub Star** | Yes | Become a [GitHub Star](https://stars.github.com) |
| ![Dark badge Discussion answered](https://user-images.githubusercontent.com/65187002/173078083-15a75f15-b040-4a92-8d70-561a206d9fd9.svg#gh-dark-mode-only)![Light badge Discussion answered](https://user-images.githubusercontent.com/65187002/173078106-28bea542-4620-46ee-837d-defda3e44ca6.svg#gh-light-mode-only) | **Discussion answered** | No | Have  your reply to a discussion marked as the answer |

[gce-dark]: https://user-images.githubusercontent.com/65187002/173082819-b3625c23-bfd6-4492-b828-56ed91c45f52.svg#gh-dark-mode-only
[gce-light]: https://user-images.githubusercontent.com/65187002/173082836-08be81fe-13b7-4acf-9096-e5241d76f237.svg#gh-light-mode-only
[SAC-dark]: https://user-images.githubusercontent.com/65187002/173084051-79a0a626-1c1a-4d60-afdf-50ad001d7b21.svg#gh-dark-mode-only
[SAC-light]: https://user-images.githubusercontent.com/65187002/173084071-5f321da2-b2a9-490b-a524-1b21fa384d7e.svg#gh-light-mode-only

---
*Happy coding, and keep achieving! 🏆*