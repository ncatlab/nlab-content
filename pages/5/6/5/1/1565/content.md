
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[algebra]], by a _rig_ one means a [[mathematical structure]] much like a [[ring]] but without the assumption that every element has an additive inverse, hence without the assumption of *negatives* (whence the omission of "n" from "ring" &lbrack;[Schanuel 1991 p. 379](#Schanuel91), [Lawvere 1992 p. 2](#Lawvere92)&rbrack;)


\begin{remark}
**(Terminology: Rigs and semirings)**
Rigs are commonly also called _semirings_, but the term 'semiring' is overloaded in the mathematics literature, with different authors each defining a semiring to be different algebraic structures from each other. See *[[semiring]]* for a discussion about the various definitions of semirings; only one of the proposed definitions is the same as the one of *rigs* as considered here. 
\end{remark}

## Definition
 {#Definition}

A _rig_ is a [[set]] $R$ with binary operations of addition and multiplication, such that

* $R$ is a [[monoid]] under multiplication;
* $R$ is a [[commutative monoid]] under addition;
* multiplication distributes over addition, i.e. the distributivity laws hold:
  $$x\cdot (y+z) = (x\cdot y) + (x\cdot z)$$
  $$(y+z)\cdot x = (y\cdot x) + (z\cdot x)$$
and also the absorption laws, which are the nullary version of the distributive laws:
  $$0\cdot x = 0 = x\cdot 0.$$

In a ring, the absorption laws follow from distributivity, since for example $0\cdot x + 0\cdot x = (0+0)\cdot x = 0\cdot x$ and we can cancel one copy to obtain $0\cdot x = 0$.  In a [[rig]], however, we have to assert the absorption laws separately.

More sophisticatedly, we can say that just as a ring is a [[monoid object]] in [[abelian group]]s, so a rig is a monoid object in [[commutative monoid]]s.  Here the categories of abelian groups and commutative monoids must be given suitable monoidal structures: not the cartesian product, but the tensor product $\otimes$ that has a universal property for bilinear maps.

Equivalently, a rig is the [[hom-set]] of a category with a single object that is [[enriched category|enriched]] in the category of [[commutative monoids]].

Rigs and rig [[homomorphisms]] form the category [[Rig]].

### Further weakening

As with rings, one sometimes considers non-associative or non-unital versions (where multiplication may not be [[associative]] or may have no [[identity]]).  It is rarer to remove requirements from addition as we have done here.  But notice that while $R$ can be proved (from the other axioms) to be an [[abelian group]] under addition (and therefore a ring) as long as it is a [[group]], this argument does not go through if it is only a monoid.  If we assert only distributivity on one side, however, then we can have a noncommutative addition; see [[near-ring]].

## Properties

Many rigs are either [[ring]]s or [[distributive lattice]]s.  Indeed, a ring is precisely a rig that forms a group under addition, while a distributive lattice is precisely a commutative, simple rig in which both operations are idempotent (see ([Golan 2003, Proposition 2.25](#Golan2003))). Note that a [[Boolean algebra]] is a rig in both ways: as a lattice and as a [[Boolean ring]].

Any rig can be "completed" to a ring by adding negatives, in generalization of how the [[natural numbers]] are completed to the [[integers]].  When applied to the [[set]] of [[isomorphism classes]] of objects in a [[rig category]], the result is part of [[algebraic K-theory]]. 

More formally, the ring completion of a rig $R$ is obtained by applying the [[group completion]] functor to the underlying additive monoid of $R$, and extending the rig multiplication to a ring multiplication by exploiting distributivity; this gives the [[left adjoint]] $F: Rig \to Ring$ to the forgetful functor $U: Ring \to Rig$. Note however that the unit of the [[adjunction]] $R \to U F(R)$ is not [[monomorphism|monic]] if the additive monoid of $R$ is not [[cancellation monoid|cancellative]], despite an informal convention that "[[completion]]" should usually mean a [[monad]] where the unit *is* monic. 

Matrices of rigs can be used to formulate versions of [[matrix mechanics]].

Every rig with [[positive characteristic]] is a [[ring]]. 

## Examples

Some rigs which are neither rings nor distributive lattices include:

* The [[natural numbers]].
* The nonnegative [[rational number]]s and the nonnegative [[real numbers]].
* Polynomials with coefficients in any rig.
* The set of isomorphism classes of objects in any [[distributive category]], or more generally in any [[rig category]].

* The [[tropical rig]], which is $\mathbb{R}\cup \{\infty\}$ with addition $x\oplus y = min(x,y)$  and multiplication $x\otimes y = x+y$.

  Tropical rigs are among the important class of *[[idempotent semirings]]*. 

* The [[ideals]] of a [[commutative ring]] form a rig under ideal addition and multiplication, where the unit and zero ideals are the unit and zero elements of the rig, respectively.  They also form a [[distributive lattice]] and therefore a rig in another way; note that the addition operation is the same in both rigs but the multiplication operation is different (being intersection in the lattice).

## Related concepts

* [[semiring]]

* [[rng]] ([[nonunital ring]])

* [[ring]], [[near-ring]]

* [[tropical geometry]], [[tropical semiring]]

* [[idempotent semiring]]

* A [[categorification]] of the notion of rig is the notion of [[rig category]], or more generally [[colax-distributive rig category]].  See also [[2-rig]] and [[distributivity for monoidal structures]].

* [[semi-monoid]]/[[semi-group]]

* [[semi-category]], [[semi-Segal space]]

* [[semi-simplicial set]]

* [[Burnside rig]]

* [[division rig]]

* [[multiplicatively cancellable rig]]

* [[star rig]]

* [[Conway rig]]

* [[Kleene star algebra]]

## References

The terminology "rig" is due to:

* {#Schanuel91} [[Stephen H. Schanuel]], p. 379 of: *Negative sets have Euler characteristic and dimension*, in: *Category Theory*, Lecture Notes in Mathematics **1488** (1991) 379–385 &lbrack;[doi:10.1007/BFb0084232](https://doi.org/10.1007/BFb0084232)&rbrack;

* {#Lawvere92} [[William Lawvere]], pp. 1 of: *Introduction to Linear Categories and Applications*, course lecture notes (1992) &lbrack;[pdf](https://github.com/mattearnshaw/lawvere/blob/192dac273e8bf352f307f87b9ec4fe8ef7dc85b9/pdfs/1992-introduction-to-linear-categories-and-applications.pdf), [[Lawvere-LinearCategories.pdf:file]]&rbrack;

as recalled in: 

* [[F. William Lawvere]]: *The legacy of Steve Schanuel!* (2015) &lbrack;[[Lawvere-LegacyOfSchanuel.pdf:file]], [archive](https://web.archive.org/web/20230311022135/https://www.acsu.buffalo.edu/~wlawvere/Schanuel%20Memorial%20posting.htm)&rbrack;

> "We were amused when we finally revealed to each other that we had each independently come up with the term 'rig'."

Discussion under the name *semirings*:

* {#Golan1999} Jonathan S. Golan, _Semirings and their applications_. Updated and expanded version of The theory of semirings, with applications to mathematics and theoretical computer science, Longman Sci. Tech., Harlow, 1992, MR1163371. Kluwer Academic Publishers, Dordrecht, 1999. xii+381 pp.

* {#Golan2003} Jonathan S. Golan, _Semirings and affine equations over them: theory and applications_ (Vol. 556). Springer Science & Business Media, 2003.

* [[M. Marcolli]], R. Thomgren, _Thermodynamical semirings_, [arXiv/1108.2874](http://arxiv.org/abs/1108.2874)

* wikipedia [semiring](http://en.wikipedia.org/wiki/Semiring)

* J. Jun, S. Ray, J. Tolliver, _Lattices, spectral spaces, and closure operations on idempotent semirings_, [arxiv/2001.00808](https://arxiv.org/abs/2001.00808)

* [[Manfred Droste]], [[Werner Kuich]], *Semirings and Formal Power Series* (2009). In: Manfred Droste, Werner Kuich, [[Heiko Vogler]] (editors), Handbook of Weighted Automata. Monographs in Theoretical Computer Science. An EATCS Series. Springer, Berlin, Heidelberg. pp. 3–28.([doi:10.1007/978-3-642-01492-5_1](https://doi.org/10.1007%2F978-3-642-01492-5_1))

* [[Zoltán Ésik]], *Iteration semirings* (2008). In: Masami Ito, Masafumi Toyama (editors), Developments in language theory. 12th international conference, DLT 2008, Kyoto, Japan, September 16–19, 2008. Proceedings. Lecture Notes in Computer Science. Vol. 5257. Berlin: Springer-Verlag. pp. 1–20. ([doi:10.1007/978-3-540-85780-8_1](https://doi.org/10.1007%2F978-3-540-85780-8_1))

* [[Dexter Kozen]] (1990). *On Kleene algebras and closed semirings*. In: [[Branislav Rovan]] (editor). Mathematical Foundations of Computer Science 1990. MFCS 1990. Lecture Notes in Computer Science, vol 452. Springer, Berlin, Heidelberg. ([doi:10.1007/BFb0029594](https://doi.org/10.1007/BFb0029594), [pdf](https://www.cs.cornell.edu/~kozen/Papers/kacs.pdf))

[[!redirects rigs]]
[[!redirects Rigs]]
[[!redirects commutative rig]]

