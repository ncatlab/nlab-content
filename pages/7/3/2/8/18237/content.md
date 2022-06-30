
> This page is about the concept in [[topology]]. For the more general concept see at _[[open morphism]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn #OpenMap}
###### Definition
**([[open maps]] and [[closed maps]])**

A [[continuous function]] $f \colon (X,\tau_X) \to (Y, \tau_Y)$ between [[topological spaces]]  is called

*  an _[[open map]]_ if the [[image]] under $f$ of an [[open subset]] of $X$ is an open subset of $Y$;

* a _[[closed map]]_ if the [[image]] under $f$ of a [[closed subset]] of $X$  is a closed subset of $Y$.

=--

## Examples

+-- {: .num_example #OpenClosedImageProjection}
###### Example
**([[image]] projections of [[open map|open]]/[[closed maps]] are themselves open/closed)**

If a [[continuous function]] $f \colon (X,\tau_X) \to (Y,\tau_Y)$ is an [[open map]] or [[closed map]] (def. \ref{OpenMap})
then so is its [[image]] projection $X \to f(X) \subset Y$, respectively, for $f(X) \subset Y$ regarded with its
[[subspace topology]].

=--

+-- {: .proof}
###### Proof

If $f$ is an open map, and $O \subset X$ is an open subset, so that $f(O) \subset Y$ is also open in $Y$, then, since $f(O) = f(O) \cap f(X)$, it is also still open in the subspace topology, hence $X \to f(X)$ is an open map.

If $f$ is a closed map, and $C \subset X$ is a closed subset so that also $f(C) \subset Y$ is a closed subset, then the [[complement]] $Y \backslash f(C)$ is open in $Y$ and  hence $(Y \backslash f(C)) \cap f(X) = f(X) \backslash f(C)$ is open in the subspace topology, which means that $f(C)$ is closed in the subspace topology.


=--

+-- {: .num_example #ProjectionsAreOpenContinuousFunctions}
###### Example
**([[projections]] out of [[product spaces]] are open maps)**

For $(X_1,\tau_{X_1})$ and $(X_2,\tau_{X_2})$ two [[topological spaces]], then the projection maps

$$
  pr_i \;\colon\; (X_1 \times X_2, \tau_{X_1 \times X_2}) \longrightarrow (X_i, \tau_{X_i})
$$

out of their [[product topological space]] 

$$
  \array{
    X_1 \times X_2 &\overset{pr_1}{\longrightarrow}& X_1
    \\
    (x_1, x_2) &\overset{\phantom{AAA}}{\mapsto}& x_1
  }
$$

$$
  \array{
    X_1 \times X_2 &\overset{pr_2}{\longrightarrow}& X_2
    \\
    (x_1, x_2) &\overset{\phantom{AAA}}{\mapsto}& x_2
  }
$$

are [[open maps|open]] [[continuous functions]]  (def. \ref{OpenMap}).

This is because, by definition, every open subset $O \subset X_1 \times X_2$ in the product space topology is a union of products of
open subsets $U_i \in X_1$ and $V_i \in X_2$ in the factor spaces

$$
  O = \underset{i \in I}{\cup} \left( U_i \times V_i  \right)
$$

and because taking the image of a function preserves unions of subsets

$$
  \begin{aligned}
    pr_1\left(
      \underset{i \in I}{\cup} \left( U_i \times V_i \right)
    \right)
    & =
    \underset{i \in I}{\cup}
    pr_1
    \left(
      U_i \times V_i
    \right)
    \\
    & =
    \underset{i \in I}{\cup} U_i
  \end{aligned}
  \,.
$$


=--


\begin{proposition}\label{LocalHomeosAreOpenMaps}
  A [[local homeomorphism]] is an [[open map]].
\end{proposition}
\begin{proof}
  Let $f \colon X \to Y$ be a [[local homeomorphism]] and $U \subset X$ an [[open subset]]. We need to see that the [[image]] $f(U) \subset Y$ is an open subset of $Y$. 
For this we may equivalently show that each $y \in f(U)$ has an [[open neighbourhood]] inside $f(U)$.

But since any function is [[surjection|surjective]] onto its [[image]], there exists $x \in U$ with $f(x) = y$.
By local homeomorphy of $f$, this $x \in X$ has an  [[open neighbourhood]] $U_x \subset X$ with $f_{|U_x} \colon U_x \to f(U_x)$ a [[homeomorphism]]. Since $U \cap U_x \subset U_x$ is an [[open neighbourhood]] of $x$ in $U_x$, the homeomorphy of $f_{|U_x}$ implies that $f(U \cap U_x) \subset f(U)$ is an open neighbourhood of $f(x) = y$.
\end{proof}


## Properties
 {#Properties}

\begin{proposition}\label{PreimagesOfOpenMapsPreserveInteriors}
**([[preimages]] of [[open maps]] preserve [[topological interiors]])**
\linebreak
For $f \,\colon\, X \longrightarrow Y$  an [[open map]] and $U \subset X$ a [[subset]], the [[preimage]] under $f$ of the [[interior]] of $U$ is the [[interior]] of the preimage of all of $U$:
$$
  \big( f^{-1}(U) \big)^\circ
  \;=\;
  f^{-1}\big( U^\circ\big)
  \,.
$$
\end{proposition}
\begin{proof}
In one direction, the inclusion
$$
  f^{-1}\big( U^\circ\big)
  \;\subset\;
  \big( f^{-1}(U) \big)^\circ
$$
follows since the left hand side is an [[open subset]] of $f^{-1}(U) \subset X$ by [[continuous map|continuity]] of $f$, while the right hand side is the largest such subset, by definition.

In the other direction, the inclusion
$$
  \big( f^{-1}(U) \big)^\circ
  \;\subset\;
  f^{-1}\big( U^\circ\big)
$$
is equivalent (see [there](interactions+of+images+and+pre-images+with+unions+and+intersections#PreimageRightAdjointToImage)) to the inclusion
$$
  f\Big( \big( f^{-1}(U) \big)^\circ \Big)
  \;\subset\;
  U^\circ 
  \,.
$$
This follows since now the left hand side is an open subset of $f(U)$ by [[open map|open-ness]] of $f$, while the right hand side is again the largest open subset of $U$, by definition.
\end{proof}

And dually:
\begin{proposition}\label{PreimagesOfOpenMapsPreserveClosures}
**([[preimages]] of [[open maps]] preserve [[topological closure]])**
\linebreak
If $f \,\colon\, X \longrightarrow Y$ is an [[open map]], and $U \subset X$ a [[subset]] with [[topological closure]] $\overline{U}$, then the [[preimage]] $f^{-1}\big( \overline{U}\big)$ of the [[topological closure]] is the [[topological closure]] of the [[preimage]] of $U$:
$$
  \overline{f^{-1}(U)}
  \;=\;
  f^{-1}\big(  \overline{U} \big)
  \,.
$$
\end{proposition}
\begin{proof}
Noticing that 

1. the topological closure is equivalently the [[complement]] of the [[topological interior]] of the [[complement]] (see [there](closed+subspace#RelationToInteriorSubspaces)):

   $$
      \overline{U}
      \,=\,
      X \setminus (X \setminus U)^\circ
   $$

1. [[preimages]] evidently preserve [[complements]]

it is sufficient to observe that forming preimages of open maps preserves interiors. This is the statement of Prop. \ref{PreimagesOfOpenMapsPreserveInteriors}.
\end{proof}




## Related concepts

* [[open morphism]]

* [[embedding of topological spaces]]

* [[closed map]], [[proper map]]

[[!redirects open maps]]
[[!redirects open mapping]]
[[!redirects open mappings]]
