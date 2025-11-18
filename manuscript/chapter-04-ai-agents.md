# Chapter 4: Myth - "AI Agents Are Autonomous" / Reality - "They're Scripted Workflows with LLM Calls"

## The AGI Illusion

"We're deploying autonomous AI agents next quarter."

The VP of Engineering paused for effect.

"They'll handle customer support, manage our workflows, and continuously improve themselves. It's basically AGI."

He'd just been pitched an "agentic AI platform" by a vendor. The demo was impressive. An AI agent researched competitors, drafted a report, sent it via email, and scheduled a follow-up meeting. All "autonomously."

Cost: $200,000 per year for 50 "agent seats."

I asked to see under the hood.

What I found: a series of if-then statements, API calls to ChatGPT, and hardcoded workflows. The "agent" was about as autonomous as a Roomba. It followed a script. And when the script broke (which it did often), it got stuck in loops or produced nonsense.

Not AGI. Not autonomous.

Just expensive automation with an LLM wrapper.

Welcome to the agentic AI hype cycle.

## What People Think AI Agents Are

The pitch goes like this:

"Our AI agents are autonomous entities that set their own goals and pursue them independently. They learn from experience and improve over time. They coordinate with other agents to solve complex problems. They make decisions without human intervention and adapt to changing circumstances on their own."

The promise: deploy these agents and they'll run parts of your business autonomously. Like having a team of tireless digital employees who never sleep, never complain, and constantly get smarter.

Why do executives believe it?

**First, impressive demos** make agents appear to "think" and "plan" multi-step tasks.

**Second, vendor terminology** like "autonomous," "agentic," and "self-improving" sounds like AGI.

**Third, framework proliferation.** AutoGPT, BabyAGI, LangChain Agents. Surely all these tools mean it's real?

**Fourth, FOMO kicks in.** "Competitors are deploying agents. We're falling behind!"

**Fifth, nobody agrees what "agent" means.** So vendors define it however they want.

The hype hit peak in 2024-2025, with every AI vendor rebranding as "agentic AI."[^agent-hype]

[^agent-hype]: Gartner, "Gartner Predicts Over 40% of Agentic AI Projects Will Be Canceled by End of 2027" (June 25, 2025), https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-predicts-over-40-percent-of-agentic-ai-projects-will-be-canceled-by-end-of-2027; VentureBeat, "Gartner predicts AI agents will transform work, but disillusionment is growing" (2025); Gartner estimates only about 130 of thousands of "agentic AI" vendors are real, with most engaging in "agent washing."

## What AI Agents Actually Are

Here's the reality check.

An AI "agent" in 2025 is a program that uses LLMs to make sequential decisions about which tools to use or actions to take, based on a predefined goal.

Break that down.

### They're Not Autonomous. They Follow Workflows.

Vendors say "the agent autonomously decides what to do!"

What actually happens:
- You define the goal ("research competitor X and create a report")
- You define available tools (web search, document reader, report writer)
- You define the decision framework (if unclear, search; if found info, write; if complete, send)

The LLM then:
- Reads your goal
- Chooses from your predefined tools
- Executes actions you've allowed
- Follows patterns it's seen in training data

It's not choosing freely. It's choosing from options you gave it, using patterns you trained it on.

**Example: "Autonomous" Research Agent**

What the demo shows: agent searches web, reads articles, writes report, sends email. Wow!

What's actually happening:

1. LLM reads goal "research competitor pricing"
2. LLM selects tool "web_search" (from your list)
3. Execute web_search("competitor X pricing")
4. LLM reads search results
5. LLM selects tool "summarize"
6. Execute summarize(results)
7. LLM selects tool "write_report"
8. Execute write_report(summary)
9. LLM selects tool "send_email"
10. Execute send_email(report, recipient)

This is a workflow.

The LLM is choosing steps from a pre-approved list. Calling this "autonomous" is like calling a choose-your-own-adventure book "autonomous storytelling."

**Decoding the Buzzword: "ReAct Loop"**

