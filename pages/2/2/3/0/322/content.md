<div class="rightHandSide toc">

[[!include higher algebra - contents]]

</div>


#Contents#
* automatic table of contents goes here
{:toc}

# The idea #

An **operad** is a gadget used to describe algebraic structures in [[symmetric monoidal category|symmetric monoidal categories]].  An operad is like a [[Lawvere theory]] in that it can be used to describe structures having finitary operations obeying equational laws.  However, unlike Lawvere theories, operads can be applied to general symmetric monoidal categories where the tensor product might not be the cartesian product. 

Actually the notion of operad (and allied notions such as [[PROP]], [[club]], [[multicategory]] and so on) come in many flavors. Originally used in algebraic topology to provide a systematic formalism for describing the internal operations which exist on iterated loop spaces, the basic idea is quite flexible and adaptable to many categorical situations, and the importance of operads continues to grow. 

# The rough definition # 

The original definition is due to J.P. May and was given in his book _The Geometry of Iterated Loop Spaces_. Since the detailed definition is available from many sources, we will just sketch May's definition; in the section following this, we give a more detailed higher-level description which generalizes in a number of directions. 

Let $V$ be a symmetric monoidal category. A (permutative) _operad_ in $V$ consists of objects $F(n)$ of $V$ indexed over the natural numbers $n = 0, 1, 2, \ldots$ [which we intuitively think of as "objects that parametrize the $n$-ary operations of an algebraic theory"] equipped with the following extra structure: 

* Right actions of symmetric groups $\rho_n: S_n \to \hom(F(n), F(n))$; 
* An _unit_ $e: I \to F(1)$ [which we think of as picking out the identity map as unary operation]; 
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

$$\rho(\sigma) \otimes 1, 1 \otimes \lambda(\sigma): F(k) \otimes \bigotimes_{i=1}^n F(n_i) \stackrel{\to}{\to} F(k) \otimes \bigotimes_{i=1}^n F(n_i)$$ 

where $\sigma$ acts on the big tensor product on the left by permuting tensor factors in the obvious way. If $V$ has suitable colimits, this condition could be expressed in terms of tensor products over $S_n$. 

The associativity condition will be left for others to fill in. 

### Algebras ### 

An _algebra_ over an operad $F$ in $V$ is just a semantics for interpreting the $F(n)$ as objects of actual $n$-ary operations on an object $v$. That is, an $F$-algebra structure on an object $v$ in $V$ consists of a collection of maps 

$$F(n) \otimes v^{\otimes n} \to v$$ 

which intuitively is a mapping like this: 

$$\theta \otimes x_1 \otimes \ldots \otimes x_n \mapsto \theta(x_1, \ldots, x_n)$$ 

so that "elements" of $F(n)$ are interpreted as as $n$-ary operations on $v$. These data are subject to some natural conditions which implement this idea. 

Perhaps the quickest way to define it is to suppose that $V$ is symmetric monoidal closed, and work by way of parallel to how [[representations]] or [[modules]] work. Just as an $R$-module (over a ring $R$) can be defined as a ring homomorphism 

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

# A detailed conceptual treatment # 

We describe here a compact one-sentence definition of operad first worked out by G.M. Kelly, after a few preliminaries which are important in their own right. The treatment is essentially an exercise in [[enriched category theory]] and the formalism of [[Day convolution]]. We will work this out fully in the case of ordinary [[category theory]] first, that is for categories [[enriched category|enriched in]] $V = Set$; the case for categories enriched in a complete, cocomplete, [[symmetric monoidal category|symmetric monoidal]] [[closed monoidal category|closed]] $V$ is completely parallel. 

## Preparation ##

1. Let $\mathbb{P}$ be the groupoid of finite cardinals and bijections thereon. Since $\mathbb{P}$ is the [[underlying groupoid]] of the category $Fin$ of finite cardinals and functions between them, the tensor product given by the coproduct on $Fin$ restricts to a symmetric monoidal product on $\mathbb{P}$. Under this symmetric monoidal structure, $\mathbb{P}$ may be characterized as the free symmetric strict monoidal category on one generator. 

