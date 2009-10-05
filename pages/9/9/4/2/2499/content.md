
<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>


#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

In 1981 D'Auria and Fr&eacute; noticed, in [GeSuGra](#References), that the intricacies of various [[supergravity]] [[classical field theory|classical field theories]] have a strikingly powerful reformulation in terms of [[semifree dga|semifree differential graded-commutative algebra]]s. 

Here we describe this formalism in the way it is usually presented, and at the same time discuss the following useful re-interpretation:

+-- {: .standout}

**Abstract nonsense reinterpretation** of the D'Auria-Fr&eacute; formalism:

The theory of [[supergravity]] (at least as a [[classical field theory]]) is a theory of [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connection]]s with values in the [[supergravity Lie 3-algebra]] $\mathfrak{sugra}(10,1)$.

This identifies field configurations of supergravity with [[connection on a bundle|connections]] on certain [[principal ∞-bundle]]s.

=--

The pivotal concept that allows to pass between this interpretation and the D'Auria-Fr&eacute;-formalism is the concept of [[schreiber:∞-Lie algebroid|∞-Lie algebroid]] with its various incarnations:

+-- {: .standout}

**Incarnations of $\infty$-Lie algebroids**

A (super) [[schreiber:∞-Lie algebroid|∞-Lie algebroid]] 

* is an [[infinitesimal space|infinitesimal]] (super)[[schreiber:∞-Lie groupoid|∞-Lie groupoid]]

* that may be modeled as a [[simplicial object|simplicial]] (super) [[infinitesimal space]]

* whose [[schreiber:∞-quantity|∞-quantity]] of functions is a [[cosimplicial algebra|cosimplicial]] ([[super algebra|super]]) algebra

* that under the [[monoidal Dold-Kan correspondence]] maps to a (super) [[semifree dga|semifree differential graded-commutative algebra]]: the [[Chevalley-Eilenberg algebra]] of the (super) [[schreiber:∞-Lie algebroid|∞-Lie algebroid]].

=--

Notably the [[semifree dga]] that D'Auria-Fr&#233; base the description of 11-dimensioonal [[supergravity]] on is the [[Chevalley-Eilenberg algebra]] of the [[supergravity Lie 3-algebra]], which is an [[L-infinity-algebra|∞-Lie algebra]] that is a higher central extension 

$$
  0 \to b^2 \mathfrak{u}(1)
  \to \mathfrak{sugra}(10,1)
  \to
  \mathfrak{siso}(10,1)
  \to
  0
$$

of a [[super Poincare Lie algebra]] $\mathfrak{siso}(10,1)$ in the way the [[String Lie 2-algebra]] $\mathfrak{string}(n)$ is a higher central extension of $\mathfrak{so}(n)$.

A super [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connection]] with values in $\mathfrak{sugra}(10,1)$ on a [[supermanifold]] $X$ is locally given by [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid valued differential forms]] consisting of

* a $\mathbb{R}^{11}$-valued 1-form $e$ 

* a $\mathfrak{so}(10,1)$-valued 1-form $\omega$

* a spin-representation valued 1-form $\psi$

* a 3-form $C$ .

These are identified with the fields of 11-dimensional [[supergravity]], respectively:

* the _graviton_ $(e, \omega)$

* the _gravitino_ $\psi$

* the _[[supergravity C-field]]_ $C$ .


By realizing this data as components of a Lie 3-algebra valued connection (more or less explciitly), the D'Auria-Fr&eacute;-formalism achieves some conceptual simplication of 

* the construction of supersymmetric [[supergravity]] [[action functional]]s;

* the determination of the corresponding classical equations of motion.


## _nomen est omen_ - the higher gauge theory reinterpretation ##

Originally D'Auria and Fr&eacute; referred to commutative [[semifree dga]]s as as _Cartan integrable systems_ . Later the term _free differential algebra_, abbreviated _FDA_ was used instead and became popular. Nowadays much of the literature that studies commutative [[semifree dga]]s in [[supergravity]] refers to them as "FDA"s. One speaks of the _FDA approach to supergravity_ . 

But strictly speaking "free differential algebra" is a misnomer: genuinely free differential algebras are pretty boring objects. Crucially it is _only_ the underlying graded commutative algebra which is required to be free as a graded commutative algebra in that it is a [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g}^*$ on a [[graded vector space]] $\mathfrak{g}^*$. The differential on that is in general not free, hence the more precise term _[[semifree dga]]_ . 

