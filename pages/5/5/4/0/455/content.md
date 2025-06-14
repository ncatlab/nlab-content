
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Boolean algebras
* table of contents
{: toc}

## Idea

A _Boolean algebra_ or _Boolean [[lattice]]_ is an algebraic structure which models classical [[propositional calculus]], roughly the fragment of the logical calculus which deals with the basic logical connectives "and", "or", "implies", and "not". 


## Definitions

### General

There are many known ways of defining a __Boolean algebra__ or __Boolean lattice__. Here are just a few: 

* A Boolean algebra is a [[complement|complemented]] [[distributive lattice]]. 

* A Boolean algebra is a [[Heyting algebra]] $H$ satisfying the [[law of excluded middle]], which means 
$$\forall_{x \in H} x \vee \neg x = \top$$
or (equivalently) satisfying the [[double negation law]], which means
$$\neg \neg = id: H \to H$$ 

* A Boolean algebra is a [[lattice]] $L$ equipped with a function $\neg: L \to L$ satisfying 
$$a \wedge b \leq c \qquad iff \qquad a \leq \neg b \vee c$$

* A Boolean algebra is a cartesian [[star-autonomous category|*-autonomous poset]] i.e. a [[meet-semilattice]] which is a $*$-autonomous category with tensor product $a \wedge b$ and monoidal unit $\top$. In other words, a Boolean algebra is a cartesian closed poset $P$ together with an object $\bot$ such that $(a \rightarrow \bot) \rightarrow \bot \le a$ for every $a \in P$. 

### Explicitly

There are even two explicit definitions: [[order theory|order-theoretic]] and algebraic.

A __Boolean lattice__ is a [[poset]] such that:

*  there is an element $\top$ (a [[top element]]) such that $x \leq \top$ always holds;
*  there is an element $\bot$ (a [[bottom element]]) such that $\bot \leq x$ always holds;
*  given elements $a$ and $b$, there is an element $a \wedge b$ (a [[meet]] of $a$ and $b$) such that $x \leq a \wedge b$ holds iff $x \leq a$ and $x \leq b$;
*  given elements $a$ and $b$, there is an element $a \vee b$ (a [[join]] of $a$ and $b$) such that $a \vee b \leq x$ holds iff $a \leq x$ and $b \leq x$;
*  given an element $a$, there is an element $\neg{a}$ (a [[complement]] of $a$) such that $a \wedge \neg{a} \leq \bot$ and $\top \leq a \vee \neg{a}$;
*  given elements $a$, $b$, and $c$, we have $a \wedge (b \vee c) \leq (a \wedge b) \vee (a \wedge c)$.

Although we don\'t say so, we can prove that $\top$, $\bot$, $a \wedge b$, $a \vee b$, and $\neg{a}$ are unique; this makes it more clear what the last two axioms actually mean. 

Notice that a poset carries at most one Boolean algebra structure, making it [[stuff, structure, property|property-like structure]]. (The same is true of [[Heyting algebra]] structure.) 

Alternatively, a __Boolean algebra__ is a [[set]] equipped with elements $\top$ and $\bot$, binary operations $\wedge$ and $\vee$, and a unary operation $\neg$, satisfying these identities:

1.  $a \wedge \top = a$,
1.  $a \vee \bot = a$,
1.  $a \wedge (b \wedge c) = (a \wedge b) \wedge c$,
1.  $a \vee (b \vee c) = (a \vee b) \vee c$,
1.  $a \wedge b = b \wedge a$,
1.  $a \vee b = b \vee a$,
1.  $a \wedge (a \vee b) = a$,
1.  $a \vee (a \wedge b) = a$,
1.  $a \wedge (b \vee c) = (a \wedge b) \vee (a \wedge c)$,
1.  $a \vee (b \wedge c) = (a \vee b) \wedge (a \vee c)$,
1.  $a \wedge \neg{a} = \bot$,
1.  $a \vee \neg{a} = \top$.

We can recover the poset structure: $a \leq b$ iff $a \wedge b = a$. There is a certain amount of redundancy or overkill in this axiom list; for example, it suffices to give just axioms 1, 2, 5, 6, 9, 10, 11, 12.  

A very distilled algebraic definition was conjectured by Herbert Robbins: any *nonempty* set equipped with a binary operation $\vee$ and a unary operation $\neg$ obeying

1. associativity: $a\vee \left(b\vee c\right)=\left(a\vee b\right)\vee c$
1. commutativity: $a \vee b = b \vee a$
1. the Robbins equation: $\neg \left(\neg \left(a\vee b\right)\vee \neg \left(a\vee \neg b\right)\right)=a $

is a Boolean algebra.  William McCune proved the conjecture in 1996, using the automated theorem prover EQP.  A short proof was found by Allan Mann (see the references).

#### Principle of duality 

However it is defined, the theory of Boolean algebras is **self-dual** in the sense that for any sentence stated in the language $(\leq, \wedge, \vee, \bot, \top, \neg)$, the sentence is a theorem in the theory of Boolean algebras iff the dual sentence, obtained by interchanging $\wedge$ and $\vee$, $\bot$ and $\top$, and replacing $\leq$ by the opposite relation $\leq^{op}$, is also a theorem. 

This incredibly useful result can be rephrased in several ways; for example, if a poset $B$ is a Boolean algebra, then so is its opposite $B^{op}$. 

#### Boolean rings 

A [[Boolean ring]] is a [[ring]] (with [[identity]]) for which every element is idempotent: $x^2 = x$. Notice that from 

