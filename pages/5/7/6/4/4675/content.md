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
  \frac{1}{2} p_1 : \mathcal{B}Spin \to \mathcal{B}^4 \mathbb{Z}
$$ 

in the [[(∞,1)-topos]] $\mathbf{H} = $ [[∞Grpd]] $\simeq$ [[Top]] has a refinement to $\mathbf{H} = $ [[?LieGrpd]] of the form 

$$
  \frac{1}{2}\mathbf{p}_1 : \mathbf{B}Spin \to \mathbf{B}^3 U(1)
$$ 

-- the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth first fractional Pontryagin class</a>.

The induced morphism

$$
  \frac{1}{2}\mathbf{p}_1
  :
  \mathbf{H}(X,\mathbf{B} Spin)
  \stackrel{}{\to}
  \mathbf{H}(X,\mathbf{B}^3 U(1))
$$

sends a [[spin group]]-[[principal bundle]] $P$ to its corresponding [[Chern-Simons circle 3-bundle]] $\frac{1}{2}\mathbf{p}_1(P)$.
 
A choice of trivialization of $\frac{1}{2}p_1(P)$ is a [[string structure]]. The 2-groupoid of smooth string structures is the [[homotopy fiber]] of $\frac{1}{2}\mathbf{p}_1$.

By [[Chern-Weil theory]] this morphism may be further refined to land in [[ordinary differential cohomology]] $\mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))$, classifying [[circle n-bundle with connection|circle 3-bundles with connection]]. The [[2-groupoid]] of **differential string structures** is the homotopy fiber of this refinement

$$
  \frac{1}{2}\hat \mathbf{p}_1
  :
  \mathbf{H}_{conn}(X,\mathbf{B} Spin)
  \stackrel{}{\to}
  \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
$$

Such a differential string structure is represented by a tuple consisting of

* a [[connection on a bundle|connection]] $\nabla$ on a $Spin$-[[principal bundle]];

* a choice of trivial [[circle n-bundle with connection|circle 3-bundle]] with connection $(0, C)$;

* a choice of equivalence $\lambda$ of the [[Chern-Simons circle 3-bundle]] with connection $\frac{1}{2}\hat\mathbf{p}_1(\nabla)$ of $\nabla$ with this chosen 3-bundle

  $$
    \lambda : \frac{1}{2}\hat \mathbf{p}_1(\nabla) \stackrel{\simeq}{\to}
    (0,C)
    \,.
  $$

More generally, one can consider the [[homotopy fiber]]s of $\frac{1}{2}\hat \mathbf{p}_1$ over arbitrary circle 3-bundles with connection. According to the general notion of [[twisted cohomology]], these may be thought of as **twisted differential string structures**, where the twist is the class of cocycle over which one computes the homotopy fiber.


## Definition {#Definition}

Let 

$$
  \frac{1}{2}\hat p_1 : 
  \mathbf{H}_{conn}(-,\mathbf{B}Spin)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^3 U(1))
$$

be the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothFirstFracPontryaginClass">smooth first fractional Pontryagin class</a>.


+-- {: .un_def }
###### Definition

For any $X \in \mathbf{H} :=$ [[nLab:?LieGrpd]], the [[2-groupoid]]  of **differential string-structures** $String_{diff}(X)$ is the [[nLab:homotopy fiber]] of  $\frac{1}{2}\mathbf{p}_1(X)$ over the trivial differential cocycle.

More generally, following the general definition of [[twisted cohomology]] -- the 2-groupoid of **twisted differential string structures** is the [[(∞,1)-pullback]] $String_{diff,tw}(X)$ in

$$
  \array{
    String_{diff,tw}(X) &\to& H_{diff}(X,\mathbf{B}^3 U(1))
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}_{conn}(X,\mathbf{B}Spin)
    &\stackrel{\frac{1}{2}\hat \mathbf{p}_1}{\to}&
    \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
  }
  \,,
$$

where $H_{diff}(X,\mathbf{B}^3 U(1))$ is the set of connected components of $\mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))$ and where the right vertical morphism picks one object in each connected component.

=--

+-- {: .un_remark }
###### Remark

