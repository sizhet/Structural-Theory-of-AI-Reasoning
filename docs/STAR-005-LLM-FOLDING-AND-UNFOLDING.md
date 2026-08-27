# STAR-005 — LLM Folding and Unfolding

## From Folded Language Intelligence to Selective Reasoning Expansion

**Repository:** Structural Theory of AI Reasoning
**Series:** STAR — Structural Theory of AI Reasoning
**Document:** STAR-005
**Status:** Core Theory Paper

---

![Fig-005-Unfolding-Meets-Localization.png](./figures/Fig-005-Unfolding-Meets-Localization.png)

---

## Abstract

Large Language Models can be interpreted, at a useful structural level, as systems in which large amounts of linguistic, conceptual, relational, procedural, and task-relevant regularity are compressed into a learned parameterized representation.

This paper calls that process:

$$
\boxed{
Folding
}
$$

The term is used as a structural abstraction rather than as a claim that Transformer training implements a literal reversible folding operator.

At inference time, the model does not reconstruct everything it has learned. Instead, a prompt, goal, and context cause selected capabilities to become operational in the current reasoning trajectory.

This paper calls that process:

$$
\boxed{
Selective\ Unfolding
}
$$

Thus:

$$
Language
+
Knowledge
+
Patterns
+
Relations
\xrightarrow{Folding}
Folded\ Intelligence
$$

and:

$$
Folded\ Intelligence
+
Goal
+
Context
\xrightarrow{Selective\ Unfolding}
Reasoning
$$

The resulting reasoning can include interpretation, decomposition, hypothesis generation, abstraction, planning, relation construction, candidate extension, and multi-stage transformation.

Unfolding is not the inverse of Folding.

It is not:

$$
F^{-1}
$$

Instead, it is a goal-conditioned and context-conditioned expansion of relevant capability:

$$
U(F,G,C,B)
\rightarrow
R
$$

where:

* \(F\) is Folded Intelligence;
* \(G\) is the current goal;
* \(C\) is context;
* \(B\) is reasoning budget;
* \(R\) is the resulting reasoning trajectory or reasoning structure.

This interpretation leads to an important principle:

> **Good reasoning is not maximal unfolding. It is correctly localized unfolding.**

That principle creates the theoretical bridge between LLM reasoning and Structural Intelligence.

LLMs provide powerful latent capability that can be unfolded.

Structural Intelligence provides explicit mechanisms for deciding where reasoning should occur, which structural gap matters, and how newly unfolded reasoning should be validated and preserved.

The resulting handshake is:

$$
\boxed{
LLM\ Unfolding
\leftrightarrow
SI\ Localization
}
$$

---

# 1. Why Introduce Folding?

A modern LLM is exposed during training to enormous amounts of:

* natural language;
* code;
* concepts;
* factual relationships;
* argument patterns;
* procedures;
* classifications;
* causal descriptions;
* mathematical structures;
* task patterns;
* social conventions;
* domain-specific regularities.

The trained system does not store all of these as a conventional database of explicit sentences.

Instead, training produces a distributed parameterized system:

$$
\theta
$$

capable of reconstructing, transforming, combining, and generating task-relevant behavior.

At a structural level, this can be interpreted as:

$$
\boxed{
Many\ Observed\ Structures
\rightarrow
Compressed\ Learned\ Capability
}
$$

This paper calls that transformation:

$$
\boxed{
Folding
}
$$

---

# 2. Folding Is a Structural Abstraction

The term Folding should be used carefully.

It does **not** imply:

$$
Training
=
Literal\ Geometric\ Folding
$$

It does not imply that:

$$
Unfolding
=
Exact\ Mathematical\ Inverse
$$

of training.

Instead, Folding expresses the idea that a very large space of observable patterns becomes represented within a more compact reusable computational system.

Thus:

$$
\boxed{
Folding
=
Structural\ Compression\ into\ Reusable\ Capability
}
$$

The model does not preserve every training example as an independently addressable explicit object.

It develops a distributed capability to respond to future conditions.

---

# 3. What Is Folded?

The folded content is not only language form.

It can include regularities associated with:

* syntax;
* semantics;
* concepts;
* categories;
* relationships;
* procedures;
* explanations;
* argument forms;
* programming structures;
* task decomposition;
* analogy;
* causal descriptions;
* mathematical patterns.

Therefore the useful abstraction is broader than:

$$
Language\ Folding
$$

It is closer to:

$$
\boxed{
Language\text{-}Mediated\ Intelligence\ Folding
}
$$

Natural language is the dominant interface and training substrate, but the folded capability can support much more than sentence completion.

---

# 4. From Language Folding to Intelligence Folding

A simplified progression can be written as:

$$
Language
\rightarrow
Patterns
\rightarrow
Relations
\rightarrow
Abstractions
\rightarrow
Learned\ Capability
$$

Training repeatedly exposes the model to structured regularities.

The resulting system becomes able to respond to new combinations of:

$$
Goal
+
Context
+
Prompt
$$

This suggests:

$$
\boxed{
LLM
\approx
Folded\ Language\text{-}Intelligence\ System
}
$$

as a high-level explanatory model.

The word "folded" emphasizes that potentially useful capability is latent until a specific inference context activates it.

