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

4. Epistemic Claim Architecture Overview

The Epistemic Claim Architecture (ECA) is designed to support reasoning, evaluation, and action in domains where truth cannot be reduced to a single canonical state. Rather than attempting to eliminate uncertainty or disagreement, the architecture provides a structured substrate for expressing claims, linking evidence, recording evaluations, and preserving the processes that connect them.

At a high level, the architecture separates three distinct but interacting concerns:
(1) the recording of claims,
(2) the evaluation of those claims, and
(3) the traceability of the processes through which claims are formed and acted upon.

These concerns are implemented through three primary components: the Claim Ledger, the Neutral Witness, and the Flight Recorder. Each component has a clearly defined role and operates independently, yet their interaction produces an auditable and pluralistic epistemic system.

The architecture is intentionally modular. None of the components presuppose a specific blockchain, storage backend, or AI model. This allows the system to be deployed incrementally, adapted to different risk profiles, and integrated into existing institutional or technical environments.

4.1 System Diagram and Data Flows

Conceptually, the Epistemic Claim Architecture can be understood as a loop rather than a pipeline. Claims are issued and recorded, evaluated against evidence and context, acted upon under policy constraints, and subsequently re-evaluated as new information becomes available. No step irreversibly overwrites the epistemic record.

The Claim Ledger serves as the persistent layer. It stores claims as first-class objects, along with their metadata, evidentiary links, and relationships to other claims. The ledger does not determine truth; it preserves assertions and their evolution over time.

The Neutral Witness operates as an evaluation layer external to the ledger. Given a claim, associated evidence, and relevant context, the witness produces a structured assessment indicating whether the claim is supported, contradicted, insufficiently specified, or unclear. Crucially, the witness records how it interpreted the claim and which materials informed its assessment.

The Flight Recorder captures the procedural trace of reasoning and action. For AI-assisted systems, this includes model invocations, tool calls, retrieved artifacts, intermediate claims, and decision points. For human-in-the-loop processes, it may include structured annotations or checkpoints. These traces allow outcomes to be reconstructed, audited, and attributed without requiring that the underlying systems be perfectly reliable.

Data flows between these components are explicit and directional. The ledger provides inputs to witnesses and agents. Witness reports and process traces are written back as new claims or attestations. Actions taken on the basis of claims generate additional trace data, which may later become evidence in subsequent evaluations.

This separation ensures that no single component becomes an epistemic authority. The ledger does not evaluate, the witness does not decide, and the recorder does not judge. Authority emerges only through documented interaction among these parts.

The following sections describe each component in detail, beginning with the Claim Ledger.

4.2 Separation of Roles: Claim vs Evidence vs Witness Report

A core design decision of the Epistemic Claim Architecture is the strict separation between claims, evidence, and witness reports. Although these elements are tightly related, conflating them leads to epistemic failure modes that are difficult to detect and impossible to audit after the fact.

A claim is an assertion made by an identifiable issuer. It expresses a proposition about the world under a specified context, scope, and modality. Claims may be true or false, supported or unsupported, but the ledger itself does not assume any of these properties. Its role is to preserve the assertion as made, not to validate it.

Evidence consists of artifacts offered in relation to a claim. Evidence does not speak for itself; it acquires meaning only in context and relative to an interpretation. The same evidence may support multiple claims, contradict others, or become irrelevant as assumptions change. For this reason, evidence is never embedded into claims as truth, but linked as a reference with preserved provenance and granularity.

A witness report is an evaluation of a claim relative to a set of evidence, assumptions, and evaluation policies. Witnesses do not assert new facts about the world; they produce structured assessments about the relationship between claims and evidence. Crucially, a witness report must always declare how the claim was interpreted and under which constraints the evaluation was performed.

Separating these roles prevents several common failure modes. When claims and evaluations are merged, subjective judgments are mistaken for objective facts. When evidence is overwritten by conclusions, minority interpretations and alternative readings are lost. When evaluators are allowed to modify claims directly, responsibility and accountability become blurred.

The separation also enables pluralism. Multiple witnesses may evaluate the same claim differently, using different models, data sources, or policies. Their reports may agree, partially overlap, or directly conflict. All such outcomes are valid records. The system does not require reconciliation unless imposed by a downstream decision policy.

This design mirrors established epistemic institutions. In legal systems, testimony, exhibits, and judgments are distinct objects with different rules of admissibility and authority. In scientific practice, experimental results, hypotheses, and peer reviews occupy separate roles. The Epistemic Claim Architecture formalizes this separation at the infrastructure level.

