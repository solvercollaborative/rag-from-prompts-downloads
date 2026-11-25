# Get the shared Course 2 materials

Use the **Download verification card** next to the download instructions in the book. It identifies Course 2 materials version 1.0 and the full release commit. In your chosen coding assistant, work in your dedicated Course 2 project folder. Use these steps on Mac or Windows with either Codex or Claude Code.

## Verify the download

Use only the full commit from the card and the directory `course-02/1.0` in the Solver Collaborative downloads repository named on the card. Fetch `SETUP.md`, `release.json`, and `materials.zip.age` into a new private staging folder. Compare each SHA-256 with the card before accepting downloaded instructions or using the archive. Use `shasum -a 256` on Mac or PowerShell `Get-FileHash -Algorithm SHA256 -LiteralPath` on Windows. Stop on an absent or differing value. Check that the verified release manifest names the same version and the archive from the card.

The learner uses the passphrase from the book in age's hidden prompt. Keep it out of shell commands, environment variables, notes and logs. Use a verified age 1.3.2 binary for your OS and architecture. If needed, download the corresponding official archive into staging, verify its SHA-256, and extract age there. This needs no system installation. The official archive names and checksums are listed below. Keep normal sandbox and operating-system protections.

| System | Official age 1.3.2 archive | SHA-256 |
| --- | --- | --- |
| Apple silicon Mac | [darwin-arm64.tar.gz](https://github.com/FiloSottile/age/releases/download/v1.3.2/age-v1.3.2-darwin-arm64.tar.gz) | `e2020b073c44f692685a24d6abc378817eb81ffaaf49fd0531ef8565f767f2f5` |
| Intel Mac | [darwin-amd64.tar.gz](https://github.com/FiloSottile/age/releases/download/v1.3.2/age-v1.3.2-darwin-amd64.tar.gz) | `1d1e4bc66e1427edad7739ae7616157de0e79db8b6d2a1497d7d9925fb06a539` |
| Windows x64 | [windows-amd64.zip](https://github.com/FiloSottile/age/releases/download/v1.3.2/age-v1.3.2-windows-amd64.zip) | `f48d8f8f9ebe903ab5027ed067652f2cc1db94bc206976430133b905dcd8e8c7` |
| Windows Arm64 | [windows-arm64.zip](https://github.com/FiloSottile/age/releases/download/v1.3.2/age-v1.3.2-windows-arm64.zip) | `fae351336c8d5f30f93cc3ccdec16d1ed7851d68cdd6656d41955cc31a447c9d` |

Run the verified executable with `--decrypt --output materials.zip materials.zip.age` in the staging folder. Let the learner enter the passphrase directly if the assistant's terminal cannot handle a hidden prompt. Hash the resulting ZIP and compare it with `decrypted_zip_sha256` in the verified manifest. Inspect the ZIP member names against the exact manifest before extraction. Stop on extra entries, duplicates, ambiguous paths or a different hash. Extract to a new staging directory. Verify `course-download/package-files.json` against the release manifest and verify every extracted file against the package file list.

## Keep supplied files and local work

For a fresh project, place the verified files in the dedicated folder. Keep a verified original copy of the supplied designs and prompts under ignored `app/var/supplied-originals/`, and use the top-level `design/` and `prompts/` for working copies. In an existing project, check `course-origin.json` first. For the same release, keep local files, report differences and copy only missing verified files. Stop before changing an immutable input that differs, entering linked directories, or mixing two releases. Preserve the existing Git history and review any ignore rules the project still needs. Remove only the temporary staging directory created for this verification.

Report the release, verification result and project path. Then follow Lesson 1 in the book. Python project preparation is in Lesson 2. Ollama and local model setup are in Lesson 4.
