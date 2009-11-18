## Idea

A compactum, or compact Hausdorff space, is a space in which every limit that should exist does exist and does so uniquely.

One can define this literally for [[topological spaces]], or in terms of [[convergence spaces|convergence]], or for [[locales]]; although these are all different contexts, the resulting notion of compactum is (at least assuming the [[axiom of choice]]) always the same.  Interestingly, there is even an algebraic definition, not one that uses only finitary operations, but one which uses a [[monad]]. 


## Definitions

If you know what a [[compact space]] is and what a [[Hausdorff space]] is, then you know what a compact Hausdorff space is, so let\'s be fancy.

Given a [[set]] $S$, let $\beta S$ be the set of [[ultrafilters]] on $S$.  Note that $\beta$ is an [[endofunctor]] on [[Set]]; every [[function]] $f: S \to T$ induces a function $\beta f: \beta S \to \beta T$ using the usual application of functions to [[filters]].  In fact, $\beta$ is a [[monad]]; it comes with a [[natural transformation|natural]] (in $S$) unit $\eta_S: S \to \beta S$, which maps a point $x$ to the [[principal ultrafilter]] that $x$ generates, and multiplication $\mu_S: \beta \beta S \to \beta S$, which maps an ultrafilter $U$ on ultrafilters to the ultrafilter of sets whose principal ultrafilters of ultrafilters belong to $U$.  That is,
*  $ A \in \eta x \;\Leftrightarrow\; x \in A $, so $ \eta x = \{ A \subseteq S \;|\; x \in A \} $;
*  $ A \in \mu U \;\Leftrightarrow\; \{ F \in \beta S \;|\; A \in F \} \in U $.

Then a __compactum__ is simply an [[algebra for a monad|algebra]] for this monad; that is, a set $X$ together with a function $\lim: \beta X \to X$, such that
*  each point $x$ is the limit ($\lim$) of the principal ultrafilter $\eta x$, and
*  given an ultrafilter $U$ on ultrafilters, the limit of $\mu U$ is the limit of $(\beta \lim) U$.

It is then a theorem that this $\lim$ generates a [[convergence space|convergence]] on $S$ that is [[compact space|compact]], [[Hausdorff space|Hausdorff]], and [[topological space|topological]].  The converse, that every compact Hausdorff topological convergence is of this form, is equivalent to the [[ultrafilter principle]].

Every compact Hausdorff space is [[regular space|regular]] and [[sober space|sober]] and so defines a compact regular locale.  Again, the [[axiom of choice]] gives us a converse: every compact regular locale is spatial and so comes from a compactum.
>Probably this is also equivalent to the ultrafilter principle, but I need to check.

Note that every compact Hausdorff space (topological or localic) is not only regular but also [[normal space|normal]].


## In weak foundations

In the absence of the axiom of choice, and especially in [[constructive mathematics]], the best definition of compactum seems to be a compact regular locale.  That is, it is the category of compact regular locales that has all of the nice properties, forming a [[nice category of spaces]], and that has the desired examples, such as the [[unit interval]].  (See the discussion at [[Tychonoff theorem]] for an example of how the category of compact Hausdorff topological spaces might fail to be nice; see [Frank Waaldijk's PhD thesis](http://home.kpn.nl/sufra/foundations%20of%20constructive%20mathematics.pdf) (pdf) for a thorough discussion of what is needed to make the unit interval a compact Hausdorff topological space.)

The monadic definition, in particular, falls quite flat without some form of the axiom of choice; even [[excluded middle]] and [[COSHEP]] are powerless here.  In fact, it is quite consistent to assume that every ultrafilter is principal (a strong denial of the ultrafilter principle), in which case $\beta$ is the [[identity monad]].  Then a compactum would be just a set if that were the definition used.

On the other hand, it is the monadic definition that gives an [[algebraic category]] with a nice relationship to [[Set]].  Without the ultrafilter principle, there is no reason to think that the set-of-points functor from compact regular locales to sets is even [[continuous functor|continuous]].


## Stone--&#268;ech compactification

The monad $\beta$ is commutative, so every $\beta S$ is itself a compactum.  The functor $\beta: Set \to Comp$ is [[left adjoint]] to the [[forgetful functor]] $Comp \to Set$.  Assuming the ultrafilter principle, this can be generalised to a functor $\beta: Top \to Comp$ (identifying a set with its [[discrete space]]) that is left adjoint to the forgetful functor $Comp \to Top$.  This (or at least its restriction to [[Tychonoff space]]s) is the __Stone--&#268;ech compactification__ functor.  We have a similar Stone-&#268;ech compactification functor $Loc \to Comp$; we do not need the ultrafilter principle here if $Comp$ is defined in terms of locales.


[[!redirects compact Hausdorff space]]
[[!redirects compact Hausdorff topological space]]
[[!redirects compact regular locale]]
[[!redirects compacta]]
[[!redirects Stone-∞ech compactification]]
[[!redirects Stone-Cech compactification]]
[[!redirects Stone?ech compactification]]
[[!redirects StoneCech compactification]]
[[!redirects Stone--∞ech compactification]]
[[!redirects Stone--Cech compactification]]