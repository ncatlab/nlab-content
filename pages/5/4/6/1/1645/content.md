

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

There are at least two things that are called _quantum anomalies_ in the context of [[quantum field theory]]

* **anomalous action functional**: the [[action functional]] (in [[path integral|path integral quantization]]) is not a globally well defined [[function]], but instead a [[section]] of a [[line bundle]] on [[configuration space]];

* **anomalous symmetry**: a symmetry of the [[action functional]] does not extend to a symmetry of the exponentiated action times the path integral measure; or equivalently the [[action]] of a group on classical [[phase space]] is not preserved by [[deformation quantization]].

## Definition

### Anomalous action functional

There are two major kinds of [[action functional]]s that may be anomalous in that they are not actually [[function]]s/[[functional]]s on the configuration space of fields, but just [[section]]s of some [[line bundle]]:

* theories with fermions (see e.g. [[spinors in Yang-Mills theory]])

* [[gauge theory|gauge theories]] with higher degree gauge fields ([[differential cohomology|differential cocycles]] of higher degree.) 

#### Fermionic anomalies

The [[path integral]] for a [[quantum field theory]] with fermions can be decomposed into the integral over the [[fermionic field]]s follows by that over the [[bosonic field]]s. The former, a [[Berezin integral]] is typically well defined for a fixed configuration of the bosonic fields, but does not produce a well defined function on the space of all bosonic fields: but a _twisted function_ , a section of some line bundle called a [[determinant line bundle]] or, in $8k+2$ dimensions, its square root, the [[Pfaffian line bundle]]. 

So to even start making sense of the remaining path integral over the bosonic degree of freedom, this [[determinant line bundle]] or the corresponding [[Pfaffian line bundle]] has to be trivializale. Its non-trivializability is the _fermionic anomaly_ .


#### Higher gauge-theoreric anomalies

For the moment see [[Green-Schwarz mechanism]] for more.


### Anomalous symmetry

...

## Examples

### Anomalous action functional

#### Spinning particles and super-branes 

The [[sigma-model]] for a [[supersymmetry|supersymmetric]] fundamental brane on a target space $X$ has an anomaly coming from the nontriviality of Pfaffian line bundles associated with the fermioninc fields on the worldvolume. These anomalies disappear (i.e. these bundles are trivializable) when the structure group of the [[tangent bundle]] of $X$ has a sufficiently high lift through the [[Whitehead tower]] of $O(n)$.

* **Spin structure** the worldline anomaly for the spinning particle/superparticle vanishes when $X$ has [[Spin structure]] 

  This is a classical result. A concrete derivation is in 

  * [[Edward Witten]], _Global anomalies in String theory_ in _Symposium on anomalies, geometry, topology_ , World Scientific Publishing, Singapore (1985)

* **String structure** the worldsheet anomaly for the spinning string/superstring in [[heterotic string theory]] vanishes (essentially) when $X$ has [[String structure]] 

  This is originally due to Killingback and Witten. A commented list of literature is [here](http://golem.ph.utexas.edu/string/archives/000572.html). Recently [[Ulrich Bunke]] gave the rigorous proof

  * [[Ulrich Bunke]], _String structures and trivialisations of a Pfaffian line bundle_ ([arXiv](http://arxiv.org/abs/0909.0846))

* **Fivebrane structure** the worldvolume anomaly for the super-5-brane in [[dual heterotic string theory]] vanishes (essentially) when $X$ has [[Fivebrane structure]]. See there.


### Anomalous symmetry

#### Conformal anomaly

For the moment see [[Liouville cocycle]].



## References

The role of [[spin structure]]s as the qnomaly cancellation condition for the spinning particle is discussed in

* [[Edward Witten]], _Global anomalies in String theory_ in _Symposium on anomalies, geometry, topology_ , World Scientific Publishing, Singapore (1985)

The fundamental article for the role of the [[determinant line bundle]] in understanding the anomalies is

* M. F. Atiyah, I. M. Singer, _Dirac operators coupled to vector potentials_, Proc. Nat. Acad. Sci. USA __81__, 2597-2600 (1984)

A physicists' monograph:

* Reinhold A. Bertlmann, _Anomalies in quantum field theory_, Oxford Science Publ., 1996, 2000

A reference that very clearly identifies the mathematical nature of quantum anomalies for higher gauge theories is

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_ ([arXiv](http://arxiv.org/abs/hep-th/0011220))

[[!redirects anomaly]]


[[!redirects anomalies]]
[[!redirects quantum anomalies]]