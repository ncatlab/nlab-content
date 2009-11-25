# Monadic adjunctions
* tic
{: toc}


## Idea

One can turn [[monads]] into [[adjunctions]] and adjunctions into monads, but one doesn\'t always return where one started.  Every monad comes from an adjunction, but only a _monadic adjunction_ comes from a monad.  (To be fair, there are two ways to turn a monad into an adjunction, given by the [[Kleisli category]] and the [[Eilenberg–Moore category]]; we are talking about the latter here.)


## Definition

We give the definitions in [[Cat]] and leave it to future readers and writers to generalise.

Let $(C,D,\ell,r,\iota,\epsilon)$ be an adjunction in $Cat$; that is, $\ell: C \to D$ and $r: D \to C$ are [[adjoint functors]] with $\ell \dashv r$, where $\iota$ and $\epsilon$ are the unit and counit.  Let $T$ be $r \circ \ell$; $T$ has the structure of a monad on $C$, so consider the [[Eilenberg–Moore category]] $C^T$ of [[module for a monad|modules (algebras)]] for $T$.  Then $r \circ \epsilon: T \circ r \to r$ endows $r: D \to C$ with a $T$-algebra structure, hence defines a [[functor]] $k: D \to C^T$.

The adjunction $\ell \dashv r$ is __monadic__ if this functor $k$ is an [[equivalence of categories]].  


## Beck's monadicity theorem

__Beck's Monadicity Theorem__ gives a necessary and sufficient condition for an adjunction to be monadic.  Namely, the adjunction $(C,D,\ell,r,\iota,\epsilon)$ is monadic iff:

*  $r$ reflects isomorphisms; and
   
*  $D$ has coequalizers of $r$-split coequalizer pairs, and $r$ preserves those coequalizers.


## Algebraic categories

The typical categories studied in [[algebra]], such as [[Grp]], [[Ring]], etc, all come equipped with monadic adjunctions from [[Set]].  Specifically, the [[right adjoint]] is the [[forgetful functor]] from algebras to sets, and the [[left adjoint]] maps each set to the [[free object|free]] algebra on that set.  Their composite (a monad on $Set$) may be thought of as mapping a set $A$ to the set of words with alphabet taken from $A$ and the connections between letters taken from the appropriate algebraic operations, with two words identified if they can be proved equal by the appropriate algebraic axioms.

Abstractly, one may *define* an [[algebraic category]] to be a category equipped with a monadic adjunction from $Set$.  However, there are now more examples than the ones from algebra; the best known of these is the category of [[compact Hausdorff spaces]], which corresponds to the [[ultrafilter]] monad.  (This result relies on the [[ultrafilter principle]], regardless of whether one interprets 'space' here as referring to [[topological spaces]] or [[locales]].)


## References

*  [[Michael Barr]] and [[Charles Wells]], _Toposes, Triples and Theories_ ([online](http://www.cwru.edu/artsci/math/wells/pub/ttt.html))


## Discussion

[[John Baez]]:  We read above: "One can turn [[monads]] into [[adjunctions]] and adjunctions into monads, but one doesn\'t always return where one started."  This suggests that there is something like an _adjunction_ between monads and adjunctions!  What's the precise story?  

I imagine something like this: there's a functor (or 2-functor) 

$$ [adjunctions] \to [monads] $$

and this has left and right adjoints (or 2-adjoints)

$$ Kleisli : [monads] \to [adjunctions] $$

$$ Eilenberg Moore: [monads] \to [adjunctions] $$

As evidence, note that the [[Kleisli category]] gives the initial object among adjunctions that give rise to a specified monad, while the [[Eilenberg-Moore category]] gives the terminal one.  See the [Wikipedia article](http://en.wikipedia.org/wiki/Monad_%28category_theory%29#Monads_and_adjunctions).

Zoran &#352;koda: the best-well-known article on monads, R. Street, _Formal theory of monads_, JPAA 2, 149--168, 1972, has the basic fact that Eilenberg-Moore construction as a correspondence from monads to categories, extends to a 2-functor which is right 2-adjoint to the trivial monad 2-functor and the left adjoint is the underlying 2-functor (forgetting actions). Now you are trying to view EM construction as an adjoint to adjunctions to monads correspondence. First of all, I could imagine several different 2-categories of adjunctions, hence several different questions in the game (and monads make 2-category in more than one way, but with lessvariety than adjunctions). But there are better people to ask about this...

[[Mike Shulman]]: This adjunction does exist (although you sometimes have to be careful about size issues) and is called the **semantics-structure adjunction**.  The EM-category functor $Mnd(C) \to RAdj/C$ is called the "semantics" functor (here $RAdj/C$ is the subcategory of $Cat/C$ consisting of the right adjoints) and its left adjoint (the monad underlying an adjunction) is called the "structure" functor.  In fact, the structure functor is defined on a larger subcategory of $Cat/C$, namely those functors $g:A\to C$ such that $Ran_g g$ exists (if $g$ has a left adjoint $f$ then $Ran_g g$ always exists and is equal to $g f$).  In this case $Ran_g g$ is the image of $g$ under "structure", also called its *codensity monad*.  Presumably by duality, "structure" also has a left adjoint "cosemantics" given by the Kleisli construction.  The semantics-structure adjunction can be found in Chapter II of Dubuc's "Kan Extensions in Enriched Category Theory" and also in section 2 of "The Formal Theory of Monads".

If anyone can give a nice conceptual explanation of the terms "semantics" and "structure" in this context, Daniel Schaeppi is currently writing a paper which could benefit from such an explanation.  I've never found anyone who really explains the words (nor is it entirely clear who pioneered their use in this context---Dubuc perhaps?)  It makes sense to me that the E-M category can be called the "semantics" of a monad, but my intuition for "structure" is fuzzier, except that of course any monad can be regarded as a notion of [[stuff, structure, property|structure]] with which one can equip objects.  But why is that "the" structure associated to an adjunction?

[[Mike Shulman]]: In case anyone is following this, Daniel has come up with what seems to be the right answer to this question; I'm hoping that eventually he will write about it here.

[[!redirects Beck's Monadicity Theorem]]
[[!redirects Beck's Monadicity Theorem]]
[[!redirects Beck Monadicity Theorem]]
[[!redirects Beck's monadicity theorem]]
[[!redirects Beck's monadicity theorem]]
[[!redirects Beck monadicity theorem]]
[[!redirects semantics-structure adjunction]]
