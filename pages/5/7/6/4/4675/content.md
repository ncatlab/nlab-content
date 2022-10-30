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

1. a choice of trivial [[circle n-bundle with connection|circle 3-bundle]] with connection $(0, H_3)$, hence a differential 3-form $H_3 \in \Omega^3(X)$;

1. a choice of [[equivalence in an (∞,1)-category|equivalence]] $\lambda$ of the [[Chern-Simons circle 3-bundle]] with connection $\frac{1}{2}\hat\mathbf{p}_1(\nabla)$ of $\nabla$ with this chosen 3-bundle

  $$
    \lambda : \frac{1}{2}\hat \mathbf{p}_1(\nabla) \stackrel{\simeq}{\to}
    (0,H_3)
    \,.
  $$

More generally, one can consider the [[homotopy fiber]]s of $\frac{1}{2}\hat \mathbf{p}_1$ over arbitrary circle 3-bundles with connection $\hat \mathcal{G}_4 \in \mathbf{H}_{diff}^4(X, \mathbf{B}^3 U(1))$ and hence replace $(0,H_3)$ in the above with $\hat \mathcal{G}_4$. According to the general notion of [[twisted cohomology]], these may be thought of as **twisted differential string structures**, where the class $[\mathcal{G}_4] \in H^4_{diff}(X)$ is the twist.


## Definition {#Definition}

We will assume that the reader is familiar with basics of the discussion at [[Smooth∞Grpd]]. We often write $\mathbf{H} := Smooth \infty Grpd$ for short.

