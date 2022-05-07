
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

A jet can be thought of as the [[infinitesimal]] [[germ]] of a [[section]] of some [[bundle]] or of a map between spaces. Jets are a coordinate free version of Taylor-polynomials and Taylor series.

## Definition

### Concrete

For 

$$
  p \coloneqq E \to X
$$ 

a [[surjective submersion]] of [[smooth manifolds]] and $k \in \mathbb{N}$, the bundle 

$$
  J^k P \to X
$$ 

of **order-$k$ jets of sections of $p$** is the bundle whose [[fiber]] over a point $x \in X$ is the space of equivalence classes of [[germ|germs]] of [[section|sections]] of $p$, where two germs are considered equivalent if their first $k$ partial [[derivative|derivatives]] at $x$ coincide.

In the case when $p$ is a trivial bundle $p:X\times Y \to X$ its sections are canonically in bijection with maps from $X$ to $Y$ and two sections have the same partial derivatives iff the partial derivatives of the corresponding maps from $X$ to $Y$ agree. So in this case the [[jet space]] $J^k P$ is called the space of jets of maps from $X$ to $Y$ and commonly denoted with $J^k(X,Y)$.

In order to pass to $k \to \infty$ to form the _infinite jet bundle_ $J^\infty P$ one forms the [[projective limit]] over the finite-order jet bundles, 

$$
  J^\infty E \coloneqq \underset{\longleftarrow}{\lim}_k J^k E
  = 
  \underset{\longleftarrow}{\lim}
  \left(
    \cdots J^3 E \to J^2 E \to J^1 E \to E
  \right)
$$

but one has to decide in which category of [[infinite-dimensional manifolds]] to take this limit:

