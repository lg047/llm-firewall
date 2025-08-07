# LLM Safety-Proxy

A drop-in reverse-proxy that anonymises prompts, filters risky AI output, and stores tamper-proof logs — so small & mid-size teams can ship AI features without leaking data or breaking GDPR / EU-AI-Act rules.

---

## Why you’d use it

* **Blocks leaks** – masks credit-cards, emails, IDs before they reach the model  
* **Stops jailbreaks & toxicity** – open-source guards + Grok copy-check  
* **Audit in one click** – every prompt/response hashed & stored WORM-locked in S3  
* **Model-agnostic** – point it at OpenAI today, Grok or Ollama tomorrow  
* **Five-minute setup** – swap your API URL, drop in the starter YAML policy  

---

## Quick-start (local run)

```bash
# 1. clone & enter repo
git clone https://github.com/<you>/llm-firewall.git
cd llm-firewall

# 2. set up dev-container OR local venv (choose one)
#    a) VS Code: “Reopen in Container”   – or –
python -m venv .venv && source .venv/bin/activate

# 3. install deps
pip install -r requirements.txt -r requirements-dev.txt
pre-commit install     # auto-format on save / commit

# 4. run proxy
uvicorn proxy.entry:app --reload  # now listening on http://localhost:8000
```


