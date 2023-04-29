
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of *essential fiber* of a [[functor]] is an enhancement of the naive notion of *[[fiber]]* which, for [[functors]], would violate the [[principle of equivalence]].  It is a [[category theory|category-theoretic]] version of a [[homotopy fiber]].

The essential fiber of a functor $p:E\to B$ over an object $b \in B$ can be thought of as the category of ways $b$ can arise from applying $p$ to some object in $E$.

## Definition

Let $p:E\to B$ be a functor and $b\in B$ an [[object]].  The **essential fiber** of $p$ over $b$ is the following category:

* its objects are pairs $(e,\phi)$ where $e\in E$ is an object and $\phi\colon p(e)\cong b$ is an [[isomorphism]].
* its morphisms $(e,\phi)\to (e',\phi')$ are morphisms $f\colon e\to e'$ in $E$ such that $\phi' \circ p(f) = \phi$.

The essential fiber can be identified with the [[pseudopullback]] or "isocomma object" of $p$ along the functor $b\colon 1\to B$ from the [[terminal category]] which picks out the object $b$:

$$
  \array{
    E \times_B 1 &\to& E
    \\
    \downarrow && \downarrow_p
    \\
    1 &\stackrel{b}{\to}& B
  }
$$

It can also be identified with a [[homotopy fiber]] in the [[canonical model structure]] on [[Cat]].  When [[groupoids]] are identified with [[homotopy 1-types]], the essential fiber actually coincides with the classical homotopy fiber (up to equivalence).

## Relationship to fibrations

If $p$ is an [[isofibration]], then any of its essential fibers is equivalent to the corresponding strict fiber.  This includes the case when $p$ is a [[Grothendieck fibration]].

On the other hand, when $p$ is a [[Street fibration]] (the version of [[Grothendieck fibration]] which respects the [[principle of equivalence]]), then essential fibers do *not* coincide with strict fibers, and essential fibers are the more useful notion.  In particular, the correspondence between fibrations and [[pseudofunctors]] only goes through for Street fibrations if one defines the pseudofunctor using essential fibers.

## Properties

Some properties of a functor are reflected in properties of its essential fibers.   A good intuition is that the more a functor resembles an injective function, the simpler its essential fibers are.

+-- {: .num_prop #essential_fibers_conservative}
###### Proposition

A functor $f: A \to B$ is [[conservative functor|conservative]] if and only if all its essential fibers are groupoids.
=--

+-- {: .num_prop #essential_fibers_faithful}
###### Proposition

If the functor $p: E \to B$ is [[faithful]], all its essential fibers are preorders.  (The converse is not true.)
=--

and thus:

+-- {: .num_prop #essential_fibers_faithful_and_conservative_1}
###### Proposition

If the functor $p: E \to B$ is faithful and conservative all its essential fibers are equivalent to discrete categories.  
=--

For example, there is typically a nontrivial preorder of ways that a set can arise as the underlying set of a topological space, because the forgetful functor from $\mathrm{Top}$ to $\mathrm{Set}$ is faithful but not conservative.  On the other hand, there is a mere set (or discrete category) of ways that a set can arise as the underlying set of a group, because the forgetful functor from $\mathrm{Grp}$ to $\mathrm{Set}$, being [[monadic]], is both faithful and conservative.

Note that the automorphism group of $b \in B$ always acts on the essential fiber of $b$.  For example on objects, $\alpha \in \mathrm{Aut}_B(b)$ acts to send $(e,\phi)$ to $(e, \alpha \circ \phi)$.  When the essential fiber is essentially a set as in the above proposition, this lets us describe the essential fiber as a union of orbits:

+-- {: .num_prop #essential_fibers_faithful_and_conservative}
###### Proposition

If the functor $p: E \to B$ is faithful and conservative, Tthe essential fiber over $b \in B$ is equivalent to the discrete category on the set
$$ \coprod_e \mathrm{Aut}_B (b) / \mathrm{Aut}_E (e) $$
where $e \in E$ ranges over one representative of each isomorphism class in $E$ whose image is the isomorphism class of $b$.
=--

When $p: E \to B$ is not only faithful and conservative but also injective on isomorphism classes, there is at most one isomorphism class in $E$ whose image is the isomorphism class of $b$.  Thus the coproduct in the preceding proposition has at most one summand, and the automorphism group of $b$ acts transitively on the relevant set:

+-- {: .num_prop #essential_fibers_faithful_conservative_injective}
###### Proposition

If the functor $p: E \to B$ is [[faithful]], [[conservative functor|conservative]] and it is injective on isomorphism classes, then for any $e \in E$, the essential fiber over $b = f(e)$ is equivalent to the discrete category on the set
$$    \mathrm{Aut}_B (b) / \mathrm{Aut}_E (e). $$
Thus $\mathrm{Aut}_B (b)$ acts transitively on this set.
=--

For example, the forgetful functor from complex vector spaces to real vector spaces is faithful, conservative and injective on isomorphism classes.  The essential fiber over a real vector space is the set of [[complex structures]] on this vector space, and if this vector space is $\mathbb{R}^{2n}$, the proposition implies this set of complex structures is isomorphic to
$$     \mathrm{GL}(2n,\mathbb{R})/\mathrm{GL}(n,\mathbb{C}) .$$

## References

The results on essential fibers were proved in this discussion:

* [Homotopy fibers](https://categorytheory.zulipchat.com/#narrow/stream/266967-general.3A-mathematics/topic/homotopy.20fibers/near/353365094), Category Theory Community Server.

[[!redirects essential fibre]]
[[!redirects essential fibers]]
[[!redirects essential fibres]]
