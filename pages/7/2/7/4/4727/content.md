
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--



* [[groupoid of Lie-algebra valued forms]]

* [[2-groupoid of Lie 2-algebra valued forms]]

* [[3-groupoid of Lie 3-algebra valued forms]]

* **$\infty$-groupoid of ∞-Lie-algebra valued forms**

***

#Contents#
* table of contents
{:toc}

## Idea

For $\mathfrak{g}$ an [[∞-Lie algebra]] (or more generally [[∞-Lie algebroid]]), the **$\infty$-groupoid of $\mathfrak{g}$-valued forms** is the [[∞-groupoid]] whose 

* [[object]]s are [[differential forms]] with values in $\mathfrak{g}$;

* [[morphism]]s are [[gauge transformation]]s between these;

* [[k-morphisms]] are order $k$ higher gauge transformations.

This naturally refines to a non-[[concrete sheaf|concrete]] [[∞-Lie groupoid]] whose $U$-parameterized smooth families of objects are [[∞-Lie algebroid]]-valued [[differential form]]s on $Z$.

A [[cocycle]] with coefficients in this is a [[connection on an ∞-bundle]].

For an introduction see the section <a href="http://ncatlab.org/nlab/show/infinity-Chern-Weil+theory+introduction#LieConnections">∞-Lie algebra valued forms</a> at [[∞-Chern-Weil theory introduction]].

## Definition

For $X$ a [[smooth manifold]] and $\mathfrak{g}$ an [[∞-Lie algebra]] or more generally an [[∞-Lie algebroid]], a  **$\infty$-Lie algebroid valued differential form** on $X$ is a morphism of [[dg-algebra]]s

$$
  \Omega^\bullet(X)
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

from the [[Weil algebra]] of $\mathfrak{g}$ to the [[de Rham complex]] of $X$. Dually this is a morphism of [[∞-Lie algebroid]]s

$$
  A : T X \to inn(\mathfrak{g})
$$

from the [[tangent Lie algebroid]] to the [[Weil algebra|inner automorphism ∞-Lie algebra]].

Its [[curvature]] is the composite of morphisms of [[graded vector space]]s

$$
  \Omega^\bullet(X) \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{F_{(-)}}{\leftarrow}
  \wedge^1 \mathfrak{g}^*
  : 
  F_{A}
  \,.
$$

Precisely if the curvatures vanish does the morphism factor through the [[Chevalley-Eilenberg algebra]] $W(\mathfrak{g}) \to CE(\mathfrak{g})$.

$$
  (F_A = 0) 
  \;\;\Leftrightarrow
  \;\;
  \left(
  \array{
     && CE(\mathfrak{g})
     \\
     & {}^{\mathllap{\exists A_{flat}}}\swarrow & \uparrow
     \\
     \Omega^\bullet(X) &\stackrel{A}{\leftarrow}& W(\mathfrak{g})     
  }
  \right)
$$

in which case we call $A$ **flat**.

The [[curvature characteristic form]]s of $A$ are the composite

$$
  \Omega^\bullet(X)
  \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{\langle F_{(-)} \rangle}{\leftarrow}
  inv(\mathfrak{g})
  :
  \langle F_A\rangle
  \,,
$$

where $inv(\mathfrak{g}) \to W(\mathfrak{g})$ is the inclusion of the [[invariant polynomial]]s. 


+-- {: .un_defn}
###### Definition

For $U$ a [[smooth manifold]], the **$\infty$-groupoid of $\mathfrak{g}$-valued forms is the [[Kan complex]]

$$
  \exp(\mathfrak{g})_{conn}(U)
  :
  [k]
  \mapsto
  \left\{
     \Omega^\bullet(U \times \Delta^k)
      \stackrel{A}{\leftarrow}
     W(\mathfrak{g})
     \;\;
     |
     \;\;
       \forall v \in \Gamma(T \Delta^k) : \iota_v F_A = 0
  \right\}
$$


whose [[k-morphism]]s are $\mathfrak{g}$-valued forms $A$ on $U \times \Delta^k$ with sitting instants, and with the property that their [[curvature]] vanishes on vertical vectors.

The canonical morphism

$$
  \exp(\mathfrak{g})_{conn} \to \exp(\mathfrak{g})
$$

to the untruncated [[Lie integration]] of $\mathfrak{g}$ is given by restriction of $A$ to [[vertical differential form]]s (see below).

=--

+-- {: .un_remark}
###### Remark

