e finito

\linebreak

\linebreak

\linebreak


***


\section{Idea}

Expositions of [[topological data analysis]] traditionally invoke *point clouds* -- [[discrete space|discrete]] [[subsets]] of some [[metric space]] --  as the generic mathematical incarnation of datasets to be analyzed. 

Maybe a more realistic and more encompassing model for sets of observed data -- namely for *measurement results* -- is the time-honored notion of a tuple of (values of) *[[real number|real]] [[observables]]*, namely a [[continuous function]]

$$
  Obs
  \;\colon\;
  X 
  \xrightarrow{\phantom{---}}
  \mathbb{R}^n
$$

to the [[one-point compactification]] of $n$-[[dimension of a vector space|dimensional]] [[Cartesian space]].

A feature in the data as seen by such an observable is then an [[isosurface]] of $Obs$, hence the [[pre-image]] 

$$
  Obs^{-1}(\vec v) 
  \;\coloneqq\;
  \Big\{
    x \in X
    \,\big\vert\,
    Obs(x) = \vec v
  \Big\}
  \;\subset\; X
$$ 

of a [[tuple]] $\vec v \in \mathbb{R}^n$ of observed values.

Without restriction of generality we may assume that the observed value of interest is the origin $0 \in \mathbb{R}^n$, for if it is instead some $\vec v \in \mathbb{R}^n$ then we may instead pass to the observable $Obs \coloneqq Obs - const_{\vec v}$ without changing the essence of the situation.

In practice, the value of an observable can never be determined with the accuracy of a mathematical point in $\mathbb{R}^n$, instead there will be some [[positive number|positive]] [[real number]] $r \in \mathbb{R}_{\gt 0}$ such that one may hope (or wish) to measure $Obs$ up to measurement errors within a [[radius]] $r$. In this case, the desired [[isosurface]] could be any element in the set

$$
  \Big\{
    f^{-1}(0)
    \subset 
    X
    \,\vert\,
    f \in C^0(X,\mathbb{R}^n)
    ,\,
    \Vert f - Obs \Vert_\infty \lt r
  \Big\}
$$



For example, $X$ might model the interior of a plasma container (say a fusion reactor) and $Ob = (T, p) : X \to \mathbb{R}^2$ could be the combined [[temperature]]- and [[pressure]]-observable (say as seen by laser probes into the plasma). Its [[isosurfaces]] are the [[intersections]] of given [[isobars]] with [[isotherms]].


The aim of *[[topological data analysis]]* (TDA) is to provide qualitative analysis of large data/parameter sets in a way which is *robust* against uncertainties and noise. This is accomplished using tools and theorems from the mathematical field of *[[algebraic topology]]*. While a tool called *[[persistent homology]]* has become the signature method of TDA, it tends to produce answers that are either hard to interpret or impossible to compute. Both problems are solved by a variant method which we may call *[[persistent cohomotopy]]*: A first result shows that this new method provides computable answers to the concrete question of detecting whether there exist data+parameters that meet a prescribed target indicator precisely, even in the presence of uncertainty and noise. Strikingly, [[cohomotopy]]-theory has deep roots in the mathematics of [[differential topology]] and [[schreiber:Hypothesis H|profound relations]] to [[string theory|formal high energy physics]] and [[topological phase of matter|quantum materials]], connecting to which is likely to enhance the power of [[topological data analysis]].


