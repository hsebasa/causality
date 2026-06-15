## Chapter 17. A Complete Worked Identification

Binary $A_0 \to L \to A_1 \to Y$, hidden $H \to L, Y$; mechanisms: $H, A_0 \sim \mathrm{Be}(.5)$; $P(L{=}1 \mid A_0, H) = .8/.4/.5/.1$ for $(0,0),(0,1),(1,0),(1,1)$; $P(A_1{=}1 \mid L) = .8/.3$; $P(Y{=}1) = .2 + .2A_0 + .2A_1 + .3H$. Truth by construction: $P(Y(a_0,a_1){=}1) = .35 + .2a_0 + .2a_1$. $L$ is both a confounder of $A_1$ (must condition) and a collider/post-treatment variable for $A_0$ (must not) — **no adjustment set exists**: the 1986 double-bind. **SWIG template** $\mathcal{G}(a_0,a_1)$: $a_0 \to L(a_0) \to A_1(a_0)$; $a_0, a_1 \to Y(a_0,a_1)$; $H \to L(a_0), Y(a_0,a_1)$. d-separation gives the two single-world conditions $Y(a_0,a_1) \perp A_0$ and $Y(a_0,a_1) \perp A_1(a_0) \mid L(a_0), A_0$; Robins' criterion licenses $\sum_l P(Y \mid a_0, l, a_1)\,P(l \mid a_0)$ despite hidden $H$ — and *not* the near-misses $P(Y \mid a_0, a_1)$, $\sum_l P(Y \mid a_0,l,a_1)P(l)$, or $\sum_l \cdots P(l \mid a_0, a_1)$. Key observed ingredients: $P(L{=}1 \mid A_0{=}0) = 3/5$, $P(L{=}1 \mid A_0{=}1) = 3/10$; $P(Y{=}1 \mid 1, L{=}1, 1) = 13/20$, $P(Y{=}1 \mid 1, L{=}0, 1) = 111/140$ — so the $(1,1)$ cell is $\tfrac{3}{10}\cdot\tfrac{13}{20} + \tfrac{7}{10}\cdot\tfrac{111}{140} = 0.75$ exactly. Full table (exact rationals, App. E):

| regime | truth | g-formula | naive cond. | naive adj. |
|---|---|---|---|---|
| $(0,0)$ | .3500 | **.3500** | .3875 | .3688 |
| $(0,1)$ | .5500 | **.5500** | .5250 | .5687 |
| $(1,0)$ | .5500 | **.5500** | .5773 | .5286 |
| $(1,1)$ | .7500 | **.7500** | .7167 | .7286 |
| joint effect | **.4000** | **.4000** | .3292 | .3598 |

Dynamic regime "treat iff sick" ($A_1 := L$): **.4700 / .6100** for $a_0 = 0, 1$ — exact. Lessons: ignorability read off a *derived* graph; only single-world independencies used; hidden variables fine (Robins' criterion); statics and dynamics by one construction; both naive estimands fail in every cell (by 18% and 10% of the true effect).
