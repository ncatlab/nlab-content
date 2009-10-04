In [[set theory]] and the [[foundations]] of mathematics, the axiom of __subset collection__, or __fullness__, is an axiom intermediate in strength between the existence of [[power set]]s and [[function set]]s.  Of course, these can only be distinguished in [[constructive mathematics]], since classically power sets and function sets are equiavelent (at least if you have the set $\mathbf{2} = \{\top, \bot\}$).


## Statements

In its guise as _fullness_, the axiom states that, given any [[sets]] $X$ and $Y$, there is a set $F_{X,Y}$ of _enough [[entire relation]]s_ from $X$ to $Y$ in this sense:

*  Every element of $F_{X,Y}$ is an entire relation from $X$ to $Y$;
*  If $R$ is an entire relation from $X$ to $Y$, then for some $S \in F_{X,Y}$, $S \subseteq R$.


We have written this in a material fashion; structurally the axiom says that $F_{X,Y}$ *parametrises* enough entire relations in this sense:

*  There is a [[subset]] $E_{X,Y}$ of $F_{X,Y} \times X \times Y$ such that:
   *  for every element $r$ of $F_{X,Y}$ and every element $b$ of $Y$, there is an element $a$ of $X$ such that $(r,a,b) \in E_{X,Y}$;
   *  (we think of $E_{X,Y}$ as giving the evaluation, as a [[truth value]], of $r$, as an entire relation, on the elements $a$ and $b$).
*  If $R$ is an entire relation from $X$ to $Y$, then for some $s$ in $F_{X,Y}$:
   *  for every element $a$ of $X$ and $b$ of $Y$, if $(s,a,b) \in E_{X,Y}$, then $a$ is $R$-related to $b$;
   *  (we think of $s$ as entire relation via $E_{X,Y}$ and say that it is contained in $R$).

(In the context of material set theory, the structural axiom is weaker than the material axiom, but they become equivalent in the presence of the [[axiom of replacement]].)

You can also write down an [[internalization|internal]] version of fullness by adding arbitrary additional parameters to the structural version above (analogously to the generalisation from [[power set]] to [[power object]]).  

In its guise as _subset collection_, the axiom states ...
+-- {: .query}
I need to look this up, including a proof of its constructive equivalence with fullness if that\'s not obvious.)
=--


## Relation to other axioms

In the presence of the usual basic axioms of set theory (in particular, the axioms of separation and pairing in a material set theory and the existence of equalisers and products in a structural set theory), we have:
> power set &#8594; fullness &#8594; function sets

On the one hand, $F_{X,Y}$ can be constructed as the [[subset]] of the [[power set]] $\mathcal{P}(X \times Y)$ consisting of *all* entire relations from $X$ to $Y$.  On the other hand, the [[function set]] $Y^X$ may be constructed as a subset of $F_{X,Y}$ consisting of those elements $S$ such that $S \subseteq R$ for $R$ (the graph of) some function from $X$ to $Y$.  (The key here is that $S = R$ must follow when $S$ is entire and $R$ is a function.)

Fullness follows from function sets in the presence of [[COSHEP]], a fairly strong but constructive form of the [[axiom of choice]].  If $P$ is a [[projective set]] with a [[surjection]] $p: P \to X$, then we may take $Y^P$ as $F_{X,Y}$, with $(r,a,b) \in E_{X,Y}$ iff, for some $c$ in $P$, $p(c) = a$ and $r(c) = b$.

