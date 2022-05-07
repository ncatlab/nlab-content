
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


There are several theorems by [[Serre]] which deserve to be called "finiteness theorems".

## In homotopy theory
 {#InHomotopyTheory}

On the [[homotopy groups of spheres]]:

+-- {: .num_theorem }
###### Theorem
**(Serre finiteness theorem)**

The [[homotopy groups of spheres]] $\pi_{n+k}(S^k)$, for $k \geq 1$, are [[finite groups]] (in fact [[finite abelian groups]]), hence pure [[torsion subgroup|torsion]], *except*

1. for $n = 0$ in which case $\pi_k(S^k) = \mathbb{Z}$ is the [[integers]];

1. $k = 2m$ and $n = 2m -1$ in which case

   $$
     \pi_{4m - 1}(S^{2m}) \simeq \mathbb{Z} \oplus F_m
   $$

   for $F_m$ some [[finite group]].

=--


([Serre 53](#Serre53), see [Ravenel 86, Chapter I, Lemma 1.1.8](#Ravenel86))

+-- {: .num_remark }
###### Remark

The non-torsion element in $\pi_{4k-1}(S^{2k})$ may be seen explicitly in the [[minimal Sullivan model]] for the [[rational n-sphere|rational 2k-sphere]], see there for more.

=--

## Related concepts

* [[Nishida nilpotence theorem]]

## References

The original proof is due to

* {#Serre53} [[Jean-Pierre Serre]], _Groupes d'homotopie et classes de groupes abelien_, Ann. of Math. 58 (1953), 258&#8211;294 ([jstor:1969789](https://www.jstor.org/stable/1969789))

The statement is reviewed in

* [[Douglas Ravenel]], Chapter I, Theorem 1.1.8 in: _[[Complex cobordism and stable homotopy groups of spheres]]_. Academic Press Orland (1986) reprinted as: AMS Chelsea Publishing, Volume 347 (2004) ([ISBN:978-0-8218-2967-7](https://bookstore.ams.org/chel-347-h), [webpage](http://www.math.rochester.edu/people/faculty/doug/mu.html), [pdf](https://web.math.rochester.edu/people/faculty/doug/mybooks/ravenel.pdf))
 

An entirely different proof, using only elementary concepts, is given in 

* S. S. Podkorytov, _An Alternative Proof of a Weak Form of Serre's Theorem_, Journal of Mathematical Sciences July 2002, Volume 110, Issue 4, pp 2875&#8211;2881 ([doi:10.1023/A:1015370800473](https://doi.org/10.1023/A:1015370800473))

[[!redirects Serre finiteness theorems]]

