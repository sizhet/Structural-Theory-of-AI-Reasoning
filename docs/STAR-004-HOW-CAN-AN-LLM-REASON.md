# STAR-004 — How Can an LLM Reason?

## Distributed Computation, Latent Structure, Reasoning Trajectories, and the Boundary of Explanation

**Repository:** Structural Theory of AI Reasoning
**Series:** STAR — Structural Theory of AI Reasoning
**Document:** STAR-004
**Status:** Core Theory Paper

---

## Abstract

Large Language Models demonstrate reasoning capabilities that cannot be adequately characterized as simple lookup, single-point classification, or Per-Node Winner-Take-All decision making.

An LLM can interpret a problem, transform representations, construct intermediate relations, decompose tasks, generate hypotheses, revise earlier conclusions, follow multi-step trajectories, use tools, and produce novel combinations that were not explicitly supplied in the prompt.

These behaviors constitute important evidence of reasoning capability.

They do not, however, imply that the complete internal mechanism of LLM reasoning is already understood.

This paper therefore separates three questions:

1. **Can an LLM exhibit reasoning behavior?**
2. **What computational properties plausibly support that behavior?**
3. **How far can we confidently explain the internal structure of that reasoning?**

At a useful structural level, LLM reasoning can be interpreted as emerging from distributed learned representations, attention-mediated interactions, repeated transformations across layers, and autoregressive trajectories in which generated outputs modify the context for subsequent computation.

This suggests:

$$
\boxed{
LLM\ Reasoning
\neq
Simple\ Per\text{-}Node\ Winner\text{-}Take\text{-}All
}
$$

and supports a broader interpretation:

$$
\boxed{
LLM\ Reasoning
\approx
Implicit / Latent / Distributed\ Structural\ Reasoning
}
$$

This paper does not claim that an LLM contains explicit internal equivalents of Differential Trees, Calling Graphs, CCCs, or TaskGraphs.

Rather, it proposes that strong LLM reasoning behavior is consistent with the existence of learned latent relationships and distributed computational structures capable of producing functionally structured reasoning trajectories.

This distinction prepares the foundation for the next major concept in this series:

$$
\boxed{
LLM\ Reasoning
\ as
\ Selective\ Unfolding
}
$$

and ultimately for the convergence:

$$
\boxed{
LLM\ Unfolding
\leftrightarrow
Structural\ Intelligence\ Localization
}
$$

---

# 1. The Question Is No Longer Simply "Can LLMs Reason?"

Early discussions of language models often framed the issue as a binary question:

> Can a language model really reason?

The observable capabilities of modern LLMs make this binary framing increasingly unproductive.

LLMs can perform tasks involving:

* decomposition;
* comparison;
* abstraction;
* planning;
* mathematical transformation;
* program generation;
* debugging;
* hypothesis generation;
* explanation;
* analogy;
* synthesis;
* revision;
* tool selection;
* multi-stage problem solving.

Performance is imperfect.

Failures remain substantial.

But the existence of failure does not eliminate the reasoning capability demonstrated by successful cases.

A more productive question is:

> **What kind of reasoning does an LLM perform, what computational properties support it, and where are its structural boundaries?**

This paper addresses that question.

---

# 2. Three Levels Must Be Distinguished

Any theory of LLM reasoning should distinguish three levels.

## Level 1 — Behavioral Evidence

What can the system demonstrably do?

For example:

$$
Problem
\rightarrow
Decomposition
\rightarrow
Intermediate\ Results
\rightarrow
Synthesis
\rightarrow
Solution
$$

These are externally observable behaviors.

---

## Level 2 — Computational Architecture

What known computational mechanisms participate?

Examples include:

* learned parameters;
* token representations;
* attention;
* MLP transformations;
* residual pathways;
* repeated Transformer layers;
* autoregressive generation;
* context reuse.

These mechanisms are known parts of the architecture.

---

## Level 3 — Mechanistic Explanation of Reasoning

Exactly how does a particular reasoning concept, dependency, abstraction, or intermediate inference arise from those computations?

This is substantially harder.

Therefore:

$$
\boxed{
Behavioral\ Capability
\neq
Complete\ Mechanistic\ Explanation
}
$$

Maintaining this distinction is essential.

---

# 3. A Useful Epistemic Boundary

This repository proposes structural explanations of AI reasoning.

It should therefore avoid two opposite errors.

## Error A — Understatement

> LLMs merely predict the next token and therefore do not reason.

This description is too weak at the behavioral level.

Next-token generation can be the output interface of a computational system whose internal processing supports complex transformations.

---

## Error B — Overstatement

> Because LLMs demonstrate reasoning behavior, we therefore know exactly how reasoning is internally represented.

This is also unjustified.

Strong behavioral evidence does not automatically reveal the full internal mechanism.

The appropriate position is:

$$
\boxed{
Observe\ Capability
+
Analyze\ Architecture
+
Maintain\ Mechanistic\ Humility
}
$$

---

# 4. LLM Reasoning Is Not Simple Winner-Take-All

A simple decision model might be represented as:

```text id="3b6c93"
Input
  |
  v
Candidate A
Candidate B
Candidate C
  |
  v
Score
  |
  v
Winner
  |
  v
Output
```

