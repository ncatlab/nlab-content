
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In every [[cohesive (∞,1)-topos]] there is an <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#ChernWeilTheory">intrinsic notion of ∞-Chern-Weil theory</a> that gives rise to a notion of _connection_ on [[principal ∞-bundle]]s. We describe here details of the realization of this general abstract structure in the cohesive $(\infty,1)$-topos [[Smooth∞Grpd]] of [[smooth ∞-groupoid]]s.

For $G$ an [[∞-Lie group]], a _connection_ on a smooth $G$-[[principal ∞-bundle]] is a structure that supports the [[Chern-Weil homomorphism in Smooth∞Grpd]]: it interpolates between the [[nonabelian cohomology]] class $c \in H^1_{smooth}(X,G)$ of the bundle and the refinements to [[ordinary differential cohomology]] of its [[characteristic class]]es: the [[curvature characteristic form|curvature characteristic class]]es.

This generalizes the  notion of [[connection on a bundle]] and the ordinary [[Chern-Weil homomorphism]] in [[differential geometry]].

See the <a href="http://nlab.mathforge.org/nlab/show/Chern-Weil+theory+in+Smooth%E2%88%9EGrpd#Motivation">Motivation section</a> at [[Chern-Weil theory in Smooth∞Grpd]] and the page [[∞-Chern-Weil theory introduction]] for more background.

## Definition

### For braided $\infty$-groups

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] equippd with [[differential cohesion]] and let $\mathbb{G} \in Grp(\mathbf{H})$ be a [[braided ∞-group]]. Write 

$$
  curv_{\mathbb{G}} = \theta_{\mathbf{B}\mathbb{G}}
  \;\colon\;
  \mathbf{B}\mathbb{G}
  \to 
  \flat_{dR}\mathbf{B}^2 \mathbb{G}
$$

for the [[Maurer-Cartan form]] on the [[delooping]] [[∞-group]] $\mathbf{B}\mathbb{G} \in Grp(\mathbf{H})$.

Let 

$$
  \Omega(-,\mathbb{G})
  \to
  \flat_{dR}\mathbf{B}^2 \mathbb{G}
$$

be the morphism out of a [[0-truncated]] object which is universal with the property that for $\Sigma \in \mathbf{H}$ any [[manifold]], the induced [[internal hom]] map

$$
  [\Sigma, \Omega(-,\mathbb{G})]
  \to
  [\Sigma, \flat_{dR}\mathbf{B}^2 \mathbb{G}]
$$

is a [[1-epimorphism]].

Then write $\mathbf{B}\mathbb{G}_{conn}$ for the [[(∞,1)-pullback]] in 

$$
  \array{
    \mathbf{B}\mathbb{G}_{conn}
    &\to&
    \Omega(-,\mathbb{G})
    \\
    \downarrow
    &&
    \downarrow
    \\
    \mathbf{B}\mathbb{G}
    &\stackrel{curv_{\mathbb{G}}}{\to}&
    \flat_{dR}\mathbf{B}^2 \mathbb{G}
  }
  \,.
$$

We say that $\mathbf{B}\mathbb{G}_{conn}$ is the [[moduli ∞-stack]] of **$\mathbb{G}$-principal $\infty$-connections.

For instance for $\mathbb{G} = \mathbf{B}^{n-1}U(1)$ the [[circle n-group]] the moduli $n$-stack $\mathbf{B}^n U(1)_{conn}$ is presented by the [[Deligne complex]] for [[ordinary differential cohomology]] in degree $(n+1)$, hence is the moduli $n$-stack for [[circle n-bundles with connection]].

