# Gemini Chat Enhanced

A feature-rich desktop chat application built with PyQt5 that uses Google's Gemini API for text generation, multi-agent conversations, and image generation capabilities.

## Disclaimer

This application is an independent project and is not developed, endorsed, or officially associated with Google. "Gemini" is a trademark of Google LLC, and this application uses the Gemini API as a third-party service.

## Features

- **Advanced Chat Interface**: Clean, tabbed interface with multiple chat sessions
- **Themable UI**: Choose from built-in themes or create custom themes
- **Multi-Agent Mode**: Enable conversations between multiple AI agents with different roles
- **Custom Actions**: Create and manage reusable actions for common tasks
- **Environment Management**: Easily load API keys and configurations from .env files
- **File Operations**: Save and load chats, outputs, and sessions

## Getting Started

### Prerequisites

- Python 3.7+
- PyQt5
- Google Generative AI Python SDK
- PIL/Pillow for image handling
- python-dotenv for environment variables

### Installation

1. Clone the repository
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

### Using Multi-Agent Mode

1. Go to the "Agents" tab in the settings panel
2. Enable "Agent Mode" and "Multi-Agent Dialog"
3. Configure the number of agents and their roles
4. Return to the chat and send a message
5. Watch as multiple agents discuss your query

### Generating Images ###Under development###

1. Go to the "Tools" tab
2. Enter an image prompt in the text field
3. Select the desired model and size
4. Click "Generate Image"
5. Save the generated image using the "Save Image" button

### Custom Actions

1. Click "Manage Actions" to open the action manager
2. Create new actions for common tasks
3. Use actions from the dropdown in the chat interface

## Configuration

The application saves your preferences, including:

- UI theme and fonts
- Model settings
- Agent configurations
- Custom actions

These settings are stored in JSON files in the application directory.

## Known Issues

- **Image Generation**: The image generation feature is currently under development. Some models or configuration combinations may not work properly, and errors may occur during image generation.

- **Goal Updates**: The goal tracking and update functionality is still in development and may not reflect accurate progress or properly save goal states.

- **Multi-agent Conversation**: For multi-agent dialogs in continuous mode, stopping the conversation might have a delay as the system completes the current agent's response before fully terminating.

- **API Rate Limits**: When using the API extensively, especially with multi-agent conversations or image generation, you may encounter rate limiting from Google's API. Consider implementing appropriate delays between requests.

## Troubleshooting

If you encounter issues:

1. Check the console for error messages
2. Verify your API key is correctly set in the `.env` file
3. Ensure you have the latest version of the Google Generative AI SDK:
   ```bash
   pip install --upgrade google-generativeai
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- Google Gemini API for powering the AI capabilities
- PyQt5 for the GUI framework
- The Python community for various libraries and tools
