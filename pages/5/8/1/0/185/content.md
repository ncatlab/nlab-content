
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* tic
{:toc}


## Idea

A **smooth algebra** or **$C^\infty$-ring** is an [[algebra]] $A$ over the reals $\mathbb{R}$ for which not only the product operation $\cdot : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ lifts to the algebra product $A \times A \to A$, but for which _every smooth map_ $f : \mathbb{R}^n \to \mathbb{R}^m$ ([[morphism]] in [[Diff]]) lifts to a map $A(f) : A^n \to A^m$ in a compatible way. 

In short this means that $A$ is 

* a [[product]]-preserving [[presheaf|co-presheaf]] on [[CartSp]];

* equivalently: an algebra for the [[Lawvere theory]] [[CartSp]];

The smoothness of such $C^\infty$-rings is witnessed by the fact that this Lawvere theory is even a [[Fermat theory]].

The [[opposite category]] of the [[category]] of $C^\infty$-rings is the category of [[smooth loci]]. This and its subcategories play a major role as [[site]]s for [[category of sheaves|categories of sheaves]] that serve as  [[Models for Smooth Infinitesimal Analysis|models]] for [[synthetic differential geometry]].


## Motivating example

For $X$ a [[smooth manifold]], the assignment

$$
  \mathbb{R}^n \mapsto C^\infty(X,\mathbb{R}^n)
   = Hom_{Diff}(X,\mathbb{R}^n)
$$

of the [[set]] of smooth $\mathbb{R}^n$-valued functions on $X$ is clearly covariant and hence yields a co-presheaf on [[CartSp]] $\subset$ [[Diff]]: a [[functor]]

$$
  C^\infty(X,-) : CartSp \to Set
  \,.
$$

Since the [[hom-functor]] sends [[limit]]s to [[limit]]s in its second argument this is clearly [[product]] preserving. 

$$
  C^\infty(X, \mathbb{R}^n \times \mathbb{R}^m)
  \simeq
  C^\infty(X,\mathbb{R}^n)
  \times
  C^\infty(X, \mathbb{R}^m)
$$

If as usual we write $C^\infty(X) := C^\infty(X,\mathbb{R})$ for the set of just $\mathbb{R}$-valued smooth functions, then the usual pointwise product of functions

$$
 \cdot :  C^\infty(X) \times C^\infty(X) \to C^\infty(X)
$$ 

can be regarded as the image of our co-presheaf under the muliplication map $\mathbb{R} \times \mathbb{R} \stackrel{-\cdot -}{\to} \mathbb{R}$ on the algebra of real numbers:

$$
  \cdot
  :
  C^\infty(X)
  \times
  C^\infty(X)
  :=  
  C^\infty(X,\mathbb{R})
  \times
  C^\infty(X,\mathbb{R})
  \simeq
  C^\infty(X,\mathbb{R}\times \mathbb{R})
  \stackrel{C^\infty(X,-\cdot-)}{\to}
  C^\infty(X,\mathbb{R})
  =:
  C^\infty(X)
  \,.
$$


## Definitions

+-- {: .num_defn}
###### Definition

[[CartSp]] is the full subcategory of [[Diff]]
on manifolds of the form $\mathbb{R}^n$.

=--


+-- {: .num_defn}
###### Definition

A $C^\infty$-algebra is a finite [[product]]-preserving [[presheaf|co-presheaf]] on [[CartSp]], i.e. a finite [[product]] preserving [[functor]]

$$
  A : CartSp \to Set
  \,.
$$

The category of such functors and [[natural transformation]]s between them we denote by $C^\infty Alg$.


=--



+-- {: .num_remark}
###### Remark on terminology

The standard name in the literature for generalized smooth algebras is
**$C^\infty$-rings**. Even though standard, this has the disadvantages for us 
that it collides badly with the use of $\infty$- for 
[[higher category theory|higher categorical]] structures. 

=--


### Tensor product 

+-- {: .num_defn}
###### Definition (smooth tensor product)


The [[coproduct]] in $C^\infty Alg$
we call the **smooth tensor product**

$$
  \otimes_\infty : C^\infty Alg \times C^\infty Alg
   \to C^\infty Alg
  \,.
