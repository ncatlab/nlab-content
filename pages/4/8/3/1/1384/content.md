<div class="rightHandSide toc">
[[!include higher algebra - contents]]
</div>

#Idea#

Recall the pattern in ordinary [[algebra]]:

* In a [[monoidal category]] one can consider [[monoid]] or [[algebra]] objects.

* In a [[symmetric monoidal category]] one can consider commutative [[monoid]] or [[algebra]] objects.

Accordingly in [[higher algebra]]:

* In a [[monoidal (infinity,1)-category]] one can consider [[algebra in an (infinity,1)-category]].

* In a [[symmetric monoidal (infinity,1)-category]] one can consider commutative algebra objects.

#Definition#

A **commutative algebra object** in a [[symmetric monoidal (infinity,1)-category]] $C$ is a lax symmetric monoidal $(\infty,1)$-functor

$$
  * \to C
  \,.
$$

In more detail, this means the following:


+-- {: .un_defn}
###### Definition

Given a [[symmetric monoidal (infinity,1)-category]] in its [[quasi-category|quasi-categorical]] incarnation as a coCartesian fibration of [[simplicial set]]s

$$
  p : C^\otimes \to N(FinSet_*)
$$

a **commutative algebra object** in $C$ is a [[section]]

$$
  A : N(FinSet_*) \to C^\otimes
$$

such that $A$ carries collapsing morphisms in $FinSet_*$ to coCartesian morphisms in $C^\otimes$.

=--




#Examles#

* A commutative algebra object in the [[stable (infinity,1)-category of spectra]] is a [[commutative ring spectrum]] or [[E-infinity ring]].


#References#

the above definition is definition 1.19 in

* [[Jacob Lurie]], [[higher algebra|Commutative algebra]]

[[!redirects commutative algebra in an (∞,1)-category]]
[[!redirects commutative monoid in an (∞,1)-category]]
[[!redirects commutative monoid in an (infinity,1)-category]]
[[!redirects commutative algebra in a monoidal (∞,1)-category]]
[[!redirects commutative monoid in a monoidal (∞,1)-category]]