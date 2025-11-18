# The Hidden Humans Behind "AI" Coding Tools

**Few verified cases exist of AI-powered software development tools being criminally exposed as frauds**, but those that have been revealed share striking patterns: offshore workers disguised as algorithms, investors deceived by billions, and a modern echo of the 1770 "Mechanical Turk" chess automaton that concealed a human operator for 84 years. The most spectacular failure—Builder.ai's $1.5 billion collapse in 2025—exemplifies how "AI washing" became a multi-billion dollar problem triggering criminal prosecutions.

## The flagship scandal: Builder.ai's $1.5 billion fraud

Builder.ai (formerly Engineer.ai) represents the software development industry's largest documented case of AI fraud. Founded in 2016 by Sachin Dev Duggal, the company promised to make app development "as easy as ordering pizza" through its AI assistant "Natasha," claiming apps could be built 6x faster and 70% cheaper than traditional methods.

**The deception was breathtaking in scale.** The company raised $445 million from Microsoft, SoftBank, and Qatar Investment Authority, achieving unicorn status at $1.5 billion valuation. Behind the slick interface and AI marketing, approximately 700 human engineers in India and Ukraine manually coded every application. Workers were instructed to time communications to UK business hours and avoid Indian-English colloquialisms to maintain the AI illusion.

The Wall Street Journal first exposed the scheme in August 2019, citing former Chief Business Officer Robert Holdheim, who sued for $5 million alleging "smoke and mirrors." Duggal denied the allegations, claiming a "Human-Assisted AI" model. But the deception extended beyond technical capabilities—the company inflated revenues by over 300%, claiming $220 million in 2024 when actual revenues were approximately $50 million. Internal investigations revealed round-tripping schemes with partner companies to fabricate transactions.

**Discovery came through multiple channels.** The 2019 WSJ investigation interviewed former employees who described the system as having "1950s-style decision tree logic" wrapped in polished interfaces, with NLP and autonomous capabilities completely absent. The financial fraud emerged in 2025 when lender Viola Credit conducted an audit after default concerns, seizing $37 million from accounts. The company filed for bankruptcy in May 2025 owing $85 million to Amazon and $30 million to Microsoft in unpaid cloud services.

An important nuance emerged from The Pragmatic Engineer's detailed 2025 investigation: Builder.ai did develop some genuine code generation capabilities using Claude and GPT-4 by 2023-2024. The company's collapse stemmed primarily from massive financial fraud rather than purely being a Mechanical Turk operation. However, the early years (2016-2021) involved significant human-powered work marketed as AI, and the AI that was eventually built never matched the autonomous capabilities claimed.

Federal prosecutors are now investigating for securities fraud. Former employees summarized it simply: "all engineer, no AI."

## Criminal prosecution: Nate Inc. and the 0% automation lie

In April 2025, the U.S. Department of Justice filed the first major criminal charges for AI washing when they indicted Nate Inc. CEO Albert Saniger for securities and wire fraud. This marked an escalation from civil penalties to criminal prosecution, with each charge carrying a maximum 20-year sentence.

Nate marketed itself as an AI-powered e-commerce app that could complete online purchases in under 3 seconds using "deep learning models," claiming 93-97% automation rates capable of handling 10,000 daily transactions. **The actual automation rate was 0%**, according to the DOJ indictment. Hundreds of workers in call centers in the Philippines—and later Romania after an October 2021 tropical storm disrupted operations—manually processed every single transaction while mimicking AI behavior.

These workers viewed highly sensitive private data: credit card numbers, addresses, and personal information. Saniger instructed employees to keep automation rates secret, restricted access to internal dashboards showing the truth, and prioritized investor test transactions to avoid detection. When The Information exposed the human workforce in 2022, the company falsely claimed workers were only handling "edge cases."

**The deception unraveled through investigative journalism followed by federal investigation.** The Information's 2022 reporting first revealed the extensive human labor. The SEC and DOJ launched parallel investigations, with the criminal indictment coming three years later. Acting U.S. Attorney Matthew Podolsky stated: "This type of deception not only victimizes innocent investors, it diverts capital from legitimate startups, makes investors skeptical of real breakthroughs, and ultimately impedes the progress of AI development."

The company raised over $40 million from venture capitalists before shutting down in 2023, leaving investors with near-total losses. Saniger pleaded not guilty and faces trial.

## The founder who admitted the con: Fireflies.ai

