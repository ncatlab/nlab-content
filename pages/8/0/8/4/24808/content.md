+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--

\tableofcontents

## Idea

Russell universes or universes à la Russell are types whose terms are types. In [[type theories]] without a separate type [[judgment]] $A \; \mathrm{type}$, only typing judgments $a:A$, what would have been type judgments are represented by typing judgments that $A$ is a term of a Russell universe $U$, $A:U$. Russell universes without a separate type judgment are used in many places in type theory, including in the [[HoTT book]], in [[Coq]], and in [[Agda]]. 

## Formal definition

### Without a separate type judgment

Russell universes are formally defined in a three-layer type theory. The first and second layers consists of an untyped [[predicate logic]] consisting of proposition judgments and index judgments, the [[natural deduction]] rules for [[predicate logic]], and inference rules to define a [[linear order]] without an [[upper bound]], or more commonly, the inference rules for [[first-order theory|first-order]] [[Peano arithmetic]]. The third layer only contains term judgments, and is the dependent type theory where the Russell universes live in. 

We begin with the formal rules of the first and second layers. The first and second layer consists of three judgments: proposition judgments $A \; \mathrm{prop}$, where we judge $A$ to be a proposition, true proposition judgments $A \; \mathrm{true}$, where we judge $A$ to be a true proposition, index judgments, where we judge $a$ to be a universe index, $a \; \mathrm{index}$, and metacontext judgments, where we judge $\Xi$ to be a metacontext, $\Xi \; \mathrm{metactx}$. Metacontexts are lists of index judgments $a \; \mathrm{index}$, $b \; \mathrm{index}$, $c \; \mathrm{index}$, et cetera, and true proposition judgments $A \; \mathrm{true}$, $B \; \mathrm{true}$, $C \; \mathrm{true}$, et cetera, and are formalized by the rules for the empty metacontext and extending the metacontext by an index judgment or true proposition judgment:

$$\frac{}{() \; \mathrm{metactx}} \qquad \frac{\Xi \; \mathrm{metactx} \quad \Xi \vdash A \; \mathrm{prop}}{(\Xi, A \; \mathrm{true}) \; \mathrm{metactx}} \qquad \frac{\Xi \; \mathrm{metactx}}{(\Xi, i \; \mathrm{index}) \; \mathrm{metactx}}$$

Next, we have the inference rules for [[predicate logic]]:

* Rules for implication:
$$\frac{\Xi \vdash P \; \mathrm{prop} \quad \Xi \vdash Q \; \mathrm{prop}}{\Xi \vdash P \to Q \; \mathrm{prop}} \qquad \frac{\Xi \vdash P \; \mathrm{prop} \quad \Xi, P \; \mathrm{true} \vdash Q \; \mathrm{true}}{\Xi \vdash P \to Q \; \mathrm{true}} \qquad \frac{\Xi \vdash P \to Q \; \mathrm{true}}{\Xi, P \; \mathrm{true} \vdash Q \; \mathrm{true}}$$

* Rules for universal quantifiers:
$$\frac{\Xi, x \; \mathrm{index} \vdash P(x) \; \mathrm{prop}}{\Xi \vdash \forall x.P(x) \; \mathrm{prop}} \qquad \frac{\Xi, x \; \mathrm{index} \vdash P(x) \; \mathrm{true}}{\Xi \vdash \forall x.P(x) \; \mathrm{true}} \qquad \frac{\Xi \vdash \forall x.P(x) \; \mathrm{true}}{\Xi, x \vdash P(x) \; \mathrm{true}}$$

* Rules for conjunction:
$$\frac{\Xi \vdash P \; \mathrm{prop} \quad \Xi \vdash Q \; \mathrm{prop}}{\Xi \vdash P \vee Q \; \mathrm{prop}} \quad \frac{\Xi \vdash P \; \mathrm{true} \quad \Xi \vdash Q \; \mathrm{true}}{\Xi \vdash P \vee Q \; \mathrm{true}}$$

