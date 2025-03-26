# Gemini Chat Enhanced

![Gemini Chat Enhanced](assets/logo.png)

A feature-rich desktop chat application built with PyQt5 that uses Google's Gemini API for text generation, multi-agent conversations, and image generation capabilities.

## Disclaimer

This application is an independent project and is not developed, endorsed, or officially associated with Google. "Gemini" is a trademark of Google LLC, and this application uses the Gemini API as a third-party service.

## Features

- **Advanced Chat Interface**: Clean, intuitive tabbed interface with multiple chat sessions
- **Themable UI**: Choose from built-in themes or create custom themes with the theme editor
- **Multi-Agent Conversations**: Enable dialog between multiple specialized AI agents with different roles
- **Image Generation**: Generate images using Google's Gemini 2.0 Flash API and Imagen 3
- **Custom Actions**: Create and manage reusable actions for common tasks and prompts
- **Environment Management**: Load API keys and configurations from .env files
- **Agent Memory System**: Agents retain information across conversation turns for context-aware interactions
- **File Operations**: Save and load chats, outputs, and entire sessions

## Getting Started

### Prerequisites

- Python 3.7+
- Google Gemini API key ([Get one here](https://ai.google.dev/))
- Windows, macOS, or Linux operating system

### Installation

1. Clone the repository or download the source code
2. Create a virtual environment (recommended)
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```
3. Install required packages
```bash
pip install -r requirements.txt
```
4. Create a `.env` file with your Google Gemini API key
```
GEMINI_API_KEY=your_api_key_here
```
5. Run the application
```bash
python GAI.py
```

## Usage

### Basic Chat

1. Type your message in the input area
2. Click "Generate" or press Ctrl+Enter
3. View the AI's response in the output area

### Keyboard Shortcuts

- `Ctrl+Enter`: Generate response
- `Ctrl+Tab`: Next chat tab
- `Ctrl+Shift+Tab`: Previous chat tab
- `Ctrl+S`: Save output to file
- `Ctrl+L`: Clear history
- `Esc`: Stop generation

### Using Multi-Agent Mode

1. Go to the "Agents" tab in the settings panel
2. Enable "Agent Mode" and "Multi-Agent Dialog"
3. Configure the number of agents (2-6) and their roles
4. Choose an interaction mode (Sequential, Interactive, or Continuous Debate)
5. Return to the chat and send a message
6. Watch as multiple specialized agents discuss your query

### Generating Images

1. Go to the "Tools" tab
2. Enter an image prompt in the text field
3. Select the desired model and size
4. Click "Generate Image"
5. Wait for the image to generate (this may take some time)
6. Save the generated image using the "Save Image" button

### Custom Actions

1. Click "Manage Actions" to open the action manager
2. Create new actions for common tasks:
   - `insert_text`: Add predefined text to the input area
   - `generate`: Insert text and automatically generate a response
   - `clear`: Clear input, output, or both
   - `execute_code`: Run custom Python code for advanced functionality
3. Use actions from the dropdown in the chat interface

## Configuration

The application saves your preferences, including:
- UI theme and fonts
- Model settings
- Agent configurations
- Custom actions

These settings are stored in JSON files in the application directory.

## Known Issues

- **Image Generation**: Some models or configurations may cause errors. If an image fails to generate, try a different model or prompt.
- **Multi-agent Conversation**: For continuous mode, stopping might have a delay as the system completes the current agent's response.
- **API Rate Limits**: When using the API extensively, you may encounter rate limiting. Consider implementing delays between requests.

## Troubleshooting

If you encounter issues:

1. Check if your API key is correctly set in the `.env` file
2. Ensure you have the latest version of the Google Generative AI SDK:
   ```bash
   pip install --upgrade google-generativeai
   ```
3. Check the `app.log` file for detailed error messages
4. Try restarting the application after making configuration changes

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- Google Gemini API for powering the AI capabilities
- PyQt5 for the GUI framework
- The Python community for various libraries and tools