---

# 5. Why Folding Naturally Raises the Question of Unfolding

If capability is folded into the model, then inference must make some part of that capability operational.

Suppose:

$$
F
$$

represents the folded capability of the model.

Given:

$$
Goal=G
$$

and:

$$
Context=C
$$

the system produces:

$$
R
$$

where \(R\) may be:

* an answer;
* a reasoning trajectory;
* a plan;
* a hypothesis;
* a classification;
* a candidate structure.

At the structural level:

$$
F
+
G
+
C
\rightarrow
R
$$

This paper interprets this as:

$$
\boxed{
Selective\ Unfolding
}
$$

---

# 6. Unfolding Is Selective

The model does not expose everything it has learned.

For a given task, only a limited portion of its available capability becomes relevant.

Thus:

$$
Unfold(F)
\neq
Everything(F)
$$

Instead:

$$
\boxed{
Unfold(F,G,C)
\rightarrow
Relevant(F|G,C)
}
$$

The current goal and context constrain what becomes operational.

This is why the same model can respond differently to:

* a legal question;
* a coding question;
* a biological question;
* a planning task;
* a mathematical problem.

The folded capability is broad.

The unfolding is local.

---

# 7. Unfolding Is Not Retrieval

Unfolding should not be reduced to:

$$
Prompt
\rightarrow
Retrieve\ Stored\ Answer
$$

An LLM may instead:

* combine concepts;
* generate a new abstraction;
* decompose a task;
* synthesize a plan;
* construct a new analogy;
* propose a new relation.

Thus:

$$
\boxed{
Unfolding
\neq
Simple\ Retrieval
}
$$

A more useful interpretation is:

$$
\boxed{
Unfolding
=
Context\text{-}Conditioned\ Generative\ Activation
}
$$

of learned capability.

---

# 8. Unfolding Is Not Full Reconstruction

Likewise, Unfolding is not:

$$
Compressed
\rightarrow
Original\ Training\ Data
$$

It is:

$$
Compressed\ Capability
\rightarrow
Task\text{-}Relevant\ Expression
$$

Thus:

$$
\boxed{
Unfolding
\neq
Decompression\ of\ the\ full\ training\ corpus
}
$$

The result is functional rather than reconstructive.

---

# 9. Unfolding Is Not the Inverse of Folding

Let:

$$
Folding = \mathcal{F}
$$

and:

$$
Unfolding = \mathcal{U}
$$

It would be misleading to assert:

$$
\mathcal{U}
=
\mathcal{F}^{-1}
$$

because:

* the training process is not necessarily reversible;
* the model does not reconstruct the original data;
* one folded capability can support many possible outputs;
* unfolding is conditioned by the current goal and context.

Therefore:

$$
\boxed{
\mathcal{U}
\neq
\mathcal{F}^{-1}
}
$$

Folding and Unfolding are **functional duals**, not mathematical inverses.

---

# 10. Folding–Unfolding Duality

The useful relationship is:

$$
\boxed{
Folding
\leftrightarrow
Unfolding
}
$$

where:

### Folding asks:

> What reusable capability can be compressed into the model?

### Unfolding asks:

> What part of that capability should become operational now?

This creates a functional duality:

$$
Many
\rightarrow
Compact
$$

versus:

$$
Compact
+
Goal
+
Context
\rightarrow
Relevant\ Expansion
$$

---

# 11. A Minimal Unfolding Equation

A useful abstraction is:

$$
\boxed{
U(F,G,C,B)
\rightarrow
R
}
$$

where:

* \(F\) = Folded Intelligence;
* \(G\) = Goal;
* \(C\) = Context;
* \(B\) = Reasoning Budget;
* \(R\) = Reasoning result or reasoning trajectory.

The inclusion of:

$$
B
$$

is important.

Reasoning is computationally bounded.

The system cannot unfold indefinitely.

Thus Unfolding is constrained by:

$$
Relevance
+
Cost
+
Depth
+
Time
$$

---

# 12. Passive Unfolding

Current LLM use already contains a simple form of Unfolding.

A prompt is presented:

$$
P
$$

The model responds:

$$
F
+
P
\rightarrow
R
$$

The model does not explicitly decide:

> I will now execute an Unfolding operation.

Yet relevant capability becomes expressed.

This can be called:

$$
\boxed{
Passive\ or\ Emergent\ Unfolding
}
$$

It is driven mainly by external prompting and autoregressive continuation.

---

# 13. Prompting as Unfolding Control

A prompt can strongly influence what gets unfolded.

Compare:

```text id="j4oegn"
Explain this problem.
```

with:

```text id="4k8s2c"
Analyze only the missing dependency.
```

and:

```text id="8rk6cb"
Decompose the problem into three competing causal models.
```

Each prompt changes:

$$
U(F,G,C)
$$

by constraining the reasoning region.

Thus prompt design can be interpreted as:

$$
\boxed{
External\ Unfolding\ Control
}
$$

This connects prompting with reasoning localization.

---

# 14. Context as an Unfolding Boundary

The context window provides temporary reasoning state.

It can contain:

* definitions;
* task constraints;
* intermediate results;
* evidence;
* previous outputs;
* tool results;
* structural maps.

