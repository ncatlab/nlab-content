<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>


#Contents#
* tic
{:toc}


## Idea

A **smooth algebra** or **$C^\infty$-ring** is an [[algebra]] $A$ over the reals $\mathbb{R}$ for which not only the product operation $\cdot : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ lifts to the algebra product $A \times A \to A$, but for which _every smooth map_ $f : \mathbb{R}^n \to \mathbb{R}^m$ ([[morphism]] in [[Diff]]) lifts to a smooth map $A(f) : A^n \to A^m$ in a compatible way. 

In short this means that $A$ is 

* a [[product]]-preserving [[presheaf|co-presheaf]] on [[CartSp]];

* equivalently: an algebra for the [[Lawvere theory]] [[CartSp]];

The smoothness of such $C^\infty$-rings is witnessed by the fact that this Lawvere theory is even a [[Fermat theory]].

The [[opposite category]] of the [[category]] of $C^\infty$-rings is the category of [[smooth loci]]. This and its subcategories play a major role as [[site]]s for [[category of sheaves|categories of sheaves]] that serve as  [[Models for Smooth Infinitesimal Analysis|models]] for [[synthetic differential geometry]].


## Motivating example

For $X$ a smooth [[manifold]], the assignment

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

+-- {: .un_defn}
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
that it collides badly with the use of $\infty$- for 
[[higher category theory|higher categorical]] structures. 

=--

+-- {: .query}
I don\'t see why this is a problem; it\'s not like our '$\infty$' ever gets into a superscript.  I find '$C^\infty$-ring' much more descriptive than 'generalized smooth algebra', in fact.  ---Toby

[[Urs Schreiber]]: I'll see what to do about it here. Over at [[derived smooth manifold]]s and related entried before long we'll have to be talking about "$\infty-C^\infty$-rings" or $C^\infty_\infty$-rings or the like, which is not good. Also, the term "$C^\infty$-ring" hides that it is necessarily an $\mathbb{R}$-algebras. Finally, the entire theory is really a special case of algebras over a [[Fermat theory]] and hence most other examples of a similar kind will by default be called algebras, not rings. For all these reasons I find "$C^\infty$-ring" an unfortunate term. But of course I am aware that it is entirely standard. 

=--

### Tensor product 

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



### Finitely generated $C^\infty$-rings

+-- {: .un_defn}
###### Definition

For $X$ a smooth [[manifold]], the smooth algebra 
$C^\infty(X)$ is the functor

$$
  C^\infty(X) := Hom_{Diff}(X,-)
$$

=--




+-- {: .un_defn}
###### Definition
**(finitely generated and finitely presented $C^\infty$-rings)**

For $R$ a $C^\infty$-ring, and $I \in U(R)$ an ideal in the underlying ordinary ring, there is a canonical $C^\infty$-ring structure $R/I$ on the ordinaryy quotient ring $U(R)/I$.

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

+-- {: .un_defn}
###### Definition
**(germ-determined finitely generated / fair )**

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

+-- {: .un_defn}
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

+-- {: .un_prop}
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

1. the forth step is the definition of $\mathb{L}$ as the [[opposite category]] of
   $C^\infty Ring^{op}$
   
1. the fifth step expresses that $C^\infty(R^n)$ is the free [[generalized smooth algebra]]
   on $n$ generators ([[Models for Smooth Infinitesimal Analysis|MSIA, chaper I, prop 1.1]])
   
=--

## Examples

### Functions on smooth manifolds

+-- {: .un_defn}
###### Definition

For $X$ a smooth [[manifold]], the smooth algebra 
$C^\infty(X)$ is the functor

$$
  C^\infty(X) := Hom_{Diff}(X,-)
$$

=--


### Weil algebras: functions on small infintiesimal spaces

A _Weil algebra_ in this context is a finite-dimensional commutative $\mathbb{R}$-algebra $W$ with a maximal ideal $I$ such that $W/I \simeq \mathbb{R}$ and $I^n = 0$ for some $n \in \mathbb{N}$. 

+-- {: .un_prop}
###### Proposition

There is a unique $C^\infty$-ring structure on a Weil alghebra $W$. It makes $W$ a finitely presented $C^\infty$-ring.

=--

+-- {: .un_remark}
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


### The underlying ordinary algebra

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


### Finitely presented $C^\infty$-rings

+-- {: .un_prop}
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

+-- {: .un_prop}
###### Proposition 

Points of a $C^\infty$-ring are in bijection with points of the underlying $\mathbb{R}$-algebra $U(C)$, i.e. with ordinary $\mathbb{R}$-algebra morphisms $U(C) \to \mathbb{R}$.

=--

In particular every Weil algebra $W$ has a unique point $* \to \mathbb{L}(W)$: every Weil algebra is the algebra of functions on an _infinitesimal thickening_ of an ordinary point.

By the properties of $C^\infty(X)$ for $X$ a smooth manifold discussed below, the $\mathbb{R}$-points of $C^\infty(X)$ are precisely the ordinary points of the manifold $X$.


