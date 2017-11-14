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
       (k_0)^2 - {\vert \vec k\vert}^2  -\left( \tfrac{m c}{\hbar}\right)^2 \mp i \epsilon  
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
       (k_0)^2 - \left(\omega_\epsilon(\vec k)/c\right)
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
         k_0 - \omega_\epsilon(\vec  k)/c
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
          
          & \pm (x^0 - y^0) \gt 0
       }
     \right.
  \end{aligned}
$$
