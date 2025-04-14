
>This entry is about a generalized notion of [[topology]]. For the notion of _formal space_ in the sense of [[rational homotopy theory]], see [[formal dg-algebra]].

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Formal topology
* table of contents
{: toc}

## Idea

Formal topology is a programme for doing [[topology]] in a [[finite mathematics|finite]], [[predicative mathematics|predicative]], and [[constructive mathematics|constructive]] fashion.

It is a kind of [[pointless topology]]; in the context of [[classical mathematics]], it reproduces the theory of [[locales]] rather than [[topological spaces]] (although of course one can recover topological spaces from locales).

The basic definitions can be motivated by an attempt to study locales entirely through the [[posites]] that generate them.  However, in order to recover all basic topological notions (particularly those associated with *closed* rather than *open* features) predicatively, we need to add a 'positivity' relation to the 'coverage' relation of sites.


## Definitions

A __formal topology__ or __formal space__ is a [[set]] $S$ together with

*  an [[element]] $\top$ of $S$,
*  a [[binary operation]] $\cap$ on $S$,
*  a [[binary relation]] $\lhd$ between elements of $S$ and [[subsets]] of $S$, and
*  a [[unary relation]] $\Diamond$ on $S$,

such that

1.  $a = b$ whenever $a \lhd \{b\}$ and $b \lhd \{a\}$,
2.  $a \lhd U$ whenever $a \in U$,
3.  $a \lhd V$ whenever $a \lhd U$ and $x \lhd V$ for all $x \in U$,
4.  $a \cap b \lhd U$ whenever $a \lhd U$ or $b \lhd U$,
5.  $a \lhd \{ x \cap y \;|\; x \in U,\; y \in V \}$ whenever $a \lhd U$ and $a \lhd V$,
6.  $a \lhd \{\top\}$,
7.  $\Diamond x$ for some $x \in U$ whenever $\Diamond a$ and $a \lhd U$, and
8.  $a \lhd U$ whenever $a \lhd U$ if $\Diamond a$,

for all $a$, $b$, $U$, and $V$.

We interpret the elements of $S$ as __basic opens__ in the formal space.  We call $\top$ the __[[improper subset|entire space]]__ and $a \cap b$ the __[[intersection]]__ of $a$ and $b$.  We say that $a$ is __covered__ by $U$ or that $U$ is a __[[cover]]__ of $a$ if $a \lhd U$.  We say that $a$ is __positive__ or __[[inhabited subset|inhabited]]__ if $\Diamond a$.  (For a [[topological space]] equipped with a strict [[topological base]] $S$, taking these intepretations literally does in fact define a formal space; see the Examples.)

Some immediate points to notice:

*  If we drop (1), then the hypothesis of (1) defines an [[equivalence relation]] on $S$ which is a [[congruence]] for $\top$, $\cap$, $\lhd$, and $\Diamond$, so that we may simply pass to the [[quotient set]].  In appropriate foundations, we can even allow $S$ to be a [[preset]] originally, then use (1) as a definition of equality.
*  We can prove that $(S,\cap,\top)$ is a bounded [[semilattice]]; if (as the notation suggests) we interpret this as a [[meet]]-semilattice, then $a \leq b$ if and only if $a \lhd \{b\}$.  Conversely, we could require that $(S,\cap,\top)$ be a semilattice originally, then let (1) say that $a \leq b$ whenever $a \lhd \{b\}$.
*  We can prove that $\Diamond a$ holds iff every cover of $a$ is inhabited and that $\Diamond a$ fails iff $a \lhd \empty$.  Accordingly, this predicate is uniquely definable (in two equivalent ways, one impredicative and one nonconstructive) in a classical treatment; only in a treatment that is both predicative and constructive do we need to include it in the axioms.  See [[positivity predicate]].

## Examples

Let $X$ be a [[topological space]], and let $S$ be the collection of [[open subsets]] of $X$.  Let $\top$ be $X$ itself, and let $a \cap b$ be the literal intersection of $a$ and $b$ for $a, b \in S$.  Let $a \lhd U$ if and only $U$ is literally an [[open cover]] of $a$, and let $\Diamond a$ if and only if $a$ is literally inhabited.  Then $(S,\top,\cap,\lhd,\Diamond)$ is a formal topology.

