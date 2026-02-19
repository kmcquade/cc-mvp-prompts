# Tool Description: fetch-url-content-analyze

- Name: WebFetchTool

## Summary

Tool that fetches an HTTPS page, converts to markdown, and analyzes it with a model.

# Raw Prompt Text
- Fetches content from a specified URL and processes it using an AI model
- Takes a URL and a prompt as input
- Fetches the URL content, converts HTML to markdown
- Processes the content with the prompt using a small, fast model
- Returns the model's response about the content
- Use this tool when you need to retrieve and analyze web content

Usage notes:
  - The URL must be a valid HTTPS URL
  - The prompt should describe what information you want to extract from the page
  - This tool is read-only and does not modify any files
  - Results may be summarized if the content is very large
