# Clones

* table of contents
{: toc}

## Idea

An __abstract clone__ is a structure that describes a single-sorted [[algebraic theory]] in a presentation-invariant way.

An abstract clone is equivalent to a [[cartesian operad]], that is, a [[cartesian multicategory]] with one object. However, clones are presented differently, and quite economically, with projections rather than with symmetries, contraction and weakening. 

Abstract clones are equivalent to [[Lawvere theories]], and also to [[finitary monads]]. These are all different ways of giving presentation-invariant descriptions of single-sorted algebraic theories. 

## Definition

A set of algebraic operations on a fixed set $S$ is a __concrete clone__
on $S$ if it contains all (component) projections $S^{n}\to S$ and is closed under composition ("superposition").

An **abstract clone** consists of an abstract set of "$n$-ary operations" for every $n$ together with projection and composition operations.  This is the notion that's equivalent to a cartesian operad or a Lawvere theory.


More precisely, the usual presentation of abstract clone comprises 

* a set $T(n)$ for each natural number $n$;

* functions $\eta_n : n \to T(n)$; 

* functions $c_{m,n} : T(m) \times T(n)^m\to T(n)$

such that 

* $\eta(i) \rhd j. t=t$;

* $t \rhd i.\eta(i) =t$;

* $t \rhd i.(u(i) \rhd j.v(j)) = (t \rhd i.u(i)) \rhd j. v(j)$

where we omit subscripts and write $(t \rhd i.u(i))$ for $c(t,(u_i)_i)$. 

