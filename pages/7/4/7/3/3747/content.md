
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A Cauchy real number is a [[real number]] that is given as the limit of a [[Cauchy sequence]] of [[rational numbers]].  One may use this idea as a *definition* of the general concept of real number. This is due to [[Georg Cantor]] in 1872, the same year that [[Richard Dedekind]] developed [[Dedekind cuts]] as a definition of the same concept.


## Definitions

If we simply want a construction of the [[real line]] $\mathbb{R}$ for the purposes of [[classical mathematics]], then we can use Cantor\'s original version.  If we wish to use weak [[foundations]] or [[internalisation|internalise]] the Cauchy real line, then there are subtler alternatives.


### Classical version

Putting Cantor\'s definition in modern terminology, $\mathbb{R}$ is the [[quotient set]] of the set of Cauchy sequences of rational numbers, with two sequences considered equivalent if their difference converges to zero.  Although the notion of Cauchy sequence (and convergence, for that matter) is best known in the context of [[metric spaces]] or [[Booij premetric spaces]] (which cannot be defined in general without having, at least implicitly, constructed $\mathbb{R}$ already), it is easy to state the definitions in elementary terms.  If there is any tricky point, it is that the requirements made for all $\epsilon \gt 0$ need be made only for rational $\epsilon$. (We could also treat $\mathbb{Q}$ as a [[uniform space]] or even a [[Cauchy space]], although again to write down the definitions of those structures still requires one to handle the $\epsilon$s.)

To be explicit:  A __Cauchy real number__ $x$ is an [[infinite sequence]] $(x_0,x_1,x_2,\ldots)$ of [[rational numbers]] such that, for every positive rational number $\epsilon$, there exists a [[natural number]] $\alpha$ such that
$$ {|x_i - x_j|} \leq \epsilon $$
holds whenever $i,j \geq \alpha$.  Two Cauchy real numbers $x,y$ are considered __equal__ if, for every positive rational number $\epsilon$, there exists a natural number $\alpha$ such that
$$ {|x_i - y_i|} \leq \epsilon $$
holds whenever $i \geq \alpha$.  It is easy to prove that this is an [[equivalence relation]] on the set of Cauchy sequences, so the set $\mathbb{R}$ of real numbers is a quotient set.

This definition comes in two steps: one to identify the Cauchy sequences from among the infinite sequences, another to identify equivalent sequences.  Actually, we can do this in one step by placing a [[partial equivalence relation]] on the set of *all* infinite sequences of rational numbers.  Two sequences $x,y$ are considered equivalent if, for every positive rational number $\epsilon$, there exists a natural number $\alpha$ such that
$$ {|x_i - y_j|} \leq \epsilon $$
holds whenever $i,j \geq \alpha$.  It is immediate that a sequence $x$ is Cauchy if and only if it equivalent to itself, and it is easy to prove that two Cauchy sequences $x,y$ are equivalent if and only if they are equal as real numbers using the definition above.  Thus, we can construct $\mathbb{R}$ immediately as a [[subquotient]] of the [[function set]] $\mathbb{Q}^{\mathbb{N}}$.


### Moduli of convergence

In weak foundations, we sometimes want to be a little more strict about how a sequence is Cauchy and how the difference of two such sequences converges to zero.  We do this by requiring explicit moduli of convergence.  These moduli can always be constructed using (for example) either [[countable choice]] or the principle of [[excluded middle]], but the requirement makes a difference in (for example) a [[localic topos]] over any non-[[discrete space]].

