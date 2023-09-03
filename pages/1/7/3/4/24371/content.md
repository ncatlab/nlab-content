
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The *Born rule* is the core statement of [[coordination]] in the foundations of [[quantum physics]]: 

In its version for [[pure states]] the Born rule says that 

* for $A$ an [[observable]] in the form of a [[Hermitean operator]] on the given [[Hilbert space]] $\mathcal{H}$ of [[pure state|pure]] [[quantum states]] with [[Hermitian form|Hermitian]] [[inner product]] $\langle\text{-}\vert\text{-}\rangle$ 

* $P$ denoting the [[projection operator]] on a given [[eigenvector|eigenstate]] of this operator, 

* $\pi \,\in\, \mathcal{H}$ a [[pure state]]; 

then the [[probability]] of observing the given eigenstate in a [[quantum system]] which is in state $\psi$ equals (in [[bra-ket notation]]):

$$
  \frac{
    \langle \psi \vert P \vert \psi \rangle
  }{
    \langle \psi \vert \psi \rangle
  }
  \,.
$$

In particular, if $W$ is an [[orthonormal basis]] for the [[Hilbert space]] [[space of quantum states|of states]] associated with a [[quantum measurement]]-procedure, then the probability of measuring the result $w$ on a system in state $\left\vert \psi \right\rangle$ is 

$$
  \frac{
    \langle \psi \vert w \rangle \langle w \vert \psi \rangle
  }{
    \langle \psi \vert \psi \rangle
  }
  \;\;=\;\;
  \frac{
    \big\vert \langle w \vert \psi \rangle \big\vert^2
  }{
    \langle \psi \vert \psi \rangle
  }
$$

and so if the state is normalized to begin with ($\langle \psi \vert \psi \rangle$ = 1 ), then the probability is

$$
  P_\psi(w)
  \;=\;
  \big\vert \langle w \vert \psi \rangle \big\vert^2
  \,.
$$

Essentially in this form the rule was first formulated by [Born 1926b p 805](#Born26b).


## Related concepts


[[!include states and observables -- content]]



## References
 {#References}

The Born rule is named in honor of 

* {#Born26a} [[Max Born]], *Zur Quantenmechanik der Stoßvorgänge*, Zeitschrift für Physik **37** (1926) 863–867 &lbrack;[doi:10.1007/BF01397477](https://doi.org/10.1007/BF01397477)&rbrack;

where it appears (though disregarding the norm symbol) as a brief footnote-added-in-proof:

\begin{imagefromfile}
    "file_name": "Born_stating_the_BornRule-Footnote.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

and its expanded version

* {#Born26b} [[Max Born]], *Quantenmechanik der Stoßvorgänge*, Zeitschrift für Physik **38** (1926) 803–827 &lbrack;[doi:10.1007/BF01397184](https://doi.org/10.1007/BF01397184)&rbrack;

which provides the details:

\begin{imagefromfile}
    "file_name": "Born_stating_the_BornRule-Expanded.jpg",
    "width": 460,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Review:

* [[Klaas Landsman]], *The Born rule and its interpretation*, in: *Compendium of Quantum Physics*, Springer (2009) 64-70 &lbrack;[doi:10.1007/978-3-540-70626-7_20](https://doi.org/10.1007/978-3-540-70626-7_20), [pdf](https://www.math.ru.nl/~landsman/Born.pdf), [[Landsman-BornRule.pdf:file]]&rbrack;

    

See also:

* Wikipedia, *[Born rule](https://en.wikipedia.org/wiki/Born_rule)*


