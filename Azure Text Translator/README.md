# Azure Text Translation Python Application

This is a Python application that leverages the Azure AI Translation Service to translate text input from the user into a target language. It interacts with the Azure Translator API to detect supported languages and perform text translation.

## Prerequisites

Before you can run this application, make sure you have the following:

- Python 3.x installed on your machine.
- Azure subscription with access to the Translator resource.
- `.env` file containing your Azure Translator credentials.

## Installation

1. Clone this repository to your local machine.

    ```bash
    git clone https://github.com/your-repo-name/azure-text-translation.git
    cd azure-text-translation
    ```

2. Install the required Python dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Set up the `.env` file in the project root directory with your Azure Translator credentials:

    ```bash
    TRANSLATOR_KEY=your-translator-key
    TRANSLATOR_REGION=your-translator-region
    ```

    Replace `your-translator-key` and `your-translator-region` with your actual Azure Translator API key and region.

## Dependencies

This project requires the following Python libraries:

- `azure-ai-translation-text==1.0.0b1`
- `python-dotenv`

To install the dependencies, you can run:

```bash
pip install azure-ai-translation-text==1.0.0b1 python-dotenv

```

# Usage
1.Run the application:
```bash
python translate.py
```
2. The application will:

- Load your Azure Translator API key and region from the .env file.
- Fetch and list supported translation languages.
- Prompt you to enter a target language code (e.g., en for English, fr for French).
- Ask for input text that you want to translate.
- Translate the text and display the translation.
- Repeat the translation until you type "quit" to exit.

# Example:
```bash
Enter a target language code for translation (for example, 'en'):
es
Enter text to translate ('quit' to exit): Hello, how are you?
'Hello, how are you?' was translated from en to es as 'Hola, ¿cómo estás?'
Enter text to translate ('quit' to exit): quit
```