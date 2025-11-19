# Glossary of Key Terms

This glossary defines technical terms used throughout the book. Terms are explained in plain language for executives and managers without assuming technical background.

**Agent (AI Agent)**: A program that uses large language models to make sequential decisions about which tools to use or actions to take. Despite marketing claims, agents are scripted workflows, not autonomous entities. [See Chapter 4](#chapter-4-myth-ai-agents-are-autonomous-reality-theyre-scripted-workflows-with-llm-calls).

**AGI (Artificial General Intelligence)**: Hypothetical AI that matches or exceeds human intelligence across all domains. Does not currently exist. Marketing often conflates narrow AI capabilities with AGI to inflate product claims.

**API (Application Programming Interface)**: A way for different software systems to communicate with each other. APIs allow AI tools to connect to your existing systems (databases, email, calendars, etc.).

**Augmentation**: Using AI to enhance human work rather than replace it. The copilot model where AI handles routine tasks while humans provide judgment, context, and accountability. [See Chapter 3](#chapter-3-myth-ai-will-replace-you-reality-ai-augments-your-work).

**Demo**: A working prototype that demonstrates core functionality under ideal conditions. Demos typically show the "happy path" (when everything works perfectly) but lack 80% of the work needed for production readiness: error handling, security, scalability, monitoring. [See Chapter 8](#chapter-8-myth-demos-equal-production-ready-reality-the-vibe-coding-gap).

**Deployed**: Software that is running in a live production environment where real users access it. More specific than "production" - implies the code is actively serving users.

**Edge Case**: An unusual or extreme scenario that falls outside normal operating parameters. Examples: names with special characters, users with thousands of records, simultaneous conflicting updates. AI often fails on edge cases because training data focuses on common patterns.

**Generative AI (GenAI)**: AI systems that generate new content (text, images, code) by predicting what should come next based on patterns in training data. Includes ChatGPT, Claude, Gemini, and similar tools. Distinguished from earlier AI that classified or predicted but didn't generate.

**Hallucination**: When AI confidently generates false information. Not a bug - it's how the system works. AI predicts plausible-sounding text based on patterns, not facts. Hallucinations occur 17-33% of the time even in specialized AI. [See Chapter 5](#chapter-5-myth-ai-is-always-right-reality-hallucinations-and-limitations).

**Happy Path**: The ideal scenario where everything works as expected. Users enter valid data, systems don't crash, network connections are fast. Demos focus on happy paths. Production systems must handle unhappy paths (errors, failures, unexpected inputs).

**LLM (Large Language Model)**: The underlying technology powering tools like ChatGPT and Claude. A statistical model trained on massive amounts of text to predict what words come next. LLMs don't understand meaning - they complete patterns. [See Chapter 2](#chapter-2-myth-ai-can-think-reality-ai-completes-patterns).

**MVP (Minimum Viable Product)**: The simplest version of a product that can be released to test a concept with real users. More developed than a demo but still lacks many production-ready features. Often confused with "production-ready" despite significant gaps.

**Production / Production Environment**: The live system that real users interact with. Distinguished from development or demo environments. Production systems require error handling, security, monitoring, scalability that demos lack.

**Production-Ready**: Software that meets all requirements for deployment to real users: functional completeness, reliability, performance, security, operational monitoring, and maintainability. Typically requires 4-10x the time invested in the demo. [See Chapter 8](#chapter-8-myth-demos-equal-production-ready-reality-the-vibe-coding-gap).

**Prompt**: The text input you provide to an AI system. Quality of output depends heavily on prompt quality. Strong prompts include context, format requirements, constraints, examples, and success criteria. [See Chapter 7](#chapter-7-myth-just-prompt-and-go-reality-engineering-good-results).

**Prompt Engineering**: The practice of crafting effective prompts to get useful AI output. Not magic - it's being specific about what you want. Involves providing context, specifying format, setting constraints, giving examples, and defining success criteria.

**Prototype**: An early model built to test a concept. More exploratory than an MVP. Used for validation and stakeholder buy-in, not for serving real users. Often confused with demos.

**RAG (Retrieval Augmented Generation)**: A technique where AI searches provided documents or databases before generating responses, reducing (but not eliminating) hallucinations. Used in specialized tools to ground AI responses in your actual data rather than just training patterns.

**Token**: The basic unit AI models process. Roughly 0.75 words per token. AI doesn't read word by word - it breaks text into tokens. Important for understanding why AI struggles with tasks like "count the R's in strawberry" (sees tokens, not letters).

**Training Data**: The massive collection of text, code, images, etc. that AI systems learn patterns from. AI can only generate what resembles patterns in training data. Can't go beyond training data to handle truly novel problems.

**Vibe Coding**: Rapid prototyping using AI code generation, going on "feel" rather than rigorous engineering. Excellent for demos and throwaway prototypes. Dangerous for production systems because it accumulates technical debt and lacks production-ready features. [See Chapter 8](#chapter-8-myth-demos-equal-production-ready-reality-the-vibe-coding-gap).

---

*For more detailed explanations, see the chapter referenced with each term.*
