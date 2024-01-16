
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

In [[dependent type theory]], **Coquand universes** or **universes à la Coquand** are an alternative to [[Russell universes]] and [[Tarski universes]] in presenting [[types]] and the hierarchy of [[type universes]]. Unlike type theories with Russell universes, which usually have either no separate type judgment, like that found in the *[[HoTT book]]*, or one type judgment, or type theories with Tarski universe, which are required to have one type judgment, type theories with Coquand universes have a type judgment for every universe in the type theory. 

## Formal definition

### With a type judgment for each universe

One formal definition of a type theory with Coquand universes is as follows:

The type theory has [[judgments]] 

* $\Gamma \; \mathrm{ctx}$, that $\Gamma$ is a [[context]]

* $i \; \mathrm{level}$, that $i$ is a universe level, 

* $\phi \; \mathrm{prop}$, that $\phi$ is a [[proposition]], 

* $\phi \; \mathrm{true}$, that $\phi$ is a [[true]] proposition, 

and consists of the formal [[signature (in logic)|signature]] and [[inference rules]] of [[first-order theory|first-order]] [[Heyting arithmetic]] or [[Peano arithmetic]]. These rules ensure that there are an [[infinite]] number of indices, which are strictly ordered with [[strict total order]] $\lt$ and upwardly unbounded, where $i \lt s(i)$ is true for all indices $i$. 

This allows us to add an infinite number of [[type]] [[judgments]], one type judgment $A \; \mathrm{type}_i$ for every level $i$, indicating that $A$ is a type with level $i$, as well as [[term]] judgments $a:A$. Then, one has the following [[inference rules]] for Coquand universes: 

$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash U_i \; \mathrm{type}_{s(i)}} \quad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \mathrm{Lift}_i(A) \; \mathrm{type}_{s(i)}}$$

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \mathrm{Code}(A):U_i} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash B:U_i}{\Gamma \vdash \mathrm{El}(B) \; \mathrm{type}_i}$$

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \mathrm{El}_i(\mathrm{Code}_i(A)) \equiv A \; \mathrm{type}_i} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash B:U_i}{\Gamma \vdash \mathrm{Code}_i(\mathrm{El}(B)) \equiv B:U_i}$$

There are also weak versions of Coquand universes, where one uses [[identifications]] and [[equivalences of types]] instead of [[judgmental equality]]:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \beta_{U_i}^A:\mathrm{El}_i(\mathrm{Code}_i(A)) \simeq A} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash B:U_i}{\Gamma \vdash \eta_{U_i}(B):\mathrm{Code}_i(\mathrm{El}(B)) =_{U_i} B}$$

The [[univalence axiom]] for Coquand universes states that for all $A:U_i$ and $B:U_i$, [[type transport|transport]] across $\mathrm{Lift}_i(\mathrm{El}_i(-))$ is an [[equivalence of types]]

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash B:U_i}{\Gamma \vdash \mathrm{ua}_{U_i}(A, B):\mathrm{isEquiv}(\mathrm{transport}_{x:U_i.\mathrm{Lift}_i(\mathrm{El}_i(x))}(A, B))}$$

### With a single separate type judgment

It is also possible to define the hierarchy of Coquand universes with a single separate type judgment, such that every single type is in a Coquand universe. The advantage of doing so is that one doesn't need to define the theory of universe levels before defining the type theory; one could instead simply define the natural numbers inside of the type theory itself, along with the hierarchy of Coquand universes:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{N} \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{Level}(A):\mathbb{N}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash U(n) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{Code}(n)(A):U(\mathrm{Level}(A))}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma \vdash \mathrm{El}(n, A) \; \mathrm{type}} \quad \frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma \vdash \mathrm{Level}(\mathrm{El}(n, A)) \equiv n:\mathbb{N}}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma \vdash \mathrm{Code}(n)(\mathrm{El}(n, A)) \equiv A:U(n)}$$ 

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{El}(n, \mathrm{Code}(n)(A)) \equiv A \; \mathrm{type}} \quad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{Level}(\mathrm{El}(n, \mathrm{Code}(n)(A))) \equiv \mathrm{Level}(A):\mathbb{N}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Level}(\mathbb{N}) \equiv 0:\mathbb{N}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash s(n):\mathbb{N}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{Level}(U(n)) \equiv s(n):\mathbb{N}}$$

In particular, every type $A$ has a universe level, which is a natural number, and the universe level of $\mathbb{N}$ is zero and the universe level of $U(n)$ given natural number $n$ is the successor $s(n)$. 

