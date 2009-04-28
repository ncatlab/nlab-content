#Idea#

A gentle, detailed introduction to the basic ideas of the notion "sheaf" is at

* [[heuristic introduction to sheaves, cohomology and higher stacks]].

A [[presheaf]] can be regarded as an assignment of "sets of structures to [[space and quantity|spaces]]", such that these structures can be pulled back along maps of spaces. A presheaf is a _sheaf_ if this assignment satisfies [[descent]]: if $\pi: Y \to X$ is a _cover_ of a space $X$ by a space $Y$, then the collection of structures assigned to $X$ is isomorphic to the collection of structures assigned to $Y$ which _glue_ and hence descend from $Y$ down to $X$.

Generally, to any cover $Y \to X$  and presheaf $G$ there is associated a descent [[set]] $Desc(Y,G)$ whose objects are the elements of $G(Y)$ which glue. There is also a canonical morphism

$$
  G(X) \to Desc(Y,G)
  \,.
$$

A presheaf is a _sheaf_ if this canonical morphism is an [[isomorphism]].

#Remarks#

* The [[vertical categorification|categorifications]] of sheaves are
  * [[stack|stacks]];
  * [[infinity-stack|infinity-stacks]].

Here the descent set ($0$-category) is replaced by a descent [[category]] or $\infty$-[[infinity-category|category]].

#Definition#

## In terms of sieves ##

One formalization of the descent set is obtained from representing a cover $Y$ by the corresponding [[presheaf]] $S_Y : C^{op} \to Set$ -- a [[sieve]] -- and defining the descent set as

$$
  Desc(Y,G) := Set^{C^{op}}(S_Y, G)
  \,.
$$

So: given a [[site]] $(C, J)$, a _sheaf_ over that site is a [[presheaf]] 

$$G: C^{op} \to Set$$ 

such that whenever $i: F \hookrightarrow \hom(-, c)$ is a [[Grothendieck topology|covering sieve]], the map 

$$G(c) \stackrel{Yoneda}{\cong} Set^{C^{op}}(\hom(-, c), G) \stackrel{Set^{C^{op}}(i, G)}{\to} Set^{C^{op}}(F, G)$$ 

is an isomorphism. 

## In terms of orientals ##

When generalizing sheaves to  [[stack|stacks]] and then to  [[infinity-stack|infinity-stacks]] the Hom-set $Set^{C^{op}}(F, G)$ in the above definition, representing the descent set (0-category), needs to be generalized to a corresponding [[category]] or [[infinity-category]] [[functor category|of infinity-functors]] whose objects are the $\infty$-functors from the cover/sieve $F$ to the presheaf $G$, whose morphisms are homotopies between these, whose higher morphisms are the higher homotopies. The technical problem is to formalize these $\infty$-categories of $\infty$-functors. This is one of the central issues of [[higher category theory]].

One partial solution to the problem has been given by Ross Street, who defined descent [[strict omega-category|strict omega-categories]] $Desc(Y,G)$ for $\omega$-category-valued presheaves $G : C^{op} \to \omega Cat$ in terms of [[oriental|orientals]]. The $\omega$-category $Desc(Y,G)$ can be regarded as the $\omega$-category of lax $\infty$-functors from the sieve associated with $Y$ to $G$.

In the case that the $\omega$-categories in questions happen to be just [[n-category|0-categories]] this reduces to the definitin of descent 0-categories for presheaves. 

Of course the machinery of [[oriental|orientals]] is overkill for just defining sheaves, but it is instructive to understand sheaves in this language, since then the generalization to [[stack|stacks]] and [[infinity-stack|infinity-stacks]] is straightforward.

So let $\pi : Y \to X$ be a morphism of objects of $C$ such that the pullback of $\pi$ along itself

$$
  \array{
    Y^{[2]} &\stackrel{\pi_1}{\to}& Y
    \\
    \downarrow^{\pi_2} && \downarrow^\pi
    \\
    Y &\stackrel{\pi}{\to}& X
  }
$$

exists. Let $G : C^{op} \to Set \hookrightarrow \omega Cat$ be a [[strict omega-category]] valued presheaf which happens to take values just in $0$-[[0-category|categories]]. Then an _object_ (an element) in the descent $\omega$-category $Desc(Y,G)$ (which is a set here) is a tuple consisting of

* an element $a \in G(Y)$;

* a morphism $\pi_1^* a \stackrel{g}{\to} \pi_2^* a$ in $G(Y^{[2]})$, which is by assumption necessarily an 
[[identity]]: $\pi_1^* a \stackrel{=}{\to} \pi_2^* a$.

The point to notice is that the morphism $\pi_1^* a \stackrel{g}{\to} \pi_2^* a$ is the image of the [[oriental|first oriental]] $G_1 = \{a \to b\}$ in $G(Y^{[2]})$.

This definition can be formalized as an [[end]]

$$
  Desc(Y,G) := \int_{[n] \in \Delta}
  hom(O([n]), G(Y^n))
  \,,
$$

where

* $\Delta$ is the [[simplex category]];

* $O : \Delta \to \omega Cat$ are the [[oriental|orientals]].


From this definition one obtains the canonical morphism

$$
  G(X) \to Desc(Y,G)
$$

form the universal property of then end. The _sheaf condition_ is, as before, that this canonical morphism is an isomorphism for all covers $Y \to X$. 

From the above explicit characterization of $Desc(Y,G)$ this is manifestly the familiar gluing condition for sheaves: the presheaf $G$ is a sheaf if the elements in $G(Y)$ which coincide (glue) on double intersections $Y^{[2]}$ correspond bijectively to the elements in $G(Y)$.



#Examples#

The archetypical example of sheaves are _sheaves of functions_:

* for $X$ a topological space, $\mathbb{C}$ a topological space and $O(X)$ the [[site]] of open subsets of $X$, the assignment $U \mapsto C(U,\mathbb{C})$ of continuous functions from $U$ to $\mathbb{C}$ for every open subset $U \subset X$ is a sheaf on $O(X)$.

* for $X$ a complex manifold and $\mathbb{C}$ a complex manifold, the assignment $U \mapsto C_{hol}{X,\mathbb{C}}$ of holomorphic functions in a sheaf.


#References#

The book by MacLane and Moerdijk has an emphasis on the [[topos]]-theoretic aspects of sheaves:

* S. MacLane, I. Moerdijk, _Sheaves in geometry and logic -- A first introduction to topos theory_, Springer

The book by Kashiwara and Shapira discusses sheaves with motivation from homological algebra and [[homotopy theory]], leading over in the last chapter to the notion of [[stack]].

* Kashiwara, Shapira, [[Categories and Sheaves]], Springer
