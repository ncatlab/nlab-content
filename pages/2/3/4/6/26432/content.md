
## Disambiguation

There are a few different types which can be called *heterogeneous path types* or *dependent path types* in [[dependent type theory]]:

* The [[heterogeneous identity type]] $u =_{B(-)}^{p} v$ for type family $B(x)$ indexed by $x:A$, and elements $x:A$, $y:A$, $u:B(x)$, $v:B(y)$, and identification $p:x =_A y$, which is the type of paths between $u:B(x)$ and $v:B(y)$ across $p:x =_A y$;

* The [[dependent sum type]] $\sum_{u:B(x)} \sum_{v:B(y)} u =_{B(-)}^{p} v$, which is the type of all heterogeneous paths in the type family $B(x)$ across the identification $p:x =_A y$; 

* The [[dependent function type]] $\prod_{i:\mathbb{I}} B(x)$ from the [[interval type]] $\mathbb{I}$ to the type family $B(x)$. 

* In [[cubical type theory]], the [[cubical path type]] $\mathrm{path}_{i.A}(x, y)$ for a line of types $A(i)$ indexed by interval variable $i:\mathbb{I}$, given interval terms $i:\mathbb{I}$ and $j:\mathbb{I}$ and elements $x:A(i)$ and $y:A(j)$. 

See also [[path type]] for the homogeneous version of path types. 

category: disambiguation

[[!redirects dependent path type]]
[[!redirects dependent path types]]
[[!redirects heterogeneous path type]]
[[!redirects heterogeneous path types]]
[[!redirects dependent heterogeneous path type]]
[[!redirects dependent heterogeneous path types]]
[[!redirects non-dependent heterogeneous path type]]
[[!redirects non-dependent heterogeneous path types]]

[[!redirects dependent path]]
[[!redirects dependent paths]]
[[!redirects heterogeneous path]]
[[!redirects heterogeneous paths]]
[[!redirects dependent heterogeneous path]]
[[!redirects dependent heterogeneous paths]]
[[!redirects non-dependent heterogeneous path]]
[[!redirects non-dependent heterogeneous paths]]

[[!redirects weak dependent path type]]
[[!redirects weak dependent path types]]
[[!redirects weak heterogeneous path type]]
[[!redirects weak heterogeneous path types]]
[[!redirects weak dependent heterogeneous path type]]
[[!redirects weak dependent heterogeneous path types]]
[[!redirects weak non-dependent heterogeneous path type]]
[[!redirects weak non-dependent heterogeneous path types]]

[[!redirects strict dependent path type]]
[[!redirects strict dependent path types]]
[[!redirects strict heterogeneous path type]]
[[!redirects strict heterogeneous path types]]
[[!redirects strict dependent heterogeneous path type]]
[[!redirects strict dependent heterogeneous path types]]
[[!redirects strict non-dependent heterogeneous path type]]
[[!redirects strict non-dependent heterogeneous path types]]

[[!redirects judgmentally strict dependent path type]]
[[!redirects judgmentally strict dependent path types]]
[[!redirects judgmentally strict heterogeneous path type]]
[[!redirects judgmentally strict heterogeneous path types]]
[[!redirects judgmentally strict dependent heterogeneous path type]]
[[!redirects judgmentally strict dependent heterogeneous path types]]
[[!redirects judgmentally strict non-dependent heterogeneous path type]]
[[!redirects judgmentally strict non-dependent heterogeneous path types]]

[[!redirects propositionally strict dependent path type]]
[[!redirects propositionally strict dependent path types]]
[[!redirects propositionally strict heterogeneous path type]]
[[!redirects propositionally strict heterogeneous path types]]
[[!redirects propositionally strict dependent heterogeneous path type]]
[[!redirects propositionally strict dependent heterogeneous path types]]
[[!redirects propositionally strict non-dependent heterogeneous path type]]
[[!redirects propositionally strict non-dependent heterogeneous path types]]