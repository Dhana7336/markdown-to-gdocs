# Markdown to Google Docs Converter

A Python-based utility that converts structured Markdown meeting notes into a fully formatted Google Doc using the Google Docs API. The script is designed to run in Google Colab and demonstrates clean API usage, formatting accuracy, and robust error handling.

## Features
- **Heading Conversion** — Markdown `#`, `##`, `###` mapped to Google Docs Heading 1–3  
- **Nested Bullet Lists** — Preserves multi-level bullet hierarchy with proper indentation  
- **Checkbox Support** — Markdown task items (`- [ ]`) converted to native Google Docs checkboxes  
- **Styled Assignee Mentions** — `@mentions` highlighted using bold and color styling  
- **Footer Styling** — Footer metadata rendered in a distinct, subtle style  
- **Error Handling** — Defensive parsing with meaningful runtime errors  
- **Index-Safe Updates** — Cursor-based document updates to avoid range errors  

## Tech Stack
- Python
- Google Docs API
- Google Drive API
- Google Colab

## Setup Instructions

1. Open notebook.ipynb in Google Colab
2. Run the authentication cell and sign in with your Google account
3. Execute all cells from top to bottom
4. A new Google Doc will be created automatically in your Google Drive.

## Dependencies

The following libraries are required (preinstalled in most Colab environments):
- google-api-python-client
- google-auth
- google-auth-httplib2
- google-auth-oauthlib

## Running in Google Colab

1. Open the notebook
2. Click Runtime → Run all
3. Approve Google authentication when prompted
4. The formatted Google Doc ID will be printed in the output

## Notes
- The document body is cleared before formatting to ensure repeatable runs
- All formatting is applied using a single batchUpdate request for efficiency
- The solution focuses on correctness, clarity, and API best practices within a constrained time limit
