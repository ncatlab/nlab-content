
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[site]] is **$\infty$-local** if it satisfies sufficient conditions for the [[(∞,1)-sheaf (∞,1)-topos]] over it to be a [[local (∞,1)-topos]].



## Definition

+-- {: .un_def}
###### Definition

A [[site]] $C$ is **$\infty$-local** if 

* it has a [[terminal object]];

* the [[limit]]-functor $\lim_\leftarrow : [C^{op}, sSet] \to$ [[sSet]]
  sends [[Cech nerve]] projections $C(U) \to X$ over [[covering]] families
  $\{U_i \to X\}$ to [[weak homotopy equivalence]]s:

  $$
    Hom_C(*, C(U)) \stackrel{\simeq}{\to} Hom_C(*,X)
    \,.
  $$

=--


+-- {: .un_remark}
###### Remark

If $C$ is also a [[strongly ∞-connected site]] then it is an [[∞-cohesive site]].

=--

## Proposition

+-- {: .un_prop}
###### Proposition

For $C$ an $\infty$-local site, the [[(∞,1)-sheaf (∞,1)-topos]] $Sh_{(\infty,1)}(C)$ over it is a [[local (∞,1)-topos]].

=--

The proof is currently at [[∞-cohesive site]]. To me moved here.

## Examples

* [[CartSp]], [[ThCartSp]]


## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / [[locally ∞-connected site]]

  * [[connected site]] / [[∞-connected site]]

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]] / **∞-local site**

* [[cohesive site]], [[∞-cohesive site]]


[[!redirects ∞-local site]]

[[!redirects ∞-local sites]]
[[!redirects infinity-local sites]]
