+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _Chern-Simons element_ on an [[∞-Lie algebroid]] is an element of its [[Weil algebra]] that exhibits a [[transgression]] between an [[∞-Lie algebroid cocycle]] and an [[invariant polynomial]].



## Definition

We discuss [[∞-Lie algebra]]s and [[∞-Lie algebroid]]s $\mathfrak{a}$ of [[finite type]] in terms of their [[Chevalley-Eilenberg algebra]]s $CE(\mathfrak{a})$. For $\infty$-Lie algebras these are objects in the [[category]] [[dgAlg]] of [[dg-algebra]]s (over a given ground [[field]]). For $\infty$-Lie algebroids these are dg-algebras equipped with a lift of the degree-0 algebra to an algebra over a given [[Fermat theory]] $T$ and such that the [[differential]] is a $T$-[[derivation]] in this degree. (See [[∞-Lie algebroid]] for details). We shall write in the following $dgAlg$ also for the category of dg-algebras with this extra structure and leave the [[Fermat theory]] $T$ implicit.


+-- {: .un_def}
###### Definition

For $\mathfrak{g}$ an [[∞-Lie algebra]] or more generally [[∞-Lie algebroid]], $\mu \in CE(\mathfrak{g})$ a [[∞-Lie algebra cocycle]] (a closed element of the [[Chevalley-Eilenberg algebra]]) and $\langle - \rangle \in W(\mathfrak{g})$ an [[invariant polynomial]], a **Chern-Simons element** exhibiting the _[[transgression]]_ between the two is an element

$$
  cs \in W(\mathfrak{g})
$$

such that

1. we have $d_{W(\mathfrak{g})} cs = \langle -\rangle$

1. and $cs|_{CE(\mathfrak{g})} = \mu$

where the restriction is along the canonical morphism $W(\mathfrak{g}) \to CE(\mathfrak{g})$.

=--

+-- {: .un_remark}
###### Remark 


Notice that a degree-$n$ [[∞-Lie algebroid cocycle]] $\mu$ is equivalently a morphism

$$
  CE(\mathfrak{g}) \leftarrow CE(b^{n-1}\mathbb{R}) : \mu
$$

and an [[invariant polynomial]] of degree $n+1$ is equivalently a morphism

$$
  int(\mathfrak{g}) \leftarrow inv(b^{n-1}\mathbb{R}) = 
  CE(b^n \mathbb{R}) : \langle - \rangle
$$

in [[dgAlg]]. 

=--

+-- {: .un_prop}
###### Observation

A **Chern-Simons element** $cs$ an $\mathfrak{a}$ witnessing the [[transgression]] of $\langle - \rangle$ to $\mu$ is equvivalently a morphism

$$
  W(\mathfrak{g}) \leftarrow W(b^{n-1} \mathbb{R})
  : cs
$$

such that we have a [[commuting diagram]] in [[dgAlg]] 

\[
  \array{
    CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}& CE(b^{n-1} \mathbb{R})
    &&&
    cocycle
    \\
    \uparrow && \uparrow^{\mathrlap{i^*}}
    \\
    W(\mathfrak{g}) &\stackrel{cs}{\leftarrow}& W(b^{n-1} \mathbb{R})
    &&&
    Chern-Simons\;element
    \\
    \uparrow && \uparrow
    \\
    inv(\mathfrak{g}) &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(b^{n-1} \mathbb{R})
    &&&
    invariant polynomial
  }
  \,,
  \label{TheDiagram}
\]

where the vertical morphisms are the canonical ones.

=--


+-- {: .un_remark}
###### Remark

If we think of 

* $W(\mathfrak{g})$ as differential forms on the total space of the universal $G$-bundles;

* $CE(\mathfrak{g})$ as differential forms on the fiber

* $inv(\mathfrak{g})$ as differential forms on the base space

