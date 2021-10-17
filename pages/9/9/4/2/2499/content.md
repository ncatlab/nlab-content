

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The D'Auria-Fr&#233; formalism ([D'Auria-Fr&#233;-Regge 80](#DAuriaFre80), [D'Auria-Fr&#233; 80](#DAuriaFre), [Castellani-D'Auria-Fr&#233; 91](#CastellaniDAuriaFre)) is a natural "[[superspace]]" formulation of [[supergravity]] in general [[dimensions]], including [[type II supergravity]] and [[heterotic supergravity]] in dimension 10 as well as notably [[11-dimensional supergravity]].

This proceeds in generalization of how [[Einstein gravity]] in [[first order formulation of gravity]] is equivalently the [[Cartan geometry]] for the inclusion of the [[Lorentz group]] inside the [[Poincare group]]: a [[field (physics)|field]] configuration of the field of [[gravity]] is equivalently a [[Cartan connection]] for this [[subgroup]] inclusion. 

Accordingly, low dimensional [[supergravity]] without [[extended supersymmetry]] is equivalently the [[super-Cartan geometry]] of the inclusion of the [[spin group]] into the [[super Poincaré group]].

What D'Auria-Fr&#233; implicitly observe (not in this [[homotopy theory|homotopy theoretic]] language though, that was developed in [Sati-Schreiber-Stasheff 08](#SSS), [Fiorenza-Schreiber-Stasheff 10](#FiorenzaSchreiberStasheff10), [Fiorenza-Sati-Schreiber 13](#FSS)) is that for higher supergravity with [[extended supersymmetry]] such as [[11-dimensional supergravity]] with its [[M-theory super Lie algebra]] symmetry, the description of the fields is in the _[[higher differential geometry]]_ version of [[Cartan geometry]], namely _[[higher Cartan geometry]]_, where the [[super Poincare Lie algebra]] is replaced by one of its exceptional [[super L-infinity algebra|super Lie n-algebra]] extensions (those that also control the [[brane scan]]), such as notably the [[supergravity Lie 3-algebra]] and the [[supergravity Lie 6-algebra]]. This is the refinement of [[super-Cartan geometry]] to [[higher Cartan geometry]].

