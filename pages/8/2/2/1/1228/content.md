<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


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

Under [[duality|abstract duality]] an [[end]] turns into a [[coend]], so a co-Yoneda lemma ought to be a similarly fundamental expression for $F(c)$ in terms of a [[coend]].

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

[[Mike Shulman|Mike]]: With tongue in cheek, I would say that there isn't any elegant way to see it, because it's not an elegant statement: it doesn't have any enriched analogue.  But it is an instance of the general fact that $W$-[[weighted limit|weighted]] colimits for any $Set$-weight $W:D\to Set$ can be computed as 'unweighted' colimits over the [[category of elements]] of $W$ (see section 3.4 of Kelly's book).

=--

# MacLane's co-Yoneda lemma#

In a brief uncommented exercise on p. 63 of 

* MacLane, [[Categories Work|Categories for the Working Mathematician]],

the following statement, which is atrributed to Kan, is called the **co-Yoneda lemma**.


For $D$ a [[category]], [[Set]] the [[category]] of [[set]]s, $K : D \to Set$ a [[functor]], let $(* \darr K)$ be the [[comma category]] of elements $x \in K d$, let $\Pi: (* \darr K) \to D$ be the projection $(x \in K d) \mapsto d$ and let for each $a \in D$  the functor $\Delta_a: (* \darr K) \to D$ be the diagonal functor sending everything to the constant value $a$. 

The **co-Yoneda lemma in the sense of Kan/MacLane** is the statement that there is a natural isomorphism of [[functor category|functor categories]]

$$
[D,Set](K, D(a, -)) \cong [(*\darr K), D](\Delta_a, \Pi).
$$

#Proof of the MacLane version of co-Yoneda#

## outline of an explicit proof ##

A natural transformation $\phi: K \to D(a, -)$ assigns to each element $x \in K c$ an element $\phi_c(x) \in D(a, c)$, i.e., an arrow $\phi_c(x): a \to c$. We define a corresponding transformation $\psi: \Delta_a \to \Pi$ which assigns to each object $(c, x \in K c)$ in $(*\darr K)$ the morphism $\phi_c(x): a \to c = \Pi(c, x)$. It is easy to check that the naturality condition on $\phi$ corresponds to the naturality condition on $\psi$, and that the correspondence is bijective.   


## a conceptual proof in terms of comma categories ##


[[Set]] classifies discrete fibrations, in the sense that a functor $G : D \to Set$ classifies the discrete [[fibration]]

$$
  Q : \Pi_G : El(G) \to D
$$

and natural transformations $\alpha : G \to F$ correspond to maps of fibrations 

$$
  El(G) \to El(f)
$$

i.e. functor which commute on the nose with the projections $\Pi_G$, $\Pi_F$ to the base category $D$).


This applies in particular to $F = hom(a,-)$. Notice the [[category of elements]] $El(hom(a,-))$ is the co-slice $(a \downarrow D)$, with its usual projection $\Pi$ to $D$.

However, the [[comma category]] $(a \downarrow D)$ is the "lax pullback" (really, the [[comma object]], the discussion at [[2-limit]]) appearing in

$$
  \array{
    (a \downarrow D) &\stackrel{\Pi}{\to}& D
    \\
    \downarrow &\Uparrow& \downarrow^{Id}
    \\
    * &\stackrel{a}{\to}& D
  }  
$$

and so a fibration map $El(G) \to (a \downarrow D)$ corresponds exactly to a lax square

$$
  \array{
    El(G) &\stackrel{\Pi_G}{\to}& D
    \\
    \downarrow &\Uparrow& \downarrow^{Id}
    \\
    * &\stackrel{a}{\to}& D
  }    
   \,.
$$


This yields the co-Yoneda lemma in the sense of MacLane's exercise.


#References#

The coYoneda lemma appears as a brief uncommented exercise on p. 63 of 

* MacLane, [[Categories Work|Categories for the Working Mathematician]],

where it is atributed to Kan.

A blog discussion which led to the creation of this entry is [here](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html#c023106).


[[!redirects Coyoneda lemma]]
[[!redirects coYoneda lemma]]