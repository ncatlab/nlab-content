
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc} 

## Idea

The notion of *enriched groupoids* is the generalization to [[enriched category theory]] of the notion of *[[groupoids]]* from plain [[category theory]].

## Definition

Let $(\mathcal{V}, \times, \ast)$ be a *[[cartesian monoidal category]]* (serving as an [[base of enrichment]]), so that, in particular, 

* the [[tensor unit]] is a [[terminal object]] $\ast$,

* for each [[object]] $v \in \mathcal{V}$ there is a [[diagonal morphism]]

  $$
    \Delta_v \,\colon\, v \to v \times v
    \,.
  $$

A *$\mathcal{V}$-enriched groupoid is a $\mathcal{V}$-[[enriched category]] $\mathcal{C}$ equipped for $X, Y \,\in\, Obj(\mathcal{C})$ with [[morphisms]] (in $\mathcal{V}$) of the form

$$
  inv_{X,Y}
  \;\colon\;
  \mathcal{C}(X,Y)
  \longrightarrow
  \mathcal{C}(Y,X)
$$

which behave like assigning [[inverse morphisms]] in that the [[composition]] morphisms of $\mathcal{C}$ 

$$
  comp_{X, Y, Z}
  \;\colon\;
  \mathcal{C}(X,Y)
  \otimes
  \mathcal{C}(Y,Z)
  \longrightarrow
  \mathcal{C}(Y,Z)
$$

satisfy

$$
  comp_{Y,X,Y}
    \circ
  \big(
    inv_{X,Y} 
      \times 
    id_{\mathcal{C}(X,Y)}
  \big)
    \circ
  \Delta_{\mathcal{C}(X,Y)}
  \;\;=\;\;
  \mathcal{C}(X,Y)
  \overset{}{\longrightarrow}
  \ast
  \overset{id_Y}{\longrightarrow}
  \mathcal{C}(Y,Y)
$$

and


$$
  comp_{X,Y,X}
    \circ
  \big(
    id_{\mathcal{C}(X,Y)}
      \times 
    inv_{X,Y} 
  \big)
  \circ
  \Delta_{\mathcal{C}(X,Y)}
  \;\;=\;\;
  \mathcal{C}(X,Y)
  \overset{}{\longrightarrow}
  \ast
  \overset{id_Y}{\longrightarrow}
  \mathcal{C}(X,X)
  \,.
$$

## Examples

\begin{example}
  A [[Set]]-enriched groupoid is an ordinary [[groupoid]].
\end{example}

\begin{example}\label{SimplicialGroupoid}
  The [[sSet]]-enriched groupoids are traditionally  misnamed *[[simplicial groupoids]]* (following [Dwyer & Kan (1984)](simplicial+groupoid#DwyerKan84) and similar abuse for *[[simplicial category]]*), see there for more. More pedantically, $sSet$-enriched groupoids are only those [[sSet]]-[[internal groupoids]] whose set of objects is constant, cf. Exp. \ref{RelationToInternalGroupoids} below.

Moreover, [[fundamental infinity-groupoid|fundamental $\infty$-groupoids]] incarnated as [[sSet]]-[[enriched groupoids]] aka "Dwyer-Kan [[simplicial groupoids]]" are (mis-)named *[[Dwyer-Kan loop groupoids]]*.
\end{example}

\begin{example}
  A $\mathcal{V}$-enriched groupoid with a single object is equivalently the [[delooping groupoid]] of a [[group object]] [[internalization|internal]] to $\mathcal{V}$.

For instance, a one-object [[sSet]]-groupoid (Exp. \ref{SimplicialGroupoid}) is the [[delooping groupoid]] of a [[simplicial group]].
\end{example}

\begin{example}\label{RelationToInternalGroupoids}
  An [[internal groupoid]] in $\mathcal{V}$ is equivalently a $\mathcal{V}$-enriched groupoid if its $\mathcal{V}$-object of objects is in the image of the [[coproduct]]-[[preserved colimit|preserving]] [[functor]] $Set \to \mathcal{V}$ (using here the assumption that $\mathcal{V}$ is a [[Bénabou cosmos]], hence [[cocomplete category|cocomplete]], hence with all [[coproducts]]).
\end{example}

## Related concepts

* [[enriched category]]

* [[internal groupoid]], [[internal group]]

* [[groupoid object in an (∞,1)-category]]

## References

The notion of enriched groupoids is [[folklore]], originating in the special case of enrichment over [[sSet]], where it is traditionally discussed, going back to [Dwyer & Kan (1980)](simplicial+groupoid#DwyerKan80), [(1984)](simplicial+groupoid#DwyerKan84), in the guise of [[simplicial objects]] in [[Grpd]] with discrete simplicial set of objects and then referred to (inaccurately) as *[[simplicial groupoids]]* (see there for more).

Later

* [[John F. Jardine]], §9.3 in: *[[Local homotopy theory]]*, Springer Monographs in Mathematics (2015) &lbrack;[doi:10.1007/978-1-4939-2300-7](https://doi.org/10.1007/978-1-4939-2300-7)&rbrack;

switches to the terminology of *enriched groupoids* over simplicial sets (but still does not give the definition of enriched groupoids).

References that make the general definition of enriched groupoids explicit:

* [[Jacopo Emmenegger]], [[Fabio Pasquali]], [[Giuseppe Rosolini]], §3 in: *Elementary fibrations of enriched groupoids*, Mathematical Structures in Computer Science **31** 9 (2021) 958-978 &lbrack;[doi:10.1017/S096012952100030X](https://doi.org/10.1017/S096012952100030X)&rbrack;

  > (discussed as [[categorical semantics]] for [[homotopy type theory]])


[[!redirects enriched groupoids]]

