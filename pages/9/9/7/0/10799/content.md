
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _ring of adeles_ $\mathbb{A}_k$ of any [[global field]] $k$ -- in particular of the [[rational numbers]] $\mathbb{Q}$ -- is the [[restricted product]] of all [[formal completions]] $k_v$ of $k$ at all its [[places]] $v$, where the restriction is such that only a [[finite number]] of components have [[norm]] greater than 1. (This has a useful geometric interpretation and motivation by the [[function field analogy]], more on which [below](#FunctionFieldAnalogy)).

In particular the ring of adeles of the rational numbers is equivalently the [[rationalization]] of the [[product]] of all [[p-adic integers]] (including the "prime at infinity").

In classical [[algebraic number theory]] one embeds a [[number field]] into the [[cartesian product]] of its [[completion of a ring|completions]] at its [[archimedean absolute values]]. This embedding is very useful in the [[proofs]] of several fundamental [[theorems]]. For example, the [[algebraic integers]] in the number field embed discretely and co-compactly into this [[cartesian product]], i.e., as a [[lattice in a vector space|lattice]], and this opens the way for example to the concrete realization of the [[group of units]] (modulo [[torsion subgroup|torsion]]) as a [[lattice]], and also to the technique of [[Fourier analysis]] where Poisson summation applied to the lattice has classical implications for [[theta functions]] and [[zeta functions]]. 

It was noticed by [[Claude Chevalley]] and [[André Weil]] that the situation is made even better if the [[number field]] itself is embedded in the cartesian product of its [[formal completions]] at all of its [[absolute values]]. With a few additional restrictions, these objects are known as the _adeles_, and the [[group of units|units]] of this ring are called the _[[ideles]]_. Under these restrictions, the given number field embeds discretely and cocompactly into the adeles, i.e., behaves as a lattice where it is again possible to apply Poisson summation. 

When considering the adeles and ideles, it is their [[topology]] as much as their algebraic structure that is of interest. Many important results in [[number theory]] translate into simple statements about the topologies of the adeles and ideles. For example, the finiteness of the [[ideal class group]] and the [[Dirichlet unit theorem]] are equivalent to a certain quotient of the ideles being compact and discrete.

([Weston, p. 1](#Weston))


## Definition

The concept of a _ring of adeles_ (older synonym: ring of valuation vectors) makes sense for any [[global field]], hence for any finite-dimensional [[field extension]] of either the [[rational numbers]] or of a [[function field]] over a [[finite field]]. The ring of adeles of the [[rational numbers]] themselves is the classical case which we discuss first in 

* [For the rational numbers](#ForTheRationalNumbers)

Then we consider the definition more generally

* [For a number field](#ForAnyNumberField)

and finally in full generality 

* [For a global field]().

### For the rational numbers
 {#ForTheRationalNumbers}


We start off very simply with the algebraic description of the adele ring over the [[rational numbers]]. 

+-- {: .num_defn #RingOfAdeles}
###### Definition

The ring of _integral adeles_ $\mathbb{A}_{\mathbb{Z}}$ is the [[product]]
of the [[profinite completion of the integers]] $\widehat{\mathbb{Z}}$, with the [[real numbers]]

$$
  \mathbb{A}_{\mathbb{Z}}
  \coloneqq
  \mathbb{R} \times \widehat{\mathbb{Z}}
  \,.
$$

The _ring of adeles_ $\mathbb{A}_{\mathbb{Q}}$ (or just $\mathbb{A}$, for short) itself is the [[rationalization]] of the ring of integral adeles, hence its [[tensor product]] with the [[rational numbers]] 

$$
  \mathbb{A}_\mathbb{Q} 
    \coloneqq 
  \mathbb{Q} 
    \otimes_\mathbb{Z} 
  \mathbb{A}_\mathbb{Z}
  \,.
$$

=--

This definition has various equivalent reformulations which are often useful.

+-- {: .num_remark #ProfiniteIntegersAsProductOverpAdics}
###### Remark

By [this proposition](profinite+completion+of+the+integers#AsProductOverAlsoPAdicIntegers) we have that the [[profinite completion of the integers]] is equivalently the [[product]] of all [[p-adic integers]] as $p$ ranges over all [[prime numbers]] 

$$
  \hat \mathbb{Z} \simeq \underset{p\;prime}{\prod} \mathbb{Z}_p
$$ 

Using this in def. \ref{RingOfAdeles} says that the ring of integral adeles is the product

$$
  \mathbb{A}_{\mathbb{Z}} 
    \simeq 
   \mathbb{R} \times
  \underset{p\;prime}{\prod} \mathbb{Z}_p
  \,.
$$


=--

From this one obtains the following equivalent characterization:

+-- {: .num_prop #RationalRingOfAdelesAsRestrictedProduct}
###### Proposition

The ring of adeles $\mathbb{A}$, def. \ref{RingOfAdeles}, is equivalently the [[restricted product]] $\prod^\prime$ of the [[p-adic rational numbers]], the restriction being along the inclusion $\mathbb{Z}_p \to \mathbb{Q}_p$:

$$
  \mathbb{A}_{\mathbb{Q}} 
    =
  \mathbb{R} \times \underset{p \; prime}{\prod^\prime} \mathbb{Q}_p
$$

=--

+-- {: .proof}
###### Proof

By remark \ref{ProfiniteIntegersAsProductOverpAdics} the 
[[tensor product]] to be computed is equivalently

$$
  \mathbb{A}_{\mathbb{Q}}
  \simeq
  \mathbb{Q}\otimes_{\mathbb{Z}}
   \left(
     \mathbb{R} \times
    \underset{p \; prime}{\prod} \mathbb{Z}_p
   \right)
  \,.
$$

Now notice that a [[natural number]] $n$ is a [[group of units|unit]] in $\mathbb{Z}_p$ if $p$ is not a [[prime factor]] of $n$. 
Therefore for $(a_p) \in \underset{p}{\prod} \mathbb{Z}_p$ and $\frac{c}{d} \in \mathbb{Q}$, then for each of the [[finite number]] of [[prime factors]] $p$ of $d$ the tensor product
element $\frac{c}{d} \otimes_{\mathbb{Z}} a_p \in \mathbb{Q}_p$ contains a non-vanishing negative power of $p$ and is hence not in $\mathbb{Z}_p$, whereas for all $p$ that do not appear as prime factors in $d$ it is.

=--



Finally notice:

+-- {: .num_remark #AsProductOverPlaces}
###### Remark

The [[prime numbers]] correspond to the non-archimedean [[places]] of $\mathbb{Z}$, and under this identification there is one more real [[place at infinity]], "$p = \infty$", the [[completion of a ring|completion]] of $\mathbb{Q}$ at which is the real numbers $\mathbb{R}$, which one may therefore write $\mathbb{R} = \mathbb{Q}_\infty$. Using this the characterization of the ring of adeles from prop. \ref{RationalRingOfAdelesAsRestrictedProduct} is equivalently the [[restricted product]] over all real places of the [[formal completion]] of $\mathbb{Q}$ at this place

$$
  \mathbb{A}_{\mathbb{Q}} 
    \simeq 
  \underset{p \in Places(\mathbb{Z})}{\prod^{\prime}} \mathbb{Q}_p
  \,.
$$

Considering this [[restricted product]] not just in bare [[commutative rings]] but in [[topological rings]] yields the right structure of a topological ring on $\mathbb{A}_{\mathbb{Q}}$. This is the content of the following proposition. 

=-- 

+-- {: .num_prop} 
###### Proposition 
$\mathbb{A}_\mathbb{Q}$ is a [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] commutative ring. In particular, it is complete with respect to its [[uniform space]] structure. 
=-- 

+-- {: .proof} 
###### Proof 
The restricted product is a filtered colimit of a system of *open* inclusions between locally compact Hausdorff rings, and is therefore itself locally compact Hausdorff. If $x_\alpha$ is a Cauchy net, then for all sufficiently large $\alpha, \beta$ the differences $x_\alpha - x_\beta$ lie in a compact neighborhood of the identity. Holding $\beta$ fixed, the limit $\lim_\alpha x_\alpha - x_\beta$ exists by compactness; if $x$ is this limit, then $x + x_\beta$ is the limit of the Cauchy net. 
=-- 

If one omits the factor of $\mathbb{R} = \mathbb{Q}_\infty$, then one speaks of the _ring of finite adeles_.

$$
  \mathbb{A}_{\mathbb{Q}}^f \coloneqq \underset{p \; prime}{\prod^\prime} \mathbb{Q}_p
  \,.
$$


All of this generalizes to any [[number field]] $k$. 



### For a number field
 {#ForAnyNumberField}

Let 

* $k$ be a [[number field]];

* $\mathcal{O} = \mathcal{O}_k$ the [[ring of integers|ring of]] [[algebraic integers]] in $k$: 

* $P$ be its [[set]] of [[places]] (equivalence classes of [[absolute values]] on $\mathcal{O}$); 

* $S\subset P$ be the set of [[archimedean valuation|archimedean]] places;

* $k_v$ the [[formal completion]] of $k$ at $v\in P$. 

Notice that

* for $v \in S$ then $k_v$ is isomorphic to one of the [[local fields]] $\mathbb{R}$ or $\mathbb{C}$;

* for $v \notin S$ then $k_v$ is a [[local field]] with an open compact subring $\mathcal{O}_v$ consisting of elements of [[norm]] $1$ or less. 


+-- {: .num_defn} 
###### Definition 

For $k$ a [[number field]], the ring of _integral adeles_ $\mathbb{A}_{\mathcal{O}}$ is the [[product]] of the [[profinite completion]] $\widehat{\mathcal{O}}$ with all the archimedean completions, 

$$
  \mathbb{A}_\mathcal{O} 
   \coloneqq 
  \widehat{\mathcal{O}} \times \prod_{v \in S} k_v 
  \,,
$$ 

and the _ring of adeles_ over $k$ is the [[tensor product]] $\mathbb{A}_k \coloneqq k \otimes_\mathcal{O} \mathbb{A}_\mathcal{O}$. 

=-- 

It may be shown that 

$$\widehat{\mathcal{O}} \cong \prod_{v \notin S} \mathcal{O}_v$$ 

where each non-archimedean place $v$ may be identified with a prime ideal $p$. Now, if we view $k$ as the localization of $\mathcal{O}$ obtained by inverting all nonzero elements $x \in \mathcal{O}$, then $k$ may be written as a filtered colimit of a system of inclusions of localizations:  

$$k \cong colim_x \; \mathcal{O}[x^{-1}].$$ 

Componentwise, we may calculate 

$$\array{
\mathcal{O}[x^{-1}] \otimes_\mathcal{O} \mathcal{O}_p & = & k_p & \text{if}\; x \in p \\ 
 & = & \mathcal{O}_p & \text{if}\; x \notin p
}$$ 

and so 

$$\array{
\mathcal{O}[x^{-1}] \otimes_\mathcal{O} \widehat{\mathcal{O}} & \cong & \mathcal{O}[x^{-1}] \otimes_\mathcal{O} \prod_{p \in P \backslash\; S} \mathcal{O}_p \\ 
 & \cong & (\prod_{x \in p} k_p) \times (\prod_{x \notin p} \mathcal{O}_p)
}$$ 

Putting these facts together, 

$$k \otimes_\mathcal{O} \widehat{\mathcal{O}} \cong colim_x\; (\prod_{x \in p} k_p) \times (\prod_{x \notin p} \mathcal{O}_p)$$ 

whence 

$$\begin{array}{lll} 
k \otimes_\mathcal{O} \mathbb{A}_\mathcal{O} & \cong & k \otimes_\mathcal{O} \left(\prod_{v \in S} k_v \times \widehat{\mathcal{O}}\right) \\ 
 & \cong & colim_x \; \prod_{v \in S} k_v \times (\prod_{p: x \in p} k_p) \times (\prod_{p: x \notin p} \mathcal{O}_p)
\end{array}$$ 

where each component of the filtered diagram is locally compact (a product of finitely many locally compact and infinitely many compact spaces) in the [[product topology]]. Taking the filtered colimit in $Top$ over the resulting diagram of open inclusions, the result is again a locally compact ring. In this way the ring of adeles $\mathbb{A}_k$ is topologized. 

+-- {: .num_remark} 
###### Remark 
The topology on the adele ring $\mathbb{A}_k$ is strictly finer than the subspace topology inherited from its natural inclusion into $\prod_{v \in P} k_v$ with the product topology. For example, $(\prod_{v \in S} k_v) \times \prod_{p \in P \backslash\; S} \mathcal{O}_p$ is open in the ring of adeles, but not in $\prod_{v \in P} k_v$. 
=-- 

+-- {: .num_defn }
###### Definition

The [[group of units]] of the ring of adeles $\mathbb{A}_k$ is called the group of [[ideles]], denoted $\mathbb{I}_k$.

=-- 

Under the subspace topology inherited from $\mathbb{A}_k$, there is no reason for inversion $(-)^{-1}: \mathbb{I}_k \to \mathbb{I}_k$ to be continuous (and in fact it isn't!), so $\mathbb{I}_k$ isn't a topological group when topologized this way. However, we can endow $\mathbb{I}_k$ with the subspace topology given by the embedding $\mathbb{I}_k \to \mathbb{A}_k \times \mathbb{A}_k: x \mapsto (x, x^{-1})$; topologized this way, we get a locally compact topological group. _This is the topology on the ideles._ 

Alternatively, for each finite $T \subset P$ containing the set of archimedean places $S$, we have a locally compact group 

$$\mathbb{I}_{k, T} = (\prod_{v \in T} k_v^\times) \times (\prod_{v \notin T} \mathcal{O}_v^\times)$$ 

(noting that each unit group $\mathcal{O}_v^\times$ is compact), and the idele group can be described as the colimit over a filtered system of open inclusions 

$$\mathbb{I}_k = colim_T \; \mathbb{I}_{k, T}$$ 

and indeed the idele topology coincides with the filtered colimit topology. 

### For a global field
 {#ForAGlobalField}

Fully generally, let $k$ be a [[global field]]. Write $P$ for its [[set]] of [[places]] and $k_v$ for its [[formal completion]] at $v \in P$.

+-- {: .num_defn #AsRestrictedProduct} 
###### Definition

The _ring of adeles_ of a [[global field]] $k$ is the [[restricted product]]

$$
  \mathbb{A}_k \coloneqq \underset{v \in P}{\prod} k_v
$$

where the restriction is to elements $(x_v)_{v\in P}$ of the actual [[product]] whose components have [[norm]] at most unity -- ${\vert x_v\vert} \leq 1$, except for at most a [[finite number]] of $v$. 

This is topologized in the same way as discussed [above](#ForAnyNumberField).

=--

Reviews includes ([Mathew 10](#Mathew10)). 

In the function field case, where $k$ is a finite extension of $\mathbb{F}_p(T)$, the analogous ring of integers $\mathcal{O}(k)$ is the [[integral closure]] in $k$ of the subring $\mathbb{F}_p[T] \hookrightarrow \mathbb{F}_p(T)$. And analogously, the ring of integer adeles $\mathbb{A}_{\mathcal{O}(k)}$ may be defined to be the product of all the completions of $\mathcal{O}(k)$ over all the places of $k$. This is a compact ring. The restricted direct product above map may then, in parallel with the number field case described above, be described as a tensor product 

$$\mathbb{A}_k = k \otimes_{\mathcal{O}(k)} \mathbb{A}_{\mathcal{O}(k)}$$ 

where the right side is again interpreted as a colimit in the category of topological rings of a diagram consisting of compact topological rings and open inclusions between them. 


## Properties

### Basic results 

+-- {: .num_prop} 
###### Proposition 
Under the natural inclusion $i: k \to \mathbb{A}_k$, the subspace topology on $k$ is discrete, and the quotient topology on $\mathbb{A}_k/k$ is compact. 
=-- 

As an additive topological group, there is a natural pairing on $\mathbb{A}_k$: 

$$\langle -, - \rangle: \mathbb{A}_k \times \mathbb{A}_k \to \mathbb{R}/\mathbb{Z} \cong S^1.$$ 

If $x = (x_v)_{v \in P}$ and $y = (y_v)_{v \in P}$, then 

$$\langle x, y \rangle \coloneqq \prod_v \langle x_v, y_v \rangle_v$$ 

where each local pairing $\langle -, - \rangle_v$ is defined to be a composite of the form 

$$k_v \times k_v \stackrel{mult}{\to} k_v \stackrel{Tr}{\to} \mathbf{Q}_v \stackrel{\chi_v}{\to} \mathbb{R}/\mathbb{Z} \cong S^1,$$ 

noting that a place $v$ of $k$ restricts to a place on $\mathbb{Q}$. 

+-- {: .num_remarks} 
###### Remarks 
* The trace map $Tr$ on the finite algebraic extension $k_v/\mathbf{Q}_v$ is of course defined by $Tr(x) = \sum_\sigma \sigma(x)$ where $\sigma$ ranges over all embeddings of $k_v$ into the algebraic closure of $\mathbb{Q}_v$. 

* When $v$ is the archimedean place on $\mathbb{Q}$, we will take the map $\chi_v: \mathbb{R} \to \mathbb{R}/\mathbb{Z}$ to be not the quotient map, but its *additive inverse*. For non-archimedean places $v = p$, the character $\chi_p$ is the composite $\mathbf{Q}_p \to \mathbb{Z}(p^\infty) \hookrightarrow \mathbb{R}/\mathbb{Z}$ as defined [here](http://ncatlab.org/nlab/show/p-adic+number#duality). 

* For each $x, y \in \mathbb{A}_k$, observe that $\langle x_v, y_v \rangle_v = 1 \in S^1$ for all but finitely many places $v$, since $x_v, y_v \in \mathcal{O}_v$ for all but finitely many places. Hence $\langle x, y\rangle$ is well-defined. 
=-- 

+-- {: .num_prop} 
###### Proposition 
The additive group $\mathbb{A}_k$ is [[Pontrjagin duality|Pontrjagin self-dual]] in the sense that the map $\phi: \mathbb{A}_k \to \mathbb{A}_k^\wedge$ induced from the pairing $\langle-, -\rangle$ is an isomorphism onto the character group. 
=-- 

Moreover, define $\pi: \mathbb{A}_k \to k^\wedge$ to be the composite 

$$\mathbb{A}_k \stackrel{\phi}{\to} \mathbb{A}_k^\wedge \stackrel{i^\wedge}{\to} k^\wedge.$$ 

+-- {: .num_prop} 
###### Proposition 
The map $\pi \circ i: k \to k^\wedge$ vanishes. The map $\mathbb{A}_k/k \to k^\wedge$ induced by $\pi: \mathbb{A}_k \to k^\wedge$ is an isomorphism of topological groups, so that $\mathbb{A}_k/k$ is Pontrjagin dual to $k$. 
=-- 

### Function field analogy
 {#FunctionFieldAnalogy}

Via the [[function field analogy]] one may understand any [[number field]] or [[function field]] $F$ as being the [[rational functions]] on an [[arithmetic curve]] $\Sigma$. Under this identification the  ring of adeles $\mathbb{A}_F$ of $F$ has the interpretation of being the ring of functions on all punctured [[formal disks]] around all points of $\Sigma$, such that only finitely many of them do not extend to the given point. ([Frenkel 05, section 3.2](#Frenkel05)). This is most manifest in terms of def. \ref{AsRestrictedProduct} above.

This means for instance that the [[general linear group]] $GL_n(\mathbb{A}_F)$ with [[coefficients]] in the ring of adeles has the interpretation as being the [[Cech cohomology|Cech cocycles]] for [[algebraic vector bundles]] of [[rank]] $n$ on an [[algebraic curve]] with respect to any [[cover]] of that curve by the complement of a finite number of points together with the [[formal disks]] around these points. (Notice that for $n = 1$ then $GL_1(\mathbb{A}_F)$ is the [[group of ideles]]). This is part of a standard construction of the [[moduli stack of bundles]] on algebraic curves, see at _[Moduli space of bundles and the Langlands correspondence](moduli+space+of+bundles#OverCurvesAndTheLanglandsCorrespondence)_.



[[!include function field analogy -- table]]


## Related concepts

* [[adelic string theory]]

* [[adelic integration]]

## References

* wikipedia: [adele ring](http://en.wikipedia.org/wiki/Adele_ring), [adelic algebraic group](http://en.wikipedia.org/wiki/Adelic_algebraic_group)

* D. Goldfeld, J. Hundley, chapter 1 of _Automorphic Representations and L-functions for the General Linear Group_, vol. 1, Cambridge University 
Press, 2011 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/text/gl1.pdf))

* {#Mathew10} [[Akhil Mathew]], _[The adele ring](http://amathew.wordpress.com/2010/05/21/the-adele-ring/)_, 2010 

* _Adeles_ [pdf](http://wiki.epfl.ch/gant/documents/lecture2-cib2011.pdf)

* Pete Clark, _Adeles and Ideles_ ([pdf](http://math.uga.edu/~pete/8410Chapter6.pdf))

* Erwin Dassen , _Adeles & Ideles_ ([pdf](http://www.math.leidenuniv.nl/~astolk/monday/notes/dassen-adeles-ideles.pdf))

* {#Weston} Tom Weston, _The idelic approach to number theory_ ([pdf](http://www.math.umass.edu/~weston/oldpapers/idele.pdf))

* [MO/96137/categorical-description-of-the-restricted-product-adeles](http://mathoverflow.net/questions/96137/categorical-description-of-the-restricted-product-adeles)
 
Discussion in the context of the [[function field analogy]] and the [[geometric Langlands correspondence]] is in


* {#Frenkel05} [[Edward Frenkel]], _Lectures on the Langlands Program and Conformal Field Theory_, in _Frontiers in number theory, physics, and geometry II_, Springer Berlin Heidelberg, 2007. 387-533. ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172))

[[!redirects rings of adeles]]

[[!redirects adele]]
[[!redirects adeles]]

[[!redirects adele ring]]
[[!redirects adele rings]]

[[!redirects integral adele]]
[[!redirects integral adeles]]

[[!redirects ring of integral adeles]]
[[!redirects rings of integral adeles]]

[[!redirects ring of valuation vectors]]
[[!redirects valuation vector]]
[[!redirects valuation vectors]]

[[!redirects ring of finite adeles]]
[[!redirects rings of finite adeles]]