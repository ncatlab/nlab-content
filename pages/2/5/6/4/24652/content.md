+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A **complete loop graph** is a [[loop graph]] $G$ where between any two vertices $a:G$ and $b:G$ there is exactly one edge $p:a \to_G b$. 

In the context of [[homotopy type theory]], a complete loop graph is a type $G$ with a type family $\to_G$ such that the [[dependent type]] $a \to_G b$ is a [[contractible type]] for all elements $a:G$ and $b:G$. 

A complete loop graph is **univalent**, a **[[subsingleton]]**, or a **[[proposition]]** if the canonical function 
$$idtoedge:(a =_G b) \to (a \to_G b)$$
is an equivalence of types. 

## See also

* [[loop graph]]
* [[directed loop graph]]
* [[setoid]]
* [[pregroupoid]]
* [[precategory]]
* [[Segal space]]