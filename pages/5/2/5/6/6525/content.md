
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

**Surreal numbers** (or Conway numbers, after John H. Conway) are a kind of [[numbers]] that originally arose in the context of [[Conway game|combinatorial games]], as a kind of generalized quantity for measuring strength of positions. The class of surreal numbers forms an ordered field in which any small ordered field may be embedded, so that the field of surreal numbers forms a universal field for expressing any set-bounded degree of infinite and infinitesimal quantities. Any ordinal number may be construed as a surreal number, and new surreal numbers may be defined from old ones by generalizing the notion of Dedekind cut. Surreal numbers are a very large extension of real numbers, where one may make sense of fanciful quantities such as 

$$(\omega^2 + 5\omega - 13)^{\frac1{3} - \frac{2}{\omega}} + \pi$$

The term "surreal number" was introduced by Donald Knuth, who wrote a short novel about a couple who check out from Western civilization and live on a remote beach in India and who, finding a mysterious engraved stone and with an abundance of time to spend on things besides food and sex, discover for themselves surreal numbers and their delightful properties. 

## Conway-style definitions 

The notions of Conway game and Conway number, as given by Conway in his book _On Numbers and Games_, are disarmingly simple-looking. Here is a Conway-style definition of game: 

* A game $G$ consists of a set of games called **left options** of $G$, and a set of games called **right options** of $G$. All games are constructed this way. 

The second sentence is a shorthand way of saying this is supposed to be a recursive or inductive definition: if a collection $G^L$ of left options and a collection $G^R$ is given, one can construct a game $G = \{G^L \vert G^R\}$. Games are built recursively, starting with $G = \{\emptyset \vert \emptyset\}$. 

Here is a Conway-style definition of number: 

* A number $x$ consists of a set $L_x$ of numbers and a set $R_x$ of numbers, under the condition that no member of $L_x$ is $\geq$ any member of $R_x$ 

followed immediately by a recursive definition of $\geq$: 

* $x \geq y$ if $y \geq x'$ is false for any $x' \in R_x$ and $y' \geq x$ is false for any $y' \in L_y$. 

Ultimately, each number $x$ is considered to be a (Dedekind) cut between the set of left options (which are 'below' $x$) and the set of right options (which are 'above' $x$). 

Equality of numbers is a derived notion: 

* $x = y$ is defined to mean $x \geq y$ and $y \geq x$. 

Finally, field operations on surreal numbers are defined recursively: 

* $x + y$ is defined by letting $L_{x+y}$ be the set $\{x' + y \vert x' \in L_x\} \cup \{x + y' \vert y' \in L_y\}$, and $R_{x+y}$ the set $\{x' + y \vert x' \in R_x\} \cup \{x + y' \vert y' \in R_y\}$; 

* $-x$ is defined by letting $L_{-x}$ be the set of negatives of elements of $R_x$, and $R_{-x}$ the set of negatives of $L_x$; 

* $x y$ is defined by letting $L_{x y}$ be the set 
$$\{x' y + x y' - x'' y'' \vert x', x'' \in L_x, y', y'' \in L_y\} \cup \{x' y + x y' - x'' y'' \vert x', x'' \in R_x, y', y'' \in R_y\},$$ 
and $R_{x y}$ be the set 
$$\{x' y + x y' - x'' y'' \vert x', x'' \in L_x, y', y'' \in R_y\} \cup \{x' y + x y' - x'' y'' \vert x', x'' \in R_x, y', y'' \in L_y\}.$$ 

The style of such definitions is familiar from [[material set theory]], where elements are conceived to be sets of elements, which themselves have elements, and so on, down to a bedrock established by a foundation axiom. In fact, games can be axiomatized as elements of a structure with two predicates $\in_L$, $\in_R$ satisfying some set-theoretic axioms. 

The definition of multiplication is the most involved. We can summarize it by saying that the left set gets contributions from like sets, and the right set gets contributions from opposite kinds. For example, $0 \cdot 1$ is $\{|\} \cdot \{0 | \emptyset\}$, so the left-hand contributions to the left set are

$$\emptyset \cdot \{0|\} + 0 \cdot \{0\} - \emptyset \cdot \{0\} = \emptyset + 0 \cdot \{0\} - \emptyset \cdot \{0\} = \emptyset.$$

The other contributions work out similarly: everything ends up being the empty set, so the answer is $\{\emptyset | \emptyset\} = 0$.