Thus:

$$
C_t
$$

defines part of the current Unfolding boundary.

At the next step:

$$
C_{t+1}
=
C_t
+
Output_t
$$

Therefore Unfolding changes its own subsequent conditions.

This creates:

$$
\boxed{
Progressive\ Unfolding
}
$$

---

# 15. Progressive Unfolding

A reasoning trajectory can be represented as:

$$
U_1
\rightarrow
U_2
\rightarrow
U_3
\rightarrow
...
\rightarrow
U_n
$$

where each step makes additional reasoning capability explicit.

For example:

$$
Problem
$$

may first unfold into:

$$
Classification
$$

then:

$$
Classification
\rightarrow
Relevant\ Relation
$$

then:

$$
Relation
\rightarrow
Hypothesis
$$

then:

$$
Hypothesis
\rightarrow
Test
$$

then:

$$
Test
\rightarrow
Conclusion
$$

Thus reasoning can be seen as:

$$
\boxed{
Sequential\ Structural\ Unfolding
}
$$

---

# 16. Unfolding Can Branch

Unfolding need not be linear.

A problem may produce:

$$
Candidate_A
$$

$$
Candidate_B
$$

$$
Candidate_C
$$

Then:

$$
Candidate_B
$$

may require further expansion:

$$
B_1,
B_2,
B_3
$$

This suggests:

```text id="3fnb2a"
              Goal
               |
       +-------+-------+
       |       |       |
      U1      U2      U3
               |
          +----+----+
          |         |
         U21       U22
                    |
                    v
                   U221
```

This is an:

$$
\boxed{
Unfolding\ Tree
}
$$

as a functional abstraction.

---

# 17. Unfolding Can Be Multi-Axial

A reasoning problem may need expansion along different axes.

Examples:

* causal;
* temporal;
* structural;
* logical;
* procedural;
* social;
* computational;
* risk-related.

Thus:

$$
U
$$

can be decomposed into:

$$
U_{causal}
$$

$$
U_{temporal}
$$

$$
U_{structural}
$$

$$
U_{procedural}
$$

This suggests that future reasoning systems may explicitly choose:

> **Along which axis should intelligence be unfolded?**

---

# 18. Unfolding Depth

Not every task requires the same depth.

A simple question may require:

$$
Depth=1
$$

A complex scientific problem may require:

$$
Depth=n
$$

Thus:

$$
U(F,G,C,B,D)
\rightarrow
R
$$

where:

$$
D
=
Unfolding\ Depth
$$

This introduces an important optimization problem:

$$
\boxed{
How\ much\ unfolding\ is\ enough?
}
$$

---

# 19. More Unfolding Is Not Always Better

A naive assumption is:

$$
More\ Reasoning
\rightarrow
Better\ Answer
$$

But additional reasoning can also create:

* drift;
* unnecessary branches;
* contradiction;
* speculative complexity;
* increased cost;
* longer error chains.

Therefore:

$$
\boxed{
More\ Unfolding
\neq
Better\ Reasoning
}
$$

The key problem is relevance.

---

# 20. Unfolding Efficiency

This motivates:

$$
\boxed{
Unfolding\ Efficiency
=
\frac{
Useful\ Reasoning\ Expansion
}{
Inference\ Cost
}
}
$$

A more structural form is:

$$
\boxed{
UE
=
\frac{
Useful\ Structural\ Progress
}{
Unfolding\ Cost
}
}
$$

The objective is not:

$$
Maximize(Unfolding)
$$

but:

$$
\boxed{
Maximize(Relevant\ Unfolding)
}
$$

---

# 21. The Need for Localization

Unfolding immediately creates another question:

> **Where should the model unfold?**

A large model may contain capability relevant to many regions.

Without guidance:

$$
F
\rightarrow
Large\ Candidate\ Space
$$

A localization mechanism can reduce this:

$$
F
\rightarrow
Localized\ Region
\rightarrow
Selective\ Unfolding
$$

Thus:

$$
\boxed{
Localization
\ can\ control
\ Unfolding
}
$$

This is the bridge to Structural Intelligence.

---

# 22. Soft Localization Inside LLM Reasoning

LLMs already perform a form of soft localization.

Prompt and context influence:

$$
Task\text{-}Relevant\ Computation
$$

Thus:

$$
Prompt
+
Context
\rightarrow
Soft\ Reasoning\ Region
$$

However, this region is typically not exposed as an explicit:

$$
Tree\ Path
$$

$$
Node
$$

$$
Graph\ Region
$$

or:

$$
CCC
$$

Thus:

$$
\boxed{
LLM
=
Soft\ Localization
+
Selective\ Unfolding
}
$$

at a high structural level.

---

# 23. Explicit Localization in Structural Intelligence

Structural Intelligence can instead use explicit structures:

$$
Differential\ Tree
$$

$$
Classification\ Tree
$$

$$
CallingGraph
$$

$$
TaskGraph
$$

$$
CCC
$$

to perform:

$$
Global\ Space
\rightarrow
Relevant\ Region
\rightarrow
Node
$$

This gives:

$$
\boxed{
Explicit\ Localization
}
$$

