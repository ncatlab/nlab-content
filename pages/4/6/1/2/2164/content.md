<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

An infinitesimal quantity is a quantity which is infinitely small in size, yet not necessarily perfectly small (zero).  An infinitesimal object is an object whose [[generalised elements]] are to be thought of as infinitesimal quantities.

+-- {: .query}
Do all of the following really involve infinitesimal *objects*?  Or should we move the others to [[infinitesimal quantity]] to clarify that this page is about objects of categories as defined below?  ---Toby

[[Urs Schreiber]]: good point. I think Lawvere's definition is, as stated, to be thought of as defining _infinitesimal space_s, yes. For infinitesimal quantities it will likely have to be dualized (in the hopefully obvious way). 

So maybe we should rename the entry here into _infinitesimal space_ and, yes, create another entry on infinitesimal quantities. Yes, I think that's a good idea. I have to run now, but I can implement it later.

_Toby_:  I could do it too, although I\'d like to see what Zoran thinks.

_Zoran_: I don't really feel/know what is the most sensitive here. Surely our understanding is developing and we will see more in future (you see yet another thing are the sheaves supported on infinitesimal neighborhoods as well as the duality between infinitesimals and (regular) differential operators in algebraic setting, the duality whose analogue I do not understand in the smooth context (cf. Maszczyk 0611806). 
=--

## in synthetic differential geometry ##

In the context of [[synthetic differential geometry]] the notion of
the _infinitesimal small_, which was historically formalised and is still
widely thought of in terms
of the limit constructions of differential calculus, is conceived 
instead axiomatically in terms of special properties of certain
_infinitesimal objects_ in a suitable [[topos]] of [[space]]s. 

## in algebraic geometry ##

In [[algebraic geometry]]
there is an earlier and closely related formalism of infinitesimal neighborhoods, which is the foundation of Grothendieck's approach to [[regular differential operators]], costratifications, crystalline cohomology and de Rham descent. The infinitesimal thickenings also appear in a variant of noncommutative geometry of Kapranov
, and in the language of abelian categories of quasicoherent sheaves in the work of Lunts and Rosenberg on regular differential operators in noncommutative context, which strongly takes into account tensor product.

## in nonstandard analysis ##

See 

* [[nonstandard analysis]]


# Definition #

## atomic space ##

+-- {: .un_defn}
###### Definition (Lawvere)

In a [[cartesian closed category]] $C$ an [[object]] $D$ is called
**infinitesimal** or **tiny** or **atomic** if the [[hom-functor]]
$(-)^D : C \to C$ for maps out of $D$ (i.e. the functor of 
[[exponential object|exponentiation]] by $D$) is a [[left adjoint]], i.e.
if it has a [[right adjoint]].
=--

In particular, since every [[left adjoint]] functor preserves colimits,
such an object is a [[compact object]].


Here is how to think of what this definition means intuitively. For that, notice how maps out of an ordinary space fail to preserve colimits:

for definiteness, consider the case of a [[cover]] of a [[space]] $X$ by spaces $\{U_i \to X\}_i$ so that $X$ is the [[coequalizer]]

$$
  (\coprod_{i,j} U_i \times_X U_j)
  \stackrel{\to}{\to}
  (\coprod_i U_i)
  \to X
$$

as discussed in detail at [[sieve]] and [[sheaf]]. This says effectively that every point of $X$ is element of at least one of the covering spaces $U_i$ and that one obtains $X$ by identifying the points in the covering spaces that correspond to the same one in $X$.

Now let $\Sigma$ be any other space. We may assume here that the [[internal hom]] $[\Sigma,-] : T \to T$ at least preserves [[coproduct]]s, so that applying this functor to the above diagram yields

$$
  (\coprod_{i,j} [\Sigma,U_i \times_X U_j])
  \stackrel{\to}{\to}
  (\coprod_i [\Sigma,U_i])
  \to [\Sigma,X]
  \,.
$$

Now notice how this will in general fail to still be a [[coequalizer]]: if it were, for one the morphism $  (\coprod_i [\Sigma,U_i])
  \to [\Sigma,X]$ would have to be an [[epimorphism]]. But this can't be in general, because it would mean that every map $\Sigma \to X$ factors through one of the covering spaces. The problem here is that in general the image of $\Sigma \to X$ may be _larger_ than any of the $U_i$.

