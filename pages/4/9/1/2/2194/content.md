
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let $A$ be a [[abelian group|commutative]] ([[Hausdorff space|Hausdorff]]) [[topological group]]. A (continuous) *[[group character]]* of $A$ is any continuous homomorphism $\chi: A\to S^1$ to the [[circle group]]. The __Pontrjagin dual group__ $\widehat{A}$ is the commutative group of all characters of $A$ with pointwise multiplication (that is multiplication induced by multiplication in the [[circle group]], the multiplication of norm-$1$ complex numbers in $S^1\subset\mathbb{C}$) and with the topology of [[uniform convergence]] on each [[compact space|compact]] $K\subset A$ (this is equivalent to the [[compact-open topology]]). 

## Examples

The Pontrjagin dual of the additive group of [[integers]] $\mathbb{Z}$ is the [[circle group]] $S^1$, and conversely, $\mathbb{Z}$ is the Pontrjagin dual of $S^1$. This pairing of dual topological groups, given by $(n,z) \mapsto z^n$, is related to the subject of [[Fourier transforms]]. 

In general, the dual of a [[discrete space|discrete]] group is a [[compact space|compact]] group and conversely. In particular, therefore, the dual of a [[finite group]] is again finite.

For example, the finite [[cyclic groups]] are Pontrjagin self-dual.

The Pontrjagin dual $\hat{\mathbb{R}}$ of the additive group of [[real numbers]] is isomorphic again to $\mathbb{R}$ itself, with the pairing given by $(x,p) \mapsto \mathrm{e}^{\mathrm{i} x p}$.

Similarly, $\hat{\mathbb{R}^n}$ is isomorphic to the [[Cartesian space]] $\mathbb{R}^n$.

## Properties

### Pontrjagin duality theorem

\begin{theorem}
For every [[locally compact space|locally compact]] (Hausdorff) topological abelian group $A$, the natural function $A \mapsto \widehat{\widehat{A}}$ from $A$ into the Pontrjagin dual of the Pontrjagin dual of $A$, assigning to every $g\in A$ the continuous character $f_g$ given by $f_g(\chi)=\chi(g)$, is an [[isomorphism]] of topological groups (that is, a group isomorphism that is also a [[homeomorphism]]). 
\end{theorem}

Thus, the [[functor]]

$$LocCompAb^{op} \to LocCompAb: G \to \widehat{G}$$ 

is an [[equivalence of categories]], in fact an [[adjoint equivalence]] whose [[unit of an adjunction|unit]] is

$$A \to \widehat{\widehat{A}}: g \mapsto f_g$$ 

and whose [[counit of an adjunction|counit]] (the same arrow read in the opposite category) are [[isomorphisms]]. This contravariant self-equivalence restricts to equivalences 

$$Ab^{op} \to CompAb$$


$$CompAb^{op} \to Ab$$ 

where [[Ab]] is the category of ([[discrete topological space|discrete topological]]) groups and $CompAb$ is the category of abelian [[Hausdorff space|Hausdorff]] [[compact topological groups]], each 
embedded in $LocCompAb$ in the evident way. 

The [[Fourier transform]] on locally compact abelian groups is formulated in terms of Pontrjagin duals (see below). 



### Basic properties of dual groups

There are many properties of locally compact Hausdorff abelian groups that implies properties of their Pontrjagin duals.  For example:

* If $A$ is [[finite group|finite]], then $\widehat{A}$  is finite.

* If $A$ is [[compact topological group|compact]], then $\widehat{A}$ is [[discrete group|discrete]].

* If $A$ is [[discrete group|discrete]], then $\widehat{A}$  is [[compact topological group|compact]].

* If $A$ is [[torsion subgroup|torsion]]-free and [[discrete group|discrete]], then $\widehat{A}$ is [[connected topological space|connected]] and [[compact topological group|compact]].

* If $A$ is an [[abelian group|abelian]] [[torsion group]], then $\widehat A$ is an abelian [[profinite group]] (for more see at _[[Pontryagin duality for torsion abelian groups]]_)

* If $A$ is [[connected topological space|connected]] and [[compact topological group|compact]], then $\widehat{A}$ is [[torsion subgroup|torsion]]-free and [[discrete group|discrete]].

* If $A$ is a [[Lie group]], then $\widehat{A}$ is compactly generated in that there is a [[compact topological space|compact]] [[neighborhood]] of the [[neutral element]] that generates $\widehat{A}$ as a group. 

* If $A$ is compactly generated, then $\widehat{A}$ is a Lie group.

* If $A$ is [[second countable topological space|second countable]], then $\widehat{A}$ is second countable.

* If $A$ is [[separable topological space|separable]], then $\widehat{A}$ is [[metrizable topological space|metrizable]].

