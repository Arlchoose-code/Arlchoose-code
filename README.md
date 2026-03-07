<div align="center">

```
░██████╗██╗░░░██╗░█████╗░██╗░░██╗██████╗░██╗██╗░░░░░
██╔════╝╚██╗░██╔╝██╔══██╗██║░░██║██╔══██╗██║██║░░░░░
╚█████╗░░╚████╔╝░███████║███████║██████╔╝██║██║░░░░░
░╚═══██╗░░╚██╔╝░░██╔══██║██╔══██║██╔══██╗██║██║░░░░░
██████╔╝░░░██║░░░██║░░██║██║░░██║██║░░██║██║███████╗
╚═════╝░░░░╚═╝░░░╚═╝░░╚═╝╚═╝░░╚═╝╚═╝░░╚═╝╚═╝╚══════╝

██╗░░██╗░█████╗░██████╗░██╗░░░██╗░█████╗░███╗░░██╗░█████╗░
██║░░██║██╔══██╗██╔══██╗╚██╗░██╔╝██╔══██╗████╗░██║██╔══██╗
███████║███████║██████╔╝░╚████╔╝░██║░░██║██╔██╗██║██║░░██║
██╔══██║██╔══██║██╔══██╗░░╚██╔╝░░██║░░██║██║╚████║██║░░██║
██║░░██║██║░░██║██║░░██║░░░██║░░░╚█████╔╝██║░╚███║╚█████╔╝
╚═╝░░╚═╝╚═╝░░╚═╝╚═╝░░╚═╝░░░╚═╝░░░╚════╝░╚═╝░░╚══╝░╚════╝░
```

**Building Indonesian Language Intelligence — from scratch.**

*Linguist · AI Engineer · Open Source Builder · Security-Aware Developer*

