# An Epistemic Claim Architecture for Agents, Evidence, and Pluralistic Evaluation
## Quick Tech Specs   
### 0. Scope, intent and contributions

**Problem:** How to work with uncertain, conflicting, and evolving information without forcing it into a  single canonical truth. This applies wherever: claims cannot be conclusively verified at the time they are made, evidence is incomplete, ambiguous, or value-laden, and decisions must still be taken responsibly. Autonomous and automatic systems collapse probabilistic judgments into boolean truth too early. When a model treats a 0.9 confidence as true, subsequent reasoning compounds certainty implicitly, even though 0.9 × 0.9 × 0.9 × 0.9 represents materially lower confidence. This is analogous to performing multi-step calculations with prematurely rounded numbers.

**Approach:** Preserve uncertainty by representing reasoning as structured, versioned claim–evidence pairs. Claims, evidence, evaluations, and assumptions are explicitly documented, evaluated from multiple independent perspectives by a neutral witness, and linked into traceable reasoning chains rather than collapsed into a single truth assignment.

**Enables:** AI agents in accountability-critical tasks and blockchain systems beyond purely mathematical or financial domains.

That being said, ECA architecture or Neutral Witness is not AI-specific and not blockchain-dependent. 
AI systems and blockchains are implementation tools, not defining features.

This paper introduces four independent but composable contributions:

##### Epistemic Claim Architecture (ECA): 
a process-oriented framework for representing and evaluating claims without collapsing uncertainty, disagreement, or contextual information into a single irreversible outcome.
##### Triple-pass stateless evaluation:
a structured evaluation procedure that separates interpretation, support, and conflict analysis.
##### Zero-Knowledge Claim Evaluation (ZKCE):
a method for verifiable claim evaluation without revealing the claim, evidence, or evaluation criteria.
### Temporal Claim Branching (TCB):
a method for maintaining multiple alternative futures as explicit, 
parallel claim structures that can coexist until evidence resolves them, 
enabling adaptive decision-making and systematic counterfactual analysis.

### 1. Core abstraction: claims, not states 
The system is claim-centric rather than state-centric. 
A claim is: 
- an explicit assertion (“X supports Y”, “Event A occurred”, “Condition C holds”), 
- scoped in time, context, and definition, 
- allowed to coexist with competing or contradictory claims. 

Claims are never collapsed into a single authoritative state.
### 2. Neutral Witness (NW) 
Neutral Witness is an institutional role, not a technology. 
Its function is to: 
- receive claims, 
- evaluate them through multiple independent assessment processes,surface agreement, disagreement, and uncertainty, 
- and record the evaluation trace for later inspection. 

Evaluators may be: 
- humans, 
- AI systems, 
- rule-based programs, 
- cryptographic or sensor-based attestations, 
- or any combination of the above. 

What matters is independence and comparability, not intelligence. NW does not decide what is true. 
It structures disagreement and makes it inspectable. 

### 3. Stateless plural evaluation (general principle) 
To prevent narrative lock-in, evaluations are designed to be stateless and independent. Each evaluation: 
- starts from the same claim and evidence set, 
- has no memory of prior evaluations, 
- and produces a bounded assessment under explicit assumptions. This principle applies equally to: 
	- 	human reviewers (no shared deliberation),
	- 	automated systems, 
	- 	or institutional audits. 

Statelessness prevents internally consistent but externally incorrect stories from forming. 
### 4. Triple-pass stateless evaluation (reference pattern) 
A common evaluation pattern uses three independent passes: 
1. Support analysis 
What supports the claim, and under which assumptions? 
2. Refutation / gap analysis 
What contradicts the claim, or fails to support it? 
3. Ambiguity and scope audit 
Where could reasonable disagreement arise? 
What definitions, time bounds, or missing evidence matter? 
The purpose is not balance, but exposure of epistemic structure. 
Disagreement is treated as signal, not failure. 

### 5. Claim Register
All claims and evaluations are stored as traceable records, not verdicts. A claim register allows mutually contradictory claims while binding them into an explicit structure. It may include: 
- the original claim, 
- referenced evidence, 
- each independent evaluation output, 
- surfaced contradictions,
- stated assumptions and uncertainty bounds, 
- and links to related claims. 


This record functions as: 
- institutional memory, 
- audit trail, 
- and basis for later comparison or dispute resolution. 

Storage backends may include: 
- append-only logs, 
- document stores, 
- or immutable ledgers (e.g. blockchains). 

Immutability preserves process, not truth. 

### 6. Temporal Claim Branching (TCB)

