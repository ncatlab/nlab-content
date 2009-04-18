

#Idea#

Differential cohomology is a refinement of ordinary [[cohomology]] such that a differential cocycle is to its underlying ordinary cocycle as a bundle with connection is to its underlying bundle.

The details of a formulation of differential cohomology depend on how the generalized [[cohomology]] theory itself is formulated.

The best known version of differential cohomology is a differential refinement of generalized cohomology in the sense of  the generalized Eilenberg-Steenrod axioms. This is a [[stable (infinity,1)-category|stable]] version of generalized cohomology.

A differential refinement of non-stable, i.e. [[nonabelian cohomology]] is developed [[schreiber:Differential Nonabelian Cohomology|here]].

# Differential stable cohomology #

Let $\Gamma^\bullet$ be a generalized cohomology theory in the sense of the generalized Eilenberg-Steenrod axioms, and let 
$\Gamma^\bullet \to H^\bullet(-,\mathbb{R}) \otimes \Gamma^\bullet(*)$ be a morphism to real singular cohomology with coefficients in the ring of $\Gamma$-cohomology of the point. Then the differential refinement of $\Gamma^\bullet$, the **differential $\Gamma$-cohomology** is the [[homotopy pullback]] $\bar \Gamma^\bullet$ in

$$
  \array{
  \bar \Gamma^\bullet(-)
  &\to&
  \Omega^\bullet(-)\otimes \Gamma^\bullet(*)
  \\
  \downarrow && \downarrow
  \\
  \Gamma^\bullet(-)
  &\to&
  H^\bullet(-, \mathbb{R}) \otimes \Gamma^\bullet(*)
  }
  \,,
$$

where $\Omega^\bullet(-,\mathbb{R})$ is the complex underlying deRham cohomology and $\Omega^\bullet(-) \to H^\bullet(-,\mathbb{R})$ is the deRham map.

##Examples##

* Differential integral cohomology $\bar H^\bullet(-,\mathbb{Z})$ is modeled by 

  * [[Deligne cohomology]];

  * [[Cheeger-Simons differential character]]s;
 
  * higher circle [[bundle gerbe]]s with connection;

* apart from that people studied mainly differential [[K-theory]]

##References##

A detailed discussion of the axiomatization of differential stable cohomology is

* M. Hopkins and I. Singer, _Quadratic functions in geometry, topology,and M-theory_ ([arXiv](http://arxiv.org/abs/math/0211216))

Based on this Dan Freed interpreted large classes of gauge fields in [[physics]] in terms of differential stable cohomology in 

* D. Freed, _Dirac Charge Quantization and Generalized Differential Cohomology_ ([arXiv](http://arxiv.org/abs/hep-th/0011220))

The differential refinement of K-theory was and is studied in a series of articles by Bunke and Schick. See for instance

* U. Bundle, _Differential cohomology in geometry and analysis_ ([pdf slides](http://www.uni-regensburg.de/Fakultaeten/nat_Fak_I/Bunke/Vortrag-Erlangen.pdf))

and many more...


## blog discussion ##

* [(Generalized) Differential Cohomology and Lie Infinity-Connections](http://golem.ph.utexas.edu/category/2008/02/lie_infinityconnections_and_ge.html)


# Differential non-abelian cohomology #

for the moment, see [[schreiber:Differential Nonabelian Cohomology]]
