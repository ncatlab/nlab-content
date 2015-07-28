
# Contents
* automatic table of contents goes here
{: toc}

## Idea

NBG or von Neumann--Bernays--G&#246;del set theory is a [[material set theory]]. It is a conservative extension of [[ZFC]] and its ontology includes [[proper classes]], like [[MK]]. But unlike [[ZFC]] and [[MK]], NBG can be finitely axiomatized.


## History

[[Georg Cantor]] was well acquainted with the phenomenon that some collections are 'too big' to be sets and in his late years made a distinction between _consistent_ and _inconsistent multitudes_, the former comprising sets, but his ideas were confined to private letters to (Jourdain and) Dedekind that were not published until 1932.

[[John von Neumann]] began $NBG$ in the 1920s ([von Neumann 1925](#vN1925), [von Neumann 1928](#vN1928)), but his version was unwieldy.  [[Paul Bernays]] and [[Kurt Gödel]] simplified it later.  It also illustrates G&#246;del\'s theorem that any [[first-order theory]] has a [[conservative extension]] with a finite axiomatization.


## Axioms

NBG is a [[material set theory]], based on a global binary membership [[predicate]] $\in$. The objects of NBG are called [[classes]]. If a class $x$ is a member of another class $A$, i.e., $x \in A$, then $x$ is called [[set]]. A class which is not a set is called [[proper class]]. NBG can be presented as a two-sorted theory, with lowercase letters denoting sets and uppercase letters denoting classes.

1. [[axiom of extensionality|Extensionality]]: Two classes are equal if and only if the have the same members.

2. [[axiom of pairing|Pairing]], [[axiom of union|Union]], [[axiom of power sets|Power Sets]] and [[axiom of infinity|Infinity]]: regard sets and are identical to the [[ZFC]] counterparts.

3. [[axiom of foundation|Foundation]]: For each nonempty class $A$ there exists a set $x \in A$ such that $x \cap A = \varnothing$.

4. [[axiom of comprehension|Class Comprehension schema]]: For any formula $\phi$ containing no quantifiers over classes (it may contain quantifiers over sets and it may contain both class and set parameters), there is a class $A$ whose elements are precisely those sets $x$ satisfying $\phi(x)$.  In particular, taking $\phi(x)$ as $x = x$ it follows that there exists the class $V$ of all sets.

5. Limitation of Size: A class $A$ is a set if and only if there is no bijection between $A$ and the class $V$ of all sets.

From the axiom of Limitation of Size, it turn out that $V$ is not a set but a proper class, avoiding [[Russell's paradox]]. Moreover, since one can prove that the [[ordinal number|ordinal numbers]] form a proper class, there is a bijection beetween $V$ and $\mathrm{Ord}$, i.e., the class of all sets can be well-ordered which implies the [[axiom of global choice]].


## Finite axiomatization

Every instance of class comprehension can be built out of a few, based on the logical connnectives.  This is similar to the finite axiomatization of [[bounded separation|bounded]] $ZFC$ (or, in other language, [[ETCS]]); indeed, $NBG$ is essentially bounded [[MK]].

## References

* [[John von Neumann]], "Eine Axiomatisierung der Mengenlehre", Journal f&#252;r die Reine und Angewandte Mathematik 154 (1925) 219&#8211;240, doi:[10.1515/crll.1925.154.219](http://dx.doi.org/10.1515/crll.1925.154.219), [GDZ](http://gdz.sub.uni-goettingen.de/index.php?id=resolveppn&PPN=GDZPPN002169606)
{#vN1925}

* [[John von Neumann]], "Die Axiomatisierung der Mengenlehre", Mathematische Zeitschrift 27 (1928) 669&#8211;752, doi:[10.1007/bf01171122](http://dx.doi.org/10.1007/bf01171122), [GDZ](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=PPN266833020_0027&DMDID=DMDLOG_0042)
{#vN1928}

* [[Gerhard Osius]], _Kategorielle Mengenlehre: Eine Charakterisierung der Kategorie der Klassen und Abbildungen_ , Math. Ann. **210** (1974) pp.171-196. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002309939))

[[!redirects NBG]]
[[!redirects Neumann-Bernays-Gödel set theory]]
[[!redirects Neumann–Bernays–Gödel set theory]]
[[!redirects Neumann--Bernays--Gödel set theory]]
[[!redirects von Neumann-Bernays-Gödel set theory]]
[[!redirects von Neumann–Bernays–Gödel set theory]]
[[!redirects von Neumann--Bernays--Gödel set theory]]