Here we are thinking of $U \times \Delta^k \to U$ as a trivial [[bundle]].

The _first_ [[Ehresmann connection|Ehresmann condition]] will be identified with the conditions on lifts $\nabla$ in [[∞-anafunctor]]s

$$
  \array{
    && \exp(\mathfrak{g})_{conn}
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    C(U) &\stackrel{g}{\to}& \exp(\mathfrak{g})
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

that define [[connections on ∞-bundles]]. More on this in the [Properties](#Properties)-section below.

=--

## Properties {#Properties}

### Curvature characteristics

+-- {: .un_prop}
###### Proposition

For $A \in \exp(\mathfrak{g})_{conn}(U,[k])$ a $\mathfrak{g}$-valued form on $U \times \Delta^k$ and for $\langle - \rangle \in W(\mathfrak{g})$ any [[invariant polynomial]], the corresponding [[curvature characteristic form]] $\langle F_A \rangle \in \Omega^\bullet(U \times \Delta^k)$ descends down to $U$.

=--

+-- {: .proof}
###### Proof

It is sufficient to show that for all $v \in \Gamma(T \Delta^k)$ we have

1. $\iota_v \langle F_A \rangle = 0$;

1. $\mathcal{L}_v \langle F_A \rangle = 0$.

The first condition is evidently satisfied if already $\iota_v F_A = 0$. The second condition follows with [[Cartan calculus]] and using that $d_{dR} \langle F_A\rangle = 0$:

$$
  \mathcal{L}_v \langle F_A \rangle = 
  d \iota_v \langle F_A \rangle
  + 
  \iota_v d \langle F_A \rangle
  = 0
  \,.
$$

=--

+-- {: .un_lemma}
###### Remark

For a general $\infty$-Lie algebra $\mathfrak{g}$ the curvature forms $F_A$ themselves are not closed, hence requiring them to have no component along the simplex does not imply that they descend. This is different for abelian $\infty$-Lie algebras: for them the curvature forms themselves are already closed, and hence are themselves already curvature characteristics that do descent.

=--


It is useful to organize the $\mathfrak{g}$-valued form $A$, together with its restriction $A_{vert}$ to [[vertical differential form]]s and with its [[curvature characteristic form]]s in the [[commuting diagram]]

$$
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
      &&&
      gauge\;transformation
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{g})
      &&&
      \mathfrak{g}-valued\;form
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
      &&&
      curvature\;characteristic\;forms
    }
$$

in [[dgAlg]].

The commutativity of this diagram is implied by $\iota_v F_A = 0$.

+-- {: .un_defn}
###### Definition

Write $\exp(\mathfrak{g})_{CW}(U)$ for the $\infty$-groupoid of $\mathfrak{g}$-valued forms fitting into such diagrams.


$$
  \exp(\mathfrak{g})_{CW}(U)
  :
  [k]
  \mapsto
  \left\{
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
    }
  \right\}
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

If we just consider the top horizontal morphism in this diagram we obtain the object

$$
  \exp(\mathfrak{g})(U)
  :
  [k]
  \mapsto
  \left\{
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
     }
  \right\}
$$

discussed in detail at [[Lie integration]]. If we consider the top square of the diagram we obtain the object

$$
  \exp(\mathfrak{g})_{diff}(U)
  :
  [k]
  \mapsto
  \left\{
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{g})
   }
  \right\}
  \,.
$$

This forms a [[resolution]] of $\exp(\mathfrak{g})$ and may be thought of as the $\infty$-groupoid of [[pseudo-connection]]s.


We have an evident sequence of morphisms

$$
  \array{
    \exp(\mathfrak{g})_{conn} &&& genuine\;connections
    \\
    \downarrow
    \\
    \exp(\mathfrak{g})_{CW} &&& pseudo-connection\;with\;global\;curvature\;characteristics 
    \\
    \downarrow
    \\
    \exp(\mathfrak{g})_{diff} &&& pseudo-connections
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \exp(\mathfrak{g}) &&& bare bundles
  }
  \,,
$$

where we label the objects by the structures they classify, as discussed at [[∞-Chern-Weil theory]].


Here the botton morphism is a weak equivalence and the others are [[monomorphism]]s. 

Notice that in full [[∞-Chern-Weil theory]] the fundamental object of interest is really $\exp(\mathfrak{g})_{diff}$ -- the object of [[pseudo-connection]]s. The other objects only serve the purpose of picking particularly nice representatives: 