By enforcing role separation, the architecture ensures that epistemic authority does not collapse into a single layer. Claims remain claims, evidence remains interpretable, and evaluations remain attributable judgments. This clarity is essential for traceability, disagreement preservation, and long-term auditability.

4.3 Minimal Viable Platform Assumptions (fast, cheap, “good enough” security)

The Epistemic Claim Architecture is designed to function under pragmatic constraints. It does not assume perfect security, universal trust, or ideal operating conditions. Instead, it is explicitly shaped to be deployable early, incrementally, and at low cost, while still delivering meaningful epistemic benefits.

At a minimum, the platform assumes the availability of persistent storage, basic identity and signing mechanisms, and reliable timestamping. Strong cryptographic guarantees, decentralized consensus, or tamper-proof hardware are advantageous but not required for the architecture to be useful. The system remains valuable even when some components are operated in semi-trusted or centralized environments.

This is a deliberate design choice. Epistemic robustness does not depend on eliminating all possible failures, but on making failures visible and attributable. A claim ledger running on conventional databases can already preserve competing claims, evidence links, and evaluation histories. Even if records can theoretically be altered, the architecture still improves over systems that overwrite disagreement entirely.

Performance and cost are treated as first-class concerns. Claim creation, evidence linking, and witness evaluation must be fast enough to support real-world workflows, including automated agent interactions. Storage costs are minimized by favoring references, hashes, and summaries over raw data retention. Full artifacts may be stored off-chain or externally, with integrity verified through content addressing.

Security guarantees are layered rather than absolute. Higher-risk deployments may incorporate stronger anchoring, distributed storage, or hardware-backed execution. Lower-risk or exploratory deployments may accept weaker guarantees in exchange for speed and flexibility. The architecture does not mandate a single security posture; it allows deployments to choose an appropriate point on the cost–assurance spectrum.

Importantly, the system is resilient to partial compromise. If a witness is biased, its reports remain attributable. If a data source is poisoned, the resulting claims can be contested. If a storage backend fails, previously exported or anchored records retain evidentiary value. The architecture assumes that failures will occur and focuses on containing their epistemic impact rather than preventing them entirely.

By adopting “good enough” security as a baseline, the Epistemic Claim Architecture lowers the barrier to adoption and experimentation. It allows organizations to begin capturing claims, evaluations, and process traces immediately, and to strengthen guarantees over time as requirements evolve. This incremental path is essential for adoption outside narrowly defined, high-assurance domains.

The next section outlines the threat model assumed by the architecture and clarifies which classes of failure it is designed to expose, tolerate, or explicitly exclude.

4.4 Threat Model at a Glance

The Epistemic Claim Architecture is not designed to prevent all forms of failure, manipulation, or adversarial behavior. Instead, it is designed to make epistemically relevant failures observable, attributable, and contestable. This threat model reflects that priority.

The architecture assumes that participants may be mistaken, biased, or strategically motivated. Claims may be false. Evidence may be incomplete, misleading, or selectively presented. Evaluators may disagree or apply flawed methodologies. These conditions are treated as normal operating assumptions rather than exceptional cases.

Accordingly, the system does not attempt to guarantee correctness, truthfulness, or honesty. It does not prevent misinformation from being submitted, nor does it assume that any single evaluator, model, or institution is trustworthy by default. Its primary defense is transparency of process rather than exclusion of actors.

The architecture is explicitly designed to expose the following classes of risk:

Overclaiming: assertions presented without sufficient scope, context, or evidence.

Ambiguity masking: forced interpretations that hide unresolved assumptions.

Evaluator bias: systematic tendencies in witness reports, made visible through attribution and comparison.

Evidence fragility: broken links, outdated sources, or contested provenance.

Responsibility diffusion: outcomes without a traceable chain of reasoning or decision-making.

At the same time, the architecture does not aim to fully mitigate certain threats. These include collusion among participants, coordinated misinformation campaigns, or coercive external pressures. While such behaviors may leave detectable traces within the system, preventing them entirely is outside the scope of the infrastructure.

Security breaches and data tampering are similarly treated as contingent risks rather than absolute failures. If records are altered, missing, or compromised, the architecture focuses on preserving evidence of inconsistency and maintaining the ability to contest affected claims. Stronger guarantees, such as tamper-evident logs or cryptographic anchoring, may be layered on top where required but are not assumed universally.

