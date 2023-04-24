
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

Let $(\mathcal{V}, \times, \ast)$ be a *[[cartesian monoidal category|cartesian]]* [[Bénabou cosmos]], so that, in particular, 

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
  \mathcal{C}(y,Z)
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
\end{example}

\begin{example}
  A $\mathcal{V}$-enriched groupoid with a single object is equivalently the [[delooping groupoid]] of a [[group object]] [[internalization|internal]] to $\mathcal{V}$.

For instance, a one-object [[sSet]]-groupoid (Exp. \ref{SimplicialGroupoid}) is the [[delooping groupoid]] of a [[simplicial group]].
\end{example}

\begin{example}\label{RelationToInternalGroupoids}
  An [[internal groupoid]] in $\mathcal{V}$ is equivalently a $\mathcal{V}$-enriched groupoid if its $\mathcal{V}$-object of objects is in the image of the [[coproduct]]-[[preserved colimit|preserving]] [[functor]] $Set \to \mathcal{V}$ (using here the assumption that $\mathcal{V}$ is a [[Bénabou cosmos]]).
\end{example}

## Related concepts

* [[enriched category]]

* [[internal groupoid]], [[internal group]]

* [[groupoid object in an (∞,1)-category]]

[[!redirects enriched groupoid]]