then the abov expresses the classical notion of transgression of forms from the fiber to the base of a fibe bundle (for instance [Borel, section 9](#Borel)).

=--

## Properties

+-- {: .un_pop}
###### Observation

For a given transgressive cocycle $\mu$ and transgressing invariant polynomial $\langle - \rangle$ the set of Chern-Simons elements witnessing the [[transgression]] is a [[torsor]] (based over the point and) over the additive [[group]] 

$$
  \{\omega \in W(\mathfrak{g}) | d_{W(\mathfrak{g}) \omega = 0, i^* \omega = 0}\}
$$

of Chern-Simons elements for vanishing cocycle and vanishing invariant polynomial.

=--



## Origin and relation to other concepts

We discuss the general abstract structures of which Chern-Simons elements are presentations and how they are related to other structures.

The term _Chern-Simons element_ alludes to the term _[[Chern-Simons form]]_ and [[Chern-Simons theory]]. In the following we explain the relation.


### As presentations for the $\infty$-Chern-Weil homomorphism
  {#PresentationForChernWeil}


We explain here briefly how Chern-Simons elements provide a _presentation_ of a generalization of the [[Chern-Weil homomorphism]] -- the [[∞-Chern-Weil homomorphism]] in [[cohesive (∞,1)-topos]] theory -- in the sense in which [[(∞,1)-topos]]es have [[presentable (∞,1)-category|presentations]] by a [[model structure on simplicial presheaves]].


To warm up, we start with considering a traditional setup of [[Lie groupoid]] theory. Recall that for $G$ a [[Lie group]], we may form its [[delooping]] [[Lie groupoid]] dnoted $*//G$ or $\mathbf{B}G$. Then with $X$ any [[smooth manifold]], we have that the [[groupoid]] of [[morphism]]s of [[Lie groupoid]]s $X \to \mathbf{B}G$ is equivalent to that of $G$-[[principal bundle]]s on $X$:

$$
  SmoothGrpd(X, \mathbf{B}G) \simeq G Bund(X)
  \,.
$$

Here we are thinking of [[Lie groupoid]]s as [[differentiable stack]]s, hence as [[object]]s in the [[(2,1)-topos]] 

$$
  SmoothGrpd := Sh_{(2,1)}(SmoothMfd)
$$ 

of [[stack]]s/[[(2,1)-sheaves]] on the [[site]] [[SmoothMfd]] (equivalently on its [[small category|small]] [[dense subsite]] [[CartSp]] of [[Cartesian space]]s). (This is discussed in detail at _[[principal bundle]]_ ).

There is a _differential refinement_ of the [[Lie groupoid]] $\mathbf{B}G$, to the smooth groupoid 

$$
  \mathbf{B}G_{conn}
   :=
  SmoothGrpd(\mathbf{P}_1(-), \mathbf{B}G)
  \,,
$$ 

where $\mathbf{P}_1(X)$ is the [[path groupoid]] of $X$. This is the [[(2,1)-sheaf]] given by the 
[[(∞,1)-sheafification|(2,1)-sheafification]] of the assignment that sends a [[smooth manifold]] $U$ to the [[groupoid of Lie algebra-valued 1-forms]] on $U$.

There is a corresponding [[natural equivalence]]

$$
  SmoothGrpd(X, \mathbf{B}G_{conn}) \simeq G Bund_{conn}(X)
$$

of morphisms into $\mathbf{B}G_{conn}$ with the groupoid of $G$-[[principal bundle]]s with [[connection on a bundle|with connection]] on $X$. (This is described in detail at _[[connection on a bundle]]_ ).

In particular if $G = U(1)$ is the [[circle group]], a morphism $X\to \mathbf{B}U(1)_{conn}$ is a [[circle n-bundle with connection|circle bundle with connection]]. This 

This allows already to consider a simple case of a [[characteristic class]] and its refinement to a [[differential characteristic class]]: 
Let $U$ be the [[unitary group]]. There is a canonical morphism of [[Lie groupoid]]s $\mathbf{c}_1 : \mathbf{B}U \to \mathbf{B}U(1)$ given by the [[determinant]]. This -- or rather its image in [[cohomology]]

$$
  \mathbf{c}_1 : SmoothGrpd(- ,\mathbf{B}U) \to SmoothGrpd(-, \mathbf{B} U(1))
$$

is a smooth representative of the [[characteristic class]] called the _first [[Chern class]]_ . Its differential refinement is the evident morphism

$$
  \hat \mathbf{c}_1 : \mathbf{B}U_{conn} \to \mathbf{B}U(1)_{conn} 
$$

that sends a $\mathfrak{u}$-[[Lie algebra valued 1-form|valued differential form]] to the [[trace]] of its Lie algebra value. Postcomposition with this is the refined [[Chern-Weil homomorphism]]

$$
  \array{
    SmoothGrpd(X, \mathbf{B}U)_{conn} 
      &\stackrel{\hat \mathbf{c}_1}{\to}&
    SmoothGrpd(X, \mathbf{B}U(1)_{conn})
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    U Bund_\nabla(X) &\to& U(1) Bund_\nabla(X)
  }
$$

with values in circle bundles with connection, hence in degree-2 [[ordinary differential cohomology]].


It is this kind of construction on [[Lie groupoid]]s that we now want to generalize to a notion of [[smooth ∞-groupoid]]s, to see that Chern-Simons elements are a means to constructi morphisms akind to the differential first Chern-class $\hat \mathbf{c}_1$.

A general abstract context for [[higher geometry]] equipped with [[differential cohomology]] is a [[cohesive (∞,1)-topos]] $\mathbf{H}$ of [[∞-groupoid]]s equipped with _cohesive structure_ , such as [[Smooth∞Grpd|smooth cohesive structure]].

An example for such is the [[∞-stack]]-analog of the [[stack]]-[[(2,1)-topos]] over [[SmoothMfd]]: the [[(∞,1)-sheaf (∞,1)-topos|∞-stack (∞,1)-topos]] [[Smooth∞Grpd]] $:= \hat Sh_{(\infty,1)}(SmoothMfd)$.

In that context we have for instance all the higher [[delooping]]s of $U(1)$: the <a href="">circle Lie (n+1)-groups</a>

$$
  \mathbf{B}^n U(1) \in Smooth\infty Grpd
  \,.
$$

This is such that the evident generalizations of the above classification statements hold: we have that morphisms $X \to \mathbf{B}^n U(1)$ form an [[n-groupoid]]

$$
  Smooth\infty Grpd(X, \mathbf{B}^n U(1))
   \simeq
  U(1) (n-1)Bund(X)
$$

equivalent to that of [[circle n-bundle with connection|circle n-bundles]]/$(n-1)$-[[bundle gerbe]]s on $X$.

If here $X = \mathbf{B}G$ is again the [[delooping]] of a [[Lie group]], this means that now also the higher [[characteristic class]]es are represented by morphisms

$$
  \mathbf{B}G \to \mathbf{B}^n U(1)
  \,.
$$

For instance for $G = Spin$ the [[spin group]], the first fractional [[Pontryagin class]] has a smooth incarnation given by a morphism of the form

$$
  \frac{1}{2}\mathbf{p}_1 : \mathbf{B} Spin \to \mathbf{B}^3 U(1)
$$

corresponding under the above equivalence to the ordinary [[Chern-Simons circle 3-bundle]] on $\mathbf{B}G$.

Every [[cohesive (∞,1)-topos]] comes canonically and essentially uniquely equipped with <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Structures">all the intrinsic structure</a> that we need for the discussion of a refinement of this to [[differential characteristic class]]es:

There is an  [[adjoint (∞,1)-functor|endo-(∞,1)-adjunction]]

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat}) : Smooth\infty Grpd \to 
  Smooth \infty Grpd
$$

where $\mathbf{\Pi}(X)$ is the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Paths">path ∞-groupoid</a> of a [[smooth ∞-groupoid]] $X$.
A morphism $\mathbf{\Pi}(X) \to \mathbf{B}^n U(1)$ encodes therefore the flat [[higher parallel transport]] of a flat [[circle n-bundle with connection]], and we have that the [[n-groupoid]] of morphisms

$$
  Smooth \infty Grpd(\mathbf{\Pi}(X), \mathbf{B}^n U(1))
  \simeq
  U(1) n Bund_{\nabla_{flat}}(X)
$$

is that of flat [[circle n-bundles with connection]]/ (n-1)-[[connection on a bundle gerbe|bundle gerbes with connection]].

A _trivial_ circle $n$-bundle with connection is equivalently just a globally defined [[differential form|differential n-form]]. Therefore if we define the modified [[adjoint (∞,1)-functor|(∞,1)-adjunction]]

$$
  (\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR})
  : 
   */Smooth\infty Grpd
    \stackrel{\leftarrow}{\to}
   Smooth\infty Grpd
