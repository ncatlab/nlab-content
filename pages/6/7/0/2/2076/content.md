
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The theorem ([B&#233;nabou-Roubaud 70](#BenabouRoubaud70)) identifies the [[Eilenberg-Moore category]] of algebras over the [[monad]] induced from a [[base change]] [[adjoint triple]] for some [[bifibration]] satisfying the [[Beck-Chevalley condition]] with the [[category of descent data]] along this morphism. This is the basis for the monadic reformulation of [[descent]] theory: [[monadic descent]].


## Context

A [[functor]] $P : F\to A$ is a [[Grothendieck opfibration]] if $P^{op}:F^{op}\to A^{op}$ is a [[Grothendieck fibration]], and a functor $P:F\to A$ is a __[[bifibration]]__ if $P$ is both a Grothendieck opfibration and fibration (no additional compatibility asked!). Thus we can talk about [[cartesian morphism|cartesian]] and [[cocartesian morphism|cocartesian]] arrows in $F$.

Given a bifibration  $P : F\to A$, automatically for any morphism $a:A_1\to A_0$ in $A$ the "inverse image" (or "pullback" or "restriction") functor $a^*:F(A_0)\to F(A_1)$ is [[right adjoint]] to the "pushforward" functor $a_!:F(A_1)\to F(A_0)$; with unit $\eta^a : Id_{F(A_1)} \to a^* a_!$ and counit $\epsilon^a : a_! a^* \to Id_{F(A_0)}$.

(Note that in [[topos theory]] and [[algebraic geometry]], functors $a^*$ called "[[inverse images]]" usually have *right* adjoints $a_*$.  This situation can be reconciled with the setup of bifibrations either by taking fiberwise opposites, so that left and right adjoints are switched, or by taking opposites of both the base and total categories, so that the direct and inverse images are switched.  However, there are also many bifibrations arising in other contexts in which $a^*$ has both a left adjoint $a_!$ *and* a right adjoint $a_*$, although the latter cannot then be described cleanly in fibrational terms.)

The [[adjunction]] $a_!\dashv a^*$ generates a [[monad]] $\mathbf{T}^a=(T^a,\mu^a,\eta^a)$ in the usual way: the functor is $T^a = a^* a_!\colon  F(A_1)\to F(A_1)$, the multiplication is $\mu^a = a^* \epsilon^a a_!\colon  T^a \circ T^a \to T^a$, and the unit is just the unit of the adjunction.  Denote by $F^a$ the [[Eilenberg–Moore category]] $F(A_1)^{\mathbf{T}^a}$ of modules (algebras) over the monad $\mathbf{T}^a$, with canonical forgetful functor $U^{\mathbf{T}} \colon  F^a \to F(A_1)$ and canonical [[comparison functor]] $\Phi^a \colon F(A_0) \to F^a$.

Now we assume that $A$ has [[pullbacks]], and that $P$ satisfies what is nowadays called the **[[Beck-Chevalley property]]**, namely that for each commutative square

$$
  \array{
    N_0 & \stackrel{\chi'}\leftarrow & N_1
     \\
     {}^{\mathllap{k_0}}\downarrow 
     && 
     \downarrow^{\mathrlap{k_1}}
     \\
     M_0 &\stackrel{\chi}\leftarrow & M_1
  }
$$

in $F$ such that its image in $A$ is a [[pullback]] square, if $\chi$ and $\chi'$ are cartesian and $k_0$ is cocartesian then $k_1$ is cocartesian.

An equivalent way to state the condition is that for any pullback square

$$
  \array{
    x & \overset{a}{\to} & y
    \\
    {}^{\mathllap{c}} \downarrow 
    && 
   \downarrow^{\mathrlap{d}}
   \\
   z & \underset{b}{\to} & w
  }
$$

in $A$, the canonical transformation $c_! a^* \to b^* d_!$ is an isomorphism.   In the B&#233;nabou--Roubaud paper this is called the *Chevalley property* and said to make $P$ into a *Chevalley functor*.


Denote by $A_2 :=A_1\times_{A_0}A_1$ the pullback of $a$ along itself, with the canonical projections $a_1,a_2\colon A_2\to A_1$.  Now consider the lift of the cartesian square defining $A_2$ to $F$ in such a way that $a_1$ is lifted to a cartesian arrow, $a_2$ to a cocartesian arrow, and $a$ to a cocartesian arrow.  Then by the universality there is a lift of $a$ completing the square, and by the Beck--Chevalley property it is cartesian. Together with the isomorphism given by adjunction this gives a morphism

$$
K^a: Hom_{F(A_2)}(a_1^*(M_1),a_2^*(M_1))\to Hom_{F(A_1)}(T^a(M_1),M_1).
$$ 

One checks that an invertible morphism $\phi\colon a_1^*(M_1)\to a_2^*(M_1)$ satisfies the cocycle equation 
(making it into a [[descent]] datum) iff $K^a(\phi)$ is an action of $\mathbf{T}^a$ on $M_1$, and similarly for the unitality axiom.

## The theorem

Denote by $Desc(a)$ the category of [[descent]] data for the fibration $P$ along the morphism $a$; it comes with canonical functors 

$$
  \Psi^a\colon F(A_0)\to Desc(a)
$$ 

and 

$$
  U^a\colon Desc(a)\to F(A_1)
  \,.
$$

The __B&#233;nabou--Roubaud theorem__ asserts that this induces an [[equivalence of categories]] between $Desc(a)$ and $F^a$.  

In addition, this equivalence satisfies some naturality properties, including that it commutes appropriately with the canonical functors to the fibers $F(A_0)$ and $F(A_1)$. Combining this theorem with Beck's [[monadicity theorem]], it becomes a practical tool for establishing a descent property in bifibrations, with variants in some other setups (to be covered later).

There are several characterizations of a [[Beck-Chevalley property]] for bifibrations:

+-- {: .un_prop}
###### Proposition
(Du&#353;ko Pavlovi&#263;, in Category theory Como 1990, LNM 1488, Springer 1991)

Let $p: F\to B$ be a bifibration, $Q = (f,g,s,t)$ a square in $B$ such that $f\circ g = s\circ t$, and $\Theta = (\phi, \gamma, \sigma, \theta)$ a square in $F$ such that $\phi\circ\gamma=\sigma\circ\theta$, with $p(\phi)=f$, $p(\gamma)=g$, $p(\sigma)=s$ and $p(\theta)=t$. The following conditions are equivalent:

a) if $\theta$ and $\phi$ are cartesian and if $\sigma$ is cocartesian *then* $\gamma$ must be cocartesian;

b) if $\sigma$ and $\gamma$ are cocartesian and if $\theta$ is cartesian *then* $\phi$ must be cartesian;

c) if $\theta$ is cartesian and if $\sigma$ is cocartesian *then* $\phi$ is cartesian iff $\gamma$ is cocartesian.

If some inverse image functors $f^*$ and $t^*$ and some direct image functors $g_!$ and $s_!$ are chosen,
then every square $\Theta$ over $Q$ satisfies conditions (a-c) iff there is a canonical natural isomorphism

d) $f^*\circ s_! \cong g_! \circ t^*$.
=--

