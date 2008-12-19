In ordinary category theory, given a functor $F: C^{op} \times C \to X$, an <i>end</i> of $F$ in $X$ is an object $e$ of $X$ equipped with a universal dinatural transformation from $e$ to $F$. This means that given any dinatural transformation from an object $x$ of $X$ to $F$, there exists a unique map $x \to e$ which respects the dinatural transformations. 

In more detail: the end of $F$ is traditionally denoted $\int_{c: C} F(c, c)$, and the components of the universal dinatural transformation, 

$$\pi_c: \int_{c: C} F(c, c) \to F(c, c)$$ 

are called the <i>projection maps</i> of the end. Then, given any dinatural transformation with components 

$$\theta_c: x \to F(c, c),$$ 

there exists a unique map $f: x \to e$ such that 

$$\theta_c = \pi_c f$$ 

for every object $c$ of $C$. The notion of coend is dual to the notion of end. 

There is an enriched category version of end, as follows. Let $V$ be a symmetric monoidal category, let $C, X$ be $V$-enriched categories, and let $F: C^{op} \times C \to X$ be a $V$-enriched functor. 