$$\frac{\Xi \vdash P \; \mathrm{prop} \quad \Xi \vdash Q \; \mathrm{prop} \quad \Xi, P \wedge Q \; \mathrm{true}}{\Xi \vdash P \; \mathrm{true}} \qquad \frac{\Xi \vdash P \; \mathrm{prop} \quad \Xi \vdash Q \; \mathrm{prop} \quad \Xi, P \wedge Q \; \mathrm{true}}{\Xi \vdash Q \; \mathrm{true}}$$ 

* Rules for existential quantifiers:
$$\frac{\Xi, x \; \mathrm{index} \vdash P(x) \; \mathrm{prop}}{\Xi \vdash \exists x.P(x) \; \mathrm{prop}}$$ 

$$\frac{\Xi, x \; \mathrm{index} \vdash P(x) \; \mathrm{prop} \quad \Xi \vdash x \; \mathrm{index} \quad \Xi \vdash P(x) \; \mathrm{true}}{\Xi \vdash \exists x.P(x) \; \mathrm{true}}$$ 

$$\frac{\Xi, x \; \mathrm{index} \vdash P(x) \; \mathrm{prop} \quad \Xi, \exists x.P(x) \; \mathrm{true} \vdash Q \; \mathrm{prop} \quad \Xi, x \; \mathrm{index}, P(x) \; \mathrm{true} \vdash Q \; \mathrm{true}}{\Xi, \exists x.P(x) \; \mathrm{true} \vdash Q \; \mathrm{true}}$$

* Rules for disjunction:
$$\frac{\Xi \vdash P \; \mathrm{prop} \quad \Xi \vdash Q \; \mathrm{prop}}{\Xi \vdash P \vee Q \; \mathrm{prop}} \qquad \frac{\Xi \vdash P \; \mathrm{prop} \quad \Xi \vdash Q \; \mathrm{prop}}{\Xi, P \; \mathrm{true} \vdash P \vee Q \; \mathrm{true}} \qquad \frac{\Xi \vdash P \; \mathrm{prop} \quad \Xi \vdash Q \; \mathrm{prop}}{\Xi, Q \; \mathrm{true} \vdash P \vee Q \; \mathrm{true}}$$ 

$$\frac{\Xi \vdash P \; \mathrm{prop} \quad \Xi \vdash Q \; \mathrm{prop} \quad \Xi, P \vee Q \; \mathrm{true} \vdash R \; \mathrm{prop} \quad \Xi, P \; \mathrm{true} \vdash R \; \mathrm{true} \quad \Xi, Q \; \mathrm{true} \vdash R \; \mathrm{true}}{\Xi, P \vee Q \; \mathrm{true} \vdash R \; \mathrm{true}}$$ 

* Rules for true:
$$\frac{\Xi \; \mathrm{metactx}}{\Xi \vdash \top \; \mathrm{prop}} \qquad \frac{\Xi \; \mathrm{metactx}}{\Xi \vdash \top \; \mathrm{true}}$$ 

* Rules for false:
$$\frac{\Xi \; \mathrm{metactx}}{\Xi \vdash \bot \; \mathrm{prop}} \qquad \frac{\Xi \vdash P \; \mathrm{prop}}{\Xi, \bot \; \mathrm{true} \vdash P \; \mathrm{true}}$$ 

Next, we have the [[inference rules]] for [[propositional equality]]:

$$\frac{\Xi \; \mathrm{metactx}}{\Gamma, x \; \mathrm{index}, y \; \mathrm{index} \vdash x = y \; \mathrm{prop}} \quad \frac{\Xi \; \mathrm{metactx}}{\Gamma, x \; \mathrm{index} \vdash x = x \; \mathrm{true}}$$

$$\frac{\Xi, x \; \mathrm{index}, y \; \mathrm{index}, x = y \; \mathrm{true} \vdash P(x, y) \; \mathrm{prop}}{\Gamma \vdash \left(\forall x.P(x, x)\right) \implies \left(\forall x.\forall y.x = y \implies P(x, y)\right) \; \mathrm{true}}$$

Finally, we have the [[inference rules]] for a [[linear order]] which has no [[upper bound]]:

$$\frac{\Xi \vdash x \; \mathrm{index} \quad \Xi \vdash y \; \mathrm{index}}{\Gamma \vdash x \lt y \; \mathrm{prop}} \quad \frac{\Xi \; \mathrm{metactx}}{\Gamma \vdash \forall x.(x \lt x) \implies \bot \; \mathrm{true}}$$

$$\frac{\Xi \; \mathrm{metactx}}{\Gamma \vdash \forall x.\forall y.x \lt y \implies ((y \lt x) \implies \bot) \; \mathrm{true}}$$

$$\frac{\Xi \; \mathrm{metactx}}{\Gamma \vdash \forall x.\forall y.\forall z.(x \lt z) \implies ((x \lt y) \vee (y \lt z)) \; \mathrm{true}}$$

$$\frac{\Xi \; \mathrm{metactx}}{\Gamma \vdash \forall x.\forall y.((x \lt y) \implies \bot) \wedge ((y \lt x) \implies \bot) \implies (x = y) \; \mathrm{true}}$$

$$\frac{\Xi \vdash x \mathrm{index}}{\Gamma \vdash s(x) \; \mathrm{index}} \qquad \frac{\Xi \vdash x \mathrm{index}}{\Gamma \vdash x \lt s(x) \; \mathrm{true}}$$

Most commonly, the linear order is that of the [[natural numbers]], in which one replaces the axioms of a linear order without upper bound with the [[axioms]] and [[signature (in logic)|signatures]] for [[first-order theory|first-order]] [[Peano arithmetic]]. 

Now, we introduce the third layer, which consists of a type theory with only one judgment, the typing judgment $a:A$, which says that $a$ is a term of the type $A$. Instead of type judgments, we introduce a special kind of type called a **Russell universe** or **universe à la Russell**, whose terms are the types themselves. Russell universes are formalized with the following rules:

$$\frac{\Xi \vdash i \; \mathrm{index} \quad \Xi \vdash j \; \mathrm{index} \quad \Xi \vdash i \lt j \; \mathrm{true}}{\Xi \vdash U_i:U_j} \quad \frac{\Xi \vdash i \; \mathrm{index} \quad \Xi \vdash j \; \mathrm{index} \quad \Xi \vdash i \lt j \; \mathrm{true} \quad \Xi \vdash A:U_i}{\Xi \vdash \mathrm{Lift}_{i, j}(A):U_j}$$

Contexts are defined as a metacontext with a list of typing judgments, with the metacontext always preceding the list of typing judgments:

$$\frac{\Xi \; \mathrm{metactx}}{\Xi \vert () \; \mathrm{ctx}} \qquad \frac{\Xi \vert \Gamma \vdash A:U_i}{\Xi \vert (\Gamma, a:A) \; \mathrm{ctx}}$$

The general rules for Russell universes then follows:

$$\frac{\Xi \vert \Gamma \vdash i \; \mathrm{index} \quad \Xi \vert \Gamma \vdash j \; \mathrm{index} \quad \Xi \vert \Gamma \vdash i \lt j \; \mathrm{true}}{\Xi \vert \Gamma \vdash U_i:U_j} \quad \frac{\Xi \vert \Gamma \vdash i \; \mathrm{index} \quad \Xi \vert \Gamma \vdash j \; \mathrm{index} \quad \Xi \vert \Gamma \vdash i \lt j \; \mathrm{true} \quad \Xi \vert \Gamma \vdash A:U_i}{\Xi \vert \Gamma \vdash \mathrm{Lift}_{i, j}(A):U_j}$$

### With a separate type judgment

If the type theory has a separate type judgment $A \; \mathrm{type}$, the rules for Russell universes become simpler, as one doesn't have to assume infinitely many Russell universes and a second level to house the natural numbers type used to index the universes. Instead, we merely have

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash U \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:U}{\Gamma \vdash A \; \mathrm{type}}$$

