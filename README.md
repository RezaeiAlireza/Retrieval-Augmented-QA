# Document-based Question Answering Pipeline with LangChain and HuggingFace

This Python project implements a document processing pipeline that extracts text from scanned PDF documents, structures it, and enables question answering (QA) based on the extracted content. The pipeline integrates powerful libraries and models, including LangChain, HuggingFace, spaCy, and more.

## Features:

#### PDF Processing:

- Converts scanned PDF pages into images using the fitz library (PyMuPDF).
- Applies OCR with pytesseract to extract text from the images.

#### Text Structuring:

- Uses the spaCy library to process the extracted text and segment it into sentences.
- Outputs structured, organized text for further use.

#### PDF Output:

- Generates a new PDF file with the structured text, preserving the original layout and formatting from the source PDF.

#### Question Answering (QA):

- Integrates with Hugging Face's language model (LLM) via the LangChain library, enabling natural language question answering based on the structured text.

#### Embedding and Retrieval:

- Converts the extracted text into vector embeddings using HuggingFace's embeddings model.
- Creates a Chroma vector store to efficiently retrieve relevant information from the extracted text for QA tasks.

## Usage:
1. Text Extraction:
- Provide a scanned PDF document as input.
- The pipeline will automatically extract text, structure it, and output a new PDF with the structured text.
2. Question Answering:
- Pose questions to the system based on the extracted text.
- The pipeline leverages a pre-trained HuggingFace language model (fine-tuned for question answering) to provide relevant answers.

## Dependencies:

The following Python libraries are used in this project:

- fitz: For PDF processing and converting pages to images.
- pytesseract: For Optical Character Recognition (OCR) to extract text from images.
- spaCy: For text processing tasks like sentence segmentation and structuring.
- FPDF: For generating PDF files from structured text.
- langchain: For integrating HuggingFace's pre-trained language models and embedding-based tasks.
- HuggingFaceTransformers: For working with HuggingFace models and transformers.
- Chroma: For storing and retrieving vector embeddings for efficient document search.

### Important:

Ensure that you have a valid HuggingFace API token. This token must be set as an environment variable (TKN) for using the language model and embeddings.

## Installation:

To set up the project, clone the repository and install the required dependencies:

```bash
git clone https://github.com/RezaeiAlireza/Retrieval-Augmented-QA.git
cd Retrieval-Augmented-QA
pip install -r requirements.txt
```

You will also need to install Tesseract for OCR functionality. Instructions for installation can be found in the Tesseract documentation.

## Example Workflow:

1. Text Extraction:

- Input a PDF file to extract and structure text.
- The output is a new PDF file with structured text.

2. Question Answering:

- After text extraction, interact with the system by asking questions based on the PDF content.
- The system uses retrieval-augmented generation (RAG) to fetch relevant chunks of text and provide precise answers.

## Future Improvements:

- Error Handling: Enhance error handling to manage edge cases during PDF processing and QA.
- Performance Optimization: Speed up the pipeline, especially for large PDFs and complex queries.

## Contributing:

Contributions are welcome! You can contribute by:

- Reporting issues or bugs.
- Submitting pull requests for bug fixes or feature enhancements.
- Providing suggestions to improve performance or features.

Feel free to open issues or submit pull requests via the GitHub repository.

## Acknowledgments:

This project uses several powerful open-source libraries and models:

- spaCy: For text processing.
- pytesseract: For OCR-based text extraction.
- LangChain: For creating a pipeline with HuggingFace models.
- HuggingFace: For language models and embeddings.

We acknowledge the efforts of all the contributors to these libraries.