Temporal Claim Branching (TCB) preserves multiple conditional future claim paths for claims whose consequences unfold over time. Unlike forecasting or scenario planning, branches are not merged into a single outcome before evidence resolves them. This enables conditional decision-making without narrative lock-in. In multi-agent negotiation, each party can propose multiple branches simultaneously, allowing counterparties to select preferred paths rather than negotiating single outcomes—transforming agreement from "find one acceptable solution" to "explore and commit to a compatible subset of the option space."

### 7. What the system explicitly does NOT do 
- Does not guarantee correctness 
- Does not eliminate uncertainty 
- Does not enforce consensus 
- Does not replace human judgment 
- Does not act as a truth oracle 

Its value lies in making error, disagreement, and assumption visible. 
### 8. Example implementation: AI as Neutral Witness,  Arweave as claim register (with optional confidential evaluation) 
This architecture can be instantiated as follows. 
Input (human-initiated) 
- Claim: “The source at URL X supports the statement Y.” 
- Evidence: URL X
- Optional confidential material: additional documents or data not suitable for  public disclosure. 

The human submitter defines the scope and constraints of evaluation, including what may  be quoted publicly and what must remain confidential. Before evaluation begins, the  Neutral Witness explicitly restates how it has understood the claim, its scope, and  evaluation criteria, making any misinterpretation visible and correctable. 
Evaluation (AI in Neutral Witness role) 
Neutral Witness orchestrates multiple stateless evaluation passes, each executed  independently. 
- Pass A (support-focused): 
Identifies evidence in the source that supports the claim, under explicit  assumptions. 
- Pass B (refutation / gap-focused): 
Identifies contradictions, missing support, or scope mismatches. 
- Pass C (ambiguity audit): 

Examines alternative interpretations, unclear definitions, and boundary conditions. Each pass is: 
- memoryless, 
- bounded in scope, 
- unaware of the others’conclusions. 

Confidential evaluation (optional, via TEE / ZKCE) 
If part of the relevant evidence cannot be disclosed:
- One or more evaluation passes are executed under Zero-Knowledge Claim Evaluation (ZKCE), potentially within a Trusted Execution Environment (TEE).
- The confidential data remains protected and is never written to the public record.
- The evaluation code, inputs, and environment are cryptographically attested.

Confidential evaluation produces:
- a bounded assessment,
- explicit assumptions and uncertainty notes,
- and attestation metadata.

These outputs are treated as one evaluator among others, not as an authority.

Comparison 
Neutral Witness compares all evaluation outputs: 
- public AI evaluations, 
- confidential claim evaluations (ZKCE, including TEE-backed runs, if present),
- and optionally human-provided assessments. 

It explicitly surfaces: 
- convergence, 
- bounded disagreement, 
- hard contradiction, 
- or insufficient evidence. 

No single conclusion is forced. 
Disagreement is returned as structured output. 
Recording (AI Flight Recorder)
A permanent claim register is generated: 
-HTML report for human readers: 
- summarizes each evaluation,
- highlights
	-  disagreements and assumptions, 
	- explains where confidentiality limits disclosure. 
- JSON record for machines: 
	- includes structured evaluation outputs, 
	- links related claims, 
	- records hashes and attestation metadata. 

These artifacts are written to Arweave as content-addressed, immutable records. The record captures how the claim was evaluated, not what is true. 
Outcome 
- The researcher retains interpretive responsibility. 
- The evaluation becomes citable, inspectable, and reusable. 
- Future claims can reference, extend, or contest this register. 
- Confidential evidence contributes to evaluation without becoming public or  authoritative. 

Why this matters 
This example shows that: 
- humans can initiate Neutral Witness evaluations, 
- AI can act as one evaluator among others, 
- confidential data can participate without disclosure, 
- and immutable storage preserves accountability without enforcing consensus. 

### 9. Representative Use Cases (non-exhaustive) 
The Neutral Witness architecture is applicable wherever claims must be evaluated under  uncertainty without collapsing disagreement into forced consensus. The following  examples illustrate typical patterns.
#### 9.1 Research and source criticism  
A researcher submits a claim together with a cited source for evaluation. Neutral Witness assesses how the source supports the claim, surfaces ambiguities and  counterevidence, and records the evaluation trace as a citable artifact. 
Because the evaluation captures quoted passages, contextual assumptions, and the  relationship between claim and source at a specific point in time, it also provides a partial  mitigation against link rot and inaccessible sources. Even if the original material later  changes or disappears, the reasoning trace and referenced excerpts remain inspectable. 
#### 9.2 Confidential due diligence and compliance 
Organizations often need to assess claims that depend on sensitive or proprietary  information. 
Using a combination of public evaluation and confidential evaluation (e.g. via TEEs),  Neutral Witness allows: 
- claims to be evaluated without full disclosure, 
- disagreements to be surfaced explicitly, 
- and accountability to be preserved without leaking data. 

