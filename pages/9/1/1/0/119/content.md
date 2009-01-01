A _preorder_ is a [[category]] such that for any pair of objects $x, y$, there is at most one morphism from $x$ to $y$. In other words, it's a category [[enriched category theory|enriched]] over the category of truth values (aka ($-1$)-[[(-1)-category|categories]]).

Any preorder is [[equivalence|equivalent]] to a [[poset]]. This is a special case of the theorem that every category has a [[skeleton]], but this case does _not_ require the [[axiom of choice]].

+--{.query}
It's not clear to me how one avoids the axiom of choice. For example, any equivalence relation E on a set X defines a preorder whose posetal reflection is the quotient X --> X/E, and it seems to me you need to split that quotient to get the equivalence between the preorder and the poset.
=--