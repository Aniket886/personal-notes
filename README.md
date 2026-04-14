# GitHub Streak Maintainer for @Aniket886

Automated daily commits to maintain your GitHub contribution streak.

## Features
- **10-50 random commits per day** - Ensures consistent activity
- **Runs daily at midnight UTC** - Automated via GitHub Actions
- **Manual trigger available** - Use `workflow_dispatch` for testing

## Setup Instructions

### 1. Fork this repository to your account
Click the Fork button on GitHub to create your own copy.

### 2. Enable GitHub Actions
- Go to your fork's **Settings** → **Actions** → **General**
- Ensure "Allow all actions" is selected

### 3. Add Repository Secret
- Go to **Settings** → **Secrets and variables** → **Actions**
- Click **New repository secret**
- Name: `GITHUB_USER_EMAIL`
- Value: Your GitHub email address

### 4. Enable Workflow
- Go to **Actions** tab
- Click on the workflow
- Click **Enable workflow**

## Configuration

| Setting | Value |
|---------|-------|
| Min commits | 10 |
| Max commits | 50 |
| Schedule | Daily at 00:00 UTC |
| Branch | main |

## Manual Trigger
You can manually run the workflow from the Actions tab using "Run workflow" button.
