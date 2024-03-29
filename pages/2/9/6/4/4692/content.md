
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **monoidal fibration** is a [[functor]] $\Phi\colon E\to B$ such that

* $\Phi$ is a [[Grothendieck fibration]]

* $E$ and $B$ are [[monoidal categories]] and $\Phi$ is a strict [[monoidal functor]], and

* the [[tensor product]] of $E$ preserves [[cartesian arrows]].

If $B$ is [[cartesian monoidal category|cartesian monoidal]], then monoidal fibrations over $B$ are equivalent to [[pseudofunctors]] $B^{op} \to MonCat$, which are called [[indexed monoidal categories]]. In this case the tensor product on $E$ is the [[external tensor product]] of the indexed monoidal category.

## Related concepts

* [[indexed monoidal category]], [[dependent linear type theory]]

* [[monoidal Grothendieck construction]]

## References

* [[Mike Shulman]], _Framed bicategories and monoidal fibrations_, [TAC](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html)

[[!redirects monoidal fibrations]]