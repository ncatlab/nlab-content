#Idea#

Under certain conditions on a given [[homotopy theory]] on a category $C$, the morphisms in the homotopy category $Ho(C)$ are represented already by spans 

$$
  \array{
    \hat X
    &\to&
    A
    \\
    \downarrow^\simeq
    \\
    X
  }
$$
([[anafunctor|ana-morphisms]]) instead of longer sequences of zig-zags. 

In such a case it makes sense to address such a span as a [[cocycle]] on $X$ with coefficients in $A$ and to regard

$$
  H(X,A) := Ho(C)(X,A)
$$
as the **cohomology** of $X$ with coefficients in $A$.
From the point of view of generalized [[sheaf cohomology]] this can be understood by recognizing the replacement object $\hat X$ appearing here as a [[descent and codescent|codescent object]].

#Literature#

The fundamental ideas and facts are given in

* Kenneth S. Brown, _Abstract Homotopy Theory and Generalized Sheaf Cohomolohgy_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458 ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Abstract%20homotopy%20theory%20and%20generalized%20sheaf%20cohomology.pdf))

This develops the theory of localization in _categories of fibrant objects_ and then applies it to cohomology with coefficients in sheaves with values in combinatorial spectra.

Homotopical cohomology theory in the context of the [[homotopy theory]] of simplicial presheaves (presheaves with values in simplcial sets) has been much developed by Jardine. For instance

* J. Jardine, _Cocycle categories_ ([arXiv](http://arxiv.org/abs/math.AT/0605198))