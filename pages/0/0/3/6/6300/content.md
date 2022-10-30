[[!redirects E-∞ operad]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An **$E_\infty$-operad** is a [[topological operad]] that is a [[homotopy theory|homotopy theoretic]] [[resolution]] of [[Comm]], the operad for [[commutative monoid]]s: an [[algebra over an operad]] over an $E_\infty$-operad is an [[E-∞ ring|E-∞ algebra]].

## Definition

The definition of $E_\infty$-operads depends a bit on which [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-category]] of [[(∞,1)-operad]]s one uses:

* abstractly, in the [[(∞,1)-category]] of [[(∞,1)-operad]]s, the operad [[Comm]] itself already _is_ an $E_\infty$-operad, in that its [[∞-algebras over an (∞,1)-operad]] are [[E-∞ ring|E-∞ algebras]];

* when presenting $(\infty,1)-Operad$ by the [[model structure on operads]] for [[topological operad]]s, forming the homotopy-algebras over any operad means forming the ordinary [[algebras over an operad]] for any of its cofibrant [[resolution]]s. Therefore one say: an $E_\infty$-operad is (any) cofibrant resolution of [[Comm]] in the standard [[model structure on operads]] over the [[model structure on topological spaces]].

## Properties

For every $E_\infty$-operad $P$, all the spaces $P_n$ are [[contractible]].

In fact,  _every_ [[topological operad]] $P$ for which $P_n \simeq *$ for all $n \in \mathbb{N}$ is weakly equivalent to [[Comm]]: because $Comm_n = *$ there is a unique morphism of operads (necessarily respecting the action of the [[symmetric group]])

$$
  P \to Comm
$$

and for each $n$ this is by assumption a [[weak homotopy equivalence]]

$$
  P_n \to Comm_n = *
$$

of topological spaces. 

The only extra condition on an operad $P$ with contractible operation spaces to be $E_\infty$ is that it is in addition _cofibrant_ . This imposes the condition that the [[action]] of the [[symmetric group]] $\Sigma_n \times P_n \to P_n$ in each degree is _free_ .

## Examples

* In some sense the [[universal construction|universal]] model for an $E_\infty$-operad is the [[Barratt-Eccles operad]].

* The [[little k-cubes operad]] for $k \to \infty$ is $E_\infty$.

## Related concepts

* [[A-∞ operad]]

* [[E-∞ ring]]


[[!redirects E-infinity operad]]
[[!redirects E-∞ operad]]
[[!redirects E-infinity-operad]]
[[!redirects E-∞-operad]]
