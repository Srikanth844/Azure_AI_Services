# Azure AI Text Classification using Custom Document Classification 

## Overview

This project demonstrates how to use Azure AI's **Custom Document Classification** to classify text files based on predefined categories. It utilizes the **Azure AI Text Analytics API** and requires proper authentication via Azure credentials.

## Features

- Reads multiple text files from a directory (`articles`).
- Uses Azure AI's `TextAnalyticsClient` for document classification.
- Implements single-label classification with high confidence scores.
- Retrieves classification results and handles errors gracefully.

## Prerequisites

Before running this project, ensure you have:

1. An **Azure AI Services** account with **Custom Document Classification** enabled.
2. API credentials (`AI_SERVICE_ENDPOINT` and `AI_SERVICE_KEY`).
3. Python 3.x installed on your system.
4. Required dependencies installed (see [Installation](#installation)).

## Installation

Clone the repository and install dependencies:

```sh
git clone <repository-url>
cd <repository-folder>
pip install -r requirements.txt
```

Create a `.env` file in the project root and add the following environment variables:

```ini
AI_SERVICE_ENDPOINT=<your-ai-service-endpoint>
AI_SERVICE_KEY=<your-ai-service-key>
PROJECT=<your-project-name>
DEPLOYMENT=<your-deployment-name>
```

## Usage

Run the script to classify text documents:

```sh
python classify-text.py
```

## Folder Structure

```
|-- articles/             # Folder containing text files to classify
|-- classify-text.py               # Main script for classification
|-- .env                  # Environment variables file
|-- README.md             # Project documentation
```

## Output

After execution, the script prints classification results:

```
document1.txt was classified as 'Technology' with confidence score 0.95.
document2.txt was classified as 'Healthcare' with confidence score 0.89.
document3.txt has an error with code 'InvalidDocument' and message 'Document too short.'
```

## Error Handling

- If a document cannot be classified, the script will print the error message.
- Ensure your text files are formatted properly to improve classification accuracy.
