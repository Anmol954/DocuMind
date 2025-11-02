# 📚 DocuMind - Document-based Question Answering System

An intelligent document query system powered by LangChain and OpenAI that allows users to upload text documents and ask questions about their content. The system uses advanced RAG (Retrieval-Augmented Generation) techniques to provide accurate, context-based answers.

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/streamlit-latest-red.svg)
![LangChain](https://img.shields.io/badge/langchain-latest-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🌟 Features

- **📄 Document Upload**: Upload any text file (.txt) for analysis
- **🤖 AI-Powered Q&A**: Ask natural language questions about your documents
- **🔍 Smart Retrieval**: Uses FAISS vector store for efficient similarity search
- **💡 Context-Aware Answers**: Leverages GPT-4 to provide accurate, context-based responses
- **⚡ Real-time Processing**: Get instant answers to your queries
- **🎯 Semantic Understanding**: Advanced text chunking and embedding techniques

## 🛠️ Technology Stack

- **Frontend**: Streamlit
- **AI/ML Framework**: LangChain
- **LLM**: OpenAI GPT-4
- **Vector Store**: FAISS (Facebook AI Similarity Search)
- **Embeddings**: OpenAI Embeddings
- **Text Processing**: RecursiveCharacterTextSplitter

## 📋 Prerequisites

- Python 3.8 or higher
- OpenAI API key
- pip package manager

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Anmol954/DocuMind.git
   cd DocuMind
   ```

2. **Install required packages**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory and add your OpenAI API key:
   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   ```

## 💻 Usage

1. **Run the application**
   ```bash
   streamlit run document_query_app.py
   ```

2. **Upload a document**
   - Click on "Choose a text file" button
   - Select a `.txt` file from your computer
   - Sample documents are provided in the `Data/` folder

3. **Ask questions**
   - Enter your question in the text input field
   - Click "Get Answer" button
   - Receive AI-generated answers based on your document

## 📁 Project Structure

```
Document-based-Question-Answering-System/
│
├── document_query_app.py   # Main application file
├── requirements.txt         # Python dependencies
├── README.md               # Project documentation
├── .env                    # Environment variables (create this)
│
└── Data/                   # Sample documents
    ├── climate.txt         # Sample: Climate change information
    └── cvd.txt            # Sample: Cardiovascular disease information
```

## 🎯 How It Works

1. **Document Processing**
   - The uploaded document is split into smaller chunks (500 characters with 100 overlap)
   - Each chunk is converted into embeddings using OpenAI's embedding model

2. **Vector Storage**
   - Document embeddings are stored in a FAISS vector database
   - Enables fast similarity search for relevant context

3. **Query Processing**
   - User query is processed and similar document chunks are retrieved
   - Top 3 most relevant chunks are selected

4. **Answer Generation**
   - Retrieved context is passed to GPT-4
   - The model generates an accurate answer based solely on the provided context

## 📝 Example Use Cases

- **Research**: Quickly extract information from research papers
- **Education**: Get answers from textbooks and study materials
- **Business**: Query company documents and reports
- **Healthcare**: Extract information from medical documents (see `cvd.txt` example)
- **Environmental Studies**: Learn from climate and environmental documents (see `climate.txt` example)

## 🔧 Configuration

The system uses the following default parameters (can be modified in `document_query_app.py`):

- **Chunk Size**: 500 characters
- **Chunk Overlap**: 100 characters
- **LLM Model**: GPT-4
- **Top K Results**: 3 most similar chunks

## ⚠️ Important Notes

- Ensure your `.env` file contains a valid OpenAI API key
- The system currently supports only `.txt` files
- API usage may incur costs based on OpenAI's pricing
- Answers are generated based solely on the uploaded document content

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author

**Anmol954**

- GitHub: [@Anmol954](https://github.com/Anmol954)

## 🙏 Acknowledgments

- OpenAI for GPT-4 and embedding models
- LangChain for the excellent framework
- Streamlit for the user-friendly interface
- FAISS for efficient vector similarity search

## 📞 Support

If you have any questions or run into issues, please open an issue on GitHub.

---

**Made with ❤️ using LangChain and OpenAI**