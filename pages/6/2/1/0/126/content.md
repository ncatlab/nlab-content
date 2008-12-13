Given a [[category]] $C$, a _subcategory_ $D$ consists of a subcollection of the collection of [[object|objects]] of $C$ and a subcollection of the collection of [[morphism|morphisms]] of $D$ such that:

* If the morphism $f : x \to y$ is in $D$, then so are $x$ and $y$.

* If $f : x \to y$ and $g : y \to z$ are in $D$, then so is the [[composition|composite]] $g f : x \to z$.  

* If $x$ is in $D$ then so is the [[identity]] morphism $1_x$.

These conditions ensure that $D$ is a category in its own right.  We say $D$ is a [[full]] subcategory if additionally 

* If $x$ and $y$ are in $D$, every morphism $f : x \to y$ is in $D$.

More generally, one may define a _subcategory_ of $C$ as a category $D$ equipped with a [[faithful]] [[functor]] $F: D \to C$. This is the same as a subcategory (in the sense above) of a category [[equivalence|equivalent]] to $C$.  In these terms, we define a _full subcategory_ to be a category equipped with a [[full]] and [[faithful]] functor $F : D \to C$.

