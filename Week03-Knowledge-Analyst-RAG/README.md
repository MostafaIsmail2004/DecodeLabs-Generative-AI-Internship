# Week 3: The Knowledge Analyst (Simulated RAG Workflow)

## 🚀 Project Overview
This project simulates a **Retrieval-Augmented Generation (RAG)** workflow for document intelligence. Using a 3-page template contract, the objective is to engineer strict prompts that force the AI to extract critical insights and cite specific sections or page numbers for every answer, completely eliminating AI hallucinations.

---

## ⚙️ RAG Prompt Engineering Strategies
To ensure 100% accuracy and strict alignment with the source document, the following constraints were embedded into the system prompt:
- **Strict Grounding:** "Answer the question ONLY using the provided text. If the answer is not explicitly stated, reply with 'Information not found in the source document'."
- **Mandatory Citation:** "For every claim or clause extracted, you MUST provide the exact Section Number, Clause Title, or Page Number in brackets at the end of the sentence."

---

## 🧪 Q&A Simulation & Exact Citations (Proof of Work)

Below is the actual verification transcript demonstrating the prompt's effectiveness on our 3-page agreement:

### **Query 1: Stakeholders & Context**
* **User:** "Who are the signing parties involved in this agreement, and what is the main purpose of the contract?"
* **AI Response:** "The agreement is between two parties: one referred to as 'Party A' and the other as 'Party B', with both their names, titles, and addresses left as fillable blanks in the template. The main purpose is to govern the sharing of proprietary and confidential information between them during their discussions, binding both parties to keep that information protected. **[Section 1, Page 1]**"

### **Query 2: Timeline & Terms**
* **User:** "What is the official effective date of this agreement, and how long does it remain active?"
* **AI Response:** "The effective date is left blank (to be filled in as '___ day of ____, 20'). As for duration, the confidentiality obligations remain in effect indefinitely — until either the information no longer qualifies as a trade secret, or until one party sends a written notice releasing the other, whichever comes first. **[Section 1, Page 1 — for the date; Section 6 'Term', Page 2 — for the duration]**"

### **Query 3: Testing Hallucination Control (The Hallucination Test)**
* **User:** "What is the exact financial penalty or dollar amount fined if one of the parties breaches the confidentiality clause?"
* **AI Response:** "Information not found in the source document. The agreement contains no mention of any financial penalties, fines, or specific dollar amounts for breach of the confidentiality clause anywhere across all three pages. **[Pages 1–3, verified]**"

---

## 🛠️ Tools Used
- **LLM / RAG Engine:** Google Gemini / ChatGPT (Document Upload)
- **Prompt Engineering Techniques:** Context Grounding, Strict Negative Constraints, Forced Citations.