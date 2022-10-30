
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There exists a [[model category]] structure on a [[category]] of [[dg-coalgebra]]s whose fibrant objects are precisely [[L-∞ algebra]]s.

## Definition

### On dg-coalgebras

(...)

See [[model structure on dg-coalgebras]] and [[model structure on dg-Lie algebras]].

See ([Hinich](#Hinich))

(...)

### Equivalent models


(...)

+-- {: .num_defn #DGSp}
###### Definition

Write $DG_{\mathbb{Z}}Sp(k)$ for the [[model category]] whose

...

=--


See [Pridham](#Pridham)


(...)

## Properties


+-- {: .num_prop #QuillenEquivalence}
###### Proposition

There is a [[Quillen equivalence]]

$$
  dgCoAlg(k) \simeq DG_{\mathbb{Z}}Sp(k)
  \,.
$$

=--

([Pridham](#Pridham))

+-- {: .num_prop #RightProperness}
###### Proposition

The model category $DG_{\mathbb{Z}}Sp(k)$, def. \ref{DGSp}, is a [[right proper model category]].

=--

This observation has been communicated privatly by [[Jonathan Pridham]]

+-- {: .proof}
###### Proof

We need to show that the [[pullback]] of a weak equivalence $w$ along a fibration $f$ is again a weak equivalence. If $w$ is a fibration, this is automatic, so by factorisation we reduce to the case where $w$ is a cofibration. Now, every trivial cofibration is $Spf$ of a composition of acyclic small extensions, so we may take $w$ to be $Spf$ of an acyclic small extension $A \to B$ with [[kernel]] $I$. Then $f$ is $Spf$ of a quasi-free map $A \to R$, so the pullback is $Spf$ of $R \to R/IR$, and $IR =I\hat{\otimes}_A R$, so $R \to R/IR$ is also an acyclic small extension.

=--

## Related concepts

* [[model structure on dg-coalgebras]]

* [[model structure on dg-Lie algebras]]

## References

* [[Vladimir Hinich]], _DG coalgebras as formal stacks_ ([arXiv:9812034](http://arxiv.org/abs/math/9812034))
 {#Hinich}

* [[Jonathan Pridham]], _Unifying derived deformation theories_, Adv. Math. 224 (2010), no.3, 772-826 ([arXiv:0705.0344](http://arxiv.org/abs/0705.0344))
 {#Pridham}

* [[Jacob Lurie]], _[[Formal Moduli Problems]]_
 {#Lurie}

[[!redirects model structure for L-∞ algebras]]
