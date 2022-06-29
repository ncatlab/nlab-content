
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Definition

A **closed cover** of a [[topological space]] $X$ is a collection $\{U_i \subset X\}$ of [[closed subsets]] of $X$ whose [[union]] equals $X$: $\cup_i U_i = X$. 

Often 
it is also required that every point $x \in X$ is in the [[interior]] of one of the $U_i$ (e.g  in [Floyd 1957](#Floyd57), but e.g. not in [Karoubi & Weibel 2016](#KaroubiWeibel16)).


## Properties
 {#Properties}

Closed covers can be obtained from [[open covers]] by forming the [[closed subset|closure]] of each of the [[open subsets]]. The result clearly satisfies the clause that every point is in the interior of one of the closed subsets.


## Related concepts

* [[open cover]]

* [[schedule]]

## References

### General


* Dragan Jankovi&#263;, Chariklia Konstadilaki, _On covering properties by regular closed sets_, Mathematica Pannonica, 7/1 (1996) 97-111 &lbrack;[pdf](http://www.kurims.kyoto-u.ac.jp/EMIS/journals/MP/index_elemei/mp07-1/mp07-1-097-111.pdf)&rbrack;

* {#KaroubiWeibel16} [[Max Karoubi]], [[Charles Weibel]], *On the covering type of a space*, L’Enseignement Mathématique, **62** 3/4 (2016) 457-474 &lbrack;[arXiv:1612.00532](https://arxiv.org/abs/1612.00532), [doi:10.4171/LEM/62-3/4-4](https://www.ems-ph.org/journals/show_abstract.php?issn=0013-8584&vol=62&iss=3&rank=4)&rbrack;


Applications of closed covers in [[Čech homology]]:

* {#Floyd57} [[Edwin E. Floyd]], *Closed coverings in Čech homology theory*, Trans. Amer. Math. Soc. **84** (1957) 319-337  &lbrack;[doi:10.1090/S0002-9947-1957-0087100-2](https://doi.org/10.1090/S0002-9947-1957-0087100-2), [pdf](http://www.ams.org/journals/tran/1957-084-02/S0002-9947-1957-0087100-2/S0002-9947-1957-0087100-2.pdf)&rbrack;

Related discussion is also in [this MO thread](http://mathoverflow.net/questions/24103/ech-cohomology-of-compact-spaces-via-closed-covers)

### Examples

In [[analytic geometry]], [[affinoid domains]] have [[closed sets]] as [[analytic spectra]] and hence the [[topological space]] underlying a [[Berkovich analytic spaces]] is equipped by a closed cover by affioid domains

* {#Berkovich09} [[Vladimir Berkovich]], _Non-archimedean analytic spaces_, lectures at the _Advanced School on $p$-adic Analysis and Applications_, ICTP, Trieste, 31 August - 11 September 2009 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Trieste_2009.pdf))


[[!redirects closed covers]]

[[!redirects closed covering]]
[[!redirects closed coverings]]
