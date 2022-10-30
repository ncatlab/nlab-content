


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Given a [[differential form]] $\omega$ of degree $n$ on some [[smooth space]] $X$ and given a [[closed manifold|closed]] [[smooth manifold]] $\Sigma$ of [[dimension]] $k \leq n$, then there is canonically induced a differential form $\tau_\Sigma \omega$ of degree $n-k$ on the [[mapping space]] $[\Sigma,X]$: its restriction to any smooth family $\Phi_{(-)}$ of smooth functions $\Phi_u \colon \Sigma \to X$ is the result of first forming the [[pullback of differential forms]] of $\omega$ along $\Phi_{(-)}$ and then forming the [[integration of differential forms]] of the result over $\Sigma$:

$$
  \tau_{\Sigma} \omega\vert_{\Phi_{(-)}}
    \coloneqq
  \int_\Sigma (\Phi_{(-)})^\ast \omega
  \,.
$$

This differential form $\tau_\Sigma \omega$ on the mapping space is called the _[[transgression]]_ of $\omega$ with respect to $\Sigma$

This construction has a variety of immediate generalizations, for instance $\Sigma$ may have [[manifold with boundary|boundary]] and [[manifold with corners|corners]], and it may be a [[supermanifold]] and/or a [[formal manifold]]; and the [[mapping space]] may be generalized to a [[space of sections]] of a given [[fiber bundle]]. Finally, the construction also generalizes to coefficients richer than differential forms, such as [[cocycles]] in [[differential cohomology]], but this is no longer the topic of the present entry.

Important examples of transgression of differential forms appear in [[Lagrangian field theory]] (in the sense of [[physics]]) defined by a [[Lagrangian density|Lagrangian form]] on the [[jet bundle]] of a [[field bundle]]. Here the transgression of the Lagrangian itself is the corresponding _[[action functional]]_, the transgression of its [[Euler-Lagrange operator|Euler-Lagrange variational derivative]] is the 1-form whose vanishing is the _[[equations of motion]]_ and the transgression of the induced [[pre-symplectic current]] is the _[[pre-symplectic form]] on the [[covariant phase space]]_ of the field theory. 


## Definition

There are two definitions of transgression of differential forms: A traditional formulation is def. \ref{TransgressionOfDifferentialFormsToMappingSpacesViaEvaluationMap} below, which transgresses by [[pullback of differential forms]] along the [[evaluation map]], followed by [[integration of differential forms]].

Another definition is useful, which makes more use of the existence of smooth classifying spaces for differential forms in [[smooth sets]], this we consider as def. \ref{ParameterizedIntegrationOfDifferentialForms} below.

That these two definitions are indeed equivalent is the content of prop. \ref{EquivalenceOfTransgressionOfDifferentialFormsToMappingSpaces} below


### Preliminaries on smooth sets

Since the concept of transgression of differential forms involves [[mapping spaces]] between, in particular, [[smooth manifolds]], it is most conveniently formulated in terms of the concept of [[generalized smooth spaces]] called _[[smooth sets]]_. For the following discussion we assume background on [[smooth sets]] as introduced in 

* _[[geometry of physics -- smooth sets]]_

* _[[geometry of physics -- differential forms]]_.

(This entry itself here overlaps with _[[geometry of physics -- integration]]_, where more background may be found.)

Recall form the discussion there that a [[smooth set]] $X$ is _defined_ by specifying, in a consistent way, what counts as a smooth functions $U \to X$  from a [[Cartesian space]] $U$ (a "plot" of $X$). Given two smooth sets $X$ and $Y$ then a [[smooth function]] $f \;\colon\; X \longrightarrow Y$ is a function that takes plots $U \overset{\phi}{\to} X$ of $X$ to plots $f \circ \phi \colon U \to Y$ of $Y$. 

A key example of a smooth set which is in general not a [[smooth manifold]] is the [[mapping space]] $[X,Y]$ between two smooth sets $X$ and $Y$, hence the set of all smooth functions $X \to Y$ equipped with a smooth structure itself. Namely a plot $\phi_{(-)} \colon U \to [X,Y]$ is defined to be a smooth function $\phi_{(-)}(-) \colon U \times X \to Y$ out of the [[Cartesian product]] of $U$ with $X$ to $Y$,  hence a "U-parameterized smooth family of smooth functions".