This is maybe most familiar in the context of [[loop space]]s (for $\Sigma$ the circle): the loop space of a cover of $X$ is not in general a cover of the loop space.

But suppose that $\Sigma$ were infinitesimal. One thning that should mean is that there is no other space that is "effectively smaller" in some useful sense. For $\Sigma$ infinitesimal, we do expect that every map $\Sigma \to X$ can always be factored through at least one of the $U_i$: because $\Sigma$ is so small, the image of a map out of it can never be too large.

So only if $\Sigma$ qualifies as having infinitesimal extension can the functor $[\Sigma,-]$ be expected to preserve colimits.

## formal infinitesimal space ##

**definition**
**(formal infinitesimal space)**

An object $\Delta$ in a [[smooth topos]] $(\mathcal{T}, R)$
is called a **formally infinitesimal object** if it is the
algebra-spectrum of a Weil-$R$-algebra in $\mathcal{T}$

$$
  \Delta \simeq Spec_R(W)
  \,,
$$

where 

* $W = R \oplus J$ is an [[internalization|internal]] $R$-algebra object in $\mathcal{T}$
  with $J$ an $R$-finite dimensional nilpotent ideal
  
* $Spec_R(W) := R Alg_{\mathcal{T}}(W,R) \subset R^W$ is the [[subobject]]
  of the [[internal hom]] of morphisms that respect the $R$-algebra structure
  on $W$ and $R$.


All the spaces that are described as collection of degree $n$ infinitesimal
neighbours are of this form. Infinitesimal spaces not of this form
are germ-spaces. These violate the finite-dimensionality assumption on $J$.



# Examples #

We list some standard examples of infinitesimal spaces that exist in 
reasonably nice contexts, in particular in contexts that model the axioms of 
[[synthetic differential geometry]] including the [[Kock-Lawvere axiom]].


## the infinitesimal interval ##

There are several different objects that one may think 
of as an infinitesimal interval. 

The smallest of them is often denoted $D$ and sometimes called the 
"disembodied tangent vector" or the "walking tangent vector". It is
such that a morphism $D \to X$ into a [[manifold]] $X$ is the same as
a choice of point $x \in X$ and of a [[tangent vector]] 
$v \in T_x X$. Equivalently, it is such that restricting a smooth function
$f : \mathbb{R} \to \mathbb{R}$ along the inclusion 
$D \hookrightarrow \mathbb{R}$ produces the first-order [[jet]] defined
by $f$ at the point $0 \hookrightarrow D \to \mathbb{R}$.

Accordingly, for each $k \in \mathbb{N}$ 
there is a "slightly bigger" infinitesimal interval often denoted $D_k$, which 
is such that restricting a smooth function $f : \mathbb{R} \to \mathbb{R}$
along $D_k \to \mathbb{R}$ produces the order-$k$ jet represented by this 
function at the given point. 

Still infinitesimal but bigger than all these is the object 
$\Lambda_0 := \cap_{0 \in U \subset \mathbb{R}} U$ of intersections of all
neighbourhods of the origin of $\mathbb{R}$. This is such that the restriction of
a map $f : \mathbb{R} \to \mathbb{R}$ along $\Lambda_0 \hookrightarrow \mathbb{R}$
produces the [[germ]] of $f$ at $0$. 


### concrete realizations of the smallest infinitesimal interval: $D$ ###

The classical example of a realization of an infinitesimal object
is in terms of what is (traditionally but undescriptively)
called the _ring of [[dual number]]s_. For that we place ourselves
in some context in which [[space]]s are characterized [[duality|dually]]
in terms of the [[space and quantity|quantities]] on them, i.e. in terms of their
would-be function algebras. 

For some real number $t \in \mathbb{R}$, 
functions on the closed [[interval]] $[-t,t] \subset \mathbb{R}$ 
of length $2 t$ may be thought of 
as represented by functions on the whole real line $\mathbb{R}$, where
two representatives represent the same function on the interval if they differ
by a function that vanishes on the interval.

Precisely: 

+-- {: .un_lemma}
###### Lemma

The ([[generalized smooth algebra|generalized smooth]]) algebra of smooth 
functions $C^\infty([-t,t])$ on $[-t,t]$ is isomorphic to the quotient of the
algebra of smooth functions $C^\infty(\mathbb{R})$ on all of $\mathbb{R}$ by the
functions that vanish on $[-t,t]$

