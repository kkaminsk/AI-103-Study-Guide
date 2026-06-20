# AI-103 Study Guides — Developing AI Apps and Agents on Azure

A set of dense, fact-checked study guides for Microsoft **Exam AI-103: Developing AI Apps and Agents on Azure**, which leads to the **Microsoft Certified: Azure AI Apps and Agents Developer Associate** certification. AI-103 is the successor to **AI-102** (*Designing and Implementing a Microsoft Azure AI Solution*), which **retires June 30, 2026**.

Each guide maps to one official exam domain, built around the platform now called **Microsoft Foundry** (formerly *Azure AI Foundry*, earlier *Azure AI Studio*). The skills outlines referenced here are the blueprint dated **April 16, 2026**.

> **Who this is for:** Azure AI engineers and developers who build, manage, and deploy agents and AI solutions with Python and Microsoft Foundry, and who want a service-selection-focused review rather than a click-through tutorial.

## The guides

| # | Guide | Exam domain | Weight |
|---|---|---|---|
| 1 | [Plan and manage an Azure AI solution](1.md) | Plan and manage an Azure AI solution | **25–30%** |
| 2 | [Generative AI and agentic solutions](2.md) | Implement generative AI and agentic solutions | **30–35%** |
| 3 | [Text analysis and speech](3.md) | Implement text analysis solutions (speech is a subsection here) | **10–15%** |
| 4 | [Computer vision solutions](4.md) | Implement computer vision solutions | **10–15%** |
| 5 | [Information extraction solutions](5.md) | Implement information extraction solutions | **10–15%** |

> **Note on weighting:** Domain 2 is the largest single slice of the exam at 30–35% — on AI-102 this material was split into two smaller domains, so it's a strong signal of where to invest study time. Speech is **not** its own domain; it's a subsection inside the text-analysis domain (Guide 3), so don't double-count it.

## What each guide covers

- **[1 · Plan and manage](1.md)** — Choosing models, Foundry services, and tools; designing retrieval, indexing, memory, and knowledge integration; setting up Foundry resources, deployments (Standard / Provisioned / Batch / Data Zone), and CI/CD pipelines; operating, monitoring, securing (RBAC, Entra ID, private networking); and responsible AI governance with guardrails.
- **[2 · Generative AI and agentic solutions](2.md)** — Building generative apps on the Foundry project endpoint; the **Responses API (Agents v2)** runtime model (agents, conversations, responses); agent tools, function calling, and multi-agent orchestration; tuning, evaluation, tracing, and observability.
- **[3 · Text analysis and speech](3.md)** — Entity/topic/summary extraction and structured JSON outputs; sentiment, PII, and content safety; Azure Translator vs. LLM translation flows; speech-to-text/text-to-speech, custom speech, the Realtime API, and multimodal audio reasoning.
- **[4 · Computer vision](4.md)** — Image generation (`gpt-image-*`, not the retired DALL-E 3) and video generation (Sora 2); vision-enabled chat models; captions and accessibility alt text; Content Understanding analyzers; and multimodal safety, provenance (Content Credentials / C2PA), and moderation.
- **[5 · Information extraction](5.md)** — Retrieval and grounding pipelines (pull vs. push ingestion, full-text/vector/hybrid/semantic/agentic retrieval, enrichment skills); and document extraction with **Azure AI Document Intelligence** (deterministic fields) vs. **Content Understanding** (generative, schema-driven, RAG-ready output).

## High-leverage facts that are easy to get wrong

These claims drift fast as Microsoft renames and re-scopes services through 2026:

- **The platform is Microsoft Foundry.** Don't reintroduce the old *Azure AI Foundry* / *Azure AI Studio* names except when contrasting legacy vs. current.
- **The exam is AI-103**, not AI-102.
- **Keyless model inference in new Foundry uses the `Foundry User` role**, not `Cognitive Services User` (the latter was the classic Azure OpenAI answer — watch the resource type in the question).
- **The runtime is the Responses API (Agents v2)** — conversations / items / responses / agent versions — not the legacy **Assistants API** (threads / messages / runs / assistants), reported to sunset **August 26, 2026**.

## Accuracy and verification

These guides make specific, drift-prone claims about Foundry, Azure AI Search, deployment types, RBAC roles, quotas, and guardrails. Every factual claim should be verifiable against current Microsoft Learn documentation. The guides are fact-checked per file; some open with a dated **"Accuracy note (verified \<month year\>)"** block recording when the check happened.

**Citation styles differ by file** (preserve whichever a file already uses):

- `2.md` and `5.md` use Markdown footnotes (`[^sg]`, `[^foundry]`, …) with a **Sources** section listing full Microsoft Learn URLs — the cleaner style.
- `1.md`, `3.md`, and `4.md` carry inline `citeturn…` tokens, which are research-tool artifacts rather than real links. Converting these to real footnote citations is the right direction — but verify each source first; don't invent URLs.

## Suggested study order

Work the domains in weighting order, building one small end-to-end project per guide. Start with **Guide 2** (largest weight) to get a generative app and a stateful agent running, layer in retrieval and grounding from **Guides 1 and 5**, then add the modality-specific skills from **Guides 3 and 4**. Each guide ends with a high-yield "what to memorize" list and, in most cases, practice questions with an answer key.
