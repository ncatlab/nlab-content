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

## Definition of a single Russell universe

If the type theory has a separate type judgment $A \; \mathrm{type}$, then one could define a single Russell universe in the type theory. We merely have

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash U \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:U}{\Gamma \vdash A \; \mathrm{type}}$$

## Formal definition of a hierarchy of Russell universes

Dependent type theories typically come with a hierarchy of Russell universes, so that all types in the dependent type theory are elements of Russell universes. This is especially the case for dependent type theories without any separate type judgments at all, where types are necessarily defined as terms of Russell universes. 

### Without a separate type judgment

One formal definition of a type theory with a hierarchy of Russell universes is as follows:

The type theory has [[judgments]] 

* $\Gamma \; \mathrm{ctx}$, that $\Gamma$ is a [[context]]

* $i \; \mathrm{level}$, that $i$ is a universe level, 

* $\phi \; \mathrm{prop}$, that $\phi$ is a [[proposition]], 

* $\phi \; \mathrm{true}$, that $\phi$ is a [[true]] proposition, 

and consists of the formal [[signature (in logic)|signature]] and [[inference rules]] of [[first-order theory|first-order]] [[Heyting arithmetic]] or [[Peano arithmetic]]. These rules ensure that there are an [[infinite]] number of indices, which are strictly ordered with [[strict total order]] $\lt$ and upwardly unbounded, where $i \lt s(i)$ is true for all indices $i$. 

Now, we introduce the typing judgment $a:A$, which says that $a$ is a term of the type $A$. Instead of type judgments, we introduce a special kind of type called a **Russell universe** or **universe à la Russell**, whose terms are the types themselves. Russell universes are formalized with the following rules:

$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash U_i:U_{s(i)}} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i}{\Gamma \vdash A:U_{s(i)}}\mathrm{cumul} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i}{\Gamma \vdash \mathrm{Lift}_{i, j}(A):U_{s(i)}}\mathrm{lifting}$$

In addition, we have rules for contexts which state that one could add typing judgments to the list of contexts:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i}{(\Gamma, a:A) \; \mathrm{ctx}}$$

as well as rules saying that equality is preserved across universe levels:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash j \; \mathrm{level} \quad \Gamma \vdash i = j \; \mathrm{true}}{\Gamma \vdash U_i \equiv U_j:U_{s(i)}}\mathrm{judgmental} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash j \; \mathrm{level} \quad \Gamma \vdash i = j \; \mathrm{true}}{\Gamma \vdash \mathrm{ap}_U^{i = j}:U_i =_{U_{s(i)}} U_j}\mathrm{typal}$$

### With a type judgment for each universe

One could also define a hierarchy of Russell universes [[à la Coquand]], in that the type theory has a type judgment for each universe $U$. Using the dependent type theory with no separate type judgment, instead of having only one term judgment $a:A$, for level $i$ and type $A:U_i$, we instead have an infinite number of [[type]] [[judgments]], one type judgment $A \; \mathrm{type}_i$ for every level $i$, indicating that $A$ is a type with level $i$, in addition to the [[term]] judgments $a:A$. Then, one has the following rules for Russell universes à la Coquand: 

$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash U_i \; \mathrm{type}_{s(i)}} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash A \; \mathrm{type}_{s(i)}}\mathrm{cumul} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \mathrm{Lift}(A) \; \mathrm{type}_{s(i)}}\mathrm{lifting}$$

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash A:U_i} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i}{\Gamma \vdash A \; \mathrm{type}_i}$$

In addition, we have rules for contexts which state that one could add typing judgments to the list of contexts:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i}{(\Gamma, a:A) \; \mathrm{ctx}}$$

One could derive from these rules the above rules for Russell universes and context extension

$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash U_i:U_{s(i)}} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i}{\Gamma \vdash A:U_{s(i)}}\mathrm{cumul} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i}{\Gamma \vdash \mathrm{Lift}(A):U_{s(i)}}\mathrm{lifting}$$

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i}{(\Gamma, a:A) \; \mathrm{ctx}}$$

### With a single separate type judgment