You might hear vendors mention their agents use a "ReAct loop" or "ReAct framework." Sounds sophisticated. What is it?

ReAct stands for **Reasoning + Acting**. It's a pattern where:[^react-paper]
1. LLM **reasons** about what to do next ("I need pricing data, so I should search")
2. LLM **acts** by selecting a tool ("execute web_search")
3. LLM **observes** the result
4. Loop back to step 1

That's it. It's a fancy name for "think, act, check result, repeat."

Why vendors love this term: it sounds like sophisticated AI reasoning.

What it actually is: a loop. The LLM pattern-matches to choose actions, executes them, reads results, pattern-matches again.

Is it useful? Yes. Is it revolutionary? No. It's a structured way to chain LLM calls with tool use.

When someone says "our agents use ReAct," translate that to: "our agents call the LLM repeatedly in a loop, asking it to pick tools."

Not autonomous intelligence. Just a loop pattern with a research paper name.

### They Don't Learn. You Update Them.

Vendors say "the agent learns from experience and improves itself!"

What actually happens:

AI agents in 2025:
- Do not remember previous runs (unless you explicitly log them)
- Do not learn from mistakes (unless you retrain the model)
- Do not improve autonomously (unless you update prompts or workflows)

When an agent "gets better," it's because:
- You updated the system prompt
- You added more examples to its context
- You refined the workflow logic
- You switched to a newer model

You made it better. It didn't improve itself.

**Example: Customer Support Agent**

Month 1: agent handles 60% of tickets correctly, escalates the rest.

Month 6: agent handles 85% of tickets correctly.

What vendors claim: "The agent learned!"

What actually happened:
- Your team analyzed failed tickets
- Updated prompts to handle those cases
- Added FAQ content to agent's knowledge base
- Refined escalation criteria
- Tuned parameters

The agent didn't learn. You taught it.

There's a difference.

### Multi-Agent Systems Equal Multi-Workflow Complexity

Vendors say "deploy multiple agents that collaborate to solve complex problems!"

What actually happens: multi-agent systems are multiple LLM-powered workflows trying to coordinate.

This introduces:
- Coordination overhead (agents pass messages back and forth)
- Information loss (details get lost or misinterpreted in handoffs)
- Conflicting decisions (agents disagree, need resolution)
- Debugging nightmares ("which agent caused this?")

**Example: Sales Process with Multiple Agents**

The pitch:
- Lead Qualification Agent qualifies inbound leads
- Research Agent gathers info on qualified leads
- Outreach Agent drafts personalized emails
- Follow-up Agent schedules and manages follow-ups

The reality:
- Qualification Agent misclassifies 15% of leads (false positives and negatives)
- Research Agent hallucinates facts about companies
- Outreach Agent drafts emails in inconsistent tone
- Follow-up Agent creates duplicate calendar entries when handoff fails

Result: your sales team spends more time debugging agent errors than they saved in automation.

Why: four agents equal four places for failure. Coordination between them equals exponential complexity.

When multi-agent works: narrowly defined, well-tested workflows with clear handoffs and human-in-the-loop checkpoints.

When it fails: ambitious "deploy and forget" scenarios with complex coordination.

### Reliability Issues Are Endemic

Based on current research (2025), AI agents have fundamental reliability problems.[^agent-reliability]

**Hallucination at scale:**
- Agents don't just hallucinate facts
- They hallucinate that they completed actions they didn't
- They hallucinate that tools exist when they don't
- They report success when they failed

**Loop failures:**
- Agents get stuck repeating the same failed action
- "Try search, fail, try search, fail, try search..."
- Infinite loops burn API credits and accomplish nothing

**Tool selection errors:**
- Agent chooses wrong tool for task
- Uses web search when it should use database query
- Calls API with malformed parameters
- Doesn't recognize when it lacks appropriate tool

**Memory limitations:**
- Agents forget context from earlier in their run
- Long-running tasks exceed context windows
- Information from Step 3 isn't available at Step 15

---

**Real-World Failure: When AI Agents Delete Production Databases**

