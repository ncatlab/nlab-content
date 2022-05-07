## Idea

## Definition

A [[module]] $M$ over a [[commutative ring]] $R$
is __dualizable__ if it is a [[dualizable object]]
in the [[symmetric monoidal category]] of $R$-[[modules]]
equipped with the [[tensor product]] over $R$.

Since this [[symmetric monoidal category]]
is a [[closed monoidal category]],
the [[dual object]] to $M$
is necessarily $Hom_R(M,R)$.

Furthermore, the abstract [[evaluation map]]
$$Hom_R(M,R)\otimes_R M\to R$$
must coincide with the map induced by the [[bilinear map]]
$$Hom_R(M,R)\times_R M\to R$$
that sends $(f,m)$ to $f(m)$.

## Characterization

\begin{theorem}
An $R$-module is dualizable if and only if
it is a [[finitely generated]] [[projective module]].
\end{theorem}

\begin{proof}
First, [[dualizable objects]] are closed under [[retracts]]
and finite [[direct sums]].
Any [[finitely generated]] [[projective module]]
is a [[retract]] of $R^n$ for some $n\ge0$,
so to show that
[[finitely generated]] [[projective modules]] are [[dualizable]],
it suffices to observe that $R$ is dualizable as an $R$-[[module]].

Conversely, we show that [[dualizable objects]] are [[finitely generated]]
[[projective modules]].
Unfolding the definition of a [[dualizable object]],
an $R$-[[module]] $M$ is dualizable
if the coevaluation map
$$coev: R \to M\otimes Hom_R(M,R)$$
and the evaluation map
$$ev: Hom_R(M,R)\otimes M\to R$$
satisfy the [[triangle identities]]:
$$(id_M \otimes ev)\circ (coev\otimes id_M) = id_M,$$
$$(ev \otimes id_{Hom(M,R)})\circ (id_{Hom(M,R)}\otimes coev) = id_{Hom(M,R)}.$$

The coevaluation map sends $1\in R$ to a _finite_ sum
$$\sum_{i\in I} m_i\otimes f_i.$$
The [[triangle identities]] now read
$$\sum_{i\in I} m_i f_i(p) = p,\qquad p\in M$$
$$\sum_{i\in I} r(m_i) f_i = r, \qquad r\in Hom_R(M,R).$$
The first identity implies that $m_i$ ($i\in I$) generate $M$ as an $R$-module,
i.e., $M$ is [[finitely generated]].

Consider the map $a: R^I\to M$ that sends $(r_i)_{i\in I}$
to $\sum_{i\in I} m_i r_i$.
Consider also the map $b: M\to R^I$ that sends $p\in M$
to $(f_i(p))_{i\in I}\in R^I$.
The first triangle identity now reads $b a = id_M$.
Thus, $M$ is a retract of $R^I$, i.e., $M$ is a [[projective module]].
\end{proof}

## Geometric interpretation

See also [[Serre–Swan theorem]] and [[smooth Serre–Swan theorem]].

\begin{theorem}
(Serre, 1955.)
The [[category]] of dualizable modules over a [[commutative ring]] $R$
is equivalent to the [[category]] of [[algebraic vector bundles]]
(defined as [[locally free sheaves]] over the [[structure sheaf of rings]])
over the [[Zariski spectrum]] of $R$.
\end{theorem}

\begin{theorem}
(Swan, 1962.)
Given a [[compact Hausdorff space]] $X$,
the [[category]] of dualizable modules over the real [[algebra]]
of [[continuous maps]] $X\to\mathbf{R}$
is equivalent to the category of finite-dimensional continuous [[vector bundles]] over $X$.
\end{theorem}

\begin{theorem}
(See, e.g., Nestruev 2003, 11.33.)
Given a [[smooth manifold]] $X$,
the [[category]] of dualizable modules over the real [[algebra]]
of [[smooth maps]] $X\to\mathbf{R}$
is equivalent to the category of finite-dimensional smooth [[vector bundles]] over $X$.
\end{theorem}

## Related concepts

* [[dualizable object]]

* [[perfect chain complex]]

* [[perfect module]]

* [[Serre–Swan theorem]]

* [[smooth Serre–Swan theorem]]

* [[duality between geometry and algebra]]

[[!redirects dualizable modules]]