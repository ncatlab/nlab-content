
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--

> under construction

> so far these are notes taken in talks by [[Ezra Getzler]]

#Contents#
* table of contents
{:toc}

## $L_\infty$-algebras

The notion of [[L-infinity algebra]] is something that naturally arises in [[deformation theory]]
and in [[descent]] problems. 

A [[dg-Lie algebra]] is a [[chain complex]] of [[vector space]]s

$$
  \cdots
  \to
  V^{-1}
  \stackrel{d}{\to}
  V^0
  \stackrel{d}{\to}
  V^1
  \stackrel{d}{\to}
  V^2
  \to
  \cdots
$$

and is equipped with a bracket operation

$$
  [-,-] : V^i \otimes V^j \to V^{i + j}
$$

which is

* bilinear

* graded antisymmetric: $[x,y] = - (-1)^{deg(x) deg(y)} [y,x]$

* satisfies the graded Jacobi identity $[x,[y,z]] = [[x,y],z] + (-1)^{deg(x) deg(y)} [y,[x,z]]$.

* is graded Leibnitz: $d[x,y] = [d x,y] + (-1)^{deg(x)} [x, d y]$.
(aka a graded derivation)

**Note** If $deg(x)$ is odd, then $[x,x]$ need not vanish. (see also [[super Lie algebra]]).

Let $L$ be a [[dg-Lie algebra]], degreewise finite dimensional ("of finite type" in the language of [[rational homotopy theory]]).

We can form its [[Chevalley-Eilenberg algebra]] (see there for details) of cochains

$$
  CE(L) = (\wedge^\bullet L[1]^*, d)
$$

a [[quasi-free dga]]. 

(N.B. In full generality, read this as

$$
  CE(L) = ((\wedge^\bullet L[1])^*, \delta)
$$
and regard 
$$
 \wedge^\bullet L[1]
$$
as a graded commutative COalgebra.)

The underlying graded algebra we may dually think of as functions on some 
space, a (so-called) **formal graded manifold**.

The total differential 

$$
  \delta = \delta_1 + \delta_2
$$

where the first is $d$ and the second is the dual of the bracket: $[-,-]^*$ extended as a 
graded derivation.

Being a [[derivation]], dually we may think of this as a [[vector field]]
on our formal smooth manifold. This is sometimes called an [[NQ-supermanifold]].

**Definition**

An [[L-infinity algebra]] (see there) 
of finite type  is the evident generalization of this
inroduced by [[Jim Stasheff]] and [[Tom Lada]]

what kind of link is needed here??

 in the early 1990s:

An [[L-infinity algebra]]  is equivalent to  ( in the degreewise finite dimensional case) a
free graded-commutative algebra equipped with a differential of degree +1.

Now the differential corresponds to a sequence of $n$-ary brackets. For $n = 1$ this is
the differential on the complex, for $n = 2$ this is the binary bracket from 
above, and then there are higher brackets.


### Morphisms of $L_\infty$-algebras

One can consider two notions of morphisms: strict ones and general ones.

A strict one would be a linear map of the underlying vector spaces that
strictly preserves all the brackets.

A general definitin of morphisms is: in terms of the dual [[dg-algebra]]s
just a morphism of these, going the opposite way. In the dual formulation this 
is due to Lada and Stasheff.

We may also think of this as a morphism of [[NQ-supermanifold]]s.

All this arose in this form probably most vivedly in the [[BFV-BRST formalism]] or in the [[BV-BRST formalism]].

So in components such a morphism $f : L \to K$ of $L_\infty$-algebras 
consists of $n$-ary maps

$$
 f_k : L^{i_1} \otimes \cdots L^{i_k} \to K^{i_1 + \cdots + 1 - k}
$$

(where the shift in the indices is due to the numbering convention here only).

### The homotopical category of $L_\infty$-algebra

We will now describe on the [[category]] of $L_\infty$-algebras the structure of
a [[category of fibrant objects]].

The issue is that the category of $L_\infty$-alghebras as defined above has not
all products and coproducts. 

But we can turn it into a [[category of fibrant objects]].

#### A notion of category of fibrant objects {#GetzlerCatFibOb}

This is analogous to (in fact an example of the same general fact) 
how [[Kan complex]]es inside all [[simplicial set]]s
are the fibrant objects of the [[model structure on simplicial sets]] but do
not form among themselves a [[model category]] but a 
[[category of fibrant objects]].

See [[Kan complex]] for more...

We now look at the axioms for our category of fibrant objects. It is a slight
variant of those in [[BrownAHT]] described at
[[category of fibrant objects]] and draws bit from work of Dwyer and Kan.

