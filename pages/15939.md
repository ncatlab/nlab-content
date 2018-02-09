[[!redirects Generalized Lambda-structure]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

* table of contents
{:toc}

## Overview

The usual notion of [[Lambda-ring]] is directly related to the Banach ring
$(\mathbb{Z},|\cdot|_0)$ of integers equipped with their trivial norm in
the following way: a [[Lambda-ring]] is a usual ring equipped with
an action of the monoid $\mathbb{N}=\mathbb{Z}$-$\{0\}/\{\pm 1\}$.
Remark that some important Lambda-rings, such as K-theory, are
actually equipped with an additional $\mathbb{Z}/2$-grading,
that may be combined with the Lambda-structure to get an action
of the full monoid $\mathbb{Z}$-$\{0\}$. It is important to remark here
that the $\Lambda$-structure on $K$-theory allows one to get back
(as the spectrum of the Lambda-operations) the full $\mathbb{Z}$-grading
on Betti cohomology.

From the perspective of [[global analytic geometry]], one thinks of Lambda-structures
as related to the Banach ring of integers with their trivial norm,
so that one may seek for various generalizations, that will be called
"generalized Lambda-structure", associated to more general Banach or ind-Banach rings.

## Definition

Let $(R,|\cdot|)$ be an integral Banach ring equipped with a multiplicative norm.
We will denote $\Lambda(R,|\cdot|)$ the monoid given by
$$\Lambda(R,|\cdot|):=\mathrm{Frac}(R)\cap \{a\in R,\;|a|\leq 1\}.$$

## Examples

There is not yet a precise notion of generalized Lambda-structure, but one may easily give various of its concrete incarnations.

1. The classical notion of ($\mathbb{Z}/2$-graded) Lambda-ring may be seen as a $\Lambda(\mathbb{Z},|\cdot|_0)=\mathbb{Z}$-$\{0\}$-structure. The (geometric/Weil) cohomology theories of arithmetic geometry (i.e. for schemes over $\mathbb{Z}$) are often equipped with an $\mathbb{N}$-grading, that one may interpret as a classical Lambda-ring structure.

1. The [[absolute cohomology]] theories in arithmetic geometry such as Beilinson-[[Deligne cohomology]] or [[motivic cohomology]] are equipped with a natural bi-graduation, related to the fact that they are defined by the (homotopical: think of a Leray spectral sequence) combination of geometric methods (Lambda-structures/Frobenii) and of differential methods (Hodge filtration of de Rham cohomology or $\mathbb{G}_m$-stabilization in motivic homotopy theory, that corresponds to the "[[Tate twist]]" grading).
The corresponding Banach ring may be simply given by the Banach ring
$$(R,|\cdot|):=(\mathbb{Z}[T],|\cdot|_0)$$
of polynomials equipped with their trivial norm (analytic functions on the non-archimedean global analytic unit disc). The bigrading is given by the action of the monoid
$$
\Lambda(R,|\cdot|):=
\mathbb{Q}(T)^\times\cap \mathbb{Z}[T]=\mathbb{Z}[T]-\{0\}.
$$
The ([[Tate twist]]) motivic and cohomological gradings are given respectively by the actions of the monoid $\mathbb{Z}-\{0\}$ and the monoid of powers of $T$.

1. The (yet to be properly defined) cohomology theories in [[global analytic geometry]] have a different type of bigrading (that is related to the idea of the algebra of polynomials over the [[field with one element]], formulated precisely, e.g., in Durov's setting of [[generalized rings]], i.e., commutative algebraic monads).
We will now extend the above definition of the monoid $\Lambda$ to the setting of ind-Banach ring, since this operation seems necessary to understand absolute cohomologies.
The corresponding (ind-)Banach ring may be simply given by the ind-Banach ring
$$R:=\mathbb{Z}\{T\}^\dagger$$
of overconvergent power series on the unit disc with coefficients in the Banach ring $(\mathbb{Z},|\cdot|_\infty)$: the `geometric` classical Lambda-structure is given by the base Banach ring, and the differential/absolute graduation is given by the $T$-part of the monoid (we may need to make a completion here)
$$
\Lambda(R):=
\mathrm{Frac}(\mathbb{R}\{T\}^\dagger)^\times\cap \{P\in \mathbb{Z}\{T\}^\dagger,|P|_{\infty,1}\leq 1\}=\mathbb{F}_{\{\pm 1\}}[T]-\{0\}.
$$
This is the monoid of polynomials whose terms are all equal to zero except exactly one, that is equal to $\{\pm 1\}$. It contains and extends the monoid $\Lambda(\mathbb{Z},|\cdot|_\infty)=\{\pm 1\}=(\mathbb{F}_{\{\pm 1\}})^\times$ in degree zero. This will be the natural grading monoid (generalized Lambda-structure) for absolute motives, i.e., motivic cohomology theories over $(\mathbb{Z},|\cdot|_\infty)$. Remark that the recent work of [[Peter Scholze]] on local Schtukas in mixed characteristic also uses in an essential way objects such as the unit disc over the given base Banach ring.

1. The notion of $\Lambda(\mathbb{Z},|\cdot|_\infty)=\{\pm 1\}$-structure is simply given by the notion of $\mathbb{Z}/2$-grading. Many cohomological invariants, such as [[K-theory]], negative [[cyclic homology]] and the [[Chern character]] are equipped with a natural $\mathbb{Z}/2$-grading. It is quite probable that one can't hope to get something more that a $\mathbb{Z}/2$-grading on a "really natural" cohomology theory in [[global analytic geometry]].

1. In the theory of $(\Phi,\Gamma)$-modules, the monoid $\Lambda(\mathbb{Z}_p,|\cdot|_p)=\mathbb{Z}_p$-$\{0\}$ plays a central role. It looks like a not so hard but important task to clarify the relation of this theory with the classical notion of Lambda-ring.

1. It is an interesting question to try to understand the relation of classical Hodge theory (over $\mathbb{R}$ or $\mathbb{C}$) with the notion of Lambda-structure on the corresponding Banach ring. This may show interesting limits to the idea of generalizing Lambda-structures to other Banach rings. The case of $\mathbb{R}$ may (or may not) be treated using $\mathbb{Z}/2$-equivariant methods. An important point, in this perspective, is that the naive archimedean generalization of the notion of $(\Phi,\Gamma)$-module does not work, because $S^1$ does not act directly on the open complex unit disc $D^\circ(1,1)$. One only has an infinitesimal action (connection $\nabla$), whose combination with the infinitesimal generator $\Phi$ of $\mathbb{R}_+^*$ may be seen as an archimedean analog of the $p$-adic differential equations used in Berger's thesis to prove the monodromy theorem of $p$-adic Hodge theory. An important drawback of this infinitesimal approach (in the $p$-adic setting) is that the functor from $p$-adic Hodge structures (i.e., $(\Phi,\Gamma)$-modules) to $p$-adic Frobenius-equivariant differential equations is `not fully faithful`: making the action of $U(1)=\mathbb{Z}_p^*$ infinitesimal kills an important part of the information (essentially, the Hodge filtration on de Rham cohomology). A possible solution to this problem may be to work with a multiplicative theory over $[\mathbb{A}^1/\mathbb{G}_m]$ instead of an additive one over $[D^\circ(1,1)/\Lambda]$ or $[D^\circ(1,1)/(\Phi,\nabla)]$, or to use a combination of the additive and multiplicative theory.

1. The monoid that should come in play into the theory of [[spectral interpretation]] for zeroes and poles of global arithmetic and automorphic [[L-functions]] may be given by the monoid $\Lambda(\mathbb{A})$, where $\mathbb{A}$ is the ind-Banach ring of ad&#232;les.

## Geometric interpretation (to be checked very carefully: may be problematic)

One may take inspiration from the theory of $(\Phi,\Gamma)$-modules ($p$-adic Hodge structures) to define a natural notion of $\Lambda$-module in [[global analytic geometry]]. This gives a version of the notion of a "Hodge structure" that works over an integral base, which makes it quite well adapted to the global analytic situation.

Let $R$ be a Banach ring, and $\overset{\circ}{D}(1,1)$ be the open unit disc on $R$. We denote (be careful, this differs from the previously used notation, because it is a different kind of object)
$$\Lambda\subset \overset{\circ}{D}(1,1)\times \overset{\circ}{D}(1,1)$$
the (non-strict) analytic subgroupoid of the groupoid of pairs acting on $\overset{\circ}{D}(1,1)$ given by pairs of the form $(1+x,(1+x)^a)$ where $a\in D(0,1)\cap \GL_1\subset \mathbb{A}^1$,  and
$$(1+x)^a:=\sum_{k\geq 0}\binom{a}{k}x^k.$$
If $R=(\mathbb{Q}_p,|\cdot|_p)$, then we have actually that $\mathbb{Z}_p-\{0\}\subset D(0,1)(\mathbb{Q}_p)$.

A $\Lambda$-module over $R$ is a module over the analytic stack $B\Lambda$ that one may denote as a quotient stack $[\overset{\circ}{D}(1,1)/\Lambda]$. We then have, if $R$ contains the rational numbers, a natural logarithm map
$$log:[\overset{\circ}{D}(1,1)/\Lambda]\to [\mathbb{A}^1/\GL_1]$$
that allows us to give a relation between the classical Hodge filtration of a (say) proper or logarithmically proper analytic space over $R$ to its $R$-Hodge structure, that should be a module over $[\overset{\circ}{D}(1,1)/\Lambda]$.

If we suppose given a (say) strict analytic space over $R$, and one wants to define the associated $R$-Hodge structure, one may simply try to adapt Simpson's construction of the deformation to the normal bundle, to get what one wants. 
Actually, one needs a loop space analog of this construction, that is due to Vezzosi for a derived scheme. Recall that in this derived scheme case, we have
$$LX=\Hom_{dSt}(B\mathbb{Z},X)\cong \Hom_{dSt}(B\mathbb{G}_a,X).$$
We may use the action by multiplication of $\mathbb{A}^1$ on $B\mathbb{G}_a$ to define a family
of actions of $B\mathbb{G}_a$ on $LX$, parametrized by $\mathbb{A}^1$. This gives a $\mathbb{G}_m$-equivariant family
$$Hod(LX)\to \mathbb{A}^1$$
whose fiber at $0$ is $LX$ with the trivial action of $B\mathbb{G}_a$ and whose fiber at $1$ is $LX$ equipped with the usual action of $B\mathbb{G}_a$.

If we want to define a construction that is related to the loop space Hodge filtration through the logarithm map
$$log:[\overset{\circ}{D}(1,1)/\Lambda]\to [\mathbb{A}^1/\mathbb{G}_m],$$
we need to replace $B\mathbb{G}_a$ by $BD^\circ:=B\overset{\circ}{D}(1,1)$,
and the multiplicative action of $\mathbb{A}^1$ on $B\mathbb{G}_a$ by the (partial) action of $D(0,1)$ on $BD^\circ$ through the power map
$$(1+x,a)\mapsto (1+x)^a.$$
We thus replace the derived loop space by the space
$$L^D X:=Hom_{dSt}(B\overset{\circ}{D}(1,1),X),$$
together with its (partial) action of $B\overset{\circ}{D}(1,1)$ given by the (partial) multiplication of $\overset{\circ}{D}(1,1)\subset \mathbb{G}_m$. There is actually a family of such actions parametrized by $D(0,1)$ through the (partial) map
$$D(0,1)\times B\overset{\circ}{D}(1,1)\times L^D X\to L^D X$$
given by $(a,d,\gamma)\mapsto \gamma\circ m_{d^a}$. This family of actions gives a space
$$Hod(L^D X)\to D(0,1)$$
whose fiber at $0$ is the trivial action of $B\overset{\circ}{D}(1,1)$ on $L^D X$
and whose fiber at $1$ is the standard action.

## Related notion

[[generalized higher loop spaces]]