This threat model reflects a broader design philosophy: epistemic systems should prioritize auditability over invulnerability. In environments where uncertainty and disagreement are unavoidable, the ability to reconstruct how a conclusion was reached is often more valuable than the ability to assert that it cannot be questioned.

With this threat model established, the paper now turns to the detailed design of the first core component of the architecture: the Claim Ledger.

5. Claim Ledger

The Claim Ledger is the persistent substrate of the Epistemic Claim Architecture. Its role is to record claims as first-class objects, along with their context, provenance, and relationships, without asserting their correctness or forcing convergence toward a single canonical state.

Unlike traditional ledgers, the Claim Ledger does not encode truth as state. It encodes assertions as artifacts. Its primary function is preservation rather than validation: to ensure that claims, supporting materials, and subsequent evaluations remain inspectable over time, even as interpretations change.

The ledger is intentionally conservative in what it assumes and permissive in what it records. It enforces structural requirements for admissibility, attribution, and traceability, but delegates judgment, ranking, and decision-making to external evaluators and policies. This separation allows the ledger to remain neutral while supporting a wide range of epistemic workflows.

At a conceptual level, the Claim Ledger can be understood as a graph rather than a chain. Claims reference evidence, relate to other claims, and accumulate evaluations and revisions. No operation irreversibly overwrites prior assertions. New information extends the graph; it does not collapse it.

The following sections describe the data model, linking semantics, and operational properties of the Claim Ledger in detail, beginning with the structure of an individual claim.

5.1 Claim Data Model

A claim is a structured assertion about the world, issued by an identifiable actor under specified conditions. The Claim Ledger represents claims explicitly rather than implicitly, making interpretive choices visible and auditable.

At minimum, a claim consists of the following components:

Proposition: a subject–predicate–object (S–P–O) triple expressing the core assertion.

Context: qualifiers defining scope, such as time, location, domain, or version.

Modality: the stance of the issuer (e.g., assertion, denial, hypothesis).

Uncertainty: an explicit expression of confidence, range, or epistemic status.

In addition, each claim includes metadata required for attribution and lifecycle management, such as:

Claim identifier: a stable, unique reference.

Issuer identity: cryptographically or institutionally attributable.

Timestamp: indicating when the claim was made.

Audience or sensitivity level (optional): constraining visibility or use.

This model deliberately avoids embedding evaluation outcomes into the claim itself. A claim does not become “true” or “false” within the ledger. Instead, it becomes linked to evidence, counterclaims, and witness reports that collectively define its epistemic position.

By enforcing explicit structure, the data model prevents common failure modes of natural language reasoning. Implicit scope becomes explicit scope. Vague assertions are either clarified or rendered inadmissible. Confidence is stated rather than inferred. What would otherwise be hidden assumptions are promoted to inspectable fields.

The Claim Data Model is designed to be minimal but extensible. Domains may introduce additional fields or constraints, provided that the core distinction between assertion, evidence, and evaluation is preserved.

Subsequent sections describe how claims are linked to evidence, versioned over time, and related to one another within the ledger graph.

5.2 Evidence Linking (URLs, hashes, anchors, provenance)

In the Claim Ledger, evidence is treated as a referenced artifact rather than embedded content. This design choice reflects the fact that evidence rarely has a single, stable interpretation and must remain accessible for re-evaluation as claims, contexts, and evaluators change.

Evidence may take many forms, including documents, datasets, images, videos, sensor readings, transcripts, or external records. Regardless of format, evidence is linked to claims through explicit references that preserve identity, provenance, and granularity. The ledger does not assume that evidence is immutable or authoritative; it assumes only that references to evidence must be stable and inspectable.

At a minimum, an evidence reference includes:

a locator, such as a URL, content address, or storage identifier,

a cryptographic hash or fingerprint, where available, to detect modification,

a type or modality descriptor (e.g., document, observation, dataset, testimony),

and provenance metadata, describing origin, authorship, or acquisition method.

Where possible, evidence references may include anchors to specific fragments rather than entire artifacts. Page numbers, paragraph identifiers, timestamps, bounding boxes, or byte ranges allow claims to cite precisely what portion of an artifact is relevant. This avoids the common failure mode of citing large sources while relying on unstated interpretation.

Evidence linking is many-to-many. A single piece of evidence may support multiple claims, contradict others, or become contested over time. Conversely, a claim may reference multiple evidentiary artifacts, each contributing partial support under different assumptions. The ledger preserves these relationships explicitly rather than collapsing them into a single judgment.