Furthermore, the separate type judgment amounts to collapsing the two levels in the theory above into one level: Instead of defining the identity type and the type of natural numbers as external to the type theory, we instead define it as normal types internal to the type theory. Then the rules for the infinite tower of Russell universes are as follows:

$$\frac{\Gamma \vdash i:\mathbb{N}}{\Gamma \vdash U(i):U(s(i))} \qquad \frac{\Gamma \vdash i:\mathbb{N} \quad \Gamma \vdash A:U(i)}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \vdash i:\mathbb{N} \quad \Gamma \vdash A:U(i)}{\Gamma \vdash \mathrm{Lift}(i)(A):U(s(i))}$$

We could also add rules which state that every type is an element of a Russell universe:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{level}_A:\mathbb{N}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A:U(\mathrm{level}_A)}$$

Then the first rule for the infinite tower becomes one of

$$\frac{\Gamma \vdash i:\mathbb{N}}{\Gamma \vdash \mathrm{level}_{U(i)} \equiv s(i):\mathbb{N}}\mathrm{strict} \quad \frac{\Gamma \vdash i:\mathbb{N}}{\Gamma \vdash \mathrm{defLevelU}(i):\mathrm{level}_{U(i)} =_\mathbb{N} s(i)}\mathrm{weak}$$

This is how one would formally present a dependent type theory like the one in [[Book HoTT]] or the ones in [[Agda]], [[Coq]], [[Lean]], without resorting to external layers. 

However, these set of rules are incompatible with the statement that all [[dependent sum types]] exist, because the dependent sum type $\sum_{n:\mathbb{N}} U(n)$ contains as elements pairs of every type in the type theory and the universe level the type is in. However, by the inference rules above, $\sum_{n:\mathbb{N}} U(n)$ is in the universe $U(\mathrm{level}_{\sum_{n:\mathbb{N}} U(n)})$ which means that by right projecting $\sum_{n:\mathbb{N}} U(n)$, every type is in the universe $U(\mathrm{level}_{\sum_{n:\mathbb{N}} U(n)})$ resulting in [[Girard's paradox]] which is contradictory. 

Instead, usually the inference rules for [[dependent sum types]] require that the type family $x:A \vdash B(x)$ in the dependent sum type have the same universe level $n:\mathbb{N}$, $x:A \vdash B(x):U(n)$. Since none of the universes in the above diagram have the same universe level, the dependent sum type $\sum_{n:\mathbb{N}} U(n)$ cannot be constructed. The same is true of the formers of any type which could construct dependent sum types, such as [[wide pushouts]]. 

Similarly, these set of rules are incompatible with the statement that all [[sequential colimits]] exist, because one could then find the sequential colimit of the diagram 

$$U(0) \overset{\mathrm{Lift}(0)}\to U(s(0)) \overset{\mathrm{Lift}(s(0))}\to U(s(s(0))) \overset{\mathrm{Lift}(s(s(0)))}\to \ldots$$

and one would get a type $U_\infty$, which by definition of sequential colimits contains every type in the universe hierarchy. However, $U_\infty$ is in the universe $U(\mathrm{level}_{U_\infty})$, which means that lifting $U_\infty$ from $U(\mathrm{level}_{U_\infty})$ to $U_\infty$ via the sequential colimit results in [[Girard's paradox]] which is contradictory. 

Instead, usually the inference rules for sequential colimits require that the types in the above diagram have the same universe level $n:\mathbb{N}$. Since none of the universes in the above diagram have the same universe level, the sequential colimit $U_\infty$ cannot be constructed. The same is true of the formers of any type which could construct sequential colimits, such as [[pushout types]]. 

But none of this are problems in [[Book HoTT]] as the formers for every type have the same universe level as the type to be put in the universe. 

## See also

* [[Tarski universe]]

* [[two-level type theory]]

## References

The notion is due to:

* [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]): p. 48 in: _Intuitionistic type theory_, Lecture notes Padua 1984, Bibliopolis, Napoli (1984) &lbrack;[pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]]&rbrack;

For more see the references at *[[type universe]]*.

[[!redirects Russell universe]]
[[!redirects Russell universes]]

