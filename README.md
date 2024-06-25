# NexHire

NexHire is an intelligent HR resume screening assistant that utilizes advanced natural language processing (NLP) techniques to streamline the recruitment process. It uses Pinecone for vector storage and retrieval, LangChain for language model operations, and various libraries for document processing and summarization. It converts resumes into embeddings with SentenceTransformer, storing them in Pinecone for efficient similarity searches, enabling quick identification of the most relevant candidates. NexHire also provides intelligent summarization of resumes, giving concise overviews of candidate qualifications and experience. Built with Streamlit, it offers an intuitive interface for easy interaction, enhancing the recruitment process for HR professionals.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Features

- Extracts text from PDF resumes.
- Converts text to embeddings using `SentenceTransformer`.
- Uses Pinecone to store and retrieve vectors.
- Finds similar documents based on input queries.
- Summarizes the content of resumes.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/NexHire.git
    cd NexHire
    ```

2. **Create a virtual environment and activate it**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install the required packages**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Set up environment variables**:
    - Create a `.env` file in the root directory of the project.
    - Add your Pinecone API key:
        ```env
        PINECONE_API_KEY=your_pinecone_api_key
        ```

## Usage

1. **Upload the documents**:
    - Place your PDF files in a directory.

2. **Run the Streamlit application**:
    ```bash
    streamlit run app.py
    ```

3. **Interact with the application**:
    - Upload your PDF files.
    - Enter a query to find similar documents.
    - View summaries of the documents.

## Project Structure

NexHire/

├── app.py # Entry point for the Streamlit application 

├── constants.py # Constant values used in the project (not included in the repo, create your own) 

├── requirements.txt # List of required Python packages 

├── utils.py # Utility functions for PDF extraction, embeddings, and Pinecone operations 

├── .env # Environment variables (not included in the repo, create your own) 

└── ...


### app.py

The main script that runs the Streamlit application. It initializes the application and handles user interactions.

### constants.py

Contains constant values used throughout the project, such as the Pinecone environment and index names.

### utils.py

Includes utility functions for:
- Extracting text from PDF files.
- Creating embeddings.
- Pushing data to Pinecone.
- Retrieving data from Pinecone.
- Performing similarity searches.
- Summarizing documents.

## Contributing

Contributions to NexHire are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch with your feature or bugfix.
3. Make your changes.
4. Submit a pull request with a detailed description of your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