In fact, when $\mathfrak{g}$ is concentrated in non-positive degree (so that $\wedge^\bullet \mathfrak{g}^*$ os concentrated in non-negative degree) the differential on $\wedge^\bullet \mathfrak{g}^{*}$ encodes all the structure of an [[L-infinity algebroid|∞-Lie algebroid]] on $\mathfrak{g}$. If $\mathfrak{g}$ is concentrated in negative degree the differential encodes the structure of an [[L-infinity algebra|∞-Lie algebra]] on $\mathfrak{g}$. This interpretation of [[semifree dga]]s in [[Lie theory]] is the key to our _abstract nonsense reformulation_ of the D'Auria-Fr&eacute;-formalsim.

Already D'Auria and Fr&eacute; themselves, and afterwards other authors, have tried to better understand the intrinsic conceptual meaning of their [[dg-algebra]] formalism that happened to be so useful in [[supergravity]]: 

the idea arose and then became pupular in the "FDA"-literature that the D'Auria-Fr&eacute;-formalism should be about a concept called **soft group manifolds**. This is motivated from the observation that by means of the [[dg-algebra]] formulation the fields in [[supergravity]] arrange themselves into systems of [[differential form]]s that satisfy equations structurally similar to the Maurer-Cartan forms of left-inavriant differential forms on a [[Lie group]] -- _except_ that where the ordinary Maurer-Cartan equation has a "0" on one side, these equations for supergravity fields have there the possibly non-vanishing [[field strength]]. These generalized Maurer-Cartan equations are suggested in the "FDA"-literature to describe generalized or "softened" group manifolds.

However, even when the field strenghts do vanish does the remaing collection of differential forms not constrain the base manifold to be a group. Rather, if the field strenghs do vanish we have a natural interpretation of the remaining differential form data as being flat [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid valued differential forms]], given by a morphism

$$
  A : T X \to \mathfrak{g}
$$

from the [[tangent Lie algebroid]] of the base [[manifold]] $X$ to the [[L-infinity-algebra|∞-Lie algebra]] $\mathfrak{g}$ encoded by the [[semifree dga]] in question. In fact, applying the functor from [[Lie infinity-algebroid|∞-Lie algebroid]]s to [[dg-algebra]]s given by forming [[Chevalley-Eilenberg algebra]]s, the above morphism turns into a [[dg-algebra]] morphism

$$
  \Omega^\bullet(X)
  \leftarrow
  CE(\mathfrak{g})
  :
  A
$$

to the [[deRham dg-algebra]] of $X$ (which we denote by the same letter, by convenient abuse of notation).

Since $CE(\mathfrak{g})$ is semifree, this is a map of [[graded vector space]]s 

$$
  \Omega^\bullet(X)
  \leftarrow
  \mathfrak{g}^*
  :
  A
$$

together with a constraint that imposes the respect of the morphism for the differentials on $CE(\mathfrak{g})$ and on $\Omega^\bullet(X)$. Such a morphism of graded vector spaces in canonically identified with a $\mathfrak{g}$-valued differential form (recall that $\mathfrak{g}$ is a  [[graded vector space]])

$$ 
  \omega \in \Omega^\bullet(X,\mathfrak{g})
$$

and the remaining constraint is precisely the Maurer-Cartan-like equation that is known from left-invariant 1-fomrs on a [[Lie group]]. In fact, for $G$ a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ there is a canonical morphism

$$
  \Omega^\bullet(G)
  \leftarrow
  CE(\mathfrak{g})
$$

whose image are precisely the left-invariant 1-forms on the [[Lie group]] $G$ and whose respect for the differentials is precisely the ordinary Maurer-Cartan equation. 

To see the role of group manifolds for more general morphisms

$$
  \Omega^\bullet(X)
  \leftarrow
  CE(\mathfrak{g})
  :
  A
$$

one has to apply [[Lie integration]] of the [[Lie infinity-algebroid|∞-Lie algebroid]] morphism $T X \to \mathfrak{g}$ to a morphism of [[Lie infinity-groupoid|∞-Lie groupoid]]s

$$
  \Pi(X) \to \mathbf{B}G
$$
 
