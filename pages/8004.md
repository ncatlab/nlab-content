
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **permutative category** is a [[symmetric monoidal category]] (possibly taken to be [[internal category|internal to]] [[Top]]) in which [[associativity]] (including [[unitality]]) holds strictly.  Also known as a **symmetric strict monoidal category**.

## Definition

([May, def. 1](#May)) ([Elmendorf-Mandell, def. 3.1](#ElmendorfMandell)).

A permutative category is a [[strict monoidal category]] equipped with a natural transformation $B_{x,y}:x \otimes y \rightarrow y \otimes x$ such that:

* $(B_{x,y} \otimes Id_{z});(Id_{y} \otimes B_{x,z}) = B_{x,y \otimes z}$
* $B_{x,y};B_{y,x} = Id_{x \otimes y}$

In [[string diagrams]]:

[[permutative.jpg:pic]]

## Properties

Every [[symmetric monoidal category]] is [[equivalence of categories|equivalent]] to a permutative one ([Isbell](#Isbell)). 

The [[nerve]] of a permutative category is an [[E-infinity space]], and therefore can be infinitely delooped to obtain an [[infinite loop space]] as its [[group completion]].

\begin{proposition}
In a permutative category, for every object $x$, we have $B_{x,1}=Id_{x}$.
\end{proposition}
\begin{proof}
Apply the two equations of the definition by putting $y=1$ and $z=1$. We obtain:

* $(B_{x,1})^{2} = B_{x,1}$
* $B_{x,1};B_{1,x} = Id_{x}$

We obtain that $B_{x,1}=Id_{x}$ by postcomposing the first equation by $B_{1,x}$.

Note that it is not really possible to do this proof by using string diagrams.

\end{proof}

The equation $B_{x,1}=Id_{x}$ is taken as an axiom of a permutative category in the references above. This is maybe the consequence of a lack of care about what is an [[identity natural transformation]] in the definition of a [[strict monoidal category]]. The equations $f \otimes Id_{1} = f = Id_{1} \otimes f$ are of critical importance in the proposition above and they are obtained by requiring that the structural natural isomorphims $\lambda_{x}:1 \otimes x \rightarrow x$ and $\rho_{x}:x \otimes 1 \rightarrow x$ are [[identity natural transformations]]. However, even knowing this, the proposition is not completely trivial and appears in a version for non-strict braided monoidal categories in the paper "Braided monoidal categories" (Joyal, Street, 1986). 

## Related concepts

* [[PermCat]]

* [[K-theory of a permutative category]]

* [[bipermutative category]]

## References

An original account is in

* [[John Isbell]], _On coherent algebras and strict algebras_, J. Algebra 13 (1969)

Discussion in relation to [[symmetric spectra]] is in

* {#Schwede12} [[Stefan Schwede]], chapter I, section 7.5 of _[[Symmetric spectra]]_ (2012)


Discussion in the context of [[K-theory of a permutative category]] is in

* {#May} [[Peter May]], _The spectra associated to permutative categories_, Topology 17 (1978) ([pdf](http://www.math.uchicago.edu/~may/PAPERS/23.pdf))

* [[Peter May]], *$E_\infty$-spaces, group completions, and permutative categories*,  London Math. Soc. Lecture Notes No. 11, 1974, 61-94 ([doi:10.1017/CBO9780511662607.008](https://doi.org/10.1017/CBO9780511662607.008), [pdf](http://www.math.uchicago.edu/~may/PAPERS/13.pdf))

 
* [[Peter May]], _$E_\infty$ Ring Spaces and $E_\infty$ Ring spectra_, Springer lectures notes in mathematics, Vol. 533, (1977) ([pdf](http://www.math.uchicago.edu/~may/BOOKS/e_infty.pdf)) chaper VI

* {#ElmendorfMandell} [[Anthony Elmendorf]], [[Michael Mandell]], _Rings, modules and algebras in infinite loop space theory_, K-Theory 0680 ([web](http://www.math.uiuc.edu/K-theory/0680/), [pdf](http://www.math.uiuc.edu/K-theory/0680/RMAsubmit.pdf))

Discussion in the context of [[equivariant stable homotopy theory]] is in

* [[Bert Guillou]], [[Peter May]], _Permutative $G$-categories in equivariant infinite loop space theory_, Algebr. Geom. Topol. 17 (2017) 3259-3339 ([arXiv:1207.3459](http://arxiv.org/abs/1207.3459))
 


[[!redirects permutative categories]]
[[!redirects symmetric strict monoidal category]]
[[!redirects symmetric strict monoidal categories]]
