# 🤝 Contributing to BPM Registry

Thank you for wanting to publish a library for **ByteC**! Follow this step-by-step guide to add your package to the official registry without triggering automated security blocks.

---

## 📋 Step 1: Prepare Your Library Repository

Before submitting a package to `BPM-registry`, make sure your library repository on GitHub meets these requirements:

1. **Public Repository:** Your repository must be public and owned by your GitHub account.
2. **Clean File Structure:** Put your `.bytec` source files and documentation inside the repository.
   * **Allowed files only:** `.bytec`, `.md`, `.txt`, and `LICENSE`.
   * **Forbidden files:** `.exe`, `.dll`, `.bat`, `.ps1`, `.sh`, or any compiled binaries.
3. **Create an Immutable Tag or Release:**
   * Go to your library repository → **Releases → Create a new release**.
   * Create a version tag (e.g., `v1.0.0`) and publish the release.
   * Your archive link will look like: `https://github.com<your-username>/<your-repo>/archive/refs/tags/v1.0.0.zip`.

---

## 📝 Step 2: Create Your Package Metadata File

1. **Fork** the `BPM-registry` repository (or use the **[+ Publish Package](https://github.io)** generator on our web portal).
2. Create a new file in the **root directory** named after your package.
   * **Naming rules:** Only letters (`a-z`, `A-Z`), digits (`0-9`), `-`, and `_`. **Do not add any file extension** (e.g., `json-parser`, not `json-parser.txt`).
3. Add the four required fields in `key=value` format:

```ini
url=https://github.comyour-username/your-repo/archive/refs/tags/v1.0.0.zip
version=1.0.0
author=your-username
description=Short and clear description of what your ByteC library does
```

---

## 🚀 Step 3: Open a Pull Request

1. Submit a **Pull Request** to the `main` branch of `BPM-registry`.
2. Wait ~20 seconds for the automated **`check-package`** bot to verify your metadata, download the archive, and inspect its contents.
3. Once the check turns green (✅) and a maintainer approves your PR, your package will automatically appear in `README.md` and on the **[Web Catalog](https://github.io)**.

---

## ❌ Common Rejection Reasons

* **Using `/refs/heads/main.zip`:** Mutable branch URLs are blocked for security. Always use `/refs/tags/...` or `/releases/download/...`.
* **Author mismatch:** The `author=` field must match your GitHub username and the repository owner in `url=`.
* **Extra files in archive:** Remove any `.exe`, `.c`, or script files from your release archive before submitting.
* **Modifying existing packages:** You cannot overwrite or delete packages published by other authors.
