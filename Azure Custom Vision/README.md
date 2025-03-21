# Object Detection with Azure Custom Vision

## Overview
This project demonstrates how to use Azure Custom Vision to detect objects in an image using a trained model. The script loads an image, sends it to the Custom Vision API for object detection, and then visualizes the results by drawing bounding boxes around detected objects.

## Prerequisites
Before running the script, ensure you have the following:

- An Azure account with a Custom Vision project set up.
- A trained model in Azure Custom Vision.
- Python installed on your local machine.
- Required Python packages installed (see below).

## Installation

1. Clone the repository or download the script.
2. Install the required Python packages using:
   ```bash
   pip install azure-cognitiveservices-vision-customvision msrest matplotlib pillow numpy python-dotenv
   ```
3. Set up a `.env` file with the following environment variables:
   ```bash
   PredictionEndpoint="YOUR_CUSTOM_VISION_PREDICTION_ENDPOINT"
   PredictionKey="YOUR_CUSTOM_VISION_PREDICTION_KEY"
   ProjectID="YOUR_CUSTOM_VISION_PROJECT_ID"
   ModelName="YOUR_CUSTOM_VISION_MODEL_NAME"
   ```

## Usage

1. Place the image you want to process in the same directory as the script and name it `produce.jpg` (or modify the script to specify a different image file).
2. Run the script:
   ```bash
   python script.py
   ```
3. The output image with detected objects will be saved as `output.jpg` in the same directory.

## How It Works

1. Loads environment variables from `.env`.
2. Authenticates with Azure Custom Vision using API credentials.
3. Loads an image and extracts its dimensions.
4. Sends the image to Azure Custom Vision for object detection.
5. Draws bounding boxes around detected objects with a probability greater than 50%.
6. Saves the resulting image as `output.jpg`.

## Example Output
The script processes an image and outputs a new image (`output.jpg`) with detected objects highlighted.

## Troubleshooting
- Ensure your `.env` file contains the correct Azure Custom Vision credentials.
- Verify that the image file exists in the correct directory.
- If you encounter any errors, check the console output for details.
