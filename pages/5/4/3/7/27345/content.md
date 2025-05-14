
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

Dependent type theory is traditionally said to be a [[predicative mathematics|predicative]] [[foundations of mathematics]]. However, this is only the case if [[excluded middle]] is not assumed in the theory, because once excluded middle holds, then [[power sets]] are simply [[function types]] into the [[type of booleans]] resulting in an [[impredicative mathematics|impredicative]] foundations of mathematics. Function types into the type of booleans are in most versions of dependent type theory. 

The real problem here is with [[function types]] and [[dependent product type]]. These types are usually placed in the same [[type universe]] as the types from which they are formed from; i.e. if $A:U_i$ and $B:U_i$, then $A \to B:U_i$. For dependent type theory to remain predicative even in the presence of excluded middle, the function types and dependent product type have to lie in the next universe up; i.e. if $A:U_i$ and $B:U_i$, $A \to B:U_{i+1}$. Thus, the concept of a *[[strongly predicative mathematics|strongly predicative]] dependent type theory*, which can implement [[strongly predicative mathematics]]. 

In strongly predicative dependent type theory, the resulting universes of $U$-small sets only form a [[arithmetic pretopos]] instead of a [[ΠW-pretopos]]. However, there have been some precedent in the existing literature of working in an arithmetic pretopos instead of a ΠW-pretopos. For example, [[Steve Vickers]]'s program of [[geometric mathematics]] occurs informally inside of a [[Grothendieck topos]] and does not assume function types for [[topology|topological]] reasons, and he has proposed a kind of [[geometric type theory]] as the [[internal logic]] of said Grothendieck topos ([Vickers 2007](#Vickers07), [Vickers 2017](#Vickers17), [Vickers 2018](#Vickers18), [Vickers 2022](#Vickers22)). In addition, [[Ulrik Buchholtz]] and [[Johannes Schipp von Branitz]] have proposed a version of [[dependent type theory]] where the base universe $U_0$ does not contain any [[function types]] or [[dependent product types]], so that they can study [[primitive recursive arithmetic]] in the context of [[homotopy type theory]] ([Buchholtz & von Branitz 2024](#BvB24)). 

## Formal presentation

We present strongly predicative dependent type theory as a dependent type theory with a [[hierarchy of universes]] and no [[type]] [[judgment]], in the manner of [[Book HoTT]] found in [Univalent Foundations Project 2013](#UFP13). We also add the [[type theoretic axiom of replacement]] from [Bezem et al 2021](#BBCDG) and [Rijke 2022](#Rijke22), so that we have [[quotient sets]] in all universes. 

The type theory has [[judgments]] for contexts

* $\Gamma \; \mathrm{ctx}$, that $\Gamma$ is a [[context]]

### Universe levels and Peano arithmetic

Then we have judgments for universe levels and predicate logic:

* $i \; \mathrm{level}$, that $i$ is a universe level, 

* $\phi \; \mathrm{prop}$, that $\phi$ is a [[proposition]], 

* $\phi \; \mathrm{true}$, that $\phi$ is a [[true]] proposition, 

and the formal [[signature (in logic)|signature]] and [[inference rules]] of [[first-order theory|first-order]] [[Heyting arithmetic]] or [[Peano arithmetic]]. 

These rules ensure that there are an [[infinite]] number of indices, which are strictly ordered with [[strict total order]] $\lt$ and upwardly unbounded, where $i \lt s(i)$ is true for all indices $i$. 

### Typing judgments and Russell universes

Now, we introduce the typing judgment $a:A$, which says that $a$ is a term of the type $A$. Instead of type judgments, we introduce a special kind of type called a [[Russell universe]], whose terms are the types themselves. Russell universes are formalized with the following rules:

$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash U_i:U_{s(i)}} \qquad \frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i}{\Gamma \vdash A:U_{s(i)}}$$

In addition, we have rules for contexts which state that one could add typing judgments to the list of contexts:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i}{(\Gamma, a:A) \; \mathrm{ctx}}$$

### Structural rules

There are three structural rules in dependent type theory, the [[variable rule]], the [[weakening rule]], and the [[substitution rule]]. 

