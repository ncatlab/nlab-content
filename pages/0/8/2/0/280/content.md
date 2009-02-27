#Definition#


There are various variants of the notion of something _acting_ on something else. They are all closely related.

For an entity $K$ to be able to act on anything else in the first place, $K$ needs to have some notion of composition or product with itself. Quite generally this is modeled by realizing $K$ as an [[n-category]] of sorts. In particular, if $K$ is a monoidal entity with a product $K \otimes K \to K$ there is usually a one-object category $\mathbf{B} K$ which encodes the same information.

From this perspective one fundamental way to realize an action of some entity $K$ on some entity in the [[category]] or [[n-category]] $C$ is an ($n$-)functor

$$
  \rho : K \to C
$$
or
$$
  \rho : \mathbf{B} K \to C
$$


Here the collection $\sqcup_{k \in Obj(k)} \rho(k)$ of objects in $C$ in the image of objects of $K$ is "what $K$ is acting on" and the images of the morphisms in $K$ under $\rho$ produce the action itself.

##Action of a group ##

An **action** of a [[group]] $G$ on an [[object]] $x$ in a [[category]] $C$ is a [[group homomorphism]] $\rho : G \to Aut(x)$, where $Aut(x)$ is the group of [[automorphism|automorphisms]] of $x$.  


As indicated above, a more sophisticated but equivalent definition treats the group $G$ as a category denoted $\mathbf{B} G$ with one object, say $*$.  Then an _action_ of $G$ in the category $C$ is just a [[functor]] 
$$\rho : \mathbf{B} G \to C.$$  
Here the object $x$ of the previous definition is just $\rho(*)$. 


## Action of a monoid ##

More generally we can define an _action_ of a [[monoid]] $M$ in the category $C$ to be a functor
$$\rho: \mathbf{B} M \to C $$
where $\mathbf{B} M$ is (again) $M$ regarded as a one-object category.

The _category of actions_ of $M$ in $C$ is then defined to be the [[functor category]] $C^{\mathbf{B} M}$.

## Action of a category ##

One can also define an [[action of a category on a set|action of a category]] $D$ on the category $C$ as a functor from $C$ to $D$, but usually one just calls this a [[functor]].

Another perspective on the same situation is: a (small) category is a [[monad]] in the category of [[span]]s in [[Set]]. An action of the category is an algebra for this monad. See [[action of a category on a set]].

+--{.query}
I am wondering if we will need the notion of action which works in categories with product, i.e. $G\times X\to X$ and so on. There is also an action of one Lie algebra on another (for instance in some definitions of crossed module of Lie algebra, where $Aut$ is replaced by the Lie algebra of derivations. (a similar situation would seem to exist in various other categories where action is needed in a slightly wider context. I think most would be covered by an enriched setting but I am not sure.) Thoughts please.[[Tim Porter|Tim]]

Yes, I think certainly all those types of action should eventually be described somewhere, possibly on this page.  -Mike

=--