## Related concepts

* [[Beck-Chevalley condition]]

* [[monadicity theorem]]

## References

The original article:

* {#BenabouRoubaud70} [[Jean Bénabou]], [[Jacques Roubaud]], _Monades et descente_, C. R. Acad. Sc. Paris, Ser. A **270**  (1970) 96-98 &lbrack;[gallica:12148/bpt6k480298g/f100](http://gallica.bnf.fr/ark:/12148/bpt6k480298g/f100), [[BenabouRoubaud-MonadesEtDescente.pdf:file]],   English translation (by [[Peter Heinig]]): [MO:q/279152](https://mathoverflow.net/q/279152)&rbrack;

See also:

* {#JanelidzeTholen94} [[George Janelidze]], [[Walter Tholen]], _Facets of Descent I_, Applied Categorical Structures 1994, Volume 2, Issue 3, pp 245-281

* {#JanelidzeTholen97} [[George Janelidze]], [[Walter Tholen]], _Facets of Descent II_, Applied Categorical Structures September 1997, Volume 5, Issue 3, pp 229-248


* X. Guo, thesis, p. 58 of _Monadicity, purity and descent equivalence_, [pdf](http://www.collectionscanada.gc.ca/obj/s4/f2/dsk2/ftp02/NQ59136.pdf)

There has been some historical discussion on this in the category list; Zoran's response is [here](http://mathlight.wordpress.com/2010/01/07/becks-theorem-vs-benabou-roubaud).

The following reference presents a proof for a (generalization) of the Bénabou-Roubaud Theorem (pages 435 and 436):

* [[Fernando Lucatelli Nunes]], *Pseudo-Kan extensions and descent theory*, TAC [33-15] (http://www.tac.mta.ca/tac/volumes/33/15/33-15abs.html)

[[!redirects Benabou-Roubaud theorem]]
[[!redirects Benabou–Roubaud theorem]]
[[!redirects Benabou--Roubaud theorem]]
[[!redirects Bénabou-Roubaud theorem]]
[[!redirects Bénabou–Roubaud theorem]]
[[!redirects Bénabou--Roubaud theorem]]

[[!redirects Bénabou-Roubaud's theorem]]
