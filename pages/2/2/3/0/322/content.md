
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

* [[algebraic theory]] / [[Lawvere theory]] /  [[(∞,1)-algebraic theory]]

* [[monad]] / [[(∞,1)-monad]]

* **operad** / [[(∞,1)-operad]]

***



#Contents#
* automatic table of contents goes here
{:toc}

## The idea 

An **operad** is a gadget used to describe algebraic structures in [[symmetric monoidal category|symmetric monoidal categories]].  An operad is like a [[Lawvere theory]] in that it can be used to describe structures having finitary operations obeying equational laws.  However, unlike Lawvere theories, operads can be applied to general symmetric monoidal categories where the tensor product might not be the cartesian product. 


Actually the notion of operad (and allied notions such as [[PROP]], [[club]], [[multicategory]] and so on) come in many flavors. Originally used in algebraic topology to provide a systematic formalism for describing the internal operations which exist on iterated loop spaces, the basic idea is quite flexible and adaptable to many categorical situations, and the importance of operads continues to grow. 

## The rough definition 

The original definition is due to J.P. May and was given in his book _The Geometry of Iterated Loop Spaces_. Since the detailed definition is available from many sources, we will just sketch May's definition; in the section following this, we give a more detailed higher-level description which generalizes in a number of directions. 

Let $V$ be a [[symmetric monoidal category]]. A 
(_permutative_ or _symmetric_) **operad** in $V$ consists of objects $F(n)$ of $V$ indexed over the natural numbers $n = 0, 1, 2, \ldots$ [which we intuitively think of as "objects that parametrize the $n$-ary operations of an algebraic theory"] equipped with the following extra structure: 

* Right actions of [[symmetric group]]s $\rho_n: S_n \to \hom(F(n), F(n))$; 
* A _unit_ $e: I \to F(1)$ [which we think of as picking out the identity map as unary operation]; 
* Composition operations 
$$F(k) \otimes F(n_1) \otimes F(n_2) \otimes \cdots \otimes F(n_k) \to F(n_1 + \ldots + n_k)$$
[which we think of as the result of plugging the outputs of operations $\theta_1, \ldots, \theta_k$ into a $k$-ary operation $\theta$, to produce a new operation $\theta \circ (\theta_1 \otimes \ldots \otimes \theta_k)$]. 

These data are subject to obvious identities such as associativity of composition, unit laws, and compatibility of composition with symmetric group actions. For example, the unit laws say that the evident composite 

$$F(n) \cong I \otimes F(n) \stackrel{e \otimes 1}{\to} F(1) \otimes F(n) \stackrel{comp}{\to} F(n)$$ 

is the identity map, as is 

$$F(n) \cong F(n) \otimes I^{\otimes n} \stackrel{1 \otimes e^{\otimes n}}{\to} F(n) \otimes F(1)^{\otimes n} \stackrel{comp}{\to} F(n)$$ 

Compatibility with symmetric group actions means that for each element $\sigma \in S_k$, the composition operation 

$$F(k) \otimes \bigotimes_{i = 1}^n F(n_i) \to F(n_1 + \ldots + n_k)$$ 

coequalizes a pair of automorphisms 

$$\rho(\sigma) \otimes 1, 1 \otimes \lambda(\sigma): F(k) \otimes \bigotimes_{i=1}^n F(n_i) \;\rightrightarrows\; F(k) \otimes \bigotimes_{i=1}^n F(n_i)$$ 

where $\sigma$ acts on the big tensor product on the left by permuting tensor factors in the obvious way. If $V$ has suitable colimits, this condition could be expressed in terms of tensor products over $S_n$. 

The associativity condition will be left for others to fill in. 

### Algebras 

An _[[algebra over an operad|algebra]]_ over an operad $F$ in $V$ is just a semantics for interpreting the $F(n)$ as objects of actual $n$-ary operations on an object $v$. That is, an $F$-algebra structure on an object $v$ in $V$ consists of a collection of maps 

$$F(n) \otimes v^{\otimes n} \to v$$ 

which intuitively is a mapping like this: 

$$\theta \otimes x_1 \otimes \ldots \otimes x_n \mapsto \theta(x_1, \ldots, x_n)$$ 

so that "elements" of $F(n)$ are interpreted as as $n$-ary operations on $v$. These data are subject to some natural conditions which implement this idea. 

Perhaps the quickest way to define it is to suppose that $V$ is symmetric monoidal [[closed monoidal category|closed]], and work by way of parallel to how [[representations]] or [[modules]] work. Just as an $R$-module (over a ring $R$) can be defined as a ring homomorphism 

