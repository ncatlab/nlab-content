# Cartesian closed enriched categories

* table of contents
{: toc}

## Definition

Let $V$ be a [[monoidal category]] with [[products]] and $C$ a $V$-[[enriched category]] with [[products]], in the enriched sense that we have a $V$-natural isomorphisms of [[hom-objects]] in $V$:

$$ C(Z, X\times Y) \cong C(Z,X) \times C(Z,Y). $$

We say $C$ is **$V$-cartesian-closed** if each $V$-functor $(X\times -) : C\to C$ has a $V$-enriched [[right adjoint]].


## Relation to ordinary cartesian closedness

If $C$ is $V$-cartesian-closed, then its [[underlying ordinary category]] $C_0$ is [[cartesian closed category|cartesian closed]] in the usual sense, since $V$-enriched right adjoints have underlying ordinary right adjoints.

The converse is true in some cases, such as the following:

* When $V=Set$, trivially.

* More generally, whenever the underlying-set functor $V(I,-) : V\to Set$ is [[conservative functor|conservative]], since the morphism of hom-objects $C(X,Y^Z) \to C(X\times Y,Z)$ induced by the evaluation morphism $Y^Z\times Y \to Z$ has invertible image in $Set$, hence is itself invertible if $V(I,-)$ is conservative.

* When $V$ is cartesian monoidal and $C=V$: a cartesian closed category is automatically enriched-cartesian-closed over itself.  In other words, the defining isomorphisms $V_0(X\times Y,Z) \cong V_0(X, Z^Y)$ induce, by the [[Yoneda lemma]], isomorphisms of [[exponential objects]] $Z^{X\times Y} \cong (Z^Y)^X$.

However, the converse is false in general.  Counterexamples can be found in [[cartesian closed enriched category#MO|this mathoverflow discussion]].


## References

* {#MO} [Enriched cartesian closed categories on MO](https://mathoverflow.net/q/322085)
* {#MO2} [Simplicial cartesian closed categories on MO](https://mathoverflow.net/q/322917)


[[!redirects cartesian closed enriched category]]
[[!redirects cartesian closed enriched categories]]
[[!redirects enriched cartesian closed category]]
[[!redirects enriched cartesian closed categories]]
[[!redirects simplicially cartesian closed category]]
[[!redirects simplicially cartesian closed categories]]
