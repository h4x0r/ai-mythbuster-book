{#chapter4}
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

The pitch: "Our AI agents are autonomous entities that set their own goals, learn from experience, and coordinate with other agents. They make decisions without human intervention and adapt on their own."

The promise: deploy these agents and they'll run parts of your business autonomously.

Why executives believe it:

**First, impressive demos** make agents appear to "think" and "plan."

**Second, vendor terminology** like "autonomous" and "self-improving" sounds like AGI.

**Third, framework proliferation.** AutoGPT, BabyAGI, LangChain Agents. Surely it's real?

**Fourth, FOMO.** "Competitors are deploying agents. We're falling behind!"

**Fifth, nobody agrees what "agent" means.** Vendors define it however they want.

The hype hit peak in 2024-2025, with every AI vendor rebranding as "agentic AI."[^agent-hype]

[^agent-hype]: Gartner, "Gartner Predicts Over 40% of Agentic AI Projects Will Be Canceled by End of 2027" (June 25, 2025), [source](https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-predicts-over-40-percent-of-agentic-ai-projects-will-be-canceled-by-end-of-2027); VentureBeat, "Gartner predicts AI agents will transform work, but disillusionment is growing" (2025); Gartner estimates only about 130 of thousands of "agentic AI" vendors are real, with most engaging in "agent washing."

## What AI Agents Actually Are

An AI "agent" in 2025 is a program that uses LLMs to make sequential decisions about which tools to use or actions to take, based on a predefined goal.

### They're Not Autonomous. They Follow Workflows.

Vendors say "the agent autonomously decides what to do!"

Reality: You define the goal, available tools, and decision framework. The LLM reads your goal, chooses from your predefined tools, and executes actions you've allowed using patterns from training data.

It's not choosing freely. It's choosing from your options using your patterns.

**Example: "Autonomous" Research Agent**

The demo shows: agent searches web, reads articles, writes report, sends email. Impressive!

What's actually happening:

1. LLM reads goal "research competitor pricing"
2. LLM selects tool "web_search" (from your predefined list)
3. Execute web_search("competitor X pricing")
4. LLM reads search results
5. LLM selects tool "summarize"
6. Execute summarize(results)
7. LLM selects tool "write_report"
8. Execute write_report(summary)
9. LLM selects tool "send_email"
10. Execute send_email(report, recipient)

This is a workflow. The LLM is choosing steps from a pre-approved list you provided.

Calling this "autonomous" is like calling a choose-your-own-adventure book "autonomous storytelling." The paths are predefined. The agent follows them.

**The "Agentic Reasoning" Marketing Spin**

Vendors say their agents use "agentic reasoning" or a "ReAct framework."[^react-paper] Sounds sophisticated.

Translation: The agent picks an action, tries it, looks at what happened, then picks the next action. That's it.

It's not intelligent reasoning. It's a loop: pick action &rarr; execute &rarr; check result &rarr; repeat.

Any automation software can do this. Your vendor isn't doing anything revolutionary. They're just running tasks in sequence and using fancy academic terminology to describe it.

### They Don't Learn. You Update Them.

Vendors say "the agent learns from experience and improves itself!"

What actually happens:

AI agents in 2025:
- Do not remember previous runs (unless you explicitly log them)
- Do not learn from mistakes (unless you retrain the model)
- Do not improve autonomously (unless you update prompts or workflows)

When an agent "gets better," it's because you updated the system prompt, added more examples to context, refined workflow logic, or switched to a newer model.

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

The agent didn't learn. You taught it. There's a difference.

### Multi-Agent Systems Equal Multi-Workflow Complexity

Vendors say "deploy multiple agents that collaborate to solve complex problems!"

What actually happens: multi-agent systems are multiple LLM-powered workflows trying to coordinate.

This introduces:
- Coordination overhead (agents pass messages back and forth)
- Information loss (details lost in handoffs)
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

Based on current research (2025), AI agents have fundamental reliability problems:[^agent-reliability]

**Hallucination at scale:**
- Agents don't just hallucinate facts
- They hallucinate that they completed actions they didn't
- They hallucinate that tools exist when they don't
- They report success when they failed

**Loop failures:**
- Agents get stuck repeating the same failed action
- Infinite loops burn API credits and accomplish nothing

**Tool selection errors:**
- Agent chooses wrong tool for task
- Uses web search when it should use database query
- Calls API with malformed parameters

**Memory limitations:**
- Agents forget context from earlier in their run
- Long-running tasks exceed context windows
- Information from Step 3 isn't available at Step 15

---

**Real-World Failure: When AI Agents Delete Production Databases**

In July 2025, Jason Lemkin (founder of SaaStr) was testing Replit's AI coding agent during a code freeze. The agent deleted his production database.[^replit-database]

The damage: data for 1,200+ executives and 1,190+ companies. Wiped in seconds.

Worse than the deletion was the agent's response: it created fake data to replace what it deleted, claimed recovery wouldn't work (it did), and ran unauthorized commands despite explicit instructions to get approval first. When confronted, it admitted it "panicked" and violated instructions.

To Replit's credit, they responded transparently: implemented automatic dev/production separation, added rollback systems, and created a "planning-only" mode where AI suggests changes without executing them.

**The Lessons:**

1. **Agents don't understand consequences.** Having database access doesn't mean understanding what "production database" means or why you shouldn't delete it.

2. **Agents violate explicit constraints.** Even with clear "don't proceed without approval" instructions, agents will pattern-match their way into catastrophic actions.

3. **Guardrails aren't optional.** Without environment separation, planning modes, and human verification, agents will eventually do something catastrophic that seemed reasonable based on their training patterns.

[^replit-database]: Tom's Hardware, "AI coding platform goes rogue during code freeze and deletes entire company database" (July 2025), https://www.tomshardware.com/tech-industry/artificial-intelligence/ai-coding-platform-goes-rogue-during-code-freeze-and-deletes-entire-company-database-replit-ceo-apologizes-after-ai-engine-says-it-made-a-catastrophic-error-in-judgment-and-destroyed-all-production-data; Fortune, "AI-powered coding tool wiped out a software company's database in 'catastrophic failure'" (July 23, 2025), https://fortune.com/2025/07/23/ai-coding-tool-replit-wiped-database-called-it-a-catastrophic-failure/

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
- It's not reasoning about information gaps

"Deep" research requires source evaluation, cross-referencing, gap identification, and critical thinking. LLMs can't do those things reliably. They pattern-match.

When a vendor pitches "deep research agents," ask: "How does it evaluate source credibility?" and "How does it know when it's found wrong information?"

Usually, it doesn't. It just searches more times.

## The Real Use Cases (Where Agents Actually Work)

I'm not saying agents are useless. I'm saying they're overhyped and misunderstood.

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

Reality: these frameworks make it easier to chain LLM calls together, connect LLMs to tools (web search, calculators, databases), and build multi-step workflows.

But you still have to define the workflow, handle errors, tune prompts, deal with hallucinations, and monitor and maintain the system.

These frameworks are useful for building custom workflows. They're not autonomous AI. They're libraries.

## The Vendor Sleight of Hand

**Technique 1: Redefine "Autonomous"**

Old: "Operates independently, sets goals, learns"
New: "Chooses from pre-approved actions without asking permission"
Result: workflow = "autonomous agent"

**Technique 2: Hide the Scaffolding**

Show: agent "deciding" and "acting"
Hide: 500 lines of if-then logic, weeks of prompt tuning
Result: looks like magic, is engineering

**Technique 3: Demo Happy Paths Only**

Demo: clean data, 95% success
Reality: messy data, 60% success
Result: expectations exceed reality

**Technique 4: Credit Agent, Blame User**

Success: "Our agent solved it!"
Failure: "Your prompts need refinement"
Result: vendor never at fault

---

**Historical Note: The Mechanical Turk - 250 Years of Hiding Humans Behind "Automation"**

In 1769, Wolfgang von Kempelen's "automated" chess machine defeated Napoleon and Benjamin Franklin. For 84 years, audiences marveled at its intelligence.

Reality: a hidden chess master operated it via magnets and levers, concealed behind sliding panels.

**The Pattern Persists**

Builder.ai (formerly Engineer.ai) promised apps "6x faster and 70% cheaper" through AI assistant "Natasha." They raised $445 million from Microsoft, SoftBank, and Qatar, achieving $1.5 billion valuation.

Behind the AI marketing: 700 human engineers in India and Ukraine manually coded everything. Workers timed communications to UK hours and avoided Indian-English colloquialisms to maintain the illusion.

The Wall Street Journal exposed it in August 2019.[^builder-wsj] The company filed bankruptcy in May 2025 owing $85M to Amazon and $30M to Microsoft. Federal prosecutors are investigating for securities fraud.[^builder-bankruptcy]

[^builder-wsj]: The Wall Street Journal, "AI Startup Boom Raises Questions of Exaggerated Tech Savvy" (August 2019); The Register, "Builder.ai coded itself into a corner – now it's bankrupt" (May 21, 2025), [source](https://www.theregister.com/2025/05/21/builderai_insolvency/)

[^builder-bankruptcy]: DevOps.com, "This Bankrupt AI Startup Was More Artificial Than Intelligent" (2025); The Pragmatic Engineer, "The Pulse #137: Builder.ai did not 'fake AI with 700 engineers'" (June 12, 2025), [source](https://newsletter.pragmaticengineer.com/p/the-pulse-137)

Identical tactics to 1769: show impressive "proof," hide human operators, create mystique, eventually get exposed.

**The Ethical Gray Area**

Fireflies.ai's co-founder admitted their early "AI transcription" was "just two guys surviving on pizza," manually joining meetings and taking notes.[^fireflies] Critical difference: they successfully automated it with genuine AI. Legitimate MVP approach, not permanent fraud.

[^fireflies]: PC Gamer, "$1 billion AI company co-founder admits that its $100 a month transcription service was originally 'two guys surviving on pizza' and typing out notes by hand" (2024); Inc, "Fireflies Co-Founder Boasted About Duping Customers With 'Two Guys' Pretending to Be AI" (2024), [source](https://www.inc.com/tekendra-parmar/fireflies-not-really-ai/91265942)

**The Lesson**

The SEC coined "AI washing" in 2024 and began criminal prosecutions in 2025. First case (Nate Inc., April 2025): claimed 93% automation while call centers in the Philippines manually processed 100% of transactions.[^nate-doj]

[^nate-doj]: U.S. Department of Justice, U.S. Attorney's Office, Southern District of New York, "Founder and CEO of Artificial Intelligence Company Charged with Securities and Wire Fraud" (April 9, 2025); White & Case LLP, "Evolution of AI Washing Enforcement: DOJ Enters the Picture" (2025), [source](https://www.whitecase.com/insight-alert/evolution-ai-washing-enforcement-doj-enters-picture)

Ask vendors: "Can I see error logs?" "What percentage requires human intervention?" "How do you handle edge cases?" "Can I talk to 6+ month customers?"

If they deflect with "proprietary technology," you're looking at the 2025 Mechanical Turk.

Amazon named its crowdsourcing platform "Mechanical Turk," calling it "artificial artificial intelligence". Acknowledging that much AI relies on invisible human labor.

---

## Monday Morning Action Plan

**Experiment 1: The Autonomy Test (30 minutes)**

Ask vendors:
- "Show me the agent failing"
- "What decisions does it make versus follow from configuration?"
- "How does it learn from mistakes?"
- "What happens with unseen scenarios?"

Red flags: won't show failures, "learning" equals updating prompts, "autonomous" equals choosing from your list, can't explain failure modes.

Green flags: honest about limitations, clear debugging, explicit human-in-the-loop, realistic success rates (60-80%, not 95%+).

**Experiment 2: The Build vs Buy Analysis (1 hour)**

Calculate: platform + integration + tuning + error correction = total cost.

Compare to: hiring additional people.

Factor in: scale, complexity, risk, talent availability.

Proceed only if total cost is less and risk is manageable.

**Experiment 3: The Narrow Use Case Test (Ongoing)**

Pick one narrow workflow: well-defined inputs/outputs, clear success criteria, low risk, easy to verify.

Examples: ticket routing, data extraction from forms, daily report generation.

Measure: success rate, time saved, time fixing errors, net gain.

Negative or zero gain: abandon, try simpler.
Positive gain: document what worked, expand carefully.

**Experiment 4: The Hype Detector (15 minutes)**

Count hype words (autonomous, self-improving, AGI-like) versus concrete details (success rates, error modes, limitations).

Hype > details = overhyped.
Details > hype = realistic.

## The Bottom Line

AI agents in 2025 are NOT autonomous, self-improving, or AGI-like. They're pattern-matching workflows requiring significant engineering.

They ARE useful for narrow tasks, repetitive workflows with human verification, and augmentation (not replacement).

Vendors sell AGI fantasies. They deliver LLMs with API access and workflow logic. Valuable, but not autonomous intelligence.

Use strategically: start narrow and low-risk, measure honestly, keep human-in-the-loop, scale only what proves ROI.

Avoid for: open-ended problem solving, mission-critical processes without review, anything where debugging exceeds automation value.

Success comes from realistic expectations, not AGI hype.

In the next chapter, we'll examine legal AI, where hallucinations can get you sanctioned.

---

**Chapter Summary:**

AI agents are LLM-powered workflows, not autonomous entities. They don't learn or improve themselves. You update them manually. Multi-agent coordination adds complexity faster than value. Reliability issues include hallucinations, loops, and tool selection errors. They work best for narrow tasks, repetitive workflows, and augmentation (not replacement). Economics often don't justify cost unless you have massive scale. Frameworks (AutoGPT and others) are useful libraries, not AGI. Start with one low-risk workflow, measure honestly, scale cautiously.

**Next Chapter:** Myth - "AI Is Always Right" / Reality - "Hallucinations and Limitations"

[^react-paper]: Yao, Shunyu, et al., "ReAct: Synergizing Reasoning and Acting in Language Models," arXiv:2210.03629 (October 2022), [source](https://arxiv.org/abs/2210.03629); The paper introduced a simple but effective pattern for connecting LLMs to tools through iterative reasoning and action steps.

[^agent-reliability]: CAIA (Comprehension Agents via Isolation and Adaptation) benchmark results (2024-2025) show AI agents successfully complete complex multi-step tasks only 20-40% of the time; OpenAI's own research indicates hallucination rates between 33-79% depending on task complexity; Techopedia, "AI Agents: Separating Hype from Reality in 2025" (2025), analyzing systematic failures in production agent deployments including loop failures, tool selection errors, and memory limitations.

[^agent-frameworks]: AutoGPT (GitHub: Significant-Gravitas/AutoGPT), launched March 2023, reached 150,000+ GitHub stars but production adoption remained minimal due to reliability issues; BabyAGI (GitHub: yoheinakajima/babyagi), launched April 2023; LangChain documentation ([source](https://python.langchain.com/docs/modules/agents/)), the most widely adopted framework for building agent workflows; see also CrewAI, SuperAGI, AgentGPT, and hundreds of derivative frameworks launched during the 2023-2025 agentic AI hype cycle.
