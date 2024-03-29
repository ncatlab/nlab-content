
* tic
{: toc}

## Idea

The notion of *variety of algebras* is a classical notion from [[universal algebra]] that subsumes nearly all of the usual kinds of [[algebra|algebraic]] objects, such as [[groups]], [[rings]], [[vector spaces]] (over a fixed [[field]]), and so on.  Those algebraic objects that do not form a variety of algebras, such as [[fields]], can still usually be easily described as a subcategory of some variety of algebras (in this case, [[commutative rings]]).

A variety of algebras is not to be confused with an [[algebraic variety]], although in fact there is a connection: both concepts are (roughly speaking) given by a set of equations, but an algebraic variety is the set of elements (of a fixed generic structure) that satisfy the equations, while a variety of algebras is the class of structures in which *every* element satisfies the equations.


##  Definitions

A __signature__ (in this context) is a [[set]], whose elements are called __operations__, to each of which is assigned a [[cardinal number]] ($0, 1, 2, \ldots$) called its [[arity]].  A signature is __finitary__ if its set of operations is [[finite set|finite]] (in the strictest sense for the purposes of [[constructive mathematics]]) and every arity is finite (so a [[natural number]]); similar definitions apply to other [[arity classes]].  Given a signature $\sigma$ and a set $V$, whose elements are called __variables__[^1], a __word__ (in $\sigma$ using $V$) is a (well-founded directed rooted) [[tree]] in which each node is labelled by either a variable or an operation, such that every node labelled by a variable has no branches away from the root and every node labelled by an operation $o$ has as many branches away from the root as the arity of $o$.  An __axiom__ (in $\sigma$ using $V$) is a pair of such words; we write the axiom consisting of the words $v$ and $w$ as $v = w$ or $\vdash v = w$.  A __theory__ (in our sense) consists of a signature $\sigma$ and a set of axioms in $\sigma$.  An algebraic theory is __finitary__ if its signature is finitary and its set of equational axioms is finite ([[Kuratowski-finite]] in constructive mathematics); analogous remarks apply to other arity classes.

[^1]: For a finitary signature, we may without loss of generality use the set $V \coloneqq \{x_0, x_1, x_2, \ldots\}$, effectively the set of [[natural numbers]], as the only set of variables; similar remarks apply to other arity classes.

A __variety of algebras__ is given precisely by a theory in this sense, but it is more usual to think of the variety as being the class (or [[category]]) of models, so we continue with the definitions.

Given a theory $T$, a __model__ or __algebra__ of $T$ consists of a [[set]] $A$ together with, for each operation of $T$ with arity $\kappa$, a [[function]] to $A$ from its $\kappa$th [[cartesian power]] $A^\kappa$ such that, for each axiom $\vdash v = w$ and each assignment of elements of $A$ to the variables in that axiom, the equation holds that is given by applying the operations to the elements of $A$ as indicated by the trees defining $v$ and $w$ (the meaning of which we hope is obvious).  We say that $A$ __carries__ the operations and __satisfies__ the axioms.

Given a algebras $A$ and $B$ of the same (quasi)-algebraic theory, a __homomorphism__ from $A$ to $B$ consists of a [[function]] $f\colon A \to B$ such that, for each operation, the diagram
$$ \array {
   A^\kappa   & \stackrel{f^\kappa}\rightarrow & B^n \\
   \downarrow &                                & \downarrow \\
   A          & \stackrel{f}\rightarrow        & B
} $$
commutes.  We say that $f$ __preserves__ the operations.

It is fairly straightforward to define a model (and homomorphisms) in any [[cartesian monoidal category]] $C$, replacing [[Set]] in the two paragraphs above.  But note that the operations and axioms still form sets, not objects of $C$; the theory $T$ is independent of the modelling category.  In any case, given any theory $T$ and any cartesian monoidal category $C$, the models of $T$ in $C$ (as [[objects]]) and the homomorphisms between them (as [[morphisms]]) form a [[category]], which is the __variety of $T$-algebras in $C$__.


## Generalisations

A __sorted variety__ or __many-sorted variety__ is a generalisation.  A __sorted signature__ or __many-sorted signature__ consists of a set, whose elements are called __sorts__, together with operations and arities as before, except that now an arity is a [[list]] of __input__ sorts instead of merely a natural number (the length of the list) together with one __output__ sort.  Each variable in an axiom comes equipped with a sort, which we may also classify as an output sort; then each branch in (the tree reprsenting) a word must link output sort to input sort.  The root of a word gives the entire word a sort; the two words in an equational axiom must have the same sort.  Then a model of a sorted variety consists of one set for each sort, and the rest should be obvious.  A sorted variety is __finitary__ if it satisfies the finitarity conditions of a variety and its set of sorts is also finite.  An ordinary variety as above may be called __unsorted__ or __single-sorted__ to avoid invoking the [[red herring principle]]; it is the same thing as a sorted variety with exactly one sort.

