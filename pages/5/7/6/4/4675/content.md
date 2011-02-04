+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Where a [[string structure]] is a trivialization of a class in [[integral cohomology]], a _differential string structure_ is the trivialization of this class refined to [[ordinary differential cohomology]]:

the first fractional [[Pontryagin class]] 

$$
  \frac{1}{2} p_1 : B Spin \to B^4 \mathbb{Z}
$$ 

in the [[(∞,1)-topos]] [[∞Grpd]] $\simeq$ [[Top]] has a refinement to $\mathbf{H} = $ [[Smooth∞Grpd]] of the form 

$$
  \frac{1}{2}\mathbf{p}_1 : \mathbf{B}Spin \to \mathbf{B}^3 U(1)
$$ 

-- the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth first fractional Pontryagin class</a>.

The induced morphism on [[cocycle]] [[∞-groupoid]]s

$$
  \frac{1}{2}\mathbf{p}_1
  :
  \mathbf{H}(X,\mathbf{B} Spin)
  \stackrel{}{\to}
  \mathbf{H}(X,\mathbf{B}^3 U(1))
$$

sends a [[spin group]]-[[principal bundle]] $P$ to its corresponding [[Chern-Simons circle 3-bundle]] $\frac{1}{2}\mathbf{p}_1(P)$.
 
A choice of trivialization of $\frac{1}{2}p_1(P)$ is a [[string structure]]. The [[2-groupoid]] of smooth string structures is the [[homotopy fiber]] of $\frac{1}{2}\mathbf{p}_1$ over the trivial [[circle n-bundle with connection|circle 3-bundle]].

By [[Chern-Weil theory in Smooth∞Grpd]] this morphism may be further refined to a [[differential characteristic class]] $\frac{1}{2}\hat \mathbf{p}_1$ that lands in the [[ordinary differential cohomology]] 
$\mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))$, 
classifying [[circle n-bundle with connection|circle 3-bundles with connection]]

$$
  \frac{1}{2}\hat \mathbf{p}_1
  :
  \mathbf{H}_{conn}(X,\mathbf{B} Spin)
  \stackrel{}{\to}
  \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
$$

The [[2-groupoid]] of **differential string structures** is the [[homotopy fiber]] of this refinement $\frac{1}{2}\hat \mathbf{p}_1$ over the [[circle n-bundle with connection|trivial circle 3-bundle with trivial connection]] or more generally over the trivial circle 3-bundles with possibly non-trivial connection

Such a differential string structure over a [[smooth manifold]] $X$ is characterized by a tuple consisting of

1. a [[connection on a bundle|connection]] $\nabla$ on a [[Spin group|Spin]]-[[principal bundle]] on $X$;

1. a choice of trivial [[circle n-bundle with connection|circle 3-bundle]] with connection $(0, C_3)$, hence a differential 3-form $C_3 \in \Omega^3(X)$;

1. a choice of [[equivalence in an (∞,1)-category|equivalence]] $\lambda$ of the [[Chern-Simons circle 3-bundle]] with connection $\frac{1}{2}\hat\mathbf{p}_1(\nabla)$ of $\nabla$ with this chosen 3-bundle

  $$
    \lambda : \frac{1}{2}\hat \mathbf{p}_1(\nabla) \stackrel{\simeq}{\to}
    (0,C_3)
    \,.
  $$

More generally, one can consider the [[homotopy fiber]]s of $\frac{1}{2}\hat \mathbf{p}_1$ over arbitrary circle 3-bundles with connection $\hat \mathcal{G}_4 \in \mathbf{H}_{diff}^4(X, \mathbf{B}^3 U(1))$ and hence replace $(0,C_3)$ in the above with $\hat \mathcal{G}_4$. According to the general notion of [[twisted cohomology]], these may be thought of as **twisted differential string structures**, where the class $[\mathcal{G}_3] \in H^4_{diff}(X)$ is the twist.


## Definition {#Definition}

We will assume that the reader is familiar with basics of the discussion at [[Smooth∞Grpd]]. We often write $\mathbf{H} := Smooth \infty Grpd$ for short.