Conway motivates this definition from the observation that, if $x' \in L_x$ and $y' \in L_y$, then $x - x' \gt 0$ and $y - y' \gt 0$. And so, if multiplication makes any sense at all, we should have $(x - x')(y - y') \gt 0$ and thus $x y \gt x' y + x y' - x' y'$. Therefore, elements of this form should appear in $L_{x y}$. Following this kind of logic for the other possible combinations leads to the definition of multiplication given above.

## In constructive mathematics

The definition of $\geq$ for numbers as formulated by Conway leans heavily upon properties of negation, and in particular the classical [[principle of excluded middle]].  However, it can be made more constructive by defining $\lt$ separately from $\le$:

* A number $x$ consists of a set $L_x$ of numbers and a set $R_x$ of numbers, under the condition that every member of $L_x$ is $\lt$ every member of $R_x$.
* $x \leq y$ if $x' \lt y$ is true for any $x' \in L_x$, and $x \lt y'$ is true for any $y' \in R_y$.
* $x \lt y$ if there exists an $x'\in R_x$ such that $x'\le y$, or there exists a $y'\in L_y$ such that $x\le y'$.
* $x = y$ is defined to mean $x \le y$ and $y \le x$.

This approach works up to a point.  However, it encounters a problem in proving that multiplication is well-defined, i.e. that it respects equality.  We can prove that if $x\ge 0$ then $y\le z \Rightarrow x y \le x z$ and hence $y = z \Rightarrow x y = x z$, and that if $x\le 0$ then $y\le z \Rightarrow x y \ge x z$ and hence $y = z \Rightarrow x y = x z$; but without excluded middle we can't say that every $x$ is either $\ge 0$ or $\le 0$, so how can we conclude that $y = z \Rightarrow x y = x z$?  It is unknown whether there is a solution to this problem.

## Structural approach 

It is a routine matter to rewrite the definitions in a more structural fashion, say within [[ETCS]]. In outline, a game is a rooted [[tree]] with no infinite branches and equipped with a labeling of each edge by a symbol $L$ or $R$. The nodes are called **positions** of the game. The root is the initial position, and starting from any position, there are positions that a player named $Left$ may move to, and positions that the other player $Right$ may move to, according to the edge-labelings. Any sequence of moves proceeding from the initial position (and not necessarily alternating between $Left$ and $Right$) must eventually terminate, since there are no infinite branches. 

Each position has a definite depth $n$, where $n$ is the number of edges one must back-track through along the unique path that leads back to the initial position. A tree is thus an internal presheaf $X$ on the ordered set $\omega$, whose value at the initial object $0 \in \omega$ is terminal (occupied by the initial position), and where $X(n)$ is the set of positions at depth $n$. A move is a morphism in the corresponding category of elements of the presheaf, and moves are labeled by $L$ or $R$. 

In this set-up, the condition of no infinite branches plays the role of a foundation axiom, and inductive arguments tend to devolve upon the use of the principle of [[dependent choice]]. 

Numbers may be similarly elaborated within this context. The definition of $\geq$ on numbers is ultimately derived from a posetal reflection of a category of games (with strategies as morphisms), and the definition of addition of numbers is derived from a Day convolution product on the category of games. More information may be found at [[Conway game]]. 

## In homotopy type theory

In [[homotopy type theory]], the surreal numbers can be defined as a [[higher inductive type]], roughly following Conway's definition but imposing the "defined" notion of equality as the "actual" equality with an identification-constructor.  This can also be done constructively by separating $\lt$ from $\le$, as remarked above.  See chapter 11.6 of the [[HoTT Book]].

## In algebraic set theory

An axiomatic approach to surreal numbers analogous to the approach to sets and ordinals in [[algebraic set theory]] can be found in [Rangel-Mariano 19](#RM19).

## Properties of surreal numbers 

The surreal numbers form a large (i.e., proper-class size) [[real closed field]] with exponentiation. 

To some degree, and with appropriate caveats, one can do analysis and number theory on surreal numbers. We refer to Conway's book for more information. 

## Related pages

* [[ordinal number]]
* [[real number]]
* [[Hahn series]]
* [[infinitesimal]]
* [[∞-number]]
* [[Surreal space]]
* [[Surreal geometry]]

## References 

* John H. Conway, _On Numbers and Games_ ($2^{nd}$ edition), A.K. Peters, Ltd (2001). 

* [[Donald Knuth|Donald E. Knuth]], _Surreal numbers_, Addison-Wesley (1974) 

* The [[HoTT Book]], chapter 11.6.

* Dimi Rocha Rangel, Hugo Luiz Mariano, *An algebraic (set) theory of surreal numbers, I*, 2019, [arxiv](https://arxiv.org/abs/1911.12726)
 {#RM19}



[[!redirects surreal numbers]] 
