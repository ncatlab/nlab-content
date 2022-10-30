
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In fundamental [[physics]] the basic entities that are being described are called _fields_, as they appear in the terms _[[classical field theory]]_ and _[[quantum field theory]]_.

The basic example that probably gives the whole concept is name is the [[electric field]] and the [[magnetic field]] in the [[theory (physics)|theory]] of [[electromagnetism]]: if we fix a [[coordinate chart]] of [[spacetime]], then the [[electromagnetic field]] splits into the [[electric field]] and the [[magnetic field]] which are both modeled by a _[[vector field]]_, traditionally denoted $\vec E$ and $\vec B$, respectively, on this coordinate chart. The value $\vec E(x)$ of the vector field at a given point of spacetime is a [[vector]] that expresses the magnitude and direction of the electric [[force]] that is excerted on an [[electric charge|electrically charged]] [[particle]] at $x$. 

But in general a _field_ in physics need not be a [[vector field]]. In fact more fundamentally, if we do not specify a [[coordinate chart]], then the [[electromagnetic field]] is not in fact represented by two fector field. Rather, its [[field strength]] is represented by a [[differential 2-form]] and the the whole field as such is a [[cocycle]] of degree-2 in [[ordinary differential cohomology]]: a [[circle n-bundle with connection|circle bundle with connection]].

Similar statements hold for all [[forces]] of nature, such as the force of [[gravity]] and the [[weak nuclear force]] and [[strong nuclear force]]: a configuration of these is mathematically modeled by what mathematically are _[[tensor]] fields_ and [[connection on a bundle|connections]], hence one speaks of the _field of gravity_ etc.

The [[electromagnetic field]] and the field of [[gravity]] are the physical fields that historically gave rise to what is now called _[[classical field theory]]_. But it turns out that fundamentally, in [[quantum physics]], also all [[matter]] in physics is constituted by fields in a similar sense. Specifically, where [[force]] fields in physics are usually [[connection on a bundle|connections on a bundle]], matter fields are [[sections]] of bundles. 

Indeed, a standard proposals to formalize the notion of _physical field_ is to declare that a [[physical system]] comes with a [[fiber bundle]] $E \to X$ over the [[spacetime]]/[[worldvolume]] $X$, and that a field configuration of the system is a [[section]] of this field bundle, see for instance the discussion at the beginning of _[[multisymplectic geometry]]_ for more on such field bundles. (Also connections can be encoded as sections of suitable bundles).

While this goes in the right direction, it cannot be quite the final answer:

some fields considered in theoretical physics are sections of/connections on not an ordinary [[fiber bundle]], but a [[higher geometry|higher geomtric]] fiber bundle: a [[fiber ∞-bundle]]. For instance the higher analog of the [[electromagnetic field]] which is called the _[[B-field]]_ or _[[Kalb-Ramond field]]_ is a [[circle n-bundle with connection|2-connection]] on a [[principal 2-bundle]]. There is no way to faithfully encode this as a secton of any ordinary [[fiber bundle]]. For instance an accurate description of _[[magnetic charge]]_ (as discussed there) shows that it is represented by such a 2-connection.

Below we discuss a natural unified formulation of the notion of physical field in terms of [[higher geometry]] and spell out many examples.

## Definition 

A notion of _field_ in physics is part of a specification of _[[theory (physics)|physical theory]]_ or _[[model (physics)|physical model]]_. We consider specifically the framework of [[prequantum field theory]]. Here a [[theory (physics)|theory]]/[[model (physics)|model]] is specified by or at least comes with a an _[[action functional]]_. The _field_ content of the theory is part of the specification of the [[domain]] of the action functional. Therefore in def. \ref{FieldsInAnActionFunctional} below we define _action functionals_ and the fields relative to this notion.

We work in the following context.

+-- {: .num_defn}
###### Context

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]]. For many of the examples below it is furthermore assumed that $\mathbf{H}$ is equipped with [[differential cohesion]]. This implies in particular that there is a notion of [[smooth manifold]] [[internalization|internal]] to $\mathbf{H}$.

Fix $\mathbb{G} \in Grp(\mathbf{H})$ a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, hence a cohesive [[∞-group]].

=--

For the main definition below we need the following basic notation.

