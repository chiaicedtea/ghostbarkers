# Setting up the second computer

One-time setup so you can work on Ghostbarkers from either computer.

- GitHub project: https://github.com/chiaicedtea/ghostbarkers
- Live game: https://chiaicedtea.github.io/ghostbarkers/

## Easiest: let Claude Code do it
Open Claude Code on the other computer and say:

> Set up my GitHub project chiaicedtea/ghostbarkers in C:\LaLaCorgi\Games. Install Git and GitHub CLI with winget if they're missing, help me sign in, then download the project.

## Or do it by hand (PowerShell)
1. Install the tools (approve the Windows prompts):
   ```powershell
   winget install --id Git.Git -e --source winget
   winget install --id GitHub.cli -e --source winget
   ```
2. **Close and reopen PowerShell**, then sign in. Answer **Y**, press **Enter** when it says "Press Enter…", paste the code in the browser, approve, and wait for "Logged in as chiaicedtea":
   ```powershell
   gh auth login --hostname github.com --git-protocol https --web
   ```
3. Connect Git to your account and set your name:
   ```powershell
   gh auth setup-git
   git config --global user.name "chiaicedtea"
   git config --global user.email "24421696+chiaicedtea@users.noreply.github.com"
   ```
4. Download the project:
   ```powershell
   gh repo clone chiaicedtea/ghostbarkers C:\LaLaCorgi\Games
   ```
5. In Claude Code, open the folder `C:\LaLaCorgi\Games`.

## Every time you switch computers
- **Starting work:** tell Claude "get the latest from GitHub" (`git pull`).
- **Done working:** tell Claude "save my changes to GitHub" (commit + push).
- The live game updates about a minute after each save.
