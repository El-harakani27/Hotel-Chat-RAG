# Hotel-Chat-RAG

A conversational AI chatbot for answering questions about "The Grand Horizon Hotel" using Retrieval-Augmented Generation (RAG) and chat history awareness. Powered by LangChain, Streamlit, and Groq API, this project demonstrates how to build an intelligent assistant capable of context-aware, document-grounded Q&A for hotel information.

## Features

- **Conversational Chatbot**: Remembers chat history for more contextually accurate answers.
- **Retrieval-Augmented Generation (RAG)**: Answers are grounded in real hotel data from a PDF.
- **Multiple LLM Support**: Select from models such as deepseek, llama, and qwen (via Groq API).
- **Session Management**: Supports multiple chat sessions, each with its own history.
- **User-Friendly UI**: Streamlit-based web interface for easy interaction.

## Technologies Used

- **Python**
- **Streamlit**: For building the interactive web app.
- **LangChain**: For chaining LLMs and retrieval operations.
- **Groq API**: For accessing supported language models.
- **PyPDFLoader**: For loading hotel info from PDF.
- **Chroma**: For vector storage and retrieval.
- **HuggingFaceEmbeddings**: Embedding model for document chunks.
- **dotenv**: For managing API keys and secrets.

## Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/El-harakani27/Hotel-Chat-RAG.git
   cd Hotel-Chat-RAG
   ```

2. **Install dependencies:**
   Make sure you have Python 3.8+ and pip installed. Then run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Prepare environment variables:**
   - Create a `.env` file in the root directory.
   - Add your HuggingFace token (`HF_TOKEN`) and Groq API key:
     ```
     HF_TOKEN=your_huggingface_token
     GROQ_API=your_groq_api_key
     ```

4. **Place hotel info PDF:**
   - Ensure `hotelinfo.pdf` is in the root directory. This file should contain all reference information about the hotel.

5. **Run the application:**
   ```bash
   streamlit run main.py
   ```

6. **Interact:**
   - Open the web interface.
   - Enter your Groq API key and select a model.
   - Start chatting! The bot will answer based on hotel information from the PDF and maintain context across the conversation.

## Usage

- Ask any question related to "The Grand Horizon Hotel" (e.g., amenities, location, policies).
- The chatbot uses retrieval-augmented generation to provide answers grounded in the uploaded PDF.
- You can select different LLMs and manage chat sessions via the sidebar.

## Notes

- The app only answers questions related to "The Grand Horizon Hotel."
- If the answer is not found in the document, the bot will say it doesn't know.
- All sensitive tokens/keys should be kept secure and never shared publicly.

## License

*No license specified. Please add a license if you plan to distribute or use this code.*

## Author

[El-harakani27](https://github.com/El-harakani27)
