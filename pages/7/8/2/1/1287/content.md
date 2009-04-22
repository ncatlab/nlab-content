#Definitions and characterizations#

A __local system__ is a locally constant [[sheaf]] on a topological space $X$ (or manifold, analytic manifold, or algebraic variety) whose stalk is a finite-dimensional vector space. On a connected topological space this is the same as a sheaf of sections of a finite-dimensional vector space equipped with flat connection; and it also corresponds to the representations of the [[fundamental group]] $\pi_1(X,x_0)$ in the typical stalk. On an analytic manifold or a variety, there is an equivalence between the category of non-singular coherent $D_X$-[[D-module|modules]] and local systems on $X$.

+-- {: .query}

  [[Urs Schreiber|Urs]]: I am hoping that maybe David Speyer, whose expositional blog entry is linked to below, or maybe somebody else would enjoy filling in some material here.

 [[Bruce Bartlett|Bruce]]: Could it perhaps be "On a  topological space (why do we need _connected_?) this is the same as a sheaf of _flat_ sections of a finite-dimensional vector _bundle_ equipped with flat connection;". I guess by "flat connection" in this general topological context we would mean simply a functor from the homotopy groupoid to the category of vector spaces?

[[Zoran Škoda]]: connected because otherwise you do not have 
even the same dimension of the typical stalk of teh lcoally constant sheaf. Maybe there is a fancy wording with groupoids avoiding this, but when you have a representation on a single space, you need connectedness. 

[[Ronnie Brown]] I do not have time to write more tonight but mention that there is a section of the paper 

* (with P.J.HIGGINS), "The classifying space of a crossed
complex",   Math. Proc. Camb. Phil. Soc. 110 (1991) 95--120.

on local systems, where a module over the fundamental groupoid of a space is regarded as a special case of a crossed complex. This seems convenient for the singular theories but has not been developed in a Cech setting. The homotopy classification theorem 

$$ [X, \mathcal{B}C] \cong [\Pi X_* ,C] $$

where $X_*$ is the skeletal filtration of the CW-complex $X$, $C$ is a crossed complex, and $\mathcal{B}C$ is the classifying space of $C$,  thus includes the local coefficient version of the classical Eilenberg-Mac Lane theory. 



=--

#Examples#

...

#Related entries#

* [[D-module]]

* [[abelian sheaf cohomology]]

#References#

There is a starting thread (still little info) at

* David Speyer: _Three ways of looking at a local system_

  * [Introduction and connection to cohomology theories](http://sbseminar.wordpress.com/2009/04/20/three-ways-of-looking-at-a-local-system-introduction-and-connection-to-cohomology-theories/)

A categorification of local systems to (a bit nontrivial) notion of locally constant stacks is given in 

* P. Polesselo, I. Waschkies, Higher monodromy, Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150;
[arXiv](http://arxiv.org/abs/math/0407507)

There is an another direction of categorifications of local systems (where roughly speaking the base is categorified) considered by M. Hopkins (unpublished). 