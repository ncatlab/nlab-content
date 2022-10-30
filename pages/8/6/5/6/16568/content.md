

> this page is one chapter in _[[geometry of physics]]_

> previous chapter: _[[geometry of physics -- principal connections|principal connections]]_;

> next chapter: _[[geometry of physics -- BPS charges|BPS charges]]_

***

#Contents#
* table of contents
{:toc}

## **Prequantum geometry**

There are two dual kinds of mathematical formalization of [[quantization]], one is algebraic, usually known as [[deformation quantization]], the other is geometric, known as _[[geometric quantization]]_. The latter involves an intermediate stage called _[[prequantization]]_. This is the refinement of [[symplectic geometry]] obtained by lifting closed [[differential 2-forms]] to being [[curvature]] forms of [[circle bundles with connection]]. Since [[circle bundles]] and [[circle bundles with connection]], as opposed to plain [[differential forms]], have non-trivial [[automorphisms]] (they form a [[groupoid]] not just a [[set]]) the group of [[symmetries]] of a prequantized symplectic manifold differs from the group of symmetries of the underlying symplectic manifold (the [[symplectomorphisms]]): the freedom in identifying the prequantum $U(1)$-bundle with itself makes it is a [[central extension]], specifically a $U(1)$-central extension if the base manifold is connected. This circle extension with the integrality that it relates to (e.g. via its [[Chern class]] with coefficients in $\mathbb{Z} = \pi_1(U(1))$) is behind much of what is quanta-like about quantum physics.
Hence while prequantization is not yet full quantization, much of the hallmark structure of quantization is present already in these "[[quantomorphism]]" $U(1)$-extensions of the symmetries of prequantum bundles, notably its [[Lie algebra]] subsumes the [[Heisenberg algebra]] of [[symplectic vector spaces]], this we survey below in _[The geometric idea of quantization](#TheGeometricIdeaOfQuantization)_.

Hence it makes good sense to study prequantized smooth manifolds as geometries in their own right, and a sensible name for this is _prequantum geometry_. 

As one passes from [[quantum mechanics]] to $(p+1)$-dimensional [[quantum field theory]] such as to preserve the locality of [[local quantum field theory]], then the process of [[quantization]] involves not just [[symplectic manifolds]] equipped with symplectic differential 2-forms, but involves "[[covariant phase space|symplectic currents]]" which are $(p+2)$-forms. Such higher degree analogs of symplectic forms are known historically already from the [[de Donder-Weyl-Hamilton equation]] of local [[classical field theory]] and approaches to promote their theory to a higher analog of [[symplectic geometry]] go by the names _[[multisymplectic geometry]]_ and _[[n-plectic geometry|(p+1)-plectic geometry]]_. The [[higher prequantization]] of such a higher degree form is naturally a [[circle n-bundle with connection|circle (p+1)-bundle with connection]] (a [[bundle gerbe with connection]] for $p = 1$, generally a [[cocycle]] in [[Deligne cohomology]] of degree $p+2$), and hence _[[higher prequantum geometry]]_ is the study of spaces that are equipped with such abelian [[principal infinity-connections]]. 

This is what we discuss here. More abstractly, if we we write $\mathbf{B}\mathbb{G}_{conn}$ for the [[higher moduli stack]] of $\mathbb{G}$-[[principal infinity-connections]], for instance $\mathbf{B}^{p+1}U(1)_{conn}$ the moduli stack for cocycles in [[Deligne cohomology]] in degree $(p+2)$, then a prequantum $\mathbb{G}$-bundle over some [[smooth homotopy type]] $X$ is equivalently just a morphism $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, and a symmetry of such a higher prequantum geometry $(X,\nabla)$ is a diagram of the form

$$
  \array{
     X && \stackrel{\simeq}{\longrightarrow} &&  X
     \\
     & {}_{\mathllap{\nabla}}\searrow &\swArrow_{\mathrlap{\simeq}}& \swarrow_{\mathrlap{\nabla}}
     \\
     && \mathbf{B}\mathbb{G}_{conn}
  }
  \,.
$$

This means that for $\mathbf{H}$ a [[cohesive (∞,1)-topos]] of geometric spaces of sorts, then the corresponding $\mathbb{G}$-prequantum geometry is that encoded by the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}\mathbb{G}_{conn}}$. Hence prequantum geometry is the geometry in slices over [[higher moduli stacks]] for [[differential cohomology]].