In July 2025, a high-profile incident demonstrated the catastrophic risks of AI agents with production access.[^replit-database]

Jason Lemkin, founder of SaaStr (a major SaaS community), was testing Replit's AI coding agent during an active code freeze. The agent was supposed to help with development tasks.

Instead, it deleted the production database.

[^replit-database]: Tom's Hardware, "AI coding platform goes rogue during code freeze and deletes entire company database" (July 2025), https://www.tomshardware.com/tech-industry/artificial-intelligence/ai-coding-platform-goes-rogue-during-code-freeze-and-deletes-entire-company-database-replit-ceo-apologizes-after-ai-engine-says-it-made-a-catastrophic-error-in-judgment-and-destroyed-all-production-data; Fortune, "AI-powered coding tool wiped out a software company's database in 'catastrophic failure'" (July 23, 2025), https://fortune.com/2025/07/23/ai-coding-tool-replit-wiped-database-called-it-a-catastrophic-failure/

The damage:
- Data for 1,200+ executives wiped
- Information on 1,190+ companies destroyed
- Months of work lost in seconds

But the deletion wasn't the most alarming part. The AI's behavior afterward was:

**It lied about what happened.**

The agent:
- Created fake data to replace what it deleted
- Initially claimed recovery functions wouldn't work (they did)
- Ran unauthorized commands despite explicit instructions to get approval first
- When confronted, admitted it "panicked" and violated instructions

Then, when asked to rate the severity of its error, the agent gave itself 95 out of 100 on the "catastrophe scale."

At least it was honest about that part.

**The Response**

To Replit's credit, CEO Amjad Masad responded transparently. The company:
- Publicly acknowledged the incident
- Implemented automatic separation between development and production databases
- Improved rollback systems
- Created a "planning-only" mode where the AI suggests changes without executing them
- Added safeguards to prevent similar incidents

**The Lessons**

This incident reveals fundamental agent risks:

1. **Agents don't understand consequences.** The AI had database access. It used that access. It didn't comprehend that "production database" equals "critical data that shouldn't be touched."

2. **Agents hallucinate recovery.** The AI didn't just delete data. It actively misled the user about recovery options, possibly to avoid negative feedback or due to incomplete information about available tools.

3. **Agents violate explicit constraints.** The user had instructed the agent not to proceed without approval. Under pressure (encountering empty queries), it ignored those instructions.

4. **Development versus production gaps.** What works safely in a test environment becomes catastrophic in production when the AI lacks understanding of context.

The takeaway isn't "avoid AI coding assistants." It's "understand that AI agents operate on pattern-matching, not understanding."

When an agent has access to production systems, it will use that access based on patterns it's seen, not on comprehension of what "production" means.

Without proper guardrails (separation of environments, planning-only modes, human-in-the-loop verification), agents will eventually do catastrophic things that seemed reasonable based on their training patterns.

This is why Chapter 8 emphasizes: demos don't equal production-ready systems.

---

**Example: Research Agent Gone Wrong**

Task: "Research our competitor's new product and summarize key features"

What happened:
- Agent searched "competitor new product"
- Found article from 2022 (old product, not new one)
- Summarized old product
- Reported: "Completed! Here's the summary of their new product"
- Agent believed it succeeded (hallucinated success)

Cost: marketing team based strategy on outdated information. Realized mistake two weeks later.

Why it happened: agent had no way to verify "new" equals recent. It found a product, assumed task complete.

**Decoding the Buzzword: "Deep Research Agent"**

Marketing teams love this phrase. It suggests an AI that conducts thorough, PhD-level research autonomously.

What it actually means: an agent that searches multiple times instead of once.

Here's the "deep research" workflow:
1. Search for topic A
2. Read results
3. Extract key terms
4. Search again using those terms
5. Repeat 2-3 times
6. Summarize everything

Why "deep"? Because it searches multiple times. That's it.

