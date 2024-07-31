### README.md

# Crime and Punishment Summary

## Overview
This project involves generating a concise 20-page summary of the book "Crime and Punishment" using advanced natural language processing techniques and the LangChain library.

## How the Summarizer Works

1. **Install Dependencies**:
   - Install required libraries using `pip install` for handling PDF files, generating AI responses, and creating PDF summaries.

2. **Load Environment Variables and Initialize LLM**:
   - Load environment variables and initialize the Google Generative AI model with specified parameters for text generation.

3. **Load the Book**:
   - Use the `PyPDFLoader` to read and load the entire "Crime and Punishment" book in PDF format.

4. **Split the Text into Chunks**:
   - Utilize `RecursiveCharacterTextSplitter` to split the book's text into manageable chunks for easier processing and summarization.

5. **Create Embeddings for Text Chunks**:
   - Generate embeddings for each text chunk using `GoogleGenerativeAIEmbeddings` to facilitate clustering and summarization.

6. **Cluster Text Chunks**:
   - Perform K-means clustering on the text embeddings to group similar chunks together.

7. **Generate Summaries for Each Cluster**:
   - Create detailed summaries for each cluster using the Google Generative AI model and `load_summarize_chain`.

8. **Combine Summaries into a Single Document**:
   - Merge individual summaries into a single comprehensive summary document.

9. **Create a PDF of the Final Summary**:
   - Convert the final summary text into a PDF format using `FPDF`.

## How to Run

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/yourusername/crime-and-punishment-summary.git
   cd crime-and-punishment-summary
   ```

2. **Install Dependencies**:
   ```sh
   pip install -r requirements.txt
   ```

3. **Run the Script**:
   - Ensure you have the book PDF file in the specified path.
   - Execute the summarization script to generate the summary and PDF.

## Dependencies
- `python-dotenv`
- `langchain`
- `langchain-google-genai`
- `pypdf`
- `fpdf`

## Output
- The final summary will be saved as `Crime_and_Punishment_Summary.pdf`.