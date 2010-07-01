# Contents
* the following line creates the automatic table of contents
{:toc}

## Idea

A $C^*$-system is a [[C-star-algebra]] together with a group of automorphisms. In [[quantum mechanics]] as well as in [[AQFT]] the observables of the theory are [[self-adjoint operator]]s of (a net of) [[C-star-algebra]]s, in this context the [[gauge group]] of the theory is the maximal group of [[unitary operators]] that leave all observables invariant, the algebra and the gauge group form a $C^*-$system.


## Definition

+-- {: .un_defn}
###### Definition
A **$C^*-$system** $(\mathcal{A}, \alpha_G)$ consists of a $C^*-$algebra $\mathcal{A}$, a locally compact group $G$ and a continuous morphism $\alpha$ of $G$ into the group $aut(\mathcal{A})$ of $*$-automorphisms of $\mathcal{A}$ equipped with the topology of pointwise convergence.
=--

If the algebra is a $*$-[[star-algebra|algebra]] only, then some authors call it a __$*$-system__. 

Sometimes the continuity condition is dropped entirely or replaced by some weaker assumption, therefore one should always check what -- if any -- continuity assumption an author makes.

+-- {: .un_defn}
###### Definition
The **fixed point algebra** of a $C^*-$system  $(\mathcal{A}, \alpha_G)$ is $\{ A \in \mathcal{A}: a_g A = A \; \forall \; g \in G  \}$. If the fixed point algebra is trivial then $\alpha_G$ **acts ergodically**. 
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

The set of invariant states is convex, weak $*-$ closed and -compact.

=--

## References ##

* Hellmut Baumg&#228;rtel, Manfred Wollenberg: _Causal nets of operator algebras._ Berlin: Akademie Verlag 1992 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0749.46038&format=complete))
[[!redirects C-star-system]]
[[!redirects C-star-systems]]
[[!redirects C-star system]]
[[!redirects C-star systems]]
[[!redirects invariant state]]
