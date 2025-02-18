
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

is equivalent ([[equality|equal]] as a [[function]] from given input to output [[data types]]) to

* a [[quantum circuit]] in which all [[quantum measurement]] happens "at the end", i.e. where no [[quantum gates]] are classically [[controlled quantum gate|controlled]] by previous measurement results, but all [[controlled quantum gate|quantumly controlled]] by coherent control qbits.

The principle can be useful in practice for optimizing [[quantum circuits]]. It also clearly relates to the issue of [[interpretations of quantum mechanics]]: Since it is the [[collapse of the wavefunction]] upon [[quantum measurement]] which makes the [[interpretation of quantum mechanics]] subtle, it is interesting to note that this collapse may be (arbitrarily) deferred, in a precise sense.

## Formalizations
 {#Formalizations}

One way to formalize the deferred measurement principle is briefly mentioned in [Staton (2015), Axiom B (p. 6 of 12)](#Staton15), there proposed as an [[axiom]] to be satisfied by [[quantum programming languages]]. 

Another formalization and proof was proposed by [Gurevich & Blass 2021](#GurevichBlass21). 


{#InTermsOfQuantumModalLogic}
A quick *proof* of essentially the formulation of [Staton (2015)](#Staton15) exists in the [quantum modal logic](necessity+and+possibility#ModalQuantumLogic) of [SS23](#SS23) (cf.  *[[quantum circuits via dependent linear types]]*): Here the deferred measurement principle is essentially the [Kleisli equivalence](Kleisli+category#KleisliEquivalence) for the [[necessity]] [[comonad]] $\Box_B$ on [[dependent linear types]], like this ([SS23](#SS23), [Prop. 2.38](https://arxiv.org/pdf/2310.15735#page=79)):

\begin{imagefromfile}
    "file_name": "DeferredMeasurementAsKleisliEquiv-230807.jpg",
    "width": "800",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


\linebreak

{#ExampleCNOT} For the **example** of a [[CNOT gate]]:

\begin{imagefromfile}
    "file_name": "CNOT-DeferredMeasurement-230809.jpg",
    "width": "800",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


\linebreak

## Interpretation of Deferred measurement
 {#DeferredMeasurementAndInterpretations}

The folklore of quantum physics knows [[paradox|paradoxical]]-sounding stories under the title of 

* *[Schr&ouml;dinger's cat](https://en.wikipedia.org/wiki/Schrödinger's_cat)* (1935)

* *[Everett's observers](#EverettObservers)* (1957)

* *[Wigner's friend](https://en.wikipedia.org/wiki/Wigner%27s_friend)* (1961)

The author of these paragraphs asserts that:

1. These are all the same story, recast with different actors: Schr&ouml;dinger's cat plays the same role as Everett's observer A and the same role as Wigner's friend. The point in any case is that this first observer makes a quantum measurement and (only) ofterwards is himself observed by a second observer.

1. This is just what is formalized by the set-up of the deferred measurement principle: 

   1. The first observer (called "cat" or "A" or "friend") is the controlled quantum gate denoted "$G$" above,

   1. the quantum system observed by the first observer is $\mathrm{Q}W$ above,

   1. the state space of the first observer is $\mathscr{H}$ (before) and $\mathscr{H}'$ (after the observation).

   1. The second observer inspecting the scene at the end is the right hand side of the above setup, where the measurement is made at the end of the circuit execution. Before it is made, the first observer may have been in a superposition (in $\mathscr{H}'$).

   1. But the deferred measurement principle says the outcome is indistinguishable from the situation where the first observer already collapses the original state in $\mathrm{Q}W$.

For the record, we recall Everett's version of this story:

{#EverettObservers} A key argument in the discussion of [Everett (1957)](interpretation+of+quantum+mechanics#Everett57a), which famously led its author to the *[[many-worlds interpretation of quantum mechanics]]*, is that *intermediate state collapse* caused by one observer seems [[paradox|paradoxical]], since to a later observer the analogous state collapse occurs (only) at a later time. 
(This is really the same paradox as that of [Schrödinger's cat](https://en.wikipedia.org/wiki/Schr%C3%B6dinger%27s_cat), if we grant the cat the role of the first observer).

[Everett (1957)](interpretation+of+quantum+mechanics#Everett57a) casts this into the following prose:

>> &lbrack;[pp 4:](https://www.pbs.org/wgbh/nova/manyworlds/pdf/dissertation.pdf#page=3)&rbrack; Isolated somewhere out in space is a room containing an observer, $A$, who is about to perform a measurement upon a system $S$. After performing his measurement he will record the result in his notebook. We assume that he knows the state function of $S$ (perhaps as a result of previous measurement), and that it is not an eigenstate of the measurement he is about to perform. $A$, being an orthodox quantum theorist, then believes that the outcome of his measurement is undetermined and that the process is correctly described by Process 1 &lbrack;[[collapse of the wavefunction|state collapse]]&rbrack;.

>> In the meantime, however, there is another observer, $B$, outside the room, who is in possession of the state function of the entire room, including $S$, the measuring apparatus, and $A$, just prior to the measurement. $B$ is only interested in what will be found in the notebook one week hence, so he computes the state function of the room for one
week in the future according to Process 2 &lbrack;unitary time evolution&rbrack;. One week passes, and we find $B$ still in possession of the state function of the room, which
this equally orthodox quantum theorist believes to be a complete description of the room and its contents. If $B$'s state function calculation tells beforehand exactly what is going to be in the notebook, then $A$ is incorrect in his belief about the indeterminacy of the outcome of his measurement. We therefore assume that $B$'s state function contains non-zero amplitudes over several of the notebook entries.

>> At this point, $B$ opens the door to the room and looks at the notebook (performs his observation). Having observed the notebook entry, he turns to $A$ and informs him in a patronizing manner that since his ($B$'s) wave function just prior to his entry into the room, which he knows to have been a complete description of the room and its contents, had non-zero amplitude over other than the present result of the measurement, the result must have been decided only when $B$ entered the room, so that $A$, his notebook entry, and his memory about what occurred one week ago had no independent objective existence until the intervention by $B$. In short, $B$ implies that $A$ owes his present objective existence to $B$'s generous nature which compelled him to intervene on his behalf. However, to $B$'s consternation, $A$ does not react with anything like the respect and gratitude he should exhibit towards $B$, and at the end of a somewhat heated reply, in which $A$ conveys in a colorful manner his opinion of $B$ and his beliefs, he rudely punctures $B$'s ego by observing that if $B$'s view is correct, then he has no reason to feel complacent, since the whole present situation may have no objective existence, but may depend upon the
future actions of yet another observer.

> It is now clear that the interpretation of quantum mechanics with which we began &lbrack;the Copenhagen interpretation&rbrack; is untenable if we are to consider a universe containing more than one observer.



## Related concepts

* [[no-cloning theorem]]

## References
 {#References}

While the principle of deferred measurement is a classical statement in [[quantum information theory]], it was not defined or proven in generality and with precision (hence has remained [[folklore]]) until [Gurevich & Blass 2021](#GurevichBlass21) (see the critical discussion of the literature provided there).

Accounts of the informal statement:

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], §4.4 of *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

As an [[axiom]] for [[quantum programming languages]]:

* {#Staton15} [[Sam Staton]], Axiom B (p. 6) in: *Algebraic Effects, Linearity, and Quantum Programming Languages*, POPL '15: Proceedings of the 42nd Annual ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages (2015) 395–40 &lbrack;[doi:10.1145/2676726.2676999](https://doi.org/10.1145/2676726.2676999), [pdf](http://www.cs.ox.ac.uk/people/samuel.staton/papers/popl2015.pdf)&rbrack;



See also:

* Wikipedia, *[Deferred Measurement Principle](https://en.wikipedia.org/wiki/Deferred_Measurement_Principle)*

General precise statement and [[proof]]:

* {#GurevichBlass21} [[Yuri Gurevich]], [[Andreas Blass]], *Quantum circuits with classical channels and the principle of deferred measurements*, Theoretical Computer Science **920** (2022) 21–32 &lbrack;[arXiv:2107.08324](https://arxiv.org/abs/2107.08324), [doi:10.1016/j.tcs.2022.02.002](https://doi.org/10.1016/j.tcs.2022.02.002)&rbrack;

* {#SS23} [[Hisham Sati]], [[Urs Schreiber]], [Prop. 2.38](https://arxiv.org/pdf/2310.15735#page=79) in: *[[schreiber:The Quantum Monadology]]* &lbrack;[arXiv:2310.15735](https://arxiv.org/abs/2310.15735)&rbrack;