The above example is impredicative (since the collection of open subsets is generally large), but now let $S$ be a [[base for the topology]] of $X$ which is strict in the sense that it is closed under finitary [[intersection]].  Let the other definitions be as before.  Then $(S,\top,\cap,\lhd,\Diamond)$ is a formal topology.

More generally, let $B$ be a [[subbase]] for the topology of $X$, and let $S$ be the [[free monoid]] on $B$, that is the set of [[finite lists]] of elements of $B$ (so this example is not strictly finitist), modulo the [[equivalence relation]] by which two lists are identified if their [[intersections]] are equal.  Let $\top$ be the [[empty list]], let $a \cap b$ be the [[concatenation]] of $a$ and $b$, let $a \lhd U$ if the intersection of $a$ is contained in the [[union]] of the intersections of the elements of $U$, and let $\Diamond a$ if the intersection of $a$ is inhabited.  Then $(S,\top,\cap,\lhd,\Diamond)$ is a formal topology.

Let $X$ be an [[accessible locale]] generated by a [[posite]] whose underlying [[poset]] $S$ is a (meet)-[[semilattice]].  Let $\top$ and $\cap$ be as in the semilattice structure on $S$, and let $a \lhd U$ if $U$ contains a basic cover (in the posite structure on $S$) of $a$.  Then we get a formal topology, defining $\Diamond$ in the unique way.

The last example is not predicative, and this is in part *why* one studies formal topologies instead of sites, if one wishes to be strictly predicative.  (It still needs to be motivated that we want $\Diamond$ at all.)

## In dependent type theory

### Impredicative definition

In [[dependent type theory]], let $(\Omega, \mathrm{El}_\Omega)$ be the [[type of all propositions]], and let the relation $a \in_S A$ for $a:S$ and $A:S \to \Omega$ as

$$a \in_S A \coloneqq \mathrm{El}_\Omega(A(a))$$

The singleton subtype function is a function $\{-\}:S \to (S \to \Omega)$, such that for all elements $a:S$, $p(a):a \in_S \{a\}$, and for all functions $R:S \to (S \to \Omega)$ such that for all elements $a:S$, $p_R(a):a \in_S R(a)$, the type of functions $(b \in_S \{a\}) \to (b \in_S R(a))$ is contractible for all $a:A$ and $b:A$. 

A **formal topology** or **formal space** is a [[type]] $S$ together with

*  an [[element]] $\top:S$,
*  a [[binary operation]] $\cap:S \times S \to S$,
*  a [[binary relation]] $a \lhd A$ between elements of $S$, $a:S$, and [[subtypes]] of $S$, $A:S \to \Omega$, and

such that

1. For all elements $a:S$ and $b:S$, the canonical function 
$$\mathrm{idToFormalTop}(a, b):(a =_S b) \to ((a \lhd \{b\}) \times (b \lhd \{a\}))$$
is an [[equivalence of types]]. 
$$\prod_{a:S} \prod_{b:S} \mathrm{isEquiv}(\mathrm{idToFormalTop}(a, b))$$
2. For all elements $a:S$ and subsets $A:S \to \Omega$, if $a \in_S A$, then $a \lhd A$
$$\prod_{a:S} \prod_{A:S \to \Omega} (a \in_S A) \to (a \lhd A)$$
3.  For all elements $a:S$ and subsets $A:S \to \Omega$ and $B:S \to \Omega$, if $a \lhd A$ and for all elements $x:S$, $x \lhd B$ and $x \in_S A$, then $a \lhd B$
$$\prod_{a:S} \prod_{A:S \to \Omega} \prod_{B:S \to \Omega} \left((a \lhd A) \times \prod_{x:S} (x \in_S A) \times (x \lhd B)\right) \to (a \lhd B)$$
4.  For all elements $a:S$ and $b:S$ and subsets $A:S \to \Omega$, if $a \lhd A$ or $b \lhd A$, then $a \cap b \lhd A$.
$$\prod_{a:S} \prod_{b:S} \prod_{A:S \to \Omega} ((a \lhd A) \times (b \lhd A)) \to (a \cap b \lhd A)$$
5.  For all elements $a:S$ and subsets $A:S \to \Omega$ and $B:S \to \Omega$, if $a \lhd A$ and $a \lhd B$, then
$$a \lhd \sum_{z:S} \prod_{x:S} \prod_{y:S} (x \in_S A) \times (y \in_S B) \times (z =_S x \cap u)$$
$$\prod_{a:S} \prod_{A:S \to \Omega} \prod_{B:S \to \Omega} (a \lhd A) \times (a \lhd B) \to \left(a \lhd \sum_{z:S} \prod_{x:S} \prod_{y:S} (x \in_S A) \times (y \in_S B) \times (z =_S x \cap y)\right)$$
6.  For all elements $a:S$, $a \lhd \{\top\}$,
$$\prod_{a:S} a \lhd \{\top\}$$

