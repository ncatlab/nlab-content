
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[set theory]] and the [[foundations]] of mathematics, the axiom of __fullness__ is an axiom intermediate in strength between the existence of [[power sets]] and [[function sets]].  Of course, these can only be distinguished in [[constructive mathematics]], since classically power sets and function sets are equivalent (at least if you have the set $\mathbb{2} = \{\top, \bot\}$).

## Statements

### In set theory

The **axiom of fullness** states that, given any [[sets]] $X$ and $Y$, there is a set $F_{X,Y}$ of _enough [[entire relations]]_ from $X$ to $Y$ in this sense:

*  Every element of $F_{X,Y}$ is an entire relation from $X$ to $Y$;
*  If $R$ is an entire relation from $X$ to $Y$, then for some $S \in F_{X,Y}$, $S \subseteq R$.

We have written this in a [[material set theory|material]] fashion; [[structural set theory|structurally]], the axiom says that $F_{X,Y}$ *parametrises* enough entire relations in this sense:

*  There is a [[subset]] $E_{X,Y}$ of $F_{X,Y} \times X \times Y$ such that:

   *  for every element $r$ of $F_{X,Y}$ and every element $a$ of $X$, there is an element $b$ of $Y$ such that $(r,a,b) \in E_{X,Y}$;

   (we think of $E_{X,Y}$ as giving the evaluation, as a [[truth value]], of $r$, as an entire relation, on the elements $a$ and $b$).

*  If $R$ is an entire relation from $X$ to $Y$, then for some $s$ in $F_{X,Y}$:

   *  for every element $a$ of $X$ and $b$ of $Y$, if $(s,a,b) \in E_{X,Y}$, then $a$ is $R$-related to $b$;

   (we think of $s$ as an entire relation via $E_{X,Y}$ and say that it is contained in $R$).

In the context of material set theory, the structural axiom is weaker than the material axiom, but they become equivalent in the presence of [[axiom of replacement|restricted replacement]], which is quite weak.

You can also write down an [[internalization|internal]] version of fullness by adding arbitrary additional parameters to the structural version above (analogously to the generalisation from [[power set]] to [[power object]], although more complicated since $F_{X,Y}$ is not given by a [[universal property]]).  

Given [[function sets]], fullness is equivalent to the set theory having sets of [[inhabited]] [[subsets]], since an entire relation between $A$ and $B$ is a [[function]] from $A$ to the set of inhabited subsets of $B$. (Power sets on the other hand are sets of *all* subsets). 

### In dependent type theory

In [[dependent type theory]], given a [[Russell universe]] $U$, the type of all [[entire relations]] between types $A:U$ and $B:U$ is given by the type 

$$\sum_{R:A \times B \to U} \prod_{x:A} \left(\prod_{y:A} \mathrm{isProp}(R(x, y))\right) \times \exists y:A.R(x, y)$$

In general, this type is not [[small type|$U$-small]]. The **axiom of fullness** for $U$ states that the above type is $U$-small, and is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U}{\Gamma \vdash \mathrm{EntRel}(A, B):U}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U}{\Gamma \vdash \mathrm{EntRel}(A, B) \equiv \sum_{R:A \times B \to U} \prod_{x:A} \left(\prod_{y:A} \mathrm{isProp}(R(x, y))\right) \times \exists y:A.R(x, y) \; \mathrm{type}}$$

Similarly, for [[Tarski universes]] $(U, T)$, the type of all entire relations between $U$-small types $A:U$ and $B:U$ is given by the type 

$$\sum_{R:T(A) \times T(B) \to U} \prod_{x:T(A)} \left(\prod_{y:T(A)} \mathrm{isProp}(T(R(x, y)))\right) \times \exists y:T(A).T(R(x, y))$$

There are similar inference rules for [[strict Tarski universes]]:

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U}{\Gamma \vdash \mathrm{EntRel}(A, B):U}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U}{\Gamma \vdash T(\mathrm{EntRel}(A, B)) \equiv \sum_{R:T(A) \times T(B) \to U} \prod_{x:T(A)} \left(\prod_{y:T(A)} \mathrm{isProp}(T(R(x, y)))\right) \times \exists y:T(A).T(R(x, y)) \; \mathrm{type}}$$

For [[weak Tarski universes]], one uses an [[equivalence of types]] instead of [[judgmental equality]]

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U}{\Gamma \vdash \mathrm{fullness}(A, B):T(\mathrm{EntRel}(A, B)) \simeq \sum_{R:T(A) \times T(B) \to U} \prod_{x:T(A)} \left(\prod_{y:T(A)} \mathrm{isProp}(T(R(x, y)))\right) \times \exists y:T(A).T(R(x, y))}$$

and the two inference rules could be reduced down to the element:

$$\mathrm{fullness}:\sum_{F:U \times U \to U} \prod_{A:U} \prod_{B:U} T(F(A, B)) \simeq \sum_{R:T(A) \times T(B) \to U} \prod_{x:T(A)} \left(\prod_{y:T(A)} \mathrm{isProp}(T(R(x, y)))\right) \times \exists y:T(A).T(R(x, y))$$

If the dependent type theory does not have any type universes at all, one could still express the axiom of fullness by explicitly postulating the [[type of all entire relations]] using [[inference rules]]. 

## Relation to other axioms

In the presence of the usual basic axioms of set theory (in particular, the axioms of [[bounded separation]] and [[axiom of pairing|pairing]] in a material set theory and the existence of [[equalisers]] and [[products]] in a structural set theory), we have:

> power sets &#8594; fullness &#8594; function sets