### Smooth function algebras on smooth manifolds


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

=--

+-- {: .un_remark}
###### Remark 

In the context of [[geometric function theory]] the corresponding general statement (without the transversality condition) says that $C^\infty(X)$ is a "good" kind of function. The above equation is one sub-aspect of the one of the fundamental theorems of [[geometric infinity-function theory]].

=--



Turning this inclusion into an equivalence is usually called a _completion_ of the algebraic tensor product. Therefore we see:
+-- {: .standout}
The smooth tensor product is automatically the completed tensor product.
=--


In summary this yields the following characterization of smooth function algebras on manifolds.

+-- {: .un_theorem}
###### Theorem ([[Models for Smooth Infinitesimal Analysis|MSIA]], theorem 2.8)

The functor $C^\infty(-) = Hom_{Diff}(-,-) : Diff \to C^\infty Alg$ 

* is a [[full and faithful functor]]

* takes values in finitely presented smooth $C^\infty$-algebras

* sends transversal [[pullback]]s to [[coproduct]]s (and hence to the smooth tensor product).

=--

## Deformation theory of smooth algebras

Recall the general setup of [[deformation theory]] for objects in an arbitrary category $C$. Here we take $C = C^\infty Ring$ and see what happens.

As describe there, the key structure of interest in deformation theory is the tangent category 

$$
 T C \to C
 \,.
$$

Over each $A \in C$ its [[fiber]] is the category of abelian [[group object]]s in the [[overcategory]] $C/A$.

By an old argument by Quillen, for $C = $ [[CRing]] we have that $T C = Mod$ is the [[bifibration]] of [[module]]s over rings:

for $N$ an $A$-module, the corresponding object in the overcategory is the square-0-extension $R \oplus N \to R$.

We can then find various notions derived from $T C \to C$. For $C = CRing$ this is the following:

* a [[derivation]] $\delta A \to N$ is precisely a [[section]] of the corresponding morphism $A \olus N \to A$ in $C/A$, namely a ring homomorphism $Id \oplus \delta : A \to A \oplus N$.

* to be continued



## References {#References}

A standard textbook reference is chapter 1 of

* [[Ieke Moerdijk]] and [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ Springer (1991)

The concept of $C^\infty$-rings in particular and that of [[synthetic differential geometry]] in general was introduced in

* [[Bill Lawvere]], _Categorical dynamics_ 

  in [[Anders Kock]] (eds.) _Topos theoretic methods in geometry_, volume 30 of _Various Publ. Ser._, pages 1-28, Aarhus Univ. (1997)

but examples of the concept are older. A discussion from the point of view of [[functional analysis]] is in 

* G. Kainz, A. Kriegl, [[Peter Michor]], _$C^\infty$-algebras from the functional analytic view point_ Journal of pure and applied algebra 46 (1987) ([pdf](http://www.mat.univie.ac.at/~michor/c-oo-alg.pdf))

A characterization of those $C^\infty$-rings that are algebras of smooth functions on some smooth [[manifold]] is given in 

* [[Peter Michor]], [[Jiri Vanzura]], _Characterizing algebras of $C^\infty$-functions on manifolds_ ([pdf](http://www.emis.de/journals/CMUC/pdf/cmuc9603/michor.pdf))

Lawvere's ideas were later developed by [[Eduardo Dubuc]], [[Anders Kock]], [[Ieke Moerdijk]], [[Gonzalo Reyes]], and [[Gavin Wraith]]. 

Studies of the properties of $C^\infty$-rings include 

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[RingsOfSmoothFunctionsI.pdf:file]]_ , Journal of Algebra 99 (1986)

Synthetic spaces locally isomorphic to smooth loci were discussed in

* [[Eduardo Dubuc]], _$C^\infty$-schemes_ Amer. J. Math. 103 (1981) ([pdf](http://www.math.ist.utl.pt/~jroquet/Dubuc.pdf) [JSTOR](http://www.jstor.org/stable/select/2374046)).

and more recently in

* [[Dominic Joyce]], _Algebraic geometry over $C^\infty$-rings_ ([arXiv:1001.0023](http://arxiv.org/abs/1001.0023))


The [[higher geometry]] generalization to a theory of [[derived smooth manifold]]s -- [[space]]s with [[structure sheaf]] taking values in [[simplicial C∞-ring]]s -- was initiated in

* [[David Spivak]], _Quasi-Smooth derived manifolds_ 
  ([pdf of original version](http://www.uoregon.edu/~dspivak/thesis2.pdf), [arXiv:0810.5174](http://arxiv.org/abs/0810.5174))

based on the general machinery of [[structured (∞,1)-topos]]es in

* [[Jacob Lurie]], _[[Structured Spaces]]_

where this is briefly mentioned in the very last paragraph.

See also the references at [[Fermat theory]], of which $C^\infty$-rings are a sepcial case. And the references at [[smooth locus]], the formal dual of a $C^\infty$-ring.
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