1. The symmetric monoidal product on $\mathbb{P}$ extends along the Yoneda embedding to a symmetric monoidal product $F \otimes G$ on the category $Set^{\mathbb{P}^{op}}$ of presheaves on $\mathbb{P}$; this is an instance of [[Day convolution]]. The [[presheaf]] category is cocomplete, and Day convolution is cocontinuous in each of its separate arguments $F, G$; we say in that case that $Set^{\mathbb{P}^{op}}$ is symmetric monoidally cocomplete. 

$\mathbb{P}$ is also a skeleton of the category $FB$ of finite sets and bijections; a functor $FB^{op} \to Set$ (or what is more or less the same thing, a functor $FB \to Set$) is called a [[species]]. The Day convolution product on the category of species may be described by the rule 

$$(F \otimes G)[S] = \sum_{S = T + U} F[T] \times G[U]$$ 

where the sum is over all ways of partitioning the finite set $S$ into two (possibly empty) parts. 

3. According to the yoga of presheaf categories and Day convolution, given a symmetric monoidally cocomplete category $D$, a symmetric monoidal functor 
$$X: \mathbb{P} \to D$$
extends uniquely up to isomorphism to a symmetric monoidal _cocontinuous_ functor 
$$\hat{X}: Set^{\mathbb{P}^{op}} \to D,$$ 
taking a presheaf $F: \mathbb{P}^{op} \to Set$ to the [[limit|weighted colimit]] $F \cdot X$. Putting items 1. and 2. together, we may therefore describe $Set^{\mathbb{P}^{op}}$ universally up to equivalence as the free symmetric monoidally cocomplete category on a single generator. 

In general, weighted colimits may be described by coend formulas; here 

$$F \cdot_{\mathbb{P}} X = \int^{k: \mathbb{P}} F(k) \cdot X(k)$$ 

where $S \cdot d$ denotes the tensoring of a set $S$ with an object $d$, that is the coproduct of an $S$-indexed set of copies of $d$. The coend here indicates a coequalizer  

$$\sum_k F(k) \cdot S_k \cdot X(k) \stackrel{\to}{\to} \sum_k F(k) \cdot X(k) \to \int^k F(k) \cdot X(k)$$ 

where one of the parallel arrows involves right actions of symmetric groups $S_k$ on the $F(k)$, and the other involves left actions of $S_k$ on objects $X$. In other words, the coend in this instance may be described as a sum of tensor products: 

$$F \cdot_{\mathbb{P}} X = \sum_k F(k) \otimes_{S_k} X(k).$$

The aforementioned universal property of $Set^{\mathbb{P}^{op}}$ with its convolution product may be more explicitly described as follows: given a symmetric monoidally cocomplete category $D$ and an object $d$ therein, there exists up to isomorphism a unique symmetric monoidal cocontinuous functor $Set^{\mathbb{P}^{op}} \to D$ which sends $\hom_{\mathbb{P}}(-, 1)$ to $d$. This functor takes a presheaf $F: \mathbb{P}^{op} \to Set$ to the following object of $D$: 

$$\sum_k F(k) \otimes_{S_k} d^{\otimes k}.$$

For instance, when $D$ is the symmetric monoidally cocomplete category $(Set, \times)$ and $x$ is a set, this formula 

$$\hat{F}(x) = \sum_n F(k) \otimes_{S_k} x^k$$ 

is the value at $x$ of what Joyal calls the _analytic functor_ $\hat{F}: Set \to Set$ associated to a species $F$, proposed as the categorification of exponential generating functions. The fact that $F \mapsto \hat{F}(x)$ is symmetric monoidal (cocontinuous) means that there is a canonical isomorphism

$$\hat{(F \otimes_{Day} G)}(x) \cong \hat{F}(x) \times \hat{G}(x)$$ 

In other words, $F \mapsto \hat{F}$ behaves like a categorified version of Fourier transform, taking convolution products to ordinary (pointwise) products. 

