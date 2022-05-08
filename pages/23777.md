# Remark
This is a collection of my (Tom Mainiero's) personal notes on some functorial aspects on the GNS representation that have been sitting around for a while. Please feel free to contribute! The ideas here underlie some of the constructs of [Homtools](#Mainiero2019)

## The GNS correspondence as a functor on a fixed $C^{*}$-algebra

There are a few interesting preorders on positive linear functionals.
\begin{definition}

Let $f, g \colon A \rightarrow \mathbb{C}$ be positive linear functionals on a $C^\ast$-algebra $A$.

* We say $f$ is *weakly dominated* by $g$ and write $f \ll g$ if there is an inclusion of left-kernels $\ker^{L}(g) \subseteq \ker^{L}(f)$.
		
* We say $f$ is *dominated by* $g$ and write $f \lesssim g$ if there exists an $M$ such that $f(a^{*}a) \leq M g(a^{*} a)$ for every $a \in A$.  
		
* We say $f$ is *strongly dominated* by $g$ if $f \leq g$ as positive linear functionals (i.e. such that $f(a^{*}a) \leq g(a^{*} a)$ for every $a \in A$).

\end{definition}

\begin{remark}
		
* Of course $f \leq g \Rightarrow f \lesssim g \Rightarrow f \ll g$.
		
* $\leq$ is a partial order as it is antisymmetric: $f \leq g$ and $g \leq f$ if and only if $f = g$.

  However, the weaker preorders $\ll$ and $\lesssim$ do not satisfy antisymmetry: e.g. $2 f \lesssim f$ and $f \lesssim 2f$. 
		
		
* While $\lesssim$ is only a mild weakening of $\leq$, the weakest preorder $\ll$ is vastly different. In particular, we will show there is a unique Radon-Nikodym derivative associated to every pair of functionals related by the preorders $\leq$ and $\lesssim$;the result can be weakened for $\ll$ but the Radon-Nikodymderivative will be an \textit{unbounded} (densely defined) operator. 

  See [Stanley Gudder's ``A Radon-Nikodym Theorem for $*$-Algebras.](\href{https://projecteuclid.org/download/pdf_1/euclid.pjm/1102785959)

\end{remark}


\begin{definition}
Fix $\prec$ to be one of the partial orders $\ll,\,\lesssim,\,$ or $\leq$ and let $A$ be a fixed $C^{*}$-algebra.
		
-  The category $\textbf{State}^{\prec}(A)$ is the opposite of the thin category determined by the preorder $\prec$, i.e. it is the category whose objects are all positive linear functionals on $A$ (including the zero functional), and whose morphism sets are given by
\[
  \textbf{State}^{\prec}(A)(\omega, \nu) = 
  \left\{
    \begin{array}{ll}
       - & \text{if $\nu \prec \omega$}\\    
       \emptyset & \text{otherwise}    
    \end{array}
\right.
\]
where $*$ denotes the one point set.

* The category $\textbf{ptRep}(A)$ is the category whose objects are pointed $\ast$-representations and whose morphisms are given by "$\ast$-intertwiners" preserving points. I.e. objects are triples $(\mathcal{H}, v, \pi: A \rightarrow B \mathcal{H})$ of a Hilbert space $\mathcal{H}$ a vector $v \in \mathcal{H}$ and a $\ast$-representation $\pi$, while a morphism from $\pi_1$ to $\pi_2$ is a bounded linear map $f: \mathcal{H}_{1} \rightarrow \mathcal{H}_{2}$ such that $f v_{1} = v_{2}$ and
\[
  f \circ \pi_{1}(a) =  \pi_{2}(a) \circ f	
\]
for all $a \in A$.

\end{definition}


# References

* {#Mainiero2019} [[Tom Mainiero]], _Homological Tools for the Quantum Mechanic_, ([arXiv:1901.02011](https://arxiv.org/abs/1901.02011))


