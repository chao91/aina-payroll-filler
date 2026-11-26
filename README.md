# Aina Payroll Filler: update channel

This repository is only the update channel for **Aina Payroll Filler**, a Windows program. It holds no source code
and no payroll data.

Every release (tag `buildNNNN`) carries exactly three files:

| File | What it is |
|---|---|
| `AinaPayrollFiller.exe` | the program |
| `manifest.json` | build number, release notes, size and SHA-256 of the exe |
| `manifest.json.sig` | the ECDSA P-256 signature of `manifest.json` |

The installed program checks the **latest** release when it starts. It accepts it only if the signature matches
the key built into it, the build is newer, and the exe's size and SHA-256 match. Then it offers the update; one click
swaps it in and restarts. Settings and the holiday list on the PC are kept.

Nothing needs setting up on a PC: the program knows this address. Only the holder of the signing key can make a
release the program will accept, so a file put anywhere else is refused.
