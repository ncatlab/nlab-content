#Contents#
* automatic table of contents goes here
{:toc}

## Idea

this page is a draft, see:


* Wikipedia on the [Wightman axioms] (http://en.wikipedia.org/wiki/Wightman_axioms)

The Wightman axioms are an attempt to develop a mathematically rigorous set of axioms for quantum field theory.  The axioms serve as the basis of what is known as _constructive_ field theory which seeks to show that quantum theory is _mathematically_ compatible with special relativity.  Arthur Wightman first formulated them in the 1950s but they were not published until 1964 after advances in scattering theory suggested confirmed their applicability.


## Wightman Axioms

Note: the numbering - and indeed the actual number - of axioms varies depending on the source.  In many sources, several of the axioms below are combined.

+--{: .query}

[[Ian Durham]]: Can we add an axiom environment to the LaTeX template/CSS-style sheets?  According to the Instiki guide, it is supposedly relatively easy.  I just don't know how to do it on nLab.

=--

* **Axiom 1:** There is a physical Hilbert space $\mathcal{H}$ in which a unitary representation $U(a,\Lambda)$ of the [[Poincaré spinor group]], $P_{0}$ acts.

* **Axiom 2:** The spectrum of the energy-momentum operator P is concentrated in the closed upper (forward) light cone $V^{+}$.

* **Axiom 3:** There exists in $\mathcal{H}$ a unique unit vector $|0\rangle$ (vacuum), which is invariant with respect to the space-time translations $U(a,1)$. 

* **Axiom 4:** The components $\phi_{i}$ of the quantum field $\phi$ are operator valued generalized functions $\phi_{i}(x)$ over the [[Schwartz space]] $S(M)$ (tempered distributions) with domain of definition $D$ which is common to all the operators and is dense in $\mathcal{H}$. $|0\rangle$ is contained in $D$ and $D$ is taken into itself under the action of $\phi (f)$ and $U(a,\Lambda)$. 

* **Axiom 5:** $U(a,\Lambda)\phi_{i}(x)U(a,\Lambda)^{-1}=\sum_{j}V_{ij}(\Lambda^{-1})\phi_{j}(\Lambda x + a)$ where $V_{ij}(\Lambda)$ is a complex or real finite-dimensional matrix representation of $SL(2,C)$.

* **Axiom 6:** Any two field components $\phi_{i}(x)$ and $\phi_{j}(y)$ either commute or anticommute under a space-like separation of the arguments $x$ and $y$.

* **Axiom 7:** The set $D_{0}$ of finite linear combinations of vectors of the form $\phi_{i1}(f_{1})\ldots\phi_{in}(f_{n})|0\rangle$ is dense in $\mathcal{H}$.



## The Wightman Reconstruction Theorem
...will go here

## Equivalence to Euclidean Field Theory
see [[Osterwalder–Schrader theorem]]

## Equivalence to the Haag--Kastler Axioms
...aspects of this will go here, see [[Haag–Kastler axioms]]

## References
The classic reference already listed by Wikipedia is of course:

* Raymond F. Streater and Arthur S. Wightman: "PCT, spin and statistics, and all that." ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1026.81027&format=complete) of the newest edition).


Raymond Streater relates some historical background about the book and the approach [on his webpage] (http://www.mth.kcl.ac.uk/~streater/wightman.html).
