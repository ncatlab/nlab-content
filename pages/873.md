In traditional [[set theory]], a subset of a [[set]] $A$ is a set $B$ with the *property* that
$$x \in B \;\Rightarrow\; x \in A$$
for any object $x$ whatsoever.  One writes $B \subseteq A$ or $B \subset A$ (depending on the author) if $B$ has this property.  Set theory\'s _axiom of extensionality_ says that $A = B$ if (and only if) $A \subseteq B$ and $B \subseteq A$.

In other [[foundations]] of mathematics, this definition doesn\'t make sense, because there is no global membership predicate $\in$ (and there may not be a global equality predicate either).  Accordingly, we define a __subset__ of $A$ to be a set $B$ with the *structure* of an [[injection]]
$$i: B \hookrightarrow A.$$

We can still define a *local* membership predicate $\in_A$ as follows:  Given an element $x$ of $A$ and a subset $B$ (technically, $(B,i)$) of $A$,
\[\label{indef}
x \in_A B \;\Leftrightarrow\; \exists(y: B),\; x = i(y).\]
Similarly, we can define a local containment predicate $\subseteq_A$ as follows:  Given subsets $B$ and $C$ of $A$,
$$B \subseteq_A C \;\Leftrightarrow\; \forall(x: A),\; x \in B \;\Rightarrow\; x \in C.$$
We can also define a local equality predicate $=_A$ on subsets of $A$:
$$B =_A C \;\Leftrightarrow\; B \subseteq C \;\wedge\; C \subseteq B.$$
In foundations that already have a global equality predicate on sets (and functions between equal sets), this local equality predicate must be interpreted as an [[equivalence relation]]; then a __subset__ of $A$ is technically an equivalence class of injections to $A$ rather than simply an injection to $A$.

As you can see from the right-hand sides of the above sequence of definitions, one usually suppresses the subscript $A$ from the notation.  Even the right-hand side of (eq:indef) may use a local equality relation $=_A$ on elements of $A$ (which is not the same as the local equality relation on subsets of $A$, of course).  It may be necessary to distinguish $x: E$ (introducing a variable $x$ for an element of a given set $E$) from $x \in_A E$ (the proposition that a given element $x$ of a given set $A$ is a member of a given subset $E$ of $A$).  Some authors may use $x \in A$ for either or both of these, trusting on context (particularly whether $x$ has been introduced before) to distinguish them.  Another notational convenience is to suppress the injection $i$, writing $y$ instead of $i(y)$.

The concept of subset as it appears here generalises to [[subobject]] in category theory.  To be precise, a subset of $A$ is exactly a subobject of $A$ as an object of the category [[Set]].