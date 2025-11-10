Vibe Matcher — AI-Powered Fashion Recommender

**Author:** Komal Nayan Sawant  
**Program:** MSc Data Science  
**Tools Used:** Python, Pandas, OpenAI Embeddings, Scikit-learn, Matplotlib, Excel  

Overview
**Vibe Matcher** is a prototype AI recommender system that matches fashion products to the *vibe* users describe.  
It embeds product descriptions using OpenAI’s `text-embedding-ada-002` model and recommends the top 3 products that best fit a given query using cosine similarity.  If the OpenAI API or internet is unavailable, the notebook automatically switches to **offline mock embeddings**, ensuring it runs smoothly anywhere.

Features
- Upload your own **Excel product sheet** (`name`, `description`, `vibes`)  
  or use the built-in **sample dataset** (10 mock fashion items)
- Generate **text embeddings** via OpenAI or fallback mode
- Compute **cosine similarity** to find the top-3 vibe matches
- Test with **3 example vibe queries**
- Measure and plot **latency per query**
- Export results to Excel (`vibe_match_results_<timestamp>.xlsx`)
- Includes **evaluation metrics**, **reflection**, and **Why AI at Nexora**

Workflow
| Step | Description |
|------|--------------|
| 1 | Upload Excel file or use built-in sample data |
| 2 | Generate embeddings (OpenAI + offline fallback) |
| 3 | Compute cosine similarity between query & products |
| 4 | Run 3 test vibe queries |
| 5 | Measure latency and log metrics |
| 6 | Export results to Excel |
| 7 | Reflect on process and improvements |
| 8 | Conclude with “Why AI at Nexora” |

 Example Queries
1. `energetic urban chic`  
2. `cozy comfortable winter wear`  
3. `elegant formal evening outfit`

Each query returns the **top 3** most relevant products with similarity scores.

---

Metrics Logged
| Metric | Description |
|--------|-------------|
| **Cosine Similarity** | Measures product-query closeness |
| **Good Match Threshold** | ≥ 0.7 indicates a strong recommendation |
| **Latency (seconds)** | Measures query processing time |
| **Good Match Ratio** | % of queries that achieved ≥ 0.7 similarity |

---

Reflection
- Implemented dual-mode embedding (OpenAI + offline) for reliability.  
- Added latency measurement for performance analysis.  
- Defined a clear similarity threshold (≥0.7) for evaluation.  
- Handled missing Excel input and API/network issues gracefully.  
- Future improvements: Pinecone or FAISS integration, multimodal embeddings, and batch vector storage.

---
How to Run

**In Google Colab**
1. Open [Google Colab](https://colab.research.google.com/)
2. Upload the notebook (`Vibe_Matcher_Prototype_Komal_Sawant.ipynb`)
3. Run all cells sequentially
4. (Optional) Upload your own Excel dataset when prompted

### 💻 **Locally (Jupyter/VS Code)**
```bash
pip install openai pandas numpy scikit-learn matplotlib openpyxl
