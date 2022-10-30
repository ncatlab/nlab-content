
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_theorem #KoszulMalgrangeTheorem}
###### Theorem 

[[holomorphic vector bundle|Holomorphic vector bundles]] over a ([[compact topological space|compact]]) [[complex manifold]] $X$ are equivalently [[complex vector bundles]] $E$ which are equipped with a holomorphically [[flat connection]] $\nabla$, hence with a [[covariant derivative]] 

$$
  \bar \partial_E \colon \Gamma(E)\longrightarrow \Gamma(E) \otimes_{C^\infty(X, \mathbb{C})}\Omega^{0,1}(X)
$$

such that $\bar \partial_E \circ \bar \partial_E = 0$, hence with a compatible [[Dolbeault operator]]

The analogous statement is true for generalization of vector bundles to [[chain complexes]] of [[module sheaves]] with [[coherent cohomology]].

=--

For [[complex vector bundles]] over [[complex varieties]] this statement is due to [[Alexander Grothendieck]] and ([Koszul-Malgrange 58](#KoszulMalgrange58)), recalled for instance as ([Pali 06, theorem 1](#Pali06)). It may be understood as a special case of the [[Newlander-Nirenberg theorem]], see ([Delzant-Py 10, section 6](#DelzantPy10)), which also generalises the proof to [[infinite-dimensional manifold|infinite-dimensional]] vector bundles. Over [[Riemann surfaces]], see [below](#OverRiemannSurfaces), the statement was highlighted in ([Atiyah-Bott 83](#AtiyahBott83)) in the context of the [[Narasimhan-Seshadri theorem]]. 

As an [[equivalence of categories]] and with [[vector bundles]] generalized to [[coherent sheaves]] the statement appears in ([Pali 06](#Pali06)). This is generalized to an equivalence of [[homotopy categories]] of [[categories of chain complexes]] of coherent sheaves, hence to the [[derived category]] $D_{coh}^b(X)$ of $\mathcal{O}_X$-[[modules]] with [[coherent cohomology]], in ([Block 05, theorem 4.1.3](#Block05)).

+-- {: .num_remark}
###### Remark

The equivalence in theorem \ref{KoszulMalgrangeTheorem} serves to relate a fair bit of [[differential geometry]]/[[differential cohomology]] with constructions in [[algebraic geometry]]. For instance [[intermediate Jacobians]] arise in [[differential geometry]] and [[quantum field theory]] as [[moduli spaces of flat connections]] equipped with [[symplectic structure]] and [[Kähler polarization]], all of which in terms of [[algebraic geometry]] directly comes down [[moduli spaces]] of [[abelian sheaf cohomology]] with [[coefficients]] in the [[structure sheaf]] (and/or some variants of that, under the exponential exact sequence).

=--

We state the derived version in more detail:

+-- {: .num_defn #ChainComplexesOfHolomorphicFlatConnections}
###### Definition

For $X$ a [[complex manifold]], write 

$$
  CE(T_{hol} X) \coloneqq (\Omega^{0,\bullet}(X), \bar \partial)
$$ 

for its [[Dolbeault complex]] regarded as a [[differential graded algebra]] (the [[Chevalley-Eilenberg algebra]] of its holomorphic [[tangent Lie algebroid]]). Define a [[dg-category]] $Rep(T_{hol} X)$ whose

* [[objects]] are [[finite type]] [[∞-Lie algebroid representations]] of $T_{hol} X$, hence [[cochain complexes]] of [[complex vector bundles]] $E^{\bullet}$ over $X$ equipped with a $\mathbb{C}$-linear map

  $$
    \bar \partial_E
    \;\colon\;
    \Gamma(E)^\bullet
    \longrightarrow
    \Gamma(E)^\bullet \otimes_{C^\infty(X,\mathbb{C})} CE(T_{hol}X)
  $$

  that extend to a graded [[derivation]] on $\Gamma(E)^\bullet \otimes_{C^\infty(X,\mathbb{C})} CE(T_{hol}X)$;

* [[hom-objects]] are the evident [[chain complexes]] (...).


=--

([Block 05, def. 2.3.2 in theorem 4.1.3](#Block05)).

+-- {: .num_theorem}
###### Theorem

For $X$ a [[compact topological space|compact]] [[complex manifold]], there is an [[equivalence of categories]]

$$
  Ho Rep(T_{hol}X) \simeq D^b_{coh}(X)
$$

between the [[homotopy category]] of the [[dg-category]] of complexes of holomorphic flat connections, def. \ref{ChainComplexesOfHolomorphicFlatConnections}, and the bounded [[derived category]] of $\mathcal{O}_X$-[[module sheaves]] with [[coherent cohomology]].

=--

([Block 05, theorem 4.1.3](#Block05)).

## Related theorems

* [[Narasimhan-Seshadri theorem]]

* [[Donaldson-Uhlenbeck-Yau theorem]]

* [[Kobayashi-Hitchin correspondence]]

## References

The classical statement of theorem \ref{KoszulMalgrangeTheorem} is due (according to [Pali 06](#Pali06)) to [[Alexander Grothendieck]] and

* {#KoszulMalgrange58} [[Jean-Louis Koszul]], [[Bernard Malgrange]], _Sur certaine structures fibr&#233;es complexes_, arch. mat, vol IX, 1958

Over [[Riemann surfaces]] and in the context of the [[moduli space of flat connections]]:

* {#AtiyahBott83} [[Michael Atiyah]], [[Raoul Bott]], _The Yang-Mills equations over Riemann surfaces_, Philosophical Transactions of the Royal Society of London. Series A, Mathematical and Physical Sciences
Vol. 308, No. 1505 (Mar. 17, 1983), pp. 523-615 ([jstor](http://www.jstor.org/stable/37156), [lighning summary](http://math.stackexchange.com/a/295505/58526))

* {#Evans} [[Jonathan Evans]], _[Aspects of Yang-Mills theory](http://www.homepages.ucl.ac.uk/~ucahjde/yangmills.htm)_, lecture notes, ([lecture 10](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture10.pdf), [lecture 11](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture11.pdf), [lecture 12](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture12.pdf))

Generalization to [[coherent sheaves]] is due to 

* {#Pali06} N. Pali, _Faisceaux $\bar \partial$-cohrents sur les vari&#233;t&#233; complexes_ ( _$\bar \partial$-Coherent sheaves on complex manifolds) Math.
Ann. 336 (2006), no. 3, 571&#8211;615 ([arXiv:math/0305422](http://arxiv.org/abs/math/0305422))

Further Generalization to [[chain complexes]] of holomorphic vector bundles is discussed in 

* {#Block05} [[Jonathan Block]], _Duality and equivalence of module categories in noncommutative geometry I_ ([arXiv:0509284](http://arxiv.org/abs/math/0509284))


in terms of [[Lie infinity-algebroid representations]] of the holomorphic [[tangent Lie algebroid]].

Generalization to [[infinite-dimensional manifold|infinite-dimensional]] vector bundles is in 

* {#DelzantPy10} Thomas Delzant, Pierre Py, _K&#228;hler groups, real hyperbolic spaces and the Cremona group_, Compositio Math. 148, no. 1 (2012), 153--184 ([arXiv:1012.1585](http://arxiv.org/abs/1012.1585))