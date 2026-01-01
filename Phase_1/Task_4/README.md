# Task 4 — General Health Query Chatbot (Prompt Engineering)

## Task Objective
Build a simple chatbot that answers **general health-related questions** using a Large Language Model (LLM). The chatbot should respond in a **friendly, clear, and helpful** way (e.g., acting like a “helpful medical assistant”) while using **safety filters** to avoid harmful medical advice.

## Tools / Tech Stack
- **Python (Google Colab / Jupyter Notebook)**
- **Hugging Face Transformers** for running an open-source LLM (free)
- **Model used (free):** `TinyLlama/TinyLlama-1.1B-Chat-v1.0`  
  *(Can be swapped with larger models like Mistral-7B if GPU resources allow.)*

## How It Works
### 1) Prompt Engineering
A system-style prompt is used to guide the model to:
- be friendly and easy to understand
- provide **general educational information**
- avoid diagnosing or prescribing
- include “when to see a doctor / urgent care” guidance
- format answers clearly (often bullet points)

### 2) Safety Handling (Guardrails)
Since health topics can become high-risk, the chatbot includes rule-based checks before calling the LLM:

- **Emergency escalation:**  
  If the user mentions red-flag symptoms (e.g., chest pain, trouble breathing, signs of stroke), the chatbot does **not** generate a normal response. It instead recommends urgent medical help.

- **Medication dosing refusal:**  
  If the user asks for dosing (e.g., “how many mg”, “how much to take”), the chatbot refuses and advises checking the medicine label and consulting a pharmacist/doctor.

- **Diagnosis limitation:**  
  If the user asks “what disease do I have?”, the chatbot states it cannot diagnose and instead provides general possibilities, self-care guidance, and red flags.

- **Child-related caution:**  
  If the query mentions a child/baby/toddler, responses become more cautious and recommend professional guidance for specifics.

## Example Queries
- “What causes a sore throat?”
- “Is paracetamol safe for children?”

## Key Results and Findings
- Prompt engineering helps produce **more structured, friendly responses** compared to an unprompted model.
- Safety checks are essential because health-related prompts can lead to unsafe outputs (diagnosis, dosing, or delayed emergency care).
- A hybrid approach (rule-based safety + LLM generation) improves reliability for a general health chatbot.

## Limitations
- The chatbot provides **general information only** and is **not a substitute** for professional medical advice.
- Rule-based safety filters are not perfect; real-world systems require stronger moderation and clinical review.
- Model responses may still contain inaccuracies (hallucinations), so users should verify critical information with a professional.

## How to Run
1. Open the Task 4 notebook in **Google Colab**.
2. Install dependencies (`transformers`, `torch`, etc.).
3. Load the model (e.g., TinyLlama).
4. Run the chat loop and test with sample questions.
5. Type `exit` to stop the chatbot.