the object $\exp(\mathfrak{g})_{CW}$ may contain pseudo-connections, those for which at least the associated [[circle n-bundles with connection]] given by the $\infty$-Chern Weil homomorphism are genuine connections.

This distinction is important: over objects $X \in $ [[?LieGrpd]] that are not [[smooth manifold]]s but for instance [[orbifold]]s, the genuine connections for higher Lie algebras do _not_ exhaust all nonabelian differential cocycles. This just means that not every differential class in this case does have a nice representative in the usual sense.

=--



### 1-Morphisms: integration of infinitesimal gauge transformations {#InfGaugeTrafo}

The 1-[[morphism]]s in $\exp(\mathfrak{g})(U)$ may be thought of as [[gauge transformation]]s between $\mathfrak{g}$-valued forms. We unwind what these look like concretely.


+-- {: .un_defn}
###### Definition

Given a 1-morphism in $\exp(\mathfrak{g})(X)$, represented by $\mathfrak{g}$-valued forms

$$
  \Omega^\bullet(U \times \Delta^1) 
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

consider the unique decomposition

$$
  A = A_U + ( A_{vert} := \lambda \wedge d t)  \; \; 
  \,,
$$

with $A_U$ the horizonal differential form component and $t : \Delta^1 = [0,1] \to \mathbb{R}$ the canonical coordinate.

We call $\lambda$ the **gauge parameter** . This is a function on $\Delta^1$ with values in 0-forms on $U$ for $\mathfrak{g}$ an ordinary [[Lie algebra]], plus 1-forms on $U$ for $\mathfrak{g}$ a [[Lie 2-algebra]], plus 2-forms for a Lie 3-algebra, and so forth.

=--

We describe now how this enccodes a gauge transformation

$$
  A_0(s=1) \stackrel{\lambda}{\to} A_U(s = 1)
  \,.
$$

+-- {: .un_lemma}
###### Observation


By the nature of the [[Weil algebra]] we have

$$
  \frac{d}{d s} A_U
  =
  d_U \lambda + [\lambda \wedge A] + [\lambda \wedge A \wedge A] + \cdots
  + 
  \iota_s F_A
  \,,
$$

where the sum is over all higher brackets of the [[∞-Lie algebra]] $\mathfrak{g}$.

=--

In [[Cartan calculus]] for $\mathfrak{g}$ an ordinary one writes the corresponding  **[[Ehresmann connection|second Ehremsnn condition]]** $\iota_{\partial_s} F_A = 0$ equivalently

$$
  \mathcal{L}_{\partial_s} A = ad_\lambda A
  \,.
$$


+-- {: .un_def}
###### Definition

Define the **[[covariant derivative]] of the gauge parameter** to be

$$
  \nabla \lambda := d \lambda + [A \wedge \lambda] + [A \wedge A \wedge \lambda] + \cdots
  \,.
$$

=--

In this notation we have

* the general identity 

  \[
    \frac{d}{d s} A_U = \nabla \lambda + (F_A)_s
    \label{ShiftedGaugeTrafo}
  \]

* the **horizontality** or **[[rheonomy]]** constraint or **[[Ehresmann connection|second Ehresmann condition]]** $\iota_{\partial_s} F_A = 0$, the [[differential equation]]

  \[
    \frac{d}{d s} A_U = \nabla \lambda
    \label{GaugeTrafo}
    \,.
  \]

This is known as the equation for **infinitesimal [[gauge transformation]]s** of an $\infty$-Lie algebra valued form. 



+-- {: .un_lemma}
###### Observation

By [[Lie integration]] we have that $A_{vert}$ -- and hence $\lambda$ -- defines an element $\exp(\lambda)$ in the [[∞-Lie group]] that integrates $\mathfrak{g}$. 

The unique solution $A_U(s = 1)$ of the above [[differential equation]] at $s = 1$ for the initial values $A_U(s = 0)$ we may think of as the result of acting on $A_U(0)$ with the gauge transformatin $\exp(\lambda)$. 

=--




## Examples

### Lie algebra valued 1-forms

+-- {: .un_prop}
###### Proposition
**(connections on ordinary bundles)**

For $\mathfrak{g}$ an ordinary [[Lie algebra]] with simply connected [[Lie group]] $G$ and for $\mathbf{B}G_{conn}$ the [[groupoid of Lie algebra-valued forms]] we have an [[isomorphism]]

$$
  \tau_1 \exp(\mathfrak{g})_{conn} = \mathbf{B}G_{conn}