Not all cases involve criminal fraud—some represent the ethical gray area of "Wizard of Oz" prototyping. Fireflies.ai CTO Krish Ramineni admitted on LinkedIn that the company's early "AI transcription" service in 2016 was actually him and his co-founder manually joining meetings and taking notes.

This represents the classic Mechanical Turk approach to prove market demand before building actual technology. **The critical difference from fraud: Fireflies.ai successfully automated the process with genuine AI and remains operational today**, raising questions about when human involvement crosses from legitimate prototyping to deceptive practice.

The company claims early customers knew there was "human in the loop," though the extent of disclosure remains unclear. This case illustrates the tension in Silicon Valley's "fake it till you make it" culture—where the line between MVP testing and investor deception becomes blurred.

## Mechanical Turk workers behind "SmartScan" AI: Expensify

Expensify's "SmartScan" technology, marketed as AI-powered expense report verification from photos, relied on Amazon Mechanical Turk workers for manual processing when the AI failed—which happened frequently. The company had used this approach since 2009, but the practice was exposed in 2017.

**Discovery came from workers themselves.** Rochelle LaPlante, a Mechanical Turk worker, found receipts she had processed publicly visible on Twitter, revealing names, addresses, bank details, Social Security numbers, and even sensitive medical information. Workers were paid 1.6 to 2 cents per receipt to manually transcribe data that customers believed was being automatically processed.

Expensify marketed these workers as "secure technicians" rather than disclosing they were crowdsourced gig workers with minimal vetting. CEO David Barrett admitted the company had used Mechanical Turk since 2009, later claiming they switched to a "private workforce" after 2012—still humans, just employees rather than anonymous crowdworkers.

This case highlights a pattern: companies use terms like "human-in-the-loop" or "human verification" to obscure that humans are doing the primary work, not just checking AI's output.

## Facebook's short-lived M assistant

Facebook launched M in August 2015 as a Messenger-based virtual assistant that could supposedly book restaurants, order gifts, arrange travel, and schedule meetings using AI. Over 70% of requests were handled by human operators, though users were largely unaware of this extensive human involvement.

The service remained in limited beta with only 2,000-10,000 users out of Facebook's 1.3 billion Messenger users. **The human workforce made scaling economically unsustainable.** When AI couldn't answer a request, humans took over "unbeknownst to the user," according to reports. Facebook shut down the service in January 2018.

Facebook characterized M as a legitimate "experiment" for training AI systems, and the company openly described it as "trained and supervised by people" in some contexts. However, the extent to which users understood they were largely communicating with humans rather than AI remains disputed. This case occupies the middle ground—more transparent than outright fraud but less than fully disclosed.

## Adjacent cases: When "autonomous" systems need human intervention

Several cases from related fields illuminate patterns relevant to software development:

**Amazon Just Walk Out** (2016-2024) marketed "automated" checkout using computer vision but required approximately 700 human reviewers per 1,000 transactions, according to The Information's 2024 investigation. Over 1,000 workers in India manually reviewed footage to verify purchases. Amazon phased out the technology from U.S. stores in April 2024, with the company describing the human reviewers as necessary for "training" the AI—though this "training" lasted eight years. A privacy lawsuit was filed by the Surveillance Technology Oversight Project.

**X.ai's scheduling assistant** "Amy" involved humans behind every email response in its early years. Bloomberg interviews revealed 24-year-old workers manually scheduling meetings and ordering food while reading users' emails. The company claimed AI was "in early stages," using a long training period to justify permanent human involvement.

**Presto Automation** claimed its drive-thru voice ordering system achieved "95% automation without human intervention" in August 2023. The reality: over 70% of orders required human intervention from workers in the Philippines. The SEC launched an investigation in July 2023 and issued a cease-and-desist order in January 2025 after discovering the company's "proprietary AI" was actually third-party technology requiring significant human oversight. The company settled on negligent fraud charges.

## Patterns of deception: How companies hide humans behind algorithms

Research across these cases reveals consistent operational tactics:

**Geographic arbitrage** is universal. Every exposed case used offshore workers in low-wage countries: India, Philippines, Romania, Ukraine, Nepal, Honduras. This serves dual purposes—reducing costs and creating geographic distance between the marketed AI and the actual human workforce, making discovery more difficult.

**Communication control** maintains the illusion. Companies instruct workers to time responses to match supposed AI processing speeds. Builder.ai workers were told to avoid regional language patterns. Nate employees prioritized investor test transactions to ensure they appeared flawless. This theatrical element echoes the original 1770 Mechanical Turk, where the hidden chess master had to time moves to seem like mechanical processing.