Let $Spin(n) \in $ [[SmoothMfd]] $\hookrightarrow$ [[Smooth∞Grpd]] be the [[Spin group]], for some $n \in \mathbb{N}$, regarded as a [[Lie group]] and thus canonically as an [[∞-group]] object in [[Smooth∞Grpd]]. We shall notationally suppress the $n$ in the following. Write $\mathbf{B}Spin$ for the [[delooping]] of $Spin$ in [[Smooth∞Grpd]]. (See the discussion <a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#LieGroups">here</a>). 
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
$\frac{1}{2}\hat \mathbf{p}_1$ we now find a [[resolution]] of this morphism $\exp(\mu,cs)$ by a fibration in $[CartSp_{smooth}^{op}, sSet]_{proj}$. By the fact that this is a [[simplicial model category]] then also the hom of any cofibrant object into this morphism, computing the cocycle $\infty$-groupoids, is a fibration, and therefore, by the general discussion at [[homotopy pullback]], we obtain the [[homotopy fiber]]s as the ordinary [[fiber]]s of this fibration.


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
  (\wedge^\bullet(  \mathfrak{g}^* \oplus \langle b\rangle \oplus \langle h \rangle ), d)
  \,,
$$

with $b$ a generator in degree 2, and $h$ a generator in degree 3, and with differential defined on generators by

$$
  \begin{aligned}
    d|_{\mathfrak{g}^*} & = [-,-]^*
    \\
    d  b & = - \mu + h
    \\
    d h & =  0
  \end{aligned}
  \,.
$$

=--

+-- {: .un_prop #FactorizationOfTheCocycle}
###### Observation

The 3-cocycle $ CE(\mathfrak{g}) \stackrel{\mu}{\leftarrow} CE(b^2 \mathbb{R})$ factors as 

$$
  CE(\mathfrak{g})
   \stackrel{(h \mapsto \mu, b \mapsto 0)}{\leftarrow}
  CE(b\mathbb{R} \to \mathfrak{g})
   \stackrel{(h \mapsto h)}{\leftarrow}
  CE(b^2 \mathbb{R})
  :
  \mu
$$

where the morphism on the left (which is the identity when restricted to $\mathfrak{g}^*$ and acts on the new generators as indicated) is a [[quasi-isomorphism]].

=--

+-- {: .un_prop #BareFibration}
###### Proposition

The image under [[Lie integration]] of the above factorization is

$$
  \exp(\mu) 
  :
   \mathbf{cosk}_3\exp(\mathfrak{g})
   \to 
   \mathbf{cosk}_3\exp(b \mathbb{R} \to \mathfrak{g}_\mu)
   \to 
   \mathbf{B}^3 \mathbb{R}/\mathbb{Z}_c
$$

where the first morphism is a weak equivalence followed by a fibration in the [[model structure on simplicial presheaves]] $[CartSp_{smooth}^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

To see that the left morphism is objectwise a [[weak homotopy equivalence]], notice that 
a $[k]$-cell of $\exp(b \mathbb{R} \to \mathfrak{g}_\mu)$ is identified with a pair consisting of a based [[smooth function]] $f : \Delta^k \to Spin$ and a [[vertical differential form|vertical 2-form]] $B \in \Omega^2_{si,vert}(U \times \Delta^k)$, (both suitably with sitting instants perpendicular to the boundary of the simplex). Since there is no further condition on the 2-form, it can always be extended from the boundary of the $k$-simplex to the interior (for instance simply by radially rescaling it smoothly to 0). Accordingly the [[simplicial homotopy group]]s of $\exp(b \mathbb{R} \to \mathfrak{g}_\mu)(U)$ are the same as those of $\exp(\mathfrak{g})(U)$. The morphism between them is the identity in $f$ and picks $B = 0$ and is hence clearly an isomorphism on homotopy groups. 

We turn now to discussing that the second morphism is a fibration. The nontrivial degrees of the lifting problem

$$
  \array{
    \Lambda[k]_i &\to& \exp(b\mathbb{R} 
      &\to&  \mathbf{cosk}_3\mathfrak{g}_\mu)(U)
    \\
    \downarrow && \downarrow
    \\
    \Delta[k] &\to& \mathbf{B}^3 \mathbb{R}/\mathbb{Z}_c(U)
  }
$$

are $k = 3$ and $k = 4$.

Notice that a $3$-cell of $\mathbf{B}^3 \mathbb{R}/ \mathbb{Z}_c(U)$ is a [[smooth function]] $c : U \to \mathbb{R}/\mathbb{Z}$ and 
that the morphism $\exp(b\mathbb{R} \to \mathfrak{g}_\mu) \to \mathbf{B}^3 \mathbb{R}/\mathbb{Z}_c$ sends the pair $(f,B)$ to the [[fiber integration]] $\int_{\Delta^3}(f^* \langle \theta \wedge [\theta \wedge \theta]\rangle + d B)$. 

Given our lifting problem in degree 3,
we have given a function $c : U \to \mathbb{R}/\mathbb{Z}$ and a smooth function (with sitting instants at the subfaces) $U \times \Lambda^3_i \to Spin$ together with a 2-form $B$ on the [[horn]] $U \times \Lambda^3_i$.

By pullback along the standard [[continuous function|continuous]] [[retract]] $\Delta^3 \to \Lambda^3_i$ which is non-smooth only where $f$ has sitting instants,  we can always extend $f$ to a smooth function $f' : U \times \Delta^3 \to Spin$ with the property that $\int_{\Delta^3} (f')^* \langle \theta \wedge [\theta \wedge \theta]\rangle = 0$. (Following the general discussion at [[Lie integration]].)

In order to find a horn filler for the 2-form component, consider any smooth 2-form with sitting instants and non-vanishing integeral on $\Delta^2$, regarded as the missing face of the [[horn]]. By multiplying it with a suitable smooth function on $U$ we can obtain an extension $\tilde B \in \Omega^3_{si,vert}(U \times \partial \Delta^3)$ of $B$ to all of $U \times \partial \Delta^3$ with the property that its integral over $\partial \Delta^3$ is the given $c$. By the [[Stokes theorem]] it remains to extend $\tilde B$ to the interior of $\Delta^3$ in any way, as long as it is smooth and has sitting instants.

To that end, we can find in a similar fashion a smooth $U$-parameterized family of closed 3-forms $H$ with sitting instants on $\Delta^3$, whose integral over $\Delta^3$ equals $c$. Since by sitting instants this 3-form vanishes in a neighbourhood of the boundary, the standard formula for the [[Poincare lemma]] applied to it produces a 2-form $B' \in \Omega^2_{si, vert}(U \times \Delta^3)$ with $d B' = H$ that itself is radially constant at the boundary. By construction the difference $\tilde B - B'|_{\partial \Delta^3}$ has vanishing surface integral. By the discussion at [[Lie integration]] it follows that the difference extends smoothly and with sitting instants to a closed 2-form $\hat B \in \Omega^2_{si,vert}(U \times \Delta^3)$. Therefore the sum 

$$
  B' + \hat B \in \Omega^2_{si,vert}(U \times \Delta^3)
$$

equals $B$ when restricted to $\Lambda^k_i$ and has the property that its integral over $\Delta^3$ equals $c$.
Together with our extension $f'$, this constitutes a pair that solves the lifting problem.

The extension problem in degree 4 amounts to a similar construction: by coskeletalness the condition is that for a given $c : U \to \mathbb{R}/\mathbb{Z}$ and a given vertical 2-form on $U \times \partial \Delta^3$ such that its integral equals $c$, as well as a function $f : U \times \partial \Delta^3 \to Spin$, we can extend the 2-form and the functionalong $U \times \partial \Delta^3 \to U \times \Delta^3$. The latter follows from the fact that $\pi_2 Spin = 0$ which guarantees a continuous filler (with sitting instants), and using the [[Steenrod-Wockel approximation theorem]] to make this smooth. We are left with the problem of extending the 2-form, which is the same problem we discussed above after the choice of $\tilde B$.

=--

We now proceed to extend this factorization to the exponentiated differential coefficients (see [[connection on an ∞-bundle]]).


+-- {: .un_prop }
###### Observation

The [[Weil algebra]] $W(b\mathbb{R} \to \mathfrak{g}_\mu)$ of $(b^2 \mathbb{R} \to \mathfrak{g})$ is given on the extra shifted generators $\{r^a, c, l\}$ by

* $d t^a = C^a{}_{b c} t^b \wedge t^c + r^a$;

* $d r^a  = - C^a{}_{b c} t^b \wedge r^a$;

* $d b = - \mu + h + c$;

* $d c = \sigma \mu - g$;

* $d h = g$ 

(where $\sigma$ is the shift operator extended as a graded derivation, see [[Weil algebra]]).

Let $\tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)$ be the dg-algebra
with the same underlying graded algebra as $W(b\mathbb{R} \to \mathfrak{g}_\mu)$ 
but with the differential modified as follows

* $d t^a = C^a{}_{b c} t^b \wedge t^c + r^a$;

* $d r^a  = - C^a{}_{b c} t^b \wedge r^a$;

* $d b = - cs + h + c$;

* $d c = \langle -,-\rangle - g$;

* $d h = g$ .

There is an [[isomorphism]] 

$$
  W(b\mathbb{R} \to \mathfrak{g}_\mu)
  \to 
  \tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)
$$

in [[dgAlg]] that is the identity on all generators except on $c$, where it is given by

$$
  c \mapsto c + (\mu - cs)
  \,.
$$

=--

+-- {: .un_remark }
###### Remark

Where the formula for the differential of $W(b\mathbb{R}\to \mathfrak{g}_\mu)$ has the 3-cocycle $\mu$ that for $\tilde W(b\mathbb{R}\to \mathfrak{g}_\mu)$ has the [[Chern-Simons element]] $cs$.  The shift by $cs-\mu$ is precisely what shifts the curvature characteristic $d_{W(\mathfrak{g})}\mu$ into the shifted copy $\mathfrak{g}^*$ in the Weil algebra, thus exhibiting the modified $c$ as an [[invariant polynomial]].

=--

We shall in the following write $c$ for the generator of that name in $c \in \tilde W(b\mathbb{R} \to \mathfrak{g}_\mu) \stackrel{\simeq}{\to} \tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)$.

