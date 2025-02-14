
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

* [[quantum probability]]


[[!include states and observables -- content]]



## References
 {#References}

### Historical origins
  {#ReferencesHistoricalOrigins}

The Born rule is named in honor of 

* {#Born26a} [[Max Born]], *Zur Quantenmechanik der Stoßvorgänge*, Zeitschrift für Physik **37** (1926) 863–867 &lbrack;[doi:10.1007/BF01397477](https://doi.org/10.1007/BF01397477)&rbrack;

where it appears (though disregarding the norm symbol) as a brief footnote-added-in-proof:

\begin{imagefromfile}
    "file_name": "Born_stating_the_BornRule-Footnote.jpg",
    "width": 560,
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

which provides the mathematical details (p. 805):

\begin{imagefromfile}
    "file_name": "Born_stating_the_BornRule-Expanded.jpg",
    "width": 480,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

and finally in the followup

* {#Born27} [[Max Born]], *Das Adiabatenprinzip in der Quantenmechanik*, Zeitschrift für Physik **40** (1927) 167–192 &lbrack;[doi:10.1007/BF01400360](https://doi.org/10.1007/BF01400360)&rbrack;

which makes the interpretation more explicit (p. 171):

\begin{imagefromfile}
    "file_name": "Born_stating_the_BornRule-ExpandedII.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

The generalization of this idea to probability *densities* for continuous [[observables]] is due to [[Wolfgang Pauli]], as first recounted in:
 
* {#Jordan27} [[Pascual Jordan]], *Über eine neue Begründung der Quantenmechanik*, Zeitschrift für Physik **40** (1927) 809–838 &lbrack;[doi:10.1007/BF01390903](https://doi.org/10.1007/BF01390903)&rbrack;

\begin{imagefromfile}
    "file_name": "Jordan-PauliBornRule.jpg",
    "width": 510,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

and then by Pauli himself, again in a footnote:

* [[Wolfgang Pauli]], *Über Gasentartung und Paramagnetismus*, Zeitschrift für Physik: A Hadrons and nuclei **41** (1927) 81–102 &lbrack;[doi:10.1007/BF01391920](https://doi.org/10.1007/BF01391920)&rbrack;

\begin{imagefromfile}
    "file_name": "PauliStatingBornPauliRule.jpg",
    "width": 540,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Early review of the Born-Pauli rule:

* {#HilbertvonNeumannNordheim} [[David Hilbert]], [[John von Neumann]], [[Lothar W. Nordheim]], *Über die Grundlagen der Quantenmechanik*,  Math. Ann. **98** (1928) 1–30 &lbrack;[doi:10.1007/BF01451579](https://doi.org/10.1007/BF01451579)&rbrack;

where it is once again a footnote:

\begin{imagefromfile}
    "file_name": "HilbertNeumannNordheim-BornRule.jpg",
    "width": 530,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

and in 

*  [[Paul A. M. Dirac]], *The physical interpretation of the quantum dynamics*, Proceedings of the Royal Society of London **113** 765 (1927) &lbrack;[doi:10.1098/rspa.1927.0012](https://doi.org/10.1098/rspa.1927.0012)&rbrack;


\begin{imagefromfile}
    "file_name": "Dirac_OnBornPauliRule.jpg",
    "width": 530,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


The full recognition and amplification of the Born rule as a pillar of quantum physics making it a [[probability theory|probabilistic]] [[theory (physics)|theory]] (cf. *[[quantum probability]]*) is (maybe besides [Jordan 1927](#Jordan27)) due to:

* [[John von Neumann]], *Die quantenmechanische Statistik*, Part III in:

  *Mathematische Grundlagen der Quantenmechanik*, Springer (1932, 1971) &lbrack;[doi:10.1007/978-3-642-96048-2](https://link.springer.com/book/10.1007/978-3-642-96048-2)&rbrack;

  *Mathematical Foundations of Quantum Mechanics* Princeton University Press (1955) &lbrack;[doi:10.1515/9781400889921](https://doi.org/10.1515/9781400889921), [Wikipedia entry](https://en.wikipedia.org/wiki/Mathematical_Foundations_of_Quantum_Mechanics)&rbrack;

\begin{imagefromfile}
    "file_name": "vonNeumann-BornRule.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\begin{imagefromfile}
    "file_name": "vonNeumann-QMStatistics.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Historical survey:

* [[Jagdish Mehra]], Helmut Rechenberg, *The Probability Interpretation and the Statistical Transformation Theory, the Physical Interpretation, and the Empirical and Mathematical Foundations of Quantum Mechanics 1926-1932*, Part 1 in:  *The Historical Development of Quantum Theory. Volume 6: The Completion of Quantum Mechanics, 1926-1941*, Springer (2001)   &lbrack;[ISBN:978-0-387-98971-6](https://link.springer.com/book/9780387989716)&rbrack;

### Further discussion

Review:

* [[Klaas Landsman]], *The Born rule and its interpretation*, in: *Compendium of Quantum Physics*, Springer (2009) 64-70 &lbrack;[doi:10.1007/978-3-540-70626-7_20](https://doi.org/10.1007/978-3-540-70626-7_20), [pdf](https://www.math.ru.nl/~landsman/Born.pdf), [[Landsman-BornRule.pdf:file]]&rbrack;

* [[Arnold Neumaier]]: *The Born rule -- 100 years ago and today* &lbrack;[arXiv:2502.08545](https://arxiv.org/abs/2502.08545)&rbrack;


    
See also:

* Wikipedia, *[Born rule](https://en.wikipedia.org/wiki/Born_rule)*


[[!redirects Born-Pauli rule]]

