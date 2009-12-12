# Varieties of algebras
* tic
{: toc}


## Idea

A variety of algebras (not to be confused with an [[algebraic variety]]) is a classical notion from [[universal algebra]] that includes nearly all of the usual kinds of algebraic objects, such as [[groups]], [[rings]], [[vector spaces]] (over a fixed [[field]]), and so on.  Those algebraic objects that don\'t form a variety of algebras, such as [[fields]], can still usually be easily described as a subclass of an algebraic variety (in this case, [[commutative rings]]).


##  Definitions

A __signature__ (in this context) is a [[set]] of __operations__, each of which is assigned a [[natural number]] ($0, 1, 2, \ldots$) called its __arity__.  Given a signature $\sigma$ and a set of __variables__, a __word__ is a (well-founded directed rooted) [[tree]] in which each node is labelled by either a variable or an operation, such that every variable-labelled node has no branches away from the root and every operation-labelled node has as many branches away from the root as the operation\'s arity.  An __axiom__ in a given signature is a pair of words in that signature.

Then a __variety of algebras__ consists of a signature and a set of axioms in that signature.

Given a variety $V$ of algebras, a __model__ or __algebra__ of $V$ consists of a [[set]] $A$ together with, for each operation of $V$ with arity $n$, a [[function]] to $A$ from its $n$-fold [[cartesian product]] $A^n$ such that, for each axiom and each assignment of elements of $A$ to the variables in that axiom, the equation holds that is given by applying the operations to the elements of $A$ as indicated by the tree.  We say that $A$ __carries__ the operations and __satisfies__ the axioms.

Given a algebras $A$ and $B$ of the same variety, a __homomorphism__ from $A$ to $B$ consists of a [[function]] $f: A \to B$ such that, for each operation, the diagram
$$ \array {
   A^n        & \stackrel{f^n}\rightarrow & B^n \\
   \downarrow &                           & \downarrow \\
   A          & \stackrel{f}\rightarrow   & B
} $$
commutes.  We say that $f$ __preserves__ the operations.

It is fairly straightforward to define a model (and homomorphisms) in any [[cartesian monoidal category]] $C$, replacing [[Set]] in the above.  But note that the operations and axioms still form sets, not objects of $C$; the variety itself is independent of the modelling category.

A __typed variety__ is a generalisation.  A __typed signature__ consists of a set of __types__, together with operations and arities as before, except that now an arity is a [[list]] of __input__ types instead of merely a natural number (the length of the list) together with one __output__ type.  Each variable in an axiom comes equipped with a type, which we may also classify as an output type; then each branch in (the tree reprsenting) a word must link output type to input type.  The root of a word gives the entire word a type; the two words in an axiom must have the same type.  Then a model of a typed variety consists of one set for each type, and the rest should be obvious.  An ordinary variety as above may be called an __untyped variety__ to avoid invoking the [[red herring principle]]; it is the same thing as a typed variety with exactly one type.  (This paragraph may be original research.  Probably the concept does appear in the literature but under a different name.)

Another generalisation is a __quasivariety__.  While an axiom in a variety gives an equation, an axiom in a quasivariety is a [[conditional statement]] stating that one equation holds if some (generally finite) collection of equations holds.


##  Examples

For each definition of an appropriate algebraic object, there is a corresponding variety of algebras, a few of which are given below:

