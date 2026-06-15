## Chapter 2. Abduction: The Free Right Adjoint

**2.1 Theorem (abduction exists, uniquely).** *Every join-preserving $f$ has a right adjoint $f^{\sharp}(B) := \bigvee\{C : f(C) \leq B\}$, characterized by $f(C) \leq B \iff C \leq f^{\sharp}(B)$, and it is unique.* *Proof:* $f(f^{\sharp}B) = \bigvee\{f(C) : f(C) \leq B\} \leq B$ by the axiom; so $C \leq f^{\sharp}B \Rightarrow f(C) \leq f(f^{\sharp}B) \leq B$; the converse is membership in the defining family; adjoints are unique. $\square$ Reading: $f^{\sharp}(B)$ is **the largest cause of $B$** — the maximal event guaranteed to produce within $B$. Explainability is not postulated; it is the adjoint shadow of production.

**2.2 Theorem (explanation is logical).** *$f^{\sharp}$ preserves arbitrary meets.* *Proof:* $C \leq f^{\sharp}(\bigwedge B_i) \iff f(C) \leq \bigwedge B_i \iff \forall i\, f(C) \leq B_i \iff \forall i\, C \leq f^{\sharp}(B_i) \iff C \leq \bigwedge f^{\sharp}(B_i)$. $\square$

**2.3 Notation ($R$ and $f$ determine each other).** A relation on $X$ is $R \subseteq X \times X$, read causally: $(x,y) \in R$ means "$y$ is a possible immediate successor of $x$"; successor sets $R(x)$; image $R[A] = \bigcup_{x \in A} R(x)$. Dictionary, one line each way: $f_R(A) := R[A]$ preserves joins; conversely $R_f(x) := f(\{x\})$ — **the relation is the law read on atoms** — and join-preservation forces $f(A) = \bigcup_{x \in A} f(\{x\}) = R_f[A]$, with $R_f$ the unique relation presenting $f$ (test on singletons). **Sharpness** (state-determinism): $|R(x)| = 1$; then $R(x) = \{f(x)\}$ recovers the state map, resolving the overloading $f(\{x\}) = \{f(x)\}$.

**2.4 Example (the coin) + the two explainers.** For 1.7(a): $f^{\sharp}(B) = \{x : R(x) \subseteq B\}$, so $f^{\sharp}\{h\} = \{h\}$, $f^{\sharp}\{t\} = \{t\}$, but $f^{\sharp}(\{h\} \vee \{t\}) = \top \ni c$: **certainty of a disjunction does not split** — $f^{\sharp}$ does not preserve joins. Relational abduction splits: $\Diamond B := \{x : R(x) \cap B \neq \varnothing\}$ (possible cause; preserves joins, breaks meets) vs. $\Box B := f^{\sharp}(B)$ (necessary cause; preserves meets, breaks joins). **Theorem:** $\Diamond = \Box$ on all events iff $R$ is total and functional — *sharpness is exactly the collapse of possible and necessary causation*. *Proof:* a fiber with two elements is split by a separating $B$; an empty fiber puts $x$ in $\Box\bot$; singletons identify the two. $\square$

**2.5 Remark (determinism wears three hats — only one is optional).** (i) *The law of events is a function, always*: $f(A)$ is uniquely determined — "if it rains, a determinate set of events happens" is the definition, not an axiom. (ii) *Sharpness* is the optional claim: maximal descriptions stay maximal; its failure is **branching** — a menu of alternatives, no weights, a possibilistic not probabilistic notion. At the atom level multiplicity can only be disjunctive (distinct maximal descriptions exclude each other); the conjunctive multiplicity of "the ground gets wet *and* it cools" is description overlap, present even when sharp. (iii) *Stochasticity does not exist at this level at all* — weights are Part III structure.

**2.6 Proposition (determinization, both directions).** (a) Every $(L, f)$ *is* a deterministic arena: states $= L$, law $= f$ — a relational arena is the atom-level shadow of $(\mathcal{P}(X), R[\cdot])$ (the subset construction): **nondeterminism is the determinism of regions**. (b) Every relational law is the projection of a sharp law on $X \times U$ (a hidden branch-selecting coordinate) — the move unit-resolution makes systematic (Ch. 8). $\square$

**2.7 Observability.** A *read-interface* is a designated subframe $\mathcal{O} \subseteq L$ (closed under arbitrary joins and finite meets; $\bot, \top \in \mathcal{O}$), or dually a quotient $L \twoheadrightarrow L_{\mathrm{obs}}$ — sub vs. quotient is the mono/epi pair of Ch. 12. **Axiom OBS:** $f^{\sharp}(\mathcal{O}) \subseteq \mathcal{O}$ — explanations of observables are observable. **Theorem (continuity, located):** in the sharp powerset case $f^{\sharp} = f^{-1}$ (the adjoint of direct image is preimage), so OBS *is* the historical $\mathcal{O}$-continuity axiom. **Counterexample (do not require forward closure):** $X = \{a, b\}$, $\mathcal{O} = \{\varnothing, \{a\}, X\}$, $f \equiv b$: OBS holds, yet $f(\{a\}) = \{b\} \notin \mathcal{O}$ — a visible cause with hidden effect. The historical $(X, \mathcal{O}, f)$ decomposes as world $+$ read-interface $+$ their compatibility.

**2.8 The instrument panel.** Each candidate preservation law is the axiom, a theorem, or *equivalent to a world property*:

| law | status / world property | witness |
|---|---|---|
| joins forward | **axiom** | — |
| $f(\bot) = \bot$ | theorem (production stance) | — |
| meets backward ($f^{\sharp}$) | theorem (adjointness, 2.2) | — |
| meets forward | $\iff$ injectivity (no merging) | $f[\{2\} \wedge \{9\}] = \bot$, $f[\{2\}] \wedge f[\{9\}] = \{4\}$ (squaring, Ch. 21) |
| joins backward ($f^{\sharp}$) | $\iff$ sharpness | the coin (2.4) |
| $f(\sim A) \leq \sim f(A)$ | $\iff$ injectivity | as above |
| $\sim f(A) \leq f(\sim A)$ | $\iff$ no uncaused states | Garden-of-Eden states are the obstruction |
| both complement laws | $\iff$ **reversibility** | the arrow of time as a failed equation |

$f_{\flat}(B) := \bigvee\{C : f^{\sharp}(C) \leq B\}$: in the sharp powerset case $\{y : f^{-1}(\{y\}) \subseteq B\}$ — the largest event *all of whose causes* lie in $B$ (Garden-of-Eden states belong vacuously). Sharp abduction sits in the adjoint triple $f \dashv f^{\sharp} \dashv f_{\flat}$ — a left and right adjoint at once, which is *why* deterministic $f^{-1}$ preserved every Boolean operation.

**2.9 Induced subtheories.** $M \subseteq L$ closed under $L$-joins with $f(M) \subseteq M$ gives a causal structure $(M, f|_M)$. Examples: (i) every future cone $\downarrow f^{\ast}(A)$ — "the world after $A$" ($f(B) \leq f(f^{\ast}A) \leq f^{\ast}A$); (ii) state-level forward-invariant regions — basins, the recurrent core; the shrinking possibility chain $f^t[X]$ is a *descending chain of subtheories*; (iii) $\mathcal{O}$ under OBS is backward-invariant, so what observation carries is the *abduction* dynamics $(\mathcal{O}, f^{\sharp})$, not production. Honesty: meets in $M$ may differ from meets in $L$ (cf. 3.3).