In terms of just the underlying $\infty$-Lie algebra valued local connection data, i.e. before Lie integration as discussed [below](#ChernWeilTheory), this has been considered in ([SSSIII](#SSSIII)).

For the case where the twist is given just by globally defined 3-forms, i.e. by  trivial 2-gerbes with connection, essentially this definition, explicitly modeled on [[bundle 2-gerbe]]s, has been given in ([Waldorf](#Waldorf)).

=--


## In $\infty$-Chern-Weil theory {#ChernWeilTheory}

We discuss here an explicit computation of the homotopy fibers in the [above definition](#Definition) using tools described at [[∞-Chern-Weil theory]]. That is we describe a model for $\frac{1}{2}\mathbf{p}_1$ in terms of [[Lie integration]] of a morphism in [[∞-Lie algebra cohomology]] (following [SSSIII](#SSSIII)).

At [[circle n-bundle with connection]] is described an explicit model for the [[ordinary differential cohomology]] $\mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))$ as the ordinary [[pullback]]

$$
  \array{
    \mathbf{H}_{diff}(C(U), \mathbf{B}^3 U(1))
    &\to&
    H_{dR}^4(X)
    \\
    \downarrow && \downarrow
    \\
    [CartSp^{op}, sSet](C(U), \mathbf{B}^3 U(1)_{diff,simp})
    &\stackrel{curv}{\to}&
    [CartSp^{op}, sSet]((C(U), \mathbf{\flat}_{dR}\mathbf{B}^4 U(1)_{chn})
  }
$$

in the category of [[simplicial presheaves]] over [[CartSp]]. Our strategy is therefore to produce a _fibration_ 

$$
  \hat \mathbf{B}G \to \mathbf{B}^3 U(1)_{diff,simp}
$$

in the projective [[model structure on simplicial presheaves]] that models the morphism $\frac{1}{2}\mathbf{p}_1$, for that allows to compute the [[homotopy pullback]] in questions (as described there) by an ordinary pullback along $[CartSp^{op}, sSet](C(U), \hat \mathbf{B}G) \to [CartSp^{op}, sSet](C(U), \mathbf{B}^3 U(1)_{diff,simp})$.


### The twisted $\mathfrak{string}$-Lie 2-algebra

To that end, we replace the [[Lie algebra]] $\mathfrak{g}$ by an equivalent [[∞-Lie algebra|Lie 3-algebra]] (following [SSSIII](#SSSIII)).

In all of the following we take

* $\mathfrak{g} = \mathfrak{so}$

  the [[special orthogonal Lie algebra]] (the Lie algebra of the [[spin group]]);

* $\langle -,-\rangle \in W(\mathfrak{g})$ is the [[Killing form]] [[invariant polynomial]], regarded as an element of the [[Weil algebra]];

* $\mu = \langle -,[-,-]\rangle \in CE(\mathfrak{g})$ the degree 3 [[Lie algebra cohomology|Lie algebra cocycle]], identified with a morphism

  $$
    CE(\mathfrak{g}) \leftarrow CE(b^2 \mathbb{R}) : \mu
  $$

  of [[Chevalley-Eilenberg algebra]]s; and normalized such that its continuation to a 3-form on $Spin$ is the image in de Rham cohomology of a generator of $H^3(Spin,\mathbb{Z}) \simeq \mathbb{Z}$;

* $cs \in W(\mathfrak{g})$ is a Chern-Simons element interpolating between the two; exhibited by the commuting diagram

  $$
    \array{
       CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}&
       CE(b^2 \mathbb{R})
       \\
       \uparrow && \uparrow
       \\
       W(\mathfrak{g})
       &\stackrel{(cs,\langle -,-\rangle)}{\leftarrow}&
       W(b^2 \mathbb{R})
    }
  $$

* $\mathfrak{g}_\mu := \mathfrak{string}$ the [[string Lie 2-algebra]];

+-- {: .un_def }
###### Definition

Let $(b\mathbb{R} \to \mathfrak{g}_\mu)$ denote the $\infty$-Lie algebra defined by the fact that its [[Chevalley-Eilenberg algebra]] is

$$
  CE(b\mathbb{R} \to \mathfrak{g}_\mu) = 
  (\wedge^\bullet(  \mathfrak{g}^* \oplus \langle b\rangle \oplus \langle k \rangle ), d)
  \,,
$$

with $b$ a generator in degree 2, and $k$ a generator in degree 3, and with differential

$$
  d|_{\mathfrak{g}^*} = [-,-]^*
  \,; 
$$

$$
  d : b \mapsto \mu - k
$$

$$
  d : k \mapsto 0
  \,.
$$

=--


+-- {: .un_remark }
###### Remark

This is a thickening of $\mathfrak{g}$ in that the canonical morphism

$$
  \array{
    CE(b\mathbb{R} \to \mathfrak{g}_\mu) 
    \\
    \uparrow^{\mathrlap{\simeq}}
    \\
    CE(\mathfrak{g})
  }
$$

that is the identity on $\mathfrak{g}^*$ and sends $b$ to $0$ and $c $ to $\mu$ is a weak equivalence. It is adapted to computing the obstructions to string-lifts in that there is a canonical inclusion 

$$
  CE(\hat \mathfrak{g})
  \leftarrow
  CE(b^2 \mathbb{R}) = (\wedge^\bullet(\langle k \rangle), d =0)
$$

which includes the generator $k$.

=--



+-- {: .un_lemma }
###### Lemma

Composition with $CE(\hat \mathfrak{g}) \leftarrow CE(b^2 \mathbb{R})$ induces a fibration

$$
  \array{
    \mathbf{cosk}_3\exp(b\mathbb{R} \to \mathfrak{g}_\mu)
    &\to&
    \mathbf{B}^3 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}G
  }
$$

in $[CartSp^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

A 3-morphism in $\mathbf{cosk}_3 \exp(b\mathbb{R} \to \mathfrak{g}_\mu)$ is a based 3-ball $\phi : \Delta^3 \to G$ together with a 2-form $B \in \Omega^2(D^3)$, all with sitting instants at the boundaries. The morphism sends this to the number 

$$
  \int_{\Delta^3} (\phi^* \langle \theta\wedge [\theta\wedge \theta]\rangle + d B) \;\; \in \mathbb{R}\;\; mod \;\; \mathbb{Z}
  \,,
$$

where $\theta$ is the [[Maurer-Cartan form]] on $Spin$. By the integrality of $\mu = \langle -,[-,-]\rangle$ this is well defined.

Now for

$$
  \array{
     \Lambda[3]^i &\stackrel{(f,B)}{\to} & \mathbf{cosk}_3(\exp(\hat \mathfrak{g}))
     \\
     \downarrow && \downarrow
     \\
     \Delta[3] &\stackrel{c}{\to}& \mathbf{B}^3 U(1)
  }
$$

a lifting problem, with $c \in U(1)$, and $f : \Lambda[3]^i \to D^2 \to G$ a map on the horn, with sitting instants, a lift is given by extending $f$ along a smooth [[retract]] $\pi : D^3 \to D^2$ identifying the upper hemisphere as $\pi^* f : \Delta^3 \to D^3 \to  G $, and extending $B$ to any 2-form $\hat B \in \Omega^2(D^3 )$ such that $\int_{S^2} B = c - \int_{D^3} \pi^*f^*\langle \theta\wedge [\theta\wedge \theta]\rangle$. Such a $B$ can always be found:

pick and 2-form $B_2$ on $D^2$ with sitting instants that matches $B$ at the boundary, then goes smoothly to 0 away from the boundary and becomes non-vanishing $B_2^{inn} \in \Omega^2(U \subset D^2)$ with non-vanishing surface integral in the interior of $D^2$. Together with $B$ this gives a smooth 2-form on $S^2$. By letting this smoothly decay to 0 radially along $D^3$ it can always be extended to $D^3$. By rescaling $B_2^{inn}$ appropriately, any integral value can be obtained. And this construction evidently goes through for $U$-parameterized families of this problem.

All other lifting problems are trivial, hence we have for each $U \in $ [[CartSp]] a [[Kan fibration]], hence a fibration in $[CartSp^{op}, sSet]_{proj}$.


=--

We may now straightforwardly extend this to differential coefficients.

Write $\hat \mathbf{B}G_{diff}$ for the 3-[[coskeleton]] of the simplicial presheaf

$$
  U,[n]
  \mapsto
  \left\{
    \array{
      C^\infty(U)\otimes\Omega^\bullet(\Delta^n)
      &\leftarrow& CE(b\mathbb{R} \to \mathfrak{g}_\mu)
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^n)
      &\leftarrow&
      W(b \mathbb{R} \to \mathfrak{g}_\mu)
    }
  \right\}
$$

according to the definition of <a href="">∞-connections</a>.

The canonical [[pasting]] composite

$$
  \array{
    C^\infty(U)\otimes\Omega^\bullet(\Delta^n)
    &\leftarrow& 
    CE(b\mathbb{R} \to \mathfrak{g}_\mu)
    &\leftarrow&
    CE(b^2 \mathbb{R})
    \\
    \uparrow && \uparrow && \uparrow
    \\
    \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^n)
    &\leftarrow&
    W(b\mathbb{R} \to \mathfrak{g}_\mu)
    &\leftarrow&
    W(b^2 \mathbb{R})
  }
$$

induces a morphism

$$
  \array{
    \hat \mathbf{B}G_{diff}  
    &\to&
    \mathbf{B}^3 U(1)_{diff}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}G
  }
$$

in $[CartSp^{op}, sSet]$.


+-- {: .un_corollary }
###### Corollary

This is again a fibration in $[CartSp^{op}, sSet]_{proj}$

=--

Before reading off the fibers of this morphism [below](#ExplicitCocycles) it shall be useful to reorganize this slightly by passing to an [[isomorphism|isomorphic]] copy of the [[Weil algebra]].

### The Chern-Simons Lie 3-algebra

Notice that the [[Weil algebra]] $W(b\mathbb{R} \to \mathfrak{g}_\mu)$ is given by

* $d t^a = C^a{}_{b c} t^b \wedge t^c + r^a$;

* $d r^a  = - C^a{}_{b c} t^b \wedge r^a$;

* $d b = \mu + c - k$;

* $d c = l - \sigma \mu$;

* $d k = l$ .

+-- {: .un_def }
###### Definition

Define $\tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)$ by

* $d t^a = C^a{}_{b c} t^b \wedge t^c + r^a$;

* $d r^a  = - C^a{}_{b c} t^b \wedge r^a$;

* $d b = cs + c - k$;

* $d c = l - \langle -,-\rangle$;

* $d k = l$ .

=--

This is like the Weil algebra, but where the former has the 3-cocycle $\mu$ this has the Chern-Simons element $cs$. The result is that $d c$ cleanly picks up the [[invariant polynomial]] $\langle - ,-\rangle$.

+-- {: .un_lemma }
###### Lemma

There is an [[isomorphism]]

$$
  W(b\mathbb{R} \to \mathfrak{g}_\mu)
  \to 
  \tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)
