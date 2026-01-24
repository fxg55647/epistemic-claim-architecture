1. Introduction

Digital systems inherit more from human psychology and institutional history than is often acknowledged. Long before databases, blockchains, or artificial intelligence, humans developed a strong preference for clear outcomes, authoritative answers, and resolved states. Decisions feel safer when ambiguity is closed, responsibility is delegated, and uncertainty is hidden behind a final verdict. This preference has shaped not only institutions, but also the technical architectures that now mediate economic, legal, and informational processes.

Modern computing systems reflect this legacy. They are optimized to converge toward a single, canonical state: a balance is settled, a transaction is final, a flag is either true or false. These abstractions enable scale, coordination, and automation. They also feel psychologically comfortable. A system that produces one answer appears decisive; a system that exposes uncertainty feels unfinished, even when it is more honest.

As digital systems expand from arithmetic and record-keeping into language, judgment, and autonomous action, this inherited preference becomes a source of structural risk. The problem is not that ambiguity exists, but that our systems are designed to suppress it.

1.1 The Seduction of a Single Truth

Humans are not neutral observers of uncertainty. Open-ended questions impose cognitive cost: they slow decision-making, increase anxiety, and distribute responsibility in uncomfortable ways. Institutions historically addressed this by centralizing judgment. Courts issue verdicts, authorities publish official records, editors finalize texts. Once a decision is made, the underlying disagreement is typically discarded or archived beyond reach.

Digital systems replicate this pattern. A canonical database row, a finalized ledger state, or a single AI-generated answer provides closure. Even when the underlying evidence is incomplete or contested, the system presents a resolved outcome. This is not a technical accident; it is an ergonomic feature. Systems that hesitate or qualify are often perceived as weak, even when they are epistemically sound.

Artificial intelligence intensifies this dynamic. Large language models produce fluent, confident responses by design. When uncertainty is not explicitly represented, fluency is easily mistaken for correctness. As a result, ambiguity is not merely hidden; it is transformed into apparent certainty, leaving no trace of the assumptions, interpretations, or missing information that shaped the output.

1.2 Forced State: When It Works (Transfers) and When It Breaks (Language)

There are domains where forcing a single state is both appropriate and necessary. Monetary transfers, counters, ownership registries, and settlement systems require unambiguous outcomes. In these contexts, ambiguity is failure. Boolean state transitions enable reliability precisely because the underlying reality is mechanically decidable.

Language-based reasoning does not share this property. Natural language is inherently underdetermined: terms are vague, scopes are implicit, references shift over time, and context is often unstated. Two reasonable actors may disagree without either being mistaken. Attempting to force such reasoning into a single canonical state does not resolve ambiguity; it merely obscures it.

The historical success of state-based computation has encouraged its overextension. Data models, databases, and blockchains inherited assumptions from arithmetic domains and applied them to semantic ones. The result is a growing mismatch between what systems can faithfully represent and what they are increasingly asked to decide.

1.3 Boolean Ledgers vs Claim Ledgers

Traditional ledgers encode truth implicitly. Once an entry is finalized, it becomes part of an authoritative state. Disagreement, if it existed, is external to the system. This model resembles edited encyclopedias: a single, curated version stands as the record, while drafts and debates disappear.

A claim ledger adopts a different institutional posture. Instead of recording truth as state, it records claims as first-class objects. Each claim is contextual, time-bound, and attributable. Competing claims may coexist. Evidence is linked rather than consumed. Evaluation does not erase disagreement but documents it.

This distinction has institutional consequences. Boolean ledgers resemble digital monarchies: one chain, one history, one accepted state. Claim ledgers resemble digital republics: multiple voices, documented dissent, and legitimacy derived from transparent process rather than finality. Truth, in this model, is not crowned; it is argued, supported, revised, and sometimes withdrawn.

1.4 Contributions and Scope

