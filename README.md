# SkillSauce Secure Sandbox — releases

Installers for the SkillSauce Secure Sandbox desktop app.

**[Download the latest release](../../releases/latest)**

| Platform | File |
|---|---|
| Ubuntu / Debian | `skillsauce-secure-sandbox_<version>_amd64.deb` |
| Any Linux | `SkillSauce-Secure-Sandbox-<version>.AppImage` |

### Install the .deb
```bash
sudo dpkg -i skillsauce-secure-sandbox_<version>_amd64.deb
skillsauce-secure-sandbox
```

### Or the AppImage
```bash
chmod +x SkillSauce-Secure-Sandbox-<version>.AppImage
./SkillSauce-Secure-Sandbox-<version>.AppImage
```

Optionally add it to your applications menu and register invitation links:
```bash
./install-appimage.sh SkillSauce-Secure-Sandbox-<version>.AppImage
```

---

This repository holds **release artifacts only** — there is no source code here.
The app is developed in a private repository; this one is public so that the
installers can be downloaded without a GitHub account.

`latest-linux.yml` is the auto-update manifest. Do not delete it from a release.

> **Not yet code-signed.** Windows will show a SmartScreen warning and macOS
> will refuse to open the app. Internal testing only until signing certificates
> are in place.