This resembles the [[monad (in computer science)#RelationToMonadsInCategoryTheory|Kleisli triple presentation]] of a [[monad]], except that $n$ is a natural number rather than an arbitrary set; in this sense it is the Kleisli triple form of a [[relative monad]] for the embedding $\mathbf{FinSet}\to\mathbf{Set}$. 

## Examples

### Concrete clones as abstract clones

Suppose a concrete clone is given on a set $S$, i.e. a set of operations $S^n\to S$ of different arities, closed under composition and containing all the projections. We regard this as an abstract clone by putting $T(n)$ as the set of admitted operations $S^n\to S$. The functions $\eta_n$ pick out the projections, and $c_{m,n}$ is multi-ary function composition. 

### Abstract clones from algebraic signatures

An [[signature (in logic)|algebraic signature]] comprises, for each number $n$, a set $\Sigma_n$ of formal $n$-ary operations. For example, the theory of groups has $\Sigma_0=\{1\}$; $\Sigma_1=\{(-)^{-1}\}$; $\Sigma_2=\{\cdot\}$. 

We then build for all $n$ the terms in $n$ variables, written $x_1\dots x_n\vdash x_i$, by the following inductive definition: 

* $x_1\dots x_n\vdash x_i$ is a term if $1\leq i\leq n$;

* if $n\vdash t_1\ \ \dots\ \  n\vdash t_m$ are terms and $\sigma\in \Sigma_m$ then $n\vdash \sigma(t_1,\dots, t_m)$ is a term. Here we write $n =(x_1\dots x_n)$. 

Now we form an abstract clone by putting $T_\Sigma(n)=\{t\ \ |\ \ (n\vdash t\ \ \text{ is a term})\}$. 
The functions $\eta_n$ picks out the variables, and the function $c_{m,n}$ amount to substitutions of terms for variables, which produces well-formed terms. 

The inhabitants of $T_\Sigma$ are sometimes called "derived operations", since although they are not in the signature they have an interpretation in any model. 

### Abstract clones from presentations of algebraic theories

An algebraic theory over a signature is given by a collection of axioms of the form $\Gamma\vdash t=u$, where $\Gamma \vdash t$ and $\Gamma \vdash u$. We then form  equivalence relations $\sim_n$ of terms by closing under substitution instances, congruence, and reflexivity, symmetry and transitivity. These are the equations that are true in all models of the theory. 

We can now form an abstract clone for the theory, derived from the abstract clone for the signature. Put $T(n)=T_\Sigma(n)/_{\sim_n}$. The $\eta$ and $c$ respect equivalence relations because we closed under substitution instances and congruence. 

For example, starting from the theory of groups, $T(n)$ will be the free group on $n$ generators. 

### Algebraic theories from abstract clones

Conversely, any abstract clone can be regarded as a presentation of an algebraic theory. The signature has $\Sigma_n=T(n)$, and we include the axioms

* $\eta_n(i) = x_i$

* $s(t_1\dots t_n) = (s \rhd i. t(i))$.

An abstract clone is a presentation of a "saturated" algebraic theory: all derived operations are equivalent to basic operations that are already in the signature. 

### Lawvere theories and abstract clones

If $T$ is an abstract clone, we can form a category whose objects are natural numbers and where a morphism $m\to n$ is a tuple $T(m)^n$. The identity morphisms are $\eta_n$. Composition is $(g\circ f)(i)=(g(i)\rhd j.f(j))$. This category is a [[Lawvere theory]]. 

(This is the [[opposite category]] of the [[Kleisli category]] of $T$ regarded as a [[relative monad]].)

Conversely, if $L$ is a Lawvere theory then we can build a clone $T(n)=L(n,1)$. This gives an equivalence between abstract clones and Lawvere theories.  

## Algebras of abstract clones and connection with finitary monads 

We can define an __algebra of an abstract clone $T$__ to be a set $X$ together with $n$-ary function $t \rhd : X^n\to X$ for each $t\in T(n)$, such that 

* $\eta_i \rhd i.x(i)= x(i)$; 

* $(t\rhd i.u(i))\rhd j.x(j)= t\rhd i.(u(i)\rhd j.x(j))$.

Here we are writing $\rhd$ for both the clone composition and the algebra structure, and again writing $t \rhd i.x(i)$ for $t\rhd(x_i)_i$.

For example, an algebra for the abstract clone of groups is a group. 

Now the category of $T$-algebras has a forgetful functor 

$$ T\mathbf{-Alg} \to \mathbf{Set}$$

One can show that this functor is [[monadic]] by showing it preserves limits, satisfies the solution set condition, reflects isomorphisms, and has reflexive coequalizers. Thus every abstract clone gives rise to a monad. 

Another way to define this monad is to note that $T$ can be regarded as a functor $\mathbf{FinSet}\to \mathbf{Set}$, with $T(f):T(m)\to T(n)$ given by $T(f)(t)=(t\rhd i.\eta(f(i)))$. 
Then we extend this to a functor $M:\mathbf{Set}\to\mathbf{Set}$ by a [[coend]] or by [[Kan extension]]:

$$ M(X) = \int^n T(n)\times X^n = (\mathrm{Lan}\,T)(X)$$

In other words, an inhabitant of $M(X)$ is a derived operation $t\in T(n)$ formally applied to an $n$-tuple in $X^n$, modulo change of variables. 
This functor $M$ can be given the structure of a monad on $\mathbf{Set}$, and its [[Eilenberg-Moore algebras]] are the $T$-algebras.

Conversely, suppose that $M$ is a [[monad]] on the category of sets. We can define an abstract clone by regarding a natural number $n$ as a finite set and putting $T(n)=M(n)$. Then $\eta$ is the unit of the monad and $c$ is the Kleisli composition (called "monadic bind").  

This gives an equivalence between [[finitary monads]] and abstract clones. They are also the [[monad with arities|monads with arities]] in $\mathbf{FinSet}$.


## Monadicity of the category of abstract clones

The definition of abstract clones given here is itself a presentation of algebraic structure. Indeed we can consider an obvious notion of homomorphism of clones, and then the forgetful functor 

$$ \mathbf{AbstractClones} \to [\mathbf{FinSet},\mathbf{Set}]$$

is [[monadic]]. 

In fact this adjunction is [[enriched]] in $[\mathbf{FinSet},\mathbf{Set}]$. Moreover, we can consider a more general notion of abstract clone enriched in a [[locally presentable category]], where the arities $n$ are replaced by finitely presentable objects. Then the plain abstract clones themselves are algebras for an abstract clone enriched in $[\mathbf{FinSet},\mathbf{Set}]$. One way to present this formally is in terms of the substitution algebras of Fiore, Plotkin and Turi.

Another view of this adjunction starts from viewing $[\mathbf{FinSet},\mathbf{Set}]$ as a [[monoidal category]]. To get this, we can understand functors $\mathbf{FinSet}\to \mathbf{Set}$ as [[filtered colimit]] preserving endofunctors $\mathbf{Set}\to\mathbf{Set}$, and then composition forms a monoidal structure on a category of endofunctors. In detail, the unit is $\mathbf{FinSet}(1,-)$ and tensor product is 

$$(F \otimes G) (n) = \int^m F(m) \times G(n)^m = ((\mathrm{Lan}\,F)\circ G)(n)$$

Then the category of abstract clones is (equivalent to) the category of [[monoids]] for this monoidal structure. Since a finitary monad is a filtered-colimit-preserving "monoid in the category of endofunctors", this also gives an abstract view of the connection between abstract clones and finitary monads on $\mathbf{Set}$.

## References 

* &#193;gnes Szendrei, _Clones in universal algebra_, S&#233;minaire de math&#233;matiques sup&#233;rieures 99, Les presses de l'universit&#233; de Montreal, 1986. &#8212; 166 p.

A rather general framework is discussed in 

* Zhaohua Luo, _Clone theory, its syntax and semantics, applications to universal algebra, lambda calculus and algebraic logic_, [arxiv/0810.3162](https://arxiv.org/abs/0810.3162)
* Dietlinde Lau, _Function algebras on finite sets: Basic course on many-valued logic and clone theory_, Springer Monographs in Mathematics

A common generalization of a clone and of an operad is proposed, using a new notion of a verbal category, in

* S. Tronin, _Abstract clones and operads_, Siberian Mathematical Journal 43, No.4, 746&#8211;755, 2002 [link](http://rd.springer.com/content/pdf/10.1023%2FA%3A1016340806503.pdf)

Another unification of clones and operads is via the formalism in

* Pierre-Louis Curien, _Operads, clones, and distributive laws_, [arxiv/1205.3050](https://arxiv.org/abs/1205.3050)

See also the thesis 

* Miles Gould, _Coherence for operadic theories_, Glasgow 2009 [pdf](http://theses.gla.ac.uk/689/1/2009gouldphd.pdf)

Algebraic theories are treated as abstract clones in the enriched setting (but abstractly), and monadicity is dealt with, in 

* [[Max Kelly]], [[John Power]], _Adjunctions whose counits are coequalizers, and presentations of finitary enriched monads_. JPAA 1993. [doi:10.1016/0022-4049(93)90092-8](https://doi.org/10.1016/0022-4049%2893%2990092-8).

Substitution algebras as a theory over $[\mathbf{FinSet},\mathbf{Set}]$ are presented in: 

* [[Marcelo Fiore]], [[Gordon Plotkin]] and Daniele Turi. Abstract syntax and variable binding. Proc LICS 1999. [preprint](https://www.dcs.ed.ac.uk/home/dt/FiorePlotkinTuri.pdf). 

One description of enriched abstract clones is in Section 5 of 

* [[Sam Staton]], An algebraic presentation of predicate logic. FOSSACS 2013. [preprint](http://www.cs.ox.ac.uk/people/samuel.staton/papers/fossacs13.pdf).

[[!redirects clones]]
[[!redirects cartesian operad]]
[[!redirects cartesian operads]]
