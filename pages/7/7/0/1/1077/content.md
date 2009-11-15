# Idea #

A _biproduct_ in a [[category]] $C$ is an operation that is both a [[product]] and a [[coproduct]].  Finite biproducts are best known from [[additive category|additive categories]] and their generalisations.

Morphisms between finite biproducts are encoded in a [[matrix calculus]].

# Definition #

Let $C$ be a [[category]] with [[zero morphisms]]; that is, $C$ is [[enriched category|enriched]] over [[pointed sets]] (for example, $C$ might have a [[zero object]]).  For $c_1, c_2$ two objects in $C$, suppose a [[product]] $c_1 \times c_2$ and a [[coproduct]] $c_1 \sqcup c_2$ both exist.  Then consider the canonical morphism
$$
  r : c_1 \sqcup c_2 \to c_1 \times c_2
$$
defined by
$$
  \left(
    c_i \to c_1 \sqcup c_2 \stackrel{r}{\to} c_1 \times c_2 \to c_j
  \right)
  =
  \left\{
    \array{
      Id_{c_i} & if i = j
      \\
      0_{i,j} & if i \neq j
    }
  \right.
  \,
$$
where $0_{i,j}$ is the zero morphism from $c_i$ to $c_j$.

If this morphism $r$ is an [[isomorphism]], then the isomorphic objects $c_1 \times c_2$ and $c_1 \sqcup c_2$ are called [[generalized the|the]] __biproduct__ of $c_1$ and $c_2$.  This object is often denoted $c_1 \oplus c_2$, alluding to the [[direct sum]] (which is often an example).

The above definition has a straightforward generalization to biproducts of any number of objects (although this requires extra structure on the category in [[constructive mathematics]] if the set indexing these objects might not have [[decidable equality]]).  A [[zero object]] is the biproduct of no objects.

+--{: .query}
_Mike_: Can anyone give a definition of a biproduct that doesn't require the category to be presupposed to have a zero object, but which specializes to a zero object in the 0-ary case?

[[Toby Bartels]]:  Actually, our current definition does this; I just wrote it badly.  Of course, now the category starts with an enriched structure ... but at least it is a weaker requirement.

[[Mike Shulman|Mike]]: The reason I ask is that I'm trying to work out an indexed version of biproducts.  In a fibration or indexed category, coproducts are left adjoint $f_!$ to reindexing $f^*$ and products are right adjoint $f_*$, so having $f$-indexed biproducts should mean that some canonical map $f_!\to f_*$ is an isomorphism.  But I'm not having much luck constructing such a canonical map.  Perhaps this is related to the need for decidable equality?

_Toby_:  If it helps, here is a bit more on that subject, which I wrote at [[direct sum]]:
>An arbitrary index set will still work if $C$ is enriched over the category of sets and [[partial functions]]; this may be embedded as a [[full subcategory]] of the category of pointed sets, and the embedding is an [[equivalence of categories]] if and only if the law of [[excluded middle]] holds.  But the usual examples of $C$ are not (constructively) so enriched.

[[Mike Shulman|Mike]]: Was that what you had in mind for the "extra structure" above?  It occurred to me that it could also mean the existence of "subzero objects," i.e. $\coprod_A X \to \prod_A X$ is an isomorphism whenever $A$ is a subsingleton---which is also, I think, not constructively true in the usual examples.

_Toby_:  Yes, that\'s what I had in mind.  (Although you could also do a more local version, letting the requirement that the index set be discrete and the requirement the hom-sets be enriched over $Set_part$ meet halfway, if you see what I mean.)
=--

# Biproducts imply enrichment #

A category with all finite biproducts is automatically [[enriched category|enriched]] over the [[monoidal category]] of abelian [[monoids]] with the usual [[tensor product]], as follows.

Given two morphisms $f, g: a \to b$ in $C$, let their sum $f + g: a \to b$ be
$$ a \to a \times a \cong a \oplus a \overset{f \oplus g}{\to} b \oplus b \cong b \sqcup b \to b .$$
One proves that $+$ is associative and commutative. Of course, the zero morphism $0: a \to b$ is the usual [[zero morphism]] given by the zero object:
$$ a \to 1 \cong 0 \to b .$$
One proves that $0$ is the neutral element for $+$ and that this matches the $0$ morphism that we began with in the definition.

If additionally every morphism $f: a \to b$ has an inverse $-f: a \to b$, then $C$ is enriched over the category $Ab$ of abelian [[groups]] and is therefore (precisely) an _[[additive category]]_.

If, on the other hand, the addition of morphisms is idempotent ($f+f=f$), then $C$ is enriched over the category $SLat$ of [[semilattices]] (and is therefore a kind of [[2-poset]]).

# Biproducts as enriched Cauchy colimits #

Conversely, if $C$ is already known to be enriched over abelian monoids, then a binary biproduct may be defined purely diagrammatically as an object $c_1\oplus c_2$ together with injections $n_i:c_i\to c_1\oplus c_2$ and projections $p_i:c_1\oplus c_2 \to c_i$ such that $p_j n_i = \delta_{i j}$ (the [[Kronecker delta]]) and $n_1 p_1 + n_2 p_2 = 1_{c_1\oplus c_2}$.  It is easy to check that makes $c_1\oplus c_2$ a biproduct, and that any binary biproduct must be of this form.  Similarly, an object $z$ of such a category is a zero object precisely when $1_z= 0_z$, its identity is equal to the zero morphism. It follows that functors enriched over abelian monoids must automatically preserve finite biproducts, so that finite biproducts are a type of [[Cauchy colimit]].  Moreover, any product _or_ coproduct in a category enriched over abelian monoids is actually a biproduct.

For categories enriched over [[suplattices]], this extends to all small biproducts, with the condition $n_1 p_1 + n_2 p_2 = 1_{c_1\oplus c_2}$ replaced by $\bigvee_{i} n_i p_i = 1_{\bigoplus_i c_i}$.  In particular, the category of suplattices has all small biproducts.

[[!redirects biproducts]]