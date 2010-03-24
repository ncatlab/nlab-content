#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _Eilenberg--Mac Lane object_ in an [[(∞,1)-topos]] or [[stable (∞,1)-category]] generalizes the notion of [[Eilenberg?Mac Lane space]] from the [[(∞,1)-topos]] [[Top]] of [[topological space]]s or the [[stable (∞,1)-category]] of [[spectrum|spectra]]:

it is an object $\mathbf{B}^n A$ obtained from an abelian [[group object]] $A$ by [[delooping]] that $n$ times.


An object that is both $n$-[[truncated]] as well as $n$-connected.

## Definition and properties

+-- {: .un_defn}
###### Definition

Let $\mathbf{H}$ be an [[(∞,1)-topos]] [[pointed object]].

For $n \in \mathbb{N}$ an **Eilenberg-MacLane object** $X$ of degree $n$ 

* a [[pointed object]] $* \to X \in \mathbf{H}$ 

* which is both $n$-[[connected]] as well as $n$-truncated.

=--

This appears as [[Higher Topos Theory|HTT, def. 7.2.2.1]]

The next proposition asserts that Eilenberg-MacLane objects defined this way are shifted [[group object in an (∞,1)-category|(∞,1)-categorical group objects]]:

+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ an [[(∞,1)-topos]], $\mathbf{H}_*$ its [[(∞,1)-category]] of [[pointed object]]s, $Disc(\mathbf{H})$ the full sub-[[(∞,1)-category]] on discrete objects (0-[[truncated]] objects) and $n \in \mathbb{N}$, write

$$
  \pi_n : \mathbf{H}_* \to Disc(\mathbf{H}_*)
$$

for the [[(∞,1)-functor]] that assigns the $n$-th [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]].

* For $n = 0$ this establishes an equivalence between the full subcategory on degree 0 Eilenberg-MacLane objects and [[pointed object]]s of $Disc(\mathbf{H})$.

* For $n = 1$ this establishes an equivalence between the full subcategory on degree 1 Eilenberg-MacLane objects and the category of [[group object in an (∞,1)-category|group objects]] in $Disc(\mathbf{H})$.

* For $n \geq 2$ this establishes an equivalence between the full subcategory on degree $n$ Eilenberg-MacLane objects and the category of commutative [[group object in an (∞,1)-category|group objects]] in $Disc(\mathbf{H})$.


=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 7.2.2.12]].

=--


+-- {: .un_def}
###### Definition

For $\mathbf{H}$ an [[(∞,1)-topos]] and $n \in \mathbb{N}$ write $K(-,n)$ for [[generalized the|the]] homotopy inverse to the equivalence induced by $\pi_n$ by the above proposition. For $A \in Disc(\mathbf{H})$ an (abelian) group object we say that

$$
  K(A,n) \in \mathbf{H}
$$

is the degree $n$-Eilenberg-MacLane object of $A$.

=--

+-- {: .un_prop}
###### Proposition

We have that 

$$
  K(A,n) \simeq \mathbf{B}^n A
$$

is [[generalized the|the]] $n$-fold [[delooping]] of the discrete group object $A$.

=--

+-- {: .proof}
###### Proof

> check

The [[homotopy groups in an (∞,1)-topos|categorical homotopy groups]] are defined in terms of the canonical [[power]]ing of $\mathbf{H}$ over [[∞Grpd]]

$$
  (-)^{(-)} : \infty Grpd \times \mathbf{H} \to \mathbf{H}
  \,.
$$

For fixed [[∞-groupoid]] $K$ this 

$$
  (-)^{K} : \mathbf{H} \to \mathbf{H}
  \,.
$$

preserves $(\infty,1)$-[[limit]]s and hence [[pullback]]s. It follows that the categorical homotopy groups of the [[loop space object]] $\Omega K(A,n)$ are those of $K(A,n)$, shifted down by one degree. 

By the above proposition on the equivalence between Eilenberg-MacLane objects and group objects, this identifies $\Omega K(A,n) \simeq K(A,n-1)$.

=--



## Examples

### In $Top$

In the archetypical [[(∞,1)-topos]] [[Top]]$\simeq$ [[∞Grpd]] the notion of Eilenberg-MacLane object reduces to the traditional notion of [[Eilenberg-MacLane space]].

### In $\infty$-stack $(\infty,1)$-toposes

Recall that an [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaf]]/[[∞-stack]] [[(∞,1)-topos]] $\mathbf{H} = Sh_{(\infty,1)}(C)$ may be [[presentable (∞,1)-category|presented]] by the [[model structure on simplicial sheaves]] on $C$.

In terms of this model the Eilenberg-Mac Lane objects $K(A,n) \in \mathbf{H}$ (for abelian $A$) are the **Eilenberg-MacLane [[sheaf|sheaves]]** of [[abelian sheaf cohomology]] theory.

Under the [[Dold?Kan correspondence]] 

$$
  N : sAb \stackrel{\leftarrow}{\to} Ch_+ : \Gamma
$$

[[chain complex]]es $A[n]$ of abelian groups concentrated in degree $n$ map into [[simplicial set]]s 

$$
  K(A,n) := \Gamma(A[n])
$$

and these to the corresponding constant simplicial sheaves on the [[site]] $C$, that we denote by the same symbol, for convenience.

Under the equivalence

$$
  \mathbf{H} = Sh_{(\infty,1)}(C) \simeq (sSh(C)_{loc})^\circ
$$

of $\mathbf{H}$ with the [[Kan complex]]-enriched full subcategory of $sSh(C)$ on fibrant cofibrant objects, this identifies the fibrant reeplacement -- the [[∞-stackification]] -- of $\Gamma(A[n])$ with the Eilenberg-MacLane object in $\mathbf{H}$.

## Cohomology


The notion of [[cohomology]] in the [[(∞,1)-topos]] $\mathbf{H}$ with coefficients in an object $\mathcal{A} \in \mathbf{H}$ is often taken to be restricted to the case where $\mathcal{A}$ is an Eilenberg-MacLane object.

For $A \in Disc(\mathbf{A})$ an abelian group object, and $n \in \mathbb{N}$, the degree $n$-cohomology of an object $ X \in \mathbf{H}$ is the cohomology with coefficients in $K(A,n)$:

$$
  H^n(X, A) := H(X, K(A,n)) := \pi_0 \mathbf{H}(X, K(A,n))
  \,.
$$

## References

The general discussion of Eilenberg-MacLane objects is in section 7.2.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

For a discussion of Eilenberg-MacLane objects in the context of the [[model structure on simplicial presheaves]] see top of page 4 of

* Jardine, _Fields Lectures: Simplicial Presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))


[[!redirects Eilenberg-MacLane object]]
[[!redirects Eilenberg?MacLane object]]
[[!redirects Eilenberg--MacLane object]]
[[!redirects Eilenberg-Mac Lane object]]
[[!redirects Eilenberg?Mac Lane object]]
[[!redirects Eilenberg--Mac Lane object]]
[[!redirects Eilenberg-MacLane objects]]
[[!redirects Eilenberg?MacLane objects]]
[[!redirects Eilenberg--MacLane objects]]
[[!redirects Eilenberg-Mac Lane objects]]
[[!redirects Eilenberg?Mac Lane objects]]
[[!redirects Eilenberg--Mac Lane objects]]