$$

=--

+-- {: .proof}
###### Proof

To see this, first note that the sheaves of objects on both sides are manifestly isomorphic, both are the sheaf of $\Omega^1(-,\mathfrak{g})$. For morphisms, observe that for a form $\Omega^\bullet(U \times \Delta^1) \leftarow W(\mathfrak{g}) : A$ which we may decompose into a horizontal and a verical pice as $A = A_U + \lamnda \wedge d t$ the condition $\iota_{\partial_t} F_A = 0$ is equivalent to the [[differential equation]]

$$
  \frac{\partial}{\partial t} A
  =
  d_U \lambda + [\lambda, A]
  \,.
$$

For any initial value $A(0)$ this has the unique solution

$$
  A(t) = g(t)^{-1} (A + d_{U}) g(t)
  \,,
$$

where $g : [0,1] \to G$ is the [[parallel transport]] of $\lambda$:

$$
  \begin{aligned}
    &
    \frac{\partial}{\partial t}
    \left(
       g_(t)^{-1} (A + d_{U}) g(t)
     \right)
     \\
     = &
     g(t)^{-1} (A + d_{U}) \lambda g(t)
     -
     g(t)^{-1} \lambda (A + d_{U}) g(t)    
   \end{aligned}
$$

(where for ease of notaton we write actions as if $G$ were a [[matrix Lie group]]).

In particular this implies that the endpoints of the path of $\mathfrak{g}$-valued 1-forms are related by the usual cocycle condition in $\mathbf{B}G_{conn}$

$$
  A(1) = g(1)^{-1} (A + d_U) g(1)
  \,.
$$

In the same fashion one sees that given 2-cell in $\exp(\mathfrak{g})(U)$ and any 1-form on $U$ at one vertex, there is a unique lift to a 2-cell in $\exp(\mathfrak{g})_{conn}$, obtained by parallel transporting the form around. The claim then follows from the previous statement of [[Lie integration]] that $\tau_1 \exp(\mathfrak{g}) = \mathbf{B}G$.

=--

### Lie 2-algebra valued forms

* For $\mathfrak{g}$ [[Lie 2-algebra]], a $\mathfrak{g}$-valued differential form in the sense described here is precisely an [[Lie 2-algebra valued form]].

### Ordinary $n$-forms and the de Rham complex

For $n \in \mathbb{N}$, $n \geq 1$ we have that $b^{n-1}\mathbb{R}$-valued differential forms are in natural bijection to ordinary closed [[differential form]]s in degree $n$


+-- {: .un_lemma}
###### Observation

Notice that under addition of differential forms, $\exp(b^{n-1}\mathbb{R})_{conn}$ is over each $U \in CartSp$ an abelian [[simplicial group]].

Under the [[Dold-Kan correspondence]] $Ch_\bullet^+ \stackrel{\overset{N}{\leftarrow}}{\underset{\Xi}{\to}} sAb$ we may therefore identify $\exp(b^{n-1}\mathbb{R})_{conn}$ with a presheaf $N \exp(b^{n-1}\mathbb{R})_{conn}$ of chain complexes.

=--



+-- {: .un_prop}
###### Proposition

The degreewise [[fiber integration]] of differential forms over simplices
constitutes a morphism 

$$
  \int_{\Delta^\bullet} :
  N\exp(b^{n-1}\mathbb{R})_{conn}
  \to 
  \left(
    C^\infty(-, \mathbb{R})
    \stackrel{d_{dR}}{\to}
    \Omega^1(-)
    \stackrel{d_{dR}}{\to}
    \cdots
    \stackrel{d_{dR}}{\to}
    \Omega^n(-)
  \right)
  \,.
$$

that is a weak equivalence.


=--

+-- {: .proof}
###### Proof

First notice that we do have a chain homomorphism:

an element in $N \exp(b^{n-1} \mathbb{R})_{conn}$ in degree $k$ is an $n$-form $\omega \in \Omega^n(U \times \Delta^k)$. The differential acts on this as the alterating sum of the restriction to the $(k-1)$-faces

$$
  \partial \omega = \sum_{i = 0}^k (-1)^i \partial_i^* \omega
  \,.
$$

The integral over that is the integral over the boundary of the simplex (see [[simplex]] for details)

$$
  \int_{\Delta^{k-1}} \sum_{i = 0}^k (-1)^i \partial_i^* \omega
  =
  \int_{\partial \Delta^k} \omega
