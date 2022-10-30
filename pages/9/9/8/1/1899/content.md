
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Tall--Wraith monoids
* table of contents
{: toc}

## Idea

Given an [[algebraic theory]] $V$, a $V$-algebra is a model of $V$ in the category $Set$.  A _Tall--Wraith $V$-monoid_ is _the kind of thing that acts on $V$-algebras_.  


## Definition

+-- {: .num_definition #twmonoid}
###### Definition
Let $V$ be an [[algebraic theory]] and let $V Alg$ be the category of models of this theory in $Set$.  Then a **Tall--Wraith $V$-monoid** is a [[monoid|monoid object]] in the category of co-$V$-objects in $V Alg$.   
=--

To see why these are _what acts on $V$-algebras_ one needs to understand what a co-$V$-object in $V Alg$ actually is.
A co-$V$-object in some category $D$ is a [[representable functor|representable covariant functor]] from $D$ to $V Alg$.  To give a particular $D$-object, $d$, the structure of a co-$V$-object is to give a lift of the $Set$-valued $Hom$-functor $D(d,-)$ to $V Alg$.
Thus a co-$V$-object in $V Alg$ is a representable covariant functor from $V Alg$ to itself.

One can therefore consider composition of such representable covariant functors.
The main result of this can be simply stated:

+-- {: .num_proposition #repcomp}
###### Proposition
The composition of representable covariant functors $V Alg \to V Alg$ is again representable.
=--

This is a basic result in general algebra, and is not stated here in its full generality.

An almost corollary of this is that the category of representable covariant functors from $V Alg$ to itself is monoidal (the "almost" refers to the fact that you have to show that the identity functor is representable, but this is not hard).

Thus for two co-$V$-algebra objects in $V$, say $R_1$ and $R_2$, there is a product $R_1 \odot R_2$ and a natural isomorphism

$$
Hom_V(R_1 \odot R_2,A) \cong Hom_V(R_1, Hom_V(R_2,A))
$$

for any $V$-algebra, $A$.

A **Tall--Wraith $V$-monoid** is thus a triple $(P,\mu,\eta)$ with $\mu : P \odot P \to P$ and $\eta : I \to P$ (where $I$ is the free $V$-algebra on one element --- this represents the identity functor), satisfying the obvious coherence diagrams.
An action of $P$ on a $V$-algebra, say $A$, is then a morphism $\rho : P \odot A \to A$ again satisfying certain coherence diagrams.

Ah, but I have not told you what $P \odot A$ is!
At the moment, one can take the "product" of two co-$V$-algebra objects in $V Alg$ but now I want to take the product of a co-$V$-algebra object with a $V$-algebra.
How do I do this?
I do this by observing that a $V$-algebra is a _co-$Set$-algebra object in $V Alg$_!
That's a complicated way of saying that $V$ represents a covariant functor $V Alg \to Set$.
Precomposing this with the functor represented by $P$ yields again a covariant functor $V Alg \to Set$.
This is again representable and we write its representing object $P \odot A$.

As an aside, we note a consequence.  As we've seen, the category of co-$V$-algebra objects in $V$ is a monoidal category, with the tensor product $\odot$.  Now we're seeing this monoidal category [[action|acts]] on the category of $V$-algebras.   Indeed, it acts on the categories of $V$-algebra and co-$V$-algebra objects in a reasonably arbitrary base category.

One postscript to this is that although the category of co-$V$-algebra objects in $V Alg$ is not a variety of algebras, for a specific Tall--Wraith $V$-monoid $P$, the category of $P$-modules _is_ a variety of algebras.


## Examples

* If $V$ is the theory of [[commutative ring|commutative unital rings]], a $V$-algebra is a commutative unital ring, and the corresponding sort of Tall--Wraith $V$-monoid is called a [[biring]].  

* If $V$ is the theory of [[commutative algebra|commutative associative algebras]] over a [[field]] $k$, then a $V$-algebra is a commutative associative algebra over $k$, and the corresponding sort of Tall--Wraith $V$-monoid is called a [[plethory]].

* If $V$ is the theory of [[abelian group|abelian groups]], than a $V$-algebra is an abelian group, and the corresponding sort of Tall--Wraith $V$-monoid is a [[ring]].

  To understand the last example, we need to think about _co-abelian group objects in the category of abelian groups_.  Abstractly, such a thing is an abelian group object [[internalization|internal to]] $AbGp^{op}$ (though this picture gets the morphisms the wrong way around; in full abstraction then the category of co-abelian group objects in $AbGrp$ is the _opposite_ category of the category of abelian group objects in $AbGrp^{op}$). Concretely, such a thing is an abelian group $A$ together with group homomorphisms

  $$
  \begin{aligned}
  \mu &: A \to A \coprod A, \\
  \epsilon &: A \to I \\
  \iota &: A \to A
  \end{aligned}
  $$

  where $I$ is the initial object in the category of abelian groups.  These homomorphisms must satisfy certain laws: just the abelian group axioms written out diagrammatically, with all the arrows turned around.

  In fact, $I = \{0\}$.  Thus $\epsilon$ is forced to be the map that sends everything to $0$: we have no choice here.

  We also have that $A \coprod A = A \oplus A$.
That means that for $a \in A$, $\mu(a) = (a_1,a_2)$ for some $a_1, a_2 \in A$.  Now, one of the laws says that $\epsilon$ is a counit for $\mu$. This means that $(\epsilon \oplus 1) \mu = 1$ and similarly for $1 \oplus \epsilon$. Thus $a_1 = a_2 = a$ and $\mu$ is the diagonal map.  So, we have no choice here either.

  The diagram for $\iota$ (representing the inverse map) is a little more complicated.  As $I$ is the initial object in $AbGrp$, there is a unique morphism $I \to A$ (inclusion of the zero).  Composing this with $\epsilon$ yields a morphism $A \to A$ which maps every element to the zero in $A$.  Using $\mu$ and $\iota$ we can construct another morphism $A \to A$ as

  $$
  A \overset{\mu}\rightarrow A \coprod A \overset{1 \coprod \iota}\rightarrow A \coprod A \overset{\Delta^c}\rightarrow A
  $$

  where $\Delta^c$ is the co-diagonal.  The relations for abelian groups say that this morphism must be the same as the zero morphism $A \to A$.  Using the fact that $A \coprod A \cong A \oplus A$ and that $\mu$ is the diagonal, this says that $a + \iota(a) = 0$.  Hence, by the uniqueness of inverses for abelian groups, $\iota(a) = -a$.

  Thus _if_ $(A, \mu, \iota, \epsilon)$ is a co-abelian group object in $AbGrp$ then $\mu$ is the diagonal, $\iota$ the inverse from abelian groups, and $\epsilon$ the zero morphism.

  However, that is still not quite the same as saying that $(A, \mu, \iota, \epsilon)$ is a co-abelian group object in $AbGrp$.  Certainly, $(A, \mu, \epsilon)$ is a co-commutative co-monoid object in $AbGrp$ since $\mu$ is the diagonal, which is automatically co-commutative and co-associative, and $\epsilon$ the zero map, which is the co-unit for the diagonal.  What remains is to fit $\iota$ into the structure.

  The first issue is that $\iota$ is not _automatically_ a morphism in $AbGrp$.  That is to say, when defining an algebraic theory then the operations are defined on the underlying objects.  It is a consequence of the relations of abelian groups that the operations lift to morphisms of abelian groups (algebraic theories where this happens for all operations are sometimes called _commutative_).  Thus $\iota$ is a morphism of abelian groups and so $(A, \mu, \iota, \epsilon)$ is a co-commutative co-monoid with an extra unary co-operation.  In fact, it is an involution from the relations for abelian groups.

  The final relation is that $\iota$ is the inverse for $\mu$.  The relation that $\iota$ is the inverse for addition (let us write it as, say, $\alpha$) is that

  $$
  A \overset{\Delta}\rightarrow A \times A \overset{1 \times \iota}\rightarrow A \times A \overset{\alpha}\rightarrow A
  $$

  is the zero map $A \to I \to A$.  This is precisely the relation that $\iota$ is the inverse for $\mu$ since we have the following identifications: $\mu = \Delta$, $A \coprod A = A \times A$, and $\Delta^c = \alpha$.  Also, $\epsilon = 0$ and $\eta : I \to A$ is the initial morphism in $AbGrp$.

  Thus the fact that $\iota$ is the inverse for the diagonal+zero co-monoidal structure is due to the fact that $\iota$ is the inverse for $(\alpha,\eta)$ and $\alpha : A \oplus A \to A$ is the co-diagonal in $AbGrp$ and $\eta : I \to A$ is the unit.

  +-- {: .query}
  [[Andrew Stacey]]: I've deleted the original query boxes.  The above now contains the all the details, but I suspect that there may be neater ways of putting it and other ways to see it.  If so, these are certainly worth discussing but I think that the above is a new launching point for discussion.  If anyone is interested in the discussion that led up to that point then they can look in the history but I don't think that that is necessary to discuss the above.

  And remember what Tony Blair said: _Indentation, Indentation, Indentation_.
  =--
 
  It is part of the general theory that the category of co-$V$-objects in $V$ is monoidal (though not, in general, symmetric). For details on this see _The Hunting of the Hopf Ring_, referred to belelow.  This monoidal structure for abelian groups turns out to be the tensor product.

  Thus a Tall--Wraith monoid for abelian groups is actually an ordinary monoid in the category of abelian groups: in other words, a [[ring]]!


## References

* D. Tall, [[Gavin Wraith|G. Wraith]], _Representable functors and operations on rings_,  Proc. London Math. Soc. (3), 1970, 619--643, [MR265348](http://www.ams.org/mathscinet-getitem?mr=265348), [doi](http://dx.doi.org/10.1112/plms/s3-20.4.619)

* J. Borger, B. Wieland, _Plethystic algebra_, Adv. Math. __194__ (2005), no. 2, 246&#8211;283, [doi](http://dx.doi.org/10.1016/j.aim.2004.06.006), [pdf](http://wwwmaths.anu.edu.au/~borger/papers/03/lambda.pdf), [MR2006i:13044](http://www.ams.org/mathscinet-getitem?mr=2139914)

* [[Andrew Stacey|A. Stacey]] and S. Whitehouse, _The Hunting of the Hopf Ring_,   Homology, Homotopy and Applications __11__(2), 2009, 75--132, [online](http://intlpress.com/HHA/v11/n2/a6), [arXiv/0711.3722](http://arxiv.org/abs/0711.3722).

An old and long query-discussion has been archived starting [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=291&Focus=26302#Comment_26302).

[[!redirects Tall-Wraith monoid]]
[[!redirects Tall-Wraith monoids]]
[[!redirects Tall–Wraith monoid]]
[[!redirects Tall–Wraith monoids]]
[[!redirects Tall--Wraith monoid]]
[[!redirects Tall--Wraith monoids]]

