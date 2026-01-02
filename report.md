# Local LLM Evaluation Lab Report

## 1. Introduction

- The aim of this lab was to test and compare two local large language models
using Ollama on my machine. 
- The focus was on seeing how well each model handled common tasks such as summarisation, code explanation, refactoring, unit testing, and structured JSON generation. 

---

## 2. Machine Setup

- **Operating System:** Windows 11  
- **CPU:** 11th Gen Intel® Core™ i7-1185G7 (8 cores)  
- **RAM:** 32 GB  
- **GPU:** Intel Iris Xe Graphics (no dedicated GPU used for inference)  
- **LLM Runtime:** Ollama  

All models were run locally using CPU inference.

---

## 3. Models Tested

| Model             | Size  | Speed (Observed)        | Notes                         |
|-------------------|-------|--------------------------|------------------------------|
| Llama3.1          | 8B    | Faster, more consistent  | Better instruction following |
| Deepseek-coder    | 6.7B  | Slower on some prompts   | Strong code focus            |

---

## 4. Experiments

Both models were tested using the **same prompts**, covering:

- Text summarisation (technical paragraphs)
- Structured research summaries
- Python code explanation
- Code refactoring
- Writing unit tests
- JSON extraction from text
- Comparison-style reasoning questions

All prompts were run manually using the Ollama CLI.
Exact prompts are saved in `prompts.md` and full raw outputs are saved in
`outputs.md`.

---

## 5. Results & Observations

### Speed Differences
- Llama3.1 generally responded faster.
- Deepseek-coder was noticeably slower on longer reasoning and refactoring
  tasks (up to several minutes in one case).
- Performance dropped slightly when the system was being used for browsing
  at the same time.

### Quality Differences
- Llama3.1 produced clearer explanations and more balanced summaries.
- Deepseek-coder performed well on coding tasks, especially refactoring and
  unit tests.
- Llama3.1 sometimes added unnecessary constraints (e.g. limiting Fibonacci
  input size without being asked).

### Formatting Issues
- Llama3.1 usually followed formatting instructions more closely.
- Deepseek-coder often wrapped answers with extra explanation even when a
  strict format was requested.

### Hallucinations
- No major factual hallucinations were observed.
- Some minor questionable claims appeared (e.g. incorrect justification for
  input limits), but nothing severe.

### JSON Reliability
- Both models produced **valid JSON structures**.
- However, Deepseek-coder often included explanatory text **before or after**
  the JSON block, meaning extra cleaning would be required in real systems.
- Llama3.1 more consistently returned only JSON when explicitly instructed.

---

## 6. Comparison

Using the same prompts:

- Llama3.1 was more reliable for instruction-following and formatting.
- Deepseek-coder was stronger for programming-focused tasks.
- **Deepseek-coder prioritised explanation, while Llama3.1 prioritised task completion.**

---

## 7. Reflection

### What worked well?
- Running models locally made behaviour differences very clear.
- Using the same prompts across models helped with fair comparison.
- JSON and code tasks clearly showed strengths and weaknesses.

### What didn’t work?
- Deepseek-coder’s slower speed made iteration harder.
- Some outputs included unnecessary explanations when not requested.
- CPU-only inference limited performance.

### Which model would I use for:
- **Code review:** Deepseek-coder  
- **Summarisation:** Llama3.1  

### What I’d change next time
- Automate timing instead of manual observation.
- Add stress tests with longer inputs.