For a discussion of these facts see [Morris 77](#Morris77), [Armacost 81](#Armacost81), exposition in:

* Variations on Pontryagin duality, ([nCafe](http://golem.ph.utexas.edu/category/2008/11/variations_on_pontryagin_duali.html))

Another statement of this type is presented in [Mackey 1948](#Mackey48):

* $A$ is connected if and only if $\widehat{A}$ is a product of a discrete torsion-free group with a finite dimensional real vector space.

## Applications

Pontrjagin duality underlies the abstract framework of [[Fourier analysis]] on locally compact Hausdorff abelian groups $A$: by Fourier duality on $A$, there is a Hilbert space isomorphism ([[Fourier transform]])

$$\mathcal{F}_A: L^2(A, d\mu) \to L^2(\hat{A}, d\hat{\mu})\,,$$

where $d\mu$ is a suitable choice of [[Haar measure]] on $A$, and $d\hat{\mu}$ is a suitable choice of Haar measure on the dual group. Fourier duality is compatible with Pontrjagin duality in the sense that if $\hat{\hat{A}}$ is identified with $A$, then $\mathcal{F}_{\hat{A}}$ is the inverse of $\mathcal{F}_A$.

## Related concepts

* [[dual object]]

* [[Cartier duality]], [[Poincaré line bundle]]

* [[character group]]

* [[Pontryagin duality for torsion abelian groups]]


## References

### General

The original article:

* [[Lev Pontrjagin]], *Theory of topological commutative groups*, Uspekhi Mat. Nauk, 1936, no. 2, 177–195 ([mathnet:umn8882](http://mi.mathnet.ru/eng/umn8882))

  English translation: Annals of Mathematics Second Series, Vol. 35, No. 2 (Apr., 1934), pp. 361-388 ([doi:10.2307/1968438](https://doi.org/10.2307/1968438))


Gentle exposition:

* Partha Sarathi Chakraborty, *Pontrjagin duality for finite groups* ([[Chakraborty_PontrjaginDuality.pdf:file]])

Textbook accounts:

* {#Morris77} Sidney A. Morris, _Pontryagin Duality and the Structure of Locally Compact Abelian Groups_, London Math. Soc. Lecture Notes 29, Cambridge U. Press, 1977.

* {#Armacost81} David A. Armacost, _The Structure of Locally Compact Abelian Groups_, Dekker, New York, 1981.

See also

* Wikipedia, *[Pontryagin duality](https://en.wikipedia.org/wiki/Pontryagin_duality)*

Also:

* {#Mackey48} [[George Mackey]], *The Laplace Transform For Locally Compact Abelian Groups*, Proceedings of the National Academy of Sciences of the United States of America Vol. 34, No. 4 (Apr. 15, 1948), pp. 156-162 ([jstor:87968](https://www.jstor.org/stable/87968))

* [[Michael Barr]], *On duality of topological abelian groups* ([pdf](http://www.math.mcgill.ca/barr/ftp/pdffiles/abgp.pdf), [[Barr_PontrjaginDuality.pdf:file]])

  which provides a perhaps better context for Pontryagin duality than the category of locally compact Hausdorff abelian groups (also known as 'LCA groups').  Barr explains:

  > Did you know that there is a [[star-autonomous category|*-autonomous category]] of topological abelian groups that includes all the LCA groups and whose duality extends that of Pontrjagin?  The groups are characterized by the property that among all topological groups on the same underlying abelian group and with the same set of continuous homomorphisms to the circle, these have the finest topology.  It is not obvious that such a finest exists, but it does and that is the key.

### For higher groups

Discussion of [[categorification|categorified]] Pontrjagin duality for [[2-groups]] and application to [[topological T-duality]]:

* [[Ulrich Bunke]], [[Thomas Schick]], [[Markus Spitzweck]], [[Andreas Thom]], _Duality for topological abelian group stacks and T-duality_, Proceedings of the ICM 2006 satellite conference, Valladolid, Spain, 2006. Z&#252;rich: EMS. Series of Congress Reports, 227-347 (2008) ([arXiv:math/0701428](http://arxiv.org/abs/math/0701428))

* [[Calder Daenzer]], _A groupoid approach to noncommutative T-duality_, PhD, 2007 ([pdf](http://www.math.upenn.edu/grad/dissertations/DaenzerThesis.pdf))

[[!redirects Pontrjagin duals]]

[[!redirects Pontryagin dual]]
[[!redirects Pontryagin duals]]

[[!redirects Pontrjagin duality]]
[[!redirects Pontrjagin dualities]]

[[!redirects Pontryagin duality]]
[[!redirects Pontryagin dualities]]

[[!redirects Pontriagin dual]]
[[!redirects Pontriagin duals]]

[[!redirects Pontriagin duality]]
[[!redirects Pontriagin dualities]]

[[!redirects Понтрягин dual]]
[[!redirects Понтрягин duals]]

[[!redirects Понтрягин duality]]
[[!redirects Понтрягин dualities]]