On the one hand, $F_{X,Y}$ can be constructed as the [[subset]] of the [[power set]] $\mathcal{P}(X \times Y)$ consisting of *all* entire relations from $X$ to $Y$.  On the other hand, the [[function set]] $Y^X$ may be constructed as a subset of $F_{X,Y}$ consisting of those elements $S$ such that $S \subseteq R$ for $R$ (the graph of) some function from $X$ to $Y$; (the key here is that $S = R$ must follow when $S$ is entire and $R$ is a function).  Conversely, if we have function sets, then the [[axiom of choice]] states precisely that the function set $Y^X$ always qualifies as $F_{X,Y}$ (although function sets and [[excluded middle]] are already sufficient for power sets and thus fullness).


Fullness also follows from function sets in the presence of [[COSHEP]], a fairly strong but constructive (in that it implies no general [[principle of omniscience]]) form of the [[axiom of choice]].  If $P$ is a [[projective set]] with a [[surjection]] $p\colon P \to X$ (which this axiom asserts must exist), then we may take $Y^P$ as $F_{X,Y}$, with $(r,a,b) \in E_{X,Y}$ iff, for some $c$ in $P$, $p(c) = a$ and $r(c) = b$.

Note that $F_{X,Y}$ is not categorical (in the logicians\' sense); that is, there may be many sets $F, F', \ldots$ that all satisfy the axiom without being (in an appropriate sense) equal.  This is the downside to adopting the fullness axiom, compared to power sets or function sets; this is also why the internal version is complicated.

As fullness is weaker than power sets in a constructive framework, we may consider it [[predicative mathematics|predicative]] in the sense of the constructive school; this is one reason for adopting it while rejecting power sets.  

## Definition of the real numbers

One reason for adopting the axiom of fullness instead of (only) function sets is this: it is strong enough to construct the set $\mathbb{R}$ of (located Dedekind) [[real numbers]] from the set $\mathbb{N}$ of [[natural numbers]] *without* assuming [[excluded middle]] or [[countable choice]]. Using [[function sets]], one can easily construct the set $\mathbb{R}_C$ of [[Cauchy reals]] as a [[subquotient]] of the function set $\mathbb{N}^{\mathbb{N}}$.  Both classical and constructive mathematicians usually adopt axioms in which one can prove that $\mathbb{R}$ is [[isomorphic]] to $\mathbb{R}_C$; this is equivalent to a [[weak countable choice]] principle $\mathrm{AC}_{\mathbb{N},2}$ that follows from either [[excluded middle]] (classically accepted) or [[countable choice]]. But there are (for example) some [[Grothendieck toposes]] in which $\mathbb{R}$ is not [[isomorphic]] to $\mathbb{R}_C$ (as a statement in the [[Mitchell–Bénabou language]]), so any sort of constructive mathematics that wants to apply to such toposes cannot rely on this method to define the [[real numbers object]] $\mathbb{R}$.

Of course, in a topos, there are other ways to define $\mathbb{R}$, but what if you want your theory to *also* be predicative?  If you adopt the fullness axiom, then you can modify the definition of $\mathbb{R}_C$ to produce a definition of $\mathbb{R}$ *without* assuming any choice principle.  Instead of using $\mathbb{N}^{\mathbb{N}}$, you use $F_{\mathbb{N},\mathbb{N}}$ instead; $\mathbb{R}$ can be constructed as a subquotient of that set.

Let an element of $F_{\mathbb{N},\mathbb{N}}$ be a _[[multivalued function|multivalued]] [[sequence]]_ of natural numbers, and fix a [[bijection]] $\phi\colon \mathbb{N} \to \mathbb{Q}$ between $\mathbb{N}$ and the set $\mathbb{Q}$ of [[rational numbers]].  We call such a multivalued sequence $r$ _regular_ if, whenever $i,j,x,y$ are natural numbers such that $r(i,x)$ and $r(j,y)$, we have
$$ {|\phi(x) - \phi(y)|} \leq 1/i + 1/j .$$
(It is common, but not really necessary in the presence of function sets, to use regular sequences instead of the more general Cauchy sequences when defining $\mathbb{R}_C$ in constructive mathematics, and we follow that here.)  We call two regular multivalued sequences $r,s$ _equivalent_ if, whenever $i,j,x,y$ are natural numbers such that $r(i,x)$ and $s(j,y)$, we have
$$ {|\phi(x) - \phi(y)|} \leq 1/i + 1/j .$$
Then this defines an [[equivalence relation]] on the set of regular multivalued sequences, and the [[quotient set]] is $\mathbb{R}$. (That is, it may be given, in the usual way, the structure of an [[Archimedean ordered field]] which is [[Dedekind complete]] relative to located pairs of upper and lower sets.)

However, on one hand, if one's goal is to have the real numbers, the axiom of fullness is overkill: one can simply just postulate the real numbers in any number of ways, such as a [[real numbers object]] or a [[terminal object|terminal]] [[Archimedean ordered field]]: they contain all real numbers by definition and are [[Dedekind complete]] relative to located pairs of upper and lower sets. In [[dependent type theory]], there is also a [[resizing axiom]] for [[Dedekind cuts]]. On the other hand, in [[constructive mathematics]], the set of real numbers is less well behaved then the [[locale of real numbers]], and it is currently unknown how to define the locale of real numbers with only the axiom of fullness. 

## Related concepts

* [[resizing axiom]]

* [[axiom of power sets]]

* [[axiom of function sets]]

* [[subset collection]]

## References

* [[Michael Shulman]], _Comparing material and structural set theories_ &lbrack;[arXiv:1808.05204](https://arxiv.org/abs/1808.05204)&rbrack;

category: foundational axiom

[[!redirects fullness]]
[[!redirects axiom of fullness]]
[[!redirects fullness axiom]]