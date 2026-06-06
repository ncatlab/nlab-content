
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

The most studied examples include [[Markov processes]] (Def. \ref{MarkovProcess}), *[[Brownian motion]]*, *[[Ornstein-Uhlenbeck processes]]* and *[[Lévy processes]]*. 


## Definitions
 {#Definitions}

We denote by:

* *$\mathbb{N}$ the [[category]] with [[countable set|countably many]] [[objects]], $\{0,1,2,...\}$, and no non-[[identity morphisms]], 

* $\mathbf{Meas}_G$ the [[Kleisli category]] of the [[Giry monad]],

* $\mathbf{Meas}_G^{\mathbb{N}}$ the [[category]] whose [[objects]] $\mathbf{\Omega}$ are [[sequences]] $\Omega_0, \Omega_1,\ldots$ of objects in $\mathbf{Meas}_G$ which are [[measurable spaces]],

* $\mathbf{Meas}_G^{N} \xrightarrow{\mathbf{\Phi}} \mathbf{Meas}_G^{N}$ the [[endofunctor]] given by

  \[
    \label{TheEndofunctor}
    \mathbf{\Phi}\big(\Omega_\bullet\big)_n
    \,\coloneqq\, 
    \textstyle{\prod_{k \lt n}} 
    \Omega_k 
    \mathrlap{\,,}
  \]
  
  where $\prod_{k \lt n} \Omega_k$ denotes the [[Cartesian product|product]] measurable space with the smallest [[sigma-algebra|$\sigma$-algebra]] such that all the [[coordinate]]-[[projection]] functions are [[measurable function|measurable]].  

  So if $\Omega_n$ is thought of as the space of all possible states of a system at time $n$, then $\mathbf{\Phi}(\Omega_\bullet)_n  = \prod_{k \lt n}\Omega_k$ is the space of all possible histories of the system before time $n$.

### Stochastic processes
 {#DefinitionStochasticProcesses}

The following definition in [[category-theoretic probability theory]] is due to [Lawvere 1962 §3.2](#Lawvere62).  

\begin{definition}
\label{DiscreteTimeStochasticProcess}
A *discrete time stochastic process* is an [[algebra over an endofunctor|algebra over the endofunctor]] $\mathbf{\Phi}$ (eq:TheEndofunctor).

This means that a *discrete time stochastic process* is:

1. a [[sequence]] $\Omega_\bullet$ of [[measurable spaces]] $\Omega_n$ (an object in $\mathbf{Meas}_G^{\mathbb{N}}$), 

1. a [[morphism]] $Q_\bullet$ in $\mathbf{Meas}_G^{\mathbb{N}}$:

\begin{equation} 
  Q_\bullet
  \,\colon\,
  \mathbf{\Phi}(\Omega_\bullet) \longrightarrow \Omega_\bullet
  \mathrlap{\,.}
\end{equation}

Because $\mathbb{N}$ is a discrete category, the morphism $Q_\bullet$ consists of a sequence of component morphisms $Q_n$ (which are [[Kleisli morphisms]])
$$
  Q_n
  \,\colon\,
  \textstyle{\prod_{k \lt n}} 
  \Omega_k \longrightarrow \Omega_n
$$
also called  *dynamic laws* (of motion) at time $n$.
\end{definition}



\begin{definition}
\label{MorphismOfDiscreteTimeStochasticProcesses}
The [[homomorphisms]] between stochastic processes are [homomorphisms of algebras of endofunctors](algebra+for+an+endofunctor#AlgebraOverAnEndofunctor). This means:

Given a [[pair]] $\mathbf{Q}$ and $\mathbf{Q}'$  of such (discrete time) stochastic processes (Def. \ref{DiscreteTimeStochasticProcess}) a *[[morphism]]* 
$$
  \mathbf{Q} \longrightarrow \mathbf{Q}'
$$  
is a [[sequence]] $\big(f_n \colon \Omega_n \to \Omega_n^{'}\big)_{n \in \mathbb{N}}$  of [[morphisms]] in $\mathbf{Meas}_G$ such that for each $n \in \mathbb{N}$, the following $\mathbf{Meas}_G$-[[diagram]] [[commuting diagram|commutes]]:

\begin{tikzpicture}
  \node  (POn) at (0,0)  
  {$\big( \mathbf{\Phi}(\Omega_\bullet) \big)_n$};
   \node  (POpn) at (3,0)  
  {$\big( \mathbf{\Phi}  (\Omega'_\bullet) \big)_n$};
   \node (On) at (0,-1.5)  {$\Omega_n$};
   \node (Opn) at (3, -1.5) {$\Omega^{'}_n$};
   \draw[->,above] (POn) to node {$\mathbf{\Phi}(f_\bullet)_n$} (POpn);
   \draw[->,below] (On) to node {$f_n$} (Opn);
   \draw[->,left] (POn) to node {$Q_n$} (On);
   \draw[->,right] (POpn) to node {$Q'_n$} (Opn);
\end{tikzpicture}

With the evident notion of [[composition]], this defines the *category of discrete time stochastic processes*, $\mathbf{dStoch}$.  
\end{definition}


\begin{remark}
Beware that some authors use the notation [[Stoch|$Stoch$]] instead to denote the [[Kleisli category]] of the [[Giry monad]], traditionally denoted by $\mathbf{Meas}_G$ or $\mathcal{K}(G)$, which can also be interpreted (for modeling) as the category of [[Markov process|Markov stochastic processes]].
\end{remark}



### Markov processes

The following definition is as in [Lawvere 1962 §3.3](#Lawvere62).

\begin{definition}
\label{MarkovProcess}
A stochastic process $Q_\bullet$ (Def. \ref{DiscreteTimeStochasticProcess}) is called a *[[Markov process]]* if each $Q_n$ for $n \geq 1$ depends only on the current state in that it factors as:

\begin{tikzpicture}
  \node  (POn) at  (0,0)  {$\prod_{k < n} \Omega_k$};
  \node  (On)  at  (6,0)  {$\Omega_n$};
  \node  (On1) at  (3,-1.5)  {$\Omega_{n-1}\mathrlap{\,,}$};
  \draw[->,above] (POn) to node {$Q_n$} (On);
  \draw[->,left]  (POn) to node {$\pi_{n-1}$} (On1);
  \draw[->,right] (On1) to node [xshift=3pt,yshift=-3pt]{$\tilde{Q}_n$} (On); 
\end{tikzpicture}

where $\pi_{n-1}$ is the canonical [[coordinate]] [[projection]] ([[measurable function|measurable]]) [[function]] which specifies the deterministic [[Kleisli morphism]] (with the same notation).  

In  the special case where $\Omega_\bullet$ is [[constant function|constant]] on some $\Omega$, $\forall_n \colon \Omega_n = \Omega$, then a Markov stochastic process on $\Omega_\bullet$ is called a *[[Markov chain]]*.
\end{definition}

\begin{remark}
 When a non-[[Markov process|Markov]] stochastic process can be re-expressed as a Markov stochastic process by formally augmenting its states with a suitable collection of unobservable variables, then the resulting process is called a *hidden Markov model*.  The unobservable variables added to make the process look Markov are said to be *latent* or *hidden variables*.  For example, [[Bohmian mechanics|pilot wave theories]] can be viewed as Hidden Markov Models ([Barandes 2026](#Barandes26))
\end{remark}

### (In)Divisible processes
 {#InDivisibleProcesses}

The term "(in)divisible stochastic process" is not classical but has been brought up by [Barandes 2025](#Barandes25) in a suggestion to give an "[[indivisible stochastic process interpretation of quantum mechanics]]". Here is a way to state the definition in line with the above category-theoretic definitions and beyond finite state spaces:

\begin{definition}
\label{MultiStepMarginalTransition}
Given a discrete time stochastic process $Q_\bullet$ (Def. \ref{DiscreteTimeStochasticProcess}), its *multi-step marginal transition* from time $0$ to time $n$, denoted $Q_{0,n} \colon \Omega_0 \to \Omega_n$, is the [[Kleisli morphism]] obtained by forming the joint distribution over all intermediate states up to time $n$, and subsequently projecting onto the state space at time $n$.

Explicitly, one constructs a sequence of history-accumulating morphisms $J_n \colon \Omega_0 \to \prod_{k \le n} \Omega_k$ in $\mathbf{Meas}_G$ by [[mathematical induction|induction]]:

1. **Base case ($n=0$):** $J_0 \colon \Omega_0 \to \Omega_0$ is the [[identity morphism]] in $\mathbf{Meas}_G$ (representing the deterministic assignment $x \mapsto \delta_x$).
2. **Inductive step ($n \ge 1$):** Given $J_{n-1} \colon \Omega_0 \to \prod_{k \lt n} \Omega_k$, define $J_n$ as the [[Kleisli category|Kleisli composition]]:
   $$
     J_n \;\coloneqq\; \langle \mathbf{id}, Q_n \rangle \circ J_{n-1}
   $$
   where $\langle \mathbf{id}, Q_n \rangle \colon \prod_{k \lt n} \Omega_k \longrightarrow \prod_{k \le n} \Omega_k$ is the morphism given by pairing the deterministic identity on the history with the dynamic law $Q_n$. In the context of the [[Giry monad]], this pairing is canonically constructed via the [[monad|monadic]] [[tensorial strength]] (or equivalently, via the copy morphism in the framework of [[Markov categories]]).

The multi-step marginal transition $Q_{0,n}$ is then defined as the Kleisli composition of $J_n$ with the canonical [[coordinate]] [[projection]] $\pi_n$:
$$
  Q_{0,n} \;\coloneqq\; \pi_n \circ J_n
$$
where $\pi_n \colon \prod_{k \le n} \Omega_k \to \Omega_n$ is pushed forward as a deterministic Kleisli morphism. This construction is summarized by the following commuting diagram in $\mathbf{Meas}_G$:

\begin{tikzpicture}
  \node (O0)  at (0,0) {$\Omega_0$};
  \node (Hn1) at (3,0) {$\prod_{k < n} \Omega_k$};
  \node (Hn)  at (7,0) {$\prod_{k \le n} \Omega_k$};
  \node (On)  at (7,-1.5) {$\Omega_n$};
  
  \draw[->] (O0) to node[above] {$J_{n-1}$} (Hn1);
  \draw[->] (Hn1) to node[above] {$\langle \mathbf{id}, Q_n \rangle$} (Hn);
  \draw[->] (Hn) to node[right] {$\pi_n$} (On);
  \draw[->, dashed] (O0) to node[below left, xshift=-5pt] {$Q_{0,n}$} (On);
\end{tikzpicture}
\end{definition}

\begin{definition}
\label{DivisibleStochasticProcess}
A stochastic process $Q_\bullet$ (Def. \ref{DiscreteTimeStochasticProcess}) is called *divisible* if its multi-step marginal transitions $Q_{0,n} \colon \Omega_0 \to \Omega_n$ (Def. \ref{MultiStepMarginalTransition}) satisfy the *Chapman-Kolmogorov property*: 

Namely, for all stages $m \le n$, there exists a [[Kleisli morphism]] $\tilde{Q}_{m,n} \colon \Omega_m \to \Omega_n$ such that the following diagram in $\mathbf{Meas}_G$ [[commuting diagram|commutes]]:

\begin{tikzpicture}
  \node (O0) at (0,0) {$\Omega_0$};
  \node (Om) at (3,1.5) {$\Omega_m$};
  \node (On) at (3,-1.5) {$\Omega_n$};
  \draw[->] (O0) to node[above left] {$Q_{0,m}$} (Om);
  \draw[->] (O0) to node[below left] {$Q_{0,n}$} (On);
  \draw[->] (Om) to node[right] {$\tilde{Q}_{m,n}$} (On);
\end{tikzpicture}
  
Meaning that $Q_{0,n} = \tilde{Q}_{m,n} \circ Q_{0,m}$. 

\end{definition}

\begin{example}
 In discrete time, every [[Markov process]] (Def. \ref{MarkovProcess}) is automatically divisible (Def. \ref{DivisibleStochasticProcess}) by defining $\tilde{Q}_{m,n}$ as the composition of its 1-step transitions. 

Therefore, indivisibility is inherently a feature of non-Markovian processes (or continuous-time processes where intermediate transition kernels may fail to exist).
\end{example}



## Examples

\begin{example}
 A 3-stage Markov stochastic process $\mathbf{Q}$ with  measurements $\Omega_i \xrightarrow{f_i} \mathbb{R}$, modeled within the category of algebras of the [[Giry monad]] $(G, \eta, \mu)$ so that the process $\mathbf{Q}$ can be characterized in terms of the expected values of the measurements, is given by

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
Here are two  elementary examples of an indivisible stochastic process due to [Barandes 2025](#Barandes25).  Taking the [[finite space]] $\Omega = \{1,2\}=\Omega_n$ for all $n$, and defining the dynamic law $\Omega \xrightarrow{\tilde{Q}_n} \Omega$ by 
$$ \tilde{Q}_n =  \begin{pmatrix} e^{-\frac{t_n^2}{\tau^2}} & 1-e^{-\frac{t_n^2}{\tau^2}} \\ 1-e^{-\frac{t_n^2}{\tau^2}} & e^{-\frac{t_n^2}{\tau^2}} \end{pmatrix} 
$$
where $t_n$ is the time at stage $n$, and $\tau$ is a constant. (For a finite space $\Omega$ a dynamic law $\Omega \rightarrow \Omega$ can be represented by a matrix.)

Similarly, on the same space $\Omega$, we can define
$$ \tilde{Q}_n =  \begin{pmatrix} \cos^2(\omega t_n) & \sin^2(\omega t_n) \\ \sin^2(\omega t_n) & \cos^2(\omega t_n) \end{pmatrix} 
$$
where $\omega$ is a constant.
\end{example}



## References

General:

* Wikipedia: *[Stochastic process](https://en.wikipedia.org/wiki/Stochastic_process)*

Discussion in the context of [[category-theoretic approaches to probability theory]]:

* {#Lawvere62} [[William Lawvere]]: *The Category of Probabilistic Mappings With Applications to Stochastic Processes, Statistics, and Pattern Recognition* (1962), including abstract and commentary added by Lawvere in 2020, [Lawvere Archive](https://lawverearchives.com) (2025) &lbrack;[pdf](https://lawverearchives.com/wp-content/uploads/2025/07/1962.probmap.pdf)&rbrack;

* [[Xiao-Qing Meng]]: *Categories of convex sets and of metric spaces with applications to stochastic programming and related areas*, PhD thesis, New York (1988) &lbrack;[[Meng.djvu|djvu:file]], [[Meng-Stochastic.pdf|pdf:file]]&rbrack;


With an eye towards [[quantum noise]];

* [[Stéphane Attal]]: *Stochastic Processes*, Lecture 4 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Stochastic_Processes.pdf), [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;

On some kind of [[supersymmetry]] in stochastic PDEs:

* Igor V. Ovchinnikov: *Ubiquitous order known as chaos* &lbrack;[arXiv:2503.17157](https://arxiv.org/abs/2503.17157)&rbrack;

In the context of a proposed "[[indivisible stochastic process interpretation of quantum mechanics]]":

* {#Barandes25} [[Jacob Barandes]], *Quantum Systems as Indivisible Stochastic Processes* &lbrack;[arXiv:2507.21192](https://arxiv.org/abs/2507.21192)&rbrack;

* {#Barandes26} [[Jacob Barandes]], *Pilot-Wave Theories as Hidden Markov Models* &lbrack;[arXiv:2602.10569](https://arxiv.org/abs/2602.10569)&rbrack;



[[!redirects stochastic processes]]

[[!redirects random process]]
[[!redirects random processes]]
