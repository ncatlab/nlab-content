
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

Given a [[simplicial group]] $\mathcal{G} \in Groups(sSet)$, hence a [[group object]] [[internalization|internal]] to [[SimplicialSets]], a [[group action]] of $\mathcal{G}$ on a [[simplicial set]] $X$ is a $\mathcal{G}$-[[action object]] [[internalization|internal]] to [[SimplicialSets]], hence a morphism of simplicial sets of the form

$$  
  \mathcal{G} \times X
  \xrightarrow{\;\; \rho \;\;}
  X
$$

satisfying the action property.

The [[category]] of simplicial $\mathcal{G}$-action may be understood as the [[sSet]]-[[enriched functor|enriched]] [[functor category]] from the one-object [[sSet-category]] $\mathbf{B}\mathcal{G}$ to [[sSet]]:

\[
  \label{CategoryOfSimplicialGroupActions}
  \mathcal{G}Actions(sSet)
  \;\;
  \simeq
  \;\;
  sSetCat
  \big(
    \mathbf{B}\mathcal{G},
    \,,
    sSet
  \big)
\]

## Properties

### Model category structure

\begin{proposition}
**([[model structure on simplicial group actions]])** \linebreak
  There is a [[model category]]-structure on simplicial group actions (eq:CategoryOfSimplicialGroupActions) whose [[weak equivalences]] and [[fibrations]] are those in the underlying [[classical model structure on simplicial sets]], hence are the [[simplicial weak equivalences]] and [[Kan fibrations]] of the underlying simplicial sets.
\end{proposition}

([DDK 80, Prop. 2.2. (ii)](#DDK80), $\;$ [Guillou, Prop. 5.3](#Guillou), $\;$ [Goerss & Jardine 09, V Lem. 2.4](#GoerssJardine09)).


## Related concepts

* [[Borel model structure]]

* [[G-set]], [[topological G-space]]

* [[∞-action]]

## References

* {#DDK80} [[Emmanuel Dror]], [[William Dwyer]], [[Daniel Kan]], _Equivariant maps which are self homotopy equivalences_, Proc. Amer. Math. Soc. 80 (1980), no. 4, 670&#8211;672 ([jstor:2043448](http://www.jstor.org/stable/2043448))

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section V.2 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))

* {#Guillou} [[Bert Guillou]], _A short note on models for equivariant homotopy theory_, 2006 ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf), [[GuillouModelsForEquivariantHomotopyTheory.pdf:file]])


[[!redirects simplicial group actions]]