Another generalisation is a __quasivariety__.  While an axiom in a variety gives an equation, an axiom in a quasivariety is a [[Horn clause]], stating that one equation (the __consequent__) holds whenever each equation in some set of equations (the __premises__) holds.  A Horn clause is __finitary__ if this set of premises is (Kuratowski)-finite; a quasivariety is __finitary__ if it satisfies the fintarity conditions of a variety and additionally each Horn clause is finitary.  An ordinary variety is a quasivariety in which each Horn clause has an [[empty set]] of premises.


##  Examples

For each definition of an appropriate algebraic object, there is a corresponding variety of algebras, a few of which are given below:

*  The variety of _[[groups]]_ is given by a theory with three operations $m,e,i$ (traditionally called multiplication, identity, and inverse), with respective arities $2,0,1$ (so multiplication is a binary operation, identity is a nullary operation, and inverse is a unary operation).  There are five axioms, given by the following pairs of trees (with their traditional names):

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

   Then a model of this variety is a set $A$ together with functions $m\colon A^2 \to A$, $e\colon 1 \to A$ (which may be identified with an element of $A$), and $i\colon A \to A$ such that, for all $x,y,z$ in $A$, $m(m(x,y),z) = m(x,m(y,z))$, $m(e,x) = x$, $m(x,e) = x$, $m(x,i(x)) = e$, and $m(i(x),x) = e$.  In other words, an algebra in this variety is simply a [[group]].  Similarly, a homomorphism of such algebras is simply a [[group homomorphism]].  Also, an algebra in this variety in the category $C$ is a [[group object]] in $C$.

Note that it is not necessary to draw explicit trees; these can be recovered from the succinct equations like $m(m(x,y),z) = m(x,m(y,z))$; we will do this below.

*  The variety of _[[monoids]]_ is given by a subtheory of the theory of groups.  It has only the operations $m,e$ and the axioms (eq:ass),(eq:runit),(eq:lunit).  An algebra in this theory is a monoid, and a homomorphism of such algebras is a monoid homomorphism (including the condition that it preserve the identity).

*  There is no variety of _[[cancellative monoid]]s_, but there is a quasivariety of them.  In addition to the axioms for a monoid, we have an axiom stating that the equation $x = y$ follows from the equation $m(x,z) = m(y,z)$, which we write succinctly as $m(x,z) = m(y,z) \vdash x = y$.

*  The variety of _[[abelian groups]]_ is given by a supertheory of the theory of groups.  In addition to the operations and axioms of the variety of groups, it has an additional axiom, the commutative law: $m(x,y) = m(y,x)$.

*  The variety of (associative unital) _[[rings]]_ has five operations $a,z,n,m,e$, with respective arities $2,0,2,0,1$, and ten axioms.  Five of these axioms are those of groups, applied to $a,z,n$ in place of $m,e,i$; three of these axioms are those of monoids (applied to $m,e$ as before).  The remaining two axioms are:
   *  left distributive law:  $m(x,a(y,z)) = a(m(x,y),m(x,z))$,
   *  right distributive law:  $m(a(x,y),z) = a(m(x,z),m(y,z))$.

*  There is no variety or quasivariety of [[fields]]; the elements with multiplicative inverses are not identified by an equation.  One can, however, define fields as certain rings and then get the correct notion of field homomorphism as a ring homomorphism between rings that happen to be fields.

*  The variety of (real) _[[vector spaces]]_ has infinitely many operations and axioms (so is not finitary).  First, there are operations $a,z,n$ with the arities and axioms of an abelian group (as with rings).  In addition, there is one operation $m_r$ of arity $1$ for each [[real number]] $r$, satisfying these axioms:
   *  left distributive law:  for each real number $r$, $m_r(a(x,y)) = a(m_r(x),m_r(y))$,
   *  right distributive law:  for each real number $r$ and real number $s$, $m_{r+s}(x) = a(m_r(x),m_r(y))$ (where $r + s$ is the sum of $r$ and $s$ as real numbers),
   *  associative law:  for each real number $r$ and real number $s$, $m_{r s}(x) = m_r(m_s(x))$ (where $r s$ is the product of $r$ and $s$ as real numbers),
   *  unit law:  $m_1(x) = x$ (where $1$ the real number [[1]]).

