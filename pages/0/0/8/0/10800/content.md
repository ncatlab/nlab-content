
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

The _group of ideles_ $\mathbb{I}$ is the [[group of units]] in the [[ring of adeles]] $\mathbb{A}$:

$$
  \mathbb{I} = \mathbb{A}^\times \coloneqq GL_1(\mathbb{A})
  \,.
$$

In classical [[algebraic number theory]] one embeds a [[number field]] into the [[Cartesian product]] of its [[completions]] at its [[archimedean absolute values]]. This embedding is very useful in the [[proofs]] of several fundamental [[theorems]]. However, it was noticed by [[Claude Chevalley]] and [[André Weil]] that the situation was improved somewhat if the number field is embedded in a certain [[restricted product]] of its [[formal completions]] at all of its [[absolute values]]. These objects are known as the _[[adeles]]_, and the [[group of units|units]] of this ring are called the _ideles_.


When considering the adeles and ideles, it is their [[topology]] as much as their algebraic structure that is of interest. Many important results in [[number theory]] translate into simple statements about the topologies of the adeles and ideles. For example, the finiteness of the [[ideal class group]] and the [[Dirichlet unit theorem]] are equivalent to a certain quotient of the ideles being compact and discrete.

([Weston, p. 1](#Weston))

## Definition



+-- {: .num_defn }
###### Definition

The [[group of units]] of the ring of adeles $\mathbb{A}_{\mathbb{Q}}$ is called the _group of ideles_

$$
  \mathbb{I}_{\mathbb{Q}} \coloneqq GL_1(\mathbb{A}_{\mathbb{Q}}) = \mathbb{A}_{\mathbb{Q}}^\times
  \,.
$$

It is a [[topological group]] via identification with the set $\{(x, x^{-1}) \in \mathbb{A}_\mathbb{Q}^2: \; x \in \mathbb{I}_\mathbb{Q}\}$, seen as a [[subspace]] of $\mathbb{A}_\mathbb{Q}^2$. 
=--

+-- {: .num_remark} 
###### Remark 
The topology on $\mathbb{I}_\mathbb{Q}$ is strictly finer than the subspace topology inherited from $\mathbb{A}_\mathbb{Q}$. For example, the set $\mathbb{R}^\times \times \prod_p \mathbb{Z}_p^\times$ is a neighborhood of $1$ in $\mathbb{I}_\mathbb{Q}$, but not in the subspace topology. Cf. the discussion [here](https://math.stackexchange.com/a/145452/43208). Note: multiplicative inversion is not continuous in the subspace topology. 
=-- 

The same definition holds for the [[ring of adeles]] of any other [[global field]] $K$, here one writes

$$
  \mathbb{I}_K \coloneqq GL_1(\mathbb{A}_K)
$$

or similar. The notation $J_K$ is also common. 

+-- {: .num_defn #IdeleClassGroup}
###### Definition

The [[quotient]]

$$
  K^\times \backslash \mathbb{I}_K
  =
  GL_1(K)\backslash GL_1(\mathbb{A}_K)
$$

is called the _idele class group_ of $K$.

=--

+-- {: .num_remark }
###### Remark

The idele class group, def. \ref{IdeleClassGroup}, appears prominently in the description of the [moduli space of line bundles](moduli+space+of+bundles#OverCurvesAndTheLanglandsCorrespondence) over the [[arithmetic curve]] on which $K$ is the [[rational functions]]. From there it appears in the abelian [[Langlands correspondence]] and in the abelian case of [[Tamagawa measures]].

=--

The idele class group is a key object in _[[class field theory]]_.

## Properties

### Product formula
 {#ProductFormula}

Recall the [[p-adic norm]] ${\vert -\vert}_p$ on $\mathbb{Q}$ for $p$ a [[prime number]], given by

$$
  {\left \vert \frac{a}{b}p^\ell \right \vert}_p
  \coloneqq
  p^{-\ell}
$$

for $a,b$ coprime to $p$. The usual [[absolute value]] [[norm]] one writes

$$
  {\vert -\vert}_\infty
$$

and associates with the "[[place at infinity|prime at infinity]]". When an index runs over the set of all primes ("finite primes") union with the "prime at infinity" one usually writes it "$v$" instead of $p$. 

This induces:

+-- {: .num_defn #IdeleNorm}
###### Definition

The _idele norm_

$$
  {\vert -\vert} \colon \mathbb{I}_{\mathbb{Q}} \longrightarrow \mathbb{C}^\times
$$

is the function given by

$$
  {\vert \alpha\vert} \coloneqq \underset{v}{\prod} {\vert \alpha_v\vert}_v
  \,.
$$

=--

Notice that by construction there is a [[diagonal]] map $\mathbb{Q}^\times \to \mathbb{I}_{\mathbb{Q}}$.

+-- {: .num_prop #ProductFormula}
###### Proposition
**(product formula)**

The idele norm, def. \ref{IdeleNorm}, is trivial on the diagonal of $\mathbb{Q}^\times$ inside the ideles, in that

$$
  (\alpha \in \mathbb{Q}^\times \to \mathbb{I}_{\mathbb{Q}})
  \;\Rightarrow\;
  {\vert \alpha\vert}
  \coloneqq 
  \underset{v}{\prod} {\vert \alpha_v\vert}_v
  = 1
  \,.
$$


=--

+-- {: .num_remark }
###### Remark

The product formula, prop. \ref{ProductFormula}, says that the idele norm descends to the idele class group, def. \ref{IdeleClassGroup}.

=--

(e.g. [Garrett 11, section 1](#Garrett11))

### Strong approximation theorem for the idele class group
 {#StrongApproximationTheorem}


+-- {: .num_prop #StrongApproximationTheorem}
###### Proposition
**(strong approximation form ideles)**

The idele class group, def. \ref{IdeleClassGroup}, may be expressed as

$$
  \mathbb{Q}^\times \backslash \mathbb{A}_{\mathbb{Q}}^\times
  \simeq
  (0,\infty)
   \times
  \underset{p}{\prod}
  \mathbb{Z}_p^\times
  \,.
$$

=--

(e.g. [Goldfeld-Hundley 11, prop. 1.4.5 and below (2.2.7)](#GoldfeldHundley11))

This implies that the [[ring of adeles]] may be decomposed into a rational and an idele class factor as:


$$
  \begin{aligned}
    \mathbb{A}_{\mathbb{Q}}^\times
     & \simeq
    \mathbb{Q}^\times
    \times
    (\mathbb{Q}^\times \backslash \mathbb{A}_{\mathbb{Q}}^\times)
    \\
    & \coloneqq
    \underset{n \in \mathbb{Q}^\times}{\cup}
    n \cdot 
    (\mathbb{Q}^\times \backslash \mathbb{A}_{\mathbb{Q}}^\times)
 \end{aligned}
  \,.
$$

(e.g. [Goldfeld-Hundley 11, prop. 1.4.6 and below (2.2.7)](#GoldfeldHundley11))

This decomposition is crucial in the discussion of the [[Riemann zeta function]] (see there) as an [[adelic integral]].

### Automorphic forms and Relation to Dirichlet characters

The [[automorphic forms]] of the idele group are essentially
[[Dirichlet characters]] in disguise ([Goldfeld-Hundley 11, below def. 2.1.4](#GoldfeldHundley11))

### Function field analogy
 {#FunctionFieldAnalogy}

Via the [[function field analogy]] one may understand any [[number field]] or [[function field]] $F$ as being the [[rational functions]] on an [[arithmetic curve]] $\Sigma$. Under this identification the [[ring of adeles]] $\mathbb{A}_F$ of $F$ has the interpretation of being the [[ring of functions]] on all punctured [[formal disks]] around all points of $\Sigma$, such that only finitely many of them do not extend to the given point. ([Frenkel 05, section 3.2](#Frenkel05)). 

This means for instance that the [[general linear group]] $GL_n(\mathbb{A}_F)$ with [[coefficients]] in the [[ring of adeles]] has the interpretation as being the [[Cech cohomology|Cech cocycles]] for [[algebraic vector bundles]] of [[rank]] $n$ on an [[algebraic curve]] with respect to any [[cover]] of that curve by the complement of a finite number of points together with the [[formal disks]] around these points. Here for $n = 1$ then $GL_1(\mathbb{A}_F)$ is the group of ideles. 

This is part of a standard construction of the [[moduli stack of bundles]] on algebraic curves, see at _[Moduli space of bundles and the Langlands correspondence](moduli+space+of+bundles#OverCurvesAndTheLanglandsCorrespondence)_.



[[!include function field analogy -- table]]


## Related concepts

* [[differential cohesion and idelic structure]]

## References

Basics are recalled in

* _Adeles_ [pdf](http://wiki.epfl.ch/gant/documents/lecture2-cib2011.pdf)

* Pete Clark, _Adeles and Ideles_ ([pdf](http://math.uga.edu/~pete/8410Chapter6.pdf))

* Erwin Dassen , _Adeles & Ideles_ ([pdf](http://www.math.leidenuniv.nl/~astolk/monday/notes/dassen-adeles-ideles.pdf))


* {#Weston} Tom Weston, _The idelic approach to number theory_ ([pdf](http://www.math.umass.edu/~weston/oldpapers/idele.pdf))
 
* {#GoldfeldHundley11} {#GoldfeldHundley11} [[Dorian Goldfeld]], [[Joseph Hundley]], chapter 2 of _Automorphic representations and L-functions for the general linear group_, Cambridge Studies in Advanced Mathematics 129, 2011 ([pdf](https://web.archive.org/web/20150326125549/https://www.maths.nottingham.ac.uk/personal/ibf/text/gl2.pdf))

* {#Garrett11} [[Paul Garrett]], _Iwasawa-Tate on &#950;-functions and L-functions_, 2011 ([pdf](http://www-users.math.umn.edu/~garrett/m/mfms/notes_c/Iwasawa-Tate.pdf)
[[!redirects Poisson formula]]
 
Discussion in the context of the [[geometric Langlands correspondence]] is in 

* {#Frenkel05} [[Edward Frenkel]], section 3.2 of _Lectures on the Langlands Program and Conformal Field Theory_, in _Frontiers in number theory, physics, and geometry II_, Springer Berlin Heidelberg, 2007. 387-533. ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172))

[[!redirects idele]]
[[!redirects ideles]]

[[!redirects idele class group]]
[[!redirects idele class groups]]

[[!redirects idele group]]
[[!redirects idele groups]]


[[!redirects idèle group]]
[[!redirects group of idèles]]