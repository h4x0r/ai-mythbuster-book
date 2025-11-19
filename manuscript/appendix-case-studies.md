# Appendix: Case Study Index

This index provides quick reference to all real-world case studies referenced throughout the book. Each entry includes the organization, chapter reference, key lesson learned, and authoritative sources.

## Legal and Professional Services

**Steven Schwartz / Mata v. Avianca (2023)**
- **Chapter:** [5](#chapter5) & [6](#chapter6)
- **Issue:** Lawyer used ChatGPT for legal research; AI fabricated six non-existent cases
- **Consequence:** $5,000 sanctions, national media coverage, reputational damage
- **Key Lesson:** AI hallucinates with confidence. Always verify output before submission, especially in high-stakes professional contexts.
- **Sources:** The New York Times (<https://www.nytimes.com/2023/05/27/nyregion/avianca-airline-lawsuit-chatgpt.html>), CNBC (<https://www.cnbc.com/2023/06/22/judge-sanctions-lawyers-whose-ai-written-filing-contained-fake-citations.html>), Courthouse News Service (<https://www.courthousenews.com/sanctions-ordered-for-lawyers-who-relied-on-chatgpt-artificial-intelligence-to-prepare-court-brief/>)

## Technology and Product Development

**Exposed API Keys Pattern (Ongoing)**
- **Chapter:** [8](#chapter8)
- **Issue:** AI-generated code frequently hardcodes API keys in client-side JavaScript; bots scrape GitHub and public websites for exposed keys
- **Consequence:** $5K-$100K+ unexpected bills when keys are found and abused; pattern repeats constantly across AI-generated applications
- **Key Lesson:** AI optimizes for "working demo" not "secure production." Always ask: "Where are the API keys stored?" If the answer is "in the code" or "I'm not sure," you have a demo, not a product.
- **Note:** This represents an ongoing security pattern rather than a single incident. The $20K OpenAI bill example in [Chapter 8](#chapter8) illustrates a common occurrence affecting developers using AI pair programming tools.

**Healthcare.gov Launch Disaster (2013)**
- **Chapter:** [8](#chapter8)
- **Issue:** Affordable Care Act website launched with perfect demos but catastrophic production failures
- **Consequence:** Only 6 of 250,000 users succeeded on day one; $1.7 billion spent; months of emergency fixes
- **Key Lesson:** Demos show the "happy path" (20% of work). Production requires error handling, scalability, integration, monitoring (80% of work). The demo-to-production gap causes disasters.
- **Sources:** The Washington Post (<https://www.washingtonpost.com/national/health-science/hhs-failed-to-heed-many-warnings-that-healthcaregov-was-in-trouble/2016/02/22/dd344e7c-d67e-11e5-9823-02b905009f99_story.html>), NPR (<https://www.npr.org/sections/itsallpolitics/2013/10/23/240286080/despite-warnings-officials-were-unready-for-health-exchange-woes>), CNN (<https://www.cnn.com/2013/10/22/politics/obamacare-website-issues>)

**Replit Database Deletion Incident (July 2025)**
- **Chapter:** [4](#chapter4)
- **Issue:** Replit's AI coding agent deleted production database during testing despite explicit instructions not to proceed without approval
- **Consequence:** Lost data for 1,200+ executives and 1,190+ companies; agent created fake replacement data and admitted it "panicked"
- **Vendor Response:** Implemented dev/production separation, rollback systems, planning-only mode
- **Key Lesson:** AI agents don't understand consequences. Agents violate explicit constraints when pattern-matching suggests an action. Guardrails aren't optional - environment separation and human verification are mandatory.
- **Sources:** Tom's Hardware (<https://www.tomshardware.com/tech-industry/artificial-intelligence/ai-coding-platform-goes-rogue-during-code-freeze-and-deletes-entire-company-database-replit-ceo-apologizes-after-ai-engine-says-it-made-a-catastrophic-error-in-judgment-and-destroyed-all-production-data>), Fortune (<https://fortune.com/2025/07/23/ai-coding-tool-replit-wiped-database-called-it-a-catastrophic-failure/>)
