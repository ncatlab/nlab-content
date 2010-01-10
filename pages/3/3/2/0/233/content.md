
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

### Basic idea

The basic idea is that a _module_ $V$ is an object equipped with an [[action]] by a [[monoid]] $A$. This is closely related to the concept of a [[representation]] of a [[group]].

A familiar example of a module is a [[vector space]] $V$ over a [[field]] $k$: this is a _module_ over $k$ in the category [[Ab]] of abelian groups. But nothing in the definition of [[vector space]] really depends on the fact that $k$ here is a [[field]]: more generally it could be any [[ring]] $R$. The analog of a vector space for fields replaced by rings is that of a module over the ring $R$.


### More general perspectives

There are two distinct and separately important perspective on the notion of module from the [[nPOV]]:

* modules may usefully be thought of in the context of [[enriched category theory]];

* modules may usefully be thought of in terms of [[abelian category|abelianization]]/[[stabilization]] of [[overcategory|overcategories]].

#### Enriched presheaves

The [[action]] $\rho$ of a [[monoid]] $A$ in a [[monoidal category]] $V$ may be equivalently encoded in terms of a  $V$-[[enriched functor]] 
   
   $$
     \rho : \mathbf{B}A \to V
   $$ 

   from the [[delooping]] one-object $V$-[[enriched category]] $\mathbf{B}A$ corresponding to $A$ to $V$ itself. 

   This means that more generally it makes sense to replace $\mathbf{B}A$ by any $V$-[[enriched category]] $C$ -- regarded as the [[horizontal categorification]] of a monoid, a "monoid-oid" -- and think of $V$-enriched functors $\rho : C \to V$ -- $V$-[[presheaf|presheaves]] -- as modules for $C$. 

   From this perspective a $C$-$D$-[[bimodule]] is a $V$-[[enriched functor]] $C^{op}\times D \to V$, which is in this context known as a [[profunctor]] from $C$ to $D$. The notion of the [[bicategory]] $V Mod$ of $V$-enriched categories, $V$-profunctors between these and transformations between those is then a generalization of the 

#### Stabilized overcategories

A module $N$ over a (commutative, unital) ring $R$ may be encoded in another ring: the one that as an abelian group is the [[direct sum]] $R \oplus N$ and whose product is defined by the formulas

$$
  (r_1, n_1) \cdot (r_2,n_2) := (r_1 r_2, r_1 n_1 + r_2 n_2)
  \,.
$$

This is a **square-0 extension** of $R$. It is canonically equipped with a ring homomorphism $R \oplus N \to R$ which is the identity on $R$ and sends all elements of $N$ to 0. As such, $R \oplus N \to R$ is an object in the [[overcategory]] $CRing/R$. But a special such object: it is in fact canonically an abelian [[group object]] in $CRing/R$, where the group operation (over $R$!) is given by addition of elements in $N$.

From this perspective, it makes sense for general [[category|categories]] $C$ to think of the [[abelian category|abelianization]] of their [[overcategory|overcategories]] $C/A$ as categories of modules over the object $A$.

Taken all together, this makes the fiberwise [[abelian category|abelianization]] of their [[codomain fibration]] $cod : [I,C] \to C$ the category of all possible modules over all objects of $C$.

This general perspective has a nice [[vertical categorification]] to the context of [[(∞,1)-category|(∞,1)-categories]]: abelianization becomes [[stabilization]] in this context, and the fiberwise stabilization of the [[codomain fibration]] of any [[(∞,1)-category]] $C$ is the [[tangent (∞,1)-category]] $T_C \to C$. 

For instance for $sAlg_k$ the [[(∞,1)-category]] of [[simplicial ring|simplicial algebras]] over a ground field $k$ of characteristic 0, we have that the [[stabilization]] $Stab(sAlgk/A)$ of the [[over quasi-category|over (∞,1)-category]] over $A$ is equivalent to the $(\infty,1)$-category $A Mod$ of 
$A$-modules.


## Details 

### Ordinary concept

A (right) module over a [[monoid]] $A$ [[internalization|internal to]] a [[monoidal category]] $(V, \otimes, I)$ is an object $N$ of $V$ equipped with a morphism

$$
  \rho : N \otimes A \to N
$$

in $C$ which satisfies the usual axioms of an [[action]].  

### In enriched category theory

Equivalently, regarding the [[monoid]] $A$ as a one-object $V$-[[enriched category]] $\mathbf{B}A$, the module together with its action are given by a $V$-[[enriched functor]]

$$
  \rho : \mathbf{B}A \to V
  \,.
$$

Correspondingly, a _left_ module over $A$ is a functor

$$
  \rho : (\mathbf{B}A)^{\mathrm{op}} \to V
  \,.
$$

In this language the concept directly generalizes to the [[horizontal categorification]] of monoids $A$. Let $K$ be _any_ $V$-[[enriched category]], then $V$-functors
$
  \rho : K \to V
