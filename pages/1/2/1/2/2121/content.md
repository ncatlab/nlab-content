
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
=--
=--


#Contents#
* tabel of contents
{:toc}

## Idea

The concept of _diffiety_ ([Vinogradov 81](#Vinogradov81)) reflects the concept of _[[partial differential equation]]_ (generally non-linear) in analogy to how the concept of _[[algebraic variety]]_ reflects that of _[[polynomial]] [[equation]]_: 

A _diffiety_ is the [[solution]]-locus $\mathcal{E}\hookrightarrow J^\infty_\Sigma(E)$ of a [[partial differential equation]] $D \Phi = 0$  regarded as an ordinary [[equation]]  $\tilde D = 0$ on the [[jet bundle]] $J^\infty_\Sigma(E)$ of some [[bundle]] $E \overset{fb}{\to} \Sigma$.

Here $\Sigma$ is the space of [[free variables]] of the [[PDE]], $E \overset{fb}{\to} \Sigma$ is the bundle of [[dependent variables]], and a [[differential operator]] 

$$
  D \;\colon\; \Gamma_\Sigma(E) \longrightarrow \Gamma_\Sigma(F)
$$

on the [[space of smooth sections]] of $fb$ is represented by a [[bundle morphism]] 

$$
  \tilde D \colon J^\infty_\Sigma(E) \to F
$$

out of the [[jet bundle]] via [[jet prolongation]] $j^\infty_\Sigma \colon \Gamma_\Sigma(E) \to \Gamma_\Sigma(J^\infty_\Sigma(E))$ as $D \Phi = \tilde D (j^\infty_\Sigma(\Phi))$:

$\,$

$$
  \array{
    & \text{diffiety} && \text{jet bundle} & \array{\text{differential} \\ \text{operator}} &
    \\
    & 
    \mathcal{E}
      &\overset{\tilde D = 0}{\hookrightarrow}&
    J^\infty_\Sigma(E)
      &\overset{\tilde D}{\longrightarrow}&
    F
  }
$$


For instance in [[Lagrangian field theory]] the bundle in question is a [[field bundle]] $E \overset{fb}{\to} \Sigma$, the [[partial differential equation]] is the [[Euler-Lagrange equation]] $\delta_{EL}\mathbf{L} = 0$, and its diffiety solution locus $\mathcal{E}$ inside the [[jet bundle]] $J^\infty_\Sigma(E)$ is called the _[[shell]]_ of the field theory.


In [Marvan 86](#Marvan86) it was observed that Vinogradov's [[formally integrable PDE|formally integrable diffieties]] are equivalently the [[coalgebra over a comonad|coalgebras]] over the [[jet comonad]] acting on [[locally pro-manifold]]-[[bundles]] (over a base space $\Sigma$ of [[free variables]]). This statement generalizes to the [[synthetic differential geometry]] of the [[Cahiers topos]] $\mathbf{H}$ ([Khavkine-Schreiber 17](#KhavkineSchreiber17)), where the [[jet comonad]] is realized as the comonad corresponding to [[base change]] along the [[de Rham shape]] projection $\Sigma \overset{\eta_\Sigma}{\longrightarrow} \Im \Sigma$. By [[comonadic descent]] this implies that over [[formally smooth]] base spaces $\Sigma$ [[formally integrable PDE|formally integrable diffieties]] are equivalently the [[bundles]] over the [[de Rham shape]] $\Im \Sigma$:

$$
  PDEs_\Sigma(\mathbf{H})
  \;=\;
  Diffeties_\Sigma(\mathbf{H})
  \;\simeq\;
  J^\infty_\Sigma CoAlg\left(\mathbf{H}_{/\Sigma} \right)
  \;\simeq\;
  \mathbf{H}_{/\Im(\Sigma)}
$$

([Khavkine-Schreiber 17, thorem 3.52, theorem 3.60](#KhavkineSchreiber17))

This makes manifest how [[diffieties]] are the analog in [[differential geometry]] of concepts in [[algebraic geometry]]: For $\Sigma$ a suitable [[scheme]] then a [[quasicoherent module]] over its [[de Rham shape]] $\Im \Sigma$ ("[[crystal]]") is called a _[[D-module]]_ and represents an algebraic [[linear partial differential equation]], while a [[relative scheme]] over $\Im \Sigma$ is called a _[[D-scheme]]_ and represents a general algebraic [[partial differential equation]]. See also at _[[D-geometry]]_ for more on this.

## Related concepts

* [[variational calculus]]


## References

### General

* {#Vinogradov81} [[Alexandre Vinogradov]], _Geometry of nonlinear differential equations_, Journal of Soviet Mathematics 17 (1981) 1624&#8211;1649 ([doi:10.1007/BF01084594](https://doi.org/10.1007/BF01084594))

* {#Vinogradov84} [[Alexandre Vinogradov]], _Local symmetries and conservation laws_, Acta Appl. Math., Vol. 2, 1984, p. 21 ([MR85m:58192](http://www.ams.org/mathscinet-getitem?mr=736872), [doi](http://dx.doi.org/10.1007/BF01405491))

* {#Vinogradov89} [[Alexandre Vinogradov]], _Symmetries and conservation laws of partial differential equations: basic notions and results_, Acta Appl. Math., Vol. 15, 1989, p. 3. [MR91b:58282](http://www.ams.org/mathscinet-getitem?mr=1007340), [doi](http://dx.doi.org/10.1007/BF00131928)

* [[Alexandre Vinogradov]], _Scalar differential invariants, diffieties and characteristic classes_, in: Mechanics, Analysis and Geometry: 200 Years after, 379&#8211;414, [MR92e:58244](http://www.ams.org/mathscinet-getitem?mr=1098525)

* G. Cicogna, G. Gaeta, _Lie-point symmetries in bifurcation problems_, Annales de l'institut Henri Poincar&#233; (A) Physique th&#233;orique, 56 no. 4 (1992), p. 375-414 [numdam](http://www.numdam.org/item?id=AIHPA_1992__56_4_375_0)

* L. Vitagliano, _Hamilton-Jacobi diffieties_, [arxiv/1104.0162](http://arxiv.org/abs/1104.0162)



* [[Alexandre M. Vinogradov]]'s [webpage](https://diffiety.mccme.ru/curvita/amv.htm) 

* [[Joseph Krasil'shchik]]'s [webpage](https://diffiety.mccme.ru/curvita/isk.htm) (with links to some papers) and [wiki list of publications](http://gdeq.org/index.php?title=Joseph_Krasil%27shchik)


### Review

* [[Joseph Krasil'shchik]], [[Alexander Verbovetsky]], _Homological methods in equations of mathematical physics_, [arxiv:math.DG/9808130](http://xxx.lanl.gov/abs/math/9808130v2), 150 p.

* [[Joseph Krasil'shchik]], [[Alexander Verbovetsky]], Geometry of jet spaces and integrable systems, J. Geom. Phys. (2010), [doi](doi:10.1016/j.geomphys.2010.10.012), [arXiv:1002.0077](http://arxiv.org/abs/1002.0077)


See also

* wikipedia: [diffiety](http://en.wikipedia.org/wiki/Diffiety), [secondary calculus and cohomological physics](http://en.wikipedia.org/wiki/Secondary_calculus_and_cohomological_physics)


### As jet coalgebras
 {#ReferencesAsJetCoalgebras}

Diffieties as [[coalgebra over a comonad|coalgebras]] over the [[jet comonad]] are discussed in

* {#Marvan86} [[Michal Marvan]], _A note on the category of partial differential equations_, in _Differential geometry and its applications_, Proceedings of the Conference August 24-30, 1986, Brno ([[MarvanJetComonadPDE.pdf:file]])

* {#MarvanThesis} [[Michal Marvan]], thesis, 1989 ([[MarvanThesis.pdf:file]], [web](http://www.slu.cz/math/cz/lide/marvan-michal/docs/mar89-ocr.pdf))

* {#Marvan89} [[Michal Marvan]], _On the horizontal cohomology with general coefficients_, 1989 ([web announcement](http://old.math.slu.cz/People/MichalMarvan/Annotations/horizontal.php), [web archive](http://dml.cz/dmlcz/701469))

* {#Marvan93} [[Michal Marvan]], section 1.1 of _On Zero-Curvature Representations of Partial Differential Equations_,  (1993) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.45.5631))

* {#KhavkineSchreiber17} [[Igor Khavkine]], [[Urs Schreiber]], _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations: I. Jets and comonad structure]]_ ([arXiv:1701.06238](https://arxiv.org/abs/1701.06238))

### Conferences
 {#Conferences}

* [diffiety school](http://school.diffiety.org), [diffiety institute](https://diffiety.mccme.ru), [gdeq.org wiki](http://gdeq.org/index.php?title=Welcome_to_GDEq.org!)

* <div style="float:right;margin:0 10px 10px 0;"> <a href="http://www.dipmat2.unisa.it/people/vitagliano/www/DS2018_poster.png"><img src="http://www.dipmat2.unisa.it/people/vitagliano/www/DS2018_poster.png" width="150"></a></div> [XXI Summer Diffiety School School on Geometry of PDEs](https://sites.google.com/site/levicivitainstitute/Activities/DiffietySchools/xxi-summer-diffiety-school), July 19 - 31, 2018
   

[[!redirects diffieties]]