$$R \to \hom(A, A)$$ 

where the hom here is an internal hom of abelian groups, called an _endomorphism ring_, so there is such a thing as an _endomorphism operad_ attached to any object $v$ in a symmetric monoidal closed category, and an $F$-algebra over an operad $F$ is the same thing as an operad morphism 

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

We describe here a compact one-sentence definition of operad first worked out by G.M. Kelly, after a few preliminaries which are important in their own right. The treatment is essentially an exercise in [[enriched category theory]] and the formalism of [[Day convolution]]. We will work this out fully in the case of ordinary [[category theory]] first, that is for categories [[enriched category|enriched in]] $V = Set$; the case for categories enriched in a complete, cocomplete, [[symmetric monoidal category|symmetric monoidal]] [[closed monoidal category|closed]] $V$ is completely parallel. 

### Preparation 

Let $\mathbb{P}$ be the [[groupoid]] of finite cardinals with [[bijections]] as morphisms. Since $\mathbb{P}$ is the [[core]] groupoid of the category $Fin$ of finite cardinals and functions between them, the [[coproduct]] on $Fin$ restricts to a symmetric monoidal product called the cardinal sum on $\mathbb{P}$. 

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

+-- {: .un_example style="margin-left:2em"}
######Example
When $D$ is the symmetric monoidally cocomplete category $(Set, \times)$ and $x$ is a set, this formula 

$$\hat{F}(x) = \sum_n F(k) \otimes_{S_k} x^k$$ 

is the value at $x$ of what Joyal calls the _analytic functor_ $\hat{F}: Set \to Set$ associated to a [[combinatorial species|species]] $F$, which has been proposed as the categorification of the theory of exponential [[generating function]]s. The fact that $F \mapsto \hat{F}(x)$ is symmetric monoidal (cocontinuous) means that there is a canonical isomorphism

$$\hat{(F \otimes_{Day} G)}(x) \cong \hat{F}(x) \times \hat{G}(x)$$ 

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

We are at last ready for the one-sentence **definition**: 

A ($Set$-based) **operad** is a [[monoid]] in the [[monoidal category]] $(Psh(\mathbb{P}), \circ, I)$. 

### Remarks 

* We can get different flavors of operad by considering different notions of monoidal category. For instance, for the theory of monoidal categories, the discrete category $\mathbb{N}$ plays the role of the free (strict) monoidal category on one generator, and $Set^{\mathbb{N}^{op}}$ the free monoidally cocomplete category on one generator. Similarly, for braided monoidal categories, we have the braid category $\mathbb{B}$, and $Set^{\mathbb{B}^{op}}$ is the free braided monoidally cocomplete category on one generator. Again, for cartesian categories, we have $Fin^{op}$ (the opposite of finite sets and functions) as the free cartesian category on one generator, and $Set^{Fin}$ is the free cartesian monoidally cocomplete category on one generator. In each of these cases we get a corresponding notion of operad by following the above treatment _mutatis mutandis_: nonpermutative operads, braided operads, cartesian operads (better known as [[Lawvere theory|Lawvere theories]]).  These are all special cases of the notion of [[generalized multicategory]].

* All of the above carries over to the enriched setting, where we work over a complete, cocomplete symmetric monoidal closed base category $V$. Here ordinary categories (like $\mathbb{N}, \mathbb{P}, \mathbb{B}, Fin$) are viewed as $V$-enriched by a simple change of base: change from [[hom-set]]s to [[hom-objects]] by applying the change of base functor 
$$Set \to V$$ 
that takes a set $S$ to the $S$-fold coproduct $S \cdot I$, where $I$ is the monoidal unit of $V$.  These can also be defined in the framework of [[generalized multicategories]].

* The notion of generalized muticategories is even more general than this; for instance it also includes [[globular operads]] and [[topological spaces]].  See [[generalized multicategory]] for details.

* In still other directions, there are for example notions of [[cyclic operad]] and [[modular operad]].   

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

> this list of examples should eventually be collected in a table of contents on operad theory

* [[associative operad]]

* [[endomorphism operad]]

* [[E-k operad]]

  * [[E-infinity operad]]

* [[Eilenberg-Zilber operad]]

* [[linear operad]]

generalizations:

* [[(∞,1)-operad]]

## Free operads {#FreeOperads}

