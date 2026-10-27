# MaxiBestOf MCP

Connect an AI assistant to MaxiBestOf for web design research.
Search real website designs, UI sections, fonts, color palettes, and public
design profiles. Search saved website, font, and section references in your
connected account.

## Requirements

- A MaxiBestOf account with Pro access.
- An MCP client that supports Streamable HTTP and OAuth.

## Connect

Use this remote MCP endpoint:

```text
https://maxibestof.one/mcp-server
```

Complete the client's OAuth flow with your own MaxiBestOf account.
No static API key is required. The connection uses the `mcp:read` scope.

For Claude Code:

```sh
claude mcp add --transport http maxibestof https://maxibestof.one/mcp-server
```

For a client that supports the `mcpServers` configuration format:

```json
{
  "mcpServers": {
    "maxibestof": {
      "url": "https://maxibestof.one/mcp-server"
    }
  }
}
```

Use the client's normal OAuth connection step after adding the server.

## Example requests

- Find dark portfolio websites that use serif typography.
- Find sans serif fonts used in portfolio websites.
- Find font pairings for a chosen font family.
- Show dark color palettes with a warm accent.
- Find SaaS hero sections that include a product screenshot.
- Find design agencies in Los Angeles.
- Search my saved websites for homepage references.

## About this repository

This repository contains connection configuration for the hosted service.
The service source is private. No local server, credentials, or package
installation is included.

- [MCP setup](https://maxibestof.one/mcp)
- [Developer documentation](https://maxibestof.one/developers)
- [Public MCP manifest](https://maxibestof.one/.well-known/mcp.json)
- [Official MCP Registry entry](https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.luminous8%2Fmaxibestof)
- [Terms and privacy](https://maxibestof.one/legals)

Created by Bertrand Bruandet. Contact: bertrand@maxibestof.one.

## License

The connection configuration and documentation use the [MIT license](LICENSE).
The MaxiBestOf name, logo, hosted service, private source, and library content
are excluded from that license.