One can define the [[positivity predicate]] $\Diamond a$ on $S$ by 

$$\Diamond a \coloneqq \prod_{A:S \to \Omega} (a \lhd A) \to (\exists x:S.x \in_S A)$$

\begin{theorem}
For all elements $a:S$ and subsets $A:S \to \Omega$, if $\Diamond a$ and $a \lhd A$, there exists an element $x:S$ such that $x \in_S A$ and $\Diamond x$. 
$$\prod_{a:S} \prod_{A:S \to \Omega} (\Diamond a) \times (a \lhd A) \to \sum_{x:S} (x \in_S A) \times (\Diamond x)$$
\end{theorem}

\begin{theorem}
For all elements $a:S$ and subsets $A:S \to \Omega$, if $\Diamond a$ implies $a \lhd A$, then $a \lhd A$. 
$$\prod_{a:S} \prod_{A:S \to \Omega} (\Diamond a \to a \lhd A) \to (a \lhd A)$$
\end{theorem}

### Predicative definition

Suppose that the [[dependent type theory]] does not have a [[type of all propositions]], nor any [[type universes]]. This means that subtypes of a type $S$ do not form a type, which is necessary for defining the cover relation, which is inherently a relation between elements of $S$ and subtypes of $S$. However, one can resolve this problem by using a definition of formal topology which does not require a cover relation in its definition, and then [[inductively define]] the cover relation on $S$ as a [[higher inductive type|higher]] [[inductive family]] of [[inductive cover relations]] for every single type in $A$. 

In addition, the positivity predicate $S$ also needs to be separately defined. 

#### Cover relation

Ayberk Tosun in [Tosun 2020](#Tosun20) defined a **formal topology** as a [[poset]] $(A, \leq)$ with families of types $x:A \vdash B(x)$, $x:A, y:B(x) \vdash C(x, y)$ and a dependent function 

$$d:\prod_{x:A} \prod_{y:B(x)} C(x, y) \to A$$

such that

* for all $x:A$, $y:B(x)$, and $z:C(x, y)$, $d(x, y, z) \leq x$

$$\prod_{x:A} \prod_{y:B(x)} \prod_{z:C(x, y)} d(x, y, z) \leq x$$

* for all $x:A$ and $x':A$, $x' \leq x$ implies that for all $y:B(x)$ one can construct $y':B(x')$ such that for all $z:C(x, y)$, one can construct $z':C(x', y')$ such that $d(x', y', z') \leq d(x, y, z)$. 

$$\prod_{x:A} \prod_{x:A'} (a \leq a') \to \prod_{y:B(x)}\sum_{y':B(x')} \prod_{z:C(x, y)} \sum_{z':C(x', y')} d(x', y', z') \leq d(x, y, z)$$

If one has a [[type universe]] $U$, then the locally $U$-small inductive cover relation is given by 

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash I:U \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash p:\exists x:I.e(x) =_A a}{\Gamma \vdash \mathrm{dir}_U(a, I, e, p):a \lhd_U (I, e)}$$

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash I:U \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash b:B(a) \quad \Gamma \vdash f:\prod_{c:C(a, b)} d(a, b, c) \lhd_U (I, e)}{\Gamma \vdash \mathrm{branch}_U(a, I, e, b, f):a \lhd_U (I, e)}$$

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash I:U \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash p:a \lhd_U (I, e) \quad \Gamma \vdash q:a \lhd_U (I, e)}{\Gamma \vdash \mathrm{squash}_U(a, I, e, p, q):p =_{a \lhd_U (I, e)} q}$$

