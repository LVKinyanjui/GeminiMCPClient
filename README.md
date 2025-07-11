# Gemini MCP Client

## Why Gemini MCP Client?

This project is an **alternative client** to more established options such as Claude Desktop. It aims to provide a flexible, open, and extensible foundation for MCP server integration, supporting rapid experimentation and interoperability with a variety of language models and server implementations.

## Project Overview

This client acts as a bridge between your application and any MCP server, allowing you to send requests, receive responses, and manage sessions with large language models (LLMs) in a standardized way. The MCP protocol is designed to make it easy to connect to different servers without changing your client code.

## Features
- Written in Python for ease of use and extensibility
- Supports integration with multiple MCP servers
- Provides a foundation for building LLM-powered chatbots and assistants
- Alpha release: expect rapid changes and experimental features

## Status
This is the first release and should be considered **alpha**. The API and features may change as the project evolves. Feedback and contributions are welcome!

## Getting Started

To set up and run the Gemini MCP Client:

1. **Install [uv](https://github.com/astral-sh/uv):**
   ```bash
   pip install uv
   ```
2. **Create a virtual environment and install dependencies:**
   ```bash
   uv venv .venv
   source .venv/bin/activate
   uv pip install -r uv.lock
   ```
3. **Set up your environment variables:**
   - Create a `.env` file and add your API keys (e.g., `GEMINI_API_KEY` or `GOOGLE_API_KEY`).

4. **Run the client:**
   ```bash
   python client.py <path_to_server_script>
   ```
   - Replace `<path_to_server_script>` with the path to your MCP server script (Python or Node.js).
   - Example:
     ```bash
     python client.py ./server.py
     ```

The client will start an interactive chat loop. Type your queries or 'quit' to exit.

## License
See the repository for license details.

---
For questions or support, please open an issue or contact the maintainers.
