# Tool Description: fetch-url-and-summarize

- Name: WebFetchTool

## Summary

Fetches an HTTPS URL, converts to markdown, and analyzes it with a small model using a provided prompt.

# Raw Prompt Text
- Fetches content from a specified URL and processes it using an AI model
- Takes a URL and a prompt as input
- Fetches the URL content, converts HTML to markdown
- Processes the content with the prompt using a small, fast model
- Returns the model's response about the content
- Use this tool when you need to retrieve and analyze web content

Usage notes:
  - The URL must be a valid HTTPS URL
  - For security reasons, the URL must have been provided directly by the user in the current or a previous message
  - The prompt should describe what information you want to extract from the page
  - This tool is read-only and does not modify any files
  - Results may be summarized if the content is very large