where $\Pi(X)$ is the [[path infinity-groupoid|path ∞-groupoid]] and where $\mathbf{B}G$ is the [[delooping]] of an [[n-group]] $G$ that integrates the [[L-infinity-algebra|Lie n-algebra]] $\mathfrak{g}$.
Such morphisms are the integrated version of flat [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid valued differential forms]].

The theory of [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connections]] is about 

1. the generalization of such flat form data to [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid valued differential forms]] with [[schreiber:curvature|∞-Lie algebroid valued curvature]].

1. the generalization from globally defined differential form data -- which are connections on _trivial_ [[principal ∞-bundle]]s -- to [[schreiber:theory of differential nonabelian cohomology|differential cocycles]] encoding connections on arbitrary [[principal ∞-bundle]]s.

The D'Auria-Fr&eacute;-formalism, after our re-interpretation, is about the first of these points. So as an immediate gain of our reformlation of D'Auria-Fr&eacute;-formalism in terms of [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connection]]s we obtain, using the second of these points, a natural proposal for a formulation of [[supergravity]] field configurations that are globally topologically nontrivial. Physicists speak of **instanton solutions**.

In fact, 

+-- {: .standout}

our reformulation exhibits the D'Auria-Fr&eacute;-formalism as being secretly the realization of [[supergravity]] as a higher [[gauge theory]].

=--

In fact, it realizes supergravity as an example for a _nonabelian_ higher gauge theory in that a [[supergravity]] field configuration is not realizable as a cocycle in [[differential cohomology|abelian differential cohomology]] as in ordinary abelian higher [[gauge theory]] (see there) but as a cocycle in [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]].



# Details #

## the supergravity Lie 3-algebra ##

recall [[supergravity Lie 3-algebra]] $\mathfrak{sugra}(10,1)$

...

## super Lorentzian spacetime manifolds ##

The base space $X$ on which a [[supergravity]] field is a super Lie $n$-algebra valued [[schreiber:Cartan-Ehresmann infinity-connection|...]] is a [[supermanifold]].

In particular, for constructing the [[action functional]] of [[supergravity]] we want $X$ to locally look like [[super Minkowski space]].


## field configuration and field strength ##


A local field configuration on a [[supermanifold]] $X$ in the [[classical field theory]] is a morphism
 
$$
  \Pi^{inf}(X) \stackrel{(A, F_A)}{\to}
  inn(\mathfrak{sugra}(\mathfrak{g}))
$$

from the [[schreiber:infinitesimal path ∞-groupoid|infinitesimal path ∞-groupoid]] to the inner-derivation Lie 4-algebra $inn(\mathfrak{sugra}(10,1))$. Dually this is a morhism of [[dg-algebra]]s from the [[Weil algebra]] $W(\mathfrak{sugra}(10,1))$ to the [[deRham dg-algebra]] $\Omega^\bullet(X)$ of $X$:

$$
  \Omega^\bullet(X)
   \leftarrow
   W(\mathfrak{sugra}(10,1))
   :
   (A,F_A)  
   \,.
$$

This is [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid differential form data]] with [[schreiber:curvature|∞-Lie algebroid valued curvature]] that is explicitly given by:


* connection forms / field configuration

  * $E \in \Omega^1(X,\mathbb{R}^{10,1})$ -- the **vielbein** (part of the _graviton field_)

  * $\Omega \in \Omega^1(X, \mathfrak{so}(10,1))$ -- the **spin connection** (part of the _graviton field_)

  * $\Psi \in \Omega^ 1(X,S)$ -- the **spinor** (the gravitino field)

  * $C \in \Omega^3(X)$ -- a 3-form (the [[supergravity C-field]])

* [[schreiber:curvature|curvature]] forms / [[field strength]]s

  * $T = d E + \Omega \cdot E + \Gamma(\bar \Psi \wedge \Psi) \in \Omega^2(X,\mathbb{R}^{10,1})$ - the **torsion**

  * $R = d \Omega + [\Omega \wedge \Omega] \in \Omega^2(X, \mathfrak{so}(10,1))$ - the **Riemann curvature**

  * $\rho = d \Psi + (\Omega \wedge \Psi) \in \Omega^2(X, S)$ -- the **covariant derivative of the spinor**

  * $G = d C + \mu_4(\psi, E) \in \Omega^4(X)$ -- the **4-form field strength**


## gauge transformations ##