$$
  C^\infty([-t,t]) \simeq C^\infty(\mathbb{R})/\{f \in C^\infty(\mathbb{R})| \forall x \in [-t,t]: f(x) = 0\}
    \,.
$$
=--

+-- {: .proof}
###### Proof

This is a corollary of the smooth version of [[Tietze's theorem]], 
which says that for $U \subset \mathbb{R}^n$ a closed subset, every smooth
function on $U$ extends to a smooth function on all of $\mathbb{R}^n$.

See page 20 of [[Models for Smooth Infinitesimal Analysis|MSIA]].
=--


As we think of the length of the interval shrinking to an infinitesimal 
value, the notion of derivative of functions is such that we want to say
that the statement "a function vanishes on the infinitesimal interval"
is equivalent to "a function vanishes at the origin and its first derivative there vanishes, 
too". This in turn is usually equivalent (in a smooth context) to "a function is a square of a function that vanishes
at the origin".


Accordingly, in a context where one considers [[polynomial]] functions over the [[ground field]]
$k$, the infinitesimal
interval is given by the [[space]] -- usually called $D$ --
that is [[duality|dual]] to the [[ring]]
$k[\epsilon] := k[Z]/Z^2$ which is the quotient of the polynomial ring in 
one variable $Z$ modulo the polynomial $Z^2$. This is often called the 
**ring of dual numbers** (where the term 'dual' historically refers to its being $2$-dimensional). In terms of generators and relations this is the ring
generated by a single element $\epsilon$ subject to the relation that $\epsilon^2 = 0$.

Similarly, in the smooth context of, for instance, Moerdijk--Reyes
_[[Models for Smooth Infinitesimal Analysis]]_, $D$ is the [[space]] [[duality|dual]]
to the [[generalized smooth algebra]] $C^\infty(\mathbb{R})/J^2$ obtained as the
smooth functions on the real line modulo squares of functions that vanish at the origin.

+-- {: .un_defn}
###### Definition (the $1$-dimensional infinitesimal space)

In the context of [[generalized smooth algebra]], the $1$-dimensional infinitesimal
space is the space $D$ whose function algebra is the quotient 

$$
  C^\infty(D) := C^\infty(\mathbb{R})/\{x^2\}
$$

of all functions on the real line, modulo those that are a product with the function $x \mapsto x^2$.
=--

This does reproduce the above ring of dual numbers due to _Hadamard's lemma_,
which says that for $g \in C^\infty(\mathbb{R})$ a smooth function, there exists
a smooth function $h \in C^\infty(\mathbb{R})$ such that for all $x \in \mathbb{R}$
we have
$g(x) = g(0) + x g'(x) + x^2 h(x)$. So modulo $x^2$, every smooth function is in fact
a polynomial function. 

+--{.query}
Zoran:  reason, if my memory is right, Leites in his around 1976 survey of supermanifolds proveds and puts important role of Hadamard's lemma in supercontext, but I do not recall details, maybe somebody shoudl check.
=--

See pages 19&20 of _[[Models for Smooth Infinitesimal Analysis|MSIA]]_.

In this dual generators-and-relations description, the infinitesimal interval is very
familiar in many mathematically less sophisticated contexts. It prevails for instance
in the basic physics textbook treatment since [[Newton]] up to this day. [[Sophus Lie]] is famously
quoted as having said that he found many of his famous insights by such 
"synthetic reasoning" and only a lack of proper formalization prevented him
from writing them up in this way instead of in the more wide-spread way of 
differential calculus.


### the axiomatic definition of the infinitesimal interval ###

More generally, one may abstract the above properties of concrete realizations
of the infinitesimal interval such as to get such a notion in an arbitrary suitable
context. A suitable context for [[synthetic differential geometry]] is any
[[topos]] $C$ equipped with an [[internalization|internal]] [[commutative ring]] $R$. 

Using the [[topos]]-[[internal logic]] we may speak of both $R$ and $D$ as 
if they were [[set]]s, where "element" means [[generalized element]]. This 
way we have:

+-- {: .un_defn}
###### Definition (infinitesimal interval)

Let $C$ be a topos with commutative ring object $R$. Then the **infinitesimal interval**
$D$ is the [[subobject]] of $R$ of all those elements whose square is 0.

$$
  D = \{x \in R | x^2 = 0\}
$$
=--

It may be helpful to recall that in terms of [[limit]]s this notation means that
$D$ is the [[equalizer]] of 

$$
  R \stackrel{(-)^2}{\to} R
$$

and

$$
  R \stackrel{}{\to} 0 \stackrel{}{\to} R
  \,.
$$

For with $x : U \to D$ any morphism embodying a generalized element
$x \in D$, the universal property of the [[limit]] identifies this
uniquely with a morphism $U \to R$, hence with a generalized element 
of $R$, such that $U \to R \stackrel{(-)^2}{\to} R$ is the $0$ element 
of $R$ with domain of definition $U$ : $\cdots = U \to 0 \to R$.


## the infinitesimal $k$-cube

This works analogously to how the $k$-[[cube]] is the $k$-fold [[cartesian product]]
$D^k$ of the [[unit interval]] $[-1,1]$ with itself.

+-- {: .un_defn}
###### Definition

The infinitesimal $k$-cube $D^k$ is the $k$-fold cartesian product of the
infinitesimal interval $D$ with itself.

This means that in terms of generalized elements we have

$$
  D^k = \{(x_1, \cdots, x_n) \in R^n | \forall j,k  : \;x_j \cdot x_k = 0 \}
$$
=--


## the infinitesimal $k$-disk

+-- {: .un_defn}
###### Definition

For $n\in \mathbb{N}$ the infinitesimal $k$-disk is

$$
  D(n) := \{ (x_1,\cdots, c_k) \in R^k | \forall j,k : x_j \cdot x_k = 0 \}
$$
=--

+-- {: .un_remark}
###### Remark

Since in particular $x_j^2 = 0$ for all elements of the 
infinitesimal $n$-disk, we have an inclusion

$$
  D(n) \subset D^n
$$

which is proper if $n \gt 1$. For $n = 1$ we have $D(1) = D$.

While $D(n)$ is closed under multiplication by elements of $R$, it is
not in general closed under addition of its elements. For instance for
$d_1,d_2 \in D(1) = D$ we have that $d_1 + d_2$ (the operation being in $R$)
is still in $D$ precisely if $(d_1,d_2)$ is in $D(2)$.
=--


## the infinitesimal neighbourhood ##

For $x \in X$ a point in a manifold, the infinitesimal [[neighbourhood]] $U_p$ is the intersection of all open neighbourhoods of $x$. This is such that the restriction of a function $f : X \to \mathbb{R}$ along the inclusion $U_p \to X$ is precisely the [[germ]] of the function $f$.

All of the infinitesimal spaces above are contained in the corresponding infinitesimal neighbourhood. So this is the "largest" of the infinitesimal spaces discussed here.


#References#

Infinitesimal spaces and their properties were familiar in all
those areas where spaces are characterized by the algebras of functions on them.

It was in a seminal lecture 

* [[William Lawvere]], _Categorical Dynamics_ lectures at the University of Chicago (1967) 

reproduced in  

* [[Anders Kock]], _Topos theoretic methods in Geometry_, Aarhus Universitet (1979)

that the proposal was made
to axiomatize the properties of infinitesimal objects by making use
of the fact that they are supposed to be objects of a 
[[cartesian closed category]].

It was from this insight that [[synthetic differential geometry]] was
eventually developed. 

* Lawvere, _Outline of synthetic differential geometry_,
([web](http://www.acsu.buffalo.edu/~wlawvere/downloadlist.html))

This is a classical case of [[general abstract nonsense]] used to
understand a subtle situation.

A summary and discussion of the axiomatically defined standard infinitesimal 
objects $D$, $D_k$, $D_k(n)$ is in section 1.2 of

* Anders Kock, _Synthetic Geometry of Manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

## atomic spaces ##

Details on the right adjoint to the exponentiation functor $(-)^X$ for
$X$ an infinitesimal object are in appendix 4 of 

* Moerdijk, Reyes, _[[Models for Smooth Infinitesimal Analysis]]_


## formally infinitesimal spaces ##

For formal infinitesimal objects and Weil algebras see 

section I.16 of 

* [[Anders Kock]], _Synthetic differential geometry_ ([pdf]())

and chapter I, section 4 and chapter II, theorem 1.13 and onwards in

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal  Analysis]]





[[!redirects infinitesimal space]]
[[!redirects infinitesimal quantity]]