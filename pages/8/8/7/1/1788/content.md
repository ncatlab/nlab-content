[[!redirects sandbox]]

A test, test, test

\begin{tikzcd}
   X \arrox}ww[rr, "f"] \arrow[dr, swap, "I f"]
&& Y \\
&  \Gamma f \arrow[ur, "P f"]
\end{tikzcd}

Anyons via fictitious gauge fields:

From Chen et al. p. 359:

> Here the particles are to be regarded (in the absence of 
interactions) as fermions; the interaction then makes them anyons with statistical 
parameter ($\theta = \pi(1 - 1/ n$).

***




* [[Alexander B. Zamolodchikov]], [[Vladimir A. Fateev]] *Nonlocal (parafermion) currents in two-dimensional conformal quantum field theory and self-dual critical points in $Z_N$-symmetric statistical systems*, Sov. Phys. JETP **62** 2 (1985) 215-225 $[$[pdf](http://www.jetp.ras.ru/cgi-bin/dn/e_062_02_0215.pdf), [osti:5929972](https://www.osti.gov/biblio/5929972)$]$


* Yi-Ting Tu, Po-Yao Chang, *Non-Abelian fracton order from gauging a mixture of subsystem and global symmetries*, Phys. Rev. Research **3** (2021) 043084 $[$[arXiv:2103.08603](https://arxiv.org/abs/2103.08603), [doi:10.1103/PhysRevResearch.3.043084](https://doi.org/10.1103/PhysRevResearch.3.043084)$]$

* *Classification and surface anomaly of glide symmetry protected topological phases in three dimensions* [pdf](https://iopscience.iop.org/article/10.1088/1367-2630/aa769b/pdf)

* Mircea Trif, Pramey Upadhyaya, Yaroslav Tserkovnyak, *Theory of electromechanical coupling in dynamical graphene*, Phys. Rev. B **88** 245423 (2013) $[$[doi:10.1103/PhysRevB.88.245423](https://doi.org/10.1103/PhysRevB.88.245423), [arXiv:1210.7384](https://arxiv.org/abs/1210.7384)$]$

***

test

\linebreak

\linebreak

\linebreak


***

Original articles:

* [[Michael Levin]], [[Xiao-Gang Wen]], *String-net condensation: A physical mechanism for topological phases*, Phys.Rev. B **71** (2005) 045110 $[$[arXiv:cond-mat/0404617](http://arxiv.org/abs/cond-mat/0404617)$]$

  > (see also at *[[Levin-Wen model]]*)

* [[Michael Levin]], [[Xiao-Gang Wen]], *Detecting topological order in a ground state wave function*, Phys. Rev. Lett., 96, 110405 (2006) ([arXiv:cond-mat/0510613](https://arxiv.org/abs/cond-mat/0510613))

  > (introducing [[topological entanglement entropy]] with regards to string-net models)

In terms of [[tensor networks]]:

* O. Buerschaper, M. Aguado, G. Vidal, *Explicit tensor network representation for the ground states of string-net models*, Phys. Rev. B **79** (2009) 085119 $[$[arXiv:0809.2393](https://arxiv.org/abs/0809.2393), [doi:10.1103/PhysRevB.95.195110](https://doi.org/10.1103/PhysRevB.95.195110)$]$


* [[Zheng-Cheng Gu]], [[Michael Levin]], [[Brian Swingle]], [[Xiao-Gang Wen]], *Tensor-product representations for string-net condensed states*, Phys. Rev. B **79** (2009) 085118 $[$[doi:10.1103/PhysRevB.79.085118](https://doi.org/10.1103/PhysRevB.79.085118)$]$  

Further development:

* Ling-Yan Hung, Yidun Wan, *String-Net Models with $\mathbb{Z}_N$ Fusion Algebra*, Phys. Rev. B **86** (2012) 235132 $[$[arXiv:1207.6169](https://arxiv.org/abs/1207.6169)$]$


* Chien-Hung Lin, *Multi-flavor string-net models*, Phys. Rev. B **95** 195110 (2017) $[$[arXiv:1611.08288](https://arxiv.org/abs/1611.08288), [doi:10.1103/PhysRevB.95.195110](https://doi.org/10.1103/PhysRevB.95.195110)$]$

Review and exposition:

* [[Bei Zeng]], [[Xie Chen]], [[Duan-Lu Zhou]], [[Xiao-Gang Wen]]: 

  Sections 6.4-6.9 in: *[[Quantum Information Meets Quantum Matter]] -- From Quantum Entanglement to Topological Phases of Many-Body Systems*, Quantum Science and Technology (QST), Springer (2019) $[$[arXiv:1508.02595](https://arxiv.org/abs/1508.02595), [doi:10.1007/978-1-4939-9084-9](https://doi.org/10.1007/978-1-4939-9084-9)$]$

* Chien-Hung Lin, [[Michael Levin]], Fiona J. Burnell, *Generalized string-net models: A thorough exposition*, Phys. Rev. B **103** (2021) 195155  $[$[arXiv:2012.14424](https://arxiv.org/abs/2012.14424), [doi:10.1103/PhysRevB.103.195155](https://doi.org/10.1103/PhysRevB.103.195155)$]$


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


