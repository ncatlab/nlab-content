
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

This is a basic result in general algebra, and is not stated here in its full generality (although see [below](/nlab/show/Tall-Wraith+monoid#general) for some reasonably general constructions).

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

* If $V$ is the theory of [[commutative ring|commutative unital rings]], a $V$-algebra is a commutative unital ring, a co-$V$-algebra object in $V$ is a [[biring]] and the corresponding sort of Tall--Wraith $V$-monoid is called, in Tall and Wraith's original paper, a *biring triple*.

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
 
  It is part of the general theory that the category of co-$V$-objects in $V$ is monoidal (though not, in general, symmetric). For details on this see _The Hunting of the Hopf Ring_, referred to below.  This monoidal structure for abelian groups turns out to be the tensor product.

  Thus a Tall--Wraith monoid for abelian groups is actually an ordinary monoid in the category of abelian groups: in other words, a [[ring]]!


## General results and constructions {#general}

We now recapitulate the discussion above in a slightly more general context. 

### Bialgebras over a monad 

For now our context is that of [[monads]] $T$ on [[Set]], although all of what follows can be generalized considerably, for example to [[enriched category theory]] replacing $Set$ by a suitable [[cosmos]] $\mathbf{V}$. 

Notation: the category of $T$-[[Eilenberg-Moore category|algebras]] is denoted $Set^T$, with forgetful functor $U: Set^T \to Set$ and free functor $F: Set \to Set^T$, whose composite is the monad $T = U F$, and whose [[counit]] is denoted $\epsilon: F U \to 1_{Set^T}$. 

For each $T$-algebra $R$, there is an [[adjunction|adjoint pair]] of functors 

$$- \cdot R \dashv \hom(R, -): Set^T \to Set$$ 

with associated monad $\hom(R, - \cdot R)$. The functor $- \cdot R: Set \to Set^T$ takes a set $X$ to the $T$-algebra $X \cdot R$, an $X$-indexed [[coproduct]] of copies of $R$ in $Set^T$. We define a $T$-*bialgebra* to be a $T$-algebra $R$ equipped with a morphism of monads $\phi: T \to \hom(R, -\cdot R)$. By the adjunction, the datum $\phi$ is equivalent to a left $T$-algebra structure 

$$\alpha: T \circ \hom(R, -) \to \hom(R, -)$$ 

on $\hom(R, -): Set^T \to Set$, thus giving a lifting denoted (by abuse of language) $\hom(R, -): Set^T \to Set^T$. This datum is also equivalent to a right $T$-algebra (aka right $T$-module) structure 

$$\beta: W T \to W$$ 

where $W = W_R \coloneqq - \cdot R: Set \to Set^T$. A $T$-*bialgebra map* is a $T$-algebra map $f: R \to S$ such that the induced map $W_f: W_R \to W_S$ is a morphism of right $T$-modules. 

+-- {: .num_example} 
###### Example 
A good case to keep in mind is that of [[birings]], which are $T$-bialgebras for the [[Lawvere theory]] $T$ of [[commutative rings]]. The monad morphism $T \to \hom(R, -\cdot R)$ has components $T X \to \hom(R, X \cdot R)$ for each set $X$. Here $X \cdot R$ is an $X$-indexed coproduct of copies of $R$, where coproduct in the category of commutative rings $Set^T$ is given by tensor product. Thus, for example, $2 \cdot R$ is the ring $R \otimes R$. The component $T(2) \to \hom(R, 2\cdot R)$ therefore "interprets" each element $\theta \in T(2)$, i.e., each binary operation in the Lawvere theory, as a binary *co*-operation $R \to R \otimes R$. This applies in particular to the elements $m, a \in T(2)$ which abstractly represent multiplication and addition (seen as natural operations on the category of commutative rings). 
=-- 

### Monoidal product on bialgebras over a monad 

We thus have several perspectives on what a $T$-bialgebra is: 

* A $T$-algebra $R$ equipped with a monad morphism $T \to \hom(R, -\cdot R)$, 

* A $T$-algebra equipped with a compatible $T$-coalgebra structure (actually the same as the preceding item, but in different words), 

* A $T$-algebra $R$ for which $\hom(R, -)$ is provided with a left $T$-algebra structure, 

* A $T$-algebra $R$ for which $-\cdot R$ is provided with a right $T$-algebra/module structure. 

The following proposition gives two more useful descriptions: 

+-- {: .num_prop} 
###### Proposition 
Let $Ladj(Set^T, Set^T)$ ($Radj(Set^T, Set^T)$) be the category of left (right) adjoint functors $\Psi: Set^T \to Set^T$. The functor $T$-$BiAlg \to Ladj(Set^T, Set^T)$ that takes $(R, \phi)$ to the right $T$-module $(W_R, \beta)$ is an equivalence. Or, what is the same, the functor $T$-$BiAlg \to Radj(Set^T, Set^T)^{op}$, taking $(R, \phi)$ to the left $T$-algebra $\hom(R, -), \alpha)$, is an equivalence. 
=-- 

+-- {: .proof} 
###### Sketch of proof 
The main thing to check is that the functor $R \mapsto \hom(R, -)$ to $Radj(Set^T, Set^T)^{op}$ is [[essentially surjective functor|essentially surjective]]. The essential point is that $\Phi$ has a left adjoint iff $U \Phi$ has a left adjoint iff $U \Phi: Set^T \to Set$ is [[representable functor|representable]]: $U \Phi \cong \hom(R, -)$ for some $T$-algebra $R$ (in which case the lift $\Phi$ of $\hom(R, -)$ through $U$ is tantamount to a $T$-algebra structure on $\hom(R, -)$). The only (mildly) tricky part is that $\Phi$ has a left adjoint if $U\Phi$ has a left adjoint $W = W_R$. To define the left adjoint $\Psi$ of $\Phi$ objectwise, we take any $T$-algebra $S$ with its canonical presentation 

$$F U F U S \stackrel{\overset{\epsilon F U S}{\to}}{\underset{F U \epsilon}{\to}} F U S \stackrel{\epsilon}{\to} S$$ 

which is a [[coequalizer]] diagram. A left adjoint $\Psi$ must preserve this coequalizer, and we must have $\Psi F \cong W$ since both sides are left adjoint to $U \Phi$. Thus we define $\Psi (S)$ to be a coequalizer 

$$W(T U S) \stackrel{\overset{\beta U S}{\to}}{\underset{W U\epsilon S}{\to}} W(U S) \to \Psi(S)$$ 

where $\beta: W T \to T$ is the $T$-module structure coming from the monad morphism $\phi: T \to \hom(R, -\cdot R)$. This objectwise definition of $\Psi$ easily extends to morphisms by [[universal property|universality]] and provides a left adjoint to $\Phi$. Remaining details are left to the reader. 
=-- 

One import of this proposition is that left adjoint endofunctors on $Set^T$ compose, i.e., endofunctor composition gives a monoidal structure on $Ladj(Set^T, Set^T)$, and this monoidal structure transports across the categorical equivalence of the proposition to give a monoidal structure on $T$-$BiAlg$. The resultant monoidal product on $T$-bialgebras is denoted $\odot$. 

A second import of this proposition is that the canonical functor $T\text{-}Bialg \to Ladj(Set^T, Set^T)$ induces a functor which is reasonably denoted 

$$\odot: T\text{-}Bialg \times Set^T \to Set^T,$$ 

realizing an [[actegory]] structure over the monoidal category $T\text{-}Bialg$. 

A direct construction of the monoidal product $\odot$ can be extracted by following the proof of the proposition. If $R, S$ are $T$-bialgebras, then the underlying $T$-algebra of $S \odot R$ (corresponding to composition of $\hom(S, -) \circ \hom(R, -)$ of right adjoints $Set^T \to Set^T$) is computed as a reflexive coequalizer in $Set^T$: 

$$T U S \cdot R \stackrel{\overset{\epsilon U S \cdot R}{\to}}{\underset{\beta U S}{\to}} U S \cdot R \to S \odot R.$$ 

Here $\epsilon U S$ is the same as the $T$-algebra structure $T U S \to U S$ on $S$. Whereas $\beta X: T X \cdot R \to X \cdot R$ is a component of the $T$-module structure $W_R T \to W_R$; it is mated by the $- \cdot R \dashv \hom(R, -)$ adjunction to the component of the coalgebra structure $\phi X: T X \to \hom(R, X \cdot R)$. 

To extract the $T$-coalgebra structure on $S \odot R$, let us observe generally that if $F: C \to D$ is a left adjoint, then for any category $E$ there is an induced left adjoint $[1_E, F]: [E, C] \to [E, D]$ and similarly an induced left adjoint $Ladj(E, C) \to Ladj(E, D)$. Applying this to the case where $C = D = E = Set^T$ and where $F$ is the left adjoint to the lift $\hom(R, -): Set^T \to Set^T$, we find that 

$$- \odot R: Ladj(Set^T, Set^T) \to Ladj(Set^T, Set^T)$$ 

is a left adjoint, and in particular preserves $Y$-indexed copowers $Y \cdot S$. In other words, for each $X$ we have canonical isomorphisms 

$$X \cdot (S \odot R) \cong (X \cdot S) \odot R, \qquad T X \cdot (S \odot R) \cong (T X \cdot S) \odot R$$ 

so that the desired right $T$-module structure is given componentwise by a composite 

$$\beta (S \odot R)_X \coloneqq \left(T X \cdot (S \odot R) \cong (T X \cdot S) \odot R \stackrel{(\beta S)_X \odot R}{\to} (X \cdot S) \odot R \cong X \cdot (S \odot R)\right).$$ 

### Tall-Wraith monoids relative to a monad 

A *Tall-Wraith monoid* over $T$ is of course a monoid in the monoidal category $(T\text{-}BiAlg, \odot)$. We note that the unit in his monoidal category is the free $T$-algebra $F(1)$, equipped with its canonical lift $id: Set^T \to Set^T$. That is, the $T$-coalgebra structure on $F(1)$ is given tautologously by 

$$T(X) \cong U F(X) \cong Set^T(F(1), F(X)) \cong Set^T(F(1), X \cdot F(1)).$$ 

So, multiplication on a Tall-Wraith monoid is a bialgebra map $m: R \odot R \to R$ and the unit is a bialgebra map $u: F(1) \to R$. Such a monoid is tantamount precisely to a monoid in $Ladj(Set^T, Set^T)$, i.e., to a *left adjoint monad* on $Set^T$. In particular, for a Tall-Wraith monoid $R$, one has a category $R Alg$ of algebras over that monad, giving a monadic functor $Alg_R \to Set^T$. 

Now, recall that left adjoint monads are canonically [[mate|mated]] to right adjoint comonads $C$, in such a way that the category of algebras over the monad is equivalent to the category of coalgebras over the comonad. In short, Tall-Wraith monoids over $T$ are essentially the same thing as functors 

$$G: C \to Set^T$$ 

which are simultaneously *monadic and comonadic*: the comonadicity means $G$ is a left adjoint and has a left adjoint $F$, so that the monad $G F: Set^T \to Set^T$ resides in $Ladj(Set^T, Set^T)$, and such monads are tantamount to Tall-Wraith monoids. 

+-- {: .num_example} 
###### Example 
In the important example where $T$ is the theory of commutative rings and $\Lambda$ is the bialgebra $\mathbb{Z}[x_1, x_2, \ldots]$, equipped with a Tall-Wraith multiplication $\Lambda \odot \Lambda \to \Lambda$ given by [[plethysm]] (a decategorified product that arises by viewing $\Lambda$ as the Grothendieck ring of the category of $Ab$-valued [[species]] together with its substitution or plethystic product), the category $Alg_\Lambda$ may be identified with the category of [[lambda-rings]]. In this case the monad $\Lambda \odot -$ has right adjoint given by $\hom(\Lambda, -)$. The *right* adjoint $CRing \to \Lambda Ring$ to the forgetful functor is the big Witt functor, often denoted $W$. 
=-- 


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

