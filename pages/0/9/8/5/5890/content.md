
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

Throughout, let $\mathcal{H}$ be a [[separable Hilbert space|separable]] infinite-dimensional [[complex numbers|complex]] [[Hilbert space]].

+-- {: .num_theorem}
###### Theorem
**(Kuiper's theorem)**

The [[group]] of [[bounded operator|bounded]] and [[invertible element|invertible]] [[linear operators]] $GL(\mathcal{H})$, regarded as a [[topological group]] under the [[norm topology]] or [[strong operator topology]] or [[weak operator topology]], is ([[weak homotopy equivalence|weakly]]) [[contractible]]. 

Similarly, the [[unitary group]] [[U(ℋ)|$\mathrm{U}(\mathcal{H})$]], being [[homotopy equivalence|homotopy equivalent]] to $GL(\mathcal{H})$ by the [[Gram-Schmidt process]], is also contractible. 

=--

The original paper [Kuiper 64](#Kuiper64) proved this group to be contractible in the 
[[norm topology]]; later Dixmier and Douady proved contractibility for the [[operator topology|strong operator topology]].  

Direct proofs for the unitary group:

Atiyah and Segal note in their paper on twisted K-theory that there is an easy proof of contractibility in the [[weak operator topology]] ([Atiyah & Segal 2004, Prop. A2.1](#AtiyahSegal04)).  One major difference in the topologies is that with the operator topology then it is a [[CW-complex]] but with the weak topology then it isn't even an [[ANR]]. 

Note that on [[U(ℋ)|$U(\mathcal{H})$]] the strong [[operator topology]] coincides with the [[compact open topology]] ([Schottenloher](#Schottenloher)), and with these topologies $U(\mathcal{H})$ is a topological group (the same is not true for $GL(\mathcal{H})$). In fact more is true: the compact open, strong and weak topologies *and* their $\ast$-counterparts all agree on $U(\mathcal{H})$, which in this topology is a [[Polish space|Polish]] group ([Espinoza-Uribe](#EspinozaUribe)).


## Related statements

* [[the infinite-dimensional sphere is weakly contractible]]

* [[U(ℋ)|$U(\mathcal{H})$]]

## References 

The original article

* {#Kuiper64} [[Nicolaas Kuiper]], *Contractibility of the unitary group in Hilbert space*, Topology, 3, 19-30 (1964)

* {#AtiyahSegal04} [[Michael Atiyah]], [[Graeme Segal]], _Twisted K-theory_, Ukrainian Math. Bull. **1**, 3 (2004) ([arXiv:math/0407054](http://arxiv.org/abs/math/0407054), [journal page](http://iamm.su/en/journals/j879/?VID=10), [published pdf](http://iamm.su/upload/iblock/45e/t1-n3-287-330.pdf))


* {#Schottenloher} [[Martin Schottenloher]], _The Unitary Group In Its Strong Topology_ ([arXiv:1309.5891](https://arxiv.org/abs/1309.5891)), Advances in Pure Mathematics **08** 05 (2018) ([doi:10.4236/apm.2018.85029](https://www.scirp.org/html/4-5301487_84967.htm))

* {#EspinozaUribe} [[Jesus Espinoza]], [[Bernardo Uribe]], _Topological properties of the unitary group_, JP Journal of Geometry and Topology **16** (2014) Issue 1, pp 45-55 ([arXiv:1407.1869](https://arxiv.org/abs/1407.1869), [journal](http://www.pphmj.com/abstract/8730.htm))


See also: 

* Wikipedia, _[Kuiper's theorem](http://en.wikipedia.org/wiki/Kuiper%27s_theorem)_


[[!redirects Kuiper theorem]]

