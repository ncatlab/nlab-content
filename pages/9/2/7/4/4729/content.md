
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In every [[cohesive (∞,1)-topos]] there is an <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#ChernWeilTheory">intrinsic notion of ∞-Chern-Weil theory</a> that gives rise to a notion of _connection_ on [[principal ∞-bundle]]s. We describe here details of the realization of this general abstract structure in the cohesive $(\infty,1)$-topos [[Smooth∞Grpd]] of [[smooth ∞-groupoid]]s.

For $G$ an [[∞-Lie group]], a _connection_ on a smooth $G$-[[principal ∞-bundle]] is a structure that supports the [[Chern-Weil homomorphism in Smooth∞Grpd]]: it interpolates between the [[nonabelian cohomology]] class $c \in H^1_{smooth}(X,G)$ of the bundle and the refinements to [[ordinary differential cohomology]] of its [[characteristic class]]: the [[curvature characteristic form|curvature characteristic class]]es.

This generalizes the  notion of [[connection on a bundle]] and the ordinary [[Chern-Weil homomorphism]] in [[differential geometry]].

See the <a href="http://nlab.mathforge.org/nlab/show/Chern-Weil+theory+in+Smooth%E2%88%9EGrpd#Motivation">Motivation section</a> at [[Chern-Weil theory in Smooth∞Grpd]] and the page [[∞-Chern-Weil theory introduction]] for more background.

## Definition

We assume that the reader is familiar with the notation and constructions discussed at [[Smooth∞Grpd]].

We discuss connections on $G$-[[principal ∞-bundle]]s for $G \in $ [[Smooth∞Grpd]] an [[∞-Lie group|smooth ∞-group]] that arises from [[Lie integration]] of an [[L-∞ algebra]] $\mathfrak{g}$.

(...)

We have seen above for $\mathfrak{g}$ an $\infty$-Lie algebroid the object
$\exp(\mathfrak{g})_{diff}$ that classifies [[pseudo-connection]]s
on $\exp(\mathfrak{g})$-principal $\infty$-bundles and serves to support the $\infty$-Chern-Weil homomorphism. We now discuss the genuine $\infty$-connections among these pseudo-connections. From the point of view of the general abstract theory these are particularly nice representatives of more intrinsically defined structures. 

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
  \mathfrak{g}^*[1]
  : 
  F_{A}
  \,.
$$

Precisely if the curvatures vanish does the morphism factor through the [[Chevalley-Eilenberg algebra]] 

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

The _first_ [[Ehresmann connection|Ehresmann condition]] 
can be identified with the conditions on lifts $\nabla$ in [[∞-anafunctor]]s

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

that define [[connections on ∞-bundles]]. 

=--



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

For a general $\infty$-Lie algebra $\mathfrak{g}$ the curvature forms $F_A$ themselves are not necessarily closed (rather they satisfy the [[Bianchi identity]]), hence requiring them to have no component along the simplex does not imply that they descend. This is different for abelian $\infty$-Lie algebras: for them the curvature forms themselves are already closed, and hence are themselves already curvature characteristics that do descent.

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



## Examples


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
  A_0(s=0) \stackrel{\lambda}{\to} A_U(s = 1)
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

In the [[Cartan calculus]] for $\mathfrak{g}$ an ordinary 
[[Lie algebra]] one writes the corresponding  **[[Ehresmann connection|second Ehremsnn condition]]** $\iota_{\partial_s} F_A = 0$ equivalently

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

The unique solution $A_U(s = 1)$ of the above [[differential equation]] at $s = 1$ for the initial values $A_U(s = 0)$ we may think of as the result of acting on $A_U(0)$ with the gauge transformation $\exp(\lambda)$. 

=--



### Ordinary connections on principal 1-bundles


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

To see this, first note that the sheaves of objects on both sides are manifestly isomorphic, both are the sheaf of $\Omega^1(-,\mathfrak{g})$. For morphisms, observe that for a form $\Omega^\bullet(U \times \Delta^1) \leftarrow W(\mathfrak{g}) : A$ which we may decompose into a horizontal and a verical pice as $A = A_U + \lambda \wedge d t$ the condition $\iota_{\partial_t} F_A = 0$ is equivalent to the [[differential equation]]

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

### Further examples

* For $\mathfrak{g}$ [[Lie 2-algebra]], a $\mathfrak{g}$-valued differential form in the sense described here is precisely an [[Lie 2-algebra valued form]].


* For $n \in \mathbb{N}$, a $b^{n-1}\mathbb{R}$-valued differential form is the same as an ordinary differential $n$-form.


