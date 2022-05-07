
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--





#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

An **operad** is a gadget used to describe algebraic structures in [[symmetric monoidal category|symmetric monoidal categories]].  It is

* a bunch of abstract _operations_ of arbitrarily many arguments;

* equipped with a notion of how to compose these;

* subject to evident [[associativity]] and [[unitality]] conditions.

An [[algebra over an operad]] is a concrete realization of these abstract operations: an [[object]] $A$ equipped with $n$-ary operations $A \otimes \cdots \otimes A \to A$ as specified by the operad, subject to the composition relation as specified by the operad.

This way an operad is like a [[Lawvere theory]] in that it can be used to describe algebraic structures having finitary operations obeying equational laws.  However, unlike Lawvere theories, operads can be defined internal to general [[symmetric monoidal categories]] where the [[tensor product]] might not be the [[cartesian product]]. 

The notion of operad (and allied notions such as [[PROP]], [[club]], [[multicategory]] and so on) come in many flavors. Originally used in [[algebraic topology]] to provide a systematic formalism for describing the internal operations which exist on iterated [[loop space]]s, the basic idea is quite flexible and adaptable to many categorical situations, and the importance of operads continues to grow. 

## Definition in components

The original definition is due to [[Peter May]] and was given in his book ([The Geometry of Iterated Loop Spaces](#May1972)). It describes an operad as a collection of operations equipped with a notion of composition and subject to various conditions. 

This definition is essentially that of an [[enriched category]], only that the [[hom-object]]s are allowed to go from more than one object to a given output object.

There is a more abstract way to encode all this simply as a [[monoid in a monoidal category|monoid]] in a suitable ambient [[monoidal category]]. This more abstract definition we discuss below in [A detailed conceptual treatment](#Conceptual).


### Symmetric operads {#PedestrianDefOperad}

Let $V$ be a [[symmetric monoidal category]]. A 
( _permutative_ or _[[symmetric operad|symmetric]]_) **operad** in $V$ consists of objects $F(n)$ of $V$ indexed over the [[natural number]]s $n = 0, 1, 2, \ldots$ [which we intuitively think of as "objects that parametrize the $n$-ary operations of an algebraic theory"] equipped with the following extra structure: 

* Right [[actions]] of [[symmetric group]]s $\rho_n: S_n \to \hom(F(n), F(n))$; 
* A _unit_ $e: I \to F(1)$ [which we think of as picking out the identity map as unary operation]; 
* Composition operations 
$$F(k) \otimes F(n_1) \otimes F(n_2) \otimes \cdots \otimes F(n_k) \to F(n_1 + \ldots + n_k)$$
(which we think of as the result of plugging the outputs of operations $\theta_1, \ldots, \theta_k$ into a $k$-ary operation $\theta$, to produce a new operation $\theta \circ (\theta_1 \otimes \ldots \otimes \theta_k)$). 

These data are subject to obvious identities such as [[associativity]] and [[unitality]] of composition, and compatibility of composition with symmetric group actions. For example, the unit laws say that the evident composite 

$$F(n) \cong I \otimes F(n) \stackrel{e \otimes 1}{\to} F(1) \otimes F(n) \stackrel{comp}{\to} F(n)$$ 

is the identity map, as is 

$$F(n) \cong F(n) \otimes I^{\otimes n} \stackrel{1 \otimes e^{\otimes n}}{\to} F(n) \otimes F(1)^{\otimes n} \stackrel{comp}{\to} F(n)$$ 

Compatibility with symmetric group actions means that for each element $\sigma \in S_k$, the composition operation 

$$F(k) \otimes \bigotimes_{i = 1}^k F(n_i) \to F(n_1 + \ldots + n_k)$$ 

coequalizes a pair of automorphisms 

$$\rho(\sigma) \otimes 1, 1 \otimes \lambda(\sigma): F(k) \otimes \bigotimes_{i=1}^k F(n_i) \;\rightrightarrows\; F(k) \otimes \bigotimes_{i=1}^k F(n_i)$$ 

where $\sigma$ acts on the big tensor product on the left by permuting tensor factors in the obvious way. If $V$ has suitable colimits, this condition could be expressed in terms of tensor products over $S_n$. 

The associativity condition will be left for others to fill in. 

### Coloured operads {#PedestrianDefColouredOperad}

There is an evident generalization of the above where we allow the operad to have several [[object]]s -- called _colours_ in operad theory. This models algebraic structures where elements of different _types_ may be fed into $n$-ary operations.

Let $C$ be a [[set]], called the _set of colours_ . Then a **coloured operad** is 

* for each $n \in \mathbb{N}$ and each $(n+1)$-tuple $(c_1, \cdots c_n, c)$ an object $P(c_1, \cdots, c_n;c) \in V$;

* for each $c \in C$ a morphism $1_c : I \to P(c;c)$ in $V$ -- the _identity_ on $c$; 

* for each $(n+1)$-tuple $(c_1, \cdots, c_n, c)$ and $n$ other tuples

  $(d_{1,1}, \cdots, d_{1,k_1}), \cdots, (d_{n,1}, \cdots, d_{n,k_n})$

  a morphism

  $$
    P(c_1, \cdots, c_n; c) \otimes P(d_{1,1}, \cdots, d_{1,k_1}; c_1)
    \otimes \cdots \otimes P(d_{n,1}, \cdots, d_{n,k_n}; c_n)
    \to 
    P(d_{1,1}, \cdots, d_{n,k_n}, c)
  $$

  the _composition_ operation;

* for all $n$, all tuples, and each [[permutation]] $\sigma$ in the [[symmetric group]] $\Sigma_n$ a morphism

  $$
    \sigma^* : P(c_1, \cdots, c_n;c) \to P(c_{\sigma(1)}, \cdots, c_{\sigma(n)};c)
  $$

* subject to the conditions that

  * the $\sigma$s form a [[representation]] of $\Sigma_n$;

  * the composition operation satisfies [[associativity]] and [[unitality]] in the obvious way;

  * and is $\Sigma_n$ equivariant in the evident way.

An equivalent term for a colored operad in $V$ is a [[symmetric multicategory]] which is [[enriched category|enriched]] over $V$.  Which term is used depends on the author and the point of view being taken.  (According to the common terminology of [[horizontal categorification]], one might also call a colored operad an "operad-oid," but thankfully this seems not to be common.  On the other hand one might adapt the terminology backwards and call a [[category]] a "colored [[monoid]]" or call a [[groupoid]] a "colored [[group]]".)


### Algebras 

An _[[algebra over an operad]]_  $F$ in $V$ is just a semantics for interpreting the $F(n)$ as objects of actual $n$-ary operations on an object $v$. That is, an $F$-algebra structure on an object $v$ in $V$ consists of a collection of maps 

$$F(n) \otimes v^{\otimes n} \to v$$ 

which intuitively is a mapping like this: 

$$\theta \otimes x_1 \otimes \ldots \otimes x_n \mapsto \theta(x_1, \ldots, x_n)$$ 

so that "elements" of $F(n)$ are interpreted as as $n$-ary operations on $v$. These data are subject to some natural conditions which implement this idea. 

Perhaps the quickest way to define it is to suppose that $V$ is symmetric monoidal [[closed monoidal category|closed]], and work by way of parallel to how [[representations]] or [[modules]] work. Just as an $R$-module (over a ring $R$) can be defined as a ring homomorphism 

$$R \to \hom(A, A)$$ 

where the hom here is an internal hom of abelian groups, called an _[[endomorphism ring]]_, so there is such a thing as an _[[endomorphism operad]]_ attached to any object $v$ in a symmetric monoidal closed category, and an $F$-algebra over an operad $F$ is the same thing as an operad morphism 

$$F \to \hom(v^{\otimes \bullet}, v)$$ 

to an endomorphism operad (also called a _tautological operad_). 

Now that the clue has been given, the rest is not hard to figure out. The components of the endomorphism operad are defined by 

$$End(v)(n) = \hom(v^{\otimes n}, v)$$ 

Certainly $S_n$ acts on the right (that is, contravariantly) on the [[hom-object]] $\hom(v^{\otimes n}, v)$. And clearly there is a canonical map $e: I \to \hom(v, v)$ to play the role of the unit. The operad composition involves an instance of enriched functoriality of iterated tensor products: there is a map 

$$\hom(v^{\otimes n_1}, v) \otimes \ldots \otimes \hom(v^{\otimes n_k}, v) \to \hom(v^{n_1 + \ldots + n_k}, v^{\otimes k})$$

The endomorphism operad composition is obtained by tensoring this last arrow with $\hom(v^{\otimes k}, v)$ on the left, and composing the result with ordinary internal hom-composition 

$$\hom(v^{\otimes k}, v) \otimes \hom(v^{\otimes n_1 + \ldots + n_k}, v^{\otimes k}) \to \hom(v^{\otimes n_1 + \ldots + n_k}, v)$$ 

A closely related way of defining an $F$-algebra is via the monad attached to an operad, which we will describe below.

Note that this definition still makes sense when $v$ lives in any symmetric monoidal $V$-[[enriched category]], not only $V$ itself.


## A detailed conceptual treatment 
 {#Conceptual}

We describe here a compact one-sentence definition of operad first worked out by [[Max Kelly]], after a few preliminaries which are important in their own right. The treatment is essentially an exercise in [[enriched category theory]] and the formalism of [[Day convolution]]. We will work this out fully in the case of ordinary [[category theory]] first, that is for categories [[enriched category|enriched in]] $V = Set$; the case for categories enriched in a complete, cocomplete, [[symmetric monoidal category|symmetric monoidal]] [[closed monoidal category|closed]] $V$ is completely parallel. 

More details along these lines are add _[[toddtrimble:Towards a doctrine of operads]]_.

### Preparation 

Let $\mathbb{P}$ be the [[groupoid]] of finite cardinals with [[bijections]] as morphisms --  the _[[permutation category]]_. Since $\mathbb{P}$ is the [[core]] groupoid of the category $Fin$ of finite cardinals and functions between them, the [[coproduct]] on $Fin$ restricts to a symmetric monoidal product called the cardinal sum on $\mathbb{P}$. 

+-- {: .un_remark style="margin-left:2em"}
###### Remark
Under this symmetric monoidal structure, $\mathbb{P}$ may be characterized as the free symmetric strict monoidal category on one generator.
=--

The cardinal sum on $\mathbb{P}$ extends along the [[Yoneda embedding]] to a symmetric monoidal product $F \otimes G$ on the [[presheaf category]] $Psh(\mathbb{P}):=[\mathbb{P}^{op},Set]$. This is an instance of the [[Day convolution]]. 

+-- {: .un_note style="margin-left:2em"}
###### Warning
By abuse of notation, we will also denote the presheaf category $Psh(\mathbb{P})$ equipped with the monoidal structure induced by the cardinal sum by $Psh(\mathbb{P})$.
=--

Since $Psh(\mathbb{P})$ is a presheaf category, it is cocomplete, and since the Day convolution is [[cocontinuous functor|cocontinuous]] in each of its separate arguments we say that $Psh(\mathbb{P})$ is **symmetric monoidally cocomplete**. 

+-- {: .un_note style="margin-left:2em"}
###### Note
In addition to the standard [[coend]] formula, the Day convolution product on the $Psh(\mathbb{P})$ may be described by the rule:

$$(F \otimes G)[S] = \sum_{S = T + U} F[T] \times G[U],$$ 

summing over all partitions of $S$ into two parts (each possibly empty). 
=--

According to the yoga of presheaf categories and Day convolution, given a symmetric monoidally cocomplete category $D$, a symmetric monoidal functor 

$$X: \mathbb{P} \to D$$

extends uniquely up to isomorphism to a symmetric monoidal _cocontinuous_ functor 

$$\hat{X}: Psh(\mathbb{P}) \to D,$$ 

taking a presheaf $W: \mathbb{P}^{op} \to Set$ to the [[weighted colimit]] $W \cdot X$.  

+-- {: .un_remark style="margin-left:2em"}
###### Remark
It follows from the earlier remark and the above that we may describe $Psh(\mathbb{P})$ universally up to equivalence as the free symmetric monoidally cocomplete category on a single generator.
=--

+-- {: .un_note style="margin-left:2em"}
###### Digression
Recall that we can describe $W \cdot_{\mathbb{P}} X$ as follows: First note that the functor 

$$\Lambda_0:=Hom_D(X(\cdot),\cdot):\mathbb{P}^{op}\times D\to Set,$$ 

so $\Lambda_0$ also gives a functor $\Lambda: D\to [\mathbb{P}^{op},Set]$ by [[currying]] through the second coordinate. 

Then we define $W \cdot_{\mathbb{P}} X$ to be the object representing the functor 

$$\Lambda_W:=Hom_Psh(\mathbb{P})(W,\Lambda(\cdot)):D\to Set$$ 

whenever $\Lambda_W$ is [[representable functor|representable]].

In general, weighted colimits may be described explicitly by coend formulas; here 

$$W \cdot_{\mathbb{P}} X = \int^{k: \mathbb{P}} F(k) \cdot X(k)$$ 

where $S \cdot d$ denotes the tensoring of a set $S$ with an object $d$, that is the coproduct of an $S$-indexed set of copies of $d$. The coend here indicates a coequalizer.

$$\sum_k W(k) \cdot S_k \cdot X(k) \rightrightarrows \sum_k W(k) \cdot X(k) \to \int^k W(k) \cdot X(k)$$ 

where one of the parallel arrows involves right actions of symmetric groups $S_k$ on the $F(k)$, and the other involves left actions of $S_k$ on objects $X$. In other words, the coend in this instance may be described as a sum of tensor products: 

$$W \cdot_{\mathbb{P}} X = \sum_k W(k) \otimes_{S_k} X(k).$$
=--

The aforementioned universal property of $Psh(\mathbb{P})$ with its convolution product may be more explicitly described as follows: given a symmetric monoidally cocomplete category $D$ and an object $d$ therein, there exists up to isomorphism a _unique_ symmetric monoidal cocontinuous functor $Psh(\mathbb{P}) \to D$ which sends the presheaf representable by the cardinal $1$, $h_1$, to $d$. 

Explicitly, this functor takes a presheaf $F: \mathbb{P}^{op} \to Set$ to the following object of $D$: 

$$\sum_k F(k) \otimes_{S_k} d^{\otimes k}.$$

+-- {: .num_example style="margin-left:2em" #analytic}
###### Example
When $D$ is the symmetric monoidally cocomplete category $(Set, \times)$ and $x$ is a set, this formula 

$$\hat{F}(x) = \sum_k F(k) \otimes_{S_k} x^k$$ 

is the value at $x$ of what Joyal calls the _analytic functor_ $\hat{F}: Set \to Set$ associated to a [[combinatorial species|species]] $F$, which has been proposed as the categorification of the theory of exponential [[generating function]]s. The fact that $F \mapsto \hat{F}(x)$ is symmetric monoidal (cocontinuous) means that there is a canonical isomorphism

$$\widehat{(F \otimes_{Day} G)}(x) \cong \hat{F}(x) \times \hat{G}(x)$$ 

In other words, $F \mapsto \hat{F}$ behaves like a categorified version of Fourier transform, taking convolution products to ordinary (pointwise) products. 
=--

+-- {: .un_definition}
For symmetric monoidally cocomplete categories $C, D$, let $\underline{Hom}(C, D)$ denote the category of symmetric monoidal cocontinuous functors $C \to D$. The universal property of $Psh(\mathbb{P})$ means that we have an equivalence 

$$\underline{Hom}(Psh(\mathbb{P}), D) \simeq D.$$ 

Consequently, we have an equivalence $\underline{Hom}(Psh(\mathbb{P}), Psh(\mathbb{P})) \simeq Psh(\mathbb{P}).$ 

Since symmetric monoidal cocontinuous functors are stable under composition, the category on the left carries a monoidal product given by endofunctor composition. By transport of structure across the equivalence, we  induce a monoidal product on $Psh(\mathbb{P})$ given by endofunctor composition called the _substitution product of species_. The substitution product of species $F, G$ is denoted $F \circ G$. 
=--

In detail: a species $G: \mathbb{P}^{op} \to Set$ induces a symmetric monoidal cocontinuous functor 

$$Psh(\mathbb{P}) \to Psh(\mathbb{P}): F \mapsto F \circ G = \sum_k F(k) \otimes_{S_k} G^{\otimes_{Day} k}$$ 

The $k$-fold Day tensor power of $G$ is given (in the language of species) by the formula 

$$G^{\otimes k}[S] = \sum_{S = T_1 + \ldots + T_k} G[T_1] \times G[T_2] \times \ldots \times G[T_k]$$ 

where we sum over all ways of breaking up a finite set $S$ into $k$ blocks, some possibly empty. Thus we have an explicit description of the substitution product, 

$$(F \circ G)[n] = \sum_k F[k] \otimes_{S_k} (\sum_{[n] = T_1 + \ldots + T_k} G[|T_1|] \times \ldots \times G [|T_k|]),$$ 

and it is clear from our discussion above that substitution is a monoidal product. The monoidal unit $I$ is a functor $\mathbb{P}^{op} \to Set$ where $I[n]$ is terminal if $n = 1$, else is initial. 

### Definition as monoid 
 {#DefinitionAsMonoid}

We are at last ready for the one-sentence **definition**: 

A ($Set$-based) **operad** is a [[monoid in a monoidal category|monoid]] in the [[monoidal category]] $(Psh(\mathbb{P}), \circ, I)$. 

### Remarks 

* {#CartesianOperads} We can get different flavors of operads by considering different notions of ambient [[monoidal category]]. For instance, for the theory of monoidal categories, the discrete category $\mathbb{N}$ plays the role of the free (strict) monoidal category on one generator, and $Set^{\mathbb{N}^{op}}$ the free monoidally cocomplete category on one generator. Similarly, for braided monoidal categories, we have the braid category $\mathbb{B}$, and $Set^{\mathbb{B}^{op}}$ is the free braided monoidally cocomplete category on one generator. Again, for cartesian categories, we have $Fin^{op}$ (the opposite of finite sets and functions) as the [[free cartesian category]] on one generator, and $Set^{Fin}$ is the free cartesian monoidally cocomplete category on one generator. In each of these cases we get a corresponding notion of operad by following the above treatment _mutatis mutandis_: nonpermutative operads, braided operads, cartesian operads (better known as [[Lawvere theory|Lawvere theories]]).  These are all special cases of the notion of [[generalized multicategory]].

* All of the above carries over to the enriched setting, where we work over a complete, cocomplete symmetric monoidal closed base category $V$. Here ordinary categories (like $\mathbb{N}, \mathbb{P}, \mathbb{B}, Fin$) are viewed as $V$-enriched by a simple change of base: change from [[hom-set]]s to [[hom-objects]] by applying the change of base functor 
$$Set \to V$$ 
that takes a set $S$ to the $S$-fold coproduct $S \cdot I$, where $I$ is the monoidal unit of $V$.  These can also be defined in the framework of [[generalized multicategories]].

* The notion of generalized muticategories is even more general than this; for instance it also includes [[globular operads]] and [[topological spaces]].  See [[generalized multicategory]] for details.

* In still other directions, there are for example notions of [[cyclic operad]] and [[modular operad]]. 

* It is sometimes useful to consider an alternative definition of operad based on "partial" composition operations
$$sub_i: C(m) \times C(n) \to C(m+n-1)$$ 
which encode the idea of substituting an $n$-ary operation into the $i-th$ argument of an $m$-ary operation, to get an $(m+n-1)$-ary operation. 
For example, this notion of composition allows the consideration of [[non-unital operad]]s without identity operations (called "pseudo-operads" by [(Markl, Shnider, and Stasheff)](#MarklShniderStasheff)).
On the other hand, in the presence of identity operations, the two forms of operadic composition are mutually definable (see Proposition 13 of [(Markl 2008)](#Markl2008), or Chapter 2 of [(Fresse, HOGTG I)](#FresseHOGTG) for a more detailed discussion).

* Finally, some authors place restrictions on operations of arity zero (a.k.a. nullary operations, or "constants"). May's original definition [(1972)](#May1972) required exactly one nullary operation, while the definition in [(Markl, Shnider, and Stasheff)](#MarklShniderStasheff) considers only operations of positive arity.
Fresse gives a special status to these two restricted forms of operads, referring to them respectively as **unitary operads** and **non-unitary operads** (see 3.1.10 of [(Fresse 2009)](#FresseMOF) and 1.1.19 [(Fresse, HOGTG I)](#FresseHOGTG)).
Beware that non-unitary operads (which have no nullary operations) are _not_ the complement of unitary operads (which have exactly one nullary operation), nor are they the same thing as non-unital operads (which have no identity operation).
As an example, Stasheff's original presentation of the [[associahedra]] [(Stasheff 1963)](#Stasheff63a) implicitly defined an operad which was _both_ non-unitary and non-unital.

## The monad attached to an operad 

Each $Set$-based operad $M$ gives rise to a monad $\hat{M}$ on $Set$. Specifically, the monoidal category $(Psh(\mathbb{P}), \circ, I)$ acts on $Set$ in such a way as to give an [[actegory]] structure, and therefore an operad or $\circ$-monoid gives rise to a monad on $Set$. 

Here are the details. There is a functor 

$$i: Set \to Psh(\mathbb{P})$$ 

which sends a set $X$ to the functor

$$\hat{X}: \mathbb{P}^{op} \to Set$$ 

taking $[n]$ to $X$ if $n = 0$, else to $0$. This functor is full and faithful; conceptually, it treats a set $X$ as giving a set of 0-ary operations or constants indexed by itself. Notice that the composite 

$$Psh(\mathbb{P}) \times Set \stackrel{1 \times i}{\to} Psh(\mathbb{P}) \times Psh(\mathbb{P}) \stackrel{\circ}{\to} Psh(\mathbb{P})$$ 

factors through the inclusion $i: Set \to Psh(\mathbb{P})$ (conceptually, when one applies a formal operation to constants, the result is again a constant). This gives an action

$$Psh(\mathbb{P}) \times Set \to Set$$ 

for an actegory structure; as it is the restriction of the substitution product $\circ$ along the inclusion $i$ in the second argument, we again denote it $\circ$, by abuse of notation. Given $F: \mathbb{P}^{op} \to Set$ and a set $X$, we have 

$$F \circ X \cong \sum_{k \geq 0} F(k) \otimes_{S_k} X^k$$ 

and given $G: \mathbb{P}^{op} \to Set$, we also have coherent natural isomorphisms $(F \circ G) \circ X \cong F \circ (G \circ X)$, $I \circ X \cong X$. 

+-- {: .un_def} 
######Definition 
The **monad** associated with an operad $(M, m: M \circ M \to M, u: I \to M)$ is the functor $\hat{M}: Set \to Set$ taking $X$ to $M \circ X$, equipped with natural transformations 

$$\hat{M} \hat{M} X = M \circ (M \circ X) \cong (M \circ M) \circ X \stackrel{m \circ X}{\to} M \circ X = \hat{M} X$$ 

[ ] 

$$X \cong I \circ X \stackrel{u \circ X}{\to} M \circ X = \hat{M} X$$ 

which provide $\hat{M}$ with the structure of a monad. 
=-- 

This definition of the associated monad carries over with ease to the enriched case, and to variants such as nonpermutative operads, braided operads, and cartesian operads (Lawvere theories). 

Notice that an algebra for the operad $\hat{M}$ is a set $X$ equipped with a structure map $\alpha: M \circ X \to X$ which makes $i(X)$ a [[module]] over the monoid $M$ in the monoidal category $Psh(\mathbb{P})$. 

See also related discussion at [[club]]. 

## Examples 

Ambient categories of relevance in practice are

* [[Top]]/[[sSet]] -- an operad in here is called a [[topological operad]];

* [[category of chain complexes]] -- an operad in here is called a [[dg-operad]]

### Specific examples

* [[endomorphism operad]]

* [[associative operad]]

  * [[A-infinity operad]]

* [[commutative operad]]

  * [[little cubes operad|E-k operad]]

    * [[E-infinity operad]]

    * [[framed little 2-disk operad]]
    
    * [[framed little n-disk operad]]

    * [[Fulton-MacPherson operad]]

* [[operad for modules over an algebra]]

* [[Lie operad]]

  * [[L-∞ operad]]

* [[Eilenberg-Zilber operad]]

* [[linear operad]]

* The [[Goodwillie derivatives of the identity functor]] form an operad in [[spectra]]


### General

* For $C$ a set, the [[initial object]] $I_C$ of $C$-coloured operads has $I_C(c;c) = I_V$ for all $c$ in $C$ and all other components of $I_C$ are the [[initial object]] of $V$.


* There is also a canonical notion of [[free operad]].

## Properties

### Change of colour

Coloured operads form a [[fibered category]] over the category [[Set]] of colours. The fiber over a set $C$ is the category of $C$-coloured operads. 

For $\alpha : D \to C$ a [[function]] of sets, there is an evident pullback functor

$$
  \alpha^* : Oper_C(V) \to Oper_D(V)
$$

given by

$$
  \alpha^*(P)(d_1, \cdots, d_n; d) :=
  P(\alpha(d_1), \cdots, \alpha(d_n); \alpha(d))
  \,.
$$

Together with a morphism $\phi : Q \to \alpha^* P$ of operads this 
induces a pair of [[adjoint functor]]s on [[algebra over an operad|algebras over an operad]]

$$
 ( (\alpha,\phi)_! \dashv (\alpha,\phi)^* )
  :
 Alg_V(P) \stackrel{\overset{(\alpha,\phi)_!}{\leftarrow}}{\underset{(\alpha,\phi)^*}{\to}} Alg_V(Q) 
  \,.
$$

### Model structures on operads 


If the [[symmetric monoidal category]] $V$ that the operads under consideration are enriched in carries the structure of a [[monoidal model category]], then under suitable conditions there is also the structure of a [[model category]] on the category of $V$-operads. This is important for the notion of _homotopy_ [[algebra over an operad]], such as $A_\infty$- and $E_\infty$-algebras.

See 

* [[model structure on operads]].

### Koszul duality

On [[quadratic operads]] in chain complexes there is a duality operation called [[Koszul duality]]. See there for details.

### The category of operads

Operads and operad [[homomorphisms]] (for any given flavor of operads, as discussed above) form a [[category]], _[[Operad]]_.

The [[Boardman-Vogt tensor product]] makes the category of symmetric colored operads over [[Set]] into a [[closed monoidal category]].



## Related concepts

* [[symmetric colored sequence]]

* [[algebraic theory]] / [[Lawvere theory]] /  [[(∞,1)-algebraic theory]]

* [[monad]] / [[(∞,1)-monad]]

* **operad** / [[(∞,1)-operad]]

  * [[multicategory]], [[polycategory]]

  * [[cooperad]]

* [[properad]]

* [[PROP]]

* [[cohomology of operads]]

* [[club]]

## References

Stasheff implicitly described the operad of [[associahedra]] in

* {#Stasheff63a} [[James Dillon Stasheff]], _Homotopy associativity of H-spaces I_, Trans. Amer. Math. Soc. 108 (1963), 275--312.  ([web](http://www.jstor.org/stable/1993608))

* [[James Dillon Stasheff]], _Homotopy associativity of H-spaces II_, Trans. Amer. Math. Soc. 108 (1963), 293--312.  ([web](http://www.jstor.org/stable/1993609))

but without making the abstract concept of operad explicit.
The abstract definition (as well as the name) is originally due to

* {#May1972} [[Peter May]], _The geometry of iterated loop spaces_ ([pdf](http://www.math.uchicago.edu/~may/BOOKS/gils.pdf))

An earlier version was the notion of [[analyser]] (known usually by French version *analyseur*), introduced in

* M. Lazard, _Lois de groupes et analyseurs_, Ann. &#201;cole Norm. Sup. __72__  (1955), pp. 299&#8211;400. 

Monographs include:

* [[Igor Kriz]], [[Peter May]], _Operads, algebras, modules and motives_, Ast&#233;risque __233__, Soci&#233;t&#233; Math&#233;matique de France (1995).

* [[Tom Leinster]], _Higher operads, higher categories_, London Math. Soc. Lec. Note Series __298__, [math.CT/0305049](http://arxiv.org/abs/math.CT/0305049)

* {#MarklShniderStasheff} [[Martin Markl]], [[Steve Shnider]], [[Jim Stasheff|James D. Stasheff]], _Operads in algebra, topology and physics_, Math. Surveys and Monographs __96__, Amer. Math. Soc. 2002.

* {#Markl2008} [[Martin Markl]], Operads and PROPS, In volume 5 of _Handbook of Algebra_, pages 87&#8211;140. Elsevier, 2008. [arXiv:math/0601129](https://arxiv.org/abs/math/0601129)

* V.A. Smirnov, _Simplicial and operad methods in algebraic topology_

* [[Jean-Louis Loday]], [[Bruno Vallette]], _Algebraic operads_, Grundlehren der mathematischen Wissenschaften, Volume 346, Springer-Verlag (2012), xviii+512 pp. ([pdf](https://www.math.univ-paris13.fr/~vallette/Operads.pdf))

* {#FresseMOF} [[Benoit Fresse]], _Modules over operads and functors_, Springer LNM __1967__, 2009, x+308 pp. [MR2010e:18009](http://www.ams.org/mathscinet-getitem?mr=2494775)

* {#FresseHOGTG} [[Benoit Fresse]], _Homotopy of Operads and Grothendieck-Teichm&#252;ller Groups (Volumes 1 & 2)_, [website](http://math.univ-lille1.fr/~fresse/OperadHomotopyBook/) 


See also

* [[Todd Trimble]], _[[toddtrimble:Notes on operads and the Lie operad]]_ ([pdf](http://math.ucr.edu/home/baez/trimble/trimble_lie_operad.pdf))


[[!redirects operads]]

[[!redirects coloured operad]]
[[!redirects coloured operads]]

[[!redirects colored operad]]
[[!redirects colored operads]]

[[!redirects substitution product]]
[[!redirects substitution products]]