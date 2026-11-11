# Postify MCP

The official Postify Model Context Protocol (MCP) server configuration and Cursor plugin. It connects an AI assistant to your Postify account so it can create, schedule and publish social media posts.

## Server

- URL: `https://api.postify.tech/mcp`
- Transport: Streamable HTTP (remote)
- Authentication: OAuth 2.1 with PKCE. You sign in to Postify in the browser. There is no API key.
- Documentation: https://postify.tech/mcp

The legacy SSE endpoint `https://api.postify.tech/v1/mcp/sse` keeps working until July 28, 2027. New setups should use the URL above.

## Install

### Cursor

Install the Postify plugin from the Cursor Marketplace, or add the server to your `.cursor/mcp.json`:

```json
{
    "mcpServers": {
        "postify": {
            "url": "https://api.postify.tech/mcp"
        }
    }
}
```

### Other MCP clients

Add a remote MCP server with the URL `https://api.postify.tech/mcp` and choose HTTP or Streamable HTTP as the transport. When the client opens the browser, sign in to Postify to authorize it. Setup steps for Claude, ChatGPT and other clients are at https://postify.tech/mcp.

## Features

* **Read & Draft:** Quickly summarize drafts or generate new posts without leaving your IDE.
* **Security Auditing:** Ask your assistant to list all active AI sessions connected to your account.
* **Secure OAuth:** Connects securely via WorkOS AuthKit using strict PKCE flows.

## How to use

Once connected, ask your assistant to work with your Postify account:

> "Check my Postify profiles for recent analytics."
> "Create a new post on Postify for my linked profiles announcing our new feature."

## License

MIT. See [LICENSE](LICENSE).