* What is called an  "extended soft group manifold" in the literature on the [[D'Auria-Fre formulation of supergravity]] is precisely a collection of $\infty$-Lie algebroid valued forms with values in a super $\infty$-Lie algebra such as the 
[[supergravity Lie 3-algebra]]/[[supergravity Lie 6-algebra]] (for 11-dimensional [[supergravity]]). The way [[curvature]] and [[Bianchi identity]] are read off from "extded soft group manifolds" in this literature is -- apart from this difference in terminology -- precisely what is described above. 



## Properties

### Existence of $\infty$-connections

+-- {: .un_prop #ExistenceOfInftyConnections}
###### Proposition
**(existence of $\infty$-connections)**

In $\mathbf{H} = $ [[nLab:?LieGrpd]] over a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] $X$, every $G$-[[nLab:principal ∞-bundle]] for $G = \tau_n \exp(\mathfrak{g})$ obtained from [[nLab:Lie integration]] admits a genuine $\infty$-connection.

=--

+-- {: .proof}
###### Proof

By the assumptions on $X$, there is a [[nLab:good open cover]] $\{U_i \to X\}$ and a [[nLab:partition of unity]] $(\rho_i \in C^\infty(U_i))$ subordinate to that cover. 

Let $C(\{U_i\})$ be the [[nLab:Cech nerve]] of the cover and let $g : C(\{U_i\}) \to cosk_{n+1} \exp(\mathfrak{g})$ be a cocycle for the given $G$-principal $\infty$-bundle on $X$. This is given by a collection of [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebra valued differential forms]]

$$
  ( C^\infty(U_{i_0, \cdots i_k})\otimes \Omega^\bullet(\Delta^k) 
  \leftarrow
  CE(\mathfrak{g}) : \lambda_{i_0, \cdots, i_n})
  \,.
$$

We need to extend these to a cocycle of differential forms

$$
  ( \Omega^\bullet(U_{i_0, \cdots i_k})\otimes \Omega^\bullet(\Delta^k) 
  \leftarrow
  W(\mathfrak{g}) : (\lambda_{i_0, \cdots, i_n},A_{i_0, \cdots, i_n})) 
$$

such that the curvature components have no leg along the simplices.  This constraint is hierarchy of systems of partial differential equations. consider first the $A_{i_0, \cdots, i_k}(\frac{\partial}{\partial u}, \{\frac{\partial}{\partial t_r}\})$ with exactly one leg along $U_{i_0, \cdots, i_k}$. For these the constraint is a system of differential equations of the schematic form


$$
  \frac{\partial}{\partial t_r} A
  =
  d_U \lambda(\frac{\partial}{\partial t_r})
  + 
  [\lambda(\frac{\partial}{\partial t_r}), A]
$$

By the [[nLab:Bianchi identity]] and the fact that the curvature with all components along the simplex vabishes, it follows that this is an integrable system of partial differential equations. Fixing the boundary condition that $A$ vanishes in the $0$-corner of $\Delta^k$, this has a unique solution. $\hat A_{i_0, \cdots, i_k}$.

Set then 

$$
  A_{i_1, \cdots, i_k} := \sum_{i_0} \rho_{i_0} \hat A_{i_0, \cdots, i_k}|_{\delta_0(\Delta^k)}
  \,.
$$


The system of differential forms obtained this way does satisfy the cocycle condition and the curvature component with one leg along $U$ and the other legs along the simplices vanish:

$$
  \frac{\partial}{\partial t_r} 
  A_{i_1, \cdots, i_k}
  =
  \frac{\partial}{\partial t_r} 
\sum_{i_0} \rho_{i_0}  \hat A_{i_0, \cdots, i_k}
  =
  \sum_{i_0} \rho_{i_0} d_U \lambda(\frac{\partial}{\partial t_r})
  + 
  [\lambda(\frac{\partial}{\partial t_r}), \sum_{i_0} \rho_{i_0} \hat A_{i_0, \cdots, i_k}]
  =
  d_U \lambda(\frac{\partial}{\partial t_r})
  + 
  [\lambda(\frac{\partial}{\partial t_r}), A_{i_1, \cdots, i_k}]
  \,.
$$

Next continue iteratively in the above fashion, by induction on the number of legs of the forms along $U$.

=--



## Related concepts

* [[connection on a bundle]]

* [[connection on a 2-bundle]] / [[connection on a gerbe]] / [[connection on a bundle gerbe]]

* [[connection on a 3-bundle]] / [[connection on a bundle 2-gerbe]]

* **connection on an ∞-bundle**



## References

The local differential form data of $\infty$-connections was introduced in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]],
  _$L_\infty$-algebra connections_ in Fauser (eds.) Recent Developments in QFT, Birkh&#228;user (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)
  {#SSSI}

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Twisted differential String- and Fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">web</a>).
{#SSSIII}

The global description was then introduced in 

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Cech cocycles for differential characteristic classes -- An $\infty$-Lie theoretic construction_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#FSS">web</a>)

An attempt at a comprehensive account is in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

in section 3.3.9.

[[!redirects ∞-connection on a principal ∞-bundle]]
[[!redirects ∞-connection on a principal ∞-bundle]]

[[!redirects connection on a principal ∞-bundle]]

[[!redirects connection on an ∞-bundle]]
[[!redirects connections on an ∞-bundle]]

[[!redirects connection on an infinity-bundle]]

[[!redirects connections on ∞-bundles]]
[[!redirects connections on infinity-bundles]]

[[!redirects connection on a smooth principal ∞-bundle]]
[[!redirects connections on smooth principal ∞-bundles]]
[[!redirects connection on a principal infinity-bundle]]
