
> This entry is about the notion in [[physics]]. For the notion of the same name in [[algebra]] see at _[[field]]_.

***

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

### General

The basic example that probably gives the whole concept its name is the [[electric field]] and the [[magnetic field]] in the [[theory (physics)|theory]] of [[electromagnetism]]: if we fix a [[coordinate chart]] of [[spacetime]], then the [[electromagnetic field]] splits into the [[electric field]] and the [[magnetic field]] which are both modeled by a _[[vector field]]_, traditionally denoted $\vec E$ and $\vec B$, respectively, on this coordinate chart. The value $\vec E(x)$ of the vector field at a given point of spacetime is a [[vector]] that expresses the magnitude and direction of the electric [[force]] that is exerted on an [[electric charge|electrically charged]] [[particle]] at $x$. 

In fact more fundamentally, if we do not specify a [[coordinate chart]], then the [[electromagnetic field]] is not in fact represented by two vector fields. Rather, its [[field strength]] is represented by a [[differential 2-form]], hence a [[tensor field]] of rank $(0,2)$, but the the whole field as such is not a tensor field, but is a [[cocycle]] of degree-2 in [[ordinary differential cohomology]]: a [[circle n-bundle with connection|circle bundle with connection]].

Or for instance the field of [[gravity]] if modeled as a [[pseudo-Riemannian metric]] is a [[tensor field]] of rank $(2,0)$ -- but subject to the constraint that this be pointwise non-degenerate. More fundamentally the field of gravity is instead a [[vielbein field]].

Similar statements hold for all [[forces]] of nature, such as the force of [[gravity]] and the [[weak nuclear force]] and [[strong nuclear force]]: a configuration of these is mathematically modeled by [[connection on a bundle|connections]]. Their [[field strengths]] are rank $(0,2)$-tensor fields.

The [[electromagnetic field]] and the field of [[gravity]] are the physical fields that historically gave rise to what is now called _[[classical field theory]]_. But it turns out that fundamentally, in [[quantum physics]], also all [[matter]] in physics is constituted by fields in a similar sense. Specifically, where [[force]] fields in physics are usually [[connection on a bundle|connections on a bundle]], matter fields are [[sections]] of [[associated bundles]]. 


