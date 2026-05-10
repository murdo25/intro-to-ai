# Intro to AI: An Executive Learning Plan
My thoughts on getting up to speed on the intelligence explosion

This guide is designed to take you from initial environment setup to building and iterating on autonomous AI agents, with a focus on practical business applications, evaluation, and iteration.

## The AI Learning Plan

### Milestone 1: Foundations & Setup
**Goal:** Set up your technical environment and understand the fundamentals of communicating with Large Language Models (LLMs).

#### Environment Setup
*   **Python:** The lingua franca of AI. We'll set up a basic Python environment.
*   **GitHub:** Version control to track our code and prompts.
*   **Antigravity:** Setting up the agentic coding assistant to pair program with you. We will use Antigravity exclusively instead of a traditional code editor.

**Resources:**
*   **[Antigravity Download](https://antigravity.google/download?app=antigravity):** The agentic AI assistant we'll use for all coding and experimentation. This is your primary workspace. Learning to use an AI pair programmer shifts your mindset from "writing code" to "directing an AI that writes code."
*   **[Google AI Studio](https://aistudio.google.com/welcome):** The web console for experimenting with Gemini models and prompts directly. Before building agents, you need an intuitive feel for how models respond to instructions. AI Studio is the sandbox where you rapidly test ideas and learn the "personality" of the models.
*   **[Python Official Guide](https://wiki.python.org/moin/BeginnersGuide):** Getting Python installed on your machine. Python is the glue that holds AI systems together. You don't need to be a software engineer, but understanding basic Python lets you read what the AI writes and connect scripts to real data.
*   **[GitHub Hello World Guide](https://docs.github.com/en/get-started/quickstart/hello-world):** Getting started with repositories. Prompts and agent logic are valuable assets. GitHub is how you version control these assets so you don't lose a "magic prompt" when experimenting.
*   **[Git Download](https://git-scm.com/downloads):** The standard Git command line tools. This is the underlying engine for GitHub. Having it installed allows tools like Antigravity to automatically track and save the work they do on your behalf.

#### Prompting Fundamentals
*   Zero-shot vs. Few-shot prompting.
*   Chain-of-Thought (CoT) reasoning.
*   System prompts and context window management.
*   Structured Output (JSON) for reliability.
*   **Context Assembly (Project Prompting):** How to gather and provide all necessary context (files, documentation, architecture goals) to the AI before asking it to build a complex project. The AI is only as good as the context you provide it.

**Resources:**
*   **[Google AI Studio Prompting Guide](https://ai.google.dev/docs/prompt_best_practices):** Google's official guide to prompting strategies. Learn the exact syntax to get models to do what you want consistently.
*   **[LearnPrompting.org](https://learnprompting.org/):** A comprehensive, open-source course on prompting techniques. A deep dive into advanced techniques if you want to push the models further.
*   **[JSON Prompts for AI Reliability](https://medium.com/coding-nexus/why-json-prompts-make-ai-more-reliable-with-code-real-examples-edf439999ce7):** Real examples on how outputting JSON makes your AI workflows more robust. AI is useless in an automated workflow if its output format is unpredictable. JSON fixes that.

### Milestone 2: Connecting the Plumbing
**Goal:** Bridge the conceptual gap between a web interface and your own code by running a basic API call.

*   Obtaining an API Key from Google AI Studio.
*   Setting up environment variables so you don't leak your key.
*   Writing a 10-line Python script to send a prompt to Gemini and print the response.

**Resources:**
*   **[Gemini API Quickstart](https://ai.google.dev/gemini-api/docs/quickstart?lang=python):** The official quickstart guide. This proves you can talk to the model programmatically, which is the foundational step before building any agents.

### Milestone 3: Moving to Action
**Goal:** Transition from passive chats to proactive AI agents that can use tools and execute tasks.

*   What separates an LLM from an Agent (Tools, Memory, Planning, Action).
*   Understanding the ReAct (Reason + Act) loop.
*   *Finance Use Case:* Building an agent that can browse the web for market news, read local PDFs (financial reports), and summarize findings.

**Resources:**
*   **[Andrew Ng on AI Agentic Workflows](https://www.youtube.com/watch?v=sal78ACtGTc) (Video):** Excellent high-level overview of why agents are the next frontier. Ng explains why agents are a paradigm shift, not just a buzzword.
*   **[Google Cloud AI Agents](https://cloud.google.com/use-cases/ai-agents):** An overview of what AI agents are and how they drive enterprise value. This frames agents in a business context rather than just a technical one.
*   **[Gemini Function Calling (Meeting Example)](https://ai.google.dev/gemini-api/docs/function-calling?example=meeting):** A practical example of how models use function calling to interact with external tools. Shows exactly how an AI decides to take a real-world action (like scheduling a meeting).

### Milestone 4: Measurement & Evaluation
**Goal:** Learn how to objectively measure if your AI is performing well (a critical skill for leadership).

*   The challenge of testing non-deterministic outputs.
*   Creating "Golden Datasets" (ground truth).
*   Using a highly capable model (like Gemini 1.5 Pro) to score the outputs of your prompts or agents based on a strict rubric.

**Resources:**
*   **[Judging LLM-as-a-Judge](https://arxiv.org/abs/2306.05685):** The seminal paper explaining how to use strong LLMs to evaluate other models. If you can't measure it, you can't manage it. This shows how to scientifically measure AI output.
*   **[LangSmith Evaluation Documentation](https://docs.smith.langchain.com/evaluation):** Practical tool concepts for evaluating LLM applications. Shows how industry professionals build testing frameworks for AI.

### Milestone 5: Optimization
**Goal:** Systematically improve your AI's performance.

*   The prompt engineering lifecycle: Write -> Evaluate -> Refine.
*   "Hill Climbing": Making incremental tweaks to your system prompt or agent logic to maximize your evaluation scores.
*   Version controlling your prompts to ensure you don't regress.

**Resources:**
*   **[Google Cloud Generative AI Learning Path](https://www.cloudskillsboost.google/journeys/118):** A collection of courses by Google covering everything from GenAI fundamentals to building applications. It ties all the concepts together in a structured, Google-certified curriculum.

### Milestone 6: Advanced Agents & Tool Use
**Goal:** Understand how agents interact with external systems, specifically using web browsers and calling custom tools.

*   What is "Function Calling" (or Tool Use) and how models use it to interact with the world.
*   Browser-based agents: Automating web research and interacting with web apps.
*   *Real-World Application:* Having an agent log into a financial dashboard, extract data, and input it into an internal spreadsheet.

**Resources:**
*   **[Gemini API: Function Calling](https://ai.google.dev/gemini-api/docs/function-calling):** Official documentation on how to give Gemini access to your tools and APIs. The technical manual on how to give your AI "hands" to manipulate your internal systems.
*   **[Gemini Function Calling Tutorial (Video)](https://www.youtube.com/watch?v=mVXrdvXplj0&t=8s):** A great visual guide on setting up and understanding function calling with Gemini. A clear, step-by-step video walk-through if the documentation is too dense.
*   **[Google Cloud Vertex AI Extensions](https://cloud.google.com/vertex-ai/docs/generative-ai/extensions/overview):** Using pre-built or custom extensions to allow models to interact with real-world data and services. Learn how enterprise AI plugs directly into databases and SaaS tools.
*   **[Browser Use (GitHub)](https://github.com/browser-use/browser-use):** An open-source framework demonstrating how AI agents can autonomously navigate and interact with web browsers. A glimpse into the future: an AI that literally clicks and scrolls through web pages like an intern.

---

## Next Steps
1. Install Python on your machine.
2. Create a GitHub account.
3. Open Antigravity and let it guide you through your first coding experiments.
4. Review the resources above, starting with Milestone 1.
