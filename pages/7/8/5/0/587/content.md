In [[logic]], the **context** of an assertion (or judgement) consists of all of the assumptions that are made when that assertion to claimed be valid; whether an assertion is in fact valid (or even meaningful) may depend on the context.

Generally, a context is thought of as relative to some underlying logical theory.  This underlying theory will contain most of the assumptions of what constitutes validity; the context of an assertion in this theory will then include only those extra assumptions that may be used by that assertion.  (On the other hand, one could also think of the entire base theory as part of the context.)

For example, in the theory of a [[group]], it is understood that there is a group $G$, that $G$ has various elements, that two elements of $G$ may be equal, that any two elements of $G$ have as product an element of $G$, and that various equational laws are satisfied (which we will not list here).  However, the validity and meaningful of an assertion that two elements of $G$ commute will depend on the context.

To be more explicit, the assertion that $a$ and $b$ commute does not make sense without the additional context that $a$ and $b$ are elements of $G$.  Even in that context, this assertion, while at least meaningful, is not valid.  However, if we add to the context the assumption that $(a b)^2 = a^2 b^2$, then the assertion is valid.  Written symbolically,
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

However, these versions involve $\forall$ and $\Rightarrow$, while the previous versions work in weaker logics.  In fact, these assertions make sense (and the valid one may be proved) in the [[internal logic]] of a [[group object]] in a [[finitely complete category]] (and somewhat more generally than that).  Accordingly, they can be interpreted as statements about any group object in any finitely complete category (and the valid one will then be interpreted as a true statement), exactly as they do for groups (which are group objects in the finitely complete category [[Set]]).

Even if one is completely uninterested in [[internalization]] or weak logics, a basic familiarity with contexts may help drive home a point that is important throughout reasoning:  **What you can state and prove depends on your assumptions.**

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

That we can interpret $E$ in $\Delta$ without renaming variables is essentially the meaning of the judgement (eq:valid) above.  That is, we get a morphism from $\Delta$ to $E$ by performing the substitution
$$ a := a,\; b := b $$
and then inserting a proof of (eq:valid).  As it happens, the argument in such a proof is reversible, so you should expect that $\Delta$ and $E$ are also isomorphic.

Are there any morphisms from $\Gamma$ to $\Delta$?  The obvious substitution does not define a morphism, since the required fact cannot be proved.  However, you get one using the substitution
$$ a := a,\; b := a $$
and then inserting a proof that
$$ \Gamma \;\vdash\; (a a)^2 = a^2 a^2 .$$
All the same, we would not want to say that $\Gamma$ and $\Delta$ are isomorphic contexts; although there are morphisms in each direction, composing them should never produce identity morphisms on both sides.

Now I should finish defining the category.  First, given a context $\Gamma$, there is an obvious **identity** morphism where every variable is substituted for itself and every statement assumed is proved immediately from itself.

Given morphisms $\Gamma \to^f \Delta \to^g E$, form the **composite** as follows:  First, for each variable $X$ required by $\Gamma$, $f$ tells us how to substitute a term $T$ built out of the variables in $\Delta$, while $g$ tells us how to substitute a term from $E$ for each of these variables.  So in the end, $X$ is expressed as a term $T[g]$ involving variables available in $E$.  Also, by combining the proofs provided by $f$ and $g$, we get the proofs required for their composite.

To really complete the definition of a category, I should also describe when two morphisms $\Gamma \to \Delta$ are **equal**.  There are actually many options here; the most strict is to say that they are equal only if the substitutions and proofs used are syntactically identical, and the most weak is to say that any parallel morphisms are equal.  Neither of these is very useful; for purposes of this example, let us require only that the expressions substituted for each variable $X$ in $\Gamma$ can be proved equal in the context $\Delta$.

Now you should be able to prove that composition satisfies the axioms of a [[category]].

Notice that the exact definition of equality of morphisms can depend heavily on the theory in question and your own purposes.  For example, this definition makes sense only because we have a notion of proving equality of elements of a group.  Also, you can sometimes place interesting conditions on whether two proofs count as equivalent, rather than requiring either syntactic identity or (as we do here) accepting proof irrelevance.

+--{.un_example}
###### Exercise
Now that the category of contexts (in one sense) of the theory of a group has been completely defined, describe that category (up to [[equivalence of categories|equivalence]]) in terms familiar to an algebraist.  In particular, compare it to the [[Grp|category of groups]].
=--

