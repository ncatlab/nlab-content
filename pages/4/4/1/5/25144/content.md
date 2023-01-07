\tableofcontents

## Idea

In [[dependent type theory]], a dependent function is like a [[function]] but where we allow the [[codomain]] of the to depend on elements of the [[domain]]. 

## Definition

In [[dependent type theory]], a [[type]] $A$ is a [[contractible type]] if it comes with an element $a:A$ and a family of identities $x:A \vdash c(x):a =_A x$ indicating that $a$ is a [[center of contraction]]. A **dependent function** from type $A$ to the type family $x:A \vdash B(x)$ could be defined as

* a family of elements $x:A \vdash f(x):B(x)$
* a dependent multivalued partial function $(x:A \vdash P(x); x:A, p:P(x) \vdash f(x, p):B(x))$ for which the dependent type $P(x)$ is a [[contractible type]] for all $x:A$
* a [[dependent anafunction]], a [[dependent correspondence]] $x:A, y:B(x) \vdash R(x, y)$ for which the dependent type $\sum_{y:B(x)} R(x, y)$ is a [[contractible type]] for all $x:A$. 
* an element of the [[dependent function type]] $f:\prod_{x:A} B(x)$, in dependent type theories with dependent function types. 

The first three definitions are interdefinable with each other in [[dependent type theories]] with [[identity types]] and [[dependent sum types]], and the fourth definition is interdefinable with the other three via the rules for [[dependent function types]]

## See also

* [[function]]
* [[dependent function type]]
* [[dependent anafunction]]

[[!redirects dependent function]]
[[!redirects dependent functions]]