Let $C$ be a [[category]]. The axioms used here are the following.

1. There is a [[subcategory]] $W \subset C$ 
   whose morphisms are called **weak equivalences**, 
   such that this makes $C$ into a 
   [[category with weak equivalences]].

1. There is another [[subcategory]] $F \subset C$, whose morphisms
   are called  **fibrations** (and those that are also 
   in $W$ are called **acyclic fibrations**) , such that

   * it contains all [[isomorphism]]s;

   * the [[pullback]] of a fibration is again a fibration.

   * the pullback of an acyclic fibrations is an acyclic fibration.

1. $C$ has all [[product]]s and in particular a [[terminal object]] $*$.


#### Filtered $L_\infty$-algebras as a Getzler-category of fibrant objects {#Filtered}

Write $\mathbb{L}$ for the category of _filtered_ [[L-infinity algebra]]s

Let $L^\bullet$ be a [[graded vector space]]

a decreasing filtrration on it is

$$
  L = F^0 L \supset F^1 L \supset \cdots 
$$

such that $L$ is the [[limit]] over this 

$$
  L \simeq \lim_{\leftarrow} L/F^1 K
$$

i.e. if $(x_i \in F^i L)$ then $\sum_{i=0}^\infty x_i$ exists

something missing here

$$
  [-,- , \dots ]_k
$$

has filtration degree 0 if $k \gt 0$ or filtration degree 1 if $k = 0$.

The differential $d x = [x]_1$ has the property 

namely?

Then $gr(d)$ is a  true differential $gr(L)$

Morphisms:

$$
  f_k : L^{\otimes k} \to N
$$

where we take $f_k$ to have filtration degree 0 for $k \gt 0$ and filtration degree 1
for $k = 0$.

So $gr(f_1)$ is a morphism of complexes from $gr(L)$ to $gr(N)$.

**Definition** A morphism $f$ is a **weak equivalence** if $gr(f)$ is a 
[[quasi-isomorphism]] of complexess.

It is a **fibration** if $gr(f_1)$ is surjective. 

**Theorem** This defines the structure of 
a (Getzler-version of a) [[category of fibrant objects]]
as defined above.

Given $C$ be a Getzler-[[category of fibrant objects]].

Define a new Getzler-category of fibrant objects $s C$ as follows:

* The [[object]]s  of $s C$ are [[simplicial object]]s in $C$, subject to 
  a condition stated in the following item.

* As in the [[Reedy model structure]], for $X_\bullet$ a simplicial objects
  let $M_k X_\bullet$ be the corresponding _matching object_ , defined by the 
  [[pullback]] diagram
  
  $$
    \array{
      M_k X_\bullet &\to& (X_{k-1})^{k+1}
      \\
      \downarrow && \downarrow
      \\
      (X_{k-2})^{\left(k+1 \atop 2\right)}&\to& (M_{k+1} X_\bullet)^{k+1}
    }
    \,.
  $$ 
  
  Here the right vertical morphism is assumed to be a fibration, hence so
  is the left vertical morphism. 
  
  So $M_k X_\bullet$ comes with a map $X_k \to M_k X_\bullet$. We assume that this 
  is a fibration. This allows us to define $M_{k+1} X_\bullet$ and to continue
  the induction.
  
  So this defines a _Reedy fibrant object_ .
  
So the objects of $s C$ are Reedy fibrant objects $X_\bullet$ and morphisms are morphisms
of simplicial objects.

The weak equivalences in $s C$ are taken to be the levelwise weak equivalences.

The fibrations are taken to be the Reedy fibrations, as in the [[Reedy model structure]],
i.e. those morphisms $X_\bullet \to Y_\bullet$ such that 
$X_k \to Y_k \times_{M_k Y_\bullet} M_k X_\bullet$ is a fibration for all $k$.

So this is just the [[full subcategory]] of the [[Reedy model structure]] on 
$[\Delta^{}op], C$ on the fibrant objects.

There is still a fourth axiom for Getzler-cats of fibrant objects to be stated, which 
is the existence of [[path space object]]s. We take this to be gven by a 
**path space functor**

$$
  P : C \to s C
$$

which is such that 

1. for all $X$ the face maps of $(P X)_\bullet$ are weak 
equivalences;

1. $P$ preserves fibrations and acyclic fibrations;

1. $(P X)_0$ is [[natural isomorphism|naturally isomorphic]] to $X$.

**Examples** 

If $C$ is the category of [[Kan complex]]es, then $P_k X = sSet(\Delta[k],X)$.

**Proposition**

