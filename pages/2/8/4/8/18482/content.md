
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called _Tate cohomology_ are [[cohomology groups]] $\widehat{H}(G,N)$ associated to a [[representation]] $N$ of a [[finite group]] $G$. In terms of the [[Tate spectrum]] $H N^{t G}$ of the [[Eilenberg-MacLane spectrum]] $H N$ of $N$, these may be expressed as its [[stable homotopy groups]]:

$$
  \widehat H^{-n}(G,N) \simeq \pi_n( H N^{t G})
  \,.
$$

(e.g. [Nikolaus-Scholze 17, p. 13](#NikolausScholze17))

What is called _(generalized) Farrell-Tate cohomology_ is a generalization of this construction to possibly infinite [[discrete groups]] and topological groups $G$.

(e.g. [Klein 02](#Klein02), [Nikolaus-Scholze 17, section I.4](#NikolausScholze17))

## History of the idea

Tate cohomology was introduced in [Tate52](#Tate52) by [[John Tate]] for the purposes of [[class field theory]]. When a finite group $G$ acts on an abelian group $A$, then there is a natural 'norm' map $N$ from $H_0(G, A)$ to $H^0(G,A)$, $a \mapsto \sum_g g a$.

Then the Tate cohomology groups are 

* $\hat{H}^n (G, A) = H^n(G, A)$, for $n \geq 1$.
* $\hat{H}^0 (G, A) = coker N$, for $n = 0$.
* $\hat{H}^{-1} (G, A) = ker N$, for $n = 0$.
* $\hat{H}^n (G, A) = H_{-(n+1)}(G, A)$, for $n \leq -2$.

In ([Farrell78](#Farrell78)), Farrell generalized this construction to possibly infinite [[discrete groups]] of finite [[virtual cohomological dimension]].

Later this was generalized further in ([Klein 02](#Klein02)) to any topological (or discrete) group $G$ and any naive $G$-spectrum $E$.

## References

* {#NikolausScholze17} [[Thomas Nikolaus]], [[Peter Scholze]], section I-4 of _On topological cyclic homology_ ([arXiv:1707.01799](https://arxiv.org/abs/1707.01799))

* {#Tate52} [[John Tate]], _The higher dimensional cohomology groups of class field theory_, Ann. of Math. (2), 1952, 56: 294&#8211;297.

* {#Farrell78} F. Thomas Farrell,  _An extension of Tate cohomology to a class of infinite groups_, J. Pure Appl. Algebra 10 (1977/78), no. 2, 153-161.

* {#Klein02} [[John Klein]], _Axioms for generalized Farrell&#8211;Tate cohomology_, 2002, [pdf](http://www.math.wayne.edu/~klein/tate.pdf)



[[!redirects Farrell-Tate cohomologies]]

[[!redirects Tate cohomology]]
[[!redirects Tate cohomologies]]