This [[higher Cartan geometry|higher]] [[super Cartan geometry]]-description of [[supergravity]] is what D'Auria-Fr&#233; called the _geometric approach to supergravity_ or _geometric supergravity_ (e.g. [D'Auria 20](#DAuria20)). 


[[!include local and global geometry - table]]


For more background on [[principal ∞-connections]] see also at _[[∞-Chern-Weil theory introduction]]_.

### History

Around 1981 D'Auria and Fr&#233; noticed, in [GeSuGra](#DAuriaFre), that the intricacies of various [[supergravity]] [[classical field theory|classical field theories]] have a strikingly powerful reformulation in terms of super [[semifree dga|semifree differential graded-commutative algebra]]s. 

They defined various such super dg-algebras $W(\mathfrak{g})$ and showed (paraphrasing somewhat) that

* the field content, [[field strength]]s, [[covariant derivative]]s and [[Bianchi identity|Bianchi identities]] are all neatly encoded in terms of dg-algebra homomorphism $\Omega^\bullet(X) \leftarrow W(\mathfrak{g}) : \phi$;

* the [[action functional]]s of supergravity theories on such $\phi$ may be constructed as images under $\phi$ of certain elements in $W(\mathfrak{g})$ subject to natural conditions.

Their algorithm was considerably more powerful than earlier more pedestrian methods for construction such action functionals. The textbook [CastellaniDAuriaFre](#CastellaniDAuriaFre) on [[supergravity]] and [[string theory]] from the perspective of this formalism gives a comprehensive description of this approach.


We observe here that the D'Auria-Fre-formalism is [[schreiber:∞-Chern-Simons theory]] for [[∞-Lie algebra-valued forms]] with values in super [[∞-Lie algebra]]s such as the [[supergravity Lie 3-algebra]] and the [[supergravity Lie 6-algebra]].

The pivotal concept that allows to pass between this interpretation and the original formulation is the concept of [[∞-Lie algebroid]] with its various incarnations:

+-- {: .num_remark}
###### Remark
**(Incarnations of $\infty$-Lie algebroids)**

A (super) [[∞-Lie algebroid]] 

* is an [[infinitesimal space|infinitesimal]] (super)[[∞-Lie groupoid]]

* that may be modeled as a [[simplicial object|simplicial]] (super) [[infinitesimal space]]

* whose [[function algebras on ∞-stacks|function algebra]] is a [[cosimplicial algebra|cosimplicial]] ([[super algebra|super]]) algebra

* that under the [[monoidal Dold-Kan correspondence]] maps to a (super) [[semifree dga|semifree differential graded-commutative algebra]]: the [[Chevalley-Eilenberg algebra]] of the (super) [[∞-Lie algebroid]].

=--


Notably the [[semifree dga]] upon which D'Auria-Fr&#233; base their description is the [[Chevalley-Eilenberg algebra]] of the [[supergravity Lie 3-algebra]], which is an [[∞-Lie algebra]] that is a [[∞-Lie algebra cohomology|higher central extension]]

$$
  0 \to b^2 \mathfrak{u}(1)
  \to \mathfrak{sugra}(10,1)
  \to
  \mathfrak{siso}(10,1)
  \to
  0
$$

of a [[super Poincare Lie algebra]] $\mathfrak{siso}(10,1)$ in the way the [[String Lie 2-algebra]] $\mathfrak{string}(n)$ is a higher central extension of the [[special orthogonal Lie algebra]] $\mathfrak{so}(n)$.

A super [[connection on an ∞-bundle]] with values in $\mathfrak{sugra}(10,1)$ on a [[supermanifold]] $X$ is locally given by [[∞-Lie algebroid valued differential forms]] consisting of

* a $\mathbb{R}^{11}$-valued 1-form $e$ -- the [[vielbein]]

* a $\mathfrak{so}(10,1)$-valued 1-form $\omega$ -- the [[spin connection]]

* a spin-representation valued 1-form $\psi$ -- the spinor

* a 3-form $C$ .

These are identified with the fields of 11-dimensional [[supergravity]], respectively:

* the _[[graviton]]_ $(e, \omega)$

* the _[[gravitino]]_ $\psi$

* the _[[supergravity C-field]]_ $C$ .


By realizing this data as components of a Lie 3-algebra valued connection (more or less explicitly), the D'Auria-Fr&#233;-formalism achieves some conceptual simplication of 

* the construction of supersymmetric [[supergravity]] [[action functional]]s;

* the determination of the corresponding classical equations of motion.


### Higher gauge theory reinterpretation 

Originally D'Auria and Fr&#233; referred to commutative [[semifree dga]]s as _Cartan integrable systems_. Later the term _free differential algebra_, abbreviated _FDA_ was used instead and became popular. Nowadays much of the literature that studies commutative [[semifree dga]]s in [[supergravity]] refers to them as "FDA"s. One speaks of the _FDA approach to supergravity_ . 

But strictly speaking "free differential algebra" is a misnomer: genuinely free differential algebras are pretty boring objects. Crucially it is _only_ the underlying graded commutative algebra which is required to be free as a graded commutative algebra in that it is a [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g}^*$ on a [[graded vector space]] $\mathfrak{g}^*$. The differential on that is in general not free, hence the more precise term _[[semifree dga]]_ . 

In fact, when $\mathfrak{g}$ is concentrated in non-positive degree (so that $\wedge^\bullet \mathfrak{g}^*$ is concentrated in non-negative degree) the differential on $\wedge^\bullet \mathfrak{g}^{*}$ encodes all the structure of an [[∞-Lie algebroid]] on $\mathfrak{g}$. If $\mathfrak{g}$ is concentrated in negative degree the differential encodes the structure of an [[∞-Lie algebra]] on $\mathfrak{g}$. This interpretation of [[semifree dga]]s in [[Lie theory]] is the key to our _general abstract reformulation_ of the D'Auria-Fr&#233;-formalism.

Already D'Auria and Fr&#233; themselves, and afterwards other authors, have tried to better understand the intrinsic conceptual meaning of their [[dg-algebra]] formalism that happened to be so useful in [[supergravity]]: 

The idea arose and then became popular in the "FDA"-literature that the D'Auria-Fr&#233;-formalism should be about a concept called **[[soft group manifold]]s**. This is motivated by the observation that by means of the [[dg-algebra]] formulation the fields in [[supergravity]] arrange themselves into systems of [[differential form]]s that satisfy equations structurally similar to the [[Maurer-Cartan form]]s of left-invariant differential forms on a [[Lie group]] -- _except_ that where the ordinary Maurer-Cartan form has vanishing [[curvature]] (= [[field strength]]) these equations for supergravity fields have a possibly non-vanishing [[field strength]]. It is proposed in the "FDA"-literature that these generalized Maurer-Cartan equations describe generalized or "softened" group manifolds.

However, even when the field strengths _do_ vanish, the remaining collection of differential forms does not constrain the base manifold to be a group. Rather, if the field strengths vanish we have a natural interpretation of the remaining differential form data as being flat [[∞-Lie algebroid valued differential forms]], given by a morphism

$$
  A : T X \to \mathfrak{g}
$$

from the [[tangent Lie algebroid]] of the base [[manifold]] $X$ to the [[∞-Lie algebra]] $\mathfrak{g}$ encoded by the [[semifree dga]] in question. In fact, applying the functor from [[∞-Lie algebroid]]s to [[dg-algebra]]s given by forming [[Chevalley-Eilenberg algebra]]s, the above morphism turns into a [[dg-algebra]] morphism

$$
  \Omega^\bullet(X)
  \leftarrow
  CE(\mathfrak{g})
  :
  A
$$

to the [[deRham dg-algebra]] of $X$ (which we denote by the same letter, $A$, in a convenient abuse of notation).

Since $CE(\mathfrak{g})$ is semifree, this is a map of [[graded vector space]]s 

$$
  \Omega^\bullet(X)
  \leftarrow
  \mathfrak{g}^*
  :
  A
$$

together with a constraint that the morphism respects the differentials on $CE(\mathfrak{g})$ and on $\Omega^\bullet(X)$. Such a morphism of graded vector spaces in canonically identified with a $\mathfrak{g}$-valued differential form (recall that $\mathfrak{g}$ is a  [[graded vector space]])

$$ 
  \omega \in \Omega^\bullet(X,\mathfrak{g})
$$

and the aforementioned constraint is precisely the Maurer-Cartan-like equation that is known from left-invariant 1-forms on a [[Lie group]]. In fact, for $G$ a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ there is a canonical morphism

$$
  \Omega^\bullet(G)
  \leftarrow
  CE(\mathfrak{g})
$$

whose image is precisely the left-invariant 1-forms on the [[Lie group]] $G$ and whose respect for the differentials is precisely the ordinary Maurer-Cartan equation. 

To see the role of group manifolds for more general morphisms

$$
  \Omega^\bullet(X)
  \leftarrow
  CE(\mathfrak{g})
  :
  A
$$

one has to apply [[Lie integration]] of the [[∞-Lie algebroid]] morphism $T X \to \mathfrak{g}$ to a morphism of [[∞-Lie groupoid]]s

$$
  \Pi(X) \to \mathbf{B}G
$$
 
where $\Pi(X)$ is the [[path ∞-groupoid]] and where $\mathbf{B}G$ is the [[delooping]] of [[infinity-Lie groupoid|Lie in-group]] $G$ that integrates the [[Lie n-algebra]] $\mathfrak{g}$.
Such morphisms are the integrated version of flat [[∞-Lie algebroid valued differential forms]].

The [[∞-Chern-Weil theory]] of [[connections on ∞-bundles]] is about 


1. the generalization of such flat form data to [[∞-Lie algebroid valued differential forms]] with [[curvature]].

1. the generalization from globally defined differential form data -- which are connections on _trivial_ [[principal ∞-bundle]]s -- to connections on arbitrary [[principal ∞-bundle]]s.

The D'Auria-Fr&#233;-formalism -- after this re-interpretation -- is about the first of these points. So as an immediate gain of our reformulation of D'Auria-Fr&#233;-formalism in terms of [[connections on ∞-bundles]] we obtain, using the second of these points, a natural proposal for a formulation of [[supergravity]] field configurations that are possibly globally topologically nontrivial. Physicists speak of **instanton solutions**.

In fact, the [[∞-Lie theory]]-reformulation exhibits the D'Auria-Fr&#233;-formalism as being secretly the realization of [[supergravity]] as a higher [[gauge theory]].


It realizes supergravity as an example for a _nonabelian_ higher gauge theory in that a [[supergravity]] field configuration is not realizable as a cocycle in [[ordinary differential cohomology]] as in ordinary abelian higher [[gauge theory]] (see there) but as a nonabelian [[connection on an ∞-bundle]].


## Kinematics

### The supergravity Lie $n$-algebras 

We have a sequence of [[∞-Lie algebra cohomology|∞-Lie algebra extensions]]

[[supergravity Lie 6-algebra]] $\to$ [[supergravity Lie 3-algebra]] $\to$ [[super Poincare Lie algebra]]

$$
  \mathfrak{sugra}_6 \to \mathfrak{sugra}_3 \to \mathfrak{siso}(10,1)
  \,.
$$

...

### Super Lorentzian spacetime manifolds 

The base space $X$ on which a [[supergravity]] field is a super Lie $n$-algebra valued [[connection on an ∞-bundle]] is a [[supermanifold]].

In particular, for constructing the [[action functional]] of [[supergravity]] we want $X$ to locally look like [[super Minkowski space]].


### Field configuration and field strength 


A local field configuration on a [[supermanifold]] $X$ in the [[classical field theory]] is a morphism
 
$$
  T X \stackrel{(A, F_A)}{\to}
  inn(\mathfrak{sugra}(\mathfrak{g}))
$$

from the [[tangent Lie algebroid]] to the inner-derivation Lie 4-algebra $inn(\mathfrak{sugra}(10,1))$, defined as the formal dual of the [[Weil algebra]] of $\mathfrak{sugra}$). So dually this is a morhism of [[dg-algebra]]s from the [[Weil algebra]] $W(\mathfrak{sugra}(10,1))$ to the [[deRham dg-algebra]] $\Omega^\bullet(X)$ of $X$:

$$
  \Omega^\bullet(X)
   \leftarrow
   W(\mathfrak{sugra}(10,1))
   :
   (A,F_A)  
   \,.
$$

This is [[∞-Lie algebroid valued differential form]] data with [[curvature|∞-Lie algebroid valued curvature]] that is explicitly given by:



* connection forms / field configuration

  * $E \in \Omega^1(X,\mathbb{R}^{10,1})$ -- the **[[vielbein]]** (part of the _[[graviton]] [[field (physics)|field]]_)

  * $\Omega \in \Omega^1(X, \mathfrak{so}(10,1))$ -- the **[[spin connection]]** (part of the _[[graviton]] [[field (physics)|field]]_)

  * $\Psi \in \Omega^ 1(X,S)$ -- the **[[spinor]]** (the [[gravitino]] [[field (physics)|field]])

  * $C \in \Omega^3(X)$ -- a [[differential 3-form]] (the [[supergravity C-field]])

* [[curvature]] forms / [[field strength]]s

  * $T = d E + \Omega \cdot E + \Gamma(\bar \Psi \wedge \Psi) \in \Omega^2(X,\mathbb{R}^{10,1})$ - the **[[torsion of a metric connection|torsion]]**

  * $R = d \Omega + [\Omega \wedge \Omega] \in \Omega^2(X, \mathfrak{so}(10,1))$ - the **[[Riemann curvature]]**

  * $\rho = d \Psi + (\Omega \wedge \Psi) \in \Omega^2(X, S)$ -- the **[[covariant derivative]] of the [[spinor]]**

  * $G = d C + \mu_4(\psi, E) \in \Omega^4(X)$ -- the **4-form field strength**


### Gauge transformations {#GaugeTransformations}


A [[gauge transformation]] of a field configuration

$$
  \phi : T X \to inn(\mathfrak{g})
$$

is a diagram

$$
    \array{
      \Omega^\bullet(X \times \Delta^{1})_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{a})
      &&&
      gauge\;transformation
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(X \times \Delta^{1})
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{a})
      &&&
      field
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(X)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
      &&&
      gauge\;invariant\;observable
    }
