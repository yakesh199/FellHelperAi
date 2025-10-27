# FellHelperAI 🤖

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

FellHelperAI is an advanced voice-enabled AI assistant that combines the power of Google's Gemini AI with real-time speech recognition. It creates a seamless, natural interaction between users and AI, making it perfect for various applications from interviewing to coaching and educational assistance.

## ✨ Key Features

- 🎙️ **Real-time Voice Recognition**: Crystal-clear speech recognition powered by AssemblyAI
- 🧠 **Advanced AI Processing**: Leverages Google's Gemini AI for sophisticated natural language understanding
- 💡 **Context-Aware**: Maintains conversation context for more natural and coherent interactions
- 🔄 **Real-time Responses**: Instant AI responses with minimal latency
- 🎯 **Customizable Personality**: Easily adaptable for different roles and use cases
- 🔊 **Voice Output**: Natural speech synthesis for AI responses

## 🛠️ Technical Stack

- **Speech Recognition**: AssemblyAI API
- **AI Processing**: Google Gemini AI
- **Language**: Python 3.8+
- **Audio Processing**: SoundDevice & SoundFile
- **Environment Management**: python-dotenv
- **Dependencies**: Managed with pip

## Prerequisites

Before running the voice agent, make sure you have:

- Python 3.8 or higher
- A microphone connected to your computer
- AssemblyAI API key (get it from [AssemblyAI](https://www.assemblyai.com/))
- Google API key for Gemini AI (get it from [Google AI Studio](https://makersuite.google.com/app/apikey))

## Installation

1. Clone the repository:
```bash
git clone <your-repository-url>
cd <repository-directory>
```

2. Create and activate a virtual environment:
```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# Linux/Mac
python -m venv venv
source venv/bin/activate
```

3. Install the required packages:
```bash
pip install google-generativeai assemblyai sounddevice soundfile requests python-dotenv
```

4. Create a `.env` file in the project root and add your API keys:
```
ASSEMBLYAI_API_KEY=your_assemblyai_api_key
GOOGLE_API_KEY=your_google_api_key
```

## Running the Voice Agent

1. Make sure your microphone is connected and working
2. Activate your virtual environment (if not already activated)
3. Run the script:
```bash
python voiceagent.py
```

4. Start speaking when you see "🎙️ Listening..."
5. Say "Power off" to exit the program

## Customizing the Agent

You can customize the agent's behavior by modifying the system prompt in the `__init__` method of the `AIVoiceAgent` class. The current implementation is set up as an interviewer, but you can modify it for different roles such as:

- Python/Data Science coach
- Language learning assistant
- General assistant
- Task-specific expert

Example modification:
```python
self.transcript = [{"role": "system", "content": """
    You are a helpful Python programming coach.
    Keep your answers concise and clear.
    Focus on practical examples and best practices.
"""}]
```

## Troubleshooting

1. **Microphone Issues**
   - Check if your microphone is properly connected
   - Ensure it's set as the default input device
   - Check microphone permissions for Python/your IDE

2. **API Key Issues**
   - Verify your API keys are correctly set in the `.env` file
   - Check if the API keys are valid and have sufficient credits

3. **Package Issues**
   - Try reinstalling the packages if you encounter import errors
   - Make sure you're using a compatible Python version

## Dependencies

- `google-generativeai`: Google's Gemini AI API
- `assemblyai`: Real-time speech recognition
- `sounddevice`: Audio input handling
- `soundfile`: Audio file operations
- `python-dotenv`: Environment variable management
- `requests`: HTTP requests handling

## Contributing

Feel free to submit issues, fork the repository, and create pull requests for any improvements.

## License

[Add your chosen license here]

## Acknowledgments

- AssemblyAI for real-time speech recognition
- Google for Gemini AI capabilities
- All contributors and users of this project