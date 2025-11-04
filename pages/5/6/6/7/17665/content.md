
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
A __stochastic process__ describes a dynamical system evolving over a [[linearly ordered set]] $T$ ("time", typically the integers or positive real axis) whose dynamical laws are morphisms in the Kleisi category of the [[Giry monad]] (or any other probability monad). By working in the larger category of algebras of that monad, a characterization  of a stochastic processes can be modeled in terms of the expected value of measurements on that process. 

By a __random process__ physicists usually mean the same, but mathematicians sometimes allow random processes indexed by more general sets, not usually with meaning of time or equipped with a linear order. 

The most studied examples include [[Brownian motion]], [[Ornstein-Uhlenbeck process]] and [[Lévy process]]es. The concept of an __indivisible stochastic process__ leads to [[Jacob Barandes]] [[indivisible stochastic process interpretation of quantum mechanics]].

## Definition

We define discrete time stochastic processes following Lawvere 1962 unpublished document.  Let $N$ be the category with countably many objects and no non-identify morphisms, and let $\mathbf{Meas}_G$ denote the Kleisi category of the Giry monad.  Let $\mathbf{Meas}_G^{N}$ denote the category whose objects $\mathbf{\Omega}$ are sequences $\Omega_0, \Omega_1, \Omega_2,\ldots$ of objects in $\mathbf{Meas}_G$. (The objects in $\mathbf{Meas}_G$ are measurable spaces.)  We define an endofunctor $\mathbf{Meas}_G^{N} \xrightarrow{\mathbf{\Phi}} \mathbf{Meas}_G^{N}$ by 
$
\mathbf{\Phi}(\mathbf{\Omega})= \{ \prod_{k \lt n} \Omega_k \}_{k \in N}  
$
where $\prod_{k \lt n} \Omega_k$ denotes the product measurable space with the smallest $\sigma$-algebra such that all the coordinate-projection functions are measurable.  If $\Omega_n$ is thought of as the space of all possible states of a system at time $n$, then $\mathbf{\Phi}(\mathbf{\Omega})_n=\prod_{k \lt n}\Omega_k$ is the space of all possible histories of the system before time $n$.

We define a __discrete time stochastic process__ $\mathbf{Q}$ to be a [[natural transformation]]
\begin{equation} 
\mathbf{\Phi} \xrightarrow{\mathbf{Q}} \mathbf{id}
\end{equation}
where $\mathbf{id}$ is the identity functor on $\mathbf{Meas}_G^N$.  Given any two (discrete time) stochastic processes $\mathbf{Q}$ and $\mathbf{Q}'$  we define a sequence of morphisms in $\mathbf{Meas}_G$, $\Omega_n \xrightarrow{f_n} \Omega_n^{'}$ to be a morphism from $\mathbf{Q}$ to $\mathbf{Q}'$ when, for each $n \in N$, the $\mathbf{\Meas}_G$-diagram

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

commutes. Since there is an obvious notion of composition for such maps,all stochastic processes and all such maps of such determine the category of discrete time stochastic processes $\mathbf{dStoch}$.  (Warning: Some authors have used the notation $\mathbf{Stoch}$ ([[Stoch]]) to mean the Kleisi category of the Giry monad, traditionally denoted by $\mathbf{Meas}_G$ or $\mathcal{K}(G)$. The two categories $\mathbf{Stoch}$ and $\mathbf{dStoch}$ are only related in the loose sense that they both employ the Kleisi category of the Giry monad in their definition.)

In the preceding diagram the morphisms $Q_n$, which are Kleisi morphisms
$
\prod_{k \lt n} \Omega_k \xrightarrow{Q_n} \Omega_n
$
are called  __dynamic laws__, and stochastic processes are classified by properties of the dynamic laws.

A __Markov dynamic law__ $Q_n$ is a dynamic law depending only on the current state, i.e., $Q_n$ factors as
\begin{tikzpicture}
  \node  (POn) at  (0,0)  {$\prod_{k < n} \Omega_k$};
  \node  (On)  at  (6,0)  {$\Omega_n$};
  \node  (On1) at  (3,-1.5)  {$\Omega_{n-1}$};
  \draw[->,above] (POn) to node {$Q_n$} (On);
  \draw[->,left]  (POn) to node {$\prod_{n-1}$} (On1);
  \draw[->,right] (On1) to node [xshift=3pt,yshift=-3pt]{$\tilde{Q}_n$} (On); 
