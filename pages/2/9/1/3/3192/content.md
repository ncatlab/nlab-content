# Contents
* automatic table of contents goes here
{:toc}


## Definition

A continuous linear operator $F:B_1\to B_2$ between [[Banach spaces]] is **Fredholm** if it has finite dimensional [[kernel]] and finite dimensional [[cokernel]]. It follows that its image (range) is closed. The difference between the dimensions of the kernel and the cokernel is called the **index** of the Fredholm operator

$$
ind F = dim ker F - dim coker F = dim ker F - codim im F
$$


## Properties

* A **characterization** : a bounded linear operator $F:B_1\to B_2$ between Banach spaces is Fredholm iff it there is an operator $T:B_2\to B_1$ which is its inverse up to a [[compact operator]], i.e. $F T - Id_{B_2}$ and $T F - Id_{B_1}$ are compact operators. 

* [[elliptic operator|Elliptic operators]] on compact manifolds are naturally Fredholm, when understood between the appropriate [[Sobolev spaces]].

* The subspace $Fred(B_1,B_2)\subset B(B_1,B_2)$ of Fredholm operators in the space of bounded linear operators with the norm topology is open. 

  In other words, given a Fredholm operator $F$, there exists $\epsilon\gt 0$ such that every bounded linear operator $G$ satisfying $\| G-F\|\lt \epsilon$ is Fredholm. Fredholm operators on a fixed separable Hilbert space $H = B_1 = B_2$ form a [[semigroup]] with respect to the composition and the index is a morphism of semigroups: $ind F G = ind F + ind G$. 

* The space $Fred$ of all Fredholm operators is a model for the classiying space of degree-0 [[topological K-theory]].


## Generalizations

Fredholm operators generalize to Fredholm complexes. A finite [[chain complex]]

$$
0 \to C_0 \stackrel{d_0}\to C_1\stackrel{d_1}\to C_2 \ldots C_n\to 0
$$

of [[Banach space]]s and bounded operators is said to be a **Fredholm complex** if the images $d_i$ are closed and the [[chain homology]] of the complex is finite dimensional. The [[Euler characteristic]] (the alternative sum of the dimensions of the homology groups) is then called the __index__ of the Fredholm complex. Each Fredholm operator can be considered as a Fredholm complex concentrated at zero. Each Fredholm complex produces a Fredholm operator from the sum of the even- to the sum of the odd-numbered spaces in the complex. 

One can consider *Fredholm almost complexes*, where $d_i \circ d_{i-1}$ is not zero but the image of that operator is compact. Out of every Fredholm almost complex one can make a complex by correcting the differentials by compact perturbation terms. [[elliptic complex|Elliptic complexes]] give examples of Fredholm complexes. 


## References

* [wikipedia:Fredholm operator](http://en.wikipedia.org/wiki/Fredholm_operator)

* A. S. Mishchenko, &#1042;&#1077;&#1082;&#1090;&#1086;&#1088;&#1085;&#1099;&#1077; &#1088;&#1072;&#1089;&#1089;&#1083;&#1086;&#1077;&#1085;&#1080;&#1103; &#1080; &#1080;&#1093; &#1087;&#1088;&#1080;&#1084;&#1077;&#1085;&#1077;&#1085;&#1080;&#1103; (Vector bundles and their applications), Nauka, Moscow, 1984. 208 pp. MR87f:55010  

* S. Rempel, B-W. Schulze, _Index theory of elliptic boundary problems_, Akademie--Verlag, Berlin, 1982.

* Lars H&#246;rmander, _The analysis of linear partial differential operators. III. Pseudo-differential operators_, 1994, reprinted 2007. 

* Pietro Aiena, _Fredholm and local spectral theory, with applications to multipliers_, [book page](http://www.springer.com/mathematics/analysis/book/978-1-4020-1830-5)

* Otgonbayar Uuye, _A simple proof of the Fredholm Alternative_, [arxiv/1011.2933](http://arxiv.org/abs/1011.2933)

[[!redirects Fredholm complex]]