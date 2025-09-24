# AI-Powered-Meeting-Assistant
Upload audio files to get AI-generated key points using Whisper transcription + IBM Watson Llama 3.2 summarization.
Built as part of an IBM Skills Network course demonstrating enterprise AI integration with Watson ML services.

Quick Setup
1. Install Dependencies
    bashpip install torch gradio langchain transformers ibm-watson-machine-learning

3. Configure IBM Watson
    Get your API key and project ID from IBM Cloud Watson ML, then update the code:
    pythonmy_credentials = {
    "url": "https://us-south.ml.cloud.ibm.com",
    "apikey": "your_api_key_here"
}

# Replace "skills-network" with your project ID
    project_id="your_project_id_here"

3. Run the App
    bashpython app.py
    Visit http://localhost:7860 to upload audio files and get key points.

How It Works
    Upload audio file (WAV, MP3, etc.)
    Whisper converts speech to text
    Llama 3.2 extracts key points
    Results displayed in web interface

Troubleshooting
    Import errors: Install missing packages with pip
    Watson errors: Check API key and project ID
    GPU issues: Add --index-url https://download.pytorch.org/whl/cpu to pip install torch
