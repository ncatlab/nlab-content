<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>

#Contents#
* tic
{:toc}

#Idea#

A **smooth algebra** or **$C^\infty-ring$** is an [[algebra]] $A$ over the reals for which not only the product operation $\cdot : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ lifts to the algebra product $A \times A \to A$, but for which _every smooth map_ $f : \mathbb{R}^n \to \mathbb{R}^m$ ([[morphism]] in [[Diff]]) lifts to a smooth map $A(f) : A^n \to A^m$ in a compatible way. 

In short this means that $A$ is a [[product]]-preserving [[presheaf|co-presheaf]] on [[CartSp]].

The [[opposite category]] of the [[category]] of $C^\infty$-rings is the category of [[smooth loci]]. This and its subcategories play a major role as [[site]]s for [[category of sheaves|categories of sheaves]] that serve as  [[Models for Smooth Infinitesimal Analysis|models]] for [[synthetic differential geometry]].


#Motivating example#

For $X$ a smooth [[manifold]], the assignment

$$
  \mathbb{R}^n \mapsto C^\infty(X,\mathbb{R}^n)
   = Hom_{Diff}(X,\mathbb{R}^n)
$$

of the [[set]] of smooth $\mathbb{R}^n$-valued functions on $X$ is clearly covariant and hence yields a co-presheaf on [[CartSp]] $\subset$ [[Diff]]. Since the [[hom-functor]] sends [[limit]]s to [[limit]]s in its second argument this is clearly [[product]] preserving. 

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



#Definitions#

 {: .un_defn}
###### Definition

[[CartSp]] is the full subcategory of [[Diff]]
on manifolds of the form $\mathbb{R}^n$.

=--


+-- {: .un_defn}
###### Definition

A $C^\infty$-algebra is a finite [[product]]-preserving [[presheaf|co-presheaf]] on [[CartSp]], i.e. a finite [[product]] preserving [[functor]]

$$
  A : CartSp \to Set
  \,.
$$

The category of such functors and [[natural transformation]]s between them we denote by $C^\infty Alg$.


=--



+-- {: .un_remark}
###### Remark on terminology

The standard name in the literature for generalized smooth algebras is
**$C^\infty$-rings**. Even though standard, this has the disadvantages for us 
that it collides badly with the use of $\infty-$ for 
[[higher category theory|higher categorical]] structures. 

=--


+-- {: .un_defn}
###### Definition

For $X$ a smooth [[manifold]], the smooth algebra 
$C^\infty(X)$ is the functor

$$
  C^\infty(X) := Hom_{Diff}(X,-)
$$

=--



+-- {: .un_defn}
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


## internal smooth algebras ##

For any [[smooth topos]] $(\mathcal{T}, R)$, there is an [[internalization|internal]]
notion of [[generalized smooth algebra]]:

**definition**
**(internal generalized smooth algebra)**

For $(\mathcal{T}, R)$ a [[topos]] equipped with an [[internalization|internal]]  
[[ring]] object $R$ (possibly but not necessarily a [[smooth topos]]), let
$CartSp(\mathcal{T},R)$ be the full [[subcategory]] of $\mathcal{T}$ on 
objects of the form $R^n$ for $n \in \mathbb{N}$. Then a
**$(\mathcal{T},R)$-algebra** is a product-preserving functor 
$A : CartSp(\mathcal{T}, R) \to Set$.

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
**Pro

Let $A$ be a finitely generated $C^\infty$-ring, $\ell A$ its incarnation as an object in 
$\mathbb{L} = (C^\infty Ring^{fin})^{op}$ and $Y\ell A$ its incarnation in 
$Sh(\mathbb{L}) \subset PSh(\mathbb{L})$, with $Y$ the [[Yoneda embedding]] and
using the assumption that the [[Grothendieck topology]] used to form $Sh(\mathbb{L})$
is [[subcanonical coverage|subcanonical]].

Also that the line object $R$ is [[representable functor|represented]]
by $\ell C^\infty(\mathbb{R})$ 

Then we have for all
$A \in C^\infty Ring^{fin}$ that

$$
  C(Y\ell A) : R^n \mapsto A({*})^n
$$


**Proof**

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

1. the forth step is the definition of $\mathb{L}$ as the [[opposite category]] of
   $C^\infty Ring^{op}$
   
