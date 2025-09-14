# @petah/mcp-example

A simple example MCP (Model Context Protocol) server that provides a "hello world" tool.

## Installation

You can run this MCP server directly using npx:

```bash
npx -y @petah/mcp-example
```

Or install it globally:

```bash
npm install -g @petah/mcp-example
```

## Usage

This server provides a single tool called `hello_world` that returns a friendly greeting message.

### Tool: hello_world

**Description**: Returns a friendly hello world message

**Parameters**:
- `name` (optional string): Name to greet (defaults to "World")

**Example**:
```json
{
  "name": "hello_world",
  "arguments": {
    "name": "Alice"
  }
}
```

**Response**:
```json
{
  "content": [
    {
      "type": "text",
      "text": "Hello, Alice! 👋"
    }
  ]
}
```

## MCP Configuration

To use this server with an MCP client, add it to your MCP configuration:

```json
{
  "mcpServers": {
    "example": {
      "command": "npx",
      "args": ["-y", "@petah/mcp-example"]
    }
  }
}
```

## Development

### Setup

```bash
git clone https://github.com/petah/mcp-example.git
cd mcp-example
npm install
```

### Build

```bash
npm run build
```

### Development Mode

```bash
npm run dev
```

### Testing Locally

After building, you can test the server:

```bash
npm start
```

## License

MIT - see LICENSE file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.# mcp-example
