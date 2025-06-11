
> This entry is about _the_ [[small category]] named after [[Graeme Segal]]. Not to be confused with the model in [[higher category theory]] called _[[Segal categories]]_.

# Contents
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

**Segal's category**, denoted by $\Gamma$, is the category opposite to the [[skeleton]] of the [[category]] $FinSet^{*/}$ of [[pointed object|pointed]] [[finite sets]]: 
$$\Gamma^{op} \simeq FinSet^{*/}.$$

Equivalently, $\Gamma$ is the category [[opposite category|opposite]] to the category $FinSetPart$ of finite sets and partially defined maps.  Objects are finite sets.  Morphisms $A\to B$ are pairs $(A',f)$, where $A'\subset A$ and $f\colon A'\to B$ is a map of sets.  Identity morphisms are specified by $id_A=(A,id_A)$.  Composition is defined as follows:
$$(A',f)\colon A\to B,\qquad (B',g)\colon B\to C,\qquad(B',g)\circ(A',f)=(A'\cap f^{-1}B',g\circ f|_{A'\cap f^{-1}B'}).$$

Equivalently ([Segal, Definition 1.1](#Segal)), $\Gamma$ admits the following covariant description.  Objects are finite sets.  Morphisms $A\to B$ are maps $f\colon A\to P(B)$ such that $a_1\ne a_2$ implies $f(a_1)\cap f(a_2)=\emptyset$.  Identity morphisms are specified by $id_A(a)=\{a\}$.  Composition is defined as follows:
$$f\colon A\to P(B),\qquad g\colon B\to P(C),\qquad (g\circ f)(a)=\bigcup_{b\in f(a)}g(b).$$

=--

+-- {: .num_remark}
###### Remark

The category $\Gamma$ is related to [[(infinity,1)-operads]] in a way similar to how the [[simplex category]] (non-empty and _linearly ordered_  finite sets) is related to [[(∞,1)-categories]].

=--

+-- {: .num_remark}
###### Remark

The categories $FinSetPart$ and $FinSet_*$ are [[equivalence of categories|equivalent]] via the following pair of functors.
The functor
$$FinSetPart\to FinSet_*$$
sends
$$A\mapsto A\sqcup\{*\},\qquad ((A',f)\colon A\to B)\mapsto(g\colon A\sqcup\{*\}\to B\sqcup\{*\}),\qquad g|_{A'}=f,\qquad g|_{\bar A'}(x)=*.$$
The functor
$$FinSet_* \to FinSetPart$$
sends
$$A\mapsto A\setminus\{*\},\qquad (g\colon A\to B)\mapsto(g^{-1}(B\setminus\{*\}),g|_{A\setminus\{*\}}).$$

=--

## Comparison to the simplex category

Recall the [[simplex category]] $\Delta$, whose objects are finite inhabited totally ordered sets and morphisms are order-preserving maps of sets.
We set
$$[m]=\{0\lt\cdots\lt m\}.$$

Interpreting a simplex $A\in\Delta$ as a (posetal) category, a __spine edge__ in $A$ is a morphism in $A$ that is not an identity morphism and cannot be decomposed as the composition of two nonidentity morphisms.
That is to say, in a standard simplex $[m]$, a spine edge is a pair of the form $(i-1,i)$, $0\lt i\le m$, which encodes the morphism $(i-1)\to i$.

The canonical functor
$$\iota\colon\Delta\to\Gamma$$
sends a simplex to its set of spine edges:
$$[m]=\{0\lt1\lt2\lt\cdots\lt m\}\mapsto \{(0,1),(1,2),\ldots,(m-1,m)\}=\iota[m].$$

To define $\iota$ on morphisms, observe that a morphism of simplices $f\colon[m]\to[n]$ can be interpreted as a functor between posetal categories.  This functor sends a spine edge in $[m]$ to the composition of a set of spine edges in $[n]$.  More specifically, $f$ sends a spine edge $i-1\to i$ to the composition of spine edges 
$$f(i-1)\to f(i-1)+1\to \cdots \to f(i)-1\to f(i).$$

Using Segal's covariant description of $\Gamma$, we can define a morphism $\iota(f)\colon\iota[m]\to\iota[n]$ by sending a spine edge $e$ in $[m]$ to the set of spine edges in $[n]$ whose composition yields the image of $e$ under the functor $f\colon[m]\to [n]$.

In terms of the category FinSetPart, we can describe $\iota(f)$ as a partial map of finite sets $\iota[n]\to\iota[m]$ that sends $(j-1,j)\in\iota[n]$ to the unique pair $(i-1,i)\in\iota[m]$ such that $f(i-1)\lt j\le f(i)$.  (If no such pair exists, then $\iota(f)$ is undefined on $(j-1,j)$.)

## Monoidal structure

The category $\Gamma$ is a [[symmetric monoidal category]], induced from the [[cartesian monoidal structure]] on the category [[Set]]:
$$A_1\otimes A_2=A_1\times A_2,\qquad (A'_1,f_1)\otimes(A'_2,f_2)=(A'_1\times A'_2,f_1\times f_2).$$
The reader should keep in mind that $\times$ is _not_ a [[product]] in the category FinSetPart, but only in [[Set]].

In terms of the category $FinSet_*$, the monoidal structure is given by the [[smash product]] of [[pointed sets]]:
$$A_1\otimes A_2=(A_1\times A_2)/(\{*\}\times A_2\cup A_1\times \{*\}).$$

## Applications

A __Γ-object__ in a [[cartesian monoidal category]] (more generally, [[cartesian monoidal (∞,1)-category]]) $C$
is a functor
$$X\colon \Gamma^{op} \to C$$
(equivalently, a functor $FinSetPart \to C$)
such that for all $A,B\in FinSetPart$ the map
$$X_{A\sqcup B}\to X_A\times X_B$$
induced by the morphisms
$$(A,id_A)\colon A\sqcup B\to A, \qquad (B,id_B)\colon A\sqcup B\to B$$
is an equivalence, as is the map $X_\emptyset\to1$.
Here $A\sqcup B$ denotes the [[coproduct]] in the category [[Set]] (i.e., [[disjoint union]]).  It does not denote the coproduct in the category FinSetPart.

Γ-objects in $C$ encode $\mathrm{E}_\infty$-monoids in $C$, i.e., homotopy coherent commutative monoids.
See the article [[Γ-space]] for more information.

## Related concepts

* [[category of operators]]

* [[Gamma space]]


## References

Original reference:

* {#Segal} [[Graeme Segal]], _Categories and cohomology theories_, Topology 13, 293–312, 1974 (<a href="https://doi.org/10.1016/0040-9383(74)90022-6">doi:10.1016/0040-9383(74)90022-6</a>, [pdf](http://ncatlab.org/nlab/files/SegalCategoriesAndCohomologyTheories.pdf))

For instance notation 2.0.0.2 in 

* [[Jacob Lurie]], _[[Higher Algebra]]_
  {#Lurie}


[[!redirects Segal's category]]
[[!redirects Segal's category]]
[[!redirects Segal's category]]
[[!redirects Segal's category]]
[[!redirects Segal\'s category]]
[[!redirects Gamma category]]
[[!redirects Gamma-category]]
[[!redirects Segal Gamma-category]]