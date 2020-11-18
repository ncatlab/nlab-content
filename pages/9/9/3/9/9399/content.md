
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

# Equifibered natural transformation

* table of contents
{: toc}

## Definition

Let $F,G:C\to D$ be [[functors]].  A [[natural transformation]] $\alpha:F\to G$ is **equifibered** (also called **cartesian**) if for any [[morphism]] $f:x\to y$ in $C$, the naturality square

$$\array{ F x & \overset{F f}{\to} & F y\\
  ^{\alpha_x}\downarrow & & \downarrow^{\alpha_y} \\
  G x & \underset{G f}{\to} & G y}
$$
is a [[pullback]].

The name "equifibered" comes from the fact that since $\alpha_x$ is a pullback of $\alpha_y$, they must have [[isomorphism|isomorphic]] [[fibers]].  (Of course, if $C$ is not [[connected category|connected]], then being equifibered does not imply that *all* components of $\alpha$ have isomorphic fibers.)

There is an evident generalization to natural transformations between [[higher category theory|higher categories]].

## Properties

* Given a functor $G:C\to D$, if $C$ has a [[terminal object]] $1$, then to give a functor $F$ and an equifibered transformation $F\to G$ is equivalent to giving a single object $F1$ and a morphism $F1 \to G1$.  The rest of $F$ can then be constructed uniquely by taking pullbacks.  This construction is important in the theory of [[clubs]].



[[!include colimits of equifibered transformations -- section]]



## Related pages

* [[cartesian monad]]
* [[club]]
* [[polynomial functor]]
* [[van Kampen colimit]]

## References 

In the context of [[category theory]] the concept is discussed in

* [[Aurelio Carboni]] and [[Peter Johnstone]], *Connected limits, familial representability and Artin glueing*, Mathematical Structures in Computer Science, Vol. 5 Iss. 4, Cambridge U. Press (December 1995), 441-459. 
([doi:10.1017/S0960129500001183](https://doi.org/10.1017/S0960129500001183) [web](https://www.cambridge.org/core/journals/mathematical-structures-in-computer-science/article/div-classtitleconnected-limits-familial-representability-and-artin-glueingdiv/54E93903F7D7321B98B64AE7CB3E7AE0)) 

* [[Tom Leinster]], *Higher Operads, Higher Categories*, Cambridge University Press 2003. ([arXiv:math/0305049](https://arxiv.org/abs/math/0305049)) 

In the context of [[(infinity,1)-categories]] (with an eye towards [[(infinity,1)-toposes]]) the concept is considered in

* {#Rezk10} [[Charles Rezk]], p. 9 of _Toposes and homotopy toposes_ (2010) ([pdf](http://www.math.uiuc.edu/~rezk/homotopy-topos-sketch.pdf))

* {#Rezk14} [[Charles Rezk]], p. 2 of _When are homotopy colimits compatible with homotopy base change?_ (2014) ([pdf](http://www.math.uiuc.edu/~rezk/i-hate-the-pi-star-kan-condition.pdf))

[[!redirects equifibered natural transformation]]
[[!redirects equifibered natural transformations]]
[[!redirects equifibred natural transformation]]
[[!redirects equifibred natural transformations]]
[[!redirects cartesian natural transformation]]
[[!redirects cartesian natural transformations]]



