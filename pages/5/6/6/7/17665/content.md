
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



## Example

 A 2-stage stochastic process $\mathbf{Q}$ with  measurements $\Omega_i \xrightarrow{f_i} \mathbb{R}$ modeled within the category of algebras of the [[Giry monad]] $G$ is given by

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
  \draw[->,left] (GO1) to node {$G(f)$} (GR0);
  \draw[->>,left] (GR0) to node {$\mathbb{E}_{\bullet}(id_{\mathbb{R}_{\infty}})$} (R0);

  \node (GR) at (15,-1.5) {$G(\mathbb{R}_{\infty})$};
  \node (R)  at (15, -3)  {$\mathbb{R}_{\infty}$};
  \draw[->,left] (GO2) to node {$G(f)$} (GR);
  \draw[->>,left] (GR) to node {$\mathbb{E}_{\bullet}(id_{\mathbb{R}_{\infty}})$} (R);
\end{tikzpicture}

The [[standard Borel space]] $\mathbb{R}_{\infty}$ is the one point compactification of the real line. (There is no $G$-algebra $G(\mathbb{R}) \rightarrow \mathbb{R}$; so to model any process with measurement $\Omega \xrightarrow{f} \mathbb{R}$ we first need to embedd $\mathbb{R}$ into $\mathbb{R}_{\infty}$.)
The operator $\mathbb{E}_{\bullet}(id_{\mathbb{R}_{\infty}})$ is defined at each $P \in G(\mathbb{R}_{\infty})$ by $\mathbb{E}_{P}(id_{\mathbb{R}_{\infty}}) =\int f \, dP$.  

Note that measurements $\Omega \xrightarrow{f} X$ can be taken over any object $X$ which lies in the category of algebras of the monad $G$. In the case where $X$ is a [[standard Borel space]] the $G$-algebra $G(X) \xrightarrow{\mathbb{E}_{\bullet}(id_X)} X$, which is a morphism in the category of algebras, is defined by $\mathbb{E}_{P}(id_X)$ is the unique element in $X$ such that for all affine maps $X \xrightarrow{m} \mathbb{R}_{\infty}$, the property $m(\mathbb{E}_P(id_X)) = \int_X f \, dP$ holds. (Every algebra $X$ necessarily possesses a convex space structure. The case $X=\mathbb{R}_{\infty}$ is just a special case of the general condition which simplifies to the standard expectation operator.)
 
## References


* Wikipedia [stochastic process](https://en.wikipedia.org/wiki/Stochastic_process)

With an eye towards [[quantum noise]];

* [[Stéphane Attal]], *Stochastic Processes*, Lecture 4 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Stochastic_Processes.pdf), [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;

On some kind of [[supersymmetry]] in stochastic PDEs:

* Igor V. Ovchinnikov: *Ubiquitous order known as chaos* &lbrack;[arXiv:2503.17157](https://arxiv.org/abs/2503.17157)&rbrack;





[[!redirects stochastic processes]]

[[!redirects random process]]
[[!redirects random processes]]
