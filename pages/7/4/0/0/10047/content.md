
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Continuous categories
* table of contents
{: toc}

## Idea

The notion of _continuous category_ is a [[categorification]] of the notion of _[[continuous poset]]_.  It can be further categorified to a notion of continuous [[(∞,1)-category]].


## Definition

Let $C$ be a [[category]] and $Ind(C)$ its category of [[ind-objects]].  We assume that $C$ has [[filtered colimits]], which is equivalently to say that the restricted [[Yoneda embedding]] $\hat{(-)} : C\to Ind(C)$ has a [[left adjoint]] $\colim$.

+-- {: .num_defn}
###### Definition
A category $C$ with filtered colimits is a **continuous category** if $\colim: Ind(C) \to C$ has a left adjoint.
=--

If $C$ is a [[poset]], then $Ind(C) = Idl(C)$ is its category of [[ideals]].  Thus, a poset is a continuous category exactly when it is a [[continuous poset]].  This definition can be extended to $(\infty,1)$-categories essentially verbatim.


## Examples

* Any finitely [[accessible category]], and hence any [[locally finitely presentable category]], is a continuous category.

* A [[Grothendieck topos]] is a continuous category if and only if it is an [[exponentiable object]] in the 2-category of Grothendieck toposes and [[geometric morphisms]], i.e. an [[exponentiable topos]].

  * If $X$ is a [[stably locally compact locale]] (or more generally a [[metastably locally compact locale]]), then $Sh(X)$ is continuous and hence exponentiable.  It does *not* suffice for $X$ to be locally compact (i.e. for its [[frame of opens]] to be a continuous poset).

  * Similarly, a [[Grothendieck (∞,1)-topos]] is a continuous $(\infty,1)$-category if and only if it is an exponentiable object, in the appropriate sense, in the $(\infty,1)$-category of $(\infty,1)$-toposes and geometric morphisms.

* In general, a [[locally small category]] $C$ is continuous if and only if it is a [[retract]] of a category $Ind(D)$ of [[ind-objects]], where the functors exhibiting the retract preserve [[filtered colimits]] ([Johnstone-Joyal 82, Theorem 2.8](#JohnstoneJoyal82)).

## Wavy arrows

If $C$ is continuous, with $L:C\to Ind(C)$ the left adjoint of $\colim$, and $x,y\in C$, we define a **wavy arrow** $x\rightsquigarrow y$ to be a morphism $\hat{x} \to L(y)$ in $Ind(C)$.  This is a categorification of the [[way-below relation]] on a continuous poset: when $C$ is a poset we have a wavy arrow $x\rightsquigarrow y$ just when $x\ll y$.  But unlike in the posetal case, it is not clear how to define wavy arrows unless $C$ is continuous (whereas $\ll$ can be defined in any poset with directed joins).  However, see [[totally distributive category]].

Since $\colim \hat{x} = x$ and $\colim L(y)=y$, the functor $\colim$ assigns to every wavy arrow a "straight" arrow $x\to y$ in $C$.  Moreover, wavy arrows can be composed: the composite of $f:\hat{x} \to L(y)$ and $g:\hat{y} \to L(z)$ is the composite
$$ \hat{x} \xrightarrow{f} L(y) \xrightarrow{i} \hat{y} \xrightarrow{g} L(z) $$
where $i$ is the [[adjunct]] of the identity $y = \colim \hat{y}$ (or of the identity $\colim L(y) = y$).  This composition is associative.  Thus, we _almost_ have a category whose objects are those of $C$ and whose morphism are wavy arrows --- but it does not have identities.

However, if $\tilde{C}(x,y)$ denotes the set of wavy arrows, then the composition defines a map of [[profunctors]] $\tilde{C} \otimes_C \tilde{C} \to \tilde{C}$ which is in fact an isomorphism.  Combined with the map from wavy arrows to straight ones, this makes $\tilde{C}$ into an idempotent [[comonad]] on $C$ in the bicategory [[Prof]].


## Remark

* Continuous categories can be generalized to [[continuous algebras]] for any [[lax-idempotent 2-monad]].

## The setting of (∞,1)-categories

Continuous [[(∞,1)-categories]] are introduced under the name of __compactly assembled ∞-categories__ in Lurie [SAG](#SAG), §21.1.2.


## Related entries

* [[totally distributive category]]

* [[injective topos]]

* [[domain theory]]

* [[Scott topos]]

## References

* [[Jiří Adámek]], [[F. William Lawvere]], [[Jiří Rosický]], _Continuous categories revisited_ , TAC **11** no.11 (2003) pp.252-282. ([abstract](http://www.tac.mta.ca/tac/volumes/11/11/11-11abs.html))

* {#JohnstoneJoyal82} [[Peter Johnstone]], [[Andre Joyal]], *Continuous categories and exponentiable toposes*, JPAA 25 (1982), [doi (free PDF)](http://dx.doi.org/10.1016/0022-4049%2882%2990083-4)

* [[Mathieu Anel]], Damien Lejay, _Exponentiable Higher Toposes_ , arXiv:1802.10425 (2018). ([abstract](https://arxiv.org/abs/1802.10425))

* {#SAG} [[Jacob Lurie]], _[[Spectral Algebraic Geometry]]_.

[[!redirects continuous category]]
[[!redirects continuous categories]]
[[!redirects wavy arrow]]
[[!redirects wavy arrows]]
