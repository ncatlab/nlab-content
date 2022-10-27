
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In [[quantum physics]] and specifically in [[quantum information theory]], the *principle of deferred measurement* is a [[theorem]] which says that 

* any [[quantum circuit]] involving [[quantum measurement]] of some of the [[qbits]] followed by [[quantum gates]] [[controlled quantum gate|controlled]] by the respective measurement outcomes 

is equivalent ([[equality|equal]] as a [[function]] from given input to output [[data types]]) as

* a [[quantum circuit]] in which all [[quantum measurement]] happens "at the end", i.e. where no [[quantum gates]] are [[controlled quantum gate|controlled]] by previous measurement results.

The principle can be useful in practice for optimizing [[quantum circuits]]. It also clearly relates to the issue of [[interpretations of quantum mechanics]]: Since it is the [[collapse of the wavefunction]] upon [[quantum measurement]] which makes the [[interpretation of quantum mechanics]] subtle, it is interesting to note that this collapse may be (arbitrarily) deferred, in a precise sense.

## Formalizations
 {#Formalizations}

See [Gurevich & Blass 2021](#GurevichBlass21).

{#InTermsOfQuantumModalLogic}
Alternatively: In terms of the discussion at *[[quantum circuits via dependent linear types]]*, the deferred measurement principle is essentially the [Kleisli equivalence](Kleisli+category#KleisliEquivalence) for the [[necessity]] [[comonad]] $\Box_B$ on [[dependent linear types]], like this:


\begin{imagefromfile}
    "file_name": "DeferredMeasurementAsKleisliEquiv-221027b.jpg",
    "width": "800",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


## References
 {#References}

While the principle of deferred measurement is a classical statement in [[quantum information theory]], it was not defined or proven in generality and with precision (hence has remained [[folklore]]) until [Gurevich & Blass 2021](#GurevichBlass21) (see the critical discussion of the literature provided there).

Accounts of the informal statement:

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], §4.4 of *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

See also:

* Wikipedia, *[Deferred Measurement Principle](https://en.wikipedia.org/wiki/Deferred_Measurement_Principle)*

Precise statement and [[proof]]:

* {#GurevichBlass21} [[Yuri Gurevich]], [[Andreas Blass]], *Quantum circuits with classical channels and the principle of deferred measurements*, Theoretical Computer Science **920** (2022) 21–32 &lbrack;[arXiv:2107.08324](https://arxiv.org/abs/2107.08324), [doi:10.1016/j.tcs.2022.02.002](https://doi.org/10.1016/j.tcs.2022.02.002)&rbrack;