$$

More generally, for 
$i : C \to A$ and $j : C \to B$ two morphisms in $C^\infty Alg$, we call the [[pushout]]

$$
  \array{
    C &\stackrel{i}{\to}& A
    \\
    \downarrow && \downarrow
    \\
    B &\stackrel{j}{\to}& A \otimes_C B
  }
$$

the **smooth tensor product over $C$** of $A$ and $B$.

=--



### Finitely generated $C^\infty$-rings

+-- {: .num_defn}
###### Definition

For $X$ a [[smooth manifold]], the smooth algebra 
$C^\infty(X)$ is the functor

$$
  C^\infty(X) := Hom_{Diff}(X,-)
$$

=--




+-- {: .num_defn}
###### Definition
**(finitely generated and finitely presented $C^\infty$-rings)**

For $R$ a $C^\infty$-ring, and $I \in U(R)$ an ideal in the underlying ordinary ring, there is a canonical $C^\infty$-ring structure $R/I$ on the ordinary quotient ring $U(R)/I$.

A $C^\infty$-ring $R$ is called **finitely generated** if it is of the form $C^\infty(\mathbb{R}^n)/I$ for $n \in \mathbb{N}$ and $I $ an ideal in $U(C^\infty(\mathbb{R}^n))$. 

It is **finitely presented** if also $I$ is finitely generated, as an ideal, $I = (i_1, \cdots, i_k)$ with $i_j \in U(R)$.

This is equivalent to $R$ being a [[pushout]] of the form

$$

  \array{
    C^\infty(\mathbb{R}^k) &\to& C^{\infty}(*) \simeq \mathbb{R}
    \\
    \downarrow && \downarrow
    \\
    C^\infty(\mathbb{R}^n) &\to& R
  }
  \,.
$$

=--

+-- {: .num_defn}
###### Definition
**([[germ-determined ideal]])**

For $p \in \mathbb{R}^n$ let

$$
  \pi_p : C^\infty(\mathbb{R}^n) \to C^\infty_p(\mathbb{R}^n)
$$