Let $Spin(n) \in $ [[SmoothMfd]] $\hookrightarrow$ [[Smooth∞Grpd]] be the [[Spin group]], for some $n \in \mathbb{N}$, regarded as a [[Lie group]] and thus canonically as an [[∞-group]] object in [[Smooth∞Grpd]]. We shall notationally suppress the $n$ in the following. Write $\mathbf{B}Spin$ for its [[delooping]] of $Spin$ in [[Smooth∞Grpd]]. (See the discussion <a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#LieGroups">here</a>). 
Let moreover $\mathbf{B}^2 U(1) \in Smooth \infty Grpd$ be the <a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#CircleLienGroup">circle Lie 3-group</a> and $\mathbf{B}^3 U(1)$ its [[delooping]].

At [[Chern-Weil theory in Smooth∞Grpd]] the following statement is proven ([FSS](#FSS)).

+-- {: .un_prop }
###### Proposition

The image under [[Lie integration]] of the canonical [[Lie algebra cohomology|Lie algebra 3-cocycle]]

$$
  \mu = \langle -,[-,-]\rangle : \mathfrak{so} \to b^2 \mathbb{R}
$$

on the [[semisimple Lie algebra]] $\mathfrak{so}$ of the [[Spin group]] -- the [[special orthogonal Lie algebra]] -- is a morphism in [[Smooth∞Grpd]] of the form

$$
  \frac{1}{2} \mathbf{p}_1 : 
  \mathbf{B}Spin
    \to
  \mathbf{B}^3 U(1)
$$

whose image under the <a href="http://nlab.mathforge.org/nlab/show/Euclidean-topological%20infinity-groupoid#GeometricHomotopy">the fundamental ∞-groupoid (∞,1)-functor/ geometric realization</a> $\Pi : Smooth \infty Grpd \to $ [[∞Grpd]] is the ordinary fractional [[Pontryagin class]]

$$
  \frac{1}{2}p_1 : B Spin \to B^4 \mathbb{Z}
$$

in [[Top]]. Moreover, the corresponding <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#ChernWeilTheory">refined differential characteristic class</a> 

$$
  \frac{1}{2}\hat \mathbf{p}_1 : 
  \mathbf{H}_{conn}(-,\mathbf{B}Spin)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^3 U(1))
$$

is in [[cohomology]] the corresponding refined [[Chern-Weil homomorphism]]

$$
  [\frac{1}{2}\hat \mathbf{p}_1] : 
  H^1_{Smooth}(X,Spin) \to H_{diff}^4(X)
$$

with values in [[ordinary differential cohomology]] that corresponds to the [[Killing form]] [[invariant polynomial]] $\langle - , - \rangle $ on $\mathfrak{so}$.


=--

+-- {: .un_def #DifferentialStringStructure}
###### Definition

For any $X \in $ [[Smooth∞Grpd]], the [[2-groupoid]]  of **differential string-structures** on $X$ -- $String_{diff}(X)$ -- is the [[homotopy fiber]] of  $\frac{1}{2}\hat \mathbf{p}_1(X)$ over the trivial differential cocycle.

More generally (see [[twisted cohomology]]) the 2-groupoid of **twisted differential string structures** is the [[(∞,1)-pullback]] $String_{diff,tw}(X)$ in

$$
  \array{
    String_{diff,tw}(X) &\to& H_{diff}^4(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}_{conn}(X,\mathbf{B}Spin)
      &\stackrel{\frac{1}{2}\hat \mathbf{p}_1}{\to}&
    \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
  }
  \,,
$$

where the right vertical morphism is a choice of (any) one point in each [[connected component]] (differential cohomology class) of the [[cocycle]] [[∞-groupoid]] $\mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))$ (the [[homotopy type]] of the [[(∞,1)-pullback]] is independent of this choice).

=--


+-- {: .un_remark }
###### Remark

In terms of local [[∞-Lie algebra valued differential forms]] data this has been considered in ([SSSIII](#SSSIII)), as we shall discuss [below](#ChernWeilTheory).
For the case where the twist is given by globally defined 3-forms, i.e. by  trivial 2-gerbes with connection, essentially this definition, explicitly modeled on [[bundle 2-gerbe]]s, has been given in ([Waldorf](#Waldorf)).

=--


## Construction in terms of $L_\infty$-Cech cocycles 
  {#ChernWeilTheory}

We use the [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-topos]] [[Smooth∞Grpd]] (as described there) by the local [[model structure on simplicial presheaves]] $[CartSp_{smooth}^{op}, sSet]_{proj,loc}$ to give an explicit construction of twisted differential string structures in terms of [[Cech cohomology|Cech]]-cocycles with coefficients in [[∞-Lie algebra valued differential forms]].

Recall the following fact from [[Chern-Weil theory in Smooth∞Grpd]] ([FSS](#FSS)).

+-- {: .un_prop }
###### Proposition

The differential fractional Pontryagin class $\frac{1}{2} \hat \mathbf{p}_1$ is presented in $[CartSp_{smooth}^{op}, sSet]_{proj}$ by the top morphism of simplicial presheaves in

$$
  \array{
    \mathbf{cosk}_3\exp(\mathfrak{so})_{ChW,smp}
     &\stackrel{\exp(\mu, cs)}{\to}&
    \mathbf{B}^3 \mathbb{R}/\mathbb{Z}_{ChW,smp}     
    \\
    \downarrow && \downarrow
    \\
    \mathbf{cosk}_3\exp(\mathfrak{so})_{diff,smp}
     &\stackrel{\exp(\mu, cs)}{\to}&
    \mathbf{B}^3 \mathbb{R}/\mathbb{Z}_{smp} 
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}Spin_{c}
  }
  \,.
$$

=--

Here the middle morphism is the direct [[Lie integration]] of the [[infinity-Lie algebra cohomology|L-∞ algebra cocycle]] while the top morphisms is its restriction to coefficients for [[connection on an ∞-bundle|∞-connections]].

In order to compute the [[homotopy fiber]]s of 
$\frac{1}{2}\hat \mathbf{p}_1$ we now find a [[resolution]] of this morphism $\exp(\mu,cs)$ by a fibration in $[CartSp_{smooth}^{op}, sSet]_{proj}$. By the fact that this is a [[simplicial model category]] then also the hom of any cofibrant object into this morphism, computing the cocycle $\infty$-groupoids, is a fibration, and therefore we obtain the homotopy fibers as the corresponding ordinary fibers.

### Presentation of the differential class by a fibration

In order to factor $\exp(\mu,cs)$ into a weak equivalence followed by a fibration, we start by considering such a factorization before differential refinement, on the underlying characteristic class $\exp(\mu)$.

To that end, we replace the [[Lie algebra]] $\mathfrak{g} = \mathfrak{so}$ by an equivalent but bigger [[∞-Lie algebra|Lie 3-algebra]] (following [SSSIII](#SSSIII)). We need the following notation:

* $\mathfrak{g} = \mathfrak{so}$, the [[special orthogonal Lie algebra]] (the Lie algebra of the [[spin group]]);

* $b^2 \mathbb{R}$ the [[line Lie n-algebra|line Lie 3-algebra]], the single genetator in degee 3 of its [[Chevalley-Eilenberg algebra]] we denote $k \in CE(b^2 \mathbb{R})$, $d k = 0$.

* $\langle -,-\rangle \in W(\mathfrak{g})$ is the [[Killing form]] [[invariant polynomial]], regarded as an element of the [[Weil algebra]] of $\mathfrak{so}$;

* $\mu := \langle -,[-,-]\rangle \in CE(\mathfrak{g})$ the degree 3 [[Lie algebra cohomology|Lie algebra cocycle]], identified with a morphism

  $$
    CE(\mathfrak{g}) \leftarrow CE(b^2 \mathbb{R}) : \mu
  $$

  of [[Chevalley-Eilenberg algebra]]s; and normalized such that its continuation to a 3-form on $Spin$ is the image in 
[[de Rham cohomology]] of $Spin$ of a generator of $H^3(Spin,\mathbb{Z}) \simeq \mathbb{Z}$;

* $cs \in W(\mathfrak{g})$ is a [[Chern-Simons element]] interpolating between the two; characterized by the fact that it fits into the commuting diagram

  $$
    \array{
       CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}&
       CE(b^2 \mathbb{R})
       \\
       \uparrow && \uparrow
       \\
       W(\mathfrak{g})
       &\stackrel{cs}{\leftarrow}&
       W(b^2 \mathbb{R})
       \\
       \uparrow && \uparrow
       \\
       inv(\mathfrak{g}) &\stackrel{\langle-,-\rangle}{\leftarrow}&
       inv(b^2 \mathbb{R})
       & = CE(b^3 \mathbb{R})
    }
  $$

* $\mathfrak{g}_\mu := \mathfrak{string}$ the [[string Lie 2-algebra]].



+-- {: .un_def }
###### Definition

Let $(b\mathbb{R} \to \mathfrak{g}_\mu)$ denote the 
[[L-∞ algebra]] whose [[Chevalley-Eilenberg algebra]] is

$$
  CE(b\mathbb{R} \to \mathfrak{g}_\mu) = 
  (\wedge^\bullet(  \mathfrak{g}^* \oplus \langle b\rangle \oplus \langle k \rangle ), d)
  \,,
$$

with $b$ a generator in degree 2, and $k$ a generator in degree 3, and with differential defined on generators by

$$
  \begin{aligned}
    d|_{\mathfrak{g}^*} & = [-,-]^*
    \\
    d  b & = \mu - k
    \\
    d k & =  0
  \end{aligned}
  \,.
$$

=--

+-- {: .un_prop #FactorizationOfTheCocycle}
###### Observation

The 3-cocycle $ CE(\mathfrak{g}) \stackrel{\mu}{\leftarrow} CE(b^2 \mathbb{R})$ factors as 

$$
  CE(\mathfrak{g})
  \stackrel{(k \mapsto \mu, b \mapsto 0)}{\leftarrow}
  CE(b\mathbb{R} \to \mathfrak{g})
   \stackrel{(k \mapsto k)}{\leftarrow}
  CE(b^2 \mathbb{R})
  :
  \mu
$$

where the morphism on the left is a [[quasi-isomorphism]].


=--

+-- {: .un_observation }
###### Observation

The image under [[Lie integration]] of this factorization

$$
  \exp(\mu) 
  :
   \exp(\mathfrak{g})
   \to 
   \exp(b \mathbb{R} \to \mathfrak{g})
   \to 
   \exp(b^2 \mathbb{R})
$$

is a weak equivalence in the [[model structure on simplicial presheaves]] $[CartSp_{smooth}^{op}, sSet]_{proj}$, followed by a fibration. 

=--

+-- {: .proof}
###### Proof

A $[k]$-cell of $\exp(b \mathbb{R} \to \mathfrak{g}_\mu)$ is identified with a pair consisting of a based [[smooth function]] $f : \Delta^k \to Spin$ and a [[vertical differential form|vertical 2-form]] $B \in \Omega^2_{si,vert}(U \times \Delta^k)$, (both suitably with sitting instants peerpendicular to the boundary of the simplex). Since there is no further condition on the 2-form, it can always be extended from the boundary of the $k$-simplex to the interior (for instance simply by radially rescaling it smoothly to 0). Accordingly the [[simplicial homotopy group]]s of $\exp(b \mathbb{R} \to \mathfrak{g}_\mu)(U)$ are the samee as that of $\exp(\mathfrak{g})(U)$. The morphism between them simply picks the pairs for which $B = 0$ and is hence clearly an isomorphism on homotopy groups. 

A $k$-cell of $\exp(b^2 \mathbb{R})(U)$ is a closed vertical 3-form $K \in \Omega^3_{si,vert}(U \times \Delta^k)$.
The morphism $\exp(b\mathbb{R} \to \mathfrak{g}_\mu) \to \exp(b^2 \mathbb{R})$ sends the pair $(f,B)$ to the 3-form $f^* \langle \theta \wedge [\theta \wedge \theta]\rangle - d B$. 

Again, since there is no further condition on $B$, we can fill all [[horn]]s along this morphism: let $K$ be any vertical 3-form on $U \times \Delta^k$ and $(f|,B|)$ function and form on a [[horn]] $\Lambda^3_i$. We may extend $f$ in any way whatsoever from the horn to the simplex, and then use the [[Poincare lemma]] to solve for $B$ the equation $d B = 
f^*\langle \theta \wedge [\theta \wedge \theta]\rangle - K$.

=--

+-- {: .un_prop }
###### Observation


The [[Weil algebra]] $W(b\mathbb{R} \to \mathfrak{g}_\mu)$ of $(b^2 \mathbb{R} \to \mathfak{g})$ is given on extra shifted generators $\{r^a, ,c, l\}$ by

* $d t^a = C^a{}_{b c} t^b \wedge t^c + r^a$;

* $d r^a  = - C^a{}_{b c} t^b \wedge r^a$;

* $d b = \mu + c - k$;

* $d c = l - \sigma \mu$;

* $d k = l$ .

Let $\tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)$ 
have the same
underlying graded algebra as $W(b\mathbb{R} \to \mathfrak{g}_\mu)$ 
but with the differential modified as follows

* $d t^a = C^a{}_{b c} t^b \wedge t^c + r^a$;

* $d r^a  = - C^a{}_{b c} t^b \wedge r^a$;

* $d b = cs + c - k$;

* $d c = l - \langle -,-\rangle$;

* $d k = l$ .

There is an [[isomorphism]] 

$$
  W(b\mathbb{R} \to \mathfrak{g}_\mu)
  \to 
  \tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)
$$

in [[dgAlg]] that is the identity on all generators except on $c$, where it is given by

$$
  c \mapsto c' + (cs-\mu)
  \,.
$$

=--

+-- {: .un_remark }
###### Remark

Where the formula for the differential of $W(b\mathbb{R}\to \mathfrak{g}_\mu)$ has the 3-cocycle $\mu$ that for $\tilde W(b\mathbb{R}\to \mathfrak{g}_\mu)$ has the [[Chern-Simons element]] $cs$.  The shift by $cs-\mu$ is precisely what shifts the curvature characteristic $d_{W(\mathfrak{g})}\mu$ into the shifted copy $\mathfrak{g}^*$ in the Weil algebra, thus making it well-adapted to genuine (as opposed to pseudo-)connections.

=--




+-- {: .un_prop #PresentationByFibration}
###### Proposition
**(presentation of the differential class by a fibration)**

Under [[Lie integration]] 
the [above factorization](#FactorizationOfTheCocycle)
of the Lie algebra cocycle  
maps to the factorization

$$
  \exp(\mu, cs)
   :
  \mathbf{cosk}_3 \exp(\mathfrak{g})_{ChW} 
   \stackrel{\simeq}{\to} 
  \mathbf{cosk}_3 \exp((b \mathbb{R} \to \mathfrak{g}_\mu))_{ChW}
   \to
  \mathbf{B}^3 U(1)_c
$$

of $\exp(\mu,cs)$ in $[CartSp^{op}, sSet]_{proj}$, where the first morphism is a weak equivalence and the second a fibration.

=--

+-- {: .proof}
###### Proof

We check that the second morphism is a fibration. The only nontrivial [[horn]]-filling condition is in degree 3.

First consider the for the underlying non-differential coefficients, hence for the [[vertical differential form]]s: a 3-cell in $\exp(b\mathbb{R} \to \mathfrak{g}_\mu)$ may be identified with a based 3-ball $\phi : \Delta^3 \to G$ together with a 2-form $B \in \Omega^2(D^n)$, all with sitting instants at the boundaries. Here and in the following we denote by capital letters the differential forms in the image of the dg-algebra generators denoted by the same but lower case letters in the above discussion.

The morphism sends this to the number 

$$
  \int_{\Delta^3} (\phi^* \langle \theta\wedge [\theta\wedge \theta]\rangle + d B) \;\; \in \mathbb{R}\;\; mod \;\; \mathbb{Z}
  \,,
$$

where $\theta$ is the [[Maurer-Cartan form]] on $Spin$. (Recall that by the integrality of $\mu = \langle -,[-,-]\rangle$ this is well defined.)

Now for

$$
  \array{
     \Lambda[3]^i &\stackrel{(f,B)}{\to} & 
      \mathbf{cosk}_3\exp(b \mathbb{R} \to \mathfrak{g})
     \\
     \downarrow && \downarrow
     \\
     \Delta[3] &\stackrel{c}{\to}& \mathbf{B}^3 U(1)_c
  }
$$

a lifting problem, with $c \in U(1)$, and $f : \Lambda[3]^i \to D^2 \to G$ a map on the horn, with sitting instants, a lift is given by extending $f$ along a smooth [[retract]] $\pi : D^3 \to D^2$ identifying the upper hemisphere as $\pi^* f : \Delta^3 \to D^3 \to  G $, and extending $B$ to any 2-form $\hat B \in \Omega^2(D^3 )$ such that $\int_{S^2} B = c - \int_{D^3} \pi^*f^*\langle \theta\wedge [\theta\wedge \theta]\rangle = c$. Such a $B$ can always be found:

pick any 2-form $B_2$ on $D^2$ with sitting instants that matches $B$ at the boundary and then goes smoothly to 0 away from the boundary and becomes non-vanishing $B_2^{inn} \in \Omega^2(U \subset D^2)$ with non-vanishing surface integral in the interior of $D^2$. Together with $B$ this gives a smooth 2-form on $S^2$. By letting this smoothly decay to 0 radially along $D^3$ it can always be extended to $D^3$. By rescaling $B_2^{inn}$ appropriately, any integral value can be obtained. And this construction evidently goes through for $U$-parameterized families of this problem.

To get a full lift to the differential coefficients we need to extend this construction from vertical forms to connection forms.

Given the above, $B$ and $CS(A)$ are fixed on $U \times D^3$ and $K$ is fixed by the extension problem. Then the equation $d B = CS + C - K$ induced by the differential in  $\tilde W(b\mathbb{R}\to \mathfrak{g}_\mu)$ may be uniquely solved for $C$ over all of $D^3$. By the very nature of the differential in $\tilde W(b\mathbb{R}\to \mathfrak{g}_\mu)$ its differential is guaranteed to be horizontal: it is

$$
  d C = L - \langle F_A \wedge F_A \rangle
  \,.
$$

The first term $L = d K$ is horizontal because it is so by definition of the extension problem (this is the datum of the 3-cell in $\exp(b^2 \mathbb{R})_{ChW}(U)$). The second term is the pullback along the chosen [[retract]]ion $D^3 \to D^2$ of the Killing form curvature characteristic of the $\mathfrak{g}$-valued form $A$ on $U \times D^2$. Since it is horizontal there by definition, so its its pullback.

=--



### Explicit Cech cocycles {#ExplicitCocycles}

+-- {: .un_cor }
###### Corollary

For any $X \in $ [[SmoothMfd]] $\hookrightarrow$ [[Smooth∞Grpd]], for any choice of differentiaby [[good open cover]] with corresponding cofibrant presentation $\hat X = C(\{C_i\})\in [CartSp_{smooth}^{op}, sSet]_{proj}$ we have that the [[2-groupoid]]s of [twisted different String structures](#DifferentialStringStructure)s are presented by the ordinary [[fiber]]s of the morphism of [[Kan complex]]es

$$
  \exp(\mu,cs)
  :
  [CartSp^{op}, sSet](\hat X, \mathbf{cosk}_3 \exp(b \mathbb{R} 
   \to \mathfrak{g}_\mu)_{ChW})
  \to 
  [CartSp^{op}, sSet](\hat X, \mathbf{B}^3 U(1)_{ChW})
  \,.
$$

over any basepoints in the connected components of the [[Kan complex]] on the right, which correspond to the elements  
$[\hat \mathbf{C}_3] \in H_{diff}^4(X)$ in the [[ordinary differential cohomology]]  of $X$.

=--

We unwind the explicit expression for a twisted differential string structure under this equivalence.

Any twisting cocycle is in the above presentation given by a [[Cech cohomology|Cech]] [[Deligne cohomology|Deligne]]-cocycle (as discussed at [[circle n-bundle with connection]])

$$
  \hat \mathbf{C}_3 = ((C_3)_i, \cdots) 
$$

with local connection 3-form $(C_3)_i \in \Omega^3(U_i)$ and globally defined [[curvature]] 4-form $\mathcal{G}_4 \in \Omega^4(X)$.

A differential string structure on $X$ twisted by this cocycles is on patches $U_i$ a morphism

$$
  \Omega^\bullet(U_i)
  \leftarrow
  \tilde W(b\mathbb{R}\to \mathfrak{g}_\mu)
$$

in [[dgAlg]], subject to some horizontality constraints.
The components of this are over each $U_i$ a collection of differential forms of the following structure

$$
  \left(
    \array{ 
      F_A =& d A + [A\wedge A]
      \\
      H_3 =& \nabla B = d B + C_3 - CS(A)
      \\
      d F_A =& - [A \wedge F_A]
      \\
      d H_3 =& \mathcal{G}_4 - \langle F_A \wedge F_A\rangle
      \\
      d \mathcal{G}_4 =& 0
    }
  \right)_i
  \;\;\;\;
  \stackrel{
    \array{
       t^a & \mapsto A^a
       \\
       r^a & \mapsto F^a_A
       \\
       b & \mapsto B
       \\
       c & \mapsto H_3
       \\
       k & \mapsto C_3
       \\
       l & \mapsto \mathcal{G}_4
    }
  }{\leftarrow}|
  \;\;\;\;
  \left(
    \array{  
       t^a =& C^a{}_{b c} t^b \wedge t^c + r^a
       \\
       c = & d b - cs + k     
       \\
       d r^a  =&  - C^a{}_{b c} t^b \wedge r^a
       \\
       d c =& l - \langle -,-\rangle
       \\
       d k =& l
    }
  \right)
  \,.
$$

Here we are indicating on the right the generators and their relation in $\tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)$ and on the left their images and the images of the relations in $\Omega^\bullet(U_i)$.   This are first the definitions of the [[curvature]]s themselves and then the [[Bianchi identities]] satisfied by these.

### The Green-Schwarz mechanism in heterotic supergravity

Local differential form data as above is known in [[higher category theory and physics|theoretical physics]] in the context of the [[Green-Schwarz mechanism]] for 10-dimensional [[supergravity]].

In this context 

* $A$ is called the [[spin connection]]; 

* $\hat \mathbf{C}_3$ is called the [[supergravity C-field]] 

* the components $((H_3)_i, \cdots)$ of the above cocycle are known as the $\hat \mathbf{C}_3$-twisted [[Kalb-Ramond field]].

More discussion of this is in ([SSSIII](#SSSIII)).


## Related concepts

[[Whitehead tower]] of the [[orthogonal group]]

* [[orientation]]

* [[spin structure]]

* [[string structure]],  **differential string structure**

* [[fivebrane structure]], [[differential fivebrane structure]]

## References

A discussion of differential string structures in terms of [[bundle 2-gerbe]]s is given in

* [[Konrad Waldorf]], _String Connections and Chern-Simons Theory_ ([arXiv:0906.0117](http://arxiv.org/abs/0906.0117))
{#Waldorf}

The local data for the [[∞-Lie algebra valued differential forms]] for the description of twisted differential string structures as above was given in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Twisted differential string and fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(?%2C1)-topos+--+references#SSSIII">web</a>)
{#SSSIII}

The full Cech-Deligne cocycles induced by this (but not yet the homotopy fibers over them) were discussed in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Cocycles for differential characteristic classes_ (
<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+%28%E2%88%9E%2C1%29-topos+--+references#FSS">web</a>)
{#FSS}

A comprehensive discussion is at

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

in section 4.2.

[[!redirects differential string structures]]

[[!redirects differential string-structure]]
[[!redirects differential string-structures]]