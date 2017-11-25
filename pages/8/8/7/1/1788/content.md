

We have seen that the [[positive real number|positive]] [[frequency]] component of the [[causal propagator]] $\Delta_S$ for the [[Klein-Gordon equation]] on [[Minkowski spacetime]] (prop. \ref{AdvancedRetardedPropafatorsForKleinGordonOnMinkowskiSpacetime}) is the [[Hadamard propagator]] $\Delta_H$ (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime}) given, according to prop. \ref{SkewSymmetricPartOfHadmrdPropagatorIsCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetime}, by (eq:DeompositionOfHadamardPropagatorOnMinkowkski)

$$
  \begin{aligned}
    \Delta_H
    & =
    \tfrac{i}{2} \Delta_S
    +
    H
    \\
    & =
    \tfrac{i}{2}
    \left(
      \Delta_+ - \Delta_-
    \right)
    +
    H
  \end{aligned}
  \,,
$$

+-- {: .num_defn #FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}
###### Definition
**([[Feynman propagator]] for [[Klein-Gordon equation]] on [[Minkowski spacetime]])**

The _[[Feynman propagator]]_ for the [[Klein-Gordon equation]] on [[Minkowski spacetime]] is the [[linear combination]]

$$
  \Delta_F
  \coloneqq
    \tfrac{i}{2}
    \left(
      \Delta_+ + \Delta_-
    \right)
    +
    H
$$

where the first terms is proportional to the sum instead of the [[advanced and retarded propagators]] (prop. \ref{AdvancedRetardedPropafatorsForKleinGordonOnMinkowskiSpacetime}) and the second is the symmetric part of the [[Hadamard propagator]] according to prop. \ref{SkewSymmetricPartOfHadmrdPropagatorIsCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetime}.

=--


+-- {: .num_prop #ModeExpansionForFeynmanPropagatorOfKleinGordonEquationOnMinkowskiSpacetime}
###### Proposition
**(mode expanion for [[Feynman propagator]] of [[Klein-Gordon equation]] on [[Minkowski spacetime]])**

The [[Feynman propagator]] (def. \ref{FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}) for the [[Klein-Gordon equation]] on [[Minkowski spacetime]] is given by

$$
  \begin{aligned}
  \Delta_F(x,y)
  & =
  \left\{
    \array{
    \frac{1}{(2\pi)^p}
    \int
    \frac{1}{\omega(\vec k)c}
    e^{-i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot \vec x}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \gt 0
    \\
    \frac{1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{+i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot \vec x}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \lt 0
    }
  \right.
  \\
  &=
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{-i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu (x^\mu - y^\mu)}
  }{
    - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 + i \epsilon
  }
  \, d k_0 \, d^p \vec k
  \end{aligned}
$$

Here in the second line we have a [[limit of a sequence|limit]] of [[distributions]] as for the [[Cauchy principal value]] ([this prop](#CauchyPrincipalValueEqualsIntegrationWithImaginaryOffsetPlusDelta)).

=--

+-- {: .proof}
###### Proof


By prop. \ref{ModeExpansionForMinkowskiAdvancedRetardedPropagator} and the expression for $H$ from(eq:SymmetricPartOfHadamardPropagatorForKleinGordonOnMinkowskiSpacetime) we have

$$
  \begin{aligned}
   \Delta_F(x,y)
   & =
  \left\{
    \array{
      \underset{
        = \tfrac{i}{2} \Delta_+(x,y) + 0 \;\text{for}\; (x^0 - y^0) \gt 0
      }{
      \underbrace{
      \frac{- i}{(2\pi)^{p}}
      \int
      \frac{1}{2 \omega(\vec k)/c}
      \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
      e^{i \vec k \cdot (\vec x - \vec  y) }
      \, d^p \vec k
      }
      }
      +
      \underset{
        = H(x,y)
      }{
      \underbrace{
      \frac{1}{(2\pi)^p}
      \int \frac{1}{2 \omega(\vec k)/c}
      \cos\left( \omega(\vec k)(x^0 - y^0)/c  \right)
      e^{i \vec k \cdot (\vec x - \vec y) }
      \, d^p \vec k
      }
      }
      &\vert&
      (x^0 - y^0) \gt 0
      \\
      \underset{
         = 0 + \tfrac{i}{2}\Delta_-(x,y) \;\text{for}\; (x^0 - y^0) \lt 0
      }{
      \underbrace{
      \frac{+ i}{(2\pi)^{p}}
      \int
      \frac{1}{2 \omega(\vec k)/c}
      \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
      e^{i \vec k \cdot (\vec x - \vec  y) }
      \, d^p \vec k
      }
      }
      +
      \underset{ = H(x,y) }{
      \underbrace{
      \frac{1}{(2\pi)^p}
      \int \frac{1}{2 \omega(\vec k)/c}
      \cos\left( \omega(\vec k)(x^0 - y^0)/c  \right)
      e^{i \vec k \cdot (\vec x - \vec y) }
      \, d^p \vec k
      }
      }
      &\vert&
      (x^0 - y^0) \lt 0
    }
  \right.
  \\
  & = 
  \left\{
    \array{
    \frac{1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{-i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot \vec x}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \gt 0
    \\
    \frac{1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{+i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot \vec x}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \lt 0
    }
  \right.
  \end{aligned}
$$

where in the second line we used [[Euler's formula]].

For the second statement we compute as follows:

$$
  \begin{aligned}
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{-i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu (x^\mu - y^\mu)}
  }{
    - k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 + i \epsilon
  }
  \, d k_0 \, d^p \vec k
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{-i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu (x^\mu - y^\mu)}
  }{
    (k_0)^2 
      - 
    \underset{
      \coloneqq \omega_\epsilon(\vec k)^2/c^2
    }{\underbrace{ \left( \omega(\vec k)^2/c^2 - i \epsilon \right) }}
  }
  \, d k_0 \, d^p \vec k  
  \\
  & =
  \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{-i}{(2\pi)^{p+1}}
  \int
  \int_{-\infty}^\infty
  \frac{
     e^{i k_\mu (x^\mu - y^\mu)}
  }{
     \left(
       k_0 - \omega_\epsilon(\vec k)/c
     \right)
     \left(
       k_0 + \omega_\epsilon(\vec k)/c
     \right)
  }
  \, d k_0 \, d^p \vec k  
  \\
  & =
  \left\{
    \array{
    \frac{1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{-i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot \vec x}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \gt 0
    \\
    \frac{1}{(2\pi)^p}
    \int
    \frac{1}{2\omega(\vec k)c}
    e^{+i\omega(\vec k)(x^0 - y^0)/c} e^{i \vec k \cdot \vec x}
    \, d^p \vec k
    &\vert&
    (x^0 - y^0) \lt 0
    }
  \right.
  \end{aligned}
$$

Here 

1. In the first step we introduced the [[complex number|complex]] [[square root]] $\omega_\epsilon(\vec k)$. For this to be compatible with the choice of _non-negative_ square root for $\epsilon = 0$ in (eq:DispersionRelationForKleinGordonooeratorObMinkowskiSpacetime) we need to choose that complex square root whose [[complex phase]] is one half that of $\omega(\vec k)^2 - i \epsilon$ (instead of that plus $\pi$). This means that $\omega_\epsilon(\vec k)$ is in the _[[lower half plane]]_.

1. In the third step we observe that

   1. for $(x^0 - y^0) \gt 0$ the [[integrand]] decays for [[positive real number|positive]] [[imaginary part]] and hence the integration over $k_0$ may be deformed to a [[Jordan curve|contour]] which encircles the [[pole]] in the [[upper half plane]];


   1. for $(x^0 - y^0) \lt 0$ the integrand decays for [[negative real number|negative]] [[imaginary part]]  and hence the integration over $k_0$ may be deformed to a [[Jordan curve|contour]] which encircles the [[pole]] in the [[lower half plane]]

   and then apply [[Cauchy's integral formula]] which picks out $2\pi i$ times the [[residue]] a these poles.

<img src="https://ncatlab.org/nlab/files/ContourForFeynmanPropagator.png" height="300">


=--