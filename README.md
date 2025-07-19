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

1. **Install [uv](https://docs.astral.sh/uv/getting-started/installation/):**  
This is for managing our isolated virtual environments.

2. **Create a virtual environment and install dependencies:**
   ```bash
   uv venv .venv
   source .venv/bin/activate
   uv sync
   ```  
   More information about dependency resolution in uv can be found [here](https://docs.astral.sh/uv/concepts/projects/sync/).

3. **Set up your environment variables:**
   - You must have a Google API key `GOOGLE_API_KEY` configured. This can be set in your shell environment or by creating a `.env` file in the project root with the following content:
     ```env
     GOOGLE_API_KEY=your-google-api-key-here
     ```
   - The client will automatically load these keys from the environment or `.env` file.

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

## Running MCP Servers
You can find a list of open mcp servers to experiment with in this [repo](https://github.com/punkpeye/awesome-mcp-servers).  
Note that servers can be written in a variety of languages. This mcp client can only handle the following:  
- Python
- Javascript
- Typescript

### Dependencies
You are only meant to setup your environment for the kinds of servers you intend to use. If your server is in python, only those dependencies are relevant.

1. **Python**  
These will be specified in uv's lock file and will be installed when `uv sync` is run.
2. **Javascript**  
Requires the `node` runtime to be installed. Find the install steps [here](https://nodejs.org/en/download).
3. **Typescript**  
Requires `tsx` (an execution environment) to be installed. Install it after you have installed `node`. You'll find install steps [here](https://nodejs.org/en/learn/typescript/run#running-typescript-code-with-tsx).


## LImitations
Currently only one server can be run at a time. Running multiple servers will be addressed in future releases.

