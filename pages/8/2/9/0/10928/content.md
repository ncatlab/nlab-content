[[!redirects C-star-system]]
[[!redirects C-star-system]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

A __$C^*$-dynamical system__, or only $C^*$-system
is a [[C-star-algebra]] together with an
[[action]] of a [[group]] of [[automorphisms]]. In [[quantum mechanics]] as well as in [[AQFT]] the [[observables]] of the theory are [[self-adjoint operator]]s of (a [[local net]] of) [[C-star-algebra]]s, in this context the [[global gauge group]] of the theory is the maximal group of [[unitary operators]] that leave all observables invariant, the algebra and the gauge group form a $C^*$-system.


## Definition

+-- {: .un_defn}
###### Definition

A **$C^*$-system** $(\mathcal{A}, \alpha_G)$ consists of a $C^*$-algebra $\mathcal{A}$, a [[locally compact space|locally compact]] group $G$ and a [[continuous map|continuous]] [[homomorphism]] $\alpha$ of $G$ into the [[group]] $aut(\mathcal{A})$ of $*$-[[automorphisms]] of $\mathcal{A}$ equipped with the [[topology]] of pointwise convergence.

=--

If the algebra is a $*$-[[star-algebra|algebra]] only, then some authors call it a __$*$-system__. 

Sometimes the continuity condition is dropped entirely or replaced by some weaker assumption, therefore one should always check what -- if any -- continuity assumption an author makes.

+-- {: .un_defn}
###### Definition

The **fixed point algebra** of a $C^*$-system  $(\mathcal{A}, \alpha_G)$ is $\{ A \in \mathcal{A}: a_g A = A \; \forall \; g \in G  \}$. If the fixed point algebra is trivial then $\alpha_G$ **acts ergodically**. 

=--

+-- {: .un_defn}
###### Definition

A [[state]] $\rho$ of the algebra $\mathcal{A}$ is an **invariant state** if 
$$
\rho (A) = \rho(\alpha_g A) \; \forall A \in \mathcal{A}, \; \forall g \in G.
$$

=--


## Properties ##

+-- {: .un_lemma }
###### Lemma

The set of invariant states is convex, weak-$*$ closed and weak-$*$ compact.
(see [[operator topology]]).

=--


## References ##

* [[Hellmut Baumgärtel]], Manfred Wollenberg: _Causal nets of operator algebras._ Berlin: Akademie Verlag 1992 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0749.46038&format=complete))

* chapter 6 in Gerd Petersen, _Pullback and pushout constructions in $C^\ast$-algebra theory_, J. Funct. Analysis __167__, 243--344 (1999) [pdf](http://www.math.ru.nl/~mueger/ped2.pdf)

category: operator algebras
[[!redirects C-star-system]]
[[!redirects C-star-systems]]
[[!redirects C-star system]]
[[!redirects C-star systems]]
[[!redirects C-star dynamical systems]]
[[!redirects invariant state]]
