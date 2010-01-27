<div class="rightHandSide toc">
[[!include higher geometry - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _structured [[(∞,1)-topos]]_ is a generalization of a [[ringed space]] or rather of a [[ringed site]]: 
a generalized [[space]] equipped with a *[[structure sheaf]]* taking values in generalized [[quantity|quantities]]. 

A structured $(\infty,1)$-topos that is constrained to locally look like an object in a prescribed category of _test spaces_ is a [[generalized scheme]].

At the bottom of it, a structured $(\infty,1)$-topos is a
[[(∞,1)-functor]]

$$
  X : S^{op}\times R \to V
  \,,
$$

where

* $V$ is the suitable enriching category, i.e. [[SSet]] for the full [[(infinity,1)-category|(∞,1)-categorical]] version;

* and for $U \in S$ and $C \in R$ the object $X(U,C)$ is to be thought of as the collection of morphisms from $U$ to $C$ that decompose into a morphism from $U$ into the generalized space and another morphism from that to $C$.

Here the generalization is in the sense described at [[space and quantity]]:

* _[[space]]s_ modeled on test spaces in some category $S$ are [[presheaf|presheaves]] $X$ on $S$: $X(U)$ is the collection of probes of $X$ by $U \in S$.

* _[[quantity|quantities]]_ (meaning: function algebras) modeled on value spaces in some category $S$ are [[presheaf|co-presheaves]] $A$ on $S$: $A(U)$ is the collection of the quantities with values  in $U \in S$.

In the context of structured $(\infty,1)$-toposes $S$ is called a [[geometry (for structured (∞,1)-toposes)]].

Combined, this allows to give an analogous general way to think of the notion of a _space equipped with a structure sheaf_. A _structured generalized space_ is such a generalization.

The basic idea is most simple:

First of all a _space with structure sheaf_ (for instance a [[ringed space]]) is supposed to be nothing but 

* an ordinary space $X$,

* equipped with a [[presheaf]] $O_X$ that takes values in some category of quantities

$$
  O_X : (Op(X))^{op} \to Quantities
$$

where we think -- for $U \subset X$ an object in the [[category of open subsets]] of $X$ -- of $O_X(U)$ as the collection of admissable functions on $U \subset X$. For instance $O_X(U)$ might be 

* the set of all continuous functions from $U$ to $\mathbb{R}$

* or, if $X$ has a smooth structure, the set of all smooth functions to $\mathbb{R}$

* or, if $X$ has a complex structure, the set of all holomorphic functions to $\mathbb{C}$

etc. In any case, the choice of the structure sheaf $O_X$ is a choice of which maps out of $X$ one wants to concentrate on.

Now, taking the idea of [[space and quantity]] seriously, we should regard the category $Quantities$ that $O_X$ takes values in itself as a category of co-presheaves on some category of co-test spaces. 

For instance if we let $Cartesian$ be the category whose objects are real cartesian spaces $\mathbb{R}^n$ and whose morphisms are continuous maps between these, then every continuous real-valued function on $U \subset X$ naturally forms the co-presheaf $C(U) : \mathbb{R}^n \mapsto C(U,\mathbb{R}^n)$. In this case our structure sheaf $O_X$ is therefore actually a co-presheaf-valued presheaf:

$$
  O_X : Op(X)^{op} \to [Cartesian, Set]
$$

$$
  O_X(U)(\mathbb{R}^n) := C(U,\mathbb{R}^n)
  \,.
$$

But equivalently, this is a presheaf-valued copresheaf

$$
  O_X : Cartesian \to [Op(X)^{op}, Set] = PSh(X)\,.
$$

If we want to impose the condition that we actually want a structure-[[sheaf]], we have a sheaf-valued copresheaf

$$
  O_X : Cartesian \to Sh(X)
  \,.
$$

Notice that $Sh(X)$ is a ([[Grothendieck topos|Grothendieck]]-)[[topos]], just as [[Set]] itself is. So we can think of $O_X$ as a generalized quantity in the sense of [[space and quantity]] which takes values not in the topos [[Set]] but in some other [[topos]], such as $Sh(S)$.

There are other perspectives possible on a structure sheaf $O_X$, but this is the one whose full generalization we describe in the following.

We now describe the theory of structure sheaves encoded in topos-valued co-presheaves as developed in 

* [[Jacob Lurie]], _Structured spaces_ ([arXiv](http://arxiv.org/abs/0905.0459))


## Definition

Let $S$ be a [[geometry (for structured (infinity,1)-toposes)|geometric]], i.e. essentially  an $(\infty,1)$-[[site]], i.e. some small [[(∞,1)-category]] equipped with a [[coverage]], and let $Sh(S)$ be the [[(∞,1)-topos]] of [[(∞,1)-category of (∞,1)-sheaves]] on $S$. 

Notice that if $S = Op(X)$ is the nerve of the [[category of open subsets]] of some [[topological space]] $X$, then $Sh(X) := Sh(S)$ is the [[(∞,1)-category of (∞,1)-sheaves]] on $X$, as in the above motivating introduction. 

We want to define a _structure sheaf_ on $S$ (for instance on $Op(X)$) of quantities modeled on some $(\infty,1)$-category $V$ to be an [[(∞,1)-functor]]

$$
  O_X : V \to Sh(S)
$$

to be thought of as the assignment to each _value space_ $v \in V$ of an $(\infty,1)$-sheaf  of $v$-valued functions on $S$ (on $X$ if $S = Op(X)$).

But since we are taking care of the sheaf condition on $S$, we also want to allow a similar kind of co-sheaf condition on $V$. In order to do so, $V$ is taken to be equipped with extra structure encoding covers in $V$, and $O_X$ is then required to respect this structure suitably


+-- {: .un_defn}
###### Definition ([StrSh, def 1.2.1](http://arxiv.org/abs/0905.0459))

An **admissablility structure** on an $(\infty,1)$-category $V$ is a [[Grothendieck topology]] on $V$ such that it is _generated_ by a system of **admissable morphisms** (to be defined...)
=--


+-- {: .un_defn}
###### Definition ([StrSh, def 1.2.5](http://arxiv.org/abs/0905.0459))

An $(\infty,1)$-category $V$ equipped with an admissablility structure is a **geometry** if it is essentially small, admits finite limits and is idempotent complete.
=--

+--{: .query}
[[Mike Shulman]]: What does "idempotent complete" mean for an $(\infty,1)$-category?  Any 1-category with finite limits is automatically idempotent complete, but I assume from the way this is phrased that that is no longer true for $(\infty,1)$-categories?

[[Zoran ?koda]]: see Higher Topos Theory 4.4.5. This involves structure rather than just being a property.
=--


+-- {: .un_defn}
###### Definition ([StrSh, def 1.2.8](http://arxiv.org/abs/0905.0459))
**(structure sheaf)**

Let $\mathcal{G}$ be a geometry and $\mathcal{X}$ an $(\infty,1)$-topos
An [[(∞,1)-functor]]

$$
  O_X : \mathcal{G} \to \mathcal{X}
$$

is a $\mathcal{G}$-**structure** on $\mathcal{X}$ or 
$\mathcal{G}$-**[[structure sheaf]]** on $\mathcal{X}$ if 

* it is a left exact functor;

* it respects gluing in $\mathcal{G}$ in that 
  for $\{U_i \to V\}_i$ 
  a covering [[sieve]] consisting of admissible morphism, 
  the induced morphism

  $$
    \coprod_i O_X(U_i) \to O_X(V)
  $$

  is an [[effective epimorphism]] in $\mathcal{X}$.

=--

Write $Str_{\mathcal{G}}(\mathcal{X}) \subset Func(\mathcal{G},\mathcal{X})$ for the full subcategory of such morphisms of the [[(∞,1)-category of (∞,1)-functors]].


+--{: .query}

[[Urs Schreiber]]: second attempt to illustrate what this means:

=--

+-- {: .un_example}
###### Examples

1. Consider $X$ an ordinary [[topological space]] and
   $Sh(X)$ the ordinary [[category of sheaves]] on its 
   [[category of open subsets]]. Let $\mathcal{G} = Top$
   be some [[small category|small]] version of [[Top]]
   with its usual [[Grothendieck topology]] with covering
   families being open covers. Consider the functor

   $$
     O_X : Top \to Sh(X)
   $$

   that sends a topological space $V$ to the sheaf of continuous
   functions with values in $V$:

   $$
     O_X(V) : U \mapsto C(U,V) = Hom_{Top}(U,V)
     \,.
   $$

   This functor clearly respects [[limit]]s, just by the
   general property of the hom. The gluing condition says that
   for $V_1, V_2 \subset V$ an open cover of $V$ by two patches, 
   the morphism of sheaves

   $$
     O_X(V_1) \coprod O_X(V_2) \to O_X(V)
   $$

   is an [[epimorphism]] of sheaves. This means that 
   for each point $x \in X$ the map of [[stalk]]s

   $$
     O_X(V_1)_x \coprod O_X(V_2)_x \to O_X(V)_x
   $$
   
   is an epimorphism of sets. But this just says that given
   any function $f : U_x \to V$ on a neighbourhood $U_x$ of $x$, 
   there is a smaller neighbourhood $V_x \subset U_x$ such that 
   the restriction $f|_{V_x}$ factors either through $V_1$ or
   through $V_1$. This is clearly the case by the fact that $V_1,V_2$
   form an opeen cover. (A neighbourhood  of $f(x) \in V$ exists which
   is contained in $V_1$ or in $V_2$, so take its preimage under
   $f$ as $U_x$).


2. [StrSh, remark 2.5.11](http://arxiv.org/PS_cache/arxiv/pdf/0905/0905.0459v1.pdf#page=71) 

   Let $X$ be a topological space as before, but consider now the
   geometry $\mathcal{G} = CRing^{op}$ to be the opposite category of
   commutative [[ring]]s, where a covering family of 
   $Spec R \in CRing^{op}$ is a family of maos of the form
   $R \to R[\frac{1}{r_i}]$ with $\{r_i \in R\}_i$ generating the unit
   ideal in $R$. So we think of $Spec R[\frac{1}{r_i}]$ as 
   an the open subset of $Spec R$ on wich the function $r_i$
   does not vanish, and a covering family we think of as an open 
   cover by such open subsets, in direct analogy to the above example.
 
   Now given a sheaf of rings 

   $$
     \bar O_X \in Sh(X,CRing)
   $$

   on $X$ (making $X$ a [[ringed space]]), which we 
   may regard as the functor

   $$
     O_X : CRing^{op} \to Sh(X)
   $$

   that it [[representable functor|represents]]

   $$
     O_X(Spec R) : U \mapsto  
                   Hom_{CRing^{op}}(\bar O_X(U), Spec R)
                           = Hom_{CRing}(R, \bar O_X(U))
   $$

   we check what 
   conditions this has to satisfy to qualify as a 
   structure sheaf in the above sense.

   The condition that

   $$
     \coprod_i O_X(Spec R[\frac{1}{r_i}])
     \to Spec R
   $$

   is an epimorphism of sheaves again means that it is [[stalk]]wise
   an epimorphism of sets. Now, a ring homomorphism 
   $R[\frac{1}{r_i}] \to \bar O_X(U)$ is given by
   a ring homomorphism $f : R \to O_X(U)$ such that $f(r_i)$ is
   invertible in $O_X(U)$. (We think of this as the pullback of
   functions on $Spec R$ to functions on $U$ by a map $U \to Spec R$
   that lands only in the open subset where the functoin $r_i$ is 
   non-vanishing).

   So the condition that the above is an epimorphism on small enough
   $U$ says that for every ring homomorphism $\phi : R \to \bar O_X(U)$
   the value of $\phi$ on at least one of the $r_i$ is invertible 
   element in $O_X(U)$. 

   Thinking of this dually this is just the same kind of statement as
   in the first example, really. But now we can say this more 
   algebraically: 

   by assumption there is a linear combination of the $r_i$ to the
   identity in $R$

   $$
     1 = \sum_i \alpha_i r_i
   $$

   in $R$ (the partition of unity of functions on $Spec R$) 
   and hence $\sum_i \alpha_i \phi(r_1) = 1$ in $(O_X)_x$
   That for this invertible finite sum at least one of the
   summands is invertible is the condition that $(O_X)_x$ is
   a _local ring_ .

   So [[ringed space]] has a structure sheaf in the above sense
   if it is a [[locally ringed space]].
   
   
=--



## Examples

### Ordinary ringed spaces

It may be worthwhile to retell the motivating example in the "Idea" introduction above for the maybe more familiar case of ordinary (1-categorical) structure sheaves with values in (unital) rings.

An ordinary [[topological space]] $X$ with its [[category of open subsets]] $Op(X)$ is a [[ringed space]] or $Op(X)$ is a [[ringed site]] if it is equipped with a [[sheaf]] $O_X : Op(X)^{op} \to Rings$ with values in the category of [[rings]]. For $U \subset X$ one thinks of $O_X(U)$ as the ring of allowed functions on $U$.

If for the moment we ignore the technicality that $O_X$ is supposed to be a [[sheaf]] and just regard it as a [[presheaf]], and if we furthermore invoke the idea of [[space and quantity]] and think of a ring $R$ as a generalized quantity in form of a copresheaf, canonically the [[representable functor|co-representable]] co-presheaf

$$
  R : (Ring^fin)^{op} \Set
$$

on finitely generated rings, which sends

$$
 R : R' \mapsto Hom(R,R')
$$

then we find that $O_X$ is in fact a presheaf on $Op(X)$ with values in a co-presheaf on $(Ring^{fin})^{op}$

$$
  O_X : Op(X)^{op} \to [(Ring^{fin})^{op}, Set]
$$

or equivalently a generalized quantity on $(Ring^{fin})^{op}$ with values in presheaves on $X$:

$$
  O_X : (Ring^{fin})^{op} \to [Op(X)^{op}, Set]
  \,.
$$

+--{: .query}
[[Mike Shulman]]: What is the admissibility structure on $(Ring^{fin})^{op}$ in this example?  It seems to me like you would want to consider only functions preserving finite limits, since that would amount to treating $(Ring^{fin})^{op}$ as the syntactic category of the theory of rings and you would recover the usual notion of a ring object in $Sh(X)$.  But preserving finite limits doesn't seem to be a property that could be specified by an admissibility structure.
=--


### Derived ringed spaces

Now formulate the previous example according to the above definition:

Let $CRing^{fin}$ be the category of finitely generated commutative rings There is a standard admissability structure on $(CRing^{fin})^{op}$ that makes it a _geometry_ in the above sense.

Then for $X$ a topological space an $(\infty,1)$-functor $(CRing^{fin})^{op} \to Sh(S)$ to $(infty,1)$-sheaves on $X$  is a sheaf of local commutative rings on $X$. ([StrSh, example 1.2.13](http://arxiv.org/abs/0905.0459))

To generalize this to **derived structure sheaves** we replace the category of rings here with the $(\infty,1)$-category of simplicial rings.

**Definition**  ([StrSh def 4.1.1](http://arxiv.org/abs/0905.0459))

The $(\infty,1)$-category of **simplicial commutative rings** over an ordinary commutative ring $k$ is

$$
  SCR_k := PSh_\Sigma(FreeAlg_k)
$$

the $(\infty,1)$-category of [[(∞,1)-presheaves]] on commutative $k$-algebras of the form $k[x_1, \cdots, x_n]$.

Then...

see also

* [[generalized scheme]]


### Derived smooth manifolds 

([StrSh, example 4.5.2](http://arxiv.org/abs/0905.0459))

Every ordinary smooth [[manifold]] $X$ becomes canonically a generalized space with structure sheaf as follows:

Let $V := Diff$ be some version of the category of smooth manifolds. This becomes a _pregeometry_ in the above sense by taking admissable morphisms to be inclusions of open submanifolds.

Then for $Sh(X) := Sh(Op(X))$ the $(\infty,1)$-topos of $(\infty,1)$-sheaves on $X$, the obvious $(\infty,1)$-functor

$$
  O_X : V \to Sh(X)
$$

which for every co-test manifold $v$ is the sheaf

$$
  O_X(v) : (U \subset X) \mapsto Hom_{Diff}(U,v)
$$

is a $Diff$-structure sheaf. Notice that this is precisely nothing but the structure sheaf of smooth functions from the introduction above. 

The point is that there are other, more fancy structure sheaves

$$
  O_X : V \to Sh(X)
$$

possible. They describe **[[derived smooth manifolds]]** as described in [DerSmooth](http://math.berkeley.edu/~dspivak/thesis2.pdf).

## References

The general theory is developed in

* **StrSh** [[Jacob Lurie]], [[Structured Spaces]] ([arXiv](http://arxiv.org/abs/0905.0459))

The special case of "smoothly structured spaces" called [[derived smooth manifold]] is 
discussed in 

* David Spivak, _Derived smooth manifolds_ PhD thesis ([pdf](http://www.uoregon.edu/~dspivak/files/thesis1.pdf))

Apart from looking at the special case this article also contains useful introduction
and details on the general case.

In the version of this that is available on the arXiv ([arXiv](http://arxiv.org/abs/0810.5174))
the point of view is more on bi-presheaves, a useful discussion to the relation
to structured morphisms here is in section 10.1. there.


[[!redirects structured (∞,1)-topos]]
[[!redirects structured generalized spaces]]
[[!redirects structured generalized space]]
[[!redirects ringed (∞,1)-topos]]
[[!redirects ringed generalized spaces]]
[[!redirects ringed generalized space]]
