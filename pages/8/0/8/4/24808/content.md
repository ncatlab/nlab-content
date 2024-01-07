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

One formal definition of a type theory with Russell universes is as follows:

The type theory has [[judgments]] 

* $\Gamma \; \mathrm{ctx}$, that $\Gamma$ is a [[context]]

* $i \; \mathrm{index}$, that $i$ is a universe index, 

* $\phi \; \mathrm{prop}$, that $\phi$ is a [[proposition]], 

* $\phi \; \mathrm{true}$, that $\phi$ is a [[true]] proposition, 

and consists of the formal [[signature (in logic)|signature]] and [[inference rules]] of [[first-order theory|first-order]] [[Heyting arithmetic]] or [[Peano arithmetic]]. These rules ensure that there are an [[infinite]] number of indices, which are strictly ordered with [[strict total order]] $\lt$ and upwardly unbounded, where $i \lt s(i)$ is true for all indices $i$. 

Now, we introduce the typing judgment $a:A$, which says that $a$ is a term of the type $A$. Instead of type judgments, we introduce a special kind of type called a **Russell universe** or **universe à la Russell**, whose terms are the types themselves. Russell universes are formalized with the following rules:

$$\frac{\Gamma \vdash i \; \mathrm{index}}{\Gamma \vdash U_i:U_{s(i)}} \qquad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A:U_i}{\Gamma \vdash A:U_{s(i)}}\mathrm{cumul} \qquad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A:U_i}{\Gamma \vdash \mathrm{Lift}_{i, j}(A):U_{s(i)}}\mathrm{lifting}$$

In addition, we have rules for contexts which state that one could add typing judgments to the list of contexts:

$$\frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A:U_i}{(\Gamma, a:A) \; \mathrm{ctx}}$$

### With a type judgment for each universe

One could also define Russell universes [[à la Coquand]], in that the type theory has a type judgment for each universe $U$. Using the dependent type theory with no separate type judgment, instead of having only one term judgment $a:A$, for index $i$ and type $A:U_i$, we instead have an infinite number of [[type]] [[judgments]], one type judgment $A \; \mathrm{type}_i$ for every index $i$, indicating that $A$ is a type with level $i$, in addition to the [[term]] judgments $a:A$. Then, one has the following rules for Russell universes à la Coquand: 

$$\frac{\Gamma \vdash i \; \mathrm{index}}{\Gamma \vdash U_i \; \mathrm{type}_{s(i)}} \qquad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash A \; \mathrm{type}_{s(i)}}\mathrm{cumul} \qquad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \mathrm{Lift}(A) \; \mathrm{type}_{s(i)}}\mathrm{lifting}$$

$$\frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash A:U_i} \qquad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A:U_i}{\Gamma \vdash A \; \mathrm{type}_i}$$

In addition, we have rules for contexts which state that one could add typing judgments to the list of contexts:

$$\frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{type}_i}{(\Gamma, a:A) \; \mathrm{ctx}}$$

One could derive from these rules the above rules for Russell universes and context extension

$$\frac{\Gamma \vdash i \; \mathrm{index}}{\Gamma \vdash U_i:U_{s(i)}} \qquad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A:U_i}{\Gamma \vdash A:U_{s(i)}}\mathrm{cumul} \qquad \frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A:U_i}{\Gamma \vdash \mathrm{Lift}(A):U_{s(i)}}\mathrm{lifting}$$

$$\frac{\Gamma \vdash i \; \mathrm{index} \quad \Gamma \vdash A:U_i}{(\Gamma, a:A) \; \mathrm{ctx}}$$

### With a single separate type judgment

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

## Analogues in set theory

There are analogues of cumulative Russell universes [[à la Coquand]] in [[set theory]]. Instead of having a single set theory, one has a whole collection of set theories which embed into each other, with indices indicating which level the set theory lies on. 

### With a separate set judgment for each set theory

One formal definition of a set theory with cumulative Russell universes [[à la Coquand]] is as follows:

The set theory has [[judgments]] 

* $\Gamma \; \mathrm{ctx}$, that $\Gamma$ is a [[context]]

* $\kappa \; \mathrm{index}$, that $\kappa$ is a level of set theory, 

* $\phi \; \mathrm{prop}$, that $\phi$ is a [[proposition]], 

* $\phi \; \mathrm{true}$, that $\phi$ is a [[true]] proposition, 

and consists of the formal [[signature (in logic)|signature]] and [[inference rules]] of [[first-order theory|first-order]] [[Heyting arithmetic]] or [[Peano arithmetic]]. These rules ensure that there are an [[infinite]] number of indices, which are strictly ordered with [[strict total order]] $\lt$ and upwardly unbounded, where $\kappa \lt \kappa^+$ is true for all indices $\kappa$. 

This allows us to add an infinite number of [[set]] [[judgments]], one set judgment $A \; \mathrm{set}_\kappa$ for every index $\kappa$, indicating that $A$ is a set with level $\kappa$, as well as an infinite number of [[membership relations]] $x \in_\kappa A$, one for each set judgment $\mathrm{set}_\kappa$. Then, one has the following [[inference rules]] for cumulative Russell universes [[à la Coquand]]: 

$$\frac{\Gamma \vdash \kappa \; \mathrm{index}}{\Gamma \vdash V_\kappa \; \mathrm{set}_{\kappa^+}} \quad \frac{\Gamma \vdash \kappa \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{set}_\kappa}{\Gamma \vdash A \; \mathrm{set}_{\kappa^+}}$$

$$\frac{\Gamma \vdash \kappa \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{set}_\kappa}{\Gamma \vdash A \in_{\kappa^+} V_\kappa \; \mathrm{true}} \qquad \frac{\Gamma \vdash \kappa \; \mathrm{index} \quad \Gamma \vdash A \; \mathrm{set}_{\kappa^+} \quad \Gamma \vdash A \in_{\kappa^+} V_\kappa \; \mathrm{true}}{\Gamma \vdash A \; \mathrm{set}_\kappa}$$

This says that each $V_\kappa$ is a [[set]] which satisfies a [[reflection principle]]. 

## See also

* [[Tarski universe]]

* [[Coquand universe]]

* [[two-level type theory]]

* [[reflection principle]]

## References

The notion is due to:

* [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]): p. 48 in: _Intuitionistic type theory_, Lecture notes Padua 1984, Bibliopolis, Napoli (1984) &lbrack;[pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]]&rbrack;

For more see the references at *[[type universe]]*.

[[!redirects Russell universe]]
[[!redirects Russell universes]]

[[!redirects à la Russell]]

[[!redirects universe à la Russell]]
[[!redirects universes à la Russell]]