$$

by the [[(∞,1)-pullback]] 

$$
  \mathbf{\flat}_{dR}\mathbf{B}^n U(1) 
  := * \prod_{\mathbf{B}^n U(1)} \mathbf{\flat} \mathbf{B}^n U(1)
$$ 

one finds (discussed in detail <a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#StrucDeRham">here</a>) that morphisms $X \to \mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ correspond to trivial circle bundle with connection, hence to cocycles in [[de Rham cohomology]] of $X$.

This now allows us to construct differential refinements:

one can show (detailed discussion is <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#CurvatureCharacteristics">here</a>) that there are canonical cocycles

$$
  curv : \mathbf{B}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}
$$

in the degree $(n+1)$-[[de Rham cohomology]] of $\mathbf{B}^n U(1)$: the universal [[curvature characteristic form]]s. 

Then for $\mathbf{c} : \mathbf{B}G \to \mathbf{B}^n U(1)$ any smooth [[characteristic class]], the correspodning (unrefined) [[differential characteristic class]] is simply the composite

$$
  \mathbf{c}_{dR} : \mathbf{B}G \stackrel{\mathbf{c}}{\to}
   \mathbf{B}^n U(1)
   \stackrel{curv}{\to}
  \mathbf{\flat}_{dR} \mathbf{B}^{n+1} U(1)
  \,.
$$

The (unrefined) [[∞-Chern-Weil homomorphism]] is postcomposition with this morphism. 

This is finally where the Chern-Simons elements come in:

+-- {: .standout}

Chern-Simons elements are a means to present the composite morphism $\mathbf{c}_{dR}$ of [[smooth ∞-groupoid]]s by an [[∞-anafunctor]].

=--

This presentation we describe in the next section.


(In fact a bit more is true: the serve to present the refinement of $\mathbf{c}_{dR}$ to a morphism $\hat \mathbf{c}$ with values in [[ordinary differential cohomology]]. This we come to further below.)



### Chern-Simons forms

This is where the notion of Chern-Simons elements starts to show up: one finds that there is a presentation of this morphism by a morphism of [[simplicial presheaves]] built as follows: the object $\mathbf{B}^n U(1)$ turns out to be presented by a quotient of the presheaf of [[Kan complex]]es given by

$$
  \mathbf{B}^n U(1)_{diff} : 
  (U \in SmoothMfd, [k] \in \Delta)
   \mapsto
  \left\{
    \array{
      \Omega^\bullet_{si,vert}(U \times \Delta^k)
      &\leftarrow& CE(b^{n-1} \mathbb{R})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet_{si}(U \times \Delta^k)
      &\stackrel{\omega}{\leftarrow}&
      W(b^{n-1} \mathbb{R})
    }
  \right\}
  \,,
$$

where on the right we have the set of horizontal morphisms in [[dgAlg]] that make a [[commuting diagram]] with the canonical vertical morphisms as indicated.

(We may think of a morphism of simplicial presheaves $X \to \mathbf{B}^n U(1)_{diff}$ as a [[circle n-bundle with connection|circle n-bundle]]/$(n-1)$-bundle gerbe equipped with a _[[pseudo-connection]]_ . )


Notice that the bottom morphism here encodes precisely a degree-$n$ [[differential form]] $\omega$ on $U \times \Delta^k$, The morphism $curv$ is then presented by the map that sends such a form to its [[curvature]] $d A$. If the [[pseudo-connection]]s that we are dealing with are genuine connections the [[curvature]] is a basic form down on $U$ and this means diagrammatically means that it forms the [[pasting]] composite

$$
  \array{
    \Omega^\bullet_{si,vert}(U \times \Delta^k)
    &\leftarrow& CE(b^{n-1} \mathbb{R})
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet_{si}(U \times \Delta^k)
    &\stackrel{\omega}{\leftarrow}&
    W(b^{n-1} \mathbb{R})
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)
    &\stackrel{d \omega}{\leftarrow}&
    inv(b^{n-1} \mathbb{R})
  }
  \,.