*  There is a similar variety of vector spaces over any given [[ground field]], but there is no variety of vector spaces over arbitrary fields, since we would have to specify the field as well as the vector space.  The problem is not really that there is no variety of fields; there is no variety of (left) [[modules]] over arbitrary [[commutative rings]] either.  However, there is a _sorted_ variety of modules over arbitrary rings, with two types, one for the ring and one for the module.  Even though this variety includes the non-finitary variety of real vector spaces, it is itself a finitary sorted variety.


##  As algebraic theories

A variety of algebras is one way to look at an [[algebraic theory]].

As a [[logic]]al theory, everything that we wish to say can be said in (typed or untyped, to match the variety) [[cartesian logic]] (although one might want to use something stronger, such as full classical or intuitionistic predicate logic with equality).  We use one function symbol (of matching arity) for each operation, and each axiom in the variety becomes an axiom in the logic, a universally quantified equation.  Then the [[models]] of this logical theory are the same as the algebras in the variety.

As a [[Lawvere theory]], an untyped finitary variety of algebras defines a category $L$ whose objects are of the form $A^n$ for $n$ a natural number.  The morphisms of the category are those which are necessary to make $A^n$ the $n$-fold [[product]] of $A$, along with one morphism for each operation in the variety.  Each axiom of the variety corresponds to a commutative diagram, and $L$ is freely generated by these as a [[sketch]].  Then the models of the variety in a cartesian monoidal category $C$ are the same as the [[product-preserving functor|product-preserving]] functors from $L$ to $C$.  Conversely, any [[locally small category|locally small]] (and hence [[small category|small]]) cartesian monoidal category whose objects are all of the form $A^n$ may be thought of as a Lawvere theory and defines an untyped variety of algebras, with operation for each morphism to $A$ and one axiom for each commutative diagram.  (This can all be generalised to sorted varieties as well.)

A variety of algebras can be seen as a cartesian version of a (typed or untyped) [[operad]]; whereas an operad has models in any [[symmetric monoidal category]], a variety of algebras has models only in a cartesian monoidal category.

A variety of algebras is traditionally identified with its category $M$ of models in $Set$ (or even with simply the [[class]] of objects of this category), but it then becomes unclear what an algebra in the variety would be in some other category $C$.  However, it is worth noting that $M$ is always an [[algebraic category]]; see below for the construction of free objects.


## Free algebras

Given a variety $V$ and a [[cartesian monoidal category]] $C$ (such as $Set$), let $C^V$ be the category of algebras in $V$ in $C$, with homomorphisms as morphisms.  There is an obvious [[forgetful functor]] $U\colon C^V \to C$; $C$ is a [[cocomplete category|cocomplete]] $W$-[[W-pretopos|pretopos]] (or if $C$ is just a $W$-pretopos if $V$ is finitary), then $U$ has a [[left adjoint]], the [[free functor]] $F\colon C \to C^V$.  In fact, this adjunction is [[monadic adjunction|monadic]]; we can identify the models of $V$ in $C$ with the [[module of a monad|modules/algebras]] of the [[monad]] $U \circ F$.

Given an object $A$ of $C$, we construct the free algebra $F(A)$ as follows.  First, let $W(A)$ be the [[inductive type]] in $C$ given by the signature of $V$, that is the [[initial algebra]] of the [[endofunctor]] $A \mapsto \sum_o A^{\#o}$, where $o$ ranges over the operations of $V$ and $\#o$ is the arity of $o$.  Then each axiom specifies an internal binary [[relation]] on $W(A)$; the [[colimit]] of these is $F(A)$.  Note that, if $C$ is $Set$ and $A$ is a set, then $W(A)$ consists precisely of the words (defined as trees above) with variables from $A$.

The __word problem__ for a variety $V$ consists of deciding, whenever $A$ is a [[finite set]], whether two elements of $W(A)$ are equal in $F(A)$.  As a problem in algorithmic decidability, the word problem can be very difficult; for example, it is:

*  trivial for [[Boolean algebras]],
*  impossible for [[Heyting algebras]],
*  nontrivial but possible for [[lattices]],

even though each of these is a supertheory of the next.

## Literature

* [[Jiří Adámek]], [[Lawvere|F.W. Lawvere]], J. Rosick&#253;, _On the duality between varieties and algebraic theories_, Algebra universalis 2003, __49__:1, pp 35&#8211;49 [doi](https://doi.org/10.1007/s000120300002)

[[!redirects variety of algebras]]
[[!redirects varieties of algebras]]
[[!redirects quasivariety of algebras]]
[[!redirects quasivarieties of algebras]]

[[!redirects word problem]]
[[!redirects word problems]]
