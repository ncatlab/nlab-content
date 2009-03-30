#Definition#

An __adjunction__ in a [[2-category]] is a pair of objects $C,D$ together with morphisms $L: C \to D$, $R : D \to C$ and 2-cells $\eta : 1_C \to R L$, $\epsilon : L R \to 1_D$ satisfying the equations

$$ 
  R\epsilon . \eta R = 1_R
  \qquad \text{i.e.} \qquad
  \array{\arrayopts{ \padding{0} }
    &&&&1_C& 
    \\
    &&\cellopts{\colspan{5}}\begin{svg}
       <svg xmlns="http://www.w3.org/2000/svg" width="8.5em" height="2em" viewBox="0 0 85 20">
          <defs>
            <marker id='svg195arrowhead' markerHeight='5' markerUnits='strokeWidth' markerWidth='8' orient='auto' refX='0' refY='5' viewBox='0 0 10 10'>
              <path d='M 0 0 L 10 5 L 0 10 z'/>
            </marker>
         </defs>
         <path marker-end='url(#svg195arrowhead)' stroke-width="1" stroke="#000" fill="none" d="M5 15q40-28 75 0"/>
         <foreignObject height='20' width='20' x='40' y='3' font-size='10'><math xmlns="http://www.w3.org/1998/Math/MathML" display='inline'><msup><mo>&#8659;</mo><mi>&#951;</mi></msup></math></foreignObject>
       </svg>
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
       <svg xmlns="http://www.w3.org/2000/svg" width="8.5em" height="2em" viewBox="0 0 85 20">
         <path marker-end='url(#svg195arrowhead)' stroke-width="1" stroke="#000" fill="none" d="M5 5q40 28 75 0"/>
           <foreignObject height='20' width='20' x='40' y='0' font-size='10'><math xmlns="http://www.w3.org/1998/Math/MathML" display='inline'><msup><mo>&#8659;</mo><mi>&#1013;</mi></msup></math></foreignObject>
       </svg>
       \end{svg}
    \\
    &&1_D&
  }
  \quad = \quad D \stackrel{R}{\to} C
$$
and
$$ 
  \epsilon L . L\eta = 1_L
$$

i.e.

<center markdown="1">[[zigzag-1-bigger.png:pic]]</center>

variously called the _triangle identities_ or the _zig-zag identities_.  We call $L$ the **left adjoint** (of $R$) and $R$ the **right adjoint** (of $L$).  We call $\eta$ the [[unit]] and $\epsilon$ the [[counit]] of the adjunction.

When interpreted in the prototypical 2-category [[Cat]], $C$ and $D$ are [[category|categories]], $L$ and $R$ are [[functor|functors]], and $\eta$ and $\epsilon$ are [[natural transformation|natural transformations]].  In this case (which was of course the first to be defined) there are a number of equivalent definitions of an adjunction, which can be found on the page [[adjoint functor]].  Conversely, the definition in any 2-category can be obtained by [[internalization]] from the definition in $\Cat$.

#Remarks#

Essentially everything that makes category theory nontrivial and interesting can be derived from the concept of adjunction. In particular [[universal construction]]s such as [[limit|limits and colimits]] are examples of certain adjunctions.
