# Contents
* this block creates the table of contents, leave as is
{: toc}

## Idea

Diagrammatic sets are [[presheaf|presheaves]] over the [[atom category]]. There are kind of geomtrical [[polygraph|polygraphs]], and can serve as a model for [[higher category theory|higher categories]].


## Definition 

\begin{definition}
**(diagrammatic set)**\linebreak
A **diagrammatic set** $X$ is a presheaf over $\odot$, the [[atom category|category of atoms]] and cartesian maps. Diagrammatic sets and [[natural transformations]] form the category $\odot\mathbf{Set}$
\end{definition}


## Properties

Let $\mathbf{RDCpx}$ be the category of [[regular directed complex|regular directed complexes]] and cartesian maps, we have a full subcategory inclusion $i \colon \odot \hookrightarrow \mathbf{RDCpx}$ which defines a functor
$$
    i^* \colon \mathbf{RDCpx} \to \odot\mathbb{Set}
$$
that sends a regular directed complex $P$ to the presheaf $\mathbf{RDCpx}(i^*(-), P)$. This is the [[restricted Yoneda embedding]]. 

\begin{proposition}
The [[Yoneda embedding]] factors as
$$
    \odot \hookrightarrow \mathbf{RDCpx} \hookrightarrow \odot\mathbf{Set},
$$
i.e. the functor $i$ is a [[dense functor|dense]]. 
\end{proposition}


## Examples

(...)


## References

The origin of the name is in:

* Kapranov, M. M., and Voevodsky, V. A.. _$\infty $-groupoids and homotopy types._ Cahiers de Topologie et Géométrie Différentielle Catégoriques 32.1 (1991) ([link](http://eudml.org/doc/91469))

An older treatment of diagrammatic sets:

* [[Amar Hadzihasanovic]], _Diagrammatic sets and rewriting in weak higher categories_, ([arXiv:2007.14505](https://arxiv.org/abs/2007.14505))

For an updated version:
 
* {#ChanavatHadzihasanovic2024} Clémence Chanavat, Amar Hadzihasanovic, _Diagrammatic sets as a model of homotopy types_, 2024 ([arXiv:2407.06285](https://arxiv.org/abs/2407.06285v1))



[[!redirects diagrammatic sets]]