(Since the term 'Cauchy real number' is used ambiguously in the constructive literature, we can identify Cantor\'s classical definition above as a __Cantor real number__ or a __classical Cauchy real number__.)

In general, a __[[modulus of convergence]]__ may be any function $\alpha$ from the positive rational numbers to the natural numbers such that, for every natural number $n$, there is a positive rational number $\epsilon$ such that $\alpha(\epsilon) \geq n$.

A __[[modulated Cauchy real number]]__ $x$ is an infinite sequence $(x_0,x_1,x_2,\ldots)$ of rational numbers such that there exists a modulus $\alpha$ such that
$$ {|x_i - x_j|} \leq \epsilon $$
holds whenever $i,j \geq \alpha(\epsilon)$.  Two modulated Cauchy real numbers $x,y$ are considered __equal__ if there exists a modulus $\alpha$ such that
$$ {|x_i - y_i|} \leq \epsilon $$
holds whenever $i \geq \alpha(\epsilon)$.  Again we can combine these conditions into a single partial equivalence relation: that there exists a modulus $\alpha$ such that
$$ {|x_i - y_j|} \leq \epsilon $$
holds whenever $i,j \geq \alpha(\epsilon)$.

Some variations are often met.  A modulus $\alpha$ may be extended to all rational numbers, although the conditions above can only be required for positive $\epsilon$.  Alternatively, it is enough to define $\alpha$ (and require the conditions) for $\epsilon$ of specific form; common choices are $1/n$ and $1/2^n$ for $n$ a natural number.  (The important criterion is to use a set of positive rational numbers of which zero is a limit point.)

It is also possible to fix a specific modulus $\alpha$ ahead of time.  Then we need to treat each index separately, in this way:  An __$\alpha$-regular Cauchy real number__ $x$ is an infinite sequence $(x_0,x_1,x_2,\ldots)$ of rational numbers such that
$$ {|x_i - x_j|} \leq \delta + \epsilon $$
holds whenever $i \geq \alpha(\delta)$ and $j \geq \alpha(\epsilon)$.  Two $\alpha$-regular Cauchy real numbers are considered __equal__ if
$$ {|x_i - y_i|} \leq 2\epsilon $$
holds whenever $i \geq \alpha(\epsilon)$.  Once more, we can combine these conditions into a single partial equivalence relation: that
$$ {|x_i - y_j|} \leq \delta + \epsilon $$
holds whenever $i \geq \alpha(\delta)$ and $j \geq \alpha(\epsilon)$.

### Cauchy approximations

The modulated Cauchy real numbers could also be constructed through [[Cauchy approximations]] rather than sequences of rational numbers with a modulus of convergence. Let $\mathbb{Q}$ be the [[rational numbers]] $\mathbb{Q}$ and let 

$$\mathbb{Q}_{+} \coloneqq \{x \in \mathbb{Q} \vert 0 \lt x\}$$ 

be the positive rational numbers. 

#### As an initial algebra

Let us define a *modulated Cauchy algebra* to be a [[set]] $A$ with a function $\iota \in A^{C(\mathbb{Q})}$, where $C(\mathbb{Q})$ is the set of [[Cauchy approximation]]s in $\mathbb{Q}$ and $A^{C(\mathbb{Q})}$ is the set of functions with domain $C(\mathbb{Q})$ and codomain $A$, such that 
$$\forall a \in C(\mathbb{Q}). \forall b \in C(\mathbb{Q}). \left( \forall \epsilon \in \mathbb{Q}_{+}. \vert a_\epsilon - b_\epsilon \vert \lt 4 \epsilon \right) \implies (\iota(a) = \iota(b))$$

A *modulated Cauchy algebra homomorphism* is a function $f:B^A$ between modulated Cauchy algebras $A$ and $B$ such that 

$$\forall a \in C(\mathbb{Q}). f(\iota_A(a)) = \iota_B(a)$$

The *category of modulated Cauchy algebras* is the category $MCAlg$ whose objects $Ob(MCAlg)$ are modulated Cauchy algebras and whose morphisms $Mor(MCAlg)$ are modulated Cauchy algebra homomorphisms. The set of **modulated Cauchy real numbers**, denoted $\mathbb{R}_C$, is defined as the initial object in the category of modulated Cauchy algebras. 

#### As a quotient inductive type

The __modulated Cauchy real numbers__ $\mathbb{R}_C$ are a [[quotient inductive type]] inductively generated by the following:

* a function $\iota: C(\mathbb{Q}) \to \mathbb{R}_C$, where $C(\mathbb{Q})$ is the type of [[Cauchy approximation]]s in $\mathbb{Q}$.  

* a dependent family of terms
$$a:C(\mathbb{Q}), b:C(\mathbb{Q}) \vdash eq_{\mathbb{R}_C}(a, b): \left( \prod_{\epsilon:\mathbb{Q}_{+}} \vert a_\epsilon - b_\epsilon \vert \lt 4 \epsilon \right) \to (\iota(a) =_{\mathbb{R}_C} \iota(b))$$

* a family of dependent terms 
$$a:\mathbb{R}_C, b:\mathbb{R}_C \vdash \tau(a, b): isProp(a =_{\mathbb{R}_C} b)$$

This is the approach of [Booij20](#Booij20)

### Generalisations

While requiring a modulus of convergence, even fixing the modulus of convergence, may be more restrictive, it is also possible to use a potentially more lax definition.

One way is to use [[multivalued functions]] from the natural numbers.  A __multivalued Cauchy real number__ $x$ is an [[entire relation]] between natural numbers and rational numbers such that, for every positive rational number $\epsilon$, there exists a natural number $\alpha$ such that, whenever $i, j \geq \alpha$,
$$ {|a - b|} \leq \epsilon $$
holds for some $a,b$ such that $x_{i,a}$ and $x_{j,b}$ hold.  Two multivalued Cauchy real numbers are considered __equal__ if, for every positive rational number $\epsilon$, there exists a natural number $\alpha$ such that, whenever $i \geq \alpha$,
$$ {|a - b|} \leq \epsilon $$
holds for some $a,b$ such that $x_{i,a}$ and $y_{i,b}$ hold. The partial equivalence relation subsuming both conditions is that, for every positive rational number $\epsilon$, there exists a natural number $\alpha$ such that, whenever $i,j \geq \alpha$,
$$ {|a - b|} \leq \epsilon $$
holds for some $a,b$ such that $x_{i,a}$ and $y_{j,b}$.

Another way is to use [[nets]] (also called 'generalised sequences').  A __generalised Cauchy real number__ $x$ is a net $(x_\nu)_{\nu\colon D}$ (where $D$ is any [[directed set]] of indices) of rational numbers such that, for every positive rational number $\epsilon$, there exists an index $\alpha$ in $D$ such that
$$ {|x_i - x_j|} \leq \epsilon $$
holds whenever $i,j \geq \alpha$ in $D$.  Two generalised Cauchy real numbers $x,y$ are considered __equal__ if, for every positive rational number $\epsilon$, there exists an index $\alpha$ for $x$ and an index $\beta$ for $y$ such that
$$ {|x_i - y_j|} \leq \epsilon $$
holds whenever $i \geq \alpha$ and $j \geq \beta$.  Actually, this is already a partial equivalence relation on all nets which subsumes both conditions.

Requiring a modulus of convergence would make no difference for either of these, since we would expect such a modulus to also to be either multivalued or given by a net, and these are easy to construct explicitly (even in constructive	mathematics).

(Since the term 'Cauchy real number' logically applies just as well to these generalisations, we may speak of __sequential real numbers__ for the classical or modulated version.)


### Relations between these definitions

Classically, all of these definitions are equivalent.  In fact, to prove their equivalence, we need only the principle of __[[weak countable choice]]__ ($WCC$):  A [[surjective function]] $f\colon S \to \mathbb{N}$ [[split epic|splits]], if, whenever $i \ne j$, either $f^*(i)$ or $f^*(j)$ is a [[singleton]].  (This is a rather special case of [[countable choice]] that can also be proved using only [[excluded middle]].)

If we don\'t accept $WCC$, then we still have these results:

+-- {: .un_theorem}
###### Theorems
(constructive).

Given any modulus of convergence $\alpha$, every $\alpha$-regular Cauchy real number is a modulated Cauchy real number.  Furthermore, any two $\alpha$-regular real numbers are equal as $\alpha$-regular real numbers if and only if they are equal as modulated Cauchy real numbers.  Conversely, every modulated Cauchy real number is equal (as a modulated Cauchy real number) to some $\alpha$-regular Cauchy real number.

Every modulated Cauchy real number is a classical Cauchy real number, and any two equal modulated Cauchy real numbers are equal as classical Cauchy real numbers.

Every classical Cauchy real number is a multivalued Cauchy real number, and any two equal classical Cauchy real numbers are equal as multivalued Cauchy real numbers.

Every multivalued Cauchy real number becomes a generalised Cauchy real number whose index set $D$ comes equipped with a surjection to the natural numbers.  Furthermore, any two multivalued Cauchy real numbers are equal as multivalued Cauchy real numbers if and only if they are equal as generalised Cauchy real numbers.  Conversely, any generalised Cauchy real number is equal (as a generalised Cauchy real number) to some multivalued Cauchy real number.

Every generalised Cauchy real number becomes a [[Dedekind real number]] in the usual way, defining lower and upper sets in terms of the order relation on generalised Cauchy real numbers.  Furthermore, any two generalised Cauchy real numbers are equal as generalised Cauchy real numbers if and only if they are equal as Dedekind cuts.  Conversely, any Dedekind cut is equal (as a Dedekind cut) to some generalised Cauchy real number.
=--

Hence even in [[constructive mathematics]], there are only three notions that we need consider: modulated Cauchy real numbers, classical Cauchy real numbers, and Dedekind real numbers; and there is a [[function]] from each of these to the next.

Just to be explicit, here are the missing converses:

+-- {: .un_theorem}
###### Theorems
(assuming $WCC$).

Every classical Cauchy real number is modulated, and any two equal Cauchy real numbers are equal as modulated Cauchy real numbers.

Every multivalued Cauchy real number is equal (as a multivalued Cauchy real number) to some classical Cauchy real number, and two classical Cauchy real numbers are equal if they are equal as multivalued Cauchy real numbers.
=--

Most practitioners of both [[constructive mathematics]] and [[topos theory]] want to use the Dedekind real numbers.  Without $WCC$, the classical Cauchy real numbers are not very well behaved.  The modulated Cauchy real numbers, however, do have their good points; for example, the [[fundamental theorem of algebra]] is simplest for them.  They also make sense in [[predicative mathematics]] with [[function sets]], whereas the Dedekind reals require [[powersets]] for their definition.

On the other hand, even the (modulated) Cauchy real numbers are not necessarily Cauchy complete, i.e. a Cauchy sequence (even a modulated one) of Cauchy real numbers need not converge to another Cauchy real number (though it always does converge to a Dedekind real number, since the Dedekind real numbers *are* always Cauchy complete).  The problem is that without countable choice, we cannot lift a (modulated) Cauchy sequence of (modulated Cauchy) real numbers to a Cauchy sequence of Cauchy sequences in order to "diagonalize" it; a countermodel is constructed by [Lubarsky](#Lubarsky).

For non-modulated Cauchy sequences and reals, there are additional problems even if we assume representatives are already chosen.  A modulated Cauchy sequence of modulated Cauchy sequences does converge to a modulated Cauchy sequence.  Moreover, a *modulated* Cauchy sequence of *classical* Cauchy sequences, and a *classical* Cauchy sequence of *modulated* Cauchy sequences, both necessarily converge to a *classical* Cauchy sequence.  But the results need not be modulated, and a classical Cauchy sequence of classical Cauchy sequences need not converge to a classical Cauchy sequence.  In fact, [Lubarsky](#Lubarsky) shows that:

* The generic classical Cauchy sequence, in the [[classifying topos]] of classical Cauchy sequences, is not modulated.  Thus, we cannot prove that every classical Cauchy sequence is modulated.  Hence, we cannot prove that a classical Cauchy sequence of modulated Cauchy sequences has a modulated limit (since a classical Cauchy sequence of rationals can be regarded as a classical Cauchy sequence of (constant) modulated Cauchy sequences).

* The generic classical Cauchy sequence of classical Cauchy sequences, in the classifying topos of such, does not converge to a classical Cauchy sequence.

* The generic modulated Cauchy sequence of classical Cauchy sequences, in the classifying topos of such, does not converge to a modulated Cauchy sequence.

(Actually, Lubarsky writes using [[Heyting-valued sets]] on topological spaces rather than classifying toposes of propositional [[geometric theories]], but it seems almost certain to me that his results can be rephrased as the above.)

## Locators

* A [[locator]] is equivalent to having the structure of a [[Cauchy sequence]] with [[modulus of convergence]]. This is stronger than merely being a modulated Cauchy real number.

## Algebraic closure

The [[algebraic closure]] of the modulated Cauchy real numbers is the modulated Cauchy [[complex numbers]]; i.e. the [[fundamental theorem of algebra]] is true for the modulated Cauchy real numbers. 

## Generalisations

Although the notion of [[metric space]] doesn\'t make sense until we know what real numbers are, once we have these, we can recognise that the rational numbers form a metric space $\mathbb{Q}$ and the real numbers were constructed from them in a way that makes reference only to the metric-space structure of $\mathbb{Q}$.  Thus, this procedure may be generalised to any metric space to produce its [[complete metric space|completion]].

We can also interpret $\mathbb{Q}$ as a [[uniform space]] or even as a [[Cauchy space]] and define analogous notions of completion for these.  However, these require us (in general) to use generalised Cauchy sequences, that is Cauchy [[nets]], even in classical mathematics.  (Of course, without [[weak countable choice]], we should use nets even for metric spaces.)

## Motivation

Suppose that we wish to approximate a real number $x$ by common fractions with arbitrarily large denominators.  That is, given any natural number $i$, we wish to find [[integers]] $a_i$ such that $x_i \coloneqq a_i/i$ is within $1/i$ of $x$.  Then the sequence of values $(0,x_1,x_2,x_3,\ldots)$ is an $\alpha$-regular Cauchy real with $\alpha(1/i) \coloneqq i$ as modulus of convergence.  (You can extend $\alpha$ to every positive rational number by $\alpha(\epsilon) \coloneqq \lfloor{1/\epsilon}\rfloor$, but that is not important.)  Conversely, given an $\alpha$-regular Cauchy real $(x_0,x_1,x_2,\ldots)$ for this modulus $\alpha$, we can round each $x_i$ (for $i \gt 0$) to the nearest rational number with denominator $i$ (which can be done using only rational arithmetic) to produce an equal $\alpha$-regular Cauchy real.

We might instead want to approximate $x$ by arbitrarily long decimal fractions.  That is, given any natural number $i$, we wish to find integers $a_i$ such that $x_i \coloneqq a_i/10^i$ is within $1/10^i$ of $x$.  Now the sequence of values $(x_0,x_1,x_2,\ldots)$ is an $\alpha$-regular Cauchy real with $\alpha(1/10^i) \coloneqq i$ as modulus of convergence.  Conversely, we can round off the values of any $\alpha$-regular Cauchy real as before.  Of course, there is nothing special about the base $10$ here; for theoretical purposes, base $2$ is popular.

Thus, to *define* a real number to be an $\alpha$-regular Cauchy real (for any of these choices of $\alpha$) is to make into a definition our intuition that we can round real numbers in this way.

Note we may be rounding up or down, regardless of which is nearer.  For example, in approximating $e = \exp\,1$ by decimal fractions, we might get ($2,2.7,2.71,\ldots)$ or $(3,2.7,2.72,\ldots)$, but we might also get $(2,2.8,2.71,\ldots)$.  To choose to always round down, towards zero, or towards the nearer approximant (with a rule for $0.5$) requires an application of [[excluded middle]] (or at least the [[lesser limited principle of omniscience]]).

Even for Dedekind reals without $WCC$, we can always approximate a real number in this way up to any given $i$.  Choice is needed only to make infinitely many approximations at once.  Trying to avoid this can motivate multivalued Cauchy real numbers.

## See also ##

* [[generalized Cauchy real number]]
* [[HoTT book real number]]
* [[Eudoxus real number]]
* [[prealgebra real number]]
* [[locator]]

## References

*  [[Georg Cantor]]; 1872; _[Ueber die Ausdehnung eines Satzes aus der Theorie der trigonometrischen Reihen](http://www.maths.tcd.ie/pub/HistMath/People/Cantor/Ausdehnung/)_; Section 1.

*  [[Fred Richman]], Douglas Bridges, Peter Schuster; 1998; _A weak countable choice principle_; available from <http://math.fau.edu/richman/html/docs.htm>.

On why Cauchy sequences with a modulus of convergence are sequentially Cauchy complete. 

*  [[Fred Richman]]; 1998; _The fundamental theorem of algebra: a constructive development without choice_; available from <http://math.fau.edu/richman/html/docs.htm>.

On why the modulated Cauchy real numbers are not [[sequentially Cauchy complete]]

* [[Robert Lubarsky]], _On the Cauchy Completeness of the Constructive Cauchy Reals_, [doi](https://doi.org/10.1016/j.entcs.2006.09.012)
 {#Lubarsky}

* Auke Booij, *Extensional constructive real analysis via locators*, ([abs:1805.06781](https://arxiv.org/abs/1805.06781))

A [[constructive mathematics|constructive]] algebraic proof of the [[fundamental theorem of algebra]] for the [[modulated Cauchy real numbers]] without choice princples such as [[weak countable choice]]

* Wim Ruitenberg, Constructing Roots of Polynomials over the Complex Numbers, Computational Aspects of Lie Group Representations and Related Topics, CWI Tract, Vol. 84, Centre for Mathematics and Computer Science, Amsterdam, 1991, pp. 107–128. ([pdf](https://www.mscsnet.mu.edu/~wim/publica/roots_new.pdf))

Formalization of Cauchy real numbers in [[homotopy type theory]] is discussed in 

* [[Egbert Rijke]], [[Bas Spitters]], _Cauchy reals in the univalent foundations_ (talk notes, May 2013) ([pdf](http://www.cs.ru.nl/~spitters/presentation_reals.pdf))
* {#Booij20} Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))
* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects Cauchy real number]]
[[!redirects Cachy real number]]
[[!redirects Cauchy real numbers]]
[[!redirects Cauchy real]]
[[!redirects Cauchy reals]]

[[!redirects Cantor real number]]
[[!redirects Cantor real numbers]]
[[!redirects Cantor real]]
[[!redirects Cantor reals]]

[[!redirects modulated Cauchy real number]]
[[!redirects modulated Cauchy real numbers]]
[[!redirects modulated Cauchy real]]
[[!redirects modulated Cauchy reals]]

[[!redirects regular Cauchy real number]]
[[!redirects regular Cauchy real numbers]]
[[!redirects regular Cauchy real]]
[[!redirects regular Cauchy reals]]

[[!redirects sequential real number]]
[[!redirects sequential real numbers]]
[[!redirects sequential real]]
[[!redirects sequential reals]]
