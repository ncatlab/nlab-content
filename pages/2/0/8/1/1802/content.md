The **Mitchell-B&#233;nabou language** is a method of assigning to any [[topos]] $E$ a language (or [[type theory]]) $L(E)$ where:
* the **types** are the objects of E
* **terms** of type X in the variables x<sub>i</sub> of type X<sub>i</sub> are polynomial expressions &#966;(x<sub>1</sub>,...,x<sub>m</sub>):1&#8594;X in the arrows x<sub>i</sub>:1&#8594;X<sub>i</sub> in E
* **formulas** are terms of type $\Omega$ (arrows from types to $\Omega$), where $\Omega$ is the [[subobject classifier]] 
* connectives are induced from the internal [[Heyting algebra]] structure of $\Omega$
* quantifiers bounded by types and applied to formulas are also treated
* for each type X there are also two binary relations =<sub>X</sub> (defined applying the diagonal map to the product term of the arguments) and &#8712;<sub>X</sub> (defined applying the evaluation map to the product of the term and the power term of the arguments).

A formula is true if the arrow which interprets it factor through the arrow true:1&#8594;&#937;. The Mitchell-B&#233;nabou internal language is a powerful way to describe various objects in a topos as if they were sets and hence is a way of making the topos into a generalized set theory, to write and prove statements in a topos using first order intuitionistic predicate logic, to concider toposes as type theories and to express properties of a topos. Any language $L$ also generates a [[linguistic topos]] $E(L)$.