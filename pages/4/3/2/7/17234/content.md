[[!redirects prestable ∞-category]]
# Prestable ∞-category
* table of contents
{: toc}

## Idea

A _prestable ∞-category_ axiomatizes the properties
of the connective part of a [[t-structure]] on a [[stable ∞-category]].

## Definition

A _prestable ∞-category_ is a [[pointed]] [[finitely cocomplete]] [[∞-category]]&#160;$C$ with a fully faithful [[suspension functor]] such that the [[base change]] of any morphism $Y\to\Sigma Z$ along a map $0\to\Sigma Z$ exists and the resulting pullback square is also a pushout square.

The fully faithfulness condition can be rephrased
by saying that the functor $C\to SW(C)$ is fully faithful,
and then the base change condition can be reformulated
by saying that the image of $C\to SW(C)$ is closed under extensions.
Here $SW(C)$ is the [[Spanier-Whitehead category]] of&#160;$C$.

## Properties

An ∞-category is prestable if and only if it is a full subcategory of a stable ∞-category closed under finite colimits and extensions.

## Examples

Any stable ∞-category is prestable.

If $C$ is a stable ∞-category with a [[t-structure]] $(C_{\ge0},C_{\le0})$, then $C_{\ge0}$ is prestable.
Any finitely complete prestable ∞-category arises in such a fashion, and there are two canonical choices for&#160;$C$:
the [[Spanier-Whitehead category]] and the category of [[spectrum objects]].
In fact, any other choice can be squeezed in between these two.

## Grothendieck prestable ∞-categories and a Gabriel-Popescu theorem

A prestable ∞-category is _Grothendieck_ if it is presentable
and [[filtered colimits]] are [[left exact]].

There is a [[Gabriel-Popescu theorem]] for prestable ∞-categories:
the class of Grothendieck prestable ∞-categories
coincides with the class of accessible left exact localizations
of [[connective]] modules over a connective [[E1-ring|E_1-ring]].

## References

Lurie, [[Spectral Algebraic Geometry]], &#167;A.3.

[[!redirects prestable ∞-category]]
[[!redirects prestable ∞-categories]]
[[!redirects prestable (∞,1)-categories]]