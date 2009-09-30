
#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

In 1981 D'Auria and Fr&#233; noticed, in [GeSuGra](#References), that the intricacies of various [[supergravity]] [[classical field theory|classical field theories]] have a strikingly powerful reformulation in terms of [[semifree dga|semifree differential graded-commutative algebra]]s. 

Here we describe this formalism in the way it is usually presented, and at the same time discuss the following useful re-interpretation:

+-- {: .standout}

**Abstract nonsense reinterpretation** of the D'Auria-Fr&#233; formalism:

The theory of [[supergravity]] (at least as a [[classical field theory]]) is a theory of [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connection]]s with values in the [[supergravity Lie 3-algebra]] $\mathfrak{sugra}(10,1)$.

This identifies field configurations of supergravity with [[connection on a bundle|connections]] on certain [[principal ∞-bundle]]s.

=--

The [[supergravity Lie 3-algebra]] is an [[L-infinity-algebra|∞-Lie algebra]] that is a higher central extension 

$$
  0 \to b^2 \mathfrak{u}(1)
  \to \mathfrak{sugra}(10,1)
  \to
  \mathfrak{siso}(10,1)
  \to
  0
$$

of a [[super Poincare Lie algebra]] $\mathfrak{siso}(10,1)$ in the way the [[String Lie 2-algebra]] $\mathfrak{string}(n)$ is a higher central extension of $\mathfrak{so}(n)$.

A [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connection]] with values in $\mathfrak{sugra}(10,1)$ is locally given by [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid valued differential forms]] consisting of

* a $\mathbb{R}^{11}$-valued 1-form $e$ 

* a $\mathfrak{so}(10,1)$-valued 1-form $\omega$

* a spin-representation valued 1-form $\psi$

* a 3-form $C$ .

These are identified with the fields of 11-dimensional [[supergravity]], respectively:

* the _graviton_ $(e, \omega)$

* the _gravitino_ $\psi$

* the _[[supergravity C-field]]_ $C$ .


By realizing this data as components of a Lie 3-algebra valued connection (more or less explciitly), the D'Auria-Fr&#233;-formalism achieves some conceptual simplication of 

* the construction of supersymmetric [[supergravity]] [[action functional]]s;

* the determination of the corresponding classical equations of motion.


## _nomen est omen_ - the higher gauge theory reinterpretation ##

Originally D'Auria and Fr&#233; referred to commutative [[semifree dga]]s as as _Cartan integrable systems_ . Later the term _free differential algebra_, abbreviated _FDA_ was used instead and became popular. Nowadays much of the literature that studies commutative [[semifree dga]]s in [[supergravity]] refers to them as "FDA"s. One speaks of the _FDA approach to supergravity_ . 

But strictly speaking "free differential algebra" is a misnomer: genuinely free differential algebras are pretty boring objects. Crucially it is _only_ the underlying graded commutative algebra which is required to be free as a graded commutative algebra in that it is a [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g}^*$ on a [[graded vector space]] $\mathfrak{g}^*$. The differential on that is in general not free, hence the more precise term _[[semifree dga]]_ . 

In fact, when $\mathfrak{g}$ is concentrated in non-positive degree (so that $\wedge^\bullet \mathfrak{g}^*$ os concentrated in non-negative degree) the differential on $\wedge^\bullet \mathfrak{g}^{*}$ encodes all the structure of an [[L-infinity algebroid|∞-Lie algebroid]] on $\mathfrak{g}$. If $\mathfrak{g}$ is concentrated in negative degree the differential encodes the structure of an [[L-infinity algebra|∞-Lie algebra]] on $\mathfrak{g}$. This interpretation of [[semifree dga]]s in [[Lie theory]] is the key to our _abstract nonsense reformulation_ of the D'Auria-Fr&#233;-formalsim.

Already D'Auria and Fr&#233; themselves, and afterwards other authors, have tried to better understand the intrinsic conceptual meaning of their [[dg-algebra]] formalism that happened to be so useful in [[supergravity]]: 

the idea arose and then became pupular in the "FDA"-literature that the D'Auria-Fr&#233;-formalism should be about a concept called **soft group manifolds**. This is motivated from the observation that by means of the [[dg-algebra]] formulation the fields in [[supergravity]] arrange themselves into systems of [[differential form]]s that satisfy equations structurally similar to the Maurer-Cartan forms of left-inavriant differential forms on a [[Lie group]] -- _except_ that where the ordinary Maurer-Cartan equation has a "0" on one side, these equations for supergravity fields have there the possibly non-vanishing [[field strength]]. These generalized Maurer-Cartan equations are suggested in the "FDA"-literature to describe generalized or "softened" group manifolds.

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

