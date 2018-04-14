# Protocategories

* table of contents
{: toc}

## Idea

A *protocategory* is a way to present a [[category]] that makes formal the idea that a single datum (a "protomorphism") can represent many different [[morphisms]] with different sources and targets.  For instance, in [[material set theory]], a given set of [[ordered pairs]] can represent [[functions]] with many different codomains.

As compared to the definition of category with one set of objects and one set of morphisms, a protocategory removes the requirement that each morphism have a unique source and target.  As compared to the definition of category with separate hom-sets $\hom(A,B)$ for each pair of objects, a protocategory requires all these homsets to be (not necessarily disjoint) subsets of one set of all "protomorphisms".

## Definition

A **protocategory** consists of:

* Two collections of objects and protomorphisms
* A ternary "source-target relation" relating two objects and one protomorphism, written "$f : A\to B$" and read as "$f$ represents a morphism from $A$ to $B$"
* A ternary "composition predicate" relating three protomorphisms, written "$h = g \circ f$" and read as "$h$ is a possible composite of $f$ and $g$".

satisfying the axioms

* If $f:A\to B$ and $g:B\to C$, there is exactly one $h$ satisfying $h:A\to C$ and $g = g\circ f$.
* If we define the set of morphisms $\hom(A,B)$ to be the set of protomorphisms $f$ satisfying $f:A\to B$, then the composition operation given by the previous axiom results in a [[category]] (i.e. it is associative and has identities).

## Examples

* Let the objects be the [[sets]] in [[material set theory]] (such as [[ZFC]]), and let the protomorphisms be sets $f$ of ordered pairs such that for any $x$ there is at most one $y$ such that $(x,y)\in f$.  The *domain* of such an $f$ is the set of all $x$ such that there is such a $y$, and its *range* is the set of all $y$ such that there exists an $x$ with $(x,y)\in f$.  We say $f:A\to B$ if $A$ is the domain of $f$ and $B$ is a superset of the range of $f$.  With a suitable definition of composition, this yields a protocategory that generates the category [[Set]].

* More generally, if we take the protomorphisms to be *all* sets of ordered pairs, and $f:A\to B$ to mean that $A$ is a superset of the domain of $f$ in addition to $B$ being a superset of the codomain of $f$, then we get a protocategory that generates the category [[Rel]].

* Let the objects be [[groups]], let the protomorphisms be [[functions]], and say that $f:G\to H$ when $f$ is a function between the underlying sets of $G$ and $H$ that is a group homomorphism.  This protocategory generates the category [[Grp]].

* Any category can be presented by a protocategory in a trivial way, by taking the protomorphisms to be the [[disjoint union]] of all the sets of morphisms (i.e. the set $C_1$ in the one-set-of-morphisms definition of category), with the source-target relation being simply a function from protomorphisms to pairs of objects.

## References

* The notion is due to Freyd and Scedrov, [[Categories, Allegories]].

* It is recalled in A1.1 of [[Sketches of an Elephant]].

[[!redirects protocategories]]
[[!redirects protomorphism]]
[[!redirects protomorphisms]]