It is also possible to define the hierarchy of Russell universes with a single separate type judgment, such that every single type is in a Russell universe. The advantage of doing so is that one doesn't need to define the theory of universe levels before defining the type theory; one could instead simply define the natural numbers inside of the type theory itself, along with the hierarchy of Russell universes:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{Level}(A):\mathbb{N}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash U(n) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash A:U(\mathrm{Level}(A))}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma \vdash A \; \mathrm{type}} \quad \frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma \vdash \mathrm{Level}(A) \equiv n:\mathbb{N}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Level}(\mathbb{N}) \equiv 0:\mathbb{N}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash s(n):\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{Level}(U(n)) \equiv s(n):\mathbb{N}}$$

In particular, every type $A$ has a universe level, which is a natural number, and the universe level of $\mathbb{N}$ is zero and the universe level of $U(n)$ given natural number $n$ is the successor $s(n)$. 

Furthermore, every type $A$ of level $n$ lifts to another type $\mathrm{Lift}(A)$ of level $s(n)$, such that $\mathrm{Lift}(A)$ is a [[negative copy]] of $A$:

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma \vdash \mathrm{Lift}(A):U(s(n))}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma, x:A \vdash \mathrm{LiftEl}(A)(x):\mathrm{Lift}(A)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma, y:\mathrm{Lift}(A) \vdash \mathrm{LiftEl}(A)^{-1}(y):A}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma, x:A \vdash \mathrm{LiftEl}(A)^{-1}(\mathrm{LiftEl}(A)(x)) \equiv x:A}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma, y:\mathrm{Lift}(A) \vdash \mathrm{LiftEl}(A)(\mathrm{LiftEl}(A)^{-1}(y)) \equiv y:\mathrm{Lift}(A)}$$

Next are the rules for [[function types]], which are necessary to define [[type families]] as elements of a type for [[dependent product types]] and the induction principle of the [[natural numbers type]]. Here, [[function types]] are indexed by the universe level $n$, since the function type indexed by $n$ are only definable for $U(n)$-small types, aka types with level $n$. 

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:U(n)}{\Gamma \vdash A \to_{n} B:U(n)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:U(n) \quad \Gamma, x:A \vdash b(x):B}{\Gamma \vdash \lambda x:A.b(x):A \to_{n} B}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:U(n) \quad \Gamma \vdash b:A \to_{n} B}{\Gamma, x:A \vdash b(x):B}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:U(n) \quad \Gamma, x:A \vdash b(x):B}{\Gamma, x:A \vdash (\lambda x:A.b(x))(x) \equiv b(x):B}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:U(n) \quad \Gamma \vdash b:A \to_{n} B}{\Gamma \vdash \lambda x:A.b(x) \equiv b:A \to_{n} B}$$

Similarly, the rules for dependent function types are as follows:

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:\mathrm{Lift}(A) \to_{s(n)} U(n)}{\Gamma \vdash \Pi(n, A, B):U(n)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:\mathrm{Lift}(A) \to_{s(n)} U(n) \quad \Gamma, x:A \vdash b(x):B(\mathrm{LiftEl}(A)(x))}{\Gamma \vdash \lambda x:A.b(x):\Pi(n, A, B)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:\mathrm{Lift}(A) \to_{s(n)} U(n) \quad \Gamma \vdash b:\Pi(n, A, B)}{\Gamma, x:A \vdash b(x):B(\mathrm{LiftEl}(A)(x))}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:\mathrm{Lift}(A) \to_{s(n)} U(n) \quad \Gamma, x:A \vdash b(x):B(\mathrm{LiftEl}(A)(x))}{\Gamma, x:A \vdash (\lambda x:A.b(x))(x) \equiv b(x):B(\mathrm{LiftEl}(A)(x))}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:\mathrm{Lift}(A) \to_{s(n)} U(n) \quad \Gamma \vdash b:\Pi(n, A, B)}{\Gamma \vdash \lambda x:A.b(x) \equiv b:\Pi(n, A, B)}$$

Finally, we have for each universe level $n:\mathbb{N}$ a [[natural numbers type]] $\mathrm{Nat}(n)$ such that $\mathrm{Nat}(0) \equiv \mathbb{N}$ and $\mathrm{Nat}(s(n)) \equiv \mathrm{Lift}(\mathrm{Nat}(n))$. In addition, each $\mathrm{Nat}(n)$ has element $\mathrm{zero}(n):\mathrm{Nat}(n)$ and function $\mathrm{succ}(n):\mathrm{Nat}(n) \to_{n} \mathrm{Nat}(n)$, defined via lifting the elements of $\mathrm{Nat}(n)$ across universe levels. Finally, each $\mathrm{Nat}(n)$ satisfies the induction principle of the [[natural numbers type]] over the universe $U(n)$. 

