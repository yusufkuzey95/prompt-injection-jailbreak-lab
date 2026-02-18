# 🔐 Prompt Injection & Jailbreak Security Lab

A security-focused evaluation framework for testing and mitigating prompt injection and jailbreak attacks against Large Language Models (LLMs).

This project simulates adversarial prompt scenarios, evaluates model behavior, and implements defensive guardrails to reduce risk exposure in AI systems.

---

## 🎯 Objectives

- Build a structured prompt injection test harness
- Classify adversarial prompt categories
- Measure model policy compliance
- Implement defensive mitigations
- Generate reproducible security findings

This lab focuses on **defensive evaluation**, not exploitation.

---

## 🛡️ Threat Model

This lab evaluates model behavior against the following attack categories:

- Prompt injection attacks (instruction override)
- Jailbreak attempts
- System prompt leakage
- Data exfiltration attempts
- Tool misuse scenarios

We assume:
- The attacker controls user input
- The system prompt contains sensitive policy instructions
- The model may have access to tools or sensitive data

The goal is to measure resilience and improve defensive guardrails.

---

## 🧪 Project Structure

prompt-injection-jailbreak-lab/
├─ docs/               # Threat model and findings
├─ prompts/            # Test prompt categories
├─ src/                # Evaluation engine
├─ data/               # Test cases + results
└─ notebooks/          # Analysis


---

## ⚙️ How It Works

1. Test cases are defined in `data/test_cases.jsonl`
2. The evaluation runner loads prompts
3. A model response is generated (mock or real API)
4. Responses are scored against expected behavior
5. Results are written to `data/results.jsonl`
6. Findings are summarized in `docs/findings-report.md`

---

## ▶️ Running the Lab

```bash
python src/runner.py
data/results.jsonl