An example of a smooth set which is far from being a smooth manifold is for $n \in \mathbb{N}$ the smooth set $\mathbf{\Omega}^n$ which is the "smooth [[classifying space]]" for [[differential n-forms]], defined by the rule that a smooth function $\phi \colon U \to \mathbf{\Omega}^n$ is equivalently a smooth differential $n$-form on $U$ (to be thought of as the [[pullback of differential forms|pullback]] of a "universal $n$-form" on $\mathbf{\Omega}^n$ along $\phi$).
It follows from this in particular that for $X$ any [[smooth manifold]] then smooth functions $X \to \mathbf{\Omega}^n$ are equivalent to smooth $n$-forms on $X$. Accordingly we may say that for $X$ any [[smooth set]] (which may be far from being a smooth manifold) then a differential $n$-form on $X$ is equivalently a smooth function $X \to \mathbf{\Omega}^n$. Under this identification the operation of [[pullback of differential forms]] along some smooth function $f \colon Y \to X$ is just [[composition]] of smooth functions $f^\ast \omega \colon Y \overset{f}{\to} X \overset{\omega}{\to} \mathbf{\Omega}^n$.

These examples may be combined: the [[mapping space]] $[\Sigma, \mathbf{\Omega}^n]$ is a kind of smooth classifying space for differential forms _on_ $\Sigma$: a smooth function $\omega_{(-)} \colon U \to [\Sigma,\mathbf{\Omega}^n]$ into this space is, by the above, a [[differential n-form]] on the [[Cartesian product]] $U \times \Sigma$.

(There is a smooth space that has more right to be called "the" classifying space of differential $n$-foms on $\Sigma$, namely the [[concretification]] $\sharp_1 [\Sigma, \mathbf{\Omega}^n]$, but for the discussion of trangression actually the unconcretified space is the right one to use.)




### Via parameterized integration of differential forms


