
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Idea

Equivariant stable homotopy theory over some [[topological group]] $G$ is the [[stable homotopy theory]] of [[G-spectra]]. This includes the [[naive G-spectra]] which constitute the actual [[stabilization]] of [[equivariant homotopy theory]], but is more general.

The concept of [[cohomology]] in equivariant stable homotopy theory is _[[equivariant cohomology]]_:

[[!include equivariant cohomology -- table]]

## Basic definitions

### In terms of looping by representation spheres

The definition of _[[G-spectrum]]_ is typically given in generalization of the definition of [[coordinate-free spectrum]].

A **[[G-universe]]** in this context is (e.g. [Greenlees-May, p. 10](#GreenleesMay)) an infinite dimensional real [[inner product space]] equipped with a linear $G$-[[action]] that is the [[direct sum]] of countably many copies of a given [[set]] of (finite dimensional? -DMR) [[representations]] of $G$, at least containing the trivial representation on $\mathbb{R}$ (so that $U$ contains at least a copy of $\mathbb{R}^\infty$).

Each such subspace of $U$ (representation contained in $U$? -DMR) is called an _indexing space_ . For $V \subset W$ indexing spaces, write $W-V$ for the orthogonal complement of $V$ in $W$. Write $S^V$ for the [[one-point compactification]] of $V$ and for $X$ any (pointed) [[topological space]] write $\Omega^V := [S^V,X]$ for the corresponding (based) sphere space.

A **[[G-space]]** in the following means a [[pointed object|pointed]] [[topological space]] equipped with a continuous [[action]] of the [[topological group]] $G$ that fixes the base point. A  morphism of $G$-spaces is a continuous map that fixes the basepoints and is $G$-equivariant.

A weak equivalence of $G$-spaces is a morphism that induces isomorphism on all $H$-fixed homotopy groups (...)

A **$G$-spectrum** $E$ (indexed on the chosen universe $U$) is

* for each indexing space $V \subset U$ a $G$-space $E V$;

* for each pair $V \subset W$ of indexing spaces a $G$-equivariant [[homeomorphism]]

  $$
    E V \stackrel{\simeq}{\to} \Omega^{W-V} E 
    \,.
  $$

A [[morphism]] $f : E \to E'$ of $G$-spectra is for each indexing space $V$ a morphism of $G$-spaces $f_V : E V \to E' V$, such that this makes the obvious diagrams commute.

This becomes a [[category with weak equivalences]] by setting:

a morphism $f$ of $G$-spectra is a **weak equivalence of $G$-spectra** if for every indexing space $V$ the component $f_V$ is a weak equivalence of $G$-spaces (as defined above).

This may be expressed directly in terms of the notion of **homotopy group of a $G$-spectrum**: this is ...


### In terms of Mackey-functors

A _[[Mackey functor]]_ with values in [[spectra]] ("spectral Mackey functor") is an [[(∞,1)-functor]] on a suitable  [[(∞,1)-category of correspondences]] 
$Corr_1^{eff}(\mathcal{C}) \hookrightarrow Corr_1(\mathcal{C})$ which sends [[coproducts]] to [[smash product]]. (This is similar to the concept of [[sheaf with transfer]].)

$$
  S \;\colon\; Corr_1^{eff}(\mathcal{C}) \longrightarrow Spectra
$$

For $G$ a [[finite group]] and $\mathcal{C}= G Set$ its category of [[permutation representations]], then $S$ is a genuine $G$-[[equivariant spectrum]] ([Guillou-May 11](#GuillouMay11)).
 So in this case the [[homotopy theory]] of spectral Mackey functors is a presentation for [[equivariant stable homotopy theory]] ([Guillou-May 11](#GuillouMay11), [Barwick 14](#Barwick14)).

For $\mathcal{C}$ an [[abelian category]] this definition reduces ([Barwick 14](#Barwick14)) Mackey functors as originally defined in ([Dress 71](#Dress71)).



## Equivariant cohomology

The notion of [[cohomology]] relevant in equivariant stable homotopy theory is the flavor of [[equivariant cohomology]] (see there for details) called [[Bredon cohomology]].

## Related concepts

* [[global equivariant homotopy theory]]

* [[slice spectral sequence]]

## References

Introductions and surveys include

* {#Carlsson92} [[Gunnar Carlsson]], _A survey of equivariant stable homotopy theory_,Topology, Vol 31, No. 1, pp. 1-27, 1992 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/carlsson1.pdf))

* {#Bohmann} [[Anna Marie Bohmann]], _Basic notions of equivariant stable homotopy theory_ ([pdf](math.northwestern.edu/~bohmann/basicequivnotions.pdf&#8206;))

* {#GreenleesMay} [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

A comprehensive textbook account in terms of [[G-spectra]] modeled on a complete [[G-universe]] is in 

* L.G. Lewis, [[Peter May]], and M. Steinberger (with contributions by J.E. McClure), _Equivariant stable homotopy theory_ Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))

and a more modern version taking into account the theory of [[symmetric monoidal categories of spectra]] is in

* [[Michael  Mandell]], [[Peter May]], _Equivariant orthogonal spectra and S-modules_, Mem. Amer. Math. Soc. 159 (2002), no. 755, x+108. MR 2003i:55012 ([pdf](http://www.math.uiuc.edu/K-theory/0408/MMM.pdf), [K-theory archive](http://www.math.uiuc.edu/K-theory/0408/))

An alternative perspective on this is in 

* [[Mark Hovey]], [[David White]], _An alternative approach to equivariant stable homotopy theory_ ([arXiv:1312.3846](http://arxiv.org/abs/1312.3846))

Generalization from equivariance under [[compact Lie groups]] to [[compact topological groups]] (Hausdorff) and in particular to [[profinite groups]] and [[pro-homotopy theory]] is in  

* {#Fausk06} [[Halvard Fausk]], _Equivariant homotopy theory for pro-spectra_ ([arXiv:math/0609635](http://arxiv.org/abs/math/0609635))

The [[May recognition theorem]] for [[G-spaces]] and [[genuine G-spectra]] is discussed in 

* Costenoble and Warner, _Fixed set systems of equivariant infinite loop spaces_ Transactions of the American mathematical society, volume 326, Number 2 (1991) ([JSTOR](http://www.jstor.org/pss/2001770))

Characterization of [[G-spectra]] [via excisive functors](spectrum+object#ViaExcisiveFunctors) on [[G-spaces]] is in 

* [[Andrew Blumberg]], _Continuous functors as a model for the equivariant stable homotopy category_ ([arXiv:math.AT/0505512](http://arxiv.org/abs/math.AT/0505512))


The characterization of $G$-equivariant functors in terms of topological [[Mackey functors]] is discussed in example 3.4 (i) of

* [[Stefan Schwede]], [[Brooke Shipley]], _Classification of stable model categories_ ([pdf](http://hopf.math.purdue.edu/Schwede-Shipley/class.final.pdf))

A comprehensive construction of equivariant stable homotopy theory in terms of [[Mackey functors]] is in the series

* B. Guillou and [[Peter May]],  _Models of $G$-spectra as presheaves of spectra, ([arXiv:1110.3571](http://arxiv.org/abs/1110.3571))

  _Permutative $G$-categories in equivariant infinite loop space theory ([arXiv:1207.3459](http://arxiv.org/abs/1207.3459))

A fully [[(∞,1)-category theory|(∞,1)-category theoretic]] formulation is i 

* {#Barwick14} [[Clark Barwick]], _Spectral Mackey functors and equivariant algebraic K-theory (I)_ ([arXiv:1404.0108](http://arxiv.org/abs/1404.0108))