* Formation rules for natural numbers types:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{Nat}(n):U(n)}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Nat}(0) \equiv \mathbb{N}:U(0)} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{Nat}(s(n)) \equiv \mathrm{Lift}(\mathrm{Nat}(n)):U(s(n))}$$

* Introduction rules for natural numbers types:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{zero}(n):\mathrm{Nat}(n)} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{succ}(n):\mathrm{Nat}(n) \to_{n} \mathrm{Nat}(n)}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{zero}(0) \equiv 0:\mathrm{Nat}(0)} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{succ}(0) \equiv s:\mathrm{Nat}(0) \to_{0} \mathrm{Nat}(0)}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{zero}(s(n)) \equiv \mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{zero}(n)):\mathrm{Nat}(s(n))}$$ 

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N}, m:\mathrm{Nat}(s(n)) \vdash \mathrm{succ}(s(n)) \equiv \mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{succ}(n)):\mathrm{Nat}(s(n)) \to_{s(n)} \mathrm{Nat}(s(n))}$$

* Elimination rules for natural numbers types:

$$\frac{
\begin{array}{c}
\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash C:\mathrm{Lift}(\mathrm{Nat}(n)) \to_{s(n)} U(n) \quad \Gamma \vdash c_0:C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{zero}(n))) \\
\Gamma \vdash c_s:\Pi\left(n, \mathrm{Nat}(n), \lambda x:\mathrm{Nat}(n).C(\mathrm{LiftEl}(\mathrm{Nat}(n))(x)) \to_{n} C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{succ}(n, x)))\right) \\
\end{array}}{\Gamma \vdash \mathrm{ind}_\mathrm{Nat}(n, C, c_0, c_s):\Pi\left(n, \mathrm{Nat}(n), \lambda x:\mathrm{Nat}(n).C(\mathrm{LiftEl}(\mathrm{Nat}(n))(x))\right)}$$

* Computation rules for natural numbers types:

$$\frac{
\begin{array}{c}
\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash C:\mathrm{Lift}(\mathrm{Nat}(n)) \to_{s(n)} U(n) \quad \Gamma \vdash c_0:C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{zero}(n))) \\
\Gamma \vdash c_s:\Pi\left(n, \mathrm{Nat}(n), \lambda x:\mathrm{Nat}(n).C(\mathrm{LiftEl}(\mathrm{Nat}(n))(x)) \to_{n} C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{succ}(n, x)))\right) \\
\end{array}}{\Gamma \vdash \mathrm{ind}_\mathrm{Nat}(n, C, c_0, c_s, \mathrm{zero}(n)) \equiv c_0:C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{zero}(n)))}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash C:\mathrm{Lift}(\mathrm{Nat}(n)) \to_{s(n)} U(n) \quad \Gamma \vdash c_0:C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{zero}(n))) \\
\Gamma \vdash c_s:\Pi\left(n, \mathrm{Nat}(n), \lambda x:\mathrm{Nat}(n).C(\mathrm{LiftEl}(\mathrm{Nat}(n))(x)) \to_{n} C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{succ}(n, x)))\right) \\
\end{array}}{\Gamma, x:\mathrm{Nat}(n) \vdash \mathrm{ind}_\mathrm{Nat}(n, C, c_0, c_s, \mathrm{succ}(n, x)) \equiv c_s(\mathrm{ind}_\mathrm{Nat}(n, C, c_0, c_s, x)):C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{succ}(n, x)))}$$

Something similar could be done for [[Coquand universes]]. 

## Analogues in set theory

There are analogues of cumulative Russell universes in [[set theory]]. 

### With a single set judgment

One formal definition of a set theory with cumulative Russell universes is as follows:

The set theory has [[judgments]] 

* $\Gamma \; \mathrm{ctx}$, that $\Gamma$ is a [[context]]

* $\kappa \; \mathrm{level}$, that $\kappa$ is a universe level, 

* $\phi \; \mathrm{prop}$, that $\phi$ is a [[proposition]], 

* $\phi \; \mathrm{true}$, that $\phi$ is a [[true]] proposition, 

