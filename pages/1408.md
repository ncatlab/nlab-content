#Idea#

A _structured generalized space_ is a generalization of a [[ringed space]] or rather of a [[ringed site]]: a generalized space equipped with a _structure [[sheaf]]_ taking values in generalized quantities. 

Here the generalizaton is in the sense described at [[space and quantity]]:

* _spaces_ modeled on test spaces in some category $S$ are [[presheaf|presheaves]] $X$ on $S$: $X(U)$ is the collection of probes of $X$ by $U \in S$.

* _quantities_ (meaning: function algebras) modeled on value spaces in some category $S$ are [[presheaf|co-presheaves]] $A$ on $S$: $A(U)$ is the collection of the quantities with values  in $U \in S$.

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


#Definition#

Let $S$ be an $(\infty,1)$-[[site]], i.e. some small [[(infinity,1)-category]] equipped with a [[coverage]], and let $Sh(S)$ be the [[(infinity,1)-topos]] of [[(infinity,1)-category of (infinity,1)-sheaves]] on $S$. 

Notice that if $S = Op(X)$ is the nerve of the [[category of open subsets]] of some [[topological space]] $X$, then $Sh(X) := Sh(S)$ is the [[(infinity,1)-category of (infinity,1)-sheaves]] on $X$, as in the above motivating introduction. 

We want to define a _structure sheaf_ on $S$ (for instance on $Op(X)$) of quantities modeled on some $(\infty,1)$-category $V$ to be an [[(infinity,1)-functor]]

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

+-- {: .un_defn}
###### Definition ([StrSh, def 1.2.8](http://arxiv.org/abs/0905.0459))

An [[(infinity,1)-functor]]

$$
  O_X : V \to Sh(S)
$$

is a $V$-**structure** on $Sh(S)$ or 
$V$-**structure sheaf** on $S$ if it respects gluing in $V$ in that for $\{u_i \to v\}_i$ a collection of admissable morphisms in $V$ that generates a covering [[sieve]], the induced map

$$
  \coprod_i O_X(u_i) \to O_X(v)
$$

is an [[effective epimorphism]] in $Sh(S)$.
=--

Write $StrSh(S,V) \subset Func(V,Sh(S))$ for the full subcategory of such morphisms of the [[(infinity,1)-category of (infinity,1)-functors]].

+-- {: .un_remark}
###### Remark
Notice that in words following the above introduction this just says that we require that for every open subset $U$ of our space $X$, very function $f : U \to v$ on $U$ with values in $v$ can be built from a suitable collection of functions $f_i : U \to u_i$ if the $u_i$ cover  the codomain $v$.
=--





# Examples #

## ordinary ringed spaces ##

It may be worthwhile to retell the motivating example in the "Idea" introduction above for the maybe more familiar case of ordinary (1-categorical) structure sheaves with values in (unital) rings.

An ordinary [[topological space]] $X$ with its [[category of open subsets]] $Op(X)$ is a [[ringed space]] or $Op(X)$ is a [[ringed site]] if it is equipped with a [[sheaf]] $O_X : Op(X)^{op} \to Rings$ with values in the category of [[ring]]s. For $U \subset X$ one thinks of $O_X(U)$ as the ring of allowed functions on $U$.

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


## derived ringed spaces ##

Now formulate the previous example according to the above definition:

Let $CRing^{fin}$ be the category of finitely generated commutative rings There is a standard admissability structure on $(CRing^{fin})^{op}$ that makes it a _geometry_ in the above sense.

Then for $X$ a topological space an $(\infty,1)$-functor $(CRing^{fin})^{op} \to Sh(S)$ to $(infty,1)$-sheaves on $X$  is a sheaf of local commutative rings on $X$. ([StrSh, example 1.2.13](http://arxiv.org/abs/0905.0459))

To generalize this to **derived structure sheaves** we replace the category of rings here with the $(\infty,1)$-category of simplicial rings.

**Definition**  ([StrSh def 4.1.1](http://arxiv.org/abs/0905.0459))

The $(\infty,1)$-category of **simplicial commutative rings** over an ordinary commutative ring $k$ is

$$
  SCR_k := PSh_\Sigma(FreeAlg_k)
$$

the $(\infty,1)$-category of [[(infinity,1)-presheaf|(infinity,1)-presheaves]] on commutative $k$-algebras of the form $k[x_1, \cdots, x_n]$.

Then...


## derived smooth manifolds ##

([StrSh, example 4.5.2](http://arxiv.org/abs/0905.0459))

Every ordinary smooth manifold $X$ becomes canonically a generalized space with structure sheaf as follows:

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

possible. They describe **[[derived smooth manifold]]s** as described in [DerSmooth](http://math.berkeley.edu/~dspivak/thesis2.pdf).

#References#

* **StrSh** [[Jacob Lurie]], _Structured spaces_ ([arXiv](http://arxiv.org/abs/0905.0459))


* **DerSmooth** David Spivak, _Quasi-smooth derived manifolds_ ([pdf](http://math.berkeley.edu/~dspivak/thesis2.pdf), [blog](http://golem.ph.utexas.edu/category/2008/08/david_spivak_on_derived_manifo.html))