# Engineering Difficult Systems

I am **Vitalij Hein**, a hands-on software engineer and AI architect working at
the intersection of software delivery, cloud architecture, applied AI, and
technical consulting.

I am usually most useful when a customer has an important problem but no obvious
implementation path: the platform is too limited, the existing architecture is
too slow, the system cannot be tested reliably, or several products have to be
connected into something none of them provides on its own.

> **Give me the difficult problem. I will understand it, make the necessary
> decisions, and build the solution.**

[LinkedIn](https://www.linkedin.com/in/vitalijhein) ·
[GitHub](https://github.com/vitalijhein) ·
[Email](mailto:vitalijhein@googlemail.com)

## What I do

My work normally spans the full delivery chain:

1. understand the business problem and the operating constraints;
2. turn ambiguity into requirements and explicit technical decisions;
3. design an architecture that can survive the real environment;
4. implement the critical software myself;
5. verify behavior at the actual system boundary;
6. explain, defend, and hand over the result to customers and engineering teams.

I have been developing software professionally since 2017. In one client
engagement, I led the AI workstream as technical expert, coordinating and
enabling five contributors while remaining hands-on. I currently build AI,
cloud, backend, integration, and automation systems at Cluster Dynamics Reply.

My differentiator is **Agentic Engineering**: I design the operating system
around coding agents as carefully as the software they help build. Work is
isolated, state is durable, review is independent, integration is verified, and
product, architecture, risk, and release decisions remain human-owned.

## Start here

These three cases best represent how I work.

| Case study | The difficult problem | What it demonstrates |
|---|---|---|
| [Agentic Engineering Control Plane](case-studies/agentic-engineering-control-plane.md) | How can a fleet of probabilistic coding agents work for days without losing state, corrupting concurrent work, or approving plausible but inert code? | Engineering leadership, delivery-system design, Git isolation, verified dispatch, task-aware model routing, independent review, and human accountability |
| [Secure Construction Knowledge System](case-studies/secure-construction-knowledge-system.md) | How can adding an agent to a Microsoft Team provision a secure, current, project-specific knowledge environment when no single Microsoft product provides the lifecycle? | End-to-end customer ownership, Azure architecture, Graph and SharePoint integration, authorization, automation, and advanced retrieval |
| [Voice-Agent Regression Testing](case-studies/voice-agent-regression-testing.md) | How do you test a real voice bot reproducibly when the test instrument can lose evidence and falsely blame the product? | Novel test architecture, graph analysis, real Azure Communication Services calls, evidence semantics, and non-deterministic system verification |

## More systems

### [From 30 Seconds of Silence to a 2.6-Second C# RAG Engine](case-studies/csharp-rag-latency-engine.md)

A custom retrieval and answer engine for a voice FAQ system. I removed the full
corpus from the conversational hot path, separated indexing from answering, and
kept source-selection and answer-quality gates around the latency work. A current
29-request live reference replay averages 2,608 ms end to end after an
approximately 30-second production path and a roughly 14-second first custom
variant.

### [Mirror OS: A Personal Data Operating System That Knows When It Does Not Know](case-studies/mirror-os.md)

A local-first, portable system that turns longitudinal personal records into
typed daily state, patterns, and trajectory without pretending every conclusion
is equally supported. Its central engineering problem is epistemic control:
tracking missing sources, extraction quality, provenance, and when a
recommendation must be marked tentative or withheld completely.

### [Content Engine: Agentic Production with a Real Feedback Loop](case-studies/content-engine.md)

A stateful multi-agent content system that starts with evidence from real work,
abstracts private implementation into transferable principles, creates
controlled variants, runs independent fact, privacy, voice, and review gates,
stops at a human publication boundary, and learns from later public outcomes.

## Agentic Engineering is a delivery model, not a model preference

My control plane currently registers 18 reusable terminal lanes across three
workspaces. One documented 14-lane wave produced approximately ten verified
merges in 90 minutes while four blocking review findings were caught and routed
into fix-forward rounds.

The number of agents is not the point. The system treats every agent as an
unreliable distributed worker with identity, bounded authority, isolated code
state, observable output, and a recovery path. Its controls include:

- separate orchestration, implementation, and fresh-context review roles;
- one Git worktree and branch lease per active change;
- repository-local ledgers for sessions, decisions, verification, and findings;
- dispatch that verifies paste, submission, and actual worker startup;
- event-driven scheduling from branch, lane, and remote-job state;
- producer-consumer, fabricated-default, non-empty-output, and real-seam checks;
- merged-diff review and traceable cross-assigned fix rounds;
- task-aware routing across strong, lower-cost, and local or open models;
- deliberate recovery after interruption or context compaction;
- explicit human ownership of scope, architecture, risk, release, and final
  acceptance.

This is how I make different models useful. I do not assume that a cheaper model
is equivalent to a frontier model. I give it work whose risk is bounded by the
contract and verification envelope, then spend stronger reasoning where a subtle
mistake is expensive.

## Technical foundation

My recent work is strongest in Python, C#, Azure, backend services, APIs,
retrieval systems, agentic workflows, automated testing, and cloud integration.
The systems in this repository also draw on Microsoft Graph, SharePoint,
Dataverse, Power Automate, Azure AI Search, Azure Functions, Azure Communication
Services, FastAPI, Pydantic, MongoDB, and Git-based delivery automation.

I worked with language models before ChatGPT. My TU Wien diploma thesis trained
and fine-tuned BERT, RoBERTa, and OPT variants for propaganda-technique
classification and combined them through Meta Classification with Model
Stacking, improving Micro-F1 from a 0.54 baseline to 0.78.

[Read the published thesis](https://repositum.tuwien.at/handle/20.500.12708/188206)

I was part of the team that won the Microsoft AI Challenge 2025 with a
self-correcting email workflow that generates an answer, validates it against
declarative compliance rules, and repairs or escalates failed output.

[Read the celebration post](https://www.linkedin.com/feed/update/urn:li:activity:7343598439819018241)

## About these case studies

The case studies are intentionally technical and text-heavy. They explain the
problem, architecture, difficult decisions, failure modes, operating boundaries,
and transferable engineering principles rather than presenting a gallery of
technology logos.

Customer names, private records, credentials, infrastructure identifiers,
proprietary domain logic, and unpublished source code are excluded. Metrics are
used only where their population and technical meaning can be explained.

If one of these problems is relevant to what you are building, I am happy to
discuss the architecture and the decisions behind it.