Furthermore, every type $A$ of level $n$ lifts to another type $\mathrm{Lift}(A)$ of level $s(n)$, such that $\mathrm{El}(s(n), \mathrm{Lift}(A))$ is a [[negative copy]] of $\mathrm{El}(n, A)$:

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma \vdash \mathrm{Lift}(A):U(s(n))}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma, x:\mathrm{El}(n, A) \vdash \mathrm{LiftEl}(A)(x):\mathrm{El}(s(n), \mathrm{Lift}(A))}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma, y:\mathrm{El}(s(n), \mathrm{Lift}(A)) \vdash \mathrm{LiftEl}(A)^{-1}(y):\mathrm{El}(n, A)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma, x:\mathrm{El}(n, A) \vdash \mathrm{LiftEl}(A)^{-1}(\mathrm{LiftEl}(A)(x)) \equiv x:\mathrm{El}(n, A)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n)}{\Gamma, y:\mathrm{El}(s(n), \mathrm{Lift}(A)) \vdash \mathrm{LiftEl}(A)(\mathrm{LiftEl}(A)^{-1}(y)) \equiv y:\mathrm{El}(s(n), \mathrm{Lift}(A))}$$

Next are the rules for [[function types]], which are necessary to define [[type families]] as elements of a type for [[dependent product types]] and the induction principle of the [[natural numbers type]]. Here, [[function types]] are indexed by the universe level $n$, since the function type indexed by $n$ are only definable for $U(n)$-small types, aka types with level $n$. 

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:U(n)}{\Gamma \vdash A \to_{n} B:U(n)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:U(n) \quad \Gamma, x:\mathrm{El}(n, A) \vdash b(x):\mathrm{El}(n, B)}{\Gamma \vdash \lambda x:A.b(x):\mathrm{El}(n, A \to_{n} B)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:U(n) \quad \Gamma \vdash b:\mathrm{El}(n, A \to_{n} B)}{\Gamma, x:\mathrm{El}(n, A) \vdash b(x):\mathrm{El}(n, B)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:U(n) \quad \Gamma, x:\mathrm{El}(n, A) \vdash b(x):\mathrm{El}(n, B)}{\Gamma, x:\mathrm{El}(n, A) \vdash (\lambda x:A.b(x))(x) \equiv b(x):\mathrm{El}(n, B)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:U(n) \quad \Gamma \vdash b:\mathrm{El}(n, A \to_{n} B)}{\Gamma \vdash \lambda x:A.b(x) \equiv b:\mathrm{El}(n, A \to_{n} B)}$$

Similarly, the rules for dependent function types are as follows:

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:\mathrm{El}(s(n), \mathrm{Lift}(A)) \to_{s(n)} U(n)}{\Gamma \vdash \Pi(n, A, B):U(n)}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:\mathrm{El}(s(n), \mathrm{Lift}(A)) \to_{s(n)} U(n) \quad \Gamma, x:\mathrm{El}(n, A) \vdash b(x):\mathrm{El}(n, B(\mathrm{LiftEl}(A)(x)))}{\Gamma \vdash \lambda x:A.b(x):\mathrm{El}(n, \Pi(n, A, B))}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:\mathrm{El}(s(n), \mathrm{Lift}(A)) \to_{s(n)} U(n) \quad \Gamma \vdash b:\mathrm{El}(n, \Pi(n, A, B))}{\Gamma, x:\mathrm{El}(n, A) \vdash b(x):\mathrm{El}(n, B(\mathrm{LiftEl}(A)(x)))}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:\mathrm{El}(s(n), \mathrm{Lift}(A)) \to_{s(n)} U(n) \quad \Gamma, x:\mathrm{El}(n, A) \vdash b(x):\mathrm{El}(n, B(\mathrm{LiftEl}(A)(x)))}{\Gamma, x:\mathrm{El}(n, A) \vdash (\lambda x:A.b(x))(x) \equiv b(x):\mathrm{El}(n, B(\mathrm{LiftEl}(A)(x)))}$$

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash A:U(n) \quad \Gamma \vdash B:\mathrm{El}(s(n), \mathrm{Lift}(A)) \to_{s(n)} U(n) \quad \Gamma \vdash b:\mathrm{El}(n, \Pi(n, A, B))}{\Gamma \vdash \lambda x:A.b(x) \equiv b:\mathrm{El}(n, \Pi(n, A, B))}$$

