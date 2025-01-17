
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

\tableofcontents

## Definition
 {#Definition}



The following definition of the degree of a polynomial is formulated vis the *formal [[derivative]]* or *left shift* of a polynomial. 

The idea behind this lies in the traditional conception of polynomials as [[sums]] of [[monomials]], namely of [[multiplication|products]] of non-zero [[scalars]] with powers of an "indeterminate" -- which have an associated exponent because commutative rings are [[power-associative]] in [[multiplication]]. 

Both the derivative and the left shift are functions on polynomials which reduce the exponent of the associated indeterminate by one and take polynomials, relative to the given indeterminate, to zero. Since both operations are also [[linear functions]], they act this way on each monomial summand, which means that after repeatedly taking derivatives or left shifts of polynomials, the result  will eventually become [[zero]]. 

This allows us to define the degree of a polynomial using [[induction]] on the [[natural numbers]] and on [[lists]] of natural numbers, as well as [[composition]] of left shifts, without having to write out long formulae using indices and ellipses everywhere in the definition, and without having to include additional structure with each polynomial $p$ in the form of the [[scalar]] [[coefficients]] of $p$.

### Polynomials in one indeterminate

Given a [[commutative ring]] $R$, the commutative ring of [[polynomials]] $R[x]$ in one indeterminate $x$ is the [[initial object|initial]] commutative ring $R[x]$ with an element $x \in R[x]$ and a [[ring homomorphism]] $h:R \to R[x]$. 

#### Using derivatives

The **formal derivative** $\frac{d (-)}{d x}:R[x] \to R[x]$ is a function which is inductively defined on $R[x]$ by

* Constants go to zero: $\frac{d h(r)}{d x} = 0$ for all $r \in R$
* Indeterminate goes to one: $\frac{d x}{d x} = h(1)$
* Addition preservation: $\frac{d (p + q)}{d x} = \frac{d p}{d x} + \frac{d q}{d x}$ for all $p \in R[x]$ and $q \in R[x]$. 
* Leibniz rule: $\frac{d (p \cdot q)}{d x} = \frac{d q}{d x} \cdot q + p \cdot \frac{d q}{d x}$ for all $p \in R[x]$ and $q \in R[x]$. 

By the universal property of $R[x]$, these constructors are enough to define the derivative on all polynomials $p \in R[x]$. 

Let $\frac{d^{(-)} (-)}{d x^{(-)}}:\mathbb{N} \to (R[X] \to R[X])$ be the function which takes a natural number $n \in \mathbb{N}$ to the $n$-th derivative in the [[function set]] $R[X] \to R[X]$. This is inductively defined on the natural numbers by

* $\frac{d^{0} (-)}{d x^{0}} = \mathrm{id}_{R[X]}$
* $\frac{d^{s(n)} (-)}{d x^{s(n)}} = \frac{d (-)}{d x} \circ \frac{d^{n} (-)}{d x^{n}}$ for all $n \in \mathbb{N}$

If $R$ has [[characteristic zero]], given a non-zero polynomial $p \in R[x]$, the **degree** of $p$ is the maximum [[natural number]] $n$ where the $n$-th iteration of the formal [[derivative]] of $p$ is non-zero:
$$\mathrm{deg}(p) \coloneqq \max_{n \in \mathbb{N}, \frac{d^{n} p}{d x^{n}} \neq 0}(n)$$

The degree of the zero polynomial is undefined, since the formal derivative of the zero polynomial is never non-zero. 

The above definition involving formal derivatives works for commutative rings $R$ with [[characteristic zero]]. However, if $R$ has [[positive characteristic]], the formal derivative is problematic for the degree, because given characteristic $n$, the derivative of the $n$-th power of the indeterminate $x$ is zero. Instead, we have to use something more general, the left shift. 

#### Using left shifts

For every polynomial $p \in R[x]$, $p$ could be represented as the sum of a constant polynomial $c_p$ and the product of the indeterminate $x$ and a polynomial $s_L(p)$ called the **left shift** of $p$: $p = c_p + x \cdot s_L(p)$. Given any two constant polynomials $p = c_p$ and $q = c_q$, by definition, $c_{p \cdot q} = c_p \cdot c_q$. Now, given any two general polynomials $p = c_p + x \cdot s_L(p)$ and $q = c_q + x \cdot s_L(q)$, one then has the following, through the axioms of a [[commutative ring]]:
$$p = x \cdot s_L(p) + c_p, q = x \cdot s_L(q) + c_q$$
$$p \cdot q = x \cdot s_L(p \cdot q) + c_{p \cdot q} = x s_L(p \cdot q) + c_{p} \cdot c_{q}$$
$$p \cdot q = (x \cdot s_L(p) + c_p) \cdot (x \cdot  s_L(q) + c_q) = x^2 \cdot s_L(p) \cdot s_L(q) + x \cdot s_L(p) \cdot c_q + x \cdot s_L(q) \cdot c_p + c_p \cdot c_q$$
$$x \cdot s_L(p \cdot q) = x^2 \cdot s_L(p) \cdot s_L(q) + x \cdot s_L(p) \cdot c_q + x \cdot s_L(q) \cdot c_p$$
$$s_L(p \cdot q) = x \cdot s_L(p) \cdot s_L(q) + s_L(p) \cdot c_q + s_L(q) \cdot c_p$$
$$p - x \cdot s_L(p) = c_p, q - x \cdot s_L(q) = c_q$$
$$s_L(p \cdot q) = x \cdot s_L(p) \cdot s_L(q) + s_L(p) \cdot (q - x \cdot s_L(q)) + s_L(q) \cdot (p - x \cdot  s_L(p)) = s_L(p) \cdot q + s_L(q) \cdot p - x \cdot s_L(p) \cdot s_L(q)$$
Thus, we have the formula for the left shift of the product $p \cdot q$ for any two polynomials $p \in R[x]$ and $q \in R[x]$: 
$$s_L(p \cdot q) = s_L(p) \cdot q + p \cdot s_L(q) - x \cdot s_L(p) \cdot s_L(q)$$
The only difference from the [[Leibniz rule]] for the formal [[derivative]] is the extra term $-x \cdot s_L(p) \cdot s_L(q)$ at the end of the formula. 

This allows us to inductively define on $R[x]$ the formal left shift operator $s_L:R[x] \to R[x]$ in the same manner as the formal derivative, by

* Constants go to zero: $s_L(h(r)) = 0$ for all $r \in R$
* Indeterminate goes to one: $s_L(x) = h(1)$
* Addition preservation: $s_L(p + q) = s_L(p) + s_L(q)$ for all $p:R[x]$ and $q:R[x]$. 
* Left shift product rule: $s_L(p \cdot q) = s_L(p) \cdot q + p \cdot s_L(q) - x \cdot s_L(p) \cdot s_L(q)$ for all $p \in R[x]$ and $q \in R[x]$. 

By the universal property of $R[x]$, these constructors are enough to define the left shift on all polynomials $p \in R[x]$. 

Let $s_L^n:\mathbb{N} \to (R[X] \to R[X])$ be the function which takes a natural number $n \in \mathbb{N}$ to the $n$-th left shift in the [[function set]] $R[X] \to R[X]$. This is inductively defined on the natural numbers by the following constructors

* $s_L^0 = \mathrm{id}_{R[X]}$
* $s_L^{s(n)} = s_L \circ s_L^n$ for all $n \in \mathbb{N}$

In this defintion, $R$ is not required to have [[characteristic zero]]. Given a non-zero polynomial $p \in R[x]$, the **degree** of $p$ is the [[maximum]] [[natural number]] $n$ where the $n$-th iteration of the formal left shift operator of $p$ is non-zero:
$$\mathrm{deg}(p) \coloneqq \max_{n \in \mathbb{N}, s_L^n(p) \neq 0}(n)$$

The degree of the zero polynomial is undefined, since the left shift of the zero polynomial is never non-zero. 

### Polynomials in a finite number of indeterminates

Let us define the standard [[finite set]] $\mathrm{Fin}(n)$ as the set of all [[natural numbers]] less than $n$:

$$\mathrm{Fin}(n) \coloneqq \{i \in \mathbb{N} \vert i \lt n\}$$

Given a natural number less than $n$, $i:\mathrm{Fin}(n)$, let $\mathrm{Fin}(n) \setminus \{i\}$ be the set of natural numbers less than $n$ which are not equal to $i$. 

Given a [[commutative ring]] $R$ with [[characteristic zero]] and a natural number $n$, the commutative ring of [[polynomials]] $R[X]$ is the [[initial object|initial]] [[commutative ring]] $R[X]$ with a function $X:\mathrm{Fin}(n) \to R[X]$ and a [[ring homomorphism]] $h:R \to R[X]$. We write $X_i$ for $X(i)$ throughout. Given a natural number less than $n$, $i \in \mathrm{Fin}(n)$, let $R[X \setminus \{X_i\}]$ be the polynomial [[subring]] of $R[X]$ whose indeterminates do not include $X_i$, with monomorphism $m:R[X \setminus \{X_i\}] \hookrightarrow R[X]$. 

Let $\mathrm{Fin}(n)^*$ be the [[free monoid]] on the set of natural numbers less than $n$. Every [[free monoid]] $\mathrm{Fin}(n)^*$ has a length function $\mathrm{len}:\mathrm{Fin}(n)^* \to \mathbb{N}$ which returns the number of elements in a list $a \in \mathrm{Fin}(n)^*$, inductively defined by the following constructors

* Monoidal unit preservation: $\mathrm{len}(\epsilon) = 0$
* Monoidal product preservation: $\mathrm{len}(a b) = \mathrm{len}(a) + \mathrm{len}(b)$ for all $a \in \mathrm{Fin}(n)^*$ and $b \in \mathrm{Fin}(n)^*$
* Generators have length 1: $\mathrm{len}(i) = 1$ for all $i \in \mathrm{Fin}(n)$

#### With partial derivatives

The **formal partial derivative** $\frac{\partial(-)}{\partial X_{(-)}}:\mathrm{Fin}(n) \times R[X] \to R[X]$ is inductively defined by 

* Constants relative to the indeterminant go to zero: $\frac{\partial h(r)}{\partial X_i} = 0$ for all $i \in \mathrm{Fin}(n)$ and $r \in R[X \setminus \{X_i\}]$
* Indeterminates go to one: $\frac{\partial X_i}{\partial X_i} = 1$ for all $i \in \mathrm{Fin}(n)$
* Addition preservation: $\frac{\partial (P + Q)}{\partial X_i} = \frac{\partial P}{\partial X_i} + \frac{\partial Q}{\partial X_i}$ for all $i \in \mathrm{Fin}(n)$, $P \in R[X]$ and $Q \in R[X]$. 
* Leibniz rule: $\frac{\partial (P \cdot Q)}{\partial X_i} = \frac{\partial P}{\partial X_i} \cdot Q + P \cdot \frac{\partial Q}{\partial X_i}$ for all $i \in \mathrm{Fin}(n)$, $P \in R[X]$ and $Q \in R[X]$. 

By the universal property of $R[X]$, these constructors are enough to define the partial derivatives on all polynomials $P \in R[X]$. 

Let $d:\mathrm{Fin}(n)^* \to (R[X] \to R[X])$ be the [[monoid homomorphism]] which takes a list $a \in \mathrm{Fin}(n)^*$ of natural numbers less than $n$, to the composition of formal partial derivatives 
$$d(a) \coloneqq \frac{\partial^{\mathrm{len}(a)} (-)}{\partial X_{a_0} \partial X_{a_1} \partial X_{a_2} \ldots} \coloneqq \frac{\partial (-)}{\partial X_{a_0}} \circ \frac{\partial (-)}{\partial X_{a_1}} \circ \frac{\partial (-)}{\partial X_{a_2}} \circ \ldots$$ 
in the [[function set]] $R[X] \to R[X]$. This is inductively defined by the following constructors

* Monoidal unit preservation: $d(\epsilon) = \mathrm{id}_{R[X]}$
* Monoidal product preservation: $d(a b) = d(a) \circ d(b)$ for all $a \in \mathrm{Fin}(n)^*$ and $b \in \mathrm{Fin}(n)^*$
* Generators to partial derivatives: $d(i) = \frac{\partial (-)}{\partial X_i}$ for all $i \in \mathrm{Fin}(n)$

If $R$ has [[characteristic zero]], given a non-zero polynomial $P \in R[x]$, the **degree** of $P$ is the maximum length of all lists $a \in \mathrm{Fin}(n)^*$ of natural numbers less than $n$ such that the evaluation of $d(a)$ at $P$ is non-zero
$$\mathrm{deg}(P) \coloneqq \max_{a \in \mathrm{Fin}(n)^*, d(a)(P) \neq 0}(\mathrm{len}(a))$$ 
The degree of the zero polynomial is undefined, since any composition of partial derivatives evaluated at the zero polynomial is never non-zero. 

The above definition involving formal partial derivatives works for commutative rings $R$ with [[characteristic zero]]. However, if $R$ has [[positive characteristic]], the formal derivative is problematic for the degree, because given characteristic $p$, the derivative of the $p$-th power of any indeterminate $X_i$ for natural number less than $n$, $i \in \mathrm{Fin}(n)$, is zero. Instead, we have to use something more general, partial left shifts. 

#### With partial left shifts

The **formal partial left shift operator** $s_{\partial L}:\mathrm{Fin}(n) \times R[X] \to R[X]$ is inductively defined by 

* Constants relative to the indeterminant go to zero: $s_{\partial L}(i, r) = 0$ for all $i \in \mathrm{Fin}(n)$ and $r \in R[X \setminus \{X_i\}]$
* Indeterminates go to one: $s_{\partial L}(i, X_i) = 1$ for all $i \in \mathrm{Fin}(n)$
* Addition preservation: $s_{\partial L}(i, P + Q) = s_{\partial L}(i, P) + s_{\partial L}(i, Q)$ for all $i \in \mathrm{Fin}(n)$, $P \in R[X]$ and $Q \in R[X]$. 
* Left shift product rule: $s_{\partial L}(i, P \cdot Q) = s_{\partial L}(i, P) \cdot Q + P \cdot s_{\partial L}(i, Q) - X_i \cdot s_{\partial L}(i, P) \cdot s_{\partial L}(i, Q)$ for all $i \in \mathrm{Fin}(n)$, $p \in R[x]$ and $q \in R[x]$. 

By the universal property of $R[X]$, these constructors are enough to define the partial left shifts on all polynomials $P \in R[X]$. 

Let $S:\mathrm{Fin}(n)^* \to (R[X] \to R[X])$ be the [[monoid homomorphism]] which takes a list $a\in \mathrm{Fin}(n)^*$ of natural numbers less than $n$, to the composition of formal partial left shifts 
$$S(a) \coloneqq s_{\partial L}(a_0, -) \circ s_{\partial L}(a_1, -) \circ s_{\partial L}(a_2, -) \circ \ldots$$ 
in the [[function set]] $R[X] \to R[X]$. This is inductively defined by the following constructors

* Monoidal unit preservation: $S(\epsilon) = \mathrm{id}_{R[X]}$
* Monoidal product preservation: $S(a b) = S(a) \circ S(b)$ for all $a \in \mathrm{Fin}(n)^*$ and $b \in \mathrm{Fin}(n)^*$
* Generators to partial left shifts $S(i) = s_{\partial L}(i, -)$ for all $i \in \mathrm{Fin}(n)$

Given a non-zero polynomial $P \in R[x]$, the **degree** of $P$ is the maximum length of all lists $a \in \mathrm{Fin}(n)^*$ of natural numbers less than $n$ such that the evaluation of $S(a)$ at $P$ is non-zero
$$\mathrm{deg}(P) \coloneqq \max_{a \in \mathrm{Fin}(n)^*, S(a)(P) \neq 0}(\mathrm{len}(a))$$ 
The degree of the zero polynomial is undefined, since any composition of partial derivatives evaluated at the zero polynomial is never non-zero. 

## Homogeneous polynomials

...

Given a polynomial $p \in R[x]$ in one indeterminate, it is said to be an **homogeneous polynomial** of degree $n$ if $\frac{d p}{d x}.x = n.p$ (see the [[homogeneous polynomial|Euler identity]]).

Given a polynomial $p \in R[X]$ in a finite number of indeterminates, it is said to be an homogeneous polynomial of degree $n$ if $\underset{i \in \mathrm{Fin}(n)}{\sum} \frac{\partial p}{\partial X_i}.X_i = n.p$.

One could also define a polynomial $p \in R[X]$ to be homogeneous of degree $n$ with respect to $i \in \mathrm{Fin}(n)$ if $\frac{\partial p}{\partial X_i}.X_i = n.p$. It is equivalent to the fact that $p$ can be written under the form $p=X_i^{n}.q$ where $q \in R[X]$ is such that $\frac{\partial p}{\partial X_i} = 0$.

## In constructive mathematics

In [[constructive mathematics]], where [[excluded middle]] does not hold, the above definition is correct only if the ring $R$ has [[decidable equality]]. In more general circumstances, one has to assume that the ring $R$ and thus the polynomial ring $R[X]$ is a set with a [[tight apartness relation]] $\#$, and replace all instances of "non-zero" $p \neq 0$ with instances of "apart from zero" $p \# 0$. (In [[classical mathematics]], every set $R$ has a [[tight apartness relation]] $x \neq y$ given by the [[denial negation]] of [[equality]].) For example, the degree function on the [[Dedekind real numbers]] is only defined on polynomials with at least one coefficient whose [[absolute value]] is greater than zero. 

## See also

* [[polynomial]]
* [[degree]]

[[!redirects polynomial degree]]