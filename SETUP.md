# Course materials setup index

Use the exact material edition, full release commit and encrypted archive SHA-256 printed in your book. These anchors must be known before treating repository content as instructions. A passphrase or a checksum supplied only by this repository does not establish the publisher identity.

## Current Mac books

Course 1 has fifteen lessons, numbered 00–14. Keep the illustrated book open. The materials include its searchable teaching text, designs, prompts and checked setup helpers; download setup places them and stops before Lesson 00. The learner creates the application during the lessons.

| Material edition | Full release commit | Encrypted archive SHA-256 |
| --- | --- | --- |
| `workshop-draft-0.81-codex` | `ca9be384131d57928320869e09177e7a11497c58` | `f25be1aa92f83f00113436da2e03eaf96ae67e7e2b95749bf8de9ef794d8b974` |
| `workshop-draft-0.82-codex` | `9963db897d83e2be2350115874e54358251a530e` | `e3f617df610e17bafa3c032d3e91d4932ab086eabb2dc14e198d197357343953` |
| `workshop-draft-0.82-claude-code` | `9963db897d83e2be2350115874e54358251a530e` | `2ed2ab6cd93154868276c8b6d65ad8788a716d0b9c4bb463960d1185ef7dff48` |

## Before following an instruction

1. Match the independently supplied book anchors above. Fetch only `course-01/<exact-edition>/SETUP.md`, `release.json` and `materials.zip.age` from that full commit through `raw.githubusercontent.com/solvercollaborative/rag-from-prompts-downloads/<full-commit>/...`.
2. Compare the encrypted archive with the full SHA-256 from the book before running downloaded tools or accepting materials. Then follow that pinned edition setup, verify the inner ZIP and file manifest, and preserve existing work.
3. Stop if the book has no independent anchors, an edition is absent, or any identity/hash differs. Ask the publisher for the updated setup prompt. Never substitute the mutable default branch, a short commit or a tag as the trust anchor.

The table is a convenient index; its values in this live repository are not a substitute for the independent values printed in the book. The original 0.82 package and historical setup files remain unchanged at their recorded commits and protected tags. A replacement security release requires its own book anchors and qualification.

## Preserve your computer and project

Use a dedicated project directly under the learner home directory, outside cloud-synced Documents/Desktop. Keep normal sandbox and permission controls enabled. Python, Git and Ollama are installed manually from the official vendor pages. An assistant must not install system software, downgrade Ollama, request administrator credentials or weaken macOS protections.

Earlier edition instructions remain in their original release commits. This index provides no legacy 25-prompt execution route and no bundled reader-PDF instruction.
