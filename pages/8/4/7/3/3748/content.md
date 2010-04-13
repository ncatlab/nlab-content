#Contents#
* automatic table of contents goes here
{:toc}

## Idea ## 

A club is a particular sort of [[doctrine]] or [[monad] on [[categories]], one which encapsulates the following frequently observed phenomenon: to describe [[free functor|free]] algebras $F(C)$ with respect to the monad, it frequently suffices to describe the free algebra $F(1)$ on the [[terminal category]], and then a certain "wreath product" gives the free algebra on $C$: 

$$F(C) \cong F(1) \int C$$

Examples of this phenomenon include the monad for [[monoidal categories]], [[symmetric monoidal categories]], [[braided monoidal categories]], categories with finite [[product]]s, [[closed category|closed symmetric monoidal categories]], and many others.

+--{: .query}
[[Mike Shulman]]: How do you get *closed* symmetric monoidal categories?  I thought that was one of the ones that Kelly couldn't handle because it involves extranatural transformations. 

[[Todd Trimble]]: You can get them, but there are points to watch. The real trouble to watch out in doctrines of "mixed variance" is the possibility of producing loops or "islands" in the process of composing extranaturals, but as it happens this doesn't occur in free smc categories. They do occur for compact closed categories, and that's fatal. The classical example is trace in compact closed categories, where the composite

$$1 \stackrel{\eta}{\to} c^* \otimes c \stackrel{\varepsilon}{\to} 1$$ 

is not a well-defined extranatural since it depends on $c$. 

Here are some details on clubs of mixed variance, which I was going to get to but here is a first pass. First, as you might expect, one replaces $\mathbf{P}$ below by a category $\mathbf{G}$ enriched in pointed sets whose objects are finite signed sets and whose non-basepoint morphisms are oriented 1-cobordisms. Let's say that two morphisms in $\mathbf{G}$ have a "defined" composition if no islands are produced, else their composition is taken to be the basepoint. Now let $F(1)$ be the free smc category on one generator. There is a "graph functor" $\Gamma: F(1) \to \mathbf{G}$ which takes a morphism  of $F(1)$ to its extranaturality graph. The crucial observation (and it's a bit nontrivial; the proof relies on a cut-elimination theorem) is that no basepoint morphism lies in the image of $\Gamma$, i.e., no islands can occur in formal compositions for this doctrine.

In cases like that, the basic club idea will work. Given a category $C$, the free smc category $F(C)$ has the expected objects given by formal iterated applications of hom and tensor to objects of $C$. A morphism is given by a morphism of $F(1)$ together with a labeling of the oriented edges of its underlying graph (an oriented 1-cobordism) by morphisms of $C$. Then, you compose morphisms of this "wreath product" in the obvious way, composing the morphism-labels of edges in 1-cobordisms as they get pasted together. 

