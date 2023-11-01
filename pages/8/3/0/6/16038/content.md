
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Idea

Let $K$ be the strict [[2-category]] [[Cat]] and $C$ a [[category]] in $K$. Then we can identify a [[monad]] on $C$ with an [[endofunctor]] $T \colon C\to C$ (a [[monoid]] in the [[endofunctor category]] $K(C,C)$). We recall that for any [[object]] $c$ of $C$, we obtain a certain sort of [[resolution]] of $c$. Note that the canonical resolution is not a resolution in the sense of the above cited nLab page because it is not necessarily acyclic or [[contractible]] in the relevant sense. In other words, it does not always have trivial [[cohomology]], especially since our category may not even be equipped with such a notion. 

##Definitions

The _canonical resolution_ of $c$ in $C$ with respect to a [[monad]] $T \colon C\to C$ is a [[augmented simplicial set|coaugmented]] [[simplicial object|cosimplicial object]] $CanRes_T:\Delta_+\to C$ such that $CanRes_T([-1])=c$ and $CanRes_T([n])=T^{n+1}c$ for each $n\geq 0$. It has [[coface]] [[morphisms]] $T^{n}c\to T^{n+1}c$ given by the unit map of $T$, and codegeneracies given by the monoid structure $T T c\to T c$. 

###Monadic Cohomology
{#monadiccohomology}

Given a suitable functor $E:C\to A$, for $A$ an [[additive category]], we can define the [[monadic cohomology]] of an object $c$ to be the [[cohomology]] of the [[cochain complex]] associated to the composition of [[functors]] $E\circ CanRes_T:\Delta_+\to A.$ This has been introduced by Godement who called monad and the resolution from it the standard construction (thus, standard resolution is a term which is still used). By suitably dualizing, we can define _comonadic homology_. 

###Resolution of a $T$-algebra

Suppose that $c$ is an object of $C$ and also an [[module over a monad|algebra]] for $T$. Thus there is a [[morphism]] $T c\to c$ satisfying certain properties. In particular, this map provides an extra codegeneracy which defines an [[augmented simplicial set|augmented]] [[simplicial object]] living inside of the canonical resolution of $c$. This simplicial object is frequently referred to as the [[bar construction]] of $c$. 

Note that we can consider this internal [[bar construction]] to also be the canonical resolution associated to the induced [[comonad]] on the [[Eilenberg-Moore category]] of algebras over $T$. 

This [[bar construction]] can also be obtained by precomposing $CanRes_T$ with the functor that includes $\Delta^{op}_+\hookrightarrow \Delta$ as the subcategory whose morphisms preserve the minimal and maximal elements of finite totally ordered sets. 

## Examples

### The bar resolution for abelian groups

There is a monad on [[Set]], the category of sets, comprising the [[free abelian group]] functor $F \colon Set\to Ab$ and the [[forgetful functor]] $U \colon Ab\to Set$. The [[Eilenberg-Moore category|category of algebras]] of this monad is precisely the category of [[abelian groups]] (in other words, the [[free abelian group]] functor $F$ is [[monadic]]). 

Thus we may produce the cosimplicial canonical resolution of any set $X$. If $X$ supports (at least one) abelian group structure, then we can add a codegeneracy to the canonical resolution which defines the usual [[bar construction]] on $X$ with that particular abelian group structure.  

## Related concepts

* [[homological resolution]]

* [[monadic cohomology]]

* [[simplicial resolution]]

* [[bar and cobar construction]]


## References

The original articles:

* {#Godement58} [[Roger Godement]], Appendix of: *Topologie algébrique et theorie des faisceaux*, Actualités Sci. Ind. **1252**, Hermann, Paris (1958) &lbrack;[webpage](https://www.editions-hermann.fr/livre/topologie-algebrique-et-theorie-des-faisceaux-roger-godement), [[Godement-TopologieAlgebrique.pdf:file]]&rbrack;

* {#Huber61} [[Peter J. Huber]], *Homotopy theory in general categories*, Mathematische Annalen **144** (1961) 361–385 &lbrack;[doi:10.1007/BF01396534](https://doi.org/10.1007/BF01396534)&rbrack;

Further discussion:

* [[Michael Barr]], [[Jon Beck]], _Homology and Standard Constructions_, in _[[Seminar on Triples and Categorical Homology Theory]]_, Lecture Notes in Maths. **80**, Springer (1969), Reprints in Theory and Applications of Categories __18__ (2008) 186-248 &lbrack;[TAC:18](http://www.tac.mta.ca/tac/reprints/articles/18/tr18abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/18/tr18.pdf)&rbrack;

*  {#Duskin75} [[John Duskin]], *Simplicial methods and the interpretation of "triple" cohomology"*  Memoirs  of the AMS **163**, Amer. Math. Soc. (1975) &lbrack;[ISBN:978-1-4704-0645-5](https://bookstore.ams.org/memo-3-163)&rbrack;

See also:


* [[Michael Barr]], *Cartan-Eilenberg cohomology and triples*, J. Pure Applied Algebra **112** 3 (1996) 219–238 \[<a href="https://doi.org/10.1016/0022-4049(95)00138-7">doi:10.1016/0022-4049(95)00138-7</a>, [pdf](https://www.math.mcgill.ca/barr/papers/coho.pdf), [[Barr-CECohomology.pdf:file]]\]

* [[Michael Barr]], *Algebraic cohomology: the early days*, in *Galois Theory, Hopf Algebras, and Semiabelian Categories*, Fields Institute Communications **43** (2004) 1–26 \[<a href="https://doi.org/10.1090/fic/043">doi:10.1090/fic/043</a>, [pdf](https://www.math.mcgill.ca/barr/papers/algcohom.pdf), [[Barr-AlgebraicCohomology.pdf:file]]\]


Textbook account:

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_


[[!redirects canonical resolutions]]

[[!redirects standard resolution]]
[[!redirects standard resolutions]]
[[!redirects standard construction]]

[[!redirects cotriple homology]]
[[!redirects triple cohomology]]