+--{.proof}
###### Answer
In [rot13](http://www.rot13.com/): gur bccbfvgr bs gur pngrtbel bs svavgryl cerfragrq tebhcf.
=--

+--{: .query}
_David_: Not too sophisticated a code. What can be said in general about such context phenomena? Seems reminiscent of algebraic theories being equivalent to the opposite of the category of their free models.

_Toby_:  If you mean rot13, it\'s only supposed to be sophisticated enough to keep people from reading it accidentally (and also to be involutory).  The link is mostly for lazy people.

As for the code that hides finitely presented groups in this category of contexts, or free groups on finite sets in the category of contexts without equational hypotheses, or groups in the category of contexts with arbitrary hypotheses in the language of higher-order logic, well ... that\'s sophisticated enough that I don\'t understand it very well yet.  But I do believe that it\'s closely related to hiding a Lawvere theory\'s free models in itself.

[[Mike Shulman|Mike]]: It's true in the generality of any finite-limit theory.  (And, presumably, there are infinitary generalizations.)  There's some general discussion in the [[Elephant]].
=--

# Display morphisms

...

# References
* [[Practical Foundations]], Chapter VIII
* The [[Elephant]], Section D4.4

# Discussion

The following discussion was initiated by a previous version of the above entry which referred to "cartesian multicategories" rather than finitely complete categories.

+--{: .query}
[[Mike Shulman|Mike]]: What is a cartesian multicategory, and how do I interpret the theory of groups in one?  I can guess what it would mean for a multicategory to have finite products.  But if I interpret the multiplication as a morphism $G\times G\to G$, then I'm not using the multicategory structure, so we might as well just be in a category with finite products.  And if I interpret the multiplication as a multimap $(G;G)\to G$, then I don't know how to interpret the axiom of inverses, since there is no 'diagonal' $G\to (G;G)$ or 'projection' $G\to ()$.

_Toby_:  I\'m not sure why I generalised to cartesian multicategories, but it is a nontrivial generalisation.  (Perhaps I was planning to show, as an example, how the category of contexts of the canonical language of a multicategory becomes a monoidal category or something, but that doesn\'t seem very useful.  Maybe I was just doing unnecessary generality, but of course it\'s not the absolutely most general situation either.)

Anyway ... you make a multicategory cartesian much as you might make a monoidal category cartesian by equipping it with appropriate diagonal and projection maps.  The problem is that, while $G \to G \otimes G$ and $G \to 1$ make sense in a monoidal category, they don\'t make sense in a multicategory.  But you fix this by filtering through Yoneda.

So a __cartesian multicategory__ is a multicategory equipped with, for each object $G$ and object $X$, a function $\check{G}^*_X: hom(G;X) \leftarrow hom(G,G;X)$ and a function $\hat{G}^*_X: hom(G;X) \leftarrow hom(;X)$.  (H\'m, my commas and semicolons are the opposite of yours; no matter.)  Then these are subject to various coherence requirements that should be obvious.

[[Mike Shulman|Mike]]: Okay, I see.  Though I'm guessing you wanted those natural transformations to go the other way.  Are there any naturally occurring examples of cartesian multicategories that are not cartesian monoidal categories?  Even if there are, I'm inclined to regard the concept as esoteric enough that it would be clearer to just say "category with finite products" in this introductory article.

_Toby_:  Ah, the curse of contravariance!  Going over the whole introduction again, I think that I understand why I mentioned multicategories, which is that a context like $a: G, b: G$ is more naturally interpreted as a list $(G, G)$ of objects than as a single object $G \times G$.  But if we were really to go in that direction, then we\'d also want the context $a: G, b: G, (a b)^2 = a^2 b^2$ to be interpreted as a list in its own right rather than an actual subobject of $G \times G$, and that\'s going a bit far ... farther than I understand clearly, in any case.  So in fact I let the category be finitely complete so that we could form that subobject (referred to only via the link to [[internal logic]], of course).

[[Mike Shulman|Mike]]: True.  Is a one-object cartesian multicategory the same as a Lawvere theory, aka an operad relative to the theory of categories with finite products?  If so, then perhaps the relevant place to work is a multicategory relative to the theory of lex categories?  Can that be generalized to stronger logics?

_Toby_:  Yes, that seems to be right, that Lawvere theories are equivalent to one-object cartesian multicategories (cartesian multimonoids? cartesian operads?).  So this should work.

Of course, one thing that contexts do is to form an honest category even if you start with a multicategory.  So here we\'re trying to go backwards and see what bare-bones starting point could lead to the same category of contexts of the equational theory of a group.
=--
