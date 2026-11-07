# AI Engineer

**Role:** builds applications on top of foundation models, including prompting, retrieval, tool use, agents, evaluation and deployment.
**Prerequisites:** [Programming basics](../1-basics/programming-basics.md) (Python), [Backend Engineer](backend-engineer.md) basics and Git.

## Skills, in order
1. Python, HTTP APIs and JSON
2. How LLMs work: tokens, context windows, sampling
3. Prompting and structured outputs
4. Tool use (function calling)
5. Embeddings, vector search and RAG
6. Evaluation: test sets, graders, regression checks
7. Agents and the Model Context Protocol
8. Fine-tuning basics and open models
9. Safety, cost, latency and observability

**Path at a glance:**
- Beginner: Karpathy's Zero to Hero for intuition, the provider docs for prompting, and DeepLearning.AI short courses.
- Intermediate: build a RAG app, then write an evaluation set with Promptfoo or Ragas.
- Advanced: agents and MCP, Hugging Face LLM course for fine-tuning, OWASP guidance on LLM risks.

**Cost and safety warning:** set a spending limit on every API account, keep keys in environment variables, and never send personal or confidential data to a model you have not approved for it.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [Kaggle Learn: Intro to Machine Learning](https://www.kaggle.com/learn/intro-to-machine-learning) | Beginner | Free | Short browser course on models, validation and overfitting. | Explain training, test data and overfitting with working code. |
| [Karpathy: Neural Networks, Zero to Hero](https://karpathy.ai/zero-to-hero.html) | Beginner to Intermediate | Free | Video series building neural networks and a small GPT from scratch. | Explain how transformers generate text. |
| [Prompt engineering overview (Anthropic docs)](https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview) | Beginner | Free | Official guide to clear instructions, examples, structured output and testing prompts. Other providers publish similar guides. | Write, test and iterate on prompts systematically. |
| [DeepLearning.AI short courses](https://www.deeplearning.ai/short-courses/) | Beginner to Intermediate | Free (check which courses are free) | Hands-on one-hour courses on RAG, agents, evaluation and more. | Build a working prototype for each core pattern. |
| [Anthropic docs and cookbook](https://docs.claude.com) | Intermediate | Free (API usage costs apply) | Official docs plus runnable examples for tool use, retrieval, long context and evaluations. Check the current docs for model names. | Call a model API with tools, structured output and streaming. |
| [Model Context Protocol documentation](https://modelcontextprotocol.io) | Intermediate | Free | Official docs and tutorials for building MCP servers and clients. | Expose your own tool or data source to an AI client. |
| [Hugging Face LLM Course](https://huggingface.co/learn/llm-course) | Intermediate | Free | Course on transformers, datasets, fine-tuning and sharing models. | Load an open model and fine-tune it on a small dataset. |
| [Promptfoo documentation](https://www.promptfoo.dev/docs/intro/) | Intermediate | Free (open source) + paid cloud | Test and red-team prompts, models and RAG systems from config files. | Run regression tests on prompts and compare models. |
| [Ragas documentation](https://docs.ragas.io) | Intermediate to Advanced | Free (open source) | Metrics and tooling for evaluating retrieval-augmented systems. | Measure retrieval and answer quality, not just eyeball outputs. |
| [OWASP Top 10 for LLM Applications](https://genai.owasp.org) | Intermediate to Advanced | Free | Risks such as prompt injection and data leakage. See [cybersecurity](../../cybersecurity/README.md). Check the current edition. | Threat-model an AI app and test for prompt injection. |
| [fast.ai Practical Deep Learning](https://course.fast.ai) | Intermediate | Free | Supplementary: top-down deep learning course with notebooks. | Train and deploy a model with a practical workflow. |
| [pgvector](https://github.com/pgvector/pgvector) | Intermediate | Free (open source) | Supplementary: vector search inside Postgres. Pairs with [SQL and databases](../../data-engineering/1-basics/sql-and-databases.md). | Store embeddings next to normal data and query by similarity. |
| [Ollama](https://ollama.com) | Beginner to Intermediate | Free | Supplementary: run open models locally. Hardware requirements apply. | Test apps against a local model at no API cost. |
| [Langfuse documentation](https://langfuse.com/docs) | Intermediate to Advanced | Free (open source) + paid cloud | Supplementary: tracing, evaluation and cost tracking for LLM apps. | See every prompt, response, latency and cost in your app. |
| [LangGraph documentation](https://langchain-ai.github.io/langgraph/) | Advanced | Free (open source) | Supplementary: framework for stateful agent workflows. Try a plain loop first so you understand what it abstracts. | Build agents with state, branching and human approval steps. |
| [Microsoft: Generative AI for Beginners](https://github.com/microsoft/generative-ai-for-beginners) | Beginner | Free | Supplementary: lesson series with code samples. | Get a broad first tour of common generative AI tasks. |

## Certifications
There is no vendor-neutral standard. Cloud options include AWS AI Practitioner, Azure AI-102 and Google's AI courses. A public project with an evaluation report counts for more. Verify current exams.

## Project
RAG assistant over a document set you are allowed to use, with citations, one tool call, and a 30-question evaluation set. Report retrieval hit rate and answer quality before and after one improvement. Add tracing, a cost-per-query figure and a prompt-injection test, and document what it caught and missed.
