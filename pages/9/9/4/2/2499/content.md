

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The D'Auria-Fr&#233; formalism for [[supergravity]] identifies the field content with [[∞-Lie algebra valued forms]] with values in the [[supergravity Lie 3-algebra]].

For background see [[∞-Chern-Weil theory introduction]].

***


In 1981 D'Auria and Fr&#233; noticed, in [GeSuGra](#References), that the intricacies of various [[supergravity]] [[classical field theory|classical field theories]] have a strikingly powerful reformulation in terms of [[semifree dga|semifree differential graded-commutative algebra]]s. 

Here we describe this formalism in the way it is usually presented, and at the same time discuss the following useful re-interpretation:

+-- {: .standout}

**General abstract reinterpretation** of the D'Auria-Fr&#233; formalism:

The theory of [[supergravity]] (at least as a [[classical field theory]]) is a theory of [[connections on ∞-bundles]]. The fields are locally [[∞-Lie algebra valued forms]] with values for instance in the [[supergravity Lie 3-algebra]] $\mathfrak{sugra}(10,1)$ (for maximal 11-dimensional supergravity).

=--

The pivotal concept that allows to pass between this interpretation and the D'Auria-Fr&#233;-formalism is the concept of [[∞-Lie algebroid]] with its various incarnations:

+-- {: .standout}

**Incarnations of $\infty$-Lie algebroids**

A (super) [[∞-Lie algebroid]] 

* is an [[infinitesimal space|infinitesimal]] (super)[[∞-Lie groupoid]]

* that may be modeled as a [[simplicial object|simplicial]] (super) [[infinitesimal space]]

* whose [[function algebras on ∞-stacks|function algebra]] is a [[cosimplicial algebra|cosimplicial]] ([[super algebra|super]]) algebra

* that under the [[monoidal Dold-Kan correspondence]] maps to a (super) [[semifree dga|semifree differential graded-commutative algebra]]: the [[Chevalley-Eilenberg algebra]] of the (super) [[∞-Lie algebroid]].

=--

Notably the [[semifree dga]] upon which D'Auria-Fr&#233; base their description of 11-dimensional [[supergravity]] is the [[Chevalley-Eilenberg algebra]] of the [[supergravity Lie 3-algebra]], which is an [[∞-Lie algebra]] that is a [[∞-Lie algebra cohomology|higher central extension]]

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

* a $\mathbb{R}^{11}$-valued 1-form $e$ 

* a $\mathfrak{so}(10,1)$-valued 1-form $\omega$

* a spin-representation valued 1-form $\psi$

* a 3-form $C$ .

These are identified with the fields of 11-dimensional [[supergravity]], respectively:

* the _[[graviton]]_ $(e, \omega)$

* the _[[gravitino]]_ $\psi$

* the _[[supergravity C-field]]_ $C$ .


By realizing this data as components of a Lie 3-algebra valued connection (more or less explicitly), the D'Auria-Fr&#233;-formalism achieves some conceptual simplication of 

* the construction of supersymmetric [[supergravity]] [[action functional]]s;

* the determination of the corresponding classical equations of motion.


### _Nomen est omen_ - Higher gauge theory reinterpretation 

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

In fact, 

+-- {: .standout}

The [[∞-Lie theory]]-reformulation exhibits the D'Auria-Fr&#233;-formalism as being secretly the realization of [[supergravity]] as a higher [[gauge theory]].

=--

It realizes supergravity as an example for a _nonabelian_ higher gauge theory in that a [[supergravity]] field configuration is not realizable as a cocycle in [[ordinary differential cohomology]] as in ordinary abelian higher [[gauge theory]] (see there) but as a nonabelian [[connection on an ∞-bundle]].


## Details 

### The supergravity Lie 3-algebra 

recall the [[supergravity Lie 3-algebra]] $\mathfrak{sugra}(10,1)$

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

  * $T = d E + \Omega \cdot E + \Gamma(\bar \Psi \wedge \Psi) \in \Omega^2(X,\mathbb{R}^{10,1})$ - the **torsion**

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

* the **horizontality** or **[[rheonomy]]** constraint or **[[Ehresmann connection|second Ehresmann condition]]**

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

### Rheonomy {#Rheonomy}

A central insight for the construction of supergravity theories in D'Auria-Fre formalism is their notion of _rheonomy_ . In terms of the interpretation supergravity fields as [[connections on ∞-bundles]] we shall interpret this as the [[supergeometry]] version of the [[Ehresmann connection|second Ehresmann condition]], as above for gauge transformations.

For the folowing let $U$ be an ordinary non-super manifold. Write 

$$
  \Delta^{k|p} = \Delta^k \times \mathbb{R}^{0|p}
$$

for the [[supermanifold|super-simplex]]. Then the full diagram for higher gauge transformations of _super_-[[∞-Lie algebra valued forms]], generalizing the one for bosonic [gauge transformations above](#GaugeTransformations) is

$$
    \array{
      \Omega^\bullet(X \times \Delta^{k|p})_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
      &&&
      gauge\;transformation
      \\
      \uparrow && \uparrow &&&& first\;Ehresmann\;condition
      \\
      \Omega^\bullet(X \times \Delta^{k|p})
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{g})
      &&&
      field
      \\
      \uparrow && \uparrow &&&& second\;Ehresmann\;condition
      \\
      \Omega^\bullet(X)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
      &&&
      gauge\;invariant\;observable
    }
$$

Considering this for $\Delta^{0|1} = \mathbb{R}^{0|1}$, this encodes the _horizontality_ or second Ehresmann condition in the odd super-direction. Write $\theta$ for the canonical odd coordinate on $\Delta^{0|1}$. 

The analog of the gauge parameter is now $\epsilon$ in the decomposition

$$
  \Omega^\bullet(U \times \Delta^{0|1}) 
  \leftarrow
  A_U + \epsilon \wedge d \theta
$$

and the analogs of equations \eqref{ShiftedGaugeTrafo} and \eqref{GaugeTrafo} are now the general identity

$$
  \frac{d}{d \theta} A_U = \nabla \epsilon + (F_A)_\theta
$$

for possibly shifted transformations, and the horizontality condition

$$
  \frac{d}{d \theta} A_U = \nabla \epsion
  \,.
$$

This is the _rheonomy constraint_ . (Or -- more generally -- the constraint called such is the condition that $(F_A)_\theta$ is an algebraic expression in the $(F_A)|_{T U}$).

## References {#References}

The original article that introduced th D'Auria-Fr&#233;-formalism is

* **geSuGra** R. D'Auria, P. Fr&#233; _Geometric supergravity in $D = 11$ and its hidden supergroup_ [[GeometricSupergravity.pdf:file]]
 
The standard textbook monograph on [[supergravity]] in general and this formalism is particular is

* [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fre]], [[Supergravity and Superstrings - A Geometric Perspective]]

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
