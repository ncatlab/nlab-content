[[!redirects adjoint pair]]
[[!redirects adjoint pairs]]
[[!redirects adjunctions]]

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

When interpreted in the prototypical 2-category [[Cat]], $C$ and $D$ are [[categories]], $L$ and $R$ are [[functors]], and $\eta$ and $\epsilon$ are [[natural transformations]].  In this case (which was of course the first to be defined) there are a number of equivalent definitions of an adjunction, which can be found on the page [[adjoint functor]].  Conversely, the definition in any 2-category can be obtained by [[internalization]] from the definition in $\Cat$.

#Remarks#

Essentially everything that makes category theory nontrivial and interesting can be derived from the concept of adjunction. In particular [[universal constructions]] such as [[limit|limits and colimits]] are examples of certain adjunctions.

#String Diagrams#

The definition of an adjunction may be nicely expressed using [[string diagrams]]. The data $L: C \to D$, $R : D \to C$ and 2-cells $\eta: 1_C \to R \circ L$, $\epsilon: L \circ R \to 1_D$ are depicted as

[[adjunction-L.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-R.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-unit.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-co-unit.png:pic]]

(where 1-cells read from right to left and 2-cells from bottom to top), and the zigzag identities are expressed as "pulling zigzags straight" (hence the name):

[[adjunction-up-string.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-down-string.png:pic]]

Often, arrows on strings are used to distinguish $L$ and $R$, and most or all other labels are left implicit; so the zigzag identities, for instance, become:

[[adjunction-up-string-minimal.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-down-string-minimal.png:pic]]

#References#

* Catsters, _Adjunctions_ ([YouTube](http://www.youtube.com/watch?v=loOJxIOmShE&feature=channel_page))
