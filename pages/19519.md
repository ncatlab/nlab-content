# Bishop-compact spaces

* table of contents
{: toc}

## Idea

The classical notion of [[compact space]] (defined e.g. using the finite subcover property) is not very useful in point-based [[constructive mathematics|constructive]] topology (as opposed to [[locale]] theory or [[formal topology]]).  In particular, it is impossible to prove constructively that familiar spaces like the [[unit interval]] $[0,1]\subseteq \mathbb{R}$ are compact in this sense.  Since classically, a [[metric space]] (or more generally a [[uniform space]]) is compact if and only if it is [[complete space|complete]] and [[totally bounded space|totally bounded]], [[Errett Bishop]] decided to simply take the conjunction of the latter two properties as a *definition* of compactness in [[Bishop's constructive mathematics|his]] constructive mathematics.

## Definition

A [[uniform space]] is **Bishop-compact** if it is both [[complete space|complete]] and [[totally bounded space|totally bounded]].

## Properties

### Equivalence to open-cover compactness

In [[classical mathematics]] (more precisely, assuming the [[ultrafilter principle]]), a uniform space is Bishop-compact if and only if its underlying [[topological space]] is [[compact space|compact]] in the usual sense.  In fact, more can be said: a compact [[Hausdorff space]] admits a *unique* compatible uniformity, which is complete and totally bounded.  So Bishop-compactness is really equivalent to ordinary compactness in a strong sense.  One can also use Bishop-compactness to develop various parts of the theory of compactness directly; for instance, [Shulman](#ShulmanSOI) constructs the [[Stone-Cech compactification]] using Bishop-compactness for [[gauge spaces]].

### Topological invariance

Completeness and total boundedness are not individually topological invariants.  In other words, if two uniform spaces are topologically isomorphic (i.e. their underlying [[topological spaces]] are homemorphic), it doesn't follow that if one is complete or totally bounded then so is the other.  For example, $\mathbb{R} \cong (0,1)$ topologically, but the former is complete and not totally bounded, while the latter is totally bounded and not complete.

However, the fact that Bishop-compactness is classically equivalent to open-cover compactness means that it *is* topologically invariant: if two uniform spaces are topologically isomorphic, and one is both complete *and* totally bounded, then so is the other.

In constructive mathematics, though, even this much cannot be proven: the statement that Bishop-compactness is a topological invariant implies the [[fan theorem]], which is (classically true but) unprovable constructively.  This is essentially the content of section 3.2 of [Diener's thesis](#Diener08), though it is phrased there in contrapositive form (assuming a counterexample to the fan theorem, we can construct a counterexample to the topological invariance of Bishop-compactness).

This constructive failure of topological invariance for Bishop-compactness has been one of the impetuses for the constructive study of [[proximity spaces]], in the hope of finding a structure at least somewhat weaker than uniformity under which a point-based notion of compactness is invariant.

## References

* {#Diener08} Hannes Diener, *Compactness under constructive scrutiny* (Ph.D. thesis), 2008, [pdf](http://www.math.canterbury.ac.nz/~h.diener/publications/thesis.pdf)

* {#ShulmanSOI} [[Mike Shulman]], *The shape of infinity*, [arxiv](https://arxiv.org/abs/1209.2735)

[[!redirects Bishop-compact space]]
[[!redirects Bishop-compact spaces]]
[[!redirects Bishop-compact]]
[[!redirects Bishop-compactness]]
