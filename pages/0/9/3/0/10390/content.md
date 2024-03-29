
#Contents#
* toc
{:toc}

This entry is meant as a complement to [[subobject]].  In particular, the initial author knows that it is there, and that it really doesn't mean what he intends by "concrete subobject".

## Idea

In a [[concrete category]] $|-| : \mathcal{C} \to Set $, for an object $X$, when an injection $i : A \to | X | $ naturally induces (this is deliberately vague)

 * an object $ A^\vee $ with $ A = | A ^ \vee | $
 * a monomorphism $ i^\vee : A^\vee \to X $ with $ | i^\vee | = i $

then we say $A^\vee$ is a (concrete) subobject of $X$.

Compare with [[Grothendieck fibration]]

## Examples

### Algebra

 * In the category $Gp$ of groups, a concrete subgroup is exactly a monomorphism in $Gp$, which is exactly a map in $Gp$ whose underlying function is an injection; a map of sets $f: A \to |G|$ underlies a subgroup inclusion $ ? \to G $ iff there is *exactly one* group structure on $A$ such that $f$ underlies a homomorphism.

### Topology

 * For every topological space $X$ and every set $A$ and every map $f : A \to |X|$, there is a *terminal* (coarsest) topology on $A$ with a continuous map to $|X|$ over the function $f$; a *subspace* ("embedded" subspace) is exactly an injection of underlying sets where the domain is given this terminal compatible topology.
 * A sub-$\beta$-module is a *closed* subset; that is, an embedding of a compact space.

### Geometry

 * An injection of a topological manifold to a smooth manifold may be a topological embedding, but there may be many (or no) compatible smooth structures on the domain; a submanifold is a *smooth* embedding *with injective differential*, which is exactly an embedding of a topological manifold such that smooth functions on the codomain restrict to give a smooth atlas on the domain.