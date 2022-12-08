
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

The __denial inequality relation__ is the [[negation]] of [[equality]].

This is a term found in [[constructive mathematics]], to distinguish from [[tight inequality relations]] such as [[tight apartness relations]]. In [[classical mathematics]], denial inequality relations and [[tight inequality relations]] are the same and are simply called "inequality", so the notion plays no further role classically. 

If one wishes to reserve the word "inequality" for [[order]] relations (such as $\le$ and $\lt$), then one may instead use the word **disequality** to refer to the denial inequality.  (For instance, this is common in [[type theory]] with [[subtype]] relations that form an ordering on the [[types]].)

## Properties

The denial inequality relation is an [[irreflexive symmetric relation]]. Irreflexivity follows from the negation of reflexivity of [[equality]], while symmetry follows from the [[contrapositive]] of symmetry of equality. In addition, the denial inequality relation is a [[stable relation]], because in [[constructive mathematics]], given any proposition $P$, $\neg \neg \neg P$ implies that $\neg P$. This means that $\neg \neg \neg (a = b)$ implies that $\neg (a = b)$, and since $\neg (a = b)$ if and only if $a \neq b$, this means that $\neg \neg (a \neq b)$ implies that $a \neq b$. 

### Denial apartness relation

The denial inequality relation on a set $S$ is said to be a **denial apartness relation** if for all elements $a \in S$, $b \in S$ and $c \in S$, $\neg((a \neq b) \wedge (b \neq c))$ implies that $\neg(a \neq b) \vee \neg(b \neq c)$. 

This implies that $\neq$ is an [[apartness relation]] because the contrapositive of the transitive property of equality states that $a \neq c$ implies that $\neg((a = b) \wedge (b = c))$, and the above condition implies that $\neg(a \neq b) \vee \neg(b \neq c)$, which is precisely the condition for a [[comparison]]. 

In particular, if [[de Morgan's law]] holds in the logic, then every denial inequality relation is a denial apartness relation. 

Similarly, every [[stable relation|stable]] [[tight apartness relation]] is a denial apartness relation. 

## See also

* [[stable relation]]

* [[inequality relation]]

* [[tight inequality relation]]

* [[stable equality]]

* [[Kock field]]

[[!redirects denial inequality]]
[[!redirects denial inequalities]]

[[!redirects denial inequality relation]]
[[!redirects denial inequality relations]]

[[!redirects denial apartness]]

[[!redirects denial apartness relation]]
[[!redirects denial apartness relations]]

[[!redirects disequality]]