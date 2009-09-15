<div class="rightHandSide toc">
[[!include higher algebra - contents]]
</div>


An $A_\infty$-algebra is an algebra for the cofibrant resolution of the [[operad]] $Ass$ of associative algebras: it is an algebra which is associative only up to higher coherent homotopy.

Concretely, an $A_\infty$-algebra is the structure of a degree 1 coderivation 

$$
  D : T^c V \to T^c V
$$

on the reduced tensor coalgebra $T^c V = \oplus_{n\geq 1} V^{\otimes n}$ over a graded vector space $V$ (the coproduct is the _unshuffle_ product) such that 
$$
  D^2 = 0
  \,.
$$

Coderivations on free coalgebras are entirely determined by their "value on cogenerators", which allows to decompose

$$
  D = D_1 + D_2 + D_3 + \cdots
$$

with each $D_k$ specified entirely by its action

$$
  D_k : V^{\otimes k} \to V
  \,.
$$
which is a map of degree $2-k$ (or can be alternatively understood as a map $D_k : (V[1])^{\otimes k}\to V[1]$ of degree $1$). 

Then:

* $D_1 : V\to V$ is the _differential_ with $D_1^2 = 0$;

* $D_2 : V^{\otimes 2} \to V$ is the _product_ in the algebra;

* $D_3 : V^{\otimes 3} \to V$ is the _associator_ which measures the failure of $D_2$ to be associative;

* $D_4 : V^{\otimes 4} \to V$ is the _pentagonator_ (or so) which measures the failure of $D_3$ to satisfy the pentagon identity;

* and so on.

One can also allow $D_0$, in which case one talks about weak $A_\infty$-algebras, which are less understood.

There is a resolution of the operad $\mathrm{Ass}$ of associative algebras (as operad on the category of chain complexes) which is called the $A_\infty$-operad; the algebras over the $A_\infty$-[[A-infinity operad|operad]] are precisely the $A_\infty$-algebras. 

A **morphism of $A_\infty$-algebras** $f : A\to B$ is a collection $\lbrace f_n\rbrace_{n\geq 1}$ of maps 
$$
f_n : (A[1])^{\otimes n}\to A[1]
$$
of degree $0$ satisfying
$$
\sum_{0\leq i+j\leq n} f_{i+j+1}\circ(1^{\otimes i}\otimes D_{n-i-j}\otimes 1^{\otimes j})
= \sum_{i_1+\ldots+i_r=n} D_r\circ (f_{i_1}\otimes\ldots f_{i_r}).
$$
For example, $f_1\circ D_1 = D_1\circ f_1$.

#Remarks#

* See also [[L-infinity-algebra]], [[A-infinity-category]].

#References#

* B. Keller, _A brief introduction to $A_\infty$-algebras_ ([pdf](http://people.math.jussieu.fr/~keller/publ/IntroAinfEdinb.pdf))


[[!redirects A-infinity-algebras]]
[[!redirects A-infinity algebra]]
[[!redirects A-infinity algebras]]
[[!redirects A-∞ algebra]]
[[!redirects A-∞ algebras]]
[[!redirects A? algebra]]
[[!redirects A? algebras]]
[[!redirects A-∞-algebra]]
[[!redirects A-∞-algebras]]