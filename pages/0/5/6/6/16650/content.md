
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents # 
* table of contents 
{:toc} 

## Idea 

A Euclidean domain is an integral domain which admits a form of the Euclidean quotient-and-remainder algorithm familiar from school mathematics, as well as a form of the extended Euclidean algorithm for calculating the [[greatest common divisor]] and [[Bézout coefficients]] in a [[Bézout domain]]. 

## Definition 

A **Euclidean domain** is an [[integral domain]] $A$ for which there exists a function $d: A \setminus \{0\} \to \mathbb{N}$ to the [[natural numbers]], often called a *degree function*, such that given $f, g \in A$ with $g \neq 0$, there exist $q, r \in A$ such that $f = q \cdot g + r$ and either $r = 0$ or $d(r) \lt d(g)$. (One may harmlessly stipulate that $d(0) = 0$; what to do with the zero element varies from author to author.) There is no uniqueness requirement for $q, r$. 

One could posit, instead of the [[property]] that for all $f \in A$ and $g \in A \setminus \{0\}$, there exist $q, r \in A$ such that $f = q \cdot g + r$ and either $r = 0$ or $d(r) \lt d(g)$; that the integral domain has the [[structure]] of a function $(-)\div(-):A \times A \setminus \{0\} \to A$ called the *[[division]] function*, and a function $(-)\ \%\ (-):A \times A \setminus \{0\} \to A$ called the *remainder function*, such that for all $f \in A$ and $g \in A \setminus \{0\}$, $f = (f \div g) \cdot g + (f\ \%\ g)$ and either $f\ \%\ g = 0$ or $d(f\ \%\ g) \lt d(g)$. There might be multiple such division and remainder functions for the integral domain $A$. 

Some authors also add the requirement that $d(a) \leq d(a b)$ for all nonzero $a, b$. There is no loss of generality in assuming it; every Euclidean domain admits such a degree function $d'$, defining $d'(a) = \min \{d(a b): b \in A, b \neq 0\}$. We'll use it freely below, if and when we need to. 

### In constructive mathematics ###

In constructive mathematics, there are different types of integral domains, yielding different types of Euclidean domains: the degree function, division, function, and remainder function are no longer valued in $A \setminus \{0\}$ in one variable, but in $\{x \in A \vert x \neq 0\}$, $\{x \in A \vert x \# 0\}$, or some other definition, depending on what the base [[integral domain]] ends up being (classical, Heyting, discrete, residue, et cetera). 

The definition of the Euclidean domain further bifurcates in [[constructive mathematics]] due to the disjunctive condition above. These statements, which are equivalent in the presence of [[excluded middle]], include: 

* $(r = 0) \vee (d(r) \lt d(g))$
* $\not((r \neq 0) \wedge (d(r) \geq d(g)))$ 
* $(d(r) \geq d(g)) \to (r = 0)$

or equivalently, 

* $(f\ \%\ g = 0) \vee (d(f\ \%\ g) \lt d(g))$ 
* $\not((f\ \%\ g \neq 0) \wedge (d(f\ \%\ g) \geq d(g))$ 
* $(d(f\ \%\ g) \geq d(g)) \to (f\ \%\ g = 0)$ 

## Examples 

* The (rational) [[integers]] $\mathbb{Z}$. 

* Any field (trivially). 

* The ring of [[polynomials]] $k[x]$ over a [[discrete field]] $k$, using the ordinary [[polynomial degree]]. 

* On the other hand, if $k$ is a [[Heyting field]] which is not a discrete field, not every polynomial in $k[x]$ apart from zero can be proven to have a well-defined degree, and so is not an [[Euclidean domain]]. 

* The real polynomial ring $\mathbb{R}[x]$ is only an Euclidean domain in the presence of the [[limited principle of omniscience]], since only in that case does it have [[decidable equality]]. 

* Any [[valuation ring|discrete valuation ring]]: letting $\pi$ be a generator of the maximal ideal, put $d(x) = n$ where $x = u \pi^n$, with $u$ a unit. 

* The [[Gaussian integers]] $\mathbb{Z}[i]$, with $d(a + b i) = a^2 + b^2$ (the norm). 

* The [[Eisenstein integers]] $\mathbb{Z}[\omega]$, where $\omega$ is a primitive cube [[root of unity]], with $d(a + b \omega) = a^2 - a b + b^2$ (the norm). 

## Properties 

+-- {: .num_prop} 
###### Proposition 
A Euclidean domain is a [[Bézout domain]]. 
=-- 

+-- {: .proof} 
###### Proof 
Let $I \subseteq A$ be a nonzero finitely generated ideal, and suppose $d(g)$ is the minimum degree taken over all nonzero $g \in I$. For such a $g$ and any $f \in I$, we may write $f = q g + r$ where either $r = 0$ or $d(r) \lt d(g)$ (which is impossible since $r \in I$ and $d(g)$ is minimal). So $r = 0$ it is, and thus $I = (g)$. 
=-- 

This proof uses the [[well-order|well-orderedness]] of $\mathbb{N}$. It also suggests the practical procedure known as the **extended Euclidean algorithm**: given two elements $a, b$ in a Euclidean domain $A$, this algorithm provides a generator $d$ of the ideal $I = (a) + (b)$, called a [[greatest common divisor]] of $a, b$, as follows. One constructs a sequence of pairs $(a_n, b_n)$ of elements of $I$, with $(a_0, b_0) = (a, b)$, and $(a_{n+1}, b_{n+1}) = (b_n, r_n)$ where $a_n = b_n q_n + r_n$ for some choice of $q_n, r_n$ such that $d(r_n) \lt d(b_n)$ and $r_n \neq 0$. If no such choices for $q_n, r_n$ exist, then the sequence terminates at $(a_n, b_n)$, and $b_n$ generates $I$, i.e, $(b_n) = I$. Notice that the sequence terminates after finitely many steps since we cannot have an [[infinite descent]] of natural numbers 

$$d(r_0) \gt d(r_1) \gt \ldots,$$ 
again by well-orderedness of $\mathbb{N}$. 

The proof that this algorithm produces a gcd consists in the observation that at each step we have 

$$(a_{n+1}) + (b_{n+1}) = (a_n) + (b_n),$$ 

and that from the definition of Euclidean domain, the only reason why the sequence would terminate at $(a_n, b_n)$ is that $a_n = b_n q_n + 0$ for some $q_n$, and in that case $(a_n) + (b_n) = (b_n)$. 

## Generalisations

Euclidean domains could be generalised to the case where the structure is only a [[rig]] instead of a ring; these objects could be called __Euclidean cancellative rigs__. 

## See also 

* [[integral domain]]
* [[GCD domain]]
* [[Bézout domain]]
* [[field]]
* [[Euclidean ring]]

## References 

See also:

* Wikipedia, _[Euclidean algorithm](https://en.wikipedia.org/wiki/Euclidean_algorithm)

* Wikipedia, _[extended Euclidean algorithm](https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm)

[[!redirects Euclidean domains]]
[[!redirects Euclidean algorithm]] 
[[!redirects extended Euclidean algorithm]]