Note that $F_{X,Y}$ is not categorical (in the logicians\' sense); that is, there may be many sets $F_{X,Y}, F'_{X,Y}, \ldots$ that all satisfy the axiom without being (in an appropriate sense) equal.  This is the downside to adopting the fullness axiom, compared to power sets or function sets.

As fullness is weaker than power set in a constructive framework, we may consider it [[predicative mathematics|predicative]] in the sense of the constructive school; this is one reason for adopting it while rejecting power set.  One reason for adopting it instead of (only) function sets is this: it is strong enough to construct the set $\mathbf{R}$ of (located Dedekind) [[real number]]s from the set $\mathbf{N}$ of [[natural number]]s *without* assuming [[excluded middle]] or [[countable choice]]; see below.


## Relation to type theory ##

Subset collection is justified by predicative versions of constructive [[type theory]] in the sense of Martin--L&#246;f or Thierry Coquand.  To see this, note that these theories justify [[COSHEP]]; their types define (not sets in general but) _[[preset]]s_ (following Bishop) or _[[completely presented set]]s_, which (as sets) are projective.  Analogously, an element of $F_{X,Y}$ may be considered an _operation_ or _prefunction_ (following 'preset') from $X$ to $Y$.

But note that the type of prefunctions from $X$ to $Y$, like the preset underlying $X$, is a categorical (unique) construction in type theory, while $F_{X,Y}$, like COSHEP, is not.  Thus type theory gives us constructions that are not available in set theory (even with fullness or even COSHEP), such as the predicate that states whether two functions have equal underlying prefunctions.


## Definition of $\mathbf{R}$ ##

We consider this application in some detail.

Using [[function set]]s alone, one can easily construct the set $\mathbf{R}_C$ of *Cauchy* reals as a [[subquotient]] of the function set $\mathbf{N}^{\mathbf{N}}$.  Both classical and constructive mathematicians usually adopt axioms in which one can prove that $\mathbf{R} = \mathbf{R}_C$; this is equivalent to a weak choice principle (identified by [[Fred Richman]] et al) that follows from either excluded middle (classically accepted) or countable choice (usually constructively accepted).  But there are (for example) some [[Grothendieck topos]]es in which $\mathbf{R} = \mathbf{R}_C$ (as a statement in the [[Mitchell–Bénabou language]]) fails, so any sort of constructive mathematics that wants to apply to such toposes cannot rely on this method to define $\mathbf{R}$.

Of course, in a topos, there are other ways to define $\mathbf{R}$, but what if you want your theory to *also* be predicative?  If you adopt the fullness axiom, then you can modify the definition of $\mathbf{R}_C$ to produce a definition of $\mathbf{R}$ *without* assuming any choice principle.  Instead of using $\mathbf{N}^{\mathbf{N}}$, you use $F_{\mathbf{N},\mathbf{N}}$ instead; $\mathbf{R}$ can be constructed as a subquotient of that set.

Let an element of $F_{\mathbf{N},\mathbf{N}}$ be a _pre[[sequence]]_ of natural numbers, and fix a [[bijection]] $\phi: \mathbf{N} \to \mathbf{Q}$ between $\mathbf{N}$ and the set $\mathbf{Q}$ of [[rational number]]s.  We call such a presequence $r$ _regular_ if, whenever $i,j,x,y$ are natural numbers such that $r(i,x)$ and $r(j,y)$, we have
$$ |\phi(x) - \phi(y)| \leq 1/i + 1/j .$$
(It is common, but not really necessary in the presence of function sets, to use regular sequences instead of the more general Cauchy sequences when defining $\mathbf{R}_C$ in constructive mathematics, and we follow that here.)  We call two regular presequences $r,s$ _equivalent_ if, whenever $i,j,x,y$ are natural numbers such that $r(i,x)$ and $s(j,y)$, we have
$$ |\phi(x) - \phi(y)| \leq 1/i + 1/j .$$
Then this defines an [[equivalence relation]] on the set of regular presequences, and the [[quotient set]] is $\mathbf{R}$.  (That is, it may be given, in the usual way, the structure of a [[linear order|linearly ordered]] Heyting [[field]] which is Dedekind complete using located pairs of upper and lower sets.)


category: foundational axiom

[[!redirects axiom of fullness]]
[[!redirects fullness axiom]]
[[!redirects axiom of subset collection]]