+-- {: .num_defn}
###### Definition

For $B \in \mathbf{H}$ any [[object]], and $X,A \in \mathbf{H}_{/B}$ two objects in the [[slice (∞,1)-topos]], write

$$
  [X,A]_{\mathbf{H}}
  \coloneqq
  \underset{B}{\prod} [X,A]
  \in \mathbf{H}
$$

for the $\mathbf{H}$-valued [[hom object]] between $X$ and $A$: the [[dependent product]] over $B \to *$ of the [[internal hom]] $[X, A] \in \mathbf{H}_{/B}$.

=--

The following defines the notion of _[[action functional]]_ and as part of the data it defines the notion of _physical field_.

+-- {: .num_defn #FieldsInAnActionFunctional}
###### Definition

Given

1. an [[object]] $B \in \mathbf{H}$;

1. objects $X, \mathbf{Fields} \in \mathbf{H}_{/B}$ in the [[slice (∞,1)-topos|slice]] over $B$;

then an **[[action functional]]** in ($\mathbf{H}, \mathbb{G})$ "on fields on $X$" is a [[morphism]]

$$
  S \;\colon\; [X, \mathbf{Fields}] \to \mathbb{G}
  \,.
$$

In this context we say that

* $X$ is the **[[worldvolume]]** or **[[spacetime]]**;

* $\mathbf{Fields}$ is the **[[moduli space]] of fields**;

* $S$ is the **[[action functional]]** itself.

* a **field** is an [[element]] of $[X,\mathbf{Fields}]_{\mathbf{H}}$, hence a morphims

  $$
    \phi \;\colon\; X \to \mathbf{Fields}
  $$

* a **[[gauge transformation]]** is a [[homotopy]] in $[X, \mathbf{Fields}]_{\mathbf{H}}$, hence a

  $$
    \phi \Rightarrow \phi'
  $$

* a **[[higher gauge transformation]]** is a [[higher homotopy]] in $[X, \mathbf{Fields}]_{\mathbf{H}}$.

=--

+-- {: .num_remark }
###### Remark

The literature speaks of _classical fields_ and _quantum fields_, but formal definitions are rare and the distinction is usually blurred and refers more to the focus of the author than the entity under consideration.

If one focuses on the [[critical locus]] of an [[action functional]] as above then one considers its [[classical field theory]] and hence tends to speak of "classical fields". Notably the points in the critical locus, are _fields that satisfy the classical [[equations of motion]]_.

If however one considers the [[quantization]] of an action functional as above, then one tends to speak of [[quantum fields]].

But even this distinction is not uniform in the literature. For instance if $\mathbf{H}$ is something like the collection of [[smooth super ∞-groupoids]], then there are [[fermion]] fields (see the example [Fermions](#Fermions) below) that qualify as classical fields by all accounts above, but are often referred to as quantum fields only. (This is a related to a common mistake in some textbook, the false assertion that there is no [[classical field theory]] of fermion fields, originating in a misappreciation of [[supergeometry]].) 

=--


## Examples

We distinguish two broad classes of examples

* [Force fields](#ForceFields)

* [Matter fields](#MatterFields)

### Force fields
 {#ForceFields}

Two important classes of [[force]] fields are

* [Fields of gravity and generalized geometry](#FieldsOfGravityAndGeneralizedGeometry)

* [Gauge fields](#GaugeFields)

But in general a combination of both appears:

* [Combination of gauge fields and geometry](#CombinationsOfGaugeFieldsAndGeometry)

#### Fields of gravity and generalized geometry
 {#FieldsOfGravityAndGeneralizedGeometry}

Let 

$$
  A \to \hat G \to G
$$

be an [[∞-group extension]] in $\mathbf{H}$. Then a [[lift of the structure group]] from $G$ to $\hat G$ is typically interpreted as a field of [[gravity]] and its variants.

##### Ordinary gravity




#### Gauge fields
 {#GaugeFields}

#### Combinations of gauge fields and geometry
 {#CombinationsOfGaugeFieldsAndGeometry}

### Matter fields
 {#MatterFields}

#### Fermions
 {#Fermions}

(...)


[[!redirects quantum field]]
[[!redirects quantum fields]]

[[!redirects field configuration]]
[[!redirects field configurations]]

