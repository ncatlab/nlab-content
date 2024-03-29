
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#

* automatic table of contents goes here
{:toc}

## Idea

An **algebraic stack** is essentially a [[geometric stack]] on the [[étale site]]. 

Depending on details, this is a [[Deligne-Mumford stack]] or a more general [[Artin stack]] in the traditional setup of [[algebraic space]]s.

## Definition

Let $C_{fppf}$ be the [[fppf-site]] and $\mathcal{E} = Sh_{(2,1)}(C_{fppf})$
the [[(2,1)-topos]] of [[stack]]s over it.


+-- {: .un_defn}
###### Definition

An **algebraic stack** is

* an object $\mathcal{X}\in Sh_{(2,1)}(C_{fppf})$;

* such that 

  1. the [[diagonal]] $\mathcal{X} \to \mathcal{X} \times \mathcal{X}$
  is [[representable morphism of stacks|representable]] by [[algebraic space]]s;

  1. there exists a [[scheme]] $U \in Sh(C_{fppf}) \hookrightarrow Sh_{(2,1)}(C_{fppf})$ and a morphism $U \to \mathcal{X}$ which is a surjective and
     [[smooth morphism of schemes|smooth morphism]]. 

=--

This appears in this form as ([deJong, def. 47.12.1](#deJong)).

+-- {: .un_defn}
###### Definition

A **smooth algebraic groupoid** is an [[internal groupoid]] in [[algebraic space]]s such that source and target maps are [[smooth morphism of schemes|smooth morphisms]].

=--

This appears as ([deJong, def. 47.16.2](#deJong)).

Notice that every [[internal groupoid]] in [[algebraic spaces]] represents a [[(2,1)-presheaf]] on the [[fppf-site]]. We shall not distinguish between the groupoid and the [[stackification]] of this presheaf, called the **quotient stack** of the groupoid.

+-- {: .un_theorem}
###### Theorem

Every algebraic stack is equivalent to a smooth algebraic groupoid and every smooth algebraic groupoid is an algebraic stack.

=--

This appears as ([deJong, lemma 47.16.2, theorem 47.17.3](#deJong)).



## Properties

* [[Tannaka duality for geometric stacks]].


## Examples

[[orbifold|Orbifolds]] are an example of an [[Artin stack]]. For orbifolds the stabilizer groups are [[finite group]]s, while for Artin stacks in general they are [[algebraic group]]s. 

## Generalizations

### Noncommutative spaces 

A noncommutative generalization for [[Q-category|Q-categories]] instead of [[Grothendieck topology|Grothendieck topologies]], hence applicable in noncommutative geometry of Deligne--Mumford and Artin stacks can be found in ([KontsevichRosenberg](#KontsevichRosenberg)).


## Examples

* [[projective stack]]

## Related concepts

* [[stack]], [[moduli stack]]

* [[lisse-étale site]]

* [[geometric stack]]

  * **algebraic stack**

  * [[topological stack]]

  * [[differentiable stack]]

  * [[complex analytic stack]]

* [[geometric ∞-stack]]


## References

The original articles:

* {#DeligneMumford69} [[Pierre Deligne]], [[David Mumford]], *The irreducibility of the space of curves of given genus*, Publications Math&#233;matiques de l'IH&#201;S (Paris) **36**   (1969) 75-109 &lbrack;[doi:10.1007/BF02684599](https://doi.org/10.1007/BF02684599), [numdam:PMIHES_1969__36__75_0](http://www.numdam.org/item?id=PMIHES_1969__36__75_0)&rbrack;

  > (cf. *[[Deligne-Mumford stack]]*)

* [[Michael Artin]], *Versal deformations and algebraic stacks*, Invent Math **27** (1974) 165–189 &lbrack;[doi:10.1007/BF01390174](https://doi.org/10.1007/BF01390174), [eudml:142310](https://eudml.org/doc/142310),  [pdf](http://math.uchicago.edu/~drinfeld/Artin_on_stacks.pdf)&rbrack;    

  > (cf. *[[Artin stack]]*)

Early review:

* [[Angelo Vistoli]], Appendix of: _Intersection theory on algebraic stacks and on their moduli spaces_, Inventiones mathematicae **97** (1989) 613–670 &lbrack;[doi:10.1007/BF01388892](https://doi.org/10.1007/BF01388892)&rbrack;

Monographs and review:

* {#LaumontMoret-Bailly} [[Gérard Laumon]], [[Laurent Moret-Bailly]], _Champs alg&#233;briques_, Ergebn. der Mathematik und ihrer Grenzgebiete **39**, Springer (2000) &lbrack;[doi:10.1007/978-3-540-24899-6](https://doi.org/10.1007/978-3-540-24899-6)&rbrack;

* [[Angelo Vistoli]], _Grothendieck topologies, fibered categories and descent theory_ &lbrack;[math.AG/0412512](http://arxiv.org/abs/math/0412512), [MR2223406](http://www.ams.org/mathscinet-getitem?mr=2223406)&rbrack;  in: Fantechi et al. (eds.), _Fundamental algebraic geometry. Grothendieck's [[FGA explained]]_, Mathematical Surveys and Monographs __123__, Amer. Math. Soc. (2005) 1-104 &lbrack;[ISBN:978-0-8218-4245-4](https://bookstore.ams.org/surv-123-s), [MR2007f:14001](http://www.ams.org/mathscinet-getitem?mr=2007f:14001)&rbrack;  

  > (focusing on the incarnation of stacks, under the [[Grothendieck construction]], as [[Grothendieck fibrations]]) 

* [[Bertrand Toen]], _[[Master course on algebraic stacks]]_ (2005)

* [[Frank Neumann]], *Algebraic Stacks and Moduli of Vector Bundles*, impa (2011) &lbrack;[pdf](https://impa.br/wp-content/uploads/2017/04/PM_36.pdf), [pdf](https://www.cimat.mx/~luis/seminarios/Pilas-algebraicas/neumann-Stacks.pdf)&rbrack;

* [[Michael Groechenig]], *Algebraic Stacks*, Lecture notes (2014) &lbrack;[web](http://individual.utoronto.ca/groechenig/stacks.html), [pdf](http://individual.utoronto.ca/groechenig/stacks.pdf), [[Groechenig-AlgebraicStacks.pdf:file]]&rbrack;

* [[Martin Olsson]], *Algebraic Spaces and Stacks*, Colloquium Publications **62** (2016) &lbrack;[doi:10.1090/coll/062](https://doi.org/10.1090/coll/062), [ISBN:978-1-4704-2798-6](https://bookstore.ams.org/coll-62)&rbrack;

* [[Daniel Halpern-Leistner]], *Moduli theory*, Lecture notes (2020) &lbrack;[pdf](http://pi.math.cornell.edu/~danielhl/moduli_theory_notes.pdf), [[Halpern-Leistner_ModuliTheory.pdf:file]]&rbrack;


See also:

* {#deJong} [[Aise Johan de Jong]], _[[The Stacks Project]]_, &lbrack;[tag:026K](https://stacks.math.columbia.edu/tag/026K)&rbrack;






* [[Fredrik Meyer]], *Notes on algebraic stacks* (2013) &lbrack;[pdf](https://fredrikmeyer.net/uio-math/algstacks.pdf), [[Meyer_AlgebraicStacks.pdf:file]]&rbrack;


Brief overview:

* Anatoly Preygel, _Algebraic stacks_, Seminar notes: Quantization of Hitchin's integrable system and Hecke eigensheaves, 2009, [pdf](http://www.math.harvard.edu/~gaitsgde/grad_2009/SeminarNotes/Sept15-17%28stacks%29.pdf).

The noncommutative version is discussed in

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative stacks_ , preprint MPIM2004-37 ([dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2305) [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333))
{#KontsevichRosenberg}

[[!redirects algebraic stack]]
[[!redirects algebraic stacks]]