
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

# Dependent linear type theory

* table of contents
{: toc}

## Idea

*Dependent linear [[type theory]]* should be some kind of combination of _[[dependent type theory]]_ and _[[linear type theory]]_.  Dependent linear *homotopy* type theory ([Schreiber 2014](#Schreiber14), [Riley 2022](#Riley22)) should additionally combine this with [[homotopy type theory]].  There are various things that such combinations might mean, and various approaches to making it precise.

One of the most important is a theory that includes both "linear types" and "nonlinear types", where the linear types may be dependent on the nonlinear types.  The nonlinear types might also be allowed to depend on each other, but in this theory the linear types are not allowed to depend on each other.

There are other approaches to dependent linear type theory that do allow some sort of dependence between linear types, but we will not (yet) discuss them on this page.

## Syntax


Details are still somewhat in the making: An extension of the [[LF]] [[syntax]] by dependent linear types appears in ([Pfenning 96](#Pfenning96), [WCFW 03](#WCFW03)) and a dependent linear extension of [[system L]] in ([Spiwack 14, section 5](#Spiwack14)).

Proposals for an actual [[syntax]] for dependent linear type theory appear in ([V&#225;k&#225;r 14](#Vakar14), [KPB 15](#KPB15)).

## Semantics

One sort of dependent linear type theory should have [[categorical semantics]] in [[indexed monoidal (∞,1)-categories]] -- see there for detailed discussion.

### Non-homotopy version

Notice that the following relation between syntax and semantics are well established (see at _[[relation between type theory and category theory]]_ for details):

|  [[syntax]] | [[semantics]] |
|-------------|---------------|
| [[linear type theory|multiplicative intuitionistic linear type theory]] | ([[symmetric monoidal category|symmetric]] [[closed monoidal category|closed]]) [[monoidal categories]] |
| [[dependent type theory]] | [[locally cartesian closed categories]] |

Here the correspondence in the first line works by interpreting [[types]] $X$ in the [[linear type theory]] as [[objects]] $[X]$ in a [[monoidal category]] $\mathcal{C}^{\otimes}$ and by interpreting the [[conjunctions]] (as far as they exist) as follows:

| [[type theory]] | [[category theory]] |
|------|--------|
| $\otimes$ [[multiplicative conjunction]] | $\otimes$ [[tensor product]] |
| $\multimap$ [[linear implication]]   | $[-,-]$ [[internal hom]] |
| $(-)^\bot$ [[linear negation]] | $(-)^\ast$ [[dual object]]

The correspondence in the second line works by forming for any [[locally cartesian closed category]] $\mathcal{C}$ its system of [[slice categories]] $[\Gamma] \mapsto \mathcal{C}_{/[\Gamma]}$, each of which is a [[cartesian monoidal category|cartesian]] [[closed monoidal category]], and then interpreting that as the [[semantics]] for [[dependent type theory]] in the [[context]] $\Gamma$:

$$
  \left\{
    \Gamma \vdash a \colon A
  \right\}
  \leftrightarrow
  \left\{
     (\ast \stackrel{[a]}{\longrightarrow} [A])
     \in Mor(\mathcal{C}_{/[\Gamma]})
  \right\}
  \,.
$$

Moreover, the system of slice categories has good [[base change]] in that for every morphism $[f] \colon [\Gamma_1]\to [\Gamma_2]$ in $\mathcal{C}$ there is an [[adjoint triple]] of [[functors]]

$$
   \mathcal{C}_{[\Gamma_1]}
    \stackrel{\stackrel{[f]_!}{\longrightarrow}}{\stackrel{\overset{[f]^\ast}{\longleftarrow}}{\underset{[f]_\ast}{\longrightarrow}}}
    \mathcal{C}_{[\Gamma_2]}
$$

satisfying [[Frobenius reciprocity]]. These serve as the semantics for the [[context extension]] along a map $f\colon \Gamma_1 \to \Gamma_2$ of contexts, and for the [[dependent sum]] $\sum$, and the [[dependent product]] of the dependent type theory syntax, respectively:

$$
  \left\{
     \underset{f^{-1}(-)}{\sum}
     , \; f \;,
     \underset{f^{-1}(-)}{\prod}
  \right\}
  \leftrightarrow
  \left\{
    [f]_! \dashv [f]^\ast \dashv [f]_\ast
  \right\}
  \,.
$$

Now since a [[cartesian monoidal category]] is in particular a ([[symmetric monoidal category|symmetric]] [[closed monoidal category|closed]]) [[monoidal category]], this immediately suggest to generalize the assignments
$[\Gamma] \mapsto (\mathcal{C}_{/[\Gamma]})^\times$ to assignments
$[\Gamma] \mapsto (\mathcal{C}_{[\Gamma]})^\otimes$ of ([[symmetric monoidal category|symmetric]] [[closed monoidal category|closed]]) [[monoidal categories]] (possibly but not necessarily the [[slice categories]] of $\mathcal{C}$) such that there still is good [[base change]] in the above way.

More explicitly, following the notion of [[hyperdoctrine]], the [[categorical semantics]] of dependent linear type theory should have for each [[context]] $\Gamma$ a [[linear type theory]]/possibly-non-[[cartesian monoidal category|cartesian]] [[symmetric monoidal category|symmetric]] [[closed monoidal category]] $(\mathcal{C}_{\Gamma}, \otimes, 1)$ and for each [[homomorphism]] of [[contexts]] $f \;\colon\; \Gamma_1 \longrightarrow \Gamma_2$ functorially an [[adjoint triple]] of [[functors]]

$$
  (f_! \dashv f^\ast \dashv f_\ast)
    \;\colon\;
   \mathcal{C}_{\Gamma_1}
    \stackrel{\stackrel{f_!}{\longrightarrow}}{\stackrel{\overset{f^\ast}{\longleftarrow}}{\underset{f_\ast}{\rightarrow}}}
    \mathcal{C}_{\Gamma_2}
  \,.
$$

where $f^\ast$ is [[context extension]] and where the [[left adjoint]] $f_!$ and [[right adjoint]] $f_\ast$ are to be thought of as linear analogs of [[dependent sum]] and [[dependent product]], respectively. Moreover this should satisfy [[Frobenius reciprocity]], hence $f^\ast$ should be a strong [[closed monoidal functor]].  Typically one would in addition demand the [[Beck-Chevalley condition]] for consecutive such adjoint triples.

Equivalently this is an [[indexed closed monoidal category]]; in the homotopical version, it would be an [[indexed monoidal (∞,1)-category]].  See those pages for more extensive discussion of the mathematics that takes place in such models that should be internalizable in dependent linear (homotopy) type theory once it exists.

In [[geometry]]/[[topos theory]] such a "linear hyperdoctrine" is known as _[[six operations]] yoga in [[Wirthmüller context|Wirtmüller flavor]]_. In fact there this appears in [[geometric homotopy theory]] ("[[derived functors]] on [[quasicoherent sheaves]]") hence as _dependent linear [[homotopy type theory]]_.


Details (of what?) are written out in ([Vakar 14](#Vakar14)).


+-- {: .num_remark }
###### Remark

That $f^\ast$ is a morphism of [[monoidal categories]] means that it is a [[strong monoidal functor]], preserving the [[tensor product]]

$$
  f^\ast(X\otimes Y)\simeq (f^\ast X)\otimes (f^\ast Y)
  \,.
$$

If monoidal categories involved are [[closed monoidal categories]] then the condition of [[Frobenius reciprocity]] is equivalent to $f^\ast$ also being a [[strong closed functor]] in that it preserves the [[internal hom]]

$$
  f^\ast [X,Y] \simeq [f^\ast X, f^\ast Y]
  \,.
$$

=--


+-- {: .num_defn}
###### Definition (Notation)

In view of the perspective of semantics for type theory, we may omit the notational distinction between contexts and the objects that interpret them, and between dependent sum/product and the functors that interpret them. We will write the [[base change]] as

$$
   \left(
     \underset{f}{\sum}
     \dashv
     f^\ast
     \dashv
     \underset{f}{\prod}
   \right)
    \;\colon\;
   Mod(\Gamma_1)
    \stackrel{\stackrel{f_!}{\longrightarrow}}{\stackrel{\overset{f^\ast}{\longleftarrow}}{\underset{f_\ast}{\longrightarrow}}}
    Mod(\Gamma_2)
  \,.
$$

The statement of [[Frobenius reciprocity]] then equivalently reads like this:

$$
  \underset{f}{\sum}
  \left(
    X \otimes f^\ast Y
  \right)
  \simeq
  \left(
    \underset{f}{\sum} X
  \right)
  \otimes
  Y
  \,.
$$

For $f\colon X\to Y$ a morphism in $\mathcal{C}$, we write

$$
  \epsilon_f
  \colon
  \underset{f}{\sum}f^\ast (-)
  \longrightarrow
  (-)
$$

for the [[counit of an adjunction|adjunction counit]] of $(\sum_f \dashv f^\ast)$.

Notice that $\underset{f}{\sum}$ has the interpretation of summing over all the [[fibers]] of the morphism $f$, as the elements in its [[codomain]] vary. Therefore it is sometime suggestive to use the notation

$$
  \underset{f^{-1}(-)}{\sum}
  \coloneqq
  \underset{f}{\sum}
  \,.
$$

In this vein, for $X \in \mathcal{C}$ any object and $p_X \colon X \to \ast$ the canonical morphism to the [[terminal object]], we abbreviate as

$$
  \underset{X}{\sum}
  \coloneqq
  \underset{p_X}{\sum}
  \,.
$$

=--



### Homotopy version
 {#LinearHomotopyTypeTheory}


This discussion of dependent linear type theory [above](#DependentLinearTypeTheory) has an evident straightforward refinement to [[homotopy theory]]. To appreciate this, notice that the following relation is well established (see again at _[[relation between type theory and category theory]]_ for details):


|  [[syntax]] | [[semantics]] |
|-------------|---------------|
| [[homotopy type theory]]  | [[locally cartesian closed (∞,1)-categories]] |
| [[homotopy type theory]] with [[univalence|univalent]] weak [[type universes]] | [[(∞,1)-toposes]] |

This works very much along the lines of the above relation between [[dependent type theory]] and [[locally cartesian closed categories]]. The central new ingredient is that one requires the locally cartesian closed category $\mathcal{C}$ to be equipped with a suitable structure of a [[model category]]. Using this there is then a notation of [[fibrant replacement]] of morphisms. The key point is that where in [[extensional type theory]] the [[identity type]] $(X \vdash Id_X \colon Type)$ of a type $X$ has semantics given by the [[diagonal]] morphism $\Delta_{[X]} \in \mathcal{C}_{/{[X]}}$, here in [[homotopy type theory]] it has semantics in the [[fibrant replacement]] $\hat \Delta_{[X]} \in \mathcal{C}_{/X}$. Such a fibrant replacement of the diagonal is [[path space object]] of $X$, reflecting the [[equivalences]]/[[homotopies]] "inside" the type $X$.

+-- {: .num_remark }
###### Remark

Since the Grothendieck construction of the standard indexed monoidal $(\infty,1)$-category of parametrized spectra is a [[tangent (∞,1)-toposes]],  one model for linear types depending on other *linear* types might be higher [[jet (∞,1)-category|jet (∞,1)-topos]]. This remains to be thought about.

=--

What should be the [[categorical semantics]] of one kind of dependent linear type theory was discussed in ([Shulman 08](#Shulman08), [Ponto-Shulman 12](#PontoShulman12), [Shulman 12](#Shulman12), [Schreiber 14](#Schreiber14)). 


## Related concepts

* [[dependent type theory]], [[linear type theory]]

* [[quantum set]]

* [[classical modality]]

* [[categorical semantics]]: 
  
  [[indexed monoidal (∞,1)-categories]], 

  [[tangent (∞,1)-toposes]]

* [[quantum logic]], [[quantum programming]]

* [[parameterized quantum system]]




## References
 {#References}

A [[syntax]] extending [[LF]] with linear dependent types was first published in

* {#Pfenning96} Iliano Cervesato, [[Frank Pfenning]], _A Linear Logical Framework_, 1996, ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.21.1152))

Note that this framework was restricted to the _negative_ fragment of [[intuitionistic linear logic]] and [[dependent type theory]] (i.e., $\multimap$, $\&$ and $\Pi$).  The problem of extending [[LF]] to positive connectives ($\otimes,1,!,\exists$) while retaining a reasonable notion of [[canonical form]] was later addressed by

* {#WCFW03} Kevin Watkins, Iliano Cervesato, [[Frank Pfenning]], David Walker, _A concurrent logical framework I: Judgments and properties_, CMU technical report CMU-CS-02-101, revised May 2003 ([web](http://www.cs.cmu.edu/~fp/papers/CMU-CS-02-101.pdf))

A dependent linear version of [[system L]] is considered in

* {#Spiwack14} [[Arnaud Spiwack]], section 5 of: _A dissection of L_ (2014) &lbrack;[pdf](http://assert-false.science/arnaud/papers/A%20dissection%20of%20L.pdf)&rbrack;

More recent work in the type-theoretic literature includes:

* [[Ugo Dal Lago]], _Linear Dependent Types in a Subrecursive Setting_, in _[Bounded Linear Logic Workshop](https://www.cs.bham.ac.uk/~drg/bll.html)_ Fontainebleau, 2013, [slides](https://www.cs.bham.ac.uk/~drg/bll/dallago.pdf).

* [[Ugo Dal Lago]], M. Gaboardi, _Linear Dependent Types and Relative Completeness-, in _Logical Methods in Computer Science_ Vol. 8(4:11), 2012.

* [[Ugo Dal Lago]] and B. Petit, _Linear dependent types in a call-by-value scenario_, in _Science of Computer Programming 84_, 2014.

* F.N. Forsberg, _Restricted linear dependent types for resource allocation_, in _[Bounded Linear Logic Workshop](https://www.cs.bham.ac.uk/~drg/bll.html)_, Fontainebleau, 2013, [slides](https://www.cs.bham.ac.uk/~drg/bll/fredrik.pdf).

* M. Gaboardi et al., _Linear Dependent Types for Differential Privacy_, in POPL '13, 2013.

Proposals for a genuine [[syntax]] for dependent linear type theory:

* {#SchöppStark04} [[Ulrich Schöpp]], [[Ian Stark]], *A Dependent Type Theory with Names and Binding*, in *Computer Science Logic. CSL 2004*, Lecture Notes in Computer Science **3210** (2004) 235–249 &lbrack;[doi:10.1007/978-3-540-30124-0_20](https://doi.org/10.1007/978-3-540-30124-0_20), [web](https://homepages.inf.ed.ac.uk/stark/names+binding.html)&rbrack;

* {#Vakar14} [[Matthijs Vákár]], _Syntax and Semantics of Linear Dependent Types_ ([arXiv:1405.0033](http://arxiv.org/abs/1405.0033))

* {#VakarSlides14} [[Matthijs Vákár]], _Splitting the Atom of Dependent Types... or Linear and Operational Dependent Type Theory_, talk at Oxford, November 2014 ([[VakarLinearAndOperationalDTT.pdf:file]]) 

* {#Vakar15} [[Matthijs Vákár]], *A Categorical Semantics for Linear Logical Frameworks*, In: A. Pitts  (ed.), *Foundations of Software Science and Computation Structures* FoSSaCS 2015. Lecture Notes in Computer Science, vol 9034. Springer 2015  ([arXiv:1501.05016](https://arxiv.org/abs/1501.05016), [doi:10.1007/978-3-662-46678-0_7](https://doi.org/10.1007/978-3-662-46678-0_7))

* {#Vakar17} [[Matthijs Vákár]], Section 3 of: *In Search of Effectful Dependent Types* ([arXiv:1706.07997](https://arxiv.org/abs/1706.07997), [uuid:e91e19b3-7e10-4fda-9433-f23b469e4049](https://ora.ox.ac.uk/objects/uuid:e91e19b3-7e10-4fda-9433-f23b469e4049))

* {#KPB15} [[Neelakantan Krishnaswami]], [[Pierre Pradic]], [[Nick Benton]], *Integrating Dependent and Linear Types*,  ACM SIGPLAN Notices **50** 1 (2015)  17–30  &lbrack;[pdf](https://www.cl.cam.ac.uk/~nk480/dlnl-paper.pdf),  [doi:10.1145/2775051.2676969](https://doi.org/10.1145/2775051.2676969)&rbrack;


* {#Lundfall17} [[Martin Lundfall]], *Models of linear dependent type theory*, 2017 ([[LundfallModelsOfLinerDTT.pdf:file]])

* {#Lundfall18} [[Martin Lundfall]], _A diagram model of linear dependent type theory_ &lbrack;[arXiv:1806.09593](https://arxiv.org/abs/1806.09593)&rbrack;

  > (with [[homotopy type theory]]-aspects)

* [[Conor McBride]], *I Got Plenty o’ Nuttin’*, in: *A List of Successes That Can Change the World*, Lecture Notes in Computer Science **9600**, Springer (2016) &lbrack;[doi:10.1007/978-3-319-30936-1_12](https://doi.org/10.1007/978-3-319-30936-1_12)&rbrack;

* [[Robert Atkey]], *Syntax and semantics of quantitative type theory*, in *33rd Annual ACM/IEEE Symposium on Logic in Computer Science*, LICS (2018) 56–65 &lbrack;[doi:10.1145/3209108.3209189](https://dl.acm.org/doi/10.1145/3209108.3209189)&rbrack;

* [[Mike Shulman]], _A type theory for fibred functors and polynomials_, unfinished note (2018)  &lbrack;[pdf](http://home.sandiego.edu/~shulman/papers/functors.pdf)&rbrack;

* [[Benjamin Moon]], [[Harley Eades III]], [[Dominic Orchard]], *Graded Modal Dependent Type Theory*. In: N. Yoshida (ed.) *Programming Languages and Systems ESOP 2021*, Lecture Notes in Computer Science **12648**, Springer (2021) 462-490 &lbrack;[doi:10.1007/978-3-030-72019-3_17](https://doi.org/10.1007/978-3-030-72019-3_17), [arxiv:2010.13163](https://arxiv.org/abs/2010.13163)&rbrack;


(Detailed critical discussion of most of these previous proposals is given in [Riley 2022, §1.7](#Riley22Thesis) [p. 90](https://mvr.hosting.nyu.edu/pubs/thesis.pdf#page=90), see also brief comments in [Riley 2022b](#Riley22), [p. 22](https://ncatlab.org/nlab/files/CQTS-InitialResearcherMeeting-Riley-220913.pdf#page=22)).

A satisfactory dependent [[linear homotopy type theory]] is given in

* {#Riley22Thesis} [[Mitchell Riley]], *A Bunched Homotopy Type Theory for Synthetic Stable Homotopy Theory*, PhD Thesis (2022) &lbrack;[doi:10.14418/wes01.3.139](https://doi.org/10.14418/wes01.3.139), [ir:3269](https://digitalcollections.wesleyan.edu/object/ir%3A3269), [pdf](https://mvr.hosting.nyu.edu/pubs/thesis.pdf)&rbrack;

  > (using ideas from [[bunched logic]])

based on

* {#RileyFinsterLicata21} [[Mitchell Riley]], [[Eric Finster]], [[Daniel Licata]], *Synthetic Spectra via a Monadic and Comonadic Modality* ([arXiv:2102.04099](https://arxiv.org/abs/2102.04099))

Exposition:

* [[Mitchell Riley]], *Extending Homotopy Type Theory with Linear Type Formers*, talk at *The ForML Lab* (2021)  &lbrack;[web](https://the-au-forml-lab.github.io/colloquium_talks/Riley.html), [video](https://www.youtube.com/watch?v=sPxtdCtjSDc)&rbrack;

* {#Riley22} [[Mitchell Riley]], *Linear Homotopy Type Theory*, talk at: [HoTTEST Event for Junior Researchers 2022](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest_junior_2022.html)  (Jan 2022) &lbrack;slides: [pdf](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Riley-2022-01-20-HoTTEST.pdf), [[Riley-LHoTT-talk.pdf:file]], video: [YT](https://www.youtube.com/watch?v=o2oWhHabjdM)&rbrack;

  > **Abstract.** Some ∞-toposes support constructions that are inherently 'linear', such as the external smash product of parameterised spectra. These cannot be added axiomatically to ordinary HoTT, because there is no way to enforce this linearity: there are no restrictions on variable uses. This talk describes an extension of HoTT with linear tensor and hom type formers, as a kind of 'binary modality' and its right adjoint. Trying to stay compatible with existing results in HoTT naturally leads us to a novel kind of bunched dependent type theory. Our type theory is intended to be as human-usable as possible, with an eye towards synthetic stable homotopy theory.

* {#Riley22} [[Mitchell Riley]], *Dependent Type Theories à la Carte*, [talk at](Center+for+Quantum+and+Topological+Systems#RileySep2022) *[[CQTS]] Initial Researcher's Meeting* (Sep 2022) &lbrack;[[CQTS-InitialResearcherMeeting-Riley-220913.pdf:file]]&rbrack;

* [[Mitchell Riley]], *[[schreiber:Quantum Certification via Linear Homotopy Types|A Linear Dependent Type Theory with Identity Types as a Quantum Verification Language]]* (2023) &lbrack;[pdf](https://mvr.hosting.nyu.edu/pubs/translation.pdf), [[Riley-QuantumCertification.pdf:file]]&rbrack;
  > (translation between `LHoTT` and the proto-[[nLab:Quipper|`Quipper`]] of [Fu, Kishida & Selinger 2020](Quipper#FuKishidaSelinger20))

See also:

* {#Aberle24b} [[C.B. Aberlé]], *Foundations of Substructural Dependent Type Theory* &lbrack;[arXiv:2401.15258](https://arxiv.org/abs/2401.15258)&rbrack; 


Potential semantics for dependent linear type theory and linear homotopy type theory are discussed in

* {#Shulman08} [[Mike Shulman]], _Framed bicategories and monoidal fibrations_, in  Theory and Applications of Categories,  Vol. 20, 2008, No. 18, pp 650-738.  ([TAC](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html))
 
* {#PontoShulman12} [[Kate Ponto]], [[Mike Shulman]], _Duality and traces in indexed monoidal categories_, ([arXiv:1211.1555](http://arxiv.org/abs/1211.1555),  [blog](http://golem.ph.utexas.edu/category/2011/11/traces_in_indexed_monoidal_cat.html))

* {#Shulman12} [[Mike Shulman]], _Enriched indexed categories_,([arXiv:1212.3914](http://arxiv.org/abs/1212.3914))

* {#Schreiber14} [[Urs Schreiber]], *[[schreiber:Quantization via Linear homotopy types]]* &lbrack;[arXiv:1402.7041](http://arxiv.org/abs/1402.7041)&rbrack;

* [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Entanglement of Sections]]* &lbrack;[arXiv:2309.07245](https://arxiv.org/abs/2309.07245)&rbrack;

As a [[quantum programming language]]:

* {#FuKishidaSelinger20} [[Peng Fu]], [[Kohei Kishida]], [[Peter Selinger]], _Linear Dependent Type Theory for Quantum Programming Languages_, LICS '20: Proceedings of the 35th Annual ACM/IEEE Symposium on Logic in Computer ScienceJuly 2020 Pages 440–453 ([arXiv:2004.13472](https://arxiv.org/abs/2004.13472), [doi:10.1145/3373718.3394765](https://dl.acm.org/doi/10.1145/3373718.3394765), [pdf](https://depend.cs.uni-saarland.de/lics-icalp/papers/B5.F), [video](https://www.youtube.com/watch?v=GUT8j4V6Nzg))

specifically implemented for [[Quipper]]:

* [[Peng Fu]], [[Kohei Kishida]], [[Neil Ross]], [[Peter Selinger]],  _A Tutorial Introduction to Quantum Circuit Programming in Dependently Typed Proto-Quipper_, in I. Lanese, M. Rawski  (eds.) _Reversible Computation_ RC 2020. Lecture Notes in Computer Science, vol 12227 ([arXiv:2005.08396](https://arxiv.org/abs/2005.08396), [doi:10.1007/978-3-030-52482-1_9](https://doi.org/10.1007/978-3-030-52482-1_9))

and in view of [[linear homotopy type theory]]:

* [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:The Quantum Monadology]]* &lbrack;[arXiv:2310.15735](https://arxiv.org/abs/2310.15735)&rbrack;

[[!redirects dependent linear type theories]]

[[!redirects linear dependent type theory]]
[[!redirects linear dependent type theories]]

[[!redirects dependent linear type]]
[[!redirects dependent linear types]]

[[!redirects linear dependent homotopy type theory]]
[[!redirects linear dependent homotopy type theories]]

[[!redirects dependent linear homotopy type theory]]
[[!redirects dependent linear homotopy type theories]]

[[!redirects linear homotopy type theory]]
[[!redirects linear homotopy type theories]]

[[!redirects linear homotopy-type theory]]
[[!redirects linear homotopy-type theories]]

[[!redirects linear homotopy type]]
[[!redirects linear homotopy types]]

