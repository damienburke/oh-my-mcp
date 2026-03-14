# News MCP Server

A Ktor-based server written in Kotlin implementing the Model Context Protocol (MCP) with tools for fetching news
headlines and searching news articles using the NewsAPI.

## Features

Top Headlines Tool: Fetches top news headlines by category (business, entertainment, general, health, science, sports,
technology).
Search News Tool: Searches news articles by query, with advanced search options and date/sort filters.

## Requirements

JDK
Gradle
NewsAPI Key: Register at newsapi.org and set the NEWS_API_KEY environment variable.

## Run the server

The server will start on http://localhost:3001.

## Usage

The server exposes two MCP tools:

1. Get Top Headlines
2. Search News

## Integration with Cursor

To use this MCP server with Cursor, you need to configure Cursor to connect to your local MCP server instance. Follow
these steps:

1. Start the MCP server (see instructions above).
2. Go to Cursor → Settings → Tools & Integrations → New MCP Server.
3. Add the following configuration:

```json
{
  "mcpServers": {
    "news-mpc-server": {
      "url": "http://localhost:3001/sse"
    }
  }
}
```