+-- {: .num_defn #ParameterizedIntegrationOfDifferentialForms}
###### Definition
**(parameterized [[integration of differential forms]])

Let 

1. $X$ be a [[smooth set]];

1. $n \geq k \in \mathbb{N}$;

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$.

Then we write

$$
  \int_{\Sigma}
    \;\colon\;
  [\Sigma_k, \mathbf{\Omega}^n]
    \longrightarrow
  \mathbf{\Omega}^{n-k}
$$

for the [[smooth function]] which takes a plot $\omega_{(-)} \colon U \to [\Sigma, \mathbf{\Omega}^k]$, hence equivalently a differential $n$-form $\omega_{(-)}(-)$ on $U \times \Sigma$ to the result of [[integration of differential forms]] over $\Sigma$:


$$
  \int_{\Sigma} \omega_{(-)}(-) \coloneqq \int_\Sigma \omega_{(-)}
  \,.
$$


=--


+-- {: .num_defn #TransgressionOfDifferentialFormsToMappingSpaces}
###### Definition
**(transgression of differential forms to [[mapping spaces]])

Let 

1. $X$ be a [[smooth set]];

1. $n \geq k \in \mathbb{N}$;

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$.

Then the operation of _transgression of differential $n$-forms_ on $X$ with respect to $\Sigma$ is the [[function]]

$$
  \tau_\Sigma
   \coloneqq
  \int_\Sigma [\Sigma,-]
   \;\colon\;
  \Omega^n(X) \to \Omega^{n-k}([\Sigma,X])
$$

from differential $n$-forms on $X$ to differential $n-k$-forms on the [[mapping space]] $[\Sigma,X]$ which takes the differential form corresponding to the smooth function

$$
  (X \stackrel{\omega}{\to} \Omega^n) \in \Omega^n(X)
$$

to the differential form corresponding to the following composite smooth funtion:

$$
  \tau_\Sigma \omega
   \coloneqq
  \int_{\Sigma} [\Sigma,\omega]
   \;\colon\;
  [\Sigma, X] 
    \stackrel{[\Sigma, \omega]}{\to}  
  [\Sigma, \Omega^n]
    \stackrel{\int_{\Sigma}}{\to}
  \Omega^{n-k}
  \,,
$$

where $[\Sigma,\omega]$ is the [[mapping space]] [[functor]] on [[morphisms]] and $\int_{\Sigma}$ is the parameterized integration of differential forms from def. \ref{ParameterizedIntegrationOfDifferentialForms}.

More explicitly in terms of plots this means equivalently the following 

A plot of the [[mapping space]]

$$
  \phi_{(-)} \;\colon\; U \to [\Sigma, X] 
$$

is equivalently a [[smooth function]] of the form

$$
  \phi_{(-)}(-) \;\colon\; U \times \Sigma \to X
  \,.
$$

The smooth function $[\Sigma,\omega]$ takes this smooth function to the plot

$$
  U \times \Sigma \to X
   \overset{\phi_{(-)}(-)}{\longrightarrow}
  X 
   \overset{\omega}{\longrightarrow}
  \mathbf{\Omega}^{n}
$$

which is equivalently a differential form

$$
  (\phi_{(-)}(-))^\ast \omega \in \Omega^n(U \times \Sigma)
  \,.
$$

Finally the smooth function $\int_\Sigma$ takes this to the result of [[integration of differential forms]] over $\Sigma$:

$$
  \tau_{\Sigma}\omega\vert_{\phi_{(-)}}
  \;=\;
  \int_\Sigma (\phi_{(-)}(-))^\ast \omega
  \;\in\;
  \Omega^{n-k}(U)
  \,.
$$


=--

### Via pullback along the evaluation map


+-- {: .num_defn #TransgressionOfDifferentialFormsToMappingSpacesViaEvaluationMap}
###### Definition
**(transgression of differential forms to mapping space via evaluation map)**

Let 

1. $X$ be a [[smooth set]];

1. $n \geq k \in \mathbb{N}$;

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$.

Then the operation of _transgression of differential $n$-forms_ on $X$ with respect to $\Sigma$ is the [[function]]

$$
  \tau_\Sigma
   \coloneqq
  \int_\Sigma ev^\ast
   \;\colon\;
  \Omega^n(X)
    \overset{ev^\ast}{\longrightarrow} 
  \Omega^n(\Sigma \times [\Sigma, X])
    \overset{\int_\Sigma}{\longrightarrow}
  \Omega^{n-k}([\Sigma,X])
$$

from differential $n$-forms on $X$ to differential $n-k$-forms on the [[mapping space]] $[\Sigma,X]$ which is the [[composition|composite]] of forming the [[pullback of differential forms]] along the [[evaluation map]] $ev \colon  [\Sigma, X] \times \Sigma \to X$ with [[integration of differential forms]] over $\Sigma$.


=--



+-- {: .num_prop #EquivalenceOfTransgressionOfDifferentialFormsToMappingSpaces}
###### Proposition

The two definitions of transgression of differential forms to mapping spaces from def. \ref{TransgressionOfDifferentialFormsToMappingSpaces} and def. \ref{TransgressionOfDifferentialFormsToMappingSpacesViaEvaluationMap} are equivalent.


=--

+-- {: .proof}
###### Proof


We need to check that for all plots $\gamma \colon U \to [\Sigma, X]$
the pullbacks of the two forms to $U$ coincide.

For def. \ref{TransgressionOfDifferentialFormsToMappingSpacesViaEvaluationMap} we get

$$
  \gamma^\ast \int_\Sigma \mathrm{ev}^\ast A
  =
  \int_\Sigma (\gamma,\mathrm{id}_\Sigma)^\ast \mathrm{ev}^\ast A
  \;
  \in \Omega^n(U)
$$

Here we recognize in the integrand the pullback along
the $( (-)\times \Sigma \dashv [\Sigma,-])$-[[adjunct]] $\tilde \gamma : U \times \Sigma \to \Sigma$ of $\gamma$,
which is given by applying the [[left adjoint]] $(-)\times \Sigma$ and then postcomposing with the adjunction counit $\mathrm{ev}$:

$$
  \array{
    U \times \Sigma
    &
     \overset{(\gamma, \mathrm{id}_\Sigma)}{\longrightarrow}
    &
    [\Sigma,X] \times \Sigma
    &
      \overset{\mathrm{ev}}{\longrightarrow}
    &
    X
  }
  \,.
$$
 
Hence the integral is now

$$
  \cdots = \int_{\Sigma} \tilde \gamma^\ast A
  \,.
$$

This is the operation of the top horizontal composite in the following
[[natural transformation|naturality square]] for [[adjuncts]], and so the claim follows by its [[commuting diagram|commutativity]]:

$$
  \array{
    \tilde \gamma \in 
    & 
    \mathbf{H}(U \times\Sigma, X)
    &
      \overset{\mathbf{H}(U \times \Sigma,A)}{\longrightarrow}
    &    
    \mathbf{H}(U \times \Sigma, \mathbf{\Omega}^{n+k})
    &
      \overset{\int_\Sigma(U)}{\longrightarrow}
    &
    \Omega^n(U)
    \\
    &
    {}^{\mathllap{\simeq}}\downarrow
      &&
    {}^{\mathllap{\simeq}}\downarrow
      &&
    {}^{\mathllap{\simeq}}\downarrow
    \\
    \gamma \in 
    & 
    \mathbf{H}(U,[\Sigma,X])
    &
      \overset{\mathbf{H}(U,[\Sigma,A])}{\longrightarrow}
    &
    \mathbf{H}(U,[\Sigma,\mathbf{\Omega}^{n+k}])
    &
      \overset{\mathbf{H}(U,\int_\Sigma)}{\longrightarrow}
    & 
    \mathbf{H}(U,\mathbf{\Omega}^n)
  }
$$

(here we write $\mathbf{H}(-,-)$ for the [[hom functor]] of [[smooth sets]]).

=--

## Properties

### Relative transgression over manifolds with boundary

+-- {: .num_prop }
###### Proposition
**(relative transgression over [[manifolds with boundary]])**

1. $X$ be a [[smooth set]];

1. $n \geq k \in \mathbb{N}$;

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$ with [[manifold with boundary|boundary]] $\partial \Sigma$

1. $\omega \in \Omega^n_{X}$ a [[closed differential form]].

Write

$$ 
  (-)\vert_{\partial \Sigma}
    \;\coloneqq\;
  [\partial \Sigma \hookrightarrow \Sigma, X]
  \;\colon\;
  [\Sigma, X]
   \longrightarrow
  [\partial \Sigma, X]
$$

for the smooth function that restricts smooth functions on $\Sigma$ to smooth functions on the [[boundary]] $\partial \Sigma$.

Then the operations of transgression of differential forms (def. \ref{TransgressionOfDifferentialFormsToMappingSpaces}) to $\Sigma$ and to $\partial \Sigma$, respectively, are related by


$$
  d \left(
    \tau_{\Sigma}(\omega)
  \right)
  = 
  (-1)^{k+1}
  ((-)\vert_{\partial \Sigma})^\ast \tau_{\partial \Sigma}(\omega)
    \phantom{AAAAAAAA}
  \array{
    [\Sigma, X] 
      &\overset{ \tau_{\Sigma}(\omega) }{\longrightarrow}&
    \mathbf{\Omega}^{n-k}
    \\
    {}^{\mathllap{(-)\vert_{\partial \Sigma} }}\downarrow
      &&
    \downarrow^{\mathrlap{ (-1)^{k+1} d}}
    \\
    [\partial \Sigma, X]
      &\underset{ \tau_{\partial\Sigma}(\omega) }{\longrightarrow}&
    \mathbf{\Omega}^{n-k+1}
  }
  \,.
$$

In particular this means that if the compact manifold $\Sigma$ happens to have no boundary (is a [[closed manifold]]) then transgression over $\Sigma$ takes closed differential forms to closed differential forms.


=--

+-- {: .proof}
###### Proof

Let $\phi_{(-)}(-) \colon U \times \Sigma \to X$ be a plot of the mapping space $[\Sigma, X]$. Notice that the [[de Rham differential]] on the [[Cartesian product]] $U \times \Sigma$ decomposes as

$$
  d = d_U + d_\Sigma
  \,.
$$

Now we compute as follows:


$$
  \begin{aligned}
    d \tau_{\Sigma}\omega\vert_{\phi_(-)}
    & =
    d_U \int_\Sigma (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    (-1)^k \int_\Sigma d_U (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    (-1)^k \int_\Sigma (d - d \Sigma) (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    (-1)^k \int_\Sigma d (\phi_{(-)}(-))^\ast \omega
    -
    (-1)^k \int_\Sigma d_\Sigma (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    (-1)^k \int_\Sigma (\phi_{(-)}(-))^\ast \underset{= 0}{\underbrace{d \omega}}
    -
    (-1)^k \int_\Sigma d_\Sigma (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    -
    (-1)^k \int_\Sigma d_\Sigma (\phi_{(-)}(-))^\ast \omega
    \\
    & =
    -(-1)^k \int_{\partial \Sigma} (\phi_{(-)}(-))^\ast \omega   
    \\
    & = 
    -(-1)^k \tau_{\partial \Sigma} \omega \vert_{\phi_{(-)}}
  \end{aligned}
$$

where in the second but last step we used [[Stokes' theorem]].

=--

## Examples


We discuss some examples and applications:

* [Gauge coupling action functional of charged particle](#GaugeCouplingActionFunctionalOfChargedParticle)

* [Transgression of Killing form to symplectic form of Chern-Simons theory](#TransgressionOfKillingFormToSymplecticFormOfChernSimons)

### Gauge coupling action functional of charged particle
 {#GaugeCouplingActionFunctionalOfChargedParticle}

Let $X \in \mathbf{H}$ and consider a [[circle group]]-[[principal connection]] $\nabla \colon X \to \mathbf{B}U(1)_{conn}$ over $X$. By the discussion in _[Dirac charge quantization and the electromagnetic field](#DiracChargeQuantizationAndElectromagneticField)_ above this encodes an [[electromagnetic field]] on $X$. Assume for simplicity here that the underlying [[circle principal bundle]] is trivialized, so that then the connection is equivalently given by a differential 1-form

$$
  \nabla = A \;\colon\; X \to \mathbf{\Omega}^1
  \,,
$$

the _[[electromagnetic potential]]_.

Let then $\Sigma = S^1$ be the [[circle]].  The [[transgression]] of the electromagnetic potential to the [[loop space]] of $X$ 

$$
  \int_{S^1} [S^1, A]
   \;\colon\;
  [S^1, X]
    \stackrel{[S^1, A]}{\to}
  [S^1 , \Omega^1]
    \stackrel{\int_{S^1}}{\to}
  \Omega^0
  \simeq
  \mathbb{R}
$$

is the [[action functional]] for an [[electron]] or other electrically charged [[particle]] in the [[background gauge field]] $A$ is $S_{em} = \int_{S^1} [S^1, A]$.

The [[variational calculus|variation]] of this contribution in addition to that of the [[kinetic action]]  of the electron gives the _[[Lorentz force]]_ law describing the [[force]] exerted by the [[background gauge field]] on the electron.

### Transgression of Killing form to symplectic form of Chern-Simons theory
 {#TransgressionOfKillingFormToSymplecticFormOfChernSimons}

Let $\mathfrak{g}$ be a [[Lie algebra]] with 
binary [[invariant polynomial]] 
$\langle -,-\rangle \colon \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{R}$.

For instance $\mathfrak{g}$ could be a [[semisimple Lie algebra]] and $\langle -,-\rangle$ its [[Killing form]]. In particular if $\mathfrak{g} = \mathfrak{su}(n)$ is a [[matrix Lie algebra]] such as the [[special unitary Lie algebra]], then the Killing form is given by the [[trace]] of the product of two matrices.

This pairing $\langle -,-\rangle$ defines a differential 4-form on the [[smooth space]] of [[Lie algebra valued 1-forms]]

$$
  \langle F_{(-)} \wedge F_{(-)} \rangle
  \colon
  \Omega^1(-,\mathfrak{g})
   \stackrel{F_{(-)}}{\to}
  \Omega^2(-, \mathfrak{g})
   \stackrel{(-)\wedge (-)}{\to}
  \Omega^4(-, \mathfrak{g}\otimes \mathfrak{g})
   \stackrel{\langle-,-\rangle}{\to}
  \Omega^4
$$

Over a [[coordinate patch]] $U \in $ [[CartSp]] this sends a differential 1-form $A \in \Omega^1(U)$ to the differential 4-form

$$
  \langle F_A \wedge F_A \rangle \in \Omega^4(U)
  \,.
$$

The fact that $\langle -, - \rangle$ is indeed an _[[invariant polynomial]]_ means that this indeed extends to a 4-form on the smooth [[groupoid of Lie algebra valued forms]]

$$
  \langle F_{(-)} \wedge F_{(-)}\rangle
  \colon
  \mathbf{B}G_{conn}
  \to 
  \Omega^4
  \,.
$$

Now let $\Sigma$ be an [[orientation|oriented]] [[closed manifold|closed]] [[smooth manifold]].  The [[transgression]] of the above 4-form to the [[mapping space]] out of $\Sigma$ yields the 2-form

$$
  \omega
    \coloneqq
  \int_{\Sigma} \langle F_{(-)}\wedge F_{(-)}\rangle
   \colon
  \mathbf{\Omega}^1(\Sigma,\mathfrak{g})
   \hookrightarrow
  [\Sigma, \mathbf{B}G_{conn}]
    \stackrel{[\Sigma, \langle F_{(-)}\wedge F_{(-)}\rangle]}{\to}
  [\Sigma, \Omega^4]
    \stackrel{\int_{\Sigma}}{\to}
  \Omega^2
$$

to the [[moduli stack]] of [[Lie algebra valued 1-forms]] on $\Sigma$.

Over a [[coordinate chart]] $U = \mathbb{R}^n \in $ [[CartSp]] an element $A \in \mathbf{\Omega}^1(\Sigma,\mathfrak{g})(\mathbb{R}^n)$ is a $\mathfrak{g}$-valued 1-form $A$ on $\Sigma \times U$ with no leg along $U$. Its [[curvature]] 2-form therefore decomposes as

$$
  F_A = F_A^{\Sigma} + \delta A
  \,,
$$

where $F_A^{\Sigma} $ is the curvature component with all legs along $\Sigma$ and where

$$
  \delta A
  \coloneqq 
  - \sum_{i = 1}^n \frac{\partial}{\partial x^i} A \wedge \mathbf{d}x^i
$$

is the [[variational calculus|variational]] derivative of $A$.

This means that in the 4-form

$$
  \langle F_A \wedge F_A\rangle
  = 
  \langle F_A^\Sigma \wedge F_A^\Sigma \rangle
  + 
  2 \langle F_A^\Sigma \wedge \delta A\rangle 
  + 
  \langle \delta A \wedge \delta A\rangle 
  \in
  \Omega^4(\Sigma \times U)
$$

only the last term gives a 2-form contribution on $U$. Hence we find that the transgressed 2-form is

$$
  \omega = \int_\Sigma \langle \delta A \wedge \delta A\rangle
   \colon
  \mathbf{\Omega}^1(\Sigma, \mathfrak{g})
   \to
  \Omega^2
  \,.
$$

When restricted further to flat forms

$$
  \mathbf{\Omega^1}_{flat}(\Sigma,\mathfrak{g})
  \hookrightarrow
  \mathbf{\Omega^1}(\Sigma,\mathfrak{g})  
$$

which is the [[phase space]] of $\mathfrak{g}$-[[Chern-Simons theory]], then this is the corresponding [[symplectic form]] (by the discussion at _[Chern-Simons theory -- covariant phase space](Chern-Simons+theory#CovariantPhaseSpace)_).




[[!redirects transgression of differential forms]]

