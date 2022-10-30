#Definition#

An __adjunction__ in a [[2-category]] is a pair of objects $C,D$ together with morphisms $L: C \to D$, $R : D \to C$ and 2-cells $\eta: 1_C \to R \circ L$, $\epsilon: L \circ R \to 1_D$ satisfying the equations

$$ 
  R\epsilon . \eta R = 1_R
  \qquad \text{i.e.} \qquad
  \array{\arrayopts{ \padding{0} }
    &&&&1_C& 
    \\
    &&\cellopts{\colspan{5}}\begin{svg}
       [[!include adjunction/zigzageta]]
       \end{svg}\\
    D
    & \stackrel{R}{\to}&
    C
    & \stackrel{L}{\to}&
    D
    & \stackrel{R}{\to}&
    C
    \\
    \cellopts{\colspan{4}}\begin{svg}
       [[!include adjunction/zigzagepsilon]]
       \end{svg}
    \\
    &&1_D&
  }
  \quad = \quad D \stackrel{R}{\to} C
$$
and
$$ 
  \epsilon L . L\eta = 1_L
  \qquad \text{i.e.} \qquad
  \array{\arrayopts{ \padding{0} }
    &&1_C& 
    \\
    \cellopts{\colspan{5}}\begin{svg}
       [[!include adjunction/zigzageta]]
       \end{svg}\\
    C
    & \stackrel{L}{\to}&
    D
    & \stackrel{R}{\to}&
    C
    & \stackrel{L}{\to}&
    D
    \\
    &&\cellopts{\colspan{4}}\begin{svg}
       [[!include adjunction/zigzagepsilon]]
       \end{svg}
    \\
    &&&&1_D&
  }
  \quad = \quad C \stackrel{L}{\to} D
$$

variously called the _[[triangle identities]]_ or the _zig-zag identities_.  We call $L$ the **[[left adjoint]]** (of $R$) and $R$ the **[[right adjoint]]** (of $L$).  We call $\eta$ the [[unit]] and $\epsilon$ the [[counit]] of the adjunction.

When interpreted in the prototypical 2-category [[Cat]], $C$ and $D$ are [[category|categories]], $L$ and $R$ are [[functor|functors]], and $\eta$ and $\epsilon$ are [[natural transformation|natural transformations]].  In this case (which was of course the first to be defined) there are a number of equivalent definitions of an adjunction, which can be found on the page [[adjoint functor]].  Conversely, the definition in any 2-category can be obtained by [[internalization]] from the definition in $\Cat$.

#Remarks#

Essentially everything that makes category theory nontrivial and interesting can be derived from the concept of adjunction. In particular [[universal construction]]s such as [[limit|limits and colimits]] are examples of certain adjunctions.