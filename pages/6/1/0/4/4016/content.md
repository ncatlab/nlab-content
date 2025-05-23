
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Definition

A [[cardinal number]] $\kappa$ is **measurable** if some (hence any) set of cardinality $\kappa$ admits a two-valued [[measure]] which is $\kappa$-additive, or equivalently an [[ultrafilter]] which is $\kappa$-complete.


## Properties

Any measurable cardinal is, in [[ZFC]], necessarily [[inaccessible cardinal|inaccessible]], and in fact much larger than the smallest inaccessible.  In fact, if $\kappa$ is measurable, then there is a $\kappa$-complete ultrafilter $\mathcal{U}$ on $\{\lambda | \lambda \lt \kappa\}$ which contains the set $\{\lambda | \lambda \lt \kappa$ and $\lambda$ is inaccessible $\}$.  In particular, there are $\kappa$ inaccessible cardinals smaller than $\kappa$. Note that in [[ZF]] it is consistent that $\omega_1$, a successor cardinal, is measurable.

It follows from this that the existence of any measurable cardinals cannot be proven in [[ZFC]], since the existence of inaccessible cardinals cannot be so proven.  Thus measurable cardinals are a kind of [[large cardinal]].  They play an especially important role in large cardinal theory, since any measurable cardinal gives rise to an [[elementary embedding]] of the universe $V$ into some submodel $M$ (such as an [[ultrapower]] by a countably-complete ultrafilter), while the "critical point" of any such embedding is necessarily measurable.

Measurable cardinals are sometimes said to mark the boundary between "small" large cardinals (such as inaccessibles, [[Mahlo cardinal]]s, and [[weakly compact cardinal]]s) and "large" large cardinals (such as [[strongly compact cardinal]]s, [[supercompact cardinal]]s, and so on).


## In category theory

The existence or nonexistence of measurable cardinals can have noticeable impacts on [[category theory]], notably in terms of the properties of the category [[Set]].

For instance, the existence of a measurable cardinal is equivalent to the existence of an [[exact functor]] $F: Set \to Set$ that is not naturally isomorphic to the identity.  This was essentially proved by V. Trnkov&#225;, and it was rediscovered by Blass in his paper "Exact functors and measurable cardinals" ([Blass 1976](#Blass_76)).

Furthermore, the category $Set^{op}$ has a [[small category|small]] [[dense subcategory]] if and only if there does *not* exist a [[proper class]] of measurable cardinals.  Specifically, the subcategory of all sets of cardinality $\lt\lambda$ is dense in $Set^{op}$ precisely when there are no measurable cardinals larger than $\lambda$.  In particular, the full subcategory on $\mathbb{N}$ is dense in $Set^{op}$ precisely when there are no measurable cardinals at all.

This is theorem A.5 of [[Locally Presentable and Accessible Categories]].

## Related entries

* [[large cardinal]]

* [[real-valued-measurable cardinal]]

## References

* M. Adelman, [[Andreas Blass|A. Blass]], _Exact functors, local connectedness and measurable cardinals_ , Rend. Sem. Mat. Fis. Milano **54** (1984) pp.9-28.

* {#Blass_76} [[Andreas Blass]], _Exact Functors and Measurable Cardinals_ , Pacific J. Math. **63** (1976) pp.335-346. ([euclid](https://projecteuclid.org/euclid.pjm/1102867389))


* [[Andreas Blass]], _Corrections to: 'Exact Functors and Measurable Cardinals'_ , Pacific J. Math. **73** (1977) p.540. ([euclid](https://projecteuclid.org/euclid.pjm/1102810622))

* {: #MR0175954 } [[John Isbell]], _Adequate subcategories_ , Illinois J. Math. **4** (1960) pp.541-552. [MR0175954](http://www.ams.org/mathscinet-getitem?mr=0175954). 
([euclid](https://projecteuclid.org/euclid.ijm/1255456274))
 
* [[John Isbell]], _Subobjects, adequacy, completeness and categories of algebras_ , Rozprawy Mat. **36** (1964) pp.1-32. ([toc](http://pldml.icm.edu.pl/pldml/element/bwmeta1.element.desklight-0dbcb276-0b92-49eb-b504-a9963119ea3e))

* [[David P. Blecher]], [[Nik Weaver]], *Quantum measurable cardinals* ([arXiv:1607.08505](https://arxiv.org/abs/1607.08505))

Some discussion on measurable cardinals in the context of a [[polynomial function]] whose [[Lebesgue measure|Lesbegue measurability]] is independent of [[ZFC]] occurs in:

* [[James E. Hanson]], *Any function I can actually write down is measurable, right?* ([arXiv:2501.02693](https://arxiv.org/abs/2501.02693))

[[!redirects measurable cardinal]]
[[!redirects measurable cardinals]]
