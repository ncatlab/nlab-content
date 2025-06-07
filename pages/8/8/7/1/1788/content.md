

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

****

Consider:

* $\mathbb{H}$ the [[real numbers|real]] [[star-algebra]] of [[quaternions]], with [[norm]] given by ${\vert q \vert}^2 \coloneqq q q^\ast$,

* $\mathbb{H}_{im} \subset \mathbb{H}$ the subspace of [[imaginary number|imaginary]] quaternions ($q \in \mathbb{H}$ such that $\overline{q} = - q$), in which we choose, as usual, an [[orthonormal basis|orthonormal]] [[linear basis]] $\mathbf{i}, \mathbf{j}, \mathbf{k}$,

* $\mathbb{H} \longrightarrow End(\mathbb{C}^2)$ the [[star-algebra]] [[homomorphism]] which identifies the unit imaginary quaternions with [[Pauli matrices]]

  $$
    \array{
      \mathbb{H} 
        &\overset
         {\phantom{--} \sigma \phantom{--}}
         {\longrightarrow}& 
      End(\mathbb{C}^2)
      \\
      1 &\mapsto& 
       \left[\begin{matrix}
          1 & 0 
          \\ 
          0 & 1
        \end{matrix}\right]
      \\   
      \mathbf{i} &\mapsto& 
       \mathrm{i}
       \left[\begin{matrix}
          0 & 1 
          \\ 
          1 & 0
        \end{matrix}\right]
      \\   
       \mathbf{j} &\mapsto& 
       \mathrm{i}
       \left[\begin{matrix}
          0 & \mathrm{i} 
          \\ 
          -\mathrm{i} & 0
        \end{matrix}\right]
      \\   
       \mathbf{k} &\mapsto& 
       \mathrm{i}
       \left[\begin{matrix}
          1 & 0 
          \\ 
          0 & -1
        \end{matrix}\right]
    }
  $$

* $S(\mathbb{H})$ the [[3-sphere]] of unit norm quaternions, which by the above homomorphism is identified with the [[special unitary group|special unitary]] [[matrices]], 

  $$
    S(\mathbb{H}) 
      \underoverset
        {\sim}
        {\phantom{--} \sigma \phantom{--}}
        {\longrightarrow}
    SU(2)
  $$

  because

  $$
    \begin{array}{l}
      det\big( 
        x_0 \mathrm{id} 
        + 
        x_1 \sigma_{\mathbf{i}}
        + 
        x_2 \sigma_{\mathbf{j}}
        + 
        x_3 \sigma_{\mathbf{k}}
     \big)
     \\
     \;=\;
     det
     \left[
       \begin{matrix}
          x_0  + \mathrm{i} x_3 & \mathrm{i}x_1 - x_2
          \\
          \mathrm{i} x_1 + x_2 & x_0 - \mathrm{i} x_3
       \end{matrix}
     \right]
     \\
     \;=\;
     (x_0)^2 + (x_1)^2 + (x_2)^2 + (x_3)^2
    \end{array}
  $$

  and
  
  $$
    \begin{array}{l}
    \big(
      x_0 \mathrm{id}
      + 
      x_1 \sigma_{\mathbf{i}}
      + 
      x_2 \sigma_{\mathbf{j}}
      + 
      x_3 \sigma_{\mathbf{k}}
    \big)^\dagger
    \big(
      x_0 \mathrm{id}
      + 
      x_1 \sigma_{\mathbf{i}}
      + 
      x_2 \sigma_{\mathbf{j}}
      + 
      x_3 \sigma_{\mathbf{k}}
    \big)
    \\
    \;=\;
    \big(
      x_0 \mathrm{id}
      - 
      x_1 \sigma_{\mathbf{i}}
      - 
      x_2 \sigma_{\mathbf{j}}
      - 
      x_3 \sigma_{\mathbf{k}}
    \big)
    \big(
      x_0 \mathrm{id}
      + 
      x_1 \sigma_{\mathbf{i}}
      + 
      x_2 \sigma_{\mathbf{j}}
      + 
      x_3 \sigma_{\mathbf{k}}
    \big)
    \\
    \;=\;
    (x_0)^2 
    + (x_1)^2
    + (x_2)^2
    + (x_3)^2
    \end{array}
  $$

