
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _spin structure_ on a [[manifold]] $X$ with an [[orientation]] is a lift $\hat g$ of the classifying map $g : X \to B S O(n)$ of the [[tangent bundle]] through the second step $B Spin(n) \to B S O(n)$ in the [[Whitehead tower]] of $O(n)$.

$$
  \array{
    && B Spin(n)
    \\
    & {}^{\hat g}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}&
    B S O(n)
  }
$$

Spin structures derive their name from the fact that their existence on a space $X$ make the [[quantum anomaly]] for spinning particles propagating on $X$ vanish. See there.

## Definition
 {#Definition}

Let $n \in \mathbb{N}$, write

$$
  \mathbb{Z}_2 \to Spin(n) \to SO(n)
$$

for the [[spin group]] [[group extension]] of the [[special orthogonal group]] in [[dimension]] $n$. (All of the following also applies verbatim for [[Lorentzian signature]]).

+-- {: .num_defn }
###### Definition

Write 

$$
  \widetilde{SO(n)} \coloneqq [\mathbb{Z}_2 \to Spin(n)]
$$ 

for the [[crossed module]] of [[smooth groups]] induced by the [[spin group|spin]] [[group extension]]. Write

$$
  \mathbf{B}\mathbb{Z}_2 \coloneqq [\mathbb{Z}_2 \to 1]
$$

for the [[crossed module]] given by shifting up the [[group of order two]] in degree. Finally write

$$
  \array{
    \widetilde{SO(n)}
    \\
    \downarrow
    \\
    SO(n)
  }
$$

for the canonical morphism of [[crossed modules]] which is the [[terminal object|terminal]] morphism in degree-1 and the defining projection in degree 0, and write

$$
  \tilde{\mathbf{w}}_2
  \;\colon\;
  \widetilde{SO(n)}
  = 
  [\mathbb{Z}_2 \to Spin(n)]
  \longrightarrow
  [\mathbb{Z}_2 \to 1]
  = 
  \mathbf{B}\mathbb{Z}_2
$$

for the canonical morphism of [[crossed modules]] which is the identity in degree 1 and the [[terminal object|terminal]] map in degree 0.

=--

+-- {: .num_prop #SmoothSWMap}
###### Proposition

In the [[span]]/[[zig-zag]]

$$
  \array{
      \widetilde{SO(n)} &\stackrel{\tilde{\mathbf{w}_2}}{\longrightarrow}&
       \mathbf{B}\mathbb{Z}_2
       \\
       \downarrow^{\mathrlap{\simeq}}
       \\
       SO(n)
  }
$$

the left leg is a [[weak equivalence]] of [[smooth groupoids]] (under the identification of [[crossed modules]] with [[strict 2-groups]]). Under [[delooping]] it presents a morphism of [[smooth 2-groupoids]] of the form

$$
  \mathbf{w}_2 \;\colon\; \mathbf{B}SO(n) \longrightarrow \mathbf{B}^2 \mathbb{Z}_2
$$

from the universal [[moduli stack]] of smooth $SO(n)$-[[principal bundles]] to that of $\mathbf{B}\mathbb{Z}_2$-[[principal 2-bundles]] ($\mathbb{Z}_2$-[[bundle gerbes]]). The [[homotopy fiber]] of this map in [[Smooth∞Grpd]] is $\mathbf{B}Spin(n)$, for the [[spin group]] regarded as a [[smooth group]].
Under [[geometric realization of cohesive ∞-groupoids]] ${\vert - \vert} \colon Smooth\infty Grpd \longrightarrow \infty Grpd$ this maps ti the universal [[second Stiefel-Whitney class]]

$$
  {\vert \mathbf{w}_2\vert}
  \simeq
  w_2
  \;\colon\;
  B SO(n) \longrightarrow K(\mathbb{Z}_2,2)
  \,.
$$

=--

This is discussed in ([dcct, section 5.1](#dcct)).

+-- {: .proof}
###### Proof 

One checks that the [[homotopy fiber]] of $\mathbf{w}_2$ in [[Smooth∞Grpd]] is $\mathbf{B}Spin(n)$, for $Spin(n)$ the [[spin group]] regarded as a [[smooth group]], for instance by using the techniques for computing [[homotopy pullbacks]] as discussed there. Moreover, by the general discussion at _[[smooth ∞-groupoid -- structures]]_ this homotopy fiber is preseved under [[geometric realization of cohesive ∞-groupoids]] so that the homotopy fiber of ${\vert \mathbf{w}_2 \vert}$ is the [[classifying space]] $B Spin(n)$. Since $\mathbb{K}(\mathbb{Z}_2,2)$ is [[connected]], this characterizes ${\vert \mathbf{w}_2 \vert}$ as $w_2$.

=--

+-- {: .num_remark #TangentBundleModulatingMap}
###### Remark

Given a [[smooth manifold]] $X$ with an [[orientation]], its oriented [[tangent bundle]] is modulated by a map 

$$
  \tau_X \colon X \longrightarrow \mathbf{B}SO(n)
  \,.
$$

Postcomposition with $\mathbf{w}_2$ from prop. \ref{SmoothSWMap} gives a map in [[Smooth∞Grpd]] of the form

$$
  \mathbf{w}_2(\tau_X)
  \;\colon\;
  X \stackrel{\tau_X}{\longrightarrow}
  \mathbf{B}SO(n)
  \stackrel{\mathbf{w}_2}{\longrightarrow}
  \mathbf{B}^2 \mathbb{Z}_2
  \,.
$$

This modulates a $\mathbf{B}\mathbb{Z}_2$-[[principal 2-bundle]] on $X$, also called a $\mathbb{Z}_2$-[[bundle gerbe]]. By construction (the [[universal property]] of the [[homotopy fiber]]) this is the [[obstruction]] to the existence of a lift $\hat g$ in 

$$
  \array{
    && \mathbf{B} Spin(n)
    \\
    & {}^{\hat g}\nearrow & \downarrow
    \\
    X &\stackrel{\tau_x}{\to}&
    \mathbf{B} S O(n)
    &\stackrel{\mathbf{w}_2}{\longrightarrow}&
    \mathbf{B}^2 \mathbb{Z}_2
  }
  \,.
$$

Such a lift is a choice of _spin structure_ on $X$. Therefore as [[bundle gerbes]], this $\mathbf{w}_2(\tau_X)$ is also called a _[[lifting bundle gerbe]]_.

=--



From the perspective of lifting bundle gerbes, spin structures are discussed in ([Murray-Singer 03](#MurraySinger03)).


+-- {: .num_defn }
###### Definition


For $X$ a [[manifold]], the [[groupoid]]/[[homotopy n-type|homotopy 1-type]] $Spin(X)$ of **spin structures** over $X$ is the [[homotopy fiber]] in [[∞Grpd]] $\simeq$ $L_{whe}$[[Top]]  of the second [[Stiefel-Whitney class]]

$$
  \array{
    Spin(X) &\to& *
    \\
    {}^{\mathllap{\eta}}\downarrow && \downarrow
    \\
    Top(X,B SO) &\stackrel{(w_2)_*}{\to}& Top(X, B^2 \mathbb{Z}_2)
  }
  \,.
$$

Here an [[object]] $s \in Spin(X)$ over an $SO$-[[principal bundle]] $\eta(s)$ on $X$ is called a **spin structure on $\eta(s)$** ($SO$ is the [[special orthogonal group]]).

For $\eta(s)$ the $SO$-principal bundle for which the [[tangent bundle]] $T X$ is the canonically [[associated bundle]], one says that a spin-structure on $\eta(s)$ is a **spin structure on the manifold** $X$.

=--

+-- {: .num_remark }
###### Remark

From the smooth geometric perspective on spin structures of remark \ref{TangentBundleModulatingMap} one may also start with an [[affine connection]] on the [[tangent bundle]] given, principally, by an $SO(n)$-[[principal connection]] which in turn is modulated by a map $\nabla$ in

$$
  \array{
     && \mathbf{B} SO(n)_{conn}
     \\
     & {}^{\mathllap{\nabla}}\nearrow &  \downarrow
     \\
     X &\stackrel{\tau_X}{\longrightarrow}& \mathbf{B} SO(n)
  }
  \,.
$$

But since $\mathbb{Z}_2$ is a [[discrete group]], there is no non-flat $\mathbf{B}\mathbb{Z}_2$-[[principal 2-connection]] and hence no non-trivial "differential refinement" of $\mathbf{w}_2$.

Beware that sometimes in the [[physics]] literature an $SO(n)$-[[principal connection]] is already called a "[[spin connection]]" (due to the fact that often in physics only local data is connsidered, and locally there is no difference between $Spin(n)$-principal connections and $SO(n)$-principal connections, up to equivalence.)


=--



## Properties

### Over a Riemann surface
 {#OverARiemannSurface}

Over a [[Riemann surface]] spin structures correspond to [[square roots]] of the [[canonical bundle]]. See at _[[Theta characteristic]]_.

### Over a Hermitian manifold / K&#228;hler manifold
 {#OverAKahlerManifold}

More generally:

+-- {: .num_prop #SpinstructureOnCompactKaehlerIsSquareRootOfCanonical}
###### Proposition

A spin structure on a [[compact topological space|compact]] [[Hermitian manifold]] ([[Kähler manifold]]) $X$ of complex [[dimension]] $n$ exists precisely if, equivalently

* there is a choice of [[square root]] $\sqrt{\Omega^{n,0}}$ of the [[canonical line bundle]] $\Omega^{n,0}$ (a "[[Theta characteristic]]"); 

* there is a trivialization of the [[first Chern class]] $c_1(T X)$ of the [[tangent bundle]].

=--

In this case one has:

+-- {: .num_prop}
###### Proposition

There is a [[natural isomorphism]] 

$$
  S_X \simeq \Omega^{0,\bullet}_X \otimes \sqrt{\Omega^{n,0}_X}
$$ 

of the [[sheaf]] of [[sections]] of the [[spinor bundle]] $S_X$ on $X$ with the [[tensor product]] of the  [[Dolbeault complex]] with the corresponding [[Theta characteristic]];


Moreover, the corresponding [[Dirac operator]] is the [[Dolbeault-Dirac operator]] $\overline{\partial} + \overline{\partial}^\ast$.

=--

This is due to ([Hitchin 74](#Hitchin74)). A textbook account is for instance in ([Friedrich 74, around p. 79 and p. 82](#Friedrich74)).


### As quantum anomaly cancellation condition  {#QuantumAnomaly}

In the context of [[quantum field theory]] the existence of a spin structure on a [[Riemannian manifold]] $X$ arises notably as the condition for [[quantum anomaly]] cancellation of the [[sigma-model]] for the spinning particle -- the superparticle -- propagating on $X$. 

It is the generalization of this anomaly computation from the worldlines of superparticles to super[[string theory|string]]s that leads to [[string structure]], and then further the generalizaton to the worldvolume anomaly of fivebranes that leads to [[fivebrane structure]].

## Examples

### On the 2-sphere
 {#OnThe2Sphere}

The 2-[[sphere]] $S^2$ is famously a [[complex manifold]]: the [[Riemann sphere]]. One standard way to exhibit the complex structure is to cover $S^2$ with two copies of the [[complex plane]] with [[coordinate]] transition functions on the overlap $\mathbb{C} - \{0\}$ given by

$$
  z_2 = z_1^{-1}
  \,.
$$

The 2-sphere is moreover a [[Kähler manifold]] and of course [[compact topological space|compact]]. Therefore by prop. \ref{SpinstructureOnCompactKaehlerIsSquareRootOfCanonical} a spin structure on $S^2$ is equivalently a [[square root]] $\sqrt{\Omega^{1,0}} \in \mathbf{Line}_{\mathbb{C}}(S^2)$ of the [[canonical line bundle]] $\Omega^{1,0}$, which here is simply the holomorphic 1-form bundle.

Now hermitian [[complex line bundles]] on the 2-sphere are classified by $H^2(S^2, \mathbb{Z}) \simeq \mathbb{Z}$. By the [[clutching construction]] a line bundle given by two trivializing sections $\sigma_1, \sigma_2$ of the trivial line bundle on the coordinate patch $\mathbb{C}$ has class the [[winding number]] of the transition function

$$
  S^1 \hookrightarrow \mathbb{C} - \{0\}
  \stackrel{s_2 s_1^{-1}}{\to} \mathbb{C}^\times
  \,.
$$

Now the canonical section of the holomorphic 1-form bundle on $\mathbb{C}$ is simply the canonical 1-form $d z$ itself. By the above [[coordinate charts]] we have on $\mathbb{C} - \{0\}$

$$
  d z_2 = d (z_1^{-1}) = - z_1^{-2} d z_1
$$

and so the transition function of the canonical bundle in this local trivialization is 

$$
  - z^{-2} \colon \mathbb{C}-\{0\} \to \mathbb{C}^\times
  \,.
$$

This has winding number $\pm 2$. Therefore the [[first Chern class]] of the holomorphic 1-form bundle $\Omega^{1,0}$ is $c_1(\Omega^{1,0}) =  \pm 2$ (the sign being an arbitrary convention, determined by the identification $H^2(S^2, \mathbb{Z}) \simeq \mathbb{Z}$).

And so it follows that there is a unique spin structure, namely given by choosing $\sqrt{\Omega^{1,0}}$ to be the line bundle on $S^2$ with first Chern class $\pm 1$. 


To construct $\sqrt{\Omega^{1,0}}$ by local sections analogous to how we got $\Omega^{1,0}$ from the two sections $d z_1$ and $d z_2$, slice open $\mathbb{C}$ to $\mathbb{C} - [0,\infty)$ and consider one of the two $z_1^{-1/2} d z_1$ as a local section of the trivial complex line bundle. Do the same on the other patch. Then

$$
  \begin{aligned}
    z_2^{-1/2} d z_2 
    &= 
    z_1^{1/2} (-z_1^{-2} d z_1)
    \\
    &=  -z_1^{-1}\left(z_1^{-1/2} dz_1\right)
  \end{aligned}
  \,.
$$

This is well defined also over the cut and so we can patch the cut with any small neighbourhood with any section chosen over it and conclude that these sections are the local sections locally trivializing a bundle of class $\pm 1$ and hence that of $\sqrt{\Omega^{1,0}}$.

Notice also that the canonical vector field on the first patch given by $z_1 \partial_{z_1}$ transforms on the overlap to

$$
  \begin{aligned}
    z_1 \partial_{z_1}
    &  =
    z_2^{-1} \frac{\partial z_2}{\partial z_1 } \partial_{z_2}    
    \\
    & = z_2^{-1} (- z_1^{-2}) \partial_{z_2}
    \\
    & = - z_2 \partial_{z_2}
  \end{aligned}
$$

and hence continues canonically to a well-defined vector field on all of $S^2$. If $L_k$ is the rank $k$ line bundle on $S^2$ given by the [[clutching construction]] by the transition function $z^k$, then holomorphic sections of this bundle are expressed in terms of canonical bases $z_1^{a_1}$, $z_2^{a_2}$ with $a_i \geq 0$ satisfying

$$
  z_2^{a_2} = z_2^{k} z_2^{-a_1}
$$

and hence for

$$
  a_1 + a_2 = k
  \,.
$$

This gives a $(k+1)$-dimensional space of holomorphic sections.

For more along these lines see also at _[[geometric quantization of the 2-sphere]]_.

### On the $n$-sphere
 {#SpinStructureOnTheNSphere}

Generally:

\begin{example}
The [[n-sphere]], for each $n \in \mathbb{N}$, carries a canonical [[spin structure]], induced from its [[coset space]]-realization $S^n \simeq Spin(n+1)/Spin(n)$ 
([here](sphere#LabelCosetSpaceStructure)), as a special case of the canonical $H$-structure on $G/H$ ([this example](G-structure#CanonicalHStructureOnFModH)).
\end{example}

Other ways to see this:


* {#Nowaczyk15} Nikolai Nowaczyk, Theorem A.6.6 in: _Dirac Eigenvalues of higher Multiplicity_ ([arXiv:1501.04045](https://arxiv.org/abs/1501.04045))

* {#SpinorsInGeometryAndPhysics} _Spinors in Geometry and Physics_ ([GBooks, p. 243](https://books.google.ae/books?id=d14GCwAAQBAJ&lpg=PA243&ots=_tH_He8UFg&dq=%22spin%20structure%20on%20spheres%22&pg=PA243#v=onepage&q=%22spin%20structure%20on%20spheres%22&f=false))


## Higher spin structures
 {#Higher}

Spin structures are one step in a tower of conditions that are related to the [[quantum anomaly]] cancellation of higher dimensional spinning/super [[branes]].

This is controled by the [[Whitehead tower]] of the [[classifying space]]/[[delooping]] of the [[orthogonal group]] $O(n)$, which starts out as

$$
  \array{
    & Whitehead tower
    \\
    &\vdots
    \\
    & B Fivebrane &\to& \cdots &\to& *
    \\
    & \downarrow && && \downarrow
    \\
    second frac Pontr. class & B String &\to& \cdots &\stackrel{\tfrac{1}{6}p_2}{\to}&  B^8 \mathbb{Z}
    &\to& * 
    \\
    & \downarrow && && \downarrow && \downarrow
    \\
    first frac Pontr. class & B Spin && && &\stackrel{\tfrac{1}{2}p_1}{\to}& B^4 \mathbb{Z} &\to & * 
    \\
    & \downarrow && && \downarrow && \downarrow && \downarrow
    \\
    second SW class & B S O 
    &\to&
    \cdots
    &\to&
    &\to&
    & \stackrel{w_2}{\to} &
    B^2 \mathbb{Z}_2
    &\to&
    *
    \\
    & \downarrow && && \downarrow && \downarrow &&  \downarrow && \downarrow
    \\
    first SW class & B O 
    &\to&
    \cdots
    &\to&
    \tau_{\leq 8 } B O
    &\to&
    \tau_{\leq 4 } B O
    &\to&
    \tau_{\leq 2 } B O
    &\stackrel{w_1}{\to}&
    \tau_{\leq 1 } B O
    \simeq
    B \mathbb{Z}_2
    &
    Postnikov  tower
  }
$$


where the stages are the deloopings of

...
$\to$
[[fivebrane group]]
$\to$
[[string group]]
$\to$
[[spin group]]
$\to$
[[special orthogonal group]]
$\to$
[[orthogonal group]],

where lifts through the stages correspond to 

* [[orthogonal structure]]

* [[orientation]]

* [[spin structure]]

* [[string structure]]

* [[fivebrane structure]]

and where the [[obstruction]] classes are the [[universal characteristic classes]]

* [[first Stiefel-Whitney class]] $w_1$

* [[second Stiefel-Whitney class]] $w_2$

* [[Pontryagin class|first fractional Pontryagin class]] $\tfrac{1}{2}p_1$

* [[Pontryagin class|second fractional Pontryagin class]] $\tfrac{1}{6}p_2$

and where every possible square in the above is a [[homotopy pullback]] square (using the [[pasting law]]).

Notice that for instance $w_2$ is identified as such by using that $[S^2,-]$ preserves [[homotopy pullbacks]] and sends $ B O \to \tau_{\leq 2} B O$ to a [[weak homotopy equivalence|equivalence]], so that $B SO \to B^2 \mathbb{Z}$ is an [[isomorphism]] on the second [[homotopy group]] and hence by the [[Hurewicz theorem]] is also an isomorphism on the [[cohomology group]] $H^2(-,\mathbb{Z}_2)$. Analogously for the other characteristic maps.

In summary, more concisely, the tower is

$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    B Fivebrane
    \\
    \downarrow
    \\
    B String &\stackrel{\tfrac{1}{6}p_2}{\to}& B^7 U(1) & \simeq B^8 \mathbb{Z}
    \\
    \downarrow
    \\
    B Spin &\stackrel{\tfrac{1}{2}p_1}{\to}& B^3 U(1) & \simeq B^4 \mathbb{Z}
    \\
    \downarrow
    \\
    B SO &\stackrel{w_2}{\to}& B^2 \mathbb{Z}_2
    \\
    \downarrow
    \\
    B O &\stackrel{w_1}{\to}& B \mathbb{Z}_2
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    B GL
  }
  \,,
$$

where each "hook" is a [[fiber sequence]].


## Related concepts

* [[metaplectic structure]], [[metalinear structure]]

* [[twisted differential c-structure|(twisted differential) c-structure]]

  * [[orientation]]

  * **spin structure**, [[twisted spin structure]], [[differential spin structure]]

    [[spin^c structure]], [[twisted spin^c structure]]

    [[spin^h structure]]

    [[Spin Chern-Simons theory]]

  * [[2-framing]]

  * [[string structure]], [[differential string structure]]

  * [[fivebrane structure]], [[differential fivebrane structure]]

[[!include higher spin structure - table]]


## References

### General

Standard texbooks include 

* [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], chapter II of _[[Spin geometry]]_, Princeton University Press (1989)

* {#Friedrich97} [[Thomas Friedrich]], _Dirac operators in Riemannian geometry_, Graduate studies in mathematics 25, AMS (1997)
 

A discussion of the full [[groupoid]] of spin structures is in 

* [[Johannes Ebert]], _Characteristic classes of spin surface bundles:
Applications of the Madsen-Weiss theory_ Phd thesis (2006) ([pdf](http://wwwmath.uni-muenster.de/wwwmath.uni-muenster.de/u/jeber_02/papers/thesis.pdf))

Discussion of lifting bundle gerbes for spin structures is in

* {#MurraySinger03} [[Michael Murray]], Michael Singer, _Gerbes, Clifford modules and the index theorem_ ([arXiv:math/0302096](http://arxiv.org/abs/math/0302096))
  

Discussion of spin structures in terms of smooth moduli stacks as above is in

* [[Urs Schreiber]], section 5.1 of _[[schreiber:differential cohomology in a cohesive topos]]_.
  {#dcct}


Discussion of spin structures on surfaces is in

* Dennis Johnson, _Spin structures and quadratic forms on surfaces_. J. London Math. Soc. (2) 22 (1980), no. 2, 365&#8211;373. 

See also [this MO comment](http://mathoverflow.net/a/136425/381).

Discussion of spin structure on [[Kähler manifolds]] is in 

* [[Nigel Hitchin]], _Harmonic spinors_, Adv. Math. 14 (1974), 1 &#8722; 55. 
 {#Hitchin74}

* [[Christian Bär]], _On harmonic spinors_ ([pdf](http://www.actaphys.uj.edu.pl/vol29/pdf/v29p0859.pdf))

A textbook account is in ([Friedrich 97, section 3.4](#Friedrich97))

A survey is also at

* _[Theta characteristics and framings](http://amathew.wordpress.com/2013/06/23/theta-characteristics-and-framings/)_


* _Spin manifolds_ ([pdf](http://empg.maths.ed.ac.uk/Activities/Spin/Lecture4.pdf))

Spin structures on [[orbifolds]]:

* Daniel J. Acosta, _A Furuta-like inequality for spin orbifolds and the minimal genus problem_, Topology and its Applications Volume 114, Issue 1, 16 July 2001, Pages 91-106 (<a href="https://doi.org/10.1016/S0166-8641(00)00030-4">doi:10.1016/S0166-8641(00)00030-4</a>)

* Chongying Dong, [[Kefeng Liu]], Xiaonan Ma, _On orbifold elliptic genus_ ([pdf](https://webusers.imj-prg.fr/~xiaonan.ma/mypubli/dlm02.pdf)), p. 87-105 In: [[Alejandro Adem]], [[Jack Morava]], [[Yongbin Ruan]], _[[Orbifolds in Mathematics and Physics]]_, Contemporary Mathematics 310 AMS (2002)([ams:conm-310](https://bookstore.ams.org/conm-310))

* Florin Belgun, Nicolas Ginoux, Hans-Bert Rademacher, _A Singularity Theorem for Twistor Spinors_,  Annales de l'Institut Fourier, Volume 57 (2007) no. 4, p. 1135-1159  ([arXiv:math/0409136](https://arxiv.org/abs/math/0409136), [numdam:AIF_2007__57_4_1135_0](http://www.numdam.org/item/AIF_2007__57_4_1135_0))

### In quantum anomaly cancellation

Discussions of spin structures in the context of [[quantum anomaly]] cancellation for the [[spinning particle]] date back to

* [[Edward Witten]], _Global anomalies in String theory_ in _Symposium on anomalies, geometry, topology_ , World Scientific Publishing, Singapore (1985)

* [[Luis Alvarez-Gaumé]], Communications in Mathematical Physics 90 (1983) 161

* D. Friedan, P. Windey, Nucl. Phys. B235 (1984) 395




[[!redirects Spin structure]]
[[!redirects Spin-structure]]
[[!redirects spin-structure]]

[[!redirects Spin structures]]
[[!redirects Spin-structures]]
[[!redirects spin structures]]
[[!redirects spin-structures]]

[[!redirects spin manifold]]
[[!redirects spin manifolds]]
[[!redirects spin-manifold]]
[[!redirects spin-manifolds]]