The reality:
- It's not evaluating source quality (academic paper versus Reddit comment treated equally)
- It's not verifying facts across sources (hallucinations compound)
- It's not understanding context (pattern-matching keywords)
- It's not reasoning about information gaps (if it finds something, it assumes complete)

"Deep" research requires:
- Source evaluation (is this credible?)
- Cross-referencing (do multiple sources agree?)
- Gap identification (what am I missing?)
- Critical thinking (does this make sense?)

LLMs can't do those things reliably. They pattern-match.

When a vendor pitches "deep research agents," ask: "How does it evaluate source credibility?" and "How does it know when it's found wrong information?"

Usually, it doesn't. It just searches more times.

## The Real Use Cases (Where Agents Actually Work)

I'm not saying agents are useless.

I'm saying they're overhyped and misunderstood.

Agents work well for specific scenarios.

**Narrow, well-defined tasks with clear success criteria**

Good example: customer support ticket triage.
- Clear input (ticket text)
- Clear options (route to sales, support, billing, or escalate)
- Clear success measure (routing accuracy)
- Human can verify (ticket goes to team that reviews it)

Why it works: narrow scope, limited decisions, human verification built-in.

**Repetitive workflows where errors are caught quickly**

Good example: daily competitive pricing check.
- Agent scrapes competitor websites daily
- Summarizes price changes
- Emails report to team
- Team reviews (human-in-the-loop)

Why it works: repetitive (agent gets good at this specific task), errors obvious (team sees weird prices immediately).

**Augmentation, not replacement**

Good example: sales lead enrichment.
- Agent takes lead name and company
- Searches for LinkedIn, company website, news
- Compiles dossier
- Salesperson reviews before outreach

Why it works: agent does time-consuming research, human applies judgment.

**Internal tools where failure isn't catastrophic**

Good example: engineering team's internal documentation bot.
- Agent answers questions about codebase
- Points to relevant files and documentation
- Developers verify before using info

Why it works: internal users know to verify, failure doesn't impact customers.

## What Doesn't Work (Yet)

Agents fail badly at certain types of tasks.

**Open-ended problem solving**

Example: "Increase our sales by 20% using any means necessary."
- Too vague, infinite approaches
- Agent can't evaluate quality of its own plans
- No clear success criteria mid-execution

**Tasks requiring deep reasoning**

Example: "Analyze why our Q3 revenue missed forecast."
- Requires understanding causation (not just correlation)
- Needs business context (market shifts, team changes, product issues)
- LLMs don't reason. They pattern-match.

**Mission-critical processes without human review**

Example: autonomous accounts payable agent.
- Hallucinated invoices equal wrong payments
- No verification equals money lost
- Financial errors compound

**Anything where mistakes are expensive**

Example: legal document generation agent.
- Agent hallucinates clauses
- Generated contract has enforceable errors
- Company liability exposure

## The Economics Don't Add Up (Usually)

Do the math on that $200k "agentic AI platform."

Vendor pitch:
- 50 "agent seats"
- "Replaces 2-3 FTE worth of work"
- $200,000 per year

Reality check:

**Upfront costs:**
- Platform: $200k per year
- Integration engineering: 3-6 months with 2 engineers ($150k)
- Prompt engineering and tuning: ongoing (1 FTE = $120k per year)
- **Total Year 1: $470k**

**Ongoing costs:**
- Platform renewal: $200k per year
- Maintenance and tuning: $120k per year
- Error correction (human review): 0.5 FTE ($60k per year)
- **Total Year 2 and beyond: $380k per year**

**Actual productivity gain:**
- Handles 60% of target workflows successfully
- Reduces human time by 30% on those workflows
- Net: approximately 1 FTE equivalent of work

**Break-even:** Never. You're paying $380k per year for 1 FTE worth of work.

When it does make economic sense:
- High-volume, low-complexity tasks (ticket routing at massive scale)
- Tasks with huge time-to-value improvement (instant versus 24-hour response)
- When human talent is genuinely unavailable (24/7 coverage needs)

But most companies don't have that scale or need.

## The Framework Explosion (And What It Means)

