
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition 

An [[ordered field]] $F$ is **real closed** if it satisfies the following two properties: 

* Any non-negative element $x \geq 0$ in $F$ has a [[square root]] in $F$; 

* Any odd-degree [[polynomial function]] with coefficients in $F$ has a root in $F$. 

Notice that the order on a real closed field is definable from the algebraic structure: $x \leq y$ if and only if $\exists_z x + z^2 = y$. (In particular, there is a _unique_ ordering on a real closed field, defined by taking the positive elements to be precisely the nonzero squares.) In fact, the [[category]] of real closed fields and order-preserving field homomorphisms is a [[full subcategory]] of the category [[Field]] of [[fields]] and field homomorphisms. 


## Properties 

Real closed fields can be equivalently characterized by any of the following properties: 

1. $F$ is not [[algebraically closed field|algebraically closed]], but some finite [[field extension|extension]] is. This extension is necessarily $F[\sqrt{-1}]$. See also [[fundamental theorem of algebra]]. 

2. As a field, $F$ is [[elementary equivalence|elementarily equivalent]] to the field of real numbers. 

3. The [[intermediate value theorem]] holds for all [[polynomial functions]] with coefficients in $F$. 

4. $F$ is an ordered field that has no ordered algebraic extension. 

In fact, there is a [[completion]] of any [[ordered field]] to a real closed field, in the following sense: 

+-- {: .un_theorem}
###### Theorem

The full inclusion of the category of real closed fields and field homomorphisms to the category of ordered fields and ordered field homomorphisms has a left adjoint. 
=-- 

+-- {: .proof} 
###### Proof

We give a brief sketch of proof, referring to Lang's _Algebra_ ($3^{rd}$ edition), section IX.2, for more details. 

First, for each ordered field $F$, there is a real closed algebraic extension $F \to R$ that is order-preserving (theorem 2.11). This is called a **real closure** of the ordered field $F$. 

Second, any two real closures of $F$ are uniquely isomorphic (theorem 2.9); in fact, the proof shows there is at most one order-preserving homomorphism over $F$ between any two real closures. Therefore we may speak of _the_ real closure of $F$, which we denote as $\widebar{F}$. 

Finally, let $F \to R$ be any order-preserving field homomorphism to a real closed field $R$. We must show that $F \to R$ extends uniquely to a homomorphism $i: \widebar{F} \to R$. Any such homomorphism $i$ must factor through the subfield $R' \hookrightarrow R$ consisting of elements $\alpha \in R$ that are algebraic over $F$, since $\widebar{F}$ is algebraic over $F$. But this subfield is also real closed. Therefore, by the preceding paragraph, there is at most one homomorphism $\widebar{F} \to R'$ extending $F \to R'$, and the proof is complete. 
=--


## Examples 

1. The [[real number]]s form a real closed field. 

2. Real [[algebraic number]]s form a real closed field, which is the real closure of the ordered field of [[rational numbers]]. 

3. A field of nonstandard real numbers (as in Robinson [[nonstandard analysis]]) is real closed. 

4. [[surreal number|Surreal numbers]] form a (large) real closed field. 

5. If $F$ is real closed, then the field of [[Puiseux series]] over $F$ is also real closed. 

6. More generally, given a real closed field $F$, the field of [[Hahn series]] over $F$ with [[valuation ring|value group]] $G$ (a linearly ordered group) is real closed provided that $G$ is [[divisible group|divisible]].

7. Any [[o-minimal structure|o-minimal]] ordered ring structure $R$ is a real closed field. 

8. Given an o-minimal ordered ring $R$, the field of [[germ]]s at infinity of definable functions $R \to R$ in any o-minimal expansion of $(R, 0, 1, +, -, \cdot, \lt)$ is real closed. (By "germ at infinity", we mean an equivalence class of functions for which $f \equiv g$ if and only if $f(x) = g(x)$ for all sufficiently large $x$.)

## Infinites and infinitesimals 

Each real closed field $R$ contains a [[valuation ring|valuation]] subring $B \hookrightarrow R$ consisting of the "bounded" or archimedean elements, i.e., elements $x \in R$ such that $-n \leq x \leq n$ for some integer multiple $n$ of the identity. An element in the complement of $B$ is an **infinite** element of $R$, and the reciprocal of an infinite element is an **infinitesimal** element. The field of fractions of $B$ is clearly $R$. 

