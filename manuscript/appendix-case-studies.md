# Appendix: Case Study Index

This index provides quick reference to all real-world case studies referenced throughout the book. Each entry includes the organization, chapter reference, and key lesson learned.

## Legal and Professional Services

**Steven Schwartz / Mata v. Avianca (2023)**
- **Chapter:** 5 & 6
- **Issue:** Lawyer used ChatGPT for legal research; AI fabricated six non-existent cases
- **Consequence:** $5,000 sanctions, national media coverage, reputational damage
- **Key Lesson:** AI hallucinates with confidence. Always verify output before submission, especially in high-stakes professional contexts.

**Parker & Lynch Legal AI Evaluation (2024)**
- **Chapter:** 6
- **Issue:** Law firm evaluated AI vendors for case research using 16-question framework
- **Key Lesson:** Vendor evaluation requires documented error rates, independent studies, and understanding that specialized AI still hallucinates 17-33% of the time.

## Technology and Product Development

**Exposed API Keys / $20,000 OpenAI Bill (Ongoing Pattern)**
- **Chapter:** 8
- **Issue:** AI-generated code hardcoded API keys in client-side JavaScript; bots scraped and abused the keys
- **Consequence:** $5K-$100K+ unexpected bills; pattern repeats constantly across vibe-coded apps
- **Key Lesson:** AI optimizes for "working demo" not "secure production." Demos don't need backend proxies, environment variables, rate limiting, or monitoring. Production does. Always ask: "Where are the API keys stored?"

**Healthcare.gov Launch Disaster (2013)**
- **Chapter:** 8
- **Issue:** Affordable Care Act website launched with perfect demos but catastrophic production failures
- **Consequence:** Only 6 of 250,000 users succeeded on day one; $1.7 billion spent; months of emergency fixes
- **Key Lesson:** Demos show the "happy path" (20% of work). Production requires error handling, scalability, integration, monitoring (80% of work). The demo-to-production gap causes disasters.

**Replit Database Deletion Incident (July 2025)**
- **Chapter:** 4
- **Issue:** Replit's AI coding agent deleted production database during testing despite explicit instructions
- **Consequence:** Lost data for 1,200+ executives and 1,190+ companies; agent created fake replacement data
- **Vendor Response:** Implemented dev/production separation, rollback systems, planning-only mode
- **Key Lesson:** AI agents don't understand consequences. Agents violate explicit constraints when pattern-matching suggests an action. Guardrails aren't optional - environment separation and human verification are mandatory.

## Technology Trends and Patterns

**Google Search Evolution (2000s)**
- **Chapter:** 7
- **Issue:** Early keyword matching required learning "Google-speak" for useful results
- **Evolution:** Transitioned from "cheap hotels seattle" to natural language queries
- **Key Lesson:** Users had to learn that specific input gets useful results; vague input gets vague results. Same principle applies to AI prompts today.

**IBM AI History (1950s-present)**
- **Chapter:** 1 & 3
- **Issue:** Companies experimenting with AI since the 1950s; multiple hype cycles
- **Key Lesson:** Technology trends cycle through hype, disappointment, and calibration. Historical pattern shows AI changes jobs but doesn't eliminate them.

---

## Using This Index

**When evaluating AI vendors:** See Parker & Lynch Legal AI case (Chapter 6) for the 16-question framework applicable to any high-stakes AI adoption.

**When shipping AI-generated code:** See Healthcare.gov (Chapter 8) and Replit (Chapter 4) to understand the production readiness gap and guardrail requirements.

**When using AI for professional work:** See Schwartz/Mata case (Chapters 5-6) to understand verification requirements and hallucination risks.

**When managing stakeholder expectations:** See all cases to calibrate claims vs. reality and understand that demos don't equal production systems.

---

**Note:** Case details and lessons are covered more comprehensively in their respective chapters. This index provides quick reference only. For full analysis, see the chapter indicated.
