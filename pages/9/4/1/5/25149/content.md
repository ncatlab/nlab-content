

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


\tableofcontents

## Definition

In [[dependent type theory]] with [[identity types]], [[equivalence types]], and [[dependent function types]], **equivalence extensionality** characterizes the identity type of equivalence types and is the property that for all [[equivalence in type theory|equivalences]] $f:A \simeq B$ and $g:A \simeq B$, there are equivalences

$$
  \mathrm{equivext}(f, g)  
  \;\;\colon\;\;
  \big(f =_{A \simeq B} g\big) 
  \;\simeq\; 
  \prod_{x \colon A} 
  \,
  f(x) =_{B} g(x)
  \,.
$$

While [[function extensionality]] implies equivalence extensionality, it is unknown whether equivalence extensionality implies function extensionality under any conditions or whether equivalence extensionality is strictly weaker than function extensionality. 

## See also

* [[equivalence type]]

* [[equivalence of types]]

* [[extensionality]]