The variable rule states that we may derive a typing judgment if the typing judgment is in the context already:

$$\frac{\Gamma, a:A, \Delta \; \mathrm{ctx}}{\Gamma, a:A, \Delta \vdash a:A}$$

Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

The weakening rule:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma, \Delta \vdash \mathcal{J}}{\Gamma, a:A, \Delta \vdash \mathcal{J}}$$

The substitution rule:

$$\frac{\Gamma \vdash a:A \quad \Gamma, b:A, \Delta \vdash \mathcal{J}}{\Gamma, \Delta[a/b] \vdash \mathcal{J}[a/b]}$$

The weakening and substitution rules are admissible rules: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

### Structural rules for judgmental equality

Judgmental equality has its own structural rules: introduction rules for judgmentally equal terms, reflexivity, symmetry, transitivity, the principle of substitution, and the variable conversion rule. 

* Introduction rules for judgmentally equal terms
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash a \equiv b:A}{\Gamma \vdash a:A}$$
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash a \equiv b:A}{\Gamma \vdash b:A}$$

* Reflexivity of judgmental equality
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash a:A}{\Gamma \vdash a \equiv a:A}$$

* Symmetry of judgmental equality
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash a \equiv b:A}{\Gamma \vdash b \equiv a:A}$$

* Transitivity of judgmental equality
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash a \equiv b:A \quad \Gamma \vdash b \equiv c:A}{\Gamma \vdash a \equiv c:A}$$

* Principle of substitution:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash a \equiv b : A \quad \Gamma, x:A, \Delta \vdash c:B}{\Gamma, \Delta[b/x] \vdash c[a/x] \equiv c[b/x]: B[b/x]}$$

* Variable conversion rule:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A \equiv B:U_i \quad \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Gamma, x:B, \Delta \vdash \mathcal{J}}$$

We also have a rules saying that equality is preserved across universe levels:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash j \; \mathrm{level} \quad \Gamma \vdash i = j \; \mathrm{true}}{\Gamma \vdash U_i \equiv U_j:U_{s(i)}}$$

### Dependent product types

The key difference in strongly predicative dependent type theory from the usual [[weakly predicative mathematics|weakly predicative]] dependent type theory comes in the formation rule of [[dependent product types]]. Given types $A:U_i$ and type family $x:A \vdash B(x):U_i$, instead of lying in the universe level $i$, the dependent product type instead lies in the next universe level $U_{s(i)}$. 

* Formation rules for dependent product types:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma, x:A \vdash B:U_i}{\Gamma \vdash \prod_{x:A} B(x):U_{s(i)}}$$

* Introduction rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b:B}{\Gamma \vdash \lambda(x:A).b(x):\prod_{x:A} B(x)}$$

* Elimination rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash f[a/x]:B[a/x]}$$

* Computation rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)[a/x] \equiv b[a/x]:B[a/x]}$$

* Uniqueness rules for dependent product types:

$$\frac{\Gamma \vdash f:\prod_{x:A} B(x)}{\Gamma \vdash f \equiv \lambda(x).f(x):\prod_{x:A} B(x)}$$

### Dependent sum types

* Formation rules for dependent sum types:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma, x:A \vdash B:U_i}{\Gamma \vdash \sum_{x:A} B(x):U_i}$$

* Introduction rules for dependent sum types:

$$\frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A \quad \Gamma \vdash b:B[a/x]}{\Gamma \vdash (a, b):\sum_{x:A} B(x)}$$

* Elimination rules for dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash \pi_2(z):B[\pi_1(z)/x]}$$

* Computation rules for dependent sum types:

$$\frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_1(a, b) \equiv a:A} \qquad \frac{\Gamma, x:A \vdash b:B \quad \Gamma \vdash a:A}{\Gamma \vdash \pi_2(a, b) \equiv b:B[\pi_1(a, b)/x]}$$

* Uniqueness rules for dependent sum types:

$$\frac{\Gamma \vdash z:\sum_{x:A} B(x)}{\Gamma \vdash z \equiv (\pi_1(z), \pi_2(z)):\sum_{x:A} B(x)}$$

### Resizing dependent products of dependent products

