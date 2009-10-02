# Idea

A **structural set theory** is a [[set theory]] in which the elements of a set have no structure apart from their identity as elements of that set.  In particular, they are not themselves sets, and cannot be elements of any other set, so that elements of different sets cannot be compared (unless and until extra structure is imposed).  Structural set theory thus looks very much like [[type theory]].  It is to be contrasted with [[material set theory]], in which the elements of sets can have internal structure, and are often themselves sets.

When viewed as a [[foundations|foundation]] for mathematics, the idea of structural set theory is that sets (together with other attendant concepts such as elements, functions, and relations) are the "raw material" from which mathematical structures are built.  The elements of a set thus have no "structure" until it is given to them by means of functions and relations.

Among category theorists, it's popular to state the axioms of a structural set theory by specifying elementary properties of [[Set|the category of sets]]; the orthodoxy here (to the extent that there is one) is probably Bill Lawvere's [[ETCS]]. It is weaker than ZFC and must be supplemented to handle some esoteric parts of modern mathematics, although it suffices for most everyday uses.  Another structural set theory, which is stronger than ETCS and less closely tied to category theory, is [[SEAR]].

# Semiformal Definition

The following is an attempted formal definition of when a set theory is structural.

## Notions of set

First of all, in order to give a definition pertaining to all set theories, we need to know: what is a set theory?  Probably no theory can *intrinsically* be called a set theory; it is only given that distinction by our intent to regard some of its objects of study as "sets" and others as their "elements."  Thus we make the following definition.

+-- {: .un_defn}
###### Definition
A **notion of set** in a typed first-order theory consists of:

* A type $\mathbb{S}$ called the *type of potential sets*.
* A unary predicate $set(-)$ on $\mathbb{S}$ called *being a set*.
* A type $\mathbb{E}_A$, possibly depending on $A\in\mathbb{S}$, called the *type of potential elements of $A$*.
* A unary predicate $in_A(-)$ on $\mathbb{E}_A$ called *being an element of $A$*.
=--

We have split the notions of sethood and elementhood into both a type and a predicate to allow for variation in theories which model them by one or the other method or a combination.  Here are some examples.

* [[ZF]] is a one-typed theory; we call the objects in the one type  "ZF-sets" for clarity.  The type of ZF-sets is the type of potential sets, and we take the predicate $set(-)$ to be $\top$ (every potential set is a set).  For such a set $A$, the type of potential elements of $A$ must once again be the type of ZF-sets, and the elementhood predicate is simply $in_A(x) \equiv (x\in A)$.

* ZF can be augmented by the presence of [[urelement|urelements]] or atoms.  One way to represent this is with two types, the type of ZF-sets and the type of ZF-atoms.  Again we take the type of ZF-sets to be the type of potential sets, and the sethood predicate $set(-)$ is $\top$.  The type of potential elements of $A$ is now the sum type (ZF-sets + ZF-atoms), with the membership predicate again being the ordinary membership predicate of $A$.

* Atoms can be added to ZF in another way: we maintain only a single type, say the type of "ZF-objects," but we add a "sethood" predicate which distinguishes the sets from the atoms.  Now the type of potential sets is of course the type of ZF-objects, and the predicate $set(-)$ is the ZF-sethood predicate.

* In [[NBG]] or [[MK]] set-class theory, there are two possible "notions of set": the sets and the classes.  The way to formalize this depends on how the set-class theory is stated.  For instance, one way to state NBG is with a single type of classes, defining a class $A$ to be an NBG-set when $A\in B$ for some class $B$.  In this case the sethood predicate (for the "NBG-set" notion of set) will be $set(A) \equiv (\exists B. A\in B)$.

* In [[SEAR]], which is a dependently typed theory, we take the type of potential sets to be the type of SEAR-sets, with the sethood predicate $set(-)$ being again $\top$.  For each set $A$, of course $\mathbb{E}_A$ is the type of SEAR-elements of $A$.  (In contrast to ZF, these types are now nontrivially dependent on $A$.)  The elementhood predicate is $\top$, since every object in the type of SEAR-elements of $A$ is an element of $A$ by definition (that is, in SEAR elementhood is a typing assertion).

* In the variant of SEAR without primitive equality (and thus also in [[SEAR+ε]]), the type of potential sets is the type of "SEAR-sets equipped with an endo-relation" (a [[dependent sum]] type).  The sethood predicate $set(A,R)$ then asserts that $R$ is an equivalence pre-relation, with the other structure as in ordinary SEAR.

