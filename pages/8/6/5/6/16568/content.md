

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




### Infinitesimal symmetries
 {#InfinitesimalSymmetries}
 
We discuss here the infinitesimal symmetries of prequantum geometries, exhibited by the [[Poisson bracket]] Lie algebra and its higher analogs, the [[Poisson bracket Lie n-algebra]].

#### Poisson brackets and Heisenberg algebra
 {#PoissonBracketHeisenbergAlgebraInfinitesimalQuantomorphisms}

We discuss the traditional definition of the [[Poisson bracket]] of a ([[presymplectic manifold|pre-]])[[symplectic manifold]], highlighting how conceptually it may be understood as the algebra of infinitesimal symmetries of any of its [[prequantizations]].

+-- {: .num_defn #PresymplecticManifold}
###### Definition

Let $X$ be a [[smooth manifold]]. A closed [[differential 2-form]] $\omega \in \Omega_{cl}^2(X)$ is a _[[symplectic form]]_ if it is non-degenerate in that the [[kernel]] of the operation of contracting with [[vector fields]]

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
  \iota_{v} \omega + d H = 0
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
    (v,H) | \iota_v \omega + d H  = 0
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
 [(v_1,H_1), (v_2,H_2)] \coloneqq ([v_1,v_2], \iota_{v_2}\iota_{v_1} \omega)
 \,,
$$

called the _[[Poisson bracket]]_, where $[v_1,v_2]$ is the standard Lie bracket on [[vector fields]]. Write

$$
  \mathfrak{poiss}(X,\omega)
  \coloneqq
  (Ham(X,\omega),[-,-])
$$

for the resulting [[Lie algebra]]. In the case that $\omega$ is symplectic, then $Ham(X,\omega) \simeq C^\infty(X)$ and hence in this case

$$
  \mathfrak{poiss}(X,\omega)
  \simeq
  (C^\infty(X),[-,-])
  \,.
$$

=--

+-- {: .num_example #HeisenbergAlgebraOfSymplecticVectorSpace}
###### Example

Let $X = \mathbb{R}^{2n}$ and let $\omega = \sum_{i = 1}^n d p_i \wedge d q^i$ for $\{q^i\}_{i = 1}^n$ the [[canonical coordinates]] on one copy of $\mathbb{R}^n$ and $\{p_i\}_{i = 1}^n$ that on the other ("[[canonical momenta]]"). Hence let $(X,\omega)$ be a [[symplectic vector space]] of dimension $2n$, regarded as a [[symplectic manifold]].

Then $Vect(X)$ is [[linear span|spanned]] over $C^\infty(X)$ by the canonical bases vector fields $\{\partial_{q^i}, \partial_{p^i}\}$. These basis vector fields are manifestly [[Hamiltonian vector fields]] via

$$
  \iota_{\partial_{q^i}} \omega = - d p_i
$$

$$
  \iota_{\partial_{p_i}} \omega = + d q^i
  \,.  
$$

Moreover, since $X$ is [[connected topological space|connected]], these Hamiltonians are unique up to a choice of constant function. Write $\mathbf{i} \in C^\infty(X)$ for the unit constant function, then the nontrivial Poisson brackets between the basis vector fields are 

$$
  [q^i, p_j]
  \coloneqq
  [(-\partial_{p_i}, q^i), (\partial_{q^j}, p_j)]
  =
  -
  \delta_j^i
  (0, \mathbf{i})
  =
  -
  \delta_j^i
  \mathbf{i}
  \,.
$$

This is called the [[Heisenberg algebra]].

More generally, the [[Hamiltonian vector fields]] corresponding to [[quadratic Hamiltonians]], i.e. degree-2 [[polynomials]] in the $\{q^i\}$ and $\{p_i\}$, generate the [[affine symplectic group]] of $(X,\omega)$. The freedom to add constant terms to Hamiltonians gives the [[extended affine symplectic group]].

=--

#### Infinitesimal quantomorphisms

Example \ref{HeisenbergAlgebraOfSymplecticVectorSpace} serves to motivate a more conceptual origin of the definition of the Poisson bracket in def. \ref{PoissonBracket}.

+-- {: .num_example }
###### Example

Write

$$
  \theta \coloneqq \sum_{i = 1}^n p_i d q_i \in \Omega^1(\mathbb{R}^{2n})
$$

for the canonical choice of [[differential 1-form]] satisfying 

$$
  d \theta = \omega
  \,.
$$

If we regard $\mathbb{R}^{2n} \simeq T^\ast \mathbb{R}^n$ as the [[cotangent bundle]] of the [[Cartesian space]] $\mathbb{R}^n$, then this is what is known as the [[Liouville-Poincaré 1-form]].

Since $\mathbb{R}^{2n}$ is [[contractible topological space|contractible]] as a [[topological space]], every [[circle bundle]] over it is necessarily trivial, and hence any choice of 1-form such as $\theta$ may canonically be thought of as being a [[connection on a bundle|connection]] on the trivial $U(1)$-[[principal bundle]]. As such this $\theta$ is a [[prequantization]] of $(\mathbb{R}^{2n}, \sum_{i=1}^n d p_i \wedge d q^i)$.

Being thus a [[circle bundle with connection]], $\theta$ has more symmetry than its [[curvature]] $\omega$ has: for $\alpha \in C^\infty(\mathbb{R}^{2n}, U(1))$ any smooth function, then 

$$
  \theta \mapsto \theta + d\alpha
$$

is the [[gauge transformation]] of $\theta$, leading to a different but equivalent [[prequantization]] of $\omega$.

Hence while a [[vector field]] $v$ is said to preserve $\omega$ (is a [[symplectic vector field]]) if the [[Lie derivative]] of $\omega$ along $v$ vanishes

$$
  \mathcal{L}_v \omega = 0 
$$

in the presence of a choice for $\theta$ the right condition to ask for is that there is $\alpha$ such that

$$
  \mathcal{L}_v \theta = d \alpha
  \,.
$$

=--

For more on this see also at _[[prequantized Lagrangian correspondence]]_.

Notice then the following basic but important fact.

+-- {: .num_prop}
###### Proposition

For $(X,\omega)$ a [[presymplectic manifold]] and $\theta \in \Omega^1(X)$ a 1-form such that $d \theta = \omega$ then for $(v,\alpha) \in Vect(X)\oplus C^\infty(X)$ the condition $\mathcal{L}_v \theta = d \alpha$ is equivalent to the condition that makes 

$$
  H \coloneqq \iota_v \theta - \alpha 
$$ 

a [[Hamiltonian]] for $v$ according to def. \ref{HamiltonianVectorField}:

$$
  \mathcal{L}_v \theta = d \alpha
    \;\;\;\Leftrightarrow\;\;\;  
  \iota_v \omega + d (\underset{H}{\underbrace{\iota_v \theta - \alpha}}) = 0
  \,.
$$

Moreover, the [[Poisson bracket]], def. \ref{PoissonBracket}, between two such Hamiltonian pairs $(v_i, \alpha_i -\iota_v \theta)$ is equivalently given by the skew-symmetric [[Lie derivative]] of the corresponding vector fields on the $\alpha_i$:

\[
  \label{EquationForLieHomomorphism}
  \iota_{[v_1,v_2]} \theta
  -
  \iota_{v_2}\iota_{v_1}\omega 
  = 
  \mathcal{L}_{v_1} \alpha_2 - \mathcal{L}_{v_2} \alpha_1
\]

=--

+-- {: .proof}
###### Proof

Using [[Cartan's magic formula]] and by the prequantization condition $d \theta = \omega$ the we have

$$
  \begin{aligned}
    \mathcal{L}_v \theta &= \iota_v d\theta + d \iota_v \theta
    \\
    & =  \iota_v\omega + d \iota_v \theta
  \end{aligned}
  \,.
$$

This gives the first statement. For the second we first use the formula for the [[de Rham differential]] and then again the definition of the $\alpha_i$

$$
  \begin{aligned}
    \iota_{v_2}\iota_{v_1} \omega
    & =
    \iota_{v_2}\iota_{v_1} d\theta
    \\
    & =
    \iota_{v_1} d \iota_{v_2} \theta
    -
    \iota_{v_2} d \iota_{v_1} \theta
    -
    \iota_{[v_1,v_2]} \theta
    \\
     & = 
    \iota_{v_1} d \alpha_2 - \iota_{v_1} \iota_{v_2}\omega
    - \iota_{v_2} d \alpha_1 + \iota_{v_2} \iota_{v_1}\omega 
    -
    \iota_{[v_1,v_2]} \theta
    \\
     & = 
    2 \iota_{v_2} \iota_{v_1}\omega 
    + \mathcal{L}_{v_1} \alpha_2
     -\mathcal{L}_{v_2} \alpha_1
    -
    \iota_{[v_1,v_2]} \theta
 \end{aligned}
  \,.
$$

=--



+-- {: .num_cor #EquivalenceBetweenPoissonBracketAndInfinQuantomorphism}
###### Corollary

For $(X,\omega)$ a [[presymplectic manifold]] with $\theta \in \Omega^1(X)$ such that $d \theta = \omega$, consider the [[Lie algebra]]

$$
  \mathfrak{quantmorph}(X,\theta)
  =
  \left\{
    (v,\alpha) | \mathcal{L}_v \theta = d \alpha
  \right\}
  \subset
  Vect(X) \oplus C^\infty(X)
$$

with Lie bracket

$$
  [(v_1,\alpha_1), (v_2,\alpha_2)] = ([v_1,v_2], \mathcal{L}_{v_1}\alpha_2 - \mathcal{L}_{v_2}\alpha_1)
  \,.
$$

Then by (eq:EquationForLieHomomorphism) the linear map

$$
  (v,H) \mapsto (v, \iota_v \theta - H)
$$

is an [[isomorphism]] of [[Lie algebras]]

$$
  \mathfrak{poiss}(X,\omega) 
    \stackrel{\simeq}{\longrightarrow}
  \mathfrak{quantmorph}(X,\theta)
$$

from the [[Poisson bracket Lie algebra]], def. \ref{PoissonBracket}.

=--

This shows that for exact pre-symplectic forms the Poisson bracket Lie algebra is secretly the Lie algebra of infinitesimal symmetries of any of its [[prequantizations]]. In fact this holds true also when the pre-symplectic form is not exact:

+-- {: .num_defn #CechDelignePrequantizationAnditsInfinitesimalAutomorpisms}
###### Definition

For $(X,\omega)$ a [[presymplectic manifold]], a [[Cech cohomology|Cech]]-[[Deligne cohomology|Deligne]] [[cocycle]] 

$$
  (X,\overline{\theta}) \coloneqq (X,\{U_i\},\{g_{i j}, \theta_i\})
$$ 

for a  _[[prequantization]]_ of $(X,\omega)$ is

1. an [[open cover]] $\{U_i \to X\}_i$;

1. 1-forms $\{\theta_i \in \Omega^1(U_i)\}$;

1. smooth function $\{g_{i j} \in C^\infty(U_{i j}, U(1))\}$

such that

1. $d \theta_i = \omega|_{U_i}$ on all $U_i$;

1. $\theta_j = \theta_i + d log g_{ij}$ on all $U_{i j}$;

1. $g_{i j} g_{j k} = g_{i k}$ on all $U_{i j k}$.

The _quantomorphism Lie algebra_ of $\overline{\theta}$ is 

$$
  \mathfrak{quantmorph}(X,\overline{\theta})
  =
  \left\{
    (v, \{\alpha_i\})
    |
    \mathcal{L}_v log g_{i j} = \alpha_j - \alpha_i
    \,,
    \mathcal{L}_v \theta_i = d \alpha_i
  \right\}
  \subset
  Vect(X) \oplus \left(\underset{i}{\bigoplus} C^\infty(U_i)\right)
$$

with bracket

$$
  [(v_1, \{(\alpha_1)_i\}), (v_2, \{(\alpha_2)_i\})]
  \coloneqq
  ([v_1,v_2], \{\mathcal{L}_{v_1}(\alpha_2)_i - \mathcal{L}_{v_2} (\alpha_1)_i\})
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $(X,\omega)$ a [[presymplectic manifold]] and 
$(X,\{U_i\},\{g_{i j}, \theta_i\})$ a [[prequantization]],
def. \ref{CechDelignePrequantizationAnditsInfinitesimalAutomorpisms}, the linear map

$$
  (v,H) \mapsto (v,  \{\iota_v \theta_i - H|_{U_i}\})
$$

constitutes an [[isomorphism]] of [[Lie algebras]]

$$
  \mathfrak{poiss}(X,\omega)
  \stackrel{\simeq}{\longrightarrow}
  \mathfrak{quantmorph}(X,\overline{\theta})
$$

between the [[Poisson bracket]] algebra of def. \ref{PoissonBracket} and that of infinitesimal quantomorphisms, def. \ref{CechDelignePrequantizationAnditsInfinitesimalAutomorpisms}.

=--

+-- {: .proof}
###### Proof

The condition $\mathcal{L}_v log g_{i j} = \alpha_j - \alpha_i$
on the infinitesimal quantomorphisms, together with the Cech-Deligne cocycle condition $d log g_{i j} = \theta_j - \theta_i$ says that on $U_{i j}$

$$
  \iota_v \theta_j - \alpha_j = \iota_v \theta_i - \alpha_i
$$

and hence that there is a globally defined function $H \in C^\infty(X)$ such that $\iota_v \theta_i - \alpha_i = H|_{U_i}$. This shows that the map is an isomrophism of vector spaces.

Now over each $U_i$ the the situation for the brackets is just that of corollary
\ref{EquivalenceBetweenPoissonBracketAndInfinQuantomorphism} implied by (eq:EquationForLieHomomorphism), hence the morphism is a Lie homomorphism.

=--

#### The Kostant-Souriau extension

The following fact is immediate, but important.

+-- {: .num_prop #KostantSouriauExtension}
###### Proposition

Given a [[presymplectic manifold]] $(X,\omega)$, then the 
[[Poisson bracket]] [[Lie algebra]] $\mathfrak{poiss}(X,\omega)$,
def. \ref{PoissonBracket}, is a [[central extension|central]]
[[Lie algebra extension]] of the algebra of [[Hamiltonian vector fields]],
def. \ref{HamiltonianVectorField}, by the degree-0 [[de Rham cohomology]]
group of $X$: there is a [[short exact sequence]] of Lie algebras

$$
  0 \to 
  H^0(X)
  \stackrel{}{\longrightarrow}
  \mathfrak{poiss}(X,\omega)
  \stackrel{}{\longrightarrow}
  HamVect(X,\omega)
  \to 
  0
  \,.
$$

Hence when $X$ is [[connected topological space|connected]], then $\mathfrak{poiss}(X,\omega)$ is an $\mathbb{R}$-extension of the Hamiltonian vector fields:

$$
  0 \to 
  \mathbb{R}
  \stackrel{}{\longrightarrow}
  \mathfrak{poiss}(X,\omega)
  \stackrel{}{\longrightarrow}
  HamVect(X,\omega)
  \to 
  0
  \,.
$$

Moreover, given any choice of [[split exact sequence|splitting]] of the underlying short exact sequence of [[vector spaces]] as $\mathfrak{pois}(X,\omega) \simeq_{vs} HamVect(X,\omega)\oplus H^0(X)$, which is equivalently a choice of Hamitlonian $H_v$ for each Hamiltonian vector field $v$, the [[Lie algebra cohomology]] 2-[[cocycle]] which classifies this extension is 

$$
  (v_1, v_2) = \iota_{v_2}\iota_{v_1}\omega - H_{[v_1,v_2]}
  \,.
$$


=--

+-- {: .proof}
###### Proof

The morphism $\mathfrak{poiss}(X,\omega) \to HamVect(X,\omega)$
is on elements given just by projection onto the direct summand
of vector fields, taking a Hamiltonian pair $(v,H)$ to $v$.
This is surjective by the very definition of $HamVect(X,\omega)$,
in fact $HamVect(X,\omega)$ is the [[image]] of this map regarded
as a morphism $\mathfrak{poiss}(X,\omega) \longrightarrow Vect(X)$.
Moreover, the [[kernel]] of this projection is manifestly the
space of Hamiltonian pairs of the form $(v = 0,H)$. By the 
defining constraint $\iota_v \omega = d H$ these are precisely the 
pairs for which $d H = 0$. This gives the short exact sequence as stated.

Generally, given a Lie algebra $\mathfrak{g}$ and an $\mathbb{R}$-valued 2-cocycle $\mu_2$
in [[Lie algebra cohomology]], then the [[Lie algebra extension]] that it classifies is $\hat \mathfrak{g} =_{vs} \mathfrak{g}\oplus \mathbb{R}$ with bracket

$$
  [(x_1,a_1), (x_2,x_2)] = ([x_1,x_2], \mu_2(a_1,a_2))
  \,.
$$

Applied to the case at hand, given a choice of splitting $v\mapsto (v,H_v)$ this yields

$$
  [(v_1,H_{v_1} + a_1), (v_2, H_{v_2} + a_2) ]
  =
  ([v_1,v_2], H_{[v_1,v_2]} + \iota_{v_2}\iota_{v_1}\omega - H_{[v_1,v_2]})
  =
  ([v_1,v_2], \iota_{v_2}\iota_{v_1}\omega )
  \,.
$$

=--

+-- {: .num_example}
###### Example

Consider again example \ref{HeisenbergAlgebraOfSymplecticVectorSpace} where $(X,\omega) = (\mathbb{R}^{2n}, d p_i \wedge d q^i)$ is a [[symplectic vector space]] and where we restrict along the inclusion of the translation vector fields to get the [[Heisenberg algebra]]. 
Then the KS-extension of prop. \ref{KostantSouriauExtension} also pulls back:

$$
  \array{
    H_{dR}^0(X) &\longrightarrow& H_{dR}^0(X)
    \\
    \downarrow && \downarrow
    \\
    \mathfrak{heis}(X,\omega) &\longrightarrow& \mathfrak{poiss}(X,\omega)
    \\
    \downarrow && \downarrow
    \\
    \mathbb{R}^{2 n}
    &\longrightarrow&
    HamVect(X,\omega)
  }
  \,.
$$

The [[Lie algebra cohomology]] 2-[[cocycle]] which classifiesthe Kostant-Souriau extension, $\iota_{(-)}\iota_{(-)}\omega$ manifestly restricts to the Heisenberg cocycle  $(q^i, p_j) = \delta^i_j$.


=--



#### Interlude: $L_\infty$-algebras

Recall the definition of [[L-∞ algebras]].

For $V$ a [[graded vector space]], for $v_i \in V_{\vert v_i\vert}$ homogenously graded elements, and for $\sigma$ a [[permutation]] of $n$ elements, write
$\chi(\sigma, v_1, \cdots, v_n)\in \{-1,+1\}$ for the product of the [[signature of a permutation|signature of the permutation]] with a factor of $(-1)^{\vert v_i \vert \vert v_j \vert}$ for each interchange of neighbours $(\cdots v_i,v_j, \cdots )$ to $(\cdots v_j,v_i, \cdots )$ involved in the permutation.


+-- {: .num_defn #LInfinityDefinitionViaGeneralizedJacobiIdentity}
###### Definition

An $L_\infty$-algebra is 

1. a [[graded vector space]] $V$;

1. for each $n \in \mathbb{N}$ a [[multilinear map]] called the _$n$-ary bracket_

   $l_n(\cdots) \coloneqq [-,-, \cdots, -] \colon V^{\wedge n} \to V$
  
   of degree $n-2$
  
such that 

1. each $l_n$ is graded antisymmetric, in that for every [[permutation]] $\sigma$ and homogeneously graded elements $v_i \in V_{\vert v_i \vert}$ then

   $$
     l_n(v_{\sigma(1)}, v_{\sigma(2)},\cdots ,v_{\sigma(n)}) 
     = 
     \chi(\sigma,v_1,\cdots, v_n) \cdot l_n(v_1, v_2, \cdots v_n)

   $$

1. the _generalized [[Jacobi identity]]_ holds:

   \[
     \label{LInfinityJacobiIdentity}
     \sum_{i+j = n+1} 
     \sum_{\sigma \in UnShuff(i,n-i)}
     \chi(\sigma,v_1, \cdots, v_m)
     (-1)^{i(j-1)}
      l_{j} \left(
        l_i \left( v_{\sigma(1)}, \cdots, v_{\sigma(i)} \right),
        v_{\sigma(i+1)} , \cdots , v_{\sigma(n)}
      \right)
     = 0
     \,,
   \]

   for all $n$, all and homogeneously graded elements $v_i \in V_i$ (here the inner sum runs over all $(i,j)$-[[unshuffles]] $\sigma$).

=--

There are various different conventions on the gradings possible, which lead to similar formulas with different signs.


+-- {: .num_example }
###### Example

In lowest degrees the generalized Jacobi identity says that

1. for $n = 1$: the unary map $\partial \coloneqq l_1$ squares to 0:

   $$
     \partial (\partial(v_1)) = 0
   $$

1: for $n = 2$: the unary map $\partial$ is a graded [[derivation]] of the binary map

   $$
     - [\partial v_1, v_2] 
     - (-1)^{\vert v_1 \vert \vert v_2 \vert}
     [\partial v_2, v_1]
     +
     \partial [v_1, v_2]
     =
     0
   $$

   hence
 
   $$
     \partial [v_1, v_2] =  [\partial v_1, v_2] + (-1)^{\vert v_1 \vert}[v_1, \partial v_2]
     \,.
   $$

=--

+-- {: .num_example }
###### Example

When all higher brackets vanish, $l_{k \gt 2}= 0$ then for $n = 3$: 

$$
  [[v_1,v_2],v_3] 
  +
  (-1)^{\vert v_1 \vert (\vert v_2 \vert + \vert v_3 \vert)}
  [[v_2,v_3],v_1]
  +
  (-1)^{\vert v_2 \vert (\vert v_1 \vert + \vert v_3 \vert)}
  [[v_1,v_3],v_2]
  =
  0
$$

this is the graded [[Jacobi identity]]. So in this case the $L_\infty$-algebra
is equivalently a [[dg-Lie algebra]].

=--

+-- {: .num_example }
###### Example

When $l_3$ is possibly non-vanishing, then on elements $x_i$ on which $\partial = l_1$ vanishes then the generalized Jacobi identity for $n = 3$ gives

$$
  [[v_1,v_2],v_3] 
  +
  (-1)^{\vert v_1 \vert (\vert v_2 \vert + \vert v_3 \vert)}
  [[v_2,v_3],v_1]
  +
  (-1)^{\vert v_2 \vert (\vert v_1 \vert + \vert v_3 \vert)}
  [[v_1,v_3],v_2]
  =
  - \partial [v_1, v_2, v_3]
  \,.
$$

This shows that the Jacobi identity holds up to an "exact" term, hence up to homotopy.

=--

+-- {: .num_prop #LInfinityTruncation}
###### Proposition

On connective $L_\infty$-algebras (those whose underlying chain complex is concentrated in non-negative degrees), passage to degree-0 [[chain homology]] constitutes a [[functor]] ("[[n-truncated object of an (infinity,1)-category|0-truncation]]") to plain [[Lie algebras]]

$$
  \tau_0 \coloneqq H^0 \colon L_\infty Alg_{\geq 0} \longrightarrow LieAlg
  \,.
$$

=--


#### Higher Poisson brackets and higher Heisenberg algebra

In the discussion [above](PoissonBracketHeisenbergAlgebraInfinitesimalQuantomorphisms) we amplified that the definition of the [[Poisson bracket]] of a [[symplectic form]] has an immediate generalization to [[presymplectic forms]], hence to any closed [[differential 2-form]]. This naturally suggests to ask for higher analogs of this bracket for the case of of closed [[differential form|differential (p+2)-forms]] $\omega \in \Omega^{p+2}(X)$ for $p \gt 0$.

Indeed, the natural algebraic form of definition \ref{HamiltonianVectorField} of Hamiltonian vector fields makes immediate sense for higher $p$, with the Hamiltonians $H$ now being $p$-forms, and the natural algebraic form of the binary Poisson bracket of def. \ref{PoissonBracket}  makes immediate sense as a bilinear pairing for any $p$:

$$
 [(v_1, H_1), (v_2, H_2)] 
   \coloneqq
 ([v_1,v_2], \iota_{v_2} \iota_{v_1} \omega)
 \,.
$$

However, one finds that for $p \gt 0$ then this bracket does not satisfy the [[Jacobi identity]]. On the other hand, the failure of the Jacobi identity turns out to be an exact form, and hence in the spirit of regarding the shift of a differential form by a de Rham differential as a [[homotopy]] or [[gauge transformation]] this suggests that the bracket might still give a Lie algebra upto higher [[coherence|coherent]] homotopy, called a _[[strong homotopy Lie algebra]]_ or _[[L-∞ algebra]]_. This turns out to indeed be the case ([Rogers 10](#Rogers10)).


+-- {: .num_defn #PrenplecticManifold}
###### Definition

For $p \in \mathbb{N}$, we say that a _[[pre-n-plectic manifold|pre-(p+1)-plectic manifold]]_ is a [[smooth manifold]] $X$ equipped with a closed degree-$(p+2)$ [[differential form]] $\omega \in \Omega^{p+2}(X)$.

This is called an [[n-plectic manifold|(p+1)-plectic manifold]] if the [[kernel]] of the contraction map

$$
  \iota_{(-)} \colon Vect(X) \longrightarrow \Omega^{p+1}(X)
$$

is trivial.

=--

+-- {: .num_defn #HamiltonianFormsAndVectorFields}
###### Definition

Given a pre-$(p+1)$-plectic manifold $(X,\omega)$, def. \ref{PrenplecticManifold}, write 

$$
  Ham^{p}(X) \subset Vect(X) \oplus \Omega^{p}(X)
$$

for the subspace of the [[direct sum]] of [[vector fields]] $v$ on $X$ and [[differential n-form|differential p-forms]] $J$ on $X$ satisfying


$$
  \iota_v  \omega + d J = 0
  \,.
$$

We call these the _pairs of [[Hamiltonian forms]] with their [[Hamiltonian vector fields]]_.

=--

+-- {: .num_defn #PoissonBracketLienAlgebra}
###### Definition

Given a pre-$(p+1)$-plectic manifold $(X,\omega)$, def. \ref{PrenplecticManifold}, 
define an [[L-∞ algebra]] $\mathfrak{poiss}(X,\omega)$, to be called the _[[Poisson bracket Lie (p+1)-algebra]]_ as follows.

The underlying [[chain complex]] is the truncated [[de Rham complex]] ending in Hamiltonian forms as in def. \ref{HamiltonianFormsAndVectorFields}:

$$
  \Omega^0(X)
  \stackrel{d}{\to}
  \Omega^1(X)
  \stackrel{d}{\to}
  \cdots 
  \stackrel{d}{\to}
  \Omega^{p-1}(X)
  \stackrel{(0,d)}{\longrightarrow}  
  Ham^{p}(X)
$$


with the Hamiltonian pairs, def. \ref{HamiltonianFormsAndVectorFields}, in degree 0 and with the 0-forms ([[smooth functions]]) in degree $p$. 

The non-vanishing $L_\infty$-brackets are defined to be the following

* $l_1(J) = d J$

* $l_{k \geq 2}(v_1 + J_1, \cdots, v_k + J_k) 
  \coloneqq 
  - (-1)^{\left(k+1 \atop 2\right)} \iota_{v_k}\cdots \iota_{v_1}\omega$.

=--

+-- {: .num_prop}
###### Proposition

Definition \ref{PoissonBracketLienAlgebra} indeed gives an [[L-∞ algebra]] in that the higher [[Jacobi identity]] is satisfied.

\[
 \label{LInfinityJacobiIdentity}
  \sum_{i+j = n+1} 
  \sum_{\sigma \in UnShuff(i,j)}

  (-1)^{sgn(\sigma)} 
   l_i \left(

     l_j \left( x_{\sigma(1)}, \cdots, x_{\sigma(j)} \right),
     x_{\sigma(j+1)} , \cdots , x_{\sigma(n)}
   \right)
  = 0
  \,,
\]

=--

For the special case of $(p+1)$-plectic $\omega$ this is due to ([Rogers 10, lemma 3.7](#Rogers10)), for the general pre-$(p+1)$-plectic case this is ([FRS 13b, prop. 3.1.2](#FRS13b)).

+-- {: .proof}
###### Proof

Repeatedly apply [[Cartan's magic formula]] $\mathcal{L}_v = \iota_v \circ d + d \circ \iota_v$ as well as the consequence $\mathcal{L}_{v_1} \circ \iota_{v_2} - \iota_{v_2} \circ \mathcal{L}_{v_1} = \iota_{[v_1,v_2]}$ to find that for all vector fields $v_i$ and differential forms $\beta$ (of any degree, not necessarily closed) one has

$$
  \begin{aligned}
    (-1)^k d \iota_{v_k} \cdots \iota_{v_1}  \beta
    = &
    \underset{1 \leq i \lt j \leq k}{\sum}
    (-1)^{i+j} 
     \iota_{v_k}
      \cdots
      \widehat{\iota_{v_j}}
      \cdots
      \widehat{\iota_{v_i}}
      \cdots
     \iota_{[v_i,v_j]}
     \\
     & + 
     \underoverset{i=1}{k}{\sum}
     (-1)^i
     \iota_{v_k}
     \cdots
     \widehat{\iota_{v_i}}
     \cdots
     \iota_{v_1}
     \mathcal{L}_{v_i}
     \beta
     \\
     & +
     \iota_{v_k}
     \cdots
     \iota_{v_1}
     d \beta
  \end{aligned}
  \,.
$$

With this, the statement follows straightforwardly.

=--

#### Interlude: Cech-Deligne complexes

Recall the [[Cech cohomology|Cech]] complex.

+-- {: .num_defn #CechComplex}
###### Definition
**(&#268;ech complex)**

Let $X$ be a [[smooth manifold]] and let $A_\bullet \in Ch_+(Sh(X))$ be a sheaf of [[chain complexes]] on $X$. Let $\{U_i \to X\}$ be a [[good open cover]] of $X$, i.e. an open cover such that each finite non-empty intersection $U_{i_0, \cdots, i_k}$ is [[diffeomorphism|diffeomorphic]] to an [[open ball]]/[[Cartesian space]].

The **&#268;ech cochain complex** $C^\bullet((X,\{U_i\}),A_\bullet)$ 
of $X$ with respect to the cover $\{U_i \to X\}$ and with [[coefficients]] in $A_\bullet$ is in degree $k \in \mathbb{N}$ given by the [[abelian group]]

$$
  C^k((X,\{U_i\}),A_\bullet)
  \coloneqq
  \oplus_{{l,n} \atop {k = n-l}}
  \oplus_{i_0, i_1, \cdots, i_n}
  A_l(U_{i_0, \cdots, i_n})
$$


which is the [[direct sum]] of the values of $A_\bullet$ on the given intersections as indicated; and whose [[differential]] 

$$
  d
  \colon
  C^{k}((X,\{U_i\}),A_\bullet)
  \longrightarrow
  C^{k+1}((X,\{U_i\}),A_\bullet)
$$

is defined componentwise (see at [[matrix calculus]] for conventions on maps between [[direct sums]]) by

$$
  \begin{aligned}
    (d a)_{i_0, \cdots, i_{k+1}} 
    & \coloneqq 
    (\partial_A a + (-1)^k \delta a)_{i_0, \cdots, i_{k+1}} 
    \\
    & \coloneqq
    \partial_A a_{i_0, \cdots, i_{k+1}}
    +
    (-1)^k
    \sum_{0 \leq j \leq k+1} (-1)^{j}
    a_{i_0, \cdots, i_{j-1}, i_{j+1}, \cdots, i_{k+1}} 
    |_{U_{i_0, \cdots, i_{k+1}}}
  \end{aligned}
$$

where on the right the sum is over all components of $a$ obtained via the canonical restrictions obtained by discarding one of the original $(k+1)$ subscripts.

The **Cech cohomology** groups of $X$ with coefficients in $A_\bullet$ __relative to the given cover__ are the [[chain homology]] groups of the Cech complex

$$
  H_{Cech}^k((X,\{U_i\}), A_\bullet)
  \coloneqq
  H^k(C^\bullet((X,\{U_i\}),A_\bullet))
  \,.
$$

The **Cech cohomology** groups as such are the [[colimit]] ("[[direct limit]]") of these groups over refinements of covers

$$
  H^k_{Cech}(X, A_\bullet)
  \coloneqq
  \underset{\longrightarrow}{\lim}_{\{U_i \to X\}}
  H_{Cech}^k((X,\{U_i\}), A_\bullet)
  \,.
$$

=--

Recall the [[Deligne complex]].

+-- {: .num_defn #CechComplex}
###### Definition

The _[[Deligne complex]]_ for [[Deligne cohomology]] of degree $(p+2)$ is the [[chain complex]] of [[abelian sheaves]] given by

$$
  (\mathbf{B}^{p+1}U(1)_{conn})_{\bullet}
  = 
  \left[
    C^\infty(-,U(1))
    \stackrel{d log}{\longrightarrow}
    \Omega^1(-)
    \stackrel{d}{\to}
    \Omega^2(-)
    \stackrel{d}{\to}
    \cdots
    \stackrel{d}{\to}
    \Omega^{p+1}(-)
  \right]
  \in
  Ch_{\bullet \geq 0}(Sh(X))
  \,.
$$

=--


+-- {: .num_remark}
###### Remark

So for $\{U_i\to X\}$ an [[open cover]], then we have the Cech-Deligne [[double complex]]

$$
  \array{
    0 &\longrightarrow& 0 &\longrightarrow& 0 &\longrightarrow & \cdots
    \\
    \uparrow && \uparrow && \uparrow
    \\
    \Omega^{p+1}(\coprod_i U_i)
    &\stackrel{\delta}{\longrightarrow}&
    \Omega^{p+1}(\coprod_{i,j} U_{ i j})
    &\stackrel{\delta}{\longrightarrow}&
    \Omega^{p+1}(\coprod_{i,j, k} U_{i j k})
    &\stackrel{\delta}{\longrightarrow}&
    \cdots    
    \\
    \uparrow^{\mathrlap{d}} && \uparrow^{\mathrlap{d}} && \uparrow^{\mathrlap{d}} &&
    \\
    \vdots && \vdots && \vdots
    \\
    \uparrow^{\mathrlap{d}} && \uparrow^{\mathrlap{d}} && \uparrow^{\mathrlap{d}} &&
    \\
    \Omega^2(\coprod_i U_i)
    &\stackrel{\delta}{\longrightarrow}&
    \Omega^2(\coprod_{i,j} U_{ i j})
    &\stackrel{\delta}{\longrightarrow}&
    \Omega^2(\coprod_{i,j, k} U_{i j k})
    &\stackrel{\delta}{\longrightarrow}&
    \cdots    
    \\
    \uparrow^{\mathrlap{d}} && \uparrow^{\mathrlap{d}} && \uparrow^{\mathrlap{d}} &&
    \\
    \Omega^1(\coprod_i U_i)
    &\stackrel{\delta}{\longrightarrow}&
    \Omega^1(\coprod_{i,j} U_{ i j})
    &\stackrel{\delta}{\longrightarrow}&
    \Omega^1(\coprod_{i,j, k} U_{i j k})
    &\stackrel{\delta}{\longrightarrow}&
    \cdots
    \\
    \uparrow^{\mathrlap{d log}} && \uparrow^{\mathrlap{d log}} && \uparrow^{\mathrlap{d log}} &&
    \\
    C^\infty(\coprod_i U_i, U(1))
    &\stackrel{\delta}{\longrightarrow}&
    C^\infty(\coprod_{i,j} U_{i j}, U(1))
    &\stackrel{\delta}{\longrightarrow}&
    C^\infty(\coprod_{i,j,k} U_{i j k}, U(1))
    &\stackrel{\delta}{\longrightarrow}&
    \cdots
  }
$$
where vertically we have the [[de Rham differential]] and horizontally the Cech differential given by alternating sums of [[pullback of differential forms]].

The corresponding [[total complex]] has in degree $n$ the [[direct sum]] of the entries in this double complex which are on the $n$th nw-se off-diagonal and has the total differential

$$
  d_{tot} = d + (-1)^{deg} \delta
$$

with $deg$ denoting form degree.

=--

+-- {: .num_example}
###### Example

A Cech-Deligne cocycle in degree $3$ (a "[[bundle gerbe with connection]]") is data $(\{B_{i}\}, \{A_{i j}\}, \{g_{i j k}\})$ such that
 
$$
  \array{
    \{B_i\}
    &\stackrel{\delta}{\longrightarrow}&
    {{\{B_j - B_i\}} = {d A_{i j}}}
    &&
    &&
    \\
    && \uparrow^{\mathrlap{d}} &&  &&
    \\
    &&
    \{A_{i j}\}
    &\stackrel{\delta}{\longrightarrow}&
    \{-A_{ j k} + A_{i k} - A_{i j}\} = \{d log g_{i j k}\}
    &&
    \\
     &&  && \uparrow^{\mathrlap{d log}} &&
    \\
    &&
    &&
    \{g_{i j k}\}
    &\stackrel{\delta}{\longrightarrow}&
    \{g_{j k l} g_{i k l}^{-1} g_{i j l} g_{i j k}^{-1} \} = 1
  }
$$

=--

+-- {: .num_defn #CurvatureOfDeligneCocycle}
###### Definition

The _[[curvature]]_ of a Cech-Deligne cocycle 

$$
  \overline{\theta} = (B_{i}, \cdots, g_{i_1 \cdots i_{p+2}})
$$ 

is the uniquely defined $(p+2)$-form $F_{\overline{\theta}} \in \Omega^{p+2}(X)$ such that

$$
  F_{\overline{\theta}}|_{U_i} = d B_i
  \,.
$$

=--


#### Higher infinitesimal quantomorphisms and conserved currents

There is an evident generalization of the [[prequantization]], def. \ref{CechDelignePrequantizationAnditsInfinitesimalAutomorpisms}, of closed 2-forms by [[circle bundles with connection]], hence by degree-2 cocycles in [[Deligne cohomology]], to the prequantization of closed $(p+2)$-forms by degree-$(p+2)$-cocycles in Deligne cohomology.

+-- {: .num_defn #HigherPrequantizationByDeligneCocycles}
###### Definition

Given a [[n-plectic manifold|pre-(p+1)-plectic manifold]] $(X,\omega)$, then 
a _[[prequantization]]_ is a Cech-Deligne cocycle
$\overline{\theta}$,  the _[[prequantum n-bundle|prequantum (p+1)-bundle]]_, whose [[curvature]], def. \ref{CurvatureOfDeligneCocycle}, equals $\omega$:

$$
  F_{\overline{\theta}} = \omega
  \,.
$$


=--

+-- {: .num_remark }
###### Remark

In terms of [[diagrams]] in the [[homotopy theory]] $\mathbf{H}$ of [[smooth homotopy types]], def. \ref{HigherPrequantizationByDeligneCocycles} describes lifts of the form


$$
  \array{
    && \mathbf{B}^{p+1}U(1)_{conn}
    \\
    & {}^{\mathllap{\overline{\theta}}}\nearrow & \downarrow^{\mathrlap{F_{(-)}}}
    \\
    X &\stackrel{\omega}{\longrightarrow} &
    \mathbf{\Omega}^{p+2}_{cl}
  }
  \,.
$$

=--

This way there is an immediate generalization of def. \ref{CechDelignePrequantizationAnditsInfinitesimalAutomorpisms} to forms and cocycles of higher degree:


+-- {: .num_defn #PoissondgAlgebra}
###### Definition

Let $\overline{\theta}$ be any [[Cech cohomology|Cech]]-[[Deligne cohomology|Deligne]]-[[cocycle]] relative to an [[open cover]] $\mathcal{U}$ of $X$, which gives a [[prequantum n-bundle]] for $\omega$. The [[L-∞ algebra]] 
$\mathfrak{quantmorph}(X,\overline{\theta})$ is the [[dg-Lie algebra]] (regarded as an $L_\infty$-algebra) whose underlying [[chain complex]] is the [[Cech cohomology|Cech]] [[total complex]] made to end in _Hamiltonian Cech cocycles_

* $\mathfrak{quantmorph}(X,\overline{\theta})^0 \coloneqq \{v+ \overline{\alpha}  \in Vect(X)\oplus Tot^{n-1}(\mathcal{U}, \Omega^\bullet) \;\vert\; \mathcal{L}_v \overline{\theta} = \mathbf{d}_{Tot}\overline{\alpha}\}$;


* $\mathfrak{quantmorph}(X,\overline{\theta})^{i \gt 0} \coloneqq C^{n-1-i}(\mathcal{U},\Omega^\bullet)$


with [[differential]] given by $d_{tot} = d + (-1)^{deg} \delta$.

The non-vanishing dg-Lie brackets on this complex are given by the evident [[action]] of [[vector fields]] on all the components of the Cech cochains by [[Lie derivative]]:

* $[v_1 + \overline{\alpha}_1, v_2 + \overline{\alpha}_2] \coloneqq [v_1, v_2] + \mathcal{L}_{v_1}\overline{\alpha}_2 - \mathcal{L}_{v_2}\overline{\alpha}_1$

* $[v+ \overline{\alpha}, \overline{\eta}] = - [\overline{\eta}, v + \overline{\alpha}] = \mathcal{L}_v \overline{\eta}$.

=--

([FRS 13b, def./prop. 4.2.1](#FRS13b))

One then finds a direct higher analog of corollary \ref{EquivalenceBetweenPoissonBracketAndInfinQuantomorphism} (its proof however is requires a bit more work):


+-- {: .num_prop #ComparisonTheorem}
###### Proposition

There is an [[equivalence]] in the [[model structure for L-∞ algebras|homotopy theory of L-∞ algebras]]

$$
  f
  \colon
  \mathfrak{poiss}(X,\omega)
  \stackrel{\simeq}{\longrightarrow}
  \mathfrak{quantmorph}(X,\overline{\theta})
$$

between the $L_\infty$-algebras of def. \ref{PoissonBracketLienAlgebra} and def. \ref{PoissondgAlgebra} (in particular def. \ref{PoissondgAlgebra} does not depend on the choice of $\overline{A}$) whose underlying [[chain map]] satisfies


* $f(v + J) = (v,\; \sum_{i = 0}^n (-1)^i \iota_v \theta^{n-i} - J|_{\mathcal{U}})$.

=--

([FRS 13b, theorem 4.2.2](#FRS13b))

+-- {: .num_prop #ComparisonTheorem}
###### Proposition

Proposition \ref{ComparisonTheorem} says that all the higher Poisson $L_\infty$-algebras are $L_\infty$-algebras of symmetries of [[Deligne cohomology|Deligen cocycles]] [[prequantization|prequantizing]] the give pre-$(p+1)$-plectic form, higher "[[quantomorphisms]]".

In fact the [[dg-algebra]] $\mathfrak{quantmorph}(X,\overline{\theta})$ makes yet another equivalent interpretation of $\mathfrak{poiss}(X,\omega)$ manifest: it is also a resolution of the [[Dickey bracket]] of [[conserved currents]] for [[geometry of physics -- WZW terms|WZW]] [[sigma-models]]. This we come to [below](#BPSCharges).

=--




#### Higher Kostant-Souriau extension

The higher Poisson brackets come with a higher analog of the
Kostant-Souriau extension, prop. \ref{KostantSouriauExtension}.

+-- {: .num_defn #TruncatedDeRhamComplexAsLInfinity}
###### Definition

Write

$$
  \mathbf{H}(X,\flat \mathbf{B}^p \mathbb{R})
  \coloneqq
  (\Omega^0(X) \stackrel{d}{\to} \Omega^1(X) \stackrel{d}{\to} \cdots
  \Omega^{(p-1)}(X) \stackrel{d}{\to}\Omega^p_{cl}(X))
$$

for the truncated [[de Rham complex]] regarded as an abelian [[L-∞ algebra]].

=--

+-- {: .num_prop #HigherKostantSouriauExtension}
###### Proposition

Given a [[n-plectic manifold|pre-(p+1)-plectic manifold]] $(X,\omega)$,
the [[Poisson bracket Lie n-algebra|Poisson bracket Lie (p+1)-algebra]]
$\mathfrak{poiss}(X,\omega)$, def. \ref{PoissonBracketLienAlgebra}, is an [[L-∞ extension]] of the [[Hamiltonian vector fields]] by the truncated de Rham complex,
def. \ref{TruncatedDeRhamComplexAsLInfinity}, there is a [[homotopy fiber sequence]] of $L_\infty$-algebras of the form

$$
  \array{
    \mathbf{H}(X,\flat\mathbf{B}^p \mathbb{R})
    &\longrightarrow&
    \mathfrak{poiss}(X,\omega)
    &\longrightarrow&
    HamVect(X,\omega)
    \\
    && && \downarrow^{\mathrlap{\iota_{\cdots}\omega} }
    \\
    && && \mathbf{B} \mathbf{H}(X,\flat \mathbf{B}^p \mathbb{R})
  }
  \,.
$$

=--

([FRS 13b, theorem 3.3.1](#FRS13b))

To better see what this means, we may truncate this down to a statement about ordinary Lie algebras.


+-- {: .num_prop #HpExtensionFromTruncatedHigherPoissonBracket}
###### Proposition

Given a [[n-plectic manifold|pre-(p+1)-plectic manifold]] $(X,\omega)$,
the 0-truncation, prop. \ref{LInfinityTruncation}, of the higher Kostant-Souriau extension of prop. \ref{HigherKostantSouriauExtension} is a [[Lie algebra extension]] of the [[Hamiltonian vector fields]] by the [[de Rham cohomology]] group $H^p(X)$. 

$$
  0 \to H^p(X) \longrightarrow \tau_0 \mathfrak{poiss}(X,\omega)
   \longrightarrow
   HamVect(X,\omega)
   \to 0
   \,.
$$

=--

#### Applications 

##### Higher conserved current algebras and BPS charge extensions
 {#BPSCharges}

By the discussion at _[[geometry of physics -- WZW terms]]_,  [[prequantization]] $\mathbf{L} \colon X \to \mathbf{B}^{p+1}U(1)_{conn}$ of $\omega \in \Omega^{p+2}(X)$ may be thought of as a [[parameterized WZW term]] for a [[sigma model]] field theory decribing the propagation of a [[p-brane]] on $X$.

Under this perspective, a [[Hamiltonian vector field]] $v$ on $X$ is a [[point symmetry]] of this sigma-model field theory and a [[Hamiltonian form]] $J$ for $v$ is is the [[conserved current]] corresponding to this via [[Noether's theorem]]. Inspection then shows that the bracket in def. \ref{PoissondgAlgebra} is the [[Dickey bracket]] of [[conserved currents]], while the [[differential]] in def. \ref{PoissondgAlgebra} expresses the shift of currents by trivial currents ([KS](#KS)).
 
Hence under this perspective, def. \ref{PoissondgAlgebra} gives a [[dg-Lie algebra]] resolution of the [[Dickey bracket]] Lie algebra of conserved Noether currents for [[point symmetries]] of [[geometry of physics -- WZW terms|higher WZW sigma-models]] from gauge equivalence classes of conrved currents to the currents themselves.

For the case that $X$ is a [[super spacetimes]] and $\omega$ is a [[definite form]] on a super cocycle in the [[brane scan]] then this is known as the algebra of [[supergravity]] [[BPS charges]] of $X$. Therefore we also write

$$
  \mathfrak{bps}(X,\mathbf{L})
  \coloneqq
  \mathfrak{quantmorph}(X,\mathbf{L})
  \,.
$$

From this perspective the higher Kostant-Souriau extesion as in 
prop. \ref{HpExtensionFromTruncatedHigherPoissonBracket} says the following:

+-- {: .num_cor #BPSChargeExtension}
###### Corollary

For $\omega \in \Omega^{p+2}(X)$ the [[curvature]] of a [[geometry of physics -- WZW terms|WZW term]] on the smooth manifold $X$, then the Lie algebra of [[conserved currents]] covering [[target space]] [[point symmetries]] of the corresponding $p$-brane [[sigma-model]] is a  [[Lie algebra extension]] of the taget space symmetry by the $p$th de Rham cohomology group

$$
  0 
   \to H^p(X) 
   \longrightarrow 
   \mathfrak{bps}(X,\omega)
   \longrightarrow
   HamVect(X,\omega)
   \to 0
   \,.
$$


=--

+-- {: .num_remark}
###### Remark

For $X$ a [[superspacetime]] and $\omega$ a [[definite form]], definite on a super-cocycle in the [[brane scan]], then corollary \ref{BPSChargeExtension} is folklore in the [[string theory]] literature, due to ([AGIT 89](#AGIT89)).

=--

This is discussed further in _[[geometry of physics -- BPS charges]]_.



### Finite symmetries 


We here discuss the full finite version of [[quantomorphism n-groups]].

#### Differential coefficients

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

#### Higher quantomorphism groups and Heisenberg groups

+-- {: .num_defn #QuantomorphismGroup}
###### Definition


Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$ there are the following concepts in [[schreiber:Higher geometric prequantum theory|higher geometric prequantum theory]].


1. The **[[quantomorphism ∞-group]]** is the [[stabilizer ∞-group]] of $\nabla \in \mathbb{G}\mathbf{Conn}(X)$, def. \ref{DifferentialConcretification}, under the $\mathbf{Aut}(X)$-action of \ref{PrecompositionActionOnGConn};

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

   is the [[1-image]] of the canonical morphism $\mathbf{QuantMorph}(X,\nabla) \longrightarrow \mathbf{Aut}(X)$. 

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

For $\mathbf{H} = $ [[Smooth∞Grpd]], for $X \in SmoothMfd \hookrightarrow \mathbf{H}$ a [[smooth manifold]] and for $\nabla$ a [[prequantum line bundle]] on $X$, then $\mathbf{QuantMorph}(X,\nabla)$ is Souriau's [[quantomorphism group]] covering the [[Hamiltonian diffeomorphism]] group. In the case that $(X, F_\nabla)$ is a [[symplectic vector space]] $X = V$ regarded as a linear symplectic manifold with Hamiltonian action on itself by translation, then $\mathbf{Heis}_{V}(X,\nabla)$ is the traditional [[Heisenberg group]].

=--



+-- {: .num_remark }
###### Remark


Since $\mathbf{HamSymp}(X,\nabla)\hookrightarrow \mathbf{Aut}(X)$ is by construction a [[1-monomorphism]], given any $G$-action $\rho \colon G \longrightarrow \mathbf{Aut}(X)$ on $X$, not necessarily Hamiltonian, then the homotopy pullback $\rho^\ast \mathbf{QuantMorph}(X,\nabla)$ is the Heisenberg ∞-group of the maximal sub-$\infty$-group of $G$ which does act via Hamiltonian symplectomorphisms. Therefore we will also write $\mathbf{Heis}_G(X,\nabla)$ in this case.


=--

#### The higher Kostant-Souriau extension 

The following is the refinement of the [[Kostant-Souriau extension]] to [[higher differential geometry]]

+-- {: .num_prop #TheQuantomorphismGroupExtension}
###### Proposition

Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, there is a [[homotopy fiber sequence]] of the form

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
        \mathbf{B} ((\Omega \mathbb{G})\mathbf{FlatConn}(X))
    }
   $$

exhibiting the [[quantomorphism ∞-group]] as an [[∞-group extension]] of the [[Hamiltonian symplectomorphism ∞-group]] by the [[moduli stack]] of $\Omega \mathbb{G}-$[[flat ∞-connections]], classified by a [[cocycle]] $\mathbf{KS}$.

=--

([FRS 13a](#FRS13a))

+-- {: .num_example }
###### Example

In $\mathbf{H} = $ [[Smooth∞Grpd]], let $\mathbb{G} = \mathbf{B}^p U(1)$ be the [[circle n-group|circle (p+1)-group]] and let $X \in SmoothMfd \hookrightarrow Smooth \infty Grpd$ be [[n-connected topological space|p-connected]], then $(\Omega\mathbf{B}^p U(1))\mathbf{FlatConn}(X)\simeq \mathbf{B}^{p}U(1)$. Hence here prop. \ref{TheQuantomorphismGroupExtension} gives

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

Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, and for $\rho \colon G \longrightarrow \mathbf{HamSymp}(X,\nabla)$ a $G$-[[Hamiltonian action]], then there is a [[homotopy fiber sequence]]

1. if $\mathbb{G}$ is [[0-truncated]] then

   $$
     \array{
        \mathbb{G}\mathbf{ConstFunct}(X)
        &\longrightarrow&
        \mathbf{Heis}_G(X,\nabla)
        \\
        && \downarrow
        \\
        && G
        &\stackrel{\mathbf{KS}(\rho)}{\longrightarrow}&
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
        && G
        &\stackrel{\mathbf{KS}(\rho)}{\longrightarrow}&
        \mathbf{B} ((\Omega \mathbb{G})\mathbf{FlatConn}(X))
    }
   $$

exhibiting the [[Heisenberg ∞-group]] as an [[∞-group extension]] of the $G$ by the [[moduli stack]] of $\Omega \mathbb{G}-$[[flat ∞-connections]], classified by a [[cocycle]] $\mathbf{KS}(\rho)$.


The class of the [[cocycle]] $\mathbf{KS}(\rho)$ is the [[obstruction]] to prequantizing $\rho$ to a [[moment map]] (the _[[classical anomaly]]_ of $\rho$); and the the [[Heisenberg ∞-group]] [[∞-group extension|extension]] of $G$ is the universal cancellation of this anomaly.

=--


## References

* {#AGIT89} [[José de Azcárraga]], [[Jerome Gauntlett]], J.M. Izquierdo, [[Paul Townsend]], _Topological Extensions of the Supersymmetry Algebra for Extended Objects_, Phys. Rev. Lett. 63 (1989) 2443 ([spire](http://inspirehep.net/record/26393?ln=en))


* {#Rogers10} [[Chris Rogers]], _$L_\infty$ algebras from multisymplectic geometry_ , 
Letters in Mathematical Physics April 2012, Volume 100, Issue 1, pp 29-50  ([arXiv:1005.2230](http://arxiv.org/abs/1005.2230), [journal](http://link.springer.com/article/10.1007%2Fs11005-011-0493-x)).


* {#FRS13a} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_, ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))


* {#FRS13b} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_, Homology, Homotopy and Applications, Volume 16 (2014) Number 2, p. 107 &#8211; 142 ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))

* {#KS} [[Igor Khavkine]], [[Urs Schreiber]], _$L_\infty$-algebras of conserved currents_