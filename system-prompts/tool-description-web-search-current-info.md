# Tool Description: web-search-current-info

- Name: WebSearch

## Summary

Searches the web for up-to-date information and returns formatted result blocks.

# Raw Prompt Text
- Allows Claude to search the web and use the results to inform responses
- Provides up-to-date information for current events and recent data
- Returns search result information formatted as search result blocks
- Use this tool for accessing information beyond Claude's knowledge cutoff
- Searches are performed automatically within a single API call

Usage notes:
  - Domain filtering is supported to include or block specific websites
  - Web search is only available in the US
  - Account for "Today's date" in <env>. For example, if <env> says "Today's date: ${DATE}", and the user wants the latest docs, do not use ${NUM} in the search query. Use ${NUM}.
