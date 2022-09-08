
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
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


What came to be called *Bell's inequality* ([Bell 1964](#Bell64)) is an [[inequality]] satisfied by the three pairwise [[correlation functions]] between three [[random variables]] defined on one and the same classical [[probability space]]. As such, it is an elementary statement about classical probability theory which as been argued ([Pitowsky 1989a](#Pitowsky89a)) to have been known already to [[Boole -- The Laws of Thought|Boole (1854)]].

The point of the argument by [Bell 1964](#Bell64) was to highlight that when taking these three random variables to be the results of [[quantum measurements]] of the [[spin]] of an [[electron]] along three pairwise non-orthogonal axes (as in the [[Stern-Gerlach experiment]]) then [[quantum theory]] predicts that this inequality is *violated* -- implying that there is no single classical [[probability space]] (called a *[[hidden variable theory|hidden variable]]* in the context of [[interpretations of quantum mechanics]]) on which these three [[quantum measurement]]-results are jointly [[random variables]].

A number of [[experiments]] have sought to check Bell's inequalities in [[quantum physics]] ("[[Bell tests]]") and all claim to have verified that it is indeed violated in nature (see [Aspect 2015](#Aspect15)), as predicted by [[quantum theory]].

Bell's inequality has been and is receiving an enormous amount of attention, first in discussions of [[interpretations of quantum mechanics]], but more recently and more concretely also in the context of [[quantum information theory]].


## Statement
 {#Statement}

A transparent and compact way to derive the actual [[inequality]] of [Bell 1964](#Bell64) (adjusting the original argument only slightly for mathematical elegance) is reviewed in [Khrennikov 2008, §10.1](#Khrennikov08), which we broadly follow:

\begin{proposition}
Given

1. a [[probability space]] $(\Lambda, d\rho)$ with

1. three [[random variables]] taking values in $\{\pm 1\}$ (regarded inside the [[real numbers]]):

   \[
     \label{TheRandomVariables}
     S_i 
       \;\colon\; 
     X \longrightarrow \{\pm 1\} 
     \hookrightarrow
     \mathbb{R}
     \,,
     \;\;\;\;
     i\,\in\, \{1,2,3\}
   \]

then the [[correlation functions]]

\[
  \label{TheCorrelations}
  \langle S_{i} \, S_j\rangle
  \;\coloneqq\;
  \int_{\Lambda} 
    \;
    S_i(\lambda) 
    \,
    S_j(\lambda) 
  \;
  d\rho(\lambda)
\]

satisfy this [[inequality]]:

\[
  \label{TheInequality}
  \big\vert
    \langle S_1 S_2\rangle
    -
    \langle S_3 S_2\rangle
  \big\vert
  \;\leq\;
  1 - \langle S_1 S_3\rangle
  \,.
\]

(where $\left\vert-\right\vert$ denotes the [[absolute value]])
\end{proposition}
\begin{proof}
  Recall that the [[expectation value]] of a random variable $P \,\colon\, \Lambda \longrightarrow \mathbb{R}$ is given by its [[Lebesgue integral]] against the [[probability measure]]:
  $$
    \langle P \rangle
    \;\coloneqq\;
    \int_\Lambda P(\lambda) \, d\rho(\lambda)
    \,,
  $$
  and that $d\rho$ being a [[probability measure]] implies the normalization
  \[
    \label{NormalizationOfProbability}
    \langle 1 \rangle
    \;\equiv\;
    \int_\Lambda 1 \, d\rho(\lambda)
    \;=\;
    1
    \,.
  \]

Moreover, the assumption (eq:TheRandomVariables) that the random variables $S_i$ take values in $\{\pm 1\}$
immediately implies for all $i,j \,in\, \{1,2,3\}$ that 
  \[
    \label{IdempotencyOfTheRandomVariables}
    \big( S_i \cdot S_i \big) \,=\, 1
    \,,
    \;\;\;\;
    \text{i.e.}
    \;\;\;
    \underset{\lambda \,\in\, \Lambda}{\forall}
    S_i(\lambda) \, S_i(\lambda)
    \,=\, 
    (\pm 1)^2
    \,=\,
    1
    \,.
  \]

Together this implies -- by repeatedly using the [[Cauchy-Schwarz inequality]] -- the bounds:

$$
  \big\vert 
    \langle S_i \rangle
  \big\vert
  \;\leq\;
  1
  \,,
  \;\;\;\;\;\;\;
  \big\vert
    \langle S_i S_j\rangle
  \big\vert
  \;\leq\;
  1
$$

and thus, in particular:

\[
  \label{BoundOnCorrelations}
  \big\vert
  \langle 
    P \, S_i \, S_j
  \rangle
  \big\vert
  \;\leq\;
  \big\vert
  \langle 
    P 
  \rangle
  \big\vert
  \,,
\]

for any [[random variable]] $P \,\colon\, \Lambda \to \mathbb{R}$.


Using these (evident) ingredients, we directly compute as follows
$$
  \begin{array}{ll}
  \big\vert
    \langle S_1 S_2\rangle
    -
    \langle S_3 S_2\rangle
  \big\vert
  & 
  \\
  \;=\;
  \Big\vert
    \int_{\Lambda} 
      S_1(\lambda) \, S_2(\lambda)
      \,
    d\rho(\lambda)
    -
    \int_{\Lambda} 
      S_3(\lambda) \, S_2(\lambda)
      \,
    d\rho(\lambda)
  \Big\vert
  &
  \text{by}\;\text{(eq:TheCorrelations)}
  \\
  \;=\; 
  \Big\vert
    \int_{\Lambda} 
      \big(
        S_1(\lambda) 
        -
        S_3(\lambda)
      \big)
      \,
      S_2(\lambda)
      \,
    d\rho(\lambda)
  \Big\vert
  &
  \text{by linearity of the integral}
  \\
  \;=\;
  \Big\vert
    \int_{\Lambda} 
      \big(
        1 
        -
        S_1(\lambda) \, S_3(\lambda)
      \big)
      S_1(\lambda) \, S_2(\lambda)
      \,
    d\rho(\lambda)
  \Big\vert
  &
  \text{by}\;\text{(eq:IdempotencyOfTheRandomVariables)}
  \\
  \;\leq\;
  \Big\vert
    \int_{\Lambda} 
      \big(
        1 
        -
        S_1(\lambda) \, S_3(\lambda)
      \big)
      \,
    d\rho(\lambda)
  \Big\vert
  &
  \text{by}\;\text{(eq:BoundOnCorrelations)}
  \\
  \;=\;
  1 - \langle S_1 S_3\rangle
  &
  \text{by}\;\text{(eq:NormalizationOfProbability)}\;\text{and}\; \text{(eq:TheCorrelations)}
  \end{array}
$$

This is the inequality (eq:TheInequality).
\end{proof}




## Related concepts

* [[Einstein-Podolsky-Rosen paradox]]

* [[quantum probability]]

* [[interpretation of quantum mechanics]]

* [[quantum information theory]]

## References

### General

The original article:

* {#Bell64} [[John Bell]], *On the Einstein Podolsky Rosen paradox*, Physics **1** 195 (1964) &lbrack;[doi:10.1103/PhysicsPhysiqueFizika.1.195](https://doi.org/10.1103/PhysicsPhysiqueFizika.1.195), [pdf](http://www.drchinese.com/David/Bell_Compact.pdf)&rbrack;
  
Review:

* {#Kuperberg05} [[Greg Kuperberg]], section 1.6.2 of _A concise introduction to quantum probability, quantum mechanics, and quantum computation_, 2005 ([pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf))

Experiments:

* {#Aspect15} [[Alain Aspect]], *[Closing the Door on Einstein and Bohr’s Quantum Debate](https://physics.aps.org/articles/v8/123)*, Physics **8** 123 (2015)

    


See also:

* Wikipedia, _[Bell's theorem](http://en.wikipedia.org/wiki/Bell_inequality)_

* Wikipedia, *[Bell test](https://en.wikipedia.org/wiki/Bell_test)*

* Wikipedia, *[Leggett-Garg inequality](https://en.wikipedia.org/wiki/Leggett%E2%80%93Garg_inequality)*


### Probabilistic opposition
  {#ReferencesProbabilisticOpposition}

Identification of Bell's inequalities with much older inequalities in classical [[probability theory]], due to [[George Boole]]'s *[[Boole -- The Laws of Thought|The Laws of Thought]]*, was pointed out by (among others, called the "probabilistic opposition" in [Khrennikov 2007, p. 3](#Khrennikov07)) by:
 
* {#Pitowsky89a} [[Itamar Pitowsky]], *From George Boole To John Bell — The Origins of Bell’s Inequality*, in: *Bell’s Theorem, Quantum Theory and Conceptions of the Universe*, Fundamental Theories of Physics **37** Springer (1989) &lbrack;[doi:10.1007/978-94-017-0849-4_6](https://doi.org/10.1007/978-94-017-0849-4_6)&rbrack;

* {#Pitowsky89b} [[Itamar Pitowsky]], *Quantum Probability -- Quantum Logic*, Lecture Notes in Physics **321**, Springer (1989) &lbrack;[doi:10.1007/BFb0021186](https://doi.org/10.1007/BFb0021186)&rbrack;

* [[Luigi Accardi]], *The Probabilistic Roots of the Quantum Mechanical Paradoxes*, in: *The Wave-Particle Dualism*,  Fundamental Theories of Physics **3** Springer (1984) &lbrack;[doi:10.1007/978-94-009-6286-6_16](https://doi.org/10.1007/978-94-009-6286-6_16)&rbrack;


reviewed in:


* Elemer E Rosinger, *George Boole and the Bell inequalities* &lbrack;[arXiv:quant-ph/0406004](https://arxiv.org/abs/quant-ph/0406004)&rbrack;

* {#Khrennikov07} [[Andrei Khrennikov]], *Bell's inequality: Physics meets Probability* &lbrack;[arXiv:0709.3909](https://arxiv.org/abs/0709.3909)&rbrack;

* {#Khrennikov08} [[Andrei Khrennikov]], *Bell-Boole Inequality: Nonlocality or Probabilistic Incompatibility of Random Variables?*, Entropy **10** 2 (2008) 19-32 &lbrack;[doi:10.3390/entropy-e10020019](https://doi.org/10.3390/entropy-e10020019)&rbrack;



[[!redirects Bell's inequalities]]


[[!redirects Bell inequality]]
[[!redirects Bell inequalities]]


[[!redirects Bell's theorem]]
[[!redirects Bell's theorems]]

[[!redirects Bell theorem]]
[[!redirects Bell theorems]]

[[!redirects Bell test]]
[[!redirects Bell tests]]





