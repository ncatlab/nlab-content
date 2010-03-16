#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **Wightman axioms** are an attempt to axiomatize and thus formalize the notion of a [[quantum field theory]] on [[Minkowski space]]-time in terms of the assignment of field operators to points or subsets of spacetime. They serve as the basis of what is known as **constructive quantum field theory** which seeks to provide a mathematically sound framework for quantum theory over the Minkowski space background of [[special relativity]].  Arthur Wightman first formulated them in the 1950s but they were not published until 1964 after advances in scattering theory confirmed their applicability.

The Wightman axioms served to establish rigorously several basic structural properties of quantum field theories on Minkowski spacetime, such as the [[spin-statistics theorem]]  or the [[Osterwalder–Schrader theorem]] relating Lorenzian and Euclidean quantum field theories ("Wick rotation").

They were later further abstracted to the [[Haag-Kastler axioms]] that characterize [[local net]]s of operator algebras and serve as the basis for [[AQFT|algebraic quantum field theory]]. See there for further details.


This page is a draft, see:

* Wikipedia on the [Wightman axioms] (http://en.wikipedia.org/wiki/Wightman_axioms)



## Wightman Axioms

Note: the numbering - and indeed the actual number - of axioms varies depending on the source.  In many sources, several of the axioms below are combined.

+--{: .query}

[[Ian Durham]]: Can we add an axiom environment to the LaTeX template/CSS-style sheets?  According to the Instiki guide, it is supposedly relatively easy.  I just don't know how to do it on nLab.

=--

* **Axiom 1:** There is a physical Hilbert space $\mathcal{H}$ in which a unitary representation $U(a,\Lambda)$ of the [[Poincaré spinor group]], $P_{0}$ acts.

* **Axiom 2:** The spectrum of the energy-momentum operator P is concentrated in the closed upper (forward) light cone $V^{+}$.

* **Axiom 3:** There exists in $\mathcal{H}$ a unique unit vector $|0\rangle$ (vacuum), which is invariant with respect to the space-time translations $U(a,1)$. 

* **Axiom 4:** The components $\phi_{i}$ of the quantum field $\phi$ are operator valued generalized functions $\phi_{i}(x)$ over the [[Schwartz space]] $S(M)$ (tempered distributions) with domain of definition $D$ which is common to all the operators and is dense in $\mathcal{H}$. $|0\rangle$ is contained in $D$ and $D$ is taken into itself under the action of $\phi (f)$ and $U(a,\Lambda)$. 

Note: As in distribution theory it is custom to abuse the notation and write $\phi (x)$ for a point $x$ of the Minkowski spacetime and talk about the function $\phi$, rather than the value of the distribution $\phi(f)$ of a test function $f$.

* **Axiom 5:** $U(a,\Lambda)\phi_{i}(x)U(a,\Lambda)^{-1}=\sum_{j}V_{ij}(\Lambda^{-1})\phi_{j}(\Lambda x + a)$ where $V_{ij}(\Lambda)$ is a complex or real finite-dimensional matrix representation of $SL(2,C)$.

* **Axiom 6:** Any two field components $\phi_{i}(x)$ and $\phi_{j}(y)$ either commute or anticommute under a space-like separation of the arguments $x$ and $y$.

* **Axiom 7:** The set $D_{0}$ of finite linear combinations of vectors of the form $\phi_{i_1}(f_{1})\ldots\phi_{i_n}(f_{n})|0\rangle$ is dense in $\mathcal{H}$.

## The Wightman Reconstruction Theorem
The **vacuum expectation values** of the theory are all (tempered, by the axioms) distributions of the form 
$$ 
\langle0| \phi_{i_1}(f_{1})\ldots\phi_{i_n}(f_{n})|0\rangle 
$$
The term "distribution" is used interchangably with "function" and "value" in the physics literature. The Wightman reconstruction theorem states properties that a set of tempered distributions $\{\mathcal{W}^n | n \in \N \}$ need to have to be the set of vacuum expectation values of a Wightman theory, and all such Wightman theories are then unitarily equivalent. 
...to be continued...

## Equivalence to Euclidean Field Theory
see [[Osterwalder–Schrader theorem]]

## Equivalence to the Haag--Kastler Axioms
See [[Haag–Kastler axioms]]. Since both the Wightman and the Haag-Kastler approach try to formulate an axiomatic approach to quantum field theory on Minkowski spacetime, the natural question to ask is what is their relationship? Three possible answers come to mind:

* They are equivalent.

* One contains the other, i.e. one set of axioms implies the other.

* At least one is wrong (from the physical viewpoint).

Unfortunatly the situation does not seem to be as clear as this list suggests. The current state of the affair seems to be that 

* "the Haag-Kastler approach is more convenient, because it deals with algebras of bounded operators, while Wightman fields are allowed to generate unbounded operators"

and

* "a Wightman field theory is equivalent to a Haag-Kastler theory, if some mild additional assumptions are made".

Reference:

* H.J. Borchers, Jakob Yngvason: "From quantum fields to local von Neumann algebras", Rev.Math.Phys. Special issue, 1992, p.15-47.

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

## References
The classic reference already listed by Wikipedia is of course:

* Raymond F. Streater and Arthur S. Wightman: "PCT, spin and statistics, and all that." ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1026.81027&format=complete) of the newest edition).


Raymond Streater relates some historical background about the book and the approach [on his webpage] (http://www.mth.kcl.ac.uk/~streater/wightman.html).
