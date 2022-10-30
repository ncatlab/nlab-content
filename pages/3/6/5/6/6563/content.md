## Idea ##

**Universality** is a "term of the art" which means the following:

+-- {: .standout}
Under the proper conditions, different systems can exhibit the same behaviour, as measured by quantitative indices, if they meet the same qualitative criteria.  Sets of systems which are equivalent in this manner are known as **universality classes**.
=--

If we have some complicated phenomenon we can't understand directly, and we figure out (or make a good stab at guessing) the universality class to which it belongs, we can make testable predictions about the complicated thing by working with a simpler member of that universality class.  Membership in a universality class depends on properties like how many spatial dimensions a system lives in, symmetries and the like.  People have identified universality classes, with varying degrees of rigour.  Lots of them have names, sometimes even with dashes inside; the ones we understand less well and aren't so familiar with get abstruse symbols for labels instead.  A non-exhaustive tabulation of these labels might look something like this:

Stable Distributions | Equilibrium | Random Matrices | Non-Equilibrium | Extreme-Value Distributions | Dynamical Maps |
--------------|-------------------|-----------------|-----------------|--------------|-----------|
Gaussian      | 2D Ising          | Unitary         | Directed percolation | Gumbel  | 1D Feigenbaum |
Cauchy        | 2D Potts          | Orthogonal      | Dynamic percolation  | Fr&#233;chet | 2D Volume-preserving |
L&#233;vy          | 2D Tricritical Ising    | Symplectic | CDP  | Weibull | $\vdots$ |
&#160;              | 2D Tricritical Potts | $U(N+M)/U(N)\times U(M)$ | TDP | | |
&#160;              | 2D Other RSOS | $ Sp(N+M)/Sp(N)\times Sp(M)$ | Manna | | |
&#160;              | 3D Ising | $ Sp(2N) $ | Edwards--Wilkinson | | |
&#160;              | 3D Potts | $ SO(2N) $ | KPZ | | |
&#160;              | $\vdots$ | $ O(N+M) / O(N) \times O(M) $ | $\vdots$ | | |
&#160;              | &#160; | $ SO(2N) / U(N) $ | &#160; | | |
&#160;              | &#160; | $ Sp(2N) / U(N) $ | &#160; | | |

The general concept of [[renormalization]] is really important here.  The universality classes we understand best correspond to fixed points of renormalization-group transforms.

The first column, "stable distributions", basically comes from the central limit theorem and the ways in which the conditions necessary for it to apply can fail to obtain.  The middle column with all the funny symbols comes from [[Élie Cartan]]'s classification of [[symmetric space|symmetric spaces]].  The 2D part of the equilibrium statistical systems can be given a taxonomy based on the [[ADE classification]] of [[Dynkin diagram|Dynkin diagrams]] and [[conformal field theory|conformal field theories]].

Relationships from one column to another do exist. For example, dynamical surface growth and [[random matrix theory]] are, unexpectedly, linked: the [[eigenvalue]] distributions of the Gaussian Unitary and Gaussian Orthogonal Ensembles show up as surface heights in Kardar-Parisi-Zhang phenomena. See Takeuchi _et al._ (2011), "Growing interfaces uncover universal fluctuations behind scale invariance" _Sci Rep. (Nature)_ **1** 34, [arXiv:1108.2118](http://arxiv.org/abs/1108.2118).

## References ##

Various sources: 
* J. P. Sethna (2006), _Statistical Physics: Entropy, Order Parameters, and Complexity_. Oxford University Press. [Available on the author's website](http://pages.physics.cornell.edu/sethna/StatMech/).  See in particular chapter 12.
* _Nonequilibrium Phase Transitions_ (2008) by Henkel _et al._
* Vollmayr-Lee's talks on the "field theory approach to diffusion-limited reactions", [Boulder School for Condensed Matter and Materials Physics](http://boulder.research.yale.edu/Boulder-2009/Lectures/index.html) (2009), in particular lecture 4
* Kardar's _Statistical Physics of Particles_ and _Statistical Physics of Fields_
* G. Odor (2004), "Universality classes in nonequilibrium lattice systems" _Rev. Mod. Phys._ **76**: 663. [arXiv:cond-mat/0205644v7](http://arxiv.org/abs/cond-mat/0205644) 
* Henkel's _Conformal Invariance and Critical Phenomena_ (1999)
* P. A. Pearce (1994), "Recent progress in solving _A--D--E_ lattice models" _Physica A_ **205**: 15--30. This one brings in [[Temperley-Lieb algebra]]s, two-colour braid monoid algebras and [[Reidemeister moves]].
* P. Cvitanovic, ed. _Universality in Chaos_ (1983).
* and this conversation at the n-Category Caf&#233; on [the Tenfold Way](http://golem.ph.utexas.edu/category/2010/12/the_threefold_way_part_2.html#c035973).

