<div class="rightHandSide toc">
[[!include cohomology - contents]]

***

[[!include higher category theory - contents]]


***

[[!include higher geometry - contents]]

***

[[!include higher algebra - contents]]


</div>



+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

see there for background and context.

This entry contains a basic introduction to derived [[group scheme]]s and their orientations.


=--

Previous:

* [[A Survey of Elliptic Cohomology - cohomology theories]]

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

* [[A Survey of Elliptic Cohomology - E-infinity rings and derived schemes]]

* [[A Survey of Elliptic Cohomology - elliptic curves]]

* [[A Survey of Elliptic Cohomology - equivariant cohomology]]



>the following are rough unpolished notes taken more or less verbatim from some seminar talk -- needs attention, meaning: **somebody should go through this and polish**


***

#Contents#

* toc
{:toc}


# Introduction #

Recall from last time that given $G$ an algebraic group such that the [[formal spectrum]] $Spf A(\mathbb{C}P^\infty)$ is the completion $\hat G$, we could define $A_{S^1}({*}) := \mathcal{o}_{G}$ then passing to germs gave a completion map

$$
  A_{S^1}({*}) \to A(\mathbb{C}P^\infty) = 
  A^{Bor}_{S^1}({*}).
$$

The problem we (begin) to address here is how to extend this equivariant cohomology to other spaces besides the point.  This requires derived algebraic geometry.


# Derived group schemes#


Recall that a commutative [[group scheme]] over a scheme $X$ is a functor
$$
G: \mathrm{Sch} /X^{op} \to \mathrm{Ab}
$$
such that composition with the forgetful functor $F: \mathrm{Ab} \to \mathrm{Set}$ is representable.

We would like extend this definition to the world of [[derived scheme]]s.  There are two problems

1. Because of the higher categorical nature of derived schemes Hom sets are spaces.

1. Everything should in the $\infty$-setting, that is defined only up to homotopy.

We will not worry about the second concern and address the first by replacing the category $\mathrm{Ab}$ with $\mathrm{TopAb}$ and $\mathrm{Set}$ with $\mathrm{Top}$.



> The following definition is somewhat restrictive and really should incorporate more of the $\infty$-structure.


**Definition** A commutative [[derived group scheme]] over a [[derived scheme]] $X$ is a topological functor
$$
G: \mathrm{DSch} / X^{op} \to \mathrm{TopAb}
$$ 
such that composition with the forgetful functor $F: \mathrm{TopAb} \to \mathrm{Top}$ is representable (up to weak equivalence) by an object which is [[flat]] over $X$.


**Examples**

1. Let $X$ be a scheme, then we have an associated [[derived scheme]] $\overline{X}$.  The structure sheaf of $\overline{X}$ is obtained by viewing the structure sheaf of $X$ as a presheaf of $E_\infty$-rings and then sheafifying.  We then have an equivalence between commutative [[derived group scheme]]s over $\overline{X}$ and commutative [[group scheme]]s which are flat over $X$.

1. For $X$ a [[derived scheme]] we have a map from commutative [[derived group scheme]]s over $X$ to commutative [[group scheme]]s which are flat over $\pi_0 X$.


##Preorientations##

Throughout $A$ will be an $E_\infty$-ring, $X$ the affine [[derived scheme]] $\mathrm{Spec} A$, $G$ a commutative [[derived group scheme]] over $X$, $A_{S^1}$ the $E_\infty$-ring given by $\Gamma (G)$, and $A^{\mathbb{C}P^\infty}$ the $E_\infty$-ring given by

$$
  A^{\mathbb{C}P^\infty} = \mathrm{Hom}_{E_\infty} (\mathbb{C}P^\infty , A).
$$

**Definition**(Preliminary) A preorientation of $G$ is a morphism of commutative [[derived group scheme]]s over $X$
$$
\sigma : \mathrm{Spf} A^{\mathbb{C}P^\infty} \to G,
$$
where $\mathrm{Spf} A^{\mathbb{C}P^\infty}$ is the completion wrt the ideal $\mathrm{ker} (A^{\mathbb{C}P^\infty} \to A^{pt} = A)$. A preorientation is an orientation if the induced map
$$
\hat \sigma : \mathrm{Spf} A^{\mathbb{C}P^\infty} \to \hat G
$$
is an isomorphism.

Suppose that $G$ is affine, then a map 
$$
\sigma : \mathrm{Spf} A^{\mathbb{C}P^\infty} \to G
$$
corresponds to a map $A_{S^1} \to A^{\mathbb{C}P^\infty}$
which is the same as a map
$$
\mathbb{C}P^\infty \to \mathrm{Hom} (X, G) = G(X).
$$
Hence we are led to the following definition.

**Definition** Let $X$ be a [[derived scheme]] and $G$ a commutative [[derived group scheme]] over $X$.  A preorientation of $G$ is a morphism of topological commutative monoids
$$
\mathbb{P} (\mathbb{C} [\alpha]) = \mathbb{C}P^\infty \to G(X).
$$