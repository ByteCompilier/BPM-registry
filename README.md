# BPM-registry 📦

Official community package registry for **ByteC** and **BPM (ByteC Package Manager)**.

## 🚀 Installing Packages

Use the `bpm` CLI tool in your project directory:

```cmd
bpm install <package-name>
```

You can also install or remove multiple packages at once:
```cmd
bpm install pkg1 pkg2
bpm remove pkg1 pkg2 -y
```

## 📤 How to Publish Your Package

1. **Create a public repository** on GitHub containing your `.bytec` library files in the root folder.
2. **Fork this repository** (`BPM-registry`).
3. **Create a new file** in the root directory named `<package-name>` (no file extension; allowed characters: `a-z`, `A-Z`, `0-9`, `-`, `_`).
4. **Add the package metadata** using the exact `key=value` format below:

```ini
url=https://github.com<your-username>/<your-repo>/archive/refs/heads/main.zip
version=1.0.0
author=<your-github-username>
description=Short description of what your ByteC library does
```

### Example (`add`)
```ini
url=https://github.combytecompilier/add/archive/refs/heads/main.zip
version=1.0.0
author=bytecompilier
description=Basic addition helpers for ByteC
```

5. **Open a Pull Request** to the `main` branch. Our automated GitHub Actions bot will verify your metadata, check archive structure, and scan for safety before manual review.

## ⚠️ Package Rules
- Package names must match `^[a-zA-Z0-9_-]+$` (no `.txt` or `.bytec` extensions).
- All 4 metadata keys (`url`, `version`, `author`, `description`) are required and must be non-empty.
- `url` must use `https://` and point to a valid `.zip` archive under 50 MB.
- Archives must contain source code only — executable binaries and scripts (`.exe`, `.dll`, `.bat`, `.ps1`, `.vbs`) are strictly prohibited.

---
## Available Packages

<!-- PACKAGES_START -->
| Package | Version | Author | Description |
| :--- | :--- | :--- | :--- |
| `add` | `1.0.0` | [@ByteCompilier](https://github.comByteCompilier) |  |
| `std` | `1.0.0` | [@ByteCompilier](https://github.comByteCompilier) |  |
<!-- PACKAGES_END -->
---
## 🛡️ Official Core Libraries

<!-- OFFICIAL_START -->
<!-- OFFICIAL_END -->

## 🌍 Community Packages

<!-- COMMUNITY_START -->
<!-- COMMUNITY_END -->

