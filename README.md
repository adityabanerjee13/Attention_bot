# RAG-Powered Chatbot

## Overview
This repository contains a Retrieval-Augmented Generation (RAG) chatbot that leverages the Phoenix integration for tracing, monitoring, and annotation of responses.

The chat-bot is a specialist in all the attention mechanism and transformer related topic so feel free to ask anything.

For the RAG pipeline I have used the Hyde-RAG which improves the retrival quality. I generate a document using the user query and use that document to retrive from my vector-db. This gives decent retrivals from the RAG with small coherency, this pipeline can be improved by increasing the size of the vector-db.

---

## Setup Instructions

### Prerequisites
Ensure you have the following installed:
Install all dependencies usinf environment.yml file. Create a new env using instruction 
'''bash
conda IISC_aditya_env create -f environment.yml
'''

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/rag-chatbot.git
   cd rag-chatbot
   ```
2. Create and activate a conda environment (optional but recommended):
   ```bash
   conda IISC_aditya_env create -f environment.yml 
   ```
3. Set up environment variables:
   ```bash
   export OPENAI_API_KEY="your_api_key"
   export PHOENIX_API_KEY="your_phoenix_key"
   ```
   *(Use `set` instead of `export` on Windows)*

---

## Phoenix Integration Summary

Phoenix is used for:
- **Tracing**: Logs interactions between the chatbot and the retrieval model.
- **Monitoring**: Tracks the chatbot's performance and response quality.
- **Annotation**: Allows manual review and correction of chatbot responses for model improvement.

Integration with Phoenix is handled via:
- API calls within the chatbot backend.
- Automatic logging of conversations and retrievals.
- A dashboard for reviewing chatbot performance.

---

## Running the Chatbot

### Start the Chatbot
Run the chatbot in jupyter notebook: RAG_chatbot.ipynb

This will launch a local server where you can interact with the chatbot.


To export conversation traces for analysis:

This will save the chat logs in JSON format for further analysis.


### Annotate Responses
To annotate responses using Phoenix using instructions:
1. To load conversation span it can be done automatically using code in the section Load traces.
2. The chat can be saved in a json file with timestamps.

To annotate responses using Phoenix manually:
1. Or Navigate to the Phoenix dashboard.
2. Select the relevant conversation logs.

---

## License
This project is licensed under the MIT License. See `LICENSE` for details.