According to the formation rules of dependent product types, given a type $A:U_i$, and type families $x:A \vdash B(x):U_i$, $x:A, y:B(x) \vdash C(x, y):U_i$, the dependent product type

$$\prod_{x:A} \prod_{y:B(x)} C(x, y)$$

is in the universe level $U_{i + 2}$, because for each $x:A$, the dependent product type $\prod_{y:B(x)} C(x, y)$ is already in the universe level $U_{i + 1}$. However, by [[currying]] (i.e. the induction principle of dependent sum types), the above type is equivalent to the dependent product type

$$\prod_{z:\sum_{x:A} B(x)} C(\pi_1(z), \pi_2(z))$$

which is only in the universe level $U_{i + 1}$, since both the index type $\sum_{x:A} B(x)$ and each $C(\pi_1(z), \pi_2(z))$ for $z:\sum_{x:A} B(x)$ is in $U_{i}$. Thus, the [[equivalence of types]] induced by currying allows for the resizing of 

$$\prod_{x:A} \prod_{y:B(x)} C(x, y)$$

down to the universe level $U_{i + 1}$. By induction over the natural numbers, this is true of any finite list of dependent products of type families in $U_i$ indexed by types in $U_i$. 

### Sum types

* Formation rules for sum types:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash B:U_i}{\Gamma \vdash A + B:U_i}$$

* Introduction rules for sum types:

$$\frac{\Gamma \vdash a:A}{\Gamma \vdash \mathrm{inl}(a):A + B} \qquad \frac{\Gamma \vdash b:B}{\Gamma \vdash \mathrm{inr}(b):A + B}$$

* Elimination rules for sum types:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, z:A + B \vdash C:U_i \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B}{\Gamma \vdash \mathrm{ind}_{A + B}(z.C, x.c, y.d, e):C[e/z]}$$

* Computation rules for sum types:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, z:A + B \vdash C:U_i \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{ind}_{A + B}(z.C, x.c, y.d, \mathrm{inl}(a)) \equiv c[a/x]:C[\mathrm{inl}(a)/z]}$$
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, z:A + B \vdash C:U_i \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash b:A}{\Gamma \vdash \mathrm{ind}_{A + B}(z.C, x.c, y.d, \mathrm{inr}(b)) \equiv d[b/x]:C[\mathrm{inr}(b)/z]}$$

### Empty type

* Formation rules for the empty type:

$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash \mathbb{0}:U_i}$$

* Elimination rules for the empty type:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, x:\mathbb{0} \vdash C:U_i \quad \Gamma \vdash p:\mathbb{0}}{\Gamma \vdash \mathrm{ind}_\mathbb{0}(x.C, p):C[p/x]}$$

### Unit type

* Formation rules for the unit type:

$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash \mathbb{1}:U_i}$$

* Introduction rules for the unit type:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash *:\mathbb{1}}$$

* Elimination rules for the unit type:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, x:\mathbb{1} \vdash C:U_i \quad \Gamma, y:\mathbb{1} \vdash c[y/x]:C[y/x] \quad \Gamma \vdash p:\mathbb{1}}{\Gamma \vdash \mathrm{ind}_\mathbb{1}(x.C, y.c, p):C[p/x]}$$

* Computation rules for the unit type:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, x:\mathbb{1} \vdash C:U_i \quad \Gamma, y:\mathbb{1} \vdash c[y/x]:C[y/x]}{\Gamma \vdash \mathrm{ind}_\mathbb{1}(x.C, y.c, *) \equiv c[*/x]:C[*/x]}$$

### Natural numbers

* Formation rules for the natural numbers:
$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash \mathbb{N}:U_i}$$

* Introduction rules for the natural numbers:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Gamma \vdash n:\mathbb{N}}{\Gamma \vdash s(n):\mathbb{N}}$$

* Elimination rules for the natural numbers:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, x:\mathbb{N} \vdash C:U_i \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma, x:\mathbb{N}, y:C \vdash c_s:C[s(x)/x] \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \mathrm{ind}_\mathbb{N}(x.C, c_0, x.y.c_s, n):C[n/x]}$$