Finally, we have for each universe level $n:\mathbb{N}$ a [[natural numbers type]] $\mathrm{Nat}(n)$ such that $\mathrm{Nat}(0) \equiv \mathrm{Code}(0)(\mathbb{N})$ and $\mathrm{Nat}(s(n)) \equiv \mathrm{Lift}(\mathrm{Nat}(n))$. In addition, each $\mathrm{Nat}(n)$ has element $\mathrm{zero}(n):\mathrm{El}(n, \mathrm{Nat}(n))$ and function $\mathrm{succ}(n):\mathrm{El}(n, \mathrm{Nat}(n) \to_{n} \mathrm{Nat}(n))$, defined via lifting the elements of $\mathrm{Nat}(n)$ across universe levels. Finally, each $\mathrm{Nat}(n)$ satisfies the induction principle of the [[natural numbers type]] over the universe $U(n)$. 

* Formation rules for natural numbers types:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{Nat}(n):U(n)}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Nat}(0) \equiv \mathrm{Code}(0)(\mathbb{N}):U(0)} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{Nat}(s(n)) \equiv \mathrm{Lift}(\mathrm{Nat}(n)):U(s(n))}$$

* Introduction rules for natural numbers types:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{zero}(n):\mathrm{El}(n, \mathrm{Nat}(n))} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{succ}(n):\mathrm{El}(n, \mathrm{Nat}(n) \to_{n} \mathrm{Nat}(n))}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{zero}(0) \equiv 0:\mathrm{El}(0, \mathrm{Nat}(0))} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{succ}(0) \equiv s:\mathrm{El}(0, \mathrm{Nat}(0) \to_{0} \mathrm{Nat}(0))}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N} \vdash \mathrm{zero}(s(n)) \equiv \mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{zero}(n)):\mathrm{El}(s(n), \mathrm{Nat}(s(n)))}$$ 

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, n:\mathbb{N}, m:\mathrm{Nat}(s(n)) \vdash \mathrm{succ}(s(n)) \equiv \mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{succ}(n)):\mathrm{El}(s(n), \mathrm{Nat}(s(n)) \to_{s(n)} \mathrm{Nat}(s(n)))}$$

* Elimination rules for natural numbers types:

$$\frac{
\begin{array}{c}
\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash C:\mathrm{El}(s(n), \mathrm{Lift}(\mathrm{Nat}(n)) \to_{s(n)} U(n)) \quad \Gamma \vdash c_0:\mathrm{El}(n, C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{zero}(n)))) \\
\Gamma \vdash c_s:\mathrm{El}(n, \Pi\left(n, \mathrm{Nat}(n), \lambda x:\mathrm{Nat}(n).C(\mathrm{LiftEl}(\mathrm{Nat}(n))(x)) \to_{n} C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{succ}(n, x)))\right)) \\
\end{array}}{\Gamma \vdash \mathrm{ind}_\mathrm{Nat}(n, C, c_0, c_s):\mathrm{El}(n, \Pi\left(n, \mathrm{Nat}(n), \lambda x:\mathrm{Nat}(n).C(\mathrm{LiftEl}(\mathrm{Nat}(n))(x))\right))}$$

* Computation rules for natural numbers types:

$$\frac{
\begin{array}{c}
\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash C:\mathrm{El}(s(n), \mathrm{Lift}(\mathrm{Nat}(n)) \to_{s(n)} U(n)) \quad \Gamma \vdash c_0:\mathrm{El}(n, C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{zero}(n)))) \\
\Gamma \vdash c_s:\mathrm{El}(n, \Pi\left(n, \mathrm{Nat}(n), \lambda x:\mathrm{Nat}(n).C(\mathrm{LiftEl}(\mathrm{Nat}(n))(x)) \to_{n} C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{succ}(n, x)))\right)) \\
\end{array}}{\Gamma \vdash \mathrm{ind}_\mathrm{Nat}(n, C, c_0, c_s, \mathrm{zero}(n)) \equiv c_0:\mathrm{El}(n, C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{zero}(n))))}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash n:\mathbb{N} \quad \Gamma \vdash C:\mathrm{El}(s(n), \mathrm{Lift}(\mathrm{Nat}(n)) \to_{s(n)} U(n)) \quad \Gamma \vdash c_0:\mathrm{El}(n, C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{zero}(n)))) \\
\Gamma \vdash c_s:\mathrm{El}(n, \Pi\left(n, \mathrm{Nat}(n), \lambda x:\mathrm{Nat}(n).C(\mathrm{LiftEl}(\mathrm{Nat}(n))(x)) \to_{n} C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{succ}(n, x)))\right)) \\
\end{array}}{\Gamma, x:\mathrm{Nat}(n) \vdash \mathrm{ind}_\mathrm{Nat}(n, C, c_0, c_s, \mathrm{succ}(n, x)) \equiv c_s(\mathrm{ind}_\mathrm{Nat}(n, C, c_0, c_s, x)):\mathrm{El}(n, C(\mathrm{LiftEl}(\mathrm{Nat}(n))(\mathrm{succ}(n, x))))}$$

