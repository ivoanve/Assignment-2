---
title: "Assignment 3: Deployment and Integration of Large Language Models (LLMs)"
date: 2025-06-01
---
## Assignment 3 Report

**Student Name**: Ivonne Andrea Anave Zenteno  
**Student ID**: LS2408221  
**Submission Date**: 01/06/2025  

---

## I. Online Model API: OpenAI

To explore cloud-based LLM integration, I created an account on **OpenAI** and generated a personal API key. Using the `openai` Python library, I tested the following:

- Prompt-based text generation using the `gpt-3.5-turbo` model.
- Output customization using parameters such as `max_tokens`, `temperature`, and `top_p`.

Example test used:

```python
import openai

openai.api_key = "your-api-key"

response = openai.ChatCompletion.create(
    model="gpt-3.5-turbo",
    messages=[{"role": "user", "content": "What is artificial intelligence?"}],
    max_tokens=100
)

print(response.choices[0].message["content"])
```

⚠️ *Note:* Due to usage limits, my API key reached its quota and access was restricted after initial tests.

---

## II. Local Model Deployment: Ollama + LLaMA 3

For offline access to LLMs, I installed **Ollama** on a Windows-based OMEN 16 laptop.

### Setup steps:
- Downloaded and installed Ollama.
- Pulled and launched the **LLaMA 3** model using the command:

```bash
ollama run llama3
```

- Model size: ~4.7 GB.
- Basic prompt testing was successful using PowerShell.

---

## III. Development Environment Integration

To simulate real-world development usage, I integrated the local LLM into **Visual Studio Code** with a custom Python script that sends POST requests to Ollama's local server.

### Python Integration Example:

```python
import requests

prompt = "Explain the life."

response = requests.post(
    'http://localhost:11434/api/generate',
    json={
        "model": "llama3",
        "prompt": prompt,
        "stream": False
    }
)

print(response.json()["response"])
```

✅ This allows local LLMs to assist in academic writing, code generation, and experimentation **without relying on internet access**.

---

## IV. Optional: Research Workflow Optimization (Future Work)

I plan to expand this setup by:

- Automating prompt chaining for technical research.
- Using the model to assist in summarization of papers and generation of draft reports.
- Exploring fine-tuning or prompt-engineering techniques.

This can significantly reduce manual workload and improve research productivity.

---

## V. Conclusion

This assignment demonstrated:
- How to use both **online** and **local** LLMs.
- How to **integrate models** into a development workflow using Python and HTTP APIs.
- The value of having **offline access** to AI models for academic use.

It also emphasized the importance of balancing performance, cost, and accessibility when working with AI tools.

---

## VI. References

- [OpenAI API Documentation](https://platform.openai.com/docs)
- [Ollama Documentation](https://ollama.com/)
- [LLaMA 3 Meta AI](https://ai.meta.com/llama/)
- [Python requests module](https://docs.python-requests.org/en/latest/)

---

> Report created using Markdown and tested in VS Code environment.

