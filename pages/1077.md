# Idea #

A _biproduct_ in a [[category]] $C$ is an operation that is both a [[product]] and a [[coproduct]].  Finite biproducts are best known from [[additive category|additive categories]] and their generalisations.

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

If this morphism $r$ is an [[isomorphism]], then the isomorphic objects $c_1 \times c_2$ and $c_1 \sqcup c_2$ are called [[generalized the|the]] __biproduct__ of $c_1$ and $c_2$.  This object often denoted $c_1 \oplus c_2$, after the [[direct sum]] (which is often an example), to be more neutral.

The definition generalises to a biproduct of any number of objects.  Then the [[zero object]] is itself the biproduct of no objects.

# Enriched structure #

A category with all finite biproducts is automatically [[enriched category|enriched]] over the [[monoidal category]] of abelian [[monoid]]s with the usual [[tensor product]], as follows.

Given two morphisms $f, g: a \to b$ in $C$, let their sum $f + g: a \to b$ be
$$ a \to a \times a \cong a \oplus a \to^{f \oplus g} b \oplus b \cong b \sqcup b \to b .$$
Then you can prove that $+$ is associative and commutative.

Of course, the zero morphism $0: a \to b$ is the usual [[zero morphism]] given by the zero object:
$$ a \to 1 \cong 0 \to b .$$
Then you can prove that $0$ is the neutral element for $+$.

If additionally every morphism $f: a \to b$ has an inverse $-f: a \to b$, then $C$ is enriched over the category $Ab$ of abelian [[group]]s and therefore an _[[additive category]]_.