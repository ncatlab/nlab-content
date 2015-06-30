
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Statement

Let $G$ be a [[finite group]] with [[order of a group|order]] ${\vert G\vert} \in \mathbb{N}$. 

+-- {: .num_theorem}
###### Theorem
**(Cauchy)**

If a [[prime number]] $p$ divides ${\vert G\vert}$, then equivalently

* $G$ has an element of [[order of an element|order]] $p$;

* $G$ has a [[subgroup]] of [[order of a group|order]] $p$.

=--

This result is not completely trivial. One route to this would go as follows: knowing that Sylow $p$-subgroups $H$ of $G$ exist (see [[class equation]] for a proof), any nontrivial element $h$ of $H$ would be of order $p^r$ for some $r \gt 0$, and then $h^{p^{r-1}}$ would be the desired element. Come to think of it, it's actually an immediate consequence of the theorem [here](/nlab/show/class+equation#ppower). But see [McKay](#McKay) for a snappier proof. 

+-- {: .num_remark} 
###### Remark 
Cauchy had claimed a proof of his eponymous theorem in 1845, but in fact his proof had a gap. See [Meo](#Meo) for a historical discussion. 
=-- 

## References

* James McKay, _Another proof of Cauchy's group theorem_, American Math. Monthly, 66 (1959), p. 119. 
 {#McKay} 

* M. Meo, _The mathematical life of Cauchy's group theorem_, Historia Mathematica Volume 31, Issue 2 (May 2004), 196&#8211;221. ([web](http://www.sciencedirect.com/science/article/pii/S031508600300003X)) 
 {#Meo} 


[[!redirects Cauchy theorem]]
[[!redirects Cauchy's theorem]]
[[!redirects Cauchy's theorem]]
[[!redirects Cauchy\'s theorem]]

[[!redirects Cauchy group theorem]]
[[!redirects Cauchy's group theorem]]
[[!redirects Cauchy's group theorem]]
[[!redirects Cauchy\'s group theorem]]
[[!redirects Cauchy's theorem (group theory)]]
