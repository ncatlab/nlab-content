
\begin{example}
\label{FiniteCyclicGroupsActFreelyOnAddDimensionalSpheres}
**(Finite cyclic groups act freely on odd-dimensional spheres)**
\linebreak
 For every non-[[trivial group|trivial]] [[finite group|finite]] [[cyclic group]] $\mathbb{Z}/n \,\subset\, U(1)$, its left-multiplication action on the [[n-sphere|$2n+1$-sphere]], regarded as the [[unit sphere]] in the [[complex numbers|complex]] $n$-space
i$$
  S^{2n+1} 
    \,\simeq\,
  S\big(\mathbb{R}^{2n+2}\big)
    \,\simeq\,
  S\big(\mathbb{C}^{n+1}\big)
  \,,
$$
is (a [[G-space|continuous group action]] and) [[free action|free]].
\end{example}
This follows verbatim as the (slightly more interesting) Ex. \ref{FiniteADEGroupsActFreelyOnFourNPlusThreeSpheres} below, interchanging the [[complex numbers]] with the [[quaternions]].

\begin{example}
\label{FiniteADEGroupsActFreelyOnFourNPlusThreeSpheres}
**(Finite ADE-groups act freely on $S^{4n+3}$-spheres)**
\linebreak
For every non-[[trivial group|trivial]] [[finite subgroup of SU(2)]] $G \,\subset\, $ [[SU(2)]] $\simeq$ [[Sp(1)]] its [[quaternion|quaternionic]] left-multiplication action on the [[n-sphere|$4n+3$-sphere]], regarded as the [[unit sphere]] in the [[quaternion|quaternionic]] $n$-space
$$
  S^{4n+3} 
    \,\simeq\,
  S\big(\mathbb{R}^{4n+4}\big)
    \,\simeq\,
  S\big(\mathbb{H}^{n+1}\big)
  \,,
$$
is (a [[G-space|continuous group action]] and) [[free action|free]].
\end{example}
\begin{proof}
Here are the elementary and straightforward details:
 
Under the given identification, points in $S^{4n+3}$ correspond to $(n+1)$-[[tuples]] of [[quaternions]] $\vec v \,=\, (v_1, \cdots, v_{n+1})$, $v_i \,\in\, \mathbb{H}$ (i.e. quaternionic [[vectors]]) such that

\[
  \label{UnitNormConditionOnQuaternionicVectors}
  \begin{aligned}
    \left\vert \vec v \right\vert^2
    &
    \;\coloneqq\;
    \vec v^\dagger \cdot \vec v
    \\
    &
    \;\coloneqq\;
    \bar v_1 \cdot v_1  +  \cdots  +  \vec v_{n+1} \cdot v_{n+1} 
    \\
    &
    \;\overset{!}{=}\; 
    1
  \end{aligned}
  \,,
\]

where $\overline{(-)}$ denotes [[quaternionic conjugation]]. 

Since [[Sp(1)]] is the [[subgroup]] of the quaternionic [[group of units]] on the unit-[[norm]] elements

$$
  Sp(1)
  \;\coloneqq\;
  \big\{ 
    q \,\in\, \mathbb{H}^\times
    \,\vert\,
    \bar q \cdot q \,=\, 1
  \big\}
  \;\subset\;
  \mathbb{H}^\times
$$

we have

$$
  \begin{aligned}
    \left\vert
      q \cdot \vec v
    \right\vert
    &
    \;=\;
    (q \cdot \vec v)^\dagger
    \cdot
    (q \cdot \vec v)
    \\
    &
    \;=\;
    \vec v^\dagger 
      \cdot 
    \underset{ = 1}{\underbrace{q^\dagger \cdot q}} 
      \cdot 
    \vec v
    \\
    &
    \;=\;
    \vec v^\dagger \cdot \vec v
    \\
    &
    \;=\;
    \left\vert \vec v\right\vert^2
    \,,
  \end{aligned}
$$

showing that the left multiplication action of $Sp(1)$ on $\mathbb{H}^{n+1}$ does restrict to an action on its unit sphere.
Moreover, since quaternion-multiplication is clearly [[continuous function|continuous]] with respect to the [[Euclidean topology]] on $\mathbb{H} \simeq_{\mathbb{R}} \mathbb{R}^4$, this yields a continuous action on $S^{4n+3}$.

Finally, since $\mathbb{H} \,\ni\, q \,\mapsto\, \bar q \cdot q \,\in\, \mathbb{R}$ is positive definite ($\bar q \cdot q = 0 \,\;\Leftrightarrow\;\, q = 0$ ), at least one of the components $v_i$ of $\vec v$ needs to be non-zero in order for  (eq:UnitNormConditionOnQuaternionicVectors) to hold. But on this component the left action $v_i \,\mapsto\, q \cdot v_i$ is left-multiplication in the [[group of units]] $\mathbb{H}^{\times} \,=\, \mathbb{H} \setminus \{0\}$ and hence is free, as the multiplication action of any group on itself is free.
\end{proof}

Notice that, while an analogous argument shows that with $G \subset Sp(1)$ also the [[direct product group]] $G^{n+1}$ canonically acts on $S^{4n+3}$ by componentwise left multiplication, for $n \geq 2$ this action is no longer free, as the $k$th factor subgroup now fixes the elements whose $k$th component vanishes. In fact, higher direct product powers of cyclic groups in general have *no* free action on spheres of any dimension, see Smith's $p^2$-condition (Prop. \ref{SmithPSquareCondition} below).
