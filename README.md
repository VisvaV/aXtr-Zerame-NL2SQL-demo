# NL2SQL with LangChain & SQLite Demo

---
## What This Does

This notebook takes a natural language question like:

> "List the product names in Classic Cars"

...and automatically generates an appropriate SQL query, runs it on a local SQLite database, and returns the result.

It also supports:

- Few-shot examples to improve accuracy.
- Dynamic selection of relevant tables based on the question.
- A memory system to handle follow-up questions.
- Prompt customization using LangChain templates.

---
## How to Run

1. Open the `NL2SQL_Demo.ipynb` file in Google Colab or Jupyter.
2. Upload the `nl2sql_demo.sqlite` file to your session.
3. Add your Gemini API key to secrets:

```python
import os
os.environ["GOOGLE_API_KEY"] = "your-api-key-here"
```

4. Run the notebook step by step. Try asking questions like:

```
"List the product names in Classic Cars"
"What is their stock count?"
```

The model will:
- Generate SQL from the question
- Run it on the SQLite database
- Display the results

This is a sample demo of our project that showcases how LLMs can convert natural language to SQL using LangChain.
It simplifies database access for non-technical users.
The original version is designed for scale, production use, and integration with cloud SQL systems.