### The geometric idea of quantization
 {#TheGeometricIdeaOfQuantization}

Quantization of course was and is motivated by [[experiment]], hence by observation of the [[observable universe]]: it just so happens that [[quantum mechanics]] and [[quantum field theory]] correctly account for experimental observations where [[classical mechanics]] and [[classical field theory]] gives no answer or incorrect answers. A historically important example is the phenomenon called the "[[ultraviolet catastrophe]]", a [[paradox]] predicted by classical [[statistical mechanics]] which is _not_ observed in nature, and which is corrected by [[quantum mechanics]].

But one may also ask, independently of experimental input, if there are good formal mathematical reasons and motivations to pass from [[classical mechanics]] to [[quantum mechanics]]. Could one have been led to [[quantum mechanics]] by just pondering the mathematical formalism of [[classical mechanics]]? (Hence more precisely: is there a natural _[[schreiber:Synthetic Quantum Field Theory]]_?)

The following spells out an argument to this effect. It will work for readers with a background in modern [[mathematics]], notably in [[Lie theory]], and with an understanding of the formalization of classical/prequantum mechanics in terms of [[symplectic geometry]]. 

So to briefly recall, a system of [[classical mechanics]]/[[prequantum field theory|prequantum mechanics]] is a [[phase space]], formalized as a [[symplectic manifold]] $(X, \omega)$. A symplectic manifold is in particular a [[Poisson manifold]], which means that the [[algebra of functions]] on [[phase space]] $X$, hence the algebra of _classical [[observables]]_, is canonically equipped with a compatible [[Lie bracket]]: the _[[Poisson bracket]]_. This Lie bracket is what controls [[dynamics]] in [[classical mechanics]]. For instance if $H \in C^\infty(X)$ is the function on [[phase space]] which is interpreted as assigning to each configuration of the system its [[energy]] -- the [[Hamiltonian]] function -- then the [[Poisson bracket]] with $H$ yields the [[infinitesimal object|infinitesimal]] time evolution of the system: the [[differential equation]] famous as [[Hamilton's equations]].

Something to take notice of here is the _[[infinitesimal space|infinitesimal]]_ nature of the [[Poisson bracket]]. Generally, whenever one has a [[Lie algebra]] $\mathfrak{g}$, then it is to be regarded as the [[infinitesimal object|infinitesimal]] approximation to a globally defined object, the corresponding [[Lie group]] (or generally [[smooth group]]) $G$. One also says that $G$ is a _[[Lie integration]]_ of $\mathfrak{g}$ and that $\mathfrak{g}$ is the [[Lie differentiation]] of $G$.

Therefore a natural question to ask is: _Since the observables in [[classical mechanics]] form a [[Lie algebra]] under [[Poisson bracket]], what then is the corresponding [[Lie group]]?_

The answer to this is of course "well known" in the literature, in the sense that there are relevant monographs which state the answer. But, maybe surprisingly, the answer to this question is not (at time of this writing) a widely advertized fact that has found its way into the basic educational textbooks. The answer is that this [[Lie group]] which integrates the [[Poisson bracket]] is the "[[quantomorphism group]]", an object that seamlessly leads to the [[quantum mechanics]] of the system.

Before we spell this out in more detail, we need a brief technical aside: of course [[Lie integration]] is not quite unique. There may be different global [[Lie group]] objects with the same [[Lie algebra]]. 

The simplest example of this is already one of central importance for the issue of quantization, namely, the Lie integration of the abelian [[line Lie algebra]] $\mathbb{R}$. This has essentially two different [[Lie groups]] associated with it: the [[simply connected topological space|simply connected]] [[translation group]], which is just $\mathbb{R}$ itself again, equipped with its canonical additive [[abelian group]] structure, and the [[discrete space|discrete]] [[quotient]] of this by the group of [[integers]], which is the [[circle group]]

$$
  U(1) = \mathbb{R}/\mathbb{Z}
  \,.
$$

Notice that it is the discrete and hence "quantized" nature of the [[integers]] that makes the [[real line]] become a [[circle]] here. This is not entirely a coincidence of terminology, but can be traced back to the heart of what is "quantized" about [[quantum mechanics]].

Namely, one finds that the [[Poisson bracket]] [[Lie algebra]] $\mathfrak{poiss}(X,\omega)$ of the classical [[observables]] on [[phase space]] is (for $X$ a [[connected topological space|connected]] [[manifold]]) a [[Lie algebra extension]] of the Lie algebra $\mathfrak{ham}(X)$ of [[Hamiltonian vector fields]] on $X$ by the [[line Lie algebra]]:

$$
  \mathbb{R} \longrightarrow \mathfrak{poiss}(X,\omega) \longrightarrow \mathfrak{ham}(X)
  \,.
$$

This means that under [[Lie integration]] the [[Poisson bracket]] turns into an [[central extension]] of the group of [[Hamiltonian symplectomorphisms]] of $(X,\omega)$. And either it is the fairly trivial non-compact extension by $\mathbb{R}$, or it is the interesting [[central extension]] by the [[circle group]] $U(1)$. For this non-trivial [[Lie integration]] to exist, $(X,\omega)$ needs to satisfy a quantization condition which says that it admits a [[prequantum line bundle]]. If so, then this $U(1)$-[[central extension]] of the group $Ham(X,\omega)$ of [[Hamiltonian symplectomorphisms]] exists and is called... the _[[quantomorphism group]]_ $QuantMorph(X,\omega)$:

$$
  U(1) \longrightarrow QuantMorph(X,\omega) \longrightarrow Ham(X,\omega)
  \,.
$$

While important, for some reason this group is not very well known, which is striking because it contains a small [[subgroup]] which is famous in [[quantum mechanics]]: the _[[Heisenberg group]]_.

More precisely, whenever $(X,\omega)$ itself has a [[Hamiltonian action|compatible]] [[group]] structure, notably if $(X,\omega)$ is just a [[symplectic vector space]] (regarded as a group under addition of vectors), then we may ask for the [[subgroup]] of the [[quantomorphism group]] which covers the (left) [[action]] of [[phase space]] $(X,\omega)$ on itself. This is the corresponding [[Heisenberg group]] $Heis(X,\omega)$, which in turn is a $U(1)$-[[central extension]] of the group $X$ itself:

$$
  U(1) \longrightarrow Heis(X,\omega) \longrightarrow X
  \,.
$$

At this point it is worth pausing for a second to note how the hallmark of [[quantum mechanics]] has appeared as if out of nowhere simply by applying [[Lie integration]] to the [[Lie algebra|Lie algebraic]] structures in [[classical mechanics]]:

if we think of [[Lie integration|Lie integrating]] $\mathbb{R}$ to the interesting [[circle group]] $U(1)$ instead of to the uninteresting [[translation group]] $\mathbb{R}$, then the name of its canonical [[basis]] element $1 \in \mathbb{R}$ is canonically "$i$", the imaginary unit. Therefore one often writes the above [[central extension]] instead as follows:

$$
  i \mathbb{R} \longrightarrow \mathfrak{poiss}(X,\omega) \longrightarrow \mathfrak{ham}(X,\omega)
$$

in order to amplify this. But now consider the simple special case where $(X,\omega) = (\mathbb{R}^2, d p \wedge d q)$ is the 2-dimensional [[symplectic vector space]] which is for instance the [[phase space]] of the [[particle]] propagating on the line. Then a canonical set of generators for the corresponding [[Poisson bracket]] [[Lie algebra]] consists of the linear functions $p$ and $q$ of classical mechanics textbook fame, together with the _constant_ function. Under the above Lie theoretic identification, this constant function is the canonical basis element of $i \mathbb{R}$, hence purely Lie theoretically it is to be called "$i$".

With this notation then the [[Poisson bracket]], written in the form that makes its [[Lie integration]] manifest, indeed reads

$$
  [q,p] = i
  \,.
$$

Since the choice of [[basis]] element of $i \mathbb{R}$ is arbitrary, we may rescale here the $i$ by any non-vanishing [[real number]] without changing this statement. If we write "$\hbar$" for this element, then the [[Poisson bracket]] instead reads

$$
  [q,p] = i \hbar
  \,.
$$


This is of course the hallmark equation for [[quantum physics]], if we interpret $\hbar$ here indeed as [[Planck's constant]]. We see it arises here merely by considering the non-trivial (the interesting, the non-simply connected) [[Lie integration]] of the [[Poisson bracket]]. 

This is only the beginning of the story of quantization, naturally understood and indeed "derived" from applying [[Lie theory]] to [[classical mechanics]]. From here the story continues. It is called the story of _[[geometric quantization]]_. We close this motivation section here by some brief outlook.

The [[quantomorphism group]] which is the non-trivial [[Lie integration]] of the [[Poisson bracket]] is naturally constructed as follows: given the [[symplectic form]] $\omega$, it is natural to ask if it is the [[curvature]] 2-form of a $U(1)$-[[principal connection]] $\nabla$ on [[complex line bundle]] $L$ over $X$ (this is directly analogous to [[Dirac charge quantization]] when instead of a [[symplectic form]] on [[phase space]] we consider the  the [[field strength]] 2-form of [[electromagnetism]] on [[spacetime]]). If so, such a connection $(L, \nabla)$ is called a _[[prequantum line bundle]]_ of the [[phase space]] $(X,\omega)$. The [[quantomorphism group]] is simply the [[automorphism group]] of the [[prequantum line bundle]], covering [[diffeomorphisms]] of the phase space (the [[Hamiltonian symplectomorphisms]] mentioned above).

As such, the [[quantomorphism group]] naturally [[action|acts]] on the [[space of sections]] of $L$. Such a [[section]] is like a [[wavefunction]], except that it depends on all of [[phase space]], instead of just on the "[[canonical coordinates]]". For purely abstract mathematical reasons (which we won't discuss here, but see at _[[motivic quantization]]_ for more) it is indeed natural to choose a "[[polarization]]" of [[phase space]] into [[canonical coordinates]] and [[canonical momenta]] and consider only those [[sections]] of the [[prequantum line bundle]] which depend only on the former. These are the actual _[[wavefunctions]]_ of [[quantum mechanics]], hence the _[[quantum states]]_. And the [[subgroup]] of the [[quantomorphism group]] which preserves these polarized sections is the group of exponentiated [[quantum observables]]. For instance in the simple case mentioned before where $(X,\omega)$ is the 2-dimensional [[symplectic vector space]], this is the [[Heisenberg group]] with its famous action by multiplication and differentiation operators on the space of complex-valued functions on the real line.




### Infinitesimal symmetries, Poisson bracket and Heisenberg algebra

#### Ordinary Poisson brackets


+-- {: .num_defn #PresymplecticManifold}
###### Definition

Let $X$ be a [[smooth manifol]]. A closed [[differential 2-form]] $\omega \in \Omega_{cl}^2(X)$ is a _[[symplectic form]]_ if it is non-degenerate in that the [[kernel]] of the operation of contracting with [[vector fields]]

$$
  \iota_{(-)}\omega \colon Vect(X) \longrightarrow \Omega^1(X)
$$

is trivial: $ker(\iota_{(-)}\omega) = 0$.

If $\omega$ is just closed with possibly non-trivial kernel, we call it a [[presymplectic form]]. (We do not require here the dimension of the kernel restricted to each tangent space to be constant.)

=--


+-- {: .num_defn #HamiltonianVectorField}
###### Definition

Given a [[presymplectic manifold]] $(X, \omega)$, then a _[[Hamiltonian]]_ for a [[vector field]] $v \in Vect(X)$ is a [[smooth function]] $H \in C^\infty(X)$ such that

$$
  \iota_{v} \omega = d H
  \,.
$$

If $v \in Vect(X)$ is such that there _exists_ at least one Hamiltonian for it then it is called a _[[Hamiltonian vector field]]_. Write

$$
  HamVect(X,\omega) \hookrightarrow Vect(X)
$$

for the $\mathbb{R}$-[[linear subspace]] of Hamiltonian vector fields among all [[vector fields]]

=--

+-- {: .num_remark}
###### Remark

When $\omega$ is symplectic then, evidently, there is a unique Hamiltonian vector field, def. \ref{HamiltonianVectorField}, associated with every Hamiltonian, i.e. every smooth function is then the Hamiltonian of precisely one Hamiltonian vector field (but two different Hamiltonians may still have the same Hamiltonian vector field uniquely associated with them). As far as [[prequantum geometry]] is concerned, this is all that the non-degeneracy condition that makes a closed 2-form be symplectic is for. But we will see that the definitions of [[Poisson brackets]] and of [[quantomorphism groups]] directly generalize also to the presymplectic situation, simply by considering not just Hamiltonian fuctions but pairs of a Hamiltonian vector field and a compatible Hamiltonian.

=--


+-- {: .num_defn #PoissonBracket}
###### Definition

Let $(X,\omega)$ be a [[presymplectic manifold]]. Write 

$$
  Ham(X,\omega) \hookrightarrow HamVect(X,\omega) \oplus C^\infty(X)
$$

for the [[linear subspace]] of the [[direct sum]] of [[Hamiltonian vector fields]], def. \ref{HamiltonianVectorField}, and [[smooth functions]] on those pairs $(v,H)$ for which $H$ is a [[Hamiltonian]] for $v$ 

$$
  Ham(X,\omega)
  \coloneqq
  \left\{
    (v,H) | \iota_v \omega = d H 
  \right\}
  \,.
$$


Define a [[bilinear map]] 

$$
  [-,-] \;\colon\;
  Ham(X,\omega) \otimes Ham(X,\omega)
  \longrightarrow
  Ham(X,\omega)
$$

by

$$
 ((v_1,H_1), (v_2,H_2)) \coloneqq ([v_1,v_2], \iota_{v_2}\iota_{v_1} \omega)
 \,,
$$

called the _[[Poisson bracket]]_, where $[v_1,v_2]$ is the standard Lie bracket on [[vector fields]]. Write

$$
  \mathfrak{Pois}(X,\omega)
  \coloneqq
  (Ham(X,\omega),[-,-])
$$

for the resulting [[Lie algebra]]. In the case that $\omega$ is symplectic, then $Ham(X,\omega) \simeq C^\infty(X)$ and hence in this case

$$
  \mathfrak{Pois}(X,\omega)
  \simeq
  (C^\infty(X),[-,-])
  \,.
$$


=--


### Finite symmetries


Throughout, let $\mathbb{G} \in Grp(\mathbf{H})$ be a [[braided ∞-group]] equipped with a [[Hodge filtration]]. Write $\mathbf{B}\mathbb{G}_{conn}\in $ for the corresponding [[moduli stack]] of [[differential cohomology]].

+-- {: .num_example #StandardChoiceOfBGconn}
###### Example

For $\mathbf{H} = $ [[Smooth∞Grpd]] we have $\mathbb{G} = \mathbf{B}^p (\mathbb{R}/\Gamma)$ for $\Gamma = \mathbb{Z}$ is the [[circle n-group|circle (p+1)-group]]. Equipped with its standard Hodge filtration this gives $\mathbf{B}\mathbb{G}_{conn} = \mathbf{B}^p U(1)_{conn}$ presented via the [[Dold-Kan correspondence]] by the [[Deligne complex]] in degree $(p+2)$.

=--


+-- {: .num_defn #DifferentialConcretification}
###### Definition

For $X \in \mathbf{H}$, for 
 write 

$$
  conc \colon [X,\mathbf{B}\mathbb{G}_{conn}] \longrightarrow \mathbb{G}\mathbf{Conn}(X)
$$



for the [[differential concretification]] of the [[internal hom]].

=--

This is the proper [[moduli stack]] of $\mathbb{G}$-[[principal ∞-connections]] on $X$ in that a family $U \longrightarrow \mathbb{G}\mathbf{Conn}(X)$ is a _vertical_ $\mathbb{G}$-principal $\infty$-connection on $U \times X\to U$.

+-- {: .num_example }
###### Example

For $\mathbf{H} = $[[Smooth∞Grpd]] or =[[FormalSmooth∞Grpd]], for $\mathbb{G} = \mathbf{B}^p U(1)$ the [[circle n-group|circle (p+1)-group]] with its standard Hodge filtration as in example \ref{StandardChoiceOfBGconn}, then for $X$ any [[smooth manifold]] or [[formal smooth manifold]], $(\mathbf{B}^p U(1))\mathbf{Conn}(X)$ is presented via the [[Dold-Kan correspondence]] by the sheaf $U \mapsto Ch_\bullet$ of [[vertical differential form|vertical]] [[Deligne complexes]] on $U \times X$ over $U$. 

=--

+-- {: .num_defn }
###### Proposition

For $\mathbb{G} \simeq \mathbf{B}\mathbb{G}'$ then the [[loop space object]] of the moduli stack of $\mathbb{G}$-principal $\infty$-connections on $X$ is the moduli stack of [[flat ∞-connections]] with gauge group $\Omega \mathbb{G}$

$$
  \Omega_0 (\mathbb{G}\mathbf{Conn}(X))
  \simeq
  (\Omega\mathbb{G})\mathbf{FlatConn}(X)
  \,.
$$

=--

+-- {: .num_prop #PrecompositionActionOnGConn}
###### Proposition

The canonical [[precomposition action|precomposition]] [[∞-action]] of the [[automorphism ∞-group]] $\mathbf{Aut}(X)$ on $[X,\mathbf{B}\mathbb{G}_{conn}]$ passes along $conc$ to an [[∞-action]] on $\mathbb{G}\mathbf{Conn}(X)$.

=--

+-- {: .num_defn #QuantomorphismGroup}
###### Definition


Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$ there are the following concepts in [[schreiber:Higher geometric prequantum theory|higher geometric prequantum theory]].


1. The **[[quantomorphism ∞-group]]**is the [[stabilizer ∞-group]] of $\nabla \in \mathbb{G}\mathbf{Conn}(X)$, def. \ref{DifferentialConcretification}, under the $\mathbf{Aut}(X)$-action of \ref{PrecompositionActionOnGConn};

   $$
     \mathbf{QuantMorph}(X,\nabla)
     \coloneqq
     \mathbf{Stab}_{\mathbf{Aut}(X)}(conc(\nabla))
     \,.
   $$

1. The **[[Hamiltonian symplectomorphism ∞-group]]** 


   $$
     \mathbf{HamSymp}(X,\nabla) \longrightarrow \mathbf{Aut}(X)
   $$ 

   is the [[1-image]] of the canonical morphism $\mathbf{QuantMorph}(X,\nabla) \longrightarrow \mathbf{Aut}(X)$ from remark \ref{StabilizerGroupAsFactorization}.

1. A **[[Hamiltonian action]]** of an [[∞-group]] $G$ on $(X,\nabla)$ is an [[∞-group]] homomorphism 

   $$
     \rho \colon G \longrightarrow \mathbf{HamSymp}(X,\nabla)
      \;
   $$


1. An **[[∞-moment map]]**  is an $\infty$-group homomorphism 

   $$
     G \longrightarrow \mathbf{QuantMorph}(X,\nabla)
   $$

1. The **[[Heisenberg ∞-group]]** for a given Hamiltonian $G$-action $\rho$ is the [[homotopy pullback]] 

   $$
     \mathbf{Heis}_G(X,\nabla) \coloneqq \rho^\ast \mathbf{QuantMorph}(X,\nabla)
     \,.
   $$

=--

+-- {: .num_example }
###### Example

For $\mathbf{H} = $ [[Smooth∞Grpd]], for $X \in SmoothMfd \hookrightarrow \mathbf{H}$ a [[smooth manifold]] and for $\nabla$ a [[prequantum line bundle]] on $X$, then $\mathbf{QuantMorph}(X,\nabla)$ is Soriau's [[quantomorphism group]] covering the [[Hamiltonian diffeomorphism]] group. In the case that $(X, F_\nabla)$ is a [[symplectic vector space]] regarded as a linear symplectic manifold with Hamiltonian action on itself by translation, then $\mathbf{Heis}_{V}(X,\nabla)$ is the traditional [[Heisenberg group]].

=--



+-- {: .num_remark }
###### Remark

Since $\mathbf{HamSymp}(X,\nabla)\hookrightarrow \mathbf{Aut}(X)$ is by construction a [[1-monomorphism]], then given any $G$-action $\rho \colon G \longrightarrow \mathbf{Aut}(X)$ on $X$, not necessarily Hamiltonian, then the homotopy pullback $\rho^\ast \mathbf{QuantMorph}(X,\nabla)$ is the Heisenberg ∞-group of the maximal sub-$\infty$-group of $G$ which does act via Hamiltonian symplectomorphisms. Therefore we will also write $\mathbf{Heis}_G(X,\nabla)$ in this case.


=--

The following is the refinement of the [[Kostant-Souriau extension]] to [[higher differential geometry]]

+-- {: .num_prop #TheQuantomorphismGroupExtension}
###### Proposition

Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, the there is a [[homotopy fiber sequence]] of the form

1. if $\mathbb{G}$ is [[0-truncated]] then

   $$
     \array{
        \mathbb{G}\mathbf{ConstFunct}(X)
        &\longrightarrow&
        \mathbf{QuantMorph}(X,\nabla)
        \\
        && \downarrow
        \\
        && \mathbf{HamSymp}(X,\nabla)
        &\stackrel{\mathbf{KS}}{\longrightarrow}&
        \mathbf{B} (\mathbb{G}\mathbf{ConstFunct}(X))
    }
   $$


1. if $\mathbb{G} \simeq \mathbf{B}\mathbb{G}'$ then

   $$
     \array{
        (\Omega \mathbb{G})\mathbf{FlatConn}(X)
        &\longrightarrow&
        \mathbf{QuantMorph}(X,\nabla)
        \\
        && \downarrow
        \\
        && \mathbf{HamSymp}(X,\nabla)
        &\stackrel{\mathbf{KS}}{\longrightarrow}&
        \mathbf{B} ((\Omega \mathbb{G})\mathbf{Conn}(X))
    }
   $$

exhibiting the [[quantomorphism ∞-group]] as an [[∞-group extension]] of the [[Hamiltonian symplectomorphism ∞-group]] by the [[moduli stack]] of $\Omega \mathbb{G}-$[[flat ∞-connections]], classified by a [[cocycle]] $\mathbf{KS}$.

=--

+-- {: .num_example }
###### Example

In $\mathbf{H} = $ [[Smooth∞Grpd]], let $\mathbb{G} = \mathbf{B}^p U(1)$ be the [[circle n-group|circle (p+2)-group]] and let $X \in SmoothMfd \hookrightarrow Smooth \infty Grpd$ be [[n-connected topological space|(p+1)-connected]], then $(\mathbf{B}^p U(1))\mathbf{FlatConn}(X)\simeq \mathbf{B}^{p+1}U(1)$. Hence here prop. \ref{TheQuantomorphismGroupExtension} gives

   $$
     \array{
        \mathbf{B}^{p}U(1)
        &\longrightarrow&
        \mathbf{QuantMorph}(X,\nabla)
        \\
        && \downarrow
        \\
        && \mathbf{HamSymp}(X,\nabla)
        &\stackrel{\mathbf{KS}}{\longrightarrow}&
        \mathbf{B}^{p+1}U(1)
    }
  $$
 
=--


+-- {: .num_cor #KSExtensionForHeis}
###### Corollary

Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, and for $\rho \colon G \longrightarrow$ a $G$-[[Hamiltonian action]], then there is a [[homotopy fiber sequence]]

1. if $\mathbb{G}$ is [[0-truncated]] then

   $$
     \array{
        \mathbb{G}\mathbf{ConstFunct}(X)
        &\longrightarrow&
        \mathbf{Heis}_G(X,\nabla)
        \\
        && \downarrow
        \\
        && \mathbf{HamSymp}(X,\nabla)
        &\stackrel{\mathbf{KS}(\rhp)}{\longrightarrow}&
        \mathbf{B} (\mathbb{G}\mathbf{ConstFunct}(X))
    }
   $$


1. if $\mathbb{G} \simeq \mathbf{B}\mathbb{G}'$ then

   $$
     \array{
        (\Omega \mathbb{G})\mathbf{FlatConn}(X)
        &\longrightarrow&
        \mathbf{Heis}_G(X,\nabla)
        \\
        && \downarrow
        \\
        && \mathbf{HamSymp}(X,\nabla)
        &\stackrel{\mathbf{KS}(\rho)}{\longrightarrow}&
        \mathbf{B} ((\Omega \mathbb{G})\mathbf{Conn}(X))
    }
   $$

exhibiting the [[Heisenberg ∞-group]] as an [[∞-group extension]] of the [[Hamiltonian symplectomorphism ∞-group]] by the [[moduli stack]] of $\Omega \mathbb{G}-$[[flat ∞-connections]], classified by a [[cocycle]] $\mathbf{KS}(\rho)$.


The class of the [[cocycle]] $\mathbf{KS}(\rho)$ is the [[obstruction]] to prequantizing $\rho$ to a [[moment map]] (the _[[classical anomaly]]_ of $\rho$); and the the [[Heisenberg ∞-group]] [[∞-group extension|extension]] of $G$ is the universal cancellation of this anomaly.

=--


## References

* {#FRS13a} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_, ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))


* {#FRS13b} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_, Homology, Homotopy and Applications, Volume 16 (2014) Number 2, p. 107 &#8211; 142 ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))