This paper argues that the limitations observed in AI systems, blockchains, and automated decision-making are not primarily model failures or cryptographic shortcomings. They are architectural consequences of designing systems around forced states in domains that resist such closure.

We propose an epistemic claim architecture that accepts incompleteness, preserves disagreement, and makes reasoning traceable without demanding consensus. The goal is not to eliminate uncertainty or to replace human judgment, but to build systems that remain usable, auditable, and accountable precisely because they do not pretend that uncertainty can be removed.

By relinquishing the expectation of a single authoritative truth, we gain the ability to construct more resilient systems and unlock applications that current architectures systematically exclude.# epistemic-claim-architecture
An Epistemic Claim Architecture for Agents, Evidence, and Pluralistic Evaluation

2.1 Natural Language Reasoning and Underdetermination

Natural language reasoning differs fundamentally from formal reasoning in that meaning is rarely fully specified. Statements expressed in natural language rely on implicit assumptions, shared background knowledge, contextual cues, and pragmatic conventions that are not explicitly encoded in the text itself. As a result, many claims are inherently underdetermined: multiple interpretations may be compatible with the same linguistic surface form and available evidence.

This underdetermination is not an anomaly or a defect. It is a defining feature of how humans communicate. In everyday discourse, participants routinely resolve ambiguity through social context, iterative clarification, and tolerance for partial understanding. In institutional settings, this resolution is often delegated to procedures, authorities, or time-bound decisions that collapse uncertainty into an actionable outcome.

Computational systems, however, lack access to these informal resolution mechanisms unless they are explicitly modeled. When natural language inputs are processed by machines, ambiguity does not disappear; it is merely displaced. If the system is required to produce a single output without representing uncertainty, implicit choices are made regarding scope, reference, and interpretation. These choices are typically undocumented.

Large language models exacerbate this issue. They generate coherent continuations of text without epistemic commitment to the propositions expressed. Fluency and internal consistency do not imply that a claim is well-supported, appropriately scoped, or even meaningfully defined. When such outputs are treated as answers rather than as claims, the system presents an illusion of determination where none exists.

Boolean evaluation frameworks are ill-suited to this domain. A binary true/false classification assumes that the proposition under consideration is sufficiently specified to admit such evaluation. In natural language contexts, this assumption frequently fails. Questions such as “Is this true?” often conceal unresolved issues of time, modality, perspective, and admissible evidence. Treating the result as a settled fact obscures these dimensions and makes error detection difficult or impossible.

A claim-based model addresses this mismatch by making interpretive choices explicit. Claims are represented with associated context, scope, temporal reference, modality, and uncertainty. Evaluation does not yield a definitive truth value but an assessment of support relative to stated assumptions and available evidence. Disagreement, insufficient information, and ambiguity are not exceptional outcomes; they are expected and recorded.

This shift reframes natural language reasoning from a task of producing correct answers to a process of generating, evaluating, and revising claims under explicit epistemic constraints. Subsequent sections formalize this model and describe how it can be implemented in systems that must operate reliably despite linguistic underdetermination.

2.2 Boolean Ledger (Truth Ledger): Canonical State as “Truth”

A Boolean ledger represents the world as a sequence of definitive state transitions. Each recorded entry contributes to a single, canonical state that the system treats as authoritative. Once written and finalized, the ledger does not merely record an event; it implicitly asserts that the represented proposition is settled. In this sense, truth is encoded as state.

This model has proven extraordinarily effective in domains where reality admits unambiguous resolution. Accounting systems, inventory management, counters, and asset transfers rely on precisely one outcome. A transaction either occurred or did not. A balance either reflects the transfer or it does not. In such cases, disagreement is not meaningful within the system; it must be resolved before entry or handled externally.

The success of Boolean ledgers in these domains has led to their widespread generalization. Databases, distributed systems, and blockchains all inherit the same structural assumption: conflicts are errors to be resolved, and finality is a virtue. Once consensus is reached, alternative interpretations are discarded or rendered invisible.