For our category $\mathcal{L}$ of filtered $L_\infty$-algebras we may set

$$
  P_k L = L \otimes_{compl} \Omega^\bullet(\Delta^k)
   =
   \lim_{\leftarrow} L \otimes \Omega / F^i L \otimes \Omega
   \,,
$$
where $\otimes_{compl}$ denotes the completed tensor product, more commonly denoted $\hat \otimes$.

**Remark**

We may also speak of cofibrant objects in a (Getzler-) [[category of fibrant objects]]:

those objects $X$ such that for all acyclic fibrations $f : A \to B$ the induced
map $C(X,A) \to C(X,B)$ is surjective (i.e. those with [[left lifting property]]
again acyclic fibrations).

#### Maurer-Cartan elements

All the above is designed to make the following come out right.

Generally, $C(*,X)$ is the set of points ([[global element]]s) of $X$.


A morphism from the terminal object into an $L_\infty$-algebra is a [[Maurer-Cartan element]]
in the $L_\infty$-algebra. 

Such a point is just an element of degree 1 and filtration degree 1 that satisfies the equation

$$
  \sum_{k= 0}^{\infty} \frac{1}{k!}
   [\omega, \cdots, \omega]_k = 0
   \,.
$$

In the case of [[dg-Lie algebra]]s, this is just the familiar Maurer-Cartan equation
$$
  d \omega + \frac{1}{2}[\omega, \omega] = 0
  \,.
$$

We have that $C(*, P_k X)$ is a functor from $C$ to the category of [[Kan complex]]es.


For the category of Kan complexes, it is the identity functor.

For filtered $L_\infty$-algebras it gives

$$
  L \mapsto MC_\bullet(L) = MC(L \otimes \Omega^\bullet(\Delta^\bullet))
$$

This functor $MC_\bullet$ takes fibrations to fibrations and acyclic fibrations to
acyclic fibrations and weak equivalences to weak equivalences.

Other applications to sheaves of $L_\infty$-algebras

Evaluate on a [[Cech-nerve]] to get a cosimplicial $L_\infty$-algebra

$L^\bullet = (L^0 , L^1, \cdots)$

$L^k = \prod_{i_0, \cdots, i_k} L(U_{i_0} \cap \cdots \cap U_{i_k})$

$$
  Tot(L^\bullet) = \int_{k \in \Delta} L^k \otimes \Omega^\bullet(\Delta^k)
  \,.
$$

If $L$ is a [[dg-Lie algebra]], then 

$$
  MC_1(L)
  =
  \left\{
     \omega_0 + \omega_1 d t
     |\quad 
     \omega_1 \in F^1 L^1 [t],\quad \omega_1 \in F^1 L^0 [t]
     , \quad 
     d_L \omega_0 + [\omega_1, \omega_1] = 0,
     \quad d_{dR} \omega_0 + [\omega_1, \omega_0] = 0
  \right\} 
$$

Now define the **Deligne groupoid** as in Getzler' integration article.

We find inside the large Kan complex of MC-elements a smaller one that is still
equivalent.

$$
  \gamma_1(L)
  \left\{
    \omega \in MC_1(L) | \omega_1 is constant
  \right\}
$$

To get this impose a gauge condition known from homological perturbation theory.

A _context_ is

$$
  L \stackrel{\overset{f}{\to}}{\underset{g}{\leftarrow}} M
$$

$$
  g \circ f = Id_L
$$

$$
  f \circ g = Id - (d_M h + h d_M)
$$

$$
  g \circ h = 0, \; h \circ f = 0, \; h \circ h = 0
$$

$$
  MC(L) \simeq \{\omega \in MC(M) | h \omega = 0\}
$$

See Kuranishi's article in Annals to see where the motivation for all this comes from.

+-- {: .query}

[[Jim Stasheff]]: citation please and how much does **all** refer to??

=--



**Example** Consider the space of Schouten Lie algebras

$$
  L^k = \Gamma(X, \wedge^{k+1} T X)
$$

Then $MC_(L)$ is the set of [[Poisson manifold|Poisson brackets]] $\mathcal{O}(\hbar)$.

For let $P \in MC(L)$. Then $\pi_1(MC_\bullet(L), P)$ is the 
locally Hamiltonian diffeomorphisms / Hamiltonian diffeos.

$\pi_2(MC_\bullet(L), P)$ is the set of Casimir operators of $P$.

for $k \gt 2$ $\pi_k(MC_\bullet(L), P)$.

## Descent for $L_\infty$-algebra valued sheaves {#Descent}

