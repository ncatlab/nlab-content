# Idea

An **ordinal number** (or just **ordinal**) is one generalization of the [[natural number]]s to infinite magnitudes.


# Definition

In naive [[set theory]], an **ordinal** is an [[isomorphism]] class of [[well-order|well-ordered sets]].  If the well-ordered set is finite, it is a **finite ordinal**; otherwise it is an **infinite** or **transfinite** one.

Like the naive definition of [[cardinal number]], this definition has the problem that each ordinal is then itself a [[proper class]].  Thus, in axiomatic (material) [[set theory]] it is common to consider particular representatives of these equivalence classes as "being" ordinals.  One particularly slick definition is due to von Neumann; in this approach one defines an __ordinal__ to be a [[transitive set|transitive]] set which is [[well-order|well-ordered]] by the membership relation $\in$.  In the presence of the [[axiom of foundation]] so that $\in$ is automatically a [[well-founded relation]], it suffices to require that $\in$ be a transitive relation on the ordinal $X$ in the usual sense, i.e. for $a,b,c\in X$, if $a\in b\in c$ then $a\in c$.  Defined in this way, it is the ordinals form a basis for a similar definition of  [[cardinal number]], as an ordinal which is not bijective in terms of underlying sets to any smaller ordinal (with respect to that relation).

On the other hand, from the perspective of structural [[set theory]], it is [[evil]] to care about distinctions between isomorphic objects, and silly to insist on having a canonical choice of representatives for isomorphism classes.  Therefore, from this point of view it is natural to simply define an **ordinal** to be any [[well-order|well-ordered set]].


# Properties

The class of ordinals is itself [[well-order|well-ordered]].  There are many equivalent ways to define this ordering.  One is that $\alpha\lt\beta$ iff $\alpha$ is isomorphic to a proper _initial segment_ of $\beta$ (that is, a subset $S\subsetneq \beta$ such that $b\in S$ and $a\lt b$ imply $a\in S$).  With the von Neumann definition, this is equivalent to simply saying that $\alpha\in\beta$.

Every ordinal $\alpha$ has a **successor**, which in the von Neumann definition is simply $\alpha \cup \{\alpha\}$.  A **limit ordinal** is any ordinal which is not a successor of any other ordinal.