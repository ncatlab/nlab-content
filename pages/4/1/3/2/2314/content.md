#Contents#

* automatic table of contents goes here
{:toc}

# Idea #

A _Deligne-Mumford stack_ is a [[stack]] (in the context of [[algebraic geometry]]) with the special property that it is covered, in a sense, by an ordinary [[algebraic space]].

#Definition#

Given a [[scheme]] $S$. A $S$-[[stack]] $X$ (i.e under the [[Grothendieck construction]] a [[fibered category|category fibered]] in [[groupoid]]s over $(Aff/S)_{et}$ satisfying [[descent]]) is **Deligne-Mumford** when it has a [[representable morphism of stacks|representable]], separable and quasi-compact diagonal $\Delta: X\rightarrow X\times_S X$ and a covering $P:A\rightarrow X$ which is [[surjection|surjective]], representable and [[etale map|etale]], by an [[algebraic space]] $A$.
 
Deligne-Mumford stacks correspond to [[moduli space|moduli problems]] in which the objects being parametrized have finite [[automorphism group]]s. See also [[algebraic stack]].


## as a generalized scheme ##

From the perspective of [[derived algebraic geometry]]s a Deligne-Mumford stack is a special case of a [[generalized scheme]] (or $G$-scheme for $G$ a [[geometry (for structured (∞,1)-toposes)]]) as follows:


+-- {: .un_defn}
###### Definition (etale geometry)

[[Structured Spaces|StSp Def 2.6.12]]

For $k$ a commutative [[ring]], let the **etale geometry** $G_{et}(k)$ be the [[geometry (for structured (∞,1)-toposes)]] defined as follows:

* the underlying [[(∞,1)-category]] is is ordinary [[category]]

  $$
    G_{et}(k) := (CRing_k^{fin})^{op}
  $$

  of finitely presented [[affine scheme]]s over $k$;

* a morphsim $f : Spec(A) \to Spec(B)$ is _admissibale_ precisely if the corresponding morphism $f^* : B \to A$ of commutative $k$-[[algebra]]s is an [[etale map]];

* the [[Grothendieck topology]] on $G_{et}(k)$ is the restriction of the standard [[etale topology]].

=--

+-- {: .num_theorem}
###### Theorem

[[Structured Spaces|SrSp Thm. 2.6.16]]

An [[(∞,1)-presheaf]] $F : CRing_k \to \infty Grpd$ is a Deligne-Mumford stack precisely if it is [[representable functor|representable]] by a $G_{et}(k)$-[[generalized scheme]] $(X,O_X)$ such that $X$ is [[n-localic (∞,1)-topos|1-localic]].

=--


# DM stacks in moduli space theory #

An important source of DM-stacks are [[moduli space|moduli]] problems, resulting often in [[moduli stack]]s (or their derived versions). 

#References#

DM-stacks are introduced in

* P. Deligne, D. Mumford, "The irreducibility of the space of curves of given genus". Publications Math&#233;matiques de l'IH&#201;S (Paris) 36: 75&#8211;109 (1969) [numdam](http://www.numdam.org/numdam-bin/fitem?id=PMIHES_1969__36__75_0)