It should also be mentioned (I'm sure you know this) that in such mixed variance cases, even if there are no islands in formal compositions, the result is merely a monad on $Cat$, not a 2-monad. On the other hand, you do get a 2-monad if you restict to categories, functors, and natural isomorphisms.

[[Mike Shulman]]: Ah, right, thanks.  Now I remember how Kelly dealt with graphs in that way by just throwing away the "bad composites".  I must have forgotten about it because I thought it was so weird.  (-:  Is that sort of club also a generalized operad for some cartesian monad on $Cat$? 

[[Todd Trimble]]: I'm pretty sure that it's a cartesian monad on $Cat$, and actually I don't know any real examples of Kelly's clubs which aren't.
=--

Clubs were introduced by [[Max Kelly], and are akin in spirit to [[operad|operads]].  In fact, most types of clubs are a special case of [[generalized multicategories|generalized operads]].

## Clubs over the permutation category 

### Action by substitution product

Let $\mathbf{P}$ be the category of finite sets $[n] = \{1, \ldots, n\}$ (including the empty set $[0]$) and permutations between them, and let $Cat$ be the category of small categories. We define a "wreath product" action of the category $Cat/\mathbf{P}$ on $Cat$, 

$$\circ: Cat/\mathbf{P} \times Cat \to Cat$$ 

taking a pair $(\Gamma: C \to \mathbf{P}, D)$ to the category whose objects are tuples 

$$(c; d_1, \ldots, d_n)$$

with $c \in Ob(C)$, $d_i \in Ob(D)$, and $\Gamma(c) = [n]$. A morphism is a tuple 

$$(f; g_1, \ldots, g_n)$$ 

consisting of a morphism $f: c \to c'$ in $C$ and morphisms $g_i: d_i \to d_{\Gamma(f)(i)}'$ in $D$, composed in the obvious way. 

This generalizes the standard notion of wreath product: given a group $G$ and a permutation representation, i.e., a homomorphism $\gamma: G \to Aut([n]) \hookrightarrow \mathbf{P}$, and given a group $H$, the wreath product is defined to be the semidirect product

$$G \int H = G \ltimes H^n$$ 

with the action of $G$ on $H^n$ induced from the action on $[n]$. 

Another, more abstract, way to describe this substitution product is as follows: there is a [[cartesian monad]] $T$ on $Cat$ whose algebras are symmetric strict monoidal categories, and we have $\mathbf{P} = T 1$, where $1$ is the [[terminal category]].  The substitution product $\Gamma \circ D$ can then be described as the following pullback in $Cat$.
$$\array{\Gamma \circ D & \overset{}{\to} & T D\\
  \downarrow && \downarrow^{T !}\\
  C & \underset{\Gamma}{\to} & T 1 & = \mathbf{P}}$$


### Substitution product as monoidal product

We describe how the substitution action $\circ$ lifts to a self-action denoted by the same symbol:

$$\circ: Cat/\mathbf{P} \times Cat/\mathbf{P} \to Cat/\mathbf{P}$$ 

To start, given a pair $(\Gamma: C \to \mathbf{P}, \Delta: D \to \mathbf{P})$, the domain of $\Gamma \circ \Delta$ is the category $\Gamma \circ D$ described above. The functor 

$$\Gamma \circ \Delta: \Gamma \circ D \to \mathbf{P}$$ 

sends an object $(c; d_1, \ldots, d_n)$ to $\sum_i \Delta(d_i)$. 

The effect of $\Gamma \circ \Delta$ on morphisms $(f; g_1, \ldots, g_n)$ may be summarized as "substituting the permutations $\Delta(g_i)$ into the permutation $\Gamma(f)$". To describe this more precisely, we give a little preface. The hom-set $\mathbf{P}([n], [n]) = Aut(n)$ of permutations on $n$ may be identified with the set $Lin(n)$ of total (or linear) orders on $[n]$, if we identify the identity element with the standard order on $\{1, 2, \ldots, n\}$. The sets $Aut(n) = Lin(n)$ are components of an [[operad]] $Lin$ where the operadic multiplication 

$$\mu(n; k_1, \ldots, k_n): Lin(n) \times Lin(k_1) \times \ldots \times Lin(k_n) \to Lin(k_1 + \ldots + k_n)$$ 

takes a linear ordering of $n$ linearly ordered sets of and produces the evident linear ordering on the disjoint sum of the sets. 

Then, given a morphism $(f; g_1, \ldots, g_n)$ in $\Gamma \circ D$, we define 

$$(\Gamma \circ \Delta)(f; g_1, \ldots, g_n) \stackrel{def}{=} \mu(n; k_1, \ldots, k_n)(\Gamma(f), \Delta(g_1), \ldots \Delta(g_n))$$ 

Given the abstract description above of the substitution product in terms of the cartesian monad $T$, the functor $\Gamma \circ \Delta$ can be described as the composite
$$ \Gamma \circ D \to T D \overset{T \Delta}{\to} T T 1 \overset{\mu_1}{\to} T 1  = \mathbf{P}$$
where $\mu\colon T T \to T$ is the multiplication of the [[monad]] $T$.

The substitution product thus indicated, 

$$\circ: Cat/\mathbf{P} \times Cat/\mathbf{P} \to Cat/\mathbf{P},$$ 

is the product for a [[monoidal category]] structure on $Cat/\mathbf{P}$. The monoidal unit is the functor $I: 1 \to \mathbf{P}$ which names the 1-element set.  Abstractly, we can observe that the cartesian monad $T$ induces a [[pseudomonad]] on the [[bicategory]] $Span(Cat)$ of spans in $Cat$, which has a [[Kleisli category|Kleisli bicategory]] $Span(Cat)_T$ in which a 1-cell $A\to B$ is a span $A \leftarrow X \to T B$ in $Cat$.  We then have
$$ Cat/\mathbf{P} \simeq Cat / (1 \times T 1) \simeq Span(Cat)_T (1, 1) $$
and the monoidal structure above is that induced from the bicategory composition in $Span(Cat)_T$.

Under this monoidal product, the substitution action indicated earlier, 

$$\circ: Cat/\mathbf{P} \times Cat \to Cat,$$ 

carries a structure of [[actegory]] over the monoidal category $Cat/\mathbf{P}$, in the sense that there is a coherent associativity 

$$(\Gamma \circ \Delta) \circ E \cong \Gamma \circ (\Delta \circ E)$$ 

for $Gamma: C \to \mathbf{P}$, $\Delta: D \to \mathbf{P}$, and a category $E$, and similarly coherent left and right unit isomorphisms. 

### Clubs over $\mathbf{P}$

**Definition:** A **club** over $\mathbf{P}$ is a monoid in the monoidal category $(Cat/\mathbf{P}, \circ, I)$.  By the abstract characterization above, this is equivalent to a [[monad]] in the bicategory $Span(Cat)_T$ on the object $1$, or equivalently a $T$-[[generalized multicategory|operad]] in the sense of Leinster.

A club over $\mathbf{P}$ induces (via the actegory structure) a 2-monad on $Cat$, and an algebra over the club is an algebra for this monad. That is, an **algebra** over a club $C$ is a category $D$ together with an action $m: C \circ D \to D$ compatible in the usual way with the monoid structure on $C$.

Given a club structure on $\Gamma: C \to \mathbf{P}$, we think of the objects $c$ as formal operations of arity $n = \Gamma(c)$. An algebra $D$ over $C$, $m: C \circ D \to D$, gives in effect an interpretation of each $c$ of arity $n$ as an actual operation $D^n \to D$. 

The free $C$-algebra over a category $D$ is just $C \circ D$. For the free algebra over the terminal category $1$, notice that 

$$C \circ 1 \cong C$$ 

(strictly speaking, the $C$ on the left is a category over $\mathbf{P}$ and the $C$ on the right is just the category). Thus, in a manner of speaking, the free algebra generated by $D$ is obtained by wreathing the free algebra generated by $1$ with $D$, as adumbrated in the idea section above. 

#### Examples: 

* The identity $1_{\mathbf{P}}: \mathbf{P} \to \mathbf{P}$ carries a club structure. The multiplication $\mu$ of the club, on the object level, is given by the assignment
$$(n; k_1, \ldots, k_n) \mapsto k_1 + \ldots + k_n$$ 
and on morphisms, it is given by the operad structure on $Aut(n) = Lin(n)$ discussed above. Algebras over this club are symmetric (strict) monoidal categories. Algebras in the "pseudo" sense over the induced 2-monad on $Cat$ are symmetric monoidal categories. 

* Let $\mathbf{B}$ be the [[braid category]], equipped with the usual forgetful functor $\Gamma: \mathbf{B} \to \mathbf{P}$. The club mutliplication, at the level of morphisms, is "substitution" of $n$ braids into a braid on $n$ elements. Pseudo-algebras over the induced 2-monad on $Cat$ are braided monoidal categories. 

* Let $C$ be any (permutative) operad valued in $Set$, with underlying species $\mathbf{P} \to Set$. Then category of elements gives a functor $\Gamma: El(C) \to \mathbf{P}$, and this carries a club structure induced from the operad structure on $C$. In this way, clubs generalize operads.  In fact, operads in $Set$ can be identified with those clubs for which the functor $\Gamma\colon C\to \mathbf{P}$ is a [[discrete fibration]].

## Clubs over finite sets 
