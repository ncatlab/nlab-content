In [[logic]], the **context** of an assertion (or judgement) consists of all of the assumptions that are made when that assertion to claimed be valid (regardless of whether it is in fact valid).

Generally, contexts will be thought of as relative to some underlying logical theory.  This underlying theory will contain most of the assumptions of what constitutes validity; the context of an assertion in this theory will then include only those extra assumptions that may be used by that assertion.

For example, in the theory of a [[group]], it is understood that there is a group $G$, that $G$ has various elements, that two elements of $G$ may be equal, that the product of two elements of $G$ is an element of $G$, and that various axioms are satisfied (which we will not list here).  However, the assertion that $a$ and $b$ commute in $G$ still does not make sense without the additional context that $a$ and $b$ are elements of $G$.  Even in that context, this assertion, while at least meaningful, is not valid.  However, if we add to the context the assumption that $(a b)^2 = a^2 b^2$, then the assertion is valid.  Written symbolically,
$$ \vdash\; a b = b a $$
is meaningless;
$$ a: G,\; b: G \;\vdash\; a b = b a $$
is meaningful but invalid; and
\[\label{valid} a: G,\; b: G,\; (a b)^2 = a^2 b^2 \;\vdash\; a b = b a \]
is valid.

In a sufficiently rich logical language, contexts are unnecessary, which is why contexts are not usually explained in accounts of logic for ordinary reasoning (including in ordinary mathematics).  For example, the two meaningful assertions above may be rewritten thus:
$$ \vdash\; \forall (a: G),\; \forall (b: G),\; a b = b a$$
and
$$ \vdash\; \forall (a: G),\; \forall (b: G),\; (a b)^2 = a^2 b^2 \;\Rightarrow\; a b = b a$$
Here the context on the left side is the **empty context**, consisting of no assumptions whatsoever (beyond those underlying the base theory).

However, the previous versions of these assertions work in weaker logics.  In fact, these assertions make sense (and the valid one may be proved) in the [[internal logic]] of a group object in a [[cartesian monoidal category|cartesian]] [[multicategory]].  Accordingly, they can be interpreted (and the valid one is true) as statements about any group object in any cartesian multicategory, exactly as they do for groups (which are group objects in the cartesian multicategory [[Set]]).

Even if one is completely uninterested in [[internalization]] or weak logics, a basic familiarity with contexts may help drive home a point that is important throughout reasoning: **What you can state and prove depends on your assumptions.**

# The category of contexts

The morphisms between contexts are **substitutions**, or **interpretations**.  Such a morphism from the context $\Gamma$ to the context $\Delta$ consists of a way of fulfilling the assumptions required by $\Delta$ by appropriately interpreting those provided by $\Gamma$, generally by substituting terms available in $\Gamma$ for variables needed in $\Delta$ and proving whatever is necessary from the assumptions at hand.

For example, consider these contexts in the theory of a group $G$:
$$ \Gamma \;=\; a: G,\; b: G $$
$$ \Delta \;=\; a: G,\; b: G,\; (a b)^2 = a^2 b^2 $$
$$ E \;=\; a: G,\; b: G,\; a b = b a $$
$$ Z \;=\; x: G,\; y: G $$

One interpretation of $\Gamma$ in $\Delta$ (that is, a morphism from $\Delta$ to $\Gamma$) is given by the substitution
$$ a := a,\; b := b .$$
The fact that $(a b)^2 = a^2 b^2$ in $\Delta$ is ignored.

A less obvious interpretation of $\Gamma$ in $\Delta$ is the substitution
$$ a := b,\; b := a .$$
There is no reason to keep variable names the same.  (At this point, compare $\Gamma$ and $Z$; when the definition is complete, it ought to follow that these are isomorphic.)

Another, perhaps even less obvious, morphism $\Delta \to \Gamma$ is
$$ a := a^2,\; b := a^3 .$$
Not only does this ignore that $(a b)^2 = a^2 b^2$; it also ignores the very existence of $b$ in $\Delta$.  (It also uses the existence of $a$ more than once.  Ignoring and reusing information like this is not always allowed in substructural logics such as [[linear logic]].)

That we can interpret $E$ in $\Delta$ without renaming variables is essentially the meaning of the judgement (eq:valid) above.  That is, we get a morphism form $\Delta$ to $\Epsilon$ by performing the substitution
$$ a := a,\; b := b $$
and then inserting a proof of (eq:valid).  As it happens, the argument in such a proof is reversible, so you should expect that $\Delta$ and $E$ are also isomorphic.

Are there any morphisms from $\Gamma$ to $\Delta$?  The obvious substitution does not define a morphism, since the required fact cannot be proved.  However, you get one using the substitution
$$ a := a,\; b := a $$
and then inserting a proof that
$$ \Gamma \;\vdash\; (a a)^2 = a^2 a^2 .$$
All the same, we would not want to say that $\Gamma$ and $\Delta$ are isomorphic contexts; although there are morphisms in each direction, composing them should never produce identity morphisms on both sides.

Now I should finish defining the category.  First, given a context $\Gamma$, there is an obvious **identity** morphism where every variable is substituted for itself and every statement assumed is proved immediately from itself.

Given morphisms $\Gamma \to^f \Delta \to^g E$, form the **composite** as follows:  First, for each variable $X$ required by $\Gamma$, $f$ tells us how to substitute a term $T$ built out of the variables in $\Delta$, while $g$ tells us how to substitute a term from $E$ for each of these variables.  So in the end, $X$ is expressed as a term $T[g]$ involving variables available in $E$.  Also, by combining the proofs provided by $f$ and $g$, we get the proofs required for their composite.

To really complete the definition of a category, I should also describe when two morphisms $\Gamma \to \Delta$ are **equal**.  There are actually many options here; the most strict is to say that they equal only if the substitutions and proofs used are syntactically identical, and the most weak is to say that any parallel morphisms are equal.  Neither of these is very useful; for purposes of this example, let us require only that the expressions substituted for each variable $X$ in $\Gamma$ can be proved equal in the context $\Delta$.

Now you should be able to prove that composition satisfies the axioms of a [[category]].

Notice that, the exact definition of equality of morphisms can depend heavily on the theory in question and your own purposes.  For example, this definition makes sense only because we have a notion of equality of elements of a group.  Also, you can sometimes place interesting conditions on whether two proofs count as equivalent, rather than requiring either syntactic identity or (as we do here) accepting proof irrelevance.

+--{.un_example}
###### Exercise
Now that the category of contexts (in one sense) of the theory of a group has been completely defined, describe that category (up to [[equivalence of categories|equivalence]]) in terms familiar to an algebraist.  In particular, compare it to the [[Grp|category of groups]].
=--

+--{.proof}
###### Answer
In [rot13](http://www.rot13.com/): gur bccbfvgr bs gur pngrtbel bs svavgryl cerfragrq tebhcf.
=--

+--{.query}
[[Finn Lawler]] Shouldn't that be 'gur bccbfvgr bs gur pngrtbel bs svavgryl trarengrq serr tebhcf'?

Wait, never mind.  I was confusing categories of contexts with Lawvere theories, which don't allow equations in contexts.  I can see how those would give you gur bccbfvgr bs gur pngrtbel bs svavgryl cerfragrq tebhcf.

_Toby_:  Right.  Nothing wrong with your other answer, it just depends on what you mean by 'context'.
=--

# Display morphisms

...

# References
* [[Practical Foundations]], Chapter VIII