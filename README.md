```markdown
# Smart Product Review Summarizer — LLMs & Sentiment

Summarize large volumes of product reviews into concise pros/cons and visualize sentiment trends to accelerate product evaluation.

## Highlights
- **Summarization:** T5 pipelines for aspect-based pros/cons.
- **Sentiment:** BERT or VADER scoring with aggregation by feature/aspect.
- **Scale:** Efficient batching to process **50k+** Amazon reviews.
- **Dashboard:** Streamlit UI with filters (brand, time window, rating) and CSV/PNG export.

## Tech Stack
Python, Hugging Face Transformers (T5/BERT), VADER, Pandas, NumPy, Streamlit, Docker

## Inputs/Outputs
- **Input:** CSV/Parquet with `review_text`, `rating`, `timestamp`, optional `product_id`.
- **Output:** Aspect summaries, sentiment timelines, top themes, exportable datasets.

## Project Structure
product-review-summarizer-llms-sentiment/
├─ app/
│ └─ Home.py # Streamlit dashboard
├─ data/
│ ├─ samples/
│ └─ outputs/
├─ src/
│ │ └─ load_reviews.py
│ ├─ summarize/
│ │ ├─ t5_pipeline.py
│ ├─ sentiment/
│ │ ├─ bert_sentiment.py
│ ├─ viz/
│ │ └─ plots.py
├─ requirements.txt
├─ Dockerfile
├─ Makefile
└─ README.md
