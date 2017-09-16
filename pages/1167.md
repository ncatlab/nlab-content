
#Definition#

For $K : D \to Set$ a [[functor]], let $(* \darr K)$ be the [[comma category]] of elements $x \in K d$, let $Q: (* \darr K) \to D$ be the projection $(x \in K d) \mapsto d$ and let for each $a \in D$  the functor $\Delta_a: (* \darr K) \to D$ be the diagonal functor sending everything to the constant value $a$. 

The **Coyoneda lemma** is the statement that there is a natural isomorphism of [[functor category|functor categories]]

$$
[D,Set](K, D(a, -)) \cong [(*\darr K), D](\Delta_a, Q).
$$

#Remarks#

* See also [[Yoneda lemma]].

#References#

see p. 63 of 

* MacLane, [[Categories Work|Categories for the Working Mathematician]].