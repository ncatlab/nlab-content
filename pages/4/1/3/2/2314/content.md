
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

A _Deligne-Mumford stack_ is the analogue in [[algebraic geometry]] of what in [[differential geometry]] is an [[orbifold]]: a [[stack]] quotient of a [[scheme]] over the [[étale site]] all whose [[automorphism group]]s are [[finite group]]s.

These are what originally were called [[algebraic stack]]s. The latter term nowadays often refers to the more general notion of [[Artin stack]], where the automorphism groups are allowed to be more generally [[algebraic group]]s. This case is the algebraic version of the general notion of [[geometric stack]].

## Definition

Given a [[scheme]] $S$. A $S$-[[stack]] $X$ (i.e under the [[Grothendieck construction]] a [[fibered category|category fibered]] in [[groupoid]]s over $(Aff/S)_{et}$ satisfying [[descent]]) is **Deligne-Mumford** when it has a [[representable morphism of stacks|representable]], separable and quasi-compact diagonal $\Delta: X\rightarrow X\times_S X$ and a covering $P:A\rightarrow X$ which is [[surjection|surjective]], representable and [[etale map|etale]], by an [[algebraic space]] $A$.
 
Deligne-Mumford stacks correspond to [[moduli space|moduli problems]] in which the objects being parametrized have finite [[automorphism group]]s. See also [[algebraic stack]].


### As a generalized scheme 

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

* a morphsim $f : Spec(A) \to Spec(B)$ is _admissible_ precisely if the corresponding morphism $f^* : B \to A$ of commutative $k$-[[algebra]]s is an [[etale map]];

* the [[Grothendieck topology]] on $G_{et}(k)$ is the restriction of the standard [[etale topology]].

=--

+-- {: .num_theorem}
###### Theorem

[[Structured Spaces|SrSp Thm. 2.6.16]]

An [[(∞,1)-presheaf]] $F : CRing_k \to \infty Grpd$ is a Deligne-Mumford stack precisely if it is [[representable functor|representable]] by a $G_{et}(k)$-[[generalized scheme]] $(X,O_X)$ such that $X$ is [[n-localic (∞,1)-topos|1-localic]].

=--


## In moduli space theory 

An important source of DM-stacks are [[moduli space|moduli]] problems, resulting often in [[moduli stack]]s (or their derived versions). 

## Related concepts

* [[geometric stack]]

  * [[algebraic stack]]

    * **Deligne-Mumford stack**

      [[GIT-stable point]], [[geometric invariant theory]]

    * [[Artin stack]]

* [[Deligne-Mumford compactification]]

## References

DM-stacks are introduced in

* [[Pierre Deligne]], D. Mumford, _The irreducibility of the space of curves of given genus_ . Publications Math&#233;matiques de l'IH&#201;S (Paris) 36: 75&#8211;109 (1969) [numdam](http://www.numdam.org/numdam-bin/fitem?id=PMIHES_1969__36__75_0)

Characterization of higher Deligne-Mumford stacks (see [[generalized scheme]]) are in

* [[Jacob Lurie]], _Representability theorems_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XIV.pdf))

* {#Carchedi13}[[David Carchedi]], _Higher Orbifolds and Deligne-Mumford Stacks as Structured Infinity Topoi_ , arXiv1312.2204 (2013). ([pdf](http://arxiv.org/pdf/1312.2204v1.pdf))

[[!redirects Deligne-Mumford stacks]]