$$






As the term _Chern-Simons element_ indicates, when composed with [[∞-Lie algebra valued forms]] one obtain [[Chern-Simons forms]]:

As discussed at [[∞-Chern-Weil theory]] (see [[∞-Chern-Weil theory introduction]] for an introduction), a [[connection on an ∞-bundle]] with values in an $\infty$-Lie algebroid $\mathfrak{g}$, together with its [[gauge transformation]]s, is locally -- on a patch $U \in $ [[CartSp]] -- given by a [[truncated|truncation]] of the [[∞-groupoid]] whose [[k-morphism]]s are [[commuting diagram]]s in [[dgAlg]] of the form


\[
  \array{
    \Omega^\bullet(U \times \Delta^k)_{vert}
    &\stackrel{A_{vert}}{\leftarrow}&
    CE(\mathfrak{g})
    &&& transition\;function
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U \times \Delta^k)
    &\stackrel{A}{\leftarrow}&
    W(\mathfrak{g})
    &&&
    connection
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)
    &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(\mathfrak{g})
    &&&
    curvature\;characteristic\;form
  }
  \label{ConnectionDiagram}
  \,.
\]

Given such a connection with values in $\mathfrak{g}$, and given a refinement of an [[∞-Lie algebroid cocycle]] $\mu : \mathfrak{g} \to b^{n-1}\mathbb{R}$ as above, by forming the [[pasting]] composite diagrams \eqref{ConnectionDiagram} and \eqref{TheDiagram}, we obtain the corresponding local data for a $b^{n-1}\mathbb{R}$-valued connection:


\[
  \array{
    \Omega^\bullet(U \times \Delta^k)_{vert}
    &\stackrel{A_{vert}}{\leftarrow}&
    CE(\mathfrak{g})
    &\stackrel{\mu}{\leftarrow}&
    CE(b^{n-1}\mathbb{R})
    &&& characteristic\;class
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U \times \Delta^k)
    &\stackrel{A}{\leftarrow}&
    W(\mathfrak{g})
    &\stackrel{cs}{\leftarrow}&
    W(b^{n-1}\mathbb{R})
    &&&
    Chern-Simons\;form
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)
    &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(\mathfrak{g})
    &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(b^{n-1}\mathbb{R})
    &&&
    curvature\;characteristic\;form
  }
  \label{ChernWeilDiagram}
  \,.
\]

This is the local data of a [[circle n-bundle with connection]]. The connection form itself, appearing in the middle horizontal row

$$
  \Omega^\bullet(U) \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{cs}{\leftarrow}
  W(b^{n-1}\mathbb{R})
  :
  CS(A)
$$

is the [[Chern-Simons form]] of the $\mathfrak{g}$-connection evaluated in the given Chern-Simons element. Its [[curvature]] is the [[curvature characteristic form]] $\langle F_A \rangle$ appearing in the bottom line of the diagram, which is obtained by evaluating the $\mathfrak{g}$-valued [[curvature]] in the given [[invariant polynomial]]. The top row, obtained by evaluating the [[∞-Lie algebroid cocycle]] on the transition functions yields -- after truncation followed by a quotient, see <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#IntegrationOfCocycles">integration of ∞-Lie algebra cocycles</a> -- the [[characteristic class]] that classifies the circle $n$-bundle.

The operation in the bottom row here is at the heart of the [[∞-Chern-Weil homomorphism]]. The joint operation on all rows refines this to [[secondary characteristic classes]]. 

For instance for $\mathfrak{g}$ a [[semisimple Lie algebra]] and $\mu$ the ordinary cocycle in [[Lie algebra cohomology]] in degree 3 or seven, this sends $G$-[[principal bundle]]s with [[connection on a bundle]] to the corresponding [[Chern-Simons circle 3-bundle]] and [[Chern-Simons circle 7-bundle with connection]], respectively.

This is part of the general [[∞-Chern-Weil homomorphism]].

We will see below in diagram \eqref{PhysicsDiagram} yet one incarnation of the transgression diagram, identifying it for the case that $\mathfrak{g}$ is a symplectic $\infty$-Lie algebroid with the triple $\mu =$[[Hamiltonian]], $cs = $[[Lagrangian]], $\langle - \rangle =$ [[symplectic structure]].

### Chern-Simons action functionals