We remark that any real closed field contains a copy of the field of real [[algebraic numbers]], which as before we denote by $\widebar{\mathbb{Q}}$ (not to be confused with the algebraic closure of $\mathbb{Q}$). Each of the elements of $\widebar{\mathbb{Q}}$ is archimedean. 

Let $B^\ast$ be the group of units of $B$. The quotient $R^\ast/B^\ast$ is the **value group** of $R$. It can be viewed as the "group of orders of infinities and infinitesimals" of $R$. If $R$ is real closed, then the value group is a linearly ordered [[divisible group]] (divisible because we can take $n^{th}$ roots of positive elements in $R$). The structure of the value group as ordered group is an important invariant of the real closed field. 

In the other direction, to each ordered divisible abelian group $G$, there exists a real closed field having $G$ as its value group. For example, one may form the [[Hahn series]] over $\widebar{\mathbb{Q}}$ with value group $G$. 

## In constructive mathematics

In [[constructive mathematics]], in order to define an odd degree polynomial, one has to use the [[tight apartness relation]] $x \# y$ or $x \neq y$ of an [[ordered field]], defined as $x \lt y \vee x \gt y$, instead of [[denial inequality]] $\neg (x = y)$, which is not normally related to the [[order]] of the ordered field. A polynomial $p = \sum_{i \leq n} a_n z^n$ has an odd degree if $n$ is odd and $a_n$ is apart from zero. 

In addition, the original definition of an ordered field bifurcates into two. One has to decide whether to use [[mere proposition|mere]] existence of a [[root]] in the sense of traditional [[first-order logic]] or constructive existence in the sense of the [[BHK interpretation]] in the formulation of a real closed fields: 

\begin{proposition}
An ordered field $F$ is a **real closed field** if for every non-negative element $x \geq 0$ in $F$ there exists a [[square root]] in $F$, and for any odd-degree [[polynomial function]] with coefficients in $F$ there exists a root in $F$. 
\end{proposition}

\begin{proposition}
An ordered field $F$ is a **real closed field** if for every non-negative element $x \geq 0$ in $F$ there exists a [[square root]] in $F$, and for any odd-degree [[polynomial function]] with coefficients in $F$ there exists a root in $F$. 
\end{proposition}

Note here the theorems do not consider the notion of constructing a specified square root in the [[BHK interpretation]] for non-negative elements of $F$, or the stronger notion of the squaring function $x \mapsto x^2$ having a [[principal square root]] on the non-negative elements of $F$. This is because the two notions are equivalent to each other for ordered fields $F$:

\begin{theorem}
The conditions that "for every non-negative element $x \geq 0$ in $F$ there exists a [[square root]] in $F$" and "$F$ has a [[principal square root]] [[partial function]] defined on the non-negative elements of $F$" are equivalent to each other. 
\end{theorem}

\begin{proof}
The squaring function $x \mapsto x^2$ is an injection on non-negative elements of $F$, and the first condition says that the squaring function $x \mapsto x^2$ is surjective on non-negative elements of $F$ and the second condition says that the squaring function $x \mapsto x^2$ is bijective on non-negative elements of $F$; these are equivalent conditions for injective functions. 
\end{proof}

In addition, the various equivalent definitions and properties of an ordered field are no longer provably equivalent in constructive mathematics: 

1. For every non-negative element $x \geq 0$ in $F$ there exists a [[square root]] in $F$, and for any odd-degree [[polynomial function]] with coefficients in $F$ there exists a root in $F$. 

1. For every non-negative element $x \geq 0$ in $F$ there exists a [[square root]] in $F$, and for any odd-degree [[polynomial function]] with coefficients in $F$ one can construct a specified root in $F$. 

1. For every non-negative element $x \geq 0$ in $F$ there exists a [[square root]] in $F$, and any odd-degree [[polynomial function]] $p(z)$ with degree $n$ coefficients in $F$ can be factored into a [[linear function]] $c_1 z + c_0$ with $c_0$ and $c_1$ in $F$ and a monic polynomial function $q(z)$ of degree $n - 1$ with coefficients in $F$, $p(z) = (c_1 z + c_0) q(z)$. 

1. The [[intermediate value theorem]] holds for all [[polynomial functions]] with coefficients in $F$. 

1. $F$ is an ordered field that has no ordered algebraic extension. 

1. $F$ is not [[algebraically closed field|algebraically closed]], but the finite [[field extension|extension]] $F[\sqrt{-1}]$ is. 

1. As a field, $F$ is [[elementary equivalence|elementarily equivalent]] to the field of real numbers. 

As a result, the any one of these can be used in the definition of a real closed field. 