1. one may form the limit formally, i.e. in [[pro-manifolds]]. This is what is implicit for instance in [Anderson, p.3-5](#Anderson);

1. one may form the limit in [[Fréchet manifolds]], this is farily explicit in ([Saunders 89, chapter 7](#Saunders89)). See at _[Fr&#233;chet manifold -- Projective limits of finite-dimensional manifolds](Frechet+manifold#ProjectiveLimitsOfSmoothFiniteDimensionalManifolds)_. Beware that this is not equivalent to the pro-manifold structure (see the remark [here](Frechet+manifold#DifferenceBetweenProManifoldAndFrecherManifoldStructure)). It makes sense to speak of _[[locally pro-manifolds]]_.


### The Atiyah exact sequence

When $(X,\mathcal{O}_X)$ is a complex-analytic manifold with the structure sheaf of holomorphic functions, and $E$ a locally free sheaf of $\mathcal{O}_X$-modules, we can be even more explicit.
The first jet bundle $J^1(E)$ fits into a short exact sequence, called the Atiyah exact sequence:

$$
  0\to
  E\otimes_{\mathcal{O}_X}\Omega_X^1\to
  J^1(E)\to
  E\to
  0
$$

where $J^1(E) = (E\otimes\Omega_X^1)\oplus E$ as a $\mathbb{C}$-module, but with an $\mathcal{O}_X$-action given by

$$
  f(s\otimes\omega,t)
  =
  (f s\otimes\omega+t\otimes\mathrm{d}f, f t).
$$

The extension class $[J^1(E)]\in\mathrm{Ext}_{\mathcal{O}_X}^1(E,E\otimes\Omega_X^1)$ of this exact sequence is called the Atiyah class of $E$, and is somewhat equivalent to the first Chern class of $E$.
Note that the Atiyah class is exactly the obstruction to the Atiyah exact sequence admitting a splitting, and a (holomorphic) splitting of the Atiyah exact sequence is exactly a Koszul connection.




### General abstract
 {#GeneralAbstractDefinition}

We discuss a [[general abstract]] definition of jet bundles.

Let  $\mathbf{H}$ be an [[(∞,1)-topos]] equipped with [[differential cohesion]] with [[infinitesimal shape modality]] $\Im$ (or rather a tower $\Im_k$ of such, for each infinitesimal order $k \in \mathbb{N} \cup \{\infty\}$ ).

For $X \in \mathbf{H}$, write $\Im(X)$ for the corresponding [[de Rham space]] object.

Notice that we have the canonical morphism, the $X$-component of the [[unit of a monad|unit]] of the $\Im$-[[monad]]

$$
  i \colon X \to \Im(X)
$$

("inclusion of constant paths into all infinitesimal paths").

The corresponding [[base change]] [[geometric morphism]] is

$$
  (i^\ast \dashv i_\ast)
  \;\colon\;
  \mathbf{H}_{/X}
   \stackrel{\overset{i^*}{\longleftarrow}}{\underset{Jet := i_*}{\longrightarrow}}
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

In the context of [[differential geometry]] the fact that the jet bundle construction is a comonad was explicitly observed in ([Marvan 86](#Marvan86), see also [Marvan 93, section 1.1](#Marvan93), [Marvan 89](#Marvan89)). It is almost implicit in ([Krasil'shchik-Verbovetsky 98, p. 13, p. 17](#KrasilshchikVerbovetsky98), [Krasilshchik 99, p. 25](#Krasilshchik99)).

In the context of [[synthetic differential geometry]] the fact that the jet bundle construction is [[right adjoint]] to the [[infinitesimal disk bundle]] construction is ([Kock 80, prop. 2.2](#Kock80)).

{#InTheContextOf} In the context of [[algebraic geometry]] and of [[D-schemes]] as in ([BeilinsonDrinfeld, 2.3.2](#BeilinsonDrinfeld), reviewed in [Paugam, section 2.3](#Paugam)), the base change comonad formulation inf def. \ref{GeneralAbstractDefinition} was noticed in ([Lurie, prop. 0.9](#Lurie)). 


=--

In as in ([BeilinsonDrinfeld, 2.3.2](#BeilinsonDrinfeld), reviewed in [Paugam, section 2.3](#Paugam)) jet bundles are expressed dually in terms of algebras in [[D-modules]]. We now indicate how the translation works. 

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

  * [[local Lagrangian]]

  * [[source form]], [[Lepage form]]

* [[metric jet]]

* [[h-principle]]

* [[arithmetic jet space]]


[[!include infinitesimal and local - table]]

* in [[homotopy theory]]/[[Goodwillie calculus]]: [[jet (∞,1)-category]]

## References

Exposition of [[variational calculus]] in terms of jet bundles and [[Lepage forms]] and aimed at examples from [[physics]] is in

* {#MusilovaHronek16} [[Jana Musilová]],  [[Stanislav Hronek]], _The calculus of variations on jet bundles as a universal approach for a variational formulation of fundamental physical theories_, Communications in Mathematics, Volume 24, Issue 2 (Dec 2016) ([doi.org/10.1515/cm-2016-0012]( https://doi.org/10.1515/cm-2016-0012))


Textbook accounts and lecture notes include

* {#Michor80} [[Peter Michor]], _Manifolds of differentiable mappings_, Shiva Publishing (1980) [pdf](http://www.mat.univie.ac.at/~michor/manifolds_of_differentiable_mappings.pdf)

* {#Saunders89} [[David Saunders]], _The geometry of jet bundles_, London Mathematical Society Lecture Note Series __142__, Cambridge Univ. Press 1989.

* {#Krasilshchik99} [[Joseph Krasil'shchik]] in collaboration with Barbara Prinari, _Lectures on Linear Differential Operators over Commutative Algebras_, 1998 ([pdf](http://diffiety.ac.ru/preprint/99/01_99.pdf))

* Shihoko Ishii, _Jet schemes, arc spaces and the Nash problem_, [arXiv:math.AG/0704.3327](http://arXiv.org/abs/0704.3327)

* G. Sardanashvily, _Fibre bundles, jet manifolds and Lagrangian theory_,  Lectures for theoreticians, [arXiv:0908.1886](http://xxx.lanl.gov/abs/0908.1886)

* [[Peter Olver]], _Lectures on Lie groups and differential equation_,  chapter 3, _Jets and differential invariants_, 2012 ([pdf](http://www.math.umn.edu/~olver/sm_/j.pdf))


Early accounts include

* Hubert Goldschmidt, _Integrability criteria for systems of nonlinear partial differential equations_, J. Differential Geom. Volume 1, Number 3-4 (1967), 269-307 ([Euclid](http://projecteuclid.org/euclid.jdg/1214428094))

The algebra of smooth functions of just _locally_ finite order on the jet bundle ("[[locally pro-manifold]]") was maybe first considered in

* {#Takens79} [[Floris Takens]], _A global version of the inverse problem of the calculus of variations_, J. Differential Geom. Volume 14, Number 4 (1979), 543-562. ([Euclid](https://projecteuclid.org/euclid.jdg/1214435235))


{#DiscussionOfFrechetManifoldStructure} Discussion of the [[Fréchet manifold]] structure on infinite jet bundles includes

* {#Saunders89} [[David Saunders]], chapter 7 _Infinite jet bundles_ of _The geometry of jet bundles_, London Mathematical Society Lecture Note Series __142__, Cambridge Univ. Press 1989.

* M. Bauderon, _Differential geometry and Lagrangian formalism in the calculus of variations_, in _Differential Geometry, Calculus of Variations, and their Applications_, Lecture Notes in Pure and Applied Mathematics, 100, Marcel Dekker, Inc., N.Y., 1985, pp. 67-82.

* {#DodsonGalanisVassiliou15}[[C. T. J. Dodson]], George Galanis, Efstathios Vassiliou,, p. 109 and section 6.3 of _Geometry in a Fr&#233;chet Context: A Projective Limit Approach_, Cambridge University Press (2015)

* [[Andrew Lewis]], _The bundle of infinite jets_ (2006) ([pdf](http://www.mast.queensu.ca/~andrew/notes/pdf/2006a.pdf))

Discussion of finite-order jet bundles in tems of [[synthetic differential geometry]] is in 

* {#Kock80} [[Anders Kock]], _Formal manifolds and synthetic theory of jet bundles_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques (1980) Volume: 21, Issue: 3 ([Numdam](http://www.numdam.org/item?id=CTGDC_1980__21_3_227_0))

* {#Kock10} [[Anders Kock]], section 2.7 of _Synthetic geometry of manifolds_, Cambridge Tracts in Mathematics 180 (2010). ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

The [[jet comonad]] structure on the jet operation in the context of differential geometry is made explicit in 

* {#Marvan86} [[Michal Marvan]], _A note on the category of partial differential equations_, in _Differential geometry and its applications_, Proceedings of the Conference August 24-30, 1986, Brno ([[MarvanJetComonad.pdf:file]])

  (notice that prop. 1.3 there is wrong, the correct version is in the thesis of the author)

with further developments in 

* {#Marvan89} [[Michal Marvan]] _On the horizontal cohomology with general coefficients_, 1989 ([web announcement](http://old.math.slu.cz/People/MichalMarvan/Annotations/horizontal.php), [web archive](http://dml.cz/dmlcz/701469))

  **Abstract:** In the present paper the horizontal cohomology theory is interpreted as a special case of the Van Osdol bicohomology theory applied to what we call a "jet comonad". It follows that differential equations have well-defined cohomology groups with coefficients in linear differential equations. 

* {#Marvan93} [[Michal Marvan]], section 1.1 of _On Zero-Curvature Representations of Partial Differential Equations_,  (1993) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.45.5631))

* [[Igor Khavkine]], [[Urs Schreiber]], _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations: I. Jets and comonad structure]]_ ([arXiv:1701.06238](https://arxiv.org/abs/1701.06238))


In the context of algebraic geometry, the abstract characterization of jet bundles as the direct images of base change along the de Rham space projection is noticed on p. 6 of

* {#Lurie} [[Jacob Lurie]], _Notes on crystals and algebraic D-modules_, 2009 ([pdf](http://www.math.harvard.edu/~gaitsgde/grad_2009/SeminarNotes/Nov17-19%28Crystals%29.pdf))

The explicit description in terms of formal duals of [[commutative monoids]] in [[D-module]]s is in

* {#BeilinsonDrinfeld} [[Alexander Beilinson]], [[Vladimir Drinfeld]], _[[Chiral Algebras]]_
 

An exposition of this is in section 2.3 of 

* {#Paugam} [[Frédéric Paugam]], _Homotopical Poisson Reduction of gauge theories_ ([pdf](http://people.math.jussieu.fr/~fpaugam/documents/homotopical-poisson-reduction-of-gauge-theories.pdf))
 

A discussion of jet bundles with an eye towards discussion of the [[variational bicomplex]] on them is in chapter 1, section A of

* {#Anderson} [[Ian Anderson]], _The variational bicomplex_ ([[AndersonVariationalBicomplex.pdf:file]])

The [[de Rham complex]] and [[variational bicomplex]] of jet bundles is discussed in

* G. Giachetta, L. Mangiarotti, [[Gennadi Sardanashvily]], _Cohomology of the variational bicomplex on the infinite order jet space_, Journal of
Mathematical Physics 42, 4272-4282 (2001) ([arXiv:math/0006074](http://arxiv.org/abs/math/0006074))

where both versions (smooth functions being globally or locally of finite order) are discussed and compared.

Discussion of jet-restriction of the [[Haefliger groupoid]] is in 

* Arne Lorenz, _Jet Groupoids, Natural Bundles
and the Vessiot Equivalence Method_, Thesis ([pdf](http://wwwb.math.rwth-aachen.de/~arne/Dissertation_Lorenz_Arne.pdf))

Discussion of jet bundles in [[supergeometry]] includes

* Arthemy V. Kiselev, Andrey O. Krutov, appendix of _On the (non)removability of spectral parameters in $\mathbb{Z}_2$-graded zero-curvature representations and its applications_ ([arXiv:1301.7143](http://arxiv.org/abs/1301.7143))

See also

* {#KrasilshchikVerbovetsky98} [[Joseph Krasil'shchik]], [[Alexander Verbovetsky]], _Homological Methods in Equations of Mathematical Physics_ ([arXiv:math/9808130](http://arxiv.org/abs/math/9808130))

In the context of [[supermanifolds]], discussion is in 

* [[Gennadi Sardanashvily]], _Graded infinite order jet manifolds_, _Int. J. Geom. Methods Mod. Phys. v.4 (2007) 1335-1362_ ([arXiv:0708.2434](https://arxiv.org/abs/0708.2434))

[[!redirects jet bundles]]

[[!redirects jet]]
[[!redirects jets]]

[[!redirects jet type]]
[[!redirects jet types]]