+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

In [[homotopy type theory]] a **preallegory** is a [[dagger precategory]] $C$ such that 

* for each object $a:Ob(C)$ and $b:Ob(C)$ there is a function 
$$(-)\wedge_{a, b}(-):Mor_C(a, b) \times Mor_C(a, b) \to Mor_C(a, b)$$ 
such that for each morphism $f:Mor_C(a, b)$, $g:Mor_C(a, b)$, and $h:Mor_C(a, b)$ there are [[identifications]] 
$$\mathrm{assoc}(a, b, f, g, h):f \wedge_{a, b} (g \wedge_{a, b} h) = (f \wedge_{a, b} g) \wedge_{a, b} h$$ 
$$\mathrm{comm}(a, b, f, g):f \wedge_{a, b} g = g \wedge_{a, b} f$$ 
$$\mathrm{idem}(a, b, f): f \wedge_{a, b} f = f$$ 

* for each object $a:Ob(C)$ and $b:Ob(C)$ and morphism $f:Mor_C(a, b)$ and $g:Mor_C(a, b)$ there is a function 
$$\mathrm{monotone}(a, b, f, g): (f \wedge_{a, b} g = f) \to (f^{\dagger_{a, b}} \wedge_{b, a} g^{\dagger_{a, b}} = f^{\dagger_{a, b}})$$

* for each object $a:Ob(C)$, $b:Ob(C)$, and $c:Ob(C)$ and morphism $f:Mor_C(a, b)$, $g:Mor_C(b, c)$, and $h:Mor_C(a, c)$, there is an [[identification]] 
$$\mathrm{modular}(a, b, c, f, g, h):\left((g \circ_{a, b, c} f) \wedge_{a, c} h\right) \wedge_{a, c} \left(g \circ_{a, b, c} (f \wedge_{a, b} (g^{\dagger_{b, c}} \circ_{a, c, b} h))\right) = (g \circ_{a, b, c} f) \wedge_{a, c} h$$

## Examples

* For every [[type universe]] $\mathcal{U}$ the precategory $\mathrm{Rel}_\mathcal{U}$ of $\mathcal{U}$-small sets and locally $\mathcal{U}$-small propositional-valued relations is a preallegory. 

## See also

* [[precategory]]

* [[dagger precategory]]

* [[allegory]]

[[!redirects preallegory]]