$$

and by [[Stokes theorem]] this is

$$
  \cdots = \int_{\Delta^k} d_{\Delta^k} \omega
  \,.
$$

Now we use the "second Ehresmann"-condition on $\omega$, making it a $k$-cell in $\exp(b^{n-1})_{conn}$: its curvature $d \omega = d_{\Delta^k} \omega + d_U \omega$ has no components along the simplex. Therefore this is equal to 

$$
  \cdots = - \int_{\Delta^k} d_U \omega
  \,.
$$

In this expression we can pass the $d_U$-operator by the fiber integral sign, only picking up a sign, to get

$$
  \cdots = d_U \int_{\Delta^k} \omega
  \,.
$$

So we do indeed have a chain map. 

Next we observe that over $U \in CartSp$ the chain homology of $N \exp(b^{n-1}\mathbb{R})$ in degree 0 is the group of $n$-forms modulo exact $n$-forms on $U$: the differential

$$
  \partial : N\exp(b^{n-1} \mathbb{R})(U)_1 \to N\exp(b^{n-1}\mathbb{R})(U)_0
$$

takes a path of $n$-forms $\omega = \omega_U + \lambda d t \in \Omega^\bullet(U \times \Delta^1)$ to the difference between the enpoints. 

$$
  \partial \omega = \omega_U(1) - \omega_U(0)
  \,.
$$

By the discussion of gauge transformations above, we have that due to the constraint that the curvature $d \omega$ is horizontal we have

$$
  \frac{d}{d t} \omega_U = d_U \lambda
  \,.
$$

For fixed $\omega_U(0)$ This is solved uniquely by 

$$
  \omega_U(1) = \omega_U(0) + d_U \int_{0}^1 \lambda d t
  \,.
$$

Therefore $\partial \omega = d_U \int_0^1 \lambda d t$. Clearly every exact form is obtained this way. 



=--

### Supergravity fields