$$x^2 + 1 = x + 1 = (x + 1)^2 = x^2 + 2 x + 1$$ 

the equation $2 x = 0$ follows. Also notice that commutativity comes for free, since 

$$x^2 + y^2 = x + y = (x + y)^2 = x^2 + x y + y x + y^2$$ 

whence $x y + y x = 0 = x y + x y$. 

Parallel to the way free commutative rings are polynomial rings, which are free $\mathbb{Z}$-modules generated from free commutative monoids, the free Boolean ring on $n$ generators may be constructed, &#224; la Beck [[distributive law]]s, as the free $\mathbb{Z}_2$-vector space $\mathbb{Z}_2[M_n]$ generated from the [[semilattice]] $M_n$ on $n$ generators. The latter can be identified with the function set from an $n$-element set to the 2-element [[boolean domain]] $\{0, 1\}$ with multiplication defined elementwise from the [[meet]] of $\{0, 1\}$, and $\mathbb{Z}_2[M_n]$ therefore has $2^{2^n}$ elements. 

The theory of Boolean algebras is equivalent to the theory of Boolean rings in the sense that their categories of models are equivalent. Given a Boolean ring, we define the operation $\wedge$ to be multiplication, and the operation $\vee$ by $x \vee y = x + y + x y$, and the operation $\neg$ by $\neg x = 1 + x$. The relation $x \leq y$ may be defined by the condition $x y = x$. In the other direction, given a Boolean algebra, we may define addition by [[symmetric difference]]: $x + y = (x \vee y) \wedge \neg(x \wedge y)$. According to this equivalence, the free Boolean ring on $n$ generators may be identified with the Boolean algebra $2^{2^n}$, the function set from a set with $2^n$ elements to the [[boolean domain]] $\{0,1\}$. 

### Elements of Stone duality 

The equivalence of Boolean rings and Boolean algebras was exploited by [[Marshall Stone]] to give his theory of [[Stone duality]], in which every Boolean algebra $B$ is a Boolean algebra of sets; more particularly the Boolean algebra of clopen (closed and open) sets of a topological space $Spec(B)$, the **Stone space** of $B$. The notation intentionally suggests that the Stone space is the underlying space of the [[spectrum (geometry)|spectrum]] of $B$ as Boolean ring, taking "spectrum" in the sense of algebraic geometry. 

A Stone space may be characterized abstractly as a [[topological space]] that is [[compact space|compact]], [[Hausdorff space|Hausdorff]], and [[totally disconnected space|totally disconnected]]. Stone duality asserts among other things that every such space is the [[prime spectrum]] of the Boolean algebra of its clopen subsets. 

+-- {: .num_lemma #aremax} 
###### Lemma 
All prime ideals in $B$ are kernels $\phi^{-1}(0)$ of homomorphisms $\phi: B \to \mathbf{2}$ (and thus are maximal ideals, in bijective correspondence with [[ultrafilters]] $\phi^{-1}(1)$ in $B$). 
=-- 

+-- {: .proof} 
###### Proof 
If $p$ is a prime ideal in a Boolean ring, then $B/p$ is an integral domain in which every element $x$ is idempotent: $x(x-1) = 0$. Hence $B/p = \{0, 1\}$. 
=-- 

(To be continued at some point.) 

## Homomorphisms and the category of Boolean algebras

Any [[lattice]] homomorphism automatically preserves $\neg$ and is therefore a Boolean algebra homomorphism.

Boolean algebras and Boolean algebra homomorphisms form a [[concrete category]] [[BoolAlg]]. 

## See also

* [[complete Boolean algebra]]
* [[sigma-complete Boolean algebra|$\sigma$-complete Boolean algebra]]
* [[Boolean algebra object]]
* [[BoolAlg]] - the category of Boolean algebras

## References

* Allan Mann, A complete proof of the Robbins conjecture.  ([pdf](http://math.colgate.edu/~amann/MA/robbins_complete.pdf))

* {#CF77} [[William H Cornish]], [[Peter R Fowler]], *Coproducts of de morgan algebras*, Bulletin of the Australian Mathematical Society, 16(01):1–13, 1977. ([pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/D86F551CF77BE8374CD4BFB1A73F73B6/S0004972700022966a.pdf/coproducts-of-de-morgan-algebras.pdf))

* {#CF79} [[William H Cornish]], [[Peter R Fowler]], *Coproducts of kleene algebras*, Journal of the Australian Mathematical Society (Series A), 27(02):209–220, 1979 ([pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/AAD3D8E6D208205C39C54D0873AEB883/S1446788700012131a.pdf/div-class-title-coproducts-of-kleene-algebras-div.pdf))

* [[Ulrik Buchholtz]], [[Edward Morehouse]], (2017). *Varieties of Cubical Sets*. In: [[Peter Höfner]], [[Damien Pous]], [[Georg Struth]] (eds) *Relational and Algebraic Methods in Computer Science*. RAMICS 2017. Lecture Notes in Computer Science, vol 10226. Springer, Cham. ([doi:10.1007/978-3-319-57418-9_5](https://doi.org/10.1007/978-3-319-57418-9_5), [arXiv:1701.08189](https://arxiv.org/abs/1701.08189))

[[!redirects Boolean algebra]]
[[!redirects Boolean algebras]]
[[!redirects boolean algebra]]
[[!redirects boolean algebras]]

[[!redirects Boolean lattice]]
[[!redirects Boolean lattices]]
[[!redirects boolean lattice]]
[[!redirects boolean lattices]]
