In a [discussion](http://www.mta.ca/~cat-dist/catlist/1999/atcat) with Vaughan Pratt on the categories mailing list, Peter Freyd gave a very sharp description of the commonalities and differences between Abelian categories and Toposes (or, in the first place, between abelian categories and pretoposes), by introducing a finitely axiomatized theory of "AT categories". As it turns out, this theory embodies the commonalities with such precision that every AT category splits as a product of an [[abelian category]] and a [[pretopos]]. 

Remarkably, the properties in common are basically exactness conditions, and the sharp dichotomy between abelian categories and pretoposes can be concentrated solely in the behavior of the initial object. 


## Definition

Freyd introduces some baseline assumptions on the categories in question: 

* Finite completeness, 

* Presence of an initial object, 

* Pushouts for pairs of arrows one of which is monic, 

* Pushouts for kernel pairs

Each of these assumptions obtains in any abelian category and in any pretopos. 

Most of the AT axioms Freyd introduces can be phrased directly in terms of such limits and colimits, and these axioms have a simple logical structure: they are just [[Horn theory|Horn clauses]]. This may look like a side comment for logicians, but it may well signal that Freyd intends to invoke, if pressed for details of proofs, one of a battery of representation theorems (such as the representation theorem for regular categories) whose precise expressions involve Horn clauses. 

Anyway, to follow what Freyd is saying here a bit: by making choices for each such universal construction, categories satisfying these assumptions can be considered models of a suitable essentially algebraic theory. In any case, each of these baseline assumptions can be turned into predicates (e.g., "$(p, q)$ is a pushout pair for pairs of arrows $(f, g)$" is a predicate $P(p, q; f, g)$ for a first-order theory of categories with these baseline assumptions), and the majority of axioms Freyd writes down are expressible as Horn clauses in such predicates. 

The sharp dichotomy which separates A from T is concentrated in the following definition: 

+-- {: .un_def}
######Definition
Let $0$ be the initial object, and let $\pi_1: 0 \times X \to 0$, $\pi_2: 0 \times X \to X$ be the two product projections. We say $X$ is of **type T** if $\pi_1$ is an isomorphism, and **type A** if $\pi_2$ is an isomorphism.
=--

A pretopos will turn out to be precisely an AT category in which every object is of type T, and an abelian category will turn out to be an AT category where every object is of type A. 

Now here come the AT exactness axioms. Again, each of them is satisfied in every abelian category and in every pretopos, and part of Freyd's point is that any exactness axiom satisfied in both classes of categories is a logical consequence of this set of axioms. Freyd's remarks are included in parentheses. 

1. The category is an effective regular category. ("Yes this can be stated as universal Horn conditions on pullbacks and the special pushouts mentioned
above.")

1. The arrow $0 \to 1$ is monic. ("Note that it follows that all maps from $0$ are monic.")

1. If $i: A \to C$ is monic, then any pushout square 
$$\array{
A & \stackrel{i}{\to} & C \\
\downarrow & & \downarrow \\
B & \to & D
}$$
is also a pullback. A square that is simultaneously a pushout and a pullback will be called a "dolittle square". 

1. Applying the functor $0 \times -$ to the previous dolittle square, the result is again a dolittle square. ("Note that binary coproducts therefore exist and are disjoint." See lemma 1 below.) 

1. If $f: B \to 0 \times C$ is epic and
$$\array{
A & \to & B \\
\downarrow & & \downarrow f \\
0 & \to & 0 \times C
}$$
is a pullback, then it's a dolittle square.

1. If the squares in
$$\array{
A & \to & C & \leftarrow & B \\
\downarrow & & \downarrow & & \downarrow \\
D & \to & E & \leftarrow & E
}$$
are pullbacks and if $D \to F \leftarrow E$ is a coproduct diagram, and if all the objects in the squares are type T, then $A \to C \leftarrow B$ is also a coproduct diagram.  

1. Define a functor $T$ by the pushout diagram 
$$\array{
0 \times X & \stackrel{\pi_1}{\to} & 0 \\
\pi_2 \downarrow & & \downarrow \\
X & \to & T X
}$$
Then $T$ preserves pullbacks. 

1. Given a morphism $f: X \to Y$, if $T f$ and $0 \times f$ are isomorphisms, then so is $f$. 

We'll add some more axioms in a bit, but here may be a good point to take stock and prove some results. 

+-- {: .un_prop}
######Proposition
For any $X$ the unique map $0 \to X$ is monic. 
=--

+-- {: .proof}
######Proof
By axiom 2, the map $0 \to 1$ is monic. The pullback-preserving functor $- \times X$ preserves monos, so 

$$0 \times X \stackrel{! \times 1_X}{\to} 1 \times X \cong X$$

(which is just the second projection $\pi_2: 0 \times X \to X$) is monic. The unique map $0 \to 0 \times X$ is monic since it has a retraction $\pi_1: 0 \times X \to0$. The result follows. 
=-- 

+-- {: .un_prop}
######Proposition
Binary coproducts exist. 
=-- 

+-- {: .proof} 
######Proof
Because we can take the pushout of a pair of monos $0 \to X$, $0 \to Y$. 
=-- 

+-- {: .un_prop}
######Proposition
Coproducts are disjoint. 
=-- 

+-- {: .proof}
######Proof
Hm, I'm a bit stuck on showing that the coprojections are monic; does this follow from axiom 3 in some tricky way, maybe in conjunction with effective regularity? The other bit, that the pullback of the two coprojections is initial, is obvious from axiom 3. 
=-- 

+-- {: .un_lem}
######Lemma
An object is of type A if and only if there exists a map to $0$. 
=-- 

+-- {: .proof}
######Proof
If $X$ is of type A, then we clearly have $X \cong 0 \times X \stackrel{\pi_1}{\to} 0$. Conversely, suppose there exists $p: X \to 0$. Note that since $0 \to 1$ is monic, there is at most one map $Y \to 0$ for any object $Y$. It follows quickly that maps $Y \to X$ are in natural bijective correspondence with maps $Y \to X \times 0$, so that $X \cong X \times 0$ by the Yoneda lemma.
=--



From this lemma, it follows that the full subcategory of type A objects in an AT category $C$ is equivalent to the category $C/0$, which is the category of coalgebras for the functor $A(X) = 0 \times X$. Hence the category of type A objects is coreflective. 

+-- {: .un_lem}
######Lemma
Objects of type A are closed under products, coproducts, subobjects, and quotient objects. Therefore they give a full subcategory that is an AT category, in particular an effective regular category.
=--

+--{: .un_lem}
######Lemma
The category of type A objects is $Ab$-enriched (note: this is a property, not a structure on a category). 
=--

+--{: .un_thm}
######Theorem
The category of type A objects is an abelian category. 
=--

+-- {: .proof}
######Proof
An abelian category is the same thing as an effective regular $Ab$-enriched category (see Categories and Allegories, section 1.59). Now combine the previous two lemmas. 
=--

+-- {: .un_lem}
######Lemma
If $A$ is type A and $T$ is type T, then there exists exactly one map $A \to T$. Type T objects are characterized by this property. 
=-- 

+-- {: .proof}
######Proof
There is exactly one morphism $A \to 0$. Hence morphisms $A \to T$ are in bijection with maps $A \to 0 \times T \cong 0$, of which there is exactly one. For the second statement, use the fact that...
=-- 

+-- {: .un_prop}
######Proposition
The full subcategory of objects of type T is closed under products, coproducts, subobjects, and quotient objects

+-- {: .un_thm}
######Theorem
The full subcategory of objects of type T is a pretopos. 
=--

+-- {: .proof}
######Proof
One of our earlier results was that coproducts were disjoint, and one of the AT axioms above says that coproducts are universal. Hence an AT category is extensive; it is also effective regular, hence a pretopos. 
=-- 



[[!redirects AT category]]
[[!redirects AT categories]]
[[!redirects AT-category]]
[[!redirects AT-categories]]