Thus LLM and SI approach reasoning from different directions.

---

# 24. The Two Directions

LLM:

$$
Folded\ Intelligence
\rightarrow
Unfold
\rightarrow
Local\ Reasoning
$$

SI:

$$
Explicit\ Structural\ Space
\rightarrow
Localize
\rightarrow
Local\ Reasoning
$$

This gives:

$$
\boxed{
Unfolding
\downarrow
}
$$

and:

$$
\boxed{
Localization
\uparrow
}
$$

toward a common reasoning region.

---

# 25. Functional Convergence

Let:

$$
R_{LLM}^{U}
$$

be the reasoning region reached through LLM Unfolding.

Let:

$$
R_{SI}^{L}
$$

be the reasoning region reached through SI Localization.

We should not assert:

$$
R_{LLM}^{U}
=
R_{SI}^{L}
$$

because their internal representations may differ fundamentally.

A more useful hypothesis is:

$$
\boxed{
R_{LLM}^{U}
\approx
R_{SI}^{L}
}
$$

where:

$$
\approx
$$

means functionally relevant convergence.

This is the **reasoning handshake hypothesis**.

---

# 26. The Reasoning Handshake

A simple representation is:

```text id="q6l8ue"
         LLM Folded Intelligence
                  |
                  v
        Selective Unfolding
                  |
                  v
        +------------------+
        |  Local Reasoning |
        |      Region      |
        +------------------+
                  ^
                  |
            Localization
                  |
                  ^
         SI Structural Space
```

The LLM arrives from a latent folded space.

SI arrives from an explicit structural space.

They meet around the same task-relevant reasoning region.

---

# 27. Good Reasoning Is Correctly Localized Unfolding

This leads to one of the central propositions of this repository:

$$
\boxed{
Good\ Reasoning
\neq
Maximal\ Unfolding
}
$$

Instead:

$$
\boxed{
Good\ Reasoning
=
Correctly\ Localized\ Unfolding
}
$$

This principle combines the strengths of both systems.

SI contributes:

$$
Where
$$

LLM contributes:

$$
What\ can\ be\ unfolded\ there
$$

---

# 28. Localization Before Unfolding

A hybrid system can operate as:

$$
Goal
\rightarrow
Localization
\rightarrow
Reasoning\ Region
\rightarrow
LLM\ Unfolding
$$

This may reduce:

* irrelevant reasoning;
* context drift;
* compute waste;
* unrelated associations;
* uncontrolled branch growth.

Thus:

$$
\boxed{
Better\ Localization
\rightarrow
Less\ but\ Better\ Unfolding
}
$$

This is an important inversion of the idea that intelligence always requires more computation.

---

# 29. Unfolding Before Structuralization

The reverse direction is equally important.

An LLM may unfold:

$$
Candidate\ Concept
$$

$$
Candidate\ Relation
$$

$$
Candidate\ Gap
$$

$$
Candidate\ Extension
$$

These can then be converted into explicit structures.

Thus:

$$
LLM\ Unfolding
\rightarrow
Structural\ Extraction
$$

followed by:

$$
Structural\ Extraction
\rightarrow
Validation
\rightarrow
Persistence
$$

This converts latent reasoning into reusable infrastructure.

---

# 30. Unfolding and Structural Growth

The full process becomes:

$$
F
\rightarrow
L
\rightarrow
U
\rightarrow
R
\rightarrow
E
\rightarrow
V
\rightarrow
S_{t+1}
$$

where:

* \(F\) = Folded Intelligence;
* \(L\) = Localization;
* \(U\) = Unfolding;
* \(R\) = Reasoning;
* \(E\) = Structural Extraction;
* \(V\) = Validation;
* \(S_{t+1}\) = Updated Structure.

Thus:

$$
\boxed{
Unfolding
\rightarrow
Reasoning
\rightarrow
Structural\ Growth
}
$$

---

# 31. Active Unfolding

Passive Unfolding is externally triggered.

A more advanced system may explicitly decide:

> **I need more reasoning here.**

This can be called:

$$
\boxed{
Active\ Unfolding
}
$$

A trigger may occur when:

$$
Confidence
<
Threshold
$$

or:

$$
Gap
=
Detected
$$

or:

$$
Conflict
=
True
$$

or:

$$
Evidence
=
Insufficient
$$

Then:

$$
Trigger
\rightarrow
Additional\ Unfolding
$$

---

# 32. A Minimal Active-Unfolding Rule

For example:

```text id="vx0xay"
IF structural gap detected
AND current evidence is insufficient
AND expected reasoning value exceeds cost
THEN
    unfold the relevant reasoning region
```

In CCC form:

$$
Condition
+
Context
\rightarrow
Unfolding\ Computation
$$

Thus:

$$
\boxed{
CCC
\ can\ govern
\ LLM\ Unfolding
}
$$

This directly connects a core Structural Intelligence operator to LLM reasoning control.

---

# 33. Unfolding as a Runtime Operation

If Active Unfolding becomes explicit, then:

$$
Unfold()
$$

may become a first-class runtime operation.

A future interface might conceptually support:

$$
Unfold(
Region,
Axis,
Depth,
Budget,
Goal
)
$$

This would transform reasoning from:

