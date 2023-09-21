

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[dualizable object]] in a [[symmetric monoidal (∞,n)-category]] $\mathcal{C}$ is called **fully dualizable** if the structure maps of the duality unit and counit each themselves have [[adjoints]], which have adjoints, and so on, up to level $(n-1)$.


## Properties

By the [[cobordism hypothesis]]-theorem, symmetric monoidal [[(∞,n)-functor]]s out of the [[(∞,n)-category of cobordisms]] are characterized by their value on the point, which is a fully dualizable object.

## Examples

* In the [[symmetric monoidal category]] [[Vect]] of [[vector space]]s (over some [[field]]), the fully dualizable objects are the finite-[[dimension]]al vector spaces.

* In the [[2-category]] of [[associative algebras]]  with [[bimodules]] between them as morphisms, over a [[commutative ring]], fully dualizable objects are [[separable algebras]] which are [[projective modules]] over the base ring (these conditions are given in [SchommerPries 11, Definition 3.70] (#SchommerPries11) and attributed to Lurie's paper cited below). 

* In the [[symmetric monoidal (infinity,n)-category|symmetric monoidal 3-category]] of [[monoidal categories]] and [[bimodule categories]] between them, the fully dualizable objects are (or at least contain) the [[fusion categories]]. ([DSPS 13](#DSPS13)).

## Related concepts

* [[(∞,n)-category with adjoints]]

* [[(∞,n)-category with duals]]


[[!include finite objects -- table]]


## References

The definition appears around claim 2.3.19 of

* [[Jacob Lurie]], *[[On the Classification of Topological Field Theories]]*, Current Developments in Mathematics **2008** (2009) 129-280 &lbrack;[arXiv:0905.0465](http://arxiv.org/abs/0905.0465), [doi:10.4310/CDM.2008.v2008.n1.a3](https://dx.doi.org/10.4310/CDM.2008.v2008.n1.a3), [euclid:cdm/1254748657](https://projecteuclid.org/euclid.cdm/1254748657)&rbrack;


Review:

* [[Dominic Culver]], [[Mitchell Faulk]], *Duality Notes*, lecture notes for *West Coast Algebraic Topology Summer School* (2014) &lbrack;[pdf](https://mathtube.org/sites/default/files/lecture-notes/Duality%20Notes.pdf), [[CulverFaulk-DualityNotes.pdf:file]] [mathtube](https://www.mathtube.org/lecture/notes/duality-notes)&rbrack;


Detailed discussion in degree 2 and 3:

* {#SchommerPries11} [[Chris Schommer-Pries]], _The Classification of Two-Dimensional Extended Topological Field Theories_ ([arXiv:1112.1000](http://arxiv.org/abs/1112.1000))

* {#DSPS13} [[Chris Douglas]], [[Chris Schommer-Pries]], [[Noah Snyder]], _Dualizable tensor categories_ ([arXiv:1312.7188](http://arxiv.org/abs/1312.7188))

[[!redirects fully dualizable objects]]