* Computation rules for the natural numbers:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, x:\mathbb{N} \vdash C:U_i \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma, x:\mathbb{N}, y:C \vdash c_s:C[s(x)/x]}{\Gamma \vdash \mathrm{ind}_\mathbb{N}(x.C, c_0, x.y.c_s, 0) \equiv c_0:C[0/x]}$$

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, x:\mathbb{N} \vdash C:U_i \quad \Gamma \vdash c_0:C[0/x] \quad \Gamma, x:\mathbb{N}, y:C \vdash c_s:C[s(x)/x]}{\Gamma \vdash \mathrm{ind}_\mathbb{N}(x.C, c_0, x.y.c_s, s(n) \equiv c_s(n, \mathrm{ind}_\mathbb{N}(x.C, c_0, x.y.c_s, n)):C[s(n)/x]}$$

### Identity types

There is another version of equality in dependent type theory, called [[typal equality]]. Typal equality is represented by the [[identity type]]. 

* Formation rule for identity types:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A}{\Gamma \vdash a =_A b:U_i}$$

* Introduction rule for identity types:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{refl}_A(a) : a =_A a}$$

* Elimination rule for identity types:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, x:A, y:A, p:a =_A b \vdash C:U_i \quad \Gamma, z:A \vdash t:C[z/a, z/b, \mathrm{refl}_A(z)/p] \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash q:a =_A b}{\Gamma \vdash J(x,y,p.C, z.t, a, b, q):C[a, b, q/x, y, p]}$$

* Computation rules for identity types:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, x:A, y:A, p:a =_A b \vdash C:U_i \quad \Gamma, z:A \vdash t:C[z/a, z/b, \mathrm{refl}_A(z)/p] \quad \Gamma \vdash a:A}{\Gamma \vdash J(x.y.p.C, z.t, a, a, \mathrm{refl}(a)) \equiv t:C[a, a, \mathrm{refl}_A(a)/x, y, p]}$$

### Propositional truncations

* Formation rules for propositional truncations:

$$\frac{\Gamma \vdash A:U_i}{\Gamma \vdash [A]:U_i}$$

* Introduction rules for propositional truncations:

$$\frac{\Gamma \vdash A:U_i}{\Gamma, x:A \vdash [x]:[A]}$$

$$\frac{\Gamma \vdash A:U_i}{\Gamma, x:A, y:A \vdash \mathrm{trunc}_A(x, y):[x] =_{[A]} [y]}$$

* Elimination rules for propositional truncations:

$$\frac{\Gamma \vdash A:U_i \quad \Gamma, x:A \vdash B(x):U_i \quad \Gamma, x:A, y:B(x), z:B(x) \vdash p(x, y, z):y =_{B(x)} z \quad \Gamma, x:A \vdash f(x):B([x])}{\Gamma, x:[A] \vdash \mathrm{ind}_{[A]}(B, p, f, x):B(x)}$$

* Computation rules for propositional truncations:

$$\frac{\Gamma \vdash A:U_i \quad \Gamma, x:A \vdash B(x):U_i \quad \Gamma, x:A, y:B(x), z:B(x) \vdash p(x, y, z):y =_{B(x)} z \quad \Gamma, x:A \vdash f(x):B([x]) \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{ind}_{[A]}(B, p, f, [a]) \equiv f(a):B([a])}$$

### Univalence

Given types $A:U_i$ and $B:U_i$, a function $f:A \to B$ is an [[equivalence of types]] if the fiber of $f$ at each element of $B$ has exactly one element. The property of the type $A$ having exactly one element is represented by the [[isContr]] modality which states that the type $A$ is contractible. The fiber of $f$ at an element $b:B$ is given by the type
$$\sum_{b:B} f(a) =_B b$$

We formally define the property of $R$ being a one-to-one correspondence or an equivalence of types as the type:

$$\mathrm{isEquiv}_{A, B}(f) \coloneqq \prod_{b:B} \mathrm{isContr}\left(\sum_{a:A} f(a) =_B b\right)$$

We define the type of equivalences from $A$ to $B$ as 

$$A \simeq B \coloneqq \sum_{f:A \to B} \mathrm{isEquiv}_{A, B}(f)$$

There is a function 

