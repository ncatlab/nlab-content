
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $A$ a [[von Neumann algebra]] write $A'$ for its [[commutant]] in the ambient algebra $B(\mathcal{H})$ of [[bounded operator]]s.

+-- {: .num_defn}
###### Definition

A von Neumann algebra $A$ is called a **factor** if its [[center]] is trivial
$$
  Z(A) := A \cap A' = \mathbb{C}1
  \,.
$$

Equivalently: if $A$ and its [[commutant]] $A'$ generate the full algebra of [[bounded operators]] $B(\mathcal{H})$.

=--

## Properties

Every von Neumann algebra may be written as a [[direct integral]] over factors. ([von Neumann 49](#vNeumann49))


## Classification

Factors are classified in terms of the [[K-theory]] of their categories of finite [[W\*-modules]].
A [[W\*-module]] over a factor $A$ is _finite_ if it is not isomorphic to its proper submodule.

### Type I

Type I factors are characterized by the condition that the K-theory of finite modules
is isomorphic to $\mathbf{Z}$, the group of integers.
The only factors of this type are of the from $B(H)$, bounded operators on a Hilbert space $H$.

### Type II

Type II factors are characterized by the condition that the K-theory of finite modules
is isomorphic to $\mathbf{R}$, the group of real numbers.

Type II factors are subdivided into two classes: type II$_1$ factors are characterized
by the condition that $A$ is a finite $A$-module,
whereas for a type II$_\infty$ factor $A$ is not a finite $A$-module. 

### Type III

Type III factors are characterized by the condition that the K-theory of finite modules
is trivial, i.e., only the zero module is finite.

Type III factors are further subdivided into three classes,
according to the structure of the center of their [[modular algebra]],
which is a commutative von Neumann algebra graded by purely imaginary numbers,
whose graded components are [[noncommutative L^p-spaces]].

By the [[von Neumann duality]] for commutative von Neumann algebras,
the spectrum of this center is a [[measurable space]] equipped with a σ-ideal
of negligible sets and the grading yields an action of $\mathbf{R}$, the group of real numbers.
This object is known as the [[noncommutative flow of weights]].

If the center is trivial (so the spectrum is a point), the factor has type III$_1$.
If the action of $\mathbf{R}$ is not periodic, then the factor has type III$_0$.
If the action is periodic with period $\lambda$, a positive real number,
then the factor has type III$_{\exp(-\lambda)}$.

## Related concepts

* [[C-star algebra]]

* [[uniformly hyperfinite algebra]]


## References

### General
 {#ReferencesGeneral}

The original articles:

The classification of factors into types I, II, III and the construction of examples not of type I:

* [[Francis J. Murray]], [[John von Neumann]], *On Rings of Operators*, Annals of Mathematics, Second Series, **37** 1 (1936) 116-229 &lbrack;[doi:10.2307/1968693](https://doi.org/10.2307/1968693), [jstor:1968693](https://www.jstor.org/stable/1968693)&rbrack;

Discussion of [[traces]] on these factors:

* [[Francis J. Murray]], [[John von Neumann]], *On rings of operators. II*, Trans. Amer. Math. Soc. **41** (1937) 208-248  &lbrack;[doi:10.2307/1989620](https://doi.org/10.2307/1989620), [jstor:1989620](https://www.jstor.org/stable/1989620)&rbrack;

On [[isomorphism]] of factors and proof of a single isomorphism class of approximately finite type $II_1$ factors:

* [[Francis J. Murray]], [[John von Neumann]], *On rings of operators. IV*, Annals of Mathematics, Second Series, **44** 4 (1943) 716-808 &lbrack;[doi:10.2307/1969107](https://doi.org/10.2307/1969107), [jstor:1969107](https://www.jstor.org/stable/1969107)&rbrack;

On decomposing [[von Neumann algebras]] as a [[direct integral]] of factors:

* {#vNeumann49} [[John von Neumann]], _On rings of operators, reduction theory_, Annals of Mathematics Second Series, Vol. 50, No. 2 (1949) &lbrack;[jstor:1969463]( http://www.jstor.org/stable/1969463)&rbrack;
 
Recollection of the history which made von Neumann turn to discussion of these "factors", motivated from considerations in the foundations of [[quantum mechanics]] and [[quantum logic]]:

* {#Rédei96} [[Miklos Rédei]], *Why John von Neumann did not Like the Hilbert Space formalism of quantum mechanics (and what he liked instead)*, Studies in History and Philosophy of Modern Physics **27** 4 (1996) 493-510 &lbrack;<a href="https://doi.org/10.1016/S1355-2198(96)00017-2">doi:10.1016/S1355-2198(96)00017-2</a>&rbrack;

Lecture notes:

* V.S. Sunder, _von Neumann algebras, $II_1$-factors, and their subfactors_ &lbrack;[pdf](https://www.imsc.res.in/~sunder/iitb3.pdf)&rbrack;

* Hideki Kosaki, _Type III factors and index theory_ (1993) &lbrack;[pdf](http://pages.uoregon.edu/njp/lec-f.pdf)&rbrack;

### Subfactors

The mathematics of inclusions of _subfactors_ is giving deep structural insights. See also at _[[planar algebra]]_. 

* [[Vaughan Jones]], 

  _Index for subfactors_, Invent. Math. __72__, I (I983); 

  _A polynomial invariant for links via von Neumann algebras_, Bull. AMS __12__, 103 (1985); 

  _Hecke algebra representations of braid groups and link polynomials_, Ann. Math. __126__, 335 (1987)

* [[Vaughan Jones]], [[Scott Morrison]], [[Noah Snyder]], _The classification of subfactors of index at most 5_ ([arXiv:1304.6141](http://arxiv.org/abs/1304.6141))
* Vaughan F. R. Jones, David Penneys, _Infinite index subfactors and the GICAR categories_, [arxiv/1410.0856](http://arxiv.org/abs/1410.0856)

Symmetries of depth two inclusions of subfactors may be described via associative [[bialgebroid]]s,

* Lars Kadison, Kornél Szlachányi, _Bialgebroid actions on depth two extensions and duality_, Adv. Math. __179__:1 (2003) 75-121 <a href="https://doi.org/10.1016/S0001-8708(02)00028-2">doi</a>



### Relation to quantum field theory
 {#ReferencesInQuantumFieldTheory}

On von Neumann algebra factors as algebras of [[quantum observables]] in [[quantum physics]] and [[quantum field theory]] (which was their original motivation, cf. [Rédei 1996](#Rédei96)):

* [[Jakob Yngvason]], _The role of type III factors in quantum field theory_ &lbrack;[arXiv:math-ph/0411058](https://arxiv.org/abs/math-ph/0411058)&rbrack;

* [[Jonathan Sorce]], *Notes on the type classification of von Neumann algebras* &lbrack;[arXiv:2302.01958](https://arxiv.org/abs/2302.01958)&rbrack;

* [[Roberto Longo]], [[Edward Witten]], *A note on continuous entropy* &lbrack;[arXiv:2202.03357](https://arxiv.org/abs/2202.03357), [spire:2029393](https://inspirehep.net/literature/2029393)&rbrack;

and particularly in [[quantum field theory on curved spacetime]]:

* [[Edward Witten]], *Why Does Quantum Field Theory In Curved Spacetime Make Sense? And What Happens To The Algebra of Observables In The Thermodynamic Limit?*, in *Dialogues Between Physics and Mathematics*, Springer (2022) &lbrack;[arXiv:2112.11614](https://arxiv.org/abs/2112.11614), [doi:10.1007/978-3-031-17523-7_11](https://doi.org/10.1007/978-3-031-17523-7_11)&rbrack;

* Edward Witten, *Algebras, Regions, and Observers* &lbrack;[arXiv:2303.02837](https://arxiv.org/abs/2303.02837)&rbrack;

such as on [[de Sitter spacetime]]:

* [[Venkatesa Chandrasekaran]], [[Roberto Longo]], [[Geoff Penington]], [[Edward Witten]], *An Algebra of Observables for de Sitter Space*, Journal of High Energy Physics **2023**  82 (2023) &lbrack;[arXiv:2206.10780](https://arxiv.org/abs/2206.10780), <a href="https://doi.org/10.1007/JHEP02(2023)082">doi:10.1007/JHEP02(2023)082</a>&rbrack;

and potential application of von Neumann algebra factors to [[quantum gravity]]:

* [[Edward Witten]], *Gravity and the Crossed Product*, Journal of High Energy Physics **2022** 8 (2022) &lbrack;[arXiv:2112.12828](https://arxiv.org/abs/2112.12828), <a href="https://doi.org/10.1007/JHEP10(2022)008">doi:10.1007/JHEP10(2022)008</a>&rbrack;

* [[Edward Witten]], *A Note On The Canonical Formalism for Gravity* &lbrack;[arXiv:2212.08270](https://arxiv.org/abs/2212.08270), [inspire:2615434](https://inspirehep.net/literature/2615434)&rbrack;




[[!redirects von Neumann algebra factors]]

[[!redirects von Neumann algebra subfactor]]
[[!redirects von Neumann algebra subfactors]]

[[!redirects subfactor]]
[[!redirects subfactors]]

