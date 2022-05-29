
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Contex
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

One can view the concept of a [[morphism]] or arrow in a [[category]] as an extreme abstraction of the concept of a spatial trajectory. It therefore comes with no surprise that (notions of) paths stemming from various conceptualizations of 'space' like e.g. [[quivers]] or [[topological spaces]] arrange themselves in appropriate categories thereby giving rise to several _different notions_ of **path category**.

## Free category on a directed graph

There is a [[forgetful functor]] from [[small category|small]] [[strict category|strict]] [[categories]] to [[quivers]]. This forgetful functor has a [[left adjoint]], giving the **[[free category]]** or **path category** of a quiver, whose [[objects]] are the vertices of the quiver.  The [[morphisms]] from $a$ to $b$ in this free category are *not* merely the arrows from $a$ to $b$ in the quiver but instead are [[lists]] of the form $(a_n,f_n,a_{n-1},\ldots,a_{1},f_1,a_0)$ where $n \geq 0$ is a [[natural number]], $a_0,a_1,\ldots,a_n$ are vertices of the graph, $a = a_0$, $b = a_n$,  and for all $0 \lt i \leq n$, $f_i\colon a_{i-1} \to a_i$ is an edge from $a_{i-1}$ to $a_i$.  The [[composition]] is given by the [[concatenation]] 
$$(a_n,f_n,a_{n-1},\ldots,a_{1},f_1,a_0)\circ (b_m,g_m,a_{m-1},\ldots,b_{1},g_1,b_0) := (a_n,f_n,a_{n-1},\ldots,a_{1},f_1,a_0= b_m,g_m,a_{m-1},\ldots,b_{1},g_1,b_0)$$ 
whenever $a_0 = b_m$, and the [[target]] and [[source]] maps are given by $s(a_n,f_n,a_{n-1},\ldots,a_{1},f_1,a_0)=a_0$ and $t(a_n,f_n,a_{n-1},\ldots,a_{1},f_1,a_0) = a_n$. One informally writes $f$ for the morphism $(b,f,a)\colon a \to b$ in the free category and the [[identity morphism|identities]] of the free category are $id_a = (a,a)$; thus 
$$ f_n \circ f_{n-1} \circ \ldots \circ f_1 = (t(f_n),f_n,t(f_{n-1}),\ldots,t(f_1),f_1,s(f_1))\quad .$$

### Remark

With free objects, one is often primarily interested in taking quotients whence a free category over a graph is usually a somewhat auxiliary gadget its main interest lying in the role it plays in defining [[category of fractions|categories of fractions]] (cf. [[Gabriel-Zisman]] 1967 pp.1,6; probably the original source of the path category in this sense).

But similar techniques apply to various notions of graphs or more restricted classes of categories with forgetful functors to graphs permitting to syntactically generate various notions of free categories with extra structure and in some of these cases it occurs that the corresponding free category (of paths) is indeed interesting in itself e.g. the [[free topos]] arises this way and the syntactic derivations of context free grammars arrange themselves into such categories of paths as explored in Walters ([1989a](#Walters1),[1989b](#Walters2)) or Latch ([1991](#Latch)).

## Path category of a space

Given a [[topological space]] $X$ (or some other kind of [[space]] with a notion of maps from [[intervals]] into it), there are various ways to obtain a [[small category|small]] [[strict category|strict]] [[category]] whose objects are the points of $X$ and whose morphisms are [[paths]] in $X$. This is also often called a _path category_.

* In particular, for every topological space there is its [[fundamental groupoid]] whose morphisms are [[homotopy]] classes of paths in $X$.

* If $X$ is a [[directed space]] there is a notion of path category called the [[fundamental category]] of $X$.

* When $X$ is a [[smooth space]], there is a notion of path category where less than homotopy of paths is divided out: just _thin_ homotopy. This yields a notion of [[path groupoid]]. 

* If _parameterized_ paths are used, there is a way to get a category of paths without dividing out any equivalence relation: this is the [[Moore path category]].


## Arrow category

Given a [[category]] $X$, the [[functor category]] $[I,X]$ for $I$ the [[interval category]] might be called a "directed path category of $X$" (similar to [[path space]]). However, this functor category is referred to instead as the [[arrow category]] of $X$ and sometimes even denoted $Arr(X)$.

## Related concepts

* [[concatenation]]

* [[free groupoid]]

* [[free diagram]]

* [[free monoid]], [[free operad]]

* [[free topos]]

## References

The [[free category]] on a graph has a section in

* [[Francis Borceux]], _Handbook of categorical Algebra vol. 1_ , Cambridge UP 1994.

or in

* {#MacLane} [[Saunders MacLane]], _Categories for the Working Mathematician_ , Springer 1998.

The following is another source for this, even an open source:

* {#BarrWells}[[Michael Barr]] and [[Charles Wells]], _Category Theory for Computing Science_ [PDF](http://www.math.mcgill.ca/triples/Barr-Wells-ctcs.pdf)

The path categories of context free grammars are explored in

* {#Latch} Dana Latch, _The connection between the fundamental groupoid and a unification algorithm for syntactil algebras (extended abstract)_ , Cah. Top. G&#233;om. Diff. Cat. **XXXII** (1991).  ([link](http://www.numdam.org/item?id=CTGDC_1991__32_3_203_0))

* {#Walters1} [[Bob Walters]], _The free category with products on a multigraph_ , JPAA **62** (1989). ([link](http://www.sciencedirect.com/science/article/pii/0022404989901527))

* {#Walters2} [[Bob Walters]], _A note on context-free languages_ , JPAA **62** (1989). ([link](http://www.sciencedirect.com/science/article/pii/0022404989901515))

Since the perspective on categories as 'graphs with operations' is closely related to their 'logico-deductive' side, it figures prominently in the work of [[Jim Lambek]] and [[Phil Scott]] (cf. the references at [[free topos]]).

[[!redirects path category]]
[[!redirects path categories]]

