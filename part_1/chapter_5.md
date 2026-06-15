## Chapter 5. Geometry: One Matrix, Three Semirings

**5.1 The latency quasi-metric.** $d(x, y) := \min\{n : f^n(x) = y\} \in \mathbb{N} \cup \{\infty\}$. Then $d(x,x) = 0$; $d(x,z) \leq d(x,y) + d(y,z)$ (concatenate runs); and asymmetry is generic — $d(x,y) < \infty = d(y,x)$ — *the asymmetry of causation realized as asymmetry of distance*. Future cones are the balls; orbit segments are the geodesics (the only paths the law affords, automatically shortest). **Recovery:** the law is the unit sphere — $f(x)$ is the unique point at distance exactly $1$ (sharp case under AC). $\square$

**5.2 Theorem (one matrix, three semirings).** Encode the law as a matrix $A$ indexed by states; the Kleene star $A^{\ast} = \bigvee_n A^{n}$ computes, per semiring:

| semiring | $A_{xy}$ | $A^{\ast}$ |
|---|---|---|
| Boolean $(\vee, \wedge)$ | $1$ iff $y = f(x)$ | reachability $\rightsquigarrow$ |
| tropical $(\min, +)$ | $1$ iff $y = f(x)$, else $\infty$ | **the latency $d$** — the geometry |
| affine-stochastic (normalized) | $P(y \mid x)$ | hitting structure — the measure layer |

*Proof (tropical):* $(A^{\otimes n})_{xy} = n$ iff $f^n(x) = y$, else $\infty$; the star takes the minimum over $n$. $\square$ The stochastic row is the *affine cousin*, not a literal base change (normalization is extra structure; no idempotent join, no convergent star). **The measure layer is one face of an intrinsic object, not the main object.**

**5.3 Classification of finite arenas.** Every component of a finite sharp arena is a set of trees grafted onto one cycle ($\rho$-shapes); the multiset of cycle lengths plus the grafted tree shapes is a complete isomorphism invariant — credited combinatorics [verify], causal reading: *recurrence skeleton $+$ transient anatomy $=$ the identity of a finite causal world*. Worked instance: Ch. 21 ($x^2 \bmod 11$).
