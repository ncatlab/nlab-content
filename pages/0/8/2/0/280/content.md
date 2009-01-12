An _action_ of a [[group]] $G$ on an [[object]] $x$ in a [[category]] $C$ is a [[group homomorphism]] $\rho : G \to Aut(x)$, where $Aut(x)$ is the group of [[automorphism|automorphisms]] of $x$.  

A more sophisticated but equivalent definition treats the group $G$ as a category with one object, say $*$.  Then an _action_ of $G$ in the category $C$ is just a [[functor]] 
$$\rho : G \to C .$$  
Here the object $x$ of the previous definition is just $\rho(*)$. 

More generally we can define an _action_ of a [[monoid]] $M$ in the category $C$ to be a functor
$$\rho: M \to C $$
where $M$ is regarded as a one-object category.

The _category of actions_ of $M$ in $C$ is then defined to be the [[functor category]] $C^M$.  

+--{.query}
I am wondering if we will need the notion of action which works in categories with product, i.e. $G\times X\to X$ and so on. There is also an action of one Lie algebra on another (for instance in some definitions of crossed module of Lie algebra, where $Aut$ is replaced by the Lie algebra of derivations. (a similar situation would seem to exist in various other categories where action is needed in a slightly wider context. I think most would be covered by an enriched setting but I am not sure.) Thoughts please.[[Tim Porter|Tim]]
=--