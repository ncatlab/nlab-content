In ordinary [[category theory]], given a [[functor]] $F: C^{op} \times C \to X$, an __end__ of $F$ in $X$ is an object $e$ of $X$ equipped with a [[universal construction|universal]] [[dinatural transformation]] from $e$ to $F$. This means that given any dinatural transformation from an object $x$ of $X$ to $F$, there exists a unique map $x \to e$ which respects the dinatural transformations. 

In more detail: the end of $F$ is traditionally denoted $\int_{c: C} F(c, c)$, and the components of the universal dinatural transformation, 
$$\pi_c: \int_{c: C} F(c, c) \to F(c, c)$$ 
are called the _projection maps_ of the end. Then, given any dinatural transformation with components 
$$\theta_c: x \to F(c, c),$$ 
there exists a unique map $f: x \to e$ such that 
$$\theta_c = \pi_c f$$ 
for every object $c$ of $C$.

The notion of __coend__ is dual to the notion of end, written $\int^{c: C} F(c, c)$.

There is a version in [[enriched category theory]], as follows. Let $V$ be a [[symmetric monoidal category]], let $C$ be a $V$-[[enriched category]], and let $F: C^{op} \otimes C \to V$ be a $V$-[[enriched functor]]. In particular there is a covariant [[action]] of $C$ on $F$, with components
$$\lambda_{c, d, e}: F(c, d) \otimes C(d, e) \to F(c, e),$$
[where $C(d, e)$ is customary notation for the enriched hom $\hom_C(d, e)$ of $C$ in $V$], and a contravariant action of $C$ on $F$, with components
$$\rho_{c, d, e}: F(d, e) \otimes C(c, d) \to F(c, e).$$ 

A $V$-_dinatural transformation_
$$\theta: v \stackrel{\bullet}{\to} F$$ 
from $v$ to $F$ consists of a family of arrows in $V$, 
$$\theta_c: v \to F(c, c),$$ 
indexed over objects $c$ of $C$, such that for every pair of objects $(c, d)$ in $V$, the composites of (1) and (2) agree: 
$$v \otimes C(c, d) \stackrel{\theta_c \otimes 1}{\to} F(c, c) \otimes C(c, d) \stackrel{\lambda_{c, c, d}}{\to} F(c, d) \qquad (1)$$ 
$$v \otimes C(c, d) \stackrel{\theta_d \otimes 1}{\to} F(d, d) \otimes C(c, d) \stackrel{\rho_{c, d, d}}{\to} F(c, d) \qquad (2)$$

A $V$-enriched _end_ of $F$ is an object $\int_{c: C} F(c, c)$ of $V$ equipped with a $V$-dinatural transformation 
$$\pi: \int_{c: C} F(c, c) \stackrel{\bullet}{\to} F$$ 
such any $V$-dinatural transformation $\theta$ from $v$ to $F$ is obtained by pulling back the components of $\pi$ along $f: v \to \int_{c: C} F(c, c)$, for some unique map $f$. That is,
$$\theta_c = \pi_c f$$ 
for all objects $c$ of $C$. 

If $X$ is any $V$-enriched category and $F: C^{op} \otimes C \to X$ is a $V$-enriched functor, then the _end_ of $F$ in $X$ is an object $\int_{c: C} F(c, c)$ of $X$ equipped with an $Ob(C)$-indexed family of arrows 
$$\pi_c: I \to X(\int_{c: C} F(c, c), F(c, c))$$ 
in $V$, such that for every object $x$ of $X$, the family 
of maps 
$$X(x, \pi_c): X(x, \int_{c: C} F(c, c)) \to X(x, F(c, c))$$ 
are the projection maps realizing $X(x, \int_{c: C} F(c, c))$ as the corresponding end in $V$. This is an example of the general notion of [[weighted limit]] in enriched category theory. 