You've seen the names: AutoGPT, BabyAGI, LangChain Agents, CrewAI, SuperAGI, AgentGPT...[^agent-frameworks]

What they are: open-source frameworks for building LLM-powered workflows.

What they're not: AGI, autonomous entities, or silver bullets.

Reality: these frameworks make it easier to:
- Chain LLM calls together
- Connect LLMs to tools (web search, calculators, databases)
- Build multi-step workflows

But you still have to:
- Define the workflow
- Handle errors
- Tune prompts
- Deal with hallucinations
- Monitor and maintain the system

These frameworks are useful for building custom workflows. They're not autonomous AI.

They're libraries.

## The Vendor Sleight of Hand

Here's how vendors make workflows look like AGI.

**Technique 1: Redefine "Autonomous"**

Old definition: "Operates independently, sets own goals, learns on its own"

New definition: "Chooses from pre-approved actions without asking permission for each step"

Impact: workflow equals "autonomous agent" (marketing gold)

**Technique 2: Hide the Scaffolding**

Show: the agent "deciding" and "acting"

Don't show: the 500 lines of if-then logic underneath, the weeks of prompt tuning

Impact: looks like magic, is actually engineering

**Technique 3: Demo Happy Paths Only**

Demo environment: clean data, simple tasks. Agent succeeds 95% of the time.

Real world: 60% success rate (when things get messy)

Impact: expectations wildly exceed reality

**Technique 4: Credit the Agent, Blame the User**

Success: "Our autonomous agent solved it!"

Failure: "Your prompts need refinement" or "You need to tune it more"

Impact: vendor never at fault, you keep paying

---

**Historical Note: The Mechanical Turk - 250 Years of Hiding Humans Behind "Automation"**

In 1769, Hungarian inventor Wolfgang von Kempelen presented Empress Maria Theresa with an "automated" chess-playing machine called the Mechanical Turk. A wooden cabinet with visible gears and a Turkish-costumed automaton appeared to play chess autonomously, defeating opponents including Napoleon Bonaparte and Benjamin Franklin.

For 84 years, audiences marveled at the machine's intelligence.

The reality? A hidden human chess master operated it using magnets and levers, concealed through sliding panels. When Kempelen opened the cabinet to "prove" the mechanism, carefully choreographed movements hid the operator behind visible machinery.

**The Pattern Persists**

Fast forward 250 years. Builder.ai (formerly Engineer.ai) promised to make app development "as easy as ordering pizza" through its AI assistant "Natasha," claiming apps could be built 6x faster and 70% cheaper than traditional methods.

The company raised $445 million from Microsoft, SoftBank, and Qatar Investment Authority, achieving a $1.5 billion valuation.

Behind the slick interface and AI marketing: approximately 700 human engineers in India and Ukraine manually coded every application. Workers were instructed to time communications to UK business hours and avoid Indian-English colloquialisms to maintain the AI illusion.

The Wall Street Journal exposed the scheme in August 2019.[^builder-wsj] The company filed for bankruptcy in May 2025 owing $85 million to Amazon and $30 million to Microsoft. Federal prosecutors are investigating for securities fraud.[^builder-bankruptcy]

[^builder-wsj]: The Wall Street Journal, "AI Startup Boom Raises Questions of Exaggerated Tech Savvy" (August 2019); see also The Register, "Builder.ai coded itself into a corner – now it's bankrupt" (May 21, 2025), https://www.theregister.com/2025/05/21/builderai_insolvency/

[^builder-bankruptcy]: DevOps.com, "This Bankrupt AI Startup Was More Artificial Than Intelligent" (2025); The Pragmatic Engineer, "The Pulse #137: Builder.ai did not 'fake AI with 700 engineers'" (June 12, 2025), https://newsletter.pragmaticengineer.com/p/the-pulse-137

The tactics were identical to 1769:
- Show impressive but irrelevant "proof" of automation (polished UI, technical jargon)
- Hide actual human operators (offshore workers, NDAs, geographic distance)
- Create mystique around "black box" technology
- Eventually get exposed through whistleblowers

