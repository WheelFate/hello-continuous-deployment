# Hello, Continuous Deployment! 👋

This is a simple project designed to demonstrate the concept of **Continuous Deployment (CD)** for beginners using GitHub Actions and GitHub Pages.

## ✨ Live Demo

**[Click here to see the live website!](https://wheelfate.github.io/hello-continuous-deployment/)**

This website is automatically updated every time a new change is merged into the `main` branch.

## 🤔 How Does It Work?

We use a simple pipeline: **Code Change -> Automatic Deployment**.

1.  **A Developer Makes a Change:** A developer makes a change to the `index.html` file on a new branch and opens a Pull Request.
2.  **Code is Merged:** After a review, the Pull Request is merged into the `main` branch.
3.  **GitHub Actions Triggers:** This merge event automatically triggers a workflow defined in the `.github/workflows/deploy.yml` file.
4.  **The Workflow Runs:**
    *   It checks out the latest code.
    *   It does a tiny "build" step: it replaces the `VERSION_TIMESTAMP` text in `index.html` with the current date and time. This helps us see the new version is live.
    *   It uploads the modified website files as an "artifact."
    *   It deploys this artifact to GitHub Pages.
5.  **Website is Live!** Your changes are now visible on the public GitHub Pages URL for this repository, usually within a minute.

This is **Continuous Deployment**: a change that passes our process is automatically released to users without any manual intervention.

## 🚀 How to Try It Yourself

1.  **Fork this repository** to your own GitHub account.
2.  In your forked repository, go to **Settings > Pages**.
3.  Under "Build and deployment", select **GitHub Actions** as the source.
4.  Now, **make a change to the `index.html` file** (e.g., change the text in the `<h1>` tag).
5.  **Commit the change to a new branch** and open a pull request to merge it into your `main` branch.
6.  **Merge the pull request.**
7.  Go to the **"Actions"** tab in your repository. You will see the workflow running!
8.  Once it's complete (with a green checkmark ✅), go back to your **Settings > Pages** to find your public URL and see your changes live!
