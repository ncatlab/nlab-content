+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


This is a subentry of _[[sheaf]]_ about the _plus-construction on presheaves_. For other constructions called _[[plus construction]]_, see there.

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The _plus construction_ $(-)^+ : PSh(C) \to PSh(C)$ on presheaves over a [[site]] $C$ is an operation that makes a presheaf "closer" to being a sheaf.

For ordinary sheaves of sets, the plus construction replaces a [[presheaf]] first by a [[separated presheaf]] and then by a [[sheaf]].

$$
  PSh(C) \stackrel{(-)^+}{\to} SepPSh(C)
  \stackrel{(-)^+}{\to} Sh(C)
  \,.
$$

(The first of these steps, however, is not a [[reflective subcategory|reflection]] into $SepPsh(C)$.)  Notice that in terms of [[n-truncated]] morphisms, a presheaf is

* separated precisely if every comparison map $A(U) \to Desc(A,U)$ to the set of [[descent data]] is [[(-1)-truncated]], namely a [[monomorphism]];

* a sheaf precisely if every such comparison map is [[(-2)-truncated]], namely an [[equivalence]].

More generally, in [[(n,1)-topos]] theory, the plus-construction is applied $(n+1)$-times in a row to an [[(n,1)-presheaf]] (a presheaf of $(n-1)$-groupoids), at each step decreasing the truncatedness of the comparison map until at the last step it becomes an actual [[(n,1)-sheaf]].  When $n=\infty$, even a countable sequence of applications does not suffice, but a transfinite one does.

## Definition


+-- {: .num_defn #PlusConstruction}
###### Definition

Let $C$ be a small site equipped with a [[Grothendieck topology]] $J$, let $A:C^{op}\to Set$ be a functor. Then the _plus construction (functor)_ $(-)^+ : PSh(C) \to PSh(C)$, resp. the _plus construction_ $A^+$ _of_ $A \in PSh(C)$ is defined by one of following equivalent descriptions:

1. $A^+:U\mapsto colim_{(R\to U)\in J(U)}A(R)$ where $J(U)$ denotes the poset of $J$-covering [[sieve|sieves]] on $U$.

1. For $U\in C^{op}$ we define $A^+(U)$ to be an [[equivalence class]] of pairs $(R,s)$ where $R\in J(U)$ and $s=(s_f\in A(dom f)|f\in R)$ is a [[matching family|compatible family]] of elements of $A$ relative to $R$, and $(R,s)\sim (R^\prime,s^\prime)$ iff there is a $J$-covering sieve $\R^{\prime \prime}\subseteq R\cap R^\prime$ on which the restrictions of $s$ and $s^\prime$ agree.

1. $A^+:U\mapsto colim_{(V\hookrightarrow U)\in W}A(V)$ where $W$ denotes the class $W:=(f^*)^{-1}Core(Sh(C)_1)$ of those morphisms in $PSh(C)$ which are sent to isomorphisms by the sheafification functor $f^*$ and the colimit is taken over all [[dense monomorphism|dense monomorphisms]] only. 



=--

## Properties

+-- {: .num_remark}
###### Remark

1. $(-)^+:A\mapsto A^+$ is a functor.

1. $A^+$ is a functor.

1. $A^+$ is a separated presheaf.

1. If $A$ is separated then $A^+$ is a sheaf.

=--

Note that $(-)^+ : PSh(C) \to SepPSh(C)$ is not left adjoint to the inclusion $\iota : SepPSh(C) \hookrightarrow PSh(C)$ of the full subcategory of separated presheaves. If it were, it would be a [[reflector]] and therefore satisfy $(-)^+ \circ \iota \cong Id$. But this is false, since the plus construction applied to separated presheaves yields their sheafification. See [this MathOverflow question](http://mathoverflow.net/questions/49486/the-single-plus-construction-is-not-the-left-adjoint-of-the-inclusion-of-separat) for details.


## Internal description

The plus construction can be described in the [[internal language]] of the presheaf topos $PSh(C)$. For a presheaf $A$, seen as a set from the internal point of view, the separated presheaf $A^+$ is given by the internal expression
$$ A^+ = \{ K \subseteq A \,|\, j(K\,\text{ is a singleton}) \}/{\sim}, $$
where $\sim$ is the equivalence relation given by $K \sim L$ if and only if $j(K = L)$ and $j$ is the [[Lawvere-Tierney topology]] describing the subtopos $Sh(C) \hookrightarrow PSh(C)$.

With this internal description, the verification of the properties of the plus construction becomes an exercise with sets and subsets (instead of colimits).


## Related concepts

* [[sheafification]]

* [[(∞,1)-sheafification]] / [[∞-stackification]] 



## References 

Related entries: [[sheafification]]

A standard textbook reference in the context of 1-[[topos theory]] is:

* [[Peter Johnstone]], _[[Sketches of an elephant]] - a topos theory compendium_, Section C.2.2, proof of proposition 2.2.6, p.551

Remarks on the plus-construction in [[(infinity,1)-topos theory]] is in section 6.5.3 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}

Plus construction for presheaves in values in abelian categories is also called Heller-Rowe construction:

* Alex Heller, K. A. Rowe, _On the category of sheaves_
Amer. J. Math. 84 1962 205&#8211;216, [MR144341](http://www.ams.org/mathscinet-getitem?mr=144341), [doi](http://dx.doi.org/10.2307/2372759)
[[!redirects plus-construction on presheaves]]
[[!redirects plus constructions on presheaves]]
[[!redirects plus-constructions on presheaves]]
