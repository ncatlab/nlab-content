+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

> This entry is about the phenomenon of [[universality]] in [[physics]]. See also [[universal property]] for a (different) concept of a similar name in [[mathematics]].

***

#Contents#
* table of contents
{:toc}

## Idea ##

In [[physics]], **universality** is a term which means the following:

+-- {: .standout}
Under the proper conditions, different systems can exhibit the same behaviour, as measured by quantitative indices, if they meet the same qualitative criteria.  Sets of systems which are equivalent in this manner are known as **universality classes**.
=--

If we have some complicated phenomenon we can't understand directly, and we figure out (or make a good stab at guessing) the universality class to which it belongs, we can make testable predictions about the complicated thing by working with a simpler member of that universality class.  Membership in a universality class depends on properties like how many spatial [[dimensions]] a system lives in, [[symmetry|symmetries]] and the like.  People have identified universality classes, with varying degrees of rigour.  Lots of them have names, sometimes even with dashes inside; the ones we understand less well and aren't so familiar with get abstruse symbols for labels instead.  A non-exhaustive tabulation of these labels might look something like this:

Stable Distributions | Equilibrium | Random Matrices | Non-Equilibrium | Extreme-Value Distributions | Dynamical Maps |
--------------|-------------------|-----------------|-----------------|--------------|-----------|
Gaussian      | 2D Ising          | [[unitary group|Unitary]]         | Directed percolation | Gumbel  | 1D Feigenbaum |
Cauchy        | 2D Potts          | [[orthogonal group|Orthogonal]]      | Dynamic percolation  | Fr&#233;chet | 2D Volume-preserving |
L&#233;vy          | 2D Tricritical Ising    | [[symplectic group|Symplectic]] | CDP  | Weibull | $\vdots$ |
&#160;              | 2D Tricritical Potts | $U(N+M)/U(N)\times U(M)$ | TDP | | |
&#160;              | 2D Other RSOS | $ Sp(N+M)/Sp(N)\times Sp(M)$ | Manna | | |
&#160;              | 3D Ising | $ Sp(2N) $ | Edwards--Wilkinson | | |
&#160;              | 3D Potts | $ SO(2N) $ | KPZ | | |
&#160;              | $\vdots$ | $ O(N+M) / O(N) \times O(M) $ | $\vdots$ | | |
&#160;              | &#160; | $ SO(2N) / U(N) $ | &#160; | | |
&#160;              | &#160; | $ Sp(2N) / U(N) $ | &#160; | | |

The general concept of [[renormalization]] is really important here.  The universality classes we understand best correspond to fixed points of renormalization-group transforms.

The first column, "stable distributions", basically comes from the [[central limit theorem]] and the ways in which the conditions necessary for it to apply can fail to obtain.  The middle column with all the funny symbols comes from [[Élie Cartan]]'s classification of [[symmetric space|symmetric spaces]].  The 2D part of the [[equilibrium]] statistical systems can be given a taxonomy based on the [[ADE classification]] of [[Dynkin diagram|Dynkin diagrams]] and [[conformal field theories]].  As [Cardy (2010)](#Takeuchi) writes,

+-- {: .standout}
[T]he study of the [[representation theory]] of the [[Virasoro algebra]] gives a way of classifying all possible [[CFT]]s and thereby universality classes in 2d. The breakthrough in this direction came following the seminal 1984 paper of Belavin, Polyakov and Zamolodchikov (BPZ) in which they showed that, for certain special rational values of $c \lt 1$, the [[CFT]] closes with only a finite number of [[representation]]s of the Virasoro algebra, and, for, these cases, all the [[critical exponent]]s and multi-point [[correlation function]]s are calculable. Shortly thereafter Friedan, Qiu and Shenker showed that unitary CFTs (corresponding to local, positive definite Boltzmann weights) are a subset of this list, with $c = 1 - 6/m(m + 1)$ and $m$ an integer $\geq 3$. This gives rise to what might be termed the 'conformal periodic table'. The first few examples may be identified with well-known universality classes. The 'hydrogen atom' of CFT is the scaling limit of the critical Ising model, 'helium' is the tricritical Ising model, and so on. Note, however, that at the next value of $c = 4$ two possible 'isotopes' arise. In the second, corresponding to the critical 3-state Potts model, not all the scaling dimensions allowed by BPZ in fact occur, but some of those that do actually appear twice. In fact the constraint of unitarity is not sufficient to determine exactly which representations actually occur in a given CFT. The answer to this is provided by demanding consistency of the theory on a [[torus]], by interchanging the interpretations of space and imaginary time [...]. For the torus, this is a [[modular form|modular]] transformation, and the requirement of modular invariance has become another powerful tool in classifying CFTs, completely solved in the case $c \lt 1$ by Cappelli, Itzykson and Zuber.
=--

