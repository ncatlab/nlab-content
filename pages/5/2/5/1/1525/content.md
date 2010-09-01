
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

There are several concepts often called a **path category**.

#Contents#
* table of contents
{:toc}


## Free category on a directed graph

There is a [[forgetful functor]] from [[small categories]] to [[quiver]]s, (i.e. [[directed graph]]s allowing more than one edge from $a$ to $b$). This forgetful functor has a left adjoint, the **free category** or **path category** of a quiver, which has the same objects (vertices) but much more arrows. The morphisms from $a$ to $b$ in this free category are the sequences of the form $(a_n,f_n,a_{n-1},\ldots,a_{2},f_1,a_0)$ where $n\geq 0$, $a_0,a_1,\ldots, a_n$ are vertices of the graph, $a=a_0$, $b=a_n$, for all $0\lt i \leq n$, $f_i:a_{i-1}\to a_i$ is an edge from $a_{i-1}$ to $a_i$.  The composition is given by the concatenation 

$$(a_n,f_n,a_{n-1},\ldots,a_{2},f_1,a_0)\circ (b_m,g_m,a_{m-1},\ldots,b_{2},g_1,b_0) := (a_n,f_n,a_{n-1},\ldots,a_{2},f_1,a_0= b_m,g_m,a_{m-1},\ldots,b_{2},g_1,b_0)$$ 

whenever $a_0 = b_m$, and the target and source maps are given by $s(a_n,f_n,a_{n-1},\ldots,a_{2},f_1,a_0)=a_0$ and $t(a_n,f_n,a_{n-1},\ldots,a_{2},f_1,a_0) = a_n$. One informally writes $f$ for the morphism $(b,f,a):a \to b$ in the free category and the identities of the free category are $id_a = (a,a)$; thus $f_n\circ f_{n-1}\circ\ldots\circ f_1 = (t(f_n),f_n,t(f_{n-1}),\ldots,t(f_1),f_1,s(f_1))$. The standard reference is [[Gabriel–Zisman]].


## Path category of a space

Given a [[topological space]] $X$ (or some other kind of [[space]] with a notion of maps from [[intervals]] into it), there are various ways to obtain a category whose collection of objects is $X$, and whose morphisms are images of intervals in $X$, i.e. paths in $X$. This is also often called a _path category_. 

* In particular, for every topological space there is its [[fundamental groupoid]] whose morphisms are [[homotopy]] classes of images of intervals in $X$.

* If $X$ is a [[directed space]] there is a notion of path category called the [[fundamental category]] of $X$.

* When $X$ is a [[smooth space]], there is a notion of path category where less than homotopy of paths is divided out: just _thin_ homotopy. This yields a notion of [[path groupoid]]. 

* If _parameterized_ paths are used, there is a way to get a category of paths without dividing out any equivalence relation: this is the [[Moore path category]].


## Arrow category

Given a [[category]] $X$, the [[functor category]] $[I,X]$ for $I$ the [[interval category]] might be called a "directed path category of $X$" (similar to [[path space]]). However, this functor category is referred to instead as the [[arrow category]] of $X$ and sometimes even denoted $Arr(X)$.


[[!redirects free category]]
[[!redirects free categories]]

[[!redirects path categories]]