$$

+-- {: .num_defn}
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
  A = A_U + ( A_{vert} \coloneqq \lambda \wedge d t)  \; \; 
  \,,
$$

with $A_U$ the horizontal differential form component and $t : \Delta^1 = [0,1] \to \mathbb{R}$ the canonical coordinate.

We call $\lambda$ the **gauge parameter** . This is a function on $\Delta^1$ with values in 0-forms on $U$ for $\mathfrak{g}$ an ordinary [[Lie algebra]], plus 1-forms on $U$ for $\mathfrak{g}$ a [[Lie 2-algebra]], plus 2-forms for a Lie 3-algebra, and so forth.

=--

We describe now how this enccodes a gauge transformation

$$
  A_0(s=1) \stackrel{\lambda}{\to} A_U(s = 1)
  \,.
$$

+-- {: .num_prop}
###### Proposition

The condition that all [[curvature characteristic form]]s descend to $U$ in that $A$ completes to a diagram

$$
  \array{
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{a})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
  }
$$

is solved by requiring all components 

$$
  \Omega^\bullet(U \times \Delta^1)
  \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{r^a}{\leftarrow}
  \wedge^1 \mathfrak{g}^*
  F_A^a
$$

of the [[curvature]] forms to vanish when evaluated on the [[vector field]] $\partial_s$ along $\partial_s$.

By the nature of the [[Weil algebra]] we have

$$
  \frac{d}{d s} A_U
  =
  d_U \lambda + [\lambda \wedge A] + [\lambda \wedge A \wedge A] + \cdots
  + 
  (F_A)(\partial_s, \cdots)
  \,,
$$

so that this condition is a system of ordinary [[differential equation]]s of the form

$$
  \frac{d}{d s} A_U
  =
  d_U \lambda + [\lambda \wedge A] + [\lambda \wedge A \wedge A] + \cdots
  \,,
$$

where the sum is over all higher brackets of the [[∞-Lie algebra]] $\mathfrak{g}$.

=--

+-- {: .num_defn}
###### Definition

Define the **[[covariant derivative]] of the gauge parameter** to be

$$
  \nabla \lambda \coloneqq d \lambda + [A \wedge \lambda] + [A \wedge A \wedge \lambda] + \cdots
  \,.
$$

=--

In this notation we have

* the general identity 

  \[
    \frac{d}{d s} A_U = \nabla \lambda + (F_A)_s
    \label{ShiftedGaugeTrafo}
  \]

* the **horizontality**  constraint or **[[Ehresmann connection|second Ehresmann condition]]**

  \[
    \frac{d}{d s} A_U = \nabla \lambda
    \label{GaugeTrafo}
    \,.
  \]

This is known as the equation for **infinitesimal [[gauge transformation]]s** of an $\infty$-Lie algebra valued form. 

+-- {: .num_prop}
###### Proposition

By [[Lie integration]] we have that $A_{vert}$ -- and hence $\lambda$ -- defines an element $\exp(\lambda)$ in the [[∞-Lie group]] that integrates $\mathfrak{g}$. 

The unique solution $A_U(s = 1)$ of the above differential equation at $s = 1$ for the initial values $A_U(s = 0)$ we may think of as the result of acting on $A_U(0)$ with the gauge transformation $\exp(\lambda)$. 

=--

