
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A *Bénabou cosmos* is a [[monoidal category]] $\mathcal{V}$ with good properties that make it well-suited for $\mathcal{V}$-[[enriched category theory]]. (There are variants of this idea, see at *[[cosmos]]* for more).

The archetypical Bénabou cosmos is the category [[Set]] of all sets, equipped with its [[Cartesian product]]-monoidal structure; and $Set$-[[enriched category theory]] is the ordinary theory of [[locally small categories]], whose [[hom-sets]] are [[sets]].

The point of the notion of Bénabou cosmoi is to allow more general [[hom-objects]] than just [[sets]], while imposing enough conditions on the category $\mathcal{V}$ which these form in order that most standard definitions and proofs of plain [[category theory]] (e.g. properties of [[categories of presheaves]]) generalize to $\mathcal{V}$-enriched category theory (e.g. concerning [[enriched presheaves]]).


## Definition

\begin{definition}\label{BenabouCosmosAccordingToStreet}
A [[Bénabou cosmos]]  is ([Street 74, p. 1](#Street74)) a 

* [[complete category|complete]] and [[cocomplete category|cocomplete]] (hence [[bicomplete category|bicomplete]]) 

* [[closed monoidal category|closed]] 

* [[symmetric monoidal category|symmetric]]

* [[monoidal category|monoidal]]

[[category]].  
\end{definition}

\begin{remark}
There is a generalization of Def. \ref{BenabouCosmosAccordingToStreet} to the context of enriched [[indexed categories]] ([Shulman 2013](#Shulman13)).  While Def. \ref{BenabouCosmosAccordingToStreet} is not "[[elementary topos|elementary]]" (as it involves infinitary (non-[[finite limit|finite]]) [[limits]] and [[colimits]]), the indexed version *is* elementary, as the infinitary structure is folded into the indexing base category.  The notion of [[Bénabou cosmoi]] is recovered as particular indexed cosmoi over [[Set]].
\end{remark}


## Examples
 {#Examples}

\begin{example}\label{TopoiAreCosmoi}
**([[topoi]] are [[cosmoi]])**
\linebreak
  Every [[Grothendieck topos]] is a Bénabou cosmos, where the [[symmetric monoidal category|symmetric monoidal]] structure is [[cartesian monoidal category|cartesian]]. Examples in this class include:

* The archetypical such example is the category [[Set]] of [[set]]. $Set$-[[enriched categories]] are ordinary [[locally small categories]].

* The category [[sSet]] of [[simplicial sets]] is the [[presheaf topos]] over the [[simplex category]], whose cartesian monoidal structure is discussed at *[[products of simplicial sets]]*. $sSet$-[[enriched categories]] are often called *[[simplicial categories]]* (though see there for ambiguity in this terminology). They serve as foundation for much of [[homotopy theory]], see at *[[simplicial homotopy theory]]* and *[[simplicial model categories]]* for more. 

\end{example}

## Related concepts

* [[cosmos]]

* [[infinity-cosmos|$\infty$-cosmos]]


## References

Apparently there is no explicit written account by [[Jean Bénabou]] on the notion, but one finds it recounted in [Street 74, p. 1](#Street74):

> to J. Benabou the word means "bicomplete symmetric monoidal category", such categories $\mathcal{V}$ being rich enough so that the theory of categories enriched in  $\mathcal{V}$ develops to a large extent just as the theory of ordinary categories.

* {#Street74} [[Ross Street]],  _Elementary cosmoi I.  *Category Seminar*. Springer, Berlin, Heidelberg, 1974. ([doi:10.1007%2FBFb0063103](https://link.springer.com/chapter/10.1007%2FBFb0063103))

See also:

* Wikipedia, *<a href="https://fr.wikipedia.org/wiki/Cosmos_(th%C3%A9orie_des_cat%C3%A9gories)">Cosmos_(théorie_des_catégories)</a>*

The [[indexed category|indexed]] generalization:

* {#Shulman13} [[Mike Shulman]], *Enriched indexed categories*, Theory and Applications of Categories, **28** 21 (2013) 616-695 ([tac:28-21](http://www.tac.mta.ca/tac/volumes/28/21/28-21abs.html)) 

[[!redirects Bénabou cosmoi]]

[[!redirects Benabou cosmos]]
[[!redirects Benabou cosmoi]]

[[!redirects cosmos for enriched category theory]]
[[!redirects cosmoi for enriched category theory]]
