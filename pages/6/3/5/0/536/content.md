+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Algebraic theories
* tic
{: toc}


## Idea

An _algebraic [[theory]]_ is a concept in [[universal algebra]] that describes a specific type of algebraic gadget, such as [[group|groups]] or [[ring|rings]]. An individual group or ring is a _model_ of the appropriate theory. Roughly speaking, an algebraic theory consists of a specification of operations and laws that these operations must satisfy.

## Commentary

Traditionally, algebraic theories were described in terms of [[logic|logical syntax]], as [[theory|first-order theories]] whose [[signature]]s have only function symbols, no relation symbols, and all of whose axioms are universally quantified equations.  Such descriptions are like presentations of a theory, analogous to generator and relations presentations of groups. In particular, different logical presentations can lead to equivalent mathematical objects. 

In his thesis, Lawvere undertook a more invariant description of (finitary) algebraic theories via the notion of [[Lawvere theory]]. Here all the definable operations of an algebraic theory, or rather their equivalence classes modulo the equational axioms imposed by the theory, are packaged together to form the morphisms of a category with finite products, for which every object is a finite power of a generating object. In the great semantic expansion envisaged by Lawvere for what constitutes a "model", the category so formed becomes a universal model of the theory, and carries all the information of the theory, independent of a particular presentation. Lawvere considers _this_ category, this universal model, to be the theory. To give an example, the universal model of the theory of groups, i.e., the Lawvere theory of groups, is the (2-)initial object in the (2-)category of categories with finite products and equipped with a group object. Traditional (set-theoretic) models of the theory are neatly defined as product-preserving functors from the Lawvere theory to the category of sets. 

Moreover, the categorical construction of the Lawvere theory is described very easily and elegantly: it is the category opposite to the category of (finitely generated) free algebras of the theory. 

Lawvere's program can be extended to cover certain theories with infinitary operations as well. In the best-behaved case, one has algebraic theories involving only operations of arity bounded by some [[cardinal number]], and these can be understood category-theoretically with a suitable generalization of Lawvere theories.  In the bounded case, the Lawvere theory can be described by a small category, and the category of models will be very well behaved, in particular it is a [[locally presentable category]]. In such cases there is a satisfying duality between syntax and semantics along the lines of [[Gabriel-Ulmer duality]]. 

Lawvere's program can to some degree be extended further: one can work with Lawvere theories which are locally small (not just small) categories. Here, the theory might not be bounded, but at least there is only a small set of operations of each arity. Examples of such large theories include 

* The theory of algebras with arbitrary sums (one model of which is $[0,\infty]$), 

* The theory of sup-lattices, in which there is one operation of each arity, and 

* The theory of compact Hausdorff spaces, where the operations are parametrized by ultrafilters. 

These examples go outside the bounded (small theory) case. Locally small theories in this sense are co-extensive with the notion of monad (on $Set$): there is a free-forgetful adjunction between $Set$ and the category of models, and algebras of the theory are equivalent to algebras of the monad. 

In the worst case, there are algebraic theories where the number of definable operations explodes, so that there may be a proper class of operations of some fixed arity. In these case there are no free algebras, and Lawvere's reformulation no longer applies. An example is the theory of complete Boolean algebras. (Note: category theorists who define a category $U: A \to Set$ over sets to be [[algebraic category|algebraic]] if it is [[monadic functor|monadic]] would therefore not consider the variety of algebras in such cases to be "algebraic"). 

