# BPM Registry

Official package registry for the **ByteC Package Manager (BPM)**.

---

## How to Publish Your Package

Anyone can submit a library to the BPM registry via a **Pull Request**. Follow the steps below to publish your package.

### 1. Prepare Your Library Repository
1. Host your library in a **public** GitHub repository.
2. Make sure your code is placed at the **root** of the repository (BPM unpacks archives using `--strip-components=1`, which extracts the top-level repository folder directly into `libs/<package_name>`).
3. Get a direct `.zip` archive link for your repository or release:
   - **Branch archive:** `https://github.com<username>/<repo>/archive/refs/heads/main.zip`
   - **Release tag archive (recommended):** `https://github.com<username>/<repo>/archive/refs/tags/v1.0.0.zip`

### 2. Add Your Package to the Registry
1. **Fork** this repository (`bytecompilier/BPM-registry`).
2. Create a new file in the root directory of your fork.
   - **File name rules:** The file name is your **package name**.
   - **No file extension** (do **not** add `.txt`, `.json`, etc.).
   - Allowed characters: letters (`a-z`, `A-Z`), numbers (`0-9`), hyphens (`-`), and underscores (`_`).
   - Forbidden characters: `.` `/` `\` `&` `|` `;` `"` `%` `<` `>` `(` `)` `^` `!`
3. Paste the direct `.zip` URL into the **first line** of the file (plain text, no extra spaces or markdown formatting):
   ```text
   https://github.comusername/my-library/archive/refs/tags/v1.0.0.zip
   ```

### 3. Test & Submit
1. Test your package locally before submitting:
   ```cmd
   bpm install <your-package-name>
   ```
2. Open a **Pull Request** to the `main` branch of `bytecompilier/BPM-registry`.
3. Once reviewed and merged, your package will be immediately available to all BPM users!

---

## Usage

Install a package:
```cmd
bpm install <package-name>
```

Remove an installed package:
```cmd
bpm remove <package-name>
```

Remove without confirmation prompt:
```cmd
bpm remove <package-name> -y
```
