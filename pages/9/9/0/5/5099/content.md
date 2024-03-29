
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Uniform and normal logics
* table of contents
{: toc}

A [[modal logic]] is **uniform** if it is closed under the rule of uniform substitution of $\mathcal{L}_\omega(n)$-formulae for propositional variables and is **normal** if it also contains the axiom schemata:
  
(K)  $\Diamond_i(\psi \vee \chi) \to \Diamond_i(\psi)\vee \Diamond_i(\chi)$  
  
(N) $\neg \Diamond_i(\bot)$

and monotonicity (for each $i$):
 
if $\psi \to \chi \in \Lambda$ then $\Diamond_i \psi \to \Diamond_i \chi \in \Lambda$.  

The smallest normal modal logic with $m$ 'agents' is [[the logic K(m)|K(m)]]. (The diamonds correspond to the $M_i$ of that entry.)


[[!redirects normal modal logic]]
[[!redirects normal modal logics]]

[[!redirects uniform modal logic]]
[[!redirects uniform modal logics]]
