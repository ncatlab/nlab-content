
#Definition#

For $K : D \to Set$ a [[functor]], let $(* \darr K)$ be the [[comma category]] of elements $x \in K d$, let $\Pi: (* \darr K) \to D$ be the projection $(x \in K d) \mapsto d$ and let for each $a \in D$  the functor $\Delta_a: (* \darr K) \to D$ be the diagonal functor sending everything to the constant value $a$. 

The **Coyoneda lemma** is the statement that there is a natural isomorphism of [[functor category|functor categories]]

$$
[D,Set](K, D(a, -)) \cong [(*\darr K), D](\Delta_a, \Pi).
$$

#Outline of Proof#

A natural transformation $\phi: K \to D(a, -)$ assigns to each element $x \in K c$ an element $\phi_c(x) \in D(a, c)$, i.e., an arrow $\phi_c(x): a \to c$. We define a corresponding transformation $\psi: \Delta_a \to \Pi$ which assigns to each object $(c, x \in K c)$ in $(*\darr K)$ the morphism $\phi_c(x): a \to c = \Pi(c, x)$. It is easy to check that the naturality condition on $\phi$ corresponds to the naturality condition on $\psi$, and that the correspondence is bijective.   

#Remarks#

* See also [[Yoneda lemma]].

#References#

see p. 63 of 

* MacLane, [[Categories Work|Categories for the Working Mathematician]].