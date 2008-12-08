This is my personal sandbox, where I'll try to work out some stuff. If anything becomes interesting in the slightest, I hope to add a new page. Any editorial angels who wish to help add, correct, etc, please feel free.

##Discrete Smooth Spaces

I hope to adapt the definition of a Frolicher space to discrete/abstract space.

***

###Definition 2.2 (Frolicher) 

A Frolicher space is a triple $(X,C,F)$ where $X$ is a set, $C$ is a family of curves in $X$, i.e. a subset of $Map(R,X)$, and $F$ is a
family of functionals on $X$, i.e. a subset of $Map(X,R)$. 


The sets $C$ and $F$ have to satisfy the following compatibility condition: a curve $c: R\to X$ is in $C$ if and only if $fc\in C^\infty(R,R)$ for all functionals $f\in F$, and similarly a functional $f: X\to R$ is in
$F$ if and only if $fc\in C^\infty(R,R)$ for all curves $c: R\to X$.

***

I guess the first place to start is to define what I mean by a discrete space.

***

###Discrete Space

A discrete space is generated from a directed graph $G$ with nodes denoted by

$$e_i$$

and directed edges denoted by

$$e_{i,j}: e_i\to e_j.$$

The higher dimensional elements are generated via differential algebra.

$$e_i e_j = \delta_{i,j} e_i$$

Therefore,

$$d(e_i e_j) = (d e_i) e_j + e_i (d e_j) = \delta_{i,j} de_i$$

Multiplying by $e_i$ on the left and $e_j$ on the right, we have

$$e_i (de_j) e_j = (\delta_{i,j} - 1) e_i (de_i) e_j$$


####Doodles

In our paper, we began the discussion in the framework of directed graphs. I wonder if we could present it in the context of the nerve of a category? Before I can do that, I probably need to learn what a nerve of a category is.

What if we begin with a discrete graph $G$ and....

***

##Research Papers

[Discrete differential geometry on causal graphs](http://arxiv.org/abs/math-ph/0407005), with
Urs Schreiber (2004).

category: people