* Since [[ETCS]] is an extension of the first-order theory of a [[category]], it can be stated in several ways.

   * If ETCS is stated with two types (objects and arrows), then the type of potential sets is the type of objects (i.e. ETCS-sets) and the sethood predicate is $\top$.  The type of potential elements of each set $A$ is the type of arrows (i.e. ETCS-functions), and $in_A(x)$ holds when the target of $x$ is $A$ and its source is a [[terminal object]].

   * If ETCS is stated with [[single-sorted definition of a category|one type]], then the type of potential sets is that type, the sethood predicate is $set(A) \equiv (A=s(A))$, the type of potential elements is of course again the single type, and the elementhood predicate is as in the two-typed version.

   * If ETCS is stated with dependent types (a type $hom(A,B)$ for every pair of objects $A$ and $B$), then the type of potential sets is the type of objects, the sethood predicate is $\top$, the type of potential elements of $A$ is $hom(1,A)$, and the elementhood predicate is $\top$.

## Structural Presentation

Now we make the following definition.

+-- {: .un_defn}
###### Definition
A notion of set in a typed first-order theory is called **structurally presented** if for any first-order formula $\varphi$ containing free variables $A:\mathbb{S}$ and $x:\mathbb{E}_A$ (and possibly others), if the only free occurrances of $A$ in $\varphi$ is in the (possibly) dependent type $\mathbb{E}_A$ of the variable $x$, then
$$(\forall \vec{z})(\forall A:\mathbb{S})(\forall x,y:\mathbb{E}_A) \Big(in_A(x) \wedge in_A(y) \Rightarrow \big(\varphi \Leftrightarrow \varphi[y/x]\big)\Big) \qquad (\star)$$
holds (where $\vec{z}$ denotes all the other free variables of $\varphi$).
=--

Equation $(\star)$ says that all elements of any set $A$ are completely indistinguishable by the formula $\varphi$.  This is intended to approximate the idea of a structural set theory: the elements of $A$ have no independent structure (and thus cannot be distinguished from each other) apart from their identity as elements of $A$.  Of course, we can't do mathematics without some way to distinguish the elements of a set, but the idea of structural set theory is that this happens only through external structure imposed *on* the set, such as functions and relations, rather than through intrinsic properties of the elements themselves.  This is the idea behind the restrictions placed on $\varphi$.

Before we go on, let's first see that ZF is definitely *not* structurally presented.  Let $A=\{\emptyset, \{\emptyset\}\}$ be the von Nemuann numeral $2$, and let $\varphi \equiv (x = \emptyset)$.  Clearly there are some $x\in A$ such that $\varphi$ holds and others such that it fails, so $(\star)$ is false.  Moreover, $\varphi$ satisfies the condition: $A$ does not occur in it at all.  For the same reasons, NBG and MK are not structurally presented.

Now, why can't we do the same thing in a structural set theory?  Consider SEAR, and let $A$ be a set containing two distinct elements $a$ and $a'$.  By analogy to what we did in ZF, we'd like to take $\varphi \equiv (x = a)$, but in SEAR this violates the required condition: $a$ must also be an element of $\mathbb{E}_A$, so $A$ appears elsewhere in $\varphi$ than in the type of $x$ (namely, in the type of $a$).  In fact, we can show:

+-- {: .un_theorem}
###### Theorem
SEAR is structurally presented.
=--
+-- {: .proof}
###### Proof
Let $\varphi$ be a formula as in the above definition.  Since it does not contain $A$ free (except in the type of $x$), it cannot contain any variables (free *or* bound) denoting elements of $A$ (other than $x$) or relations whose source or target is $A$.  But the only atomic formulas in the language of SEAR are equalities of set-elements, equalities of relations, and assertions that a relation holds of a pair of set-elements, and SEAR has no term constructors that could produce an element of some other set from an element of $A$.  Thus, the only atomic formula involving $x$ that can appear in $\varphi$ is $x=x$, whose truth is clearly independent of the value of $x$.  It follows that the truth value of $\varphi$ must also be so.
=--

For similar reasons, we have:

