# RAG from Prompts: workshop downloads

Companion materials for **The Simplest Possible RAG Application in 25 Prompts**
by Alan Street / Solver Collaborative.

## Start here

You need **Codex on your Mac**, this repository link, and the passphrase supplied
in your first workshop session or its Maven lesson. If you already have the book,
the passphrase appears in **Get your workshop downloads**.

Need Codex first? Follow the [official setup guide](https://learn.chatgpt.com/docs/quickstart).
Open the app, follow its sign-in screens, and select Codex for software development.
Create a dedicated local folder named `rag-from-prompts-course-01`.

**Current materials: Course 1 / workshop-draft-0.52.** These are workshop-draft
learning materials. The recorded draft-0.48 reference completed all 25 builds,
immediate repeats and a full replay after documented corrections. Draft 0.49
adds security guidance and package-hash requirements; its hash-lock correction
was tested separately, and its complete 75-gate execution has not been rerun. Focused
application demonstrations were checked against actual source passages. Other
evaluation questions exposed incorrect or incomplete answers; a few successful
examples do not promise correct answers to every question. Fresh-machine setup
and a student pilot remain unrun. Draft 0.50 corrects the referenced book title;
application behavior and build prompts are unchanged from draft 0.49. Draft 0.51
clarifies the instructor testing system and assistant-led download verification.
Draft 0.52 distinguishes reviews on the instructor's Mac from student installation
checks; the instructor review does not inspect student Macs.
The download contains materials for building
your app, with no completed application bundled.

Copy this message into Codex, replacing the passphrase placeholder:

> Help me start Course 1 on this Mac. The download repository is
> https://github.com/solvercollaborative/rag-from-prompts-downloads and my edition
> is workshop-draft-0.52. My materials passphrase is: REPLACE_WITH_YOUR_PASSPHRASE.
> Read the repository's SETUP.md and release.json for that edition. Download and
> verify the encrypted package, decrypt it, and put the materials in my dedicated
> rag-from-prompts-course-01 folder, preserving any existing work. Handle the
> commands yourself. Report the edition and whether all download and extracted-file
> checks passed. If any check fails or cannot be completed, stop before copying
> materials into my course folder and explain the problem; do not bypass the check.
> Preserve existing work and report any files skipped for that reason.
> Open course-download/course-book.pdf and show me where to
> find prompts/01.md. Stop before executing Prompt 01 so I can read it and begin.

You do not need to type terminal commands or create a GitHub account. The shared
materials passphrase may be given to your coding assistant; it is not an account
password. Your assistant will need internet access to download the package and,
if needed, a small decryption utility.

## What you receive

One encrypted ZIP archive contains:

- The illustrated course PDF.
- The complete manuscript text in Markdown (illustrations are in the PDF).
- The prepared course prose for the local RAG app, at `app/data/books/course.md`.
- All 25 prompt handouts, an original-prompt baseline, and learner examples.
- Edition information, file fingerprints, and starting instructions.

The prepared prose retains the course explanations; it removes fenced code and
marked exercises/answer keys so evaluation answers do not become retrieval evidence.
Only this prepared file is registered as the application's source. The full text
copy and PDF remain available for reading outside the source folder.

Python, Ollama, dependencies, and models are obtained during the course. The app,
its tests, evaluations, and local index are built through the prompts.

## Editions and access

Use the edition assigned by your instructor. Published editions are frozen; a
later edition gets a new directory. Keep your current attempt and customized
prompts when starting a new edition. Each edition's passphrase remains valid for
that edition's archived download.

The PDF and Markdown are encrypted together using the standard
[age file-encryption tool](https://github.com/FiloSottile/age). The public repository
intentionally contains no plaintext book or passphrase. Encryption discourages
casual collection of the book from this public repository; it cannot prevent a
recipient from sharing decrypted material.

Workshop dates and passphrases are supplied separately by the instructor. This
repository does not include live support or promise future workshops.
