# Assistant setup instructions

These steps are for the coding assistant. The student supplies a repository link
and materials passphrase in the conversation; do not ask them to run commands or
type the phrase into a private terminal prompt themselves.

## 1. Select and download

Confirm you are operating locally on the student's Mac in their dedicated learner
folder. Keep the public download repository separate from that learner repository;
do not make the learner work inside a clone of this distribution repository.

Read `course-01/workshop-draft-0.24/release.json`. Download its encrypted archive
from this repository to a temporary directory. Verify its SHA-256 against the
manifest before decrypting. Use the release's pinned Git tag for a frozen checkout:
`course-01-workshop-draft-0.24`.

A checksum detects an incomplete or changed download; it is not independent proof
of who published it. Use only this repository and the official age release below.

## 2. Obtain age if needed

Use an existing compatible `age` installation if available. Otherwise download
v1.3.2 for the Mac's architecture to temporary storage; no Homebrew installation,
system settings change, Python installation, or administrator access is needed.

Official assets:

- Apple silicon: https://github.com/FiloSottile/age/releases/download/v1.3.2/age-v1.3.2-darwin-arm64.tar.gz
  SHA-256: `e2020b073c44f692685a24d6abc378817eb81ffaaf49fd0531ef8565f767f2f5`
- Intel: https://github.com/FiloSottile/age/releases/download/v1.3.2/age-v1.3.2-darwin-amd64.tar.gz
  SHA-256: `1d1e4bc66e1427edad7739ae7616157de0e79db8b6d2a1497d7d9925fb06a539`

Verify the selected asset's checksum before extracting or executing it. Extract
it in the temporary directory and use its `age/age` binary.

## 3. Decrypt and inspect

Run age in a tool terminal with a PTY (interactive terminal support), for example:

```
age --decrypt --output /temporary/path/materials.zip /temporary/path/materials.zip.age
```

When age requests the passphrase, send the phrase the student supplied through
your terminal tool. age's own prompt hides typing; this does not require a separate
student action. Do not invent a passphrase. On error, stop; never unpack partially
decrypted output. Ask the student to check their assigned edition and phrase.

After age succeeds, verify the decrypted ZIP's SHA-256 against `release.json`.
Inspect the ZIP member list before extraction: no absolute paths, `..` traversal,
or symbolic links. Extract into a NEW temporary staging directory. Check each
file against `course-download/package-files.json`, and confirm the archive has
only the members listed in `release.json`.

## 4. Place without overwriting student work

If the learner folder already has `course-origin.json`, compare its source_commit
with the supplied baseline. A different revision needs a separate new attempt;
do not replace the original baseline. For the same revision, preserve existing
prompt customizations, source edits, code, and Git history. Report differences;
do not reset them. Repeat setup should leave existing content unchanged.

For a fresh learner folder, copy the staged materials into it. For a repeated
setup of the same edition, copy only missing files (macOS `unzip -n` also never
overwrites existing files). Do not copy a public-repository `.git` directory.
Preserve an existing `.gitignore`; append only missing package ignore patterns.
Confirm the encrypted book, decrypted book, source documents and runtime index
will not be accidentally committed to the student's public Git repository. The
supplied `.gitignore` excludes `course-download/`, `**/data/books/`, and `**/var/`.
Prompt files and their original baseline may be tracked in the student's project.

Validate that the untouched supplied `app/data/books/course.md` matches
`course-download/source-provenance.json` before first use. If an existing student's
file differs, preserve it and explain the difference; do not silently restore it.

Open `course-download/course-book.pdf`. Show the student `prompts/01.md` and explain
that only its fenced text build prompt should be sent for execution. Stop here.
Prompt 6 will create the app source manifest; do not prebuild application code,
install its tools, or run all 25 prompts during download setup.

The full text at `course-download/course-book.md` preserves the manuscript's
image references, but separate artwork files are not bundled; the PDF provides
the illustrations. The app does not need the PDF or those images for ingestion.
