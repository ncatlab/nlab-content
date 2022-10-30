
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


#Contents#
* table of contents
{:toc}

## Idea

Equivariant stable homotopy theory over some [[topological group]] $G$ is the [[stable homotopy theory]] of [[G-spectra]]. This includes the [[naive G-spectra]] which constitute the actual [[stabilization]] of [[equivariant homotopy theory]], but is more general, one speaks of _genuine $G$-spectra_. Notably a genuine $G$-spectrum has [[homotopy groups]] graded not by the group of [[integers]], but by the [[representation ring]] of $G$ (usually called [[RO(G)-grading]]).

The concept of [[cohomology]] in equivariant stable homotopy theory is _[[equivariant cohomology]]_:

[[!include equivariant cohomology -- table]]

## Basic definitions

### In terms of looping by representation spheres

The definition of _[[G-spectrum]]_ is typically given in generalization of the definition of [[coordinate-free spectrum]].

A **[[G-universe]]** in this context is (e.g. [Greenlees-May, p. 10](#GreenleesMay)) an infinite dimensional real [[inner product space]] equipped with a linear $G$-[[action]] that is the [[direct sum]] of [[countable|countably]] many copies of a given [[set]] of (finite dimensional? -DMR) [[representations]] of $G$, at least containing the trivial representation on $\mathbb{R}$ (so that $U$ contains at least a copy of $\mathbb{R}^\infty$).

Each such subspace of $U$ (representation contained in $U$? -DMR) is called an _indexing space_ ([[RO(G)-grading]]). For $V \subset W$ indexing spaces, write $W-V$ for the [[orthogonal complement]] of $V$ in $W$. Write $S^V$ for the [[one-point compactification]] of $V$; and for $X$ any (pointed) [[topological space]] write $\Omega^V := [S^V,X]$ for the corresponding (based) sphere space.

A **[[G-space]]** in the following means a [[pointed object|pointed]] [[topological space]] equipped with a continuous [[action]] of the [[topological group]] $G$ that fixes the base point. A  morphism of $G$-spaces is a continuous map that fixes the basepoints and is $G$-equivariant.

A weak equivalence of $G$-spaces is a morphism that induces isomorphism on all $H$-fixed homotopy groups (...)

A **$G$-spectrum** $E$ (indexed on the chosen universe $U$) is

* for each indexing space $V \subset U$ a $G$-space $E V$;

* for each pair $V \subset W$ of indexing spaces a $G$-equivariant [[homeomorphism]]

  $$
    E V \stackrel{\simeq}{\to} \Omega^{W-V} E W
    \,.
  $$

A [[morphism]] $f : E \to E'$ of $G$-spectra is for each indexing space $V$ a morphism of $G$-spaces $f_V : E V \to E' V$, such that this makes the obvious diagrams commute.

This becomes a [[category with weak equivalences]] by setting:

a morphism $f$ of $G$-spectra is a **weak equivalence of $G$-spectra** if for every indexing space $V$ the component $f_V$ is a weak equivalence of $G$-spaces (as defined above).

This may be expressed directly in terms of the notion of **homotopy group of a $G$-spectrum**: this is ...

### In terms of orthogonal spectra with $G$-action

... ([Schwede 15](#Schwede15))...

### In terms of Mackey-functors

A _[[Mackey functor]]_ with values in [[spectra]] ("spectral Mackey functor") is an [[(∞,1)-functor]] on a suitable  [[(∞,1)-category of correspondences]] 
$Corr_1^{eff}(\mathcal{C}) \hookrightarrow Corr_1(\mathcal{C})$ which sends [[coproducts]] to [[smash product]]. (This is similar to the concept of [[sheaf with transfer]].)

$$
  S \;\colon\; Corr_1^{eff}(\mathcal{C}) \longrightarrow Spectra
$$

For $G$ a [[finite group]] and $\mathcal{C}= G Set$ its category of [[permutation representations]], then $S$ is a genuine $G$-[[equivariant spectrum]] ([Guillou-May 11](#GuillouMay11)).
 So in this case the [[homotopy theory]] of spectral Mackey functors is a presentation for [[equivariant stable homotopy theory]] ([Guillou-May 11](#GuillouMay11), [Barwick 14](#Barwick14)).

For $\mathcal{C}$ an [[abelian category]] this definition reduces ([Barwick 14](#Barwick14)) Mackey functors as originally defined in ([Dress 71](#Dress71)).


## Examples

* [[equivariant sphere spectrum]], [[equivariant stable cohomotopy]]

* [[equivariant connective topological K-theory]]

[[!include Segal completion -- table]]


* [[KR cohomology theory]]

* [[equivariant complex cobordism cohomology theory]]

* [[equivariant Morava K-theory]]



## Equivariant cohomology


The notion of [[cohomology]] relevant in equivariant stable homotopy theory is the flavor of [[equivariant cohomology]] (see there for details) called [[Bredon cohomology]]. (See also at _[[orbifold cohomology]]_.)

## Related concepts

* [[equivariant differential topology]]

* [[global equivariant homotopy theory]]

* [[rational equivariant stable homotopy theory]]

* [[equivariant motivic homotopy theory]]

* [[equivariant spectrum]], 

  [[equivariant sphere spectrum]], [[equivariant suspension spectrum]], [[equivariant homotopy group]], [[equivariant stable homotopy category]], [[tom Dieck splitting]], [[slice spectral sequence]]

* [[G-spectra]], [[naive G-spectra]], [[spectra with G-action]]

  [[G-spaces]]

* [[Burnside category]], [[Burnside ring]]

  [[Mackey functor]]

## References

Original articles include

* [[Graeme Segal]], _Equivariant stable homotopy theory_, Actes du Congr&#232;s International des Math&#233;maticiens (Nice, 1970), Tome 2, pp. 59--63. Gauthier-Villars, Paris, 1971. ([pdf](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0059.0064.ocr.pdf))

A textbook account in terms of [[G-spectra]] modeled on a complete [[G-universe]] is in 

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], and Mark Steinberger (with contributions by J.E. McClure), _Equivariant stable homotopy theory_, Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))

and a more modern version taking into account the theory of [[symmetric monoidal categories of spectra]] is in

* [[Michael  Mandell]], [[Peter May]], _Equivariant orthogonal spectra and S-modules_, Mem. Amer. Math. Soc. 159 (2002), no. 755, x+108. MR 2003i:55012 ([pdf](http://www.math.uiuc.edu/K-theory/0408/MMM.pdf), [K-theory archive](http://www.math.uiuc.edu/K-theory/0408/))

See also

* {#HillHopkinsRavenel09} [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], appendix of _On the non-existence of elements of Kervaire invariant one_, Annals of Mathematics Volume 184 (2016), Issue 1 ([doi:10.4007/annals.2016.184.1.1](https://doi.org/10.4007/annals.2016.184.1.1), [arXiv:0908.3724](http://arxiv.org/abs/0908.3724), [talk slides](https://www.math.rochester.edu/people/faculty/doug/otherpapers/Skye_handout.pdf)) 


Lecture notes are in

* {#Blumberg17} [[Andrew Blumberg]], _The Burnside category_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))


Further introductions and surveys include the following

* {#Carlsson92} [[Gunnar Carlsson]], _A survey of equivariant stable homotopy theory_,Topology, Vol 31, No. 1, pp. 1-27, 1992 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/carlsson1.pdf))

* {#Bohmann} [[Anna Marie Bohmann]], _Basic notions of equivariant stable homotopy theory_ ([pdf](http://math.northwestern.edu/~bohmann/basicequivnotions.pdf))

* {#GreenleesMay} [[John Greenlees]], [[Peter May]], _[[Equivariant stable homotopy theory]]_, in [[Ioan James]] (ed.), _[[Handbook of Algebraic Topology]]_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

* [[Brooke Shipley]], _An introduction to equivariant homotopy theory_ ([pdf](http://homepages.math.uic.edu/~bshipley/bonn.2.pdf))

* [Talbot workshop 2016](http://math.mit.edu/conferences/talbot/index.php?year=2016)

Lecture notes on [[G-spectra]] modeled as [[orthogonal spectra]] with $G$-actions are

* {#Schwede15} [[Stefan Schwede]], _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))
 
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

A construction of equivariant stable homotopy theory in terms of [[spectral Mackey functors]] is due to

* [[Bert Guillou]], [[Peter May]],  _Models of $G$-spectra as presheaves of spectra, ([arXiv:1110.3571](http://arxiv.org/abs/1110.3571))

  _Permutative $G$-categories in equivariant infinite loop space theory ([arXiv:1207.3459](http://arxiv.org/abs/1207.3459))

see at _[[spectral Mackey functor]]_ for more references.

A fully [[(∞,1)-category theory|(∞,1)-category theoretic]] formulation is i 

* {#Barwick14} [[Clark Barwick]], _Spectral Mackey functors and equivariant algebraic K-theory (I)_, Adv. Math., 304:646–727 ([arXiv:1404.0108](http://arxiv.org/abs/1404.0108))