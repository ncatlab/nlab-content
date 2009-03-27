# Overview #

If $C$ is a [[locally small category]], then we say a [[functor]] 

$$F: C^{op} \to Set$$ 

is **representable** if it is [[natural isomorphism|naturally isomorphic]] to a [[hom-functor]] $\hom_C(-, c): C^{op} \to Set$. The object $c$ is determined uniquely up to isomorphism, and is called a **representing object** for $F$. 

+--{+ .query}
I am pretty unhappy that all entries related to limits, colimits and representable things at nlab say that the limit, colimit and representing functors are what normally in strict treatment are just the vertices of the corresponding universal construction. A representable functor is not a functor which is naturally 
isomorphic to Hom(-,c) but a *pair* of 
an object and such isomorphism! Similarly limit is the synonym for *limiting cone* (= universal cone), not just its vertex. Because if it were most of usages and theorems would not be true. For example, the notion and usage of creating limits under a functor, includes the words about the behaviour of the arrow under the functor, not only of the vertex. Definitions should be the collections of the data and one has to distinguish if the existence is really existence or in fact a **part of the structure**.--Zoran

[[Mike Shulman|Mike]]: I disagree (partly).  First of all, a functor $F$ *equipped with* an isomorphism $F\cong hom_C(-,c)$ is not a represent<b>able</b> functor, it is a represent<b>ed</b> functor, or a functor equipped with a representation.  A representable functor is one that is "able" to be represented, or _admits_ a representation.

Second, the page [[limit]] says "a limit of a diagram $F : D \to C$ ... is an object $lim F$ of $C$ _equipped with_ morphisms to the objects $F(d)$ for all $d \in D$..." (emphasis added).  It doesn't say "such that there exist" morphisms.  (Prior to today, it defined a limit to be a universal cone.)  It is true that one frequently speaks of "the limit" as being the vertex, but this is an abuse of language no worse than other abuses that are common and convenient throughout mathematics (e.g. "let $G$ be a group" rather than "let $(G,\cdot,e)$ be a group").  If there are any _definitions_ you find that are wrong (e.g. that say "such that there exists" rather than "equipped with"), please correct them!  (Thanks to your post, I just discovered that [[Kan extension]] was wrong, and corrected it.)

[[Zoran Skoda]] I fully agree, Mike that "equipped with" is just a synonym of a "pair". But look at entry for limit for example, and it is clear there that the limiting cone/universal cone and limit are clearly distinguished there and the term limit is used just for the vertex there. Unlike for limits where up to economy nobody doubt that it is a pair, you are right that many including the very MacLane representable take as existence, but then they really use term "representation" for the whole pair. Practical mathematicians are either sloppy in writing or really mean a pair for representable. Australians and MacLane use indeed word representation for the whole thing, but practical mathematicians (example: algebraic geometers) are not even aware of term "representation" in that sense, and I would side with them. Let us leave as it is for representable, but I do not believe I will ever use term "representation" in such a sense. For limit, colimit let us talk about pairs: I am perfectly happy with word "equipped" as you suggest. 

[[Mike Shulman|Mike]]: I'm not sure what your point is about [[limit]]s.  The definition at the beginning very clearly uses the words "equipped with."  Later on in the page, the word "limit" is used to refer to the vertex, but this is just the common abuse of language.

Regarding representable functors, since representations are unique up to unique isomorphism when they exist, it really doesn't matter whether "representable functor" means "functor such that there exists an isomorphism $F\cong hom_C(-,c)$" or "functor equipped with an isomorphism $F\cong hom_C(-,c)$."  (As long as it doesn't mean something stupid like "functor equipped with an object $c$ such that there exists an isomorphism $F\cong hom_C(-,c)$.")  In the language of [[stuff, structure, property]], we can say that the [[Yoneda embedding]] is [[full and faithful functor|fully faithful]], so that "being representable" is really a property, rather than structure, on a functor.
=--

Representability is one of the most fundamental concepts of category theory, with close ties to the notion of [[adjunction]] and to the [[Yoneda lemma]]. It is the crucial concept underlying the idea of [[universal property]]; thus for example crucial concepts such as "[[limit]]", "[[colimit]]", "[[exponential object]]", "[[Kan extension]]" and so on are naturally expressed in terms of representing objects. The concept permeates much of algebraic geometry and algebraic topology. 

# Definition #

More precisely, given a functor $F: C^{op} \to Set$ (also called a [[presheaf]] on $C$), a **representation** of $F$ is a specified natural isomorphism 

$$\theta: \hom_C(-, c) \stackrel{\sim}{\to} F$$ 