**Terminology deflection** provides plausible deniability. When caught, companies pivot to claiming "human-in-the-loop" for "training" or "edge cases." Expensify called Mechanical Turk workers "secure technicians." Amazon described eight years of human verification as "training." This linguistic sleight-of-hand transforms fraud into what sounds like standard AI development practice.

**Social media scrubbing** removes evidence. Nate directed workers to remove company references from their LinkedIn profiles. Companies avoid listing human operation centers in public filings. Job postings use vague titles like "AI trainer" or "quality assurance" rather than revealing the human workforce is doing the primary work.

**UI deception** creates technical theater. Polished interfaces with loading animations, progress bars, and technical jargon convince users they're interacting with sophisticated AI. Builder.ai's "Natasha" interface routed requests to Indian developers but looked like a conversational AI making autonomous decisions. The original Mechanical Turk similarly featured elaborate visible gears and mechanisms to prove its mechanical nature while the actual operator remained hidden.

## How frauds were uncovered

**Investigative journalism** broke the major cases. The Wall Street Journal's 2019 Builder.ai investigation drew on whistleblower Robert Holdheim and multiple former employees. The Information's 2022 Nate exposé and 2024 Amazon investigation came from workers and insiders. The Washington Post's 2023 investigation into Scale AI's "digital sweatshops" in the Philippines revealed patterns across the industry.

**Workers themselves** exposed privacy violations and poor conditions. Rochelle LaPlante's discovery that Expensify receipt data appeared on Mechanical Turk revealed systematic privacy breaches. Anonymous worker reports across multiple platforms highlighted the gap between AI marketing and human reality.

**Regulatory examinations** caught financial fraud. The SEC's Division of Examinations discovered Delphia's false AI claims during a routine exam in 2021—but the company continued false marketing for two more years. Lender audits triggered Builder.ai's collapse when Viola Credit investigated loan defaults and discovered revenue inflation.

**Technical red flags** revealed operational impossibilities. When a tropical storm hit the Philippines and Nate's transaction processing failed, it exposed the geographic dependence on human workers. Builder.ai customers complained about quality issues inconsistent with AI claims. Amazon Just Walk Out took hours to generate final receipts, far longer than the "seamless" experience marketed.

## The regulatory crackdown on AI washing

The term "AI washing"—coined by SEC Chair Gary Gensler—entered enforcement vocabulary in 2024. The SEC filed its first AI washing cases in March 2024 against investment advisers Delphia and Global Predictions, charging them with making false claims about using AI for investment decisions. Delphia paid $225,000 and Global Predictions $175,000, settling charges of violating the Investment Advisers Act.

**Criminal prosecution represents escalation.** The April 2025 DOJ indictment of Nate CEO Albert Saniger marked the first criminal (rather than civil) AI washing case. White & Case legal analysis described it as an "evolution from civil to criminal enforcement," signaling prosecutors' confidence in pursuing criminal fraud charges for AI misrepresentation.

The FTC launched "Operation AI Comply" in September 2024, a law enforcement sweep targeting AI-related deception. Five cases addressed fraudulent AI claims, including DoNotPay's "$193,000 settlement for claiming to be the 'world's first robot lawyer'" despite having no attorneys employed and untested AI. FTC Chair Lina Khan stated bluntly: "Using AI tools to trick, mislead, or defraud people is illegal. There is no AI exemption from the laws on the books."

**The SEC created a dedicated Cybersecurity and Emerging Technologies Unit (CETU)** to focus on AI-related misconduct. A May 2025 enforcement forum statement warned staff are scrutinizing how companies describe AI technology "to determine if genuinely using machine learning or merely repackaging old automation under an AI label."

Multiple legal experts note regulators are using traditional securities fraud, wire fraud, and false advertising statutes rather than AI-specific laws. The legal threshold for criminal charges requires proving intentional concealment, material false claims to investors, and knowing deception—exactly what the Nate and Builder.ai cases allegedly demonstrated.

## Why software development tools specifically are vulnerable

Despite high-profile frauds, verified cases of AI-powered code generation, bug fixing, or automated testing tools being criminally exposed as purely human-powered remain extremely rare. Builder.ai stands nearly alone as a software development-specific case—and even that involved some eventual AI development and was primarily a financial fraud.

**Developer tools face unique vulnerabilities to AI washing:**

