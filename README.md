# RAG Vision using VLM and LLM

This notebook demonstrates a functional pipeline for building a Retrieval-Augmented Generation (RAG) system with image and text processing capabilities using local llama3.2 and llama3.2 vision model. It extracts content from PDFs, processes images, creates vector stores, and allows for context-based query answering.

## Features

- **PDF Content Extraction:**
  - Extracts text and images from PDFs.
  - Processes images using a vision-language model to generate detailed descriptions.

- **Image Description Generation:**
  - Generates structured and content-focused descriptions for images using a language model.

- **Text and Image Integration:**
  - Combines text and image descriptions for enhanced content representation.

- **Vector Store Creation:**
  - Uses FAISS for creating vector stores based on processed PDF content.
  - Employs embeddings and text-splitting utilities for document chunking.

- **Contextual Query Answering:**
  - Retrieves relevant context from the vector store for answering user queries.
  - Integrates with a language model to generate responses based on retrieved context.

## Workflow

1. **PDF Processing:**
   - Extracts images and text from PDF files.
   - Describes images using a specified vision-language model.

2. **Vector Store Construction:**
   - Splits text into manageable chunks with metadata (e.g., page numbers).
   - Builds a FAISS vector store using text embeddings.

3. **Query Handling:**
   - Retrieves top-k similar documents for a user query.
   - Generates a context-aware response by combining retrieved content with the query.

## Key Functions

### PDF Content Extraction
- `extract_images_from_pdf`: Extracts and saves images from a PDF.
- `describe_image`: Generates descriptions for images using a vision-language model.
- `extract_pdf_content`: Integrates text extraction and image description for structured output.

### Vector Store Management
- `create_vector_store`: Creates a FAISS vector store from extracted content.
- `retrieve_context`: Retrieves relevant documents from the vector store based on a query.

### Response Generation
- Combines retrieved content and queries for generating detailed, context-aware answers.

## Usage

1. **Setup Environment:**
   - Install required libraries: `langchain`, `PyMuPDF`, `FAISS`, and a compatible vision-language model API.

2. **Prepare Data:**
   - Provide a PDF file for content extraction.

3. **Run the Pipeline:**
   - Execute the notebook to process the PDF, build the vector store, and handle queries.

4. **Query the System:**
   - Input questions related to the PDF content for contextual responses.

## Example Query

- **Query:** "Block diagram of project architecture"
- **Response:** Detailed explanation of the project architecture with relevant diagrams and descriptions.

## Dependencies

- Python 3.7+
- Libraries: `langchain`, `PyMuPDF`, `FAISS`, `Pillow`, `re`

## Acknowledgments

This notebook integrates advanced PDF and image processing techniques with retrieval-augmented generation to provide a seamless way to explore document content.
