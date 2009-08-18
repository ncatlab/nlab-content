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


##  Examples

For each definition of an appropriate algebraic object, there is a corresponding variety of algebras, a few of which are given below:

*  The variety of _groups_ has three operations $m,e,i$ (traditionally called multiplication, identity, and inverse), with respective arities $2,0,1$.  There are five axioms, given by the following pairs of trees (with their traditional names):

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

   Then a model of this variety is a set $A$ together with functions $m: A^2 \to A$, $e: 1 \to A$ (which may be identified with an element of $A$), and $i: A \to A$ such that, for all $x,y,z$ in $A$, $m(m(x,y),z) = m(x,m(y,z))$, $m(e,x) = x$, $m(x,e) = x$, $m(x,i(x)) = e$, and $m(i(x),x) = e$.  In other words, a model of this variety is simply a [[group]].  Similarly, a homomorphism of such models is simply a group homomorphism.

Note that it is not necessary to draw explicit trees; these can be recovered from the succinct equations like $m(m(x,y),z) = m(x,m(y,z))$; we will do this below.

*  The variety of _monoids_ is a subvariety of the variety of groups.  It has only the operations $m,e$ and the axioms (eq:ass),(eq:runit),(eq:lunit).  A model of this variety is a [[monoid]], and a homomorphism of such models is a monoid homomorphism (including the condition that it preserve the identity).

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


##  As algebraic theories

...