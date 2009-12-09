+--{: .standout}
This page is (I believe) original research.  Suggestions, corrections, and additions are very welcome.  -- [[Mike Shulman]]
=--

* a table of contents
{:toc}

# Introduction #

**SEAR**, short for **Sets, Elements, And Relations**, is a [[structural set theory]] with the following properties:

* It is equivalent in strength to the [[material set theory]] [[ZF]].  (It can be augmented by an [[axiom of choice]] to produce *SEARC*, which is strongly equivalent to [[ZFC]].)
* It contains a subtheory called **bounded SEAR** which (when augmented by choice) is strongly equivalent to [[ETCS]].  Conversely, ETCS can be augmented by a replacement axiom to become equivalent to SEARC.

Being a structural set theory, SEAR differs from ZF in the following ways (which are also ways in which it is similar to ETCS):

* There is a type distinction between *sets* and *elements*; a set is never an element of another set.  Every element is an element *of some set*.
* The elements of a set have no "internal structure;" they are merely featureless points.
* The "elementhood" relation $x\in A$ only makes sense when $x$ is known to be an element of some ambient set $X$ and $A$ is known to be a subset of $X$.

A good description of the difference between material and structural set theory can be found at [[Trimble on ETCS I]].  However, ZFC and ETCS also differ along another axis than the material-structural.  At [[Trimble on ETCS III]] the following metaphor is proposed for this dimension:

> with ZFC it's more as if you can just hop in the car and go; with ETCS you build the car engine from smaller parts with your bare hands, but in the process you become an expert mechanic, and are not so rigidly attached to a particular make and model.

Using this metaphor, SEAR can be thought of as an ETCS-car which comes preassembled with a nice slick control panel.  Or, using an alternate metaphor, ZFC is like Windows, ETCS is like UNIX, and SEAR is like OS X (or maybe Ubuntu).  With SEAR you get a nice familiar interface with which it is easy to do standard things, there is less cruft than you get with ZFC, and behind the scenes you have all the power of ETCS (and more).  (Of course, if you like Microsoft products, then this metaphor probably does not appeal to you.)

Note that experts will probably always prefer to build their own car/OS; the goal of SEAR is to make structural set theory accessible to a wider audience.  In particular, SEAR is intended to demonstrate the complete independence of [[structural set theory]] from [[category theory]].  Thus, apart from being (by default) stronger than ETCS, SEAR differs from it in the following ways:

* It includes the notion of an *element* of a set as a primitive concept, rather than defining it as a particular sort of function.
* It does *not* include the notion of a [[function]] as a primitive concept (instead it includes the notion of a [[binary relation]], with functions defined via their [[graph of a function|graphs]] in a familiar way).
* It does not include the notions of composition or identities (of either functions or relations) as primitive concepts.  In particular, it does not require the user to know what a [[category]] is, even implicitly.
* As a corollary, its axioms do not require knowledge of categorical concepts such as [[limits]] and [[natural numbers objects]] (although these concepts can be very naturally introduced while learning SEAR).
* The property of [[axiom of separation|separation]] (one of the most important facts in the everyday use of set theory) is a direct consequence of the axioms of SEAR.  Compare how in ETCS, the property of bounded separation follows from the theorem that a [[topos]] is a [[Heyting category]], which requires [[Trimble on ETCS II|substantial work]].


# Description of SEAR #

## Types ##

SEAR is a theory about three kinds of things: **sets**, **elements**, and **relations**.  Every element, and every variable that ranges over elements, is always associated to something denoting a set (which might be a constant or a variable); we say it is an element **of** that set.  If $x$ is an element of $A$ we write $x\in A$; note that this is not an *assertion* which may be true or false, but a *typing* declaration.  In formal terms, this means that SEAR is a [[dependent type theory]], with a type of sets, a type of elements for each set term, and a type of relations for each pair of set terms. 

One consequence of this is that whenever we quantify over elements we must always quantify over elements *of some set*; thus we can say "for all elements $x\in A$" but not "for all elements $x$."  Another consequence is that the assertion $x=y$ is only well-formed (a precondition to its being true _or_ false) if $x$ and $y$ are elements of the same set.

In a similar manner, every relation is always associated to an ordered pair of sets, the first called its **[[source]]** and the second its **[[target]]** (thus the fundamental relations in SEAR are binary relations).  If $\varphi$ is a relation from $A$ to $B$ we write $\varphi:A\looparrowright B$.  As with elements, the assertion $\varphi=\psi$ is only well-formed if $\varphi$ and $\psi$ have the same source and the same target.

Implicit in the existence of three types of things is that nothing is both a set and an element, etc., so in particular a statement such as $x=A$ is not well-formed if $x$ is an element and $A$ a set.  Furthermore, SEAR does not include an equality relation between sets: even if $A$ and $B$ are both sets we do not consider $A=B$ to be well-formed.  (Thus SEAR adheres to the philosophy of "speak no [[evil]].")

The final piece of data that we have is a notion of when a relation $\varphi:A\looparrowright B$ **holds** of a pair of elements $x\in A$ and $y\in B$.  We write $\varphi(x,y)$ when $\varphi$ holds of $x$ and $y$.


## Basic axioms ##

Now we can state the axioms of SEAR, beginning with the most basic ones.

**Axiom 0 (Nontriviality):** _There exists a set which contains an element._

**Axiom 1 (Relational comprehension):** _For any two sets $A$ and $B$, and any property $P$ that can obtain of an element of $A$ and an element of $B$, there exists a unique relation $\varphi:A\looparrowright B$ such that $\varphi(x,y)$ if and only if $P$ obtains of $x$ and $y$._

Here "property" is interpreted formally as "first-order formula", which makes the axiom (like later the axiom of collection) in fact an axiom scheme.

Axiom 1 basically says that relations are what we expect them to be intuitively.  It should remind the reader of the [[axiom of separation]].  The two important differences are (1) the presence of two sets and two variables, rather than one, and (2) the fact that what is produced is not a *set*, but a *relation* (a different kind of thing). The to-be-introduced Axiom 2 will enable us to make relations into (sub)sets, but first we need some terminology.

