# Aina Payroll Filler: update channel

This private repository is only the update channel for **Aina Payroll Filler**, a Windows program. It holds
no source code.

Every release (tag `buildNNNN`) carries exactly three files:

| File | What it is |
|---|---|
| `AinaPayrollFiller.exe` | the program |
| `manifest.json` | build number, release notes, size and SHA-256 of the exe |
| `manifest.json.sig` | the ECDSA P-256 signature of `manifest.json` |

The installed program reads the **latest** release, accepts it only if the signature matches the key built
into it, the build is newer, and the exe's size and SHA-256 match. Then it swaps itself and restarts.
Settings and the holiday list on the PC are kept.

Reading this private repository needs a fine-grained token limited to this repository with
**Contents: read-only**. That token goes into `update.json` next to the program on the PC; it never goes in a
release. Don't upload anything else here: every release asset is downloadable by anyone with a token.
