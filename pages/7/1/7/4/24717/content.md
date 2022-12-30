
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Classically, models of weak $n$-categories comprise sets of cells in dimension 0 up to $n$. This is also called the globularity condition. Geometrically, it corresponds to cells having a globular shape
\begin{imagefromfile}
"file_name": "Glob_Shape.jpg",
"width": 300
\end{imagefromfile}

On the other hand, non-globular structures exist in higher category theory: for instance, $n$-fold categories, defined by iterated internalization
\[
Cat^{0}=Set,\qquad\qquad Cat^{n}=Cat(Cat^{n-1})\;.
\]
The category $n\text{-}Cat$ of strict $n$-categories is defined by iterated enrichment:

$$
0\text{-}Cat=Set,\qquad\qquad n\text{-}Cat=((n-1)\text{-}Cat,\times)\text{-}Cat\;.
$$
There is an embedding
$$
n\text{-}Cat\hookrightarrow Cat^{n}
$$
such that a strict $n$-category is an $n$-fold category in which certain substructures are discrete (that is, sets).
This discreteness condition is precisely the globularity condition and the sets underlying these discrete substructures are the sets of cells in the strict $n$-category.


For instance, in the case $n=2$, strict 2-categories are double categories in which the category of objects and vertical arrows is discrete. In pictures:
\begin{imagefromfile}
"file_name": "2-Cat.jpg",
"width": 800
\end{imagefromfile}
We see that the picture on the right becomes the one on the left when all vertical morphisms are identities. 


In the weakly globular approach to higher categories, the cells in each dimension $k$ ($0\leq k\leq n$) instead of forming a set, have a higher categorical structure which is homotopically discrete, that is only equivalent (in higher categorical sense) to a set. This condition, called weak globularity condition, is a new paradigm to weaken higher categorical structures and allows to use rigid structures, namely $n$-fold categories, to model weak $n$-categories. There are strict embeddings
$$
n\text{-} Cat \hookrightarrow Cat_{wg}^{n} \hookrightarrow Cat^{n}
$$
so that the category $Cat_{wg}^{n}$ of weakly globular $n$-fold categories is intermediate between strict $n$-categories and $n$-fold categories.


In the case $n=2$, a weakly globular double category $X$ is a double category satisfying two conditions: 
the first is the weak globularity condition, stating that the category $X_0$ of objects and vertical arrows is equivalent to a discrete category, that is it is an equivalence relation. The set $pX$ of connected components of $X_0$ plays the role of 'set of objects' in the weak structure. We therefore need to define a composition of horizontal arrows whose source and target are in the same vertical connected component




## Homotopically discrete n-fold categories

## References

* {#Paoli19a} [[Simona Paoli]], *Weakly globular $N$-fold categories as a model of weak $N$-categories*, in: *Simplicial Methods for Higher Categories*, Algebra and Applications **26** Springer (2019)  &lbrack;[doi:10.1007/978-3-030-05674-2_12](https://doi.org/10.1007/978-3-030-05674-2_12)&rbrack;

* {#Paoli19} [[Simona Paoli]], _Simplicial Methods for Higher Categories -- Segal-type Models of Weak $n$-Categories_, Springer (2019)  &lbrack;[doi:10.1007/978-3-030-05674-2](https://doi.org/10.1007/978-3-030-05674-2), [toc pdf](https://link.springer.com/content/pdf/bfm%3A978-3-030-05674-2%2F1.pdf)&rbrack;

[[!redirects weakly globular n-fold categories]]

