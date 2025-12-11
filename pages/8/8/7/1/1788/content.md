> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak


***

For [[5D Maxwell-Chern-Simons theory]] on a [[spacetime]] $X^{1,4}$

* the local [[field (physics)|field]] content is a 1-form [[gauge potential]] $A \in \Omega^1_{dR}(X^{1,4})$

* the [[Lagrangian density]] is:

  $$
    L 
    \;\coloneqq\;
    \tfrac{1}{2}\mathrm{d}A \wedge \star \mathrm{d}A
    \,-\,
    \tfrac{1}{6} A \wedge \mathrm{d}A \wedge \mathrm{d}A
    \mathrlap{\,,}
  $$

where $\star$ is the [[Hodge star operator]] for the [[pseudo-Riemannian metric]] on $X^{1,d}$.

The [[Euler-Lagrange equations]] [[equations of motion|of motion]] are

$$
  \left.
  \begin{aligned}
    \mathrm{d}\, F_2 & = 0
    \\
    \mathrm{d}\, G_3 & = \tfrac{1}{2} F_2 \wedge F_2
  \end{aligned}
  \right\}
  \,,
  \;\;
  \text{where}
  \;\;
  \left\{
  \begin{aligned}
    F_2 & \coloneqq \mathrm{d}A
    \\
    G_3 & \coloneqq \star F_2
    \,.
  \end{aligned}
  \right.
$$

While $G_3$ is not closed, the combination
$$
  \widetilde G_3 
  \,\coloneqq\,
  G_3 - \tfrac{1}{2} A \wedge F_2
$$
is closed:
$$
  \mathrm{d}\, \widetilde G_3
  \;=\;
  0
  \mathrlap{\,.}
$$

Considering now

* a [[globally hyperbolic spacetime]]

  $$
    X^{1,4} \simeq \mathbb{R}^{1,0} \times X^4
  $$

  with [[Cauchy surface]] 

  $$
    \iota \colon X^d \hookrightarrow X^{1,4}
    \mathllap{\,,}
  $$

* [[temporal gauge]]$\;$$A_0 = 0$

  whence we now understand $A \in \Omega^1_{dR}(X^4)$.

The [[canonical momentum]] to the [[gauge potential]] $A$ is

$$
  \widetilde E_3 
    \;\coloneqq\;
  \tfrac{\partial L}{\partial (\partial_0 A)}
    \;=\;
  \iota^\ast G_3 
    \,-\,
  \tfrac{1}{3} A \wedge B_2
  \,,
$$

whence the basic [[Poisson bracket]] is, for $\omega \in \Omega^1_{dR}(X^4)$, given by

$$
  \Big\{
    \textstyle{\int_{X^4}} \omega \wedge E
    ,\,
    A(x)
  \Big\}
  \;=\;
  \omega(x)
  \mathrlap{\,.}
$$

Setting 

$$
  \begin{aligned}
    B_2 
      & \coloneqq\, 
    \iota^\ast \mathrm{d}A
    \\
    E_3 
      & \coloneqq\, 
    \iota^\ast G_3
    \\
    & = 
    \widetilde E_3 + \tfrac{1}{3} A \wedge B_2 
  \end{aligned}
$$

we have Poisson brackets

$$
  \Big\{
    \textstyle{\int_{X_4}} \omega \wedge E_3
    ,\,
    \textstyle{\int_{X_4}} \omega' \wedge E_3
  \Big\}
  \;=\;
  \tfrac{4}{3}
  \int_{X^4} \omega \wedge \omega' \wedge B_2
  \mathrlap{\,,}
$$






