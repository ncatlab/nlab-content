
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Idea
 {#Idea}

There are many systems of _[[formal logic]]_. By "classical logic" one broadly refers to those such systems which reflect the kind of logic as understood, quite literally, by the classics, say starting with [Aristotle, Metaphysics 1011b24](excluded+middle#AristotleMetaphysics). If you have never heard of any alternative system of logic, then classical logic is just the kind of logic that you have heard about.

There is some variance in what exactly counts as classical and as non-classical in [[logic]], but one main characteristic of classical logic is its use of the _[[principle of excluded middle]]_. Informally this says that every [[proposition]] is either [[true]] or [[false]]. (Slightly more carefully it says that for any proposition $P$, either it or its [[negation]] is true, where the 'or' is to be read in an 'internal' sense, i.e., as a formal [[disjunction]] $P \vee \neg P$.) 

It is the apparent self-evidence of this principle of excluded middle that made people take it for granted for a long period of human civilization, so that it became "classical". 

One consequence of the [[principle of excluded middle]] in classical logic is the possibility to obtain [[proof]] of a [[proposition]] by showing that its [[negation]] is [[false]] ([[proof by contradiction]]). Evident as this may superficially seem, it has the noteworthy consequence that one may for instance prove [[existential quantifier|existence]] of mathematical objects without having any way to actually construct an example.

This "non-constructive" nature of classical logic eventually led people to consider alternative and hence _non-classical_ systems of logic, such as [[constructive logic]]/[[intuitionistic logic]], where the [[principle of excluded middle]], and possibly other principle of classical logic, are not considered by default.  There is still a close relation between classical and [[constructive logic]]. For example a [[proposition]] is provable in classical logic precisely if its [[double negation]] is provable in [[constructive logic]] ("[[double negation translation]]").

Other considerations such as the [[internal logic]] of [[categories]] also led to constructive/intuitionistic logics.  More recently, other "nonclassical" logics such as [[linear logic]], [[paraconsistent logic]], [[relevance logic]], [[quantum logic]], and so on have also gained prominence.

There are other principles that are often associated with classical logic, which still seemed self-evident at a time, but maybe less so than the principle of excluded middle. One such is the [[set theory|set-theoretic]] _[[axiom of choice]]_ or one of its equivalent incarnations, such as [[Zorn's lemma]]. The presently most popular formal [[foundation of mathematics]] via the [[set theory]], called _[[ZFC]]_, includes both the [[principle of excluded middle]] as well as the [[axiom of choice]]. In this form classical logic serves as the foundation for _[[classical mathematics]]_. 


## Details

Classical logic is the form of [[logic]] usually accepted and taught as standard among working mathematicians, and traced back (at least) to Aristotle.  Some particular features that distinguish classical logic are (perhaps not a complete list):

* a [[distributive lattice]] of logical operations ($\wedge$ and $\vee$);
* the [[structural rule]]s of weakening, contraction, and (where meaningful) exchange;
* an involutory [[negation]].

In contrast, [[minimal logic|minimal]], [[intuitionistic logic|intuitionistic]], and (some forms of) [[paraconsistent logic|paraconsistent]] logics have the distributive lattice and the structural rules but no involutory negation.  On the other hand, [[linear logic]] (at least, "classical" linear logic) and (other forms of) paraconsistent logic have logical operations with at least some distributive properties and an involutory negation, but lack some structural rules.  Then again, [[quantum logic]] and (yet other forms of) paraconsistent logic have the structural rules and the involutory negation, but lack any sort of distributivity.

In [[category theory]] (and in the [[foundations]] of mathematics generally), it is intuitionistic logic that is most often contrasted to classical logic; the difference is given by the law of [[excluded middle]], which holds classically but not intuitionistically.

## Classical propositional logic 

Before describing what makes a [[propositional logic]] 'classical', let us quickly recall what propositional logic is in the first place. 

In general, a (deductive) [[logic]] specifies rules of [[syntax]] for forming well-formed [[formulas]] which can be considered as assertions, and rules of inference for deriving one formula (called a 'conclusion') from other formulas (called 'premises'), in such a way that truth of the conclusion follows on the assumption of truth of the premises. In short, a [[formal logic]] specifies a mode of reasoning that is considered valid for a particular mathematical context. 

In [[propositional logic]], one forms a formula by applying basic logical operations such as $\wedge$ ('[[logical conjunction|and]]'), $\vee$ ('[[logical disjunction|or]]'), and $\Rightarrow$ ('[[implication|implies]]')  to simpler formulas. The simplest formulas are called atomic formulas, and usually take the form of an [[equation]] $s = t$ between two [[terms]] (and underneath there are rules for term formation as well), or something like $R(a_1, \ldots, a_n)$ where $R$ stands for some basic relation (between terms $a_1, \ldots, a_n$) belonging to whatever language one is working with. A standard list of *propositional* operations would be 

* $\wedge, \vee, \Rightarrow$ (binary operations), $\neg$ ('not', an unary operator), and $\top, \bot$ ('true' and 'false', basic logical constants or nullary operators). 

Missing from propositional logic *per se* are [[quantifiers]] such as $\exists$ ([[existential quantifier]]) and $\forall$ ([[universal quantifier]]), which properly speaking belong to [[predicate logic]]. (One way of thinking about propositional logic is that it treats formulas as assertions "all of the same type", whereas quantifiers allow one to shift between classes of assertions of one type to assertions of another type.) 

As we said, there are also rules of inference. There are various styles in which these are presented, such as [[natural deduction]] or [[sequent calculus]]. But a simple example might look like this: 

$$\frac{P \wedge Q}{P}$$ 

("from $P \wedge Q$ we may infer $P$"). This might also be written $P \wedge Q \vdash P$ ("pronounced $P \wedge Q$ entails $P$"), thought of as asserting a relation between propositions called entailment. Two of the universal rules of propositional logic (whether classical or intuitionistic or quantum or whatever) is that the entailment relation should be [[reflexive relation|reflexive]] and [[transitive relation|transitive]]: the rules of inference allow an entailment $P \vdash P$ for any formula $P$, and if they allow entailments $A \vdash B$ and $B \vdash C$, then they allow $A \vdash C$. 

Thus, in a propositional logic, formulas together with the entailment relation that is provided for by the rules of inference form a [[preorder]]. Sometimes one goes a little further: in situations where one can derive $A \vdash B$ and $B \vdash A$, one says that $A$ and $B$ are provably equivalent (often abbreviated as $A \equiv B$), and one may pass to the [[poset]] of provable equivalence classes (the usual way in which a poset is associated with a preorder). 

One knows that one is in the realm of *classical* propositional logic if the poset of provable equivalence classes is a [[Boolean algebra]], in which $\wedge$ induces the meet operation and $\vee$ the join operation. Here the rules of inference allow bi-entailments such as 

$$A \Rightarrow B \equiv \neg A \vee B$$ 

and in fact the different types of propositional logic are usually conveniently described by specifying what type of algebraic structure we get on the poset of provable equivalence classes. For example, in [[intuitionistic logic]] this poset forms a [[Heyting algebra]]. 

## Related concepts

* [[logic]]
* [[classical mathematics]]
* [[constructive logic]] / [[intuitionistic logic]]
* [[material set theory]]

[[!redirects classical logics]]
