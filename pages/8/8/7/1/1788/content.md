
$$
  \begin{aligned}
    \int
    \frac{
      e^{i k_\mu x^\mu}
    }{
      k_\mu k^\mu
    }
    \, d^{p+1}k
    & =
    \int
    \int_0^\infty
      e^{
         i k_\mu x^\mu 
         -
         \tau 
         k_\mu k^\mu
      }
    \, d \tau
    \, d^{p+1} k
    \\
    & =
    \int 
    \int_0^\infty
      \exp\left(
         -
         \tau
         \left(
            k^\mu - \tfrac{i}{2 \tau} x^\mu
         \right)
         \left(
            k_\mu - \tfrac{i}{2 \tau} x^\mu
         \right)
         -
         \tfrac{4}{\tau} x^\mu x_\mu
      \right)
      \, d \tau
      \, d^{p+1} k
     \\
    \\
    & =
    \int 
    \int_0^\infty
      \exp\left(
         -\tau
         k_\mu k^\mu
         -
         \tfrac{4}{\tau} x^\mu x_\mu
      \right)
      \, d \tau
      \, d^{p+1} k
    \\
    & =
    \int 
    \int_0^\infty
      \exp\left(
         -\tau
         -
         \tfrac{4}{\tau} k_\mu k^\mu x^\mu x_\mu
      \right)
      \, d \tau
         \frac{1}{k_\mu k^\mu}
      \, d^{p+1} k
    \\
    & =
    \int 4\sqrt{k^2} \sqrt{x^2} K_{-1}\left(4 \sqrt{k^2} \sqrt{x^2}\right)
    \,\frac{d^{p+1} k}{k^2}
  \end{aligned}
$$

where the last step is [DLMF 10.32.10](http://dlmf.nist.gov/10.32#E10)

second attempt
 {#second}

$$
  \begin{aligned}
    \int
    \frac{
      e^{i k_\mu x^\mu}
    }{
      k_\mu k^\mu + m^2
    }
    \, d^{p+1}k
    & =
    \int
    \int_0^\infty
      e^{
         i k_\mu x^\mu
         -
         \tau
         (k_\mu k^\mu + m^2)
      }
    \, \frac{d \tau}{\tau}
    \, d^{p+1} k
    \\
    & =
    \int
    \int_0^\infty
      \exp\left(
         -
         \tau
         \left(
            k^\mu - \tfrac{i}{2 \tau} x^\mu
         \right)
         \left(
            k_\mu - \tfrac{i}{2 \tau} x^\mu
         \right)
         -
         \tfrac{4}{\tau} x^\mu x_\mu - \tau m^2
      \right)
      \, d \tau
      \, d^{p+1} k
     \\
    \\
    & =
    (\pi)^{(p+1)/2}
    \int_0^\infty
      \tau^{-(p+1)/2}
      \exp\left(
         -\tau m^2
         -
         \tfrac{4}{\tau} x^\mu x_\mu
      \right)
      \, d \tau
    \\
    & =
    (\pi)^{(p+1)/2}
    \int_0^\infty
      \tau^{-(p+1)/2}
      \exp\left(
         -\tau
         -
         \tfrac{4}{\tau} m^2 x^\mu x_\mu
      \right)
      \, \frac{d \tau}{m^2}
    \\
    & =
    \frac{1}{m^2 (\pi)^{(p+1)/2}}
    \frac{1}{2} \left(\frac{m\sqrt{x^\mu x_\mu}}{2}\right)^{-(p+1)/2+1}
    K_{(p+1)/2-1}\left(m \sqrt{x^\mu x_\mu}\right)
  \end{aligned}
$$


where the last step is [DLMF 10.32.10](http://dlmf.nist.gov/10.32#E10)


this diverges for $x^2 \to 0$ as $(x^2)^{-(p+1)/2 + 1}$ ([DLMF 10.30.2](http://dlmf.nist.gov/10.30#E2))