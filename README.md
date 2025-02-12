# Cold Mail Generator

## Overview
Cold Mail Generator is a Streamlit-based web application that automates the process of extracting job postings from career pages and generating personalized cold emails for job applications. The application leverages Llama 3.3 through Groq, LangChain and integrates with ChromaDB for portfolio link retrieval.

## Architecture Diagram

![image](https://github.com/user-attachments/assets/db546f30-5964-47a5-a622-af8ed26a3c6e)


## Features
- **Job Extraction**: Parses job postings from company career pages.
- **Portfolio Integration**: Matches relevant portfolio links to job descriptions.
- **Cold Email Generation**: Generates tailored cold emails based on job descriptions and portfolio links.
- **Streamlit UI**: Provides an interactive web interface for easy usage.

## Technologies Used
- **Python**
- **LangChain** (LLMs and prompt templates)
- **Streamlit** (Web application UI)
- **ChromaDB** (Vector database for portfolio retrieval)
- **Pandas** (Data processing)
- **Regular Expressions (re)** (Text cleaning)

## Installation

### Prerequisites
- Python 3.8+
- `pip` package manager
- Groq API key

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/shaadclt/Cold-Email-Generator-Using-Job-URL.git
   cd Cold-Email-Generator-Using-Job-URL
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Set up environment variables:
   Create a `.env` file and add your Groq API key:
   ```sh
   GROQ_API_KEY=your_api_key_here
   ```
4. Run the Streamlit app:
   ```sh
   streamlit run main.py
   ```

## Project Structure
```
├── chain.py          # LangChain logic for job extraction & email generation
├── portfolio.py      # ChromaDB integration for portfolio retrieval
├── utils.py          # Text cleaning utilities
├── main.py            # Streamlit app
├── requirements.txt  # Required dependencies
├── .env.example      # Environment variable example file
├── README.md         # Project documentation
├── LICENSE.txt       # MIT License
├── vectorstore/  # Persistent ChromaDB storage
└── resource/
    ├── portfolio.csv # Portfolio data
    
```

## Usage
1. Open the app in your browser after running the Streamlit command.
2. Enter the job post URL in the input field and click "Submit".
3. The app will scrape the job page, extract job details, and retrieve relevant portfolio links.
4. A personalized cold email will be displayed, ready for use.

## Contributing
Feel free to fork this repository and contribute by submitting pull requests.

## License
This project is licensed under the [MIT License](LICENSE).

