
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Elmendorf's theorem_  states that for $G$ a [[topological group]], then the [[(∞,1)-category of (∞,1)-presheaves]] on the [[orbit category]] $Orb_G$ of $G$, naturally regarded as an [[(∞,1)-site]], is [[equivalence of (∞,1)-categories|equivalent]] to the [[localization of an (∞,1)-category|localization]] of [[topological spaces]] with $G$-[[action]] ([[G-spaces]]) at the _[[weak homotopy equivalences]] on [[fixed point spaces]]_ (also presented by [[G-CW complexes]], see at _[[equivariant homotopy theory]]_ for more).

More in detail, for $G$ a [[topological group]], write $Top^G$ for the [[category]] of [[compactly generated topological spaces]] which are equipped with a [[continuous function|continuous]] $G$-[[action]]. Say that a [[continuous map]] $f \colon X \longrightarrow Y$ between $G$-spaces is a **weak $G$-homotopy equivalence** if for any [[closed subspace|closed subgroup]] $H \hookrightarrow G$, the induced function on $H$-[[fixed point spaces]] $f^H \colon X^H \longrightarrow Y^H$ is an ordinary [[weak homotopy equivalence]]. Write 

$$
  Top^G[\{weak\,G-homotopy\;equivalences\}^{-1}]
  \in (\infty,1)Cat
$$

for the corresponding [[simplicial localization]].

Next, write $Orb_G$ for the [[full subcategory]] of $Top^G$ on the $G$-[[homogeneous spaces]] of the form $G/H$, but regarded as an [[(∞,1)-category]] by regarding each [[compact-open topology|hom-space]] as its [[homotopy type]]. Write moreover $Top^{Orb_G}$ for the category of [[continuous function|continuous]] functors $Orb_G^{op} \longrightarrow Top$. Write finally

$$
  PSh_\infty(Orb_G)
   \in 
 (\infty,1)Cat
  \,.
$$

Then Elmendorf's theorem asserts that there is an [[equivalence of (∞,1)-categories]]

$$
  Top^G[\{weak\;G-homotopy\;equivalences\}^{-1}]
  \simeq
  PSh_\infty(Orb_G)
  \,.
$$


+-- {: .num_remark}
###### Remark

In particular the theorem hence asserts that the $G$-[[equivariant homotopy theory]] is an [[(∞,1)-topos]].

=--