Associated to an [[L-infinity algebra]] $L$ is a [[Kan complex]] whose set of $k$-cells is the set of [[Maurer-Cartan element]]s on the $n$-[[simplex]]

$$
  MC_k(L) = MC( L \otimes \Omega^\bullet(\Delta^k) )
  \,.
$$

Now assume that we have a [[sheaf L-∞ algebras]] over a [[topological space]] $X$. Let $\{U_\alpha \to X\}$ be an [[open cover]] of $X$.

On $k$-fold intersections we form 

$$
  L^k = \oplus_{\alpha_0,\cdots, \alpha_k}
  L(U_{\alpha_0, \cdots, \alpha_k})
  \,.
$$

The problem of [[descent]] is to glue all this to a single $L_\infty$ algebra given by the [[totalization]]  [[end]]

$$
  Tot(L^\bullet) = \int_k L^k \otimes \Omega^\bullet(\Delta^k)
$$

and check if that is equivalent to the one assigned to $X$.

We now want to compare the $\infty$-stack of $L_\infty$-algebras and that of the "integration" to the Kan complexes of Maurer-Cartan elements, so compare

$$
  MC_\bullet(Tot(L^\bullet))
$$

with 

$$
  Tot(MC_\bullet(L^\bullet))
$$

Notice that we have an evident map

$$
  MC(\int_l L^l \otimes \Omega^\bullet(\Delta^l) \otimes \Omega^\bullet(\Delta^k) )
  \to
  MC(\int_l L^l \otimes \Omega^\bullet(\Delta^l \times \Delta^k))
$$

Hinich shows in a special case that this is a [[homotopy equivalence]].

It is easy to prove it for abelian $L_\infty$-algebras.

**Theorem** (Getzler) 

This is indeed a homotopy equivalence.

**Proof** By E.G.'s own  account he has "a terrible proof" but thinks a nicer one using induction should be possible.


### Gauge fixing

Recall the notion of "context" from above, which is a collection of maps

$$
  L \stackrel{\overset{f}{\to}}{\underset{g}{\leftarrow}}
  M
  \stackrel{h}{\to} M
$$

between filtered complex-like things,


+-- {: .query}

meaning?? more general or complex with additional structure??

=--

satisfying some conditions.

We can arrange this such that $h$ imposes a certain gauge condition on $L$, or something

> I missed some details here...

**Theorem**

With

$$
  MC(M,h) := 
  \left\{
    \omega \in MC(M) | 
    h \omega = 0
  \right\}
$$

we have

$$
  g : MC(M,h) \stackrel{\simeq}{\to} MC(L)
$$

$$
  MC_\bullet(M,h) \stackrel{g \simeq}{\to} MC_\bullet(L)
  \stackrel{MC_\bullet(f) \simeq}{\to}
  MC_\bullet(M)
$$

**Proof** Along the lines of Kuranishi's construction:

$$
 h
  \left(
    [-]_0 + d_M \omega + \sum_{k = 1}^\infty
    \frac{1}{k!} [\omega, \cdots , \omega]^h 
  \right)
  = 0
  \,.
$$

So the big $\infty$-groupoid that drops out of the integration procedure is equivalent to the smaller one which is obtained from it by applying that gauge fixing condition.

It would be nice if in the definition of the MC complex we could replace differential forms on the $n$-simplex with just [[cochain on a simplicial set|simplicial cochains]] on $\Delta[n]$.

$$
  MC(L \otimes C^\bullet(\Delta^\bullet))
  \,.
$$

This would make the construction even smaller.


+-- {: .query}


What's the problem?


=--


If $L$ is abelian, then this is the [[Eilenberg-MacLane space]] which features in the [[Dold-Kan correspondence]].

This is true if one takes care of some things. This is part of the above "terrible proof".

Because one can prove that using explicit Eilenberg-MacLane's homotopies that proove the [[Eilenberg-Zilber theorem]] in terms of [[cochain on a simplicial set|simplicial cochains]] we have an equivalence

$$
  MC(
    L \otimes C^\bullet(\Delta[k] \otimes \Delta[l])
  )
  \to
  MC( L \otimes C^\bullet(\Delta[k] \times \Delta[l]))
$$


## References

The discussion of the Deligne groupoid (the $\infty$-groupoid "integrating" an $L_\infty$-algebra) and the gauge condition on the Maurer-Cartan elements is 

* [[Ezra Getzler]], _Lie theory for nilpotent L-infinity algebras_ ([arXiv:0404003](http://arxiv.org/abs/math/0404003))

> A reference for the theorem above seems not to be available yet, but I'll check.

[[!redirects descent for L-∞ algebras]]
