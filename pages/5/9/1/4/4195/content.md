+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[coherence theorem]] and [[strictification theorem]] for [[monoidal categories]] may each take several forms. In [[Categories for the Working Mathematician]], [[Mac Lane]] shows (page 257 -- 260) how to derive coherence from strictification and conversely.

### Coherence theorems

1. Every "formal" diagram in a [[monoidal category]] made up of [[associators]] and [[unitors]] commutes.

1. Every diagram in a *free* monoidal category made up of associators and unitors commutes.

1. Every monoidal category is equivalent to an [[unbiased monoidal category]].

### Strictification theorems

1. The free monoidal category on some given data is equivalent to the free [[strict monoidal category]] on the same data.

1. Every monoidal category is monoidally equivalent to a [[strict monoidal category]].

1. The forgetful 2-functor $StrMonCat \to MonCat$ has a strict [[left adjoint]] and the components of the unit are equivalences in $MonCat$.

## Proofs

* [[Mac Lane's proof of the coherence theorem for monoidal categories]]

## Discussion ## 

(I plan to get back to this and make emendations, but for now I've just pasted in some discussion from the nForum -- Todd.) 

Most people, when they first hear about strictifications, imagine that strictifying a monoidal category is like taking a quotient, in order to identify associativities with identities. That's actually the wrong picture, and it leads to a lot of confusion. The right picture is that a monoidal category $M$ can be monoidally *embedded* in a strict monoidal category $M^{st}$, in which associativity and unit isomorphisms of $M$ are assembled into what Joyal calls "contractible networks", or [[clique|cliques]] (aka anaobjects). The cliques that so arise are then the objects of the strictification. 

So, for example, a 4-fold tensor product like $(a^b \otimes (b^c \otimes c^d)) \otimes d$ is a vertex in a clique which consists of all five ways of bracketing $a^b \otimes b^c \otimes c^d \otimes d$ and the groupoid of associativities between them. Or more precisely, it consists of the infinitely many such bracketings with units inserted (e.g., $((a^b \otimes I) \otimes (b^c \otimes c^d)) \otimes (I \otimes d)$), as objects of the groupoid generated by associativity and unit isomorphisms between them. By Mac Lane's coherence theorem ("all diagrams commute"), there is exactly one morphism between any two vertices in the clique, meaning that the groupoid is equivalent to a terminal groupoid, and therefore contractible.  

Formally, a *clique* in a category $C$ consists of a contractible groupoid $G$ and a functor $F: G \to C$. A *morphism* between two cliques $(G, F: G \to C)$, $(G', F': G' \to C)$ is a collection of morphisms $F(g) \to F'(g')$, where $(g, g')$ ranges over $Ob(G) \times Ob(G')$, making all triangles in sight commute. (In fact, by contractibility, any one of the $F(g) \to F'(g')$ uniquely determines all the rest.) To form the monoidal strictification $M^{st}$, we take as objects those cliques in the monoidal category $M$ which arise by application of the "all diagrams commute" formulation of Mac Lane's coherence theorem (which specifies the structure of the free monoidal category on one generator as a disjoint sum of contractible groupoids), and the morphisms in $M^{st}$ are defined to be morphisms of cliques. The precise description is laid out <a href="http://ncatlab.org/nlab/show/clique#monoidal_strictifications">here</a>, where it is indicated that the evident embedding $i: M \to M^{st}$ is an equivalence in $MonCat$. 

In any case, because $M$ is *embedded* in $M^{st}$, any diagram we are trying to prove commutative in $M$ is *physically there* in $M^{st}$, but any associativities and units in the diagram get absorbed into cliques, or rather: any such associativity is one of the components $F(g) \to F'(g')$ of, and uniquely determines, an identity morphism of cliques. Therefore any such associativity in $M$ is reinterpreted as an identity in $M^{st}$, and the diagram we are trying to prove commutative in $M$ uniquely generates a corresponding "larger" diagram of cliques in the strict monoidal category $M^{st}$. So it is enough to prove the diagram commutes when interpreted in a strict monoidal category: we can then interpret the result in $M^{st}$, and the original diagram in $M$, which is embedded in the clique diagram, is then automatically commutative as well. 

One may have to practice visualizing this before it all sinks in, but it's a tremendously potent principle.

## References

* {#MacLane63} [[Saunders Mac Lane]]. "Natural associativity and commutativity". Rice University Studies 49, 28-46 (1963). ([Rice Digital Scholarship Archive](https://scholarship.rice.edu/handle/1911/62865)) 

* [[Saunders Mac Lane]]. [[Categories for the Working Mathematician]] (Chapter 7).

* {#JoyalStreet} [[André Joyal]], [[Ross Street]], _Braided tensor categories_,  Adv. Math. 1993 ([pdf](http://web.science.mq.edu.au/~street/JS1.pdf))

* Paul Wilson, [[Dan Ghica]] and [[Fabio Zanasi]].  "String Diagrams for Strictification and Coherence".  *Logical Methods in Computer Science* 2024

See also section 5 of

* [[Saunders Mac Lane]], Topology and Logic as a Source of Algebra (Retiring Presidential Address), _Bulletin of the AMS_ 82:1, January 1976. ([euclid](https://projecteuclid.org/euclid.bams/1183537593))

* {#Schauenburg01} [[Peter Schauenburg]], *Turning Monoidal Categories into Strict Ones*, New York Journal of Mathematics **7** (2001) 257-265 &lbrack;[nyjm:j/2001/7-16](http://nyjm.albany.edu/j/2001/7-16.html), [eudml:121925](https://eudml.org/doc/121925)&rbrack;

## See also

- [[coherence and strictification for symmetric monoidal categories]]
- [[coherence theorem]]
- [[strictification theorem]]

[[!redirects coherence theorem for monoidal categories]]