Technical customers can theoretically verify claims, but complex enterprise sales often involve non-technical decision-makers evaluating developer tools. A CTO might test the product, but procurement, finance, and executive teams making purchasing decisions cannot easily distinguish real AI from sophisticated human operations behind polished APIs.

The cost pressure to reduce expensive developer headcount creates strong demand for any tool promising automation. Companies desperately want to believe AI can replace or augment engineering teams. This demand-side desperation makes it easier to sell exaggerated AI capabilities.

High automation promises seem plausible because coding appears ideal for AI—it's logical, rule-based, and has clear inputs/outputs. This intuitive plausibility provides cover for false claims. Unlike, say, promising AI can replace doctors (which triggers immediate skepticism), claiming AI can write code sounds reasonable enough that buyers may not scrutinize technical specifics.

**The rapid evolution of genuine AI coding tools creates confusion.** GitHub Copilot, Cursor, Replit, and other tools demonstrably work. When legitimate AI coding tools exist and are improving rapidly, distinguishing between real capabilities and fraud becomes harder. Companies can point to genuine AI products and claim "we do something similar" while actually using human developers.

## The original mechanical turk and 250 years of automation fraud

Every modern case echoes a historical precedent. In 1769, Hungarian inventor Wolfgang von Kempelen presented Empress Maria Theresa with an "automated" chess-playing machine. The Mechanical Turk featured a wooden cabinet with visible gears and a Turkish-costumed automaton that appeared to play autonomously, defeating opponents including Napoleon Bonaparte and Benjamin Franklin over 84 years of touring.

**The reality: a hidden human chess master** operated the machine using magnets and levers, concealed through sliding panels and a rolling chair system. When Kempelen opened the cabinet to "prove" the mechanism, carefully choreographed panel movements hid the operator behind visible machinery.

Amazon explicitly named its crowdsourcing platform "Mechanical Turk" after this historical deception, describing it as "artificial artificial intelligence" that "reverses the roles of computers and humans." This naming choice acknowledges a fundamental truth: much of what we call AI relies on invisible human labor.

**The pattern persists across 250 years:** Show impressive but irrelevant "proof" of mechanism while hiding actual human operation. Create mystique around "black box" technology. Leverage public fascination with automation. Use hidden, often exploited workers. Eventually get exposed through whistleblowers or careful investigation. The technology changes; the deception remains structurally identical.

## The ethical spectrum: From legitimate prototyping to criminal fraud

Not all human involvement in AI systems constitutes fraud. Understanding the spectrum helps distinguish legitimate practices from criminal deception:

**Legitimate human-in-the-loop AI** includes disclosed human review for safety or quality, content moderation with human oversight, and medical AI with doctor verification. GitHub Copilot's interface makes clear it generates suggestions requiring human review. This transparency transforms human involvement from deceptive to appropriate.

**Wizard of Oz prototyping** has been a recognized UX research method since 1973, where users interact with a system they believe is autonomous but is actually human-controlled. The purpose is testing concepts before expensive development. The ethical requirement: research context, limited scope, participants debriefed afterward, and informed consent. Fireflies.ai arguably used this approach legitimately before building real automation.

**The line crosses into fraud** when companies deploy human-powered systems commercially while claiming AI capabilities, raise investment capital based on false automation claims, operate at scale with no path to genuine automation, instruct employees to hide human involvement, and access sensitive user data without disclosure. Builder.ai and Nate clearly crossed these lines.

Academic consensus holds that transparency, intent, and timeline distinguish legitimate practice from fraud. Is human involvement disclosed? Is the purpose research/development or permanent commercial operation? Is there a genuine roadmap to automation or is human labor the permanent model?

## The labor exploitation hidden inside AI hype

Behind the AI washing scandals lies systematic labor exploitation. Anthropologists Mary L. Gray and Siddharth Suri's book "Ghost Work" documents how platforms render invisible the human labor maintaining AI illusions. Their five-year study found workers earning median wages around $2 per hour, with no benefits, no job security, and instant termination possible.

**The scale of hidden labor is staggering.** Builder.ai employed approximately 700 engineers. Amazon Just Walk Out required over 1,000 workers in India. Scale AI, which trains models for Meta, Microsoft, and OpenAI, employs thousands in the Philippines under conditions the Washington Post characterized as "digital sweatshops." Workers label data, moderate traumatic content, transcribe audio, and tag images—paid $1.46 per hour after taxes according to investigations.

