The commonly accepted standard [[foundation of mathematics]] today is a material [[set theory]], $\mathbf{ZFC}$ or Zermelo--Frankel set theory with the [[axiom of choice]].


## History

The first version was developed by [[Ernst Zermelo]] in 1908; in 1922, [[Abraham Fraenkel]] and [[Thoralf Skolem]] independently proposed a precise first-order version with the [[axiom of replacement]]; finally, Zermelo added the [[axiom of foundation]] in 1930.  All of these versions included the axiom of choice, but this was considered controversial for some time; one has merely $\mathbf{ZF}$ if it is taken out.

$\mathbf{ZFC}$ is similar to the [[class]] theories $\mathbf{NBG}$ (due to [[John von Neumann]], [[Paul Bernays]], and [[Kurt Gödel]]) and $\mathbf{MK}$ (due to [[Anthony Morse]] and [[John Kelley]]) are similar; the former is a conservative, finitely axiomatisable extension, while the latter is stronger, equivalent to postulating an [[inaccessible cardinal]].

Contemporary set theorists often accept additional [[large cardinal]] axioms.  There are also weak versions, especially for [[constructive mathematics|constructive]] and [[predicative mathematics|predicative]] mathematics.  Then there are alternatives on a different basis, notably $\mathbf{NFU}$ (a very impredicative material set theory) and **[[ETCS]]** (a [[structural set theory]]).

