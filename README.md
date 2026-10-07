# SMod

<p align="center">
  <img src="logo.png" width="120" alt="SMod">
</p>

<p align="center">
  <strong>Spotify, your way.</strong><br>
  A local customization framework for the Spotify desktop client.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-1ed760?style=for-the-badge">
  <img src="https://img.shields.io/badge/platform-macOS-black?style=for-the-badge">
  <img src="https://img.shields.io/badge/version-0.6.3-blue?style=for-the-badge">
</p>

---

## What is SMod?

**SMod** is a lightweight, local Spotify customization framework designed to let you change the way your Spotify desktop client looks and behaves.

Instead of creating a separate Spotify client, SMod works with the existing Spotify desktop application and provides a foundation for **themes, extensions, custom UI and personalization**.

> SMod is currently in early development.

---

## ✨ Features

### 🎨 Customisation

SMod is designed around making Spotify feel more personal.

Current customization features include:

- Custom Spotify fonts
- Upload your own `.woff`, `.woff2`, `.ttf` and `.otf` fonts
- Accent colours
- SMod interface colours
- Animation controls
- Blur controls
- Compact mode
- Custom SMod branding

### 🧩 Extension System

SMod has an extension architecture allowing developers to create their own modifications.

Example:

```text
my-extension/
├── manifest.json
├── index.js
├── style.css
└── assets/
```

Extensions can eventually interact with the SMod API to create custom Spotify experiences without modifying the SMod core itself.

### 🛠️ SMod API

The framework is being built around a simple API:

```js
SMod.version
SMod.ui
SMod.player
SMod.track
SMod.settings
SMod.events
```

The goal is to make SMod extensions easy to build and distribute.

### 💾 Safe & Reversible

SMod creates an untouched backup of Spotify's frontend before modifying it.

You can restore the original Spotify frontend with:

```bash
./bin/smod restore
```

---

## 🚀 Getting Started

### Requirements

- macOS
- Spotify Desktop
- Python 3
- Xcode Command Line Tools

### Install

Clone the repository:

```bash
git clone https://github.com/ABDProjects/SMod.git
cd SMod
```

Make SMod executable:

```bash
chmod +x bin/smod
```

Apply SMod:

```bash
./bin/smod apply
```

Spotify will automatically launch after the modification has been successfully applied.

---

## 🔄 Restore Spotify

Want to temporarily remove SMod?

```bash
./bin/smod restore
```

This restores the original Spotify frontend from the backup created during installation.

To completely remove SMod:

```bash
./bin/smod uninstall
```

---

## 🧩 Extensions

List installed extensions:

```bash
./bin/smod extension list
```

Install an extension:

```bash
./bin/smod extension install ./extensions/my-extension
```

Enable an extension:

```bash
./bin/smod extension enable my-extension
```

Disable one:

```bash
./bin/smod extension disable my-extension
```

---

## 📁 Project Structure

```text
SMod/
├── bin/
│   └── smod
│
├── lib/
│   ├── smod-core.sh
│   └── extensions.sh
│
├── ui/
│   ├── runtime.js
│   ├── settings.js
│   └── welcome.js
│
├── extensions/
│   └── smod-test/
│
├── marketplace/
│   └── repository.json
│
├── logo.png
├── logo2.png
├── VERSION
└── README.md
```

---

## 🗺️ Roadmap

SMod is still being actively developed.

### Core

- [x] Spotify frontend patching
- [x] Automatic backup
- [x] Restore functionality
- [x] Automatic Spotify launch
- [x] In-client welcome screen
- [x] Extension framework
- [x] Basic settings
- [ ] Improved settings integration
- [ ] Automatic updates

### Customisation

- [x] Font selection
- [x] Custom font uploads
- [x] Accent colours
- [x] Performance settings
- [ ] Complete theme engine
- [ ] Theme presets
- [ ] Custom CSS support

### Extensions

- [x] Extension manifests
- [x] Enable/disable extensions
- [ ] Full SMod API
- [ ] Extension permissions
- [ ] Extension settings
- [ ] Developer tools

### Marketplace

- [ ] SMod Marketplace
- [ ] One-command extension installation
- [ ] Theme marketplace
- [ ] Automatic extension updates
- [ ] Extension discovery

---

## ⚠️ Disclaimer

SMod is an independent community project and is **not affiliated with, endorsed by, or sponsored by Spotify**.

SMod is intended for local customization and development.

SMod does not aim to bypass:

- Spotify authentication
- Premium subscriptions
- DRM
- Payment systems
- Account security

Always keep a backup of your Spotify installation and understand that Spotify updates may overwrite modifications.

---

## 🤝 Contributing

SMod is currently in early development, but contributions, ideas and extensions will eventually be welcome.

If you're interested in building something for SMod, keep an eye on the repository as the extension API develops.

---

## 💚 SMod

**Spotify, your way.**

Built independently by **ABDProjects**.

[GitHub](https://github.com/ABDProjects/SMod) · [Discord](https://discord.gg/vwH9mvw36k)
