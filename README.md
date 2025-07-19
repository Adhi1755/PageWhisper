# PageWhisper: Local Document Q\&A with LLaMA3

-----

PageWhisper is a powerful Jupyter Notebook-based application that allows you to chat with your PDF documents locally. Simply upload a PDF, ask questions, and get in-depth, human-like answers directly from the content of your document, powered by a local LLaMA3 model.

## Key Features

  * **PDF Content Extraction:** Seamlessly extracts text from your uploaded PDF files.
  * **Intelligent Text Chunking:** Employs recursive splitting to break down document content into clean, meaningful chunks, ensuring context preservation.
  * **Local Embeddings:** Generates vector embeddings for text chunks using the efficient `all-MiniLM-L6-v2` SentenceTransformer model, all processed on your local machine.
  * **FAISS-Powered Retrieval:** Utilizes **FAISS (Facebook AI Similarity Search)** for rapid storage, indexing, and retrieval of relevant document chunks, ensuring fast and accurate information access.
  * **Local LLaMA3 Integration:** Leverages a **local LLaMA3 model** via **Ollama** to generate high-quality, in-depth answers strictly based on the content of your uploaded document.
  * **Interactive Jupyter UI:** Provides a user-friendly interface built with `ipywidgets` for easy PDF uploads, query input, real-time status updates, and clear display of answers.
  * **Privacy-Focused:** All processing, from embedding to answer generation, happens locally on your machine, ensuring your document data remains private and secure.

-----

## Technologies Used

  * **Jupyter Notebook:** The primary development and execution environment.
  * **PyPDF (fitz):** For efficient PDF text extraction.
  * **LangChain (text\_splitter):** For intelligent recursive text splitting.
  * **SentenceTransformers:** To generate robust text embeddings (`all-MiniLM-L6-v2`).
  * **FAISS:** For high-performance similarity search and indexing of embeddings.
  * **Ollama:** To run the LLaMA3 large language model locally.
  * **LLaMA3:** The powerful large language model used for generating answers.
  * **ipywidgets:** For building the interactive user interface within Jupyter.

-----

## Setup Instructions

Follow these steps to get PageWhisper up and running on your local machine.

### 1\. Clone the Repository

First, clone the PageWhisper repository to your local machine:

```bash
git clone https://github.com/your-username/PageWhisper.git
cd PageWhisper
```

### 2\. Create a Conda Environment (Recommended)

It's highly recommended to use a Conda environment to manage dependencies:

```bash
conda create -n pagewhisper python=3.9
conda activate pagewhisper
```

### 3\. Install Python Dependencies

Install the required Python packages:

```bash
pip install -r requirements.txt
```

### 4\. Set up Ollama and LLaMA3

PageWhisper relies on Ollama to run the LLaMA3 model locally.

#### a. Install Ollama

Download and install Ollama from the official website: [ollama.com/download](https://ollama.com/download). Follow the instructions for your operating system.

#### b. Pull the LLaMA3 Model

Once Ollama is installed, open your terminal or command prompt and pull the LLaMA3 model:

```bash
ollama pull llama3
```

This command will download the LLaMA3 model to your local Ollama instance. This might take some time depending on your internet connection.

### 5\. Start Jupyter Notebook

Navigate to your PageWhisper project directory (if you're not already there) and start Jupyter Notebook:

```bash
jupyter notebook
```

This will open Jupyter in your web browser.

-----

## Usage Instructions

Once Jupyter Notebook is running, follow these steps to use PageWhisper:

### 1\. Open the Notebook

In the Jupyter interface, open the `PageWhisper - RAG (Retrieval-Augmented Generation).jpynb` notebook.

### 2\. Run All Cells

Execute all cells in the notebook. You can do this by selecting `Cell` \> `Run All` from the Jupyter menu.

### 3\. Upload Your PDF

You will see an "Upload PDF" widget. Click the **"Choose Files"** button and select the PDF document you wish to query.

<p align="center"\>
<img src="assets/UI.png" alt="PDF Upload Widget">
<br\>
<em\>Screenshot Placeholder: The PDF upload widget.\</em\>
</p\>

### 4\. Wait for Processing

After uploading, the notebook will display status updates as it processes the PDF (extracting text, chunking, and embedding). This may take a few moments depending on the size of your document.

\<p align="center"\>
\<img src="[https://via.placeholder.com/600x300?text=Screenshot:+Processing+Status](https://www.google.com/search?q=https://via.placeholder.com/600x300%3Ftext%3DScreenshot:%2BProcessing%2BStatus)" alt="Processing Status Placeholder"\>
\<br\>
\<em\>Screenshot Placeholder: Real-time processing status updates.\</em\>
\</p\>

### 5\. Enter Your Query

Once processing is complete, a "Enter your query:" input box will appear. Type your question related to the uploaded document.

\<p align="center"\>
\<img src="[https://via.placeholder.com/600x300?text=Screenshot:+Query+Input](https://www.google.com/search?q=https://via.placeholder.com/600x300%3Ftext%3DScreenshot:%2BQuery%2BInput)" alt="Query Input Placeholder"\>
\<br\>
\<em\>Screenshot Placeholder: The query input box.\</em\>
\</p\>

### 6\. Get Your Answer

Press Enter or click the "Ask" button (if implemented). The PageWhisper application will retrieve relevant information from your document and use the local LLaMA3 model to generate a comprehensive answer, which will be displayed below.

\<p align="center"\>
\<img src="[https://via.placeholder.com/800x400?text=Screenshot:+Answer+Display](https://www.google.com/search?q=https://via.placeholder.com/800x400%3Ftext%3DScreenshot:%2BAnswer%2BDisplay)" alt="Answer Display Placeholder"\>
\<br\>
\<em\>Screenshot Placeholder: The generated answer displayed.\</em\>
\</p\>

-----

## Example Use Case

Imagine you have a lengthy research paper on **Artificial Intelligence ethics**. You can upload this PDF to PageWhisper.

**Query:** "What are the main ethical concerns regarding AI bias mentioned in this paper?"

PageWhisper will then leverage the local LLaMA3 model to analyze the relevant sections of your uploaded paper and provide a detailed answer, summarizing the specific ethical concerns about AI bias discussed within that document, without needing to access any external information.

-----

## License

This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.
