
# Contents
* table of contents
{: toc}

## Idea

The notion of _coinvariant_ is [[duality|dual]] to that of *[[invariant]]*.


## Definitions

### Of group representations

Let $G$ be a [[discrete group]], $k$ a [[commutative unital ring]], $k[G]$ the [[group ring]] of $G$ and $V$ a left $k[G]$-[[module]], hence a linear $G$-[[representation]] over $k$. 

Then there is well-defined [[quotient]] $k$-module $V_G = V/\langle{v - g v}\rangle$ called the module of __$G$-coinvariants__. Here $\langle{v - g v}\rangle$ denotes the smallest $k$-[[submodule]] of $V$ containing all expressions of the form $v - g v$ where $g\in G$ and $v\in V$. 

Notice that here $v$ and $g v$ are two points on same [[orbit]] of $G$ and so the coinvariants are essentially the [[orbits]] of $G$ in $V$.


### Of coalgebras

Let $C$ be a $k$-[[coalgebra]], $\chi$ a [[group-like element]], that is, an element such that $\Delta_C(\chi)=\chi\otimes\chi$, and $\rho:V\to V\otimes C$ a right $C$-[[coaction]]. Any element $v\in V$ such that $\rho(v)=v\otimes\chi$ is called a __$(\rho,\chi)$-coinvariant element__ in the $C$-comodule $(V,\rho)$. Suppose $H$ is a [[bialgebra]], $A$ an algebra and $\rho:A\to A\otimes H$ a coaction making $A$ into a right $H$-comodule algebra. The unit element $1_H$ is a group-like element, and we call $(\rho,1)$-coinvariants simply __$\rho$-coinvariants__. The subset of $\rho$-coinvariants in $A$ is a subalgebra, called the __subalgebra of coinvariants__.  


## Related concepts

* [[invariant]]

* [[norm map]]

* [[homotopy coinvariant functor]]

[[!include homotopy type representation theory -- table]]


[[!redirects coinvariant]]
[[!redirects coinvariants]]