$
give right modules and functors
$
  \rho : K^{\mathrm{op}} \to V
$ give left modules over $K$. Accordingly, for $K$ and $L$ two $V$-enriched categories one says that $V$-functors

$$
  K^{op} \otimes L \to V
$$

are _$K$-$L$-[[bimodule]]s_, also known as _profunctors_ or _[[distributor]]s_ from $K$ to $L$.



### In terms of stabilized overcategories {#DefWithOCat}



**Proposition** Let $R \in CRing$ be a commutative [[ring]]. Then there is a canonical [[equivalence of categories|equivalence]] between the [[category]] $R Mod$ of $R$-modules and the category $Ab(CRing/R)$ of abelian [[group object]]s in the [[overcategory]] of $CRing$ over $R$

$$
  R Mod \simeq Ab(CRing/R)
  \,.
$$

**Proof**

The unit of the abelian group object in $CRing/R$ is a diagram

$$
  \array{
     R &&\to&& K
     \\
     & {}_{\mathllap{Id}}\searrow && \swarrow^{\mathrlap{p}}
     \\
     && R
  }
  \,.
$$

This diagram identifies $K$ with a ring of the form $R \oplus ker(p)$ in which for $r \in R$ and $n \in ker(p)$ we have $r\cdot n \in ker(p)$. 

Furthermore...

## Examples

### Modules over rings {#Rings}

A [[ring]] is a [[monoid]] in [[Ab]]. Hence a module over a ring is first of all an [[object]] $N$ in [[Ab]], hence an abelian group. Moreover, it is equipped with a [[morphism]]

$$
  \alpha : R \otimes N \to N
$$ 

in [[Ab]]. On the left we have the [[tensor product]] of abelian groups. So this is a morphism that sends

$$
  (r,n ) \mapsto r n
$$

such that

$$
  (r, n_1 + n_2) \mapsto r n_1 + r n_2
$$

and

$$
  (r_1 + r_2, n) \mapsto r_1 n + r_2 n
  \,.
$$

Moreover, this morphism respects the monoid structure on $R$, in that the diagram

$$
  \array{
     R \otimes R \otimes N 
     &\stackrel{\cdot_R \otimes Id_N}{\to}& R \otimes N
     \\
     {}^{\mathllap{Id_R \otimes \alpha}}\downarrow 
     && 
     \downarrow^{\mathrlap{alpha}}
     \\
     R \otimes N &\to& N 
  }
$$

commutes. In formulas this means that 

$$
  (r_1 \cdot r_2) n = r_1 (r_2 n)
  \,.
$$

Finally the unit axioms says that the identity element of $R$ acts as the identity on $N$.

Saying the same fully in terms of [[enriched category theory]]:

Write $\mathbf{B}R$ for the [[Ab-enriched category]] with a single object and $R = \mathbf{B}A(\bullet, \bullet)$.
A module $N$ is an $Ab$-functor 
$$   
  N : \mathbf{B}R \to Ab 
  \,.
$$

The category $R Mod$ has $R$-modules as objects and $R$-module homomorphisms as morphisms.  More abstractly, this is the [[Ab]]-[[enriched functor category]] $[\mathbf{B}R,Ab]$.

### $G$-sets {#GSets}

Classically the notion of module is always regarded internal to [[Ab]], so that a module is always an abelian group with extra structure. But noticing that such abelian ring modules are just enriched presheaves in [[Ab]]-[[enriched category theory]], it makes sense to consider enriched presheaves in general $V$-enriched category theory as a natural generalization of the notion of module.

For that generalization the case of [[Set]]-[[enriched category theory]] plays a special basic role:

a [[group]] $G$ (with no extra structre, i.e. just a [[set]] with group structure) is a monoid in [[Set]]. A module over $G$ in the sense of [[Set]]-[[enriched functor]] (just an ordinary [[functor]])

$$
  \mathbf{B}G \to Set
$$

is nothing but a **$G$-set**: a [[set]] equipped with a $G$-action:

$\mathbf{B}G$ is the [[small category]] that is the [[delooping]] [[groupoid]] of $G$, which has a single object and $Hom_{\mathbf{B}G}(\bullet,\bullet) = G$. The functor $\mathbf{B}G \to Set$ takes the single object to some set $S$ and takes each morphism $(\bullet \stackrel{g}{\to} \bullet)$ to an [[automorphism]] $\rho(g) : S \to S$ of that set, such that composition is respected. This is just a [[representation]] of $G$ on the set $S$.

Of course for this story to work, $G$ need not be a group, but could be any [[monoid]].
 


### Modules over simplicial rings {#SimpRings}

Let $sAlg_k$ (or $sAlg$ for short) be the [[(∞,1)-category]] of commutative [[simplicial ring|simplicial algebras]] over a base field $k$. 

For $A \in sAlg_k$ there is generally a functor