Importantly, evidence is never consumed or invalidated by evaluation outcomes. When a claim is revised, rejected, or superseded, its evidence links remain intact. This allows downstream auditors, evaluators, or agents to revisit the evidentiary landscape and ask not only what was concluded, but why alternative interpretations were not adopted.

The ledger does not require that evidence be publicly accessible. References may point to encrypted artifacts, confidential repositories, or controlled-access systems. In such cases, the ledger records the existence and identity of the evidence without disclosing its contents, enabling later verification under appropriate access conditions.

Anchoring mechanisms may be used to strengthen temporal and integrity guarantees. Hashes or summaries of evidence references may be timestamped or anchored in external systems to establish that a given artifact existed in a particular form at a particular time. While such anchoring improves robustness, it is optional rather than foundational to the architecture.

By separating evidence identity from evidence interpretation, the Claim Ledger enables durable reasoning across time, institutions, and evaluators. Evidence does not disappear when claims change. It remains available as a shared reference point for future disagreement, refinement, or corroboration.

5.3 Claim Status and Versioning

Claims recorded in the Claim Ledger are not static. As new evidence emerges, contexts shift, or interpretations are refined, claims may evolve. The architecture accommodates this evolution through explicit status indicators and versioning mechanisms that preserve history rather than overwrite it.

Each claim carries a status reflecting its current epistemic position within the ledger. Typical statuses include proposed, contested, revised, superseded, retracted, or merged. These statuses do not assert correctness; they describe how the claim relates to subsequent claims and evaluations.

Versioning is append-only. When a claim is modified, clarified, or narrowed in scope, a new claim is issued that references the prior version. The original claim remains intact and inspectable. This ensures that earlier assertions, including those later deemed flawed or misleading, are preserved as part of the epistemic record.

Supersession and retraction are treated as explicit actions rather than silent updates. A claim that is retracted remains visible, along with the rationale for its retraction and the identity of the actor who performed it. This prevents the erasure of error and supports accountability and learning.

Claims may also be merged or split. Multiple overlapping claims may be consolidated into a more precise formulation, or a broad claim may be decomposed into narrower assertions. These transformations are represented through explicit relationships rather than destructive edits.

Temporal context is preserved across versions. Each claim reflects what was asserted at a particular moment, under particular assumptions, using the evidence available at that time. This enables time-sliced analysis, allowing evaluators to ask not only whether a claim is supported now, but whether it was reasonable given what was known then.

By making change explicit, the Claim Ledger avoids a common failure mode of state-based systems: silent correction. Errors are not hidden by updates; they are documented. Revision becomes a signal of epistemic progress rather than an admission of failure.

The following section introduces the semantic relationships between claims, enabling the construction of claim graphs that capture support, contradiction, refinement, and dependency.

5.4 Claim Graph Semantics

(supports / contradicts / refines / depends-on / derived-from)

The Claim Ledger represents epistemic structure as a graph rather than a linear history. Claims are nodes within this graph, connected by explicitly typed relationships that describe how assertions relate to one another. These relationships encode meaning that would otherwise be implicit, disputed, or lost.

At a minimum, the architecture supports the following relationship types:

supports: indicates that one claim provides evidentiary or inferential support for another. Support does not imply sufficiency or correctness; it expresses directional relevance.

contradicts: indicates that two claims cannot both hold under the same assumptions or scope. Contradiction is contextual and may dissolve if assumptions are refined.

refines: indicates that a claim narrows, clarifies, or qualifies another claim without rejecting it. Refinement preserves continuity while increasing precision.

depends-on: indicates that the validity or interpretation of a claim relies on another claim being accepted or provisionally assumed.

derived-from: indicates that a claim is inferred or constructed from one or more other claims, possibly through an explicit reasoning or transformation process.

These relationships are first-class objects. They are recorded explicitly, attributed to an issuer, and subject to evaluation like claims themselves. This avoids embedding semantic assumptions into undocumented inference logic.

Graph semantics enable the system to localize disagreement. Rather than marking an entire conclusion as unsupported, evaluators can identify which supporting claims are weak, which dependencies are contested, or where contradictions arise. This granularity allows reasoning to proceed even when parts of the graph remain unstable.

The graph structure also supports incremental reasoning. New claims may attach to existing structures without requiring global recomputation or consensus. As evidence accumulates or interpretations shift, only affected subgraphs need to be reconsidered.

Importantly, the claim graph does not impose acyclicity or convergence. Cycles, competing derivations, and unresolved contradictions are permissible and expected. The goal is not to produce a single resolved tree, but to preserve the structure of reasoning as it unfolds over time.