By enabling repeated and comparable evaluations over time, this supports continuous,  auditable due diligence and dynamically updated, evidence-based trust assessments  rather than one-off certifications. 
By reducing reliance on upfront disclosure and privileged access, it also allows smaller  actors and organizations in weak-institution contexts to compete on more equal terms,  based on the traceability of their claims rather than inherited reputation.
#### 9.3 Autonomous agents and machine-to-machine interaction 
Autonomous agents can exchange claims about capabilities, commitments, or state  without requiring blind trust. 
Neutral Witness allows agents to: 
- present claims with explicit assumptions and uncertainty, 
- compare independent evaluations, 
- form granular, conditional agreements whose terms explicitly encode uncertainty,  assumptions, and acceptable risk, 
- And leave auditable traces of negotiation and decision making. 

This makes agent interaction economically usable without pretending agents are correct or  aligned. 
### 10. Why this matters 
By separating: 
- claims from states, 
- evaluation from authority, 
- and memory from judgment, 

the system becomes compatible with how knowledge actually behaves in the real world. AI accelerates evaluation. 
Blockchains preserve memory. 
Neutral Witness preserves responsibility. 

### One-sentence summary  
Neutral Witness is a general mechanism for evaluating and recording contested claims  under uncertainty; AI and blockchains are merely tools for implementing this role at scale.

# From Digital Monarchy to Republic  
## An Epistemic Claim Architecture Manifesto 
Modern AI systems and blockchains are often presented with the same promise: that truth can be produced without human authority. 

AI promises correct answers derived from data. 

Blockchains promise objective truth through consensus and immutability. 

Behind both lies a seductive idea: that truth is a stable, singular outcome which can be  mechanically determined and delivered. 

This idea is not just optimistic. It is wrong. 

Most meaningful claims are not simply true or false. They are interpretations of incomplete  evidence, expressed in ambiguous language, shaped by context, incentives, and values.  Even humans cannot reliably produce a single final answer in such situations. Systems  that claim to do so do not eliminate uncertainty. They hide it. 

And hidden uncertainty changes how power works. 

When systems present certainty, people stop evaluating. Judgment is quietly outsourced.  Disagreement is reframed as a shameful error. What should remain open to interpretation  becomes an authoritative output. Responsibility dissolves into phrases like “the system  decided. 

This is how a new form of central authority emerges. 

Despite decentralized infrastructure, many of these systems function socially as digital  monarchies. They issue verdicts without exposing reasoning. They allow no appeal, no  comparison, no structured disagreement. Users are not participants in judgment, but  subjects of decisions whose foundations they cannot examine. 

Human societies learned long ago that this does not work. 

We did not overcome uncertainty by eliminating judgment. We institutionalized it. 

Courts rely on trials, not oracles. Evidence, witnesses, impartial experts, reasoning, and  procedure exist not to guarantee truth, but to make decisions accountable under  uncertainty. The goal has never been perfect correctness, but visible responsibility.
The same principle must apply to computational systems. 

Instead of systems that declare truth, we need systems that expose how claims are  formed, where they are weak, and why reasonable disagreement exists. Systems that treat  error not as an embarrassment to be hidden, but as a natural property of knowledge to be  managed. 

This requires abandoning a comforting illusion. 

Machines cannot think for us. They cannot carry responsibility on our behalf. This is both  disappointing and deeply reassuring. It ends the fantasy of automated certainty, and  restores judgment to where it belongs: with humans and the institutions they build. 
Giving up the pursuit of final, machine-generated truth does not make systems weaker.  Paradoxically, systems become more trustworthy precisely when they abandon the  ambition of delivering absolute truth. It makes them usable. When uncertainty is explicit, it  can be evaluated, priced, shared, and acted upon. When reasoning is recorded,  accountability becomes possible. When multiple claims can coexist, disagreement  becomes informative instead of destructive. 

The real choice before us is not technical. It is political. 

We can build systems that rule by producing unquestionable outcomes. Or we can build systems that testify, leaving traces that others may inspect, contest, and  reinterpret. 
This is the difference between a digital monarchy and a digital republic. 

A republic does not require perfect citizens. It requires institutions that assume fallibility,  make power visible, and prevent responsibility from disappearing behind machinery. 

In such a republic, no one owns the truth. What we hold in common is a shared process for  seeking it.



Written by: Teemu Lantta  
Date: 26/01/2026 
Contact: teemun.geemeili@gmail.com / X: @TeemuLantta 
# 
