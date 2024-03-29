
# Biased definitions
* table of contents
{: toc}

## Idea

Often in mathematics, when requiring some structure/operation/property/... to exist at every [[finite set|finite]] [[arity]], it suffices to require only the binary ($2$-ary) and nullary ($0$-ary) forms, from which the others follow.  A definition in which only these are required is called __biased__.

For example, in defining a [[category]], one could use an "unbiased" definition in which [[composites]] of all [[list|finite sequences]] of [[morphisms]] are directly postulated, with corresponding [[associativity]] laws, but it suffices to require only binary composites and nullary composites (i.e., [[identity morphisms]]) and some particular corresponding associativity laws.

As a special case of this, we have perhaps the prototypical example of a binary/nullary pair sufficing to generate all finite instances of some structure: the [[natural numbers]] themselves (the arities of the operations that we are considering) are the [[free monoid]] on one generator, and thus are freely associatively produced from that one generator (aka, $1$) using only binary and nullary addition.

Sometimes it is too easy to write a definition that involves only the binary condition; writing an unbiased definition can make it easier to notice the corresponding nullary condition.  Compare when things are [[too simple to be simple]].


## When a nullary operation does not exist

Sometimes a nullary operation does not exist but one still wants to decompose a n-ary operation into binary operations. For example, consider [[real number|the reals]], $\mathbb{R}$, as an [[lattice|unbounded lattice]] ([[top|top]], $\top$, and [[bottom|bottom]], $\bot$, do not exist) where

 $\wedge =$ [[product]] $=$ [[meet]] $= infimum = min$

and

 $\vee =$ [[coproduct]] $=$ [[join]] $= supremum = max$.

Here $\bigwedge(\{\})$ does not exist while 

 $\bigwedge(\{a\}) = a$

 $\bigwedge(\{a,b\}) = a \wedge b$

 $\bigwedge(\{a,b,c\}) = a \wedge (b \wedge c) = (a \wedge b) \wedge c = a \wedge b \wedge c$.

One approach is to compute in the [[extended real number|extended reals]], $\mathbb{R}_{\pm \infty}$ ($\mathbb{R}$ enlarged with $+\infty$ and $-\infty$.) Here 

 $\top = +\infty =$ [[terminal object]]

and

 $\bot = -\infty =$ [[initial object]].

In $\mathbb{R}_{\pm \infty}$ we have the nullary $\wedge() = +\infty$ which gives:

 $\bigwedge(\{\}) = +\infty$

 $\bigwedge(\{a\}) = \bigwedge(\{a, +\infty\}) = a$.

Another approach is to define a special scheme for composition for when a nullary operator does not exist that instead uses a unary operator that is an identity map (or factored through one).

This approach generalizes to any [[semigroup]] or to any category with binary ([[coproduct|co]]) [[products]].  A yet more general context (possibly not fully worked out) would be a [[binary operation]] in any [[associative operad]].


[[!redirects binary/nullary pair]]
[[!redirects binary/nullary pairs]]
[[!redirects binary-nullary pair]]
[[!redirects binary-nullary pairs]]
[[!redirects binary nullary pair]]
[[!redirects binary nullary pairs]]

[[!redirects bias]]
[[!redirects biased]]
[[!redirects unbiased]]
[[!redirects biased definition]]
[[!redirects biased definitions]]
[[!redirects unbiased definition]]
[[!redirects unbiased definitions]]
