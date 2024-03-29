
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Over [[compact topological space|compact]] [[Kähler manifolds]] $X$, _Hodge symmetry_ is the property that the [[Dolbeault cohomology]] groups $H^{p,q}(X)$ are taken into each other under [[complex conjugation]] followed by switching the bidegree:

$$
  H^{p,q}(X) \simeq \overline{H^{q,p}(X)}
  \,.
$$

In particular this means that the [[dimension]] of the cohomology groups in degree $(p,q)$ -- the [[Hodge number]] $h^{p,q}$ -- coincides with that in bidegree $(q,p)$.

By the [[Dolbeault theorem]] this is formulated more generally in terms of [[abelian sheaf cohomology]] as saying that

$$
  dim_{\mathbb{C}} H^q(X,\Omega^p)
  =
  dim_{\mathbb{C}} H^p(X,\Omega^q)  
  \,,
$$

where $\Omega^p$ denotes the [[abelian sheaf]] of [[holomorphic p-forms]].

In this form the statement of Hodge symmetry makes sense more generally for [[complex analytic spaces]] and [[schemes]] over the [[complex numbers]] -- but it is no longer generally true in these more general cases

Sufficient conditions for Hodge symmetry to hold more generally are discussed for instance in ([Joshi 14](#Joshi14)).

## References

* {#Joshi14} Kirti Joshi, _Some remarks on Hodge symmetry_ ([arXiv:1402.4176](http://arxiv.org/abs/1402.4176))

