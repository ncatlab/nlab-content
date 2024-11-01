* table of contents
{: toc}

## Idea

For a [[2-monad]] $T$, the 2-category $T Alg$ of $T$-algebras and pseudo $T$-morphisms has weak [[2-limits]] (bilimits), and more precisely [[pie-limits]].  The 2-categories $T Alg_l$ and $T Alg_c$ of [[lax morphism|lax and colax]] $T$-morphisms do not have all 2-limits (even weak ones), but they do have some, particularly when some of the morphisms involved in the diagram are strict or pseudo; see [[rigged limit]] for a characterization of these.  There is no 2-category containing both lax and colax morphisms, but nevertheless some limits of diagrams involving lax and colax morphisms can be given a $T$-algebra structure.  Of these one of the most commonly encountered is a [[comma object]] $(f/g)$ where $f$ is colax and $g$ is lax.  It is unclear exactly how to state a universal property for this comma object, but it is probably related to the [[double category of algebras]].

## Definition

Let $T$ be a (strict, for simplicity) [[2-monad]] on a ([[strict 2-category|strict]], for simplicity) [[2-category]] $K$, and let $f:A\to C$ be a colax $T$-morphism and $g:B\to C$ a [[lax morphism|lax]] $T$-morphism.  Suppose that the ([[strict 2-limit|strict]], for simplicity) [[comma object]] $(f/g)$ exists in $K$; thus it is equipped with projections $p:(f/g)\to A$ and $q:(f/g)\to B$ (which are, so far, only morphisms in $K$) and a 2-cell

$$\array{ (f/g) & \xrightarrow{p} & A\\
^q\downarrow & \swArrow_\alpha & \downarrow^f \\
B & \xrightarrow{g} & C
}$$

that is universal among such 2-cells.  Now consider the following [[pasting diagram|pasting composite]]:

$$\array{
T(f/g) & \to & T A \\
\downarrow & \swArrow_{T\alpha} & \downarrow^{T f} & \searrow \\
T B & \to & T C & \swArrow_{\bar{f}} & A \\
& \searrow & \swArrow_{\bar{g}} & \searrow &\downarrow^f \\
&& B & \xrightarrow{g} & C
}$$

Here $\bar{f}$ is the colax $T$-morphism constraint of $f$, while $\bar{g}$ is the lax $T$-morphism constraint of $g$.  Notice that these go in exactly the right directions for the above pasting to be well-defined.  Now by the universal property of $(f/g)$, there is a unique morphism $T(f/g) \to (f/g)$ such that the above pasting composite is equal to the following one:

$$ \array{
T(f/g) & \to & T A \\
\downarrow & \searrow &  & \searrow \\
T B & & (f/g) & \to & A \\
& \searrow & \downarrow & \swArrow_\alpha &\downarrow^f \\
&& B & \xrightarrow{g} & C
} $$

where the empty quadrilaterals commute.  A similar argument shows that this map $T(f/g) \to (f/g)$ is the action map of a $T$-algebra structure on $(f/g)$, such that the projections $p:(f/g)\to A$ and $q:(f/g)\to B$ are strict $T$-morphisms and $\alpha$ is a 2-cell in the [[double category of algebras]] $T \mathbf{Alg}$.  (In fact, the latter assertion is precisely the equality of the above two pasting diagrams.)

The strictness of the projections $p,q$ is familiar from the behavior of [[rigged limits]] in $T Alg_l$ and $T Alg_c$.  However, it is unclear exactly what universal property this $T$-algebra $(f/g)$ has, although it seems likely to involve the double category $T \mathbf{Alg}$ somehow.

## Examples

* Some [[comma double categories]] are colax/lax comma objects in the double category of double categories (and lax and colax double functors).

[[!redirects oplax/lax comma object]]
[[!redirects oplax/lax comma objects]]
[[!redirects colax/lax comma object]]
[[!redirects colax/lax comma objects]]
[[!redirects lax/oplax comma object]]
[[!redirects lax/oplax comma objects]]
[[!redirects lax/colax comma object]]
[[!redirects lax/colax comma objects]]
