

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
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

The D'Auria-Fr&#233; formalism for [[supergravity]] identifies the field content with [[∞-Lie algebra valued forms]] with values in a super [[∞-Lie algebra]] such as the [[supergravity Lie 3-algebra]] or the [[supergravity Lie 6-algebra]].

For background see [[∞-Chern-Weil theory introduction]].

### History

Around 1981 D'Auria and Fr&#233; noticed, in [GeSuGra](#DAuriaFre), that the intricacies of various [[supergravity]] [[classical field theory|classical field theories]] have a strikingly powerful reformulation in terms of super [[semifree dga|semifree differential graded-commutative algebra]]s. 

They defined various such super dg-algebras $W(\mathfrak{g})$ and showed (paraphrasing somewhat) that

* the field content, [[field strength]]s, [[covariant derivative]]s and [[Bianchi identity|Bianchi identities]] are all neatly encoded in terms of dg-algebra homomorphism $\Omega^\bullet(X) \leftarrow W(\mathfrak{g}) : \phi$;

* the [[action functional]]s of supergravity theories on such $\phi$ may be constructed as images under $\phi$ of certain elements in $W(\mathfrak{g})$ subject to natural conditions.

Their algorithm was considerably more powerful than earlier more pedestrian methods for construction such action functionals. The textbook [CastellaniDAuriaFre](#CastellaniDAuriaFre) on [[supergravity]] and [[string theory]] from the perspective of this formalism gives a comprehensive description of this approach.

We observe here that the D'Auria-Fre-formalism is [[schreiber:∞-Chern-Simons theory]] for [[∞-Lie algebra-valued forms]] with values in super [[∞-Lie algebra]]s such as the [[supergravity Lie 3-algebra]] and the [[supergravity Lie 6-algebra]].

The pivotal concept that allows to pass between this interpretation and the original formulation is the concept of [[∞-Lie algebroid]] with its various incarnations:

+-- {: .un_remark}
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

the idea arose and then became pupular in the "FDA"-literature that the D'Auria-Fr&#233;-formalism should be about a concept called **[[soft group manifold]]s**. This is motivated from the observation that by means of the [[dg-algebra]] formulation the fields in [[supergravity]] arrange themselves into systems of [[differential form]]s that satisfy equations structurally similar to the [[Maurer-Cartan form]]s of left-invariant differential forms on a [[Lie group]] -- _except_ that where the ordinary Maurer-Cartan form has vanishing [[curvature]] (= [[field strength]]) these equations for supergravity fields have a possibly non-vanishing [[field strength]]. These generalized Maurer-Cartan equations are suggested in the "FDA"-literature to describe generalized or "softened" group manifolds.

However, even when the field strengths _do_ vanish the remaining collection of differential forms does not constrain the base manifold to be a group. Rather, if the field strengths vanish we have a natural interpretation of the remaining differential form data as being flat [[∞-Lie algebroid valued differential forms]], given by a morphism

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

The D'Auria-Fr&#233;-formalism -- after this re-interpretation -- is about the first of these points. So as an immediate gain of our reformlation of D'Auria-Fr&#233;-formalism in terms of [[connections on ∞-bundles]]s we obtain, using the second of these points, a natural proposal for a formulation of [[supergravity]] field configurations that are possibly globally topologically nontrivial. Physicists speak of **instanton solutions**.

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

  * $E \in \Omega^1(X,\mathbb{R}^{10,1})$ -- the **vielbein** (part of the _graviton field_)

  * $\Omega \in \Omega^1(X, \mathfrak{so}(10,1))$ -- the **spin connection** (part of the _graviton field_)

  * $\Psi \in \Omega^ 1(X,S)$ -- the **spinor** (the gravitino field)

  * $C \in \Omega^3(X)$ -- a 3-form (the [[supergravity C-field]])

* [[curvature]] forms / [[field strength]]s

  * $T = d E + \Omega \cdot E + \Gamma(\bar \Psi \wedge \Psi) \in \Omega^2(X,\mathbb{R}^{10,1})$ - the **[[torsion of a metric connection|torsion]]**

  * $R = d \Omega + [\Omega \wedge \Omega] \in \Omega^2(X, \mathfrak{so}(10,1))$ - the **Riemann curvature**

  * $\rho = d \Psi + (\Omega \wedge \Psi) \in \Omega^2(X, S)$ -- the **covariant derivative of the spinor**

  * $G = d C + \mu_4(\psi, E) \in \Omega^4(X)$ -- the **4-form field strength**


### Gauge transformations {#GaugeTransformations}


A [[gauge transformation]] of a field configuration

$$
  \phi : T X \to inn(\mathfrak{g}
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

The condition that all [[curvature characteristic form]]s descent to $U$ in that $A$ completes to a diagram

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

* the **horizontality**  constraint or **[[Ehresmann connection|second Ehresmann condition]]**

  \[
    \frac{d}{d s} A_U = \nabla \lambda
    \label{GaugeTrafo}
    \,.
  \]

This is known as the equation for **infinitesimal [[gauge transformation]]s** of an $\infty$-Lie algebra valued form. 

+-- {: .un_lemma}
###### Observation

By [[Lie integration]] we have that $A_{vert}$ -- and hence $\lambda$ -- defines an element $\exp(\lambda)$ in the [[∞-Lie group]] that integrates $\mathfrak{g}$. 

The unique solution $A_U(s = 1)$ of the above differential equation at $s = 1$ for the initial values $A_U(s = 0)$ we may think of as the result of acting on $A_U(0)$ with the gauge transformatin $\exp(\lambda)$. 

=--

### Rheonomy 
 {#Rheonomy}

(...)


## Dynamics

A [[Chern-Simons element]] $W(\mathfrak{g}) \leftarrow W(b^{n-1} \mathbb{R}) cs $ of an [[∞-Lie algebra]] defines an [[∞-Chern-Simons theory]] [[action functional]] on the space of $\mathfrak{g}$-[[∞-Lie algebra-valued differential forms]]. We discuss how actional functionals for supergravity theories are special cases of this.


### Cosmo-cocycle equations {#ChernSimonsElements}

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

We discuss a system of equations that characterizes a necessary condition [[Chern-Simons element]]s in the [[Weil algebra]] $W(\mathfrak{g})$. This condition is called the **cosmo-cocycle condition** in ([DAuriaFre](#DAuriaFre)).

To do so, we work in a basis $\{t^a\}$ of $\mathfrak{g}^*$. Let $\{r^a\}$ be the corresponding shifted basis of $\mathfrak{g}^*[1]$. Write $\{\frac{1}{n}C^a{}_{b_0 \cdots b_n}\}$ for the structure constants in this basis, so that the differential in the [[Weil algebra]] acts as

$$
  d_W : t^a \mapsto \sum_{n \in \mathbb{N}} \frac{1}{n} C^a{}_{b_0 \cdots b_n} t^{b_0} \wedge \cdots \wedge t^{b_n} + r^a
  \,.
$$

Write a general element in  $W(\mathfrak{g})$ as

$$
  cs 
  :=
  \lambda + r^a \wedge \nu_a + r^a \wedge r^b \wedge \nu_{a b} + \cdots
  + r^{a_1} \wedge \cdots \wedge r^{a_d} \nu_{a_1 \cdots a_2}
  \,,
$$

where $\lambda, \nu_a, \nu_{a b}, \cdots \in CE(\mathfrak{g})$.

+-- {: .un_lemma}
###### Observation

The condition that $d_{W(\mathfrak{g})} (cs)$ has no terms _linear_ in the curvatures $r^a$ is equivalent to the system of equations 

$$
  \begin{aligned}
    \iota_{t_a} \lambda + \nabla \nu_a
    & :=
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

This is straightforward unwinding of the [[Weil algebra]]-differential action:

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


+-- {: .un_remark}
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

+-- {: .un_remark}
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


## References {#References}




The original article that introduced th D'Auria-Fr&#233;-formalism is

* R. D'Auria, P. Fr&#233; _Geometric supergravity in $D = 11$ and its hidden supergroup_ [[GeometricSupergravity.pdf:file]]
{#DAuriaFre} 

The standard textbook monograph on [[supergravity]] in general and this formalism is particular is

* [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fre]], _[[Supergravity and Superstrings - A Geometric Perspective]]_
{#CastellaniDAuriaFre}

The _geometric perspective_ discussed there is both the emphasis of working over base [[supermanifold]]s and combined with that the the approach that here we call tthe _D'Auria-Fr&#233;-formalism_ . 

At the time of this writing the book is out of print and unavailable from bookshops. But your local physics department library may have a copy.

The interpretation of the D'Auria-Fr&#233;-formulation as identifying supergravity fields as [[∞-Lie algebra valued differential forms]]s is in

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _$L_\infty$-algebra connections_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)


Apart from that the first vague mention of the observation that the "FDA"-formalism for supergravity is about higher categorical Lie algebras (as far as [[Urs Schreiber|I]] am aware, would be grateful for further references) is page 2 of

* [[Pietro Fre]], [[Pietro Antonio Grassi]], _Free differential algebras, rheonomy and pure spinors_ ([arXiv](http://arxiv.org/abs/0801.3076))

To compare D'Auria-Fre with our language here, notice the following points in their book

* The statement that a supergravity field is a morphisms $\phi : T X \to inn(\mathfrak{g})$ or dually a morphism $\Omega^\bullet(X) \leftarrow W(\mathfrak{g}) : \phi$ out of the [[Weil algebra]] of the [[supergravity Lie 3-algebra]] or similar is implicit in $(I.3.122)$ (but it is evident, comparing with the formulas at [[Weil algebra]]) -- notice that these authors call $\phi$ here a "soft form".

* What we identify as gauge transformations and shifts by the characterization of [[curvature]] forms on the [[cylinder object]] $U \times \Delta^{1|p}$ is their equation (I.3.36).

* The _[[rheonomy]]_ condition is around (III.3.32) .




Here are some more references:

* Pietro Fr&eacute;, _M-theory FDA, twisted tori and Chevalley cohomology_ ([arXiv] (http://www.arxiv.org/abs/hep-th/0510068))

* Pietro Fr&eacute; and Pietro Antonio Grassi,
_Pure spinors, free differential algebras, and the supermembrane_ ([arXiv] (http://www.arxiv.org/abs/hep-th/0606171))

* Pietro Fr&eacute; and Pietro Antonio Grassi, _Free differential algebras, rheonomy, and pure spinors_ 
([arXiv] (http://www.arxiv.org/abs/0801.3076))


[[!redirects rheonomy]]