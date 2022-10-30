
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A jet can be thought of as the infinitesimal germ of a [[section]] of some [[bundle]] or of a map between spaces. Jets are a coordinate free version of Taylor-polynomials and Taylor series.

## Definition

### Concrete

For $p : P \to X$ a [[surjective submersion]] of [[smooth manifold]]s and $k \in \mathbb{N}$, the bundle $J^k P \to X$ of **$k$- order jets of sections of $p$** is the bundle whose [[fiber]] over a point $x \in X$ is the space of equivalence classes of [[germ]]s of [[section]]s of $p$, where two germs are considered equivalent if their first $k$ partial [[derivative]]s at $x$ coincide.

In the case when $p$ is a trivial bundle $p:X\times Y \to X$ its sections are canonically in bijection with maps from $X$ to $Y$ and two sections have the same partial derivatives iff the partial derivatives of the corresponding maps from $X$ to $Y$ agree. So in this case the [[jet space]] $J^k P$ is called the space of jets of maps from $X$ to $Y$ and commonly denoted with $J^k(X,Y)$.


### General abstract
 {#GeneralAbstractDefinition}

We discuss a [[general abstract]] definition of jet bundles.

Let 

* $\mathbf{H}$ be an [[(∞,1)-topos]] equipped with [[differential cohesion]] with [[infinitesimal shape modality]] $\Im$;

* and equipped with an [[(∞,2)-sheaf]] 

  [[Mod]]  $ \colon \; \mathbf{H}^{op} \to $ [[Stab(∞,1)Cat]] 

  of [[quasicoherent (∞,1)-sheaves]].


For $X \in \mathbf{H}$, write $\Im(X)$ for the corresponding [[de Rham space]] object.

Notice that we have the canonical morphism, the $X$-componenet of the [[unit of a monad|unit]] of the $\Im$-[[monad]]

$$
  i \colon X \to \Im(X)
$$

("inclusion of constant paths into all infinitesimal paths").

The corresponding [[base change]] [[geometric morphism]] is

$$
  (i^\ast \dashv i_\ast)
  \;\colon\;
  \mathbf{H}_{/X}
   \stackrel{\overset{i^*}{\leftarrow}}{\underset{Jet := i_*}{\to}}
  \mathbf{H}_{/\Im(X)}
$$


+-- {: .num_defn #GeneralAbstractDefinition}
###### Definition

The _[[jet comonad]]_ is the [[(∞,1)-comonad]] 

$$
  i^\ast i_\ast
  \;\colon\;
  \mathbf{H}_{/X}
  \longrightarrow
  \mathbf{H}_{/X}
$$

=--

+-- {: .num_remark}
###### Remark

Since [[base change]] gives even an [[adjoint triple]] $(i_! \dashv i^\ast \dashv i_\ast)$, there is a [[left adjoint]] $T_{inf} X \times_X (-)$ to the [[jet comonad]] of def. \ref{GeneralAbstractDefinition}, 

$$
  T_{inf}X \times_X (-) \;\dashv\; Jet
$$

where $T_{inf} X$ is the [[infinitesimal disk bundle]] of $X$, see at _[differential cohesion -- infinitesimal disk bundle -- relation to jet bundles](differential+cohesion#RelationOfInfinitesimalDiskBundleToJetBundle)_


=--

+-- {: .num_remark #LiteratureOnGeneralAbstractCharacterization}
###### Remark

In the context of [[differential geometry]] the fact that the jet bundle construction is a co-monad was explicitly observed in ([Marvan 86](#Marvan86), see also [Marvan 93, section 1.1](#Marvan93), [Marvan 89](#Marvan89)). It is almost implicit in ([Krasil'shchik-Verbovetsky 98, p. 13, p. 17](#KrasilshchikVerbovetsky98), [Krasilshchik 99, p. 25](#Krasilshchik99)).

In the context of [[synthetic differential geometry]] the fact that the jet bundle construction is [[right adjoint]] to the [[infinitesimal disk bundle]] construction is ([Kock 80, prop. 2.2](#Kock80)).

{#InTheContextOf} In the context of [[algebraic geometry]] and of [[D-schemes]] as in ([BeilinsonDrinfeld, 2.3.2](#BeilinsonDrinfeld), reviewed in [Paugam, section 2.3](#Paugam)), the base change comonad formulation inf def. \ref{GeneralAbstractDefinition} was noticed in ([Lurie, prop. 0.9](#Lurie)). 


=--

In as in ([BeilinsonDrinfeld, 2.3.2](#BeilinsonDrinfeld), reviewed in[Paugam, section 2.3](#Paugam)) jet bundles are expressed dually in terms of algebras in [[D-modules]]. We now indicate how the translation works. 

+-- {: .num_remark}
###### Remark

In terms of [[differential homotopy type theory]] this means that
forming "jet types" of [[dependent types]] over $X$ is the 
[[dependent product]] operation along the unit of the [[infinitesimal shape modality]] 

$$
  jet(E) \coloneqq \underset{X \to \Im X}{\prod} E
  \,.
$$

=--



+-- {: .num_defn}
###### Definition

A [[quasicoherent (∞,1)-sheaf]] on $X$ is a morphism of [[(∞,2)-sheaves]]

$$
  X \to Mod
  \,.
$$

We write

$$
  QC(X) := Hom(X, Mod)
$$

for the [[stable (∞,1)-category]] of [[quasicoherent (∞,1)-sheaves]].

A _[[D-module]]_ on $X$ is a morphism of [[(∞,2)-sheaves]]

$$
  \Im (X) \to Mod
  \,.
$$

We write 

$$
  DQC(X) := Hom(\Im (X), Mod)
$$

for the [[stable (∞,1)-category]] of D-modules.

=--

The **Jet algebra** functor is the [[left adjoint]] to the [[forgetful functor]] from [[associative algebra|commutative algebra]]s over $\mathcal{D}(X)$ to those over the [[structure sheaf]] $\mathcal{O}(X)$

$$
  (Jet \dashv F)
   :
   Alg_{\mathcal{D}(X)}
    \stackrel{\overset{Jet}{\leftarrow}}{\underset{F}{\to}}
   Alg_{\mathcal{O}(X)}
  \,.
$$


## Application 

Typical [[Lagrangian]]s in [[quantum field theory]] are defined on jet bundles. Their [[variational calculus]] is governed by [[Euler-Lagrange equation]]s.

## Related concepts

* [[jet prolongation]]

* [[jet space]]

* [[jet group]], [[jet groupoid]]

* [[differential equation]]

* [[evolutionary vector field]]

* [[variational bicomplex]]

* [[metric jet]]

* [[h-principle]]


[[!include infinitesimal and local - table]]

* in [[homotopy theory]]/[[Goodwillie calculus]]: [[jet (∞,1)-category]]

## References

Textbook accounts and lecture notes include

* [[David Saunders]], _The geometry of jet bundles_, London Mathematical Society Lecture Note Series __142__, Cambridge Univ. Press 1989.

* {#Krasilshchik99} [[Joseph Krasil'shchik]] in collaboration with Barbara Prinari, _Lectures on Linear Differential Operators over Commutative Algebras_, 1998 ([pdf](http://diffiety.ac.ru/preprint/99/01_99.pdf))

* Shihoko Ishii, _Jet schemes, arc spaces and the Nash problem_, [arXiv:math.AG/0704.3327](http://arXiv.org/abs/0704.3327)

* G. Sardanashvily, _Fibre bundles, jet manifolds and Lagrangian theory_,  Lectures for theoreticians, [arXiv:0908.1886](http://xxx.lanl.gov/abs/0908.1886)

* [[Peter Olver]], _Lectures on Lie groups and differential equation_,  chapter 3, _Jets and differential invariants_, 2012 ([pdf](http://www.math.umn.edu/~olver/sm_/j.pdf))


Early accounts include

* Hubert Goldschmidt, _Integrability criteria for systems of nonlinear partial differential equations_, J. Differential Geom. Volume 1, Number 3-4 (1967), 269-307 ([Euclid](http://projecteuclid.org/euclid.jdg/1214428094))

Discussion in tems of [[synthetic differential geometry]] is in 

* {#Kock80} [[Anders Kock]], _Formal manifolds and synthetic theory of jet bundles_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques (1980) Volume: 21, Issue: 3 ([Numdam](http://www.numdam.org/item?id=CTGDC_1980__21_3_227_0))


See also

* {#KrasilshchikVerbovetsky98} [[Joseph Krasil'shchik]], [[Alexander Verbovetsky]], _Homological Methods in Equations of Mathematical Physics_ ([arXiv:math/9808130](http://arxiv.org/abs/math/9808130))

The comonad structure on the jet operation in the context of differential geometry is made explicit in 

* {#Marvan86} [[Michal Marvan]], _A note on the category of partial differential equations_, in _Differential geometry and its applications_, Proceedings of the Conference August 24-30, 1986, Brno ([[MarvanJetComonad.pdf:file]])

  (notice that prop. 1.3 there is wrong, the correct version is in the thesis of the author)

with further developments in 

* {#Marvan89} [[Michal Marvan]] _On the horizontal cohomology with general coefficients_, 1989 ([web announcement](http://old.math.slu.cz/People/MichalMarvan/Annotations/horizontal.php), [web archive](http://dml.cz/dmlcz/701469))

  **Abstract:** In the present paper the horizontal cohomology theory is interpreted as a special case of the Van Osdol bicohomology theory applied to what we call a "jet comonad". It follows that differential equations have well-defined cohomology groups with coefficients in linear differential equations. 

* {#Marvan93} [[Michal Marvan]], section 1.1 of _On Zero-Curvature Representations of Partial Differential Equations_,  (1993) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.45.5631))


In the context of algebraic geometry, the abstract characterization of jet bundles as the direct images of base change along the de Rham space projection is noticed on p. 6 of

* {#Lurie} [[Jacob Lurie]], _Notes on crystals and algebraic D-modules_, 2009 ([pdf](http://www.math.harvard.edu/~gaitsgde/grad_2009/SeminarNotes/Nov17-19%28Crystals%29.pdf))

The explicit description in terms of formal duals of [[commutative monoids]] in [[D-module]]s is in

* {#BeilinsonDrinfeld} [[Alexander Beilinson]], [[Vladimir Drinfeld]], _[[Chiral Algebras]]_
 

An exposition of this is in section 2.3 of 

* {#Paugam} [[Frédéric Paugam]], _Homotopical Poisson Reduction of gauge theories_ ([pdf](http://people.math.jussieu.fr/~fpaugam/documents/homotopical-poisson-reduction-of-gauge-theories.pdf))
 

A discussion of jet bundles with an eye towards discussion of the [[variational bicomplex]] on them is in chapter 1, section A of

* {#Anderson} Ian Anderson, _The variational bicomplex_ ([pdf](http://www.math.usu.edu/~fg_mp/Publications/VB/vb.pdf))

The [[de Rham cohomology]] of jet bundles is discussed in

* G.Giachetta, L.Mangiarotti, G.Sardanashvily, _Cohomology of the variational bicomplex on the infinite order jet space_ ([arXiv:math/0006074](http://arxiv.org/abs/math/0006074))

Discussion of jet-restriction of the [[Haefliger groupoid]] is in 

* Arne Lorenz, _Jet Groupoids, Natural Bundles
and the Vessiot Equivalence Method_, Thesis ([pdf](http://wwwb.math.rwth-aachen.de/~arne/Dissertation_Lorenz_Arne.pdf))

Discussion of jet bundles in [[supergeometry]] includes

* Arthemy V. Kiselev, Andrey O. Krutov, appendix of _On the (non)removability of spectral parameters in $\mathbb{Z}_2$-graded zero-curvature representations and its applications_ ([arXiv:1301.7143](http://arxiv.org/abs/1301.7143))

[[!redirects jet bundles]]

[[!redirects jet]]
[[!redirects jets]]

[[!redirects jet type]]
[[!redirects jet types]]