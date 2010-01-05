#Contents#
* automatic table of contents goes here
{:toc}

## Idea

**Geometric function theory** 
considers notions of higher generalized functions on higher generalized spaces (such as on [[groupoid]]s, on [[Lie groupoid|orbifolds]] and more generally on [[infinity-stack homotopically|infinity-stacks]]) such that all suitably generalized linear maps between the monoidal $\infty$-structures of functions on two spaces arise from a higher analog of plain matrix multiplication, namely from a _pull-tensor-push_ operation in the given $\infty$-context.

### Motivating toy example: matrices

The motivating toy example is that where all spaces in question are just _finite sets_ and functions are just maps from finite sets to a given [[ground field]]: for $X$ a finite set the collection of functions $C(X)$ on $X$ is canonically identified with the vector space spanned by the elements of $X$. Moreover, for two finite sets $X_1$ and $X_2$ functions on the [[product]] set $X_1 \times X_2$ are canonically identified with $|X_1| \times |X_2|$-matrices 
$$
  C(X_1 \times X_2) \simeq Mat(n= |X_1|, m = |X_2|)
  \,.
$$
The point is that from this perspective on matrices the action of a matrix on a vector is given by the pull-tensor-push operation of functions through a [[span]]

$$
  \array{
     && X_1 \times X_2
     \\
     & {}^{pr_1}\swarrow && \searrow^{pr_2}
     \\
     X_1
     &&&&
     X_2
  }
$$

Given $v \in C(X_1)$ and $M \in C(X_1 \times X_2)$ the matrix product $M \cdot v \in C(X_2)$ can be understood as

$$
  M \cdot v =  \int_{pr_2}(M \cdot (pr_1^* (v)))
  \,,
$$
where

* $pr_1^* : C(X_1) \to C(X_1 \times X_2)$ is the pullback of functions along the projection map $pr_1$;

* $M \cdot (\cdot)$ is the ordinary product of functions;

* $\int_{pr_2}$ is the push-forward of field-valued functions along $pr_2$, i.e. the operation which integrates (a finite sum in this toy example) a function on $X_1 \times X_2$ over $X_1$ to a function on $X_2$.


### Groupoidification 

A closely related situation is considered in the context of [[groupoidification]], where the aim is to encode not only the operation of matrix multiplication geometrically in the above sense, but also the very notion of a function itself. 

In [[groupoidification]] functions with values in fields are essentially replaced by functions with values in (finite) [[groupoid]]s, and the notion of [[groupoid cardinality]] is used to interpret such a gadget as a function with values in rational numbers. 

More precisely, [[groupoidification]] in the sense of [[John Baez]] can be understood as geometric function theory for the case that collections of geometric functions are modeled as [[over category|over categories]]. This is described in more detail at [[examples for geometric function objects]].

Related toy examples of the general pattern are [[group]] algebras regarded as [[category algebra|category algebras]] (see the end of that entry for the span-description of category algebras). 



### General $\infty$-categorical / homotopical setup 

In full generality the idea of _geometric function theory_ is to replace in the above toy example all finite sets with generalized higher spaces in the form of [[∞-stack]]s and to realize a useful notion of higher "functions" $C(X)$, such that $C(X)$ is a [[monoidal (∞,1)-category]] in a suitable sense and behaves as expected under [[homotopy pullback]] and push-forward operations.

The **main two conditions** that one wants to have in _geometric function theory_ are

1. for $X_1 \to Y \leftarrow X_2$ two generalized spaces sitting over a third one, we have an [[equivalence]] between the generalized functions on the [[pullback|fiber product]] $X_1 \times_Y X_2$ and the [[tensor product]] of functions on $X_1$ with functions on $X_2$ over functions on $Y$:
$$
  C(X_1 \times_Y X_2)
  \simeq
  C(X_1) \otimes_{C(Y)} C(X_2)
  \,,
$$
where all operations are in the 
suitable $\infty$-context (for instance the fiber product is a [[homotopy limit]]).