### Real closure of the real numbers
{#OfConstructiveReals}

For any field of [[real numbers]], it is provable that the real numbers are a real closed field in the sense that for all non-negative real numbers there exist a [[real square root]], and for every odd degree polynomial functions on the real numbers, there exist a root of the polynomial function. However, the real numbers themselves are not provably a real closed field in the sense that for any odd-degree polynomial function with coefficients in the reals one can construct a specified root in the reals. To show that this is the case, we turn to reframing the definitions of a real closed field in terms of surjectivity and having [[right inverses]] of real polynomial functions so that one can show that the equivalence of the definitions is equivalent to a weak form of choice. 

Let $p(z) = \sum_{i \leq n} a_n z^n$ be a polynomial function on the real numbers. Every such $p(z)$ can be written as the sum of a constant $a_0$ and a polynomial function $q(z) = \sum_{1 \leq i \leq n} a_n z^n$ with a [[fixed point]] at zero. As a result, the statement that there exists a real number $z$ such that $p(z) = 0$ is equivalently the statement that there exists a real number $z$ such that $q(z) = b$, where $b = -a_0$. Thus, one can rewrite one of the conditions in the first definition of a real closed field as:

\begin{definition}
Given a real number $b$ and an odd degree polynomial function $q(z)$ on the real numbers such that $q(0) = 0$, there exists a real number $c$ such that $q(c) = b$. 
\end{definition}

Or equivalently

\begin{theorem}
Every odd degree polynomial function $q(z)$ on the complex numbers such that $q(0) = 0$ is [[surjective]]. 
\end{theorem}

One can do the same analysis with the [[BHK interpretation]] of the definition of a real closed field, the statement that one can construct a specified real number $z$ such that $p(z) = 0$ is equivalently the statement that one can construct a specified real number $z$ such that $q(z) = b$, where $b = -a_0$. Thus, one can rewrite the fundamental theorem of algebra as follows:

\begin{theorem}
Given a real number $b$ and a odd degree polynomial function $q(z)$ on the real numbers such that $q(0) = 0$, one can construct a specified real number $c$ such that $q(c) = b$. 
\end{theorem}

Or equivalently

\begin{theorem}
Every odd degree polynomial function $q(z)$ on the real numbers such that $q(0) = 0$ has a [[section]]. 
\end{theorem}

Thus, the gap between proving that the real numbers are a real closed field using [[mere proposition|mere]] existence and that the real numbers are real closed field using constructive existence is precisely this weak version of the [[axiom of choice]]:

\begin{proposition}
Every [[surjective]] [[polynomial function]] on the [[real numbers]] with odd degree and a [[fixed point]] at zero has a [[section]]. 
\end{proposition}

In particular, consider the map $z \mapsto z^3 - z$. This map is surjective on the real numbers, but cannot be proven to have a section. In fact, in certain [[topoi]], such as [[sheaves]] over $\mathbb{R}$, one can prove that there are no such sections of $z \mapsto z^3 - z$ on the real numbers, since any since any section on $z \mapsto z^3 - z$, if it exists, has to be discontinuous somewhere in the closed interval $[-1, 1]$, and in those topoi all functions on the real numbers are continuous. 

The unprovability of this weak version of choice in neutral constructive mathematics also implies that one cannot factor every odd degree real polynomial function $p(z)$ of degree $n$ into a monomial $c_1 z + c_0$ with real numbers $c_0$ and $c_1$ and a monic real polynomial function $q(z)$ of degree $n - 1$, $p(z) = (c_1 z + c_0) q(z)$, since one would need to first construct the specified real root $-\frac{c_0}{c_1}$ of $p(z)$, which is required to show that the [[complex numbers]] are an [[algebraically closed field]]. 

## Related concepts

* [[algebraic closure]]

* [[fundamental theorem of algebra]]

* [Euclidean geometry -- Tarski's axioms](Euclidean+geometry#TarskiAxioms)

## References 

* [[Serge Lang]]: _Algebra_, 3rd ed. Springer (2002) &lbrack;[doi:10.1007/978-1-4613-0041-0](https://doi.org/10.1007/978-1-4613-0041-0)&rbrack;

* David Marker, _Notes on Real Algebra_ [(link)](http://www.math.uic.edu/~marker/orsay/real_algebra.pdf) 

[[!redirects real closed field]]
[[!redirects real closed fields]]
[[!redirects real-closed field]]
[[!redirects real-closed fields]]

[[!redirects real closure]]