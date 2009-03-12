#The Idea 

A preorder is like a [[partial order]], but without the requirement that $x \le y$ and $y \le x$ implies $x = y$.  The reason is that if we think of a partially ordered set as a special sort of [[category]], it is [[evil]] to impose this equation between objects.  In a preorder, if $x \le y$ and $y \le x$, we think of $x$ and $y$ as [[isomorphism|isomorphic]].

#Definition

A set equipped with a **preorder** is a ([[small category|small]]) [[category]] such that for any pair of objects $x, y$, there is at most one morphism from $x$ to $y$. In other words, it's a category [[enriched category theory|enriched]] over the category of [[truth value]]s.

People who call a partially ordered set a '[[poset]]' and a totally ordered set a '[[toset]]' may enjoy calling a preordered set a '[[proset]]'.  While not as common as 'poset', this term is occasionally used in the literature.  It is also not uncommon to see "preorder" used in the literature to mean "set equipped with a preorder."

#Fact

Any preordered set is [[equivalence of categories|equivalent]] to a [[poset]]. This is a special case of the theorem that every category has a [[skeleton]], but (if you define 'equivalence' properly) this case does _not_ require the [[axiom of choice]].

#Discussion

_[[Todd Trimble|Todd]] says:_ It's not clear to me how one avoids the axiom of choice. For example, any equivalence relation $E$ on a set $X$ defines a preorder whose posetal reflection is the quotient $X \to X/E$, and it seems to me you need to split that quotient to get the equivalence between the preorder and the poset.

_[[Toby Bartels|Toby]] says:_ In the absence of the axiom of choice, the correct definition of an equivalence of categories $C$ and $D$ is a span $C \leftarrow X \rightarrow D$ of full, faithful, essentially surjective functors. Or equivalently, a pair $C \leftrightarrow D$ of [[anafunctor]]s (with the usual natural transformations making them inverses).

_[[Todd Trimble|Todd]] says:_ Thanks, Toby. So if I understand you aright, the notion of equivalence you have in mind here is not the one used at the top of the entry [[equivalence]], but is more subtle. May I suggest amplifying a little on the above, to point readers to the intended definition, since this point could be confusing to those inexperienced in these matters? 

_[[Urs Schreiber|Urs]] says_: as indicated at [[anafunctor]] an equivalence in terms of anafunctors can be understood as a span representing an [[isomorphism]] in the [[homotopy category]] of $Cat$ induced by the [[folk model structure]] on $Cat$.

_Toby says_: I think that this should go on [[equivalence]], so I\'ll make sure that it\'s there. People that don\'t know what 'equivalence' means without choice should look there.

***

_[[Eric Forgy|Eric]] says_: It seems to me that any category $C$ gives rise to a preorder in a natural way, i.e.

$$a\to b\in Mor(C)\implies a\le b.$$

Is there a slick arrow theoretic way to say that? Something like, "There is a [[forgetful functor]] $F:Cat\to Ord$"?

I hope to write/read some arrow theoretic definition of a [[Hasse diagram]] too.

_Mathieu says_: It's rather the other way round: there is a "forgetful" 2-functor $Ord \to Cat$ (which forgets that the category is in fact an order (it's a full inclusion, so it forgets a property rather than a structure)), and the left adjoint to this 2-functor maps a category $C$ to the order with the same objects as $C$ and $a\leq b$ iff there exists an arrow $a\to b$.

_[[John Baez|John]] says_: You might try to define a Hasse diagram to be a [[directed graph]] whose [[quiver]] is a [[poset]].  In other words, you take a directed graph, consider the free category on that graph, and demand that this category be a poset.  

However, maybe it's a rule that a [[Hasse diagram]] with directed edges $x \to y$ and $y \to z$ is not allowed to have a directed edge $x \to z$.   If so, this is a further restriction on what directed graphs count as Hasse diagrams. 

_Toby_:

Eric, there *is* a functor $\Cat \to \Ord$ as you describe.  If you call it a forgetful functor, then a category is a proset with extra stuff (not just structure), since this functor is not faithful (although interestingly it is both full and essentially surjective, so it forgets 'only stuff').  In contrast, a proset is a category with extra property (as you can literally see from John\'s slick definition above), since the functor $\Ord \to \Cat$ is fully faithful (as Matthieu points out).

(Recall that [[essentially surjective functor]]s, [[full functor]]s, and [[faithful functor]]s form the three anti-homogenous parts of the yoga of stuff, structure, and property, where in general you can call *any* functor a 'forgetful functor' and see what that gets you.  I am treating only the $1$-category of categories, since otherwise this discussion would be at [[poset]] by rights.)

For a Hasse diagram, I like John\'s definition.  It is true that a Hasse diagram shouldn\'t have an edge $x \to z$ if there are edges $x \to y \to z$, but this follows; it\'s not a further restriction.  (Similarly, there can\'t be any loops, even though directed graphs in general should allow them.)

_Mike_: I don't think the preorder reflection $Cat\to Ord$ is full.  Let $C$ be the walking commutative square (aka $\mathbf{2}\times\mathbf{2}$, where $\mathbf{2}$ is the walking arrow), and let $D$ be the walking non-commutative square (the free category on the directed graph that looks like a square with no diagonals).  Then $C$ and $D$ have isomorphic preorder reflections, but I don't believe there is a functor $C\to D$ mapping to this isomorphism.