This can describe certain local decisions.

It does not adequately describe a long LLM reasoning trajectory.

Consider instead:

$$
Context_t
\rightarrow
Computation_t
\rightarrow
Token_t
$$

The generated token becomes part of the subsequent context:

$$
Context_{t+1}
=
Context_t
+
Token_t
$$

Then:

$$
Context_{t+1}
\rightarrow
Computation_{t+1}
\rightarrow
Token_{t+1}
$$

Thus:

$$
\boxed{
State_t
\rightarrow
Computation_t
\rightarrow
State_{t+1}
}
$$

is repeatedly instantiated.

The reasoning process therefore has a trajectory.

---

# 5. Autoregression Creates a Computational Trajectory

A generated sequence can be represented as:

$$
x_1,x_2,...,x_t
$$

with:

$$
P(x_{t+1}|x_1,...,x_t)
$$

At every generation step, the available context changes.

Therefore:

$$
C_t
\neq
C_{t+1}
$$

and the computation applied at the next step operates under a modified context.

A long reasoning process becomes:

$$
C_0
\rightarrow
O_1
\rightarrow
C_1
\rightarrow
O_2
\rightarrow
C_2
\rightarrow
...
\rightarrow
O_n
$$

where each output contributes to the state from which later outputs are generated.

This provides a basic mechanism for:

$$
\boxed{
Trajectory\ Reasoning
}
$$

The trajectory can progressively construct a solution.

---

# 6. A Reasoning Trajectory Can Change Its Own Local Problem

Suppose the original problem is:

$$
P_0
$$

The model decomposes it into:

$$
P_1,P_2,P_3
$$

After solving \(P_1\), new information becomes available:

$$
E_1
$$

Now the effective problem is no longer simply \(P_0\).

It becomes:

$$
P_0 + E_1
$$

After additional reasoning:

$$
P_0 + E_1 + E_2
$$

Thus reasoning can transform the context in which subsequent reasoning occurs.

This is more than static classification.

It is:

$$
\boxed{
Progressive\ Contextual\ Transformation
}
$$

---

# 7. Transformer Computation Is Distributed

An LLM does not generally assign one explicit human-readable reasoning function to one physical node.

Its computation is distributed.

A simplified Transformer stack can be represented as:

$$
X_0
\xrightarrow{L_1}
X_1
\xrightarrow{L_2}
X_2
\rightarrow
...
\xrightarrow{L_n}
X_n
$$

Each layer transforms representations.

A simplified residual-layer view is:

