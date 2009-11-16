A Boolean algebra is an algebraic structure which models classical [[propositional calculus]], roughly the fragment of the logical calculus which deals with the basic logical connectives "and", "or", "implies", and "not". 


## Definition 

There are many known ways of defining a Boolean algebra. Here are just a few: 

* A Boolean algebra is a [[complement]]ed [[distributive lattice]]. 

* A Boolean algebra is a [[Heyting algebra]] $H$ satisfying the law of excluded middle, which means either 
$$\neg \neg = id: H \to H$$ 
or (equivalently) 
$$\forall_{x \in H} x \vee \neg x = \top$$

* A Boolean algebra is a [[lattice]] $L$ equipped with a function $\neg: L \to L$ satisfying 
$$a \wedge b \leq c \qquad iff \qquad a \leq \neg b \vee c$$


## Homomorphisms

Any [[lattice]] homomorphism automatically preserves $\neg$ and is therefore a Boolean algebra homomorphism.


[[!redirects Boolean lattice]]
[[!redirects boolean algebra]]
[[!redirects boolean lattice]]
[[!redirects Boolean algebras]]
[[!redirects Boolean lattices]]
[[!redirects boolean algebras]]
[[!redirects boolean lattices]]