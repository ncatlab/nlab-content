
$\rightrightarrows$

$\Vert$






We discuss the unitarization of the [standard representation](representation+theory+of+the+symmetric+group#StandardRepresentation) of the [[symmetric group]] $Sym_3$.

For definiteness of computation, when [[group averaging]] we will be cycling through the elements of $Sym_3$ in this order:

$$
  Sym_3 
  \;=\;
  \left\{
    \begin{array}{l}
    (1 2 3)
    ,\,\\
    (1 3 2)
    ,\,\\
    (2 1 3)
    ,\,\\
    (2 3 1)
    ,\,\\
    (3 1 2)
    ,\,\\
    (3 2 1)
    \end{array}
  \right\}
$$

Let $\big\{e_1, e_2, e_3\big\}$ be the canonical [[linear basis]] of the *defining* representation, with [[group action]] given by

$$
  \sigma \cdot e_i \;\coloneqq\; e_{\sigma(i)}
  \,.
$$

Then a linear basis for the standard representation is 

$\left[\begin{array}{c}1 \\ 0\end{array}\right] \coloneqq e_1 - e_3$

$\left[\begin{array}{c}0 \\ 1\end{array}\right] \coloneqq e_2 - e_3$

The [[group averaging|group-averaged]] inner product of these basis elements is:

$$
  \left\langle
    \left[
      \begin{array}{c}
        1 \\ 0
      \end{array}
    \right]
    ,\,
    \left[
      \begin{array}{c}
        0 \\ 1
      \end{array}
    \right]
  \right\rangle
  \;=\;
  \left(
  \begin{array}{l}
  \left[
    \begin{array}{c}
      1 
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0 
      \\
      1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      1 
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0 
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      0
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1 
      \\
      0
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      0
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      0
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      1
    \end{array}
  \right]
  \end{array}
  \right)/6
  \;=\;
  4/6
  \;=\;
  2/3
$$



$$
  \left\langle
    \left[
      \begin{array}{c}
        0 \\ 1
      \end{array}
    \right]
    ,\,
    \left[
      \begin{array}{c}
        0 \\ 1
      \end{array}
    \right]
  \right\rangle
  \;=\;
  \left(
  \begin{array}{l}
  \left[
    \begin{array}{c}
      0 
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0 
      \\
      1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      0 
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0 
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      1
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1 
      \\
      0
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      0
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      1
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      1
    \end{array}
  \right]
  \end{array}
  \right)/6
  \;=\;
  8/6
  \;=\;
  4/3
$$


$$
  \left\langle
    \left[
      \begin{array}{c}
        1 \\ 0
      \end{array}
    \right]
    ,\,
    \left[
      \begin{array}{c}
        1 \\ 0
      \end{array}
    \right]
  \right\rangle
  \;=\;
  \left(
  \begin{array}{l}
  \left[
    \begin{array}{c}
      1 
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1 
      \\
      0
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      1 
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      1 
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      0
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0 
      \\
      1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      0
      \\
      -1
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      0
      \\
      -1
    \end{array}
  \right]
  +
  \left[
    \begin{array}{c}
      -1
      \\
      0
    \end{array}
  \right]
  \cdot
  \left[
    \begin{array}{c}
      -1 
      \\
      0
    \end{array}
  \right]
  \end{array}
  \right)/6
  \;=\;
  8/6
  \;=\;
  4/3
$$


\linebreak

orthonormal basis

$$
  {\vert 0 \rangle}
  \;\coloneqq\;
  \tfrac{1}{4}
  \left[
  \begin{array}{c}
    1
    \\
    1
  \end{array}
  \right]
  \,,
  \;\;
  {\vert 1 \rangle}
  \;\coloneqq\;
  \tfrac{3}{8}
  \left[
  \begin{array}{c}
    1
    \\
    -1
  \end{array}
  \right]
$$


$$
  (132) 
  {\vert 0 \rangle}
  \;=\;
  (132)
  \tfrac{1}{4}
  \left[
  \begin{array}{c}
    1
    \\
    1
  \end{array}
  \right]
  \;=\;
  \tfrac{1}{4}
  \left[
  \begin{array}{c}
    1
    \\
    -2
  \end{array}
  \right]  
  \;=\;
  -\tfrac{1}{2} {\vert 0 \rangle}
  +
  {\vert 1 \rangle}
$$

$$
  (132) {\vert 1 \rangle}
  \;=\;
  (132)
  \tfrac{3}{8}
  \left[
  \begin{array}{c}
    1
    \\
    -1
  \end{array}
  \right]
  \;=\;
  \tfrac{3}{8}
  \left[
  \begin{array}{c}
    1
    \\
    0
  \end{array}
  \right]  
$$


\linebreak

\linebreak



## Idea

In [[quantum information theory]] and [[quantum computing]], by the *T-gate* and the *S-gate* one refers to the [[quantum gates]] acting on single [[qbits]], which in the defining measurement-[[linear basis|basis]] $\big\{ {\vert 0 \rangle}, {\vert 1 \rangle} \big\}$ are given by the [[matrices]]

$$
  T 
  \;=\;
  \left[
    \begin{array}{cc}
      1 & 0
      \\
      0 & e^{\pi \mathrm{i}/4}
    \end{array}
  \right]
$$

and


$$
  S 
  \;=\; 
  T^2
  \;=\;
  \left[
    \begin{array}{cc}
      1 & 0
      \\
      0 & \mathrm{i}
    \end{array}
  \right]
  \mathrlap{\,,}
$$

respectively.







## Defect anyons

* [[Maissam Barkeshli]], Chao-Ming Jian, [[Xiao-Liang Qi]]: *Twist defects and projective non-Abelian braiding statistics*, Phys. Rev. B **87** (2013) 045130 &lbrack;[doi:10.1103/PhysRevB.87.045130](https://doi.org/10.1103/PhysRevB.87.045130), [arXiv:1208.4834](https://arxiv.org/abs/1208.4834)&rbrack;





## Controlling anyons

* G. Rosenberg, B. Seradjeh, C. Weeks, M. Franz: *Creation and manipulation of anyons in a layered superconductor-2DEG system*, Phys. Rev. B **79** 205102 (2009) \[<a href="https://doi.org/10.1103/PhysRevB.79.205102">doi:10.1103/PhysRevB.79.205102</a>, [arXiv:0812.3140](https://arxiv.org/abs/0812.3140)\]

* Gábor B. Halász: *Gate-Controlled Anyon Generation and Detection in Kitaev Spin Liquids*, Phys. Rev. Lett. **132** 206501 (2024) \[<a href="https://doi.org/10.1103/PhysRevLett.132.206501">doi:10.1103/PhysRevLett.132.206501</a>\]



## Loop space of the 2-sphere

On the [[loop space]] $\Omega S^2$ of the 2-sphere

in relation to [[braid groups]]

* [[Frederick R. Cohen]], J. Wu: *On Braid Groups, Free Groups, and the Loop Space of the 2-Sphere*, in: *Categorical Decomposition Techniques in Algebraic Topology*, in *Progress in Mathematics* **215**,  Birkhäuser (2003) 93-105  \[<a href="https://doi.org/10.1007/978-3-0348-7863-0_6">doi:10.1007/978-3-0348-7863-0_6</a>\]

On $\Omega S^2 \,\simeq\, B \Omega^2 S^2$ regarded as a [[classifying space]] (for "$\mathbf{l}$ine" bundles):

* [[Jack Morava]]: *A homotopy-theoretic context for CKM/Birkhoff renormalization* &lbrack;[arXiv:2307.10148](https://arxiv.org/abs/2307.10148), [spire:2678618](https://inspirehep.net/literature/2678618)&rbrack;

* [[Jack Morava]]: *Some very low-dimensional algebraic topology* &lbrack;[arXiv:2411.15885](https://arxiv.org/abs/2411.15885)&rbrack;





[[test page]]