The D'Auria-Fr&#233;-formalism, after our re-interpretation, is about the first of these points. So as an immediate gain of our reformlation of D'Auria-Fr&#233;-formalism in terms of [[schreiber:Cartan-Ehresmann ∞-connection|Cartan-Ehresmann ∞-connection]]s we obtain, using the second of these points, a natural proposal for a formulation of [[supergravity]] field configurations that are globally topologically nontrivial. Physicists speak of **instanton solutions**.

In fact, 

+-- {: .standout}

our reformulation exhibits the D'Auria-Fr&#233;-formalism as being secretly the realization of [[supergravity]] as a higher [[gauge theory]].

=--

In fact, it realizes supergravity as an example for a _nonabelian_ higher gauge theory in that a [[supergravity]] field configuration is not realizable as a cocycle in [[differential cohomology|abelian differential cohomology]] as in ordinary abelian higher [[gauge theory]] (see there) but as a cocycle in [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]].



# Details #

...

recall [[supergravity Lie 3-algebra]] $\mathfrak{sugra}(10,1)$

...


## field configuration and field strength ##


A local field configuration on a [[manifold]] $X$ in the [[classical field theory]] is a morphism
 
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


## rheonomy ##


One central point of the D'Auria-Fr&#233; reformulation of supergravity is that it naturally leads to or admits the formulation of the **rheonomy constraint**.

It turns out that those field configurations of [[supergravity]] -- see above -- that satisfy the classical equations of motion are those for which the curvature forms appearing above are all expressible as local linear combinations of just the vielbein and the spinor in a certain way...

> [[Urs Schreiber]]: in light of the higher gauge theoretic formulation there must be a good way to understand the rheonomy constraint from abstract nonsense. It must be something like saying that the [[schreiber:curvature|curvature characteristic forms]] of the $\mathfrak{sugra}(10,1)$-connection are given by those of the underlying super-translation Lie algebra valued connection. But I am not entirely sure yet. 



# References #

The original article that introduced th D'Auria-Fr&#233;-formalism is

* **geSuGra** R. D'Auria, P. Fr&#233; [[GeometricSupergravity.pdf:file]]
 
There exists a monograph on this formalims is

* [[Leonardo Castellani]], [[Riccardo d' Auria]], [[Pietro Fre]], _Supergravity and superstrings: a geometric perspective_ (2 volumes) World Scientific, 1991

The _geometric perspective_ discussed there is precisely what here we call the _D'Auria-Fr&#233;-formalism_ . At the time of this writing the book is out of print and unavailable from bookshops. But your local physics department library will have a copy.

A huge list of further literature goes here

...

The interpretation of the D'Auria-Fr&#233;-formalism in the light of higher gauge theory as discussed above, together with a discussion of the [[supergravity Lie 3-algebra]] in the context of [[String Lie n-algebra]]s was given in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _$L_\infty$-algebra connections_ ([arXiv](http://arxiv.org/abs/0801.3480))

This had been preceeded by some blog discussion, for instance

* [[Urs Schreiber]], _Castellani on FDA in SuGra: gauge 3-group of M-theory_ ([blog](http://golem.ph.utexas.edu/string/archives/000840.html))

  this is, as far as [[Urs Schreiber|I]] am aware, the first occurence of the explicit observation that the FDA-formalism is about higher gauge theory, based on hearing a talk on

  * [[Leonardo Castellani]], _Lie derivatives along antisymmetric tensors, and the M-theory superalgebra_ ([arXiv](http://arxiv.org/abs/hep-th/0508213))

* [[Urs Schreiber]], _SuGra 3-connection reloaded_ ([blog](http://golem.ph.utexas.edu/category/2006/08/sugra_3connection_reloaded.html))

Apart from that the first vague mention of the observation that the "FDA"-formalism for supergravity is about higher categorical Lie algebras (as far as [[Urs Schreiber|I]] am aware, would be grateful for further references) is page 2 of

* [[Pietro Fre]], [[Pietro Antonio Grassi]], _Free differential algebras, rheonomy and pure spinors_ ([arXiv](http://arxiv.org/abs/0801.3076))