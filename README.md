# Personal Identity Layer Template (PILT)

Use this repository as the starter Personal Identity Layer. Identity Layers are Markdown bundles that define the AI’s persona, guardrails, and default context. This layer stands on its own and can also be combined with a team layer to form a blended Identity.

## Structure

| Index | File | Purpose |
|-------|------|---------|
| 00 | 00_CORE_<PILname>.md | Central system prompt: non-negotiable instructions, values, and operating intent for this layer. |
| 01 | 01_INDEX_<PILname>.md | Routing table that explains when to load each identity file and what requirements gate it. |
| 02 | 02_TASKS_<PILname>.md | Personal workflows or shortcuts the AI runs verbatim when their triggers fire. |
| 03 | 03_SOURCES_<PILname>.md | Registry of preferred sources and the allowed / disallowed lists to obey when researching. |
| 04–08 | — | Reserved for future templates. |
| 09 | 09_MEMORY.md | Optional shared memory log the AI creates when file writes are available. |
| 10 | 10_USER_<PILname>.md | In-depth profile of the primary user for tailoring responses. |
| 11 | 11_PEOPLE_<PILname>.md | Profiles for third-party contacts relevant to the user. |
| 12 | 12_ORGANIZATION_<PILname>.md | Organizations that influence the user. |
| 13 | 13_ENVIRONMENT_<PILname>.md | Devices, software, and working conditions. |
| 14–18 | — | Reserved for future templates. |
| 19 | 19_GLOSSARY_<PILname>.md | Definitions for personal terminology and shorthand. |

## How to Customize and Use Your Personal Identity Layer

1. Fork or clone this repository and rename it for your personal layer (for example `Jarvis`).
2. Replace `<PILname>` across filenames and file contents, then tailor every document to match how you work. Each heading or field is only a prompt—reshape or delete anything that doesn’t serve you, and decide which identity files to use. Remove any unused placeholders from the identity files.
3. In `03_SOURCES_<PILname>.md`, provide either an Allowed list or a Disallowed list before you start researching; omit the unused section to avoid ambiguity.
4. Slots 20–99 are available for you to add any additional files as you see fit. For compatibility, avoid adding or renaming files in the 00–19 range.
5. Whenever you add, rename, retire, or relocate an identity file—whether in the core slots (00–19) or custom extensions (20–99)—update `01_INDEX_<PILname>.md` so the AI can route correctly, and keep cross-references in other files aligned.
6. Keep the layer’s canonical source in version control (e.g., a git repository) and tag releases or branches so composite identities and future you can pull updates confidently.
7. Deploy the layer by copying `00_CORE_<PILname>.md` into the system prompt (or equivalent) and dropping the supporting files wherever your platform expects them—file upload dialog, `.github/identity`, shared drive, etc. Treat these deployed copies as read-only.
8. If you combine this personal layer with a team layer, append your `00_CORE_<PILname>.md` after the team core file and stage all identity files from both layers.
9. When durable recall is needed, ensure the deployment environment allows the AI to create `09_MEMORY.md`; the agent will generate and update the file when permitted.