* For symmetric monoidally cocomplete categories $C, D$, let $[C, D]$ denotes the category of symmetric monoidal cocontinuous functors $C \to D$. The universal property of $Set^{\mathbb{P}^{op}}$ means that we have an equivalence $[Set^{\mathbb{P}^{op}}, D] \simeq D$. Consequently, we have an equivalence $[Set^{\mathbb{P}^{op}}, Set^{\mathbb{P}^{op}}] \simeq Set^{\mathbb{P}^{op}}$. Since symmetric monoidal cocontinuous functors compose, the category on the left carries a monoidal product given by endofunctor composition. Transferring endofunctor composition across the equivalence produces a monoidal product on $Set^{\mathbb{P}^{op}}$ called _substitution product_ of species. The substitution product of species $F, G$ is denoted $F \circ G$. 

In detail: a species $G: \mathbb{P}^{op} \to Set$ induces a symmetric monoidal cocontinuous functor 

$$Set^{\mathbb{P}^{op}} \to Set^{\mathbb{P}^{op}}: F \mapsto F \circ G = \sum_k F(k) \otimes_{S_k} G^{\otimes_{Day} k}$$ 

The $k$-fold Day tensor power of $G$ is given (in the language of species) by the formula 

$$G^{\otimes k}[S] = \sum_{S = T_1 + \ldots + T_k} G[T_1] \times G[T_2] \times \ldots \times G[T_k]$$ 

where we sum over all ways of breaking up a finite set $S$ into $k$ blocks, some possibly empty. Thus we have an explicit description of the substitution product, 

$$(F \circ G)[n] = \sum_k F[k] \otimes_{S_k} (\sum_{[n] = T_1 + \ldots + T_k} G[|T_1|] \times \ldots \times G[|T_k|]),$$ 

and it is clear from our discussion above that substitution is a monoidal product. 

## Definition as monoid ##

We are at last ready for the one-sentence **definition**: 


A ($Set$-based) **operad** is a [[monoid]] in the [[monoidal category]] $(Set^{\mathbb{P}^{op}}, \circ)$. 

## Remarks ##

* We can get different flavors of operad by considering different notions of monoidal category. For instance, for the theory of monoidal categories, the discrete category $\mathbb{N}$ plays the role of the free (strict) monoidal category on one generator, and $Set^{\mathbb{N}^{op}}$ the free monoidally cocomplete category on one generator. Similarly, for braided monoidal categories, we have the braid category $\mathbb{B}$, and $Set^{\mathbb{B}^{op}}$ is the free braided monoidally cocomplete category on one generator. Again, for cartesian categories, we have $Fin^{op}$ (the opposite of finite sets and functions) as the free cartesian category on one generator, and $Set^{Fin}$ is the free cartesian monoidally cocomplete category on one generator. In each of these cases we get a corresponding notion of operad by following the above treatment _mutatis mutandis_: nonpermutative operads, braided operads, cartesian operads (better known as [[Lawvere theory|Lawvere theories]]). 

* All of the above carries over to the enriched setting, where we work over a complete, cocomplete symmetric monoidal closed base category $V$. Here ordinary categories (like $\mathbb{N}, \mathbb{P}, \mathbb{B}, Fin$) are viewed as $V$-enriched by a simple change of base: change from [[hom-set]]s to [[hom-objects]] by applying the change of base functor 
$$Set \to V$$ 
that takes a set $S$ to the $S$-fold coproduct $S \cdot I$, where $I$ is the monoidal unit of $V$. 

* There are still other notions of operad; see for example the discussion of $T$-operads under the entry [[multicategory]] for more details. See also the general framework by Hyland, Fiore, and others [to be filled in]. 

* In still other directions, there are for example notions of _cyclic operad_ and _modular operad_. Anyone want to take these up? 

# The monad attached to an operad #

...

# Examples #

> this list of examples should eventually be collected in a table of cotents on operad theory

* [[associative operad]]

* [[endomorphism operad]]

* [[E-k operad]]

* [[Eilenberg-Zilber operad]]

generalizations:

* [[(∞,1)-operad]]

[[!redirects operads]]