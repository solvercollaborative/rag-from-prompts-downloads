# Mac + Claude Code materials setup: workshop-draft-0.84-claude-code

These instructions apply to Course 1, Mac + Claude Code version 0.84 only. Read this file only at the full release commit printed independently in the book. Do not follow a mutable root SETUP.md or branch. Read its adjacent release.json and confirm edition `workshop-draft-0.84-claude-code` and source commit `43b1832182de97048f2dffd6636360cb7bffe97c` before downloading.

These steps are for the coding assistant. The learner supplies the repository link and materials passphrase from the book. For books with a Download verification card, also check the exact edition, full release commit, and SHA-256 values for this file, release.json and the encrypted archive against that card before using the files. For earlier books use the independent checks printed in their download prompt. Stop if the independent commit/hash is missing or differs; repository metadata and the shared passphrase cannot replace that trust anchor. The assistant runs the commands and reports the result. Preserve the learner's existing files and local edits.

## Download before preparing Git or Python

Work locally on the learner's Mac. Use a fresh temporary child of ignored `app/var/download-staging/` inside the learner project; remove only that child after completion and preserve compact error evidence. Download `materials.zip.age` from this exact edition directory and verify its SHA-256 against the independently printed book hash and its size against release.json before decrypting. Fetch all edition files through the book’s full release commit; a tag or branch name is not a trust anchor. a Git installation or GitHub account is unnecessary. macOS curl, shasum, tar and unzip provide the download tools. Built-in JavaScript through osascript can read JSON manifests and perform file-list checks without project Python. The learner installs any missing system tools through the official links in the book; Lesson 01 checks them and prepares only the project environment.

If the named edition is unavailable or any check fails, stop with that specific problem. Keep existing files intact and ask the learner to check the book's exact edition. Continue only after all required checks succeed.

## Obtain the verified decryption tool

Use an existing age v1.3.2 binary whose source has been verified. Otherwise download the official archive for the Mac's architecture to project-private temporary storage:

- Apple silicon: https://github.com/FiloSottile/age/releases/download/v1.3.2/age-v1.3.2-darwin-arm64.tar.gz — SHA-256 `e2020b073c44f692685a24d6abc378817eb81ffaaf49fd0531ef8565f767f2f5`.
- Intel: https://github.com/FiloSottile/age/releases/download/v1.3.2/age-v1.3.2-darwin-amd64.tar.gz — SHA-256 `1d1e4bc66e1427edad7739ae7616157de0e79db8b6d2a1497d7d9925fb06a539`.

Verify the chosen archive's checksum before extracting or executing its `age/age` binary. This is a project-private temporary tool; it needs no Homebrew installation, administrator access or global configuration change. Keep sandbox controls enabled and never weaken Gatekeeper.

## Decrypt and verify the exact materials

Run age with your tool's interactive terminal support, using actual temporary paths:

```text
/verified/path/age --decrypt --output /temporary/path/materials.zip /temporary/path/materials.zip.age
```

Supply the materials passphrase through age's hidden terminal prompt. Keep it out of command arguments, environment variables, logs and public files. The assistant handles this exchange; the learner has already supplied the phrase in the download prompt.

After successful decryption, compare the ZIP's SHA-256 with `decrypted_zip_sha256`. Inspect its complete member list before extraction. Require exactly the 46 names in release.json, including `prompts/00.md` through `prompts/14.md`. Reject absolute paths, backslashes, drive prefixes, empty/dot/parent path components, trailing spaces/dots, symlinks, special files, duplicate or case-colliding names, and file/directory conflicts. Reject encrypted inner members, invalid CRCs, over 2,000 entries, over 256 MiB of ZIP data, over 512 MiB expanded data, over 128 MiB per member or a compression ratio over 200:1. Extract only into a new temporary directory after these checks pass.

Verify every extracted file against `course-download/package-files.json`, whose own SHA-256 must match `package_manifest_sha256` in release.json. The manifest lists the other 45 supplied files; the release lists all 46. Confirm `course-origin.json` and `course-download/source-provenance.json` both name assistant edition `claude-code`, book version `0.84` and source commit `43b1832182de97048f2dffd6636360cb7bffe97c`. A model profile's baseline version identifies that profile separately; its unchanged bytes are checked through the supplied manifest.

The package contains editable designs, fifteen prompts, the glossary, complete searchable student-edition text and setup/security helpers. The generated application, runtime index and model weights are created during the lessons. Keep the illustrated book already open as the reading guide; this materials ZIP contains the matching text and helpers rather than another PDF copy.

## Place the checked materials and stop before Lesson 00

Use the learner's dedicated `rag-from-prompts-course-01` folder. Keep any public download-repository clone separate from that folder. For a fresh project, copy the verified files into it without a distribution `.git` folder. For an existing project, preserve its work, prompt/design customizations and Git history. Compare its existing `course-origin.json` before any copy; a different edition/source needs a separate attempt. For the same edition, copy only missing files, preserve existing differences and report them. Preserve an existing `.gitignore` and add only missing supplied ignore rules after review.

Confirm the folder has `design/`, `prompts/`, `glossary.md`, `course-origin.json` and `course-download/`. The searchable book is `app/data/books/course.md`; compare its exact bytes with source-provenance.json before first use. Verify supplied security helpers against the manifest before executing them in the appropriate lesson. Download setup places these files; the learner installs system tools manually and Lesson 01 prepares the project environment.

Report the edition, book version, destination, verification result and any existing files preserved. Show `prompts/00.md` and the three starting references it names: `design/shared-rules.md`, `design/application.md` and `design/00-project.md`. The learner reads Lesson 00 in the already open book, then pastes its action block into the coding-assistant conversation. Stop before executing it. The lesson creates project memory and later lessons create the application.

## Public and private files

The encrypted archive may be shared under the repository's materials permission. Keep the passphrase, decrypted book text, illustrations, generated source data, runtime index, personal records and model files out of public Git. The supplied ignore rules protect the course-download, source-book and working-data folders. The learner's editable prompt/design files and generated application can be saved according to the course's Git instructions.