+-- {: .un_corollary }
###### Corollary

The [[invariant polynomial]]s on $(b \mathbb{R} \to \mathfrak{g}_\mu)$ are generated from those of $\mathfrak{g}_\mu$ together with $c$ and $g$.

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
  \mathbf{B}^3 U(1)_{ChW,ch}
$$

of $\exp(\mu,cs)$ in $[CartSp^{op}, sSet]_{proj}$, where the first morphism is a weak equivalence and the second a fibration.

=--

+-- {: .proof}
###### Proof

We discuss that the first morphism is an equivalence. Clearly it is injective on homotopy groups: if a sphere of $A$-data cannot be filled, then also adding the $(B,C,H)$-data does not yield a filler. So we need to check that it is also surjective on homtoopy groups: if the $A$-data can be filled, then also the corresponding $(B,C,H)$-data has a filler. Since $C$ is horizontal it is already extended. We may extend $B$ in any smooth way to $U \times \Delta^k$ (for instance by rescaling it smoothly to zero at the center of the $k$-simplex) and then take th equation $d B = CS(A)+ C  - H$ to define the extension of $H$. Its curvature is then $d CS(A) = \langle F_A \wedge F_A\rangle$ and hence horizontal by the assumption that we already have a filler of $A$-data.

We now check that the second morphism is a fibration. It is itself the composite

$$
  \mathbf{cosk}_{3} \exp(b \mathbb{R} \to \mathfrak{g}_\mu)_{ChW}
  \to 
  \exp(b^2 \mathbb{R})_{ChW}/\mathbb{Z}
  \stackrel{\int_{\Delta^\bullet}}{\to}
  \mathbf{B}^3 \mathbb{R}/\mathbb{Z}_{ChW,ch}
  \,.
