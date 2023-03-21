#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The recognition principle for finite relative loop spaces states that, for $1 \leq N \lt \infty$, a pair of pointed toplological spaces is of the homotopy type of a relative $N$-loop space pair of some $(N-1)$-connected topological pair if and only if it is a grouplike algebra over the Swiss-Cheese relative operad $\mathcal{SC}_N$.

The recognition principle for infinite relative loop spaces states that a pair of pointed toplological spaces is of the homotopy type of a relative $\infty$-loop space pair of some 1-shifted morphism of connective spectra if and only if it is a grouplike algebra over $\mathcal{SC}_\infty$.


## Idempotent weak Quillen quasiadjunctions

## Finite relative recognition theorem

Let $1\leq N\leq \infty$ and $\mathcal{SC}_N$ be the cubical Swiss Cheese relative operad, a colored operad over the colors $\{c, o\}$, respectively referred to as the closed and open colors. It induces a monad $SC_N$ on the category $Top_*^2$ of pairs of pointed topological spaces. Denote by $\mathcal{SC}_N[Top]$ the category of algebras over $SC_N$, which we equip with the mixed model structure induced by the one on $Top_*^2$. We denote pairs of pointed spaces as $X=(X_{c},X_{o})$.

Denote by $Top_*^\rightarrow$ the category of pointed maps, equipped with the mixed projective model structure. We denote maps as $Y=(Y:Y_d\rightarrow Y_c)$.

\begin{definition}
For $1 \leq N \lt \infty$ the relative $N$-loop space functor is
$$
  \Omega^N_2:Top_*^{\rightarrow}\rightarrow Top_*^2,\qquad \Omega^N_2(Y):=(Y_c^{\mathbb{S}^N},(Y_o\times_{Y_c} Y_c^I)^{\mathbb{S}^{N-1}}).
$$

The $N$-suspension functor is
$$
\Sigma^N_\to : Top_*^2\to Top_*^\to, \qquad
\Sigma^N_\to(X)=
(X_{o} \wedge \mathbb{S}^{N-1} \to ((X_o \wedge I) \vee(X_c \wedge \mathbb{S}^1)) \wedge \mathbb{S}^{N-1} ).
$$
\end{definition}


## Infinite relative loop spaces

## Statement 