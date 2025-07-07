# HR Chatbot Correctness Evaluation

This project evaluates the correctness of an HR chatbot's answers by comparing them to golden (reference) answers using a set of well-defined criteria. The evaluation is performed using OpenAI's GPT models via Azure OpenAI, and results are processed and analyzed in a Jupyter notebook.

## Features
- Loads HR Q&A datasets (golden, silver, incorrect facts) from Excel files.
- Connects to an HR chatbot using Direct Line API.
- Sends questions to the chatbot and retrieves responses.
- Evaluates chatbot answers using two detailed prompt templates.
- Extracts evaluation metrics and scores for further analysis.
- Categorizes questions into HR themes and subcategories.

## Project Structure
- `correctness_new_edited_hrchat.ipynb`: Main notebook for data loading, chatbot interaction, evaluation, and analysis.
- `README.md`: Project documentation (this file).
- Excel files: HR Q&A datasets (not included here, see below).

## Setup Instructions

### 1. Clone the Repository
```
git clone <your-repo-url>
cd <your-repo-directory>
```

### 2. Prepare Data Files
Place the following Excel files in the project directory:
- `New_Documents_Silver Questions & Answers.xlsx`
- `Golden_questions.xlsx`
- `No shared facts.xlsx`

### 3. Environment Setup
Create a Python virtual environment and activate it:
```
python3 -m venv venv
source venv/bin/activate
```

### 4. Install Required Packages
Install dependencies using pip:
```
pip install -r requirements.txt
```

If you do not have a `requirements.txt`, use:
```
pip install openai azure-openai python-dotenv pandas numpy selfcheckgpt asyncio
```

### 5. Environment Variables
Create a `.env` file in the project root with the following content:
```
OPENAI_API_KEY=your-azure-openai-api-key
AZURE_OPENAI_ENDPOINT=https://your-azure-endpoint.openai.azure.com/
AZURE_OPENAI_API_VERSION=2023-05-15
DIRECT_LINE_SECRET=your-direct-line-secret
BASE_URL=https://your-bot-base-url
```
Replace the values with your actual credentials and endpoints.

### 6. Running the Notebook
Open `correctness_new_edited_hrchat.ipynb` in VS Code or Jupyter Lab/Notebook and run the cells in order. Make sure your virtual environment is activated and the required packages are installed.

## Comments and Documentation
- The notebook is organized into sections with markdown explanations.
- Each code cell contains comments explaining its purpose and logic.
- Prompts and evaluation logic are documented in markdown and code comments.

## Notes
- Ensure your API keys and secrets are kept secure and **never** committed to version control.
- The evaluation logic uses GPT-4 Turbo via Azure OpenAI; ensure your account has access.
- For any issues, check the comments in the notebook for troubleshooting tips.

## License
This project is for internal evaluation and research purposes only.