Every Chern-Simons element $cs \in W(\mathfrak{a})$ of degree $d$ on an [[∞-Lie algebroid]] $\mathfrak{a}$ induces an [[action functional]] on the space of [[∞-Lie algebroid valued forms]] on $\mathfrak{a}$ over a $d$-[[dimensional]] [[smooth manifold]] $\Sigma$ 

$$
  S_{cs} : \Omega(\Sigma, \mathfrak{a}) \to \mathbb{R}
$$

given by

$$
  (A,B,C, \cdots) \mapsto \int_\Sigma CS(A,B,C, \cdots)
  \,.
$$

This generalizes the action functional of ordinary [[Chern-Simons theory]] to general Chern-Simons elements. In the [examples](#Examples) below is a list of various [[quantum field theories]] that arise as generalized Chern-Simons theories this way.

For more details see [[schreiber:infinity-Chern-Simons theory]].


## Examples {#Examples}

### On semisimple Lie algebra-- Standard Chern-Simons action functional {#StandardCS}

Let $\mathfrak{g}$ be a [[semisimple Lie algebra]]. For the following computations, choose a [[basis]] $\{t^a\}$ of $\mathfrak{g}^*$ and let $\{r^a\}$ denotes the corresponding degree-shifted basis of $\mathfrak{g}^*[1]$. 

Notice that in terms of this the differential of the CE-algebra is

$$
  d_{CE(\mathfrak{g})} : t^a \mapsto -\frac{1}{2}C^a{}_{b c}t^b \wedge t^c
$$

and that of the Weil algebra

$$
  d_{W(\mathfrak{g})} : t^a \mapsto -\frac{1}{2}C^a{}_{b c}t^b \wedge t^c
  + r^a
$$

and

$$
  d_{W(\mathfrak{g})} : r^a \mapsto  -C^a{}_{b c} t^b \wedge r^c
  \,.
$$

Let $P_{a b} r^a \wedge r^b \in W(\mathfrak{g})$ be the [[Killing form]] invariant polynomial. This being invariant

$$
  d_{W(\mathfrak{g})} P_{a b} r^a \wedge r^b 
  =
  2 P_{a b} C^{a}{}_{d e} t^d \wedge r^e \wedge r^b = 0
$$

is equivalent to the fact that the coefficients

$$
  C_{a b c} := P_{a a'}C^{a'}{}_{b c}
$$

are skew-symmetric in $a$ and $b$, and therefore skew in all three indices.


+-- {: .un_prop}
###### Proposition

A Chern-Simons element for the [[Killing form]] invariant polynomial $ \langle -, - \rangle = P(-,-)$ is

$$
  \begin{aligned}
    cs &=
    P_{a b} t^a \wedge (d_{W(\mathfrak{g})} t^b) 
    + 
    \frac{1}{3} P_{a a'}C^{a'}{}_{b c} t^a \wedge t^b \wedge t^c 
    \\
    & =
    P_{a b} t^a \wedge r^b
    -
    \frac{1}{6} 
    P_{a a'}C^{a'}{}_{b c} t^a \wedge t^b \wedge t^c 
  \end{aligned}
  \,.
$$

In particular the Killing form $\langle -,-\rangle$ is in transgression with the degree 3-cocycle

$$
  \mu = -\frac{1}{6}\langle -,[-,-]\rangle
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

We compute 

$$
  \begin{aligned}
    d_{W(\mathfrak{g})}
    \left(
       P_{a b} t^a \wedge r^b
       +
       \frac{1}{2}P_{a a'}C^{a'}{}_{b c} t^a \wedge t^b \wedge t^c        
    \right)
    & = 
      P_{a b} r^a \wedge r^b
      \\
      & -\frac{1}{2} P_{a b} C^a{}_{d e} t^d \wedge t^e \wedge r^b
      \\
      & + P_{a b} C^b{}_{d e} t^a \wedge t^d \wedge r^e
      \\
      & - \frac{3}{6} 
       P_{a a'}C^{a'}{}_{b c} t^a \wedge t^b \wedge r^c        
      \\
      & =
      P_{a b} r^a \wedge r^b
      \\
      & + \frac{1}{2}C_{a b c} t^a \wedge t^b \wedge r^c
      \\
      & - \frac{1}{2} 
       C_{a b c} t^a \wedge t^b \wedge r^c        
      \\
      & = P_{a b } r^a \wedge r^b
  \end{aligned}
  \,.
$$

=--


Under a [[Lie algebra-valued form]]

$$
  \Omega^\bullet(X) \stackrel{}{\leftarrow} W(\mathfrak{g}) : A
$$

this Chern-Simons element is sent to

$$
  cs(A) = P_{a b} A^a \wedge d A^b + \frac{1}{3} C_{a b c} A^a \wedge A^b \wedge A^c
  \,.
$$

If $\mathfrak{g}$ is a [[matrix Lie algebra]] then the Killing form is the [[trace]] and this is equivalently

$$
  cs(A) = tr(A \wedge d A) + \frac{2}{3} tr(A \wedge A \wedge A)
  \,.
$$

This is a familiar form of the standard [[Chern-Simons form]] in degree 3.

For $\Sigma$ a 3-[[dimensional]] [[smooth manifold]] the corresponding [[action functional]] $S_{CS} : \Omega^1(\Sigma, \mathfrak{g}) \to \mathbb{R}$

$$
  S_{CS} : A \mapsto \int_\Sigma cs(A)
$$

is the standard action functional of [[Chern-Simons theory]].

### Higher CS-forms on semisimple Lie algebras

For $\mu \in CE(\mathfrak{g})$ any higher order cocycle, $CS_\mu(A)$ is the corresponding higher order Chern-Simons form.

#### Action functional for Chern-Simons (super-)gravity

Higher Chern-Simons elements on the [[Poincare Lie algebra]] $\mathfrak{g} = \mathfrak{iso}(d,1)$ or the [[super Poincare Lie algebra]] $\mathfrak{g} = \mathfrak{siso}(d,1)$ yield [[action functional]]s for [[gravity]] and [[supergravity]].

(...)

See ([Zanelli](#Zanelli)).

#### Fractional secondary Pontryagin classes

For instance for $\mu_7$ the 7-cocycle on a [[semisimple Lie algebra]], $CS_{\mu_7}(A)$ is the corresponding Chern-Simons 7-form, corresponding to the second [[Pontryagin class]].

Notice that this we may also think of as a 7-cocycle on the corresponding [[string Lie 2-algebra]]. As such it is the one that classifies the extension to the [[fivebrane Lie 6-algebra]]. The corresponding Chern-Simons 7-form appears as the local conneciton data in the [[Chern-Simons circle 7-bundle with connection]] that obstructions the lift from a [[differential string structure]] to a differential [[fivebrane structure]].


### On strict Lie 2-algebras -- BF-theory action functional {#BF}

+-- {: .un_prop}
###### Proposition

Let $\mathfrak{g} = (\mathfrak{g}_2 \stackrel{\partial}{\to} \mathfrak{g})_1$ be a [[strict Lie 2-algebra]].

Then

* every [[invariant polynomial]] $\langle -\rangle_{\mathfrak{g}_1} \in inv(\mathfrak{g}_1)$ on $\mathfrak{g}_1$ is a Chern-Simons element on $\mathfrak{g}$, restricting to the trivial [[∞-Lie algebra cocycle]];

* for $\mathfrak{g}_1$ a [[semisimple Lie algebra]] and 
  $\langle - \rangle_{\mathfrak{g}_1}$ the [[Killing form]], the corresponding Chern-Simons action functional on [[∞-Lie algebra valued forms]]

  $$
    \Omega^\bullet(X) \stackrel{(A,B)}{\leftarrow}
    W(\mathfrak{g}_2 \to \mathfrak{g}_1)
    \stackrel{(\langle - \rangle_{\mathfrak{g}_1}, d_W \langle - \rangle_{\mathfrak{g}_1} )}{\leftarrow}
    W(b^{n-1} \mathbb{R})
  $$

is the sum of the [[action functional]]s of [[topological Yang-Mills theory]] with [[BF-theory]] with [[cosmological constant]] (in the sense of [[gravity as a BF-theory]]):

$$
  CS_{\langle-\rangle_{\mathfrak{g}_1}}(A,B) 
  = 
  \langle F_A \wedge F_A\rangle_{\mathfrak{g}_1}
  - 
  2\langle F_A \wedge \partial B\rangle_{\mathfrak{g}_1}
  +
  2\langle \partial B \wedge \partial B\rangle_{\mathfrak{g}_1}   
  \,,
$$

where $F_A$ is the ordinary [[curvature]] 2-form of $A$.

=--

This is from ([SSSI](#SSSI-BFtheory)).

+-- {: .proof}
###### Proof

For $\{t_a\}$ a [[basis]] of $\mathfrak{g}_1$ and $\{b_i\}$ a basis of $\mathfrak{g}_2$ we have

$$
  d_{W(\mathfrak{g})} : \sigma t^a \mapsto 
  d_{W(\mathfrak{g}_1)}
  + 
  \partial^a{}_i \sigma b^i
  \,.
$$

Therefore with $\langle -\rangle_{\mathfrak{g}_1} = P_{a_1 \cdots a_n} \sigma r^{a_1} \wedge \cdots \sigma t^{a_n}$ we have

$$
  d_{W(\mathfrak{g})} \langle - \rangle_{\mathfrak{g}_1}
  = 
  n P_{a_1 \cdots a_n}\partial^{a_1}{}_i  \sigma b^{i} \wedge \cdots \sigma t^{a_n}
  \,.
$$

The right hand is a polynomial in the shifted generators of $W(\mathfrak{g})$, and hence an [[invariant polynomial]] on $\mathfrak{g}$. Therefore $\langle - \rangle_{\mathfrak{g}_1}$ is a Chern-Simons element for it. 

Now for $(A,B)$ an [[∞-Lie algebra-valued form]], we have that the 2-form curvature is

$$
  F_{(A,B)}^1 = F_A - \partial B
  \,.
$$

Therefore

$$
  \begin{aligned}
    CS_{\langle -\rangle_{\mathfrak{g}_1}}(A,B)
    & = \langle F_{(A,B)}^1\rangle_{\mathfrak{g}_1}
    \\
    & = 
    \langle F_A \wedge F_A\rangle_{\mathfrak{g}_1}
    - 
    2\langle F_A \wedge \partial B\rangle_{\mathfrak{g}_1}
    +
    2\langle \partial B \wedge \partial B\rangle_{\mathfrak{g}_1}   
  \end{aligned}
  \,.
$$


=--



### On symplectic $\infty$-Lie algebroids -- The AKSZ Lagrangian {#Symplectic}


A [[schreiber:symplectic ∞-Lie algebroid]] / [[n-symplectic manifold]] $(\mathfrak{a}, \omega)$ is a [[∞-Lie algebroid|Lie n-algebroid]] $\mathfrak{a}$ equipped with a binary non-degenerate [[invariant polynomial]] $\omega \in W(\mathfrak{a})$ of degree $n+2$.

The corresponding Chern-Simons elements of $\omega$ are the integrands for the [[action functional]]s of various [[TQFT]] [[sigma-model]]s.

With $\{-,-\} : CE(\mathfrak{a}) \otimes CE(\mathfrak{a}) \to CE(\mathfrak{a})$ the graded [[Poisson bracket]] induced by $\omega$ we have (see [Roytenberg](#Roytenberg)) that there exists a [[∞-Lie algebra cocycle]]  $\mu \in CE(\mathfrak{a})$ such that

$$
  d_{CE(\mathfrak{a})} = \{\mu, -\}
  \,.
$$

So in particular $\mu$ being a cocycle means that 

$$
  d_{CE(\mathfrak{a})} \mu = \{\mu, \mu\} = 0
  \,.
$$

+-- {: .un_prop}
###### Proposition

The cocycle $\mu$ is in transgression with the invariant polynomial $\frac{1}{2}\omega$ via the Chern-Simons element 

$$
  \begin{aligned}
    cs &= \frac{1}{2 (n+2)}\iota_{\epsilon} \omega - \mu
  \end{aligned}
  \,,
$$

where $\epsilon$ is the Euler vector field ([Roytenberg](#Roytenberg)).

=--

Here $\mathbf{d}$ is the shift derivation in the [[Weil algebra]], in that $d_{W(\mathfrak{a})} = d_{CE(\mathfrak{a})} + \mathbf{d}$.

+-- {: .proof}
###### Proof

To safe typing signs, we write as if all functions were even graded. By standard reasoning the computation holds true then also for arbitrary grading.
 
Observe that 

1. on unshifted generators we have

   $$
     (\mathbf{d}x^b) \omega_{a b} \{x^a  , -\} = \mathbf{d}
   $$


1. we have graded commutators 

   * $[\mathbf{d}, \iota_v] = N$ (the degree operator) 

   and 

   * $[d_{CE(\mathfrak{a})}, \iota_v] = -N d_{CE(\mathfrak{a})}\mathbf{d}^{-1}$.

   (as one checks on generators).

Therefore 

$$
  \begin{aligned}
    d_{W(\mathfrak{a})} \frac{1}{2(n+2)}\iota_{v} \omega
    &= 
    [d_{W(\mathfrak{a})}, \iota_{v}] \frac{1}{2(n+2)}\omega
    \\
    & =
    (Id - d_{CE(\mathfrak{a})} \mathbf{d}^{-1} ) \frac{1}{2}\omega
    \\
    & =
    \frac{1}{2}\omega - \omega_{a b} \{\mu, x^a\} \mathbf{d}x^b
    \\
    &= \frac{1}{2} \omega + \mathbf{d}\mu
  \end{aligned}
  \,,
$$

where in the first line we used that by definition of [[invariant polynomial]] $d_{W(\mathfrak{a})} \omega = 0$. Similarly, using that by definition $d_{CE(\mathfrak{a})} \mu = 0$ we have 

$$
  d_{W(\mathfrak{a})} \mu = \mathbf{d}\mu
  \,.
$$

So in total we have

$$
  d_{W(\mathfrak{a})} (\frac{1}{2(n+2)} \iota_\epsilon \omega - \mu)
  =
  \frac{1}{2}\omega
  \,.
$$

=--

+-- {: .remark}
###### Remark

In local coordinates where $\omega = \omega_{a b} \mathbf{d}x^a \wedge \mathbf{d}x^b$ we have 

$$
  cs = \frac{1}{2} \omega_{a b} x^a \wedge \mathbf{d}x^b + \mu
  \,.
$$

The Chern-Simons action functional corresponding to this Chern-Simons element
on $\mathfrak{a}$ is that considered in [[AKSZ theory]]. 

Below we spell out some low-dimensional cases explicitly.

=--

#### Higher phase space ---Hamiltonian and Lagrangian mechanics


The symplectic Lie $n$-algebroid $(\mathfrak{P}, \omega)$ may be thought of as an [[n-symplectic manifold]] that models the [[phase space]] of a physical system. 

This means for $(\mathfrak{g},\langle-\rangle) = (\mathfrak{P}, \omega)$ a symplectic Lie $n$-algebroid, the general diagram \eqref{TheDiagram} exhibiting the transgression between cocycles and invariant polynomials via Chern-Simons elements may be labeled in terms of [[Hamiltonian mechanics]], [[Lagrangian mechanics]] and [[symplectic geometry]] as follows

\[
  \array{
    CE(\mathfrak{P})
    &\stackrel{H}{\leftarrow}&
    CE(b^{n}\mathbb{R})
    &&& Hamiltonian
    \\
    \uparrow && \uparrow
    \\
    W(\mathfrak{P})
    &\stackrel{L}{\leftarrow}&
    W(b^n \mathbb{R})
    &&&
    Lagrangian
    \\
    \uparrow && \uparrow
    \\
    inv(\mathfrak{P})
    &\stackrel{\omega}{\leftarrow}&
    inv(b^n \mathbb{R})
    &&&
    symplectic\;structure
  }
  \label{PhysicsDiagram}
\]


=--


See [[Hamiltonian]], [[Lagrangian]], [[symplectic structure]].

#### On a symplectic manifold -- The topological particle

For $X$ a [[smooth manifold]] we may regard its cotangent bundle
$\mathfrak{a} = T^* X$ as a Lie 0-algebroid and the canonical 2-form 
$\omega \in W(\mathfrak{a}) = \Omega^\bullet(X)$ as a binary invariant 
polynomial in degree 2.

The Chern-Simons element is the canonical 1-form $\alpha$ which in local coordinates is $\alpha = p_i d q^i$.

The corresponding action functional on the line 

$$
  \int_{\mathbb{R}} \gamma^* (p_i\, d q^i)
$$

is the familiar term for the action functional of the particle (missing the kinetic term, which makes it "topological").

#### On a Poisson Lie algebroid -- The Poisson $\sigma$-model

+-- {: .un_prop}
###### Proposition

Let $\mathfrak{a} = \mathfrak{P}(X,\pi)$ by a [[Poisson Lie algebroid]]. This comes with the canonical [[invariant polynomial]] $\omega = \mathbf{d} \partial_i \wedge \mathbf{d} x^i$.

The correspinding [[∞-Lie algebroid cocycle]] is 

$$
  \mu_{\omega} = \pi
$$

and a Chern-Simons element for this is

$$
  cs_\omega = \pi^{i j} \partial_i  \wedge \partial_j 
  + \partial_i \wedge \mathbf{d}x^i
  \,.
$$

For $Sigma$ a 2-[[dimensional]] [[smooth manifold]] the corresponding [[action functional]] on [[∞-Lie algebroid-valued forms]] $S : \Omega^\bullet(X, \mathfrak{P}(X,\pi)) \to \mathbb{R}$ is the actional functional of the [[Poisson sigma-model]]

$$
  S : (X, \eta) \mapsto \int_\Sigma (\eta \wedge d X + \pi(\eta \wedge \eta)
  \,.
$$

=--

+-- {: .proof}
###### Proof

We compute in a local coordinte patch:

$$
  \begin{aligned}
    d_{W(\mathfrak{P}(X,\pi))} (\pi^{i j} \partial_i \wedge \partial_j
   + \partial_i \wedge \mathbf{d} x^i)
    = &
   \mathbf{d}x^k (\partial_k \pi^{i j}) \partial_i \wedge \partial_j
   \\
   & + 2 \pi^{i j} (\mathbf{d}\partial_i) \wedge \partial_j
   \\
   & - (\partial_i \pi^{j k}) \partial_j \wedge \partial_k \wedge 
       \mathbf{d}x^i
   \\
   & +
   (\mathbf{d}\partial_i)\wedge (\mathbf{d} x^i)
   \\
   & + (-)(-) 2\pi^{i j} \partial_i \wedge \mathbf{d}\partial_j
   \\
   = & 
   (\mathbf{d}\partial_i)\wedge (\mathbf{d} x^i)
  \end{aligned}
  \,.
$$

=--

### On higher extensions of the super Poincare Lie algebra -- supergravity

See [[D'Auria-Fre formulation of supergravity]] for the moment.


## Related concepts

* [[∞-Lie algebroid cocycle]]

* **Chern-Simons element**

* [[invariant polynomial]]


## References

A classical references on transgression of forms from the fiber to the base of a [[fiber bundle]] is section 9 of.

* [[Armand Borel]], _Topology of Lie groups and characteristic classes_  Bull. Amer. Math. Soc. Volume 61, Number 5 (1955), 397-432. ([EUCLID](http://projecteuclid.org/euclid.bams/1183520007))
{#Borel}

The general definition of Chern-Simons element on $\infty$-Lie algebras and $\infty$-Lie algebroids is <a href="http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3480v2.pdf#page=21">definition 21</a> in

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _$L_\infty$-connections_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)
{#SSSI}


The examples of the [[BF-theory]] invariant polynomials and Chern-Simons elements are in <a href="http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3480v2.pdf#page=43">prop. 18</a> and <a href="http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3480v2.pdf#page=51">def. 26</a> and the BF-action functional itself is extracted below <a href="http://arxiv.org/PS_cache/arxiv/pdf/0801/0801.3480v2.pdf#page=56">proposition 28</a>.
{#SSSI-BFtheory}

Further discussion is in 

* [[Domenico Fiorenza]], [[Chris Rogers]] [[Urs Schreiber]], _[[schreiber:∞-Chern-Simons theory]]_


A survey of higher Chern-Simons elements and their action functionals as applied to [[gravity]] and [[supergravity]] is in

* Jorge Zanelli, _Lecture notes on Chern-Simons (super-)gravities_ [arXiv:0502193](http://arxiv.org/abs/hep-th/0502193)
{#Zanelli}




[[!redirects Chern-Simons elements]]

[[!redirects generalized Chern-Simons theory]]
[[!redirects generalized Chern-Simons theories]]
[[!redirects ∞-Chern-Simons theory]]