+-- {: .un_theorem}
###### Theorem
When ETCS is written with dependent hom-types, it is structurally presented.
=--
+-- {: .proof}
###### Proof
Let $\varphi$ be a formula as above.  Similarly to the case of SEAR, $\varphi$ cannot contain any variables other than $x$ that denote functions whose source or target is $A$.  Since the only term-constructor in ETCS is function composition, the only terms containing $x$ that can occur in $\varphi$ are composites ending in $x:1\to A$ followed by zero or more applications of $id_A$, such as $x$ itself, $x\circ f$, $\id_A\circ x$, $(x\circ g)\circ h$, or $(id_A\circ x)\circ (i\circ j)$.  Note that all of these terms denote functions with target $A$.  Moreover, the only possible terms denoting functions of target $A$ are terms of this sort, or else composites of some number of copies of $id_A$ (and nothing else).

Now the only atomic formulas of ETCS are equality between parallel function terms.  Since the source of a composite involving $x$ cannot be $A$ (otherwise $A$ would have to occur as the source of the first function-variable in that composite), the only possible such formulas involving $x$ will be equality between two composites containing $x$.  But since $1$ is a terminal object, any two functions that factor through it will always be equal.  Thus, the truth value of such an atomic formula is independent of the value of $x$, and so the truth value of $\varphi$ must also be so.
=--

However, if ETCS is written using a two-sorted or one-sorted definition of a category, then it is not structurally presented.  For instance, we can take the formula
$$\varphi \equiv \big((s(f)=t(x)) \wedge (f\circ x = z)\big)$$
for variables $f$ and $z$ of type "arrow".  This formula does not contain $A$ at all, yet its truth value (for a fixed $f$ and $z$) is not independent of $x$.  This is why we have defined "structurally presented" rather than "structural"---the presentation matters.

It is, however, easy to modify the two- or one-sorted version of ETCS to make it structurally presented: we simply require the equality relation on functions to be decorated by the source and target sets, and the composition operation on functions to be decorated with the set along which composition occurs.  That is, instead of $f=g$ we write $equal(f,g,A,B)$ (which can only hold when $s(f)=s(g)=A$ and $t(f)=t(g)=B$), and instead of $g\circ f$ we write $g\circ_B f$ where $t(f)=s(g)=B$.  Now the same argument as for the dependently-typed version applies.

It would be nice to have a definition according to which any "presentation" of ETCS would be structural; intuitively, a theory should be structural if it is "equivalent" in some sense to a structurally presented one.  However, I haven't yet been able to come up with a notion of "equivalence" which includes the above modifications of ETCS, yet excludes the equivalence between ETCS and BZC (or ZFC and ETCS+R / SEARC).


## Consequences of structural presentation

From our definition of structural presentation we can deduce some of the other standard properties of structural set theories.  The first is that "elements of different sets cannot be compared for equality."

+-- {: .un_theorem}
###### Theorem
If a structurally presented notion of set includes a basic notion of equality between the elements of distinct sets, which is symmetric and transitive, then all of its sets are [[subsingletons]].
=--
+-- {: .proof}
###### Proof
Suppose that we have a basic equality relation that can relate elements of two distinct sets $A$ and $B$.  Thus, for variables $x$ of type $A$ and $z$ of type $B$, we would have an atomic formula $x=z$.  By symmetry and transitivity, if $x=z$ and $x'=z$, then $x=x'$.  But then $(\star)$ applied to $\varphi\equiv (x=z)$ implies that for any $x,y\in A$ we have $x=y$, so $A$ must be a subsingleton.  Since $A$ was arbitrary, all sets must be subsingletons.
=--

The second is "elements of sets are not themselves sets."

+-- {: .un_theorem}
###### Theorem
Suppose that a structurally presented notion of set includes relations $is:\mathbb{E}_A\looparrowright\mathbb{S}$, which we regard as giving a way to interpret some elements as sets.  Suppose moreover that each $\mathbb{E}_A$ has an equality relation, and that $is(x,B)$ and $is(y,B)$ imply $x=y$.  Then for any set $A$, if there exist $a:\mathbb{E}_A$ and $B:\mathbb{S}$ such that $is(a,B)$, then $A$ must be a subsingleton.
=--
+-- {: .proof}
###### Proof
Suppose that $is(a,B)$ and choose $\varphi\equiv is(x,B)$.  By $(\star)$ it follows that $is(x,B)$ holds for all $x:\mathbb{E}_A$, hence $x=y$ for all $x,y:\mathbb{E}_A$, i.e. $A$ is a subsingleton.
=--

Note that the assumption about equality is quite reasonable if we want to interpret "$is$" as asserting that a given element *is* a given set (rather than merely being related to one in some way).
