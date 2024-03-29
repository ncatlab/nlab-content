

# Subsets
* table of contents
{: toc}

## Idea

A subset of a given [[set]] $A$ is a set $B$ that may be viewed as contained within $A$.

## Definitions

### In material set theory

In [[material set theory]], a __subset__ of a [[set]] $A$ is a set $B$ with the *property* that
$$ x \in B \;\Rightarrow\; x \in A $$
for any object $x$ whatsoever.  One writes $B \subseteq A$ or $B \subset A$ (depending on the author) if $B$ has this property.  Set theory\'s [[axiom of extensionality]] says that $A = B$ if (and only if) $A \subseteq B$ and $B \subseteq A$ (although this is only strong enough for [[well-founded set | well-founded sets]]).

### In structural set theory

In [[structural set theory]], this definition doesn\'t make sense, because there is no global membership predicate $\in$ (and there may not be a global [[equality predicate]] either).  Accordingly, we define a __subset__ of $A$ to be a set $B$ with the *structure* of an [[injection]]
$$ i\colon B \hookrightarrow A .$$

We can still define a *local* membership predicate $\in_A$ as follows:  Given an element $x$ of $A$ and a subset $B$ (technically, $(B,i)$) of $A$,
\[\label{indef} x \in_A B \;\Leftrightarrow\; \exists(y\colon B),\; x = i(y) .\]
Similarly, we can define a local containment predicate $\subseteq_A$ as follows:  Given subsets $B$ and $C$ of $A$,
$$ B \subseteq_A C \;\Leftrightarrow\; \forall(x\colon A),\; x \in B \;\Rightarrow\; x \in C .$$
We can also define a local equality predicate $=_A$ on subsets of $A$:
$$ B =_A C \;\Leftrightarrow\; B \subseteq C \;\wedge\; C \subseteq B .$$

In foundations that already have a global equality predicate on sets (and functions between equal sets), this local equality predicate must be interpreted as an [[equivalence relation]]; then a __subset__ of $A$ is technically an [[equivalence class]] of injections to $A$ rather than simply an injection to $A$. 

In any case, if $A$ is a subset of $B$, then $B$ is a __superset__ of $A$.

### Internal subsets

One could define the subset relation as a [[set]] using the [[internal logic]] of a [[set theory]]. The inclusion [[relation]] between two sets $A$ and $B$ is defined as the [[support set|support]] of the [[injection set]] between $A$ and $B$:

$$A \subseteq B \coloneqq \left[\mathrm{Inj}(A, B)\right]$$

A **internal subset** of a [[set]] $B$ is a set $A$ with an element $p \in A \subseteq B$. A **internal superset** of a [[set]] $A$ is a set $B$ with an element $p \in A \subseteq B$. 

## Remarks

As you can see from the right-hand sides of the above sequence of definitions, one usually suppresses the subscript $A$ from the notation.  Even the right-hand side of (eq:indef) may use a local equality relation on elements of $A$.  It may be necessary to distinguish $x\colon E$ (the _[[type|typing declaration]]_ introducing a variable $x$ for an element of a given set $E$) from $x \in_A E$ (the _[[proposition]]_ that a given element $x$ of a given set $A$ is a member of a given subset $E$ of $A$).  Some authors may use $x \in A$ for either or both of these, trusting on context (particularly whether $x$ has been introduced before) to distinguish them.  Another notational convenience is to suppress the injection $i$, writing $y$ instead of $i(y)$.

The concept of subset as it appears here generalises to [[subobject]] in category theory.  To be precise, a subset of $A$ is exactly a subobject of $A$ when $A$ is thought of as an object of the category [[Set]].  The concept of superset then generalises to a notion of [[extension]] analogous to that of [[field extension]].

When the abstract set $A$ is fixed, a subset $B$ of $A$ may be thought of as a __[[concrete structure|concrete]] set__.

## Related concepts

* [[subtype]]

* [[cofinite subset]]

* [[saturated subset]]

* [[subspace]]

* [[causally closed subset]]

* [[space of finite subsets]]

[[!redirects subset]]
[[!redirects subsets]]

[[!redirects superset]]
[[!redirects supersets]]

[[!redirects internal subset]]
[[!redirects internal subsets]]

[[!redirects internal superset]]
[[!redirects internal supersets]]

[[!redirects concrete set]]
[[!redirects concrete sets]]