+-- {: .num_defn #function}
###### Definition
A relation $\varphi:A\looparrowright B$ is called a **[[function]]** from $A$ to $B$ if for any $x\in A$, there exists exactly one $y\in B$ with $\varphi(x,y)$.
=--

We write $f:A\to B$ for such a function, and for $x\in A$ we write $f(x)$ for the resulting unique $y\in B$.  Note that the uniqueness clause in Axiom 1 implies that functions are extensional: if $f,g:A\to B$ and $f(x)=g(x)$ for all $x\in A$, then $f=g$.

**Axiom 2 (Tabulations):** _For any relation $\varphi:A\looparrowright B$, there exists a set $|\varphi|$ and functions $p:{|\varphi|}\to A$ and $q:{|\varphi|}\to B$ such that: (1) for any $x\in A$ and $y\in B$, we have $\varphi(x,y)$ if and only if there exists $r\in {|\varphi|}$ with $p(r)=x$ and $q(r)=y$, and (2) for any $r\in {|\varphi|}$ and $s\in{|\varphi|}$, if $p(r)=p(s)$ and $q(r)=q(s)$, then $r=s$._

A set $|\varphi|$ equipped with $p$ and $q$ as in Axiom 2 is called a **tabulation** of the relation $\varphi$.  We think of $|\varphi|$ as "the set of pairs $(x,y)$ such that $\varphi(x,y)$ holds," with $p$ and $q$ projecting $(x,y)$ to $x$ and $y$, respectively.  Note that by Axiom 1, any set $R$ equipped with functions $p:R\to A$ and $q:R\to B$ satisfying (2) determines a unique relation $\varphi:A\looparrowright B$ such that $\varphi(x,y)$ holds iff there is an $r\in R$ with $p(r)=x$ and $q(r)=y$; then $R$ is a tabulation of $\varphi$.


## Consequences of the basic axioms ##

Axioms 0, 1, and 2 alone are very powerful!  Here are some things we can do with them.

+-- {: .num_theorem #emptyset}
###### Theorem
There exists a set $\emptyset$ which has no elements.
=--
+--{: .proof}
###### Proof
By Axiom 0, there exists a set $A$.  By Axiom 1, there exists a relation $\varphi:A\looparrowright A$ such that $\varphi(x,y)$ holds *never*.  Using Axiom 2, let $\emptyset$ be a tabulation of $\varphi$.
=--

From now on we fix a particular set $\emptyset$ having no elements.  By Axiom 1, for any set $A$ there is exactly one relation $\emptyset\looparrowright A$ and exactly one relation $A\looparrowright\emptyset$.

+-- {: .num_theorem #terminalset}
###### Theorem
There exists a set $1$ which has exactly one element.
=--
+--{: .proof}
###### Proof
By Axiom 0, there exists a set $A$ containing an element $x$.  By Axiom 1, there exists a relation $\varphi:A\looparrowright A$ such that $\varphi(y,z)$ holds iff $y=x$ and $z=x$.  Using Axiom 2, let $1$ be a tabulation of $\varphi$.
=--

From now on we fix a particular set $1$ having exactly one element;
we usually denote this element by $\star$.  By Axiom 1, for every set $A$ there exists a unique function $f:A\to 1$, defined by $f(x)=\star$ for every $x\in A$.  Likewise, to every function $g:1\to A$ there corresponds a unique element $x\in A$, by $g(\star)=x$.

We define a **subset** of a set $A$ to be a relation $S:1\looparrowright A$.  By Axiom 1, a subset $S$ of $A$ is determined by precisely those $x\in A$ such that $S(\star,x)$.  If $S(\star,x)$ we write $x\in S$.  Note that this is an *overloading* of the notation $\in$; it can be distinguished from the previous usage because here $S$ is a relation, not a set.  Note also that the previous usage $x\in A$ was a typing declaration (it says what kind of thing $x$ is when we introduce it), whereas $x\in S$ is a statement which can be either true or false.

Now Axiom 2 implies that from any subset $S$ of $A$ we can construct a set $|S|$ with a function $i:{|S|}\to A$ such that (1) $x\in S$ iff there is an $x'\in {|S|}$ with $i(x')=x$, and (2) for $x',x''\in {|S|}$, if $i(x')=i(x'')$ then $x'=x''$.  A function $i$ with property (2) is called **injective**; in this way we set up a correspondence between subsets and injective functions.  (Likewise, a function $f:A\to B$ is **surjective** if for any $y\in B$ there is an $x\in A$ with $f(x)=y$.)  Combined with Axiom 1, this implies the following *separation property*.

+-- {: .num_theorem #sep}
###### Theorem
For any property $P$ of elements of a set $A$, there exists a set $B$ and an injective function $i:B\to A$ such that for $a\in A$, we have $P(a)$ iff $a=i(b)$ for some $b\in B$.
=--

Although the set $|S|$ is not determined uniquely by the subset $S$, it is determined up to [[bijection]].  We define an **bijection** to be a relation $\psi:A\looparrowright B$ such that for every $x\in A$ there is a unique $y\in B$ with $\psi(x,y)$, and for every $y\in B$ there is a unique $x\in A$ with $\psi(x,y)$.  Clearly any bijection is a function, as is its opposite (defined by $\psi^o(y,x) \Leftrightarrow \psi(x,y)$), and these two properties characterize bijections.  It is also easy to see that a function is a bijection iff it is both injective and surjective.

For example, it is easy to see that if $A$ and $B$ both have no elements, there is a unique bijection between them; thus an empty set $\emptyset$ is determined up to unique bijection.  Likewise, if $A$ and $B$ both contain a unique element, then there is a unique bijection between them; thus a set $1$ with one element is also determined up to unique bijection.

+-- {: .num_theorem #tabuniq}
###### Theorem
If $|\varphi|$ and ${|\varphi|}'$ are two tabulations of the same relation $\varphi:A\looparrowright B$, then there is a bijection between $|\varphi|$ and ${|\varphi|}'$.
=--
+--{: .proof}
###### Proof
By Axiom 1, define $B:{|\varphi|} \looparrowright {|\varphi|}'$ such that $B(x,y)$ holds precisely when $p(x)=p'(y)$ and $q(x)=q'(y)$.  The properties of tabulations immediately imply that $B$ is a bijection.
=--

+-- {: .num_cor #sstabuniq}
###### Corollary
If $|S|$ and ${|S|}'$ are two tabulations of the same subset $S\subseteq A$, then there is a bijection between $|S|$ and ${|S|}'$.
=--

The **composite** of two relations $\varphi:A\looparrowright B$ and $\psi:B\looparrowright C$ is defined to be the relation $\psi\varphi:A\looparrowright C$ (also written $\psi\circ\varphi$) such that $\psi\varphi(x,z)$ holds of $x\in A$ and $z\in C$ iff there is a $y\in B$ with $\varphi(x,y)$ and $\psi(y,z)$.  The **identity** relation $id_A:A\looparrowright A$ is defined by $id_A(x,y) \Leftrightarrow x=y$.

+-- {: .num_theorem #category}
###### Theorem
Composition of relations is associative ($\chi(\psi\varphi)=(\chi\psi)\varphi$), and identity relations are identities for composition ($\id_B\circ \varphi = \varphi = \varphi\circ\id_A$).  The composite of functions is a function, and the identity relation is a function.  The composite of bijections is a bijection, and a relation $\varphi:A\looparrowright B$ is a bijection iff there is a relation $\psi:B\looparrowright A$ such that $\psi\varphi = id_A$ and $\varphi\psi=id_B$.
=--
+--{: .proof}
###### Proof
Just as in naive set theory.
=--

Informally speaking, we have two [[categories]] whose objects are the sets: in [[Rel]] the morphisms are the relations, while in [[Set]] the morphisms are the functions.  Formally, all we can say is that these are "meta-categories," in the sense that from any model of the first-order axioms of SEAR we can construct them as models of the first-order axioms of a category.  (This is not that different from the status of large categories such as $Set$ in material set theories such as ZF.  We could also speak about "proper classes" as is done in ZF using first-order formulas.)  See also the section on Universes, below.

In both of these (meta-)categories, the [[isomorphisms]] are the bijections.  We have also already observed that $\emptyset$ and $1$ are an [[initial object]] and a [[terminal object]] in $Set$, respectively, and that $\emptyset$ is both initial and terminal in $Rel$.

For sets $A$ and $B$, let $\top:A\looparrowright B$ denote the relation such that $\top(x,y)$ holds always.  A tabulation of $\top$ is denoted $A\times B$; it is a set equipped with functions $p:A\times B \to A$ and $q:A\times B\to B$ such that for any $x\in A$ and $y\in B$, there exists a unique $z\in A\times B$ with $p(z)=x$ and $q(z)=y$.  It is called the **cartesian product** of $A$ and $B$.

+-- {: .num_theorem #product}
###### Theorem
For any sets $A$ and $B$, $A\times B$ is a [[product]] of $A$ and $B$ in the category $Set$, and a [[coproduct]] in the category $Rel$.
=--
+--{: .proof}
###### Proof
Just as in naive set theory.
=--

In particular, $Set$ has products.

+-- {: .num_theorem #lex}
###### Theorem
The category $Set$ has finite limits.
=--
+--{: .proof}
###### Proof
It remains to construct the [[equalizer]] of two functions $f,g:A\to B$.  Let $S$ be the subset of $A$ so that $x\in S$ just when $f(x)=g(x)$; then ${|S|}\to A$ is easily shown to be an equalizer of $f$ and $g$.
=--

+-- {: .num_theorem #imfact}
###### Theorem
For any function $f:A\to B$ we have $f = m e$, where $m:im(f)\hookrightarrow B$ is an injection and $e:A\twoheadrightarrow im(f)$ is a surjection.  A set $im(f)$ equipped with such $m$ and $e$ is unique up to bijection and is called the **image** of $f$.
=--
+--{: .proof}
###### Proof
Let $im(f)$ be $|S|$ where $S$ is defined by $y\in S$ iff there exists an $x\in A$ with $f(x)=y$.  By definition, we have an injection $m:im(f)\hookrightarrow B$.  And for any $x\in A$, clearly $f(x)\in S$, so there is a unique $y\in im(f)$ with $m(y)=f(x)$; we define $e(x)=y$.  It is easy to verify the rest.
=--

Similarly, we can define the union and intersection of subsets of $A$ in the usual way: we have $x\in S\cup T$ iff $x\in S$ or $x\in T$, and $x\in S\cap T$ iff $x\in S$ and $x\in T$.

+-- {: .num_theorem #heyting}
###### Theorem
$Set$ is a [[well-pointed category|well-pointed]] [[Heyting category]] and $Rel$ is a [[division allegory]].
=--
+--{: .proof}
###### Proof
Left to the reader.
=--


## Power sets and colimits ##

In structural set theory, sets cannot contain other sets (or relations), so we cannot strictly speaking have "the set of subsets of a set $A$."  What we generally do instead is have a set $P A$ each of whose elements is *associated to* a subset of $A$ in a bijective way.  This association happens via a specified relation between $A$ and $P A$.

**Axiom 3 (power sets):** _For any set $A$, there exists a set $P A$ and a relation $\epsilon:A\looparrowright P A$ such that for any subset $S$ of $A$, there exists a unique $s\in P A$ with the property that for any $x\in A$, we have $x\in S$ iff $\epsilon(x,s)$._

As in both material set theory and ETCS, many useful consequences flow from this axiom.  We first observe that the property of $P A$ stated for subsets actually implies an analogous property for all relations.


+-- {: .num_theorem #topos}
###### Theorem
For any relation $R:B\looparrowright A$, there exists a unique function $f_R:B\to P A$ such that $R(y,x)$ if and only if $\epsilon(x,f_R(y))$.  It follows that $Set$ is a [[topos]] (and $Rel$ is a power allegory).
=--
+--{: .proof}
###### Proof
We simply define $f_R$ elementwise; for each $y$ we define $f_R(y)$ to be the unique element of $P A$ such that $\epsilon(x,f_R(y))$ holds iff $R(y,x)$ holds.  Extensionality of functions implies that it is unique.
=--

As usual, power sets also imply the existence of function sets.

+-- {: .num_theorem #ccc}
###### Theorem
For any two sets $A$ and $B$, there exists a set $B^A$ and a function $ev:B^A \times A\to B$ such that for any function $f:A\to B$ there exists a unique element $s_f\in B^A$ such that $ev(s_f,a)=f(a)$ for all $a\in A$.  It follows that $Set$ is a [[cartesian closed category]].
=--
+--{: .proof}
###### Proof
We take $B^A$ to be a tabulation of the subset of $P(A\times B)$ containing only the functions.  More precisely, define $F\subseteq P(A\times B)$ such that $s\in F$ iff for every $x\in A$, there exists a unique $y\in B$ such that $\epsilon((x,y),s)$, and let $B^A = {|F|}$.
=--

The correspondences in Theorems \ref{topos} and \ref{ccc} are "meta-bijections," but by a standard Yoneda lemma argument they can be converted into actual bijections as defined above in SEAR.  This produces bijections such as $C^{A\times B} \cong (C^A)^B$ and $P(A\times B) \cong (P A)^B$.

We now construct [[quotient set]]s.  Of course, by an **[[equivalence relation]]** on a set $A$ we mean a relation $R:A\looparrowright A$ which is reflexive, transitive, and symmetric.

+-- {: .num_theorem #quotients}
###### Theorem
If $R$ is an equivalence relation on $A$, then there is a surjective function $q:A\twoheadrightarrow B$ such that $R(x,y)$ holds iff $q(x)=q(y)$.
=--
+--{: .proof}
###### Proof
$R$ induces a function $f_R:A\to P A$ as above; let $B$ be $im(f_R)$ and $q$ the surjective part of the image factorization.  If $R(x,y)$ holds, then by symmetry and transitivity, $R(x,z)\Leftrightarrow R(y,z)$ for all $z$; hence $f_R(x)=f_R(y)$ and so $q(x)=q(y)$.  Conversely, if $q(x)=q(y)$, then $f_R(x)=f_R(y)$; but $y\in f_R(y)$ by reflexivity, hence $y\in f_R(x)$ and thus $R(x,y)$ holds.
=--

Such a $B$, which is easily seen to be unique up to bijection, is called a **quotient** of $R$ and often written $A/R$.

Likewise, given sets $A$ and $B$, let $A\sqcup B={|S|}$, where $S$ is the subset of $P A \times P B$ consisting of the pairs $(\{x\},\{\})$ for $x\in A$ and $(\{\},\{y\})$ for $y\in B$.  (Of course, here we are identifying elements of $P A \times P B$ with ordered pairs of subsets of $A$ and $B$ via the projections of the product and the defining relations $\epsilon_A$ and $\epsilon_B$.)  We have evident injections $A\to A\sqcup B$ and $B\to A\sqcup B$ which are jointly surjective and have disjoint image; we call $A\sqcup B$ the **disjoint union** of $A$ and $B$.

In particular, it follows that $Set$ is a [[pretopos]] (as is any topos).


## Infinity ##

**Axiom 4 (Infinity):** _There exists a set $N$, containing an element $o$, and a function $s:N\to N$ such that $s(n)\neq o$ for any $n\in N$ and $s(n) = s(m)$ only if $n = m$ for any $n, m\in N$._

It is easy to deduce any of the usual consequences of the axiom of infinity.  The set $N$ is not asserted to be minimal, but it is easy to cut it down to be so using separation.  In particular, this axiom implies that $Set$ has a [[natural numbers object]].  We can then proceed to construct the set $\mathbb{Q}$ of rational numbers and the set $\mathbb{R}$ of real numbers in any of the usual ways.

Note also that Axiom 4 implies Axiom 0.

We can however [[natural numbers in SEAR|define sets]] with $n$ elements for each natural number $n$ directly axioms 0, 1, 2 and 3.
 
## Collection ##

The final axiom of SEAR is somewhat trickier to motivate.  It corresponds to the [[axiom of replacement]] (or more precisely collection; see [Wikipedia](http://en.wikipedia.org/wiki/Axiom_schema_of_replacement) until we get around to writing our own article) in $\mathbf{ZFC}$, and the reasons that we need it are the same as the reasons that $\mathbf{ZFC}$ needs it.

### The ghost of a universal set

One way to motivate the collection axiom is as follows.
Suppose for the sake of argument that there existed a *universal set*, meaning a set containing all other sets.  Now in structural set theory this is meaningless, since no set can contain other sets, but there is an easy fix: we consider instead *indexed families* of sets.  There are multiple ways to make this precise, but here is a very simple one: an $A$-indexed family of sets is simply a relation $M:A\looparrowright X$.  The set indexed by each element $a\in A$ is $M_a = \{x\in X | M(a,x)\}$.  (Often one requires the $M_a$ to be a disjoint decomposition of $X$, so that $M^o$ is a function $X\to A$, but this is unnecessary.  In fact, if $M:A\looparrowright X$ is a general family, then ${|M|} \to A$ is a function that represents a family in this stronger sense which is equivalent to $M$.)

With this definition, a *universal family of sets* would be a set $U$ with a $U$-indexed family of sets $E:U\looparrowright Y$ such that for any set $A$, there exists a unique $u\in U$ and a bijection $A\cong E_u$.  The existence of such a universal set is inconsistent, but the collection axiom can be thought of as the "ghost" of what *would be implied* by Axioms 1 and 2 if a universal set *did* exist.  Let's now unravel that.

If $U$ were a universal set, then any $A$-indexed family $M:A\looparrowright X$ would induce a unique function $f:A\to U$ such that $E_{f(x)} \cong M_x$ for all $x\in A$.  Conversely, any function $f:A\to U$ would induce an $A$-indexed family of sets with this property: just take the composite relation $E \circ f$.  (This family would not be unique, but it would be unique up to a suitable notion of [[equivalence]] between indexed families.)  Thus it is reasonable to consider the "ghost" of a function $f:A\to U$ to be simply an $A$-indexed family of sets.

The ghost of a relation $A\looparrowright U$ is even easier.  By Axiom 1, to give such a relation would be equivalent to describing a property $P$ that can obtain of an element of $A$ and a set.  Thus, the ghost of a relation $A\looparrowright U$ is simply such a property.

If $U$ existed, Axiom 2 would imply that any relation $A\looparrowright U$ had a tabulation consisting of a set $B$ and functions $p:B\to A$ and $q:B\to U$.  We now kill $U$ and inspect the ghostly remnants of this tabulation.

**Axiom 5 (Collection):** _For any set $A$ and any property $P$ which can obtain of an element of $A$ and a set, there exists a set $B$, function $p:B\to A$, and a $B$-indexed family of sets $M:B\looparrowright Y$ such that (1) $P(p(b),M_b)$ holds for any $b\in B$, and (2) for any $a\in A$, if there exists a set $X$ with $P(a,X)$, then $a\in im(p)$._

What this axiom asserts is actually a bit weaker than the precise ghost of a tabulation of $P$; that would require instead of (2) that for any $a\in A$ and any set $X$ with $P(a,X)$, there exists a $b\in B$ with $p(b)=a$ and $M_b\cong X$.  However, this stronger statement is still inconsistent, because if we took $A=1$ and $P=\top$ it would resurrect $U$ in the form of $B$!  The form given above is weak enough to keep the dead in their graves, yet strong enough to be useful.  (The former statement follows from the discussion below about inter-interpretability of SEAR and ZF, at least as long as the reader believes that ZF is consistent.  The latter remains to be gone more into.)

_Exercise: why is adherence to "speak no evil" necessary for Axiom 5 to be reasonable as stated?_

### Applications of collection

One thing that Axiom 5 is good for is the recursive construction of sets.  For example, using Axioms 1-4 we can construct the sets $N$, $P(N)$, $P(P(N))$, and so on, but we cannot construct anything larger than all the sets in this sequence.  Axiom 5 allows us to do that.

(more detail to be added here...)


# Variants and Comparisons #

## The Axiom of Choice ##

We obtain a theory called **SEARC** (SEAR with Choice) by adding the following axiom:

**Axiom 6 (Choice):** _If $\varphi:A\looparrowright B$ is a relation such that for any $a\in A$, there exists a $b\in B$ with $\varphi(a,b)$, then there exists a function $f:A\to B$ with $\varphi(a,f(a))$ for all $a\in A$._

This is easily seen to be equivalent to asserting that all surjections are [[split epimorphism|split]] in $Set$, which is a more common categorical form of the [[axiom of choice]].

## Constructive SEAR ##

Axioms 1-5 of SEAR make perfect sense whether the ambient logic is [[classical logic|classical]] or [[intuitionistic logic|constructive]].  By Diaconescu's argument, Choice implies the logic is classical.

To obtain a [[predicative mathematics|predicative]] theory, Axiom 3 can be replaced by an appropriate weaker axiom, such as the existence of [[disjoint union]]s, [[quotient set]]s, and/or [[function sets]], or a structural version of the axiom of [[subset collection]].

Compare [[Erik Palmgren]]\'s [constructive ETCS](http://www.math.uu.se/~palmgren/cetcs.pdf).

## Bounded SEAR and ETCS ##

By **bounded SEAR** we mean the subtheory consisting of axioms 2-4 of SEAR plus

**Axiom 1B (Bounded relational comprehension):** _The same as Axiom 1, but the property $P$ must be bounded (it can only involve quantifiers over elements, not sets or relations)._

All the theorems cited above remain true with Axiom 1 replaced by Axiom 1B, so bounded SEAR still implies that $Set$ is a well-pointed topos with a NNO.  Therefore, *bounded SEARC* implies [[ETCS]].  Conversely, it is not hard to show that given any [[well-pointed topos]], if we interpret "set" as "object of the topos", "element of $A$" as "[[global element]] $1\to A$", and "relation $A\looparrowright B$" as "[[subobject]] of $A\times B$," then Axioms 0, 1B, 2, and 3 are satisfied.  It follows that ETCS also implies bounded SEARC, so the two are equivalent.

ETCS can also be augmented with additional axioms to make it equivalent to full SEARC, but that is beyond our scope at the moment.

## SEAR and ZF ##

### From ZF to SEAR

It is fairly straightforward to construct a model of SEAR from a model of ZF.  Given a model of ZF, we define the SEAR-sets to be the ZF-sets, and the SEAR-elements of $A$ to be the ZF-elements of $A$.  If we prefer, we can take the SEAR-elements of $A$ to be pairs $(x,A)$ where $x\in_{ZF} A$, so that the elements of distinct sets will be disjoint---but this is not necessary, since in SEAR the question of whether two distinct sets have elements in common is not even well-posed.  Finally, we of course take the SEAR-relations $A\looparrowright B$ to be the ZF-subsets of $A\times B$, and we let $\varphi(x,y)$ hold in SEAR iff $(x,y)\in_{ZF} \varphi$.  It is then easy to prove Axioms 0, 1, 2, 3, and 4 from the axioms of ZF, and likewise Axiom 6 follows easily from the axiom of choice in ZFC.  (In fact, Z and ZC, where the replacement axiom is omitted, suffice for these conclusions.)  The only axiom which requires some thought is Collection, and it is here that we use replacement.

+-- {: .num_theorem #zf-coll}
###### Theorem
The sets, elements, and relations in a model of ZF satisfy the Collection axiom of SEAR.
=--
+--{: .proof}
###### Proof
Let $A$ be a set and $P$ a property as in Axiom 5.  As given, $P$ is a first-order statement in the language of SEAR, but we can easily translate it into a statement in the language of ZF; from now on we work in ZF.  Define
$$A' = \{a\in A | \exists X. P(a,X)\}.$$
By the [[axiom of foundation]], for each $a\in A'$ there exists an [[ordinal]] $\lambda$ and an $X\in V_{\lambda}$ such that $P(a,X)$; let $\lambda_a$ be the *smallest* such $\lambda$.  Then $a\mapsto V_{\lambda_a}$ is a class function, so by the axiom of replacement, the set $\{V_{\lambda_a} | a\in A'\}$ exists.  Let $Y$ be the union of this set.  Define
$$B = \{ (a,X)\in A\times Y | P(a,X)\},$$
let $p:B\to A$ be the projection onto the first factor, and let $M:B\looparrowright Y$ be defined by
$$M((a,X),x) \Leftrightarrow x\in X.$$
Then $M_{(a,X)} = X$, since each $V_\lambda$ is a transitive set, so $P((a,X), M_{(a,X)})$ holds for any $(a,X)\in B$.  Finally, by construction, if there exists $X$ with $P(a,X)$ then $a\in im(p)$; thus the SEAR axiom of collection is satisfied.
=--

Note the use of the axiom of foundation in addition to the axiom of replacement.  This can be avoided if we use instead the ZF version of the [axiom of collection](http://en.wikipedia.org/wiki/Axiom_of_collection#Axiom_schema_of_collection), which is equivalent to the axiom of replacement over the other ZF axioms (including foundation), by an argument like that above.

### From SEAR to ZF

Conversely, from any model of SEAR one can *construct* a model of ZF.    The basic idea of this process is described at [[pure set]].  Given a model of SEAR, we define a **ZF-set** to be an equivalence class of well-founded extensional accessible graphs, as described at [[pure set]].  We define the global membership relation $\in$ on ZF-sets to be the "immediate subgraph" relation.

The proofs of most of the axioms of ZF are straightforward, and may eventually be found at [[pure set]].  Here we treat the proof of the replacement/collection axiom of ZF from the Collection axiom of SEAR, since that is specific to SEAR.

+-- {: .num_theorem #coll-zf}
###### Theorem
The ZF-sets constructed from a model of SEAR satisfy the ZF [axiom of collection](http://en.wikipedia.org/wiki/Axiom_of_collection#Axiom_schema_of_collection) (which is equivalent to the axiom of replacement over the other axioms of ZF).
=--
+--{: .proof}
###### Proof
We will prove the version of the ZF axiom of collection which states that for any first-order formula $P$ in the language of ZF, and any ZF-set $A$, there exists a ZF-set $D$ such that for any ZF-element $x\in_{ZF} A$, if there exists a ZF-set $y$ such that $P(x,y)$, then there exists such a $y$ which is a ZF-element of $D$.  Note that any first-order formula in the language of ZF about ZF-sets can easily be translated into a first-order formula in the language of SEAR.

Fix such a $P$ and $A$; thus $A$ is a SEAR-set equipped with a binary relation $\to$ of a certain type.  Let $A'$ be the subset of $A$ consisting of the children of the root of $A$.  For a SEAR-set $X$, let $P'(a,X)$ mean that $X$ admits the structure of a ZF-set such that the ZF-statement $P(down(a),X)$ holds.  By the SEAR axiom of collection, there is a set $B$, a function $p:B\to A'$, and a $B$-indexed family of sets $M:B\looparrowright Y$ such that (1) each $M_b$ admits the structure of a ZF-set with $P(down(p(b)),M_b)$, and (2) if there is a ZF-set $X$ with $P(down(a),X)$, then $a\in im(p)$.

Let $C$ be the subset of $B\times P(Y\times Y)\times Y$ consisting of pairs $(b,r,y)$ such that $y\in M_b$ and $r$ represents a binary relation on $M_b$ making it into a ZF-set such that $P(down(p(b)),M_b)$.  Now $C$ can be equipped with the relation that is the disjoint union of all the $r$s, i.e. we set $(b,r,y)\to (b',r',y')$ iff $b=b'$, $r=r'$, and $y\to_r y'$.  Let $C'=C\sqcup 1$ extend this relation with the additional point being a root, i.e. $(b,r,y)\to \star$ iff $y$ is the root of $r$.  Now $C'$ is a well-founded accessible graph, but it may not be extensional; we take $D$ to be the ZF-set represented by the extensional quotient of $C'$.  
Then for any $x\in_{ZF}A$, we have $x\cong down(a)$ for some child $a$ of the root of $A$, i.e. $a\in A'$.  Thus, if there is a ZF-set $y$ with $P(x,y)$, then $a\in im(p)$ and so there is such a ZF-set represented by one of the $r$'s occurring in $C$.  By construction, this ZF-set is then equivalent to $down(d)$ for some child of the root of $D$, hence $down(d) \in_{ZF} D$.  Thus $D$ satisfies the requirement of the ZF axiom of collection.
=--

Thus, SEAR and SEARC are at least equiconsistent with ZF and ZFC, respectively. In fact, SEARC and ZFC are equivalent, in the sense that passage back and forth in either direction yields an equivalent model.  However, passage from SEAR to ZF and back again can lose information, if there are sets in the model of SEAR which do not admit any well-founded extensional relation (this doesn't happen in the presence of choice, since then every set can be well-ordered).

## Type theory and internalization

Every topos has an [[internal logic]], which is a [[type theory]].  However, the line between type theory and structural set theory is fine and sometimes hard to see; the main difference is that structural set theory can involve quantifiers over sets (= types), while type theory only allows ("bounded") quantifiers over elements of types.  Through this correspondence, *Intuitionistic Bounded SEAR* can be treated as a type theory and interpreted internally in any topos with a NNO.  Of course, if the topos is [[boolean topos|boolean]], then the logic can be classical.

One can also write down stronger axioms on a topos such that if they are satisfied, then full Intuitionistic SEAR can be interpreted "internally" in that topos, extending the usual internal logic.


# Making alternate primitive choices #

## SEPS: Using pairs and subsets instead of relations

+-- {: .query}
This looks nice, and I think that it probably matches pretty closely the way that I usually think when reading ordinary mathematics.  I haven\'t read it very carefully yet, so take this with a grain of salt, but I think that it would be even more user-friendly to use sets, elements, and *subsets* (rather than binary relations) as the basic concepts.  Presumably you have to throw in ordered pairs too, but I think that this matches 'ordinary' language *very* closely.  ---Toby

_Mike_: Yes, you're right, and I did think of something like that.  However, I haven't managed to find a good way to "throw in ordered pairs."  I'd like an axiom like "for any sets $A$ and $B$, there exists a set $A\times B$ such that ..." but what comes after "such that?"  With only sets, elements, and subsets as the other data, there's no way to relate the elements of $A\times B$ to the elements of $A$ and $B$.

I guess one possible approach would be to make the construction of products an *operation*, rather than an existential axiom.  Then for every pair of sets $A$ and $B$ there would be a *specified* set $A\times B$, and for every pair of elements $x\in A$ and $y\in B$ there would be a *specified* element $(x,y)\in A\times B$, with an axiom asserting that every element of $A\times B$ is of the form $(x,y)$ for a unique $x$ and $y$.  I suppose we do tend to think more in terms like that, but it's less aesthetically pleasing to me because it's not really "structural" to specify a particular $A\times B$.  So now I'm undecided.

_Toby_:  I don\'t see what\'s unstructural about that!  Although I think that we\'ve had this conversation before ....

[[Mike Shulman]]: It feels unstructural because the element $(x,y)$ is no longer internally featureless; it has the intrinsic property of being the pair of $x$ and $y$.  I see "structural" as meaning that, among other things, isomorphic objects are indistinguishable; but with that approach, the selected product $A\times B$ is distinguishable from any other product.  (Additionally, in some metatheories it requires choice to get from one to the other.)

I also feel that maybe viewing relations $A\looparrowright B$ as subsets of $A\times B$ is merely a habit ingrained in us by material set theory over the course of the 20th century, and thus something that structural set theory should try to wean us from.

_Toby_:  I don\'t see how you would distinguish $A \times B$ from any other isomorphic object if you have no way to express that it equals *the* $A \times B$ in question.  More generally, strucuturalism to me isn\'t about using existential quantifiers all the time instead of operations.  In fact, I don\'t see how this is any different from your set $|\varphi|$.  (Possibly I should write SESAP out in full to make sure it does all work the same way.)  And the metatheories that think that they require choice to get an operation out of an existential statement have formalised things wrong; they should be using meta-anafunctors between the (syntactic or model) meta-categories.

I also don\'t see what\'s material about conflating $A \looparrowright B$ with $\mathcal{P}(A \times B)$.  It\'s no different, really, from making $A \to B$ a part of $A \looparrowright B$.  Personally, I *prefer* to take sets and functions as the basic concepts; I saw $\mathbf{SEAR}$ as an attempt to make a structural theory that looks more like the na&#239;ve set theory that mathematicians use (but perhaps I misjudged the idea), and I think that making unary relations basic will be even more like that.  Really, any of these concepts (function, binary relation, unary relation) have a good claim for being a basic concept that should be axiomatised directly, rather than defined in terms of one of the others, and it\'s a fairly arbitrary choice which one we use.

[[David Roberts]]: ...it makes sense to me that we probe the interior of a set by how it relates to other sets, and that we find out about the elements of a set by how it relates to the one-point set. But the aim seems to be useability by everyday mathematicians. That being said, this material seems easier to learn as a first approach to foundations (for undergraduates/early postgrads) than ZF or NBG, requiring less cruft to get to proving theorems.


[[Mike Shulman]]: You're right that the given $A\times B$ couldn't be distinguished *in the theory itself* from any other product, but I think it would still clearly have a special status.  Also, it is definitely different from $|\varphi|$.   The tabulation axiom is a purely existential statement; it could be viewed as an "operation" from relations to tabulations, but nothing forces you to view it this way.  (And you can only avoid meta-choice by calling such an operation an anafunctor once you've *proven*, in the theory, that tabulations are unique up to unique isomorphism.)  By contrast, the product axiom would be irreducibly an operation; you can't (at least, I don't see how to) make it purely existential, because it is the *only* part of the theory that relates elements of different sets.  The product can only be characterized uniquely using "projection" functions, but in order to have functions you need relations, hence you need products....

My original idea with SEAR was merely to give a proof-of-concept that structural set theory can be formalized with elements and without functions or categories.  But it does turn out looking much more like the set theory that mathematicians actually use, and making it even more so would definitely be a plus to getting structural set theory adopted more widely, which I'm all about.  Moreover, David's comment about it being easier to learn as a first approach to foundations is also an interesting point that I hadn't really thought about, and for that purpose subsets and pairs might also be better.  And I do admit that the tabulation axiom looks a little cumbersome; breaking it down into pairing and separation does feel cleaner.

It also makes it look much more like type theory!  Which I suppose is not a bad thing.  Bounded SESAP will basically *be* the internal type theoretic language of a topos with NNO, and that's actually a really *good* thing; it will make internal logic feel more natural to anyone who is familiar with structural-set-theory foundations.

I went ahead and had a go at a formalization using products down at the bottom of the page.  I have to say that "SESAP" doesn't ring as well.  (-:  But I think we could still call it SEAR even if the "relations" aren't quite a fundamental concept.  (Although if someone has a better name to suggest, I'm still listening.)  Actually, we could probably use the same name for all the different formalizations, explicitly allowing people the choice of whether to take functions or binary-relations or subsets+products as primary.  Everyone says "ZF" despite variations in the phrasing of the axioms, so the name of a theory doesn't have to be rigidly tied to a specific way of stating it.

_Toby_:  I was going to call my version 'SEAPS' until I realised that the 'A' was in the wrong place ...

[[David Roberts]]: How about SER and SEPS? And then SER-C and SEPS-C.

[[Mike Shulman]]: I like SEAR better than SER, but SEPS isn't too bad.  Although I'd also still rather not make a big deal about the difference between the two.

[[Mike Shulman]]: And actually, Subsets are just unary Relations.  So the version with subsets and products is also a theory of "sets, elements, and relations"---it's just that since it only uses unary relations, it also needs product operations on its sets and elements.

_Toby_:  Well, yeah, but you\'ve been using 'relation' to mean a [[binary relation]], so I used another term.  But if one is naming an entire system, that may not matter.
=--

An alternate formulation of the theory, suggested by Toby, has four primitive notions: sets, elements, subsets, and a pairing operation.  Sets and elements are as before.  A *subset* is, like an element, attached to a certain set; it is always a subset *of* some set.  Thus we have a typing declaration $S\subseteq A$.  We also have a primitive notion of when an element $x\in A$ *belongs to* a subset $S\subseteq A$; thus now we have $x\in S$ as a possible assertion of the theory (analogous to $R(x,y)$ before).  We allow a typed equality predicate for subsets.  Finally, there is an operation which assigns to every pair of sets $A$ and $B$ a set $A\times B$, and to every pair of elements $x\in A$ and $y\in B$ an element $(x,y)\in A\times B$.

**Axiom 0** is the same as before.

**Axiom $\frac{1}{2}$ (Pairing):** _For every pair of sets $A$ and $B$ and every element $z\in A\times B$, there exists a unique pair of elements $x\in A$ and $y\in B$ such that $z=(x,y)$._

**Axiom $1\frac{1}{2}$ (Subset comprehension):** _For every property $P$ that can obtain of elements $x$ of some set $A$, there exists a unique subset $S\subseteq A$ such that $x\in S$ precisely when $P$ obtains of $x$_

We now define a **relation** $A\looparrowright B$ to be a subset of $A\times B$.  With this definition, Axiom $1\frac{1}{2}$ clearly implies Axiom 1 (relational comprehension).  We define **functions** and their properties as before.  Axiom $\frac{1}{2}$ implies that there are projection functions $A\times B\to A$ and $A\times B\to B$ which make $A\times B$ into a product in $Set$.

**Axiom $2\frac{1}{2}$ (Separation):** _For every set $A$ and every subset $S\subseteq A$, there exists a set $|S|$ and an injective function $i:{|S|}\to A$ such that for any $x\in A$, we have $x\in S$ if and only if there is a $z\in {|S|}$ with $i(z)=x$._

Applying separation to subsets of $A\times B$ and composing $i$ with the product projections, we recover Axiom 2 (tabulations).  We can now go on with the subsequent axioms stated in the same way as before.


## Eliminating equality

As stated SEAR includes a fundamental "equality" relation on elements of a given set.  However, we can also make equality into *structure*.  This is definitely not along the "more accessible to undergraduates" direction!  But it may sometimes be technically helpful.

Consider a theory of *pre-sets*, *elements*, and *pre-relations* as in SEAR, with "pre-sets" replacing sets, except that there is no given equality relation on *anything*.  Axiom 0 requires no modification. In Axiom 1, we reinterpret the "uniqueness" clause as a *definition* of what it means for two parallel pre-relations to be equal, i.e. $\varphi=\psi$ if $\varphi(x,y)\Leftrightarrow\psi(x,y)$ for all $x$ and $y$ in the source and target of $\varphi$ and $\psi$.

Before stating the version of Axiom 2 we need some definitions.  We define a **set** to be a preset $A$ equipped with an [[equivalence relation|equivalence pre-relation]] $=_A$.  A **relation** between sets $(A,{=_A})$ and $(B,{=_B})$ is a pre-relation $\varphi:A\looparrowright B$ which is *extensional* in the sense that if $\varphi(x,y)$, $x'=_A x$, and $y'=_B y$, then $\varphi(x',y')$.  Finally, a **function** $f:(A,{=_A}) \to (B,{=_B})$ is a relation which is (a) *[[entire relation|entire]]:* for any $x\in A$, there is a $y\in B$ with $f(x,y)$, and (b) *[[functional relation|functional]]:* if $f(x,y)$ and $f(x',y')$ and $y=_B y'$, then $x=_A x'$.

Now Axiom 2 reads: for any sets $(A,{=_A})$ and $(B,{=_B})$ and any relation $\varphi:(A,{=_A})\looparrowright (B,{=_B})$, there exists a set $({|\varphi|},{=_{|\varphi|}})$ and functions $p:{|\varphi|}\to A$ and $q:{|\varphi|}\to B$ such that: (1) for any $x\in A$ and $y\in B$, we have $\varphi(x,y)$ if and only if there exists $r\in {|\varphi|}$ with $p(r,x)$ and $q(r,y)$, and (2) for any $r\in {|\varphi|}$ and $s\in{|\varphi|}$, if $p(r)=_A p(s)$ and $q(r)=_B q(s)$, then $r=_{|\varphi|}s$.  Note that it is sufficient to assert merely that $|\varphi|$ is a pre-set and $p$ and $q$ are entire relations satisfying (1), since (2) can then be used to define $=_{|\varphi|}$ in such a way as to make it a set and $p$ and $q$ functions.

The construction of $\emptyset$ is just as in ordinary SEAR.  The construction of $1$ in ordinary SEAR used equality, but we now have a simple replacement for it: let $1$ be any pre-set containing an element, equipped with the equivalence relation such that $x=y$ always for any $x,y\in 1$.  Similarly, in this variant we can construct quotient sets without needing powersets; we simply enlarge the equivalence relation on the underlying pre-set of a set.

Of course, if $(A,{=_A})$ is a set, a **subset** of $A$ is a relation $1\looparrowright (A,{=_A})$.  Axiom 3 can now be translated as-is, or it can be simplified to assert merely the existence of a pre-set $P A$ such that any subset of $A$ is represented by some element of $P A$, with the uniqueness clause turned into a definition of $=_{P A}$.
The same idea applies to all the other axioms.

If to this equality-free version of SEAR we add a primitive notion of (non-extensional) "operation" and a [[choice operator]], we obtain [[SEAR+?]].


# Related pages and spinoffs

The following pages develop various aspects of set theory in SEAR or related theories.

* [[natural numbers in SEAR]]: defining individual natural numbers without the axiom of infinity.
* [[categories in SEAR]]: defining small categories, in response to a query on the blog.
* [[universes in SEAR]]: how to formulate an axiom of [[Grothendieck universes]].
* [[SEAR+?]]: a variant theory containing a [[choice operator]].
