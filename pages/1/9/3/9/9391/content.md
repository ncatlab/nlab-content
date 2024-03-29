
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A **normed group** is to a [[group]] what a [[normed vector space]] is to a [[vector space]].  It consists of a group together with a length function (a [[norm]]) and, as for normed vector spaces, gives rise to a [[metric space]].

A [[complete space|complete]] normed group is a _[[complete normed group]]_.


## Definition

### Normed groups

+-- {: .num_defn #NormedGroup}
###### Definition

A **normed group** is a pair $(G,\rho)$ where $G$ is a [[group]] and $\rho \colon G \to [0,\infty) \subset \mathbb{R}$ is a [[function]], the _norm_, satisfying the following conditions:

1. $\rho(g) = 0$ if and only if $g$ is the identity element in $G$,
2. $\rho(g^{-1}) = \rho(g)$,
3. $\rho(g h) \le \rho(g) + \rho(h)$.

=--

+-- {: .num_defn #homomorphisms}
###### Definitions

There are a few different senses of [[homomorphism]] between normed groups; the first is usually taken as the default but the second fits in better with [[normed rings]] and the obvious notion of [[isomorphism]] as two structures\' being 'the same'.

A __bounded homomorphism__ $(G_1,\rho_1)\to (G_2,\rho_2)$ of normed groups, def. \ref{NormedGroup}, is a group homomorphism $f \colon G_1 \to G_2$
of the underlying groups such that there is $C \in \mathbb{R}_{\geq 0} $
such that for all $g\in G_1$ we have $\rho_2(f(g)) \leq C\cdot\rho_1(g)$.

A __short homomorphism__ $(G_1,\rho_1)\to (G_2,\rho_2)$ of normed groups is a group homomorphism $f \colon G_1 \to G_2$
of the underlying groups such that for all $g\in G_1$ we have $\rho_2(f(g)) \leq \cdot\rho_1(g)$.
=--

+-- {: .num_remark }
###### Remark

If $G$ is a [[vector space]] (viewed as an [[abelian group]]) the conditions on $\rho$ in def. \ref{NormedGroup} almost correspond to the [[axioms]] for a [[norm]] in the context of a [[normed vector space]].  The difference is that homogeneity is only assumed for $-1$ instead of for all elements of the coefficient field.

=--

+-- {: .num_remark }
###### Remark

A norm on a group in def. \ref{NormedGroup}
defines two [[metrics]]:

$$
d_L(g,h) = \rho(g^{-1} h), \qquad d_R(g,h) = \rho(g h^{-1})
$$

The former is left invariant, the latter right invariant.

=--

+-- {: .num_remark }
###### Remark

A normed group is not necessarily a [[topological group]], see ([Bingham-Ostaszweszki](#BinghamOstaszweszki)).

=--

### Normed groupoids

The definition can be extended to [[groupoids]].

+-- {: .num_defn }
###### Definition
A **normed groupoid** is a pair $(G,\rho)$ where $G = (G_1,G_2)$ is a [[groupoid]] and $\rho \colon G_2 \to [0,\infty)$ is a function on the arrows of $G$ satisfying the conditions:

1. $\rho(g) = 0$ if and only if $g$ is an identity arrow,
2. $\rho(g) = \rho(g^{-1})$,
3. if $g h$ exists then $\rho(g h) \le \rho(g) + \rho(h)$.
=--

From a normed groupoid we do not just get a single metric space.  Rather we get one metric space for each object.  For $x \in G_1$ the underlying set of the corresponding metric space is the set of all arrows with source $x$.  The metric is then $d_x(g,h) = \rho(g h^{-1})$.  An arrow from $x$ to $y$ induces an [[isometry]] by right translation.

This reverses: from a [[metric space]], say $X$, we get a normed groupoid by taking the trivial groupoid on $X$.  An arrow in this groupoid is simply a pair $(x,y)$ of elements, whence we define the norm on $G \coloneqq X \times X$ by $\rho(x,y) = d_X(x,y)$.


## Related concepts

* [[bornological group]]

* [[Banach space]]

* [[normed ring]]

[[!include analytic geometry ingredients -- table]]


## References

* {#BinghamOstaszweszki} N. Bingham, A. Ostaszewski, _Normed groups: dichotomy and duality_ (, [pdf](http://www.maths.lse.ac.uk/Personal/adam/DM656NormedGroups.pdf), [pdf](http://www.maths.lse.ac.uk/Personal/adam/BOst12-rev.pdf))


[[!redirects normed group]]
[[!redirects normed groups]]
