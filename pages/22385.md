+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Setoids
* table of contents
{: toc}

## Idea

A **setoid** is a collection of things (which could be a [[set]], a [[type]], or a [[preset]] depending on the chosen [[foundations]]) equipped with an [[equivalence relation]] or a [[pseudo-equivalence relation]]. Setoids are commonly used in "impoverished" foundations of mathematics that lack a primitive notion of [[quotient]]; see for instance [[Bishop set]].

## Definition with pseudo equivalence relation

### With a set and a family of sets

Using graph theoretic terminology, a **setoid** is a loop [[directed pseudograph]], a [[set]] $V$ of **vertices** with a family of sets $E(a, b)$ of **edges** for each vertex $a \in A$ and $b \in A$, which comes with the following additional structure 

* for each vertex $a \in A$ a family of edges 
$$\mathrm{refl}(a) \in E(a, a)$$ 

* for each vertex $a \in A$ and $b \in A$ a family of functions
$$\mathrm{sym}(a, b):E(a, b) \to E(b, a)$$

* for each vertex $a \in A$, $b \in A$, and $c \in A$, a family of functions
$$\mathrm{trans}(a, b, c):(E(a, b) \times E(b, c)) \to E(a, c)$$

The edge family $(E, \mathrm{refl}, \mathrm{sym}, \mathrm{trans})$ is called a **pseudo-equivalence relation**. 

### With two sets

A **setoid** is a [[set]] $V$ with a set $E$ and functions $s:E \to V$, $t:E \to V$ (a loop [[directed pseudograph]]), with with functions $\mathrm{refl}:V \to E$, $\mathrm{sym}:E \to E$, and  
$$\mathrm{trans}:\{(f,g) \in E \times E \vert t(f) =_V s(g)\} \to E$$ 
such that 

* for every $a \in V$, $s(\mathrm{refl}(a)) =_E a$
* for every $a \in V$, $t(\mathrm{refl}(a)) =_E a$
* for every $f \in E$, $s(f) =_V t(\mathrm{sym}(f))$
* for every $f \in E$, $t(f) =_V s(\mathrm{sym}(f))$
* for every $f \in E$ and $g \in E$ such that $t(f) =_V s(g)$, $s(\mathrm{trans}(f,g)) =_E s(f)$ 
* for every $f \in E$ and $g \in E$ such that $t(f) =_V s(g)$, $t(\mathrm{trans}(f,g)) =_E t(g)$

The structure $(E, s:E \to V, t:E \to V)$ is called a **pseudo-equivalence relation**. 

### Extensional functions

