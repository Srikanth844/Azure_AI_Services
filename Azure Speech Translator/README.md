# Azure Speech Translator

## Overview

Azure Speech Translator is a Python-based application that uses Microsoft Azure's Speech Services to perform real-time speech-to-text translation and speech synthesis. This application allows users to speak in English and receive translations in French, Spanish, or Hindi.

## Features

- Speech-to-text translation from English to multiple languages

- Supports French, Spanish, and Hindi translations

- Real-time speech synthesis in the translated language

- Uses Azure Cognitive Services for speech recognition and translation

## Prerequisites

To run this project, ensure you have the following:

- Python 3.x installed

- An Azure Speech Services account

- Azure Speech key and region

- Required dependencies installed

## Installation

1. **Clone the repository**:
```bash
git clone https://github.com/your-username/AzureSpeechTranslator.git
cd AzureSpeechTranslator
```
2. **Install dependencies**:
```bash
pip install -r requirements.txt
```
3. **Set up environment variables**:
Create a .env file in the root directory and add your Azure Speech credentials:
```bash
SPEECH_KEY=your_speech_key
SPEECH_REGION=your_speech_region
```
## Usage

1. Run the script:
```bash
python main.py
```
2. Choose a target language from the available options:

   - fr for French

   - es for Spanish

   - hi for Hindi

3. Speak into your microphone when prompted.

4. The application will recognize your speech, translate it, and synthesize the translated text back in the chosen language.

## Dependencies

- python-dotenv

- azure-cognitiveservices-speech

- Install dependencies manually if needed:
```bash
pip install azure-cognitiveservices-speech==1.30.0 python-dotenv
```

## Contributing

Contributions are welcome! Feel free to submit issues and pull requests.