If one doesn't have type universes, then one could use the [[stack semantics]] instead. Given a type $I$, the cover relation for $I$ is a higher inductive type family $a \lhd_I e$ between elements $a:A$ and [[embeddings of types]] $e:I \hookrightarrow A$ generated by the constructors 

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash I \; \mathrm{type} \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash p:\exists x:I.e(x) =_A a}{\Gamma \vdash \mathrm{dir}_I(a, e, p):a \lhd_I e}$$

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash I \; \mathrm{type} \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash b:B(a) \quad \Gamma \vdash f:\prod_{c:C(a, b)} d(a, b, c) \lhd_I e}{\Gamma \vdash \mathrm{branch}_I(a, e, b, f):a \lhd_I e}$$

$$\frac{\Gamma \vdash a:A \quad \Gamma \vdash I \; \mathrm{type} \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash p:a \lhd_I e \quad \Gamma \vdash q:a \lhd_I e}{\Gamma \vdash \mathrm{squash}_I(a, e, p, q):p =_{a \lhd_I e} q}$$

Families of types $x:A \vdash B(x)$ are equivalently functions $B \to A$, so one can express the above definition in terms of single types. A **formal topology** is a poset $(A, \leq)$ with a set $B$, a function $f:B \to A$, a set $C$ with a function $g:C \to B$ and a function $d:C \to A$, such that 

* for all $z:C$, $d(z) \leq g(f(z))$

$$\prod_{z:C} d(z) \leq g(f(z))$$

* for all $x:A$ and $x':A$, if $x \leq x'$, then for all $y:B$, $f(y) =_A x$ implies that one can construct a $y':B$ such that $f(y') =_A x'$ implies that for all $z:C$, $g(z) =_B y$ implies that one can construct a $z':C$ such that $g(z') =_B y'$ implies $d(z') \leq d(z)$.

$$\prod_{x:A} \prod_{x:A'} (a \leq a') \to \prod_{y:B} (f(y) =_A x) \to \sum_{y':B} (f(y') =_A x') \to \prod_{z:C} (g(z) =_B y) \to \sum_{z':C} (g(z') =_B y') \to (d(z') \leq d(z))$$

If one has a [[type universe]] $U$, then the locally $U$-small inductive cover relation is given by 

$$\frac{
\begin{array}{c}
\Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:B \to A \quad \Gamma \vdash g:C \to B \quad \Gamma \vdash d:C \to A \\
\Gamma \vdash a:A \quad \Gamma \vdash I:U \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash p:\exists x:I.e(x) =_A a
\end{array}
}{\Gamma \vdash \mathrm{dir}_U(a, I, e, p):a \lhd_U (I, e)}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:B \to A \quad \Gamma \vdash g:C \to B \quad \Gamma \vdash d:C \to A \\
\Gamma \vdash a:A \quad \Gamma \vdash I:U \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash b:B \quad \Gamma \vdash p:f(b) =_A a \quad \Gamma \vdash h:\prod_{c:C} (g(c) =_B b) \to (d(c) \lhd_U (I, e))
\end{array}
}{\Gamma \vdash \mathrm{branch}_U(a, I, e, b, p, h):a \lhd_U (I, e)}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:B \to A \quad \Gamma \vdash g:C \to B \quad \Gamma \vdash d:C \to A \\
\Gamma \vdash a:A \quad \Gamma \vdash I:U \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash p:a \lhd_U (I, e) \quad \Gamma \vdash q:a \lhd_U (I, e)
\end{array}
}{\Gamma \vdash \mathrm{squash}_U(a, I, e, p, q):p =_{a \lhd_U (I, e)} q}$$

If one doesn't have type universes, then one could use the [[stack semantics]] instead. Given a type $I$, the cover relation for $I$ is a higher inductive type family $a \lhd_I e$ between elements $a:A$ and [[embeddings of types]] $e:I \hookrightarrow A$ generated by the constructors 

$$\frac{
\begin{array}{c}
\Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:B \to A \quad \Gamma \vdash g:C \to B \quad \Gamma \vdash d:C \to A \\
\Gamma \vdash a:A \quad \Gamma \vdash I \; \mathrm{type} \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash p:\exists x:I.e(x) =_A a
\end{array}
}{\Gamma \vdash \mathrm{dir}_I(a, e, p):a \lhd_I e}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:B \to A \quad \Gamma \vdash g:C \to B \quad \Gamma \vdash d:C \to A \\
\Gamma \vdash a:A \quad \Gamma \vdash I \; \mathrm{type} \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash b:B \quad \Gamma \vdash p:f(b) =_A a \quad \Gamma \vdash h:\prod_{c:C} (g(c) =_B b) \to (d(c) \lhd_I e)
\end{array}
}{\Gamma \vdash \mathrm{branch}_I(a, e, b, p, h):a \lhd_I e}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash f:B \to A \quad \Gamma \vdash g:C \to B \quad \Gamma \vdash d:C \to A \\
\Gamma \vdash a:A \quad \Gamma \vdash I \; \mathrm{type} \quad \Gamma \vdash e:I \hookrightarrow A \quad \Gamma \vdash p:a \lhd_I e \quad \Gamma \vdash q:a \lhd_I e
\end{array}
}{\Gamma \vdash \mathrm{squash}_I(a, e, p, q):p =_{a \lhd_I e} q}$$

