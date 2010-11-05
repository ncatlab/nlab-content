
# Boolean algebras
* table of contents
{: toc}

## Idea

A Boolean algebra or Boolean lattice is an algebraic structure which models classical [[propositional calculus]], roughly the fragment of the logical calculus which deals with the basic logical connectives "and", "or", "implies", and "not". 


## Definitions

There are many known ways of defining a __Boolean algebra__ or __Boolean lattice__. Here are just a few: 

* A Boolean algebra is a [[complement|complemented]] [[distributive lattice]]. 

* A Boolean algebra is a [[Heyting algebra]] $H$ satisfying the law of excluded middle, which means either 
$$\neg \neg = id: H \to H$$ 
or (equivalently) 
$$\forall_{x \in H} x \vee \neg x = \top$$

* A Boolean algebra is a [[lattice]] $L$ equipped with a function $\neg: L \to L$ satisfying 
$$a \wedge b \leq c \qquad iff \qquad a \leq \neg b \vee c$$


### Explicitly

There are even two explicit definitions: order-theoretic and algebraic.

A __Boolean lattice__ is a [[poset]] such that:

*  there is an element $\top$ (a [[top element]]) such that $x \leq \top$ always holds;
*  there is an element $\bot$ (a [[bottom element]]) such that $\bot \leq x$ always holds;
*  given elements $a$ and $b$, there is an element $a \wedge b$ (a [[meet]] of $a$ and $b$) such that $x \leq a \wedge b$ holds iff $x \leq a$ and $x \leq b$;
*  given elements $a$ and $b$, there is an element $a \vee b$ (a [[join]] of $a$ and $b$) such that $a \vee b \leq x$ holds iff $a \leq x$ and $b \leq x$;
*  given an element $a$, there is an element $\neg{a}$ (a [[complement]] of $a$) such that $a \wedge \neg{a} \leq \bot$ and $\top \leq a \vee \neg{a}$;
*  given elements $a$, $b$, and $c$, we have $a \wedge (b \vee c) \leq (a \wedge b) \vee (a \wedge c)$.

Although we don\'t say so, we can prove that $\top$, $\bot$, $a \wedge b$, $a \vee b$, and $\neg{a}$ are unique; this makes it more clear what the last two axioms actually mean.

Alternatively, a __Boolean algebra__ is a [[set]] equipped with elements $\top$ and $\bot$, binary operations $\wedge$ and $\vee$, and a unary operation $\neg$, satisfying these identities:

*  $a \wedge \top = a$,
*  $a \vee \bot = a$,
*  $a \wedge (b \wedge c) = (a \wedge b) \wedge c$,
*  $a \vee (b \vee c) = (a \vee b) \vee c$,
*  $a \wedge b = b \wedge a$,
*  $a \vee b = b \vee a$,
*  $a \wedge (a \vee b) = a$,
*  $a \vee (a \wedge b) = a$,
*  $a \wedge (b \vee c) = (a \wedge b) \vee (a \wedge c)$,
*  $a \wedge \neg{a} = \bot$,
*  $a \vee \neg{a} = \top$.

We can recover the poset structure: $a \leq b$ iff $a \wedge b = a$.


## Homomorphisms

Any [[lattice]] homomorphism automatically preserves $\neg$ and is therefore a Boolean algebra homomorphism.

Boolean algebras and Boolean algebra homomorphisms form a [[concrete category]] [[BoolAlg]].


[[!redirects Boolean algebra]]
[[!redirects Boolean algebras]]
[[!redirects Boolean lattice]]
[[!redirects Boolean lattices]]
[[!redirects boolean algebra]]
[[!redirects boolean algebras]]
[[!redirects boolean lattice]]
[[!redirects boolean lattices]]