By the [[Yoneda lemma]], any such transformation $\theta$ (isomorphism or not) is uniquely determined by an element $\xi \in F(c)$. As above, the object $c$ is called a **representing object** (or often, **universal object**) for $F$, and the element $\xi$ is called a **universal element** for $F$. Again, it follows from the [[Yoneda lemma]] that the pair $(c, \xi)$ is determined uniquely up to unique isomorphism. 

Following the proof of the Yoneda lemma, representability means precisely this: given any object $x$ of $C$ and any element $\alpha \in F(x)$, there exists a unique morphism $f: x \to c$ such that the function $F(f)$ carries the universal element $\xi \in F(c)$ to $\alpha \in F(x)$. Such a dry formulation fails to convey the remarkable power of this concept, which can really only be appreciated through the myriad examples which illustrate it. 

# Examples #

## Example 1: limits ##

If $F:J\to C$ is a diagram in $C$, we can construct a diagram $\hom_C(-,F)$ in the [[functor category]] $Set^{C^{op}}$ as the composite of $F$ with the curried [[hom-functor]] $C\to\Set^{C^{op}}$ (the [[Yoneda embedding]]).  The object-wise [[limit]] of this diagram in [[Set]], that is, the functor $C^{op}\to\Set$ sending on object $x$ to the set which is the limit of the diagram $\hom_C(x,F):J\to\Set$, is representable iff the diagram $F$ has a limit in $C$; in fact, a representing object for that limit functor is exactly $\lim F$, and we obtain a natural isomorphism

$$\lim\hom_C(-,F)\cong\hom_C(-,\lim F).$$

### Sub-Example: Products ###

For an example in the case of the [[product]], let $c, d$ be objects of $C$, and consider the presheaf given by a product of [[hom-functor|hom-functors]]

$$\hom_C(-, c) \times \hom_C(-, d): C^{op} \to Set;$$ 

that is, the functor which takes an object $x$ of $C$ to the set $\hom_C(x, c) \times \hom_C(x, d)$. A product $c \times d$ is precisely a representing or universal object for this presheaf, where the universal element is precisely the pair of projection maps 

$$(\pi_c, \pi_d) \in \hom(c \times d, c) \times \hom(c \times d, d)$$ 

We leave it to the reader to check that the representability here means precisely that given a pair 
of maps 

$$(f, g) \in \hom(x, c) \times \hom(x, d)$$ 

there exists a unique element in $\hom(x, c \times d)$, denoted $langle f, g \rangle$, such that 

$$\pi_c \langle f, g \rangle = f \qquad \pi_d \langle f, g \rangle = g.$$

## Example 1 a: weighted limits ##

The above example has an important straightforward generalization.

Noticing that the limit over the functor $H : J \to Set$ is just the collection of [[cone]]s over $H$ whose tip is the point
$$
  lim H = [J,Set](\Delta pt, H)
$$ 
the above expression
$\lim\hom_C(-,F)$ can be rewritten equivalently as 
$[J,Set](\Delta pt, C(-,F(-)))$. Replacing in this expression the constant terminal functor $\Delta pt : J \to Set$ by any other functor leads to the notion of [[weighted limit]], as described there.

## Example 2: exponential objects ##

Suppose $C$ is a category which admits finite products; given objects $c, d$, consider the presheaf 

$$\hom_C(- \times c, d): C^{op} \to Set.$$ 

A representing or universal object for this presheaf is an [[exponential object]] $d^c$; the universal element 

$$e \in \hom_C(d^c \times c, d)$$ 

is a morphism called the **evaluation** map $eval: d^c \times c \to d$. 

## Example 3: classifying bundles ##

Consider a category $Top$ of 'nice' spaces (just to fix the discussion, let's say paracompact spaces, although this is a technical point), and a topological group $G$ therein, i.e., a group internal to $Top$. There is a presheaf 

$$G\Bund: Top^{op} \to Set$$ 

which assigns to each space $X$ the set of isomorphism classes of $G$-bundles over $X$, and assigns to each continuous map $f: X \to Y$ the function 

$$G\Bund(f): G\Bund(Y) \to G\Bund(X)$$ 

which carries a (class of a) $G$-bundle $E \to Y$ to the (class of the) pullback bundle $f^*E \to X$. It is well-known that the pullback construction is invariant with respect to homotopic deformations; that is, this presheaf descends to a functor on the [[homotopy category]], 

$$G\Bund: Ho_{Top}^{op} \to Set.$$ 

A **[[classifying space]]** $\mathcal{B}G$ is precisely a representing object for this functor; the universal element is the (isomorphism class of the) classifying $G$-bundle $[\pi: \mathcal{E}G \to \mathcal{B}G]$.

These general considerations are quite commonplace in algebraic topology, where they crop up for example in the connection between generalized cohomology theories and spectra; cf. Brown's representability theorem. 