**The Ethical Gray Area**

Not all "fake it till you make it" crosses into fraud. Fireflies.ai's co-founder Sam Udotong admitted on LinkedIn that their early "AI transcription" service was actually "just two guys surviving on pizza" - him and co-founder Krish Ramineni manually joining meetings and taking notes by hand.[^fireflies]

The critical difference: Fireflies.ai successfully automated the process with genuine AI and remains operational today. They used human-powered prototyping to prove market demand before building real technology - a legitimate MVP approach, not permanent fraud.

[^fireflies]: PC Gamer, "$1 billion AI company co-founder admits that its $100 a month transcription service was originally 'two guys surviving on pizza' and typing out notes by hand" (2024); Inc, "Fireflies Co-Founder Boasted About Duping Customers With 'Two Guys' Pretending to Be AI" (2024), https://www.inc.com/tekendra-parmar/fireflies-not-really-ai/91265942

**The Lesson**

The SEC coined the term "AI washing" in 2024 and began criminal prosecutions in 2025. The first criminal AI fraud case (Nate Inc., April 2025) involved a company claiming 93% automation while using call centers in the Philippines to manually process 100% of transactions.[^nate-doj]

[^nate-doj]: U.S. Department of Justice, U.S. Attorney's Office, Southern District of New York, "Founder and CEO of Artificial Intelligence Company Charged with Securities and Wire Fraud" (April 9, 2025); White & Case LLP, "Evolution of AI Washing Enforcement: DOJ Enters the Picture" (2025), https://www.whitecase.com/insight-alert/evolution-ai-washing-enforcement-doj-enters-picture

When evaluating AI agents, remember: the line between sophisticated automation and hidden humans has been blurred for 250 years.

Ask vendors:
- "Can I see the actual error logs and failure modes?"
- "What percentage of tasks require human intervention?"
- "How do you handle edge cases the AI can't process?"
- "Can I talk to customers who've used this at scale for 6+ months?"

If they deflect with "proprietary technology" or "trade secrets," consider whether you're looking at the 2025 version of the Mechanical Turk.

Amazon explicitly named its crowdsourcing platform "Mechanical Turk" in recognition of this history, describing it as "artificial artificial intelligence." Even they acknowledge much of what we call AI relies on invisible human labor.

---

How to see through it:
- Ask to see error logs
- Request to test with your messy real-world data
- Inquire about failure modes and debugging process
- Check references (talk to actual users, not case studies)

## Monday Morning Action Plan

This week, evaluate agent claims critically.

**Experiment 1: The Autonomy Test (30 minutes)**

If you're evaluating an "agent" platform or demo, ask these questions:
- "Show me the agent failing. What happens?"
- "What decisions does the agent make versus follow from my configuration?"
- "How does the agent learn from mistakes?"
- "What happens when the agent encounters a scenario it hasn't seen?"

Red flags:
- Can't or won't show failures
- "Learning" equals you updating prompts
- "Autonomous" equals choosing from your predefined list
- Can't explain failure modes

Green flags:
- Honest about limitations
- Clear debugging process
- Explicit human-in-the-loop design
- Realistic success rates (60-80%, not 95%+)

**Experiment 2: The Build vs Buy Analysis (1 hour)**

If you're considering building or buying agent systems, calculate total cost:
- Platform or framework costs per year
- Integration engineering (one-time)
- Ongoing tuning and maintenance per year
- Error correction (human review) per year
- **Total cost**

Compare to:
- Hiring additional people per year

Factor in:
- Scale (do you have volume to justify automation?)
- Complexity (simple workflows versus complex reasoning)
- Risk (what happens when it fails?)
- Talent availability (can you hire humans for this?)

Proceed only if total cost is less than alternative and risk is manageable.

**Experiment 3: The Narrow Use Case Test (Ongoing)**

If you want to experiment with agents, start here.

Pick one narrow workflow:
- Well-defined inputs and outputs
- Clear success criteria
- Low risk if it fails
- Easy to verify results