$$\mathrm{idtoequiv}_{A, B}:(A =_{U_i} B) \to (A \simeq B)$$ 

which is inductively defined on reflexivity to be the identity function on $A$

$$\mathrm{idtoequiv}_{A, A}(\mathrm{refl}_{U_i}(A)) \equiv id_A$$

Note that both $A =_{U_i} B$ and $A \simeq B$ lie in the universe $U_{i + 1}$ in strongly predicative dependent type theory. 

The [[univalence axiom]] then states that $\mathrm{idtoequiv}_{A, B}$ is an equivalence for all external natural numbers $i \in \mathcal{N}$ and types $A:U_i$ and $B:U_i$:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash B:U_i}{\Gamma \vdash \mathrm{ua}_{U_i}(A, B):\mathrm{isEquiv}_{A =_{U_i} B, A \simeq B}(\mathrm{idtoequiv}_{A, B})}$$ 

### Replacement

The [[image]] of a function $x:A \vdash f(x):B$ is given by the type 

$$\mathrm{im}(f) \coloneqq \sum_{y:B} \left[\sum_{x:A} f(x) =_B y\right]$$

The [[type theoretic axiom of replacement]] states that for all universe levels $i$, for every [[essentially small type|essentially $U_i$-small]] type $A$, every [[locally small type|locally $U_i$-small]] type $B$, and every function $x:A \vdash f(x):B$, the [[image]] $\mathrm{im}(f)$ is essentially $U_i$-small. From the axiom of replacement one can construct [[quotient sets]] in all $U_i$, cf. section 2.22.9 of [Bezam et al 2021](#BBCDG). 

Thus, the [[h-sets]] in each $U_i$ form an [[arithmetic pretopos]]. 

### Excluded middle

The [[law of excluded middle]] can be formulated in strongly predicative dependent type theory as the following: that for each universe level $i$, the canonical [[embedding of types|embedding]] of the [[type of booleans]] $\mathbb{2}$ into the [[type of propositions|type of $U_i$-small propositions]], which takes $0:\mathbb{2}$ to the [[empty type]] and $1:\mathbb{2}$ to the [[unit type]], is an [[equivalence of types]]. 

Thus, with excluded middle, the [[h-sets]] in each $U_i$ form an [[arithmetic pretopos|arithmetic]] [[Boolean pretopos]] and the univeres $U_i$ themselves correspond to the [[regular cardinals]] in [[set theory]]. 

## Related concepts

* [[dependent type theory]]

* [[impredicative dependent type theory]]

* [[Book HoTT]]

* [[predicative mathematics]]

* [[arithmetic pretopos]]

* [[geometric mathematics]]

* [[geometric type theory]]

## References

* {#Vickers07} [[Steve Vickers]], _Locales and toposes as spaces_, Chapter 8 in _Handbook of Spatial Logics_ (ed. Aiello, Pratt-Hartman, van Bentham), Springer, 2007, pp. 429-496. 

* {#Vickers17}[[Steve Vickers]], _Arithmetic universes and classifying toposes_, Cahiers de topologie et g&eacute;om&eacute;trie diff&eacute;rentielle cat&eacute;gorique **58 (4)** (2017), pp. 213-248 ([pdf](http://arxiv.org/abs/1701.04611))

* {#Vickers18}[[Steve Vickers]], _Sketches for arithmetic universes_, accepted 2018 for Journal of Logic and Analysis ([pdf](http://arxiv.org/abs/1608.01559))

* {#Vickers22} [[Steve Vickers]], *Generalized point-free spaces, pointwise* &lbrack;[arXiv:2206.01113](https://arxiv.org/abs/2206.01113)&rbrack;

* {#BvB24} [[Ulrik Buchholtz]], [[Johannes Schipp von Branitz]], *Primitive Recursive Dependent Type Theory* ([arXiv:2404.01011](https://arxiv.org/abs/2404.01011))

* {#UFP13} *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* {#BBCDG} [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], Section 2.19 in: *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$ 

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

Some discussion about a dependent type theory whose dependent function types reside in the next universe level appeared in:

* *One universe as a foundation & friends*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/channel/229136-theory.3A-category-theory/topic/One.20universe.20as.20a.20foundation.20.26.20friends))