By encoding epistemic relationships explicitly, the Claim Ledger transforms disagreement and dependency from hidden liabilities into navigable structures. This enables both humans and machines to reason over contested domains without forcing premature closure.

5.5 Identity and Signatures

(DID / domain identity, roles, delegation)

Claims, evidence links, and relationships in the Claim Ledger are only meaningful if they are attributable. The architecture therefore treats identity and signing not as optional metadata, but as foundational elements of epistemic accountability.

Each claim is issued by an identifiable actor. Identity may be represented through decentralized identifiers (DIDs), domain-based identities, organizational keys, or other verifiable schemes appropriate to the deployment context. The architecture does not mandate a single identity standard; it requires only that identities be stable, referenceable, and verifiable within the system’s trust assumptions.

All claims and claim relationships are cryptographically signed or otherwise authenticated by their issuer. Signatures bind the content of the claim, its context, and its metadata to the issuing identity at a specific point in time. This ensures that assertions cannot be silently altered without detection and that responsibility remains attributable even as claims evolve.

Identity in the Claim Ledger is role-sensitive. An actor may issue claims, provide evidence, evaluate claims, or define admissibility policies under different roles. These roles are explicit rather than implicit, allowing downstream systems to distinguish between assertions, assessments, and procedural actions. Role separation prevents authority leakage, where evaluative power is mistaken for epistemic fact.

Delegation is treated as a first-class concept. Actors may delegate claim issuance or evaluation authority to agents, institutions, or automated systems. Such delegation is explicitly recorded, scoped, and revocable. When an AI system issues a claim on behalf of an organization or individual, the ledger records both the agent and the delegator, preserving clarity of responsibility.

The architecture does not assume that identities are truthful, honest, or persistent. Identities may be compromised, abandoned, or malicious. Rather than attempting to prevent such failures, the ledger makes their effects traceable. Patterns of behavior, conflicting claims, or systematic bias can be analyzed at the identity level without granting any identity intrinsic trust.

By anchoring claims to explicit identities and signatures, the Claim Ledger transforms anonymity and authority into configurable design choices rather than implicit defaults. High-trust environments may rely on strong institutional identities, while open or adversarial settings may permit pseudonymity coupled with reputation or bonding mechanisms.

This approach enables accountability without centralization. Authority emerges from documented action and evaluation, not from privileged control over the ledger itself.

5.6 Anchoring and Storage

(off-chain data, on-chain timestamps, portability)

The Claim Ledger is storage-agnostic by design. It does not require that claims, evidence, or process traces reside on a specific blockchain or distributed storage system. Instead, it separates where data is stored from how it is identified, referenced, and anchored in time.

Claims and their metadata may be stored in conventional databases, distributed object stores, content-addressed networks, or hybrid systems. Large or sensitive artifacts such as documents, images, videos, or full process logs are typically kept off-chain to reduce cost and support access control. The ledger records stable references to these artifacts rather than embedding them directly.

Anchoring provides temporal integrity without enforcing semantic authority. Hashes or summaries of claims, evidence references, or ledger states may be timestamped or anchored into an external system, such as a blockchain or trusted timestamping service. Anchoring establishes that a specific assertion or artifact existed in a given form at a given time, without asserting that it is correct or complete.

This distinction is critical. The blockchain is used as a clock and a witness of existence, not as a judge of truth. It strengthens auditability while avoiding the epistemic overreach of treating canonical chain state as authoritative meaning.

Portability is a core requirement. Claim Ledgers must support export and import of claims, evidence references, and relationship graphs in canonical, versioned formats. This allows records to outlive any particular storage backend, vendor, or institution. Portability also enables parallel ledgers to interoperate, compare claims, or federate evaluations without requiring global consensus.

The architecture supports layered durability. Lightweight deployments may rely on local storage and periodic backups. Higher-assurance deployments may combine replicated databases, content-addressed storage, and multiple independent anchors. These choices affect risk tolerance and cost but do not change the epistemic model.

Importantly, anchoring is optional and contextual. Some claims require strong temporal guarantees; others do not. The absence of anchoring does not invalidate a claim, but it does affect how much weight downstream evaluators may assign to it. This allows temporal assurance to be treated as an explicit dimension of evaluation rather than a hidden assumption.

By decoupling storage, anchoring, and meaning, the Claim Ledger avoids the false equivalence between durability and truth. Data can persist without being canonized, and history can be preserved without being frozen.




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