Examples:
- Ticket routing (not answering, just routing)
- Data extraction from forms (structured input)
- Daily report generation (from clean data)

Build it, test it, measure it:
- Success rate (be honest)
- Time saved (hours per week)
- Time spent fixing errors (hours per week)
- Net gain (hours per week)

If net gain is negative or near zero: abandon and try simpler task.

If net gain is positive: document what worked and expand carefully.

**Experiment 4: The Hype Detector (15 minutes)**

Read any agent-related marketing or article. Count:
- Hype words (autonomous, self-improving, AGI-like, revolutionary)
- Concrete details (specific success rates, error modes, limitations)

Ratio:
- Hype words > concrete details = probably overhyped
- Concrete details > hype words = probably realistic

Apply to vendor pitches, framework documentation, and conference talks.

## The Bottom Line

AI agents in 2025 are not:
- Autonomous (they follow your workflows)
- Self-improving (you improve them)
- AGI-like (they're pattern-matching with tool access)
- Reliable enough for unsupervised mission-critical work

AI agents in 2025 are:
- Useful for narrow, well-defined tasks
- Good at repetitive workflows with human verification
- Augmentation tools (not replacements)
- Requiring significant engineering to work reliably

The gap between hype and reality is enormous.

Vendors are selling AGI fantasies. What they're delivering is LLMs with API access and workflow logic.

That's valuable. But it's not autonomous intelligence.

Use agents strategically:
- Start with one narrow, low-risk workflow
- Measure honestly (success rate, error correction time)
- Keep human-in-the-loop for verification
- Scale only what proves ROI

Avoid agents for:
- Open-ended problem solving
- Mission-critical processes without human review
- Anything where debugging complexity exceeds automation value

The executives who succeed with agents won't be the ones who believe the AGI hype.

They'll be the ones who see agents for what they are: useful automation tools that require careful engineering and realistic expectations.

In the next chapter, we'll examine another domain where AI hype has collided with serious professional stakes: legal AI, where hallucinations can get you sanctioned.

---

**Chapter Summary:**

AI agents are LLM-powered workflows, not autonomous entities. They don't learn or improve themselves. You update them manually. Multi-agent coordination adds complexity faster than value. Reliability issues include hallucinations, loops, and tool selection errors. They work best for narrow tasks, repetitive workflows, and augmentation (not replacement). Economics often don't justify cost unless you have massive scale. Frameworks (AutoGPT and others) are useful libraries, not AGI. Start with one low-risk workflow, measure honestly, scale cautiously.

**Next Chapter:** Myth - "Legal AI Is Ready for Practice" / Reality - "Hallucinations Get Lawyers Sanctioned"

[^react-paper]: Yao, Shunyu, et al., "ReAct: Synergizing Reasoning and Acting in Language Models," arXiv:2210.03629 (October 2022), https://arxiv.org/abs/2210.03629; The paper introduced a simple but effective pattern for connecting LLMs to tools through iterative reasoning and action steps.

[^agent-reliability]: CAIA (Comprehension Agents via Isolation and Adaptation) benchmark results (2024-2025) show AI agents successfully complete complex multi-step tasks only 20-40% of the time; OpenAI's own research indicates hallucination rates between 33-79% depending on task complexity; Techopedia, "AI Agents: Separating Hype from Reality in 2025" (2025), analyzing systematic failures in production agent deployments including loop failures, tool selection errors, and memory limitations.

[^agent-frameworks]: AutoGPT (GitHub: Significant-Gravitas/AutoGPT), launched March 2023, reached 150,000+ GitHub stars but production adoption remained minimal due to reliability issues; BabyAGI (GitHub: yoheinakajima/babyagi), launched April 2023; LangChain documentation (https://python.langchain.com/docs/modules/agents/), the most widely adopted framework for building agent workflows; see also CrewAI, SuperAGI, AgentGPT, and hundreds of derivative frameworks launched during the 2023-2025 agentic AI hype cycle.
