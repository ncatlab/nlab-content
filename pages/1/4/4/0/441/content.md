
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

##Idea##

The _horn_ $\Lambda_k[n] = \Lambda^n_k \hookrightarrow \Delta^n$ is the [[simplicial set]] obtained from the [[boundary of a simplex|boundary of the n-simplex]] $\partial \Delta^n$ of the standard simplicial $n$-[[simplex]] $\Delta^n$ by discarding the $k$th face.

##Definition##

Let 

$$
  \Delta[n] = \mathbf{\Delta}( -, [n]) \in  Simp Set
$$

be the standard simplicial $n$-[[simplex]] in [[SimpSet]].

+-- {: .num_defn #Horn}
###### Definition

For all $n,i$ with $n\geq 1$ and $0\leq i \leq n$, the **$(n,i)$-horn** or **$(n,i)$-box** 
is the subsimplicial set 

$$
  \Lambda^i[n]
  \hookrightarrow
  \Delta[n] 
$$

which is the [[union]] of all faces _except_ the  $i^{th}$ one.

This is called an **outer horn** if $k = 0$ or $k = n$.  Otherwise it is an **inner horn**.


=--

\begin{remark}
**(the 0-simplex has no horns)**
  Beware that any would-be horn of the 0-simplex is *ex*-cluded in Def. \ref{Horn}: The 0-simplex has *no* horn. 

This is not a matter of convention, in particular one must *not* declare a would-be horn of the 0-simplex to be the [[empty set]]: This would make the [[nerve of a category|nerve]] of the [[empty groupoid]] fail to be a [[Kan complex]]. 

Conversely, the fact that every horn is [[inhabited set|inhabited]] means that any morphism out of the empty [[simplicial set]], $\varnothing \to X$, is a [[Kan fibration]].
\end{remark}

+-- {: .num_remark }
###### Remark


Since [[sSet]]  is a [[presheaf topos]], [[unions]] of [[subobjects]] make sense and they are calculated objectwise, thus in this case dimensionwise.  This way it becomes clear what the structure of a horn as a functor $\Lambda^k[n]: \Delta^{op} \to Set$ must therefore be: it takes $[m]$ to the collection of ordinal maps $f: [m] \to [n]$ which factor through some coface map $[n-1] \to [n]$ which is _not_ the $i^{th}$ one.

=--


##Examples##

+-- {: .num_example}
###### Example

The inner horn of the 2-simplex 

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

##Relation to other concepts##

* A [[Kan fibration]] is a morphism of simplicial sets which has the right [[lifting property]] with respect to all horn inclusions $\Lambda^k[n] \hookrightarrow \Delta^n$.

* A [[Kan complex]] is a simplicial set in which "*all horns have fillers*": a simplicial set for which the morphism to the point is a Kan fibration.

* A [[quasi-category]] is a simplicial set in which *all inner* horns have fillers*, such that the map to the point is an [[inner fibration]].

* The [[boundary of a simplex]] is the union of its faces.

* The [[spine]] of a [[simplex]] is the [[union]] of all its generating 1-cells.

[[!redirects horns]]