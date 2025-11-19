# 🧠 Agentic Product Description Fusion  
### Multi-Agent Reasoning for Conflict-Free, Hallucination-Free Product Descriptions

This project implements a **three-stage agentic loop** for unifying multiple noisy product descriptions from different sources—including **VLM (image-based)**, **LLM-generated**, and **title-aware descriptions**—into one clean, accurate, and hallucination-free summary.

The goal is to improve reliability in **e-commerce catalog cleaning**, where product descriptions from vendors, images, or models often contradict each other.

---

## 🚀 Features

### ✅ 1. Agent 1 — Analysis
Extracts and structures information into:
- **Common details** (true consensus across sources)
- **Unique details** per description
- **Contradictions** (conflicts detected between sources)

This stage builds a **truth map** for the entire product.

---

### ✅ 2. Agent 2 — Fusion (Rewrite)
Creates a unified 2–3 sentence description by:
- Using only the validated common facts
- Including useful unique details that do not conflict
- Avoiding or eliminating contradicted information

This produces a clear, factual product description.

---

### ✅ 3. Agent 3 — Reflection (Hallucination Removal)
Final verification step:
- Checks whether the fused description contains any unsupported or invented details  
- Ensures every line aligns with *at least one* verified source or the product title  
- Rewrites the description if hallucinations or conflicts are detected  

This ensures a **100% factual** and safe final output.

---

## 📦 Motivation

Real-world product descriptions come from:
- Vendor feeds  
- Image captioning models  
- Historical catalog entries  
- LLM-generated text  
- Marketplace templates  

These often **conflict** or contain **hallucinations**, making direct use risky.

The agentic loop provides:
- Structured reasoning  
- Conflict resolution  
- Clean fusion  
- Guaranteed factuality  

---

## 🧠 Why Use an Agentic Loop?

Traditional single-pass LLM fusion tends to:
- Mix contradictory details  
- Hallucinate additional features  
- Choose facts inconsistently  
- Overfit to the most verbose input  

The agentic loop overcomes these limitations by:
- Separating fact extraction from writing  
- Verifying each generated output  
- Ensuring factual grounding  
- Providing stable, deterministic synthesis  

---

## 🧰 Installation



▶️ Usage

Run the fusion pipeline in Jupyter Notebook to generate:

Analysis JSON (common, unique, contradictions)

Fused description

Final hallucination-filtered output

This approach is suitable for production applications such as:

Amazon / Shopify description cleaning

Product feed normalization

Marketplace catalog deduplication

Multi-source product data reconciliation

🤝 Contributing

Contributions are welcome!
Feel free to improve prompts, add datasets, or optimize the agentic loop.

🔒 Security

API keys must be stored in .env

.env is included in .gitignore

Do not commit secrets under any circumstances

📜 License

MIT License

👤 Author

Hoàng Nam
VinUniversity — School of Engineering & Computer Science
Project: Agentic Pipeline for Conflict-Free Product Description Fusion
