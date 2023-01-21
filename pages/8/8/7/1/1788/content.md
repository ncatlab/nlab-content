
For $B \,\colon\, Type$ be a (base)type, 
there is a precise sense in which $B$-[[dependent types]] may be regarded as [[function type|functions]] into $B$, hence as "[[bundles]] over $B$" (in the common sense of [[topology]]) and conversely.

The idea is that the total space of this bundle is the [[dependent pair]]-type of the components of the dependent type, mapping back to the base type via [[projection]] to the first element in the pair. Conversely, given such a function $f \,\colon\, E \to B$, its [[fiber types]] 

$$
  fib_b(f)
  \;\coloneqq\;
  (e \colon E) \times Id_{B}\big( f(e),\, b \big)
$$

form a $B$-dependent type:


$$
  \array{
    \underset{ Y \,\colon\, Type }{\sum} \big( Y \to X \big)
    &\longrightarrow&
    \underset{x \,\colon\, X}{\prod} Type
    \\
    (Y,f)
    &\mapsto&
    \big(
      x \colon X \;\vdash\; fib_x(f)
    \big)
  }
$$

and

$$
  \array{
    \underset{x \,\colon\, X}{\prod} Type
    &\longrightarrow&
    \underset{ Y \,\colon\, Type }{\sum} \big( Y \to X \big)
    \\
    \big(
      x \,\colon\, X 
      \;\;\vdash\;\; E(x)
    \big)
    &\mapsto&
    \Big(
      \big(
      \pi_1 
        \,\colon\,
      \underset{x \,:\, X}{\sum}  
      E(x)
      \big)
      \to
      X
    \Big)
  }
$$


***

[[DependentFunctionsAndPairs-230120.jpg:file]]

<img src="/nlab/files/DependentFunctionsAndPairs-230120.jpg" width="680">

see:

| [[type former]]:  |  meaning of [[terms]]:  |
|--|--|
| [[dependent product]] | [[dependent function]]<br/> / [[section]] of [[bundle]] |
| [[dependent sum]] | [[dependent pair]] / <br/> [[generalized element|element]] of [[bundle]] |

[[dependent functions and dependent pairs -- table]]