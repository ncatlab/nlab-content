
+-- {: .num_example}
###### Remark

If the argument functions $f,g$ admit [[Fourier analysis]] (are [[functions with rapidly decreasing partial derivatives]]), then  the [[star product]] from def. \ref{StarPoduct} is equivalently given by the following [[integral]] expression:

$$
  \begin{aligned}
  \left(f \star_\omega g\right)(x)
   &= 
  \frac{(det(\omega)^{2n})}{(2 \pi \hbar)^{2n} }
  \int
    e^{ - \tfrac{1}{i \hbar} \omega((x - \tilde y),(x-y))}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \end{aligned}
$$

=--

+-- {: .proof}
###### Proof

We compute as follows:

$$
  \begin{aligned}
  \left(f \star_\omega g\right)(x)
  & \coloneqq
  prod 
    \circ \exp\left(
       \hbar \omega^{i j} \frac{\partial}{\partial x^i} \otimes \frac{\partial}{\partial x^j}
  \right)(f, g)
  \\
  & =
  \frac{1}{(2 \pi)^{2n}}
  \frac{1}{(2 \pi)^{2n}}
  \int
  \int
    \underbrace{
      e^{ i \hbar \omega^{-1}(k,q) }
    }
    \underbrace{
      e^{i k \cdot (x-y)}
      f(y)
    }
    \underbrace{
      e^{i q \cdot (x- \tilde y)}
      g(\tilde y)
    }
   \,
   d^{2 n} k
   \,
   d^{2 n} q
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
   \\
   & =
  \frac{1}{(2 \pi)^{2n}}
  \int
    \delta\left( x - \tilde y + \hbar \omega^{-1}(k) \right)
    e^{i k \cdot (x-y)}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} k
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \\
  & = 
  \frac{(det(\omega)^{2n})}{(2 \pi \hbar)^{2n} }
  \int
    e^{i \tfrac{1}{\hbar}\omega((x - \tilde y),(x-y))}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \end{aligned}
$$

Here in the first step we expressed $f$ and $g$ both by their [[Fourier transform]] (inserting the Fourier expression of the [[delta distribution]] from [this example](Dirac+distribution#FourierTransformOfDeltaDistribution)) and used that under this transformation the [[partial derivative]] $\omega^{a b} \frac{\partial}{\partial\phi^a}{\frac{\partial}{\phi^b}}$ turns into the product with $i \omega^{i j} k_i k_j$ ([this prop.](Fourier+transform#BasicPropertiesOfFourierTransformOverCartesianSpaces)). 
Then we identified again the Fourier-expansion of a [[delta distribution]]
and finally we applied the [[change of integration variables]] $k = \tfrac{1}{\hbar} \omega(z)$ and evaluated the [[delta distribution]].

=--