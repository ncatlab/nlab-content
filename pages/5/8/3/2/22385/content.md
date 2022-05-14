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

## Definition 

### In graph theory

A **setoid** is a [[loop digraph object|loop]] [[digraph]] $(V, E, s:E \to V, t:E \to V)$ with functions $refl:V \to E$, $sym:E \to E$, and  
$$tr:\{(f,g) \in E \times E \vert t(f) =_V s(g)\} \to E$$ 
such that 

* for every $a \in V$, $s(refl(a)) =_E a$
* for every $a \in V$, $t(refl(a)) =_E a$
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

[[!include types and logic - table]]

[[!redirects setoids]]