$$

Here the second morphism is a degreewise surjection of simplicial abelian groups, hence a degreewise surjection under the [[normalized chain complex]] functor, hence is itself already a projective fibration. Therefore it is sufficient to show that the first morphism here is a fibration.

In degree $k = 0$ to $k = 3$ the lifting problems

$$
  \array{
     \Lambda[k]_i 
       &\to & 
      \exp(b\mathbb{R} \to \mathfrak{g}_{\mu})_{smp,ChW}(U)
      \\
      \downarrow && \downarrow
      \\
      \Delta[k] 
        &\to&
      \exp(b^2 \mathbb{R})_{smp,ChW}/\mathbb{Z}(U)
  }
$$

may all be equivalently reformulated as lifting against a [[cylinder]] $D^k \hookrightarrow D^k \times [0,1]$ by using the sitting instants of all forms.

We have then a 3-form $H \in \Omega^3_{si}(U \times D^{k-1}\times [0,1])$ and differential form data $(A,B,C)$ on $U \times D^{k-1}$ given. We may always extend $A$ along the cylinder direction $[0,1]$ (its vertical part is equivalently a based smooth function to $Spin$ which we may extend constantly). $C$  has to be horizontal so is already constantly extended along the cylinder.

We can then use the kind of formula that proves the [[Poincare lemma]] to extend $B$. Let $\Psi : (D^k \times [0,1]) \times [0,1] \to (D^k  \times [0,1])$ be a smooth contraction. Then while $d(H - CS(A) - C)$ may be non-vaishing, by horizonatlity of their [[curvature characteristic form]]s we still have that $\iota_{\partial_t} \Psi_t^* d(H - CS(A) - C)$ vanishes (since the contraction vanishes).

Therefore the 2-form

$$
  \tilde B := \int_{[0,1]} \iota_{\partial_t} \Psi_t^*(H - CS(A)-C)
$$

satisfies $d \tilde B = (H - CS(A) - C)$. It may howver not coincide with our given $B$ at $t = 0$. But the difference $B - \tilde B|_{t = 0}$ is a closed form on the left boundary of the cylinder. We may find some closed 2-form on the other boundary such that the integral around the boundary vanishes. Then the argument from the proof of the [[Lie integration]] of the [[line Lie n-algebra]] applies and we find an extension $\lambda$ to a closed 2-form on the interior. The sum

$$
  \hat B := \tilde B + \lambda
$$

then still satisfies $d \hat B = H - CS(A) - C$ and it coincides with $B$ on the left boundary.

Notice that here $\tilde B$ indeed has sitting instants: since $H$, $CS(A)$ and $C$ have sitting instants they are constant on their value at the boundary in a neighbourhood perpendicular to the boundary, which means for these 3-forms in the degrees $\leq 3$ that they _vanish_ in a neighbourhood of the boundary, hence that the above integral is towards the boundary over a vanishing integrand.

In degree 4 the nature of the lifting problem 

$$
  \array{
  \Lambda[4]_i &\to& \mathbf{cosk}_3\exp(b\mathbb{R} \to \mathfrak{g}_\mu)(U)
  \\
  \downarrow && \downarrow
  \\
  \Delta[4] &\to& \mathbf{B}^3 \mathbb{R}/\mathbb{Z}_{ChW,ch}
  }
$$

starts out differently, due to the presence of $\mathbf{cosk}_3$, but it then ends up amounting to the same kind of argument:

We have four funtions $U \to \mathbb{R}/\mathbb{Z}$ which we may realize as the [[fiber integration]] of a 3-form $H$ on $U \times (\partial \Delta[4] \setminus \delta_i \Delta[3])$,
and we have a lift to $(A,B,C, H)$-data on $U \times (\partial \Delta[4]\setminus \delta_i(\Delta[3]))$ (the boundary of the 4-simplex minus one of its 3-simplex faces). 

We observe that we can 

* always extend $H$ smoothly to the remaining 3-face such that its [[fiber integration]] there reproduces the signed difference of the four given functions corresponding to the other faces (choose any smooth 3-form with sitting instants and with non-vanishing integral and rescale smoothly);

* fill the $A$-data horizonatlly due to the fact that $\pi_2 (Spin) = 0$. 

* the $C$-form is already horizontal, hence already filled. 