What is called an  "extended soft group manifold" in the literature on the [[D'Auria-Fre formulation of supergravity]] is really precisely a collection of $\infty$-Lie algebroid valued forms with values in a super $\infty$-Lie algebra such as the [[supergravity Lie 3-algebra]] (for 11-dimensional [[supergravity]]). The way [[curvature]] and [[Bianchi identity]] are read off from "extded soft group manifolds" in this literature is -- apart from this difference in terminology -- precisely what is described above. 




## References

The (obvious but conceptually important) observation that [[Lie algebra-valued 1-forms]] regarded as morphisms of [[graded vector space]]s $\Omega^\bullet(X) \leftarrow \wedge^1 \mathfrak{g}^* : A$ are equivalently morphisms of dg-algebras out of the [[Weil algebra]] $\Omega^\bullet(X) \leftarrow W(\mathfrak{g}) : A$ and that one may think of as the identity $W(\mathfrak{g}) \leftarrow W(\mathfrak{g}) : Id$ as the _universal $\mathfrak{g}$-connection_ appears in early articles for instance highlighted on p. 15 of

* Franz W. Kamber; Philippe Tondeur, _Semisimplicial Weil algebras and characteristic classes for foliated bundles in &#268;ech cohomology_ , Differential geometry (Proc. Sympos. Pure Math., Vol. XXVII, Stanford Univ., Stanford, Calif., 1973), Part 1, pp. 283--294. Amer. Math. Soc., Providence, R.I., (1975). 

following [[Eli Cartan]]'s influential work (see [[Weil algebra]] for more references).

The (evident) generalization to Weil algebras of [[∞-Lie algebra]]s and [[∞-Lie algebroid]]s is considered explicitly in

* Hisham Sati, Urs Schreiber, Jim Staasheff, _$L_\infty$-algebra valued connections_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)

but -- somewhat implicitly -- this construction appears earlier, notably in the [[D'Auria-Fre formulation of supergravity]]. A collection of such precursors to these notions is collected at

* [[schreiber:differential cohomology in an (∞,1)-topos -- references]]: <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#InfLieAlgValuedForms">∞-Lie algebra valued forms</a>

The structure of the formula \eqref{GaugeTrafo} for infinitesimal gauge transformations of higher forms is widely known in the literature on [[supergravity]] and [[string theory]], if maybe not formalized in terms of $\infty$-Lie algebra theory as we do here. One exception is the remarkable book

*  [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fre]], _[[Supergravity and Superstrings - A Geometric Perspective]]_ .

In this old book no $\infty$-Lie algebras are mentioned explicitly, but the [[dg-algebra]] computations that are considered are easily seen to be precisely their [[Chevalley-Eilenberg algebra]]-incarnations. 

The authors use the term _extended [[soft group manifold]]_ for what here we identify as an $\infty$-Lie algebra valued form $T X \to inn(\mathfrak{g})$.

With this terminological translation understood, and observing that all their constructions straightforwardly generalize to more general dg-algebras than these authors conisder explicitly, we find that

* our equation \eqref{ShiftedGaugeTrafo} for the possibly shifted gauge transformation is their equation I.3.136;

* our equation \eqref{GaugeTrafo} for the genuine gauge transfomation is their equation for _horizontal_ or [[rheonomy|rheonomic]] gauge transformations III.3.23 .


In fact their full rheonomy constraint III.3.32 is essentialy the same horizontality constraint, but applied not just to the 1-simplex $\Delta^1$, but to the [[supermanifold|super simplex]] $\Delta^{1|p}$. 
 

[[!redirects infinity-Lie algebroid-valued differential form]]
[[!redirects infinity-Lie algebroid-valued differential forms]]
[[!redirects infinity-Lie algebroid valued differential form]]
[[!redirects infinity-Lie algebroid valued differential forms]]
[[!redirects ∞-Lie algebroid-valued differential form]]
[[!redirects ∞-Lie algebroid-valued differential forms]]
[[!redirects ∞-Lie algebroid valued differential form]]
[[!redirects ∞-Lie algebroid valued differential forms]]
[[!redirects infinity-Lie algebroid-valued form]]
[[!redirects infinity-Lie algebroid-valued forms]]
[[!redirects infinity-Lie algebroid valued form]]
[[!redirects infinity-Lie algebroid valued forms]]
[[!redirects ∞-Lie algebroid-valued form]]
[[!redirects ∞-Lie algebroid-valued forms]]
[[!redirects ∞-Lie algebroid valued form]]
[[!redirects ∞-Lie algebroid valued forms]]

[[!redirects infinity-groupoid of infinity-Lie algebroid-valued differential forms]]
[[!redirects infinity-groupoid of infinity-Lie algebroid valued differential forms]]
[[!redirects ∞-groupoid of ∞-Lie algebroid-valued differential forms]]
[[!redirects ∞-groupoid of ∞-Lie algebroid valued differential forms]]
[[!redirects infinity-groupoid of infinity-Lie algebroid-valued forms]]
[[!redirects infinity-groupoid of infinity-Lie algebroid valued forms]]
[[!redirects ∞-groupoid of ∞-Lie algebroid-valued forms]]
[[!redirects ∞-groupoid of ∞-Lie algebroid valued forms]]

[[!redirects infinity-Lie algebra-valued differential form]]
[[!redirects infinity-Lie algebra-valued differential forms]]
[[!redirects infinity-Lie algebra valued differential form]]
[[!redirects infinity-Lie algebra valued differential forms]]
[[!redirects ∞-Lie algebra-valued differential form]]
[[!redirects ∞-Lie algebra-valued differential forms]]
[[!redirects ∞-Lie algebra valued differential form]]
[[!redirects ∞-Lie algebra valued differential forms]]
[[!redirects infinity-Lie algebra-valued form]]
[[!redirects infinity-Lie algebra-valued forms]]
[[!redirects infinity-Lie algebra valued form]]
[[!redirects infinity-Lie algebra valued forms]]
[[!redirects ∞-Lie algebra-valued form]]
[[!redirects ∞-Lie algebra-valued forms]]
[[!redirects ∞-Lie algebra valued form]]
[[!redirects ∞-Lie algebra valued forms]]

[[!redirects infinity-groupoid of infinity-Lie algebra-valued differential forms]]
[[!redirects infinity-groupoid of infinity-Lie algebra valued differential forms]]
[[!redirects ∞-groupoid of ∞-Lie algebra-valued differential forms]]
[[!redirects ∞-groupoid of ∞-Lie algebra valued differential forms]]
[[!redirects infinity-groupoid of infinity-Lie algebra-valued forms]]
[[!redirects infinity-groupoid of infinity-Lie algebra valued forms]]
[[!redirects ∞-groupoid of ∞-Lie algebra-valued forms]]
[[!redirects ∞-groupoid of ∞-Lie algebra valued forms]]
[[!redirects ∞-groupoid of ∞-Lie-algebra valued forms]]