$$
X_{l+1}
=
X_l
+
Attention_l(X_l)
+
MLP_l(X_l')
$$

where the exact architecture varies by model.

The important point is not the particular formula.

The important point is:

> **Reasoning behavior can emerge from many interacting transformations rather than from one explicit reasoning module.**

---

# 8. Attention Provides Conditional Relational Interaction

Attention allows token representations to interact conditionally with other representations.

At a high level:

$$
Query
\rightarrow
Relevant\ Keys
\rightarrow
Weighted\ Values
$$

This allows computation to depend on relationships across the available context.

Such interactions can support functions relevant to reasoning, including:

* reference resolution;
* comparison;
* dependency tracking;
* contextual association;
* relation composition.

But attention itself should not simply be equated with reasoning.

Rather:

$$
\boxed{
Attention
\ is\ one\ computational\ mechanism
\ participating\ in\ reasoning.
}
$$

Reasoning emerges from the larger computation.

---

# 9. MLP Transformations Also Matter

Attention receives substantial conceptual attention because its relationships are intuitively appealing.

However, Transformer reasoning cannot be reduced to attention alone.

MLP components participate in representation transformation and learned computation.

Thus a better abstraction is:

$$
Representation
\rightarrow
Attention\ Interaction
\rightarrow
Transformation
\rightarrow
Residual\ Integration
\rightarrow
Next\ Representation
$$

repeated across many layers.

The resulting process is:

$$
\boxed{
Distributed\ Representation\ Transformation
}
$$

rather than one simple symbolic reasoning step.

---

# 10. Reasoning Need Not Live in One Layer

It is tempting to imagine:

```text id="f6tt2d"
Lower Layers = Language

Middle Layers = Knowledge

Upper Layers = Reasoning
```

This may be a useful heuristic in some contexts, but it is too strong as a general theory.

A more careful interpretation is:

> **Reasoning behavior may emerge from distributed computation across layers, representations, attention interactions, MLP transformations, residual pathways, and repeated autoregressive reuse of generated context.**

Thus:

$$
Reasoning
\neq
One\ Layer
$$

and perhaps:

$$
Reasoning
\neq
One\ Module
$$

Instead:

$$
\boxed{
Reasoning
\ may\ be
\ a\ distributed\ runtime\ phenomenon.
}
$$

---

# 11. Learned Representations Contain Latent Relationships

Language contains enormous amounts of structural information.

For example:

* categories;
* hierarchies;
* causal statements;
* procedures;
* temporal relationships;
* mathematical relations;
* social relations;
* program structures;
* scientific concepts;
* argument patterns.

Training exposes a model to many manifestations of these structures.

The resulting parameterized system can support relationships that are not stored as a conventional explicit graph.

This motivates the term:

$$
\boxed{
Latent\ Structure
}
$$

The word "latent" is important.

We are not claiming:

$$
LLM
=
Hidden\ CallingGraph
$$

or:

$$
LLM
=
Hidden\ DifferentialTree
$$

Rather:

> **The model can encode and operationalize relational regularities without representing them in the same explicit form used by Structural Intelligence.**

---

# 12. Implicit Structural Reasoning

This leads to a useful conceptual category:

$$
\boxed{
Implicit\ Structural\ Reasoning
}
$$

An LLM may produce behavior corresponding to:

* classification;
* branching;
* dependency resolution;
* contextual selection;
* decomposition;
* relational traversal;
* structural completion.

But these operations are not necessarily exposed as explicit:

$$
Node
$$

$$
Edge
$$

$$
Tree
$$

$$
CCC
$$

$$
CallingGraph
$$

objects.

Thus:

$$
LLM
\rightarrow
Implicit\ / Latent\ Structure
$$

while Structural Intelligence emphasizes:

$$
SI
\rightarrow
Explicit\ / Operational\ Structure
$$

This distinction is central to the larger theory.

---

# 13. LLM Reasoning Can Span Multiple Conceptual Points

An LLM reasoning trajectory may move through:

$$
Concept_A
\rightarrow
Concept_B
\rightarrow
Hypothesis_C
\rightarrow
Constraint_D
\rightarrow
Conclusion_E
$$

This is clearly more than one local Winner-Take-All decision.

The model may:

1. reinterpret the original problem;
2. identify a useful analogy;
3. construct an intermediate abstraction;
4. discover a contradiction;
5. revise the abstraction;
6. synthesize a new answer.

The resulting reasoning behavior spans multiple conceptual points.

Thus:

$$
\boxed{
LLM\ Reasoning
\ can\ be
\ Cross\text{-}Node\text{-}Like
}
$$

in functional terms, even though those "nodes" may not exist as explicit addressable runtime objects.

---

# 14. Functional Nodes and Physical Nodes Must Be Distinguished

Suppose an LLM-generated reasoning sequence appears to contain:

$$
A
\rightarrow
B
\rightarrow
C
$$

It may be useful to describe:

$$
A,B,C
$$

as conceptual reasoning nodes.

But this does not establish that the model internally contains three corresponding physical modules or explicit symbolic nodes.

Therefore:

$$
\boxed{
Functional\ Reasoning\ Structure
\neq
Literal\ Internal\ Data\ Structure
}
$$

This distinction prevents structural interpretation from becoming mechanistic overclaiming.

---

# 15. Reasoning Can Produce Novel Structural Combinations

One important behavioral indicator of reasoning is the ability to combine existing concepts into useful structures not directly provided by the prompt.

Suppose:

$$
A
$$

and:

$$
B
$$

are known concepts.

The model may infer:

$$
C=f(A,B)
$$

where \(C\) is a useful new abstraction.

Then:

$$
C
\rightarrow
D
$$

may expose a consequence not previously explicit.

This can create:

$$
A
\rightarrow
B
\rightarrow
C
\rightarrow
D
$$

and sometimes:

$$
D
\rightarrow
A'
$$

where the newly derived concept changes the interpretation of the original concept.

This produces a reasoning loop:

$$
\boxed{
A
\rightarrow
B
\rightarrow
C
\rightarrow
D
\rightarrow
A'
}
$$

Such behavior is important evidence of generative reasoning capability.

---

# 16. Novelty Does Not Automatically Mean Correctness

A model may produce:

$$
Novel
$$

without producing:

$$
Correct
$$

Therefore:

$$
Novelty
\neq
Validity
$$

Likewise:

$$
Coherence
\neq
Truth
$$

and:

$$
Plausibility
\neq
Evidence
$$

This is one of the major boundaries of generative reasoning.

A strong reasoning architecture therefore benefits from:

$$
Generation
\rightarrow
Validation
$$

rather than:

$$
Generation
\rightarrow
Automatic\ Acceptance
$$

This becomes one important point of cooperation between LLM reasoning and Structural Intelligence.

---

# 17. LLMs Are Powerful Candidate-Structure Generators

One useful interpretation is:

$$
LLM
\rightarrow
Candidate\ Structural\ Intelligence
$$

An LLM can propose:

* new classifications;
* missing relationships;
* candidate dependencies;
* new abstractions;
* possible graph edges;
* task decompositions;
* solution paths;
* hypotheses;
* program extensions.

These candidate structures can then enter:

$$
Extract
\rightarrow
Represent
\rightarrow
Validate
\rightarrow
Preserve
$$

This gives LLM reasoning an important role in structural growth without requiring every generated structure to be trusted.

---

# 18. Reasoning as Temporary Structure Formation

During one reasoning episode, an LLM may temporarily construct a useful organization of the problem.

For example:

```text id="qvm5gu"
Goal
 |
 +-- Constraint A
 |
 +-- Constraint B
 |      |
 |      +-- Dependency C
 |
 +-- Candidate D
        |
        +-- Test E
```

The model may never explicitly store this as a graph.

Yet its generated reasoning behavior can function as if such a temporary organization exists.

This motivates another concept:

$$
\boxed{
Transient\ Structural\ Intelligence
}
$$

The structure exists functionally during reasoning but may not survive as a persistent operational object.

---

# 19. Transient Structural Intelligence

Transient Structural Intelligence can include:

* temporary classifications;
* temporary plans;
* local dependency structures;
* provisional hypotheses;
* candidate causal chains;
* temporary task decomposition;
* temporary reasoning branches.

These may be highly useful.

But after the reasoning context ends:

$$
Transient\ Structure
\rightarrow
Disappear
$$

unless an external mechanism extracts and preserves them.

This creates a fundamental distinction:

$$
\boxed{
Reasoning\ Capability
\neq
Reasoning\ Infrastructure
}
$$

An LLM can possess remarkable reasoning capability while still benefiting from external persistent reasoning infrastructure.

---

# 20. Intelligence Capability and Intelligence Infrastructure

This distinction can be generalized.

A highly intelligent human can reason internally.

Civilization still creates:

* mathematics;
* diagrams;
* libraries;
* databases;
* programming languages;
* scientific papers;
* standards;
* institutions.

Why?

Because:

$$
Individual\ Cognitive\ Capability
$$

is different from:

$$
Persistent\ Collective\ Infrastructure
$$

The same principle may apply to AI.

Thus:

$$
\boxed{
LLM\ Reasoning\ Capability
\neq
Complete\ AI\ Reasoning\ Infrastructure
}
$$

Structural Intelligence can help provide that infrastructure.

---

# 21. Why Explicit Structure Still Matters

If LLMs can already reason, why introduce explicit structural systems?

Because explicit structures provide properties that latent reasoning does not automatically guarantee.

These include:

* addressability;
* persistence;
* stable naming;
* explicit dependencies;
* graph traversal;
* gap visibility;
* policy control;
* runtime certification;
* selective reuse;
* auditability.

Therefore:

$$
\boxed{
Strong\ Reasoning
\ does\ not\ eliminate
\ the\ value\ of\ explicit\ structure.
}
$$

The two solve different parts of the intelligence problem.

---

# 22. LLM Reasoning and Structural Intelligence Reasoning

The central comparison can now be stated more precisely.

| Dimension           | LLM Reasoning                           | Structural Intelligence Reasoning         |
| ------------------- | --------------------------------------- | ----------------------------------------- |
| Structure           | Latent / distributed                    | Explicit / addressable                    |
| Localization        | Soft / learned                          | Explicit tree / differential localization |
| Node computation    | Very strong                             | Pluggable and heterogeneous               |
| Association         | Extremely strong                        | Structurally constrained                  |
| Transformation      | Extremely strong                        | Operator-controlled                       |
| Trajectory          | Autoregressive / contextual             | Explicit structural trajectory            |
| Graph relationships | Often implicit                          | Explicit Calling Graph / TaskGraph        |
| Gap detection       | Emergent / context-sensitive            | First-class structural operation          |
| Gap bridging        | Generative                              | Explicit structural operation             |
| Extension           | Context / output generation             | Persistent structural growth              |
| Validation          | Often external or additional            | Can be a native structural stage          |
| Persistence         | Context, parameters, or external memory | Explicit reusable structural objects      |
| Governance          | Relatively indirect                     | Policy / CCC / runtime controlled         |
| Auditability        | Limited                                 | High by design                            |

This table is not intended to rank one system above the other.

It is a map of complementary reasoning regimes.

---

# 23. The Table Is a Map, Not a Competition

The comparison should not be read as:

$$
LLM
<
SI
$$

or:

$$
SI
<
LLM
$$

Instead:

$$
LLM
$$

is exceptionally strong in areas such as:

* broad association;
* transformation;
* abstraction;
* generative synthesis;
* flexible language-mediated reasoning.

Structural Intelligence is strong in areas such as:

* explicit localization;
* persistent structure;
* structural traversal;
* gap representation;
* governance;
* validation;
* reuse.

Thus:

$$
\boxed{
Different\ Strengths
\rightarrow
Potential\ Cooperation
}
$$

The table is therefore a map for designing hybrid reasoning systems.

---

# 24. LLM Reasoning Is Often Softly Localized

An LLM does not necessarily begin reasoning uniformly over all learned information.

The prompt and context condition the computation.

Thus:

$$
Prompt
+
Context
\rightarrow
Relevant\ Activation
$$

At a functional level, this behaves like a form of soft localization.

The model is directed toward a region of its learned capability.

However, this localization is usually not exposed as:

$$
RegionID
$$

or:

$$
TreePath
$$

or:

$$
GraphNode
$$

Therefore we can distinguish:

$$
\boxed{
Soft\ Latent\ Localization
}
$$

from:

$$
\boxed{
Explicit\ Structural\ Localization
}
$$

This distinction will become central when discussing Unfolding.

---

# 25. Prompting as an External Localization Signal

A prompt does more than request an output.

It also constrains the reasoning space.

For example:

```text id="nh8s5f"
Explain this as a graph problem.
```

or:

```text id="42v1do"
Solve only the dependency failure.
```

or:

```text id="j1fwyv"
Compare the two mechanisms at the runtime level.
```

These instructions reduce the effective reasoning region.

Thus:

$$
Prompt
\rightarrow
Reasoning\ Constraint
$$

and:

$$
Reasoning\ Constraint
\rightarrow
Soft\ Localization
$$

Prompt engineering can therefore be interpreted partly as external reasoning localization.

---

# 26. Context Is a Temporary Reasoning Structure

The context window itself can act as a temporary structural environment.

It may contain:

* definitions;
* examples;
* intermediate conclusions;
* constraints;
* previous reasoning;
* tool outputs;
* plans.

Thus:

$$
Context_t
$$

is not merely text.

Functionally, it can become:

$$
\boxed{
Temporary\ Reasoning\ Workspace
}
$$

As generation proceeds:

$$
Context_t
\rightarrow
Context_{t+1}
$$

the workspace changes.

This contributes to trajectory reasoning.

---

# 27. External Tools Expand the LLM Reasoning Loop

An LLM can also interact with external computation.

For example:

$$
LLM
\rightarrow
Tool\ Call
\rightarrow
Result
\rightarrow
LLM
$$

This changes the reasoning process from purely internal generation to:

$$
Reason
\rightarrow
Act
\rightarrow
Observe
\rightarrow
Reason
$$

A larger cycle emerges:

$$
\boxed{
Reasoning
\leftrightarrow
External\ Evidence
}
$$

This makes modern LLM systems increasingly compatible with structural reasoning architectures.

---

# 28. Tool Use Also Exposes a Structural Boundary

Tool use reveals an important fact.

The LLM does not need to perform every computation internally.

It can decide:

$$
This\ Operation
\rightarrow
External\ Tool
$$

Thus:

$$
LLM
$$

can participate in a heterogeneous reasoning system.

This supports the Structural Intelligence principle:

$$
\boxed{
Different\ Reasoning\ Needs
\rightarrow
Different\ Computational\ Mechanisms
}
$$

The LLM can be both a reasoning engine and a coordinator of other reasoning engines.

---

# 29. LLM Reasoning Can Participate Across Multiple SI Layers

It would therefore be too restrictive to place the LLM only inside:

$$
Per\text{-}Node\ Intelligence
$$

An LLM can participate in:

### Localization

Identify the likely problem region.

### Per-Node reasoning

Solve a local problem.

### Traversal

Propose relevant next relationships.

### Gap detection

Identify missing information or structure.

### Gap Bridging

Generate candidate bridges.

### Forward Extension

Propose new directions.

### Validation

Critique or compare candidates.

### Structural extraction

Convert reasoning into explicit structures.

Thus:

$$
\boxed{
LLM
\ can\ operate
\ across\ the\ Structural\ Reasoning\ Stack.
}
$$

This is an important correction to a simplistic LLM-as-node model.

---

# 30. The LLM Can Be Both Node Intelligence and Meta-Reasoning Intelligence

At one level:

$$
LLM
=
Node\ Intelligence
$$

At another:

$$
LLM
=
Reasoning\ Coordinator
$$

At another:

$$
LLM
=
Candidate\ Structure\ Generator
$$

At another:

$$
LLM
=
Structural\ Interpreter
$$

Thus the relationship is multi-role.

A hybrid reasoning architecture should not artificially restrict the LLM to one location.

---

# 31. A More Complete LLM Reasoning Model

A useful high-level abstraction is:

```text id="y55rra"
          Prompt / Goal / Context
                    |
                    v
           Context Conditioning
                    |
                    v
        Distributed Transformer
              Computation
                    |
                    v
          Candidate Continuation
                    |
                    v
          Generated New Context
                    |
                    v
        Distributed Transformer
              Computation
                    |
                    v
        Further Transformation
                    |
                    v
              ...
                    |
                    v
        Reasoning / Answer /
        Candidate Structure
```

This is not a mechanistic explanation of every internal reasoning operation.

It is a useful functional model.

---

# 32. From Parameter Space to Relevant Reasoning

A trained model contains:

$$
\theta
$$

representing a very large learned parameter system.

A particular task does not require every learned capability to be expressed.

Instead:

$$
\theta
+
Prompt
+
Context
\rightarrow
Task\text{-}Relevant\ Computation
$$

This suggests a structural interpretation:

$$
Large\ Folded\ Capability
\rightarrow
Relevant\ Local\ Expression
$$

This is the conceptual doorway to:

$$
\boxed{
Unfolding
}
$$

---

# 33. The Folding Hypothesis

Language, knowledge, patterns, relationships, and procedures encountered during training can be viewed, at a high explanatory level, as being compressed into a parameterized model.

We can write:

$$
Language
+
Knowledge
+
Patterns
+
Relations
\rightarrow
Folded\ Intelligence
$$

The word **Folding** is used here as a structural abstraction.

It does not claim that training implements a literal reversible folding operator.

Instead it emphasizes:

> Large amounts of distributed linguistic and structural regularity become encoded into a compact computational system.

This produces:

$$
\boxed{
Folded\ Intelligence\ Space
}
$$

as a useful conceptual model.

---

# 34. Folding Naturally Raises the Question of Unfolding

If useful capability is folded into the model, inference must somehow make relevant capability operational.

At a high level:

$$
Folded\ Intelligence
+
Prompt
+
Context
\rightarrow
Relevant\ Reasoning
$$

This can be interpreted as:

$$
\boxed{
Selective\ Unfolding
}
$$

The model does not unfold everything it knows.

It produces a task-conditioned local expression.

Thus:

$$
Unfolding
\neq
Full\ Reconstruction
$$

Instead:

$$
\boxed{
Unfolding
=
Goal\text{-}Conditioned\ Selective\ Expression
}
$$

This idea will be developed formally in STAR-005.

---

# 35. Why Unfolding Is a Useful Reasoning Concept

The concept explains several important properties at once.

## Selectivity

Only a small part of possible capability becomes relevant.

## Context sensitivity

Different prompts produce different reasoning trajectories.

## Generativity

The unfolded result need not be a stored sentence.

## Trajectory

Unfolding can occur progressively over multiple generation steps.

## Structural emergence

Temporary relationships and abstractions can appear during reasoning.

Thus:

$$
\boxed{
Reasoning
\ can\ be\ interpreted
\ as\ progressive\ selective\ unfolding.
}
$$

---

# 36. Unfolding Is Not Yet Explicit Structural Reasoning

A crucial distinction remains.

LLM Unfolding may produce:

$$
Reasoning\ Region_{LLM}
$$

but this region may remain:

* latent;
* distributed;
* temporary;
* difficult to address;
* difficult to certify.

Structural Intelligence Localization produces:

$$
Reasoning\ Region_{SI}
$$

that can be:

* explicit;
* named;
* addressable;
* inspectable;
* reusable.

Therefore:

$$
\boxed{
Unfolding
\neq
Localization
}
$$

Yet they may approach functionally similar reasoning regions.

This is the basis of their future handshake.

---

# 37. Functional Convergence

Suppose an LLM receives a problem and unfolds toward:

$$
R_{LLM}
$$

Structural Intelligence independently localizes the same problem toward:

$$
R_{SI}
$$

It would be too strong to claim:

$$
R_{LLM}
=
R_{SI}
$$

because their internal representations may be fundamentally different.

A more careful hypothesis is:

$$
\boxed{
R_{LLM}^{Unfold}
\approx
R_{SI}^{Localized}
}
$$

where \(\approx\) means:

> **functionally relevant convergence toward a similar local reasoning region.**

This is a major hypothesis of the larger theory.

---

# 38. LLM and SI Can Correct Each Other

If the two systems approach a common reasoning region, cooperation becomes possible.

Structural Intelligence can provide:

$$
Localization
\rightarrow
LLM
$$

telling the LLM:

> Reason here.

The LLM can provide:

$$
Unfolding
\rightarrow
Candidate\ Structure
$$

telling SI:

> This may be missing.

Then:

$$
Candidate
\rightarrow
Validation
\rightarrow
Structural\ Growth
$$

Thus:

$$
\boxed{
SI\ Localization
\rightarrow
LLM\ Unfolding
\rightarrow
Structural\ Extension
}
$$

becomes a powerful hybrid reasoning cycle.

---

# 39. Why This Is Not "LLM vs SI"

The larger theory should avoid a false competition.

The question is not:

> Which reasoning system wins?

The more productive question is:

> **Which reasoning function is best performed by which mechanism?**

LLMs provide enormous:

$$
Generative\ Reasoning\ Capacity
$$

Structural Intelligence provides:

$$
Explicit\ Structural\ Control
$$

Together:

$$
\boxed{
Latent\ Capability
+
Explicit\ Structure
}
$$

may create a stronger reasoning architecture.

---

# 40. The Boundary of LLM Reasoning

LLM reasoning remains constrained in several important ways.

These may include:

* unstable localization;
* reasoning drift;
* hallucinated relationships;
* weak persistence of temporary structure;
* limited explicit gap representation;
* limited native structural auditability;
* uncertain confidence calibration;
* dependence on context construction;
* expensive repeated reasoning.

These are not proofs that LLMs cannot reason.

They are boundaries around how reasoning is represented, controlled, validated, and preserved.

This distinction is essential.

---

# 41. Localization Gap

LLMs can perform powerful soft localization.

But the localization is often not represented as:

$$
Global
\rightarrow
Region
\rightarrow
Branch
\rightarrow
Node
$$

in an explicit, stable, inspectable structure.

This can make it difficult to determine:

* exactly where reasoning occurred;
* whether the correct region was selected;
* whether another region should have been explored;
* how the localization should be reused.

This can be called:

$$
\boxed{
Localization\ Gap
}
$$

not because localization is absent, but because it is less explicitly structuralized.

---

# 42. Structural Tracking Gap

A long reasoning process may contain many relationships.

But those relationships may not automatically become an explicit persistent graph.

Thus:

$$
Reasoning\ Trajectory
$$

does not necessarily yield:

$$
Persistent\ CallingGraph
$$

This can create a:

$$
\boxed{
Structural\ Tracking\ Gap
}
$$

The system may reason successfully without leaving behind a stable map of what was traversed and why.

---

# 43. Persistent Growth Gap

An LLM may produce an excellent new abstraction:

$$
A^*
$$

But unless an external mechanism preserves it:

$$
A^*
$$

may remain only part of the current context or output.

Thus:

$$
Reasoning
\rightarrow
Insight
$$

does not automatically imply:

$$
Insight
\rightarrow
Persistent\ Intelligence
$$

This can be called:

$$
\boxed{
Persistent\ Growth\ Gap
}
$$

It is one of the most important boundaries addressed by Structural Intelligence.

---

# 44. The Three Structural Boundaries

The three boundaries can therefore be summarized as:

$$
\boxed{
Localization\ Gap
}
$$

$$
\boxed{
Structural\ Tracking\ Gap
}
$$

$$
\boxed{
Persistent\ Growth\ Gap
}
$$

These are not claims that LLMs completely lack localization, structural relationships, or learning.

They identify areas where explicit structural infrastructure can add value.

---

# 45. Reasoning Efficiency and Unfolding Efficiency

If reasoning is partly understood as selective unfolding, then reasoning efficiency should not be measured only by:

$$
Tokens
$$

or:

$$
Compute
$$

A more structural objective is:

$$
\boxed{
Reasoning\ Efficiency
=
\frac{
Useful\ Reasoning\ Progress
}{
Inference\ Cost
}
}
$$

Later this can be refined into:

$$
\boxed{
Unfolding\ Efficiency
=
\frac{
Useful\ Structural\ Unfolding
}{
Unfolding\ Cost
}
}
$$

This leads to an important principle:

> **More unfolding is not necessarily better reasoning.**

The goal is relevant unfolding.

---

# 46. Localization Can Guide Unfolding

If Structural Intelligence can identify:

$$
Region^*
$$

then LLM reasoning can be directed toward:

$$
Unfold(Region^*)
$$

rather than relying entirely on broad latent search.

Thus:

$$
Localization
\rightarrow
Selective\ Unfolding
$$

may improve:

* efficiency;
* relevance;
* consistency;
* auditability;
* reasoning depth allocation.

This suggests:

$$
\boxed{
Good\ reasoning
\ may\ depend\ on
\ correctly\ localized\ unfolding.
}
$$

---

# 47. LLM Reasoning as a Source of Structural Growth

The direction also works in reverse.

An LLM may unfold:

$$
Candidate\ Relationship
$$

or:

$$
Candidate\ Gap
$$

or:

$$
Candidate\ Extension
$$

Structural Intelligence can then:

$$
Extract
\rightarrow
Validate
\rightarrow
Preserve
$$

Thus:

$$
LLM\ Reasoning
\rightarrow
SI\ Structural\ Growth
$$

This creates a bidirectional relationship.

---

# 48. The Emerging Handshake

The complete interaction begins to look like:

```text id="wr18jz"
       LLM Folded Intelligence
                |
                v
       Selective Unfolding
                |
                v
       Local Reasoning Region
                ^
                |
         SI Localization
                |
                ^
       Explicit Structural Space
```

Then:

```text id="mm3j8v"
Localization
     |
     v
Unfolding
     |
     v
Reasoning
     |
     v
Candidate Structure
     |
     v
Validation
     |
     v
Structural Growth
     |
     v
New Localization
     |
     +---------------->
```

This is the beginning of a hybrid reasoning architecture.

---

# 49. From LLM Reasoning to Living Reasoning

LLM reasoning alone can produce powerful transient intelligence.

Structural preservation adds:

$$
Persistence
$$

Gap-driven reasoning adds:

$$
Self\text{-}Initiated\ Problems
$$

Forward Extension adds:

$$
Proactive\ Growth
$$

Together:

$$
LLM\ Reasoning
+
Structural\ Intelligence
+
Persistent\ Growth
$$

can support:

$$
\boxed{
Living\ Reasoning
}
$$

where reasoning modifies the infrastructure of future reasoning.

---

# 50. Research Questions

### RQ-1 — What constitutes behavioral evidence of LLM reasoning?

How should reasoning be distinguished from memorization, pattern completion, and retrieval when these mechanisms can interact?

### RQ-2 — How distributed is reasoning across Transformer components?

Which reasoning functions depend on particular layers, attention patterns, MLP computations, or combinations?

### RQ-3 — How should reasoning trajectories be represented?

Can:

$$
Context_t
\rightarrow
Context_{t+1}
$$

be mapped into useful structural trajectories?

### RQ-4 — What latent structures are recoverable?

Can explicit:

* trees;
* graphs;
* dependencies;
* task structures;

be extracted reliably from LLM reasoning?

### RQ-5 — What is the relationship between soft localization and explicit localization?

Can Structural Intelligence improve the targeting of LLM reasoning?

### RQ-6 — Can Unfolding be measured?

Can we estimate:

$$
Depth
$$

$$
Breadth
$$

$$
Relevance
$$

and:

$$
Cost
$$

of reasoning unfolding?

### RQ-7 — Can an LLM learn when to unfold further?

Can the system detect:

$$
Gap
$$

$$
Conflict
$$

$$
Low\ Confidence
$$

and trigger additional reasoning?

### RQ-8 — Can transient reasoning structures be safely promoted?

What validation mechanisms are required before:

$$
Transient
\rightarrow
Persistent
$$

### RQ-9 — Can LLM and SI reasoning regions be aligned?

Can we operationalize:

$$
R_{LLM}^{Unfold}
\approx
R_{SI}^{Localized}
$$

### RQ-10 — Can latent and explicit reasoning form a closed learning loop?

Can:

$$
LLM
\rightarrow
SI
\rightarrow
LLM
$$

produce cumulative reasoning improvement?

---

# 51. Core Propositions

## Proposition 1 — LLM reasoning is not adequately described by Winner-Take-All

$$
\boxed{
LLM\ Reasoning
\neq
Single\ Local\ Selection
}
$$

---

## Proposition 2 — Autoregression supports reasoning trajectories

$$
\boxed{
Context_t
\rightarrow
Output_t
\rightarrow
Context_{t+1}
}
$$

---

## Proposition 3 — LLM reasoning is distributed

$$
\boxed{
Reasoning
\ may\ emerge\ across
\ interacting\ computations
}
$$

rather than one explicit reasoning module.

---

## Proposition 4 — LLMs can exhibit latent structural reasoning

$$
\boxed{
LLM
\rightarrow
Implicit / Latent\ Structural\ Reasoning
}
$$

---

## Proposition 5 — Functional reasoning structure does not imply literal internal symbolic structure

$$
\boxed{
Functional\ Structure
\neq
Physical\ Representation
}
$$

---

## Proposition 6 — LLMs are powerful candidate-structure generators

$$
\boxed{
LLM\ Reasoning
\rightarrow
Candidate\ Structural\ Intelligence
}
$$

---

## Proposition 7 — Reasoning capability and reasoning infrastructure are different

$$
\boxed{
Reasoning\ Capability
\neq
Reasoning\ Infrastructure
}
$$

---

## Proposition 8 — LLM reasoning can participate across the Structural Reasoning Stack

$$
\boxed{
LLM
\not\subset
Per\text{-}Node\ Only
}
$$

---

## Proposition 9 — LLM reasoning can be interpreted as selective unfolding

$$
\boxed{
Folded\ Intelligence
\rightarrow
Selective\ Unfolding
}
$$

---

## Proposition 10 — LLM and SI reasoning may converge functionally

$$
\boxed{
R_{LLM}^{Unfold}
\approx
R_{SI}^{Localized}
}
$$

---

# 52. Central Thesis

The central thesis of this paper is:

> **LLM reasoning is best treated neither as simple token lookup nor as a fully understood symbolic reasoning mechanism. It is a powerful distributed, contextual, trajectory-based computational capability operating over learned latent representations, capable of producing temporary reasoning structures, novel combinations, and candidate extensions that can interact productively with explicit Structural Intelligence.**

In compressed form:

$$
\boxed{
LLM
=
Folded\ Capability
+
Distributed\ Computation
+
Contextual\ Trajectory
+
Generative\ Reasoning
}
$$

At the structural level:

$$
\boxed{
LLM\ Reasoning
\approx
Implicit\ / Latent\ Structural\ Reasoning
}
$$

And the next theoretical step is:

$$
\boxed{
LLM\ Reasoning
\rightarrow
Selective\ Unfolding
}
$$

---

# 53. Conclusion

Large Language Models have changed the reasoning problem.

The central question is no longer adequately captured by:

> Can a statistical language model reason?

The more useful questions are:

> What kind of reasoning capability has emerged?

> How is that reasoning distributed across the computational system?

> How does context shape its trajectory?

> What temporary structures emerge during reasoning?

> Which parts can be extracted and made explicit?

> Where does latent reasoning reach its limits?

> How can explicit structural systems guide, validate, preserve, and extend it?

The evidence supports taking LLM reasoning seriously.

At the same time, theoretical discipline requires separating:

$$
Behavior
$$

from:

$$
Mechanistic\ Explanation
$$

and:

$$
Reasoning\ Capability
$$

from:

$$
Persistent\ Reasoning\ Infrastructure
$$

This produces a more productive relationship between LLMs and Structural Intelligence.

LLMs need not be reduced to Per-Node components.

Structural Intelligence need not be positioned as a replacement for LLM reasoning.

Instead:

$$
\boxed{
LLM
\rightarrow
Latent\ Generative\ Reasoning
}
$$

and:

$$
\boxed{
SI
\rightarrow
Explicit\ Operational\ Structural\ Reasoning
}
$$

can become complementary components of a larger reasoning system.

The next paper develops the concept that connects them.

If training creates a large **Folded Intelligence Space**, then reasoning can be interpreted as a process of selectively making relevant capability operational.

That process is:

$$
\boxed{
Unfolding
}
$$

---

## Next

**STAR-005 — LLM as a Folding–Unfolding Intelligence System**

The next paper develops:

$$
\boxed{
Language
+
Knowledge
+
Patterns
+
Relations
\xrightarrow{Folding}
Folded\ Intelligence
}
$$

followed by:

$$
\boxed{
Folded\ Intelligence
+
Goal
+
Context
\xrightarrow{Selective\ Unfolding}
Reasoning
}
$$

It will distinguish **Unfolding** from literal inversion, examine passive and active Unfolding, and establish the principle:

$$
\boxed{
Good\ reasoning\ is\ not\ maximal\ unfolding.
It\ is\ correctly\ localized\ unfolding.
}
$$