In blockchain systems, this assumption is formalized as canonical chain selection and finality. Although blockchains do not explicitly claim semantic truth, the accepted chain becomes a de facto truth source. Events recorded on the canonical chain are treated as facts, while competing histories are orphaned or forgotten. The ledger does not merely record what happened; it defines what counts as having happened.

This architectural pattern has subtle epistemic consequences. By collapsing multiple possible interpretations into a single accepted state, Boolean ledgers externalize uncertainty and disagreement. Any ambiguity in meaning, evidence, or intent must be resolved prior to inclusion or else excluded entirely. The ledger itself provides no native mechanism to represent unresolved disputes, partial support, or context-dependent validity.

As systems expand beyond mechanically decidable domains, this limitation becomes increasingly problematic. When propositions concern language, interpretation, prediction, or responsibility, the act of forcing a single state prematurely transforms uncertainty into apparent certainty. Errors do not disappear; they become harder to detect, contest, or attribute.

It is important to note that Boolean ledgers are not inherently flawed. Their assumptions are appropriate within their original scope. The problem arises when the same truth-as-state model is applied to domains where truth is not a property of the system state but of a reasoning process. In such contexts, finality ceases to be a guarantee of correctness and instead becomes a mechanism for suppressing epistemic nuance.

The following section introduces the claim ledger as an alternative architectural primitive, designed to operate in domains where multiple, competing interpretations must coexist without being collapsed into a single authoritative state.

2.3 Claim Ledger (Non-Boolean Ledger): Claims as First-Class Objects

A claim ledger reverses the core assumption of a Boolean ledger. Instead of encoding truth as a finalized state, it treats claims about the world as primary objects of record. The ledger does not assert what is true; it documents who claimed what, under which conditions, supported by which evidence, and subject to which evaluations.

In this model, a claim is not equivalent to a fact. It is an explicit, attributable assertion that may be supported, contested, refined, superseded, or withdrawn over time. Multiple incompatible claims may coexist without forcing resolution. The ledger remains internally consistent precisely because it does not require agreement.

Claims are represented with explicit structure. At minimum, a claim specifies a subject, predicate, and object, along with contextual qualifiers such as temporal scope, locale, modality, and uncertainty. By making these dimensions explicit, the system avoids collapsing interpretation into an implicit, undocumented choice. What would otherwise be hidden assumptions become inspectable data.

Evidence is linked rather than consumed. Sources, documents, observations, and artifacts are referenced through stable identifiers, hashes, or anchors. The same piece of evidence may support multiple claims, contradict others, or change relevance as context evolves. Importantly, evidence does not disappear when a claim is rejected or revised; it remains available for future reinterpretation.

Evaluation is externalized. Assessments of a claim’s support, plausibility, or admissibility are recorded as separate objects rather than overwriting the claim itself. This separation allows different evaluators, models, or institutions to reach different conclusions while operating over the same underlying record. Disagreement is preserved rather than resolved by fiat.

This architecture mirrors how epistemic institutions function in practice. Courts do not store “truth” but case records, testimonies, exhibits, and judgments. Scientific communities do not maintain a single authoritative theory but a corpus of claims, experiments, critiques, and revisions. Knowledge advances not by erasing disagreement but by structuring it.

Non-Boolean ledgers therefore trade finality for traceability. They replace the simplicity of a single accepted state with the durability of a documented reasoning process. While this increases representational complexity, it enables systems to operate in domains where premature closure would otherwise obscure risk, misattribute responsibility, or suppress legitimate dissent.

Crucially, this model does not eliminate the need for decisions. Actions may still require thresholds, policies, or temporary resolutions. The difference is that decisions no longer overwrite the epistemic record. The ledger preserves the claims and counterclaims that informed the decision, enabling later audit, revision, or accountability.

The subsequent sections formalize the components required to operationalize a claim ledger, beginning with the treatment of evidence, context, and admissibility.

2.4 Evidence, Context, and Admissibility