Something similar could be done for [[Russell universes]].

## Analogues in set theory

There are analogues of Coquand universes in [[set theory]]. Instead of having a single set theory, one has a whole collection of set theories which embed into each other, with indices indicating which level the set theory lies on. 

One formal definition of a set theory with Coquand universes is as follows:

The set theory has [[judgments]] 

* $\Gamma \; \mathrm{ctx}$, that $\Gamma$ is a [[context]]

* $\kappa \; \mathrm{level}$, that $\kappa$ is a level of set theory, 

* $\phi \; \mathrm{prop}$, that $\phi$ is a [[proposition]], 

* $\phi \; \mathrm{true}$, that $\phi$ is a [[true]] proposition, 

and consists of the formal [[signature (in logic)|signature]] and [[inference rules]] of [[first-order theory|first-order]] [[Heyting arithmetic]] or [[Peano arithmetic]]. These rules ensure that there are an [[infinite]] number of indices, which are strictly ordered with [[strict total order]] $\lt$ and upwardly unbounded, where $\kappa \lt \kappa^+$ is true for all indices $\kappa$. 

This allows us to add an infinite number of [[set]] [[judgments]], one set judgment $A \; \mathrm{set}_\kappa$ for every level $\kappa$, indicating that $A$ is a set with level $\kappa$, as well as an infinite number of [[membership relations]] $x \in_\kappa A$, one for each set judgment $\mathrm{set}_\kappa$. Then, one has the following [[inference rules]] for Coquand universes: 

$$\frac{\Gamma \vdash \kappa \; \mathrm{level}}{\Gamma \vdash V_\kappa \; \mathrm{set}_{\kappa^+}} \quad \frac{\Gamma \vdash \kappa \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{set}_\kappa}{\Gamma \vdash \mathrm{Code}_{\kappa}(A) \; \mathrm{set}_{\kappa^+}}$$

$$\frac{\Gamma \vdash \kappa \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{set}_\kappa}{\Gamma \vdash \mathrm{Code}_{\kappa}(A) \in_{\kappa^+} V_\kappa \; \mathrm{true}} \qquad \frac{\Gamma \vdash \kappa \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{set}_{\kappa^+} \quad \Gamma \vdash A \in_{\kappa^+} V_\kappa \; \mathrm{true}}{\Gamma \vdash \mathrm{El}_{\kappa}(A) \; \mathrm{set}_\kappa}$$

$$\frac{\Gamma \vdash \kappa \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{set}_\kappa}{\Gamma \vdash \mathrm{El}_{\kappa}(\mathrm{Code}_{\kappa}(A)) = A \; \mathrm{true}} \qquad \frac{\Gamma \vdash \kappa \; \mathrm{level} \quad \Gamma \vdash A \; \mathrm{set}_{\kappa^+} \quad \Gamma \vdash A \in_{\kappa^+} V_\kappa \; \mathrm{true}}{\Gamma \vdash \mathrm{Code}_{\kappa}(\mathrm{El}_{\kappa}(A)) = A \; \mathrm{true}}$$

This says that each $V_\kappa$ is a [[set]] which satisfies a [[reflection principle]]. 

## Related concepts

* [[type universe]]

  * [[Russell universe]]

  * [[Tarski universe]]

* [[hierarchy of universes]]

* [[reflection principle]]

## References

Universes à la Coquand are described in section 2.1 of

* [[Daniel Gratzer]], [[G. Alex Kavvos]], [[Andreas Nuyts]], [[Lars Birkedal]]: _Multimodal Dependent Type Theory_, Logical Methods in Computer Science **17** 3 (2021) lmcs:7713 &lbrack;[arXiv:2011.15021](https://arxiv.org/abs/2011.15021), <a href="https://doi.org/10.46298/lmcs-17(3:11)2021">doi:10.46298/lmcs-17(3:11)2021</a>&rbrack;

[[!redirects Coquand universe]]
[[!redirects Coquand universes]]

[[!redirects à la Coquand]]

[[!redirects universe à la Coquand]]
[[!redirects universes à la Coquand]]


[[!redirects strict Coquand universe]]
[[!redirects strict Coquand universes]]

[[!redirects strictly à la Coquand]]

[[!redirects universe strictly à la Coquand]]
[[!redirects universes strictly à la Coquand]]

[[!redirects strict universe à la Coquand]]
[[!redirects strict universes à la Coquand]]


[[!redirects weak Coquand universe]]
[[!redirects weak Coquand universes]]

[[!redirects weakly à la Coquand]]

[[!redirects universe weakly à la Coquand]]
[[!redirects universes weakly à la Coquand]]

[[!redirects weak universe à la Coquand]]
[[!redirects weak universes à la Coquand]]