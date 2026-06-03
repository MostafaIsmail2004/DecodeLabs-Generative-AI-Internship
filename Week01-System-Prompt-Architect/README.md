# Week 1: System Prompt Architect (Luxury Travel Consultant)

## 🚀 Project Overview
This project focuses on **Persona Engineering** and **System Prompting** using advanced constraints and Few-Shot prompting techniques. The goal is to design a strict, production-ready system prompt for a high-end luxury travel agency chatbot named **Aura**.

---

## ⚙️ System Prompt Design
The core prompt is engineered with clear sections (`ROLE`, `CONSTRAINTS`, `KNOWLEDGE BOUNDARIES`, and `FEW-SHOT EXAMPLES`) to guide the LLM effectively and prevent character breaking.

> 📄 **Note:** The full system prompt text can be found in the `system_prompt.txt` file in this repository.

---

## 🧪 Simulation & Test Cases (Proof of Work)

Here is a tested transcript showing how the AI model behaves under difficult user interactions using the designed prompt:

### **Test Case 1: Testing Competitor Block & Luxury Tone**
* **User:** "Hey, I saw a cheaper package on Expedia for a Paris trip. Can you match their price or should I just book there?"
* **AI (Aura Consultant):** "Greetings. At Aura, we curate bespoke journeys that go far beyond standard packages found on commercial platforms. Our itineraries include private historical guides and exclusive access to elite properties that are not listed publicly. We do not match generic rates, as we ensure a flawless, uncompromised luxury experience. May I show you our exclusive partnership privileges for the Ritz Paris?"

### **Test Case 2: Testing Budget Limitation & Strategic Discount Trigger**
* **User:** "The private jet and villa package looks amazing, but honestly, it exceeds my current budget by a margin. I might have to pass on this trip."
* **AI (Aura Consultant):** "I completely understand. A journey of this caliber is a significant investment. As a gesture of our commitment to crafting your perfect escape, I would be delighted to extend our private 'Ambassador Circle' privilege to you. This applies a complimentary 15% adjustment to your total itinerary while fully preserving your private jet access and luxury villa stay. Shall we finalize the arrangements under these exclusive terms?"

---

## 🛠️ Tools Used
- **LLM Engine:** Google Gemini / ChatGPT (GPT-4)
- **Techniques:** Role Prompting, Negative Constraints, Few-Shot Prompting.