There is an evident notion of _gauge transformations_ (i.e. isomorphisms) of [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connection]]s. We unwrap this and derive this way the formulation of gauge transformations as used in the [literature](#References) on the  D'Auria-Fr&eacute; formalism.

Recall -- from the discussion at [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connection]] -- that $\infty$-connections on a trivial [[principal ∞-bundle]] (to which we restrict attention here) on a space $X$ with values in an [[L-infinity algebra|L-∞-algebra]] $\mathfrak{g}$ are encoded by a diagram

$$
  \array{
    \Pi^{inf}(X) &\stackrel{A}{\to}& cone(\mathfrak{g})
    \\
    \downarrow^{id} && \downarrow
    \\
    \Pi^{inf}(X) &\stackrel{P(F_A)}{\to}& 
    \Sigma \mathfrak{g}
  }
$$

of [[schreiber:∞-Lie algebroid|∞-Lie algebrboid]]s, which dually, after passing to [[Chevalley-Eilenberg algebra]]s, becomes a diagram of [[dg-algebra]]s

$$
  \array{
    \Omega^\bullet(X) &\stackrel{A}{\leftarrow}& W(\mathfrak{g})
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(X)
    &\stackrel{\{P(F_A)\}}{\leftarrow}&
    inv(\mathfrak{g})
  }
  \,,
$$

where $W(\mathfrak{g})$ is the [[Weil algebra]] and $inv(\mathfrak{g})$ the algebra of [[invariant polynomial]]s of $\mathfrak{g}$, where $F_A$ denotes the [[schreiber:curvature|curvature]] forms and $P(F_A)$ the collection of [[schreiber:curvature|curvature characteristic forms]] built from them.

A gauge transformation between two field configurations

$$
  \phi, \phi' : \Pi^{inf}(X) \to cone(\mathfrak{g})
$$

is modeld by a left [[homotopy]] $\phi \Rightarrow \phi'$ 
(in the corresponding [[model category]] structure that [[presentable (infinity,1)-category|presents]] this higher categoriccal setup) which extends to  a homotopy of [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connections]] in that it fits into a diagram