$$

that is the identity on all generators except on $c$, where it is given by

$$
  c \mapsto c' + (cs-\mu)
  \,.
$$

=--

+-- {: .un_remark }
###### Remark

That shift $cs-\mu$ is precisely the shift that shifts the curvature characteristic $d_{W(\mathfrak{g})}\mu$ into the shifted copy $\mathfrak{g}^*$ in the Weil algebra, thus making it well-adapted to genuine (as opposed to pseudo-)connections.

=--


### Explicit cocycles {#ExplicitCocycles}

With these observations we can read off the cocycles in $String_{diff,tw}(X)$ from the diagrams of dg-algebras in ([SSSIII](#SSSIII)).

A cocycle representing a twisted differential string structure is on a cover $\{U_i \to X\}$ given by a morphism

$$
  \hat \nabla : C(U) \to \hat \mathbf{B}G_{diff}
$$

in $[CartSp^{op}, sSet]$ subject to various constraints. On patches $U_i$ this is a morphism

$$
  \Omega^\bullet(U_i)
  \leftarrow
  \tilde W(b\mathbb{R}\to \mathfrak{g}_\mu)
  \,.
$$

This, in turn, is in components given of the form

$$
  \left(
    \array{ 
      H_3 =& \nabla B = d B + C_3 - CS(A)
      \\
      d H_3 =& \mathcal{G}_4 - \langle F_A \wedge F_A\rangle
      \\
      d \mathcal{G}_4 =& 0
    }
  \right)
  \;\;\;\;
  \stackrel{
    \array{
       t^a & \mapsto A^a
       \\
       r^a & \mapsto F^a_A
       \\
       b & \mapsto B
       \\
       c & \mapsto \nabla  B
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
       d r^a  =&  - C^a{}_{b c} t^b \wedge r^a
       \\
       d b =& cs + c - k
       \\
       d c =& l - \langle -,-\rangle
       \\
       d k =& l
    }
  \right)
  \,.
$$

The constraint is such that $C_3$ is the local connection 3-form on the [[circle n-bundle with connection|circle 3-bundle with connection]] over which the homotopy-pullback is computed (the _twist_ of the twisted differential string structure) and $\mathcal{G}_4$ and $\mathcal{G}_4$ is its [[curvature]] 4-form. 

In physics this is the curvature data familiar from the [[Green-Schwarz mechanism]]. $C_3$ is the [[supergravity C-field]].

(...)

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

The [[∞-Lie algebra cohomology]]-data for the description of twisted differential string structures in terms of [[∞-Chern-Weil homomorphism]] is in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Twisted differential string and fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(?%2C1)-topos+--+references#SSSIII">web</a>)
{#SSSIII}

The full cocycles are described in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Cocycles for differential characteristic classes_ ([web](http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+%28%E2%88%9E%2C1%29-topos+--+references#FSS))