In a claim-centric system, the central question is not whether a claim is true, but whether it is admissible for evaluation. Admissibility defines the minimum conditions under which a claim may participate in the epistemic process of support, critique, and comparison. This distinction is essential in domains where truth cannot be mechanically determined and where premature acceptance would obscure uncertainty.

Evidence is any artifact offered in support of or opposition to a claim. This may include documents, datasets, observations, measurements, images, videos, or references to external records. In a claim ledger, evidence is never reduced to a binary signal. Instead, it is linked to claims through explicit references that preserve provenance, granularity, and context. Hashes, stable identifiers, timestamps, and anchors allow evidence to be revisited without assuming its interpretation is fixed.

Context determines how evidence relates to a claim. Temporal scope, geographic reference, versioning, and intended modality all affect admissibility. A claim may be well-supported in one context and misleading in another. By explicitly encoding context, the system avoids conflating incompatible interpretations under a single evaluation.

Admissibility criteria enforce epistemic hygiene without asserting correctness. At a minimum, an admissible claim must specify an issuer, a scope, a modality (such as assertion, denial, or hypothesis), and at least one reference to supporting or motivating evidence. Claims that fail to meet these requirements are not rejected as false; they are excluded from evaluation until they are sufficiently specified.

This approach separates two often conflated operations: filtering and judging. Boolean systems frequently perform both simultaneously by accepting or rejecting entries as valid or invalid states. A claim ledger performs filtering through admissibility rules and reserves judgment for evaluators. As a result, low-quality or underspecified claims do not contaminate evaluations, while legitimate but controversial claims remain visible.

Importantly, admissibility does not imply neutrality. Criteria may vary by application domain, risk tolerance, or institutional policy. What counts as admissible evidence in a scientific context may differ from that in journalism, due diligence, or autonomous agent negotiation. The ledger accommodates this variation by allowing admissibility rules to be explicit, versioned, and subject to audit.

By grounding evaluation in explicit evidence and context, a claim ledger transforms ambiguity from an invisible liability into a manageable signal. Claims no longer compete for acceptance as truth; they compete for support, coherence, and relevance under stated assumptions. This reframing enables structured disagreement without degenerating into relativism.

The next section examines disagreement directly and argues that, in epistemic systems, disagreement should be treated not as a failure condition but as a source of information.

2.5 Disagreement as Signal, Not Failure

In systems designed around canonical state, disagreement is treated as an error condition. Conflicting inputs must be resolved before entry, competing interpretations are collapsed into a single outcome, and unresolved ambiguity is externalized or discarded. This approach is effective in domains where disagreement is accidental and truth is mechanically decidable.

In epistemic domains, the opposite is often true. Disagreement frequently arises not from error, but from incomplete information, differing assumptions, temporal misalignment, or legitimate interpretive divergence. Suppressing such disagreement does not eliminate uncertainty; it removes the system’s ability to reason about it.

A claim-centric architecture treats disagreement as first-class information. Conflicting claims may coexist within the ledger, each with its own context, evidence, and evaluation history. Rather than forcing convergence, the system records the structure of disagreement: which assumptions differ, which evidence is contested, and where uncertainty remains irreducible.

This representation enables several capabilities that are inaccessible in Boolean systems. First, it allows uncertainty to be localized. Instead of marking an entire outcome as wrong, the system can identify which sub-claims are unsupported or which evidentiary links are weak. Second, it preserves optionality. As new evidence emerges or contexts shift, previously incompatible claims may be reconciled without rewriting history.

Disagreement also functions as a diagnostic signal. Persistent divergence between evaluations may indicate ambiguous language, insufficient evidence, biased sources, or flawed evaluation procedures. In a claim ledger, these signals are visible and auditable rather than silently absorbed into a final state.

Importantly, treating disagreement as signal does not imply epistemic relativism. The system does not assert that all claims are equally valid. Evaluations may still rank claims by support, coherence, or admissibility. Policies may require decisions to be made under uncertainty. The difference is that decisions do not erase the underlying disagreement or its justification.

