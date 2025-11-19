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

## AI Washing and Fraud

**Builder.ai / Engineer.ai "AI Washing" (2019-2025)**
- **Chapter:** [4](#chapter4)
- **Issue:** Promised apps "6x faster and 70% cheaper" through AI assistant "Natasha"; reality was 700 human engineers in India and Ukraine manually coding everything
- **Consequence:** Raised $445M from Microsoft, SoftBank, Qatar at $1.5B valuation; exposed by Wall Street Journal in August 2019; filed bankruptcy May 2025 owing $85M to Amazon and $30M to Microsoft; federal securities fraud investigation
- **Key Lesson:** "AI washing" - vendors claiming AI automation while using hidden human labor. Verify actual automation levels, ask for error logs, request customer references with 6+ months usage.
- **Sources:** The Wall Street Journal, "AI Startup Boom Raises Questions of Exaggerated Tech Savvy" (August 2019), The Register (<https://www.theregister.com/2025/05/21/builderai_insolvency/>), The Pragmatic Engineer (<https://newsletter.pragmaticengineer.com/p/the-pulse-137>)

**Fireflies.ai Early MVP Approach (2024)**
- **Chapter:** [4](#chapter4)
- **Issue:** Co-founder admitted early "AI transcription" service was "just two guys surviving on pizza" manually joining meetings and typing notes
- **Consequence:** Public admission caused controversy but company survived; successfully automated with genuine AI and grew to $1 billion valuation
- **Key Lesson:** Ethical gray area between legitimate MVP testing (manual before automating) vs permanent fraud (Builder.ai). Fireflies represents acceptable "fake it till you make it" approach - started manual, delivered real AI automation.
- **Sources:** PC Gamer, "$1 billion AI company co-founder admits that its $100 a month transcription service was originally 'two guys surviving on pizza' and typing out notes by hand" (2024), Inc (<https://www.inc.com/tekendra-parmar/fireflies-not-really-ai/91265942>)
