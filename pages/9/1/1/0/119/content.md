#Idea

A preorder is like a partially ordered set (or [[poset]] for short), but we drop the requirement that $x \le y$ and $y \le x$ implies $x = y$.  The reason is that if we think of a poset as a special sort of [[category]], it is [[evil]] to impose this equation between objects.  

#Definition

A **preorder** is a [[category]] such that for any pair of objects $x, y$, there is at most one morphism from $x$ to $y$. In other words, it's a category [[enriched category theory|enriched]] over the category of truth values (aka ($-1$)-[[(-1)-category|categories]]).

Any preorder is [[equivalence|equivalent]] to a [[poset]]. This is a special case of the theorem that every category has a [[skeleton]], but this case does _not_ require the [[axiom of choice]].

#Discussion

_[[Todd Trimble|Todd]] says:_ It's not clear to me how one avoids the axiom of choice. For example, any equivalence relation $E$ on a set $X$ defines a preorder whose posetal reflection is the quotient $X \to X/E$, and it seems to me you need to split that quotient to get the equivalence between the preorder and the poset.

_[[Toby Bartels|Toby]] says:_ In the absence of the axiom of choice, the correct definition of an equivalence of categories $C$ and $D$ is a span $C \leftarrow X \rightarrow D$ of full, faithful, essentially surjective functors. Or equivalently, a pair $C \leftrightarrow D$ of [[anafunctor]]s (with the usual natural transformations making them inverses).

_[[Todd Trimble|Todd]] says:_ Thanks, Toby. So if I understand you aright, the notion of equivalence you have in mind here is not the one used at the top of the entry [[equivalence]], but is more subtle. May I suggest amplifying a little on the above, to point readers to the intended definition, since this point could be confusing to those inexperienced in these matters? 