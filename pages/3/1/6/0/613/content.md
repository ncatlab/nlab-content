
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

* [[fundamental groupoid]], **fundamental ∞-groupoid**

* [[fundamental category]], [[fundamental (∞,1)-category]]


***

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The [[higher category theory|higher categorical]] version of the [[fundamental groupoid]] of a space.

The fundamental $\infty$-groupoid of a topological space $X$ is supposed to be the [[infinity-groupoid]] whose $k$-morphisms are $k$-dimensional paths in $X$. Concrete realizations depend on the model of [[infinity-category]] or [[omega-category]] chosen:

* In the context of $\infty$-groupoids modeled as [[Kan complex]]es, the fundamental $\infty$-groupoid is simply the [[simplicial set]] familiar as the _singular simplicial complex_ $S(X)$ of a space, where $S(X)^n = Top(\Delta^n, X)$
with $\Delta^n$ denoting the standard topological $n$-[[simplex]] (familiar from [[geometric realization]]).


* [[Ronnie Brown|Ronnie]] One can also take a cubical approach, and suggest that the "obvious" notion of $k$-dimensional path in $X$ is a map $I^n \to X$ where $I^n$ is the $n$-cube. The cubical singular complex $S^\square X$ has the nice properties of a  [[compositions in cubical sets]] including inverses and connections, as well as being a cubical [[Kan complex]]. All these properties are exploited in the work on [[higher homotopy van Kampen theorem]]s, using the fundamental homotopy omega-groupoid of a filtered space. 


* The definition of [[Trimble n-category]] has the concept of fundamental $n$-groupoid built right into it.

* (... Batanin's weak fundamental $\omega$-groupoid)

## Strict versions of higher homotopy groupoids

It is not so obvious how to define higher homotopy groupoids which  generalise the fundamental groupoid to higher dimensions. It is possible to say that all you need is the singular complex $SX$ of the topological space, and that this is some kind of weak infinity-category, since it is a [[Kan complex]]. But even this fact has further problems, since as is standard, the Kan extension condition is due to a property of the models, namely that there is a retraction from the simplex $\Delta^n$ to $\Lambda^{n-1}_i$, the union of all the faces of $\Delta^n$ except the $i$th. So one would also like to axiomatise the properties of these [[thin element|thin]] fillers of horns in $SX$. This would be interesting from the algebraic point of view because such a retraction gives in some sense one face of the simplex as a kind of composition of the other faces. Problems are that: the retraction described is not unique; and what are the axioms on composites of such retractions, i.e. on subdivisions of subdivisions? Maybe there are good answers! 

One of the properties one would like of a proposed infinity-groupoid $G$ for a space $X$ is what one might call the **dimension condition**: _the $r$-dimensional homotopy of $X$ is modelled in $r$-dimensional structure  of $G$_. An immediate problem is that every space has the weak homotopy type of the classifying space of some category $C$; so where is the $r$-dimensional homotopy of $X$ reflected in the chosen $C$? Replacing $C$ by some weak form of $n$-category does not obviously help matters. 

There is a strict homotopy 2-groupoid for a Hausdorff space defined by  Hardie, K. A.; Kamps, K. H.; Kieboom, R. W. (MR1785844) and this was later developed into a homotopy double groupoid by Kamps et al. There is no $n$-dimensional version of these ideas on offer. 

A strict cubical omega-groupoid $\rho X_*$ for a [[filtered space]] $X_*$ was defined by Brown and Higgins in 1981. Form the filtered cubical complex $R X_*$ which in dimension $n$ consists of  filtered maps $I^n_* \to X_*$ and take filter homotopy classes of these _relative to the vertices_. The proof that the compositions in $RX_*$ are inherited by $\rho X_*$ is one of the key points of the development. 

It turns out that $\rho X_*$ is equivalent in a clear sense to the crossed complex $\Pi X_*$ defined using relative homotopy groups by Blakers in 1948 (with other terminology) and that the homotopy types modelled by crossed complexes, or by the corresponding globular or cubical gadget, are restricted, essentially to the _linear_ homotopy types, with no quadratic information.  Nonetheless, it is well known in mathematics that linear approximations can be useful. 

Loday's paper of 1982 on _Spaces with finitely many homotopy groups_ introduced the  entirely new idea of a _cubical resolution_ of a space. Some details were completed by Richard Steiner. Loday also introduced the fundamental [[cat-n-group]] of an $n$-cube of spaces. In this way we get a model of a space $X$ by a multiple groupoid in which the $r$-dimensional homotopy of $X$ occurs in the right place in the model. Also you can calculate something with this model, and it has led to new algebraic constructions, such as a nonabelian tensor product of groups, with homotopical applications.  

These strict groupoid models do satisfy the dimension condition. 

There are now uses of models of $n$-types in areas of homological algebra. 



## Remarks

* The idea of some fundamental $\infty$-groupoid plays a crucial role in the [[homotopy hypothesis]].

+--{.query}
*[[Ronnie Brown|Ronnie]] The question remains: what is such a construction supposed to do? Ideas on this might lead to restrictions on or possibilities for the construction, and comparisons with known constructions. 

[[Urs Schreiber]]: I had meanwhile had a long private discussion with Ronnie about this by private email. This showed that more discussion here about the notion of fundamental $\infty$-groupoids in homotopy theory should eventually be given here.
=--


## References

* R. Brown and P.J. Higgins, Colimit theorems for relative homotopy groups, J. Pure Appl. Algebra 22 (1981) 11-41.

* Hardie, K. A.; Kamps, K. H.; Kieboom, A homotopy 2-groupoid of a Hausdorff space. Papers in honour of Bernhard Banaschewski (Cape Town, 1996). Appl. Categ. Structures 8 (2000), no. 1-2, 209--234. 

* J.-L. Loday, Spaces with finitely many homotopy groups,
J.Pure Appl.  Alg., 24 (1982) 179--202.

* R.Steiner, Resolutions of spaces by  $n$-cubes of fibrations, J. London Math. Soc.(2), 34, 169-176, 1986.

* J. M. Casas, G. Ellis, M. Ladra, T. Pirashvili, _Derived functors and the homology of $n$-types_, J. Algebra __256__, 583--598 (2002).

[[!redirects fundamental infinity-groupoids]]
[[!redirects fundamental ∞-groupoid]]
[[!redirects fundamental ∞-groupoids]]