and consists of the formal [[signature (in logic)|signature]] and [[inference rules]] of [[first-order theory|first-order]] [[Heyting arithmetic]] or [[Peano arithmetic]]. These rules ensure that there are an [[infinite]] number of indices, which are strictly ordered with [[strict total order]] $\lt$ and upwardly unbounded, where $\kappa \lt \kappa^+$ is true for all indices $\kappa$. 

Now, we introduce a single [[set]] [[judgment]] $A \; \mathrm{set}$ which says that $A$ is a set, as well as the membership relation $a \in A$, which says that $a$ in the set $A$. We introduce a special kind of set called a **cumulative Russell universe** or **cumulative universe à la Russell**, which formalized with the following rules:

$$\frac{\Gamma \vdash \kappa \; \mathrm{level}}{\Gamma \vdash V_\kappa \; \mathrm{set}} \qquad \frac{\Gamma \vdash \kappa \; \mathrm{level}}{\Gamma \vdash V_\kappa \in V_{\kappa^+} \; \mathrm{true}} \qquad \frac{\Gamma \vdash \kappa \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{set} \quad \Gamma \vdash A \in V_\kappa \; \mathrm{true}}{\Gamma \vdash A \in V_{\kappa^+} \; \mathrm{true}}\mathrm{cumul}$$

### With a separate set judgment for each set theory

There are also analogues of cumulative Russell universes [[à la Coquand]] in [[set theory]]. Instead of having a single set theory, one has a whole collection of set theories which embed into each other, with indices indicating which level the set theory lies on. 

One formal definition of a set theory with cumulative Russell universes [[à la Coquand]] is as follows:

The set theory has [[judgments]] 

* $\Gamma \; \mathrm{ctx}$, that $\Gamma$ is a [[context]]

* $\kappa \; \mathrm{level}$, that $\kappa$ is a level of set theory, 

* $\phi \; \mathrm{prop}$, that $\phi$ is a [[proposition]], 

* $\phi \; \mathrm{true}$, that $\phi$ is a [[true]] proposition, 

and consists of the formal [[signature (in logic)|signature]] and [[inference rules]] of [[first-order theory|first-order]] [[Heyting arithmetic]] or [[Peano arithmetic]]. These rules ensure that there are an [[infinite]] number of indices, which are strictly ordered with [[strict total order]] $\lt$ and upwardly unbounded, where $\kappa \lt \kappa^+$ is true for all indices $\kappa$. 

This allows us to add an infinite number of [[set]] [[judgments]], one set judgment $A \; \mathrm{set}_\kappa$ for every level $\kappa$, indicating that $A$ is a set with level $\kappa$, as well as an infinite number of [[membership relations]] $x \in_\kappa A$, one for each set judgment $\mathrm{set}_\kappa$. Then, one has the following [[inference rules]] for cumulative Russell universes [[à la Coquand]]: 

$$\frac{\Gamma \vdash \kappa \; \mathrm{level}}{\Gamma \vdash V_\kappa \; \mathrm{set}_{\kappa^+}} \quad \frac{\Gamma \vdash \kappa \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{set}_\kappa}{\Gamma \vdash A \; \mathrm{set}_{\kappa^+}}$$

$$\frac{\Gamma \vdash \kappa \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{set}_\kappa}{\Gamma \vdash A \in_{\kappa^+} V_\kappa \; \mathrm{true}} \qquad \frac{\Gamma \vdash \kappa \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{set}_{\kappa^+} \quad \Gamma \vdash A \in_{\kappa^+} V_\kappa \; \mathrm{true}}{\Gamma \vdash A \; \mathrm{set}_\kappa}$$

This says that each $V_\kappa$ is a [[set]] which satisfies a [[reflection principle]]. 

## See also

* [[Tarski universe]]

* [[Coquand universe]]

* [[hierarchy of universes]]

* [[two-level type theory]]

* [[reflection principle]]

## References

The notion is due to:

* [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]): p. 48 in: _Intuitionistic type theory_, Lecture notes Padua 1984, Bibliopolis, Napoli (1984) &lbrack;[pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]]&rbrack;

For more see the references at *[[type universe]]*.

[[!redirects Russell universe]]
[[!redirects Russell universes]]

[[!redirects a la Russell]]

[[!redirects universe a la Russell]]
[[!redirects universes a la Russell]]

[[!redirects à la Russell]]

[[!redirects universe à la Russell]]
[[!redirects universes à la Russell]]

