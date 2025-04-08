
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


+-- {: .num_defn}
###### Definition

A __distributive lattice__ is a [[lattice]] in which [[join]] $\vee$ and [[meet]] $\wedge$ _distribute_ over each other, in that for all $x,y,z$ in the lattice, the _distributivity laws_ are satisfied:

*  $x \vee (y \wedge z) = (x \vee y) \wedge (x \vee z)$,
*  $x \wedge (y \vee z) = (x \wedge y) \vee (x \wedge z)$.

=--

+-- {: .num_remark}
###### Remark

The nullary forms of distributivity hold in any lattice: 

*  $x \vee \top = \top$,
*  $x \wedge \bot = \bot$.

Distributive lattices and [[lattice]] [[homomorphisms]] form a [[concrete category]] [[DistLat]].

=--

+-- {: .num_remark}
###### Remark

Any lattice that satisfies one of the two binary distributivity laws must also satisfy the other; isn\'t that nice? (This may safely be left as an [[exercise]].) This also means that a distributive lattice is precisely a lattice (or indeed a [[poset]]) which is a [[distributive category]] (when viewed as a [[thin category]].)

This convenience does *not* extend to infinitary distributivity, however.

=--

+-- {: .num_remark}
###### Remark

Each distributivity law holds in one direction in any lattice (the proofs of which may be left as an exercise):

* $x \vee (y \wedge z) \leq (x \vee y) \wedge (x \vee z)$
* $x \wedge (y \vee z) \geq (x \wedge y) \vee (x \wedge z)$

As a result, the real content of the definition consists of the converse directions (and as remarked above, either one suffices):

* $x \vee (y \wedge z) \geq (x \vee y) \wedge (x \vee z)$
* $x \wedge (y \vee z) \leq (x \wedge y) \vee (x \wedge z)$

=--

## Alternative characterizations 

As mentioned above, the theory of distributive lattices is self-dual, something that is proved in almost any account (or left as an exercise), but which is not manifestly obvious from the standard definition which chooses one of the two distributivity laws and goes from there. In this section we provide some other characterizations or axiomatizations which *are* manifestly self-dual. 

Here is one such characterization: 

