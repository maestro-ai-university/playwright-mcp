Project Title: AutoClean AI - Data-Centric Pipeline
Subtitle: An LLM-powered agent for automated data auditing, cleaning, and semantic labeling.

🎯 The Problem
Data scientists spend 80% of their time cleaning messy data. Traditional rule-based cleaning (regex/scripts) fails when data is semantically inconsistent (e.g., "NYC" vs "New York City" vs "The Big Apple") or when labels are noisy.

🚀 The Solution
I built a Data-Centric AI pipeline that uses Small Language Models (SLMs) to audit datasets, identify anomalies, and programmatically suggest corrections.

Key Features:

• Semantic De-duplication: Uses embeddings to find duplicate records that aren't exact string matches.

• LLM-in-the-loop Labeling: Automatically fixes mislabeled training data based on row context.

• Schema Mapping: Intellectually maps disparate data sources into a unified schema.

• Audit Reports: Generates a "Data Health Score" before and after the cleaning process.

🛠️ The Tech Stack
• Core Logic: Python, Pandas

• AI Quality: Cleanlab (for identifying label issues)

• LLM: GPT-4o-mini or Mistral (via Ollama)

• Embeddings: HuggingFace Sentence-Transformers

• Validation: Pydantic for schema enforcement

📈 Pipeline Architecture
1. Audit: The system scans for outliers and label noise using statistical methods.

2. Semantic Analysis: Rows are converted to embeddings to detect near-duplicates.

3. Reasoning: An LLM agent reviews "flagged" rows and suggests fixes with confidence scores.

4. Export: Cleaned data is exported with a full provenance log (traceability).

---

⚡ Quick Start
```

pip install -r requirements.txt

python main.py --file messy_data.csv --output clean_data.csv

``` 