
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

Given a functor $G:C\to D$, if $C$ has a [[terminal object]] $1$, then to give a functor $F$ and an equifibered transformation $F\to G$ is equivalent to giving a single object $F1$ and a morphism $F1 \to G1$.  The rest of $F$ can then be constructed uniquely by taking pullbacks.  This construction is important in the theory of [[clubs]].

## Related pages

* [[cartesian monad]]
* [[club]]
* [[polynomial functor]]
* [[van Kampen colimit]]

[[!redirects equifibered natural transformation]]
[[!redirects equifibered natural transformations]]
[[!redirects equifibred natural transformation]]
[[!redirects equifibred natural transformations]]
[[!redirects cartesian natural transformation]]
[[!redirects cartesian natural transformations]]