### The idea of field bundles and its problems
 {#IdeaOfFieldBundlesAndItsProblems}

A widespread proposal for how to formalize the notion of _physical field_ is to declare that the specification of a [[physical system]] comes with a [[fiber bundle]] $E \to X$ over the [[spacetime]]/[[worldvolume]] $X$ called the **[[field bundle]]** and that a field configuration of the system is a [[section]] of this field bundle. (Also connections can be encoded as sections of suitable bundles.)

While this goes in the right direction, it cannot be quite the final answer for several reasons:


1. Fields defined as sections of field bundles this way cannot capture "large" gauge phenomena, hence phenomena that genuinelay defined on the [[topological space|topology]] of the [[gauge group]] and not just on its [[Lie algebra]]. Spcifically, in [[Yang-Mills theory]] one can have a gauge bundle whose sections are all [[principal connections]] on on fixed underlying [[principal bundle]], but really that principal bundle is itself part of the [[Yang-Mills field]] -- it is its [[instanton]] sector -- and can vary. But there is no bundle such that sections of it would themselves be equivalent to [[principal bundles]]. 
   
   This is not a negligible problem. For instance the [[vacuum]] in the [[standard model of particle physics]] is a [[superposition]] of all possible instanton sectors, see at _[[instanton in QCD]] for more.

   Similarly for instance [[magnetic charge]], field in [[higher Chern-Simons theoy]] and in many other examples are not describeable, in total, as sections of some field bundle.

1. In [[general covariance|generally covariant]] [[theory (physics)|theories]] fields that differ by a pullback along a [[diffeomorphism]] are required to be [[gauge equivalent|gauge equivalence]]. Hence two sections of a field bundle are to be identified by they become the same when one is pulled back along a diffeomorphism of the base. Again, at least for large diffeomorphisms (thos not connected to the identity) standard field bundle formalism cannot see this.

1. Some fields considered in theoretical physics are sections of/connections on not an ordinary [[fiber bundle]], but a [[higher geometry|higher geometric]] fiber bundle: a [[fiber ∞-bundle]]. For instance the higher analog of the [[electromagnetic field]] which is called the _[[B-field]]_ or _[[Kalb-Ramond field]]_ is a [[circle n-bundle with connection|2-connection]] on a [[principal 2-bundle]]. There is no way to faithfully encode this as a secton of any ordinary [[fiber bundle]]. For instance an accurate description of _[[magnetic charge]]_ (as discussed there) shows that it is represented by such a 2-connection.

### Field $\infty$-bundles and moduli $\infty$-stacks of fields

By the [above](#IdeaOfFieldBundlesAndItsProblems), defining a physical field to be a section of some bundle goes in the right direction, but misses crucial aspects of physical fields. But it turns out that the problem is fixed simply by passing from traditional geometric bundles to bundles in [[higher geometry]].

Below in _[Definition](Definition)_ we discuss a natural unified formulation of the notion of physical field in terms of [[higher geometry]] and then we spell out many [Examples](#Examples).

## Definition 
 {#Definition}

### Physical field

A notion of _field_ in physics is part of a specification of _[[theory (physics)|physical theory]]_ or _[[model (physics)|physical model]]_. We consider specifically the framework of [[prequantum field theory]]. Here a [[theory (physics)|theory]]/[[model (physics)|model]] is specified by (or at least comes with) an _[[action functional]]_. The _field_ content of the theory is part of the specification of the [[domain]] of the action functional. Therefore in def. \ref{FieldsInAnActionFunctional} below we define _action functionals_ and the fields relative to this notion.

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

Given an [[object]] $\mathbf{BgFields} \in \mathbf{H}$ and 
given two objects, to be denoted $\Phi_X, \mathbf{Fields}  \in \mathbf{H}_{/B}$, in the [[slice (∞,1)-topos|slice]] over $\mathbf{BgFields}$,
then an **[[action functional]]** in ($\mathbf{H}, \mathbb{G})$ "on fields on $X$" is a [[morphism]]

$$
  S \;\colon\; [\Phi_X, \mathbf{Fields}]_{\mathbf{H}} \to \mathbb{G}
  \,.
$$

In this context we say that

* the [[dependent sum]] $X \coloneqq \underset{\mathbf{BgField}}{\sum} \Phi_X$ is the **[[worldvolume]]** or **[[spacetime]]**;

* the morphism $\Phi_X \;\colon\; X \to \mathbf{BgFields}$ is the **[[background field]]**;

* the object $\mathbf{Fields}$ is the **[[moduli ∞-stack]] of fields**;

* the [[elements]] of $[\Phi_X,\mathbf{Fields}]_{\mathbf{H}}$, hence the morphims

  $$
    \phi \;\colon\; \Phi_X \to \mathbf{Fields}
  $$

  in $\mathbf{H}_{/\mathbf{BgFields}}$, hence the [[diagrams]]

  $$
    \array{
       X &&\stackrel{\phi}{\to}&& \underset{\mathbf{BgFields}}{\sum} \mathbf{Fields}
       \\
       & {}_{\mathllap{\Phi_X}}\searrow && \swarrow_{\mathrlap{\mathbf{Fields}}}
       \\
       && \mathbf{BgFields}
    }
  $$

  in $\mathbf{H}$, are the **fields** on $X$;

* a **[[gauge transformation]]** is a [[homotopy]] in $[\Phi_X, \mathbf{Fields}]_{\mathbf{H}}$, hence a

  $$
    \phi \Rightarrow \phi'
  $$

* a **[[higher gauge transformation]]** is a [[higher homotopy]] in $[\Phi_X, \mathbf{Fields}]_{\mathbf{H}}$.


=--

+-- {: .num_remark}
###### Remark

The above says in particular that in [[higher geometry]] all fields are [[sigma-model]] fields: if we regard the [[moduli ∞-stack]] $\mathbf{Fields}$ as the [[target space]].

=--

### Restriction and pullback of physical fields

(...)



## Examples
 {#Examples}

We distinguish three broad classes of examples of fields as in def. \ref{FieldsInAnActionFunctional}:

1. [Force fields](#ForceFields)

   1. [Fields of gravity and generalized geometry](#FieldsOfGravityAndGeneralizedGeometry)

      In this case the [[background gauge field]] is a [[G-structure]], the [[moduli stack]] of fields is a [[delooping|delooped]] [[∞-group extension]] $\mathbf{B}\hat G \stackrel{\mathbf{Fields}}{\to} \mathbf{B}G$ and a field is a generalized [[vielbein]] exhibiting a [[reduction and lift of structure groups|reduction/lift of structure group]].

   1. [Gauge fields](#GaugeFields)

      In this case $\mathbf{Fields}$ is a [[moduli space]] $\mathbf{B}G_{conn}$ of [[connections on an ∞-bundle|∞-connections]] on $G$-[[principal ∞-bundles]] for some [[gauge group]] $G \in Grpd(\mathbf{H})$.

1. [Matter fields](#MatterFields)

   In this case the [[background gauge field]] is a $G$-[[principal ∞-bundle]] $P$ for some [[gauge group]] $G \in Grp(\mathbf{H})$ and $\mathbf{Fields}$ is the univeral $\rho$-[[associated ∞-bundle]] $V//G \stackrel{\mathbf{Fields}}{\to} \mathbf{B}G$ for $\rho$ an [[∞-action]] of $G$ on some $V \in \mathbf{H}$. A field is [[section]] of the [[associated ∞-bundle|associated]] $V$-[[fiber ∞-bundle]].

Not all examples fall squarely into one of these types, some are mixtures of these. In particular the moduli stacks $\mathbf{B}G$ here are typically all differentially refined to $\mathbf{B}G_{conn}$ so that for instance every [[reduction and lift of structure groups]] goes along with a corresponding data of the reduction of an [[connection on an ∞-bundle|∞-connection]]. The archetypical example for this are [[spin connections]], see the example _[Ordinary gravity](#OrdinaryGravity)_ below.

### **I)** Force fields
 {#ForceFields}

The two classes of [[force]] fields are:

* [Fields of gravity and generalized geometry](#FieldsOfGravityAndGeneralizedGeometry);

* [Gauge fields](#GaugeFields).


#### **I a)** Fields of gravity and generalized geometry
 {#FieldsOfGravityAndGeneralizedGeometry}

Let 

$$
  A \to \hat G \to G
$$

be an [[∞-group extension]] in $\mathbf{H}$. Then a [[lift of the structure group]] from $G$ to $\hat G$ is typically interpreted as a field of [[gravity]] and its variants.

##### Ordinary gravity
 {#OrdinaryGravity}

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$, let 

$$
  \mathbf{Fields} 
  \;\colon\;
  \mathbf{B}O(n)
   \stackrel{\mathbf{OrthStruc}_n}{\to}
  \mathbf{B}GL(n)
$$

the [[delooping]] of the [[Lie group|Lie]]-[[subgroup]] inclusion of the [[orthogonal group]] into the [[general linear group]] in [[dimension]] $n$ (the inclusion of the [[maximal compact subgroup]]).

For $X \in $ [[SmoothMfd]] $\hookrightarrow$ $\mathbf{H} \coloneqq$ [[Smooth∞Grpd]] a [[smooth manifold]] of [[dimension]] $n$, write

$$
  \Phi_X \coloneqq \tau_X \;\colon\; X \to \mathbf{B}GL(n)
$$

for the canonical map modulating the $GL(n)$-[[principal bundle]] to which the [[tangent bundle]] is canonically [[associated bundle|associated]].

=--

+-- {: .num_example #RiemannianVielbein}
###### Example

Morphisms

$$
  \phi \;\colon\; \tau_X \to \mathbf{OrthStruc}_n
$$

in $\mathbf{H}_{/\mathbf{B}GL(n)}$ hence [[diagrams]]

$$
  \array{
    X &&\stackrel{}{\to}&& \mathbf{B}O(n)
    \\
    & \searrow &\swArrow_{e}& \swarrow
    \\
    && \mathbf{B}GL(n)
  }
$$

in $\mathbf{H}$ are equivalently [[vielbein]] fields $e$ exhibiting the [[reduction of the structure group]] from $GL(n)$ to $O(n)$. A [[gauge transformation]] is a local frame transformation. Hence 

$$
  [\tau_X, \mathbf{OrthStruc}_n]_{\mathbf{H}}
  \in 
  \mathbf{H}
$$

is the [[moduli stack]] of [[Riemannian metrics]] on $X$. Every such is a field configuration of ordinary [[gravity]] on $X$. 

=--

+-- {: .num_remark}
###### Remark

The [[smooth structure]] on $X$ as embodied by $\tau_X$ is the [[background field]] in example \ref{RiemannianVielbein}.

=--

+-- {: .num_remark}
###### Remark

The [[homotopy fiber]] of $\mathbf{OrthStruc}_n$ is the [[coset space]] $GL(n)//O(n)$, hence we have a [[homotopy fiber sequence]] of [[moduli stacks]] of the form

$$
  GL(n)//O(n)
  \to
  \mathbf{B}O(n)
  \stackrel{\mathbf{OrthStruc}_n}{\to}
  \mathbf{B}GL(n)
$$

in $\mathbf{H}$. This means that locally, over a [[cover]] ([[1-epimorphism]]) $p \colon U \to X$ over which the [[tangent bundle]] has a trivialization $\tau_X|_U \simeq *$, the space of fields is simply $[U, GL(n)//O(n)]$.

=--

The next example is the differential refinement of the previous one.

+-- {: .num_example}
###### Example

Let 

$$
  \widehat \mathbf{OrthStruc}_n
  \;\colon\;
  \mathbf{B}O(n)_{conn}
  \to 
  \mathbf{B}GL(n)_{conn}
$$

be the canonical differential refinement of $\mathbf{OrthStruc}_n$, where now the [[moduli stacks]] of [[principal connections]] appear. For $X$ a manifold as above, let then

$$
  \hat \tau_X 
  \;\colon\;
  X 
  \to
  \mathbf{B}GL(n)_{conn}
$$

modulate an [[affine connection]] on the [[tangent bundle]]. A field 

$$
  \phi \;\colon\; \hat \tau_X \to \widehat \mathbf{OrthStruc}_n
$$

is now still equivalently just a [[vielbein]], but its component

$$
  \underset{\mathbf{B}GL(n)_{conn}}{\sum} \hat \tau_X
  \;\colon\;
  X \to \mathbf{B}O(n)_{conn}
$$

now captures the orthognal connection which in the physics literature is often called (inaccurately) the _[[spin connection]]_, denoted $\omega$. The [[vielbein]] then exhibits the original [[affine connection]] as that whose components are the [[Christoffel symbols]] $\Gamma$ of the [[Riemannian metric]] defined as above, a relation that is familiar from the physics literature in the form of the [[equation]]

$$
  \omega = e^{-1}\Gamma e + e^{-1} d e
$$

between local connection 1-form components.

=--

But both these examples do not fully accurately reflect the field content of [[gravity]] yet. This is because the [[theory (physics)|theory]] of [[gravity]] is supposed to by [[general covariance|generally covariant]]. This means that for two [[vielbein]] field configurations as in example \ref{RiemannianVielbein} such that one goes into the other under a [[diffeomorphism]] of [[spacetime]] $X$, there is a [[gauge transformation]] between them.

+-- {: .num_example}
###### Example

Write $\mathbf{Diff}(X) \coloneqq \mathbf{Aut}(X) \in Grp(\mathbf{H})$ for the [[diffeomorphism group]] of the [[smooth manifold]] $X$. There is then the canonical [[∞-action]] of the [[automorphism ∞-group]] $\mathbf{Diff}(X)$ on $X$ itself, exhibited by the universal [[associated ∞-bundle]]

$$
  \left(X // \mathbf{Diff}\left(X\right) \to \mathbf{B}\mathbf{Diff}\left(X\right) \right)
  \in 
  \mathbf{H}_{/\mathbf{B}\mathbf{Diff}\left(X\right)}
  \,.
$$

This induces an [[∞-action]] also on the [[tangent bundle]]

Moreover the trivial bundle

$$
  \mathbf{Fields}
  \coloneqq
  (\mathbf{Diff}(X)\times \mathbf{OrthStruc} \to \mathbf{B}\mathbf{Diff}(X) )
  \in 
  \mathbf{H}_{/\mathbf{B}\mathbf{Diff}(X)}
$$

corresponds to the trivial action.

Then

$$
  \underset{\mathbf{B}(GL(n) \times \mathbf{Diff}(X))}{\prod} [\tau_X, \mathbf{Fields}]
 \in \mathbf{H}
$$

is the accurate space of fields in gravity. 

=--



##### Type II gravity and B-field

$$
  \mathbf{Fields} 
  \;\colon\;
  \mathbf{B}O(n) \times O(n)
  \to 
  \mathbf{B}O(n,n)
$$



#### **I b)** Gauge fields
 {#GaugeFields}

##### Electromagnetic field

[[electromagnetic field]]:

$$
  \mathbf{Fields} = \mathbf{B}U(1)_{conn}
$$

##### Yang-Mills field

[[Yang-Mills field]]

$$
  \mathbf{Fields} = \mathbf{B}G_{conn}
$$


### **II)** Matter fields
 {#MatterFields}

[[matter]]

#### Fermions
 {#Fermions}

[[fermion]]:

$S$ a [[spin representation]]

$$
  \mathbf{Fields} 
  \;\colon\;
  S//Spin
  \to 
  \mathbf{B}Spin
$$

#### Tensor fields

$\mathbf{Fields} : \mathbb{R}^{n (p+q)}//GL(n) \to \mathbf{B}GL(n) $

### **III)** Sigma-model fields

[[sigma-model]]

#### Particle

[[particle]]

$\mathbf{Fields} = $ [[spacetime]]

#### Charged particle

[[1d Chern-Simons theory]]

Let $T \hookrightarrow G$ be [[maximal torus]] which fixes a given 
[[weight (in representation theory)]] $\langle \lambda, -\rangle$ on compact simple and simply connected [[Lie group]] $G$. Let $\rho$ be the corresponding [[representation]] under the [[Borel-Weil-Bott theorem]].

Then the topological part of the [[sigma model]] for the [[particle]] charged under $(G,\rho)$ in some $G$-[[background gauge field]] has

$$
  \mathbf{Fields} 
  \;\colon\;
  \Omega^1(-,\mathfrak{g})//T
  \to 
  \Omega^1(-,\mathfrak{g})//G
  \simeq
   \mathbf{B}G_{conn}
$$

## Related concepts

[[prequantum field theory]]

* **field**

* [[extended Lagrangian]], [[prequantum n-bundle]], [[action functional]]

* [[classical field theory]]

* [[quantum field theory]]


## References

Section _[Fields](geometry%20of%20physics#Fields)_ in 

* _[[geometry of physics]]_

[[!redirects quantum field]]
[[!redirects quantum fields]]

[[!redirects field configuration]]
[[!redirects field configurations]]

