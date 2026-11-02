# 🤖 One-Click GitHub Commit Bot

A beginner-friendly GitHub Actions workflow that lets you make an automatic
commit to your repository with a single button click — no terminal needed.

## 📁 Project Structure

```
your-repo/
├── .github/
│   └── workflows/
│       └── commit-bot.yml   ← the workflow file (the bot's brain)
├── bot-log.txt              ← the file the bot edits on every run
└── README.md
```

## 🚀 How to Use

1. Push this project to a GitHub repository.
2. Go to your repo on GitHub → click **Actions** tab.
3. Select **"🤖 One-Click Commit Bot"** from the left sidebar.
4. Click **"Run workflow"** → optionally type a custom message → click the green button.
5. Watch the bot run, then check your commit history!

## ⚙️ How It Works

| Step | What happens |
|------|-------------|
| 1 | GitHub checks out your repo code |
| 2 | The bot appends a timestamp line to `bot-log.txt` |
| 3 | Git is configured with a bot identity |
| 4 | The change is committed and pushed back to the repo |

## 🔒 Permissions

The workflow uses `permissions: contents: write` to allow GitHub Actions to
push commits. No personal tokens or secrets are needed — GitHub handles it
automatically via the built-in `GITHUB_TOKEN`.