## Model category presentation / Quillen equivalence
 {#ModelCategoryPresentation}

A version of the theorem that applies fairly generally for ([[discrete group|discrete]]) [[group objects]] in suitable [[cofibrantly generated model categories]] is in ([Guillou 06](#Guillou), [Stephan 10](#Stephan10), [Stephan 13](#Stephan13)).

+-- {: .num_defn}
###### Definition

For $\mathcal{C}$ a [[cofibrantly generated model category]]
and for $G$ a [[discrete group]] (canonically regarded as a [[group object]] of $\mathcal{C}$ via its [[tensoring]] over [[Set]]) write $G \mathcal{C}$ for the category of $G$-[[actions]] in $\mathcal{C}$.

=--

+-- {: .num_defn #CellularFixedPointFunctor}
###### Definition

A _cellular fixed point functor_ on $\mathcal{C}$ is ...

=--

([Guillou 06, def. 3.7](#Guillou))

+-- {: .num_example}
###### Example

The [[fixed point spaces]]-functors on the following kinds of model categories are cellular

* the [[classical model structure on topological spaces]];

* the [[classical model structure on simplicial sets]];

* the global [[model structure on simplicial presheaves]] over any small category;

* (...)

=--

([Guillou 06, section 4](#Guillou))


+-- {: .num_defn}
###### Proposition

For $\mathcal{C}$ a [[cofibrantly generated model category]] with cellular fixed point functor, def. \ref{CellularFixedPointFunctor}, then the category $G \mathcal{C}$ of $G$-actions in $\mathcal{C}$ carries a [[cofibrantly generated model category]] structure $G \mathcal{C}_{fine}$ whose weak equivalences and fibrations are those maps which induce weak equivalences or fibrations in $\mathcal{C}$, respectively, on objects of $H$-[[fixed points]], for all [[subgroups]] $H$ of $G$.

=--

([Guillou 06, theorem 3.12](#Guillou))


Write $Orb_G$ for the [[orbit category]] of $G$.

Write $(\mathcal{C}^{Orb_G^{op}})_{proj}$ for the projective global [[model structure on functors]] from the $G$-[[orbit category]] to $\mathcal{C}$. 


+-- {: .num_defn}
###### Proposition

There is a pair of [[adjoint functors]]

$$
  (\Theta, \Phi)
    \;\colon\;
  G\mathcal{C}
   \stackrel{\overset{\Theta}{\longleftarrow}}{\underset{\Phi}{\longrightarrow}}
  \mathcal{C}^{Orb_G^{op}}
$$

where $\Phi X \colon G/H \mapsto X^H$ assigns fixed-point objects and where $\Theta S$ has as underlying object $S(G/1)$.

This constitutes a [[Quillen equivalence]] between the above model structures

$$
  (\Theta, \Phi)
    \;\colon\;
  G\mathcal{C}_{fine}
    \underset{Quillen}{\simeq}
  \mathcal{C}^{Orb_G^{op}}_{proj}
 \,.
$$

=--

([Guillou 06, prop. 3.15](#Guillou), [Stephan 13, Theorem 3.17](#Stephan13))

## Generalizations

1. Elmendorf's theorem may be generalized to the case where only a sub-family $\mathcal{H}$ of the closed subgroups of $G$ is considered ([Stephan 10](#Stephan10), also [May 96](#May96)).

1. There is an evident generalization of the [[orbit category]] of a fixed group $G$ to the _[[global orbit category]]_. Under this generalization an analog of Elmendorf's theorem plays a central role in [[global equivariant homotopy theory]] ([Rezk 14](#Rezk14)).

1. The orbit category for $G$ can also be generalized to the orbit category generated by any small category, $I$, where the $I$-orbits are $I$-diagrams in $Top$ whose strict colimit is equal to a point. If the orbits are either small or complete, then the $I$-equivariant model structure is Quillen-equivalent to a presheaf category (see pt. 11 of p. 8 of [PHCTIntro](Parametrized+Higher+Category+Theory+and+Higher+Algebra#PHCTIntro) and [Chorny13](#Chorny13)).





## Related concepts

* [[equivariant Whitehead theorem]]

* [[tom Dieck splitting]]

* [[global equivariant homotopy theory]]

* [[Bredon cohomology]]

* [[equivariant rational homotopy theory]]

  * [[model structure on equivariant connective dgc-algebras]]

  * [[Quillen adjunction between equivariant simplicial sets and equivariant connective dgc-algebras]]

  * [[fundamental theorem of dg-algebraic equivariant rational homotopy theory]]

## References

Lecture notes include

* {#Blumberg17} [[Andrew Blumberg]], _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))


The "fine" homotopical structure on [[G-spaces]] (with fixed-point-wise weak equivalences) is originally due to

* {#Bredon67} [[Glen Bredon]], _[[Equivariant cohomology theories]]_, Springer Lecture Notes in Mathematics Vol. 34. 1967.

The equivalence of the homotopy theory ([[homotopy category]]) of that to presheaves over the orbit category is then due to

* [[Anthony Elmendorf]], _Systems of fixed point sets_, Trans. Amer. Math. Soc., 277(1):275&#8211;284, 1983 ([jstor:1999356](https://www.jstor.org/stable/1999356))

which considered all closed subgroups of $G$.  Also

* {#Piacenza91} [[Robert Piacenza]], section 6 of _Homotopy theory of diagrams and CW-complexes over a category_, Can. J. Math. Vol 43 (4), 1991 ([[Piazenza91.pdf:file]])

  also chapter VI of [[Peter May]] et al, _Equivariant homotopy and cohomology theory_, 1996 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf))

The generalization of the proof to other choices of families of subgroups is due to

* {#May96} [[Peter May]], _Equivariant homotopy and cohomology theory_ With contributions by M. Cole, G. Comezaa, S. Costenoble, A. D. Elmendorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. Number 91 in CBMS Regional Conference Series in
Mathematics. Published for the Conference Board of the Mathematical Sciences, Washington, DC; by the American Mathematical Society, Providence, RI, 1996

Discussion in terms of [[Quillen equivalence]] of [[model categories]] is due to

* {#Guillou} [[Bert Guillou]], _A short note on models for equivariant homotopy theory_, 2006 ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf), [[GuillouEquivariantHomotopy.pdf:file]])

* {#Stephan10} [[Marc Stephan]], _Elmendorf’s Theorem via Model Categories_,  2010 ([pdf](http://web.math.ku.dk/~jg/students/stephan.msproject.2010.pdf)) --  _Elmendorf’s Theorem for Cofibrantly Generated Model Categories_ MS thesis, Zurich 2010 ([pdf](http://web.math.ku.dk/~jg/students/stephan.msthesis.2010.pdf))

* {#Stephan13} [[Marc Stephan]], _On equivariant homotopy theory for model categories_, Homology Homotopy Appl. 18(2) (2016) 183-208 ([arXiv:1308.0856](http://arxiv.org/abs/1308.0856))


A generalization to [[orbispaces]] is discussed in 

* [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))

Discussion in the broader context of [[global equivariant homotopy theory]] is in 

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_ (2014)

Some of the categorical aspects of Elmendorf's theorem are examined in

* {#CordierPorter96} [[Jean-Marc Cordier]], [[Timothy Porter]], _Categorical Aspects of Equivariant Homotopy_, Applied Cat.Structures, **4** (1996) 195 - 212. doi:[10.1007/BF00122252](https://doi.org/10.1007/BF00122252) (Proceedings of the European Colloquium of Category Theory, 1994)

A recent n-cat café discussion initiated by [[John Huerta]] and probing some of its uses in Mathematical Physics, can be found [here](https://golem.ph.utexas.edu/category/2018/06/elmendorfs_theorem.html#more).


Generalization to $I$-orbits for a small category $I$ is in

* {#Chorny13} [[Boris Chorny]], _Homotopy  theory  of  relative  simplicial  presheaves_,  Israel J. Math. 205 (2015), no. 1, 471–484, ([arXiv:1310.2932](https://arxiv.org/abs/1310.2932))

[[!redirects Elmendorf theorem]]

[[!redirects model structure on equivariant simplicial sets]]
[[!redirects model structures on equivariant simplicial sets]]

[[!redirects model structure on topological G-spaces]]
[[!redirects model structures on topological G-spaces]]