\end{tikzpicture}
where $\prod_{n-1}$ is the canonical coordinate projection (measurable) function which specifies the deterministic Kleisi morphism (with the same notation).  Thus a Markov dynamic law only depends upon the current state and not its history.

If $\mathbf{Q}$ is a stochastic process such that the dynamic law at every stage is a Markov dynamic law we say the stochastic process $\mathbf{Q}$ is a __Markov stochastic process__.  In  the special case where $\mathbf{\Omega}$ defines a constant sequence, $\Omega_n = \Omega$ for all $n$,   then a Markov stochastic process on $\mathbf{\Omega}$ is called a [[Markov chain]].

[Ed. Note. Add the definition of an __indivisible stochastic process__].

## Example

 A 2-stage stochastic process $\mathbf{Q}$ with  measurements $\Omega_i \xrightarrow{f_i} \mathbb{R}$, modeled within the category of algebras of the [[Giry monad]] $(G, \eta, \mu)$ so that the process $\mathbf{Q}$ can be characterized in terms of the expected values of the measurements, is given by

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
The operator $\mathbb{E}_{\bullet}(id_{\mathbb{R}_{\infty}})$ is defined at each $P \in G(\mathbb{R}_{\infty})$ by $\mathbb{E}_{P}(id_{\mathbb{R}_{\infty}}) =\int f \, dP$.  

Note that measurements $\Omega \xrightarrow{f} X$ can be taken over any object $X$ which lies in the category of algebras of the monad $G$. In the case where $X$ is a [[standard Borel space]] the $G$-algebra $G(X) \xrightarrow{\mathbb{E}_{\bullet}(id_X)} X$, which is a morphism in the category of algebras, is defined as: $\mathbb{E}_{P}(id_X)$ is the unique element in $X$ such that for all affine maps $X \xrightarrow{m} \mathbb{R}_{\infty}$, the property
\begin{equation} m(\mathbb{E}_P(id_X)) = \int_X m \, dP
\end{equation}
holds. (Every algebra $X$ necessarily possesses a convex space structure. The case $X=\mathbb{R}_{\infty}$ is just a special case which trivially satisfies the above property since the affine maps $\mathbb{R}_{\infty} \xrightarrow{m} \mathbb{R}_{\infty}$ are of the form $m(r) =\lambda r + t$ (scale + translate) and hence $\mathbb{E}_{\bullet}(id_{\mathbb{R}_{\infty}})$ simplifies to the standard expectation operator.  When $X$ is a discrete standard space the operator $\mathbb{E}_{\bullet}(id_X)$ is $\mathbf{not}$ the standard expectation operator with $X=n=\{0,1,2,\ldots\}$ ''embedded'' into $\mathbb{R}_{\infty}$. More generally, if $X$ is an algebra of the $G$ monad whose convex space structure is either of discrete type or of mixed type then the expectation operator $\mathbb{E}_{\bullet}(id_X)$ is not the standard expectation operator.  Only in the special case where the convex space structure of $X$ is of geometric type does the expectation operator $\mathbb{E}_{\bullet}(id_X)$ coincide with the usual interpretation.)
 
## References


* Wikipedia [stochastic process](https://en.wikipedia.org/wiki/Stochastic_process)

* [[William Lawvere]], *The Category of Probabilistic Mappings With Applications to Stochastic Processes, Statistics, and Pattern Recognition*, including abstract and commentary added by Lawvere in 2020, [Lawvere Archive](https://lawverearchives.com) (2025) &lbrack;[pdf](https://lawverearchives.com/wp-content/uploads/2025/07/1962.probmap.pdf)&rbrack;

* Xiao-qing Meng, *Categories of convex sets and of metric spaces with applications to stochastic programming and related areas*, PhD thesis ([[Meng.djvu|djvu:file]])

With an eye towards [[quantum noise]];

* [[Stéphane Attal]], *Stochastic Processes*, Lecture 4 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Stochastic_Processes.pdf), [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;

On some kind of [[supersymmetry]] in stochastic PDEs:

* Igor V. Ovchinnikov: *Ubiquitous order known as chaos* &lbrack;[arXiv:2503.17157](https://arxiv.org/abs/2503.17157)&rbrack;



[[!redirects stochastic processes]]

[[!redirects random process]]
[[!redirects random processes]]