be the natural projection onto the [smooth algebra of germs](#Germs) of functions at $p$.

A $C^\infty$-ring $C$ is called **fair** or **finitely generated and germ-determined** if it is finitely generated $C \simeq C^\infty(\mathbb{R}^n)/I$ and the ideal $I$ has the property that $f \in C^\infty(\mathbb{R}^n)$ is an element of $I$ if (and hence precisely if) for all $p \in \mathbb{R}^n$ the germ $\pi_p(f) \in C^\infty_p(\mathbb{R})^n$ is in the germ $\pi_p(I)$ of the ideal.


=--

### Internal $C^\infty$-rings

For any [[smooth topos]] $(\mathcal{T}, R)$, there is an [[internalization|internal]]
notion of [[generalized smooth algebra]]:

+-- {: .num_defn}
###### Definition (internal generalized smooth algebra)

For $(\mathcal{T}, R)$ a [[topos]] equipped with an [[internalization|internal]]
[[ring]] object $R$ (possibly but not necessarily a [[smooth topos]]), let
$CartSp(\mathcal{T},R)$ be the full [[subcategory]] of $\mathcal{T}$ on 
objects of the form $R^n$ for $n \in \mathbb{N}$. Then a
**$(\mathcal{T},R)$-algebra** is a product-preserving functor 
$A : CartSp(\mathcal{T}, R) \to Set$.
=--

All constructions on smooth algebras generalize to $(\mathcal{T},R)$-algebras.
In particular for $X \in \mathcal{T}$ any object we have the function 
$(\mathcal{T},R)$-algebra

$$
  C(X) : R^n \mapsto \mathcal{T}(X,R^n)
  \,.
$$


The following remark asserts that when $\mathcal{T}$ is itself
a sufficiently nice [[category of sheaves]] on formal duals of $(Set,\mathbb{R})$-algebras,
then the internal notion of smooth function algebras on formal duals
of external smooth algebras reproduces these external smooth algebras.

+-- {: .num_prop}
###### Proposition

Let $A$ be a finitely generated $C^\infty$-ring, $\ell A$ its incarnation as an object in 
$\mathbb{L} = (C^\infty Ring^{fin})^{op}$ and $Y\ell A$ its incarnation in 
$Sh(\mathbb{L}) \subset PSh(\mathbb{L})$, with $Y$ the [[Yoneda embedding]] and
using the assumption that the [[Grothendieck topology]] used to form $Sh(\mathbb{L})$
is [[subcanonical coverage|subcanonical]].

Also suppose that the line object $R$ is [[representable functor|represented]]
by $\ell C^\infty(\mathbb{R})$ 

Then we have for all
$A \in C^\infty Ring^{fin}$ that

$$
  C(Y\ell A) : R^n \mapsto A({*})^n
$$
=--

+-- {: .proof}
###### Proof

This is a straightforward manipulation:

$$
  \begin{aligned}
    Sh_{\mathbb{L}}(Y(\ell A), R^n)
    & =
    Sh_{\mathbb{L}}(Y(\ell A), Y(\ell C^\infty(\mathbb{R}^n)))
    \\
    & = PSh_{\mathbb{L}}(Y(\ell A), Y(\ell C^\infty(\mathbb{R}^n)))
    \\
    & \simeq \mathbb{L}(\ell A, \ell C^\infty(\mathbb{R}^n))
    \\
    & \simeq C^\infty Ring^{fin}(C^\infty(\mathbb{R}^n), A)
    \\
    & \simeq A({*})^n
  \end{aligned}  
$$

Here

1. the first step expresses the nature of the line object in the models under consideration

1. the second step expresses that the embedding $Sh(\mathbb{L}) \to PSh(\mathbb{L})$
   is a [[full and faithful functor]]
   
1. the third step expresses that the [[Yoneda embedding]] is a [[full and faithful functor]]

1. the fourth step is the definition of $\mathbb{L}$ as the [[opposite category]] of
   $C^\infty Ring^{fin}$
   
1. the fifth step expresses that $C^\infty(R^n)$ is the free [[generalized smooth algebra]]
   on $n$ generators ([[Models for Smooth Infinitesimal Analysis|MSIA, chaper I, prop 1.1]])
   
=--

### Local $C^\infty$-algebra

The category [[CartSp]] carries a natural [[Grothendieck topology]]. 

A smooth algebra

$$
  A : CartSp \to Set
$$

is a [[locally algebra-ed topos|local algebra]] if $A$ sends [[covering]] families  to epimorphism families: for each covering $\{U_i \to U\}$ the morphism 

$$
  \coprod_i A(U_i) \to A(U) 
$$

is an [[epimorphism]].

+-- {: .num_prop}
###### Proposition

Local smooth algebras are precisely the "local Archimedian" algebras (...).

=--

This is ([Bunge-Dubuc, prop. 2.1](#BungeDubuc)).

## Examples

### Functions on smooth manifolds

+-- {: .num_defn}
###### Definition

For $X$ a [[smooth manifold]], the smooth algebra 
$C^\infty(X)$ is the functor

$$
  C^\infty(X) := Hom_{Diff}(X,-)
$$

=--


### Weil algebras: functions on small infinitesimal spaces

A _Weil algebra_ in this context is a finite-dimensional commutative $\mathbb{R}$-algebra $W$ with a maximal ideal $I$ such that $W/I \simeq \mathbb{R}$ and $I^n = 0$ for some $n \in \mathbb{N}$. 

+-- {: .num_prop}
###### Proposition

There is a unique $C^\infty$-ring structure on a Weil algebra $W$. It makes $W$ a finitely presented $C^\infty$-ring.

=--

+-- {: .num_remark}
###### Remark


The [[smooth loci]] corresponding to Weil algebras are [[infinitesimal space]]s. Weil algebras play a crucial role in the definition of [[smooth topos]]es.

=--

### Power series 

...

### Functions on germs of manifolds {#Germs}

For $p \in \mathbb{R}^n$, the algebra of [[germ]]s of smooth $\mathbb{R}$-valued functions at $p$ carries an evident $C^\infty$-ring structure $C^\infty(\mathbb{R}^n)_p$.

With $I_p \subset C^\infty(\mathbb{R}^n)$ the ideal of functions that vanish on a neighbourhood of $p$ we have

$$
  C^\infty_p(\mathbb{R}^n) \simeq C^\infty(\mathbb{R}^n)/I_p
  \,,
$$ 

yielding a finitely generated but not (for $n \gt 0$) finitely presented $C^\infty$-ring. 



## Properties


### Limits and colimits


+-- {: .num_prop}
###### Proposition 

All [[limit]]s and all [[directed colimit]]s in $C^\infty Ring$ are computed objectwise in $[CartSp,Set]$ as limits in [[Set]].

=--

+-- {: .proof}
###### Proof

As discussed at [[limits and colimits by example]], all [[limit]]s and [[colimit]]s in $[CartSp,Set]$ are computed objectwise, so the remaining question is if they preserve the property of functors $CartSp \to Set$ to preserved products. The claim follows from the observation that [[limit]]s and [[directed colimit]]s do commute with products.

=--

See also [[Models for Smooth Infinitesimal Analysis|MSIA, p. 22]].

### The underlying ordinary algebra {#UnderlyingAlgebra}

There is a [[stuff, structure, property|forgetful functor]] 

$$
  U : C^\infty Alg \to Alg
$$

from generalized smooth algebras to ordinary algebras which is given by evaluation on $\mathbb{R}$

$$
  U : A \mapsto A(\mathbb{R})
$$

and equipping the set $A(\mathbb{R})$ with the algebra structure induced on it: 

the product and sum on $A(\mathbb{R})$ is the image of the corresponding operations on the algebra $\mathbb{R}$

$$
  \cdot_A 
  :
  A(\mathbb{R}) \times A(\mathbb{R})
  \stackrel{\simeq}{\to}
  A(\mathbb{R}\times \mathbb{R})
  \stackrel{A(\cdot)}{\to}
  A(\mathbb{R})
  \,.
$$

$$
  +_A :
  A(\mathbb{R}) \times A(\mathbb{R})
  \stackrel{\simeq}{\to}
  A(\mathbb{R} + \mathbb{R})
  \stackrel{A(\cdot)}{\to}
  A(\mathbb{R})
  \,.
$$

Moreover there is canonically a morphism of rings

$$
  \mathbb{R} \to A(\mathbb{R})
$$

given by

$$
  (* = \mathbb{R}^0 \stackrel{c}{\to} \mathbb{R})
  \mapsto
  (* = A(\mathbb{R}^0) \stackrel{A(c)}{\to} A(\mathbb{R}))
  \,.
$$

This makes $A(\mathbb{R})$ an $\mathbb{R}$-algebra.

+-- {: .num_prop}
###### Proposition 

The [[forgetful functor]] $U$ fits into an [[adjunction]]

$$
  (F \dashv U)
  :
  C^\infty Alg_{\mathbb{R}}
  \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
  Alg_{\mathbb{R}}
  \,.
$$


=--


+-- {: .proof}
###### Proof

This statement may be understood as a special case of the following more general statement: 

* If $S$, $T$ are [[finitary monad]]s and $f: S \to T$ is a monad morphism, then the relative forgetful functor
$$f^*: Alg_T \to Alg_S,$$ 
which [[pullback|pulls back]] a $T$-algebra $\xi: T X \to X$ to the $S$-algebra $\xi \circ f X: S X \to X$, admits a [[left adjoint]]. 

(In the case under discussion, $S$ is the free algebra monad on $Set$, $T$ is the free smooth algebra monad, and $f: S \to T$ is induced from the obvious inclusion $f(n): S(n) \to T(n)$ which interprets an $n$-ary algebra operation (in the theory $Th_S$) as a smooth operation in the theory $Th_T$. See [[finitary monad]] for discussion on the connection between finitary monads $T$ and Lawvere theories $Th_T$.)  

The desired left adjoint $f_!$ takes an algebra $\theta: S X \to X$ to the [[reflexive coequalizer]] exhibited as a diagram  

$$T S X \stackrel{\overset{(\mu_T \circ T f)X}{\to}}{\underset{T\theta}{\to}} T X \stackrel{\pi}{\to} T \otimes_S X$$ 

in the category of $T$-algebras, where $\mu_T: T T \to T$ is the monad multiplication. The coequalizer is denoted $T \otimes_S X$ to emphasize the analogy with pushing forward $S$-modules $X$ along a ring homomorphism $f: S \to T$ to get $T$-modules; the proof below is an arrow-theoretic transcription of the usual proof of the adjunction between pushing forward and pulling back in the context of rings and modules. 

A finitary monad $T$ [preserves reflexive coequalizers](http://ncatlab.org/nlab/show/reflexive+coequalizer#applications_4), so that there is a canonical isomorphism 

$$T(T \otimes_S X) \cong (T T) \otimes_S X$$

It follows that $T$-algebra ($T$-module) maps $\bar{g}: T \otimes_S X \to Y$, i.e., maps that render commutative the diagram 

$$\array{
T T \otimes_S X & \stackrel{T\bar{g}}{\to} & T Y \\
\mu \otimes_S X \downarrow & & \downarrow \xi \\
T \otimes_S X & \underset{\bar{g}}{\to} & Y
}$$ 

are in bijection with maps $g: T X \to Y$ that render commutative 

$$\array{
T T X & \stackrel{T g}{\to} & T Y \\
\mu \downarrow & & \downarrow \xi \\
T X & \underset{g}{\to} & Y
}$$ 

(that is to say, $T$-algebra maps $g: T X \to Y$) which additionally coequalize the parallel pair in the diagram 

$$T S X \stackrel{\overset{(\mu_T \circ T f)X}{\to}}{\underset{T\theta}{\to}} T X \stackrel{g}{\to} Y$$

Since $f: S \to T$ is a monad morphism, we have commutativity of parallel squares in 

$$\array{
T S X & \stackrel{\overset{(\mu_T \circ T f)X}{\to}}{\underset{T\theta}{\to}} & T X & \stackrel{g}{\to} & Y \\
f S X \uparrow & & \uparrow f X & & \\
S S X & \stackrel{\overset{\mu_S X}{\to}}{\underset{S \theta}{\to}} & S X
}$$

so that $g \circ f X$ coequalizes the bottom pair. However, because $g: T X \to Y$ is a $T$-algebra map, its pullback $g \circ f X: S X \to Y$ defines an $S$-algebra map $S X \to f^* Y$. This $S$-algebra map $g \circ f X$ factors through the coequalizer of the bottom pair of maps in $Alg_S$, i.e., factors uniquely through an $S$-algebra map $X \to f^*Y$. This establishes the adjunction $f_! \dashv f^*$. 

=--



### Finitely presented $C^\infty$-rings

+-- {: .num_prop}
###### Proposition ([[Models for Smooth Infinitesimal Analysis|MSIA]], prop. 1.1)

$C^\infty(\mathbb{R}^n)$ is the free smooth algebra
on $n$ generators, in that for every $n \in \mathbb{N}$ 
and every smooth algebra $A$ there is an [[adjunction]]
isomorphism

$$
  Hom_{C^\infty Alg}(C^\infty(\mathbb{R}^n), A)
  \simeq
  Hom_{Alg}(\mathbb{R}[x_1,...,x_n], A(\mathbb{R}))
  \,.
$$

=--



* Every finitely presented $C^\infty$-ring is fair/germ determined.

We have a chain of inclusions

* finitely presented $C^\infty$-rings

* $\subset$ "good" $C^\infty$-rings

* $\subset$ fair $C^\infty$-rings

* $\subset$ finitely generated $C^\infty$-rings


### Points of smooth loci

An **$\mathbb{R}$-point** of a $C^\infty$-ring $C$ is a point $* \to \mathbb{L}(C)$ of the corresponding [[smooth locus]], i.e. a morphism $C \to \mathbb{R} \cong C^\infty(*)$.

+-- {: .num_prop}
###### Proposition 

Points of a $C^\infty$-ring are in bijection with points of the underlying $\mathbb{R}$-algebra $U(C)$, i.e. with ordinary $\mathbb{R}$-algebra morphisms $U(C) \to \mathbb{R}$.

=--

In particular every Weil algebra $W$ has a unique point $* \to \mathbb{L}(W)$: every Weil algebra is the algebra of functions on an _infinitesimal thickening_ of an ordinary point.

By the properties of $C^\infty(X)$ for $X$ a smooth manifold discussed below, the $\mathbb{R}$-points of $C^\infty(X)$ are precisely the ordinary points of the manifold $X$.


### Smooth function algebras on smooth manifolds
  {#SmoothFunctionAlgebrasOnSmoothManifolds}


+-- {: .num_prop}
###### Proposition ([[Models for Smooth Infinitesimal Analysis|MSIA]], prop. 2.5, 2.6 )

Let $f : X \to Z$ and $g : Y \to Z$ be  [[transversal maps]] of [[smooth manifold]]s. Then the functor $C^\infty(-)$ sends the [[pullback]]

$$
  \array{
    X \times_Z Y &\to& X
    \\
    \downarrow && \downarrow^f
    \\
    Y &\stackrel{g}{\to}& Z
  }
$$

to the [[pushout]]

$$
  \array{
    C^\infty(X) \otimes_{C^\infty(Z)} C^\infty(Y)
    =: & C^\infty(X \times_Z Y) &\leftarrow& C^\infty(X)
    \\
    & \uparrow && \uparrow^{f^*}
    \\
    & C^\infty(Y) &\stackrel{g^*}{\leftarrow}& C^\infty(Z)
  }
$$


=--

In particular this implies (for $Z = {*}$)that the the smooth tensor product of functions on $X$ and $Y$ is the algebra of functions on the [[product]] $X \times Y$:

$$
  C^\infty(X \times Y) \simeq C^\infty(X) \otimes_\infty C^\infty(Y)
  \,.
$$

+-- {: .num_remark}
###### Remark 


The ordinary algebraic tensor product of $C^\infty(X)(\mathbb{R})$ and $C^\infty(Y)(\mathbb{R})$ regarded as ordinary algebras does _not_ in general satisfy this property. Rather one has an inclusion

$$
  C^\infty(X)(\mathbb{R}) \otimes C^\infty(Y)(\mathbb{R})
  \subset
  C^\infty(X \times Y)(\mathbb{R})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark 

In the context of [[geometric function theory]] the corresponding general statement (without the transversality condition) says that $C^\infty(X)$ is a "good" kind of function. The above equation is one sub-aspect of the one of the fundamental theorems of [[geometric infinity-function theory]].

=--



Turning this inclusion into an equivalence is usually called a _completion_ of the algebraic tensor product. Therefore we see:
+-- {: .standout}
The smooth tensor product is automatically the completed tensor product.
=--


In summary this yields the following characterization of smooth function algebras on manifolds.

+-- {: .num_theorem}
###### Theorem ([[Models for Smooth Infinitesimal Analysis|MSIA]], theorem 2.8)

The functor $C^\infty(-) = Hom_{Diff}(-,-) : Diff \to C^\infty Alg$ 

* is a [[full and faithful functor]]

* takes values in finitely presented smooth $C^\infty$-algebras

* sends transversal [[pullback]]s to [[coproduct]]s (and hence to the smooth tensor product).

=--

## Deformation theory of smooth algebras

> **under construction**

For $C$ any category whose objects we think of as "functions algebras on test spaces", such as $C = C^\infty Ring$, there is a general intrinsic notion of [[tangent complex]] and [[deformation theory]] of such objects. 

As describe there, the key structure of interest from which all the other structure here is induced is the **tangent category**

$$
 T C \to C
 \,.
$$

This is $T C = Ab(Arr(C))$ the [[codomain fibration]] of $C$ "fiberwise stabilized", meaning that in each fiber one takes it to consist of $Ab(C/A)$, the abelian [[group object]]s in the [[overcategory]]. 


We now first recall what this means for ordinary rings and how it induces the ordinary notion of derivations and  modules for ordinary rings by setting $C = $ [[CRing]],  and then look at what it implies for $C^\infty$-rings by setting $C = C^\infty Rings$.

By an old argument by Quillen, for $C = $ [[CRing]] we have that $T C = Mod$ is the [[bifibration]] of [[module]]s over rings, there is a natural equivalence

$$
  Mod_A \stackrel{\simeq}{\to} Ab(C/A)
  \,.
$$

This is induced by the functor that sends
an $A$-module $N$ to the corresponding object in 
the square-0-extension $R \oplus N \to R$. (See [[module]]).

From this structure alone a lot of further structure follows:

* a [[derivation]] $\delta A \to N$ is precisely a [[section]] of the corresponding morphism $A \oplus N \to A$ in $C/A$, in the category $C$ namely a ring homomorphism 

  $$
    \array{
      A &&\stackrel{\delta}{\to}&& A \oplus N
      \\
      & {}_ {=}\searrow && \swarrow
      \\
      && A
    }
    \,.
  $$

* The forgetful functor $T Ring \simeq Mod \to Ring$ has a [[left adjoint]] 

  $$  
    \Omega_K^1 : Ring \to Mod
  $$

  that sends each ring to its module of [[Kähler differential]]s.

  The fact that it is left adjoint is the universal property
  of the K&#228;hler differentials as the objects co-representing
  derivations

  $Hom_{Ab(Ring/R)}(\Omega_K^1(A),N) \simeq 
  Hom_{Ring/A}(A,A \oplus N)$.

  So every derivation $\delta : A \to N$ uniquely corresponds to a module morphism $\Omega^1_K(A) \to N$, namely the one that sends 
  $d a \mapsto \delta(a)$.

This abstract story remains precisely the same for $C^\infty$-rings (and in fact for everything else!) but what it means concretely changes.

The crucial observation is (as one can show) that an abelian group object in $C^\infty Ring/A$ is a square-0 extension $(A \oplus N)$ for $N$ an (ordinary) module of the _underlying_ $\mathbb{R}$-algebra $A$. This square-0-extension happens to be _uniquely_ equipped with the $C^\infty$-Ring-structure given by

$$
  (f \in C^\infty(\mathbb{R}^n) \to \mathbb{R})
  \mapsto
  \left(
     (a_1, n_1), \cdots, (a_n, n_n))
     \mapsto
      f(a_1, \cdots, a_n)
      + 
      \sum_{i = 1^n} \frac{\partial f}{\partial x_i}(a_1, \cdots, a_n) n_i
  \right)
  \,.
$$

This uniquely induced smooth structure on objects in $Ab(C^\infty Ring/A)$ then in turn affects the nature of the notion of derivation and of K&#228;hler differentials, as those are defined by general abstract reasoning from the former.

First of all it follows that a [[derivation]] -- by general abstract definition  a morphism of $C^\infty$-rings $Id \oplus \delta : A \to A \oplus N$ -- is a morphism that satisfies _for all_ $f \in C^\infty(\mathbb{R}^n, \mathbb{R})$ that

$$
  \delta : f(a_1, \cdots, a_n) \mapsto 
  \sum_i \frac{\partial f}{\partial x_i}
  \delta a_i
  \,.
$$

For ordinary rings only the compatibility $\delta (a_1 \cdot a_2) = \delta (a_1) a_2 + a_1 \delta(a_2)$ with the single product operation is required. Here, however, compatibility with infinitely more operations $f \in C^\infty(\mathbb{R}^n, \mathbb{R})$ is demanded.

Accordingly, then, the K&#228;hler differentials as defined with respect to such derivations are different from the purely ring-theoretic ones: they produce the _right_ notion of smooth 1-forms here, whereas the ring-theoretic one does not.

## Variants

The generalization of the notion of smooth algebra for  [[(∞,1)-category theory]] is

* [[smooth (∞,1)-algebra]].

The generalization to [[supergeometry]] is

* [[smooth superalgebra]].

## Related concepts

* [[germ-determing C-infinity ring]]

* [[Dubuc topos]]

* [[embedding of smooth manifolds into formal duals of R-algebras]]

* [[derivations of smooth functions are vector fields]]

## References {#References}

Textbook account

* [[Ieke Moerdijk]]. [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ Springer (1991)

The concept of $C^\infty$-rings in particular and that of [[synthetic differential geometry]] in general was introduced in

* [[Bill Lawvere]], _Categorical dynamics_ 

  in [[Anders Kock]] (eds.) _Topos theoretic methods in geometry_, volume 30 of _Various Publ. Ser._, pages 1-28, Aarhus Univ. (1979)

but examples of the concept are older. A discussion from the point of view of [[functional analysis]] is in 

* G. Kainz, A. Kriegl, [[Peter Michor]], _$C^\infty$-algebras from the functional analytic view point_ Journal of pure and applied algebra 46 (1987) ([pdf](http://www.mat.univie.ac.at/~michor/c-oo-alg.pdf))

A characterization of those $C^\infty$-rings that are algebras of smooth functions on some [[smooth manifold]] is given in 

* [[Peter Michor]], [[Jiri Vanzura]], _Characterizing algebras of $C^\infty$-functions on manifolds_ ([pdf](http://www.emis.de/journals/CMUC/pdf/cmuc9603/michor.pdf))

Lawvere's ideas were later developed by [[Eduardo Dubuc]], [[Anders Kock]], [[Ieke Moerdijk]], [[Gonzalo Reyes]], and [[Gavin Wraith]]. 

Studies of the properties of $C^\infty$-rings include 

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[RingsOfSmoothFunctionsI.pdf:file]]_ , Journal of Algebra 99 (1986)

The notion of the spectrum of a $C^\infty$-ring and that of $C^\infty$-[[schemes]] is discussed in

* [[Eduardo Dubuc]], _$C^\infty$-schemes_ Amer. J. Math. 103 (1981) ([pdf](http://www.math.ist.utl.pt/~jroquet/Dubuc.pdf) [JSTOR](http://www.jstor.org/stable/select/2374046)).

and more generally in

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _Rings of smooth functions and their localization II_ , in _Mathematical logic and theoretical computer science_ page 275 ([Google books](http://books.google.nl/books?id=w02XaOa_0HAC&pg=PA262&lpg=PA262&dq=smooth+zariski+topos&source=bl&ots=Hj0AN3Lz3y&sig=TqRwTXz_u5R30AN2udLNOMQ2Ly0&hl=nl&ei=mCWZS-eLJcaD-QalyZlS&sa=X&oi=book_result&ct=result&resnum=2&ved=0CA4Q6AEwAQ#v=onepage&q=smooth%20zariski%20topos&f=false))

* [[Marta Bunge]], [[Eduardo Dubuc]], _Archimedian local $C^\infty$-rings and models of synthetic differential geometry_ Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 3 (1986), p. 3-22 ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_3_3_0)).
 {#BungeDubuc}

More recent developments along these lines are in

* [[Dominic Joyce]], _Algebraic geometry over $C^\infty$-rings_ ([arXiv:1001.0023](http://arxiv.org/abs/1001.0023))


The [[higher geometry]] generalization to a theory of [[derived smooth manifold]]s -- [[space]]s with [[structure sheaf]] taking values in [[simplicial C∞-ring]]s -- was initiated in

* [[David Spivak]], _Quasi-Smooth derived manifolds_ 
  ([pdf of original version](http://www.uoregon.edu/~dspivak/thesis2.pdf), [arXiv:0810.5174](http://arxiv.org/abs/0810.5174))

based on the general machinery of [[structured (∞,1)-topos]]es in

* [[Jacob Lurie]], _[[Structured Spaces]]_

where this is briefly mentioned in the very last paragraph.

See also the references at [[Fermat theory]], of which $C^\infty$-rings are a special case. And the references at [[smooth locus]], the formal dual of a $C^\infty$-ring.
And the references at [[super smooth topos]], which involves generalizations of $C^\infty$-rings to [[supergeometry]].


[[!redirects smooth algebras]]
[[!redirects generalized smooth algebra]]
[[!redirects generalized smooth algebras]]
[[!redirects C-infinity-ring]]
[[!redirects C-infinity ring]]
[[!redirects C-infinity-rings]]
[[!redirects C-infinity rings]]
[[!redirects C-∞-ring]]
[[!redirects C-∞ ring]]
[[!redirects C-∞-rings]]
[[!redirects C-∞ rings]]