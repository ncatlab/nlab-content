
## Idea

A certain identity for certain [[Fourier transforms]], equating a sum or integral of a function over a domain (e.g., a lattice) with a corresponding sum or integral of its Fourier dual over a dual domain (e.g., the dual lattice).

## Statement 

The Poisson summation formula is basic to harmonic analysis over general locally compact Hausdorff abelian groups. 

Consider an exact sequence in $TopAb$ of [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] [[topological abelian group|abelian groups]] 

$$0 \to A \to B \to C \to 0.$$ 

where $A, B, C$ are equipped with Haar measures $d\mu_A, d\mu_B, d\mu_C$ that make the following equation true: 

$$\int_B f(b)\; d\mu_B(b) = \int_C \int_A f(a + c)\; d\mu_A(a) d\mu_C(c)$$ 

for all [[continuous functions]] $f: B \to \mathbb{C}$ with [[compact support]]. 
(The inner integral on the right is a shorthand for $\int_A f(a + b)\; d\mu_A(a)$ for any $b$ that maps to $c \in C$; note that this quantity is invariant under changes $b \mapsto b + a'$ within the same coset $c$.) We remark that given Haar measures $d\mu_A, d\mu_B$, there exists a Haar measure $d\mu_C$ making this Fubini-type equation true. 

In this notation, the "Poisson summation formula" is the equation asserted by the following result. 

+-- {: .num_theorem} 
###### Theorem 
Let $\widehat{C}$ denote the [[Pontryagin duality|Pontryagin dual]] of $C$, and $d\mu_{\widehat{C}}$ the dual Haar measure. For any [[Schwartz-Bruhat function]] $f: B \to \mathbb{C}$, we have 

$$\int_A f(a)\; d\mu_A = \int_{\widehat{C}} \widehat{f}(\widehat{c})\; d\mu_{\widehat{C}}$$ 

where $\widehat{f}$ is the Fourier dual of $f$, as a function on $\widehat{B}$.
=--  

In the special case of a [[lattice (discrete subgroup)|lattice]] $L$ inside $B$, the dual space $L^\perp = \widehat{B/L}$ is a lattice inside $\widehat{B}$, and the integrals are over discrete spaces, i.e. integration is just summation and we have 

$$\sum_{x \in L} f(x) = \frac1{\mu(B/L)} \sum_{y \in L^\perp} \widehat{f}(y)$$

where $\mu$ is the Haar measure on $B/L$ (as above). 

Especially when $B$ is a [[Euclidean space]] $\mathbb{R}^n$, this gives the classical form of the Poisson summation formula. But this situation also obtains in the context of [Tate's thesis](#Tate1950), where a [[global field]] is viewed as a lattice inside its [[ring of adeles]]. 

## Examples

* The Poisson summation formulation implies the [[functional equation]] for the [[Jacobi theta function]], which in turn implies that of the [[Riemann zeta function]], see at _[Riemann zeta function -- functional identity](Riemann+zeta+function#functional_equation)_.

## Related entries

* [[functional equation]]

* A nonabelian version of the Poisson summation formula is the [[Selberg trace formula]].

## References




Reviews include

* theorem 4.1 in _Analytic theory of modular forms_ [pdf](http://www.math.harvard.edu/~jbland/ma259x_notes.pdf)

* E. Kowalski, prop. 2.2.1 in  _Automorphic forms, L-functions and number theory (March 12&#8211;16) Three Introductory lectures_ ([pdf](http://www.math.ethz.ch/~kowalski/lectures.pdf))

An application to [[zeta functions]] via harmonic analysis on [[adele rings]] originates in Tate's thesis: 

* {#Tate1950} [[John Tate]], _[[Fourier analysis in number fields, and Hecke's zeta-functions]]_, Princeton, May 1950, thesis; reproduced in _Algebraic Number Theory_ (Proc. Instructional Conf., Brighton, 1965) pp. 305&#8211;347, Academic Press 1967 
[MR0217026](http://www.ams.org/mathscinet-getitem?mr=0217026)

A textbook account is

* {#GoldfeldHundley11} [[Dorian Goldfeld]], [[Joseph Hundley]], chapter 2 of _Automorphic representations and L-functions for the general linear group_, Cambridge Studies in Advanced Mathematics 129, 2011 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/text/gl2.pdf))

and brief review in 

* {#Garrett11} [[Paul Garrett]], _Iwasawa-Tate on &#950;-functions and L-functions_, 2011 ([pdf](http://www-users.math.umn.edu/~garrett/m/mfms/notes_c/Iwasawa-Tate.pdf)
[[!redirects Poisson formula]]
