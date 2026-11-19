# 📦 BPM Registry

Official package registry and web catalog for the **ByteC Package Manager (`bpm`)**.

🌐 **Web Catalog & Live Search:** [github.io](https://bytecompilier.github.io/BPM-registry)

---

## 🛡️ Official Core Libraries

<!-- OFFICIAL_START -->
| Package | Version | Author | Description |
| :--- | :--- | :--- | :--- |
| `std` | `1.0.7` | 🛡️ Official | Test bytec library for BPM! |
<!-- OFFICIAL_END -->

## 🌍 Community Packages

<!-- COMMUNITY_START -->
_No community packages published yet. Be the first to open a PR!_
<!-- COMMUNITY_END -->

---

## 🚀 Quick Usage (`bpm`)

```cmd
:: Install packages from this registry
bpm install add std

:: List all installed packages and versions
bpm list

:: Update all installed packages to latest versions
bpm update

:: Remove packages
bpm remove add std -y
```

---

## 🤝 How to Publish Your Package

Anyone can publish a **ByteC** library to the official registry via a **Pull Request**:

1. **Fork** this repository.
2. Create a new file in the root directory named after your package (only letters, numbers, `-`, and `_`, **no file extension**, e.g. `json-parser`).
3. Add the required metadata in `key=value` format:
   ```ini
   url=https://github.com
   version=1.0.0
   author=your-username
   description=Short description of what your ByteC library does
   ```
4. Open a **Pull Request** to `main`. Our automated security bot will validate your metadata and archive, and once approved by a maintainer, your package will automatically appear in this catalog and on the web portal!

### ⚠️ Security & Validation Rules
* **Immutable Releases Only:** `url` must point to a GitHub Tag (`/refs/tags/...`) or Release archive (`/releases/download/...`). Mutable branch URLs like `/refs/heads/main.zip` are rejected.
* **Author Verification:** `author` must match your GitHub username, and `url` must belong to your GitHub repository.
* **Allowed File Types:** Archives may only contain `.bytec` source files and documentation (`.md`, `.txt`, `LICENSE`). Executables and scripts are strictly blocked.
* **Archive Structure:** Standard GitHub ZIP structure (all files inside a single top-level directory, max 50 MB).
