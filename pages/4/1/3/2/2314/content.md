
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

A _Deligne-Mumford stack_ (after [Deligne-Mumford 69](#DeligneMumford69)) is the analogue in [[algebraic geometry]] of what in [[differential geometry]] is an [[orbifold]]: a [[quotient stack]] of a [[scheme]] over the [[étale site]] all whose [[automorphism group]]s are [[finite group]]s.

These are what originally were called [[algebraic stacks]]. The latter term nowadays often refers to the more general notion of [[Artin stacks]], where the [[automorphism groups]] ([[isotropy groups]]) are allowed to be more general [[algebraic groups]]. This case is the algebraic version of the general notion of [[geometric stack]].

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

The concept (cf. also *[[algebraic stack]]*) is due to:

* {#DeligneMumford69} [[Pierre Deligne]], [[David Mumford]], *The irreducibility of the space of curves of given genus*, Publications Math&#233;matiques de l'IH&#201;S (Paris) **36**   (1969) 75-109 &lbrack;[doi:10.1007/BF02684599](https://doi.org/10.1007/BF02684599), [numdam:PMIHES_1969__36__75_0](http://www.numdam.org/item?id=PMIHES_1969__36__75_0)&rbrack;

Review in the general context of [[algebraic stacks]]:

* [[Angelo Vistoli]], _Grothendieck topologies, fibered categories and descent theory_ &lbrack;[math.AG/0412512](http://arxiv.org/abs/math/0412512), [MR2223406](http://www.ams.org/mathscinet-getitem?mr=2223406)&rbrack;  in: Fantechi et al. (eds.), _Fundamental algebraic geometry. Grothendieck's [[FGA explained]]_, Mathematical Surveys and Monographs __123__, Amer. Math. Soc. (2005) 1-104 &lbrack;[ISBN:978-0-8218-4245-4](https://bookstore.ams.org/surv-123-s), [MR2007f:14001](http://www.ams.org/mathscinet-getitem?mr=2007f:14001)&rbrack;  

and with emphases on the relation to [[orbifolds]]:

* {#Kresch09} [[Andrew Kresch]], _On the geometry of Deligne-Mumford stacks_ ([doi:10.5167/uzh-21342](https://doi.org/10.5167/uzh-21342), [pdf](https://www.zora.uzh.ch/id/eprint/21342/1/geodm.pdf)), in:  D. Abramovich, A. Bertram, L. Katzarkov, R. Pandharipande, M. Thaddeus (eds.) _Algebraic Geometry: Seattle 2005_, Proceedings of Symposia in Pure Mathematics 80, Providence, Rhode Island: American Mathematical Society 2009, 259-271 ([pspum-80-1](https://bookstore.ams.org/pspum-80-1))

Characterization of higher Deligne-Mumford stacks (see at *[[generalized scheme]]*):

* [[Jacob Lurie]], _Representability theorems_ &lbrack;[pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XIV.pdf)&rbrack;

* {#Carchedi13} [[David Carchedi]], _Higher Orbifolds and Deligne-Mumford Stacks as Structured Infinity Topoi_  &lbrack;[arXiv:1312.2204](http://arxiv.org/abs/1312.2204)&rbrack;

[[!redirects Deligne-Mumford stacks]]

