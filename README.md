# PDF Text Extraction and Question Answering Pipeline

This Python project encompasses a streamlined pipeline for extracting text from scanned-PDF documents, structuring it, and then performing question answering tasks using state-of-the-art language models.
It integrates various libraries for PDF processing, text extraction, natural language processing (NLP), and question answering (QA). 

## Functions:

1. Converting scanned-PDF to structured-PDF
2. Chat with your PDF Using Langchain and LLM

## Features:

- PDF Processing: Utilizes the fitz library to convert PDF pages into images, which are then processed using pytesseract to extract text.

- Text Structuring: Employs the spaCy library for NLP tasks such as sentence segmentation, providing structured text output.

- PDF Output: Generates a new PDF file with structured text, maintaining the original line formatting of the source PDF document.

- Question Answering: Integrates with Hugging Face's powerful language model (LLM) via the langchain library, enabling QA tasks based on the extracted text.

- Vectorization and Retrieval: Converts the extracted text into vector representations using Hugging Face embeddings, then creates a vector store for efficient retrieval using the Chroma module.

## Usage:

1. Text Extraction: Supply a PDF document as input, and the pipeline will automatically extract text, structure it, and output a new PDF file with the structured text.

2. Question Answering: Pose questions to the pipeline, and it will utilize the pre-trained language model to provide relevant answers based on the extracted text.

## Dependencies:

- fitz: For PDF processing and image extraction.
- pytesseract: For optical character recognition (OCR) to extract text from images.
- spaCy: For natural language processing tasks such as sentence segmentation.
- FPDF: For creating PDF files with structured text output.
- langchain: For integrating with Hugging Face's language model and vectorization tasks.
- HuggingFaceTransformers: For utilizing pre-trained language models from Hugging Face's model hub.
- NOTE that you need to get an Access Tokens from [Huggingface](https://huggingface.co/) and save it in the root folder of your notebook in ".env" file.

## Future Improvements:

- Error Handling: Enhance error handling mechanisms to gracefully handle edge cases and errors during PDF processing and QA tasks.
- Performance Optimization: Optimize the pipeline for efficiency, especially when dealing with large PDF documents and complex QA queries.
- Expand QA Capabilities: Extend question answering capabilities by fine-tuning the language model on domain-specific data or incorporating multi-step reasoning.

## Contributions:

Contributions to this project, whether in the form of bug fixes, enhancements, or new features, are highly encouraged and appreciated. Feel free to submit pull requests or open issues on the project's repository.

## Acknowledgments:

This project builds upon the efforts of various open-source libraries, without which it would not have been possible. Special thanks to the developers of spaCy, pytesseract, langchain, and other dependencies.
