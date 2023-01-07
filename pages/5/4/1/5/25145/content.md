
\tableofcontents

## Idea

In [[dependent type theory]], given types $A$ and $B$, a [[correspondence]] is a [[type family]] $x\colon A, y \colon B \vdash R(x, y) \; \mathrm{type}$. A *dependent correspondence* is like such an correspondence but where we allow $B$ to also [[dependent type|depend]] on $x\colon A$. 

## Definition 

In [[dependent type theory]] ([[homotopy type theory]]), given a type $A$ and a [[type family]] $x\colon A \vdash B(x) \; \mathrm{type}$, a **dependent correspondence** is a type family $x\colon A, y\colon B(x) \vdash R(x, y) \; \mathrm{type}$. 

## Examples

* Every [[correspondence]] is a dependent correspondence where $B$ does not depend upon $A$. 

* Every [[dependent anafunction]] is a dependent correspondence $x\colon A, y\colon B(x) \vdash R(x, y)$ which comes with a family of witnesses 
$$x \colon A \vdash p(x) \colon \mathrm{isContr}\left(\sum_{y\colon B(x)} R(x, y) \right)$$
that for each element $x\colon A$, the [[dependent sum type]] $\sum_{y\colon B(x)} R(x, y)$ is a [[contractible type]]. 

## See also

* [[correspondence]], **dependent correspondence**

* [[anafunction]], [[dependent anafunction]]

[[!redirects dependent correspondence]]
[[!redirects dependent correspondences]]