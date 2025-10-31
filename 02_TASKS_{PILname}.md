# TASKS

Task macros keyed to short triggers. When a trigger is invoked, run the associated workflow exactly as written.

## Create Identity File
- **Requirements:** file-write
- **Trigger Phrase / Intent:** "Create new identity file", "Add identity file", "Generate [category] file"
- **Purpose:** Add a new identity file to the personal layer, following established naming and categorization conventions.
- **When to Run:** Whenever the user requests a new identity file and file writes are permitted.
- **Prompt:**
  > Create a new identity file with contents specified by the user. Place the new file in the identity file directory. Follow the correct naming convention. Follow the README structure table for category and numbering. Reserve the X0 index (e.g., 20, 30, 40, etc.) for category overviews or templates. Update the INDEX file and notify the user when done.

## Conversation Report
- **Requirements:** none
- **Trigger Phrase / Intent:** "Conversation report", "Summarize this chat", "Generate session summary"
- **Purpose:** Extract and format a comprehensive report of the current conversation, including key details, open questions, and actionable next steps.
- **When to Run:** Whenever the user requests a conversation report or summary.
- **Workflow:**
  1. Extract all key details, decisions, and context from the current chat history.
  2. Identify any open questions, unresolved issues, or loose ends.
  3. Ask the user targeted follow-up questions to clarify or resolve any gaps before proceeding.
  4. Format the report with:
     - Executive summary
     - Chronological review
     - Key decisions and rationale
     - Open questions and next steps
     - References to relevant files or documentation
  5. Present the report in Markdown, ready for copy-paste or archival.
  6. Offer to save the report to memory or a designated file if file writes are enabled.
  7. Confirm with the user that the report meets their needs and make any requested adjustments.
