[[!redirects (∞,1)-vector bundle]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of an _$(\infty,1)$-vector bundle_ is a [[categorification]] of the notion of a [[vector bundle]], where [[field]]s and [[ring]]s are replaced by [[∞-ring]]s.

Recall that for $k$ a [[field]], a [[vector space]] is a $k$-[[module]], and a [[vector bundle]] over a [[space]] $X$ is classified by a morphism 
$\alpha : X \to k$[[Mod]] with $k$[[Mod]] regarded as an object in the relevant [[topos]]. For instance for _discrete_ or _flat_ vector bundles $k Mod$ is the [[category]] [[Vect]] of vector spaces.
There is the subcategory $k Line \hookrightarrow k Mod$ of 1-[[dimension]]al $k$-vector bundles, and morphisms that factor as $\alpha : X \to k Line \hookrightarrow k Mod$ are $k$-[[line bundle]]s.
In the discrete case the vector space of [[section]]s of the vector bundle classified by $\alpha$ is the [[colimit]] $\lim_\to \alpha$.

These statements [[categorification|categorify]] in a straightforward manner to the case where $k$ is generalized to a commutative [[∞-ring]]: an _[[E-∞ ring]]_ or _[[ring spectrum]]_ . Modules are replaced by [[module spectrum|module spectra]] and colimits by [[homotopy colimit]]s.

The resulting notion of $(\infty,1)$-vector bundles plays a central role in many constructions in [[orientation in generalized cohomology]], [[twisted cohomology]] and [[Thom isomorphism]]s.

Further generalization of the concept leads to [[(∞,n)-vector bundle]]s: an $(\infty,n)$-module over an [[E-∞-ring]] $K$ is essentially an object of the [[(∞,n)-category]] $(\cdots (K Mod) Mod ) \cdots Mod$.

## Definition

### Discrete $(\infty,1)$-vector bundles

Throughout we denote by $K$ an [[E-∞ ring]] and by $A$ a $K$-algebra, hence an [[A-∞ algebra]] in [[Spec]] equipped with a $\infty$-algebra homomorphism $K \to A$.

Write $A Mod$ for the [[(∞,1)-category]] of $A$-[[module spectrum|module spectra]].

+-- {: .num_defn}
###### Definition

For $X$ a [[discrete ∞-groupoid]] (often presented as a [[topological space]]), the [[(∞,1)-category]] of **$A$-module $\infty$-bundles** over $X$ is the [[(∞,1)-functor (∞,1)-category]]

$$
  A Mod(X) := Func(X, A Mod)
  \,.
$$

=--

In this form this appears as ([ABG def. 3.7](#ABG)). Compare this to the analogous definition at [[principal ∞-bundle]]. 

+-- {: .num_remark}
###### Remark

If $X$ is regarded as a [[topological space]] then the corresponding [[discrete ∞-groupoid]] is $\Pi X$, the [[fundamental ∞-groupoid]] of $X$ and the morphism encoding an $K$-module bundle over $X$ is reads

$$
  \alpha : \Pi(X) \to A Mod
  \,.
$$

This assignment of $A$-modules to points in $X$, of $A$-module morphism to paths in $X$ etc. may be regarded as the [[higher parallel transport]] of the (unique and flat, due to [[discrete ∞-groupoid|discreteness]]) [[connection on an ∞-bundle]] on $\alpha$. 

Equivalently, this morphism may be regarded as an [[∞-representation]] of $\Pi(X)$. Notaby if $X = B G$ is the [[classifying space]] of a [[discrete group]] or [[discrete ∞-group]], a $K$-module $\infty$-bundle over $X$ is the same as an [[∞-representation]] of $G$ on $A Mod$.

=--

+-- {: .num_defn}
###### Definition

Write 

$$
  A Line \hookrightarrow A Mod
$$

for the [[full sub-(∞,1)-category]] on the _$A$-line_ : on those $A$-modules that are equivalent to $A$ as an $A$-module. The full subcatgeory of $A Mod(X)$ on morphisms factoring through this inclusion we call the $(\infty,1)$-catgeory of **$A$-line $\infty$-bundles**.

=--

This appears as ([ABG def. 3.12](#ABG)).

### Structured $(\infty,1)$-vector bundles

(...)

## References

A systematic discussion of discrete $(\infty,1)$-module bundles is in the pair of articles

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 {#ABGHR}

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_ ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 [#ABG}
