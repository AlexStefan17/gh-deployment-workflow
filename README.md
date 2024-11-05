# gh-deployment-workflow
 GitHub Pages Deployment from DevOps Roadmap
 Project link: https://roadmap.sh/projects/github-actions-deployment-workflow

# GitHub Pages Deployment with GitHub Actions

This project demonstrates a GitHub Actions workflow to automatically deploy an `index.html` file to GitHub Pages after every push to the `main` branch.

## Project Structure

- **index.html**: A simple HTML file that displays "Hello, GitHub Actions!"

## Getting Started

1. Clone this repository or create a new one.
2. Make sure the repository settings allow GitHub Actions to have **read and write** permissions.

## Workflow Overview

The deployment workflow is defined in `.github/workflows/deploy.yml`. It:
1. Runs automatically on every push to the `main` branch.
2. Manually deploys when triggered from the **Actions** tab.

## How It Works

The workflow:
1. Checks out the latest code from the `main` branch.
2. Uses [peaceiris/actions-gh-pages](https://github.com/peaceiris/actions-gh-pages) to publish files to the `gh-pages` branch, which GitHub Pages serves as the live website.

### GitHub Pages Settings

To view the deployed site, set up GitHub Pages:
1. Go to **Settings** > **Pages**.
2. Set the source branch to **gh-pages**.
3. Your site will be available at `https://<username>.github.io/<repository-name>`.

## Manually Deploying

To manually deploy:
1. Go to the **Actions** tab in your GitHub repository.
2. Select the **Deploy to GitHub Pages** workflow.
3. Click **Run workflow** to trigger deployment.