1. the fifth step expresses that $C^\infty(R^n)$ is the free [[generalized smooth algebra]]
   on $n$ generators ([[Models for Smooth Infinitesimal Analysis|MSIA, chaper I, prop 1.1]])
   






# Properties #

## general properties ##

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


+-- {: .un_prop}
###### Proposition ([[Models for Smooth Infinitesimal Analysis|MSIA]], prop. 1.1)

$C^\infty(\mathbb{R})$ is the free smooth algebra
on $n$ generators, in that for every $n \in \mathbb{N}$ 
and every smooth algebra $A$ there is an [[adjunction]]
isomorphism

$$
  Hom_{C^\infty Alg}(C^\infty(\mathbb{R}^n), A)
  \simeq
  Hom_{Alg}(\mathbb{R}^n, A(\mathbb{R}))
  \,.
$$

=--

+-- {: .un_remark}
###### Remark 

While a product-preserving co-presheaf $A$ induces the structure of an algebra on each of the sets $A(\mathbb{R}^n)$, with product induced from the componentwise product $\mathbb{R}^n \times \mathbb{R}^n  \to \mathbb{R}^n$, it is not a _co-presheaf with values in algebras_: the co-restriction morphisms assigned to maps $\mathbb{R}^n \to \mathbb{R}^m$ which are not just projections or injections will not be algebra homomorphisms.

But conversely this means that restricted to such maps, i.e. restricted along the inclusion $FinSet \hookrightarrow CartSp$ of [[CartSp]], $A$ does become a co-presheaf with values in algebras. 

=--


+-- {: .un_remark}
###### Remark 

In the context of [[geometric function theory]] the corresponding general statement (without the transversality condition) says that $C^\infty(X)$ is a "good" kind of function. The above equation is one sub-aspect of the one of the fundamental theorems of [[geometric infinity-function theory]].

=--


## smooth function algebras on manifolds ##


+-- {: .un_prop}
###### Proposition ([[Models for Smooth Infinitesimal Analysis|MSIA]], prop. 2.5, 2.6 )

Let $f : X \to Z$ and $g : Y \to Z$ be  [[transversal maps]] of smooth [[manifold]]s. Then the functor $C^\infty(-)$ sends the [[pullback]]

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

+-- {: .un_remark}
###### Remark 


The ordinary algebraic tensor product of $C^\infty(X)(\mathbb{R})$ and $C^\infty(Y)(\mathbb{R})$ regarded as ordinary algebras does _not_ in general satisfy this property. Rather one has an inclusion

$$
  C^\infty(X)(\mathbb{R}) \otimes C^\infty(Y)(\mathbb{R})
  \subset
  C^\infty(X \times Y)(\mathbb{R})
  \,.
$$

Turning this inclusion into an equivalence is usually called a _completion_ of the algebraic tensor product. Therefore we see that the **smooth tensor product is automatically the completed tensor product** .

=--



In summary this yields the following characterization of smooth function algebras on manifolds.

+-- {: .un_theorem}
###### Theorem ([[Models for Smooth Infinitesimal Analysis|MSIA]], theorem 2.8)

The functor $C^\infty(-) = Hom_{Diff}(-,-) : Diff \to C^\infty Alg$ 

* is a [[full and faithful functor]]

* takes values in finitely presented smooth $C^\infty$-algebras

* sends transversal [[pullback]]s to [[coproduct]]s (and hence to the smooth tensor product).

=--













#References#

This definition was introduced in 

* Ieke Moerdijk and Gonzalo E. Reyes, [[Models for Smooth Infinitesimal Analysis]] Springer (1991)

Chpater I deals with generalized smooth algebras, where they are called **$C^\infty$-rings**.

See also

* Lawvere, _Categorical dynamics_ in _Topos theoretic methods in geometry_, volume 30 of _Various Publ. Ser._, pages 1-28, Aarhus Univ. (1997)


A brief but useful review is also on p. 3 of

* David Spivak, _Quasi-Smooth derived manifolds_ ([pdf](http://math.berkeley.edu/~dspivak/thesis2.pdf))


[[!redirects generalized smooth algebras]]
[[!redirects C-infinity-ring]]
[[!redirects smooth algebra]]