
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


\tableofcontents


## Idea
A __stochastic process__ describes a [[dynamical system]] evolving over a [[linearly ordered set]] $T$ ("[[time]]"), typically taken to be the ([[positive number|positive]])
[[integers]] or  [[real numbers]], whose dynamical [[laws of motion]] are [[morphisms]] in the [[Kleisli category]] of the [[Giry monad]] (or any other [[probability monad]]). By working in the larger [[category]] of [[algebra over a monad|algebras of that monad]], a characterization  of a stochastic processes can be modeled in terms of the [[expectation value|expected value]] of [[measurements]] on that process. 

By a __random process__ physicists usually mean the same, but mathematicians sometimes allow random processes indexed by more general sets, not usually with meaning of time or equipped with a [[linear order]]. 

The most studied examples include *[[Brownian motion]]*, *[[Ornstein-Uhlenbeck processes]]* and *[[Lévy processes]]*. The most elementary stochastic process (to define) is an  __indivisible stochastic process__ which [Barandes 2025](#Barendes25)  has used to give an [[indivisible stochastic process interpretation of quantum mechanics]].


## Definitions

We define discrete time stochastic processes following [Lawvere 1962](#Lawvere62).  Let $N$ be the [[category]] with [[countable set|countably many]] [[objects]], $\{0,1,2,...\}$, and no non-[[identity morphisms]], and let $\mathbf{Meas}_G$ denote the [[Kleisli category]] of the [[Giry monad]].  Let $\mathbf{Meas}_G^{N}$ denote the category whose objects $\mathbf{\Omega}$ are [[sequences]] $\Omega_0, \Omega_1,\ldots$ of objects in $\mathbf{Meas}_G$ which are [[measurable spaces]].  We define an [[endofunctor]] $\mathbf{Meas}_G^{N} \xrightarrow{\mathbf{\Phi}} \mathbf{Meas}_G^{N}$ by 
$
\mathbf{\Phi}(\mathbf{\Omega})= \{ \prod_{k \lt n} \Omega_k \}_{k \in N}  
$
where $\prod_{k \lt n} \Omega_k$ denotes the [[Cartesian product|product]] measurable space with the smallest [[sigma-algebra|$\sigma$-algebra]] such that all the [[coordinate]]-[[projection]] functions are [[measurable function|measurable]].  If $\Omega_n$ is thought of as the space of all possible states of a system at time $n$, then $\mathbf{\Phi}(\mathbf{\Omega})_n=\prod_{k \lt n}\Omega_k$ is the space of all possible histories of the system before time $n$.

We define a __discrete time stochastic process__ $\mathbf{Q}$ to be a [[natural transformation]]
\begin{equation} 
\mathbf{\Phi} \xrightarrow{\mathbf{Q}} \mathbf{id}
\end{equation}
where $\mathbf{id}$ is the [[identity functor]] on $\mathbf{Meas}_G^N$.  Given any two (discrete time) stochastic processes $\mathbf{Q}$ and $\mathbf{Q}'$  we define a [[sequence]] of [[morphisms]] in $\mathbf{Meas}_G$, $\Omega_n \xrightarrow{f_n} \Omega_n^{'}$ to be a morphism from $\mathbf{Q}$ to $\mathbf{Q}'$ when, for each $n \in N$, the $\mathbf{\Meas}_G$-[[diagram]]

\begin{tikzpicture}
  \node  (POn) at (0,0)  {$( \mathbf{\Phi}(\mathbf{\Omega}))_n$};
   \node  (POpn) at (3,0)  {$( \mathbf{\Phi}(\mathbf{\Omega}'))_n$};
   \node (On) at (0,-1.5)  {$\Omega_n$};
   \node (Opn) at (3, -1.5) {$\Omega^{'}_n$};
   \draw[->,above] (POn) to node {$\Phi(f_n)$} (POpn);
   \draw[->,below] (On) to node {$f_n$} (Opn);
   \draw[->,left] (POn) to node {$Q_n$} (On);
   \draw[->,right] (POpn) to node {$Q'_n$} (Opn);
\end{tikzpicture}

[[commuting diagram|commutes]]. Since there is an obvious notion of [[composition]] for such [[maps]], all stochastic processes and all such maps of such determine the *category of discrete time stochastic processes* $\mathbf{dStoch}$.  (Warning: Some authors have used the notation $\mathbf{Stoch}$ ([[Stoch]]) to mean the [[Kleisli category]] of the [[Giry monad]], traditionally denoted by $\mathbf{Meas}_G$ or $\mathcal{K}(G)$, which can also be interpreted (for modeling) as the category of [[Markov process|Markov stochastic processes]].)

In the preceding diagram the morphisms $Q_n$, which are [[Kleisli morphisms]]
$
\prod_{k \lt n} \Omega_k \xrightarrow{Q_n} \Omega_n
$
are called  __dynamic laws__ (of motion), and stochastic processes are classified by properties of the dynamic laws.

A __Markov dynamic law__ $Q_n$ is a dynamic law depending only on the current state, i.e., $Q_n$ factors as
\begin{tikzpicture}
  \node  (POn) at  (0,0)  {$\prod_{k < n} \Omega_k$};
  \node  (On)  at  (6,0)  {$\Omega_n$};
  \node  (On1) at  (3,-1.5)  {$\Omega_{n-1}$};
  \draw[->,above] (POn) to node {$Q_n$} (On);
  \draw[->,left]  (POn) to node {$\pi_{n-1}$} (On1);
  \draw[->,right] (On1) to node [xshift=3pt,yshift=-3pt]{$\tilde{Q}_n$} (On); 
\end{tikzpicture}
where $\pi_{n-1}$ is the canonical [[coordinate]] [[projection]] ([[measurable function|measurable]]) [[function]] which specifies the deterministic [[Kleisli morphism]] (with the same notation).  Thus a [[Markov process|Markov dynamic law]] only depends upon the current state and not its history.

If $\mathbf{Q}$ is a stochastic process such that the dynamic law at every stage is a [[Markov process|Markov dynamic law]] we say the stochastic process $\mathbf{Q}$ is a __[[Markov process|Markov stochastic process]]__.  In  the special case where $\mathbf{\Omega}$ defines a constant sequence, $\Omega_n = \Omega$ for all $n$,   then a Markov stochastic process on $\mathbf{\Omega}$ is called a *[[Markov chain]]*.

An even more elementary way of defining a stochastic process is by taking $\Omega_n = \Omega$, so each $\Omega_n$ is a copy of $\Omega$, and for all $n$ defining the dynamic law $Q_n$ such that it factorizes as a composite of the projection map $\pi_0$ and a [[Kleisli morphism]] $\tilde{Q}_n$, 
\begin{tikzpicture}
  \node  (POn) at  (0,0)  {$\prod_{k < n} \Omega_k$};
  \node  (On)  at  (6,0)  {$\Omega_n$};
  \node  (On1) at  (3,-1.5)  {$\Omega_{0}$};
  \draw[->,above] (POn) to node {$Q_n$} (On);
  \draw[->,left]  (POn) to node {$\pi_0$} (On1);
  \draw[->,right] (On1) to node [xshift=3pt,yshift=-3pt]{$\tilde{Q}_n$} (On); 
\end{tikzpicture}
For such dynamic laws the time at stage $0$ is thought of as the conditioning event time - subsequent stages are ''conditioned on $\Omega_0$''.

We say a stochastic process $\mathbf{Q}$ is __divisible__ if and only if for all stages $m$ and $n$, with $m \le n$ there exists a [[Kleisli morphism]] $\tilde{Q}_{m,n}$ such that the triangle on the right hand side of the Kleisli-diagram
\begin{tikzpicture}
  \node  (POm) at  (0,0)  {$\prod_{k < m} \Omega_k$};
  \node  (Om)  at  (6,0)  {$\Omega_m$};
  \node  (Om1) at  (3,-1.5)  {$\Omega_{0}$};
  \draw[->,above] (POm) to node {$Q_m$} (Om);
  \draw[->,left]  (POm) to node {$\pi_{0}$} (Om1);
  \draw[->,right] (Om1) to node [xshift=3pt,yshift=-3pt]{$\tilde{Q}_m$} (Om); 

  \node  (Pon) at (0, -3)  {$\prod_{k < n} \Omega_k$};
  \node  (On)  at (6, -3)  {$\Omega_n$}; 
  \draw[->, below] (Pon) to node {$Q_n$} (On);
  \draw[->, above] (Pon) to node {$\pi_0$} (Om1);
  \draw[->, right] (Om1) to node {$\tilde{Q}_n$} (On);

  \draw[->, right, dashed] (Om) to node {$\tilde{Q}_{m,n}$} (On);
\end{tikzpicture}
commutes, i.e., $\tilde{Q}_n = \tilde{Q}_{m,n} \circ \tilde{Q}_m$. (We have abused notation by using the notation $\pi_0$ to denote the two projection maps onto the $0^{th}$ coordinate despite the domains being distinct when $m \lt n$.)

An __indivisible stochastic process__ is a stochastic process which is not divisible.  Such processes are employed in the [[indivisible stochastic process interpretation of quantum mechanics]].

An indivisible [[stochastic process]] is a very general type of [[stochastic process]] which can exhibit wild behavior because, for any $\epsilon \gt 0$, the two dynamics laws $\Gamma_t$ and $\Gamma_{t+\epsilon}$ need not have any relationship between them.  For example, even if $\Omega$ was a [[standard Borel space]] and for every $U \in \Sigma_{\Omega}$ all the measurable functions $\Omega_0 \xrightarrow{\Gamma_t(U | \bullet)} [0,1]$ and $\Omega_0 \xrightarrow{\Gamma_{t+\epsilon}(U | \bullet)} [0,1]$ were  continuous functions the two probability measures obtained by composition with an initial probability measure on $\Omega_0$, $\mathbf{1} \xrightarrow{P_0} \Omega_0 \xrightarrow{\Gamma_t} \Omega_t$ and $\mathbf{1} \xrightarrow{P_0} \Omega_0 \xrightarrow{\Gamma_{t+\epsilon}} \Omega_{t+\epsilon}$, can vary significantly.  Such a process is in stark contrast to a [[Markov process]] on a [[standard Borel space]] where continuous [[Markov kernels]] yield a continuously varying probability measure on the [[measurable space]] $\Omega$. 

## Examples

\begin{example}
 A 3-stage Markov [[stochastic process]] $\mathbf{Q}$ with  measurements $\Omega_i \xrightarrow{f_i} \mathbb{R}$, modeled within the category of algebras of the [[Giry monad]] $(G, \eta, \mu)$ so that the process $\mathbf{Q}$ can be characterized in terms of the expected values of the measurements, is given by

\begin{tikzpicture}
 \node (one) at  (0,0)  {$\mathbf{1}$};
 \node (GO0) at  (3,0) {$G(\Omega_0)$};
 \node (G2O1) at  (6,0)  {$G^2(\Omega_1)$};
 \node (GO1) at   (9,0) {$G(\Omega_1)$};
 \node (G2O2) at   (12,0)  {$G^2(\Omega_2)$};
 \node (GO2)  at   (15,0) {$G(\Omega_2)$};

 \draw[->,above] (one) to node {$Q_0$} (GO0);
 \draw[->,above] (GO0) to node {$G(Q_1)$} (G2O1);
 \draw[->,above] (G2O1) to node {$\mu_{\Omega_1}$} (GO1);
 \draw[->,above] (GO1) to node {$G(Q_2)$} (G2O2);
 \draw[->,above] (G2O2) to node {$\mu_{\Omega_2}$} (GO2);

  \node (GR0) at (9,-1.5) {$G(\mathbb{R}_{\infty})$};
  \node (R0)  at (9, -3)  {$\mathbb{R}_{\infty}$};
  \draw[->,left] (GO1) to node {$G(f_1)$} (GR0);
  \draw[->>,left] (GR0) to node {$\mathbb{E}_{\bullet}(id_{\mathbb{R}_{\infty}})$} (R0);

  \node (GR) at (15,-1.5) {$G(\mathbb{R}_{\infty})$};
  \node (R)  at (15, -3)  {$\mathbb{R}_{\infty}$};
  \draw[->,left] (GO2) to node {$G(f_2)$} (GR);
  \draw[->>,left] (GR) to node {$\mathbb{E}_{\bullet}(id_{\mathbb{R}_{\infty}})$} (R);
\end{tikzpicture}

The [[standard Borel space]] $\mathbb{R}_{\infty}$ is the one point compactification of the real line. (There is no $G$-algebra $G(\mathbb{R}) \rightarrow \mathbb{R}$; so to model any process with measurement $\Omega \xrightarrow{f} \mathbb{R}$ we first need to embedd $\mathbb{R}$ into $\mathbb{R}_{\infty}$.)
The operator $\mathbb{E}_{\bullet}(id_{\mathbb{R}_{\infty}})$ is defined at each $P \in G(\mathbb{R}_{\infty})$ by $\mathbb{E}_{P}(id_{\mathbb{R}_{\infty}}) =\int id_{\mathbb{R}_{\infty}} \, dP$.  

Note that measurements $\Omega \xrightarrow{f} X$ can be taken over any object $X$ which lies in the category of algebras of the monad $G$. In the case where $X$ is a [[standard Borel space]] the $G$-algebra $G(X) \xrightarrow{\mathbb{E}_{\bullet}(id_X)} X$, which is a morphism in the [[category of algebras]], is defined as: $\mathbb{E}_{P}(id_X)$ is the unique element in $X$ such that for all affine [[measurable maps]] $X \xrightarrow{m} \mathbb{R}_{\infty}$, the property
\begin{equation} m(\mathbb{E}_P(id_X)) = \int_X m \, dP
\end{equation}
holds. (Every algebra $X$ necessarily possesses a [[convex space]] structure. The case $X=\mathbb{R}_{\infty}$ is just a special case which trivially satisfies the above property since the affine maps $\mathbb{R}_{\infty} \xrightarrow{m} \mathbb{R}_{\infty}$ are of the form $m(r) =\lambda r + t$ (scale + translate) and hence $\mathbb{E}_{\bullet}(id_{\mathbb{R}_{\infty}})$ simplifies to the standard expectation operator.  A derivation of the category of algebras for [[standard Borel space]] is given on the [[Giry monad]] page.)
\end{example}

\begin{example}
Here are two  elementary examples of an indivisible stochastic process due to [Barendes 2025](#Barendes25).  Taking the [[finite space]] $\Omega = \{1,2\}=\Omega_n$ for all $n$, and defining the dynamic law $\Omega \xrightarrow{\tilde{Q}_n} \Omega$ by 
$$ \tilde{Q}_n =  \begin{pmatrix} e^{-\frac{t_n^2}{\tau^2}} & 1-e^{-\frac{t_n^2}{\tau^2}} \\ 1-e^{-\frac{t_n^2}{\tau^2}} & e^{-\frac{t_n^2}{\tau^2}} \end{pmatrix} 
$$
where $t_n$ is the time at stage $n$, and $\tau$ is a constant. (For a finite space $\Omega$ a dynamic law $\Omega \rightarrow \Omega$ can be represented by a matrix.)

Similarly, on the same space $\Omega$, we can define
$$ \tilde{Q}_n =  \begin{pmatrix} \cos^2(\omega t_n) & \sin^2(\omega t_n) \\ \sin^2(\omega t_n) & \cos^2(\omega t_n) \end{pmatrix} 
$$
where $\omega$ is a constant.
\end{example}



## References


* Wikipedia [stochastic process](https://en.wikipedia.org/wiki/Stochastic_process)

* {#Lawvere62} [[William Lawvere]], *The Category of Probabilistic Mappings With Applications to Stochastic Processes, Statistics, and Pattern Recognition* (1962), including abstract and commentary added by Lawvere in 2020, [Lawvere Archive](https://lawverearchives.com) (2025) &lbrack;[pdf](https://lawverearchives.com/wp-content/uploads/2025/07/1962.probmap.pdf)&rbrack;

* Xiao-qing Meng, *Categories of convex sets and of metric spaces with applications to stochastic programming and related areas*, PhD thesis ([[Meng.djvu|djvu:file]])

* {#Barendes25} [[Jacob Barandes]], *Quantum Systems as Indivisible Stochastic Processes* &lbrack;[arXiv:2507.21192](https://arxiv.org/abs/2507.21192)&rbrack;

With an eye towards [[quantum noise]];

* [[Stéphane Attal]], *Stochastic Processes*, Lecture 4 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Stochastic_Processes.pdf), [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;

On some kind of [[supersymmetry]] in stochastic PDEs:

* Igor V. Ovchinnikov: *Ubiquitous order known as chaos* &lbrack;[arXiv:2503.17157](https://arxiv.org/abs/2503.17157)&rbrack;



[[!redirects stochastic processes]]

[[!redirects random process]]
[[!redirects random processes]]
