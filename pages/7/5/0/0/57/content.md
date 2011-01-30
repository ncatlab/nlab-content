
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Lie integration assigns to a [[Lie algebra]] $\mathfrak{g}$ -- or more generally an [[L-∞-algebra|∞-Lie algebra]] or [[∞-Lie algebroid]] -- a [[Lie group]] -- or more generally [[∞-Lie groupoid]] -- that is [[infinitesimal space|infinitesimally]] modeled by $\mathfrak{g}$.

If the [[∞-Lie algebroid]]s $\mathfrak{a}$ involved are incarnated dually in the form of their [[Chevalley-Eilenberg algebra]]s $CE(\mathfrak{a})$ then the bare [[∞-groupoid]] (that is: without the smooth structure) integrating them is effectively given by the [[Sullivan construction]] from [[rational homotopy theory]] which turns a [[dg-algebra]] into a [[simplicial set]] (and then into a [[topological space]] by [[geometric realization]]) applied here to the [[dg-algebra]] $CE(\mathfrak{a})$.

This construction applied to an ordinary [[Lie algebra]] reproduces the _integration method by paths_ in standard [[Lie theory]] (maybe less widely known than other integration methods). See our first example [below](#LieAlgebrasToLieGroups).

## Definition

Let $\mathfrak{a}$ be an [[∞-Lie algebroid]] (for instance a [[Lie algebra]], or a [[Lie algebroid]] or an [[L-∞-algebra]]). 

For $n \in \mathbb{N}$ write $\Delta^n$ for the $n$-[[simplex]] regarded as a [[smooth manifold]] (with boundary and corners).  

For $d \in \mathbb{N}$, a **$d$-path** in the $\infty$-Lie algebroid is a morphism of $\infty$-Lie algebroids

$$
  \Sigma : T \Delta^d_{Diff} \to \mathfrak{a}
$$ 

from the [[tangent Lie algebroid]] $T \Delta^d_{Diff}$ of the standard smooth $d$-simplex to $\mathfrak{a}$.


Dually this a morphism of [[dg-algebra]]

$$
  \Omega^\bullet(\Delta^n) \leftarrow CE(\mathfrak{a}) : \Sigma^*
$$

from the [[Chevalley-Eilenberg algebra]] of $\mathfrak{a}$ to the [[de Rham complex]].



### Integration to a bare $\infty$-groupoid {#IntToBareGrpd}

Here we discuss the bare [[∞-groupoid]]s underlying the [[∞-Lie groupoid]]s to which an [[∞-Lie algebroid]] integrates.

For $\mathfrak{a}$ an $\infty$-Lie algebroid, the $d$-paths in $\mathfrak{a}$ naturally form a [[simplicial set]] 

$$
  \exp(\mathfrak{a})_{bare}
  :=
  \left(
   \cdots    
   Hom(T \Delta^2, \mathfrak{a})
   \stackrel{\t}{\stackrel{\to}{\to}}
   Hom(T \Delta^1, \mathfrak{a})
   \stackrel{\to}{\to}
   Hom(T \Delta^0, \mathfrak{g})
  \right)
$$

which is a [[Kan complex]] under mild technical fine-tuning of the definition of $d$-paths.

Since morphisms of [[∞-Lie algebroid]]s are dually equivalent to [[dg-algebra]] morphisms of their [[Chevalley-Eilenberg algebra]], the above is equivalent to

$$
   \exp(\mathfrak{a})_{bare}
   :=
   (
   \cdots 
   Hom(CE(\mathfrak{a}), \Omega^\bullet(\Delta^2))
   \stackrel{\to}{\stackrel{\to}{\to}}
   Hom(CE(\mathfrak{a}), \Omega^\bullet(\Delta^1))
   \stackrel{\to}{\to}
   Hom(CE(\mathfrak{a}), \Omega^\bullet(\Delta^0))
   )
  \,.
$$

This is (up to fine-tuning of the nature of the differential forms on the simplices) the [[Sullivan construction]] of [[rational homotopy theory]] that tuns a dg-algvebra into a simplicial set, applied to the dg-algebra $CE(\mathfrak{a})$.


+-- {: .un_remarl}
###### Remark
**(spurious homotopy groups)**

For $\mathfrak{a}$ a [[infinity-Lie algebroid|Lie n-algebroid]] (an $n$-[[truncated]] $\infty$-Lie algebroid) this construction will not yield in general an $n$-[[truncated]] [[∞-groupoid]] $\exp(\mathfrak{a})$. 

To see this, consider the example (discussed in detail [below](#LieAlgebrasToLieGroups)) that $\mathfrak{a} = \mathfrak{g}$ is an ordinary [[Lie algebra]]. Then $\exp(\mathfrak{g})_n$ is canonically identified with the set of smooth based maps $\Delta^n \to G$ into the simply connected [[Lie group]] that integrates $\mathfrak{g}$ in ordinary [[Lie theory]]. This means that the simplicial [[homotopy group]]s of $\exp(\mathfrak{g})$ are the topological homotopy groups of $G$, which in general (say for $G$ the [[orthogonal group]] or [[unitary group]]) will be non-trivial in arbitrarily higher degree, even though $\mathfrak{g}$ is just a Lie 1-algebra. This phenomenon is well familiar from [[rational homotopy theory]], where a classical theorem asserts that the rational homotopy groups of $\exp(\mathfrak{g})$ are generated from the generators in a [[minimal Sullivan model]] resolution of $\mathfrak{g}$. 

=--

For the purposes of $\infty$-Lie theory therefore instead one wants to [[truncated|truncate]] $\exp(\mathfrak{g})$ to its $(n+1)$-[[coskeleton]]

$$
  \mathbf{cosk}_{n+1}\exp(\mathfrak{a})_{bare}  
  \,.
$$


This divides out [[k-morphism|n-morphisms]] by $(n+1)$-morphisms and forgets all higher higher nontrivial morphisms, hence all higher homotopy groups.


### Integration to an $\infty$-Lie groupoid {#SmoothIntegration}

We now discuss Lie integration of $\infty$-Lie algebroids to [[∞-Lie groupoid]]s.

For discussing smooth families of $d$-paths we need the following technical notion.

+-- {: .un_defn}
###### Definition

A smooth differential form $\omega$ on $\Delta^k$ is said to have **sitting instants** along the boundary if, for every $r$-face $F$ of $\Delta^k$ there is a [[neighbourhood]] $U_F$ of $F$ in $\Delta^k$ such that $\omega$ restricted to $U$ is constant in the directions perpendicular to the boundary on its value restricted to that boundary.

For any $U \in $ [[CartSp]] a smooth differential form $\omega$ on $U \times\Delta^k$ is said to have sitting instants if for all points $u : * \to U$ the pullback along  $(u, \mathrm{Id}) : \Delta^k \to U \times \Delta^k$ has sitting instants.

Smooth forms with sitting instants clearly form a sub-dg-algebra of all smooth forms. We shall write $\Omega^\bullet(U \times \Delta^k)$ by default for this sub-dg-algebra.

=--

+-- {: .un_remark}
###### Remark

Note that the dimension of the normal direction to the boundary depends on the dimension of the boundary stratum:  there is one perpendicular direction to a codimension-1 face, and $k$ perpendicular directions to a
vertex. 

=--

+-- {: .un_defn}
###### Definition

For $U \in CartSp$, we denote by the symbol 
$\Omega^\bullet(U\times \Delta^k)_{\mathrm{vert}} \subset \Omega^\bullet(U \times \Delta^k)$   the sub-dg-algebra on forms that are [[vertical differential form]]s with respect to the projection
$U \times \Delta^k \to U$.

=--


+-- {: .un_example}
###### Examples

* A smooth 0-form (a smooth function) has sitting instants on $\Delta^1$ if in a neighbourhood of the endpoints it is constant.

  A smooth function $f : U \times \Delta^1 \to \mathbb{R}$ is in $\Omega^0_{\mathrm{vert}}(U \times \Delta^1)$ if for each $u \in U$ it is constant in a neighbourhood of the endpoints of $\Delta^1$.

* A smooth 1-form has sitting instants on $\Delta^1$ if in a neighbourhood of the endpoints it vanishes.


* Let $X$ be a [[smooth manifold]], $\omega \in \Omega^\bullet(X)$ be a smooth differential form. Let 

  $$
    \phi : \Delta^n \to X
  $$

  be a [[smooth function]] that has [[sitting instant]]s as a function: towards any $k$-face of $\Delta^n$ it eventually becomes perpendicularly constant.

  Then the pullback form $\phi^* \omega \in \Omega^\bullet(\Delta^n)$ is a form with sitting instants.

=--

+-- {: .un_remark}
###### Remark

The condition of sitting instants serves to make smooth differential forms not be affected by the boundaries and corners of $\Delta^n$. Notably for $\omega_j \in \Omega^\bullet(\Delta^{n-1})$ a collection of forms with sitting instants on the $(n-1)$-cells of a horn $\Lambda^n_i$ that coincide on adjacent boundaries, and for

$$
  p : \Delta^n \to \Lambda^{n-1}_i
$$

a standard piecewise smooth [[retract]]s, the pullbacks

$$
  p^* \omega_i 
$$

glue to a single smooth form (with sitting instants) on $\Delta^n$.

=--

+-- {: .un_remark}
###### Remark

Notice that $\omega \in \Omega^\bullet(\Delta^n)$ having sitting instants does not imply that there is a neighbourhood of the boundary of $\Delta^n$ on which $\omega$ is entirely constant. It is important for the following constructions that in the vicinity of the boundary $\omega$ is allowed to vary parallel to the boundary, just not perpendicular to it.

=--


For the following definition, we use from the discussion at [[∞-Lie groupoid]] that $\infty$-Lie groupoids may be modeled by [[simplicial presheaves]] on the [[site]] [[CartSp]] $\subset$ [[Diff]].

+-- {: .un_defn}
###### Definition

For $\mathfrak{a}$ an [[∞-Lie algebroid]] define the [[simplicial presheaf]] $\exp(\mathfrak{a}) : CartSp^{op} \to sSet$ by

$$  
  \exp(\mathfrak{a})
  : 
  (U,[n]) \mapsto 
  Hom_{dgAlg}(CE(\mathfrak{a}), \Omega^\bullet(U \times \Delta^n)_{vert})
  \,,
$$

where $U \in $ [[CartSp]] and $[n] \in \Delta$. 

=--

+-- {: .un_remark}
###### Remark

Compared to the integration to bare $\infty$-groupoids [above](#IntToBareGrpd) this definition knows about $U$-parametrized _smooth families_ of $n$-paths in $\mathfrak{a}$.

The bare $\infty$-groupoid is recovered as that of the $\mathbb{R}^0 = *$-parametrized family:

$$
  \exp(\mathfrak{a}) : \mathbb{R}^0 \mapsto \exp(\mathfrak{a})_{bare}
  \,.
$$

=--

+-- {: .un_defn}
###### Definition

Write $\mathbf{cosk}_{n+1} \exp(a)$ for the simplicial presheaf obtained by postcomposing $\exp(\mathfrak{a}) : CartSp^{op} \to sSet$ with the $(n+1)$-[[coskeleton]] [[functor]] $\mathbf{cosk}_{n+1} : sSet \stackrel{tr_n}{\to} sSet_{\leq n+1} \stackrel{cosk_{n+1}}{\to} sSet$.

=--



## Examples

For more on this see (for the moment) <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieIntegrated">Lie integrated ∞-Lie groupoids</a>.


### Interating Lie algebras to Lie groups {#LieAlgebrasToLieGroups}

Let $\mathfrak{g}$ be an ordinary (finite dimensional) [[Lie algebra]].

Standard [[Lie theory]] (see [[Lie's three theorems]]) provides a [[simply connected]] [[Lie group]] $G$ integrating $\mathfrak{g}$.

If we take that standard procedure for granted, then it is easy to see that:


+-- {: .un_prop}
###### Proposition

There is a weak equivalence (in $[CartSp^{op}, sSet]_{proj}$)

$$
  \mathbf{cosk}_2 \exp(\mathfrak{g}) \simeq \mathbf{B}G
  \,,
$$

where on the right we have the [[delooping]] [[Lie groupoid]] of $G$.

=--


This follows from the [[Steenrod-Wockel approximation theorem]] and the following observation.

+-- {: .un_lemma}
###### Lemma

For $X$ a [[simply connected]] [[smooth manifold]] and $x_0 \in X$ a basepoint, there is a canonical [[bijection]]

$$
  \Omega^1_{flat}(X,\mathfrak{g}) \simeq C^\infty_*(X,G)
$$

between the set of [[Lie-algebra valued 1-form]]s on $X$ whose [[curvature]] 2-form vanishes, and the set of [[smooth function]]s $X\to G$ that take $x_0$ to the neutral element $e \in G$.

=--

+-- {: .proof}
###### Proof

The bijection is given as follows. For $A \in \Omega^1_{flat}(X,\mathfrak{g})$ a flat 1-form, the corresponding function $f_A : X \to G$ sends $x \in X$ to the [[parallel transport]] along any path $x_0 \to x$ from the base point to $x$

$$
  f_A : x \mapsto tra_A(x_0 \to x)
  \,.
$$

Because of the assumption that the [[curvature]] 2-form of $A$ vanishes and the assumption that $X$ is [[simply connected]], this assignment is independent of the choice of path.

Conversely, for every such function $f : X \to G$ we recover $A$ as the pullback of the [[Maurer-Cartan form]] on $G$

$$
  A = f^* \theta
  \,.
$$

=--

From this we obtain

+-- {: .proof}
###### Proof of the proposition

The $\infty$-groupoid $\mathbf{cosk}_2 \exp(\mathfrak{g})$ is equivalent to the [[groupoid]] with a single object (no non-trivial 1-form on the point) whose morphisms are equivalence classes of smooth based paths $\Delta^1 \to G$ (with sitting instants), where two of these are taken to be equivalent if there is a smooth [[homotopy]] $D^2 \to G$ (with sitting instant) between them.

Since $G$ is [[simply connected]], these equivalence classes are labeled by the endpoints of these paths, hence are canonically identified with $G$.

=--

We don't need to fall back to classical Lie theory to obtain $G$ in the above argument. A detailed discussion of how to find $G$ with its group structure and smooth structure from $d$-paths in $\mathfrak{g}$ is in ([Crainic](#Crainic)).





### Integrating to line/circle Lie $n$-groups {#IntegrationToLineNGroup}


+-- {: .un_def}
###### Definition

Write $b^n \mathbb{R}$ for the [[L-∞-algebra]] whose [[Chevalley-Eilenberg algebra]] is given by a single generator in degree $(n+1)$ and vanishing differential.


=--


+-- {: .un_prop}
###### Proposition

The [[discrete ∞-groupoid]] underlying $\exp(b^n \mathbb{R})$ is given by the [[Kan complex]] that in degree $k$ has the set of closed differential $n$-forms (with sitting instants) on the $k$-[[simplex]]

$$
  \exp(b^{n} \mathbb{R})_{disc}
  : 
  [k] \mapsto \Omega^n_{closed}(\Delta^k)
$$

=--

+-- {: .un_prop}
###### Proposition

The $\infty$-Lie integration of $b^n \mathbb{R}$ is the <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#CircleLienGroup">circle Lie n-group</a> $\mathbf{B}^n \mathbb{R}$. 

With $\mathbf{B}^n \mathbb{R}_{chn} \in [CartSp_{smooth}^{op}, sSet]$ the standard presentation given under the [[Dold-Kan correspondence]] by the chain complex of sheaves concentrated in degree $n$ on $C^\infty(-, \mathb{R}$ the equivalence is induced by the [[fiber integration]] of differential $n$-forms over the $n$-[[simplex]]:

$$
  \int_{\Delta^\bullet} : 
  \exp(b^n \mathbb{R})
   \stackrel{\simeq}{\to}
  \mathbf{B}^{n+1} \mathbb{R}
  \,.
$$


=--


+-- {: .un_prop}
###### Proposition

The operation of [[integration|integrating]] an $n$-form on the $n$-simplex over the $n$-simplex gives an equivalence

$$
  \int_{\Delta^\bullet} : 
  \mathbf{cosk}_{n+1}\exp(b^n \mathbb{R}) \stackrel{}{\to}
  \mathbf{B}^{n+1}\mathbb{R}
  \,.
$$

=--

+-- {: .proof}
###### Proof


First we observe that the map

$$
  \int_{\Delta^\bullet}
  :
  (\omega \in \Omega^n_{vert,cl}(U \times \Delta^k))
  \mapsto
  \int_{\Delta^k} \omega \in C^\infty(U, \mathbb{R})
$$ 

is a morphism of 
[[simplicial presheaves]] $\exp(b^n \mathbb{R}) \to \mathbf{B}^{n+1}\mathbb{R}$ on [[CartSp]]${}_{smooth}$. Since it goes between presheaves of abelian [[simplicial group]]s by the [[Dold-Kan correspondence]] it is sufficient to check that we have a morphism of [[chain complex]]es of presheaves on the corresponding [[Moore complex|normalized chain complex]]es.

The only nontrivial degree to check is degree $n$. Let $\lambda \in \Omega^{vert,cl}^n(\Delta^{n+1})$. The differential of the normalized chains complex sends this to the signed sum of its restrictions to the $n$-faces of the $(n+1)$-simplex. Followed by the integral over $\Delta^n$ this is the piecewise integral of $\lambda$ over the boundary of the $n$-simplex. Since $\lambda$ has sitting instants, there is $0 \lt \epsilon \in \mathbb{R}$ such that there are no contributions to this integral in an $\esilon$-neighbourhood of the $(n-1)$-faces. Accordingly the integral is equivalently that over the smooth surface inscribed into the $(n+1)$-simplex, as indicated in the following diagram

To prove this we repeatedly use that differential forms with sitting instants on the $n$-simplex may be treated as differential forms on the $n$-[[ball]]. 

<svg width="640" height="480" xmlns="http://www.w3.org/2000/svg">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <g>
  <title>Layer 1</title>
  <path id="svg_1" d="m40,149l281,-2l-138,192l-143,-190z" stroke="#000000" fill="#ffffff"/>
  <ellipse ry="117" rx="127" id="svg_2" cy="248" cx="495" stroke-width="2" stroke="#000000" fill="#5874c9"/>
  <path id="svg_5" d="m64,181l92,124c16.66701,23 38.33299,22 53,0l89,-125c18.33301,-26 16.66699,-33 -26,-33l-185,2c-30.66666,-0.33333 -39.33334,10.33333 -23,32z" stroke="#000000" fill="#558cc6"/>
  <path id="svg_6" d="m90,182c-16,-15.66667 -10,-22.33333 18,-20l152,-1c20,-1.33333 28,7.33333 18,20l-84,114c-6.33333,13 -14.66667,15 -22,0l-82,-113z" stroke="#000000" fill="#ffffff"/>
  <ellipse ry="52" rx="55" id="svg_7" cy="157" cx="61" stroke-dasharray="5,5" stroke="#000000" fill="none"/>
  <ellipse ry="55" rx="60" id="svg_8" cy="159" cx="289" stroke-dasharray="5,5" stroke="#000000" fill="none"/>
  <ellipse ry="46" rx="51" id="svg_9" cy="317" cx="180" stroke-dasharray="5,5" stroke="#000000" fill="none"/>
  <ellipse ry="87" rx="99" id="svg_10" cy="248.00001" cx="496" stroke-dasharray="5,5" stroke="#000000" fill="#ffffff"/>
  <line id="svg_13" y2="160" x2="103" y1="148" x1="103" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_14" y2="160" x2="240" y1="147" x1="241" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_15" y2="161" x2="144" y1="148" x1="144" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_16" y2="159" x2="185" y1="147" x1="185" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_17" y2="184" x2="425" y1="161" x1="407" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_18" y2="165" x2="458" y1="139" x1="446" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_19" y2="160" x2="507" y1="131" x1="507" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_20" y2="172" x2="543" y1="146" x1="556" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_22" y2="193" x2="76" y1="183" x1="90" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_23" y2="219" x2="93" y1="208" x1="108" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_24" y2="257" x2="121" y1="247" x1="135" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_25" y2="295" x2="150" y1="285" x1="164" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_26" y2="256" x2="396" y1="259" x1="368" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_27" y2="297" x2="413" y1="314" x1="391" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_28" y2="323" x2="444" y1="345" x1="427" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_29" y2="333" x2="479" y1="362" x1="473" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_30" y2="295" x2="215" y1="284" x1="201" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_31" y2="271" x2="231" y1="261" x1="218" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_32" y2="236" x2="255" y1="227" x1="243" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_33" y2="198" x2="283" y1="188" x1="271" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_34" y2="348" x2="555" y1="323" x1="542" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_35" y2="311" x2="602" y1="293" x1="580" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_36" y2="260" x2="620" y1="256" x1="594" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_37" y2="210" x2="615" y1="221" x1="590" stroke-width="4" stroke="#ffff00" fill="none"/>
  <path id="svg_39" d="m256,272c16.33334,40.33334 68.66666,63.66666 109,49" stroke-width="4" stroke="#000000" fill="none"/>
  <line id="svg_40" y2="320" x2="362" y1="311" x1="349" stroke-width="4" stroke="#000000" fill="none"/>
  <line id="svg_41" y2="321" x2="363" y1="332" x1="355" stroke-width="4" stroke="#000000" fill="none"/>
 </g>
</svg>

Since $\lambda$ is a closed form on the $n$-simplex, this surface integral vanishes, by the [[Stokes theorem]]. Hence $\int_{\Delta^\bullet}$ is indeed a chain map.

It remains to show that $\int_{\Delta^\bullet} : \mathbf{cosk}_{n+1} \exp(b^n \mathbb{R}) \to \mathbf{B}^{n+1}\mathbb{R}_{chn}$ is an isomorphism on the [[simplicial homotopy]] group in degree $n$ (for each $U \in CartSp$). This amounts to the statement that a closed $n$-form with sitting instants on the boundary of $\Delta^{n+1}$ may be extended to a closed form on $\Delta^n$ precisely if its integral over the boundary vanishes.

To demonstrate this, we want to work with forms on the $(n+1)$-[[ball]] insteas of the $(n+1)$-simplex. To achieve this, choose again $0 \lt \epsilon \in \mathbb{R}$ and construct the [[diffeomorphism|diffeomorphic]] image of $S^n \times [1,1-\epsilon]$ inside the $(n+1)$-simplex as indicated in the above diagram: outside an $\epsilon$-neighbourhood of the corners the image is a rectangular $\epsilon$-thickening of the faces of the simplex. Inside the $\epsilon$-neighbourhoods of the corners it bends smoothly. By the [[Steenrod-Wockel approximation theorem]] the diffeomorphism from this $\epsilon$-thickening of the smoothed boundary of the simplex to $S^n \times [0,1]$ extends to a smooth function from the $(n+1)$-simplex to the $(n+1)$-ball. 

By choosing epsilon smaller than each of the sitting instants of the given $n$-form, we have that this $n$-form vanishes on the $\epsilon$-neighbourhoods of the corners and is hence entirely determined by its restriction to the smoothed simplex, identified with the $(n+1)$-ball.

We are now reduced to showing: a smooth $n$-form $\omega \in \Omega^n_{vert,cl}(U \times S^n)$ extends smoothly to a closed $n$-form $\hat \omega \in \Omega^n_{vert,cl}(U \times B^{n+1})$ precisely if its integral vanishes, $\int_{S^n} \omega = 0 \in C^\infty(U, \mathbb{R})$.

We show this by induction on $n$.

For $n = 1$, let $\omega$ be a smooth 1-form on $S^1$ whose integral vanishes and which has sitting instants at least at one point. Let $f : [0,1] \to [0,1]$ be any smoothing function (a smooth non-degreasing surjection that is constant in a neighbourhood of 0 and 1). In terms of standard polar coordinates on the 2-[[ball]] $D^2$, with $\theta = 0$ the point where $A$ has sitting instants, write $A = A_\theta d \theta$ and set

$$
  \hat A := f \wedge A_\theta  d \theta 
    + (\int_0^{\theta} A_\theta(\theta') d \theta') f'(r) d r
  \,.
$$

This is a well defined smooth 1-form on the disk because the integral vanishes for $\theta = 2 \pi$ and in fact in a neighbourhood of that value, due to sitting instant. By construction of $f$ it equals $A$ on the boundary. Moreover, it is closed by construction and clearly depends smoothly also on the parameter in $U \in CartSp$ that we suppressed.

Now assume that the statement has been proven for some $n-1 \geq 1$. Let $B^n$ be a closed $n$-form on $S^n$, which has sitting instants around at least one point and whose integral vanishes. We now construct an $(n-1)$-form $a$ with $d a = B$ and then extend that to the $(n+1)$-ball.

To do so, cut out a little $n$-disk around the point of sitting instants on which $B$ is still constant. Identify the remaining punctured $n$-sphere with the $n$-disk via a [[smooth function]] $h : D^n \to S^n$. The pullback form $h^*B$ has by the [[Poincare lemma]] a form $A$ with $d A = B$. Concretely, in standard polar coordinates on $D^n$ we could take

$$
  A(t,\{\phi_i\}) = \int_{0}^r \iota_{\partial_r} h^*B
  \,.
$$

But we want to pass to a different representative that vanishes on the boundary of $D^n$. For that purpose, observe that the integral of $A$ around $\partial D^n$ vanishes, since by the [[Poincare lemma]] and the assumptions on $B$ we have

$$
  \int_{\partial D^n} A \simeq \int_{D^n} h^* B = \int_{S^n} B = 0
  \,.
$$

Therefore we can invoke the induction hypothesis to find (smoothly) a closed $(n-1)$-form $A'$ which equals $A$ on $\partial \Delta^n$. Then the difference $A - A'$ still has the property that

$$
  d (A-A') = h^*B
$$

but now $(A-A')$ is constantly 0 on $\partial D^n$. Moreover, we claim that at this boundary all its derivatives vanish. This follows with the above formula for $A$ from the fact that $B$ has sitting instants in the image of $\partial D^n$ under $h$ (is constantly 0 there) and that $A'$ by induction hypothesis is radially constant at the boundary.

Due to this it follows that there is a smooth $(n-1)$-form on $S^n$ whose pullback along $h$ is $A-A'$:  the extension of $A-A'$ by 0 to from $D^n \simeq$ the punctured $n$-sphere to the whose $n$-sphere.

Then with the smoothing function $f$ from above define finally the $(n-1)$-form on $S^{n+1}$ given by $\hat a (r, \{\phi_i\})= f(r) \wedge a(\{\phi_i\})$ and $\hat B = d \hat a$. This is an extension of $B$ that we needed to construct.

=--



### Integrating the string Lie 2-algebra to the string Lie 2-group

Let $\mathfrak{string} = mathfrak{g}_\mu$ be the [[string Lie 2-algebra]].

Then $\mathbf{cosk}_3 \exp(\mathfrak{g}_\mu)$ is equivalent to the [[2-groupoid]] $\mathbf{B}String$ 

* with a single object;

* whose morphisms are based paths in $G$;

* whose 2-morphisms are equivalence class of pairs $(\Sigma,c)$, where 

  * $\Sigma : D^2_*  \to D$ is a smooth based map (where we use a [[homeomorphism]] $D^2 \simeq \Delta^2$ which away from the corners is smooth, so that forms with sitting instants there do not see any non-smoothness, and the basepoint of $D^2_*$ is the 0-vertex of $\Delta^2$) 

  * and $c \in U(1)$, and where two such are equivalent if the maps coincides at their boundary and if for any 3-ball $\phi : D^3 \to G$ filling them the labels $c_1, c_2 \in U(1)$ differ by the integral $\int_{D^3} \phi^* \mu(\theta) \;\; mod \;\; \mathbb{Z}$,,

where $\theta$ is the [[Maurer-Cartan form]], $\mu(\theta) = \langle \theta\wedge [\theta \wedge \theta]\rangle $ the 3-form obtained by plugging it into the cocycle.

This is the [[string Lie 2-group]]. It's construction in terms of integration by paths is due to ([Henriques](#Henriques))





## References

The basic idea of identifying the [[Sullivan construction]] applied to [[Chevalley-Eilenberg algebra]]s as Lie integration to bare $\infty$-groupoids appears in

* [[Vladimir Hinich]], _Descent of Deligne groupoids_, Internat. Math. Res. Notices, 5:223&#8211;239, 1997 ([doi](http://dx.doi.org/10.1155/S1073792897000160), [preprint ddg.pdf](http://math.haifa.ac.il/hinich/WEB/mypapers/ddg.pdf))

and for general [[∞-Lie algebra]]s in

* [[Ezra Getzler]], _Lie theory for nilpotent $L_\infty$ algebras_, Annals of Mathematics, 170 (2009), 271&#8211;301 ([math.AT/0404003](http://arxiv.org/abs/math/0404003))

(whose main point is the discussion of a gauge condition applicable for nilpotent $L_\infty$-algebras that cuts down the result of the Sullivan construction to a much smaller but equivalent model) .

This was refined from integration to bare $\infty$-groupoids to an integration to [[internal ∞-groupoid]]s in [[Banach manifold]]s in

* [[André Henriques]], _Integrating $L_\infty$ algebras_, Compos. Math. __144__  (2008), no. 4, 1017--1045 ([doi](http://dx.doi.org/10.1112/S0010437X07003405),[math.AT/0603563](http://arxiv.org/abs/math.AT/0603563))
{#Henriques}

(whose origin possibly preceeds that of Getzler's article).

For general [[∞-Lie algebroid]]s the general idea of the integration process by "$d$-paths" had been indicated in 

* [[Pavol ?evera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv:math.SG/0105080](http://arxiv.org/abs/math.SG/0105080)).

A detailed review of how the traditional Lie integration of [[Lie algebra]]s and [[Lie algebroid]]s to [[Lie group]]s and [[Lie groupoid]]s (including the smooth structure) is reproduced in terms of $d$-pathis is given in

* [[Marius Crainic]], [[Rui Fernandes]], _Integrability of Lie brackets_ ([arXiv:math.DG/0105033](http://arxiv.org/abs/math/0105033))
{#Crainic}

The description of Lie integration with values in [[∞-Lie groupoid]]s regarded as simplicial presheaves on [[CartSp]] is in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Cech cocycles for differential characteristic classes -- An $\infty$-Lie theoretic construction_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#FSS">web</a>).



A characterization of the [[∞-stack]]s obtained by Lie integration as above is in [theorem 5.3](http://www.math.harvard.edu/~lurie/papers/moduli.pdf#page=12) of 

* [[Jacob Lurie]], _[[Moduli Problems and DG-Lie Algebras]]_ , 

The Lie integration- of [[Lie infinity-algebroid representation|Lie algebroid representations]] $\mathfrak{a} \to end(V)$ to morphisms of [[∞-categories]] $A \to Ch_\bullet^\circ$ is discussed in

* [[Camilo Arias Abad]], [[Florian Schätz]], _The $A_\infty$ de Rham theorem and integration of representations up to homotopy_ ([arXiv:1011.4693](http://arxiv.org/abs/1011.4693))

