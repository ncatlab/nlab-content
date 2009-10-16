There are several notions of a formal group. A formal group should be viewed as an infinitesimal version of an [[algebraic group]]; unlike the [[Lie algebra]] which has the infinitesimal information of the product only up to the second order, the formal groups should contain the information to all orders. 

One of the oldest formalisms is the formalism of formal group laws (early study by Bochner and Lazard), which are a version of representing a group operation in terms of coefficients of the formal power series rings. A __formal group law of dimension__ $n$ is given by a set of $n$ power series $F_i$ of $2n$ variables $x_1,\ldots,x_n,y_1,\ldots,y_n$ such that (in notation $x=(x_1,\ldots,x_n)$, $y=(y_1,\ldots,y_n)$, $F(x,y) = (F_1(x,y),\ldots,F_n(x,y))$) 

$$
F(x,F(y,z))=F(F(x,y),z)
$$

$$
F_i(x,y) = x_i+y_i+\,\,higher\,\,order\,\,terms
$$

Formal group laws of dimension $1$ proved to be important in [[algebraic topology]], especially in the study of [[cobordism]], starting with the works of Novikov, Buchstaber and Quillen; among the generalized cohomology theories the complex cobordism is characterized by the so-called universal group law; moreover the usage is recently paralleled in the theory of [[algebraic cobordism]] of Morel and Levine in [[algebraic geometry]].  Formal groups are also useful in local class field theory; they can be used to explicitly construct the local Artin map according to Lubin and Tate.

Much more general are formal group schemes from

* Grothendieck et al. SGA III, vol. 1, Expose VIIB (P. Gabriel) ETUDE INFINITESIMALE DES SCHEMAS EN GROUPES (part B) 474-560 

__Formal group schemes__ are simply the group objects in a category of [[formal schemes]]; however usually only the case of the formal spectra of complete $k$-algebras is considered; this category is equivalent to the category of complete cocommutative $k$-[[Hopf algebras]]. For a generalization over [[operads]] see

* B. Fresse, _Lie theory of formal groups over an operad_, J. Alg. __202__, 455--511, 1998. 

Formal geometry is closely related also to the *rigid* [[analytic geometry]].

(nlab remark: we should explain connections to the Witt rings, Cartier/Dieudonn&#233; modules).

[[!redirects formal groups]]
[[!redirects formal group scheme]]
[[!redirects formal group schemes]]
[[!redirects formal group law]]