For $G$ a discrete group, write $V^G$ for the category of objects of $V$ equipped with a $G$-[[action]]. For $V$ symmetric monoidal this is again a [[symmetric monoidal category]] and the [[forgetful functor]] $V^G \to V$ is symmetric monoidal.

+-- {: .un_defn}
###### Definition

The category of **collections** of $V$ is

$$
  V Coll := \prod_{n \in \mathbb{N}} V^{S_n}
  \,.
$$

=--

Notice that both $S_0$ and $S_1$ are the trivial group.

So a $V$-operad $P$ is a special $V$-collection with extra structure relating its components. This gives an evident [[forgetful functor]] $U : V Operad \to V Coll$ and its [[left adjoint]], the free operad functor

$$
  F : V Coll \stackrel{\leftarrow}{\to} V Operad : U
  \,.
$$

This is for instance used to define the [[model structure on operads]] by [[transferred model structure|transfer]] along this adjunction from a model struucture on $V$.

The free operad functor may more explcitly be described as follows (for instance [BerMor03 section 5.8](http://arxiv.org/PS_cache/math/pdf/0206/0206094v3.pdf#page=22))

Let $\mathbf{T} := Core(\Omega_pl)$ be the [[core]] of the category of planar rooted [[tree]]s. Write

* $t_n \in \Omega_n$ for the $n$-corolla (the tree with a single vertex, $n$ inputs and its unique output root)

* for $T$ any tree with $n$-ary root vertex let $\{T_i\}_{i=1}^n$ be the sub-trees such that $T = t_n(T_1, \cdots, T_n)$.

Then every $K \in V Coll$ defines a functor $\bar K : \mathbf{T}^{op} \to V$ by the inductive formula

$$
  \bar K : | \mapsto I
$$

$$
  \bar K : T \mapsto \bar K(t_n(T_1, \cdots, T_n))
  := K(n) \otimes K(T_1) \otimes \cdots K(T_n)
  \,.
$$

Let moreover $\lambda : \mathbf{T} \to Sez$ be the functor that sends a tree to the set of numbering of its incoming edges, and let $\bar \lambda : \mathbf{T} \to V$ be given by postcomposition with $S \mapsto \coprod_{s \in S} I$.

Then the **free operad** on a collection $K$ is the [[coend]]

$$
  \bar K \otimes_{\mathbf{T}} \bar \lambda
  =
  \int^{T \in \mathbf{T}}
   \bar K(T) \otimes \bar \lambda(T)
  \,.
$$

### Examples

Let $V$ be a [[cartesian monoidal category]] and $K = {*}$ the terminal collection, which is the [[terminal object]] in each degree, with, necessarily, trivial $S_n$-action.

The free operad on this should be the $V$-[[A-infinity operad]] it consists in degree $n$ of precisely $|S_n|$-operations per $n$-ary planar tree. So every planar $n$-ary tree is regarded by the operad as one distinct operation to multiply $n$ elements, and freely adjoining to each tree a $S_n$-action amounts to not dividing out any commutativity symmetry on these operations.

Riemann surfaces operad (TO BE EXPANDED)

Deligne-Mumford opeard (TO BE EXPANDED)

Little discs operad, framed little discs operad (TO BE EXPANDED) -- See [[Deligne conjecture]]




## Model structures on operads 


If the [[symmetric monoidal category]] $V$ that the operads under consideration are enriched in carries the structure of a [[monoidal model category]], then under suitable conditions there is also the structure of a [[model category]] on the category of $V$-operads. This is important for the notion of _homotopy_ [[algebra over an operad]], such as $A_\infty$- and $E_\infty$-algebras.

See 

* [[model structure on operads]].


## References

The definition is originally due to

* [[Peter May]], _The geometry of iterated loop spaces_

An earlier version was the notion of [[analyser]] (known usually by French version *analyseur* introduced in

* M. Lazard, _Lois de groupes et analyseurs_, Ann. &#201;cole Norm. Sup. __72__  (1955), pp. 299&#8211;400. 

Monographs:

* [[Igor Kriz|I. Kriz]], J. P. May, _Operads, algebras, modules and motives_, Ast&#233;risque 233, Soci&#233;t&#233; Math&#233;matique de France (1995).

* [[Martin Markl]], Steve Shnider, [[Jim Stasheff|James D. Stasheff]], _Operads in algebra, topology and physics_, Math. Surveys and Monographs __96__, Amer. Math. Soc. 2002.

* V.A. Smirnov, _Simplicial and operad methods in algebraic topology_

[[!redirects operads]]