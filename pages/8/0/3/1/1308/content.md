
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# The Eckmann--Hilton argument
* table of contents
{: toc}

## Statements

In its original form, the _Eckmann--Hilton argument_ shows that a [[monoid object]] or [[group object]] [[internalization|internal]] to the [[category of monoids]] or [[Groups]] is necessarily [[abelian group|commutative]]. 

In other words this says that if a [[set]] is equipped with a [[pair]] of [[monoid]] [[structures]], such that one is a [[homomorphism]] for the other, then the two structures actually coincide and the resulting monoid is [[commutative monoid|commutative]].

From the [[nPOV]], we may want to think of the statement in this way:

+-- {: .num_prop #2cat}
###### Proposition

Let $C$ be a [[2-category]] and $x \in C$ an [[object]]. Write $Id_x$ for the [[identity]] [[morphism]] of $X$ and $End(Id_x)$ for the set of [[endomorphism|endo]]-[[2-morphism|2-morphisms]] on $X$. Then:

* [[horizontal composition]] and [[vertical composition]] define the same [[monoid object]] structure on $End(Id_x)$;

* this is a [[commutative monoid]].
=--

On the face of it, this is a special case of the general situation, although in fact every case is an example for appropriate $C$.

A more general version is this:  If a set is equipped with two binary operations with [[identity elements]], as long as they commute with each other in the sense that one is (with respect to the other) a homomorphism of sets with binary operations, then everything else follows:

1.  the other is also a homomorphism with respect to the first;
1.  the identities are the same;
1.  the operations are the same;
1.  the operation is commutative;
1.  the operation is associative.

This can also be [[internalisation|internalised]] in any [[symmetric monoidal category]].


## Proofs

[[string diagram|String diagrams]] allow an almost trivial proof. Since there is only one object, and the only 1-morphism is the identity, the diagram of $a \circ b$ (vertical composition) is simply two dots labelled $a, b$ arranged vertically. This diagram can be morphed continuously to a horizontal arrangement, which is the diagram for $a * b$ (horizontal composition). This is then morphed to $a$ below $b$, which is the diagram for $b \circ a$.

A [[pasting diagram]]-proof of \ref{2cat} is depicted in [Cheng](#Cheng) below.  Here we prove the $6$-element general form in $Set$.

+-- {: .proof}
###### Proof
The basic equation that we have (that one operation $*$ is a homomorphism with respect to another operation $\circ$) is
$$ (a \circ b) * (c \circ d) = (a * c) \circ (b * d) .$$ 
In $End(Id_x)$, this is the [[exchange law]].

We prove the list of results from above in order:

1.  Simply read the basic equation backwards to see that $\circ$ is a homomorphism with respect to $*$.

1.  Then
$$ 1_\star = 1_\star * 1_\star = (1_\star \circ 1_\circ) * (1_\circ \circ 1_\star) = (1_\star * 1_\circ) \circ (1_\circ * 1_\star) = 1_\circ \circ 1_\circ = 1_\circ ,$$
so the identities are the same; we will now write this identity simply as $1$.

1.  Now
$$ a * b = (a \circ 1) * (1 \circ b) = (a * 1) \circ (1 * b) = a \circ b ,$$
so the operations are the same; we will write them both with concatenation.

1.  Then
$$ a b = (1 a) (b 1) = (1 b) (a 1) = b a ,$$
so this operation is commutative.

1.  Finally,
$$ (a b) c = (a b) (1 c) = (a 1) (b c) = a (b c) ,$$
so the operation is associative.
=--

If you start with a monoid object in $Mon$, then only (4&5) need to be shown; the others are part of the hypothesis.  This classic form of the Eckmann--Hilton argument may be combined into a single calculation:
$$ a * b = (a \circ 1) * (1 \circ b) = (a * 1) \circ (1 * b) = a \circ b = (1 * a) \circ (b * 1) = (1 * b) \circ (a * 1) = b * a ,$$
where the desired results involve the first, middle, and last expressions.


## Corollaries

A $2$-[[k-tuply monoidal n-category|tuply monoidal]] $0$-[[0-category|category]], if defined as a [[pointed object|pointed]] [[k-tuply connected n-category|simply connected]] [[bicategory]], is also the same as an abelian monoid.

A $2$-tuply monoidal $1$-[[1-category|category]], if defined as a pointed simply connected [[tricategory]], is the same as a [[braided monoidal category]].

Every [[homotopy group]] $\pi_n$ for $n \geq 2$ is [[abelian group|abelian]].

 

## Variation

There are variations on the Eckmann-Hilton argument that do not assume units. For example, if a set is equipped with two symmetric $(a * b = b * a)$ and idempotent $(a * a = a)$ binary operations that commute with each other, then the operations coincide. 

$$ a * b = (a * b) + (a * b) = (a * b) + (b * a) = (a + b) * (b + a) = (a + b) * (a + b) = a + b.$$

For example, we might consider the algebraic theory of [[convex space|convex spaces]], and the algebraic theory of [[semilattice|semilattices]]. These theories both contain symmetric idempotent operations: in the theory of convex spaces, take the operation $a * b=c_{0.5}(a,b)$. Thus there can be no commutative algebraic theory that includes these two theories without conflating them. Furthermore, in any conflated theory, all the dyadic rationals are the same, e.g. 

$$c_{0.25}(a,b)=c_{0.5}(c_{0.5}(a,b),b)=(a*b)*b=a*(b*b)=a*b=c_{0.5}(a,b).$$ 

This is relevant in computer science because probability is modelled by the free convex spaces monad, and non-determinism is modelled by the free semilattice monad. These monads are both [[commutative monad|commutative monads]], but there can be no commutative monad that contains both these monads non-degenerately. 
In particular, the [[convex powerset of distributions monad]] is not commutative.
### Uniform states are unique

A related guise of this result is the following: If $C$ is a [[distributive monoidal category]] whose unit $I$ is terminal, then any two morphisms $p, q : I \to I + I$ which are symmetric, i.e. invariant under the swap $I + I \cong I+I$, must be equal. From the viewpoint of [[category-theoretic approaches to probability theory|categorical probability]], this says that uniform distributions (if they exist) must be unique.

Every morphism $p : I \to I + \ldots + I$ gives rise to an $n$-ary operation on homsets $\omega_p : C(X,Y)^n \to C(X,Y)$ via

$$\omega_p(f_1,\ldots,f_n) = X \xrightarrow{p \otimes X} (I + \ldots + I) \otimes X \cong X + \ldots + X \xrightarrow{[f_1,\ldots,f_n]} Y$$

The operations $\omega_p$ and $\omega_q$ are idempotent (by terminality of $I$) and commute with each other (by monoidality). Hence if the operations are also symmetric, then they must coincide following the usual Eckmann-Hilton argument. 

We recover the connection to algebraic theories if we take $C$ to be the [[Kleisli category]] of a [[monad]] $T$ which is [[commutative monad|commutative]] and affine.  

## Related concepts

* [[internalization]]

* [[group object]]

* [[H-space]]

* [[exchange law]]

## References

Due to

* [[Beno Eckmann]], [[Peter Hilton]], Theorem 1.12 in: *Structure maps in group theory*, Fundamenta Mathematicae 50 (1961), 207-221 ([doi:10.4064/fm-50-2-207-221](https://www.impan.pl/en/publishing-house/journals-and-series/fundamenta-mathematicae/all/50/2/94854/structure-maps-in-group-theory))

reviewed (somewhat imperfectly) in:

* [[Beno Eckmann]], [[Peter Hilton]], Theorem 5.4.2 in: _Group-like structures in general categories I multiplications and comultiplications_, Math. Ann. 145, 227–255 (1962) ([doi:10.1007/BF01451367](https://doi.org/10.1007/BF01451367))

Expositions:

* {#Catsters} [[The Catsters]]

  _Eckmann-Hilton 1_ ([video](http://www.youtube.com/watch?v=Rjdo-RWQVIY))
  
  _Eckmann-Hilton 2_ ([video](http://www.youtube.com/watch?v=wnRqo7UHa-k))

* [[Eugenia Cheng]], ([picture](http://eugeniacheng.com/ehclock/))
{#Cheng}

* [[Andrew Stacey]], [animation](https://web.archive.org/web/20150326221729/http://www.math.ntnu.no/~stacey/documents/eckmannhilton.mpg) (mpeg)
{#Stacey}


Formulation in [[homotopy type theory]]:

* [[UF-IAS-2012|Univalent Foundations Project]], Thm. 2.1.6 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* 2013 ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* [[Kristina Sojakova]], *Syllepsis in Homotopy Type Theory*, 2021 ([[Sojakova_Syllepsis_20210728.pdf:file]])


Generalization to [[higher algebra]]/[[higher category theory]] via [[operads]]/[[(∞,1)-operads]]:

* {#Batanin} [[Michael Batanin]], _The Eckmann-Hilton argument and higher operads_ ,  Adv. Math.  217  (2008),  no. 1, 334--385; ([arXiv:math.CT/0207281](http://arxiv.org/abs/math/0207281))

* [[Tomer Schlank]], [[Lior Yanovski]], *The ∞-Categorical Eckmann-Hilton Argument*, Algebr. Geom. Topol. 19 (2019) 3119-3170 ([arXiv:1808.06006](https://arxiv.org/abs/1808.06006), [doi:10.2140/agt.2019.19.3119](https://doi.org/10.2140/agt.2019.19.3119))



[[!redirects Eckmann-Hilton argument]]
[[!redirects Eckmann-Hilton arguments]]
[[!redirects Eckmann–Hilton argument]]
[[!redirects Eckmann–Hilton arguments]]
[[!redirects Eckmann--Hilton argument]]
[[!redirects Eckmann--Hilton arguments]]