This shift has practical consequences for AI-assisted systems. When an AI produces an output, disagreement between models, evaluators, or interpretations is recorded and surfaced rather than averaged away. The system explicitly communicates when confidence is low, when evidence is insufficient, or when interpretations diverge. Users are no longer presented with false certainty; they are presented with structured epistemic context.

By preserving disagreement, the architecture aligns system behavior more closely with how reasoning actually occurs in human institutions. Courts, scientific communities, and audits advance not by eliminating dissent, but by documenting it and acting with awareness of its implications.

With this terminology established, the next section introduces the design principles that guide the Epistemic Claim Architecture and explain how these concepts are operationalized in practice.


## 3. Design Principles

The Epistemic Claim Architecture is guided by a set of design principles derived from the limitations identified in prior sections. These principles do not aim to eliminate uncertainty, disagreement, or human judgment. Instead, they seek to make these elements explicit, traceable, and operational within systems that must act despite epistemic limits.

Each principle reflects a deliberate trade-off: favoring robustness over simplicity, accountability over finality, and transparency over illusory certainty.

### 3.1 Process Over State

In epistemic domains, outcomes are less informative than the processes that produced them. A final answer without its reasoning path provides little basis for trust, audit, or revision. The architecture therefore prioritizes the documentation of reasoning processes over the preservation of canonical end states.

Rather than asking “What is the correct state?”, the system asks “How was this claim formed, evaluated, and acted upon?”. Process traces enable retrospective analysis, responsibility attribution, and iterative improvement. They also allow systems to remain usable even when conclusions change.

State is treated as a snapshot of process, not its replacement.

### 3.2 Admissibility Over Correctness

The architecture does not attempt to determine whether claims are correct in any absolute sense. Instead, it enforces criteria for admissibility: whether a claim is sufficiently specified, attributable, contextualized, and supported to warrant evaluation.

This distinction prevents premature closure. Claims that are controversial, incomplete, or uncertain are not excluded on that basis alone. At the same time, underspecified or unsupported assertions are prevented from contaminating evaluations.

Correctness may be pursued by evaluators, institutions, or downstream decision-makers, but it is not assumed by the infrastructure itself.

### 3.3 Pluralism Over Consensus

Consensus is costly, fragile, and often unnecessary. Many systems require action under persistent disagreement, not its elimination. The architecture therefore favors pluralism: the coexistence of multiple claims, evaluations, and interpretations within a shared framework.

Pluralism does not imply equal weighting. Claims may be ranked, filtered, or preferred according to explicit policies. The key distinction is that disagreement is preserved and visible rather than collapsed into an averaged or authoritative outcome.

By avoiding forced consensus, the system remains adaptable as evidence evolves and contexts shift.

### 3.4 Traceability Over Finality

Finality provides closure but sacrifices insight. Once a decision is finalized without traceability, errors become difficult to diagnose and responsibility difficult to assign. The architecture therefore treats traceability as a higher-order value than finality.

Every claim, evaluation, and action is linked to its inputs, assumptions, and evaluators. This enables forensic analysis, replay, and accountability without requiring that decisions be indefinitely reversible.

Finality, where required, is treated as a policy choice layered on top of a traceable epistemic substrate.

### 3.5 Privacy-Preserving Evaluation (Optional Modes)

Many epistemic processes involve sensitive or confidential information. The architecture accommodates this by separating evaluation from disclosure. Claims and evidence may be assessed without being publicly revealed, provided that admissibility and traceability requirements are met.

This enables use cases such as confidential due diligence, private negotiation, and regulated environments where transparency must be selective rather than absolute. Privacy-preserving modes are treated as extensions of the same epistemic principles, not exceptions to them.




10.2 The Blockchain Irony: Accepted Technology, Misapplied Use

