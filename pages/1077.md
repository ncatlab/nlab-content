# Idea #

A _biproduct_ in a [[category]] $C$ is an operation that is both a [[product]] and a [[coproduct]].  Finite biproducts are best known from [[additive category|additive categories]] and their generalisations.

Morphisms between finite biproducts are encoded in a [[matrix calculus]].

# Definition #

For $c_1, c_2$ two objects in a category $C$ with a [[zero object]], suppose a [[product]] $c_1 \times c_2$ and a [[coproduct]] $c_1 \sqcup c_2$ both exist.  Then consider the canonical morphism
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
      0 & if i \neq j
    }
  \right.
  \,
$$
where $0$ indicates the [[zero morphism]].

If this morphism $r$ is an [[isomorphism]], then the isomorphic objects $c_1 \times c_2$ and $c_1 \sqcup c_2$ are called [[generalized the|the]] __biproduct__ of $c_1$ and $c_2$.  This object is often denoted $c_1 \oplus c_2$, alluding to the [[direct sum]] (which is often an example).

The above definition has a straightforward generalization to biproducts of any number of objects (although this requires extra structure on the category in [[constructive mathematics]] if the set of these objects need not have [[decidable equality]]).  The [[zero object]] is itself the biproduct of no objects.

# Biproducts imply enrichment #

A category with all finite biproducts is automatically [[enriched category|enriched]] over the [[monoidal category]] of abelian [[monoid]]s with the usual [[tensor product]], as follows.

Given two morphisms $f, g: a \to b$ in $C$, let their sum $f + g: a \to b$ be
$$ a \to a \times a \cong a \oplus a \to^{f \oplus g} b \oplus b \cong b \sqcup b \to b .$$
One proves that $+$ is associative and commutative. Of course, the zero morphism $0: a \to b$ is the usual [[zero morphism]] given by the zero object:
$$ a \to 1 \cong 0 \to b .$$
One proves that $0$ is the neutral element for $+$.

If additionally every morphism $f: a \to b$ has an inverse $-f: a \to b$, then $C$ is enriched over the category $Ab$ of abelian [[group]]s and is therefore (precisely) an _[[additive category]]_.

If, on the other hand, the addition of morphisms is idempotent ($f+f=f$), then $C$ is enriched over the category $SLat$ of [[semilattice]]s (and is therefore a kind of [[2-poset]]).

# Biproducts as enriched Cauchy colimits #

Conversely, if $C$ is already known to be enriched over abelian monoids, then a binary biproduct may be defined purely diagrammatically as an object $c_1\oplus c_2$ together with injections $n_i:c_i\to c_1\oplus c_2$ and projections $p_i:c_1\oplus c_2 \to c_i$ such that $p_j n_i = \delta_{i j}$ (the [[Kronecker delta]]) and $n_1 p_1 + n_2 p_2 = 1_{c_1\oplus c_2}$.  It is easy to check that makes $c_1\oplus c_2$ a biproduct, and that any binary biproduct must be of this form.  Similarly, an object $z$ of such a category is a zero object precisely when $1_z= 0_z$, its identity is equal to the zero morphism. It follows that functors enriched over abelian monoids must automatically preserve finite biproducts, so that finite biproducts are a type of [[Cauchy colimit]].  Moreover, any product _or_ coproduct in a category enriched over abelian monoids is actually a biproduct.

For categories enriched over [[suplattice]]s, this extends to all small biproducts, with the condition $n_1 p_1 + n_2 p_2 = 1_{c_1\oplus c_2}$ replaced by $\bigvee_{i} n_i p_i = 1_{\bigoplus_i c_i}$.  In particular, the category of suplattices has all small biproducts.
