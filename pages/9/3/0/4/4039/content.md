
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

**Variational calculus** -- sometimes called **secondary calculus** -- is a version of [[differential calculus]] that deals with local extremization of [[nonlinear functionals]]: extremization of differentiable functions on non-finite dimensional spaces such as [[mapping spaces]], [[spaces of sections]] and hence [[spaces of histories]] of [[field (physics)|fields]] in [[field theory]]. 

Specifically, it studies the _[[critical points]]_ , i.e. the points where the first variational derivative of a functional vanishes, for functionals on spaces of [[sections]] of [[jet bundles]]. The kinds of equations specifying these critical points are [[Euler-Lagrange equations]].

This applies to, and is largely motivated from, the study of [[action functionals]] in [[physics]]. In [[classical physics]] the critical points of a specified action functional on the space of field configurations encode the physically observable configurations.

There are strong [[cohomology|cohomological]] tools for studying variational calculus, such as the [[variational bicomplex]] and [[BV-BRST formalism]].

## In terms of smooth spaces
 {#InTermsOfSmoothSpaces}

We discuss some basics of variational calculus of functional in terms of [[smooth spaces]] and in particular in terms of [[diffeological spaces]].

### Smooth functionals
 {#SmoothFunctionals}

Let $X$ be a [[smooth manifold]].
Let $\Sigma$ be a [[smooth manifold|smooth]] [[manifold with boundary]] $\partial \Sigma \hookrightarrow \Sigma$. 

Write 

$$
  [\Sigma, X] \in Smooth0Type
$$

for the [[smooth space]] (a [[diffeological space]]) which is the [[mapping space]] from $\Sigma$ to $X$, hence such that for each $U \in $ [[CartSp]] we have

$$
  [\Sigma, X](U) = C^\infty(U \times \Sigma, X)
  \,.
$$


+-- {: .num_defn #MappingSpaceWithNonVaryingBoundary}
###### Definition

Write

$$
  [\Sigma, X]_{\partial \Sigma}
  \coloneqq
  [\Sigma, X] \times_{[\partial \Sigma,X]} \flat [\partial \Sigma,X]
$$

for the [[pullback]] in smooth spaces

$$
  \array{
    [\Sigma,X]_{\partial \Sigma}
    &\to&
    \flat [\partial \Sigma, X]
    \\
    \downarrow && \downarrow
    \\
    [\Sigma,X] &\stackrel{(-)|_{\partial \Sigma}}{\to}& [\partial \Sigma,X]
  }
  \,,
$$

where

* the bottom morphism is the restriction $[\partial \Sigma \hookrightarrow \Sigma, X]$ of configurations to the boundary;

* the right vertical morphism is the [[counit of an adjunction|counit]] of the $(Disc \dashv \Gamma)$-[[adjunction]] on smooth spaces.

=--

+-- {: .num_prop #PlotsOfMappingSpaceWithNonVaryingBoundary}
###### Proposition

The [[smooth space]] $[\Sigma, X]_{\partial \Sigma}$ is a [[diffeological space]] whose underlying set is $C^\infty(\Sigma,X)$ and whose $U$-plots for $U \in $ [[CartSp]] are smooth functions
$\phi \colon U \times \Sigma \to X$ such that $\phi(-,s) \colon U \to X$ is the constant function for all $s \in \partial \Sigma \hookrightarrow \Sigma$.

=--


+-- {: .num_defn #SmoothFunctional}
###### Definition

A **functional** on the mapping space $[\Sigma, X]$ is a [[homomorphism]] of smooth spaces

$$
  S \colon [\Sigma, X]_{\partial \Sigma} \to \mathbb{R}
  \,.
$$

=--

### Functional derivative
 {#FunctionalDerivative}

Write

$$
  \mathbf{d} \colon \mathbb{R} \to \Omega^1
$$

for the [[de Rham differential]] incarnated as a [[homomorphism]] of [[smooth spaces]] from the [[real line]] to the smooth [[moduli space]] of [[differential 1-forms]].


+-- {: .num_defn}
###### Definition

The **[[functional derivative]]** 

$$
  \mathbf{d}S
  \in 
  \Omega^1([\Sigma,X]_{\partial \Sigma})
$$ 

of a functional $S$, def. \ref{SmoothFunctional}, is simply its [[de Rham differential]] as a homomorphism of smooth spaces, hence the composite

$$
  \mathbf{d} S \colon [
  \Sigma, X]_{\partial \Sigma} 
     \stackrel{S}{\to} 
  \mathbb{R}   
    \stackrel{\mathbf{d}}{\to}
  \Omega^1
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

This means that for each smooth parameter space $U \in $ [[CartSp]] and for each smooth $U$-parameterized collection 

$$
  \phi \colon U \times \Sigma \to X
$$

of smooth functions $\Sigma \to X$, constant in the parameter $U$ in some neighbourhood of the boundary of $\Sigma$, 

$$
  S_\phi \colon [\Sigma,X]_{\partial \Sigma}(U) \to C^\infty(U,\mathbb{R})
$$

is the function that sends each such $U$-collection of configurations to the $U$-collection of their values under $S$. Then

$$
  (\mathbf{d}S)_\phi \in \Omega^1(U)
$$

is the smooth [[differential 1-form]]

$$
  (\mathbf{d}S)_\phi = \mathbf{d}(S(\phi))
  \,.
$$

=--

+-- {: .num_example}
###### Example

Let $\Sigma = [0,1] \hookrightarrow \mathbb{R}$ be the standard [[interval]]. Let 

$$
  L(-,-) \mathbf{d}t \in \Omega^1([0,1], C^\infty(\mathbb{R}^2))
$$ 

and consider the functional

$$
  S
  \colon
  ([0,1] \stackrel{\gamma}{\to} X)
  \mapsto
  \int_{0}^1 L(\gamma(t), \dot \gamma(t)) d t
  \,.
$$

Then for $U = \mathbb{R}$ and any smooth $U$-parameterized collection $\{\gamma_{u} \colon \Sigma \to X\}_{u \in I}$ the functional derivative takes the value

$$
  \begin{aligned}
   \mathbf{d}S_{\gamma_{(-)}}
   & =
   \left(
     \frac{d}{d u} \int_0^1 L(\gamma_u(t), \dot \gamma_u(t)) dt
   \right)
   \mathbf{d}u
   \\
    & = 
     \int_{0}^1 
     \left(
       \frac{\partial L}{\partial \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{d \gamma_u(t)}{d u}
      + 
       \frac{\partial L}{\partial \dot \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{\partial \dot \gamma_u(t)}{\partial u}
     \right)
     \mathbf{d} u
     \\
     & =
     \int_{0}^1 
     \left(
       \frac{\partial L}{\partial \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{d \gamma_u(t)}{d u}
      + 
       \frac{\partial L}{\partial \dot \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{\partial }{\partial t}\frac{\partial \gamma_u(t)}{\partial u}
     \right)
     \mathbf{d} u
     \\
     & =
     \int_{0}^1
     \left(
       \frac{\partial L}{\partial \gamma}(\gamma_u(t), \dot \gamma_u(t))
      - 
       \frac{\partial}{\partial t}\frac{\partial L}{\partial \dot \gamma}(\gamma_u(t), \dot \gamma_u(t))
     \right)
     \frac{\partial \gamma_u(s)}{\partial u}
     \mathbf{d}u
  \end{aligned}
  \,.
$$

Here we used [[integration by parts]] and used that the boundary term vanishes

$$
  \begin{aligned}
    \int_{0}^1 \frac{\partial}{\partial t} 
    \left(
      \frac{\partial}{\partial \dot\gamma} L(\gamma_u(s), \dot \gamma_u(s))
      \frac{\partial \gamma_u(s)}{\partial u}
    \right)
    d s
    & = 
    \left(
      \frac{\partial}{\partial \dot\gamma} L(\gamma_u(1), \dot \gamma_u(1))
      \frac{\partial \gamma_u(1)}{\partial u}
    \right)
    - 
    \left(
      \frac{\partial}{\partial \dot\gamma} L(\gamma_u(0), \dot \gamma_u(0))
      \frac{\partial \gamma_u(0)}{\partial u}
    \right)
    \\
    & = 0
  \end{aligned}
$$

since by prop. \ref{PlotsOfMappingSpaceWithNonVaryingBoundary} $\gamma_{(-)}(1)$ and $\gamma_{(-)}(0)$ are constant.

=--

## In terms of the variational bicomplex

In the special case that the functional to be varied comes from a [[Lagrangian density]], then its variational derivative is the image under [[transgression of variational differential forms|transgression]] of the [[vertical derivative]] in the [[variational bicomplex]] of differential forms on the given [[jet bundle]].

(...)


## Related concepts

* [[principle of extremal action]]

* [[Euler-Lagrange equations]], [[shell]]

* [[source form]], [[evolutionary vector field]], [[evolutionary derivative]]

* [[de Donder-Weyl formalism]]

* [[phase space]]

* [[variational bicomplex]], [[secondary differential calculus]]

* [[Lagrange multiplier]]

* [[variational sequence]]

## References 

### General

Textbook on usual physics-style variational calculus for [[Lagrangian field theory]]:

* [[Jean-Louis Basdevant]]: *Variational Principles in Physics*, Springer (2007) \[<a href="https://doi.org/10.1007/978-3-031-21692-3">doi:10.1007/978-3-031-21692-3</a>\]


Exposition of variational calculus in terms of [[jet bundles]] and [[Lepage forms]] and aimed at examples from [[physics]]:

* {#MusilovaHronek16} [[Jana Musilová]],  [[Stanislav Hronek]], _The calculus of variations on jet bundles as a universal approach for a variational formulation of fundamental physical theories_, Communications in Mathematics, Volume 24, Issue 2 (Dec 2016) ([doi.org/10.1515/cm-2016-0012]( https://doi.org/10.1515/cm-2016-0012))

Fundamental texts on variational calculus:

* [[Ian Anderson]], _The variational bicomplex_, ([[AndersonVariationalBicomplex.pdf:file]])

* Hubert Goldschmidt, [[Shlomo Sternberg]], _The Hamilton-Cartan formalism in the calculus of variations_, Annales de l'institut Fourier 23 no. 1 (1973), p. 203-267 [numdam](http://www.numdam.org/item?id=AIF_1973__23_1_203_0)

* [[Peter Olver]], _Applications of Lie groups to differential equations_, Springer; _Equivalence, invariants, and symmetry_, Cambridge Univ. Press 1995.

* [[Demeter Krupka]], _Introduction to global variational geometry_, 2015

* Olga Krupkov&#225;, _The geometry of ordinary variational equations_, Springer 1997, 251 p.

* Robert Hermann, _Some differential-geometric aspects of the Lagrange variational problem_, Illinois J. Math. __6__, 1962, 634&#8211;673 [MR145457](http://www.ams.org/mathscinet-getitem?mr=145457) [euclid](http://projecteuclid.org/euclid.ijm/1255632711); 
_Differential geometry and the calculus of variations_, Acad. Press 1968

* J. Jost, X. Li-Jost, _Calculus of variations_, CUP 1998

* {#Zuckerman} [[Gregg Zuckerman|G. J. Zuckerman]], _Action principles and global geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scientific, Singapore, 1987, pp. 259–284. ([[ZuckermanVariation.pdf:file]])
 

Zuckerman's ideas are used in

* [[Marco Benini]], [[Alexander Schenkel]], _Poisson algebras for non-linear field theories in the Cahiers topos_, [arxiv/1602.00708](http://arxiv.org/abs/1602.00708)

Examples: [[Jürgen Jost]], _Variational problems from physics and geometry_, [pdf](http://www.mis.mpg.de/fileadmin/jjost/variational_problems_from_physics_and_geometry.pdf)

* J. J. Duistermaat, _On the Morse index in variational calculus_, Adv. Math. __21__ (1976), 2, 173--195 [pdf](http://www.maths.ed.ac.uk/~aar/papers/duistermaat.pdf).

Some new results are in   

* [[E. Getzler]], _A Darboux theorem for Hamiltonian operators in the formal calculus of variations_, Duke Math. J. __111__, n. 3 (2002), 535-560, [MR2003e:32026](http://www.ams.org/mathscinet-getitem?mr=1885831), [doi](http://dx.doi.org/10.1215/S0012-7094-02-11136-3)
* Alberto De Sole, Victor G. Kac, _The variational Poisson cohomology_, [arxiv/1106.0082](http://arxiv.org/abs/1106.0082)

Geometric extremization problems (e.g. minimal surfaces), see also [[geometric measure theory]]:

* [[Jürgen Jost]], _The geometric calculus of variations: a short survey and a list of open problems_, Exposition. Math. __6__ (1988), no. 2, 111&#8211;143, [MR89h:58036](http://www.ams.org/mathscinet-getitem?mr=938179)
* H. Federer, _Geometric measure theory_, Springer 1969(especially appendices to Russian transl.) 
* Frederick J., Jr. Almgren, Almgren's big regularity paper (book form of a 1970s preprint)

Discussion in the context of [[BV formalism]]:

* Arthemy V. Kiselev, _The geometry of variations in Batalin-Vilkovisky formalism_,  [http://arxiv.org/abs/1312.1262](http://arxiv.org/abs/1312.1262)

Other references

* J. C. P. Bus, _The Lagrange multiplier rule on manifolds and optimal control of nonlinear systems_, SIAM J. Control and Optimization __22__, 5, 1984, 740-757 [pdf](http://oai.cwi.nl/oai/asset/2552/2552A.pdf)

In the [[covariant phase space]]-perspective:

* L. Vitagliano, _Secondary calculus and the covariant phase space_, [pdf](https://diffiety.mccme.ru/preprint/2008/02-08.pdf)
 {#Vitagliano}

On [[smooth sets]] as a [[convenient category of spaces|convenient category]] for [[variational calculus]] of [[Lagrangian quantum field theory|Lagrangian]] [[classical field theory]]:

* [[Grigorios Giotopoulos]], [[Hisham Sati]], *Field Theory via Higher Geometry I: [[schreiber:Smooth Sets of Fields]]* &lbrack;[arXiv:2312.16301](https://arxiv.org/abs/2312.16301)&rbrack;


### By functorial analysis and $\mathcal{D}$-geometry

See also references at [[diffiety]]. 

A formalism for variational calculus based on [[functorial analysis]] (with a precise relation with functional analytic methods and jet formalism) and a long list of examples of variational problems arising in [[classical mechanics]] and [[quantum field theory]] are collected in

* [[Frédéric Paugam]], _Towards the mathematics of quantum field theory_ ([pdf](http://www.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics.pdf))

The formulation of variational calculus in terms of [[diffeological spaces]] is mentioned for instance in section 1.65 of

* [[Patrick Iglesias-Zemmour]], _Diffeology_ ([pdf](http://math.huji.ac.il/~piz/documents/Diffeology.pdf#page=64))
{#PIZ}

* [[Frédéric Paugam]], _Histories and observables in covariant field theory_ ([arXiv:1010.3210](http://arxiv.org/abs/1010.3210)), sec. 2.4
{#Paugam}

following section 2.3.20 of 

* [[Alexander Beilinson]], [[Vladimir Drinfeld]], _[[Chiral Algebras]]_

For variational calculus in [[nonstandard analysis]] see survey

* V&#237;tor Neves, _Nonstandard calculus of variations, a survey_, [pdf](http://www2.mat.ua.pt/vneves/nsa/CalcVar-vitor6.pdf)

category: analysis, physics
[[!redirects calculus of variations]]
[[!redirects variational derivative]]
[[!redirects variational derivatives]]