#### Positivity predicate

Since we cannot quantify over subtypes, we needs to use an [[inference rule]] to define the positivity predicate:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \Diamond x \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A, p:\Diamond x, q:\Diamond x \vdash \mathrm{squash}_\Diamond(x, p, q):p =_{\Diamond x} q}$$

$$\frac{
\begin{array}{c}
\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash I \; \mathrm{type} \quad \Gamma \vdash e:I \hookrightarrow A \\ 
\Gamma \vdash a:A \quad \Gamma \vdash p:(a \lhd_I e) \to (\exists x:I.e(x) =_A a)
\end{array}
}{\Gamma \vdash \mathrm{pos}_{A, I}(e, a, p):\Diamond a}$$

## Related concepts

* [[inductive cover]]

## References

*  [[Mike Fourman]] and Grayson (1982); _Formal Spaces_.  This is the original development, intended as an application of locale theory to logic.

*  [[Giovanni Sambin]] (1987); _Intuitionistic formal spaces_; [pdf](http://www.math.unipd.it/~sambin/txt/ifs87-97.pdf).
   *  This is the probably the main reference on the subject.
   *  Warning: you can ignore the material about [[foundations]] and [[type theory]], but if you do read any of it, the term 'category' means (roughly) [[proper class]]; this was common in type theory in the 1980s.

*  [[Giovanni Sambin]] (2001); _Some points in formal topology_; [pdf](http://www.math.unipd.it/~sambin/txt/SP.pdf).  This has newer results, alternative formulations, etc.

* {#Palmgren05} [[Erik Palmgren]], _From Intuitionistic to Point-Free Topology: On the Foundation of Homotopy Theory_, Logicism, Intuitionism, and Formalism Volume 341 of the series Synthese Library pp 237-253, 2005 ([pdf](http://www2.math.uu.se/~palmgren/homotopy_rev2.pdf))

* [[Nicola Gambino]], [[Peter Schuster]], *Spatiality for formal topologies* Mathematical Structures in Computer Science. 2007;17(1):65-80. ([doi:10.1017/S0960129506005810](https://doi.org/10.1017/S0960129506005810)) 

* {#Tosun20} Ayberk Tosun, _Formal Topology in Univalent Foundations_, ([pdf](https://odr.chalmers.se/handle/20.500.12380/301098), [slides](https://www.cs.bham.ac.uk/~axt978/talks/lab-lunch-formal-topology.pdf))

[[!redirects formal topology]]
[[!redirects formal topologies]]

[[!redirects formal space]]
[[!redirects formal spaces]]
[[!redirects formal topological space]]
[[!redirects formal topological spaces]]