$$
Generate\ More
$$

into:

$$
\boxed{
Unfold\ the\ Right\ Capability
}
$$

This is a major architectural shift.

---

# 34. Unfolding Control Variables

A controlled Unfolding system may need to determine:

### Where?

$$
Region
$$

### Along which axis?

$$
Axis
$$

### How deeply?

$$
Depth
$$

### How broadly?

$$
Breadth
$$

### Under what cost?

$$
Budget
$$

### Until what stopping condition?

$$
Stop
$$

Thus:

$$
\boxed{
Unfolding
=
Controlled\ Reasoning\ Expansion
}
$$

---

# 35. Stopping Is Part of Reasoning

An Unfolding system also needs to know when to stop.

Possible stopping conditions include:

* sufficient confidence;
* gap resolved;
* evidence threshold reached;
* structural consistency achieved;
* compute budget exhausted;
* no useful new branch found.

Thus:

$$
Continue?
\rightarrow
\{Yes,No\}
$$

is itself part of reasoning control.

This suggests:

$$
\boxed{
Stopping
\ is\ a\ reasoning\ operation.
}
$$

---

# 36. Unfolding Tree Search

If reasoning branches, Active Unfolding may resemble controlled search.

Let:

$$
U_i
$$

be a candidate reasoning branch.

The system may compute:

$$
Score(U_i)
$$

based on:

* expected value;
* structural relevance;
* uncertainty;
* cost;
* gap potential.

Then:

$$
Select(U^*)
$$

for deeper Unfolding.

This produces:

$$
\boxed{
Selective\ Unfolding\ Search
}
$$

rather than uniform expansion.

---

# 37. Unfolding and Per-Node Intelligence

Unfolding should not be confused with Per-Node Intelligence.

A Per-Node operation may solve:

$$
Local\ Problem
$$

Unfolding can span:

$$
Multiple\ Conceptual\ Regions
$$

and construct a trajectory.

Thus:

$$
\boxed{
Unfolding
\ can\ be
\ Cross\text{-}Node
}
$$

functionally.

An LLM may be invoked at one node but generate reasoning that spans multiple conceptual steps.

---

# 38. Unfolding and TaskGraph Reasoning

A task may begin as:

$$
T_0
$$

LLM Unfolding may produce:

$$
T_1,T_2,T_3
$$

Then further Unfolding may reveal:

$$
T_{2.1}
$$

The resulting TaskGraph is:

$$
TG_{t+1}
$$

Thus:

$$
\boxed{
LLM\ Unfolding
\rightarrow
TaskGraph\ Growth
}
$$

when the newly generated task structure is extracted and preserved.

---

# 39. Unfolding and Gap Bridging

A structural system may detect:

$$
Gap_G
$$

Localization identifies:

$$
Region_G
$$

Then:

$$
LLM
\rightarrow
Unfold(Region_G)
$$

to produce:

$$
Bridge_1,\ldots,Bridge_n
$$

Structural Intelligence can then validate the candidates.

Thus:

$$
\boxed{
Gap
\rightarrow
Localization
\rightarrow
Unfolding
\rightarrow
Bridge
}
$$

This is a particularly natural division of labor.

---

# 40. Unfolding and Forward Extension

Unfolding can also be used proactively.

Suppose no explicit gap exists.

The system asks:

> What useful structure could come next?

Then:

$$
Localized\ Opportunity
\rightarrow
Unfold
\rightarrow
Candidate\ Extension
$$

This creates:

$$
\boxed{
Opportunity\text{-}Driven\ Unfolding
}
$$

and can support Forward Extension.

---

# 41. From Prompt-Driven to Structure-Driven Unfolding

Current LLM use is often:

$$
Human\ Prompt
\rightarrow
Unfolding
$$

A more advanced structural system may use:

$$
Gap
\rightarrow
Unfolding
$$

or:

$$
TaskGraph
\rightarrow
Unfolding
$$

or:

$$
CCC
\rightarrow
Unfolding
$$

or:

$$
Policy
\rightarrow
Unfolding
$$

Thus the reasoning trigger changes from:

$$
External\ Language\ Prompt
$$

to:

$$
\boxed{
Internal\ Structural\ Trigger
}
$$

This is a major step toward autonomous reasoning.

---

# 42. The Unfolding Dual Transformer Hypothesis

If Unfolding becomes an explicit computational objective, future architectures may specialize it.

One possibility is a functional duality:

$$
Transformer_F
$$

for large-scale Folding and representation learning,

and:

$$
Transformer_U
$$

for goal-conditioned reasoning Unfolding.

This gives:

$$
\boxed{
Transformer_F
\leftrightarrow
Transformer_U
}
$$

But this should currently be treated as an architecture hypothesis, not an established requirement.

---

# 43. Unfolding Transformer Is Not an Inverse Transformer

A hypothetical:

$$
Transformer_U
$$

would not attempt:

$$
Recover\ Training\ Data
$$

Instead it would optimize:

$$
Folded\ Intelligence
+
Goal
+
Context
\rightarrow
Reasoning\ Structure
$$

Its objective may emphasize:

* gap resolution;
* structural completion;
* branch expansion;
* task decomposition;
* dependency recovery;
* structural consistency;
* reasoning value per unit compute.

