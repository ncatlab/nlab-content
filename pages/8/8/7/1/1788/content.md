$$
  \begin{aligned}
    \Delta_\pm(x-y)
     & =
     \frac{1}{(2\pi)^{p+1}}
     \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
     \int \int
     \frac{ 
       e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
     }{
       (k_0 \mp i\epsilon)^2 - {\vert \vec k\vert}^2  -\left( \tfrac{m c}{\hbar}\right)^2 
     }
     \, d k_0 \, d^p \vec k
     \\
     & =
     \frac{1}{(2\pi)^{p+1}}
     \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
     \int \int
     \frac{ 
       e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
     }{
       (k_0 \mp i \epsilon)^2 - \left(\omega(\vec k)/c\right)^2
     }
     \, d k_0 \, d^p \vec k
     \\
     &=
     \frac{1}{(2\pi)^{p+1}}
     \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
     \int \int
     \frac{ 
       e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
     }{
       \left(
         (k_0 \mp i\epsilon) - \omega(\vec  k)/c
       \right)
       \left(
          (k_0 \mp i \epsilon) + \omega(\vec k)/c
       \right)
     }
     \, d k_0 \, d^p \vec k
     \\
     & = 
     \left\{
       \array{
          \underset{ {\epsilon \in (o,\infty)} \atop {\epsilon \to 0} }{\lim}
          \frac{1}{(2\pi)^{p+1}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)/x} + i \vec k \cdot (\vec x - \vec  y)
            \right)
          d^p \vec k          
          & \vert & \text{if} \,  \pm (x^0 - y^0) \gt 0
          \\
          0 & \vert & \text{otherwise}
       }
     \right.
     \\
     & =
     \left\{
       \array{
          \frac{1}{(2\pi)^{p+1}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)/x} + i \vec k \cdot (\vec x - \vec  y)
            \right)
          d^p \vec k          
          &  \vert &\text{if} \, \pm (x^0 - y^0) \gt 0
          \\
          0 & \vert &  \text{otherwise}
       }
     \right.
  \end{aligned}
$$

Here key step is the application of [[Cauchy's integral formula]] in the fourth step. We discuss this for $\Delta_+$, the discussion for $\Delta_-$ is the same, just with the appropriate signs reversed.

1. If  $(x^0 - y^0) \gt 0$ thn the expression $e^{ik_0 (x^0 - y^0)}$ decays with _[[positive number|positive]] [[imaginary part]]_ of $k_0$, so that we may expand the [[integration]] [[domain]] into the [[upper half plane]] as

   $$
     \begin{aligned}
       \int_{-\infty}^\infty d k_0
       & = \phantom{+}
         \int_{-\infty}^0 d k_0 + \int_{0}^{+ i \infty} d k_0
       \\
       & = + \int_{+i \infty}^0 d k_0  + \int_0^\infty d k_0
       \,;
     \end{aligned}
   $$

   Conversely, if $(x^0 - y^0) \lt 0$ then we may analogously expand into the [[lower half plane]]. 

1. This integration domain may then further be completed to two [[contour integrations]]. For the expansion into the [[upper half plane]] these encircle counter-clockwise the [[poles]] at $\pm \omega(\vec k)+ i\epsilon \in \mathbb{C}$, while for expansion into the [[lower half plane]] no poles are being encircled.

   <img src="https://ncatlab.org/nlab/files/ContourForAdvancedPropagator.png" height="280">


1. Apply [[Cauchy's integral formula]] to find in the case $(x^0 - y^0)\gt 0$ the sum of the [[residues]] at these two [[poles]], zero in the other case.



$\,$

$\,$

$\,$

$\,$

Solutions to distributional equations of the form (in [[generalized function]]-notation)

$$
  \nu \, \widehat{\Delta_\pm}(\nu) = 1
$$

are given by sums of the [[Cauchy principal value]] $PV\left(\frac{1}{\nu}\right)$ with a multiple of the [[delta distribution]] ([this example.](Cauchy+principal+value#PrincipalValueOfInverseFunctionCharacteristicEquation)):

$$
  \label{PrincipalValuePlusDeltaAnsatzForFourierTransformedAdvPropagator}
  \widehat{\Delta_{\pm}}(\nu)
    \;=\;
   PV\left( \frac{1}{\nu}\right) + c \delta(\nu)
  \,.
$$

It is clear that (eq:PrincipalValuePlusDeltaAnsatzForFourierTransformedAdvPropagator) is a [[tempered distribution]] in $k$, so that our Ansatz via [[Fourier transform of distributions]] is indeed consistent so far.

We further specify this Ansatz by fixing the constant $c$ in (eq:PrincipalValuePlusDeltaAnsatzForFourierTransformedAdvPropagator) to $c = \pm i \pi$:

$$
  \widehat{\Delta_{\pm}}(\nu)
    \;=\;
   PV\left( \frac{1}{\nu}\right) \pm i\pi \delta(\nu)
  \,.
$$

As before, this will be justified if we later show that the inverse Fourier transform has the required future/past cone support property.

Now by [this example](Cauchy+principal+value#CauchyPrincipalValueEqualsIntegrationWithImaginaryOffsetPlusDelta) this particular Ansatz is in fact equal to the [[limit of a sequence|limit]] of $1/\nu$ with [[imaginary number|imaginary]] offset tending  to zero ([this def.](Cauchy+principal+value#IntegrationAgainstInverseOfxWithImaginaryOffset))

$$
  \widehat \Delta_{\pm}(\nu)
  \;=\;
  \underset{ {\epsilon \in (0,\infty)} \atop { \epsilon \to 0 } }{\lim} \frac{1}{\nu \pm i \epsilon^+}
   \,.
$$

Hence in summary our Ansatz for the [[Fourier transform of distributions|Fourier transformed]] advanced/retarded propagator is

$$
  \widehat \Delta_{\pm}(k)
  \;=\;
  \underset{ {\epsilon \in (0,\infty)} \atop { \epsilon \to 0 } }{\lim} \frac{1}{ (k_0)^2 -{\vert \vec k\vert}^2 - \left( \tfrac{m c}{\hbar} \right)^2  \pm i \epsilon^+}
   \,.
$$

