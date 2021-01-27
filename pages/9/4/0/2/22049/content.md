\tableofcontents

\section{Idea}

The [[category of cubical sets]], just as with any reasonable category of [[geometric shapes for higher structures|shapes for higher structures]], admits a [[geometric realization|geometric realisation]] functor to the [[category of topological spaces]]. The universal property of the [[category of cubes]] allows for a particularly economical and canonical construction of this functor compared to some other such categories of shapes.  

\section{Construction}

We make use of the notation at [[category of cubes]] and [[cubical set]], and denote the [[category of topological spaces]] by $\mathsf{Top}$. Let $I$ denote the topological [[unit interval]], let $\bullet$ denote the topological [[point]], let $0 : \bullet \rightarrow I$ and $1: \bullet \rightarrow I$ be the [[maps|continuous map]] which pick out the endpoints $0$ and $1$ of $I$ respectively, and let $t : I \rightarrow \bullet$ be the canonical map. 

\begin{notn} We denote by $\left| - \right|_{\leq 1}$ the [[functor]] $\square_{\leq 1} \rightarrow \mathsf{Top}$ given by $I^{0} \mapsto \bullet$, $I^{1} \mapsto I$, $i_{0} \mapsto 0$, $i_{1} \mapsto 1$, and $p \mapsto t$. \end{notn}

\begin{notn} We denote by $\left| - \right|_{\square}: \square \rightarrow \mathsf{Top}$ the canonical functor determined by $\left| - \right|_{\leq 1}$, the [[cartesian monoidal category|cartesian monoidal structure]] on $\mathsf{Top}$, and the universal property of $\square$. \end{notn}

\begin{defn} The _geometric realisation_ functor $\mathsf{Set}^{\square^{op}} \rightarrow \mathsf{Top}$ is the canonical functor determined by $\left| - \right|_{\square}$, the fact that $\mathsf{Top}$ is co-complete, and the universal property of $\mathsf{Set}^{\square^{op}}$. \end{defn}

[[!redirects cubical geometric realization]]
[[!redirects geometric realisation of cubical sets]]
[[!redirects geometric realization of cubical sets]]