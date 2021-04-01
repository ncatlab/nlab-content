
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Give a [[topological field|topological]] [[ground field]] $k$ and a  base [[topological space]] $B$, a [[short exact sequence]] of topological $k$-[[vector bundles]] over $B$ is a sequence of topological $k$-vector bundle homomorphisms over $B$ (i.e. [[continuous functions]] which are [[fiber]]-wise $k$-[[linear maps]])

\[
  \label{ShortExactSequenceOfTopologicalVectorBundles}
  0
  \to
  \mathcal{V}_L
    \overset{
      \;\;
        i
      \;\;}{\longrightarrow}
  \mathcal{V}
    \overset{
      \;\;
      p
      \;\;
     }{\longrightarrow}
  \mathcal{V}_R
  \to
  0
  \;\;\;\;
  \in
  k VectorBundles_B
\]

(where $0$ denotes the [[rank of a vector bundle|rank]]-[[zero]] bundle) such that 
$p$ is a [[surjection]]
and
$i = ker_B(p)$ in the [[injection]] of its [[fiber]]-wise [[kernel]],
hence such that over each point $b \colon \ast \overset{}{\longrightarrow} B$ we have a [[short exact sequence]] of $k$-[[vector spaces]]:

$$
  \underset{
    b \in B
  }{\forall}
  \;\;\;
  0
  \to
  b^\ast \mathcal{V}_L
    \overset{
      \;\;
      b^\ast i
      \;\;
    }{\longrightarrow}
  b^\ast \mathcal{V}
    \overset{
      \;\;
      b^\ast p
     \;\;
    }{\longrightarrow}
  b^\ast \mathcal{V}_R
  \to
  0
  \;\;\;
  \in
  \;
  k VectorSpaces
  \,.
$$

## Properties

### Splitting

\begin{prop}
  **(over [[paracompact topological spaces]] [[short exact sequences]] of [[real vector bundles]] [[split exact sequence|split]])**
\linebreak

If 

1. the [[ground field]] is the [[real numbers]] $k = \mathbb{R}$,

1. the base space $B$ is a [[paracompact Hausdorff space]],

1. the [[rank of a vector bundle|ranks]] are all [[finite number|finite]],

then every short exact sequence of topological vector bundles (eq:ShortExactSequenceOfTopologicalVectorBundles) [[split exact sequence|splits]] and exhibits the middle item as the [[direct sum of vector bundles]], over $B$, of the left and the right item:

$$
  \mathcal{V}
  \;\simeq\;
  \mathcal{V}_L 
    \oplus_B
  \mathcal{V}_R
  \,.
$$
\end{prop}
(e.g. [Hatcher, Prop. 1.3](#Hatcher), [Freed, Lemma 5.6](#Freed))

\begin{proof}
Sketch: Under the assumption on $B$, there exists (by [this Prop.](ExistenceOfInnerProductOfTopologicalVectorBundlesOverParacompactHausdorffSpaces)) a [[inner product on vector bundles|fiberwise inner product]] on $\mathca{V}$. With this the splitting follows by th usual splitting of short exact sequences of [[real vector spaces]], applied fiberwise: $\mathcal{V}_R$  is fiberwise identified with the [[orthogonal complement]] of $\mathcal{V}_L$.  
\end{proof}


## Related concepts

* [[vector bundle]] 
   
  * [[real vector bundle]]

  * [[complex vector bundle]]

    * [[holomorphic vector bundle]], [[pseudoholomorphic vector bundle]]

  * [[universal vector bundle]]

  * [[dual vector bundle]]

  * [[module bundle]]

  * [[direct sum of vector bundles]]
 
  * [[connection on a vector bundle]]

  * [[flat vector bundle]]

  * [[real vector bundle]], [[complex vector bundle]]

  * [[super vector bundle]]


## References

Textbook accounts:

* {#Hatcher} [[Allen Hatcher]], Prop. 1.3 in: _Vector bundles and K-Theory_ ([webpage](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html), [pdf](https://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf))

Lecture notes:

* {#Freed} [[Daniel Freed]], _More on stabilization_, Lecture 5 in _[Bordism: Old and New](https://web.ma.utexas.edu/users/dafr/M392C-2012/)_ ([pdf](https://jfdmath.sitehost.iu.edu/teaching/m529/vector_bundles.pdf))


[[!redirects short exact sequences of vector bundles]]
