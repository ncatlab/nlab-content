# Locally cartesian closed enriched categories

* table of contents
{: toc}

## Definition

Let $V$ be a [[semicartesian monoidal category]] and $C$ a $V$-[[enriched category]] with [[pullbacks]] in the enriched sense.  Then for any morphism $f:x\to y$ in (the [[underlying ordinary category]] of) $C$, there is a pullback $V$-functor $f^*:C/y \to C/x$ between the [[enriched slice categories]], and each enriched slice category $C/x$ has $V$-enriched [[products]].  We say $C$ is **$V$-locally-cartesian-closed** if the following equivalent conditions hold:

* Each $V$-functor $f^*$ has a right $V$-adjoint $f_*$.
* Each $V$-category $C/x$ is $V$-[[cartesian closed enriched category|cartesian closed]].


## Relation to ordinary local cartesian closure

If $C$ is $V$-locally-cartesian-closed, then its [[underlying ordinary category]] $C_0$ is [[locally cartesian closed category|locally cartesian closed]] in the usual sense, since $V$-enriched right adjoints have underlying ordinary right adjoints.

The converse is true in some cases, such as the following:

* When $V=Set$, trivially.

* More generally, whenever the underlying-set functor $V(I,-) : V\to Set$ is [[conservative functor|conservative]].

* When $V$ is locally cartesian closed and cartesian monoidal and $C=V$.

However, the converse is false in general.  Counterexamples can be found in [[locally cartesian closed enriched category#MO|this mathoverflow discussion]] (the discussion is only about cartesian closed enriched categories, but the counterexamples given are in fact locally cartesian closed, being indeed [[presheaf categories]]).

## Examples

* Some kinds of [[type-theoretic model categories]] are required to be simplicially locally cartesian closed.

## Related entries

* [[locally cartesian closed category]]

* [[cartesian closed enriched category]]

* [[monoidal enriched category]]

* [[locally cartesian closed model category]]

## References

* {#MO} [Enriched cartesian closed categories on MO](https://mathoverflow.net/q/322085)

* {#MO2} [Simplicial cartesian closed categories on MO](https://mathoverflow.net/q/322917)


[[!redirects locally cartesian closed enriched category]]
[[!redirects locally cartesian closed enriched categories]]
[[!redirects enriched locally cartesian closed category]]
[[!redirects enriched locally cartesian closed categories]]
[[!redirects simplicially locally cartesian closed category]]
[[!redirects simplicially locally cartesian closed categories]]
