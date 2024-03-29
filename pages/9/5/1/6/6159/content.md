{:classqn: style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

The idea of an **orthogonal structure** is a generalisation to arbitrary [[vector bundles]] of the distinguishing ingredient of a [[Riemannian manifold]]: the [[Riemannian metric]].  In short, an orthogonal structure on a vector bundle is a smooth choice of [[inner product]] on the fibres.

In finite dimensions, that is pretty much all that can be said about the basic definition.  For [[infinite dimensional manifolds]], however, there is considerably more to be said because the _linear_ notion of an inner product is much, much richer.

## Definition ##

Although the definition makes sense in the topological category, we shall confine ourselves to the smooth category for the time being.

+-- {: .num_defn #orthstr}
###### Definition
Let $\pi \colon E \to M$ be a smooth [[vector bundle]] over a [[smooth manifold]].  An **orthogonal structure** on $E$ is a smooth choice of [[inner product]] on $E$.  That is to say, an orthogonal structure $g$ on $E$ is a section of $E^* \otimes E^*$ which restricts to an inner product on each fibre.
=--

As for [[Riemannian metrics]], a standard [[partition of unity]] argument yields the following existence result.

+-- {: .num_proposition #exist}
###### Proposition
Let $\pi \colon E \to M$ be a smooth vector bundle with finite dimensional fibres which admits a trivialisation over a numerable cover.  Then $E$ admits an orthogonal structure.
=--

Moreover, in finite dimensions all orthogonal structures are equivalent in that there is a bundle isomorphism between any two.

## Properties

### Reduction of structure Groups

#### In finite dimensions

In finite dimensions, to put an orthogonal structure on a vector bundle is to give a [[reduction of structure groups|reduction of its structure group]] from the [[general linear group]] to the corresponding [[orthogonal group|orthogonal]] subgroup along the defining inclusion $O(n) \hookrightarrow GL(n)$.  Such a reduction is also known as a choice of _[[vielbein]]_.

Thus the existence in general is equivalent to the fact that the inclusions $O(n) \to GL(n)$ and $U(n) \to GL(n)$ are [[homotopy equivalences]], as for the inclusion of any [[maximal compact subgroup]].  A similar statement can be made about the fact that any two orthogonal structures are equivalent.

#### In infinite Dimensions

The situation in infinite dimensions is more complicated due to the fact that there are more situations to consider.  In finite dimensions, any two orthogonal structures are equivalent, which stems from the fact that any two inner products define equivalent norms in finite dimensions.  In infinite dimensions, it is no longer true even that all [[locally convex topological vector spaces]] admit inner products, and when one does then it is highly unlikely that it will admit only one (up to equivalence).

What gives Riemannian geometry much of its power is the induced isomorphism between the [[tangent bundle|tangent]] and [[cotangent bundles]].  Thus a natural first question to ask of an orthogonal structure in infinite dimensions is whether or not this is still true.

+-- {: classqn}
**Question:** Does the orthogonal structure induce an isomorphism $E \cong E^*$?

**Yes:** It is _strong_.

**No:** It is _weak_.
=--

The condition that an orthogonal structure be strong is very restrictive.  The bundle must be modelled on Hilbert spaces (with the correct topology) and the inner product must be the right choice.  Many orthogonal structures that occur "in the wild" do not fit those two conditions and are thus relegated to the "weak" bin.  However, all is not lost and it is still possible to work with such orthogonal structures.  Although a weak orthogonal structure means that the bundle is not modelled on Hilbert spaces, it does mean that there are Hilbert spaces nearby and it is possible to further refine the notion of a "weak orthogonal structure" by asking how "nice" are those associated Hilbert spaces.

The idea is quite simple.  To put an orthogonal structure on a vector _space_, say $V$, is to give an injection $V \to H$ in to some Hilbert space.  We can assume that $V$ has dense image, but this is not strictly necessary.  Thus an inner product is a diagram:
$$
\iota \colon V \to H
$$
and the classification of weak orthogonal structures is essentially a study of how well that diagram extends over the base space.

## Related concepts

* [[orthogonality]], [[orthogonal basis]], [[normal vector]]

* [[pseudo-orthogonal structure]]

* A choice of orthogonal structure on a [[manifold]] is also equivalently called a choice of _[[vielbein]]_. See there for more details.

* [integrability of G-structures -- Examples -- Orthogonal structure](integrability+of+G-structures#ExamplesOrthogonalStructure)

## References

* _How to Construct a Dirac Operator in Infinite Dimensions_ [[Andrew Stacey]] [0809.3104](http://arxiv.org/abs/0809.3104)

* _The Co-Riemannian Structure of Smooth Loop Spaces_ [[Andrew Stacey]] [0809.3108](http://arxiv.org/abs/0809.3108)

[[!redirects orthogonal structures]]