(My source for this history, especially the dates, is mostly [the English Wikipedia](http://en.wikipedia.org/wiki/Zermelo%E2%80%93Fraenkel_set_theory).)


## Axioms

$\mathbf{ZFC}$ is a [[material set theory]], based on a global binary __membership__ [[predicate]] $\in$.  Everything in standard $\mathbf{ZFC}$ is a [[pure set]], which we will call simply a set; but there are also variations with [[urelement]]s and [[classes]].  Urelements may be distinguished from sets and classes since they have no elements (although the [[empty set]] also has no elements); sets are those classes that are themselves elements (members) of sets.

1.  Extensionality:  If two sets (or classes) have the same members, then they are __[[equality|equal]]__ and themselves members of the same sets.  See [[axiom of extensionality]] for variations, such as whether this is taken as a definition or an axiomatisation of equality of sets, and how the condition might be strengthened if (10) is left out.

2.  Null Set:  There is an __[[empty set]]__: a set $\empty$ with no elements.  By (1), it follows that this set is unique; by even the weakest version of (5), it is enough to state the existence of some set.  (Analogous remarks apply to most of the other axioms.)

3.  Pairing:  If $a$ and $b$ are sets, then there is a set $\{a,b\}$, the __[[finite set|unordered pairing]]__ of $a$ and $b$, whose elements are precisely those sets equal to $A$ or $B$.  Between them, (2) and (3) form a nullary/binary pair; the unary version follows from (3), since $\{a\} = \{a,a\}$ by (1).

4.  Union:  If $\mathcal{C}$ is a set, then there is a set $\bigcup \mathcal{C}$, the __[[union]]__ of $\mathcal{C}$, whose elements are precisely the elements of the elements of $\mathcal{C}$.  It is normal to write $A \cup B$ for $\bigcup \{A,B\}$, etc.  Besides its own power, this gives ternary and higher versions of (3), with $\{a,b,c\} = \{a\} \cup \{b,c\}$, etc.

5.  Separation/Specification/Comprehension:  Given any predicate $\phi[x]$ in the language of set theory with the chosen free variable shown, if $U$ is a set, then there is a set $\{x \in U \;|\; \phi[x]\}$, the __[[subset]]__ of $U$ given by $\phi$, whose elements are precisely those elements $x$ of $U$ such that $\phi[x]$ holds.  There are many variations, from Bounded Separation to Full Comprehension, which we should probably describe at [[axiom of separation]].  This is an axiom scheme, but it can be made a single axiom in $\mathbf{NBG}$ (but not completely in $\mathbf{MK}$).

6.  Replacement/Collection:  Given a predicate $\psi[x,Y]$ with the chosen free variables shown, if $U$ is a set and if for every $x$ in $U$ there is a unique $Y$ such that $\psi[x,Y]$ holds, then there is set $\{\iota\,Y.\;\psi[x,Y] \;|\; x \in U\}$, the __[[image]]__ of $U$ under $\psi$, whose elements are precisely those sets $Y$ such that there is an element $x$ of $U$ such that $\psi[x,Y]$ holds; if $\Psi[x]$ is a defined term, then we write $\{\Psi[x] \;|\; x \in U\}$ for $\{\iota\,Y.\;Y = \Psi[x] \;|\; x \in U\}$.  Again there are many variations, from Weak Replacement to Strong Collection, which we should probably describe at [[axiom of replacement]].  This can be made into a single axiom in both $\mathbf{NBG}$ and $\mathbf{MK}$.  One could combine this with (5) to produce $\{\iota\,Y.\;\psi[x,Y] \;|\; x \in U \;|\; \phi[x]\}$, but nobody seems to do this.

7.  Power Sets:  If $U$ is a set, then there is a set $\mathcal{P}U$, the __[[power set]]__ of $U$, whose elements are precisely the [[subsets]] of $U$, that is the sets $A$ whose elements are all elements of $U$.  When using [[intuitionistic logic]], it is possible to accept only a weak version of this, such as [[subset collection|Subset Collection]] or (even weaker) [[function sets|Exponentiation]].

8.  Infinity:  There is a set $\omega$ of __[[ordinal number|finite ordinals]]__ as pure sets.  Normally one states that $\empty \in \omega$ and $a \cup \{a\} \in \omega$ whenever $a \in \omega$, although variations are possible.  Using any but the weakest version of (6), it is enough to state that there is a set satisfying Peano\'s axioms of [[natural numbers]], or even any Dedekind-[[infinite set]].  It seems to be common to incorporate (2) into (8).

9.  Choice:  If $\mathcal{C}$ is a set, each of whose elements has an element, then there is a set with exactly one element from each element of $\mathcal{C}$.  Note that this set is *not* unique, nor can we construct a canonical version which is, so we do not give it any name or notation.  This version is the simplest to state in the language of $\mathbf{ZFC}$; see [[axiom of choice]] for further discussion and weak versions.  It is possible to incorporate (9) into (5) or (6), but this seems to be rare.

10. Foundation/Regularity/Induction:  Given a formula $\phi$ with a chosen free variable $X$, if $\phi$ holds whenever $\phi[a/X]$ holds for every $a \in X$, then $\phi$ holds absolutely.  For variations, see [[axiom of foundation]].  This scheme can be made into a single axiom even in $\mathbf{ZFC}$ itself (although not in versions with intuitionistic logic, which can be made a single axiom only in a class theory).


## Variations

Zermelo\'s original version consists of axioms (1--5) and (7--9), in a somewhat imprecise form, which affects the interpretation of (5), of higher-order [[classical logic]].  The modern $\mathbf{ZF}$ consists of (1--8) and (10), using first-order classical logic, the strongest form (Strong Collection, although the standard Replacement is sufficient with classical logic) of (6), and the strongest form (Full Separation) of (5) possible using only sets and not classes.  $\mathbf{ZFC}$ adds (9) and is thus the strongest version without classes or additional axioms; the version originally formulated by Fraenkel and Skolem did not include (10), although the three founders all eventually accepted it.  It is common to take __Zermelo set theory__ ($\mathbf{Z}$) to be $\mathbf{ZF}$ without (6), although Zermelo never accepted the first-order formulation; note that the weakest form (Weak Replacement) of (6) follows from (7) and (5), so it holds even in $\mathbf{Z}$.


### Constructive versions

The most well-known foundations for [[constructive mathematics]] through material set theory are [[Peter Aczel]]\'s __constructive Zermelo--Frankel set theory__ ($\mathbf{CZF}$) and [[John Myhill]]\'s __intuitionistic Zermelo--Fraenkel set theory__ ($\mathbf{IZF}$).  $\mathbf{CZF}$ uses all axioms (1--10), usually weak forms, in intuitionistic logic; specifically, it uses Bounded Separation for (5), Strong Collection for (6), an intermediate (Subset Collection) form of (7), and a weak (Dependent Choice) form of (9).  $\mathbf{IZF}$ does not include (9) but uses Full Separation for (5); Myhill\'s original version uses only Replacement for (6), but Collection (equivalent to Strong Collection using Full Separation) is standard now.  Note that adding (9) at full strength to $\math{IZF}$ implies [[excluded middle]] and so makes $\mathbf{ZFC}$.

[[Mike Shulman]]\'s unfinished survey of material and structural set theories takes $\mathbf{CPZ}^{\circlearrowleft-}$ as the most basic form; it consists of (1--4) and the weakest versions (Bounded Separation and Weak Replacement) of (5&6) in intuitionistic logic.  Adding (10) gives $\mathbf{CPZ}^{-}$, adding (8) gives $\mathbf{CPZ}^{\circlearrowleft}$, and adding both gives $\mathbf{CPZ}$, __constructive pre-Zermelo set theory__.  Shulman gives systematic notation for other versions, which includes those above, except that his '$\mathbf{CZF}$' does not include any form of (9).

Myhill has another version, __constructive set theory__ ($\mathbf{CST}$); this consists of (1--4), Bounded Separation for (5), Replacement for (6), the weakest (Exponentiation) form of (7), (8), and Dependent Choice for (9).  It also uses a variation of the language, with urelements for natural numbers; note that the existence of $\omega$ still follows using (6).  This classifies $\mathbf{CST}$ as $\mathbf{C}\Pi\mathbf{ZF}^{\circlearrowleft} + DC$ in Shulman\'s system if one ignores the use of urelements and strengthens Replacement to Strong Collection.


### Class theories

__Morse--Kelley class theory__ ($\mathbf{MK}$) features both [[sets]] and [[proper classes]].  This allows it to strengthen (5) to Full Comprehension, since $\phi$ can include quantification over classes; the same holds in (6) and (10), although this does not add any additional strength.  __Von Neumann--Bernays--G&#246;del class theory__ ($\mathbf{NBG}$) uses the same language, but it still uses only Full Separation for (5).  This makes it conservative over $\mathbf{ZFC}$ and also allows for a finite axiomatisation; we replace the formulas in (5) and (6) with classes, and add some special cases of (5) for subclasses, one for each logical connective.

One can also rework all of the weak versions of set theory above into a class theory like $\mathbf{NBG}$, which is conservative over the original set theory.  One can also use a class theory like $\mathbf{MK}$, although this destroys any attempt to use a weak version of (5).


### Large cardinals

One often adds axioms for [[large cardinal]]s to $\mathbf{ZFC}$.  Even (8) can be seen as a large cardinal axiom, stating that $\aleph_0$ exists.  These additional axioms are most commonly studied in the context of a material set theory, but they work just as well in a structural set theory.  Note that adding an [[inaccessible cardinal]] to $\mathbf{ZFC}$ strenghtens it to $\mathbf{MK}$; reinterpret $\mathbf{MK}$\'s class of all sets as a strongly inaccessible cardinal.


### Relation to structural set theories


The structural set theory **[[ETCS]]** is equivalent to Shulman\'s $\Delta_0\mathbf{ZC}$ in that the [[category of sets]] in that theory satisfies $\mathbf{ETCS}$ while the well-founded [[pure sets]] in $\mathbf{ETCS}$ satisfy $\Delta_0\mathbf{ZC}$.  This uses (1--4), Bounded Separation for (5), and (7--10), with Weak Replacement following from (5) and (7).

Shulman\'s **[[SEAR|SEARC]]** is equivalent to $\mathbf{ZFC}$ in the same way.  $\mathbf{SEAR}$, which lacks the axiom of choice, is equivalent to $\mathbf{ZF}^{\circlearrowleft}$, which is $\mathbf{ZF}$ without (10), in a weaker sense.


[[!redirects ZF]]
[[!redirects Zermelo-Fraenkel set theory]]
[[!redirects Zermelo-Fraenkel set theory]]
[[!redirects Zermelo-Fraenkel set theory]]
[[!redirects Zermelo–Fraenkel set theory]]
[[!redirects Zermelo–Fraenkel set theory]]
[[!redirects Zermelo–Fraenkel set theory]]
[[!redirects Zermelo--Fraenkel set theory]]
[[!redirects Zermelo--Fraenkel set theory]]
[[!redirects Zermelo--Fraenkel set theory]]
[[!redirects Zermelo-Fraenkel]]
[[!redirects Zermelo-Fraenkel]]
[[!redirects Zermelo-Fraenkel]]
[[!redirects Zermelo–Fraenkel]]
[[!redirects Zermelo–Fraenkel]]
[[!redirects Zermelo–Fraenkel]]
[[!redirects Zermelo--Fraenkel]]
[[!redirects Zermelo--Fraenkel]]
[[!redirects Zermelo--Fraenkel]]
[[!redirects CPZ]]
[[!redirects CZF]]
[[!redirects IZF]]
[[!redirects CST]]
[[!redirects NBG]]