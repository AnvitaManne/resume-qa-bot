# Resume-Based QA Bot

This chatbot allows you to upload a resume in PDF format and ask questions based on the extracted information. It uses AI to extract and structure resume data, and then uses this data to answer your questions in a conversational manner.

## Features
- **Accepts PDF resumes**: Upload a resume in PDF format for analysis.
- **Text Extraction**: The bot extracts text from the uploaded PDF using tools like `pdfplumber` or `PyMuPDF`.
- **Data Processing**: The extracted text is split into small chunks (such as paragraphs or sections).
- **Embedding and Vector Database**: These text chunks are then embedded using a semantic model (e.g., Hugging Face models) and stored in a vector database (e.g., FAISS or Chroma).
- **Question-Answering**: Ask any question related to the resume. The system retrieves the most relevant information from the vector database and generates an accurate answer.

## How It Works
1. **Input a PDF Resume**: The user uploads a resume in PDF format.
2. **Extract Text**: The bot uses `pdfplumber` or other tools like `PyMuPDF` to extract the text from the PDF.
3. **Split Text into Chunks**: The extracted text is split into smaller chunks (such as paragraphs or sections) for better analysis.
4. **Embed Text Chunks**: The text chunks are embedded using an embedding model like Hugging Face's "sentence-transformers/all-MiniLM-L6-v2".
5. **Store in Vector Database**: The embeddings are stored in a vector database like **FAISS** or **Chroma**.
6. **Ask Questions**: Once the resume data is stored, you can ask questions like:
   - "What skills does this person have?"
   - "What are some of the projects they’ve worked on?"
7. **Retrieve and Answer**: The bot converts your question into an embedding, retrieves the most relevant resume chunks from the database, and generates an answer based on those chunks.

## Setup

### Requirements
- Python 3.7 or higher
- Required Python libraries (listed below)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/resume-qa-bot.git
   ```

2. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

### Usage

1. Provide a resume in PDF format.
2. Ask any question related to the resume (e.g., "What are their skills?").
3. Get a detailed answer based on the information extracted from the resume.


## Dependencies

* `pdfplumber` or `PyMuPDF` for extracting text from PDFs.
* `pydantic` for structured data modeling.
* `langchain` for working with embeddings, vector databases (like FAISS or Chroma), and semantic models.
* Hugging Face models for text embeddings (e.g., "sentence-transformers/all-MiniLM-L6-v2").
* Vector database (FAISS or Chroma) to store and retrieve embeddings.


## License

This project is open-source and available under the MIT License.


### Key Additions:
- **Text Extraction**: Detailed how the text is extracted from PDFs using `pdfplumber` or `PyMuPDF`.
- **Data Splitting**: Mentioned how the text is split into chunks for better processing.
- **Embedding**: Explained how embeddings are generated using models like Hugging Face's `sentence-transformers/all-MiniLM-L6-v2`.
- **Vector Database**: Described how the embeddings are stored in a vector database like **FAISS** or **Chroma**.
- **Question-Answering Process**: Clear steps on how the question-answering process works, including converting the question into embeddings and retrieving relevant resume sections to answer the query.

## Author

Anvita Manne
