+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

## Definition 

A composition ring is a [[commutative ring]] $R$ with an operation 
$$(-)\circ(-):R \times R \to R$$ 
such that for each element $f \in R$, $g \in R$, and $h \in R$, 
$$(f + g) \circ h = (f \circ h) + (g \circ h)$$
$$(f \cdot g) \circ h = (f \circ h) \cdot (g \circ h)$$
$$f \circ (g \circ h) = (f \circ g) \circ h$$

## Examples

* Every [[polynomial ring]] is a composition ring. 

* Every commutative ring is a composition ring with $f \circ g = f$. 

* The [[function algebra]] on a commutative ring is a composition ring. 

## See also

* [[commutative ring]]

* [[polynomial ring]]

* [[function algebra]]

## References 

* Adler, Irving (1962), "Composition rings", Duke Mathematical Journal, 29 (4): 607–623, doi:10.1215/S0012-7094-62-02961-7, ISSN 0012-7094, MR 0142573

[[!redirects composition rings]]