Further commentary on these aspects may be found in the dozen or so comments in [this thread](http://golem.ph.utexas.edu/category/2009/04/report_on_88th_peripatetic_sem.html#c023188), dated April 13 - May 7, 2009.

In summary, then, here is the connection between the logical and categorial descriptions, based on [Johnstone][], &#167;&#167;3.7&8.  Say that a category $C$ is:

* _small algebraic_ if it is given by a (small) set of operation symbols and equations;
* _[[algebraic category|algebraic]]_ if it is given by a monad on the category of (small) sets;
* _large algebraic_ if it is given by a (possibly proper) class of operation symbols and equations.

Then any small algebraic category is algebraic, and any algebraic category is large algebraic, but neither implication may be reversed.


## Lawvere theories and monads 

We flesh out the relationships between theories and [[monad]]s, starting from the most general situation and then adding conditions to cut down on the size of theories. The term "[[Lawvere theory]]" as used here will mean 
a large (but locally small) [[infinitary Lawvere theory]]. 

For the moment we discuss the single-sorted case. The many-sorted case should be a straightforward extension. 

First, the definition. For any cardinal n, let $[n]$ be a set of that cardinality (sometimes we just use $n$). 

+-- {: .un_def}
######Definition: 
A **Lawvere theory** or **algebraic theory** is a locally small category $C$ with small products that is equipped with an object $x$ such that the (unique-up-to-isomorphism) product-preserving functor 
$$i: Set^{op} \to C: [1] \mapsto x$$ 
is essentially surjective. 
=--

### Variations 

Algebraic theories can be extended or specialized in various directions. Here are a few variations on the theme. 

#### Essentially algebraic theories

_[[essentially algebraic theory|Essentially algebraic theories]]_ allow for partially-defined operations.  Just as finitary algebraic theories can be understood as Lawvere theories, which live in the [[doctrine]] of [[cartesian monoidal category|cartesian monoidal categories]], so finitary essentially algebraic theories can be understood by a generalisation to [[finitely complete category|finitely complete categories]].

#### Multisorted algebraic theories

_[[multi-sorted theory|Multi-sorted theories]]_ allow for more than one sort or type in the theory. 

Let $S$ be a set whose elements are called sorts. Define $Prod(S)$ to be the [[category of elements]] of the functor 

$$\hom(-, S): Set^{op} \to Set$$ 

Thus objects are pairs $(n, x: [n] \to S)$, where $[n]$ is any set, and morphisms $(n, x) \to (m, y)$ are functions $f: [m] \to [n]$ such that $y = x \circ f$, or $y_i = x_{f(i)}$ for all $i \in [m]$. There is a canonical function $i: S \to Ob(Prod(S))$ sending $s$ to the pair $(1, s: [1] \to S)$. Moreover, $Prod(S)$ has small products: if $X$ is any set and $h: X \to Ob(Prod(S))$ is any function, 

$$\prod_{x \in X} h(x) \coloneqq (\sum_{x \in X} \pi_1(h(x)), H)$$ 

where the domain of $H$ is a disjoint sum $\sum_x [\pi_1(h(x))]$ and where, for $j \in [\pi_1(h(x))]$, 

$$H(j) = \pi_2(h(x))(j)$$ 

Clearly, any object $(n, x)$ of $Prod(S)$ is a product of objects of the form $i(s)$. 

+-- {: .un_prop}
######Proposition 
$Prod(S)$ is the free category with small products generated by the set $S$. 
=-- 

+-- {: .proof}
######Proof
Let $C$ be a category with small products and let $\Phi: S \to Ob(C)$ be any function. Define a functor 

$$\prod: Prod(S) \to C$$ 

so that $(n, x: [n] \to S)$ is taken to $\prod_{i \in [n]} \Phi(x(i))$. It is immediate that $\prod$ is a product-preserving functor and is, up to unique isomorphism, the unique product-preserving functor that extends $\Phi$. 
=-- 

+-- {: .un_def}
######Definition 
A **multi-sorted algebraic theory** over the set of sorts $S$ consists of a locally small category with small products, $C$, together with a sort assignment $\Phi: S \to C$ such that the product-preserving extension 

$$\Pi: Prod(S) \to C$$ 

is essentially surjective. An **operation of arity** $x_1, \ldots, x_n \to s$ in $C$ is a morphism of the form $\prod(n, x) \to \Phi(s)$ in $C$. 
=-- 

### Commutative theories

_[[commutative algebraic theory|Commutative algebraic theories]]_ are (single-sorted) algebraic theories for which each operation is an algebra homomorphism. These form an important subclass. Their categories of models are closed: the Hom sets have a natural model-structure, and the enriched Hom-functor has a left adjoint, _tensor-product_. The theory of complete lattices and suprema-preserving functions is an interesting (non-finitary) example.


### Large Lawvere theory of a monad

Let $T: Set \to Set$ be a [[monad]] on [[Set]], with unit $u: 1 \to T$ and multiplication $m: T T \to T$. 

+-- {: .un_def}
######Definition 
The **large Lawvere theory** $Th(T)$ **of $T$** is the [[opposite category|opposite]] of the [[Kleisli category]], $Kl(T)^{op}$. 
=-- 

Objects of $Kl(T)^{op}$ are sets $n$, and every object $n$ of $Kl(T)^{op}$ is the $n^{th}$ power of a set $1$, so indeed $Kl(T)^{op}$ is a (locally small) [[infinitary Lawvere theory]]. 

A _model_ of the Lawvere theory is a functor $M: Kl(T)^{op} \to Set$ that preserves small [[product]]s. A _homomorphism_ of models is a natural transformation between such functors. (Of course we can interpret models in any category with small products, not just $Set$.) 

Each [[algebra over a monad|algebra]] $X$ of the monad gives rise to a model $M_X$ of the Lawvere theory: 

$$Kl(T)^{op} \hookrightarrow Alg(T)^{op} \stackrel{\hom(-, X)}{\to} Set$$ 

and similarly a morphism of algebras $f: X \to Y$ gives rise to a homomorphism $M_f: M_X \to M_Y$, so that we have a functor $M: Alg(T) \to Mod(Th(T))$. 

+-- {: .un_thm}
######Theorem 
$M$ is an equivalence. 
=-- 

+-- {: .proof} 
######Proof 
The proof that $M$ is fully faithful is akin to the proof of the [[Yoneda lemma]]. Suppose $\theta: M_X \to M_Y$ is a natural transformation, and let $\xi: T X \to X$ be the algebra structure of $X$, regarded as an element of $M_X(X)$. Then $\theta$ is uniquely determined from the special value $\phi = \theta(X)(\xi) \in M_Y(X) = Alg(T X, Y)$. Indeed, for any $n \in Ob(Kl(T))$ and algebra map $h: T n \to X$, we have the equation 

$$h = (T n \stackrel{T(h u(n))}{\to} T X \stackrel{\xi}{\to} X)$$ 

whence by chasing the naturality diagram 

$$\array{
\xi: Alg(T X, X) & \overset{\theta(X)}{\to} & Alg(T X, Y): \phi \\
\mathllap{Alg(T(h u(n)), X)} \downarrow & & \downarrow \mathrlap{Alg(T(h u(n)), Y)} \\
h: Alg(T n, X) & \underset{\theta(n)}{\to} & Alg(T n, Y)
}$$

applied to $\xi$ in the upper left corner, we obtain the formula 

$$\theta(n)(h) = Alg(T(h u(n)), Y)(\phi)$$ 

as an element in $Alg(T n, Y) = M_Y(n)$. Thus $\theta$ is uniquely determined from $\phi$. Finally, the algebra map $\phi: T X \to Y$ factors as $\xi: T X \to X$ followed by a uniquely determined algebra map $f: X \to Y$; to see this, it suffices to check that $\phi \circ T \xi = \phi \circ m X$ since $\xi$ is the coequalizer of the pair $T\xi, m X$. The desired equation follows from naturality (consider chasing the square above through $h = (T\xi) \xi = (m X) \xi$). Hence every $\theta: M_X \to M_Y$ is of the form $M_f$ for a (unique) algebra map $f: X \to Y$. 

To complete the proof, we must show that $M: Alg(T) \to Mod(Th(T))$ is essentially surjective. So suppose $Y: Kl(T)^{op} \to Set$ preserves small products; we must show $M_X \cong Y$ for some $T$-algebra $X$. Take the underlying set of $X$ to be $Y(1)$, and define the $T$-algebra structure on $Y(1)$ as follows. The objects $n$ of $Kl(T)$ are sets and we have a composite 

$$T(n) \cong Kl(T)^{op}(n, 1) \to Set(Y(n), Y(1)) \cong Set(Y(1)^n, Y(1))$$ 

where the last composite uses the fact that $Y$ is product-preserving. Putting $n = Y(1)$, we post-compose this composite with evaluation at the identity on $Y(1)$, yielding 

$$T(Y(1)) \to Set(Y(1)^{Y(1)}, Y(1)) \stackrel{ev_{id}}{\to} Y(1)$$ 

and this defines the algebra structure on $X$. The model $M_X$ is the functor which sends the set $[n]$ (as an object in $Kl(T)$) to $Alg(T[n], X)$, and there is an isomorphism 

$$Alg(T[n], X) \cong Set([n], Y(1)) \cong Y(n)$$ 

The proof that this isomorphism is natural with respect to homomorphisms of free algebras $T[n] \to T[m]$ is an exercise in chasing definitions which we leave to the reader. 
=--


### The monad of a locally small Lawvere theory 

Now suppose $C$ is a locally small category with small products, equipped with an object $x$ such that the product-preserving functor 

$$i: Set^{op} \to C: [1] \to x$$ 

(which is unique up to isomorphism) is essentially surjective. For each set $[n]$, let $T[n]$ be the set $C(i[n], i[1])$. This is evidently functorial in the argument $[n]$, i.e., defines a functor $T: Set \to Set$. The evident composite 

$$[n] \cong Set([1], [n]) \cong Set^{op}([n], [1]) \to C(i[n], i[1])$$ 

defines a map $u[n]: [n] \to T[n]$ which is evidently natural in $[n]$: defines a natural transformation $u: 1_{Set} \to T$. 

Morphism composition in $C$ induces a map $\xi: T[m] \times T[n]^m \to T[n]$: 

$$T[m] \times T[n]^m = C(i[m], i[1]) \times C(i[n], i[1])^m \cong C(i[m], i[1]) \times C(i[n], i[m]) \stackrel{comp}{\to} C(i[n], i[1]) = T[n]$$ 

Putting $[m] = T[n]$, there is a map $T T[n] \to T[n]$ that sends $\theta \in T T[n]$ to $\xi(\theta, 1_{T[n]}) \in T[n]$. This is evidently natural in $[n]$ and defines a natural transformation $m: T T \to T$. 


## Metaphor

Ring theory is a branch of mathematics with a well-developed terminology. A ring $A$ determines and is determined by an algebraic theory, whose models are left $A$-modules and whose n-ary operations have the form
$$(x_1,\ldots ,x_n) \to a_1x_1+\ldots +a_n x_n$$
for some n-tuple $(a_1,\ldots ,a_n)$ of elements of $A$. We may call such an algebraic theory **annular**. The pun _model/module_ is due to Jon Beck. The notion that an algebraic theory is a generalized ring is often a fertile one, that automatically provides a slew of suggestive terminology and interesting problems. Many fundamental ideas of ring/module-theory are simply the restriction to annular algebraic theories of ideas that apply more widely to algebraic theories and their models.

Let us denote the category of models and homomorphisms (in $Set$) of an algebraic theory $A$ by $A Mod$.  Then compare the following to their counterparts in ring theory:
*  [[tensor product theory|Tensor Product of Theories]]
*  [[matrix theory|Matrix Theories]]
*  [[bimodel|Bimodels]]


## Related concepts

* [[essentially algebraic theory]]

* **algebraic theory** / [[Lawvere theory]] / [[2-Lawvere theory]] /  [[(∞,1)-algebraic theory]]

* [[monad]] / [[(∞,1)-monad]]

* [[operad]] / [[(∞,1)-operad]]


## References

* <span id="Johnstone"></span>
  [[Peter Johnstone]], _[[Stone Spaces]]_
  [Johnstone]: #Johnstone

_Someone should improve this article so that it gives a **definition** of 'algebraic theory' before considering special cases such as 'commutative algebraic theory'._


[[!redirects algebraic theories]]