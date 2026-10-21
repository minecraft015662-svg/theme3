# Sarthak34 (GitHub-only version)

No server needed. Website = GitHub Pages. Theme files = this repo. The VPS only runs the installer.

Repo layout:
    index.html            license generator website (GitHub Pages)
    install.sh            installer / `sarthak34` command
    pubkey.pem            you add this after Step 1 of the website
    packages/             theme + extensions

Setup:
1. Create a PUBLIC repo named `sarthak34` and upload everything in this folder.
2. Edit `install.sh` on GitHub: change `REPO="USERNAME/sarthak34"` to your username.
3. Repo Settings > Pages > Branch `main`, folder `/ (root)` > Save. Site: https://USERNAME.github.io/sarthak34/
4. Open the site > Step 1 > Generate keys. Save the private key safely. Create `pubkey.pem` in the repo with the public key.
5. Step 2 creates license keys (email + panel domain + days).
6. On the panel server:  curl -sSL https://raw.githubusercontent.com/USERNAME/sarthak34/main/install.sh | sudo bash

Commands after install: sarthak34 status | update | uninstall | ext list | ext install <name> | ext remove <name>
Add an extension: packages/extensions/<name>/ (ext.css and/or ext.js) + add it to packages/index.json.

Limits: licenses cannot be revoked, and the theme files are readable by anyone who finds the repo.
