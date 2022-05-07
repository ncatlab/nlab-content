
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

In [[simplicial homotopy theory]] a *horn* of a [[simplex]] is a simplicial incarnation of the notion of a *boundary segment* (as opposed to the full boundary) of a [[cell]].

Specifically, the $k$th horn $\Lambda_k[n] \hookrightarrow \Delta[n]$ of the $n$-dimensional [[simplex]]  (defined for $n \geq 1$, see Rem. \ref{ZeroSimplexHasNoHorns}) is the [[simplicial set]] obtained from the [[boundary of a simplex|boundary of the n-simplex]] $\partial \Delta^n$ of the standard simplicial [[n-simplex]] $\Delta^n$ by discarding its $k$th face.


The property of a [[morphism]] of [[simplicial set]] to have the [[right lifting property]] against the inclusions of horns into their simplices (have "horn fillers") characterizes the basic types of [[fibrations]] and [[fibrant objects]] in [[simplicial homotopy theory]]:

* [[Kan fibrations]] (hence [[Kan complexes]], when over the point) are characterized as having the [[right lifting property]] against *all horns*; 

* [[left/right Kan fibrations]] are characterized as having the [[right lifting property]] against all horns *except* possibly the first/last horn inclusion in each dimension, respectively;

* [[quasi-categories]] are characterized as having the [[right lifting property]] against all horns *except* possibly the first and last horn inclusion in each dimension, respectively.

Specifically, [[Kan fibrations]] are the simplicial analog of [[Serre fibrations]] (in a precise sense so under the [[Quillen equivalence]] between the [[classical model structure on simplicial sets]] and [[classical model structure on topological spaces|on topological spaces]]) and under this correspondence the horn inclusions into the $n$th simplex correspond to the inclusion of the $(n-1)$-dimensional [[topological space|topological]] [[disk]] into its [[cylinder]]:

$$
  \Lambda_k[n] \hookrightarrow \Delta[n]
  \;\;\;\;
  \overset{\left\vert-\right\vert}{\mapsto}
  \;\;\;\;
  D^{n-1} \overset{(id,0)}{\hookrightarrow} D^{n-1} \times [0,1]
  \,,
$$

as both are the [[generating cofibrations]] in their respective [[model categories]] ([[classical model structure on simplicial sets|on sSet]], [[classical model structure on topological spaces|on Top]], respectively).


## Definition

Let 

$$
  \Delta[n] = \mathbf{\Delta}( -, [n]) \in  Simp Set
$$

denote the standard simplicial $n$-[[simplex]] in [[SimpSet]].

+-- {: .num_defn #Horn}
###### Definition
**(horns)**

For all $n,i$ with $n\geq 1$ and $0\leq i \leq n$, the **$(n,i)$-horn** or **$(n,i)$-box**  is the [[subobject|sub]]-[[simplicial set]]

$$
  \Lambda^i[n]
  \hookrightarrow
  \Delta[n] 
$$

which is the [[union]] of all faces _except_ the  $i^{th}$ one.

{#InnerHorns} This is called an **outer horn** if $k = 0$ or $k = n$, otherwise it is an **inner horn**.


=--

\begin{remark}
Since [[sSet]]  is a [[presheaf topos]], [[unions]] of [[subobjects]] make sense and they are calculated objectwise, thus in this case dimensionwise.  This way it becomes clear what the structure of a horn as a functor $\Lambda^k[n]: \Delta^{op} \to Set$ must therefore be: it takes $[m]$ to the collection of ordinal maps $f: [m] \to [n]$ which factor through some coface map $[n-1] \to [n]$ which is _not_ the $i^{th}$ one.
\end{remark}


\begin{remark}\label{ZeroSimplexHasNoHorns}
**(the 0-simplex has no horns)**\linebreak
Beware that any would-be horn of the 0-simplex (whose [[boundary of a simplex|boundary]] is the [[empty set]]) is *ex*-cluded in Def. \ref{Horn}: The 0-simplex has *no* horn. 

This is not a matter of convention if one sticks to the usual definition of [[Kan fibration]] as having [[right lifting property|right lifting]] against *all horns*:  In particular one must *not* declare a would-be horn of the 0-simplex to be itself the [[empty set]], as that would make the [[nerve of a category|nerve]] of the [[empty groupoid]] fail to be a [[Kan complex]] (Def. \ref{KanComplex}). 

Conversely, the fact that every horn is [[inhabited set|inhabited]] means that any morphism out of the empty [[simplicial set]] (an [[empty bundle]] $\varnothing \to X$) is a [[Kan fibration]] (Def. \ref{KanFibration}).
\end{remark}


## Examples ##

+-- {: .num_example}
###### Example

The [inner horn](#InnerHorns) of the 2-simplex 

$$\Delta^2 =    
  \left\{
      \array{
        && 1
        \\
        & \nearrow &\Downarrow& \searrow
        \\
        0 &&\to&& 2
      } 
     \right\}
$$

with [[boundary]]

$$\partial \Delta^2 =   \left\{
      \array{
        && 1
        \\
        & \nearrow && \searrow
        \\
        0 &&\to&& 2
      } 
     \right\}
$$ 

looks like

$$ 
\Lambda^2_1
  =
   \left\{
      \array{
        && 1
        \\
        & \nearrow && \searrow
        \\
        0 &&&& 2
      } 
     \right\}
 \,.
$$

The two outer horns look like

$$\Lambda^2_0 =   
\left\{
      \array{
        && 1
        \\
        & \nearrow && 
        \\
        0 &&\to&& 2
      } 
     \right\}
$$ 

and

$$\Lambda^2_2 =   
\left\{
      \array{
        && 1
        \\
        & && \searrow
        \\
        0 &&\to&& 2
      } 
     \right\}
$$ 

respectively. 

=--

## Lifting against horn inclusion

\begin{defn}\label{KanFibration}
**([[Kan fibration]])**\linebreak
A [[Kan fibration]] is a [[morphism]] of [[simplicial sets]] which has the [[right lifting property]] with respect to all horn inclusions $\Lambda^k[n] \hookrightarrow \Delta^n$.

\end{defn}

\begin{defn}\label{KanComplex}
**([[Kan complex]])**\linebreak
A [[Kan complex]] is a simplicial set in which "*all horns have fillers*": a simplicial set for which the morphism to the point is a Kan fibration (Def. \ref{KanFibration}).
\end{defn}

\begin{defn}\label{QuasiCategory}
**([[quasi-category]])**\linebreak
A [[quasi-category]] is a [[simplicial set]] in which *all [inner horns](#InnerHorns) have fillers*, hence such that the morphism to the [[point]] is an [[inner fibration]].
\end{defn}


## Related concepts

* The [[boundary of a simplex]] is the union of its faces.

* The [[spine]] of a [[simplex]] is the [[union]] of all its generating 1-cells.

## References

See the references at *[[simplicial homotopy theory]]*.



[[!redirects horns]]