Thus:

$$
\boxed{
Transformer_U
\neq
Transformer_F^{-1}
}
$$

It is a specialized reasoning engine.

---

# 44. Same-Model Dual Mode

A separate Unfolding model may not be necessary.

One possibility is:

$$
Single\ Model
$$

with multiple runtime modes:

$$
Generation\ Mode
$$

$$
Reasoning\ Mode
$$

$$
Unfolding\ Mode
$$

The model may dynamically change:

* compute allocation;
* search depth;
* reasoning style;
* tool usage;
* branch exploration.

This can be called:

$$
\boxed{
Same\text{-}Model\ Dual\ Mode
}
$$

---

# 45. Dual-Model Architecture

Another possibility is:

```text id="iujd4x"
          Folded Core Model
                 |
                 v
        Unfolding / Reasoner
                 |
                 v
        Reasoning Structure
```

The first model provides broad intelligence capital.

The second specializes in reasoning extraction and expansion.

This creates:

$$
\boxed{
Dual\text{-}Model\ Reasoning
}
$$

---

# 46. Structural Hybrid Architecture

A third possibility is broader:

$$
LLM
+
SI\ Localizer
+
Rules
+
Search
+
Solver
+
Tools
+
Specialized\ Unfolders
$$

This avoids assuming:

$$
Everything
=
Transformer
$$

Instead:

$$
\boxed{
Unfolding
=
Heterogeneous\ Structural\ Computation
}
$$

This may be the most general architecture.

---

# 47. One Core, Many Unfolders

A future system may use:

$$
F
+
\{U_1,U_2,...,U_n\}
$$

For example:

$$
U_{logic}
$$

$$
U_{coding}
$$

$$
U_{planning}
$$

$$
U_{science}
$$

$$
U_{policy}
$$

A structural router selects the appropriate Unfolder.

Thus:

```text id="2sz7gj"
             Folded Core
                 |
                 v
          SI Localization
                 |
                 v
        Structural Router
       /       |        \
      v        v         v
   U-Logic   U-Code   U-Planning
       \       |        /
        \      |       /
           Reasoning
```

This is a natural specialization path.

---

# 48. The Three-Way Division of Labor

The architecture can be summarized through three questions.

### Folded Core

> **What intelligence is available?**

### Structural Intelligence

> **Where should reasoning occur?**

### Unfolding Engine

> **How should that intelligence be expanded here?**

Thus:

$$
\boxed{
What
+
Where
+
How
}
$$

becomes a clean reasoning architecture.

---

# 49. Folded Intelligence Capital

The broad capability stored in a trained model can be interpreted as:

$$
\boxed{
Folded\ Intelligence\ Capital
}
$$

This capital includes reusable latent capability accumulated through training.

It can be deployed repeatedly through selective inference.

The key problem is not whether the capital exists.

It is:

> **How should it be deployed efficiently and reliably?**

That is the Unfolding problem.

---

# 50. Explicit Structural Capital

Structural Intelligence contributes another form of capital:

$$
\boxed{
Explicit\ Structural\ Capital
}
$$

including:

* trees;
* graphs;
* CCCs;
* TaskGraphs;
* policies;
* Runtime Invariants;
* validated dependencies;
* reusable structural objects.

Thus future reasoning can combine:

$$
Folded\ Intelligence\ Capital
$$

with:

$$
Explicit\ Structural\ Capital
$$

This provides a deeper explanation of LLM–SI complementarity.

---

# 51. Transient and Persistent Intelligence

LLM Unfolding may create:

$$
Transient\ Reasoning\ Structure
$$

Structural extraction can convert selected parts into:

$$
Persistent\ Reasoning\ Structure
$$

Thus:

$$
\boxed{
Folded
\rightarrow
Unfolded
\rightarrow
Structuralized
\rightarrow
Persistent
}
$$

This creates a complete knowledge lifecycle.

---

# 52. Refolding

Persistent structural growth may eventually become too large or fragmented.

New structures may need to be:

* abstracted;
* merged;
* compressed;
* generalized.

Thus:

$$
Structural\ Growth
\rightarrow
Abstraction
\rightarrow
Refolding
$$

This introduces:

$$
\boxed{
Refolding
}
$$

as another possible phase.

---

# 53. The Full Folding–Unfolding Cycle

The larger cycle becomes:

$$
\boxed{
Folding
\rightarrow
Localization
\rightarrow
Selective\ Unfolding
\rightarrow
Reasoning
\rightarrow
Structuralization
\rightarrow
Validation
\rightarrow
Growth
\rightarrow
Refolding
}
$$

This is not a claim about one current implementation.

It is a structural model for future reasoning systems.

---

# 54. Folding and Structural Growth Are Complementary

Folding reduces complexity.

Structural growth increases explicit capability.

At first this appears contradictory.

But mature intelligence may require both.

$$
Growth
\rightarrow
More\ Structure
$$

while:

$$
Folding
\rightarrow
More\ Compression
$$

Thus intelligent systems may alternate between:

$$
\boxed{
Expansion
\leftrightarrow
Compression
}
$$

This is similar to many other knowledge systems.