We define an **extensional function** $f:A \to B$ between two setoids $A = (V_A, E_A, \mathrm{refl}_A, \mathrm{sym}_A, \mathrm{trans}_A)$ and $B = (V_B, E_B, \mathrm{refl}_B, \mathrm{sym}_B, \mathrm{trans}_B)$ to be a function $f_V:V_A \to V_B$ and a family of functions $f_E(a, b):E_A(a, b) \to E_B(f_V(a), f_V(b))$ such that 
$$f_E(a, a)(\mathrm{refl}_A(a)) = \mathrm{refl}_B(f_V(a))$$
$$f_E(a, b)(\mathrm{sym}_A(a, b)(f)) = \mathrm{sym}_B(f_V(a), f_V(b))(f_E(a, b)(f))$$
$$f_E(a, c)(\mathrm{trans}_A(f,g)) = \mathrm{trans}_B(f_E(a, b)(f), f_E(b, c)(g)$$

### Equivalence of definitions

Given a one-set-of-edges setoid $E\rightrightarrows V$, we define a family-of-sets-of-edges setoid by taking $E(x,y)$ to be the [[preimage]] of $(x,y)$ under the [[function]] $(s,t):E \to V\times V$.  Conversely, given a family-of-sets-of-edges setoid we define a one-set-of-edges setoid by taking $E$ to be the [[disjoint union]] of the families of morphisms $E = \coprod_{x,y\in V} E(x,y)$. 

...

## Examples

Every [[category]] with a [[contravariant functor|contravariant]] [[endofunctor]] that is the [[identity-on-objects]] is a [[setoid]] where

* for every vertex $a:V$, $b:V$, $c:V$, and $d:V$ and morphisms $f:E(a, b)$, $g:E(b, c)$, and $h:E(c, d)$
$$\mathrm{trans}(a, b, d)(f, \mathrm{trans}(b, c, d)(g, h)) = \mathrm{trans}(a, c, d)(\mathrm{trans}(a, b, c)(f, g), h)$$

* for every vertex $a:V$, $b:V$ and morphism $f:E(a, b)$
$$\mathrm{trans}(a, b, b)(f, \mathrm{refl}(b)) = f$$

* for every vertex $a:V$, $b:V$ and morphism $f:E(a, b)$
$$\mathrm{trans}(a, a, b)(\mathrm{refl}(a), f) = f$$

This includes [[dagger categories]], where additionally

* for every vertex $a:V$, $b:V$ and morphism $f:E(a, b)$
$$\mathrm{sym}(a, b)(\mathrm{sym}(b, a)(f)) = f$$

* for every vertex $a:V$, $b:V$, $c:V$ and morphism $f:E(a, b)$, $g:E(b, c)$
$$\mathrm{sym}(a, c)(\mathrm{trans}(a, b, c)(f, g)) = \mathrm{trans}(c, b, a)(\mathrm{sym}(a, b)(f), \mathrm{sym}(b, c)(g))$$

* for every vertex $a:V$
$$\mathrm{sym}(a, a)(\mathrm{refl}(a)) = \mathrm{refl}(a)$$

and [[groupoids]], where

* for every vertex $a:V$, $b:V$ and morphism $f:E(a, b)$
$$\mathrm{trans}(a, b, a)(f, \mathrm{sym}(a, b)(f)) = \mathrm{refl}(a)$$

* for every vertex $a:V$, $b:V$ and morphism $f:E(a, b)$
$$\mathrm{trans}(b, a, b)(\mathrm{sym}(a, b)(f), f) = \mathrm{refl}(b)$$

## Core of a setoid

For any setoid $A$, the [[core]] of $A$ is defined as the maximal [[subgroupoid]] $\mathrm{Core}(A)$ of $A$. 

More specifically, a subsetoid $G$ of a setoid $A$ is a setoid $G$ with an extensional function $f:G \to A$ such that $f_V:V_G \to V_A$ is an [[injection]], and for all vertices $a:V_G$ and $b:V_G$ the function $f_E(a, b):E_{G}(a, b) \to E_A(a, b)$ is an injection. 

A subsetoid $G$ of $A$ is a subgroupoid if the edges of $G$ additionally satisfy the groupoid dependent equational axioms. 

A subgroupoid $G$ of a setoid $A$ is a maximal subgroupoid if for every other subgroupoid $H$ of $A$ the... 

## In homotopy type theory

In [[homotopy type theory]] (and more generally in any [[intensional type theory]]), the definitions above define a "[[strict setoid]]". 

When the vertex types are only required to be a [[type]] rather than a [[set]], then this defines a "[[presetoid]]", and when additionally the edge types are only required to be a type, then this defines a "[[wild setoid]]". 

There is also the notion of a [[univalent setoid]], which is a [[presetoid]] $A$ whose canonical functions 
$$\mathrm{idtocorehoms}(a, b):(a =_A b) \to (a \cong_A b)$$
from the [[identity type]] of elements $a:A$ and $b:A$ to the hom-set of $a:A$ and $b:A$ of the [[core]] [[pregroupoid]] $\mathrm{Core}(A)$ is an [[equivalence in homotopy type theory|equivalence of types]]. 

## Definition with equivalence relation

### In graph theory

A **setoid** is a [[loop digraph object|loop]] [[digraph]] $(V, E, s:E \to V, t:E \to V)$ with functions $refl:V \to E$, $sym:E \to E$, and  
$$tr:\{(f,g) \in E \times E \vert t(f) =_V s(g)\} \to E$$ 
such that 

* for every $f \in E$, $s(f) =_V t(sym(f))$
* for every $f \in E$, $t(f) =_V s(sym(f))$
* for every $f \in E$, $sym(sym(f)) =_E f$
* for every $a \in V$, $sym(refl(a)) =_E refl(a)$
* for every $f \in E$, $s(tr(g,f)) =_E s(f)$ 
* for every $f \in E$, $t(tr(g,f)) =_E t(g)$
* for every $f \in E$, $tr(f, refl(s(f))) =_E f$ 
* for every $f \in E$, $tr(refl(t(f)), f) =_E f$ 
* for every $f \in E$ and $g \in E$ such that $t(f) =_V s(g)$, $sym(tr(g,f)) =_E tr(sym(f),sym(g)$. 
* for every $f \in E$, $g \in E$, and $h \in E$ such that $t(f) =_V s(g)$ and $t(g) =_V s(h)$, $tr(h,tr(g,f)) =_E tr(tr(h,g),f)$

### In category theory

A **setoid** is a [[thin category|thin]] [[dagger category]], or a dagger category [[enriched category|enriched]] in [[truth values]]. 

The [[groupoidal categorification]] of a setoid is a [[dagger category]]. 

### In type theory

Many [[foundations]] based on [[type theory]], such as those of Per Martin-L&#246;f and Thierry Coquand, use [[type|types]], which sometimes called 'sets', but they don\'t have [[quotient set|quotients]]. A **setoid** is a type $T$ equipped with an [[equivalence relation]] $\equiv$. Sometimes these are called "[[presets]]", but strictly speaking, they are not presets, as these types have [[identity types]], while presets do not. 

Some foundations also adopt an [[axiom of choice]] for functions which do not preserve the equivalence relation that, together with the identity relations, proves the [[presentation axiom]] for general sets, which means that free sets are completely presented sets. 

If you are willing to accept the [[presentation axiom]], then you can define a notion of setoid internal to a given theory of sets: as a [[projective set]].  (With the full axiom of choice, therefore, a setoid is simply a set.)  Alternatively, you might forgo setoid as such but define a [[prefunction]] between sets to be an entire relation.

A similar result holds for [[SEAR plus epsilon|SEAR+$\epsilon$]].

## Category of setoids

Let the category $ExtType$ be defined as a [[weak category|weak]] [[category]] that is [[finitely complete category|finitely complete]], [[extensive category|infinitary extensive]], and [[well-pointed category|well-pointed]] (i.e. whose [[terminal object]] is a [[extremal epimorphism|extremal]] [[separator|generating object]]). $ExtType$ is the [[categorical semantics]] of an [[extensional type theory]] (whose types are extensional types) without quotient types (see above) such as Martin-Löf type theory. While some think of extensional types as [[presets]], extensional types still have another notion of equality, represented by the [[diagonal morphism]] $\Delta_A: A \rightarrow A \times A$ which could be found in any [[well-pointed category]] with [[finite products]]. See [[tobybartels:preset]] for a discussion of this issue.

The category [[Set|$Set$]] of [[set|sets]] is the [[full subcategory]] of $ExtType$ where all [[congruence|equivalence prerelations]] have [[effective epimorphism|effective]] [[quotient object|quotients]], and the category $Setoid$ of __[[setoid|setoids]]__ and is the [[exact completion|ex/lex completion]] of $ExtType$. This means both $Set$ and $Setoid$ are [[Grothendieck topos|Grothendieck topoi]] over the [[point]] satisfying [[Giraud's axioms]]. As the ex/lex completion is a [[free completion]], there is a [[free functor]] $F: ExtType \rightarrow Set$ that is the left adjoint of the [[forgetful functor]] $U: Set \rightarrow ExtType$, and $Setoid$ could also be thought of as a subcategory of $Set$, as the category of __[[free object|free]] sets__. (Note that the cofree set on a preset always exists; it is a [[subsingleton]].)

If the [[presentation axiom]] (a weak form of the full axiom of choice) holds in $ExtType$, as a subcategory of $Set$, $ExtType$ could be thought of as the category of [[completely presented sets]], the category of sets with a [[projective presentation]]. If the [[axiom of choice]] holds in $ExtType$, then $ExtType$ is equivalent to $Setoid$, as the axiom of choice implies that $Preset$ is its own free exact completion, and $ExtType$ is equivalent to $Set$ because the free functor from $ExtType$ to $Set$ is an [[equivalence of categories]]. 

## Applications

In [[constructive mathematics]], we want the [[real numbers]] to form a [[linearly ordered set|linearly ordered]] [[Heyting field]] $R$ with completeness for located [[Dedekind cuts]].  Using [[power sets]] and a set $N$ of [[natural numbers]], one may form $R$ directly as a [[subset]] of $\mathcal{P}N$ (or something equivalent), but what if you wish to be (at least weakly) [[predicative mathematics|predicative]]? Using [[function sets]], one may form the Cauchy reals as a [[subquotient]] of $N^N$, but these are complete in the desired sense only if a weak form of [[countable choice]] (which follows from either the presentation axiom or [[excluded middle]]) holds. (Essentially, there may not be enough [[sequences]] of natural numbers.) Alternatively, if you have them, you can use [[prefunction]] sets and form $R$ as a subquotient of the set of _presequences_ of natural numbers.

The construction of $R$ above may also be done with entire relations if the [[axiom of fullness]] holds (see also [[real numbers object]]). Conversely, the axiom of fullness follows from the existence of sets of prefunctions; in addition to defining a functional entire prerelation, a prefunction between sets also defines an entire relation, and the set of these satisfies fullness.  (This is related to the idea that prefunctions between sets may be formalised as entire relations.)

See also the discussion at [[net]] about how to force the domain of a net to be [[partially ordered|partial order]], by using either entire relations or prefunctions as nets.

## Fixing inadequate foundations

Sometimes one finds a [[foundation]] of [[predicative mathematics]] in which it appears to be impossible to construct [[quotient sets]], leading to much hand-wringing.  (For a simple example, simply remove the axiom of [[power sets]] from [[ZFC]] as normally presented.)  

Assuming (as usual) that the original foundation had equality relations on its sets, there will be identity prerelations on the presets, leading to a special class of sets which we may again call the __completely presented sets__. 

When you do this, the new kind of set is called a setoid, and then there may be hand-wringing about the need to use setoids instead of sets as one would like.  But if you didn\'t have quotient sets originally, then you shouldn\'t have been talking about 'sets' in the first place; theories of sets without quotient sets are really theories of types. 

## See also 

* [[directed graph]]
* [[thin category]]
* [[equivalence relation]]
* [[extensional function]]
* [[univalent setoid]]
* [[stable setoid]]
* [[internal setoid]]
* [[completely presented set]]
* [[monoidal setoid]]
* [[enriched setoid]]
* [[complete loop graph]]

[[!include oidification - table]]

[[!include types and logic - table]]

[[!redirects setoids]]