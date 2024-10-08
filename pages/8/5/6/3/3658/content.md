

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The **Wightman axioms** are an attempt to [[axiom|axiomatize]] and thus formalize the notion of a [[quantum field theory]] on [[Minkowski spacetime]] ([[relativistic quantum field theory]]) in the sense of [[AQFT]], i.e. in terms of the assignment of field [[quantum observables]] to points or subsets of [[spacetime]] ([[operator-valued distributions]]). 

They serve as the basis of what is known as **constructive quantum field theory** which seeks to provide a mathematically sound framework for quantum theory over the Minkowski space background of [[special relativity]].  [[Arthur Wightman]] first formulated them in the 1950s but they were not published until 1964 after advances in scattering theory confirmed their applicability.

The Wightman axioms served to establish rigorously several basic structural properties of quantum field theories on Minkowski spacetime, such as the [[spin-statistics theorem]]  or the [[Osterwalder–Schrader theorem]] relating Lorenzian and Euclidean quantum field theories ("Wick rotation").

They were later further abstracted to the [[Haag-Kastler axioms]] that characterize [[local net]]s of operator algebras and serve as the basis for [[AQFT|algebraic quantum field theory]]. See there for further details.


This page is a draft, see:

* Wikipedia on the [Wightman axioms] (http://en.wikipedia.org/wiki/Wightman_axioms)



## Wightman Axioms

Note: the numbering - and indeed the actual number - of axioms varies depending on the source.  In many sources, several of the axioms below are combined.


+-- {.num_defn}
###### Axiom
There is a physical Hilbert space $\mathcal{H}$ in which a unitary representation $U(a,\Lambda)$ of the [[Poincaré spinor group]], $P_{0}$ acts.
=--

+-- {.num_defn}
###### Axiom
The spectrum of the energy-momentum operator P is concentrated in the closed upper (forward) light cone $V^{+}$.
=--

+-- {.num_defn}
###### Axiom
There exists in $\mathcal{H}$ a unique unit vector $|0\rangle$ (the _[[vacuum state]]_), which is invariant with respect to the space-time translations $U(a,1)$. 
=--

+-- {.num_defn}
###### Axiom
The components $\phi_{i}$ of the quantum field $\phi$ are [[operator-valued distributions]] $\phi_{i}(x)$ over the [[Schwartz space]] $S(M)$ ([[tempered distributions]]) with domain of definition $D$ which is common to all the operators and is dense in $\mathcal{H}$. $|0\rangle$ is contained in $D$ and $D$ is taken into itself under the action of $\phi (f)$ and $U(a,\Lambda)$. 
=--

Note: As in distribution theory it is custom to abuse the notation and write $\phi (x)$ for a point $x$ of the Minkowski spacetime and talk about the function $\phi$, rather than the value of the distribution $\phi(f)$ of a test function $f$.

+-- {.num_defn}
###### Axiom
$U(a,\Lambda)\phi_{i}(x)U(a,\Lambda)^{-1}=\sum_{j}V_{ij}(\Lambda^{-1})\phi_{j}(\Lambda x + a)$ where $V_{ij}(\Lambda)$ is a complex or real finite-dimensional matrix representation of $SL(2,C)$.
=--

+-- {.num_defn}
###### Axiom
Any two field components $\phi_{i}(x)$ and $\phi_{j}(y)$ either commute or anticommute under a space-like separation of the arguments $x$ and $y$.
=--

+-- {.num_defn}
###### Axiom
The set $D_{0}$ of finite linear combinations of vectors of the form $\phi_{i_1}(f_{1})\ldots\phi_{i_n}(f_{n})|0\rangle$ is dense in $\mathcal{H}$.
=--

## Properties

### The Wightman Reconstruction Theorem

The **[[vacuum expectation values]]** ([[n-point functions]]) of the theory are all (tempered, by the axioms) distributions of the form 
$$ 
\langle0| \phi_{i_1}(f_{1})\ldots\phi_{i_n}(f_{n})|0\rangle 
$$
The term "distribution" is used interchangably with "function" and "value" in the physics literature. The Wightman reconstruction theorem states properties that a set of tempered distributions $\{\mathcal{W}^n | n \in \N \}$ need to have to be the set of vacuum expectation values of a Wightman theory, and all such Wightman theories are then unitarily equivalent. 
...to be continued...

### Equivalence to Euclidean Field Theory

See [[Osterwalder–Schrader theorem]]

### Equivalence to the Haag--Kastler Axioms

See [[Haag–Kastler axioms]]. Since both the Wightman and the Haag-Kastler approach try to formulate an axiomatic approach to quantum field theory on Minkowski spacetime, the natural question to ask is what is their relationship? Three possible answers come to mind:

* They are equivalent.

* One contains the other, i.e. one set of axioms implies the other.

* At least one is wrong (from the physical viewpoint).

Unfortunatly the situation does not seem to be as clear as this list suggests. The current state of the affair seems to be that 

* "the Haag-Kastler approach is more convenient, because it deals with algebras of bounded operators, while Wightman fields are allowed to generate unbounded operators"

and

* "a Wightman field theory is equivalent to a Haag-Kastler theory, if some mild additional assumptions are made".

Reference:

* [[Hans-Jürgen Borchers]], [[Jakob Yngvason]], *From quantum fields to local von Neumann algebras*, Rev. Math. Phys. **4** spec01 (1992) 15-47 &lbrack;[doi:10.1142/S0129055X92000145](https://doi.org/10.1142/S0129055X92000145)&rbrack;


+--{: .query}

[[Tim van Beek]]: The two statemants above are a condensate of diverse papers I read, any input about the true state of the art would be most welcome. My educated guess is that the "mildness" of the assumptions indicates the fact that all physically realistic models are supposed to satisfy these.

=--

Should it be bounded or unbounded operators/observables?

* Pro: Some observables do not have an upper bound, e.g. you can always increase the impulse of an electron, no matter how big that already is (in theory).

* Contra: A detector has an upper bound for every observable it can detect, and that is what is actually measured in an experiment. The situation of the pro-bullet won't arise because we measure observables in bounded regions of spacetime, and the energy contained in a bounded region is always finite (we are excluding artifacts like black holes from our consideration, of course).

* Contra to even asking the question: Theories of bounded and unbounded operators/observables are physically equivalent modulo mathematical subtleties, meaning they produce the same numbers that can be compared to experiments. 

One simple situation where the construction of a Haag-Kastler net out of Wightman fields is straight forward is this: Suppose that all smeared field operators of the Wightman theory are essentially self adjoint for real test functions and commute strongly (their spectral projections commute) if the test functions have space-like separated support.
Then we can define local algebras by
$\mathcal{M}(\mathcal{O}) := \{F(\Psi(f)) | f$ is a real test function with support contained in $\mathcal{O}$ and F is a bounded Borel measurable function on $\R \}$.

(Our assumptions allow us to use the [Borel functional calculus] (http://en.wikipedia.org/wiki/Borel_functional_calculus)).

## Examples

### Neutral Real (uncharged) Scalar Field

A neutral real quantum scalar field on Minkowski spacetime $M$ with mass parameter $m \gt 0$ can be defined as follows:

+-- {: .un_def}
###### Definition
The **positive mass shell** is the subset of Minkowski spacetime defined by 

$$
X^+_m := \{p | p^2 = m^2, \; p_0 \gt 0 \}
$$

The **normalized Lorentz-invariant measure** on the positive mass shell is defined with respect to the Lesbegue measure by
$$
d\lambda(p) = d\lambda(\omega_p, \vec p) = \frac{d^3 \vec p}{(2\pi)^3 \omega_p} \; \text{with} \; \omega_p = p^0 = \sqrt{|\vec p|^2 + m^2} 
$$

=--


Let $H = L^2(X^+_m, \lambda)$ be the Hilbert space with $X^+_m$ the positive mass shell and $\lambda$ the normalized Lorentz-invariant measure on it as defined above. Construct the Boson [[Fock space]] $F_s(H)$. 

Define the operator $R$ to be the Lorentz invariant Fourier transform restricted to $X^+_m$:
$$
R: \mathcal{S}(\mathbb{R}^4) \to H
$$

$$
R(f) := \hat f |_{X^+_m} \; \text{with} \; \hat f := \mathcal{F}(f) = \int_M e^{i p_{\mu} x^{\mu}} f(x) dx 
$$

The quantum field $\Psi$ is now a real tempered distribution on $M$ with values in the space of operators of $F_s(H)$.

$$
\Psi:   \mathcal{S}(M) \to \mathcal{B}(F_s(H)) 
$$

$$
         f \mapsto \Psi(f) = \frac{1}{\sqrt(2)} (a(Rf) + a^*(Rf))
$$
$a$ and $a^*$ are the annihilation and creation operators on $F_s(H)$, that is $a(v)$ anihilates a single particle state $v$ and $a^*(v)$ creates a single particle state $v$.

$\Psi$ is a distribution solution of the [[Klein-Gordon equation]] by construction, that is for every test function $f$ we get

$$
\Psi((\Box + m^2) f) = 0
$$

The reason for this is that
$$
\mathcal{F}{[(\Box + m^2) f]} = (-p^2 + m^2) f = 0 \; \text{on} \; X^+_m
$$

### Further examples

The Wightman axioms have been established for the following theories.

* Massive 2d scalar theories with polynomial interactions, see [this article](http://www.jstor.org/stable/1970959) by Glimm, Jaffe and Spencer.

* Massive $\phi^4$ in 3d, see [this article](http://www.sciencedirect.com/science/article/pii/0003491676902232) by Feldman and Osterwalder as well as this one by Magnen and Seneor.

* Massive Gross-Neveu in 2d see [this article](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.cmp/1104114300) by Gawedzki and Kupiainen and [this one](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.cmp/1104114625) by Feldman, Magnen, Rivasseau and Seneor.

* Massive Thirring model, see [this article](http://dx.doi.org/10.5169/seals-114796) by Frohlich and Seiler and this more recent one by Benfatto, Falco and Mastropietro.


## Related concepts

* [[AQFT]], [[local net]]

* [[conformal net]], [[conformal bootstrap]]

* analog for [[Euclidean field theory]]: [[Osterwalder-Schrader axioms]]

## References

The original texts are

* A. S. Wightman, L. Gårding, _Fields as Operator-valued Distributions in Relativistic Quantum Theory_, Arkiv f. Fysik, Kungl. Svenska Vetenskapsak. 28, 129–189 (1964).

* [[Raymond F. Streater]], [[Arthur S. Wightman]], *PCT, Spin and Statistics, and All That*, Princeton University Press (1989, 2000) &lbrack;[ISBN:9780691070629](https://press.princeton.edu/books/paperback/9780691070629/pct-spin-and-statistics-and-all-that), [jstor:j.ctt1cx3vcq](https://www.jstor.org/stable/j.ctt1cx3vcq)&rbrack;

Raymond Streater relates some historical background about the book and the approach [on his webpage] (http://www.mth.kcl.ac.uk/~streater/wightman.html).


Introduction to [[QFT]] via Wightman axioms and [[AQFT]]:

* [[Garth Warner]]: *Quantum Field Theory Seminar (School of Wightman et al.)*, seminar notes, University of Washington &lbrack;[pdf](https://sites.math.washington.edu//~warner/QFTSeminar_Warner.pdf), [[Warner-WightmanQFT.pdf:file]]&rbrack;

* [[Franco Strocchi]], _Relativistic Quantum Mechanics and Field Theory_, Found. Phys. **34** (2004) 501-527 &lbrack;[arXiv:hep-th/0401143](http://arxiv.org/abs/hep-th/0401143)&rbrack;

and with emphasis on its role in [[non-perturbative quantum field theory]]:

* [[Franco Strocchi]], Section 3 of: *An Introduction to Non-Perturbative Foundations of Quantum Field Theory*, Oxford University Press (2013) &lbrack;[doi:10.1093/acprof:oso/9780199671571.001.0001](https://doi.org/10.1093/acprof:oso/9780199671571.001.0001)&rbrack;




The list of examples above draws from:

* Abdesselam, _[TP.SE comment](http://theoreticalphysics.stackexchange.com/questions/308/which-qfts-were-rigorously-constructed/350#350)_

Discussion of the axioms for $\phi^4$-theory in 3d is in

* Joel Feldman, [[Konrad Osterwalder]], _The Wightman axioms and the mass
gap for weakly coupled $phi_3^4$ quantum field theories_, Ann. Physics 97 (1976), 80&#8211;135

See also

* Wikipedia, _[Wightman axioms](https://en.wikipedia.org/wiki/Wightman_axioms)_

[[!redirects Wightman theory]]
[[!redirects Wightman approach]]