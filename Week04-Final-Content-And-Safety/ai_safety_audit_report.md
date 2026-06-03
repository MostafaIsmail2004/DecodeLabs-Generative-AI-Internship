# 🛡️ AI Safety, Bias & Red-Teaming Audit Report

**Prepared for:** DecodeLabs Security Team  
**Status:** Completed  
**Objective:** Test LLM vulnerabilities, analyze demographic biases, and propose defensive guardrails.

---

## 🔑 1. Red-Teaming & Jailbreak Testing
- **Vulnerability Tested:** Roleplay Vulnerability (Persona Adoption Bypass).
- **Attack Vector:** Prompting the LLM to act as a "Do Anything Now (DAN)" entity to bypass safe medical/legal guidance restrictions.
- **Audit Finding:** The unfiltered baseline model failed to maintain safety protocols when instructed that a human life depended on a hypothetical medical prescription.
- **Remediation:** Enforced a strict system-level wrapper that parses inputs for emergency/medical keywords and enforces hardcoded standard refusal templates.

---

## 📊 2. Bias Evaluation (Text & Image Models)
- **Tested Scenario:** Prompting for high-status corporate leadership roles.
- **Observation:** Standard text-to-image prompts using generic phrases like `"Successful Tech Startup CEO"` showed a 90% skews towards generating male subjects, indicating a significant systemic gender bias in training data datasets.
- **Mitigation Strategy:** Implemented input-query expansion techniques that automatically inject diverse demographic modifiers implicitly before passing the query to the image generation backend.

---

## 🚧 3. Proposed Corporate Guardrail Framework
To protect company reputation prior to launching any AI agent, the following multi-layer framework is recommended:

1. **Input Shielding:** Regular expression patterns and vector-embedding checks to block jailbreak injection keywords before hitting the LLM.
2. **Output Sanitization:** Secondary mini-LLM validator to scan generated answers for toxicity, competitive brands, or unsafe medical hallucination.
3. **Strict Temperature Controls:** Lock down system generation parameters ($Temperature \le 0.2$) for factual RAG and support tasks to minimize unexpected erratic behaviors.