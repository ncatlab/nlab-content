#Idea#

The _co-Yoneda lemma_ is a statement which is related by [[duality]] to the [[Yoneda lemma]]. 

# Definition #

Recall that the [[Yoneda lemma]] says that for $C$ a $V$-[[enriched category]], $F : C^{op} \to V$ a $V$-valued [[presheaf]] on $C$ and $c \in C$ an [[object]] of $C$, there is a natural [[isomorphism]] in $V$

$$
  [C^{op},V](C(-,c), F) \simeq F(c)
  \,.
$$

Using the definition of the [[enriched functor category]] on the left in terms of an [[end]], this reads

$$
  \int_{c' \in C} V(C(c',c), F(c')) \simeq F(c)
  \,.
$$

In this form the Yoneda lemma is also referred to as [[Yoneda reduction]].

Under [[duality|abstract duality|]] an [[end]] turns into a [[coend]], so a co-Yoneda lemma ought to be a similarly fundamental expression for $F(c)$ in terms of a [[coend]].

The natural candidate is the statement that **every [[presheaf]] is a [[colimit]] of [[representable functor|representables]]** which may be stated as

$$
  F(c) \simeq \int^{c' \in C} C(c,c')\otimes F(c')
$$

hence

$$
  F(-) \simeq \int^{c' \in C} Y(c')\otimes F(c')
  \,,
$$

where $Y$ denotes the [[Yoneda embedding]]. In [[module]] language (...I forget which entry gives the discussion of this...) this reads

$$
  F(c) \simeq C(c,-)\otimes_C F
  \,.
$$

This statement we call the **co-Yoneda lemma**.

Yet another way to state this is as a [[colimit]] over the [[comma category]] $(Y,F)$, for $Y$ the [[Yoneda embedding]]:

$$
  F \simeq colim_{(U \to F) \in (Y,F)} Y(U)
  \,.
$$

+-- {: .query}

[[Urs Schreiber|Urs]]: what is, generally, a good elegant way to see the relation between the expression of [[Kan extension]] in terms of (co)ends and in terms of (co)limits over comma categories. Currently at [[Kan extension]] only the latter formula is discussed.

=--

# MacLane's co-Yoneda lemma#

In a brief uncommented exercise on p. 63 of 

* MacLane, [[Categories Work|Categories for the Working Mathematician]],

the following statement, which is atributed to Kan, is called the **co-Yoneda lemma**.


For $D$ a [[category]], [[Set]] the [[category]] of [[set]]s, $K : D \to Set$ a [[functor]], let $(* \darr K)$ be the [[comma category]] of elements $x \in K d$, let $\Pi: (* \darr K) \to D$ be the projection $(x \in K d) \mapsto d$ and let for each $a \in D$  the functor $\Delta_a: (* \darr K) \to D$ be the diagonal functor sending everything to the constant value $a$. 

The **coYoneda lemma** is the statement that there is a natural isomorphism of [[functor category|functor categories]]

$$
[D,Set](K, D(a, -)) \cong [(*\darr K), D](\Delta_a, \Pi).
$$

#Outline of Proof#

The best proof is probably the one described [here](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html#c023131).

A natural transformation $\phi: K \to D(a, -)$ assigns to each element $x \in K c$ an element $\phi_c(x) \in D(a, c)$, i.e., an arrow $\phi_c(x): a \to c$. We define a corresponding transformation $\psi: \Delta_a \to \Pi$ which assigns to each object $(c, x \in K c)$ in $(*\darr K)$ the morphism $\phi_c(x): a \to c = \Pi(c, x)$. It is easy to check that the naturality condition on $\phi$ corresponds to the naturality condition on $\psi$, and that the correspondence is bijective.   

#References#

The coYoneda lemma appears as a brief uncommented exercise on p. 63 of 

* MacLane, [[Categories Work|Categories for the Working Mathematician]],

where it is atributed to Kan.

A blog discussion which led to the creation of this entry is [here](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html#c023106).