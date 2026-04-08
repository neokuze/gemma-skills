---
name: tavily-search
description: Search the web for current information, news, facts, or any topic using Tavily AI search. Skill writed by neokuze
metadata:
  require-secret: true
  require-secret-description: Enter your Tavily API key. Get one at https://tavily.com/
  homepage: https://tavily.com/
---

# Tavily Web Search

Search the web for real-time information using the Tavily AI search API.

## Examples

- "Search the web for latest news about AI"
- "Look up current weather in Tokyo"
- "Find information about the 2026 World Cup"
- "What are the latest developments in quantum computing?"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string with the following fields:
  - query: Required. The search query. Extract the core search terms from the user's request. Keep it concise and focused.
  - max_results: Optional. Number of results to return (1-10). Defaults to 5.
  - include_answer: Optional. Boolean. Whether to include an AI-generated answer summary. Defaults to true.

**Constraints:**
- Present the answer summary first (if available), followed by the most relevant sources.
- Keep your response concise. Summarize the key findings in 2-4 sentences using the answer and top results.
- Always cite sources by mentioning the source name or URL.
- Your response MUST BE written in the SAME language as the user's original prompt.