Relationships from one column to another do exist. For example, dynamical surface growth and [[random matrix theory]] are, unexpectedly, linked: the [[eigenvalue]] distributions of the [[Gaussian Unitary Ensemble|Gaussian Unitary]] and [[Gaussian Orthogonal Ensemble|Gaussian Orthogonal Ensembles]] show up as surface heights in Kardar-Parisi-Zhang phenomena. See ([Takeuchi _et al._](#Takeuchi)).

## Timeline ##

The modern terminology of this subject dates to the late 1960s and early '70s.  By 1968, the quantitative concurrence of [[critical exponent]]s experimentally observed in magnetic materials and fluid phase transitions was sufficiently well established that it was reasonable to ask, "To what extent are the observed values of the critical-point exponents universal?" ([Fisher 1968](#Fisher1968))  At the 1970 Enrico Fermi summer school in Varenna, Italy, Leo P. Kadanoff summarized recent results with a "hypothesis of universality" which the conference proceedings record as follows:

+-- {: .standout}
All phase transition problems can be divided into a small number of different classes depending upon the dimensionality of the system and the symmetries of the order state. Within each class, all phase transitions have identical behaviour in the critical region, only the names of the variables are changed. ([Kadanoff 1971](#Kadanoff1971))
=--

The following is a capsule history tabulating some important events in the historical development of the modern understanding of universality.

|Year| |Contributors     | |Event|
|----|-|-----------------|-|-----|
|1733| |de Moivre| | Suggestion of what we now know as the [[central limit theorem]]|
|1822| |Cagniard de la Tour| | Observation of critical point at end of liquid-gas coexistence curve |
|1873--75| |van der Waals, Maxwell| | Equation of state for non-ideal gases, and its application to phase transitions |
|1895| |P. Curie| | Experimental observation of demagnetization by heat; pointing out similarity between liquid-gas and ferromagnetic transitions |
|1896| | Verschaffelt | | Discovery that the critical exponents predicted from van der Waals theory do not match experiment |
|1901| |Lyapunov| | Demonstration of why the central limit theorem works|
|1908| |Smoluchowski| | Discovery that critical opalescence is due to density fluctuations across many scales |
|1937| |Landau| | General mean-field theory of phase transitions|
|1944| |Onsager| | Exact solution of 2D [[Ising model]], illuminating the breakdown of analyticity and providing a valuable comparison point for later approximation techniques|
|1947--49| |Feynman, Schwinger, Tomonaga| | Workable [[renormalization]] techniques for "sweeping infinities under the rug" in [[quantum electrodynamics]] |
|1954--56| |Stueckelberg, Gell-Mann, Bogoliubov _et al._ | | Discovery that the "renormalization group" (RG) captured an important formal property of [[quantum field theory]] |
|1955| | Wigner | | Eigenvalue statistics of random matrices |
|1970--72| |Kadanoff, Wilson _et al._ | | Development of RG concept, discovery that it explains universal properties of phase transitions like critical exponents |
|1976 | | Doi| | Second-quantization formalism for classical stochastic many-particle dynamics |
|1976--79| |Feigenbaum| | Observation and use of RG to explain universal scaling exponents in 1D dynamical maps |
|1977| | Hohenberg, Halperin | | Classification of critical phenomena in dynamic continuum theories |
|1978--80| |Grassberger, Sundermeyer, de la Torre, Cardy, Sugar| | Connection of [[Reggeon field theory]] with directed percolation |
|1980| |Libchaber _et al._ | | Observation of Feigenbaum's constants in experimental systems, starting with convection of mercury |
| 1981--82 | | Janssen, Grassberger | | Formulation of DP conjecture, setting out the likely criteria for phase transitions to belong to the directed-percolation class | 
| 1984 | | Belavin, Polyakov, Zamolodchikov | | [[conformal field theory]] in 2D |
| 1986 | | Zamolodchikov | | [[c-theorem]] for 2D theories, identifying RG fixed points with CFTs of specific [[Virasoro algebra|central charges]] |
|1986| |Kardar, Parisi, Zhang | | KPZ equation for dynamical surface growth by deposition, showing that RG is applicable to its far-from-equilibrium dynamics |
|1996--97| |Zirnbauer, Altland| | Symmetry classes (not _exactly_ the same thing as universality classes, but clearly part of the same picture) for random matrices, following Cartan's classification of symmetric spaces |
|1998--99 | | Freedman, _et al._ | | First indications that the [[AdS/CFT correspondence]] and related implementations of gauge/gravity duality could lead to a "holographic $c$-theorem" generalising Zamolodchikov's work to higher dimensions |



## References ##

General sources: 

* [[Terence Tao|T. Tao]] (2010), "A second draft of a non-technical article on universality" ([web](http://terrytao.wordpress.com/2010/09/14/a-second-draft-of-a-non-technical-article-on-universality/))

Statistical distributions:
* Wikipedia, [stable distribution](http://en.wikipedia.org/wiki/Stable_distribution)
* Wikipedia, [Fisher&#8211;Tippett&#8211;Gnedenko theorem](http://en.wikipedia.org/wiki/Fisher%E2%80%93Tippett%E2%80%93Gnedenko_theorem)

Equilibrium critical phenomena:
* B. Berche _et al._ (2009), "Critical phenomena: 150 years since Cagniard de la Tour" _J. Phys. Studies_ **13**: 3201, [arXiv:0905.1886](http://arxiv.org/abs/0905.1886).
* J. P. Sethna (2006), _Statistical Physics: Entropy, Order Parameters, and Complexity_. Oxford University Press. [Available on the author's website](http://pages.physics.cornell.edu/sethna/StatMech/).  See in particular chapter 12.
* Kardar's _Statistical Physics of Particles_ and _Statistical Physics of Fields_
* Henkel's _Conformal Invariance and Critical Phenomena_ (1999)
* P. A. Pearce (1994), "Recent progress in solving _A--D--E_ lattice models" _Physica A_ **205**: 15--30. ([pdf](http://mac0916.ms.unimelb.edu.au/~pap/Publications_pdf/1994PearceRecentProgressADE.pdf)) This one brings in [[Temperley-Lieb algebra]]s, two-colour braid monoid algebras and [[Reidemeister moves]].
* J. Cardy (2010), _The Ubiquitous 'c': From the Stefan--Boltzmann Law to Quantum Information_, J.Stat.Mech. **2010**: P10004, ([arXiv:1008.2331](http://arxiv.org/abs/1008.2331))
  {#Cardy2010}
* A. Cappelli and J.-B. Zuber (2010), _A-D-E Classification of Conformal Field Theories_ Scholarpedia, 5(4): 10314 ([web](http://www.scholarpedia.org/article/A-D-E_Classification_of_Conformal_Field_Theories)).  Also available as [arXiv:0911.3242](http://arxiv.org/abs/0911.3242).
* Michael E. Fisher (1968), _Renormalization of Critical Exponents by Hidden Variables_ Physical Review **176**: 257--72. ([web](http://link.aps.org/doi/10.1103/PhysRev.176.257))
  {#Fisher1968}
* L. P. Kadanoff (1971), _Critical Behavior. Universality and Scaling_ in Proceedings of the International School of Physics Enrico Fermi, Course LI (27 July -- 8 August 1970). Edited by M. S. Green.
  {#Kadanoff1971}

Random matrix theory:
* Yan Fyodorov (2011) Random matrix theory. Scholarpedia, 6(3):9886 ([web](http://www.scholarpedia.org/article/Random_matrix_theory))
* this conversation at the n-Category Caf&#233; on [the Tenfold Way](http://golem.ph.utexas.edu/category/2010/12/the_threefold_way_part_2.html#c035973).

Nonequilibrium critical phenomena:
* P. C. Hohenberg and B. I. Halperin (1977). "Theory of dynamic critical phenomena" _Rev. Mod. Phys._ **49**: 435. ([web](http://www.physics.mcgill.ca/~omid/Hohenberg_Halperin.pdf))
* _Nonequilibrium Phase Transitions_ (2008) by Henkel _et al._
* Vollmayr-Lee's talks on the "field theory approach to diffusion-limited reactions", [Boulder School for Condensed Matter and Materials Physics](http://boulder.research.yale.edu/Boulder-2009/Lectures/index.html) (2009), in particular lecture 4
* G. Odor (2004), "Universality classes in nonequilibrium lattice systems" _Rev. Mod. Phys._ **76**: 663. [arXiv:cond-mat/0205644v7](http://arxiv.org/abs/cond-mat/0205644) 
* Takeuchi _et al._ _Growing interfaces uncover universal fluctuations behind scale invariance_  Sci Rep. (Nature) **1** 34, ([arXiv:1108.2118](http://arxiv.org/abs/1108.2118))
  {#Takeuchi}

Dynamical maps and chaos theory:

* P. Cvitanovic, ed. _Universality in Chaos_ (1983).
