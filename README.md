# SkillSauce Secure Sandbox — releases

Secure desktop environment for SkillSauce assessments and interviews.

## ⬇ [Download the latest release](../../releases/latest)

That link always points at the current version — don't bookmark a specific tag.

| Platform | File |
|---|---|
| **Ubuntu / Debian** | `skillsauce-secure-sandbox_<version>_amd64.deb` — recommended |
| **Any Linux** | `SkillSauce-Secure-Sandbox-<version>.AppImage` |
| Windows / macOS | not yet published |

### Install the .deb
```bash
sudo dpkg -i skillsauce-secure-sandbox_<version>_amd64.deb
skillsauce-secure-sandbox
```
Installs the icon, adds it to your applications menu, and registers
`skillsauce-sandbox://` invitation links.

### Or the AppImage
```bash
chmod +x SkillSauce-Secure-Sandbox-<version>.AppImage
./SkillSauce-Secure-Sandbox-<version>.AppImage
```
An AppImage on its own has no menu entry, no icon, and does not handle
invitation links. To get all three:
```bash
chmod +x install-appimage.sh
./install-appimage.sh SkillSauce-Secure-Sandbox-<version>.AppImage
```

> On Ubuntu 22.04 and later the AppImage will not start on its own — those
> releases ship FUSE 3 and AppImages need FUSE 2. `install-appimage.sh` works
> around it without needing sudo. **The `.deb` is unaffected**, which is why it
> is the recommendation.

## Updates

The app checks this page shortly after launch and once a day, downloads in the
background, and installs when you close it — never during a session.
`latest-linux.yml` is what makes that work; it must stay attached to every
release.

## Not code-signed yet

Windows will show a SmartScreen warning and macOS will refuse to open the app
until signing certificates are in place. **Internal testing only** — do not
send these links to candidates.

---

This repository holds **release artifacts only** — there is no source code
here. The app is developed in a private repository; this one is public so the
installers can be downloaded without a GitHub account.
