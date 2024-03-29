
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--


# Reduced Segal space
* table of contents
{: toc}

## Idea

A _reduced Segal space_ is a [[category object in an (∞,1)-category|category object]] in [[∞Grpd]] equipped with an (essentially) surjective functor from the terminal such. So it is the [[delooping]] of a [[monoid in an (∞,1)-category]].

Accordingly, if the reduced Segal space happens to be actually a [[groupoid object in an (∞,1)-category|groupoid object]], then it is the [[delooping]] of a [[group object in an (∞,1)-category|group object]] in [[∞Grpd]]: an [[∞-group]].


The notion was first introduced by [[G. Segal]] (who named it "special $\Delta$-space") as a means for the characterization of an [[infinite loop space]] via the notion of [[Gamma-space]]. 

When a reduced Segal space is group-like, it becomes a model for an [[infinity-group]] aka a loop space. Group-like reduced Segal spaces characterize loop spaces by means of finite products and weak equivalences and as such transparently show that the property of being a loop space is  invariant under any product-preserving endofunctor of topological spaces.

If $M$ is a topological monoid, its classifying space $BM$ has a model as a simplicial space in which the 0th level is a point and the nth level is n-times the product of the 1st level. The idea of a reduced Segal space is requiring the above two properties of the simplicial space $BM$ to hold up to homotopy and capture in this way all $\infty$-monoids.

The passage from reduced Segal spaces to group-like reduced Segal spaces is the step of adding "inverses up to coherent homotopy". It turns out to be equivalent to simply requiring that the monoid of path components of the 1st level admits a group structure.

## Definition

A simplicial space $X:\Delta^{op}\to Top$ is called a reduced Segal space if:

(1) the space $X_0$ is weakly [[contractible]];

(2) for each $n\geq 1$, the Segal map $X_n\to X_1\times ...\times X_1$ is a weak equivalence.

$X$ is called group-like reduced Segal space if in addition:

(3) the monoid structure on $\pi_0 X_1$, induced from the $H$-space structure on $X_1$, admits inverses (i.e. it is a group).

## Properties

Proposition([[G. Segal]]): if $X$ is a group-like reduced Segal space, the map $X_1\to \Omega |X|$ is a weak equivalence.

## Generalizations

* The idea of reduced Segal spaces can be used for the characterization of n-fold loop spaces by n-simplicial spaces $X:(\Delta^{op})^n\to Top$ in which the corresponding Segal maps are weak equivalences.
This is explained in "Iterated
Monoidal Categories" (below).


## Related concepts

* [[Segal space]], [[complete Segal space]], [[Gamma space]]

## References

* [[G. Segal]], "Categories and Cohomology Theories", Topology 13 (1974).

*  C. Balteanu, Z. Fiedorowicz, R. Schwanzl and [[R. Vogt]], "Iterated
Monoidal Categories", Advances in Mathematics (2003).

[[!redirects reduced Segal spaces]]

[[!redirects special Delta-space]]
[[!redirects special Delta-spaces]]