Moreover, by the fact that the 2-form $B$ already is defined on all of $\partial \Delta[4] \setminus \delta_i(\Delta[3])$ its fiber integral over the boundary $\partial \Delta[3]$ coincides with the fiber integral of $H - CS(A) - C$ over $\partial Delta[4] \setminus \delta_i (\Delta[3])$). But by the fact that we have lifted $H$ and the fact that $\mu(A_{vert}) = CS(A)|_{\Delta^3}$ is an integral cocycle, it follows that this equals the fiber integral of $H - CS(A)$ over the remaining face.

Use then as above the vertical Poincare lemma-formula to find $\tilde B$ on $U \times \Delta^3$ with sitting instants that satisfies the equation $d B = H - CS(A) - C$ there. Then extend the closed difference $B - \tilde B|_{0}$ to a closed smooth 2-form on $\Delta^3$. As before, the difference

$$
  \hat B := \tilde B  + \lambda
$$

is an extension of $B$ that constitutes a lift.

=--



### Explicit Cech cocycles {#ExplicitCocycles}

+-- {: .un_prop }
###### Corollary

For any $X \in $ [[SmoothMfd]] $\hookrightarrow$ [[Smooth∞Grpd]], for any choice of differentiaby [[good open cover]] with corresponding cofibrant presentation $\hat X = C(\{C_i\})\in [CartSp_{smooth}^{op}, sSet]_{proj}$ we have that the [[2-groupoid]]s of [twisted different String structures](#DifferentialStringStructure)s are presented by the ordinary [[fiber]]s of the morphism of [[Kan complex]]es

$$
  [CartSp^{op}, sSet](\hat X,\exp(\mu,cs))
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

+-- {: .proof}
###### Proof

Since $[CartSp_{smooth}^{op}, sSet]_{proj}$ is a [[simplicial model category]] the morphism 
$[CartSp^{op}, sSet](\hat X,\exp(\mu,cs))$ 
is a fibration because $\exp(\mu,cs)$ is and $\hat X$ is cofibrant.

It follows from the discussion at [[homotopy pullback]] that the ordinary [[pullback]] of [[simplicial presheaves]]

$$
  \array{
    String_{diff,tw}(X) &\to& H_{diff}^4(X)
    \\
    \downarrow && \downarrow
    \\
    [CartSp^{op}, sSet](\hat X, \mathbf{cosk}_3 \exp(b \mathbb{R} 
     \to \mathfrak{g}_\mu)_{ChW})
    &\to& 
  [CartSp^{op}, sSet](\hat X, \mathbf{B}^3 U(1)_{ChW})
  }
$$

is a presentation for the defining [[(∞,1)-pullback]] for $String_{diff,tw}(X)$, as defined [above](#DifferentialStringStructure).

=--

We unwind the explicit expression for a twisted differential string structure under this equivalence.

Any twisting cocycle is in the above presentation given by a [[Cech cohomology|Cech]] [[Deligne cohomology|Deligne]]-cocycle (as discussed at [[circle n-bundle with connection]])

$$
  \hat \mathbf{H}_3 = ((H_3)_i, \cdots) 
$$

with local connection 3-form $(H_3)_i \in \Omega^3(U_i)$ and globally defined [[curvature]] 4-form $\mathcal{G}_4 \in \Omega^4(X)$.

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
      H_3 =& \nabla B := d B + CS(A) + C_3 
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
       c & \mapsto C_3
       \\
       h & \mapsto H_3
       \\
       g & \mapsto \mathcal{G}_4
    }
  }{\leftarrow}|
  \;\;\;\;
  \left(
    \array{  
       t^a =& C^a{}_{b c} t^b \wedge t^c + r^a
       \\
       h = & d b + cs + c     
       \\
       d r^a  =&  - C^a{}_{b c} t^b \wedge r^a
       \\
       d c =& g - \langle -,-\rangle
       \\
       d h =& g
    }
  \right)
  \,.
$$

Here we are indicating on the right the generators and their relation in $\tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)$ and on the left their images and the images of the relations in $\Omega^\bullet(U_i)$.   This are first the definitions of the [[curvature]]s themselves and then the [[Bianchi identities]] satisfied by these.

### The Green-Schwarz mechanism in heterotic supergravity

Local differential form data as above is known in [[higher category theory and physics|theoretical physics]] in the context of the [[Green-Schwarz mechanism]] for 10-dimensional [[supergravity]].

In this context 

* $A$ is called the [[spin connection]]; 

* $C_3$ is called the [[supergravity C-field]] 

* the components $((H_3)_i, \cdots)$ of the above cocycle are known as the $\hat \mathbf{G}_4$-twisted [[Kalb-Ramond field]].

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