$$
  A Mod \to Stab(sAlg_k/A)
$$

from the [[stable (∞,1)-category]] of $A$-modules to the [[stabilization]] of the [[overcategory]] of $sAlg$. But in general this functor is neither [[essentially surjective functor|essentially surjective]] nor [[full functor|full]]. If however $k$ has characteristic 0, then this is an equivalence.


## Related concepts

### Vector bundles and sheaves of modules

A [[vector space]] is a [[vector bundle]] over the [[point]]. For every [[vector bundle]] $E \to X$ over a [[space]] $X$, its collection $\Gamma(E)$ of [[section]]s is a module over the monoid/ring of functions on $X$. When $X$ is a [[ringed space]], $\Gamma(X)$ is usefully thought of as a [[sheaf]] of modules over the [[structure sheaf]] of $X$:

For describing vector bundles and their generalization it turns out that this perspective of encoding them in terms of their modules of sections is useful. For instance the category of vector bundles on a space typically fails to be an [[abelian category]]. But if instead of looking just as sheaves of modules on $X$ that arise as sections of vector bundles one generalizes to [[coherent sheaf|coherent sheaves of modules]] then one obtains an abelian category, something like the completion of $Vect(X)$ to an abelian category. If one further demands that the category be closed under push-forward operations, such as to obtain a [[bifibration]] of generalized vctor bundles over spaces, one arrives at the notion of [[quasicoherent sheaf|quasicoherent sheaves of modules]] over the [[structure sheaf]].

But it turns out that the category of [[quasicoherent sheaf|quasicoherent sheaves]] over a test space (see there for details) is equivalent simply to the category of _all_ modules over the (functions on) this test space. This means that quasicoherent sheaves of modules have a nice description in terms of the general-abstract-nonsense characterization of modules discussed above:

For $C$ our [[(∞,1)-category]] of of test [[space]]s (hence the [[opposite category]] $C^{op}$ our [[(∞,1)-category]] of "functions rings" on test spaces), by the above the assignment of all modules over a test space is given by

$$
  Mod : C^{op} \to (\infty,1)Cat
$$

$$
  Mod : U \mapsto Stab( C/U )
  \,.
$$

Then for $X$ any [[space]] regarded as an [[∞-stack]] on $C$, a "quasicorent $\infty$-stack of modules" on $X$ is a morphism 

$$
  X \to Mod
  \,.
$$

By the above discussion, this procedure yieelds the expected notions of modules in particular for the choice $C = (sAlg_k)^{op}$ of simplicial algebras over a ground ring of characteristic 0. The theory of quasicoherent sheaves of modules in this case is discussed in great detail at [[geometric ∞-function theory]]. Some more general remarks along these lines are at [[schreiber:∞-vector bundle]].




## References

### On modules as enriched presheaves

See also the references at [[enriched category theory]] and at [[profunctor]].


### On modules as stabilized overcategories

The observation that the category of modules over a ring $R$ is equivalent to the category of abelian group objects in the overcategory $CRing/R$ is originally due to Quillen:

* Quillen, _..._, (...)

...more classical references go here...

The fully abstract higher categorical concept in terms of [[stabilization|stabilized]] [[overcategory|overcategories]] and the [[tangent (∞,1)-category]] appears in 

* [[Jacob Lurie]], _[[Deformation Theory]]_


##Discussion##

+-- {: .query}

> An earlier version of this entry led to the following discussion.

[[Eric Forgy|Eric]]: The wikipedia page distinguishes left $R$-modules as covariant functors and right $R$-modules as contravariant functors. Is that distinction important?

[[John Baez|John]]: Yes, very --- but I didn't have the energy to get into that yet.  For any ring $R$ there's a ring $R^{op}$ in which $x y$ is redefined to be $y x$.   I defined a left $R$-module above; a right $R$-module is the same as a left $R^{op}$-module.  Eventually we'll have to discuss all this stuff, which becomes vastly more important when we start talking about bimodules.  If we want to show off, we'll do it all not just for rings, which are [[monoid|monoids]] in [[Ab]], but more generally for monoids in any [[symmetric monoidal category]].  For any monoid $M$ in a symmetric monoidal category we can define a new monoid $M^{op}$, and we can define left and right $M$-modules, and a right $M$-module is the same as a left $M^{op}$-module.

[[Sridhar Ramesh|Sridhar]]: Given that left modules on rings are the covariant functors while right modules on rings are the contravariant functors, why does the above definition of a module on a monoid make the left modules the contravariant functors and the right modules the covariant functors? Is this actually the conflicting convention?

_Toby_:  One problem is that this mixes with the conventions that one adopts for [[composition]].  What one person thinks is left multiplication, another will think is right multiplication.  I would rather talk about left/right modules for monoids or rings, then talk about covariant/contravariant functors from categories or additive categories.

=--


[[!redirects modules]]