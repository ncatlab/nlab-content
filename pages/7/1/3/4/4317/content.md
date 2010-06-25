## The idea ##

A [[rig]] is a 'ring without negatives'.
[[categorification|Categorifying]] this notion, we obtain the notion of 'rig category'.  A typical example would be the [[groupoid]] of [[finite set|finite sets]] and [[bijection|bijections]], with disjoint union playing the role of addition and the ordinary product of sets playing the role of multiplication.  This rig category can be thought of as a categorification of the natural numbers.  Note that in this example, disjoint union is _not_ the categorical coproduct, and product of sets is _not_ the categorical product.  

So, a **rig category** $C$ is a category with a [[symmetric monoidal category|symmetric monoidal]] structure $(C,\oplus,0)$ for addition and a [[monoidal category|monoidal]] structure $(C, \otimes, I)$ for multiplication, together with left and right distributivity natural isomorphisms

$$ d_\ell : x \otimes (y \oplus z) \to 
(x \otimes y) \oplus (x \otimes z) $$

$$ d_r : (x \oplus y) \otimes z \to 
(x \otimes z) \oplus (y \otimes z) $$

satisfying a set of coherence laws worked out by Kelly and Laplaza:

* M. Laplaza, Coherence for distributivity, _Lecture Notes in Mathematics_ **281**, Springer Verlag, Berlin, 1972, pp. 29-72.

* G. Kelly, Coherence theorems for lax algebras and distributive laws, _Lecture Notes in Mathematics_ *420*, Springer Verlag, Berlin, 1974, pp. 281-375. 

Note that these authors used the term 'ring category'.  We take the liberty of switching to 'rig category' because it is typical for these to lack additive inverses.

While a rig can have the [[property]] of being commutative, a rig category can have the [[structure]] of being [[braided monoidal category|braided]] or [[symmetric monoidal category|symmetric]].  

**Conjecture** ([[John Baez]]):  Using a correct definition of the 2-category of symmetric rig categories, the groupoid $FinSet^{\times}$ of finite sets and bijections is the initial symmetric rig category, just as $\N$ is the initial commutative rig.   Note that a suitably weakened concept of 'initial' is needed here.   In other words, given any symmetric rig category $R$, there is a unique symmetric rig morphism $FinSet^{\times} \to R$, _up to 2-isomorphism_. 