* the [[group action]] of $SU(2) \simeq Spin(3)$ through [[SO(3)]] on $\mathbb{H}_{im} \simeq_{{}_{\mathbb{R}}} \mathbb{R}^3$ given by

  $$
    \begin{array}{rcl}
      \overset{
        Spin(3) \times \mathbb{R}^3
      }{
        \overbrace{
          S(\mathbb{H}) \times \mathbb{H}_{im} 
        }
      }
        &\longrightarrow& 
      \overset{
        \mathbb{R}^3
      }{
        \overbrace{
          \mathbb{H}_{im}
        }
      }
      \\
      (q, x) &\mapsto& q x q^\ast
      \mathrlap{\,,}
    \end{array}
  $$

* $S(\mathbb{H}_{im})$ the [[2-sphere]] of unit-[[norm]] imaginary quaternions.

Observing that the [[complex Hopf fibration]] is equivalently (see [there](Hopf+fibration#RealizationViaQuaternions)):
$$
  \begin{array}{c}
    S(\mathbb{H}) 
      &\overset
        {\phantom{--} h_{\mathbb{C} \phantom{--}} }
        {\longrightarrow}
      & 
    S(\mathbb{H}_{im})
    \\
    q &\mapsto& q \cdot \mathbf{i} \cdot \overline{q}
  \end{array}
$$ 
whose [[fiber]] over $\mathbf{i}$ is 
$$
  \begin{array}{rcl}
    \overset{
      \mathrm{U}(1)
    }{
      \overbrace{
        S(\mathbb{C})
      }
    }
    &\xhookrightarrow{\phantom{---}}& 
    \overset{
      \mathrm{SU}(2)
    }{
      \overbrace{
        S(\mathbb{H})
      }
    }
    \\
    x + y \mathrm{i}
    &\mapsto&
    x + y \mathbf{i}
    \,,
  \end{array}
$$
it follows that the [[basic complex line bundle on the 2-sphere]] is the [[associated bundle|associated]] [[complex line bundle]]
$$
  S(\mathbb{H}) \times_{\mathrm{U}(1)} \mathbb{C}
  \;=\;
  \Big\{
    (q,z) \in S(\mathbb{H}) \times \mathrm{U}(1)
  \Big\}_{
    \big/\big( 
      (q,z) \sim (q \alpha^{-1}, \alpha z)
      \,\forall_{\alpha \in \mathrm{U}(1)}\,
    \big)
  }
  \,.
$$

As such, this is a [[subbundle]] of the [[trivial]] [[complex vector bundle]] of [[rank of a vector bundle|rank]]$=2$, via the map:
\begin{tikzcd}[
  sep=0pt
]
  {[q,z]}
  &\mapsto&
  \left(
    q \mathbf{i} \overline{q}
    ,\,
    \sigma_{q}  
    \cdot 
    \left[\begin{matrix} z \\ 0 \end{matrix}\right]
  \right)
  \\
  S(\mathbb{H})
  \times_{\mathrm{U}(1)}
  \mathbb{C}
  \ar[d]
  \ar[rr, hook]
  &&
  S^2 \times \mathbb{C}^2
  \ar[d]
  \\[+15pt]
  S(\mathbb{H}_{\mathrm{im}})
  \ar[rr, equals]
  &&
  S^2
\end{tikzcd}
This subbundle is evidently characterized as the bundle of +1 [[eigenspaces]] of this $S^2$-parameterized linear operator:
$$
  \begin{array}{rrcl}
    S(\mathbb{H})
      &\overset{\phantom{--} \sigma \phantom{--}}{\longrightarrow}&
    End(\mathbb{C}^2)
    \\
    q \mathbf{i} q^\ast
    &\mapsto&
    \sigma_{
      q \mathbf{i} q^\ast
    }    
  \end{array}
  \;\;\;\;\;\;\;
  \text{equivalently}
  \;\;\;\;\;\;\;
  \begin{array}{rrcl}
    S^2
      &\overset{\phantom{--} H \phantom{--}}{\longrightarrow}&
    End(\mathbb{C}^2)
    \\
    \vec x \equiv (x^1, x^2, x^3)
    &\mapsto&
    x^1 \sigma_{\mathbf{i}}
    +
    x^2 \sigma_{\mathbf{j}}
    +
    x^3 \sigma_{\mathbf{k}}
    \,.
  \end{array}
$$
hence equivalently as the [[kernel]]-bundle of the $S^2$-parameterized operator
$$
  H_{\vec x} - \mathrm{id}
  \;=\;
  x^1 \sigma_{\mathbf{i}}
  +
  x^2 \sigma_{\mathbf{j}}
  +
  x^3 \sigma_{\mathbf{k}}
  -
  \mathrm{id}
$$
$$
  BasicLineBundle
  \;\simeq\;
  ker\big(H_{\bullet} - \mathrm{id}\big)
  \,.
$$






****


