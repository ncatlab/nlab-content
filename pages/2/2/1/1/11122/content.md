
# Contents
* automatic table of contents goes here
{: toc}

## Idea

NBG or von Neumann--Bernays--G&#246;del set theory is a [[material set theory]]. It is conservative extension of the [[ZFC]] and its ontology includes [[proper classes]], like [[MK]]. But unlike [[ZFC]] and [[MK]], NBG can be finitely axiomatized.


## History

[[John von Neumann]] began $NBG$ in the 1920s, but his version was unwieldy.  [[Paul Bernays]] and [[Kurt Gödel]] simplified it later.  It also illustrates G&#246;del\'s theorem that any [[first-order theory]] has a [[conservative extension]] with a finite axiomatization.


## Axioms

NBG is a [[material set theory]], based on a global binary membership [[predicate]] $\in$. The objects of NBG are called [[classes]]. If a class $x$ is a member of another class $A$, i.e., $x \in A$, then $x$ is called [[set]]. A class which is not a set is called [[proper class]]. NBG can be presented as a two-sorted theory, with lowercase letters denoting sets and uppercase letters denoting classes.

1. [[axiom of extensionality|Extensionality]]: Two classes are equal if and only if the have the same members.

2. [[axiom of pairing|Pairing]], [[axiom of union|Union]], [[axiom of power sets|Power Sets]] and [[axiom of infinity|Infinity]]: regard sets and are identical to the [[ZFC]] counterparts.

3. [[axiom of foundation|Foundation]]: For each nonempty class $A$ there exists a set $x \in A$ such that $x \cap A = \varnothing$.

4. [[axiom of comprehension|Class Comprehension schema]]: For any formula $\phi$ containing no quantifiers over classes (it may contain quantifiers over sets and it may contain both class and set parameters), there is a class $A$ whose elements are precisely those sets $x$ satisfying $\phi(x)$.  In particular, taking $\phi(x)$ as $x = x$ it follows that there exists the class $V$ of all sets.

5. Limitation of Size: A class $A$ is a set if and only if there is no bijection between $A$ and the class $V$ of all sets.

From the axiom of Limitation of Size, it turn out that $V$ is not a set but a proper class, avoiding [[Russell's paradox]]. Moreover, since one can prove that the [[ordinal numbers|ordinal number]] form a proper class, there is a bijection beetween $V$ and $\mathrm{Ord}$, i.e., the class of all sets can be well-ordered which implies the [[axiom of global choice]].


## Finite axiomatization

Every instance of class comprehension can be built out of a few, based on the logical connnectives.  This is similar to the finite axiomatization of [[bounded separation|bounded]] $ZFC$ (or, in other language, [[ETCS]]); indeed, $NBG$ is essentially bounded [[MK]].


[[!redirects NBG]]
[[!redirects Neumann-Bernays-Gödel set theory]]
[[!redirects Neumann–Bernays–Gödel set theory]]
[[!redirects Neumann--Bernays--Gödel set theory]]
[[!redirects von Neumann-Bernays-Gödel set theory]]
[[!redirects von Neumann–Bernays–Gödel set theory]]
[[!redirects von Neumann--Bernays--Gödel set theory]]
