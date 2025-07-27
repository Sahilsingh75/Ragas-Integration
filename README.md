# RAGAs-Based Evaluation of LLM Responses

This project uses [RAGAs (Retrieval-Augmented Generation Assessment)](https://github.com/explodinggradients/ragas) to evaluate the quality of LLM-generated answers using three key metrics:

- **Faithfulness** — is the answer factually grounded in the context?
- **Answer Relevancy** — does the answer directly address the user's question?
- **Context Precision** — is the provided context relevant to the question?

---

## Project Structure

ragas-evaluation/
├── logs.json # Raw input dataset for evaluation
├── ragas_output.json # Final RAGAs scores (JSON format)
├── ragas_output.csv # Same scores in spreadsheet format
├── ragas_eval.ipynb # Jupyter notebook with full pipeline
├── evaluation_report.docx # Summary report of evaluation
└── README.md


---

## How to Run Locally

1. **Clone the Repository** (or download files manually):

   ```
   git clone https://github.com/Sahilsingh75/Ragas-Integration.git
   cd Ragas-Integration
   ```

2. **Install dependencies**:
  ```
  pip install ragas[openai] datasets pandas
  ```

3. **Set your OpenAI API key**:
  ```
  set OPENAI_API_KEY=your_openai_key_here     # Windows
  export OPENAI_API_KEY=your_openai_key_here  # macOS/Linux
  ```

4. **Run the notebook or script**:

  Open ragas_integration.ipynb and execute all cells, or run the script version.

## Metrics Example
ID	Faithfulness	Answer Relevancy	Context Precision
abc123	0.82	0.94	1.0
def456	0.23	0.87	0.95

## Observations
-Faithfulness was lower on some examples due to hallucinated content.
-Context Precision remained high, indicating relevant context was consistently retrieved.
-Answer Relevancy averaged above 0.8, showing good alignment with questions.

## License
This project is for research/demo purposes only. OpenAI and RAGAs are trademarks of their respective owners.