### For $\infty$-groups obtained by Lie integration
 {#ByLieIntegration}

We assume that the reader is familiar with the notation and constructions discussed at [[Smooth∞Grpd]]. The following definition may be understood as a direct generalization of the description of ordinary $G$-connections as cocycles in the stack $\mathbf{B}G_{conn}$ as discussed at [[connection on a bundle]], in view of the characterization of [Weil algebra in the smooth infinity-topos](Weil+algebra#CharacterizationInSmoothTopos)

[[!include Weil algebra abstractly -- table]]

We discuss now connections on those $G$-[[principal ∞-bundle]]s for which $G \in $ [[Smooth∞Grpd]] is an [[∞-Lie group|smooth ∞-group]] that arises from [[Lie integration]] of an [[L-∞ algebra]] $\mathfrak{g}$.

Let $\mathfrak{g} \in L_\infty \stackrel{CE}{\hookrightarrow} $ [[dgAlg]]${}^{op}$ be an [[L-∞ algebra]] over the [[real number]]s and of [[finite type]] with [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ and [[Weil algebra]] $W(\mathfrak{g})$.

For $X$ a [[smooth manifold]], write $\Omega^\bullet(X) \in dgAlg$ for the [[de Rham complex]] of smooth [[differential form]]s. For $k \in \mathbb{N}$ let $\Delta^k$ be the standard $k$-[[simplex]] regarded as a smooth [[manifold with corners]] in the standard way. Write $\Omega^\bullet_{si}(X \times \Delta^k)$ for the sub-[[dg-algebra]] of differential forms with sitting instants perpendicular to the boundary of the simplex, and $\Omega^\bullet_{si,vert}(X\times \Delta^k)$ for the further sub-dg-algebra of [[vertical differential form]]s with respect to the canonical projection $X \times \Delta^k \to X$. 

+-- {: .un_defn}
###### Definition


A morphism

$$
  \Omega^\bullet(X)
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

in [[dgAlg]] we call an [[∞-Lie algebra valued differential forms|L-∞ algebra valued differential form]] with values in $\mathfrak{g}$, dually a morphism of [[∞-Lie algebroid]]s

$$
  A : T X \to inn(\mathfrak{g})
$$

from the [[tangent Lie algebroid]] to the [[Weil algebra|inner automorphism ∞-Lie algebra]].

Its [[curvature]] is the composite of morphisms of [[graded vector space]]s

$$
  \Omega^\bullet(X) \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{F_{(-)}}{\leftarrow}
  \mathfrak{g}^*[2]
  : 
  F_{A}
$$

that injects the shifted generators into the [[Weil algebra]].

Precisely if the curvatures vanish does the morphism factor through the [[Chevalley-Eilenberg algebra]] 

$$
  (F_A = 0) 
  \;\;\Leftrightarrow
  \;\;
  \left(
  \array{
     && CE(\mathfrak{g})
     \\
     & {}^{\mathllap{\exists A_{flat}}}\swarrow & \uparrow
     \\
     \Omega^\bullet(X) &\stackrel{A}{\leftarrow}& W(\mathfrak{g})     
  }
  \right)
$$

in which case we call $A$ **flat**.

The [[curvature characteristic form]]s of $A$ are the composite

$$
  \Omega^\bullet(X)
  \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{\langle F_{(-)} \rangle}{\leftarrow}
  inv(\mathfrak{g})
  :
  \langle F_A\rangle
  \,,
$$

where $inv(\mathfrak{g}) \to W(\mathfrak{g})$ is the inclusion of the [[invariant polynomial]]s. 

=--

We define now [[simplicial presheaves]] over the [[site]] [[CartSp]]${}_{smooth} \hookrightarrow $ [[SmoothMfd]] of [[Cartesian space]]s and [[smooth function]]s between them.

+-- {: .un_defn}
###### Definition

Write $\exp(\mathfrak{g}) \in [CartSp_{smooth}^{op}, sSet]$ for the simplicial presheaf given by

$$
  \exp(\mathfrak{g}) : 
  (U,[k])
  \mapsto
  \left\{
    \Omega^\bullet_{si,vert}(U \times\Delta^k)
     \stackrel{A_{vert}}{\leftarrow}
    CE(\mathfrak{g})
  \right\}
$$

(the untruncated [[Lie integration]] of $\mathfrak{g}$).

Write $\exp(\mathfrak{g})_{diff} \in [CartSp_{smooth}^{op}, sSet]$ for the simplicial presheaf given by


$$
  \exp(\mathfrak{g})_{diff} :
  (U,[k])
  \mapsto
  \left\{
     \array{
      \Omega^\bullet_{si,vert}(U \times\Delta^k)
       &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet_{si}(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{g})
    }
  \right\}
  \,.
$$

Write $\exp(\mathfrak{g})_{ChW} \in [CartSp_{smooth}^{op}, sSet]$ for the simplicial presheaf given by

$$
  \exp(\mathfrak{g})_{ChW}
  :
  (U,[k])
  \mapsto
  \left\{
     \array{
      \Omega^\bullet_{si,vert}(U \times\Delta^k)
       &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet_{si}(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
    }
  \right\}
  \,.
$$


Define the [[simplicial presheaf]] $\exp(\mathfrak{g})_{conn}$ by

$$
  \exp(\mathfrak{g})_{conn}(U)
  :
  [k]
  \mapsto
  \left\{
     \Omega^\bullet_{si}(U \times \Delta^k)
      \stackrel{A}{\leftarrow}
     W(\mathfrak{g})
     \;\;
     |
     \;\;
       \forall v \in \Gamma(T \Delta^k) : \iota_v F_A = 0
  \right\}
$$

=--

Here on the right we have in each case the [[set]]s of horizontal morphisms in [[dgAlg]] that make [[commuting diagram]]s in [[dgAlg]] as indicated, with the vertical morphisms being the canonical projections and inclusions. The functoriality in $f : K \to U$ and $\rho : [k] \to [l]$ is by the evident precomposition with the pullback of differential forms $\Omega^\bullet(U \times \Delta^k) \stackrel{(f,id)^*}{\to} \Omega^\bullet(K \times \Delta^k)$ and $\Omega^\bullet(U \times \Delta^l) \stackrel{(id,\rho)^*}{\leftarrow} \Omega^\bullet(U, \times \Delta^k)$.


+-- {: .un_prop #SequenceOfInclusionsOfCoefficients}
###### Proposition

There are canonical morphisms in $[CartSp_{smooth}^{op},sSet]$ between these objects

$$
  \array{
    \exp(\mathfrak{g})_{conn}
    &\hookrightarrow&
    \exp(\mathfrak{g})_{ChW}
    &\hookrightarrow&
    \exp(\mathfrak{g})_{diff}
    \\
    && && \downarrow
    \\
    && && \exp(\mathfrak{g})
  }
  \,,
$$

where the horizontal morphisms are [[monomorphism]]s of [[simplicial presheaves]] and the vertical morphism is over each $U \in CartSp$ an equivalence of [[Kan complexes]] (it is a weak equivalence between fibrant objects in the projective [[model structure on simplicial presheaves]]).

=--

+-- {: .proof}
###### Proof

The inclusion $\exp(\mathfrak{g})_{ChW} \hookrightarrow \exp(\mathfrak{g})_{dff}$ is clear. The weak equivalence $\exp(\mathfrak{g})_{diff} \to \exp(\mathfrak{g})$ is discussed at [[Smooth∞Grpd]] (but is also directly verified).

To see the inclusion $\exp(\mathfrak{g})_{conn} \hookrightarrow \exp(\mathfrak{g})_{ChW}$ we need to check that the horizonality condition $\iota_v F_A = 0$ on the [[curvature]] of a $\mathfrak{g}$-valued form $A$ for all [[vector field]]s $v$ tangent to the simplex implies that all the [[curvature characteristic form]]s $\langle F_A\rangle$ are _basic forms_ that "descend to $U$", hence that are in the image of the inclusion $\Omega^\bullet(U) \to \Omega^\bullet_{si}(U \times \Delta^k)$.

For this it is sufficient to show that for all $v \in \Gamma(T \Delta^k)$ we have

1. $\iota_v \langle F_A \rangle = 0$;

1. $\mathcal{L}_v \langle F_A \rangle = 0$

where in the second line we have the [[Lie derivative]] $\mathcal{L}_v$ along $v$.

The first condition is evidently satisfied if already $\iota_v F_A = 0$. The second condition follows with [[Cartan calculus]] and using that $d_{dR} \langle F_A\rangle = 0$ (which holds as a consequence of the definition of [[invariant polynomial]]):

$$
  \mathcal{L}_v \langle F_A \rangle = 
  d \iota_v \langle F_A \rangle
  + 
  \iota_v d \langle F_A \rangle
  = 0
  \,.
$$

=--

+-- {: .un_lemma}
###### Remark

For a general [[L-∞ algebra]] $\mathfrak{g}$ the [[curvature]] forms $F_A$ themselves are not necessarily closed (rather they satisfy the [[Bianchi identity]]), hence requiring them to have no component along the simplex does not imply that they descend. This is different for abelian [[L-∞ algebra]]s: for them the curvature forms themselves are already closed, and hence are themselves already curvature characteristics that do descent. 

=--


For $n \in \mathbb{N}$ 
let $\mathbf{cosk}_{n+1} : sSet \to sSet$ be the [[simplicial coskeleton]] functor. Its prolongation to simplicial presheaves we denote here $\tau_n$ and write 

$$
 \tau_n \exp(\mathfrak{g}) \in [CartSp_{smooth}^{op}, sSet]
$$

etc. This is the [[delooping]] 

$$
  \tau_n \exp(\mathfrak{g}) = \mathbf{B}G
$$

of the universal [[Lie integration]] of $\mathfrak{g}$ to an [[∞-Lie group|smooth n-group]] $G$.

+-- {: .un_def}
###### Definition

For any $X \in [CartSp_{smooth}^{op}, sSet]$ and $\hat X \to X$ any cofibrant [[resolution]] in the local projective [[model structure on simplicial presheaves]] (see [[Smooth∞Grpd]] for details), we say that the [[sSet]]-[[hom object]]

* $[CartSp_{smooth}^{op}, sSet](\hat X, \tau_n \exp(\mathfrak{g}))$
  is the [[∞-groupoid]] of smooth $G$-[[principal ∞-bundle]]s on $X$;

* $[CartSp_{smooth}^{op}, sSet](\hat X, \tau_n \exp(\mathfrak{g})_{diff})$
  is the [[∞-groupoid]] of smooth $G$-[[principal ∞-bundle]]s on $X$ equipped with **pseudo $\infty$-connection**;

* $[CartSp_{smooth}^{op}, sSet](\hat X, \tau_n \exp(\mathfrak{g})_{conn})$
  is the [[∞-groupoid]] of smooth $G$-[[principal ∞-bundle]]s on $X$ equipped with **$\infty$-connection**.

=--

+-- {: .un_remark}
###### Remark

In view of this definition we may read the [above](#SequenceOfInclusionsOfCoefficients) sequence of morpisms of coefficient objects as follows:

$$
  \array{
    \exp(\mathfrak{g})_{conn} &&& genuine\;connections
    \\
    \downarrow
    \\
    \exp(\mathfrak{g})_{ChW} &&& pseudo-connection\;with\;global\;curvature\;characteristics 
    \\
    \downarrow
    \\
    \exp(\mathfrak{g})_{diff} &&& pseudo-connections
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \exp(\mathfrak{g}) &&& bare bundles
  }
  \,,
$$

As we shall see in more detail below, the components of an $\infty$-connection in terms of the above diagrams we may think of as follows:

$$
    \array{
      \Omega^\bullet(U \times \Delta^k)_{vert}
      &\stackrel{A_{vert}}{\leftarrow}&
      CE(\mathfrak{g})
      &&&
      gauge\;transformation
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U \times \Delta^k)
      &\stackrel{A}{\leftarrow}&
      W(\mathfrak{g})
      &&&
      \mathfrak{g}-valued\;form
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)
      &\stackrel{\langle F_A\rangle}{\leftarrow}&
      inv(\mathfrak{g})
      &&&
      curvature\;characteristic\;forms
    }
$$

=--




+-- {: .un_remark}
###### Remark


In full [[Chern-Weil theory in Smooth∞Grpd]] the fundamental object of interest is really $\exp(\mathfrak{g})_{diff}$ -- the object of [[pseudo-connection]]s, which serves as the correspondence object for an [[∞-anafunctor]] out of $\exp(\mathfrak{g})$ that presents the differential characteristic classes on $\exp(\mathfrak{g})$. From an abstract point of view the other objects only serve the purpose of picking particularly nice representatives.

This distinction is important: over objects $X \in $ [[Smooth∞Grpd]] that are not [[smooth manifold]]s but for instance [[orbifold]]s, the genuine $\mathfrak{g}$-connections for general higher $\mathfrak{g}$ do _not_ exhaust all nonabelian differential cocycles. This just means that not every differential class in this case does have a nice representative.

=--


## Examples


### 1-Morphisms: integration of infinitesimal gauge transformations {#InfGaugeTrafo}

The 1-[[morphism]]s in $\exp(\mathfrak{g})_{conn}(U)$ may be thought of as [[gauge transformation]]s between $\mathfrak{g}$-valued forms. We unwind what these look like concretely.


+-- {: .un_defn}
###### Definition

Given a 1-morphism in $\exp(\mathfrak{g})(X)$, represented by $\mathfrak{g}$-valued forms

$$
  \Omega^\bullet(U \times \Delta^1) 
  \leftarrow
  W(\mathfrak{g})
  : 
  A
$$

consider the unique decomposition

$$
  A = A_U + ( A_{vert} := \lambda \wedge d s)  \; \; 
  \,,
$$

with $A_U$ the horizonal differential form component and $s : \Delta^1 = [0,1] \to \mathbb{R}$ the canonical [[coordinate]].

We call $\lambda$ the **gauge parameter** . This is a function on $\Delta^1$ with values in 0-forms on $U$ for $\mathfrak{g}$ an ordinary [[Lie algebra]], plus 1-forms on $U$ for $\mathfrak{g}$ a [[Lie 2-algebra]], plus 2-forms for a Lie 3-algebra, and so forth.

=--

We describe now how this enccodes a gauge transformation

$$
  \lambda : A_0(s=0) \stackrel{}{\to} A_U(s = 1)
  \,.
$$

+-- {: .un_lemma}
###### Observation

We have

$$
  \frac{d}{d s} A_U
  =
  (d_U \lambda + [\lambda \wedge A] + [\lambda \wedge A \wedge A] + \cdots)
  + 
  \iota_{\partial_s} F_A
  \,,
$$

where the sum is over all higher brackets of the [[L-∞ algebra]] $\mathfrak{g}$. 

=--

+-- {: .proof}
###### Proof

This is the result of applying the contraction $\iota_{\partial s}$ to the defining equation for the [[curvature]] $F_A$ of $A$ using the nature of the [[Weil algebra]]:

$$
  F_A = d_{dR} A + [A \wedge A] + [A \wedge A \wedge A] + \cdots
$$

and inserting the above decomposition for $A$.

=--


+-- {: .un_def}
###### Definition

Define the **[[covariant derivative]] of the gauge parameter** to be

$$
  \nabla_A \lambda := d \lambda + [A \wedge \lambda] + [A \wedge A \wedge \lambda] + \cdots
  \,.
$$

=--

In this notation we have

* the general identity 

  \[
    \frac{d}{d s} A_U = \nabla \lambda + (F_A)_s
    \label{ShiftedGaugeTrafo}
  \]

* the **horizontality** or **[[rheonomy]]** constraint or **[[Ehresmann connection|second Ehresmann condition]]** $\iota_{\partial_s} F_A = 0$, the [[differential equation]]

  \[
    \frac{d}{d s} A_U = \nabla \lambda
    \label{GaugeTrafo}
    \,.
  \]

This is known as the equation for **infinitesimal [[gauge transformation]]s** of an $L_\infty$-algebra valued form. 



+-- {: .un_lemma}
###### Observation

By [[Lie integration]] we have that $A_{vert}$ -- and hence $\lambda$ -- defines an element $\exp(\lambda)$ in the [[∞-Lie group]] that integrates $\mathfrak{g}$. 

The unique solution $A_U(s = 1)$ of the above [[differential equation]] at $s = 1$ for the initial values $A_U(s = 0)$ we may think of as the result of acting on $A_U(0)$ with the gauge transformation $\exp(\lambda)$. 

=--



### Ordinary connections on principal 1-bundles


+-- {: .un_prop}
###### Proposition
**(connections on ordinary bundles)**

For $\mathfrak{g}$ an ordinary [[Lie algebra]] with simply connected [[Lie group]] $G$ and for $\mathbf{B}G_{conn}$ the [[groupoid of Lie algebra-valued forms]] we have an equivalence

$$
  \tau_1 \exp(\mathfrak{g})_{conn} \simeq \mathbf{B}G_{conn}
$$

betweenn the 1-truncated coefficient object for $\mathfrak{g}$-valued $\infty$-connections and the coefficient objects for ordinary [[connections on a bundle]] (see there).

=--

+-- {: .proof}
###### Proof

Notice that the sheaves of [[object]]s on both sides are manifestly isomorphic, both are the sheaf of $\Omega^1(-,\mathfrak{g})$. 

On [[morphism]]s, we have by the [above](#InfinitesimalGaugeTransformations) for a form $\Omega^\bullet(U \times \Delta^1) \leftarrow W(\mathfrak{g}) : A$ decomposed into a horizontal and a verical pice as $A = A_U + \lambda \wedge d t$ that the condition $\iota_{\partial_t} F_A = 0$ is equivalent to the [[differential equation]]

$$
  \frac{\partial}{\partial s} A
  =
  d_U \lambda + [\lambda, A]
  \,.
$$

For any initial value $A(0)$ this has the unique solution

$$
  \begin{aligned}
     A(t) & = g(t)^{-1} (A + d_{U}) g(t)
      \\
     & = Ad_{g(t)}(A) + g(t)^* \theta
  \end{aligned}
$$

(with $\theta$ the [[Maurer-Cartan form]] on $G$), where $g \in C^\infty([0,1], G)$ is the [[parallel transport]] of $\lambda$:

$$
  \begin{aligned}
    &
    \frac{\partial}{\partial s}
    \left(
       g_(t)^{-1} (A + d_{U}) g(t)
     \right)
     \\
     & = 
     g(t)^{-1} (A + d_{U}) \lambda g(t)
     -
     g(t)^{-1} \lambda (A + d_{U}) g(t)    
   \end{aligned}
$$

(where for ease of notaton we write actions as if $G$ were a [[matrix Lie group]]).

This implies that the endpoints of the path of $\mathfrak{g}$-valued 1-forms are related by the usual cocycle condition in $\mathbf{B}G_{conn}$

$$
  A(1) = g(1)^{-1} (A + d_U) g(1)
  \,.
$$

In the same fashion one sees that given 2-cell in $\exp(\mathfrak{g})(U)$ and any 1-form on $U$ at one vertex, there is a unique lift to a 2-cell in $\exp(\mathfrak{g})_{conn}$, obtained by parallel transporting the form around. The claim then follows from the previous statement of [[Lie integration]] that $\tau_1 \exp(\mathfrak{g}) = \mathbf{B}G$.

=--


### Further examples

* For $\mathfrak{g}$ [[Lie 2-algebra]], a $\mathfrak{g}$-valued differential form in the sense described here is precisely an [[Lie 2-algebra valued form]].


* For $n \in \mathbb{N}$, a $b^{n-1}\mathbb{R}$-valued differential form is the same as an ordinary differential $n$-form.


* What is called an  "extended soft group manifold" in the literature on the [[D'Auria-Fre formulation of supergravity]] is precisely a collection of $\infty$-Lie algebroid valued forms with values in a super $\infty$-Lie algebra such as the 
[[supergravity Lie 3-algebra]]/[[supergravity Lie 6-algebra]] (for 11-dimensional [[supergravity]]). The way [[curvature]] and [[Bianchi identity]] are read off from "extded soft group manifolds" in this literature is -- apart from this difference in terminology -- precisely what is described above. 





## Related concepts

* [[connection on a bundle]]

* [[connection on a 2-bundle]] / [[connection on a gerbe]] / [[connection on a bundle gerbe]]

* [[connection on a 3-bundle]] / [[connection on a bundle 2-gerbe]]

* **connection on an ∞-bundle**

  * [[flat ∞-connection]]

* [[parallel transport]], [[higher parallel transport]]

* [[holonomy]]

[[!include higher Atiyah groupoid - table]]



## References

The local differential form data of $\infty$-connections was introduced in 

* {#SSSI} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:L-infinity algebra connections|L-∞ algebra connections and applications to String- and Chern-Simons n-transport]]_, in: *Quantum Field Theory*, Birkh&#228;user (2009) 303-424 ([arXiv:0801.3480](http://arxiv.org/abs/0801.3480), [doi:10.1007/978-3-7643-8736-5_17](https://doi.org/10.1007/978-3-7643-8736-5_17))
  
* {#SSSIII} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Twisted Differential String and Fivebrane Structures]]_, Communications in Mathematical Physics, October 2012, Volume 315, Issue 1, pp 169-213 ([arXiv:0910.4001](http://arxiv.org/abs/0910.4001), [doi:10.1007/s00220-012-1510-3](https://link.springer.com/article/10.1007/s00220-012-1510-3))


The global description was then introduced in 

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech cocycles for differential characteristic classes]] -- An $\infty$-Lie theoretic construction_, Advances in Theoretical and Mathematical Physics, Volume 16 Issue 1 (2012), pages 149-250 ([arXiv:1011.4735](http://arxiv.org/abs/1011.4735), [euclid:atmp/1358950853](http://projecteuclid.org/euclid.atmp/1358950853)) 


A more comprehensive account is in sections 3.9.6, 3.9.7 of


* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_


[[!redirects ∞-connection on a principal ∞-bundle]]
[[!redirects ∞-connection on a principal ∞-bundle]]

[[!redirects connection on a principal ∞-bundle]]

[[!redirects connection on an ∞-bundle]]
[[!redirects connections on an ∞-bundle]]

[[!redirects connection on an infinity-bundle]]

[[!redirects connections on ∞-bundles]]
[[!redirects connections on infinity-bundles]]

[[!redirects connection on a smooth principal ∞-bundle]]
[[!redirects connections on smooth principal ∞-bundles]]
[[!redirects connection on a principal infinity-bundle]]

[[!redirects connections on smooth principal ∞-bundles]]

[[!redirects ∞-connection]]
[[!redirects ∞-connections]]


[[!redirects principal ∞-connection]]
[[!redirects principal ∞-connections]]

[[!redirects principal infinity-connection]]
[[!redirects principal ∞-connections]]
[[!redirects principal infinity-connections]]

[[!redirects connections on principal ∞-bundles]]
