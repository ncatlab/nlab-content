
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
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

Write $SteinSp$ for the [[site]] of [[Stein spaces]] and write

$$
  \mathbb{C}Analytic\infty Grpd \coloneqq Sh_\infty(SteinSp)
$$

for the [[(∞,1)-sheaf (∞,1)-topos]] over that site. Objects in here may be thought of as [[∞-groupoids]] equipped with generated [[complex analytic geometry]] structure. This is the context of [[higher complex analytic geometry]].

## Properties

### Oka principle
 {#OkaPrinciple}

Discussion of the [[Oka principle]] in terms of $\mathbb{C}Analytic\infty Grpd$ is in ([Larusson 01](#Larusson01)).

Say that a [[complex manifold]] $X$ is an _[[Oka manifold]]_ if for every [[Stein manifold]] $\Sigma$ the canonical morphism

$$
  Maps_{hol}(\Sigma, X) \longrightarrow Maps_{top}(\Sigma, X)
$$

from the [[mapping space]] of [[holomorphic functions]] to that of [[continuous functions]] (both equipped with the [[compact-open topology]]) is a [[weak homotopy equivalence]].

+-- {: .num_theorem}
###### Theorem

This is the case precisely if $Maps_{hol}(-,X) \in Psh_\infty(SteinSp)$ satisfies [[descent]] with respect to [[finite set|finite]] [[covers]].

=--

([Larusson 01, theorem 2.1](#Larusson01))


## References


* {#Larusson01} [[Finnur Lárusson]], _Excision for simplicial sheaves on the Stein site and Gromov's Oka principle_ ([arXiv:math/0101103](http://arxiv.org/abs/math/0101103))

* [[Jacob Lurie]], section 4.4. of _[[Structured Spaces]]_


[[!redirects complex analytic ∞-groupoids]]

[[!redirects complex analytic infinity-groupoid]]
[[!redirects complex analytic infinity-groupoids]]
