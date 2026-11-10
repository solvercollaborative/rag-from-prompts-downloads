# Local-first RAG and GraphRAG from Prompts: Course 1 downloads

Companion materials for Alan Street’s illustrated Course 1 books. Both Mac books
teach the same local book-question application in fifteen guided prompts. Choose
the edition that matches your coding assistant.

| Mac book | Materials edition | Release |
| --- | --- | --- |
| Build Your First Web App with OpenAI Codex on Mac | `workshop-draft-0.82-codex` | [Mac + Codex](course-01/workshop-draft-0.82-codex/release.json) |
| Build Your First Web App with Anthropic Claude Code on Mac | `workshop-draft-0.82-claude-code` | [Mac + Claude Code](course-01/workshop-draft-0.82-claude-code/release.json) |

## Start with your book

Use the exact edition and version printed in your book. In **Get your workshop
downloads**, copy the download prompt into your coding assistant. It includes
this repository, the matched edition and the materials passphrase. The assistant
downloads and verifies the files, preserves existing work and stops before
Lesson 00 so you can read it first.

You do not need a GitHub account, Git or project Python for this download step.
Before Lesson 01, install system tools through the official vendor links in the book. The assistant then checks the tools and prepares the project environment. Keep normal sandbox and permission controls enabled. Keep the illustrated
Kindle book or PDF open as your reading guide; the small materials package
contains the matching text and helpers rather than another illustrated book.

## What the materials contain

Each encrypted package contains 46 files: fifteen action prompts, editable
designs, a glossary, the complete searchable text of that student edition,
verified security helpers and file/version information. The lessons guide your
assistant to create the application. Models and the search index are prepared
during the course.

The assistant first requires the full release commit and encrypted-archive SHA-256 printed independently in the book. It follows only that commit’s requested edition manifest and adjacent SETUP.md after comparing the archive with the book hash. See the [setup index](SETUP.md). A book without those independent values needs an updated publisher setup prompt. Each published directory has its own immutable `course-01-<edition>`
tag. Earlier releases remain available for books that name them, including
`workshop-draft-0.81-codex`. Preserve an existing project when starting another
edition.

## Access

Packages use [age passphrase encryption](https://github.com/FiloSottile/age).
The passphrase is supplied in the matching book. This repository contains the
encrypted materials, setup instructions and release manifests. Keep decrypted
course text and personal project data in your local project.
