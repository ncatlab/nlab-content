
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--

# Composition laws for factorizations
* table of contents
{:toc}

## Idea

A *composition law* for a [[functorial factorization]] is a functorial way to compose lifting structures for its algebraic right maps.  A functorial factorization whose pointed endofunctor extends to a monad over $cod$ is an [[algebraic weak factorization system]] if and only if it has a composition law.  Moreover, subject to smallness conditions, any functorial factorization with a composition law freely generates an algebraic weak factorization system.

## Definition

Suppose $\mathcal{C}$ is a category equipped with a [[functorial factorization]], sending every arrow $f:A\to B$ to a factorization $A \xrightarrow{f_L} E f \xrightarrow{f_R} B$.  As noted at [[functorial factorization]], a functorial factorization is equivalent to a pointed endofunctor $R$ on $\mathcal{C}^{\mathbf{2}}$ over $cod$, which maps each morphism $f$ (regarded as an object of the [[arrow category]] $\mathcal{C}^{\mathbf{2}}$) to its right factor $f_R$, the point being given by the left factor $f_L$ and the identity:

$$\array{ & \xrightarrow{f_L} & \\ ^f \downarrow & & \downarrow^{f_R} \\ & \xrightarrow{id}&. }$$

As with any pointed endofunctor, we can consider the category of [[algebra over a pointed endofunctor|algebras]] for $R$.  Such an $R$-algebra is an arrow $f:A\to B$ equipped with a map $s : E f \to A$ such that $s \circ f_L = id_A$ and $f \circ s = f_R$.  Equivalently, it is a diagonal lifting in the square

$$ \array{ A & \xrightarrow{id} & A \\ ^{f_L}\downarrow & & \downarrow^{f} \\ E f & \xrightarrow{f_R} & B.}$$

In particular, this means that if $(L,R)$ is a factorization for a [[weak factorization system]], then the arrows of $\mathcal{C}$ that admit some structure of $R$-algebra are precisely those in the right class of the weak factorization system.

The morphisms of $R$-algebras are commuting squares $g \circ h = k \circ f$ that additionally commute with the actions, i.e. $h \circ s_f = s_g \circ E(h,k)$.  This defines a category $R Alg$ with a forgetful functor $U : R Alg \to \mathcal{C}^{\mathbf{2}}$.

If it should happen that the pointed endofunctor $R$ is actually a [[monad]] over $cod$, i.e. it also has a multiplication $R R \to R$ that is also the identity on codomains, then we can also consider the smaller category $\mathbb{R} Alg$ of [[algebra over a monad|monad algebras]], the $R$-algebras as above such that $s$ also satisfies an associativity condition.

+-- {: .un_defn}
###### Definition
A **right weak composition law** for a functorial factorization is a functor $R Alg \times_{\mathcal{C}} R Alg \to R Alg$, where the pullback is over $dom \circ U : R Alg \to \mathcal{C}$ and $cod \circ U : R Alg \to \mathcal{C}$, lying over the composition functor $\mathcal{C}^{\mathbf{2}} \times \mathcal{C}^{\mathbf{2}}\to \mathcal{C}$.  If $R$ is a monad over $cod$, then a **right strong composition law** is defined analogously using $\mathbb{R} Alg$ instead.
=--

More explicitly, this means that

1. whenever $(f, s)$ and $(g, t)$ are $R$-algebras (resp. $\mathbb{R}$-algebras) such that $cod(f) = dom(g)$, we have a specified $R$-algebra structure (resp. $\mathbb{R}$-algebra structure) $t \bullet s$ for $g f$, such that
2. for any morphisms of $R$-algebras (resp. $\mathbb{R}$-algebras) $(u, v) : (f, s) \to (f' , s')$ and $(v, w) : (g, t) \to (g' , t')$ between composable pairs $(f, s), (g, t)$ and $(f' , s' ),(g' , t' )$, the pasted square $(u, w) : (g f, t \bullet s) \to (g ' f' , t' \bullet s ' )$ is also a map of $R$-algebras (resp. $\mathbb{R}$-algebras).

In other words, a composition law is an operation with the requisite shape to be the vertical composition in a [[double category]] whose vertical arrows are algebras, whose horizontal arrows are arbitrary arrows, and whose 2-cells are commutative squares.  Associativity is not assumed, but as noted below it often comes for free.

## Relation to awfs