+-- {: .num_prop #sd1} 
###### Proposition 
A lattice is distributive if and only if the identity 

$$(a \wedge b) \vee (a \wedge c) \vee (b \wedge c) = (a \vee b) \wedge (a \vee c) \wedge (b \vee c)$$ 

is satisfied. 
=-- 

Again this may be left as a (somewhat mechanical) exercise. 

Perhaps more useful in practice is the characterization in terms of "forbidden sublattices" due to Birkhoff. Namely, introduce the "pentagon" $N_5$ as the 5-element lattice $\{\bot \leq a, b, c \leq \top\}$ where $b \leq c$ and $a$ is incomparable to $b, c$, so that $\bot = a \wedge c$ and $a \vee b = \top$. Introduce the "thick diamond" $M_3$ as the 5-element lattice $\{\bot \leq a', b', c' \leq \top\}$ with $a', b', c'$ pairwise incomparable. Both $N_5$ and $M_3$ are self-dual. Birkhoff's characterization is the following (manifestly self-dual) criterion. 

+-- {: .num_theorem} 
###### Theorem 
A lattice $L$ is distributive if and only if there is no [[injective function|embedding]] of $N_5$ or $M_3$ into $L$ that preserves binary meets and binary joins. 
=-- 

This can be useful for determining distributivity or its failure, especially in cases where one can visualize a lattice via its [[Hasse diagram]]. 

The necessity of the forbidden sublattice condition is clear in view of the fact that the cancellation law stated in the next result fails in $N_5$ and $M_3$. This result gives another self-dual axiomatization of distributive lattices. 

+-- {: .num_prop #sd2} 
###### Proposition 
A lattice $L$ is distributive if and only if the cancellation law holds: for all $y, z \in L$, we have $y = z$ whenever $x \wedge y = x \wedge z$ and $x \vee y = x \vee z$ (for some $x$). 
=-- 

+-- {: .proof} 
###### Proof 
"Only if": if $x \wedge y = x \wedge z$ and $x \vee y = x \vee z$, then 

$$y = y \vee (x \wedge y) = y \vee (x \wedge z) = (y \vee x) \wedge (y \vee z) = (x \vee z) \wedge (y \vee z) = (x \wedge y) \vee z$$ 

which implies $z \leq y$, and similarly we have $y \leq z$. 

"If": this is harder. Assuming the cancellation law for $L$, we first show $L$ is modular. Recall from [[modular lattice]] that for any lattice $L$ and $a, b \in L$, there is a covariant [[Galois connection]] 

$$([a \wedge b, b] \to [a, a \vee b]: x \mapsto a \vee x) \; \dashv \; ([a, a \vee b] \to [a \wedge b, b]: y \mapsto b \wedge y)$$ 

and that $L$ is *modular* if this Galois connection is a [[Galois correspondence]] (or [[adjoint equivalence]]) for all $a, b$. Now, if $x \in [a \wedge b, b]$, then $a \vee x = a \vee (b \wedge (a \vee x))$ because $f = f g f$ for any Galois connection $f \dashv g$. From $a \wedge b \leq x \leq b$ we also have 

$$a \wedge x = a \wedge b \wedge x = a \wedge b = a \wedge b \wedge (a \vee x)$$ 

and so by cancellation of the $a$\'s, we conclude $x = b \wedge (a \vee x)$. Similarly (dually), for $y \in [a, a \vee b]$, we have $y = a \vee (b \wedge y)$. Hence $L$ is modular. 

Now we show $L$ is distributive. Let $x, y, z \in L$ and consider the three elements 

$$\array{
u & \coloneqq & [x \wedge (y \vee z)] \vee (y \wedge z) & = & [x \vee (y \wedge z)] \wedge (y \vee z) \\ 
v & \coloneqq & [y \wedge (x \vee z)] \vee (x \wedge z) & = & [y \vee (x \wedge z)] \wedge (x \vee z) \\ 
w & \coloneqq & [z \wedge (x \vee y)] \vee (x \wedge y) & = & [z \vee (x \wedge y)] \wedge (x \vee y)
}$$ 

where the non-definitional equalities follow from modularity. Using the first expressions, we compute 

$$\array{
u \vee v & = & [x \wedge (y \vee z)] \vee (y \wedge z) \vee [y \wedge (x \vee z)] \vee (x \wedge z) \\ 
 & = & [x \wedge (y \vee z)] \vee [y \wedge (x \vee z)] \\ 
 & = & [(x \wedge (y \vee z)) \vee y] \wedge (x \vee z) \\ 
 & = & (x \vee y) \wedge (x \vee z) \wedge (y \vee z)
}$$ 

where the third and fourth lines use modularity. By symmetry in the letters $x, y, z$, we also have $u \vee w = v \vee w = (x \vee y) \wedge (x \vee z) \wedge (y \vee z)$. Now the second expressions are dual to the first, so by duality we compute 

$$u \wedge v = u \wedge w = v \wedge w = (x \wedge y) \vee (x \wedge z) \vee (y \wedge z).$$ 

Now by cancellation of the $u$\'s, we may conclude $v = w$, but in that case we obtain 

$$(x \vee y) \wedge (x \vee z) \wedge (y \vee z) = v \vee w = v \wedge w = (x \wedge y) \vee (x \wedge z) \vee (y \wedge z)$$ 

so that $L$ is distributive by Proposition \ref{sd1}. 
=-- 

+-- {: .num_remark} 
###### Remark 
While the expressions for $u, v, w$ in the preceding proof may look as though they come out of thin air, the underlying idea is that the sublattice of $L$ generated by $x, y, z$ is the [[image]] of a lattice map $F(3) \to L$ out of the free modular lattice $F(3)$ on three elements. The only obstruction to distributivity in $F(3)$ is the presence of an $M_3$-sublattice appearing in the center of its [Hasse diagram](https://golem.ph.utexas.edu/category/2015/09/the_free_modular_lattice_on_3.html#c049685). The middle elements of that sublattice correspond to the formal expressions for $u, v, w$ given above, and the proof shows that under the cancellation law, we have $u = v = w$ in $L$, making the thick diamond collapse to a point in $L$ and removing the obstruction to distributivity. 
=-- 

From Proposition \ref{sd2}, it is not very hard to deduce Birkhoff's theorem. The presence of a copy of $M_3$ or $N_5$ in a non-distributive lattice $L$ is deduced from a failure of the cancellation law where we have three elements $x, y, z$ with $x \wedge y = x \wedge z$, $x \vee y = x \vee z$, and $y \neq z$. If $y, z$ are comparable, say $y \leq z$, then the set $\{x \wedge y, x, y, z, x \vee y\}$ forms an $N_5$. If $y, z$ are incomparable, then we have either $y \vee z \lt x \vee y$, or $y \wedge z \gt x \wedge y$, or both $y \vee z = x \vee y$ and $y \wedge z = x \wedge y$; in the first two cases we get an $N_5$ (e.g., $\{x \wedge y, x, y, y \vee z, x \vee y\}$ for the first case), and in the third case the set $\{x \wedge y, x, y, z, x \vee y\}$ forms an $M_3$. 


## Examples

Any [[Boolean algebra]], and even any [[Heyting algebra]], is a distributive lattice. 

Every [[frame]] and every [[sigma-frame|$\sigma$-frame]] is a distributive lattice. 

Any [[bounded total order]] is a distributive lattice. 

Any [[linear order]] is a distributive lattice. 

An [[integral domain]] is a [[Prüfer domain]] iff its lattice of [[ideals]] is distributive. The classical example is $\mathbb{Z}$; equivalently, the (opposite of the) multiplicative monoid $\mathbb{N}$ ordered by divisibility, with $1$ at the bottom and $0$ at the top. 

The lattice of [[Young diagrams]] ordered by inclusion is distributive. 

## Infinitely distributive property

A distributive lattice that is complete (not necessarily [[completely distributive lattice |completely distributive]]) may be **infinitely distributive** or said to satisfiy the **infinite distributive law** :

  $$ 
    x \wedge (\bigvee_i y_i) = \bigvee_i (x\wedge y_i)
  $$

This property is sufficient to give the lattice [[Heyting algebra]] stucture where the implication $a\Rightarrow b$ (or  [[exponential object]] $b^a$) is: 

$$(u \Rightarrow v) = \bigvee_{x \wedge u \leq v} x$$ 

Note that this property does not imply the dual  **co-infinitely distributive** property:

  $$ 
    x \vee (\bigwedge_i y_i) = \bigwedge_i (x\vee y_i)
  $$

Instead this dual gives the lattice [[co-Heyting algebra|co-Heyting]] structure where the co-implication or "subtraction"  ($\backslash$) is

$$(u \backslash v) = \bigwedge_{u \leq v \vee x} x$$ 

If a lattice has both properties, as in a [[completely distributive lattice]], then it has [[bi-Heyting algebra|bi-Heyting]] structure (both  Heyting and co-Heyting), but the two exponentials are not necessarily equal.
  
$$(u \Rightarrow v) = \bigvee_{x \wedge u \leq v} x$$

and 

$$(u \backslash v) = \bigwedge_{u \leq v \vee x} x$$

> Does it make sense to define "infinitely distributive property" for non-complete lattices? (Something like: "Whenever the join exists, it satisfies the infinite distributive law.")

## Properties

### Finite distributive lattices
 {#OppositeCategory}

Since a finite distributive lattice is  [[completely distributive lattice |completely distributive]] it is a bi-Heyting lattice, as shown above.

Let $FinDistLat$ be the category of finite distributive lattices and lattice homomorphisms, and let $FinPoset$ be the category of finite [[posets]] and order-preserving functions.  These are contravariantly equivalent, thanks to the presence of an [[ambimorphic object]]:

**Proposition.** The [[opposite category]] of $FinDistLat$ is [[equivalence of categories|equivalent]] to $FinPoset$:

$$
  FinDistLat^{op} \simeq FinPoset.
$$

One direction of this equivalence is given by the hom-functor

$$
  [-,2] \;\colon\; FinDistLat^{op} \stackrel{\simeq}{\to} FinPoset
$$

where $2$ is the 2-element distributive lattice and for any $X \in  FinDistLat$, $[X,2]$ is the poset of distributive lattice morphisms from $X$ to $2$.  The other direction is given by 

$$
  [-,2] \;\colon\; FinPoset^{op} \stackrel{\simeq}{\to} FinDistLat
$$

where $2 = \{0,1\}$ is the 2-element poset with $0 \lt 1$ and for any $Y \in \FinPoset$, $[Y,2]$ is the distributive lattice of poset morphisms from $Y$ to $2$.

This __Birkhoff duality__ is (in one form or another) mentioned in many places; the formulation in terms of hom-functors may be found in 

* [[Gavin C. Wraith]], _Using the generic interval_, Cah. Top. G&#233;om. Diff. Cat. **XXXIV** 4 (1993) pp.259-266. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1993__34_4/CTGDC_1993__34_4_259_0/CTGDC_1993__34_4_259_0.pdf))

The functorial nature of the correspondence means that morphisms of finite posets (i.e. order-preserving maps) naturally correspond to morphisms of finite distributive lattices (i.e. order-preserving maps that also respect meet and join).

It follows from Birkhoff's representation theorem that every finite distributive lattice can be seen as a lattice of sets (i.e. sets with join and meet given by union and intersection) -- in particular, sets whose elements are the join-irreducible elements of the lattice. Furthermore, a good intuition for why this duality holds is that either an element is generated as the join of existing elements, or it is join-irreducible. Hence given any existing poset, we can simply add all missing joins, and also a bottom (i.e. the nullary join). By general results (the adjoint functor theorem for posets) this suffices to ensure that all meets exist as well. This is analogous to the free colimit completion of a category, and indeed Birkhoff representation can be seen as a very special case of the Yoneda lemma as applied to (0,1)-category theory (i.e., order theory), since (0,1)-presheaves are functors into Bool rather than Set and hence correspond to [[lower set]]s.

Birkhoff duality does not hold for infinite distributive lattices. However, in the general case of not-necessarily-finite distributive lattices there is a correspondence not to posets, but instead to a class of spaces known as [[Priestley spaces]] or [[coherent spaces]]. In [[constructive mathematics]], one needs to use [[coherent locales]] for the correspondence to distributive lattices. This is an instance of a general phenomena known as Stone-type duality.

### The free distributive lattice

Posets also give rise to a "free" distributive lattice, which is not the same as their Birkhoff dual. Instead, it is formed by the following procedure: First, take the poset of upsets with the reverse ordering (this is the free finite meet completion). Then form the distributive lattice of finitely generated downsets in that.

In the case that one begins with a discrete poset (i.e., a set) then the number of elements in the resultant free distributive lattice is known as a Dedekind number, which also counts the number of monotone Boolean functions in $n$ variables. Dedekind numbers increase extremely rapidly, and there is no good known closed-form summation to compute them. The first ten (and only known) Dedekind numbers are (starting at $n = 0$): 2, 3, 6, 20, 168, 7581, 7828354, 2414682040998, 56130437228687557907788, and 286386577668298411128469151667598498812366; see [OEIS A000372](#A000372).

### Categorification

Every distributive lattice, regarded as a [[category]] (a [[(0,1)-category]]), is a _[[coherent category]]_.  Conversely, the notion of coherent category may be understood as a [[categorification]] of the notion of distributive lattice.  A different categorification is the notion of [[distributive category]].

### Completion


The [[completely distributive lattice|completely distributive]] [[algebraic lattices]] (the [[frames of opens]] of [[Alexandroff locales]]) form a [[reflective subcategory]] of that of all distributive lattices. The reflector is called _[[canonical extension]]_.

## Related concepts

* [[Dedekind cube category]]

* [[Phoa's principle]]

* [[flat distributive lattice]]

* [[Priestley space]]

* [[coherent space]], [[coherent locale]]

* [[coherent category]]

## References

* {#A000372} OEIS sequence [A000372](https://oeis.org/A000372)

* {#WeaverLicata20} [[Matthew Weaver]], [[Daniel Licata]], *A Constructive Model of Directed Univalence in Bicubical Sets*, in: *Proceedings of the 35th Annual ACM/IEEE Symposium on Logic in Computer Science. LICS ’20*, Association for Computing Machinery (2020) 915–928 &lbrack;[doi:10.1145/3373718.3394794](https://doi.org/10.1145/3373718.3394794)&rbrack;

[[!redirects distributive lattices]]
[[!redirects Birkhoff duality]]