New discoveries expand structure.

New abstractions compress it.

---

# 55. Reasoning as Controlled Expansion

This suggests a broader interpretation:

$$
\boxed{
Reasoning
=
Controlled\ Expansion\ of\ Relevant\ Intelligence
}
$$

The expansion is controlled by:

* goals;
* context;
* localization;
* budget;
* policies;
* validation.

This definition connects LLM reasoning with Structural Intelligence without requiring them to use the same internal representation.

---

# 56. Why the LLM–SI Handshake Matters

The handshake solves complementary problems.

Without SI guidance, Unfolding may suffer from:

* drift;
* over-expansion;
* poor targeting;
* repeated rediscovery.

Without LLM capability, explicit structural systems may suffer from:

* limited generativity;
* rigid local rules;
* expensive manual construction;
* poor abstraction flexibility.

Together:

$$
\boxed{
Localization
+
Unfolding
}
$$

can combine structure with generativity.

---

# 57. From "Think More" to "Unfold Better"

A major future shift may be from:

$$
Think\ Longer
$$

to:

$$
\boxed{
Unfold\ Better
}
$$

That means:

* better region selection;
* better axis selection;
* better depth control;
* better stopping;
* better validation;
* better structural extraction.

This is qualitatively different from simply increasing token count.

---

# 58. Unfolding and Test-Time Compute

Additional inference compute can support deeper reasoning.

From the present framework:

$$
More\ Test\text{-}Time\ Compute
$$

is useful only if it produces:

$$
More\ Useful\ Unfolding
$$

Thus the important objective is not:

$$
Compute
$$

but:

$$
\boxed{
Compute
\rightarrow
Useful\ Structural\ Progress
}
$$

This reframes reasoning-time scaling structurally.

---

# 59. Unfolding and Reasoning Budget Allocation

A reasoning controller can allocate more compute to regions with:

* high uncertainty;
* high structural importance;
* unresolved gaps;
* high expected value.

Thus:

$$
Budget_i
=
f(
Gap_i,
Risk_i,
Value_i,
Confidence_i
)
$$

This gives:

$$
\boxed{
Adaptive\ Unfolding
}
$$

as an important future direction.

---

# 60. Unfolding Should Be Governed

A powerful Unfolding system requires boundaries.

Policies may control:

* allowed reasoning regions;
* maximum depth;
* tool use;
* sensitive actions;
* structural promotion;
* human escalation.

Thus:

$$
Policy
\rightarrow
Unfolding\ Constraints
$$

and:

$$
\boxed{
Unfolding
\ should\ be
\ Governable
}
$$

---

# 61. Unfolding Should Be Auditable

If Unfolding becomes explicit, a system can report:

* why additional reasoning was triggered;
* which region was selected;
* which axis was expanded;
* which candidates were generated;
* why a branch was stopped;
* which structure was promoted.

This yields:

$$
\boxed{
Auditable\ Unfolding
}
$$

which is more informative than a final answer alone.

---

# 62. Unfolding Should Be Reusable

A successful Unfolding trajectory may reveal:

$$
Reusable\ Pattern
$$

If extracted and preserved:

$$
Trajectory
\rightarrow
Structural\ Object
$$

future systems can avoid rediscovering the same reasoning path.

Thus:

$$
\boxed{
Unfolding
\rightarrow
Reasoning\ Capital
}
$$

when its results become persistent.

---

# 63. Research Questions

### RQ-1 — How should Folding be formalized?

Can Folded Intelligence be measured beyond model size or parameter count?

### RQ-2 — How should Unfolding be identified experimentally?

What observable behaviors distinguish selective Unfolding from retrieval or direct continuation?

### RQ-3 — Can Unfolding depth be measured?

Can we estimate:

$$
Depth(U)
$$

for a reasoning episode?

### RQ-4 — Can Unfolding breadth be measured?

Can we measure how many candidate regions or branches are explored?

### RQ-5 — Can Unfolding efficiency be measured?

Can we operationalize:

$$
UE
=
\frac{
Useful\ Structural\ Progress
}{
Inference\ Cost
}
$$

### RQ-6 — How should Localization guide Unfolding?

Can explicit structural localization consistently reduce reasoning cost or improve reliability?

### RQ-7 — Can Active Unfolding be learned?

Can models learn when to continue reasoning, stop, branch, or call tools?

### RQ-8 — Should specialized Unfolding engines exist?

When is:

$$
One\ Model
$$

better than:

$$
Core + Specialized\ Unfolders
$$

### RQ-9 — Can CCC become an Unfolding control mechanism?

Can:

$$
Condition
+
Context
\rightarrow
Unfold
$$

be implemented systematically?

### RQ-10 — How should Unfolded structures be validated and preserved?

What promotion rules should govern:

$$
Transient
\rightarrow
Persistent
$$

### RQ-11 — Can Folding and Structural Growth form a stable cycle?

How can systems avoid uncontrolled accumulation?

### RQ-12 — Can Refolding compress accumulated structural intelligence?

How should newly validated structures be generalized and compressed?

---

# 64. Core Propositions

## Proposition 1 — LLM training can be usefully interpreted as Folding

