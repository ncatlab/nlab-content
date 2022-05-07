[[!redirects model structure on categories with weak equivalences]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The [[model category]] structure on the [[category]] of [[category with weak equivalences|categories with weak equivalences]] is a model for the [[(∞,1)-category of (∞,1)-categories]].

Every [[category with weak equivalences]] $C$ presents under Dwyer-Kan [[simplicial localization]] a [[simplicially enriched category]] or alternatively under [[Charles Rezk]]'s _simplicial nerve_ a [[complete Segal space|Segal space]], both of which are incarnations of a corresponding [[(∞,1)-category]] $\mathbf{C}$ with the same objects of $C$, at least the 1-morphisms of $C$ and such that every weak equivalence in $C$ becomes a true equivalence ([[homotopy equivalence]]) in $\mathbf{C}$.

By the work of Barwick and Kan, there is a model structure on relative categories presenting the (∞,1)-category of simplicial spaces.

## Details

For the purposes of the present entry, a [[category with weak equivalences]] means the bare minimum of what may reasonably go by that name: 

**Definition** A [[relative category]] $(C,W)$ is a [[category]] $C$ equipped with a choice of [[wide subcategory]] $W$.

A morphism in $W$ is called a **weak equivalence** in $C$. Notice that we do not require here that these weak equivalence satisfy [[category with weak equivalences|2-out-of-3]], nor even that they contain all [[isomorphisms]]. 

A morphism $(C_1,W_1) \to (C_2,W_2)$ of relative catgeories is a [[functor]] $C_1 \to C_2$ that preserves weak equivalences.

Write $RelCat$ for the [[category]] of relative categories and such morphisms between them.

### Model category structure

+-- {: .num_theorem}
###### Theorem
The subdivided nerve of Barwick-Kan induces a right [[transferred model structure]]
on $RelCat$ such that there is a Quillen equivalence
$$
  K_\xi : sSet^{\Delta^{\op}}_{Reedy} \leftrightarrows (RelCat, BK) : N_\xi
$$
Both functors preserve and reflect weak equivalences, and the adjunction unit and counit are natural weak equivalences. The simplicial nerve $N$ is naturally weakly equivalent to $N_\xi$.

Furthermore, this all remains true if the Reedy model structure on $sSet^{\Delta^{\op}}$ is replaced with any of its Bousfield localizations.

The model structure on RelCat is left proper. It is also right proper when the model structure on $ sSet^{\Delta^{\op}}$ is right proper.
=--
+-- {: .proof}
###### Proof
The existence and properness of the model structure and the Quillen equivalence is Theorem 6.1 of [Barwick-Kan](#BarKan), as is the fact $N_\xi$ preserves and reflects weak equivalences.

Proposition 10.3 shows the adjunction unit is a natural weak equivalence.
That the counit is a natural weak equivalence follows by considering the triangle identity, 3-for-2, and the fact $N_\xi$ reflects weak equivalences
$$
N_\xi C \xrightarrow{\eta N_\xi C} N_\xi K_\xi N_\xi C
\xrightarrow{N_\xi \varepsilon C} N_\xi C
$$
Finally, by considering the diagram
$$
 \array{
  X & \stackrel{\eta}{\to} & N_\xi K_\xi X
  \\
  \downarrow f && \downarrow
  \\
  Y & \stackrel{\eta}{\to} & N_\xi K_\xi Y
 }
$$
we see $f$ is a weak equivalence iff $N_\xi K_\xi f$ is,
and iff $K_\xi f$ is.
=--

In particular, Rezk's complete Segal space structure on bisimplicial sets is a Bousfield localization of the Reedy model structure, so we can define:

+-- {: .num_defn}
###### Definition
Let $(RelCat, Rezk)$ denote the model structure corresponding to the complete
Segal spaces.
=--

+-- {: .num_theorem}
###### Theorem
The localization $L(RelCat, Rezk) \simeq (\infty,1)Cat$ is the ∞-localization functor $(C,W) \mapsto L(C, W)$ inverting the weak equivalences
=--

+-- {: .proof}
###### Proof
We will see below that we can compute this through the map $(C,W) \to (NC, NW)$ to marked simplicial sets. Suppose we're given a fibrant replcaement $(NC, NW) \to Y^\natural$. Since $NC$ is a quasi-category, composition induces an equivalence for every quasi-category $Z$
$$
  Fun(Y, Z) \simeq Map^\flat(Y^\natural, Z^\natural)
  \to Map^\flat((NC, NW), Z^\natural) \simeq Fun_{NW}(NC, Z)
$$
thus $Y$ satisfies the universal property of $L(NC, NW)$.
=--

It is shown in [Meier](#Meier) that [[categories of fibrant objects]] are fibrant in this model structure.

### Compatibility with other models for (∞,1)-categories

One often uses the [[simplicial localization|hammock localization]] $L^H : RelCat \to sSetCat$, where $sSetCat$ is given the Bergner model structure whose weak equivalences are the Dwyer-Kan equivalences: i.e. the local weak homotopy equivalences.

+-- {: .num_prop}
###### Proposition

A functor $f$ in $RelCat$ is a Rezk equivalence iff $L^H(f)$ is a Dwyer-Kan equivalence.
=--
This is main theorem 1.4 of [Barwick-Kan](#RezkIsDK).


The idea underlying marked simplicial is directly analogous to the idea underlying relative categories. In fact, the functor $RelCat \to sSet^+ : (C,W) \to (NC, NW)$ preserves and reflects equivalences, since

+-- {: .num_prop}
###### Proposition
Let $R$ be a fibrant replacement in $sSetCat$. Then the natural transformation
$(NC, NW) \mapsto NRL^H(C,W)^\natural$ of marked simplicial sets is a natural weak equivalence.
=--
This is theorem 1.2.1 of [Hinich 13](#Hinich13)


### Nerve functors

The compatibility of the various nerve and simplicial localization functors is in section 1.11 of 

* [[Clark Barwick]] and [[Dan Kan]], _A characterization of simplicial localization functors_ ([arXiv:math/1012.1540](http://arxiv.org/abs/1012.1540))

## References

* [[Clark Barwick]] and [[Dan Kan]], 

  * {#BarKan} _Relative categories: another model for the homotopy theory of homotopy theories_ ([arXiv:math/1011.1691](http://arxiv.org/abs/1011.1691))

  * _A characterization of simplicial localization functors_ ([arXiv:math/1012.1540](http://arxiv.org/abs/1012.1540))

  * {#RezkIsDK} _In the category of relative categories the Rezk equivalences are exactly the DK-equivalences_ ([arXiv:math/1012.1541](http://arxiv.org/abs/1012.1541))

  * _A Thomason-like Quillen equivalence between quasi-categories and relative categories_ ([arXiv:math/1101.0772](http://arxiv.org/abs/1101.0772))

  * _Partial model categories and their simplicial nerves_ ([arXiv:math/1102.2512](http://arxiv.org/abs/1102.2512))

* {#Hinich13} [[Vladimir Hinich]] *Dwyer-Kan Localization Revisited*, 
Homology, Homotopy and Applications Volume 18 (2016) Number 1 ([arXiv:1311.4128](https://arxiv.org/abs/1311.4128), [doi:10.4310/HHA.2016.v18.n1.a3](https://dx.doi.org/10.4310/HHA.2016.v18.n1.a3))

* Lennart Meier, *Fibration Categories are Fibrant Relative Categories*, [arxiv](https://arxiv.org/abs/1503.02036)
 {#Meier}

[[!redirects Barwick-Kan equivalence]]
[[!redirects Barwick–Kan equivalence]]
