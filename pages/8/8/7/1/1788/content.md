

\begin{example}
**(Riemann-Cartan geometry of $S^3$)**
We discuss the [[Riemannian geometry]] of the [[round sphere|round]] [[3-sphere]] $S^3$ as a [[Cartan geometry]], hence via [[frame field]] and [[spin connection]] with vanishing [[torsion]] tensor. 

Among all spheres, this is particularly easy for the $S^3$, since its [[underlying]] [[smooth manifold]] [[diffeomorphism|is]] that of the [[Lie group]] [[SU(2)|$SU(2)$]]. This means that the [[frame field]]  can be chosen to be globally defined 

$$
  \big(
    e^i
  \big)_{i = 1}
  \,\in\,
  \Omega^1_{dR}\big(
    S^3
    ;\,
    \mathbb{R}^3
  \big)
$$

and to be given by [[left-invariant differential forms]] that satisfy the [[Maurer-Cartan equation]]

$$
  \mathrm{d}
  e^i
  \;=\;
  \epsilon^{i j k }
  \,
  e_j \, e_k
  \,,
$$

where $\epsilon^{i j k}$ is the [[Levi-Civita symbol]] in 3 dimensions, and we use the [[Einstein summation convention]] throughout.

In next defining the "[[spin connection]]" form

$$
  \big(
    \omega^{i j}
    =
    - \omega^{j i}
  \big)_{i,j = 1}^3
  \,\in\,  
  \Omega^1_{dR}\big(S^3;\, \mathfrak{so}(3)\big)
$$

we shall use the convention where the [[torsion]]-[[tensor]] $\big(T^i\big)_{i = 1}^3$ and [[curvature]]-[[tensor]] $\big(R^{i j}\big)_{i,j=1}^3$ are formed with a relative minus sign as

\begin{equation}
  \label{TorsionAndCurvatureInCartanGeometryOfS3}
  \begin{aligned}
    T^i & 
      \coloneqq\; 
        \mathrm{d} \, e^i - \omega^{i j} \, e_j
    \,,
    \\
    R^{i j} & 
      \coloneqq\; 
        \mathrm{d}\, \omega^{i j} 
          - \omega^{i k}\, \omega_k{}^j
    \,.
  \end{aligned}
\end{equation}

This implies that the unique [[torsion]]-free [[spin connection]] is given by

$$
  \omega^{i j}
  \;\equiv\;
  -
  \epsilon^{i j k} 
  e_k
  \,,
$$

since, by the above:

$$
  \begin{array}{l}
    \mathrm{d}
    e^i
    -
    \omega^{i j} e_j
    \\
    \;=\;
    \epsilon^{i j k }
    e_j e_k
    +
    \epsilon^{i j k} 
    e_k\, e_j
    \\
    \;=\;
    0
    \,.
  \end{array}
$$

To find the [[curvature]] of this connection we compute

$$
  \begin{array}{l}
    \mathrm{d} 
    \omega^{i j}
    \\
    \;=\;
    -
    \epsilon^{i j k}
    \epsilon_{k l m} e^l \, e^m
    \\
    \;=\;
    -2 \delta^{ i j }_{l m}
    e^{l}\, e^m
    \\
    \;=\;
    -2 e^{i}\, e^{j}
    \,,
  \end{array}
$$

where we take the multi-[[Kronecker symbol]] is normalized as

$$
  \delta^{i j}_{k l}
  \;\coloneqq\;
  \delta^{[i j]}_{[k l]}
  \;=\;
  \delta^{[i j]}_{k l}
  \;=\;
  \tfrac{1}{2}
  \Big(
    \delta^i_k\, \delta^j_l
    -
    \delta^j_k\, \delta^i_l
  \Big)
  \,,
$$

and

$$
  \begin{array}{l}
    \omega^{i k} \, \omega_{k}{}^j
    \\
    \;=\;
    \epsilon^{i k l}
    \epsilon_{k j m}
    e_l
    \, e^m
    \\
    \;=\;
    -2\delta^{i l}_{j m}
    e_l \, e^m
    \\
    \;=\;
    -
    e^i \, e^j
  \end{array}
$$

to obtain:

$$
  \begin{array}{l}
    R^{i j}
    \\
    \;=\;
    \mathrm{d}\omega^{i j} - \omega^{i k}\, \omega_k{}^j
    \\
    \;=\;
    -2 e^{i}\, e^{j}
    +
    e^i \, e^j
    \\
    \;=\;
    - e^{i}\, e^{j}
    \,,
  \end{array}
$$

hence

$$
  R^{i j}{}_{k l}
  \;=\;
  - \delta^{i j}_{k l}
  \,.
$$

Notice that, therefore, with the conventions (eq:TorsionAndCurvatureInCartanGeometryOfS3) the [[scalar curvature]] $\mathrm{R}$ of the $S^3$ comes out with a *negative* sign, since the [[Ricci tensor]] of $S^3$ is
$$
  Ric_{i j}
  \;\equiv\;
  R^{i k}{}_{j k}
  \;=\;
  - \delta_{i j}
$$
so that
$$
  \mathrm{R}
  \;\equiv\;
  Ric^i{}_i
  \;=\;
  - 3
  \,.
$$

This may seem undesirable, but it is a common choice in practice (cf. e.g. [Freund & Rubin 1980, below (4b)](Freund-Rubin+compactification#FreundRubin80)).
\end{example}