+-- {: .un_theorem}
###### Theorem
Suppose $(L,R)$ is a functorial factorization whose underlying pointed endofunctor $R$ over $cod$ has the structure of a [[monad]] on $\mathcal{C}^{\mathbf{2}}$ over $cod$.  Then $(L,R)$ is an [[algebraic weak factorization system]] if and only if it admits a right strong composition law.
=--
+-- {: .proof}
###### Proof
See [Garner 09](#Garner09), [Garner 10](#Garner10), [Riehl 11](#Riehl11), and [Barthel-Riehl 13](#BR13) for proofs in varying degrees of explicitness.
=--

+-- {: .un_theorem}
###### Theorem
Suppose $(L,R)$ is a functorial factorization with a right weak composition law, and that the [[algebraically free monad]] on the pointed endofunctor $R$ exists and is over $cod$ (for instance if it can be constructed by a [[transfinite construction of free algebras]]).  Then the latter monad has a right strong composition law, hence underlies an algebraic weak factorization system whose right-monad-algebras coincide with the $R$-pointed-endofunctor-algebras, including their natural composition law.
=--
+-- {: .proof}
###### Proof
By definition, the algebraically-free monad $\mathbb{F}(R)$ satisfies $\mathbb{F}(R) Alg = R Alg$.  Thus, the weak composition law for $R$ extends to a strong one for $\mathbb{F}(R)$; now we can apply the previous theorem.
=--


## References

* {#Garner09} [[Richard Garner]]. *Understanding the small object argument*. Appl. Categ. Structures. 17(3) (2009) 247--285.

* {#Garner10} [[Richard Garner]]. *Homomorphisms of higher categories*. Adv. Math. 224(6) (2010), 2269--2311.

* {#Riehl11} [[Emily Riehl]].  *Algebraic model structures*. New York J. Math. 17 (2011) 173-231.

* {#BR13} [[Tobias Barthel]] and [[Emily Riehl]].  *On the construction of functorial factorizations for model categories*.  Algebr. Geom. Topol. Volume 13, Number 2 (2013), 1089-1124. [projecteuclid](https://projecteuclid.org/euclid.agt/1513715550)


[[!redirects composition law for factorization]]
[[!redirects composition law for factorizations]]
[[!redirects composition laws for factorization]]
[[!redirects composition laws for factorizations]]

[[!redirects composition law for a functorial factorization]]
[[!redirects composition law for functorial factorizations]]
[[!redirects composition laws for a functorial factorization]]
[[!redirects composition laws for functorial factorizations]]

[[!redirects composition law for a factorization system]]
[[!redirects composition law for factorization systems]]
[[!redirects composition laws for a factorization system]]
[[!redirects composition laws for factorization systems]]

[[!redirects composition law for a weak factorization system]]
[[!redirects composition law for weak factorization systems]]
[[!redirects composition laws for a weak factorization system]]
[[!redirects composition laws for weak factorization systems]]

[[!redirects composition law for an algebraic weak factorization system]]
[[!redirects composition law for algebraic weak factorization systems]]
[[!redirects composition laws for an algebraic weak factorization system]]
[[!redirects composition laws for algebraic weak factorization systems]]

[[!redirects composition law for wfs]]
[[!redirects composition laws for wfs]]
[[!redirects composition law for awfs]]
[[!redirects composition laws for awfs]]

[[!redirects weak composition law for factorization]]
[[!redirects weak composition law for factorizations]]
[[!redirects weak composition laws for factorization]]
[[!redirects weak composition laws for factorizations]]

[[!redirects weak composition law for a functorial factorization]]
[[!redirects weak composition law for functorial factorizations]]
[[!redirects weak composition laws for a functorial factorization]]
[[!redirects weak composition laws for functorial factorizations]]

[[!redirects weak composition law for a factorization system]]
[[!redirects weak composition law for factorization systems]]
[[!redirects weak composition laws for a factorization system]]
[[!redirects weak composition laws for factorization systems]]

[[!redirects strong composition law for factorization]]
[[!redirects strong composition law for factorizations]]
[[!redirects strong composition laws for factorization]]
[[!redirects strong composition laws for factorizations]]

[[!redirects strong composition law for a functorial factorization]]
[[!redirects strong composition law for functorial factorizations]]
[[!redirects strong composition laws for a functorial factorization]]
[[!redirects strong composition laws for functorial factorizations]]

[[!redirects strong composition law for a factorization system]]
[[!redirects strong composition law for factorization systems]]
[[!redirects strong composition laws for a factorization system]]
[[!redirects strong composition laws for factorization systems]]

[[!redirects right weak composition law for factorization]]
[[!redirects right weak composition law for factorizations]]
[[!redirects right weak composition laws for factorization]]
[[!redirects right weak composition laws for factorizations]]

[[!redirects right weak composition law for a functorial factorization]]
[[!redirects right weak composition law for functorial factorizations]]
[[!redirects right weak composition laws for a functorial factorization]]
[[!redirects right weak composition laws for functorial factorizations]]

[[!redirects right weak composition law for a factorization system]]
[[!redirects right weak composition law for factorization systems]]
[[!redirects right weak composition laws for a factorization system]]
[[!redirects right weak composition laws for factorization systems]]

[[!redirects right strong composition law for factorization]]
[[!redirects right strong composition law for factorizations]]
[[!redirects right strong composition laws for factorization]]
[[!redirects right strong composition laws for factorizations]]

[[!redirects right strong composition law for a functorial factorization]]
[[!redirects right strong composition law for functorial factorizations]]
[[!redirects right strong composition laws for a functorial factorization]]
[[!redirects right strong composition laws for functorial factorizations]]

[[!redirects right strong composition law for a factorization system]]
[[!redirects right strong composition law for factorization systems]]
[[!redirects right strong composition laws for a factorization system]]
[[!redirects right strong composition laws for factorization systems]]

[[!redirects left weak composition law for factorization]]
[[!redirects left weak composition law for factorizations]]
[[!redirects left weak composition laws for factorization]]
[[!redirects left weak composition laws for factorizations]]

[[!redirects left weak composition law for a functorial factorization]]
[[!redirects left weak composition law for functorial factorizations]]
[[!redirects left weak composition laws for a functorial factorization]]
[[!redirects left weak composition laws for functorial factorizations]]

[[!redirects left weak composition law for a factorization system]]
[[!redirects left weak composition law for factorization systems]]
[[!redirects left weak composition laws for a factorization system]]
[[!redirects left weak composition laws for factorization systems]]

[[!redirects left strong composition law for factorization]]
[[!redirects left strong composition law for factorizations]]
[[!redirects left strong composition laws for factorization]]
[[!redirects left strong composition laws for factorizations]]

[[!redirects left strong composition law for a functorial factorization]]
[[!redirects left strong composition law for functorial factorizations]]
[[!redirects left strong composition laws for a functorial factorization]]
[[!redirects left strong composition laws for functorial factorizations]]

[[!redirects left strong composition law for a factorization system]]
[[!redirects left strong composition law for factorization systems]]
[[!redirects left strong composition laws for a factorization system]]
[[!redirects left strong composition laws for factorization systems]]
