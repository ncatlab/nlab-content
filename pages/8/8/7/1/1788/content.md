
$$
  (z_i - z_j  - \theta_i \theta_j)^2
  \;=\;
  (z_i - z_j)^2
  + 
  2(z_i - z_j) \theta_i \theta_j
$$

$$
  \begin{array}{l}
    \textstyle{\int}
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \underset{i \lt j}{\prod}
    ( z_i - z_j  - \theta_i \theta_j )^2
    \\
    \;=\;
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \textstyle{\underset{i \lt j}{\prod}}
    \big(
      ( z_i - z_j)^2
      +
      2( z_i - z_j ) \theta_i\theta_j
    \big)
    \\
    \;=\;
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \textstyle{\underset{i \lt j}{\prod}}
    \Big(
      ( z_i - z_j )^2
      \,
      \exp\big(
        2( z_i - z_j )^{-1} \theta_i \theta_j
      \big)
      \,
    \Big)
    \\
    \;=\;
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      ( z_i - z_j )^2
    \Big)
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      \exp\big(
        2( z_i - z_j )^{-1} \theta_i \theta_j
      \big)
    \Big)
    \\
    \;=\;
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      ( z_i - z_j )^2
    \Big)
    \,
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      \exp\big(
        2( z_i - z_j )^{-1} \theta_i \theta_j
      \big)
    \Big)
    \\
    \;=\;
    vd\big(z_\bullet\big)
    \,
    pf\Big(
      (z_{\bullet_1} - z_{\bullet_2})^{-1}
    \Big)
  \end{array}
$$

(due to [Gromov, Martinec & Ryu 2020 (13)](Laughlin+wavefunction#GromovMartinecRyu20), following [Hasebe 2008](Laughlin+wavefunction#Hasebe08))

\linebreak
\linebreak



## Loop space of the 2-sphere

* [[Frederick R. Cohen]], J. Wu: *On Braid Groups, Free Groups, and the Loop Space of the 2-Sphere*, in: *Categorical Decomposition Techniques in Algebraic Topology*, in *Progress in Mathematics* **215**,  Birkhäuser (2003) 93-105  \[<a href="https://doi.org/10.1007/978-3-0348-7863-0_6">doi:10.1007/978-3-0348-7863-0_6</a>\]