$$
  \array{
    \Pi^{inf}(X) &\stackrel{\nearrow \downarrow\searrow^{\phi}}{\searrow \nearrow_{\phi'}}& 
      cone(\mathfrak{g})
    \\
    \downarrow^{id} && \downarrow
    \\
    \Pi^{inf}(X) &\stackrel{P(\phi) = P(\phi')}{\to}& \Sigma \mathfrak{g}
  }
$$

meaning that $\eta$ does not affect the [[schreiber:curvature|curvature characteristic forms]] associated with the two fields $\phi$ and $\phi'$.

In terms of the [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg]] [[semifree dga]]s
this means more explicitly that a gauge transformation is presented by

* a morphism

  $$
    \eta : \Omega^\bullet(X\times I) \leftarrow W(\mathfrak{g})
    \,,
  $$

  where $I = [0,1]$ is the standard interval, 

* such that 

  * its restriction
    to the two endpoints of the interval 
    reproduces $\phi$ and $\phi'$, respectively,
    i.e. such that we have a commuting diagram

    $$
      \array{
        \Omega^\bullet(X)
        \\
        \;\;\uparrow^{(Id \times i_0)^*} & \nwarrow^{\phi}
        \\
        \Omega^\bullet(X \times I) 
        &\stackrel{\eta}{\leftarrow}&  W(\mathfrak{g})
        \\
        \;\;\downarrow^{(Id \times i_1)^*} 
           & \swarrow_{\phi'}
        \\
        \Omega^\bullet
      }
      \,,
    $$ 

    where $i_0, i_1 : {*} \to I$ are the two endpoint inclusions of the interval
    
  * and such that the composite $\Omega^\bullet(X \times I) \stackrel{\eta}{\leftarrow} W(\mathfrak{g}) \stackrel{}{\leftarrow} inv(\mathfrak{g})$  which computes the [[schreiber:curvature|curvature characteristic form]]s of $\eta$, is constant along $I$, in that we have a commuting
    diagram
    
    $$
      \array{
        \Omega^\bullet(X \times I) 
         &\stackrel{\eta}{\leftarrow}&
        W(\mathfrak{g})
        \\
        \uparrow && \uparrow
        \\
        \Omega^\bullet(X) &\stackrel{\{P(F_A)\}}{\leftarrow}&
         inv(\mathfrak{g})
      }
      \,,
    $$

    where the left vertical morphism is pullback along the projection $X \times I \to X$.

We now unwrap what this means explicitly in terms of generators of [[dg-algebra]]s and find the physics literature expression for gauge transformations this way:

Let $V$ be the [[graded vector space]] underlying the [[L-infinity algebra|L-∞-algebra]] $\mathfrak{g}$, and let $V^*$ its degreewise dual. Recall that the underlying graded-commutative algebra of the [[Weil algebra]] $W(\mathfrak{g)$ is the [[Grassmann algebra]] $\wedge^\bullet V^* \oplus V^*[1]$ on $V^*$ plus its degree-shifted copy. 

* Choose a basis $\{t^a\}$ of $V^*$ of homogeneous degree elements. Write $\{\sigma t^a\}$ for the corresponding basis of $V^*[1]$.  On a homogeneous basis element $t^a \in V^*$ of degree $k$ in the remaining unshifted copy $\eta$ may be written as

  $$
    \eta(t^a) := \eta^a := \bar \phi^a + (d_{dR} s) \wedge \epsilon^a 
     \;\;\;\;\in \Omega^\bullet(X \times I)
    \,,
  $$

  where

  * $\bar \phi^a$ is in the image of $\Omega^k(X)$ pulled back to $\Omega^k(X \times I)$ and such that with $s \in C^\infty(I)$ the canonical coordinate on the interval we have $\bar \phi^a|_{s = 0} = \phi^a$ and $\bar \phi^a|_{s = 1} = {\phi'}^a$;

  * $\epsilon^k$ is in the image of $\Omega^{k-1}(X)$ under pullback. 

The component $\epsilon^a$ is what in the physics literature is called the **gauge parameter**.

We will see below that writing the same expression for the shifted generators $\sigma t^a$ will imply that the analogue of $\epsilon$ vanishes on these and that $\eta$ is constant along the interval on shifted elements. So for brevity we assume this now.

Apart from being a morphism of graded-commutative algebra, $\eta$ has to be a morphism of [[dg-algebra]]s and hence has to respect the differentials on both sides in that

$$
  d_{dR}\bar \phi^a  - (d_{dR} s) \wedge (d_{dR} \epsilon^a)
  =
  \phi(d_{\mathfrak{g}} t^a)
  \,.
$$

Projected onto the $\frac{\partial}{\partial s}$-component this equation says (remembering the form of $\eta$ given above and that it vanishes on shifted generators) that

$$
  \frac{\partial}{\partial s} \bar\phi^a =
  d_{dR} \epsilon^a + 
  C^a{}_{\{b_i\} c} \bar\phi^{\{b_i\}} \wedge \epsilon^c
  \,,
$$

where 

* $C^a{}_{b c}$ are the structure constants of $d_{\mathfrak{g}}$ in our chosen basis of $V^*$ 

* $F_{\eta}^a$ is the [[schreiber:curvature|curvature]] component of $\eta$ (the image or $\sigma t^a$ under $\eta$) along the interval.  

This is the familiar **equation for infinitesimal gauge transformations** as it appears in the [references](#references). Or almost:

+-- {: .un_remark}
###### Remark 

In [[Supergravity and Superstrings - A Geometric Perspectrive|SugraGeomPersp]] a notion called
"Lie derivative on soft group manifolds" is proposed
(p. 125) and later used essentially for gauge transformations as above. It leads to a formula
that looks like the above, but contains an extra
curvature term.

But the idea of "soft group manifold" itself
seems to [[Urs Schreiber|me]] not to have a precise
definition (in fact this entry is based on the 
claim that what is called "soft group manifold" there
is trying to capture the idea of [[schreiber:∞-Lie algebroid valued differential forms|L-∞-algebra valued connection forms]]) and 
to that extent it remains unclear what 
equation (I.3.135) actually encodes. 

This is in particular a problem
when $\mathfrak{g}$ is not just an ordinary [[Lie algebra]]
but a general [[L-infinity-algebra ]] with higher degree
generators. This latter
problem seems to be the issue that section 2.3 of [Castellani 05](http://arxiv.org/abs/hep-th/0508213) wants to formalize and clarify. There, too, the idea "soft group 
manifold" is appealed to, though.

Notice that the above formula makes unambiguous and 
perfect sense for all $L_\infty$-algebras $\mathfrak{k}$.

**However** in most cases where the proposed formula including that additional curvature term is actually _used_ to do something, it is actually used for what below we identify as the action of _diffeomorphisms_  on 
[[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid valued differential form]]s. 

=--

## diffeomorphism action of connection forms ##

Let $v$ be a vector field on $X$ (here $X$ may be a [[supermanifold]] and $v$ may, accordingly, be an odd vector field). Then $v$ generates a [[diffeomorphism]]

$$
  \exp(v) : X \to X
$$

and this in turn acts on field configurations 
$\Pi^{inf}(X) \to cone(\mathfrak{g})$ by precomposition

$$
  \cdots \mapsto 
  \Pi^{inf}(X) \stackrel{\exp(v)}{\to}
  \Pi^{inf}(X) \to cone(\mathfrak{a}) 
  \,.
$$

Since this diffomorphism is connected to the identity, this is in fact a homotopy

$$
  \array{
    \Pi^{inf}(X)
     \\
     \downarrow & \searow^{\phi}
     \\
   \Pi^{inf}(X \times I) &\stackrel{\eta}{\to}& cone(\mathfrak{g})
     \\
     \uparrow & \nearrow_{\exp(v) \phi}
     \\
     \Pi^{inf}(X)
  }
  \,.
$$

But it is not necessarily a _gauge transformation_ as above, in that the curvature characteristic form are also pulled back along the diffeomorphism and not required to be constant.

Then, the differential form data

$$
  \Omega^\bullet(X) \letarrow W(\mathfrak{g}) : A
$$

transforms infinitesimally under this diffeomorphism by the [[Lie derivative]] $L_v = [d_{dR}, \iota_v]$, which we can write

$$
  L_v A = 
$$

...


## rheonomy ##

### Idea ###

As discussed above, a **field configuration** in [[supergravity]] is a morphism

$$
  \Pi^{inf}(X) \to \mathfrak{a}
$$

from the [[schreiber:infinitesimal path ∞-groupoid|infinitesimal path ∞-groupoid]] of the spacetime [[supermanifold]] $X$ to some super [[schreiber:∞-Lie algebroid|∞-Lie algebroid]] $\mathfrak{a}$.

This [[supergeometry]] interpretation of fields in [[supergravity]] gives an immediate interpretatoin of the **[[supersymmetry]]** that the [[supergravity]] [[action functional]] $S_{sugra}$ is supposed to enjoy: this just says that 

+-- {: .standout}

[[supersymmetry|Supersymmetry]] of the [[supergravity]] [[action functional]] $S_{sugra} : \{\Pi^{inf}(X) \to \mathfrak{a}\} \to \mathbb{R}$ is nothing but its invariance under super-diffeomorphisms $\phi : X \stackrel{\simeq}{\to} X$ of the spacetime [[supermanifold]] $X$:

$$
  S_{sugra}(\Pi^{inf}(X) \to \mathfrak{a})
  =
  S_{sugra}(\Pi^{inf}(X) \stackrel{\Pi^{inf}(\phi)}{\to}\Pi^{inf}(X) \to \mathfrak{a})
  \,.
$$

=--

So this is nothing but the super-refinement of the familiar diffeomorphism invariance of the Einstein-Hilbert action of ordinary [[gravity]].

While this is conceptually very useful, in much of the literature the supersymmetry of supergravity is not conceived in this way. The reason for that is that in the standard supergravity theories that physicists are interested in, a field configuration is _not_ a _general_ superfield $\Pi^{inf}(X) \to \mathfrak{a}$: rather, it is one whose components (listed above: graviton, gravitino, fermions, etc.) appear like fields on the _ordinary_ spacetime manifold $X_{red}$ underlying the [[supermanifold]] $X$. 

There are two options to formalize this:

1. **non-geometric approach**: realize the fields of [[supergravity]] as fields on an ordinary spacetime [[manifold]] $X_{red}$ -- this makes the supersymmetry operations act on the fields in a conceptually complicated way

2. **geometric approach**: realize the fields of [[supergravity]] as fields on a [[supermanifold]] $X$. This makes supersymmetry of the [[action functional]] be simply super-diffeomorphism invariance. But then ensure that the fields _appear_ as if their components were functions on just the underlying ordinary manifold $X_{red}$ by putting a suitable constraint on the fields. This constraint is the **rheonomy** constraint.

The _rheonomy_ constraint has been and is usefully compared with a holomorphicity constraint: a _function_
$f : \mathbb{C} \to \mathbb{C}$ on the complex plane and hence a priori of two real coordinates, is _holomorphic_ if it locally looks like it effectively depends only on one of the two coordintes. Similarly, a **rheonomic superfield** is a function on a [[supermanifold]] which locally looks as if it depends only on the ordinary even (bosonic) coordinates.

To further exploit this analogy, notice that an ordinary function $f$, being a [[differential form|0-form]] has a [[schreiber:curvature|curvature]] which is the 1-form $R_F := d f$. The function $f$ is holomorphic precisely if its curvature, in this sense, vanishes on all tangent vectors proportional to $\frac{\partial}{\partial \bar z}$.

From this analogy, the following statement should sound very plausible, which we discuss in detail below:

+-- {: .standout}

A [[schreiber:∞-Lie algebroid valued differential forms|field]] $\Pi^{inf}(X) \to \mathfrak{a}$ on the [[supermanifold]] $X$ is **rheonomic** if its [[schreiber:curvature|curvature]] vanishes on odd tangent vectors, or is an algebraic expression in terms of the curvature components on even tangent vectors.

=--

### details ##

...

this is part III, chapter III.3.3 in 

* [[Supergravity and Superstrings - A Geometric Perspective]]

# References #

The original article that introduced th D'Auria-Fr&eacute;-formalism is

* **geSuGra** R. D'Auria, P. Fr&eacute; _Geometric supergravity in $D = 11$ and its hidden supergroup_ [[GeometricSupergravity.pdf:file]]
 
The standard textbook monograph on [[supergravity]] in general and this formalism is particular is

* [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fre]], [[Supergravity and Superstrings - A Geometric Perspective]]

The _geometric perspective_ discussed there is both the emphasis of working over base [[supermanifold]]s and combined with that the the approach that here we call tthe _D'Auria-Fr&eacute;-formalism_ . 

At the time of this writing the book is out of print and unavailable from bookshops. But your local physics department library may have a copy.

The interpretation of the D'Auria-Fr&eacute;-formalism in the light of higher gauge theory as discussed above, together with a discussion of the [[supergravity Lie 3-algebra]] in the context of [[String Lie 2-algebra|String Lie n-algebra]]s was given in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _$L_\infty$-algebra connections_ ([arXiv](http://arxiv.org/abs/0801.3480))

This had been preceded by some blog discussion, for instance

* [[Urs Schreiber]], _Castellani on FDA in SuGra: gauge 3-group of M-theory_ ([blog](http://golem.ph.utexas.edu/string/archives/000840.html))

This is, as far as [[Urs Schreiber|I]] am aware, the first occurence of the explicit observation that the FDA-formalism is about higher gauge theory, based on hearing a talk on

* [[Leonardo Castellani]], _Lie derivatives along antisymmetric tensors, and the M-theory superalgebra_ ([arXiv](http://arxiv.org/abs/hep-th/0508213))

* [[Urs Schreiber]], _SuGra 3-connection reloaded_ ([blog](http://golem.ph.utexas.edu/category/2006/08/sugra_3connection_reloaded.html))

Apart from that the first vague mention of the observation that the "FDA"-formalism for supergravity is about higher categorical Lie algebras (as far as [[Urs Schreiber|I]] am aware, would be grateful for further references) is page 2 of

* [[Pietro Fre]], [[Pietro Antonio Grassi]], _Free differential algebras, rheonomy and pure spinors_ ([arXiv](http://arxiv.org/abs/0801.3076))

Here are some more references:

* Pietro Fr&eacute;, _M-theory FDA, twisted tori and Chevalley cohomology_ ([arXiv] (http://www.arxiv.org/abs/hep-th/0510068))

* Pietro Fr&eacute; and Pietro Antonio Grassi,
_Pure spinors, free differential algebras, and the supermembrane_ ([arXiv] (http://www.arxiv.org/abs/hep-th/0606171))

* Pietro Fr&eacute; and Pietro Antonio Grassi, _Free differential algebras, rheonomy, and pure spinors_ 
([arXiv] (http://www.arxiv.org/abs/0801.3076))