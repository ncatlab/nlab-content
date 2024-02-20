
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

Book HoTT is the [[dependent type theory]] which appears in the [[HoTT book]]. It is notable in that, unlike most other dependent type theories which have been formally written in [[natural deduction]], it does not have a separate [[type]] [[judgment]]. Instead, it only has term judgments, and an infinite sequence of [[Russell universes]] indexed by a [[natural numbers]] primitive. Types are represented by terms of a Russell universe. 

However, when formally defining the natural numbers primitive, in order to ensure that the dependent type theory does not have a separate type judgment, one has to define the natural numbers primitive in a separate [[layer]], meaning that formal book HoTT is a [[layered type theory]]. There are many different ways to define the layer containing the natural numbers primitive: 

* One could define the [[first-order theory]] of a [[category]] with [[finite products]] and a parameterized [[natural numbers object]], and use the [[hom-set]] $\mathrm{Hom}(1, \mathbb{N})$ to index the [[Russell universes]]. 
* One could define the simply typed first order theory of [[ZFC]], and use the von Neumann natural numbers or the Zermelo natural numbers to index the Russell universes. 
* One could define the simply typed first order theory of [[Peano arithmetic]], and use the natural numbers in Peano arithmetic to index the Russell universes. 
* One could define a separate [[dependent type theory]] with a [[natural numbers type]], such as the [[extensional type theory]] in [[two-level type theory]], and use the natural numbers type $\mathbb{N}$ to index the Russell universes. 

## Formal presentation

The presentation of formal book HoTT we have chosen is a  type theory with [[judgments]] for contexts

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

* Formation rules for dependent product types:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma, x:A \vdash B:U_i}{\Gamma \vdash \prod_{x:A} B(x):U_i}$$

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

There is another version of equality in book HoTT, called [[typal equality]]. Typal equality is represented by the [[identity type]]. 

* Formation rule for identity types:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A}{\Gamma \vdash a =_A b:U_i}$$

* Introduction rule for identity types:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{refl}_A(a) : a =_A a}$$

* Elimination rule for identity types:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, x:A, y:A, p:a =_A b \vdash C:U_i \quad \Gamma, z:A \vdash t:C[z/a, z/b, \mathrm{refl}_A(z)/p] \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash q:a =_A b}{\Gamma \vdash J(x,y,p.C, z.t, a, b, q):C[a, b, q/x, y, p]}$$

* Computation rules for identity types:
$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma, x:A, y:A, p:a =_A b \vdash C:U_i \quad \Gamma, z:A \vdash t:C[z/a, z/b, \mathrm{refl}_A(z)/p] \quad \Gamma \vdash a:A}{\Gamma \vdash J(x.y.p.C, z.t, a, a, \mathrm{refl}(a)) \equiv t:C[a, a, \mathrm{refl}_A(a)/x, y, p]}$$

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

The [[univalence axiom]] then states that $\mathrm{idtoequiv}_{A, B}$ is an equivalence for all external natural numbers $i \in \mathcal{N}$ and types $A:U_i$ and $B:U_i$:

$$\frac{\Gamma \vdash i \; \mathrm{level} \quad \Gamma \vdash A:U_i \quad \Gamma \vdash B:U_i}{\Gamma \vdash \mathrm{ua}_{U_i}(A, B):\mathrm{isEquiv}_{A =_{U_i} B, A \simeq B}(\mathrm{idtoequiv}_{A, B})}$$ 

## Related pages

Some of the kinds of inductive definitions mentioned in the HoTT Book are:

* [[W-types]]
* [[inductive families]]
* [[mutually inductive types]]
* [[inductive-inductive types]]
* [[inductive-recursive types]]
* [[higher inductive types]]
* [[higher inductive-inductive types]]
* [[higher inductive-recursive types]]

## See also

* [[dependent type theory]]

* [[homotopy type theory]]

* [[univalent type theory]]

## References

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

[[!redirects book HoTT]]
[[!redirects book homotopy type theory]]
[[!redirects Book homotopy type theory]]
[[!redirects Book Homotopy Type Theory]]
