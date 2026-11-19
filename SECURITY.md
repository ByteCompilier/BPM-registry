# 🛡️ Security Policy

## Registry Security Architecture

The **BPM Registry** enforces automated and manual security controls to keep the **ByteC** ecosystem safe:

* **Immutable Releases Only:** Packages must point to frozen GitHub Tags (`/refs/tags/...`) or Releases (`/releases/download/...`). Mutable branch archives are automatically rejected.
* **Strict File Allowlist:** Archives may only contain `.bytec` source files and plain-text documentation (`.md`, `.txt`, `LICENSE`). All executables and scripts are blocked.
* **Continuous Security Patrol:** An automated audit scans all registered packages every 30 minutes for broken links, archive tampering, or unauthorized modifications.
* **Manual Maintainer Review:** Every new package submission requires explicit approval from a repository maintainer before merging.

---

## Reporting a Vulnerability or Malicious Package

If you discover a malicious package, suspicious code, a compromised repository link, or a vulnerability in `bpm` or this registry, **please do not disclose it publicly in a regular Issue first**.

### How to Report
1. **GitHub Private Vulnerability Reporting (Preferred):**
   * Go to the **[Security](../../security/advisories/new)** tab of this repository and click **Report a vulnerability**.
2. **Urgent Package Takedown:**
   * If a package contains broken links or non-critical bugs, you may open an issue using the **[Report a Broken or Malicious Package](../../issues/new/choose)** template.

### Response Timeline
* **Initial Acknowledgment:** Within **24–48 hours**.
* **Malicious Package Removal:** Confirmed malicious or compromised packages are removed from the registry immediately upon verification.