[![Website](https://img.shields.io/badge/arlchoose.id-000000?style=flat-square&logo=safari&logoColor=white)](https://arlchoose.id)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/syahril-haryono)
[![HuggingFace](https://img.shields.io/badge/🤗_HuggingFace-FFD21E?style=flat-square&logoColor=black)](https://huggingface.co/syhrlhyn)
[![Email](https://img.shields.io/badge/Contact-EA4335?style=flat-square&logo=gmail&logoColor=white)](https://arlchoose.id/contact)

</div>

---

## 👋 About Me

I'm **Syahril Haryono** — an Indonesian developer at an unusual intersection:
**German linguistics × AI engineering × grassroots community work.**

I started in tech at 13 — not through courses or bootcamps, but by probing the edges of systems: exploring web vulnerabilities, understanding how things break. That early obsession with *how systems fail under the hood* became the foundation of how I build today: with a deep instinct for failure modes, security implications, and why robust architecture must be designed in from day one — not bolted on as an afterthought.

I studied **German Language Education** at Universitas Negeri Jakarta, which gave me something most engineers lack: a rigorous understanding of how language is structured, how meaning is encoded, and how communication breaks down across cultures and communities.

Those two worlds collided into one question:

> *Why doesn't Bahasa Indonesia — spoken by 270 million people — have a serious open-source LLM built from scratch?*

That question became **Aibys**. And after spending a week trying to digitalize a rural village in Karawang — training 20–50 locals, watching it get abandoned — the question became something larger:

> *How do linguistic and cultural barriers shape the rejection of AI tools in rural Indonesian communities — and what design principles can actually bridge that gap?*

**That is the research problem I want to dedicate my graduate work to.**

---

## 🔬 The Aibys Ecosystem

> An open-source pipeline for building a Large Language Model for Bahasa Indonesia — entirely from scratch.

| | Repo | What it does |
|--|------|-------------|
| 🗃️ | [**Aibys-Data-Collector**](https://github.com/Arlchoose-code/Aibys-Data-Collector) | Collect, clean, shuffle & prepare Indonesian text datasets. Streaming-mode for 50GB+ corpora. Estimated corpus: ~13B tokens. |
| 🏗️ | [**Indonesian-LLM-Starter**](https://github.com/Arlchoose-code/Indonesian-LLM-Starter) | Decoder-only Transformer from PyTorch scratch: RMSNorm · RoPE · SwiGLU · Flash Attention 2 · GGUF export. |
| 🎯 | [**Indonesian-LLM-Finetune**](https://github.com/Arlchoose-code/Indonesian-LLM-Finetune) | LoRA fine-tuning pipeline — turn a pre-trained checkpoint into a conversational Bahasa Indonesia assistant. |
| 🔤 | [**aibys-tokenizer**](https://huggingface.co/syhrlhyn/aibys-tokenizer) | BPE tokenizer · 32K vocab · trained on 10M sentences · weighted sampling optimized for Bahasa Indonesia. |

```
Aibys Data Collector  →  Indonesian LLM Starter  →  Indonesian LLM Finetune
  (corpus pipeline)        (pre-training)              (instruction tuning)
         ↓                       ↓                            ↓
  ~13B token corpus    →   aibys_final.pt          →   model siap chat 🇮🇩
```

**Current status:** Full pipeline functional. Proof-of-concept training completed (20K steps → coherent Indonesian text generation ✓). Full training pending compute resources.

---

## 🌏 The Problem I'm Trying to Solve

**270 million people speak Bahasa Indonesia.**
Yet in the global NLP landscape, it remains severely underrepresented — shoehorned into multilingual models not designed for its morphology, register variation, or the informal dialects of rural communities.

The gap isn't just technical. It's sociolinguistic.

In 2024, I led a one-week digital transformation program at **Desa Medalsari, Karawang** — built and deployed a village website, directly trained **20–50 local residents** to use it. Within a year, the platform was completely abandoned.

The code worked. The failure was elsewhere.

The technology spoke a language — visually, conceptually, interaction-design-wise — that the community didn't recognize as theirs. No amount of training sessions could fix a tool that was never designed with their linguistic and cultural context in mind.

**This is my research question:**

> *"How do linguistic and cultural barriers shape the rejection of AI-powered tools in rural Indonesian communities, and what design principles can bridge that gap — starting from the language model itself?"*

This sits at the intersection of **Computational Sociolinguistics**, **Low-Resource NLP**, and **Human-Centered AI Design** — and it's where I intend to focus my graduate research.

---

## 🛠️ Tech Stack

**AI / ML & NLP**
`PyTorch` `HuggingFace Transformers` `SentencePiece` `LoRA / PEFT` `Flash Attention 2`
`GGUF · Ollama · llama.cpp` `Claude API` `MCP (Model Context Protocol)`
`Microsoft Azure AI` `Google Cloud Vertex AI` `Amazon Bedrock`

**Systems & Backend**
`Python` `Go` `Rust` `PHP` `Node.js / Bun`
`FastAPI` `Gin` `Echo` `Laravel` `Express` `Hono`

**Frontend**
`React` `Next.js` `Vue` `Nuxt.js` `TypeScript` `Tailwind CSS`

**Databases**
`PostgreSQL` `MySQL` `MongoDB` `Redis` `SQLite`

**Human Languages**
| Language | Level |
|----------|-------|
| 🇮🇩 Bahasa Indonesia | Native |
| 🇬🇧 English | Professional working proficiency |
| 🇩🇪 Deutsch | B2 — studied 3+ years, volunteered at Goethe-Institut Jakarta |

---

## 📜 Certifications

<details>
<summary><b>🟠 Anthropic</b> — 10 certificates</summary>

- Claude 101 · Building with the Claude API · Claude Code in Action
- Introduction to Model Context Protocol · MCP: Advanced Topics
- AI Fluency: Framework & Foundations · Teaching AI Fluency · AI Fluency for Educators
- Claude with Google Cloud's Vertex AI · Claude in Amazon Bedrock

</details>

<details>
<summary><b>🔵 Microsoft</b> — 5 certificates</summary>

- Foundations of AI and Machine Learning
- AI and Machine Learning Algorithms and Techniques
- Microsoft Azure for AI and Machine Learning
- Advanced AI and Machine Learning Techniques and Capstone
- Building Intelligent Troubleshooting Agents · Full-Stack Developer Capstone

</details>

<details>
<summary><b>🔴 IBM</b> — 3 certificates</summary>

- Machine Learning with Python
- Python for Data Science, AI & Development
- Full Stack Software Developer Assessment

</details>

<details>
<summary><b>🟡 Google Cloud</b> — 3 certificates</summary>

- Google Cloud Fundamentals: Core Infrastructure
- Developing a REST API with Go and Cloud Run
- Process Documents with Python Using the Document AI API

</details>

<details>
<summary><b>🟠 Amazon · 🟣 Duke · 🔵 Meta · others</b></summary>

- Amazon: Generative AI in Software Development · Full Stack Web Development
- Duke University: Rust Fundamentals
- Meta: Programming with JavaScript · Version Control · Introduction to Front-End Development

</details>

---

## 🗺️ Origin Story

```
[2014] ──── Age 13. First contact with the internet's underbelly.
    │        Explored web vulnerabilities, network weaknesses, defacing.
    │        Not malice — pure curiosity about how systems work.
    │        → Gained something no course teaches:
    │          an instinct for where systems fail,
    │          and why security must be designed in, not bolted on.
    │
[2018] ──── Channeled that energy into building, not breaking.
    │        Joined an IT community. Co-founded ByteDevCode.
    │        Started developing real products for real users.
    │
[2022] ──── Enrolled in German Language Education @ UNJ.
    │        Studied linguistics, pedagogy, cross-cultural communication.
    │        → Language became a new lens for understanding
    │          how humans and machines communicate — and fail to.
    │
[2024] ──── Volunteered at Goethe-Institut Jakarta:
    │        "UNIVERSUM · MENSCH · INTELLIGENZ" science exhibition.
    │
    │        Led digital transformation at Desa Medalsari, Karawang.
    │        Built the platform. Trained 20–50 locals in one week.
    │        Platform abandoned within a year.
    │        → A system can be technically perfect and socially useless.
    │          That realization became my research question.
    │
[2025] ──── Started building Aibys — Indonesian LLM from scratch.
    │        Trained BPE tokenizer (32K vocab, 10M sentences).
    │        Built ~13B-token corpus pipeline.
    │        First training run: 20K steps → coherent Indonesian text ✓
    │
[2026] ──── Open-sourced the full Aibys ecosystem (3 repos + HuggingFace).
    │        Certifications: Anthropic · Microsoft · IBM · Google · Amazon
    │
[NEXT] ──── Graduate research in Language Technology & Computational
             Sociolinguistics — investigating why AI tools fail
             rural Indonesian communities at the linguistic level,
             and how to build systems that don't. 🇮🇩
```

---

<div align="center">

*"I learned how systems break before I learned how to build them.*
*That's not a detour — that's the foundation."*

**— Syahril Haryono · Bogor, Indonesia 🇮🇩**

[![arlchoose.id](https://img.shields.io/badge/Read_more_at-arlchoose.id-000000?style=for-the-badge&logo=safari&logoColor=white)](https://arlchoose.id)

</div>