Jathan Sadowski coined "Potemkin AI" in 2018 to describe technical illusions designed to fool the public, where human labor is hidden behind claims of machine intelligence. The term references fake villages built to impress Empress Catherine II—all facade, nothing behind it. Sadowski argues this serves dual purposes: profit (creating investment opportunities, appearing innovative) and power (creating illusions of inescapable surveillance and control).

The International Labour Organization's report "The Artificial Intelligence Illusion: How Invisible Workers Fuel the 'Automated' Economy" found that crowdworkers on digital platforms face "decent work deficits"—low pay, no benefits, no safety protections. Constant exposure to graphic content causes PTSD and depression. Workers provide remote access but at the cost of exploitation invisible to AI system users.

## Why verified coding tool frauds are so rare

Despite extensive research across investigative journalism, regulatory filings, academic papers, and industry reports, **verified cases of AI-powered code generation, bug fixing, or automated testing tools being criminally exposed as purely human-powered remain extraordinarily rare beyond Builder.ai.**

No scandals emerged involving GitHub Copilot competitors being fake. No documented cases exist of automated testing platforms using human testers while claiming AI. No bug-fixing services were exposed as having developers manually fix issues. The predicted wave of fraudulent AI coding tools largely hasn't materialized in documented exposés.

**Several factors explain this surprising absence:** Technical customers can verify functionality more easily than non-technical users of other AI products. Developers testing AI coding tools can quickly determine if output quality matches AI claims. Observable outputs—code quality, generation speed, consistency—are easily measured and compared against legitimate tools.

Real LLM capabilities demonstrably work for coding tasks. GitHub Copilot, Claude, GPT-4, and other models genuinely generate functional code. The existence of working AI coding tools means faking it is both harder (customers can compare to real alternatives) and less necessary (the technology actually exists).

The industry accepts "human-assisted AI" as legitimate. Code review, human oversight of AI suggestions, and human-in-the-loop development are standard practices openly discussed. This transparency reduces pressure to hide human involvement. Unlike Nate claiming 93% automation when it was 0%, AI coding tools can honestly say "this generates suggestions requiring human review" without damaging their value proposition.

**This doesn't mean AI washing is absent from developer tools**—it means outright "humans pretending to be AI" fraud is rare. The more common pattern involves exaggerating capabilities, overselling automation levels, and using marketing language that implies more autonomy than actually exists. These practices fall into gray areas rather than criminal fraud.

## Conclusion: The illusion shatters but the pattern persists

From the 1770 Mechanical Turk to Builder.ai's 2025 collapse, the fundamental deception remains consistent: hiding human intelligence behind technological facades to extract profit, investment, or power. The scale evolved from one hidden chess master to armies of offshore workers, but the pattern endures.

The regulatory response has escalated dramatically. SEC Chair Gary Gensler's coinage of "AI washing" in 2024 triggered enforcement actions, civil penalties, and ultimately criminal prosecution. The April 2025 Nate indictment established that AI fraud can carry 20-year prison sentences. The FTC's Operation AI Comply and SEC's Cybersecurity and Emerging Technologies Unit signal sustained focus on policing AI claims.

**The key lesson: transparency is the difference between legitimate and criminal practice.** Human involvement in AI systems is often necessary, especially during development. The ethical line isn't whether humans are involved—it's whether that involvement is disclosed, whether claims to investors and customers match reality, and whether there's a genuine path to the automation claimed.

For software development specifically, the most important finding is counterintuitive: despite extensive investigation, verified cases of pure AI coding tool fraud remain rare. Builder.ai stands nearly alone, and even that case involved significant financial fraud beyond the AI washing. Real AI coding capabilities have advanced faster than fraud, creating an unusual situation where the technology legitimately does much of what was promised—making fraud both more detectable and less tempting.

The ghost workers powering "automated" systems deserve recognition. The exploitation of low-wage workers in the Philippines, India, Romania, and elsewhere renders invisible the human labor that makes AI functional. As Mary L. Gray argues, this labor exploitation should be at the heart of AI ethics, not a footnote to technological discussions.

Whether we face another "AI winter" of disappointed expectations and collapsed investments depends on whether the industry learns these lessons: disclose capabilities honestly, treat workers fairly, regulate meaningfully, and remember that 250 years of automation fraud history teaches that illusions eventually shatter—it's only a question of when and how catastrophically.

The mechanical turk is exposed. Again. And it will be exposed again, unless transparency and ethics become structural features rather than marketing buzzwords.