*  The variety of _groups_ has three operations $m,e,i$ (traditionally called multiplication, identity, and inverse), with respective arities $2,0,1$ (so multiplication is a binary operation, identity is a nullary operation, and inverse is a unary operation).  There are five axioms, given by the following pairs of trees (with their traditional names):

   *  associative law:
      \[ \label{ass} \array {
           &          &   &          & m \\
           &          &   & \nearrow &   & \nwarrow \\
           &          & m &          &   &          & z \\
           & \nearrow &   & \nwarrow \\
         x &          &   & y
      } \;\;\;=\;\;\; \array {
           &          & m \\
           & \nearrow &   & \nwarrow \\
         x &          &   &          & m \\
           &          &   & \nearrow &   & \nwarrow \\
           &          & y &          &   &          & z
      } \]
   *  right unit law:
      \[ \label{runit} \array {
           &          & m \\
           & \nearrow &   & \nwarrow \\
         x &          &   &          & e
      } \;\;\;=\;\;\; \array {
         x
      } \]
   *  left unit law:
      \[ \label{lunit} \array {
           &          & m \\
           & \nearrow &   & \nwarrow \\
         e &          &   &          & x
      } \;\;\;=\;\;\; \array {
         x
      } \]
   *  right inverse law:
      \[ \label{rinv} \array {
           &          & m \\
           & \nearrow &   & \nwarrow \\
         x &          &   &          & i \\
           &          &   &          & \uparrow \\
           &          &   &          & x
      } \;\;\;=\;\;\; \array {
         e
      } \]
   *  left inverse law:
      \[ \label{linv} \array {
                  &          & m \\
                  & \nearrow &   & \nwarrow \\
         i        &          &   &          & x \\
         \uparrow \\
         x
      } \;\;\;=\;\;\; \array {
         e
      } \]

   Then a model of this variety is a set $A$ together with functions $m: A^2 \to A$, $e: 1 \to A$ (which may be identified with an element of $A$), and $i: A \to A$ such that, for all $x,y,z$ in $A$, $m(m(x,y),z) = m(x,m(y,z))$, $m(e,x) = x$, $m(x,e) = x$, $m(x,i(x)) = e$, and $m(i(x),x) = e$.  In other words, a model of this variety is simply a [[group]].  Similarly, a homomorphism of such models is simply a group homomorphism.  Also, a model of this variety in the category $C$ is a [[group object]] in $C$.

Note that it is not necessary to draw explicit trees; these can be recovered from the succinct equations like $m(m(x,y),z) = m(x,m(y,z))$; we will do this below.

*  The variety of _monoids_ is a subvariety of the variety of groups.  It has only the operations $m,e$ and the axioms (eq:ass),(eq:runit),(eq:lunit).  A model of this variety is a [[monoid]], and a homomorphism of such models is a monoid homomorphism (including the condition that it preserve the identity).

*  There is no variety of _cancellative monoids_, but there is a quasivariety of them.  In addition to the axioms for a monoid, we have an axiom stated that the equation $x = y$ follows from the equation $m(x,z) = m(y,z)$.

*  The variety of _abelian groups_ is a supervariety of the variety of groups.  In addition to the operations and axioms of the variety of groups, it has an additional axiom, the commutative law: $m(x,y) = m(y,x)$.  A model of this variety is an [[abelian group]].

*  The variety of (associative unital) _[[rings]]_ has five operations $a,z,n,m,e$, with respective arities $2,0,2,0,1$, and ten axioms.  Five of these axioms are those of groups, applied to $a,z,n$ in place of $m,e,i$; three of these axioms are those of monoids.  The remaining two axioms are:
   *  left distributive law:  $m(x,a(y,z)) = a(m(x,y),m(x,z))$,
   *  right distributive law:  $m(a(x,y),z) = a(m(x,z),m(y,z))$.

*  There is no variety of [[fields]]; there is no way to say that only *some* elements have multiplicative inverses.  One can, however, define fields as certain rings and then get the correct notion of field homomorphism as a ring homomorphism between rings that happen to be fields.

*  The variety of (real) _[[vector spaces]]_ has infinitely many operations and axioms.  First, there are operations $a,z,n$ with the arities and axioms of an abelian group (as with rings).  In addition, there is one operation $m_r$ of arity $1$ for each [[real number]] $r$, satisfying these axioms:
   *  left distributive law:  for each real number $r$, $m_r(a(x,y)) = a(m_r(x),m_r(y))$,
   *  right distributive law:  for each real number $r$ and real number $s$, $m_{r+s}(x) = a(m_r(x),m_r(y))$ (where $r + s$ is the sum of $r$ and $s$ as real numbers),
   *  associative law:  for each real number $r$ and real number $s$, $m_{r s}(x) = m_r(m_s(x))$ (where $r s$ is the product of $r$ and $s$ as real numbers),
   *  unit law:  $m_1(x) = x$ (where $1$ the real number unity).