### Rheonomy 
 {#Rheonomy}

#### Idea

In the formulation here the [[field (physics)|fields]] of [[supergravity]] are modeled by [[super differential forms]] on a [[supermanifold]] $\tilde X$, and this very fact serves to make local [[supersymmetry]] manifest, i.e., serves to model geometry by [[higher supergeometry|higher supergeometric]] [[higher Cartan geometry]].

But the actual fields of supergravity are supposed to be fields on actual [[spacetime]] $X$ (an ordinary [[smooth manifold]]) $X \hookrightarrow \tilde X$.
Hence one is to impose a constraint that ensures that the [[super differential forms]] used on $\tilde X$ are uniquely determined by their restriction to ordinary [[differential forms]] on $X$. This constraint is called _rheonomy_ ([Castellani-D'Auria-Fr&#233; 91, vol 2, section III.3.3](#CastellaniDAuriaFre)), alluding to the idea that the constraints allow the field data to "flow" from spacetime $X$ to the [[super spacetime]] $\tilde X$.

The idea here is [[analogy|analogous]] ([Castellani-D'Auria-Fr&#233; 91, vol 2, p. 660](#CastellaniDAuriaFre), [Fr&#233;-Grassi 08, p. 4](#FreGrassi08)) to how the [[Cauchy-Riemann equations]] impose the constraint for a [[function]] on the [[complex plane]] $\mathbb{C}$ to be a [[holomorphic function]] and hence to be already fixed by its values on the [[real line]] $\mathbb{R} \hookrightarrow \mathbb{C}$.

In ([Castellani-D'Auria-Fr&#233;, vol 2, section III.3.3](#CastellaniDAuriaFre)) this idea is formalized by the constraint that for the given super-$L_\infty$-algebra connection as above, those components of the [[curvature]] forms which carry fermionic indices must be [[linear combinations]] of the components carrying no fermionic indices. (See also at _[L-∞ algebra valued differential forms -- integration of transformation](infinity-Lie+algebroid-valued+differential+form#InfGaugeTrafo)_.)

This rheonomy constraint is equivalent to what elsewhere is called "superspace constraints", see ([AFFFTT 98, below (3.12)](#AFFFTT98)).

See also at _[[rheonomy modality]]_.

#### Details

> under construction
 
Let $\mathbf{H} =$  [[SuperFormalSmooth∞Groupoids]].

+-- {: .num_defn #SuperLInfinityAlgebraValuedDifferentialForms}
###### Definition
**([[super L-∞ algebra|super]]-[[L-∞ algebra valued differential forms|L-∞ algebra valued]] [[super differential forms]])**


Let $\mathfrak{g}$ be an [[super L-∞ algebra]] and let $X$ be a [[super formal smooth ∞-groupoid|super ∞-groupoid]] (for instance a [[supermanifold]] or an [[extended super Minkowski spacetime]]).

Write

\[
  \label{SuperLInfinityAlgberaValuedDifferentialForms}
  \Omega(X,\mathfrak{g})
  \coloneqq
  Hom_{dgcSuperAlg}\big( 
   W(\mathfrak{g}),
   \Omega^\bullet(X)
  \big)
  \;\in\;
  Set
\]

for the [[set]] of [[super L-∞ algebra|super]]-[[L-∞ algebra valued differential forms|L-∞ algebra valued]] [[super differential forms]] on $X$, hence of [[homomorphisms]] of [[differential graded-commutative superalgebras]] from the [[Weil algebra]] of $\mathfrak{g}$

$$
  W(\mathfrak{g})
  \;\coloneqq\;
  \Big(
    \wedge^\bullet\big( 
      \mathfrak{g}^\ast 
         \oplus 
      \underset{
        \mathbf{d}\mathfrak{g}^\ast
      }{\underbrace{\mathfrak{g}^\ast[1]}}
    \big)
    ,
    \mathbf{d}_{W(\mathfrak{g})} 
      = 
    \mathbf{d}_{CE(\mathfrak{g})} 
    + 
    \mathbf{d}
  \Big)
$$

to the [[de Rham algebra]] of [[super differential forms]] on $X$, which is given (see at [[geometry of physics -- supergeometry]] [this example](geometry+of+physics+--+supergeometry#MappingSpaceOddTangentBundle)) by

$$
  \Omega^\bullet(X)
  \;\coloneqq\;
  \flat
  \underline{\mathbf{H}}
    \Big(
    \underline{\mathbf{H}}\big(
      \mathbb{R}^{0\vert 1}, X
    \big),
    \mathbb{R}
  \Big)
$$

equipped with the [[differential graded-commutative superalgebra]]-[[structure]] induced by the [[action]] of $\mathbf{Aut}(\mathbb{R}^{0\vert 1})$ (see at [[odd line]] [there](odd+line#TheAutomorphismSuperGroup))

The restriction, as a [[linear map]], of such a homomorphism

$$
  \Omega^\bullet(X)
    \overset{ \omega }{\longleftarrow}
  W(\mathfrak{g})
$$

along the canonical inclusion of $\wedge^1 \mathfrak{g}^\ast[1] = \mathfrak{g}^\ast[2]$ into the [[Weil algebra]] yields the _[[curvature forms]]_ $F_\omega$ of $\omega$.

\[
  \label{Curvatures}
  \array{
    \Omega(X)
    && 
      \overset{F_\omega}{\longleftarrow}
    &&
    \mathfrak{g}^\ast[2]
    \\
    & {}_{\mathllap{\omega}}\nwarrow && \swarrow_{\mathrlap{}}
    \\
    && W(\mathfrak{g})
  }
\]

=--

+-- {: .num_defn #RestrictionOfSuperDifferentialFormsToBosonicSubmanifold}
###### Definition
**(restriction of [[super L-∞ algebra|super]]-[[L-∞ algebra valued differential forms|L-∞ algebra valued]] [[super differential forms]] to [[bosonic modality|bosonic]] subspace)**

Given $X \in $ [[SuperFormalSmooth∞Groupoids]], write

\[
  \label{InclusionOfBosonicPartIntoSupermanifold}
  X^{\rightsquigarrow} 
    \overset{ \epsilon_X^{\rightsquigarrow} }{\longrightarrow} 
  X
\] 

for the inclusion of the underlying [[bosonic modality|bosonic]] [[space]] (the [[counit of a comonad|counit]] morphism of the [[bosonic modality]] applied to $X$).


The [[pullback of differential forms|pullback]] of the super differential forms in Def. \ref{SuperLInfinityAlgebraValuedDifferentialForms} along (eq:InclusionOfBosonicPartIntoSupermanifold), is a [[function]] of the form

\[
  \label{PullbackOfSuperDifferentialFormsToBosonicSubspace}
  \array{
    \Omega(X, \mathfrak{g})
    &\overset{ \left( \epsilon^{\rightsquigarrow}_{X} \right)^\ast }{\longrightarrow}&
    \Omega(X^{\rightsquigarrow}, \mathfrak{g})
  }
\]


=--

+-- {: .num_example #SmoothSetOfDifferentialPForms}
###### Example


If $X$ is a [[supermanifold]] and $U \subset X$ is a [[coordinate chart]] with [[coordinates]] $(x^a, \theta^\alpha)$ then restricted to this coordinate chart the pullback map (eq:PullbackOfSuperDifferentialFormsToBosonicSubspace) is given by evaluating super-differential forms at $\theta^\alpha = 0$ and $\mathbf{d}\theta^\alpha = 0$

$$
  \left( \epsilon_X^{\rightsquigarrow} \right)^\ast
  \omega_{\vert U}
  \;=\;
  \left. \omega_{\vert U}\right|_{ {\theta^\alpha = 0} \atop {\mathbf{d}\theta^\alpha = 0} }
$$

In this form this operation appears in [Castellani-D'Auria-Fr&#233; 91, vol 2 (III.3.25)](#CastellaniDAuriaFre).

=--


+-- {: .num_defn #RheonomicSetOfDifferentialForms}
###### Definition
**(rheonomic set of super differential forms)**

We may say that a [[subset]]

$$
  \widetilde \Omega(X, \mathfrak{g})
  \subset 
  \Omega(X, \mathfrak{g})
$$

of super-[[Lie algebra valued differential forms|Lie algebra valued]] [[super differential forms]] (Def. \ref{SuperLInfinityAlgebraValuedDifferentialForms})  is _rheonomic_ if on this subset the restriction to the bosoic subspace from Def. \ref{RestrictionOfSuperDifferentialFormsToBosonicSubmanifold} (hence the [[pullback of differential forms]] along $\epsilon_X^{\rightsquigarrow}$) is [[injection|injective]]

$$
  \array{
    \widetilde \Omega(X,\mathfrak{g})
    \overset{
       \left( \epsilon_X^{\rightsquigarrow} \right)^\ast
    }{\hookrightarrow}
    \Omega\big( X^{\rightsquigarrow}, \mathfrak{g}\big)
  }
$$

hence if every super differential form

$$
  \mu 
  \;\in\;
  \widetilde \Omega(X,\mathfrak{g})
$$

is, as an element of this subset, uniquely determined by its restriction to the bosonic submanifold $X^{\rightsquigarrow}$.

=--

More specifically, let now  $V$ be an [[extended super Minkowski spacetime]], with $\mathfrak{g} = \mathrm{iso}(V)$ its super $L_\infty$-extension of the corresponding [[super Poincare Lie algebra]] let $X$ be a [[V-manifold]], and consider the subset

\[
  \label{GlobalCartanConnectionForms}
  \widetilde\Omega(X,\mathfrak{g})
  \;\coloneqq\;
  \Omega_{Cartan}(X,\mathfrak{g})
  \subset
  \Omega(X,\mathfrak{g})
\]

of globally defined [[Cartan connection]]-forms, meaning that their [[super vielbein]] component is constrained to be non-degenerate, establishing at each [[global element|global point]] an [[linear map|linear]] [[isomorphism]] between its super [[tangent space]] and $V$.

+-- {: .num_prop }
###### Proposition

A sufficient condition for the subset (eq:GlobalCartanConnectionForms) to be rheonomic(Def. \ref{RheonomicSetOfDifferentialForms}) is that the components of the [[curvature]]-forms with any odd-graded indices are linear combinations of the components of the curvature forms without odd-graded indices.

=--

([Castellani-D'Auria-Fr&#233; 91, vol 2, (III.3.30)](#CastellaniDAuriaFre))


+-- {: .proof}
###### Proof

Let

$$
  \Omega^\bullet(X) 
  \overset{\mu}{\longleftarrow}
  W(\mathfrak{g})
$$

be a given form. Choosing any basis $\{P_a, Q_\alpha\}$ of $\mathfrak{g}$, $\mu$ has components

$$
  \begin{aligned}
    \mu 
    & 
    = \mu\big( (x^a), (\theta^\alpha) \big)  
    \\
    & = 
    \mu_a\big( (x^a), (\theta^\alpha) \big) d x^a
    +
    \mu_\alpha\big( (x^a), (\theta^\alpha) \big) d \theta^\alpha
  \end{aligned}
  \,.
$$

We have to show,  under the assumption that there existlinear maps

$$
  \Big(
    \phi_{\alpha a}^{b c}
    \;\colon\;
    \mathfrak{g}
    \to \mathfrak{g}
  \Big)_{a,b,c, \alpha}
$$

with

$$
  \big( F_{\mu}\big)_{\alpha a}
  \;=\;
  \phi_{\alpha a}^{b c} \left( \big(F_\mu\big)_{b c} \right)
  \,,
$$

that $\mu$ is uniquely determined already by the component $\mu_a\big( (x^a), (\theta^\alpha = 0)  \big)$. For this it is sufficent to show that all component functions

$\mu_a\big( (x^a), (\theta^\alpha)  \big)$

and

$\mu_\alpha\big( (x^a), (\theta^\alpha)  \big)$

may be expressed as functions of the $\mu_a\big( (x^a), (\theta^\alpha = 0) \big)$.

We now first prove something weaker, namely that these functions are uniquely determined once we know not just $\mu_a\big( (x^a), (\theta^\alpha = 0) \big)$ but also $\mu_\alpha\big( (x^a), (\theta^\alpha = 0) \big)$. 

> It seems to me that this weaker statement is all that [Castellani-D'Auria-Fr&#233; 91, vol 2, III.3.3](#CastellaniDAuriaFre) really provide, for notice that the last line of their (III.3.29) still depends on $\mu_\alpha\big( (x^a), (\theta^\alpha = 0) \big)$.

By the nilpotency of the odd-graded coordinates $\theta^\alpha$, we have that $\mu$ is a [[multilinear map]] in the $\theta^\alpha$. 

Hence, by [[induction]], assume that the  $k$-linear parts $\mu\big( (x^a), (\theta^\alpha)_{k lin}  \big)$ in the $\theta^\alpha$ of $\mu\big( (x^a), (\theta^\alpha)  \big)$ is fixed by $\mu\big( (x^a), (\theta^\alpha = 0)  \big)$. It is then sufficient to show that also the $(k+1)$-linear term $\mu_a\big( (x^a), (\theta^\alpha)_{(k+1) lin}  \big)$ is fixed.

This is evidently equivalent to the statement that all the [[derivatives]] of $\mu\big( (x^a), (\theta^\alpha)_{(k+1) lin}  \big)$ by any $\theta^{\alpha_{k+1}}$ evaluated at $\theta^{\alpha_{k+1}} = 0$ are fixed. 

The key point is that by the assumption that we have a Cartan connection, these derivatives are proportional to a sum of $\big( F_\omega\big)_{\alpha_{k+1} a}$ with a linear combination of the $\mu$. But by assumption, $\big( F_\omega\big)_{\alpha_{k+1} a}$ (which a priori depends on data at $\mathbf{d}\theta^\alpha \neq 0$) is a linear combination of the curvatures with bosonic indices, and these are determined from the data at $d \theta^\alpha = 0$.

> This is essentially the argument in [Castellani-D'Auria-Fr&#233; 91, vol 2, (III.3.29)-(III.3.31)](#CastellaniDAuriaFre), except that I have added the inductive argument, which seems necessary to really conclude beyond first order in ther odd coordinates.

This shows that $\mu\big( (x^a), (\theta^\alpha)  \big)$ satisfies well-formed differential equations in the $\theta^\alpha$. 

To conclude, we hence need to see that we have sufficient boundary data on $\mu\big( (x^a), (\theta^\alpha)  \big)$ fixed to have the solution to this differential equation be unique.

Now the boundary data for $\mu_a\big( (x^a), (\theta^\alpha)  \big)$ is clearly $\mu_a\big( (x^a), (\theta^\alpha = 0)  \big)$, and if the differential equations did not also depend on $\mu_\alpha\big( (x^a), (\theta^\alpha)  \big)$ this would be the end of the story. 

We do *not* know the analogous boundary data $\mu_\alpha\big( (x^a), (\theta^\alpha = 0)  \big)$, since all of $\mu_\alpha$ is forgotten when restricting to $\mathbf{d}\theta^\alpha = 0$.
But we do have other boundary conditions on $\mu_\alpha\big( (x^a), (\theta^\alpha)  \big)$...

> this is the argument I am adding in order to patch what seems to be a gap in Castellani-D'Auria-Fre

... namely since $\mu_\alpha\big( (x^a), (\theta^\alpha)  \big)$ is the coefficient of $\mathbf{d}\theta^\alpha$, we may/should constrain it to be _independent_ of the corresponding coordinate $\theta^\alpha$, for it had a dependence on this coordinate, this would disappear as we form $\mu = \mu_\alpha \mathbf{d}\theta^\alpha$.

Hence our total boundary conditions are

$$
  \mu_a\big( (x^a), (\theta^\alpha)  \big)_{\vert (\theta^\alpha = 0)}
  =
  \mu_a\big( (x^a), (\theta^\alpha = 0)  \big)
  \;\;\,,
  \;\;
  \frac{\partial}{\partial \theta^\alpha}\mu_\alpha\big( (x^a), (\theta^\alpha)  \big)
  =
  0
$$

(no sum over $\alpha$). Since we started with a solution to these differential equations, which we are trying to reconstruct, there is no issue here of integrating these differential equations. The only question is if these are sufficient to uniquely nail down that solution which we do know exists. Just by counting variables and conditions (which should be independent conditions) this should be the case.


=--

(...)


## Dynamics

### Field equations of motion

A [[Chern-Simons element]] $W(\mathfrak{g}) \leftarrow W(b^{n-1} \mathbb{R}) cs $ of an [[∞-Lie algebra]] defines an [[∞-Chern-Simons theory]] [[action functional]] on the space of $\mathfrak{g}$-[[∞-Lie algebra-valued differential forms]]. 

The major statement/claim is that all the [[supergravity]] [[equations of motion]] specify just precisely those super-$L_\infty$-connections -- satisfying their [[Bianchi identities]]-- which are [rheonomic](#Rheonomy).




### Cosmo-cocycle equations {#ChernSimonsElements}

We discuss how actional functionals for supergravity theories are special cases of this.


In [[first-order formulation of gravity]] where the field of [[gravity]] is encoded in a [[vielbein]] $E$ and a [[spin connection]] $\Omega$, the [[Einstein-Hilbert action]] takes the _Palatini_ form

$$
  \mathcal{L} : (e,\omega) \mapsto
  \int_X R^{a_1 a_2} \wedge E^{a_3} \wedge \cdots \wedge E^{a_d}
    \epsilon_{a_1 \cdots a_d}
  + 
  \cdots
  \,,
$$

where $R^{a b} = \mathbf{d} \Omega^{a b} + \Omega^{a c}\wedge \Omega_c{}^b$ are the components of the [[curvature]] of $\Omega$ and 

$$
  \epsilon_{a_1 \cdots a_n} = sgn(a_1, \cdots, a_n)
$$

is the [[signature of a permutation|signature]] of the index-permutation.

If $E$ and $\Omega$ are components of an [[∞-Lie algebroid-valued form]] $\Omega^\bullet(X) \leftarrow W(\mathfrak{g}) : A$ then such a Palatini term is of the form as may appear in a [[Chern-Simons element]] 

$$
  \Omega^\bullet(X)
  \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{cs}{\leftarrow}
  W(b^{n-1}\mathbb{R})
  :
  cs(A)
$$

on $W(\mathfrak{g})$. We now discuss, following D'Auria-Fr&#233;, how the [[action functional]]s of supergravity are related to [[schreiber:∞-Chern-Simons theory]] for Chern-Simons elements on certain super $\infty$-Lie algebroids.

We discuss a system of equations that characterizes a necessary condition on [[Chern-Simons elements]] in the [[Weil algebra]] $W(\mathfrak{g})$. This condition is called the **cosmo-cocycle condition** in ([DAuriaFre](#DAuriaFre)).

To do so, we work in a basis $\{t^a\}$ of $\mathfrak{g}^*$. Let $\{r^a\}$ be the corresponding shifted basis of $\mathfrak{g}^*[1]$. Write $\{\frac{1}{n}C^a{}_{b_0 \cdots b_n}\}$ for the structure constants in this basis, so that the differential in the [[Weil algebra]] acts as

$$
  d_W : t^a \mapsto \sum_{n \in \mathbb{N}} \frac{1}{n} C^a{}_{b_0 \cdots b_n} t^{b_0} \wedge \cdots \wedge t^{b_n} + r^a
  \,.
$$

Write a general element in  $W(\mathfrak{g})$ as

$$
  cs 
  \coloneqq
  \lambda + r^a \wedge \nu_a + r^a \wedge r^b \wedge \nu_{a b} + \cdots
  + r^{a_1} \wedge \cdots \wedge r^{a_d} \nu_{a_1 \cdots a_2}
  \,,
$$

where $\lambda, \nu_a, \nu_{a b}, \cdots \in CE(\mathfrak{g})$.

+-- {: .num_prop}
###### Proposition

The condition that $d_{W(\mathfrak{g})} (cs)$ has no terms _linear_ in the curvatures $r^a$ is equivalent to the system of equations 

$$
  \begin{aligned}
    \iota_{t_a} \lambda + \nabla \nu_a
    & \coloneqq
    \iota_{t_a} \lambda 
    +
   d_W \nu_a + 
   (-1)^{|t_a|}
   C^c{}_{a b_1 \cdots b_n} t^{b^1} \wedge \cdots t^{b^n} \wedge \nu_c
   \\
   & = 0
  \end{aligned}
  \,,
$$

for all $t_a \in \mathfrak{g}$.

=--

In [DAuriaFre p. 9](#DAuriaFre) this system of equations is called the **cosmo-cocycle condition** . 

+-- {: .proof}
###### Proof

This follows straightforwardly from the definition of the [[Weil algebra]]-[[differential]] $d_{W(\mathfrak{g})}$:


We have $d_{W(\mathfrak{g})} = d_{CE(\mathfrak{g})} + \mathbf{d}$, where $\mathbf{d} : t^a \mapsto r^a$. So

$$
  d_{W(\mathfrak{g})} \lambda 
  = 
  d_{CE(\mathfrak{g})} \lambda
  + 
  \mathbf{d} \lambda 
  = 
  d_{CE(\mathfrak{g})} \lambda
  +
  \sum_a r^a \wedge \iota_{t_a} \lambda
  \,.
$$

Here the first term contains no curvatures, while the second is precisely linear in the curvatures.

Moreover, by the [[Bianchi identity]] we have 

$$
  d_{W(\mathfrak{g})} r^a 
  = 
  \sum_n C^a{}_{b_0 \cdots b_n} r^{b_0} \wedge t^{b_1} \wedge \cdots \wedge t^{b_n}
  \,.
$$

Therefore the condition that all terms in $d_{W} cs$ that are linear in $r^a$ in  vanish is

$$
  \begin{aligned}
    & r^a \wedge \iota_{t_a} \lambda 
    +
    (-1)^{|t_a|} 
    r^a d_{CE(\mathfrak{g})}\nu_a 
    + 
    r^a \wedge \sum_n C^c{}_{a b_1 \cdots b_n} t^{b_1} \wedge t^{b_n} \wedge \nu_c
    \\
    & = 
    r^a(
      \iota_{t_a} \lambda + 
      d_{CE(\mathfrak{g})}\nu_a   
      + 
      (-1)^{|t_a|}
      \sum_n C^c{}_{a b_1 \cdots b_n} t^{b_1}\wedge \cdots  \wedge t^{b_n} \wedge \nu_c
    )
    \\
    &
    = 0
  \end{aligned}
  \,.
$$

=--


+-- {: .num_remark}
###### Remark

For comparison with [DAuriaFre](#DauriaFre) notice the following:

* there all elements $t_a$ happen to be in even degree. Therefore the extra sign $(-1)^{|t_a|}$ that we display does not appear.


* the term that we write $d_{CE(\mathfrak{g})} \nu_a$ is there equivalently expressed as
  
  $$
    d_{W(\mathfrak{g})} \nu_a \;,\;\;\; at\; r^a = 0
  $$

  ([equation (2.21)](http://ncatlab.org/nlab/files/GeometricSupergravity.pdf#page=9)).

=--

### Examples {#Examples}

#### Minimal 4-dimensional $N=2$ supergravity

(...)

#### 5-Dimensional Supergravity

(...)

#### $11$-Dimensional Supergravity

Let $\mathfrak{g} = \mathfrak{sugra}_6$ be the [[supergravity Lie 6-algebra]].

The [[Weil algebra]]:

$$
  d_{W} c 
  =  
  \frac{1}{2} \bar \psi \wedge \Gamma^{a b} \psi \wedge e_a \wedge e_b
  +
  r^c
$$

(...)

The [[Bianchi identity]]

$$
  d_W r^c 
  =
  \bar \psi \wedge \Gamma^{a b} \rho \wedge e_a \wedge e_b
  -
  \bar \psi \wedge \Gamma^{a b} \psi \wedge \theta_a \wedge e_b
$$

The element that gives the action is 

$$
  \begin{aligned}
    \ell_{11} &=
    -\frac{1}{9} R^{a_1 a_2} \wedge e^{a_3} \wedge \cdots \wedge e^{a_{11}}
    \epsilon_{a_1 \cdots a_{11}}
    \\
    & + \cdots
    \\
    & + \cdots
    \\
    & + \cdots
    \\
    & + \cdots
    \\
    & + \cdots
    \\
    &  
    + 
    840 r^c \wedge \bar \psi \Gamma^{a b} \psi \wedge e_a \wedge e_b \wedge c
    \\
    & + \cdots
    \\
    & + 
    \frac{1}{4}\bar \psi\wedge \Gamma^{a_1 a_2} \psi \wedge \bar \psi \Gamma^{a_3 a_4} \psi \wedge e^{a_5} \wedge \cdots \wedge e^{a_{11}}
    \epsilon_{a_1 \cdots a_{11}}
    \\
    & + - 14 \cdot 15 \bar \psi \wedge \Gamma^{a_1 a_2} \psi \wedge \bar \psi
    \Gamma^{a_3 a_4} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_4}
    \wedge C
    \\
    & -840  r^c \wedge r^c \wedge c
  \end{aligned}
$$

This is [DAuriaFre, page 26](#DAuriaFre).

The first term gives the [[Palatini action]] for gravity.

The last terms is the Chern-Simons term for the the [[supergravity C-field]].

The second but last two terms are the cocycle $\Lambda$.

+-- {: .num_remark}
###### Remark

The term $\lambda$ appearing here (the two terms containing no curvature) are $d_{CE}$-exact: there is a modification of this element by a $d_W$-exact term for which the cocycles vanish, $\lambda = 0$ ([DAuriaFre, page 27](#DAuriaFre) and [CastellaniDAuriaFre (III.8.136)](#CastellaniDAuriaFre)). It follows that in particular $\lambda$ is $d_{CE}$-closed. So with the above discussion of the "cosmo-cocycle"-condition the results given in [DAuriaFre](#DauriaFre) imply that $d_{W} \ell_{11}$ has no 0-ary and no unary terms in the curvatures.

=--

We find that the $d_W$-differential of this Lagrangian term is

$$
  \begin{aligned}
    d_{W} \ell_{11}
    & = 
    r^c \wedge r^c \wedge r^c
    \\
    &
    -
    R^{a_1 a_2} \wedge \theta^{a_3} \wedge \cdots \wedge e^{a_{11}}
    \epsilon_{a_1 \cdots a_{11}}
    \\
    & + \cdots
    \\
    &
    +  840 \{ 
      \sigma(r^c \wedge \bar \psi \Gamma^{a b} \psi \wedge e_a \wedge e_b \wedge c )
      +
      (d_{W}(r^c \wedge r^c)) \wedge c
      = 0 
    \}
    \\
    & + 840 r^c \wedge r^c \wedge \bar \psi \Gamma_{a b} \psi\wedge e_a \wedge e_b
    -
    i 48 r^c \wedge \sigma(\bar \psi \wedge \Gamma^{a_1 \cdots a_5} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_5})
    \\
    & + \cdots
  \end{aligned}
  \,.
$$

This fails to sit in the shifted generators by the terms coming from the translation algebra. For the degree-3 element $c$ however it does produce
the expected term $r^c \wedge r^c \wedge r^c$.

## Related entries

* [[torsion constraints in supergravity]]

* [[super Cartan geometry]]

* [[geometry of physics -- supergeometry]]




## References 
 {#References}

The formulation of supergravity of [[supermanifolds]] and the relevance of the [[Bianchi identities]] originates in

* R. Grimm, [[Julius Wess]], [[Bruno Zumino]], _A complete solution of the Bianchi identities in superspace with supergravity constraints_, Nuclear Phys. B152 (1979), 255&#8211;265.

* [[Julius Wess]], [[Bruno Zumino]], _Superspace formulation of supergravity_, Phys. Lett. B66 (1977), 361&#8211;364.

The use in this context of [[super L-∞ algebras]] in their [[formal dual]] incarnation [[semifree dga|semifree]] super-graded commutative [[dg-algebras]] was suggested originally in

* {#Nieuwenhuizen82} [[Peter van Nieuwenhuizen]], _Free Graded Differential Superalgebras_, in _Istanbul 1982, Proceedings, Group Theoretical Methods In Physics_, Istanbul Grp.Th.Meth.1982 228-247l  and CERN Geneva - TH. 3499 ([spire:182644](http://inspirehep.net/record/182644))

The original articles that introduced specifically the D'Auria-Fr&#233;-formalism are

* {#DAuriaFre80} [[Riccardo D'Auria]], [[Pietro Fré]] [[Tullio Regge]], _Graded Lie algebra, cohomology and supergravity_, Riv. Nuov. Cim. 3, fasc. 12 (1980) ([spire](http://inspirehep.net/record/156191))

* {#DAuriaFre82}  [[Riccardo D'Auria]], [[Pietro Fré]], _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140 (<a href="https://doi.org/10.1016/0550-3213(82)90376-5">doi:10.1016/0550-3213(82)90376-5</a>,  [[GeometricSupergravityErrata.pdf:file]]) 

* {#CFGPN83} [[Leonardo Castellani]], [[Pietro Fré]], F. Giani, K. Pilch, [[Peter van Nieuwenhuizen]], _Gauging of $d = 11$ supergravity?_, Annals of Physics Volume 146, Issue 1, March 1983, Pages 35&#8211;77

The standard textbook monograph on [[supergravity]] in general and this formalism is particular is

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* [[Pietro Fré]], _Gravity, a Geometrical Course: Volume 2: Black Holes, Cosmology and Introduction to Supergravity_, Springer 2012

Review:

* [[Leonardo Castellani]], _Supergravity in the group-geometric framework: a primer_ ([arXiv:1802.03407](https://arxiv.org/abs/1802.03407))

* {#DAuria20} [[Riccardo D'Auria]], _Geometric supergravity_ ([arXiv:2005.13593](https://arxiv.org/abs/2005.13593)) in:  [[Leonardo Castellani]],  [[Anna Ceresole]], [[Riccardo D'Auria]], [[Pietro Fré]] (eds.): _Tullio Regge: An Eclectic Genius_, World Scientific 2019 ([doi:10.1142/11643](https://doi.org/10.1142/11643)) 

Discussion of [[gauged supergravity]] in this way is in 

* {#Fre05} [[Pietro Fré]], _M-theory FDA, Twisted Tori and Chevalley Cohomology_, Nucl.Phys.B742:86-123, 2006 ([arXiv:hep-th/0510068](http://arxiv.org/abs/hep-th/0510068))


The interpretation of the D'Auria-Fr&#233;-formulation as identifying supergravity fields as [[∞-Lie algebra valued differential forms]] is in

* {#SSS} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:L-∞ algebra connections]]_ in _Quantum Field Theory_, Birkh&#228;user (2009), 303-424, DOI: 10.1007/978-3-7643-8736-5_17  ([publisher link](http://www.springerlink.com/content/p421153213548t31/), [arXiv:0801.3480](http://arxiv.org/abs/0801.3480))

 

The [[Lie integration]] of that to genuine [[principal ∞-connections]] is in 

* {#FiorenzaSchreiberStasheff10} [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:?ech cocycles for differential characteristic classes]]_, Advances in Theoretical and Mathematical Phyiscs, Volume 16 Issue 1 (2012) ([arXiv:1011.4735](http://arxiv.org/abs/1011.4735))
  

The [[super L-∞ algebras]] that govern the construction are interpreted in the [[higher gauge theory]] of an [[schreiber:∞-Wess-Zumino-Witten theory]] description of the [[Green-Schwarz sigma-model]]-type $p$-[[branes]] in

* {#FSS} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ 2013 ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))
 

Apart from that the first vague mention of the observation that the "FDA"-formalism for supergravity is about higher categorical Lie algebras (as far as [[Urs Schreiber|I]] am aware, would be grateful for further references) is page 2 of

* {#FreGrassi08} [[Pietro Fré]], [[Pietro Antonio Grassi]], _Free differential algebras, rheonomy and pure spinors_ ([arXiv:0801.3076](http://arxiv.org/abs/0801.3076))

An attempt at a comprehensive discussion of the formalism in the context of [[cohesive (∞,1)-topos]]-theory for 
[[smooth super ∞-groupoid]]s is in the last section of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_


To compare D'Auria-Fre with our language here, notice the following points in their book

* The statement that a supergravity field is a morphisms $\phi : T X \to inn(\mathfrak{g})$ or dually a morphism $\Omega^\bullet(X) \leftarrow W(\mathfrak{g}) : \phi$ out of the [[Weil algebra]] of the [[supergravity Lie 3-algebra]] or similar is implicit in $(I.3.122)$ (but it is evident, comparing with the formulas at [[Weil algebra]]) -- notice that these authors call $\phi$ here a "soft form".

* What we identify as gauge transformations and shifts by the characterization of [[curvature]] forms on the [[cylinder object]] $U \times \Delta^{1|p}$ is their equation (I.3.36).





Here are some more references:

* [[Pietro Fré]], _M-theory FDA, twisted tori and Chevalley cohomology_ ([arXiv] (http://www.arxiv.org/abs/hep-th/0510068))

* [[Pietro Fré]], [[Pietro Antonio Grassi]], _Pure spinors, free differential algebras, and the supermembrane_ ([arXiv:0606171](http://www.arxiv.org/abs/hep-th/0606171))

* [[Pietro Fré]], [[Pietro Grassi]], _Free differential algebras, rheonomy, and pure spinors_  ([arXiv:0801.3076] (http://www.arxiv.org/abs/0801.3076))

Discussion in this formalism of the [[Green-Schwarz action functional]] for the [[M2-brane]] [[sigma-model]] with a [[target space]]  [[11-dimensional supergravity]] background is in 

* {#AFFFTT98} [[Gianguido Dall'Agata]], Davide Fabbri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl.Phys.B542:157-194,1999, ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

* {#FreGrassi07} [[Pietro Fré]], [[Pietro Antonio Grassi]], _Pure Spinors, Free Differential Algebras, and the Supermembrane_, Nucl. Phys.  B 763:1-34, 2007 ([arXiv:hep-th/0606171](http://arxiv.org/abs/hep-th/0606171))


[[!redirects geometric supergravity]]

[[!redirects rheonomy]]
[[!redirects D'Auria-Fré formulation of supergravity]]
[[!redirects Auria-Fre formulation of supergravity]]


