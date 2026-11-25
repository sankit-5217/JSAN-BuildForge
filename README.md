# JSAN BuildForge

Shared project for Ankit and Anshul.

## Developer workspaces

Each developer uses a separate clone on their own PC. Install Git and Visual Studio Code first. The workspace files use relative paths so they work in any clone location.

### Ankit's PC

Run in a terminal from the folder where you keep projects:

```sh
git clone --branch ankit https://github.com/sankit-5217/JSAN-BuildForge.git
cd JSAN-BuildForge
code ankit.code-workspace
```

### Anshul's PC

Run in a terminal from the folder where you keep projects:

```sh
git clone --branch anshul https://github.com/sankit-5217/JSAN-BuildForge.git
cd JSAN-BuildForge
code anshul.code-workspace
```

If the `code` command is unavailable, open VS Code, choose **File > Open Workspace from File**, and select your workspace file.

Opening a workspace does not switch Git branches. In an existing clone, run `git fetch origin` and `git switch ankit` or `git switch anshul` before opening the corresponding workspace. Confirm your branch with `git branch --show-current`.

## Git identity and access

On each PC, configure the developer's own identity in the clone before committing:

```sh
git config user.name "Your Name"
git config user.email "your-own-github-email@example.com"
```

Use your own GitHub account when authenticating. The repository owner must grant collaborator access to any developer who does not already have write access. Branches and workspace files do not grant that access.

## Daily workflow

- Keep `main` as the shared integration branch.
- Work on your own branch: `ankit` or `anshul`.
- Before starting, run `git pull --ff-only`.
- To bring shared changes into your branch, run `git fetch origin`, then `git merge origin/main`. Resolve any conflicts before continuing.
- Commit your changes and run `git push`.
- Open a pull request from your branch into `main` for review and merge.
- After a pull request is merged, bring `origin/main` into your branch again.

Do not commit passwords, access tokens, or local secrets.

