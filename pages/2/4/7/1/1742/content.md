
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

1. $\mathcal{C}, \mathcal{D}$ a [[pair]] of [[categories]], or, generally, of [[objects]] in a given [[2-category]];

1. $L \colon \mathcal{C} \to \mathcal{D}$ and $R \colon \mathcal{D} \to \mathcal{C}$ a pair of [[functors]] between these, or generally [[1-morphisms]] in the ambient [[2-category]];

1. $\eta \colon id_{\mathcal{C}} \Rightarrow R \circ L$ and $\epsilon \colon L \circ R \Rightarrow id_{\mathcal{D}}$ two [[natural transformations]] or, generally [[2-morphisms]].

This data is called an _[[adjoint pair|pair]] of [[adjoint functors]]_ (generally: an _[[adjunction]]_) if the _triangle identities_ are satisfied, which may be expressed in any of the following equivalent ways:

1. _[As equations](#AsEquations)_

1. _[As diagrams](#AsDiagrams)_

1. _[As string diagrams](#AsStringDiagrams)_

$\,$

### As equations
  {#AsEquations}

As [[equations]], the triangle identities read

$$
  \big(
    \epsilon L
  \big)
  \circ 
  \big( 
    L \eta 
  \big)
  \;=\;
  id_L
$$

$$
  \big(
    R \epsilon
  \big)
  \circ
  \big(
    \eta R
  \big)
  \;=\;
  id_R
$$

Here juxtaposition denotes the [[whiskering]] operation of [[1-morphisms]] on [[2-morphisms]], as made more manifest in the diagrammatic unravelling of these expressions:



### As diagrams
 {#AsDiagrams}

In terms of [[diagrams]] in the [[functor categories]] this means

$$ 
  L 
   \overset{\;\;L\eta\;\;}{\Rightarrow} 
  L R L
   \overset{\;\;\epsilon L\;\;}{\Rightarrow}
  L 
  \;\;
  =
  \;\;
  L \overset{\;\;id_L\;\;}{\Rightarrow} L
$$

and 

$$ 
  R
    \overset{\;\;\eta R\;\;}{\Rightarrow} 
  R L R 
    \overset{\;\;R\epsilon\;\;}{\Rightarrow} 
  R
  \;\;
  =
  \;\;
  R \overset{\;\;id_R\;\;}{\Rightarrow} R   
$$


In terms of diagrams of [[2-morphisms]] in the ambient [[2-category]], this looks as follows:

\begin{xymatrix}
  \mathcal{C}
  \ar[r]|-{ \;L\; }
  \ar@/^3pc/[rr]|-{ \;\mathrm{id}_{\mathcal{C}}\; }_-{\ }="s1"
  &
  \mathcal{D}
  \ar[r]|-{ \;R\; }
  \ar@/_3pc/[rr]|-{ \;\mathrm{id}_{\mathcal{D}}\; }^-{\ }="t2"
  & 
  \mathcal{C}
  \ar[r]|-{ \;L\; }
  &
  \mathcal{D}
  &
    =
  &
  \mathcal{C}
  \ar[r]|-{ \;L\; }
  & 
  \mathcal{D}
  %
  \ar@{=>}^\eta "s1"+(0,-2); "s1"+(0,-8)
  \ar@{=>}^\epsilon "t2"+(0,8); "t2"+(0,2)
\end{xymatrix}


\begin{xymatrix}
  \mathcal{D}
  \ar[r]|-{ \;R\; }
  \ar@/_3pc/[rr]|-{ \;\mathrm{id}_{\mathcal{D}}\; }^-{\ }="s1"
  &
  \mathcal{C}
  \ar[r]|-{ \;L\; }
  \ar@/^3pc/[rr]|-{ \;\mathrm{id}_{\mathcal{C}}\; }_-{\ }="t2"
  & 
  \mathcal{D}
  \ar[r]|-{ \;R\; }
  &
  \mathcal{C}
  &
    =
  &
  \mathcal{D}
  \ar[r]|-{ \;R\; }
  & 
  \mathcal{C}
  %
  \ar@{=>}^\eta "t2"+(0,-2); "t2"+(0,-8)
  \ar@{=>}^\epsilon "s1"+(0,8); "s1"+(0,2)
\end{xymatrix}


where on the right the [[identity morphism|identity]] [[2-morphisms]] are left notationally implicit.

If we leave the [[identity morphism|identity]] [[1-morphisms]] on the left notationally implicit, then we get the following suggestive form of the triangle identities:

<center>
<img src="https://ncatlab.org/nlab/files/Adjointness.jpg" width="540">
</center>

(taken from _[[geometry of physics -- categories and toposes]]_).


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