# AssetSkins-Mod-Storage 🌌

Welcome to the **AssetSkins Mod Storage** repository. This is a centralized, high-performance vault for managing, syncing, and deploying custom skins, mods, and assets.

---

## 🚀 Overview

This repository is designed to store, manage, and catalog custom-authored assets and skins. Due to the large size of binary files (such as `.zip` mod archive files, maps, and sound packs), it utilizes an integrated automated sync system using **GitHub Releases** to bypass traditional Git file size limitations while keeping the main repository tree lightweight, clean, and fast.

- **Primary Storage**: Lightweight assets, screenshots, configuration files, and metadata are tracked directly via git.
- **Release Assets**: Large model binaries, `.zip` mods, maps, and heavy sound packages (> 50MB) are pushed to GitHub Releases.

---

## 📂 Repository Structure

The contents are structured by champion classes, maps, and sound customizations:

```
AssetSkins-Mod-Storage/
├── assetskin.com/              # Main repository directory
│   ├── Aatrox Full/            # Champion assets
│   ├── Ahri Full/              
│   ├── ...                     # Other champions
│   ├── LoadingScreen/          # Custom loading screens
│   ├── Mod Maps LoL Full/      # Custom map modifications
│   ├── Mod Mau Mat/            # Ward skin models
│   └── Mod Sound/              # Custom voiceovers & sound replacement packs
├── .gitignore                  # Git exclusion rules
└── README.md                   # This documentation
```

---

## 🛠️ Sync & Release Workflow (`upload_to_github.py`)

To push new updates and large assets to this vault, use the automated synchronization script:

1. **Auto Detect Size**: Inspects the entire tree for files exceeding the size limit (default: **50MB**).
2. **Asset Isolation**: Automatically moves files above the limit to a local staging directory (`__large_files__`).
3. **Commit & Push**: Commits and pushes the standard git assets (like README, metadata, and folders) first.
4. **GitHub Releases Upload**: Creates a tag for each large file and uploads the raw asset directly to GitHub Releases.
5. **No Local Deletions**: Retains local backups of large files for safety.

---

## 💎 Features

- ⚡ **Zero-bloat git tree**: Keeps the git history clean without bloating the `.git` folder.
- 📦 **Unlimited size**: Stores large mods via Releases without using Git LFS or hitting GitHub's 100MB file push limit.
- 🎨 **Visual Previews**: Organized hierarchy to support image previews and metadata along side the ZIP packages.

---

*Snap finger - Boom, Comeback to beginning.* ✨
