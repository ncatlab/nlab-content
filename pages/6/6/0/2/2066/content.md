#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The _Karoubi envelope_ of a [[category]] is the universal way to ensure that every [[idempotent]] is a [[split idempotent]].  It is the [[Set]]-enriched version of [[Cauchy completion]].

## Definition ## 

Let $C$ be a [[category]]. We give an elementary construction of the __Karoubi envelope__ $\bar{C}$ which formally splits [[idempotents]] in $C$. 


The objects of $\bar{C}$ are pairs $(c, e: c \to c)$ where $e$ is an idempotent on an object $c$ of $C$. Morphisms $(c, e) \to (d, f)$ are morphisms $\phi: c \to d$ in $C$ such that $f \circ \phi = \phi = \phi \circ e$. NB: the identity on $(c, e)$ in $\bar{C}$ is the morphism $e: c \to c$. 


There is a functor 

$$E: C \to \bar{C}$$ 

which maps an object $c$ to $(c, 1_c)$. This functor is [[fully faithful functor|full and faithful]]: it fully embeds $C$ in $\bar{C}$. If $e: c \to c$ is an idempotent in $C$, then in $\bar{C}$ there are maps 

$$p: (c, 1_c) \to (c, e), \, j: (c, e) \to (c, 1_c),$$ 

both given by $e: c \to c$. It is clear that $p \circ j$ is the identity $e: (c, e) \to (c, e)$, and that $j \circ p$ is the idempotent $E(e): E(c) \to E(c)$. Thus the pair $(p, j)$ formally splits the idempotent $e: c \to c$. The same argument shows that every idempotent $\phi: (c, e) \to (c, e)$ in $\bar{C}$ splits. Actually this formal construction does more: it gives a _choice_ of splitting for every idempotent. 


Let $D$ be any category in which every idempotent $h: d \to d$ has a chosen splitting $(p_h: d \to d_h, j_h: d_h \to d)$ (using identities to split identities), and let $F: C \to D$ be a functor. Define an extension 

$$\bar{F}: \bar{C} \to D$$ 

by sending $(c, e: c \to c)$ to the underlying object $F(c)_{F(e)}$ of the splitting of $F(e): F(c) \to F(c)$ in $D$. For morphisms $\phi: (c, e) \to (c', e')$, define $\bar{F}(\phi)$ to be the composite 

$$F(c)_{F(e)} \overset{F(j_{F(e)})}{\to} F(c) \overset{F(\phi)}{\to} F(c') \overset{F(p_{F(e')})}{\to} F(c')_{F(e')}$$ 

Then $\bar{F}$ is the unique extension of $F$ which preserves chosen splittings. Thus the Karoubi envelope is universal among functors from $C$ into categories $D$ in which every idempotent has a chosen splitting. 


If $D$ is a category in which every idempotent splits, then we can choose a splitting for each idempotent using the [[axiom of choice]] (AC); the extension $\bar{F}$ depends on how we do this but is unique up to unique [[natural isomorphism]].  Alternatively, we can define $\bar{F}$ as an [[anafunctor]]; then no AC is needed, and we still have $\bar{F}$ unique up to unique natural isomorphism.  (It is key here that a splitting of an idempotent is unique up to a coherent isomorphism.)



## References ##

Karoubi envelopes for [[(infinity,1)-category|(∞,1)-categories]] are discussed in section 4.4.5 of

* [[Jacob Lurie]], [[Higher Topos Theory]]. 


Some discussion of the stable version is in section 4.1.2 of

* [[David Ben-Zvi]], John Francis, David Nadler, _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry_ ([arXiv](http://arxiv.org/abs/0805.0157), [[geometric infinity-function theory|nLab entry]])

and section 2.3 of 

* [[David Ben-Zvi]], David Nadler, _The Character Theory of a Complex Group_ ([arXiv](http://arxiv.org/abs/0904.1247))

In section 3.1.2 of latter are also given
references (to Neeman and Lurie) for an important result of Neeman's about Karoubi closure and compact generators.

The Karoubi envelope for the additive case (see also [[additive envelope]]) is covered at 

* Dror Bar-Natan, Scott Morrison, _The Karoubi envelope and Lee's degeneration of Khovanov homology_ ([arXiv](http://arxiv.org/abs/math/0606542))

