
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
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Equivariant homotopy theory is [[homotopy theory]] for the case that a [[group]] $G$ [[action|acts]] on all the [[topological spaces]]  or other objects involved, hence the homotopy theory of [[topological G-spaces]].

The canonical [[homomorphisms]] of topological $G$-spaces are $G$-equivariant [[continuous functions]], and the canonical choice of [[homotopies]] between these are $G$-equivariant continuous homotopies (for trivial $G$-action on the interval). A $G$-equivariant version of the [[Whitehead theorem]] says that on [[G-CW complexes]] these $G$-equivariant [[homotopy equivalences]] are equivalently those maps that induce [[weak homotopy equivalences]] on all [[fixed point]] spaces for all [[subgroups]] of $G$ (compact subgroups, if $G$ is allowed to be a [[Lie group]]). By [[Elmendorf's theorem]], this, in turn, is equivalent to the [[(∞,1)-presheaves]] over the [[orbit category]] of $G$. See below at _[In topological spaces -- Homotopy theory](#HomotopyTheory)_.

(Beware that $G$-homotopy theory is crucially different from (namely "finer" and "more geometric" than) the homotopy theory of the [[∞-actions]] of the underlying [[homotopy type]] [[∞-group]] of $G$, and this is so even when $G$ is a [[discrete group]], see [below](#RelationToInfinityActions)).

The union of $G$-equivariant homotopy theories as $G$ is allowed to vary is _[[global equivariant homotopy theory]]_.

The direct [[stabilization]] of equivariant homotopy theory is the theory of [[spectra with G-action]]. More generally there is a concept of [[G-spectra]] and they are the subject of [[equivariant stable homotopy theory]].

The concept of [[cohomology]] of equivariant homotopy theory is _[[equivariant cohomology]]_:

[[!include equivariant cohomology -- table]]


## In topological spaces

Let $G$ be a [[discrete group]].

### $G$-Homotopy

+-- {: .num_defn #GSpace}
###### Definition


A **[[topological G-space]]** is a [[topological space]] equipped with a $G$-[[action]].

=--

Let $I = \mathbb{R}$ be the [[interval object]] $({*} \stackrel{0}{\to} I \stackrel{1}{\leftarrow} {*})$ regarded as a $G$-space by equipping it with the trivial $G$-[[action]].

+-- {: .num_defn #GHomotopy}
###### Definition

A **$G$-[[homotopy]]**  $\eta$ between $G$-maps, $f, g  : X \to Y$, is a [[left homotopy]] with respect to this $I$

$$
  \array{
    X \times {*} = X
    \\
    {}^{\mathllap{Id \times 0}}\downarrow & \searrow^{f}
    \\
    X \times I &\stackrel{\eta}{\to}& Y
    \\
    {}^{\mathllap{1}}\uparrow & \nearrow_{g}
    \\
    X\times {*} = X
  }
  \,.
$$ 

=--

(e.g. [May 96, p. 15](#May96))


### Homotopy theory of $G$-spaces
 {#HomotopyTheory}

+-- {: .num_defn #HomotopicalStructures}
###### Definition
**(models for $G$-equivariant spaces)**

Consider the following three [[homotopical category|homotopical categories]] that model $G$-spaces:

1. Write

   $$
     G Top_{cof} \subset G Top
   $$ 

   for the full [[subcategory]] of [[G-CW-complexes]], regarded as equipped with the structure of a [[category with weak equivalences]] by taking the weak equivalences to be the $G$- [[homotopy equivalences]] according to def. \ref{GHomotopy}.

1. Write

   $$
     G Top_{loc}
   $$

   for all of $G Top$ equipped with weak equivalences given by those morphisms $(f : X \to Y) \in G Top$ that induce for all [[subgroups]] $H \subset G$ [[weak homotopy equivalences]] $f^H : X^H \to Y^H$ on the $H$-[[fixed point]] spaces, in the standard [[Quillen model structure on topological spaces]] (i.e. inducing [[isomorphism]] on [[homotopy groups]]).

1. Write

   $$
     [Orb_G^{op}, Top_{loc}]_{proj}
   $$ 

   for the projective [[global model structure on functors]] 
   from the [[opposite category]] of the [[orbit category]] $O_G$ of $G$ to the [[Top]] (with its [[classical model structure on topological spaces]]). 


=--

The following theorem (the [[equivariant Whitehead theorem]] together with [[Elmendorf's theorem]]) says that these models all present the same [[homotopy theory]].

+-- {: .num_theorem #EquivariantWhiteheadAndElmendorfTheorem}
###### Theorem
**(Elmendorf's theorem)**

The [[homotopy category|homotopy categories]] of all three [[homotopical categories]] in def. \ref{HomotopicalStructures} are [[equivalence of categories|equivalent]]:

$$
  Ho(G Top_{cof}) 
    \overset{\simeq}{\longrightarrow} 
  Ho(G Top_{loc}) 
    \overset{\simeq}{\longrightarrow} 
  Ho([Orb_G^{op}, Top])
  \,,
$$

where the equivalence is induced by the [[functor]] that sends a $G$-space to the [[presheaf]] that it [[representable functor|represents]].

The first of these equivalences is the _[[equivariant Whitehead theorem]]_, the second is _[[Elmendorf's theorem]]_.

=--

This is stated as ([May 96, theorem VI.6.3 ](#May96)).


$$
  \array{
    Ho(G Top_{cof}) 
      &\underset{}{\longrightarrow}&
    Ho(Top_{cof}) 
    \\
    {\mathllap{\text{equivariant} \atop \text{Whitehead}}}\big\downarrow{\mathrlap{\simeq}}
    &&
    {\mathllap{\simeq}}\big\downarrow{\mathrlap{\text{Whitehead}}}
    \\
    Ho(G Top_{loc})
    &\overset{}{\longrightarrow}&
    Ho(Top_{loc})
    \\
    {\mathllap{Elmendorf}}\big\downarrow{\mathrlap{\simeq}}
    &&
    \downarrow^{\mathrlap{=}}
    \\
    Ho( PSh( Orb_G, Top_{loc} ) )_{proj}
    &\longrightarrow&
    Ho( \ast, Top_{loc} )_{proj}
  }
$$


### $(\infty,1)$-category of $G$-equivariant spaces 
 {#InfGTop}

At [[topological ∞-groupoid]] it is discussed that the category [[Top]] of [[topological space]]s may be understood as the [[localization of an (∞,1)-category]] $Sh_{(\infty,1)}(Top)$ [[(∞,1)-category of (∞,1)-sheaves|of (∞,1)-sheaves]] on $Top$, at the collection of morphisms of the form $\{X \times I \to X\}$ with $I$ the real line.

The analogous statement is true for $G$-spaces: the equivariant homotopy category is the [[homotopy localization]] of the category of $\infty$-stacks on $G Top$.  

More in detail: let $G Top$ be the [[site]] whose objects are $G$-spaces that admit $G$-equivariant open covers, morphisms are $G$-equivariant maps and morphism $Y \to X$ is in the [[coverage]] if it admits a $G$-equivariant splitting over such $G$-equivariant open covers.


Write

$$
  sSh(G Top)_{loc}
$$

for the corresponding [[hypercompletion|hypercomplete]] local [[model structure on simplicial sheaves]]. 

Let $I$ be the unit interval, the standard [[interval object]] in [[Top]], equipped with the trivial $G$-action, regarded as an object of $G Top$ and hence in $sSh(G Top)$.


Write 

$$
  sSh(G Top)_{loc}^I  \stackrel{\leftarrow}{\to}
  sSh(G Top)_{loc}
$$

for the left [[Bousfield localization of model categories|Bousfield localization]] at thecollection of morphisms $\{X \stackrel{Id \times 0}{\to} X \times I\}$.

Then the [[homotopy category]] of $sSh(G Top)_{loc}^I$ is the equivariant homotopy category described above

$$  
  Ho(sSh(G Top)_{loc}^{I}) \simeq G Top_{loc}
  \,.
$$

This is ([Morel-Voevodsky 03, example 3, p. 50](#MorelVoevodsky03)). 


### Global equivariant homotopy theory

The above constructions may be unified to apply "for all groups at once",
this is the content of _[[global equivariant homotopy theory]]_.


## In more general model categories

Let $G$ be a finite [[group]] as above. We describe the generalizaton of the above story as [[Top]] is replaced by a more general [[model category]] $C$ ([Guillou](#Guillou)).

+-- {: .num_defn}
###### Definition and proposition

1. Let $C$ be a [[cofibrantly generated model category]] with generating cofibrations $I$ and generating acyclic cofibrations $J$.

   There is a cofibrantly generated model category 

   $$
     [O_G^{op}, C]_{loc}
   $$

   on the [[functor category]] from the [[orbit category]] of $G$ to $C$ by taking the generating cofibrations to be

   $$
     I_{O_G} := \{G/H \times i\}_{i \in I, H \subset G}
   $$

   and the generating acyclic cofibrations to be
  
   $$
     J_{O_G} := \{G/H \times j\}_{j \in I, H \subset G}
     \,.
   $$

1. Let $\mathbf{B}G$ be the [[delooping]] [[groupoid]] of $G$ and let

   $$
     [\mathbf{B}G^{op}, C]_{loc}
   $$

   be the [[functor category]] from $\mathbf{B}G$ to $C$ -- the category of objects in $C$ equipped with a $G$-[[action]] equipped with a set of generating (acyclic) cofibrations

   $$
     I_{\mathbf{B}G} := \{G/H \times i\}_{i \in I, H \subset G}
   $$

   and the generating acyclic cofibrations to be
  
   $$
     J_{\mathbf{B}G} := \{G/H \times j\}_{j \in I, H \subset G}
     \,.
   $$

   This defines a cofibrantly generated model category if $[\mathbf{B}G^{op}, C]$ has a _cellular fixed point functor_ (see...). 

=--

+-- {: .num_defn}
###### Definition and proposition
**(generalized Elmendorf's theorem)**


There is a [[Quillen adjunction]]

$$
  G/e \times (-) : C \stackrel{\leftarrow}{\to} [\mathbf{B}G^{op},C]_{loc} : (-)^e
$$

and a [[Quillen equivalence]]

$$
  \Theta : [O_G^{op}, C]_{loc} \stackrel{\leftarrow}{\to} [\mathbf{B}G^{op},C]_{loc}
  : \Phi
  \,.
$$

=--


+-- {: .proof}
###### Proof

This is proposition 3.1.5 in [Guillou](http://www.math.uiuc.edu/~bertg/EquivModels.pdf#page=6).

=--


### In $\infty$-stack $(\infty,1)$-toposes

The assumption on the [[model category]] $C$ entering the
generalized Elmendorf theorem above is satisfied in particular by every left [[Bousfield localization of model categories|Bousfield localization]] 

$$
  C := L_A SPSh(D)
$$ 

of the global projective [[model structure on simplicial presheaves]] onany [[small category]] $C$ at any [[set]] $A$ of morphisms, i.e. for every [[combinatorial model category]] $C$.
This is example 4.4 in [Guillou](http://www.math.uiuc.edu/~bertg/EquivModels.pdf#page=7).

For $A = \{C(\{U_i\}) \to X\}$ the collection of [[Cech cover]]s for all [[sieve|covering families]] of a [[Grothendieck topology]] on $D$, this are the standard [[models for ∞-stack (∞,1)-toposes]] $\mathbf{H}$.

This way the above theorem provides a model for $G$-equivariant refinements of [[∞-stack]] [[(∞,1)-topos]]es.


* For instance, in [[motivic homotopy theory]] one considers cohomology in a [[homotopy localization]] of the [[∞-stack]] [[(∞,1)-topos]] on the [[Nisnevich site]], presented by $C := L_{Cech} SPSh(Nis)$ . Its $G$-equivariant version as above should be the right context for the [[Bredon cohomology|Bredon]] $G$-[[equivariant cohomology]] refinement of such cohomology theories, such as [[motivic cohomology]].

  This is example 4.5 in [Guillou](http://www.math.uiuc.edu/~bertg/EquivModels.pdf#page=8).

  (Actually here one localizes moreover at [[hypercovers]] and at [[A1-homotopy theory|A1-homotopies]].)


## Properties
 {#Properties}


### Equivariant Hopf degree theorem

* [equivariant Hopf degree theorem](Hopf+degree+theorem#InEquivariantHomotopyTheory)


### $(\infty,1)$-topos

By [[Elmendorf's theorem]] the $G$-[[equivariant homotopy theory]] is an [[(∞,1)-topos]].

By ([Rezk 14](#Rezk14)) $G Top$ is also the [[base (∞,1)-topos]] of the [[cohesion]] of the [[global equivariant homotopy theory]] [[slice (∞,1)-topos|sliced]] over $\mathbf{B}G$.

### Stabilization

The [[stabilization]] of the [[(∞,1)-topos]] $G Top \simeq PSh_\infty(Orb_G)$ is the [[equivariant stable homotopy theory]] of [[spectra with G-action]] ("[[naive G-spectra]]").

### Relation to ∞-Actions (fine and coarse equivariance)
 {#RelationToInfinityActions}

For $G$ a [[discrete group]] ([[geometrically discrete ∞-groupoid|geometrically discrete]]) the homotopy theory of [[G-spaces]] which enters [[Elmendorf's theorem]] is different (finer) than the standard homotopy theory of $G$-[[∞-actions]], which is presented by the [[Borel model structure]] (see there for more, and see ([Guillou](#Guillou))).

## Examples

### $S^1$-Equivariance

[[circle group]]-equivariant homotopy theory may be presented by [[cyclic sets]].


## Related concepts

* [[equivariance]]

* [[equivariant structure]]

* [[equivariant homotopy group]]

* [[equivariant differential topology]]

* [[proper equivariant homotopy theory]]

* [[equivariant stable homotopy theory]]

* [[equivariant cobordism theory]]

* [[equivariant motivic homotopy theory]]

* [[Sullivan conjecture]]

* [[Arf-Kervaire invariant problem]]

* [[equivariant symmetric monoidal category]]

* [[Parametrized Higher Category Theory and Higher Algebra]]

* [[Burnside category]], [[Burnside ring]]

Equivariant homotopy theory is to [[equivariant stable homotopy theory]] as [[homotopy theory]] is to [[stable homotopy theory]].

[[!include equivariant homotopy theory -- table]]




## References


Lecture notes:

* {#Blumberg17} [[Andrew Blumberg]], _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))


Textbooks and other accounts

* {#tomDieck79} [[Tammo tom Dieck]], _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766, Springer 1979 ([doi:10.1007/BFb0085965](https://link.springer.com/book/10.1007/BFb0085965))

* {#May96} [[Peter May]] et al., _Equivariant homotopy and cohomology theory_, CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996 ([ISBN: 978-0-8218-0319-6](https://bookstore.ams.org/cbms-91/?startBookmarkIdx=200)  [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/alaska1.pdf), [[MayEtAlEquivariant96.pdf:file]])

* {#Schwede12} [[Stefan Schwede]], appendix A.4 of of _[[Symmetric spectra]]_ (2012)

* [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], section 1.3 of _The Arf-Kervaire problem in algebraic topology: Sketch of the proof_ ([[HHRKervaire.pdf:file]])

  (with an eye towards application to the [[Arf-Kervaire invariant problem]])

The generalization of the homotopy theory of $G$-spaces and of Elmendorf's theorem to that of $G$-objects in more general [[model category|model categories]] is in 

* {#Guillou} [[Bert Guillou]], _A short note on models for equivariant homotopy theory_ ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf))

and further discussed in

* {#Stephan13} [[Marc Stephan]], _On equivariant homotopy theory for model categories_, Homology Homotopy Appl. 18(2) (2016) 183-208 ([arXiv:1308.0856](http://arxiv.org/abs/1308.0856))

See also

* {#Waner80} [[Stefan Waner]], _Equivariant Homotopy Theory and Milnor's Theorem_, Transactions of the American Mathematical Society Vol. 258, No. 2 (Apr., 1980), pp. 351-368 ([JSTOR](http://www.jstor.org/stable/1998061))

Specifically with an eye towards equivariant [[differential topology]] (such as [[Pontryagin-Thom construction]] for [[equivariant cohomotopy]]):

* {#Wasserman69} [[Arthur Wasserman]], _Equivariant differential topology_, Topology Vol. 8, pp. 127-150, 1969 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/wasserman.pdf))


Discussion in the context of [[global equivariant homotopy theory]] is in 

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_ (2014)

Discussion via [[homotopy type theory]] is in

* {#Shulman15} [[Mike Shulman]], _Univalence for inverse EI diagrams_ ([arXiv:1508.02410](http://arxiv.org/abs/1508.02410))

An alternative [[model category]]-structure:

* Mehmet Akif Erdal, Aslı Güçlükan İlhan, _A model structure via orbit spaces for equivariant homotopy_ ([arXiv:1903.03152](https://arxiv.org/abs/1903.03152))