$$
\boxed{
Many\ Linguistic/Structural\ Regularities
\rightarrow
Folded\ Intelligence
}
$$

---

## Proposition 2 — Inference can be interpreted as Selective Unfolding

$$
\boxed{
Folded\ Intelligence
+
Goal
+
Context
\rightarrow
Relevant\ Reasoning
}
$$

---

## Proposition 3 — Unfolding is not the inverse of Folding

$$
\boxed{
U
\neq
F^{-1}
}
$$

---

## Proposition 4 — Unfolding is goal-conditioned

$$
\boxed{
U
=
U(F,G,C,B)
}
$$

---

## Proposition 5 — Unfolding can be progressive and branching

$$
\boxed{
U_1
\rightarrow
U_2
\rightarrow
...
}
$$

and:

$$
\boxed{
U
\rightarrow
\{U_1,U_2,...\}
}
$$

---

## Proposition 6 — More Unfolding is not necessarily better

$$
\boxed{
Maximal\ Unfolding
\neq
Optimal\ Reasoning
}
$$

---

## Proposition 7 — Localization can guide Unfolding

$$
\boxed{
Localization
\rightarrow
Relevant\ Unfolding
}
$$

---

## Proposition 8 — LLM Unfolding and SI Localization can converge functionally

$$
\boxed{
R_{LLM}^{Unfold}
\approx
R_{SI}^{Localized}
}
$$

---

## Proposition 9 — Active Unfolding can become a runtime operation

$$
\boxed{
Gap
+
Context
\rightarrow
Unfold
}
$$

---

## Proposition 10 — Unfolding can produce persistent structural growth

$$
\boxed{
Unfolding
\rightarrow
Reasoning
\rightarrow
Structuralization
\rightarrow
Growth
}
$$

---

# 65. Central Thesis

The central thesis of this paper is:

> **An LLM can be interpreted as a Folded Language-Intelligence system whose learned capability becomes selectively operational through goal-conditioned and context-conditioned Unfolding. Reasoning quality therefore depends not on unfolding as much capability as possible, but on unfolding the right capability in the right region at the right depth and cost.**

In compact form:

$$
\boxed{
LLM
=
Folded\ Intelligence
}
$$

$$
\boxed{
Reasoning
=
Selective\ Unfolding
}
$$

and:

$$
\boxed{
Good\ Reasoning
=
Correctly\ Localized\ Unfolding
}
$$

---

# 66. Canonical Folding–Unfolding Equation

The core equation of this paper is:

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
\xrightarrow{
Goal + Context + Localization
}
Selective\ Unfolding
\xrightarrow{}
Reasoning
}
$$

The extended lifecycle is:

$$
\boxed{
Folding
\rightarrow
Localization
\rightarrow
Selective\ Unfolding
\rightarrow
Reasoning
\rightarrow
Structuralization
\rightarrow
Validation
\rightarrow
Structural\ Growth
}
$$

And the long-term cycle may become:

$$
\boxed{
Folding
\rightarrow
Localization
\rightarrow
Unfolding
\rightarrow
Growth
\rightarrow
Refolding
}
$$

---

# 67. Conclusion

Large Language Models can be understood at more than one level.

At the implementation level, they are parameterized neural computational systems.

At the behavioral level, they can perform sophisticated reasoning.

At the structural explanatory level, they can be viewed as systems in which broad language-mediated intelligence has been folded into reusable latent capability.

Inference then selectively unfolds relevant portions of that capability.

This interpretation helps explain why:

* the same model can support many domains;
* prompts strongly shape reasoning;
* reasoning can be progressive;
* reasoning can branch;
* additional compute can sometimes help;
* too much reasoning can also hurt.

The resulting problem is not simply:

> **Can the model reason?**

It becomes:

> **What should be unfolded?**

> **Where should it be unfolded?**

> **How deeply should it be unfolded?**

> **When should unfolding stop?**

> **Which unfolded structures should persist?**

These questions naturally bring Structural Intelligence into the picture.

Structural Intelligence provides explicit mechanisms for:

* Localization;
* Gap Detection;
* TaskGraph positioning;
* CCC triggering;
* structural validation;
* persistence;
* reuse.

Thus the two reasoning systems approach the same local reasoning problem from opposite directions:

$$
LLM:
Folded\ Space
\rightarrow
Unfold
$$

$$
SI:
Structural\ Space
\rightarrow
Localize
$$

Their meeting point is:

$$
\boxed{
Local\ Reasoning\ Region
}
$$

This produces the central handshake:

$$
\boxed{
LLM\ Unfolding
\leftrightarrow
SI\ Localization
}
$$

The next paper develops that handshake directly.

---

## Next

**STAR-006 — Where LLM Unfolding Meets Structural Localization**

The next paper focuses on:

$$
\boxed{
R_{LLM}^{Unfold}
\approx
R_{SI}^{Localized}
}
$$

and develops the two-way reasoning loop:

$$
\boxed{
SI\ Localization
\rightarrow
LLM\ Unfolding
\rightarrow
Reasoning
\rightarrow
Structural\ Extraction
\rightarrow
SI\ Growth
}
$$

It will establish the local reasoning region as the functional interface between latent LLM intelligence and explicit Structural Intelligence.
