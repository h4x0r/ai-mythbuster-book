# Appendix: Case Study Index

This index provides quick reference to all real-world case studies referenced throughout the book. Each entry includes the organization, chapter reference, and key lesson learned.

## Legal and Professional Services

**Steven Schwartz / Mata v. Avianca (2023)**
- **Chapter:** 5 & 6
- **Issue:** Lawyer used ChatGPT for legal research; AI fabricated six non-existent cases
- **Consequence:** $5,000 sanctions, national media coverage, reputational damage
- **Key Lesson:** AI hallucinates with confidence. Always verify output before submission, especially in high-stakes professional contexts.

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
