#Definition#

An **action** of a [[group]] $G$ on an [[object]] $x$ in a [[category]] $C$ is a [[group homomorphism]] $\rho : G \to Aut(x)$, where $Aut(x)$ is the group of [[automorphism|automorphisms]] of $x$.  

A more sophisticated but equivalent definition treats the group $G$ as a category denoted $BG$ with one object, say $*$.  Then an _action_ of $G$ in the category $C$ is just a [[functor]] 
$$\rho : BG \to C.$$  
Here the object $x$ of the previous definition is just $\rho(*)$. 

+--{.query}
  [[Urs Schreiber|Urs]]: I would prefer if we denote 
a group $G$ when regarded as a one-object groupoid by
$\mathbf{B} G$, and keep the symbol $G$ for its incarnation
as a monoidal 0-category.
We had half of a discussion of this issue 
at the end of [[category algebra]], where I tried to list
a couple of arguments for why this practice 
is good and helpful. 
Indeed, if the counterargument is that writing 
$\mathbf{B} G$ is overly scary or the like, I would like
to make a case that this notation actually makes
it easier to understand some patterns instead of harder.
In any case, whatever we decide to do, I would enjoy
feedback on the points I raised in the discussion
at the end of [[category algebra]].
=--

More generally we can define an _action_ of a [[monoid]] $M$ in the category $C$ to be a functor
$$\rho: M \to C $$
where $M$ is regarded as a one-object category.

The _category of actions_ of $M$ in $C$ is then defined to be the [[functor category]] $C^M$.  

+--{.query}
I am wondering if we will need the notion of action which works in categories with product, i.e. $G\times X\to X$ and so on. There is also an action of one Lie algebra on another (for instance in some definitions of crossed module of Lie algebra, where $Aut$ is replaced by the Lie algebra of derivations. (a similar situation would seem to exist in various other categories where action is needed in a slightly wider context. I think most would be covered by an enriched setting but I am not sure.) Thoughts please.[[Tim Porter|Tim]]
=--