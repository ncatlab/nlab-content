
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Idea

If in the context of [[stable homotopy theory]] the [[topological space]]s and [[spectra]] are equipped with an [[action]] of a [[topological group]] $G$ the theory refines to a _$G$-equivariant_ version. This is to [[equivariant homotopy theory]] (roughly) as [[stable homotopy theory]] is to [[homotopy theory]].

## Basic definitions

The definition of _$G$-spectrum_ is typically given in generalization of the definition of [[coordinate-free spectrum]].

A **$G$-universe** in this context is a infinite dimensional real [[inner product space]] equipped with a linear $G$-[[action]] that is the [[direct sum]] of countably many copies of a given [[set]] of (finite dimensional? -DMR) [[representation]]s of $G$, at least containing the trivial representation on $\mathbb{R}$ (so that $U$ contains at least a copy of $\mathbb{R}^\infty$).

Each such subspace of $U$ (representation contained in $U$? -DMR) is called an _indexing space_ . For $V \subset W$ indexing spaces, write $W-V$ for the orthogonal complement of $V$ in $W$. Write $S^V$ for the [[one-point compactification]] of $V$ and for $X$ any (pointed) [[topological space]] write $\Omega^V := [S^V,X]$ for the corresponding (based) sphere space.

A **$G$-space** in the following means a [[pointed object|pointed]] [[topological space]] equipped with a continuous [[action]] of the [[topological group]] $G$ that fixes the base point. A  morphism of $G$-spaces is a continuous map that fixes the basepoints and is $G$-equivariant.

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




## In terms of Mackey-functors

A _Mackey functor_ with values in [[spectra]] ("spectral Mackey functor") is an [[(∞,1)-functor]] on a suitable  [[(∞,1)-category of correspondences]] 
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

* [[Anna Marie Bohmann]], _Basic notions of equivariant stable homotopy theory_ ([pdf](http://math.uchicago.edu/~bohmann/basicequivnotions.pdf))

* [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

The characterization of $G$-equivariant functors in terms of topological [[Mackey functors]] is discussed in example 3.4 (i) of

* [[Stefan Schwede]], [[Brooke Shipley]], _Classification of stable model categories_ ([pdf](http://hopf.math.purdue.edu/Schwede-Shipley/class.final.pdf))

Something on modelling the equivariant stable category using functors on _all_ (nice) $G$-spaces (instead of on just the [[orbit category]]) is in 

* [[Andrew Blumberg]], _Continuous functors as a model for the equivariant stable homotopy category_ ([(arXiv:math.AT/0505512](http://arxiv.org/abs/math.AT/0505512))

A comprehensive construction of equivariant stable homotopy theory in terms of [[Mackey functors]] is in the series

* B. Guillou and [[Peter May]],  _Models of $G$-spectra as presheaves of spectra, ([arXiv:1110.3571](http://arxiv.org/abs/1110.3571))

  _Permutative $G$-categories in equivariant infinite loop space theory ([arXiv:1207.3459](http://arxiv.org/abs/1207.3459))

A fully [[(∞,1)-category theory|(∞,1)-category theoretic]] formulation is i 

* {#Barwick14} [[Clark Barwick]], _Spectral Mackey functors and equivariant algebraic K-theory (I)_ ([arXiv:1404.0108](http://arxiv.org/abs/1404.0108))


The [[May recognition theorem]] for $G$-spaces and genuine $G$-spectra is discussed in 

* Costenoble and Warner, _Fixed set systems of equivariant infinite loop spaces_ Transactions of the American mathematical society, volume 326, Number 2 (1991) ([JSTOR](http://www.jstor.org/pss/2001770))