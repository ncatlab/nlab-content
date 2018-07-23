
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

The __triangle identities__ or __zigzag identities__ are identities characterized by the [[unit of an adjunction|unit and counit]] of an [[adjunction]], such as a [[adjoint pair|pair]] of [[adjoint functors]]. These identities _define_, equivalently, the nature of adjunction ([this prop. ](adjoint+functor#GeneralAdjunctsInTermsOfAdjunctionUnitCounit)).

## Statement
 {#Statement}

Consider:

1. $C, D$ be two [[categories]], or, generally, two [[objects]] of a given [[2-category]];

1. $L: C \to D$ and $R : D \to C$ two [[functors]] between these, or generally [[1-morphisms]] in the ambient [[2-category]];

1. $\eta: id_C \Rightarrow R \circ L$ and $\epsilon: L \circ R \Rightarrow id_D$ two [[natural transformations]] or, generally [[2-morphisms]].

This data is called an _[[adjoint pair|pair]] of [[adjoint functors]]_ (generally: an _[[adjunction]]_) if the _triangle identities_ are satisfied, which may be expressed in any of the following equivalent ways:

1. _[As equations](#AsEquations)_

1. _[As diagrams](#AsDiagrams)_

1. _[As string diagrams](#AsStringDiagrams)_

$\,$

### As equations
  {#AsEquations}

$$ L \stackrel{L\eta}\to L R L\stackrel{\epsilon L}\to L $$
and 
$$ R\stackrel{\eta R}\to R L R \stackrel{R\epsilon}\to R $$
are identities.
(Here, the composition of the $1$- with the $2$-morphisms is sometimes called [[whiskering]].)



### As diagrams
 {#AsDiagrams}

As [[diagrams]] in the ambient [[2-category]], the triangle identities look as follows

$$ 
  \array{
  \epsilon L . L\eta &=& id_L
  \\
  \array{\arrayopts{ \padding{0} }
    &&1_C& 
    \\
    \cellopts{\colspan{5}}\begin{svg}
       [[!include adjunction > zigzageta]]
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
       [[!include adjunction > zigzagepsilon]]
       \end{svg}
    \\
    &&&&1_D&
  }
  & = &  C \stackrel{L}{\to} D
  }
  \phantom{AAAAA} \text{and} \phantom{AAAAA}
  \array{
    R\epsilon . \eta R &=& id_R
  \\
  \array{\arrayopts{ \padding{0} }
    \\
    &&&&1_C& 
    \\
    &&\cellopts{\colspan{5}}\begin{svg}
       [[!include adjunction > zigzageta]]
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
       [[!include adjunction > zigzagepsilon]]
       \end{svg}
    \\
    &&1_D&
  }
  &=& D \stackrel{R}{\to} C
  }
$$

or, equivalently, like so:

<center>
<img src="https://ncatlab.org/nlab/files/Adjointness.jpg" width="540">
</center>


### As string diagrams
 {#AsStringDiagrams}

As [[string diagrams]], the triangle identities appear as the action of "pulling zigzags straight" (hence the name):

+--
<span style='margin-right: 50px'>[[adjunction-up-string.png:pic]]</span>[[adjunction-down-string.png:pic]]
=-- {: style='text-align:center'}

With labels left implicit, this notation becomes very economical:

+--
<span style='margin-right: 50px'>[[adjunction-up-string-minimal.png:pic]],</span> [[adjunction-down-string-minimal.png:pic]].
=-- {: style='text-align:center'}

## Related concepts

* [[adjunction]]

* **zig-zag law** / **triangle identity**

* [[unit of an adjunction]]

* [[adjunct]]

## References

Textbook accounts include

* {#Borceux94} [[Francis Borceux]], Theorem 3.1.5 and Diagram 3.3 in: _Basic Category Theory_, Vol. 1 of _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)

See the references at _[[category theory]]_ for more.



[[!redirects zigzag identities]]
[[!redirects zigzag identity]]
[[!redirects zig-zag identities]]
[[!redirects zig-zag identity]]
[[!redirects zig-zag law]]
[[!redirects triangle identity]]

[[!redirects zigzag-identity]]
[[!redirects zigzag-identities]]
[[!redirects zigzag-identity]]
[[!redirects zig-zag-identities]]
[[!redirects zig-zag-identity]]