One of the central ironies of blockchain adoption is that a technology originally designed to preserve history has been widely deployed in ways that actively erase it. Boolean consensus mechanisms do not merely resolve disagreement; they perform epistemic compression by collapsing complex, contested situations into a single canonical outcome.

When a blockchain-based system selects a final state, competing claims, minority interpretations, adversarial testimony, and alternative evidentiary paths become inaccessible from the canonical record. Although traces may exist outside the chain, the system itself treats the accepted state as sufficient. In epistemic terms, information is not only abstracted but destroyed as a usable object of reasoning.

This form of information loss is appropriate in domains such as payment validation or state synchronization, where ambiguity is undesirable and the underlying propositions are mechanically decidable. Outside these domains, the same mechanism becomes pathological.

An analogy to legal systems helps clarify the problem. Imagine a court that is required to choose strictly between absolute guilt and absolute innocence. No mitigating circumstances are admissible. No degrees of responsibility are recognized. Once a verdict is reached, all case materials—testimonies, exhibits, expert reports, procedural records—are discarded. Only the final judgment remains.

Such a system would be intolerable, not because decisions must never be final, but because legitimacy in legal judgment depends on the preservation of reasoning, evidence, and contestation. The authority of a verdict derives from its traceability, not merely from its finality.

Boolean blockchains, when applied to epistemic domains, replicate this failure mode. They retain the verdict while discarding the trial. The canonical chain becomes a record of outcomes without a durable account of how those outcomes were justified, challenged, or revised over time.

Claim ledgers invert this relationship. They treat the preservation of claims, counterclaims, and evidence as primary, and treat decisions as contextual, policy-bound overlays rather than epistemic endpoints. Majority and minority positions coexist. Adversarial claims remain inspectable. Temporal evolution is explicit rather than overwritten.

This outcome is particularly ironic given the historical motivations behind blockchain systems. Early blockchain designs were explicitly hostile to centralized authority, seeking to eliminate trusted intermediaries and single points of control. Yet when Boolean blockchains are applied outside of narrowly defined settlement domains, they tend to recreate a different form of centralization.

This centrality does not arise from administrative power or ownership, but from epistemic finality. The canonical chain becomes an unquestionable reference point, not because it is always correct, but because it is the only state the system is able to represent. In domains where meaning, evidence, and interpretation matter, this effectively concentrates authority in the mechanism of consensus itself.

What emerges is a paradoxical structure: a decentralized system that enforces a single authoritative narrative. Attempts to use such systems for governance, knowledge production, or dispute resolution often reintroduce institutional hierarchies through policy layers, off-chain arbitration, or privileged interpreters—centralization re-entering through the back door.

The issue is not decentralization as a goal, but the assumption that decentralization of state implies decentralization of epistemic authority. Claim-based architectures challenge this assumption by separating the preservation of shared process from the enforcement of a single outcome.

This distinction explains why blockchain technology has seen limited adoption outside financial settlement, despite being well-suited in principle to domains that value shared process, durability, independence, and censorship resistance. The failure is not one of cryptography or decentralization, but of epistemic fit. Boolean ledgers enforce finality where traceability is required.

A subtle but revealing aspect of this misalignment is linguistic rather than technical. Within mainstream blockchain discourse, the term “ledger” is implicitly assumed to denote a Boolean structure converging toward a single canonical state. The distinction between Boolean and non-Boolean ledgers is rarely articulated, not because it lacks relevance, but because the Boolean assumption has remained largely unexamined. When an architectural choice becomes a default, it disappears from vocabulary and ceases to be perceived as a choice at all. By explicitly naming this distinction, claim-based architectures open a design space that has remained effectively invisible within dominant blockchain practice.

By replacing forced consensus with structured pluralism, claim-based architectures recover the original promise of distributed ledgers: not as machines for declaring truth, but as neutral substrates for documenting how truth is argued, evaluated, and acted upon over time.

Author:
Teemu Lantta
teemu.tuomas.lantta@gmail.com
X: TeemuLantta
