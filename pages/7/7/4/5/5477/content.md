
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

A [[site]] being _locally and globally $\infty$-connected_ means that it satisfies sufficient conditions such that the [[(∞,1)-category of (∞,1)-sheaves]] over it is a [[locally ∞-connected (∞,1)-topos]] and a [[∞-connected (∞,1)-topos]].


## Definition

+-- {: .un_def}
###### Definition

A a [[site]] is **locally and globally $\infty$-connected** over [[∞Grpd]] 
if

* it has a [[terminal object]] *

* for every [[covering]] family $\{U_i \to X\}$ in $C$ 

  1. the [[Cech nerve]] $C(U) \in [C^{op}, sSet]$ is degreewise 
       a [[coproduct]] of [[representable functor|representables]];

  1. the [[simplicial set]] obtained by replacing each copy of 
     a representable by a point is [[contractible]], equivalently
     the [[colimit]] $\lim_\to : [C^{op}, sSet] \to sSet$ 
     of $C(U)$ has a [[weak homotopy equivalence]] to the point

     $$
       \lim_\to C(U) \stackrel{\simeq}{\to} *
       \,.
     $$
  
=--

## Properties

+-- {: .un_prop}
###### Proposition

The [[(∞,1)-sheaf (∞,1)-topos]] $Sh_{(\infty,1)}(C)$ over locally and globally $\infty$-conneted site $C$, regarded as an [[(∞,1)-site]], is a ([[n-localic (∞,1)-topos|1-localic]]) [[locally ∞-connected (∞,1)-topos]] and [[∞-connected (∞,1)-topos]], in that it comes with a trible of [[adjoint (∞,1)-functor]]s

$$
  (\Pi \dashv \Delta \dashv \Gamma) :
  Sh_{(\infty,1)}(C)
  \stackrel{\stackrel{\Pi}{\to}}{\stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \infty Grpd
$$

such that $\Pi$ preserves the [[terminal object]].

=--

+-- {: .proof}
###### Proof

We use the [[model structure on simplicial presheaves]] to [[locally presentable (∞,1)-category]] $Sh_{(\infty,1)}(C)$. 

Write $[C^{op}, sSet]_{proj}$ for the projective global model structure and $[C^{op}, sSet]_{proj,loc}$ for its [[Bousfield localization of model categories|left Bousfield localization]] at the set of morphisms $C(U) \to X$ for each covering family $\{U_i \to X\}$, and $[C^{op}, sSet]_{proj,loc}^\circ$ for the [[Kan complex]]-[[enriched category]] on the fibrant-cofibrant objects. By the discussion at [[model structure on simplicial presheaves]] we have

$$
  Sh_{(\infty,1)}(C) \simeq [C^{op}, sSet]_{proj, loc}^\circ
$$

and the [[adjoint (∞,1)-functor]]s in question are presented by [[Quillen adjunction]]s.

(...) (Rest to be transferred from [[∞-cohesive site]].)


=--

## Examples

* [[category of open subsets]] $Op(X)$ of a [[locally contractible space]] $X$;

* [[CartSp]], [[ThCartSp]].

## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / [[locally ∞-connected site]]

  * [[connected site]] / **∞-connected site**

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* [[local site]] / [[∞-local site]]

* [[cohesive site]], [[∞-cohesive site]]


[[!redirects ∞-connected site]]
