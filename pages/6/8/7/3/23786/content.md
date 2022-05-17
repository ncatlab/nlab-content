
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

# Contents #
* table of contents 
{: toc}



<!--
Hey, page creator! I hope you don't mind, but I made some changes, like using the with-induction version that was in the paper, moving some stuff around a bit, and removing a couple of non-models. I did my best to not delete what you wrote unless it contained an error I couldn't fix. (The model on `2 x N + 1` didn't satisfy axiom 3, for example.)
The source for the previous version is still available if you want to use it for future edits:
https://ncatlab.org/nlab/source/Nelson+arithmetic/9

If someone else sees this after like June 2022, feel free to delete it. I just don't want the possibly-a-new-contributor to think their work wasn't cared about and permanently deleted.
-->



## Idea

An extension of the [[first-order theory]] of [[Peano arithmetic]] as described in [Edward Nelson's paper](#Nelson), by introducing a set of "counting numbers" that we can't use induction on.

## Definition 

Nelson arithmetic ($NA$) is expressed in the language with a constant $0$, unary predicate $\mathcal{C}$, unary function symbol $s$ and binary functions $+$,$\cdot$; it extends [[Peano arithmetic]], which consists of the following [[axioms]]:

1. $\forall_x \neg s(x) = 0$; 

2. $\forall_{x, y} (s(x) = s(y)) \Rightarrow (x = y)$; 

3. $\forall_x x + 0 = x$, 

4. $\forall_{x, y} x + s(y) = s(x+y)$; 

5. $\forall_x x \cdot 0 = 0$; 

6. $\forall_{x, y} x \cdot s(y) = x \cdot y + x$;

7. For any predicate $\varphi$ in first-order logic in the language $0$, $s$, $+$, $\cdot$ (but <i>not</i> containing $\mathcal{C}$), the axiom $\varphi(0) \wedge (\forall_x  \varphi(x) \Rightarrow \varphi(Sx)) \Rightarrow \forall_x \varphi(x)$;

with the two additional axioms regarding $\mathcal{C}$:

8. $\mathcal{C}(0)$; 

9. $\forall_{x} \mathcal{C}(x) \Rightarrow \mathcal{C}(s(x))$;

We may choose to omit the axiom schema (7), in which case we refer to <i>Nelson arithmetic without induction</i> ($NA-Ind$). Without induction, it is not possible to prove that addition or multiplication are commutative or associative. Optionally, we could add the axiom $\forall_x x = 0 \vee \exists_y x = s(y)$ from [[Robinson arithmetic]] so that the resulting theory extends Robinson arithmetic, however we don't in this page.

### Counting numbers

The predicate $\mathcal{C}$ is supposed to refer to "counting numbers", in the familiar intuitive sense that the [[natural numbers]] are supposed to be for counting. Nelson states in his paper that

> It follows (...) that $0$, $S0$, $SS0$, and so forth, are counting numbers. But we cannot prove that all numbers are counting numbers.

And indeed, there are many [[nonstandard model of arithmetic|non-standard models of Nelson arithmetic]] where not every number in the model is a "counting number"/"natural number". Unfortunately, nonstandard models of Peano arithmetic, which Nelson arithmetic extends, are hard to describe, and cannot have computable arithmetic operations.

Nonstandard models of $NA-Ind$ are more common though. If one has any [[ordered ring]] R (meaning $R$ is partially ordered with $+$ monotone, $0 \leq 1$, and the elements $\geq 0$ are closed under multiplication), then the subset $R_{\geq 0} = \{r \in R \mid r \geq 0\}$ is a model of $NA-Ind$, where we may take the predicate $C(a)$ to be $a \in \{0, 1, 1+1, 1+1+1, \cdots\}$ (the image of $\mathbb{N}$ under the unique ring homomorphism $\mathbb{Z} \to R$). For example, the non-negative [[rational numbers]] $\mathbb{Q}_{\geq 0}$ and nonnegative [[real numbers]] $\mathbb{R}_{\geq 0}$ both produce models in this way.

On the other extreme, one could define a model where $\mathcal{C}(a)$ is true for all numbers $a$ in the model, and thus all number trivially are "counting numbers", though in that case the "counting numbers" interpretation of the predicate doesn't make much intuitive sense anymore. 

### Additionable, multiplicable, and exponentiable numbers

We define the unary predicate $\mathcal{A}$, meaning "additionable number", as $\mathcal{A}(x)$ if for all counting numbers $y$, $y + x$ is also a counting number. Similarly, we define the unary predicate $\mathcal{M}$, meaning "multiplicable number", as $\mathcal{M}(x)$ if for all additionable numbers $y$, $y \cdot x$ is also an additionable number. Without induction, we don't know that addition of "additionable numbers" or multiplication of "multiplicable numbers" is associative. 

Let $(-)\uparrow(-)$ denote the exponentiation function; if we aren't using induction, instead suppose that there is a [[binary function]] $(-)\uparrow(-):N \times N \to N$ called "exponentiation" such that

* for all $x \in N$, $x \uparrow 0 = s(0)$ 

* for all $x, y \in N$, $x \uparrow s(y) = x \cdot x \uparrow y$

Nelson states that 

> If we attempt to define “exponentiable number” in the same spirit, we are unable to prove that if $x_1$ and $x_2$ are exponentiable numbers then so is $x_1 \uparrow x_2$. There is a radical difference between addition and multiplication on the one hand and exponentiation, superexponentiation, and so forth, on the other hand. The obstacle is that exponentiation is not associative; for example, $(2 \uparrow 2) \uparrow 3 = 4 \uparrow 3 = 64$ whereas $2 \uparrow (2 \uparrow 3) = 2 \uparrow 8 = 256$. For any specific numeral SSS. . . 0 we can indeed prove that it is an exponentiable number, but we cannot prove that the world of exponentiable numbers is closed under exponentiation.

#### Categorification

The categorification of Nelson's argument would proceed as follows: Suppose we have the subcategory $CountSet \hookrightarrow FinSet$ of the category of finite sets whose cardinality is a counting number. (Here "finite" refers to the internal notion, not the external notion. Although our language only contains numbers, not sets, we can encode this category in $PA$ using a [[skeleton]] of $FinSet$ where objects are (internal) natural numbers and a morphism $m \to n$ is encoded as a natural number less than $n^m$.)

Then we can form a further subcategory $AddSet \hookrightarrow CountSet$, consisting of the objects $A$ such that the coproduct $A + C$ exists in $ContSet$ for all $C$ in $ContSet$. Although $CountSet$ may not have had binary coproducts, $AddSet$ has binary coproducts.

Next, we can form a further subcategory $MultSet \hookrightarrow CountSet$, consisting of the objects $M$ such that the product $M \times A$ exists in $AddSet$ for all $A$ in $AddSet$. Although $AddSet$ may not have had binary products, $MultSet$ has binary products.

Now, we can form a further subcategory $ExpSet \hookrightarrow MultSet$, consisting of the objects $E$ such that the exponent $M^E$ exists in $MultSet$ for all $M$ in $MultSet$ i.e. the [[exponentiable object]]s of $MultSet$. However, in constrast to the previous cases, we <i>cannot</i> prove that $ExpSet$ has exponents (hence can't prove that it's [[cartesian closed]], an [[elementary topos]], a [[Π-pretopos]], etc.).

### Ultrafinitism

The theory $NA$, or a categorification thereof, provides an option to study mathematics using ultrafinitism, by viewing the counting numbers to be the correct notion of natural numbers and the other numbers to be an idealised abstraction. (If one wants to work without these "idealised abstractions", induction would have to be substituted for weaker acceptable axioms.)

Categorifying the current axioms to the category of sets, the counting sets (represented by the sets $S$ in which $\mathcal{C}(S)$ is [[inhabited]]) could not be proven to be [[symmetric monoidal]] with respect to either the [[disjoint union]] or the [[Cartesian product]]. Thus, Nelson's [[CountSet]] forms a framework of mathematics, which is sometimes called "ultrafinite mathematics", that is significantly weaker than [[predicative mathematics|strongly predicative]] [[constructive mathematics|constructive]] [[finite mathematics]]. However, the [[subcategories]] of additionable finite sets $AddSet$ and multiplicable finite sets $MultSet$ can be proven to be symmetric monoidal. 

## Models of Nelson arithmetic

A model of Nelson arithmetic is a model of Peano arithmetic $(N,0,S,+,\cdot)$, equipped with a subset $C \subset N$ such that $0 \in C$ and $a \in C$ implies $S(a) \in C$.

A model of Nelson arithmetic without induction is a [[set]] $N$ with an element $0 \in N$, a function $s:N \to N$, binary operations $(-)+(-):N \times N \to N$ and $(-)\cdot(-):N \times N \to N$, and a predicate $\mathcal{C}:N \to \mathrm{Prop}$, such that the axioms 1-6, 8, 9 above are all satisfied. Explicitly, this means:

* for all $x \in N$, $\neg s(x) = 0$

* for all $x, y \in N$, $s(x) = s(y)$ implies $x = y$

* for all $x \in N$, $x + 0 = x$

* for all $x, y \in N$, $x + s(y) = s(x+y)$

* for all $x \in N$, $x \cdot 0 = 0$

* for all $x, y \in N$, $x \cdot s(y) = x \cdot y + x$

* $\mathcal{C}(0)$

* for all $x \in N$, $\mathcal{C}(x)$ implies $\mathcal{C}(s(x))$; 

A [[homomorphism]] of models of Nelson arithmetic without induction $N$ and $N^{'}$ is a function $f:N \to N^{'}$ such that

* $f(0_N) = 0_{N^{'}}$

* for all $x \in N$, $\mathcal{C}_N(x)$ implies $\mathcal{C}_{N^{'}}(f(x))$

* for all $x \in N$, $f(s_N(x)) = s_{N^{'}}(f(x))$

* for all $x, y \in N$, $f(x +_N y) = f(x) +_{N^{'}} f(y)$

* for all $x, y \in N$, $f(x \cdot_N y) = f(x) \cdot_{N^{'}} f(y)$

Homomorphisms of models of Nelson arithmetic with induction are defined in the same way, but as with $PA$, the notion of [[elementary embedding]]s may be more useful.

The [[category]] of models of Nelson arithmetic without induction in a [[universe]] $\mathcal{U}$ is the category $\mathrm{NelsonArithmetics}_\mathcal{U}$ whose objects $Ob(\mathrm{NelsonArithmetics}_\mathcal{U})$ are the $\mathcal{U}$-small models of Nelson arithmetic, and for any two objects $A \in Ob(\mathrm{NelsonArithmetics}_\mathcal{U})$ and $B \in Ob(\mathrm{NelsonArithmetics}_\mathcal{U})$ the [[morphisms]] $Mor_{\mathrm{NelsonArithmetics}_\mathcal{U}}(A, B)$ are the homomorphisms of models of Nelson arithmetic as defined above. 

This category is an [[accessible category]]. If $\mathcal{U}$ satisfies the [[axiom of finiteness]] (meaning it thinks every set is finite), then (because there are no finite models of $NA-Ind$) the category $\mathrm{NelsonArithmetics}_\mathcal{U}$ is [[empty category|empty]]. 

### Example models

* The set of [[natural numbers]] $\mathbb{N}$ is the standard model of Nelson arithmetic, and is the initial model of Nelson arithmetic in the [[category]] of models of Nelson arithmetic.

* If $R$ is any [[rig]] such that $+1 : R \to R\setminus\{0\}$ is (total and) injective, then $R$ is a model of Nelson arithmetic without induction, where we may take $S(r) = r + 1$ and $\mathcal{C}$ to be any of: $R$, the image of the function $i : \mathbb{N} \to R$ defined by $i(0) = 0$, $i(n+1) = i(n)+1$, or any other subset $C$ with $0 \in C$ and $a \in C \Rightarrow a + 1 \in C$. Examples include:

- The set of non-negative [[rational numbers]] $\mathbb{Q}_{\geq 0}$ with $s(q) \coloneqq q + 1$ and $\mathcal{C}(q)$ for all $q \in \mathbb{Q}_{\geq 0}$ is a model of Nelson arithmetic without induction. 

- The set of non-negative [[real numbers]] $\mathbb{R}_{\geq 0}$ with $s(r) \coloneqq r + 1$ and $\mathcal{C}(r)$ for all $r \in \mathbb{R}_{\geq 0}$ is a model of Nelson arithmetic without induction.

- The subset $P \subset \mathbb{Z}[x]$ of polynomials with leading coefficient nonnegative 

- Any [[free object|free]] [[commutative algebra|commutative $\mathbb{N}$-algebra]] on a generating set $S$ with $s(r) \coloneqq r + 1$ and $\mathcal{C}(r)$ for all $r \in \mathbb{N}[S]$, is a model of Nelson arithmetic without induction. 

* The [[disjoint union]] set $\mathbb{N} + \mathbb{1}$ where $*:\mathbb{1}$ is the unique element of the [[singleton]] cextends the model $\mathbb{N}$ with: 

1. $s(*) = *$

1. $\forall a \in \mathbb{N}. * + a = * = a + *$ and $* + * = *$

1. $\forall a \in \mathbb{N}. * \cdot a = a$

1. $\forall a \in $\mathbb{N} + \mathbb{1}$. a \cdot * = *$

1. $\mathcal{C}(*)$ 

Is a model of Nelson arithmetic without induction. Note that multiplication is not commutative and that $0 \cdot * = *$, so this is not an instance of the previous examples.

* Given any nonstandard model $N$ of Peano arithmetic, and any subset $C \subset N$ with $0 \in C$ and $a \in C \Rightarrow a+1 \in C$, $N$ and $C$ together give a model of Nelson arithemtic.

## Groupoidal categorification

The [[groupoidal categorification]] of Nelson arithmetic without induction is a [[groupoid]] $\mathcal{G}$ with 

* an object $0 \in \mathcal{G}$, 

* a [[functor]] $S:\mathcal{G} \to \mathcal{G}$, 

* a functor $(-)+(-):\mathcal{G} \times \mathcal{G} \to \mathcal{G}$ 

* a functor $(-)\cdot(-):\mathcal{G} \times \mathcal{G} \to \mathcal{G}$

* for all $A \in \mathcal{G}$, a function set $(S(A) \cong 0) \to \emptyset$ from the [[set]] of [[isomorphisms]] $S(A) \cong 0$ to the [[empty set]]

* for all $A, B \in \mathcal{G}$, a function set $(S(A) \cong S(B)) \to (A \cong B)$ from the set of isomorphism $S(A) \cong S(B)$ to the set of isomorphisms $A \cong B$

* for all $A \in \mathcal{G}$, a set of isomorphisms $A + 0 \cong A$

* for all $A, B \in \mathcal{G}$, a set of isomorphisms $A + S(B) \cong S(A+B)$

* for all $A \in \mathcal{G}$, a set of isomorphisms $A \cdot 0 \cong A$

* for all $A, B \in \mathcal{G}$, a set of isomorphisms $A \cdot S(B) \cong A \cdot B + A$

* a [[Set]]-valued functor $\mathcal{C}:\mathcal{G} \to \mathrm{Set}$ 

* an element $p \in \mathcal{C}(0)$ 

* for all $A \in \mathcal{G}$, a function $f_A:\mathcal{C}(A) \to \mathcal{C}(S(A))$ 

## See also

* [[Peano arithmetic]]
* [[finite mathematics]]

## References 

* {#Nelson} [[Edward Nelson]], _Warning Signs of a Possible Collapse of Contemporary Mathematics_ ([pdf](https://web.math.princeton.edu/~nelson/papers/warn.pdf))

