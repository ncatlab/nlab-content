
> This entry is about the notion in _[[order theory]]/[[logic]]_. For other notions of the same name, such as in [[bilinear form]]-theory, see at _[[lattice (disambiguation)]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

A **lattice** is a [[partial order|poset]] which admits all finite [[meets]] and finite [[joins]] (or all finite [[products]] and finite [[coproducts]], regarding a poset as a [[category]] (a [[(0,1)-category]])).

As [[(0,1)-limits]] are meets and [[(0,1)-colimits]] are joins, a lattice is a [[(0,1)-category]] that is [[finitely complete category|finitely complete]] and [[finitely cocomplete category|finitely cocomplete]]. 

A **lattice** can also be defined as an algebraic structure, with the binary operations $\wedge$ and $\vee$ and the constants $\top$ and $\bot$. (These correspond, respectively, to binary and nullary meets and joins in the poset-theoretic definition; accordingly, they are read 'meet', 'join', '[[top]]', and '[[bottom]]'.) Here are the axioms for these operations:

* $\wedge$ and $\vee$ are each [[idempotent]], [[commutative magma|commutative]], and [[associative magma|associative]];
* the _absorption laws_: $a \vee (a \wedge b) = a$, and $a \wedge (a \vee b) = a$;
* $\top$ and $\bot$ are the respective [[identity element|identities]] of $\wedge$ and $\vee$.

You can recover the original poset from either the meet or the join; $a \leq b$ iff $a \wedge b = a$, and $b \leq a$ iff $a \vee b = a$, and then prove that $a\wedge b$ is the greatest lower bound for $a$, $b$ and $a \vee b$ is the least upper bound for $a$, $b$. (Notice that the absorption laws guarantee that these two descriptions of $\leq$ agree.)  Indeed, we may say that a lattice is a _bisemilattice_ in that it has two semilattice structures that are compatible in that they define (but in dual ways) the same partial order.

Note that a poset with only finite meets _or_ finite joins is a (meet- or join-) [[semilattice]], while a lattice which has *all* joins and meets (not just finitary ones) is a [[complete lattice]].

## Bounded lattices and pseudolattices

Traditionally, a lattice need have only finite [[inhabited set|inhabited]] meets and joins; that is, it need not have a top or bottom element.  Algebraically, this means $\wedge$ and $\vee$ need not have identities.

Then one may call a lattice that *does* have a top and a bottom a __bounded lattice__; in general, a [[bounded poset]] is a poset that has top and bottom elements.

The other approach is to define a lattice, as above, to require a top and a bottom and then use the term __pseudolattice__ to allow for the possibility that it might not.

From an algebraic point of view, requiring top and bottom is quite natural, a special case of preferring [[monoids]] to more general [[semigroups]].  In any case, one can formally adjoin a top and a bottom if required.  On the other hand, many examples, especially from analysis, do not come with a top or a bottom, and adjoining them would break the other structure. For example, adjoining top ($\infty$) and bottom ($-\infty$) to the [[real line]] makes it no longer a [[field]] (addition is especially problematic); more generally, a [[Banach lattice]] need not (and, except in one degenerate case, cannot) have a top or a bottom. In fact, adjoining top and bottom to any [[total order|totally]] [[ordered ring]] makes it no longer a [[ring]]. 

## Lattice homomorphisms

A lattice homomorphism $f$ from a lattice $A$ to a lattice $B$ is a [[function]] from $A$ to $B$ (seen as sets) that preserves $\wedge$ and $\vee$ (and $\top$ and $\bot$, if these are required):
$$ f(x \wedge y) = f(x) \wedge f(y),\; f(\top) = \top,\; f(x \vee y) = f(x) \vee f(y),\; f(\bot) = \bot .$$
Note that such a homomorphism is necessarily a [[monotone function]], but the converse fails.

Thus, a lattice is a poset (or even a semilattice) with [[property-like structure]].

Lattices and lattice homomorphims form a [[concrete category]] [[Lat]].


## Related concepts

* [[sigma-complete lattice|$\sigma$-complete lattice]]

* [[complete lattice]]

* [[distributive lattice]]

* [[modular lattice]]

* [[orthomodular lattice]]

* [[geometric lattice]] 

* [[continuous lattice]]

* [[complemented lattice]]

* [[semilattice]]

* [[suplattice]]

* [[Hilbert lattice]]

* [[frame]]

* [[lattice-ordered abelian group]]

* [[lattice object]]

## References

* [[Peter Johnstone]], chapter 1 of _[[Stone Spaces]]_

* [[Jacob Lurie]], section A.1.1 of _[[Spectral Algebraic Geometry]]_


[[!redirects lattices]]
[[!redirects bisemilattice]]
[[!redirects bounded lattice]]
[[!redirects pseudolattice]]