*  There is a similar variety of vector spaces over any given field, but there is no variety of vector spaces over arbitrary fields, since we would have to specify the field as well as the vector space.  The problem is not really that there is no variety of fields; there is no variety of (left) [[modules]] over arbitrary rings either.  However, there is a _typed_ variety of modules over arbitrary rings, with two types, one for the ring and one for the module.  This has only finitely many operations and axioms, which you should be able to list for yourself by now.


##  As algebraic theories

A variety of algebras is one way to look at an [[algebraic theory]].

As a [[logic]]al theory, everything that we wish to say can be said in (typed or untyped, to match the variety) [[cartesian logic]] (although one might want to use something stronger, such as full classical or intuitionistic predicate logic with equality).  We use one function symbol (of matching arity) for each operation, and each axiom in the variety becomes an axiom in the logic, a universally quantified equation.  Then the models of this logical theory are the same as the models of the variety.

As a [[Lawvere theory]], an untyped variety of algebras defines a category $L$ whose objects are of the form $A^n$ for $n$ a natural number.  The morphisms of the category are those which are necessary to make $A^n$ the $n$-fold [[product]] of $A$, along with one morphism for each operation in the variety.  Each axiom of the variety corresponds to a commutative diagram, and $L$ is freely generated by these as a [[sketch]].  Then the models of the variety in a cartesian monoidal category $C$ are the same as the [[product-preserving functor|product-preserving]] functors from $L$ to $C$.  Conversely, any [[locally small category|locally small]] (and hence [[small category|small]]) cartesian monoidal category whose objects are all of the form $A^n$ may be thought of as a Lawvere theory and defines an untyped variety of algebras, with operation for each morphism to $A$ and one axiom for each commutative diagram.  (This can all be generalised to typed varieties as well.)

A variety of algebras can be seen as a cartesian version of a (typed or untyped) [[operad]]; whereas an operad has models in any [[symmetric monoidal category]], a variety of algebras has models only in a cartesian monoidal category.

Sometimes a variety of algebras is identified with its category $M$ of models in $Set$, but this is probably not wise, and it then becomes unclear what a model of the variety would be in some other category $C$.  However, it is worth noting that $M$ is always an [[algebraic category]]; see below for the construction of free objects.


## Free algebras

Given a variety $V$ and a [[cartesian monoidal category]] $C$ (such as $Set$), let $C^V$ be the category of models of $V$ in $C$, with homomorphisms as morphisms.  There is an obvious [[forgetful functor]] $U: C^V \to C$; $C$ is a [[cocomplete category|cocomplete]] $W$-[[W-pretopos|pretopos]] (or if $C$ is just a $W$-pretopos if $V$ has only finitely many operations and axioms), then $U$ has a [[left adjoint]], the [[free functor]] $F: C \to C^V$.  In fact, this adjunction is [[monadic adjunction|adjunction]]; we can identify the models of $V$ in $C$ with the [[module of a monad|modules/algebras]] of the [[monad]] $U \circ F$.

Given an object $A$ of $C$, we construct the free algebra $F(A)$ as follows.  First, let $W(A)$ be the [[inductive type]] in $C$ given by the signature of $V$, that is the [[initial algebra]] of the [[endofunctor]] $A \mapsto \sum_o A^{\#o}$, where $o$ ranges over the operations of $V$ and $\#o$ is the arity of $o$.  Then each axiom specifies an internal binary [[relation]] on $W(A)$; the [[colimit]] of these is $F(A)$.  Note that, if $C$ is $Set$ and $A$ is a set, then $W(A)$ consists precisely of the words (defined as trees above) with variables from $A$.

The __word problem__ for a variety $V$ consists of deciding, whenever $A$ is a [[finite set]], whether two elements of $W(A)$ are equal in $F(A)$.  As a problem in algorithmic decidability, the word problem can be very difficult; for example, it is:

*  trivial for [[Boolean algebras]],
*  impossible for [[Heyting algebras]],
*  nontrivial but possible for [[lattices]],

even though each of these is a subvariety of the next.


[[!redirects word problem]]
[[!redirects quasivariety of algebras]]
[[!redirects varieties of algebras]]
[[!redirects quasivarieties of algebras]]