2. again for given $X_1 \to Y \leftarrow X_2$ the generalized functions on the (homotopy/$\infty$-)fiber product are supposed to induce via (homotopy/$\infty$-) pull-tensor-push operation through the [[span]] $X_1 \leftarrow X_1 \times_{Y} X_2 \to X_2$ all $C(Y)$-linear morphism between $C(X_1)$ and $C(X_2)$:
$$
  C(X_1 \times_Y X_2)
  \simeq
  Maps_{C(Y)}(C(X_1), C(X_2))
  \,.
$$

This is to be read as a vast generalization of ordinary matrix multiplication, to which it reduces in the case that all spaces here are finite sets and all functions are ordinary functions on finite sets with values in some field.  One step higher this gives [[Fourier-Mukai transformation|Fourier?Mukai transformations]] etc.


### Relation to Hochschild (co)homology 

A particularly interesting application of items 1) and 2) above is to the case where the pullback diagram of generalized spaces in question is simply

$$
  X \stackrel{Id \times Id}{\to}
  X
  \stackrel{Id \times Id}{\leftarrow}
  X
  \,.
$$

As discussed at [[span trace]] the [[homotopy pullback]] of this is the [[loop space object]] $\Lambda X$ of $X$. 

So in this case statement 2) relates

* generalized functions $C(\Lambda X)$ on the [[loop space]] of $X$

with

* the homotopy tensor product of $C(X)$ with itself over $C(X)\otimes C(X)$

$$
  C(\Lambda X) \simeq C(X) \otimes_{C(X) \otimes C(X)} C(X)
  \,.
$$

The expression on the right is known as the higher [[trace]] of the [[monoidal (∞,1)-category]] $C(X)$, which is the higher [[Hochschild homology]] of $C(X)$. (See next subsection for concrete realizations).


#### Realization in terms of derived $\infty$-stacks on the algebraic site

Aspects of geometric function theory have a long history in the context of [[sheaf|sheaves]] and [[stack|stacks]] over algebraic [[site]]s. The [[Fourier-Mukai transformation|Fourier?Mukai transform]] is a classical example of a pull-tensor-push operation in a context where the object $C(X)$ of generalized functions on a space $X$ is taken to be $D(X)$, the [[derived category]] of [[coherent sheaf|coherent sheaves]] on $X$.

A general proof of the above item 2 in the context of generalized functions modeled by the [[derived category]] $D(X)$ has been given in 

* B. To&#235;n and G. Vezzosi, _Homotopical Geometry I: Topos theory._, Adv.
Math. 193 (2005), no. 2, 257&#8211;372 ([arXiv](http://arxiv.org/abs/math/0207028)).

As any [[homotopy category]], the [[derived category]] $D(X)$ of [[coherent sheaf|coherent sheaves]] is naturally understood as the $1$-categorical shadow of a [[stable (∞,1)-category]]. In a suitable context of derived $\infty$-stacks there is for each such $\infty$-stack $X$ an $(\infty,1)$-category $QC(X)$ whose homotopy category is the ordinary derived category $D(X)$ of quasi-coherent sheaves on $X$.

In this context geometric function theory with functions $C(X)$ taken to be given by $QC(X)$ was discussed in

* David Ben-Zvi, John Francis, David Nadler, _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))

where the above two items appear as items 1) and 2) in [theorem 1.2, p. 4,5](http://arxiv.org/PS_cache/arxiv/pdf/0805/0805.0157v4.pdf#page=4)

A detailed entry on this is at

* [[geometric ∞-function theory]]


### Further examples

Further discussion of realizations of geometric function objects is at

* [[examples for geometric function objects]]

## Remarks 

Closely related to the spans appearing in geometric function theory is the notion of [[bi-brane]].

## Further references

[[David Ben-Zvi]] kindly wrote an expositional piece on geometric function theory for the $n$-Category Caf&#233; ([blog entry](http://golem.ph.utexas.edu/category/2009/01/benzvi_on_geometric_function_t.html)):

* David Ben-Zvi, [[BenZviGeometricFunctionTheory.pdf:file]] (Jan 2009).
