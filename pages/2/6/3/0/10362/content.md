
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


In [[quantum physics]]/[[quantum information theory]], What came to be called *Bell's inequality* ([Bell 1964](#Bell64)) is an [[inequality]] satisfied by the three pairwise [[correlation functions]] between three [[random variables]] defined on one and the same classical [[probability space]]. As such, it is an elementary statement about classical probability theory which as been argued ([Pitowsky 1989a](#Pitowsky89a)) to have been known already to [[Boole -- The Laws of Thought|Boole (1854)]].

The point of the argument by [Bell 1964](#Bell64) was to highlight that when taking these three random variables to be the results of [[quantum measurements]] of the [[spin]] of an [[electron]] along three pairwise non-orthogonal axes (as in the [[Stern-Gerlach experiment]]) then [[quantum theory]] predicts that this inequality is *violated* -- implying that there is no single classical [[probability space]] (called a *[[hidden variable theory|hidden variable]]* in the context of [[interpretations of quantum mechanics]]) on which these three [[quantum measurement]]-results are jointly [[random variables]].

A number of [[experiments]] have sought to check Bell's inequalities in [[quantum physics]] ("[[Bell tests]]") and all claim to have verified that it is indeed violated in nature (see [Aspect 2015](#Aspect15)), as predicted by [[quantum theory]].

Bell's inequality has been and is receiving an enormous amount of attention, first in discussions of [[interpretations of quantum mechanics]], but more recently and more concretely also in the context of [[quantum information theory]].


## Statement
 {#Statement}

### Original formulation
 {#OriginalFormulation}

> The following is fairly verbatim recap of the original argument in [Bell 1964](#Bell64). For a streamlined re-statement see further [below](#CompactReformulation).

Let us denote the result _A_ of a measurement that is determined by a unit vector, $\vec{a}$, and some parameter $\lambda$ as $A(\vec{a},\lambda)=\pm 1$ where we further suppose that the outcome of the measurement is either +1 or -1.  Likewise, we may do the same for the result _B_ of a second measurement, i.e. $B(\vec{b},\lambda)$.  We further make the vital assumption that the result _B_ does not depend on $\vec{a}$ and likewise _A_ does not depend on $\vec{b}$.

Before proceeding, we should note that $\lambda$ here plays the role of a "hidden" parameter or variable.  We say it is "hidden" because its precise nature is not known.  However, it is still a very real parameter with a probability distribution $\rho(\lambda)$.  The expectation value of the product of the two measurements is

\[
  \label{AnExpectationValue}
  P(\vec{a},\vec{b})=\int d\lambda\rho(\lambda)A(\vec{a},\lambda)B(\vec{b},\lambda).
\]

Because $\rho$ is a normalized probability distribution,

$$
  \int d\lambda \rho(\lambda) = 1
$$

and because $A(\vec{a},\lambda)=\pm 1$ and $B(\vec{b},\lambda)=\pm 1$, P cannot be less than -1.  It can be equal to -1 at $\vec{a}=\vec{b}$ only if $A(\vec{a},\lambda)=\pm 1 = -B(\vec{a},\lambda)=\pm 1$ except at a set of points $\lambda$ of zero probability.  Thus we can write (eq:AnExpectationValue) as

\[
  P(\vec{a},\vec{b})=-\int d\lambda\rho(\lambda)A(\vec{a},\lambda)A(\vec{b},\lambda).
\]

If we introduce a third unit vector $\vec{c}$ we can find the difference between the correlation of $\vec{a}$ to the two other unit vectors,

\[
  \label{DifferenceOfCorrelations}
  P(\vec{a},\vec{b})-P(\vec{a},\vec{c})=-\int d\lambda\rho(\lambda)[A(\vec{a},\lambda)A(\vec{b},\lambda)-A(\vec{a},\lambda)A(\vec{c},\lambda)].
\]

Rearranging this we may write (eq:DifferenceOfCorrelations) as

\[
  P(\vec{a},\vec{b})-P(\vec{a},\vec{c})=-\int d\lambda\rho(\lambda)A(\vec{a},\lambda)A(\vec{b},\lambda)[A(\vec{b},\lambda)A(\vec{c},\lambda)-1].
\]

Given the limitations we have placed on the value of _A_, we may write

\[
  |P(\vec{a},\vec{b})-P(\vec{a},\vec{c})| \le \int d\lambda\rho(\lambda)[1-A(\vec{b},\lambda)A(\vec{c},\lambda)].
\]

But the second term on the right is simply $P(\vec{b},\vec{c})$ and thus

\[
  1 + P(\vec{b},\vec{c}) \ge |P(\vec{a},\vec{b})-P(\vec{a},\vec{c})|
\]

which is the original form of Bell's inequality.  Note that this may be written in terms of correlation coefficients, 

\[
  1 + C(b,c) \ge |C(a,b)-C(a,c)|
\]

where _a_, _b_, and _c_ are now settings on the measurement apparatus.


#### Quantum mechanical violations

The original derivation of Bell's inequalities involved the use of a [[Stern-Gerlach device]] that measures spin along an axis.  Suppose $\sigma_{1}$ and $\sigma_{2}$ are spins.  The result, _A_, of measuring $\sigma_{1}\cdot\vec{a}$ is then interpreted as being entirely determined by $\vec{a}$ and $\lambda$.  Likewise for _B_ and $\sigma_{2}\cdot\vec{b}$.  It is also important to remember that the result _B_ does not depend on $\vec{a}$ and likewise _A_ does not depend on $\vec{b}$.

For a singlet state (that is a state with total spin of zero), the quantum mechanical expectation value of measurements along two different axes (see the Wigner derivation below for a more intuitive explanation of the physical nature of this) is

\[
  \langle\sigma_{1}\cdot\vec{a},\sigma_{2}\cdot\vec{b}\rangle = - \vec{a}\cdot\vec{b}.
\]

In theory this ought to equal $P(\vec{a},\vec{b})$ but in practice it does not.  It is important to remember that we are using _classical_ reasoning throughout our derivations of the various forms of Bell's inequalities.

The setup envisioned here consists of pairs of spin-1/2 particles produced in singlet states that then each pass through separate Stern-Gerlach (SG) devices.  Since they are in singlet states, if we measured the first particle of a pair to be aligned with a given axis, say $\vec{a}$, then the second should be measured to be anti-aligned with that same axis, giving a total spin of zero.

In practice we are dealing with _beams_ of particles and thus we can never be absolutely certain that correlated pairs are measured simultaneously and so we ultimately are making statistical predictions.  Nevertheless, in a given sample consisting of a large-enough number of randomly distributed spin-1/2 particles, we can be certain that, for example, a definite number are aligned with an axis $\vec{a}$ while a definite number are aligned with an axis $\vec{b}$.

Now take an individual particle and suppose that, for this particle, if we measured $\sigma\cdot\vec{a}$ we would obtain a +1 with certainty (meaning it is aligned with $\vec{a}$) but if we instead chose to measure $\sigma\cdot\vec{b}$ we would obtain a -1 with certainty (meaning it is anti-aligned with $\vec{b}$).  Notationally we refer to such a particle as belonging to type $(\vec{a}+,\vec{b}-)$.  Clearly for a given pair of particles in a singlet state, if particle 1 is of type $(\vec{a}+,\vec{b}-)$, then particle 2 must be of type $(\vec{a}-,\vec{b}+)$.

#### Locality

For beams of correlated particles measuring along only two axes, we should expect to get a roughly evenly balanced distribution of types as follows:

$$
\array{
\text{ Particle 1 } & & \text{ Particle 2 } \\
(\vec{a}+,\vec{b}-) & \leftrightarrow & (\vec{a}-,\vec{b}+) \\
(\vec{a}+,\vec{b}+) & \leftrightarrow & (\vec{a}-,\vec{b}-) \\
(\vec{a}-,\vec{b}-) & \leftrightarrow & (\vec{a}+,\vec{b}+) \\
(\vec{a}-,\vec{b}+) & \leftrightarrow & (\vec{a}+,\vec{b}-)
}
$$

There is a very important assumption implied here.  Suppose a particular pair belongs to the first grouping, that is if an observer _A_ decides to measure the spin along $\vec{a}$ for particle 1, he or she _necessarily_ obtains a plus sign (corresponding to it being aligned with $\vec{a}$) _regardless_ of any measurement observer _B_ may make on particle 2.  This is the principle of locality: _A_'s result is predetermined independently of _B_'s choice of what to measure.

#### Wigner's derivation

Now suppose we introduce a third axis, $\vec{c}$, so that we can have, for example, particles of type $(\vec{a}+,\vec{b}+,\vec{c}-)$ corresponding to being aligned if measured on $\vec{a}$ and $\vec{b}$ and anti-aligned on $\vec{c}$.  Further let us "count" the pairs that fall into the various groupings and label the populations as follows:


$$
\array{
\text{ Population } & \text{ Particle 1 } & \text{ Particle 2 } \\
N_{1} & (\vec{a}+,\vec{b}+, \vec{c}+) & (\vec{a}-,\vec{b}-,\vec{c}-) \\
N_{2} & (\vec{a}+,\vec{b}+, \vec{c}-) & (\vec{a}-,\vec{b}-,\vec{c}+) \\
N_{3} & (\vec{a}+,\vec{b}-, \vec{c}+) & (\vec{a}-,\vec{b}+,\vec{c}-) \\
N_{4} & (\vec{a}+,\vec{b}-, \vec{c}-) & (\vec{a}-,\vec{b}+,\vec{c}+) \\
N_{5} & (\vec{a}-,\vec{b}+, \vec{c}+) & (\vec{a}+,\vec{b}-,\vec{c}-) \\
N_{6} & (\vec{a}-,\vec{b}+, \vec{c}-) & (\vec{a}+,\vec{b}-,\vec{c}+) \\
N_{7} & (\vec{a}-,\vec{b}-, \vec{c}+) & (\vec{a}+,\vec{b}+,\vec{c}-) \\
N_{8} & (\vec{a}-,\vec{b}-, \vec{c}-) & (\vec{a}+,\vec{b}+,\vec{c}+)
}
$$

Let's suppose that observer _A_ finds particle 1 is aligned with $\vec{a}$, i.e. $\vec{a}+$, and that observer _B_ finds particle 2 is aligned with $\vec{b}$, i.e. $\vec{b}+$.  From the above table it is clear that the pair belong to either population 3 or 4.  Note that because $N_{i}$ is positive semi-definite we must be able to construct relations like, for instance,

\[
  \label{APositivityCondition}
  N_{3} + N_{4} \le (N_{3} + N_{7}) + (N_{4} + N_{2}).
\]

Now let $P(\vec{a}+;\vec{b}+)$ be the probability that, in a random selection, _A_ finds particle 1 to be $\vec{a}+$ and _B_ finds particle 2 to be $\vec{b}+$.  In terms of populations, we have

\[
  \label{Populations1}
  P(\vec{a}+;\vec{b}+) = \frac{(N_{3} + N_{4})}{\sum_{i}^{8}N_{i}}.
\]

Similarly we have

\[
  \label{Populations2}
  P(\vec{a}+;\vec{c}+) = \frac{(N_{2} + N_{4})}{\sum_{i}^{8}N_{i}}
\]

and

\[
  \label{Populations3}
  P(\vec{c}+;\vec{b}+) = \frac{(N_{3} + N_{7})}{\sum_{i}^{8}N_{i}}.
\]

The positivity condition (eq:APositivityCondition) then becomes

\[
  \label{WignerFormOfBellInequality}
  P(\vec{a}+;\vec{b}+) \le P(\vec{a}+;\vec{c}+) + P(\vec{c}+;\vec{b}+).
\]

This is Wigner's form of Bell's inequality.

#### Violations and geometry

As we mentioned before, we have used purely classical reasoning to derive the two forms of Bell's inequality that we have thusfar encountered.  Recall that the context within which the above were derived was the Stern-Gerlach experiment are we are measuring along axes of the magnetic field.  As such, there are angles between these various axes.  Thus the quantum mechanically-derived probabilities corresponding to (eq:Populations1), (eq:Populations2), and (eq:Populations3) are

$$
  P(\vec{a}+;\vec{b}+) = \frac{1}{2}sin^{2}\left(\frac{\theta_{ab}}{2}\right),
$$

$$
  P(\vec{a}+;\vec{c}+) = \frac{1}{2}sin^{2}\left(\frac{\theta_{ac}}{2}\right),
$$

and

$$
  P(\vec{c}+;\vec{b}+) = \frac{1}{2}sin^{2}\left(\frac{\theta_{cb}}{2}\right),
$$

respectively.  Bell's inequality, (eq:WignerFormOfBellInequality), then becomes

\[
  \label{AnotherFormOfBellInequality}
  \frac{1}{2}sin^{2}\left(\frac{\theta_{ab}}{2}\right) \le \frac{1}{2}sin^{2}\left(\frac{\theta_{ac}}{2}\right) + \frac{1}{2}sin^{2}\left(\frac{\theta_{cb}}{2}\right).
\]

From a geometric point of view, this inequality is not always possible.  For example, suppose, for simplicity that $\vec{a}$, $\vec{b}$, and $\vec{c}$ lie in a plane and suppose that $\vec{c}$ bisects $\vec{a}$ and $\vec{b}$, i.e.

$$
\array{
  \theta_{ab} = 2\theta & \text{ and } & \theta_{ac}=\theta_{cb}=\theta.
}
$$

Then (eq:AnotherFormOfBellInequality) is violated for $0 \lt \theta \lt \frac{\pi}{2}$.  For example, if $\theta = \frac{\pi}{4}$, (eq:AnotherFormOfBellInequality) would become $0.500 \le 0.292$ which is absurd!



### Compact reformulation
 {#CompactReformulation}

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

* [[Grothendieck inequality]]

* [[quantum probability]]

* [[interpretation of quantum mechanics]]

* [[quantum information theory]]

Other theorems about the foundations and [[interpretation of quantum mechanics]] include:

* [[order-theoretic structure in quantum mechanics]]

  * [[Kochen-Specker theorem]]

  * [[Alfsen-Shultz theorem]]

  * [[Harding-Döring-Hamhalter theorem]]

* [[Fell's theorem]]

* [[Gleason's theorem]]

* [[Wigner theorem]]

* [[Bub-Clifton theorem]]

* [[Kadison-Singer problem]]




## References

### General

The original article:

* {#Bell64} [[John Bell]], *On the Einstein Podolsky Rosen paradox*, Physics **1** 195 (1964) &lbrack;[doi:10.1103/PhysicsPhysiqueFizika.1.195](https://doi.org/10.1103/PhysicsPhysiqueFizika.1.195), [pdf](http://www.drchinese.com/David/Bell_Compact.pdf)&rbrack;

Relation to the [[Kochen-Specker theorem]]:

* [[N. David Mermin]], *Hidden Variables and the Two Theorems of John Bell*, Reviews of Modern Physics **65** (1993) 803-815 &lbrack;[doi:10.1103/RevModPhys.65.803](https://doi.org/10.1103/RevModPhys.65.803), [arXiv:1802.10119](https://arxiv.org/abs/1802.10119)&rbrack;


  
Introduction and review:

* [[John F. Clauser]], [[Abner Shimony]], *Bell's theorem. Experimental tests and implications*, Rep. Prog. Phys. **41** (1978) 1881 &lbrack;[doi:10.1088/0034-4885/41/12/002](https://iopscience.iop.org/article/10.1088/0034-4885/41/12/002)&rbrack;

* {#Kuperberg05} [[Greg Kuperberg]], section 1.6.2 of: _A concise introduction to quantum probability, quantum mechanics, and quantum computation_ (2005) &lbrack;[pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf), [[Kuperberg-ConciseQuantum.pdf:file]]&rbrack;

* [[Valter Moretti]], Thm. 4.49 of: *Fundamental Mathematical Structures of Quantum Theory*, Springer (2019) &lbrack;[doi:10.1007/978-3-030-18346-2](https://doi.org/10.1007/978-3-030-18346-2)&rbrack;

* M.S.Guimaraes, I. Roditi, S.P. Sorella: *Introduction to Bell's inequality in Quantum Mechanics* &lbrack;[arXiv:2409.07597](https://arxiv.org/abs/2409.07597)&rbrack;


and on a background of [[quantum logic]]:

* Laura Molenaar, *Quantum logic and the EPR paradox*, Delft (2014) &lbrack;[uuid:cfee567c-425a-4b2d-9550-f7d7eea41b8b](http://resolver.tudelft.nl/uuid:cfee567c-425a-4b2d-9550-f7d7eea41b8b)&rbrack;


Further on experimental verification:

* {#Aspect15} [[Alain Aspect]], *[Closing the Door on Einstein and Bohr’s Quantum Debate](https://physics.aps.org/articles/v8/123)*, Physics **8** 123 (2015)

Relation to the [[Kochen-Specker theorem]]:

* [[Leandro Aolita]], Rodrigo Gallego, Antonio Acín, Andrea Chiuri, Giuseppe Vallone, Paolo Mataloni, Adán Cabello, *Fully nonlocal quantum correlations*, Phys. Rev. A **85** 032107 (2012) &lbrack;[arXiv:1105.3598](https://arxiv.org/abs/1105.3598), [doi:10.1103/PhysRevA.85.032107](https://doi.org/10.1103/PhysRevA.85.032107)&rbrack;

    


See also:

* Wikipedia, _[Bell's theorem](http://en.wikipedia.org/wiki/Bell_inequality)_

* Wikipedia, *[Bell test](https://en.wikipedia.org/wiki/Bell_test)*

* Wikipedia, *[Leggett-Garg inequality](https://en.wikipedia.org/wiki/Leggett%E2%80%93Garg_inequality)*

* Stanford Encyclopedia of Philosophy, _Bell's theorem_ ([url](http://plato.stanford.edu/entries/bell-theorem/))


In relation to the [[Grothendieck inequality]]:

* [[Boris S. Tsirelson]], *Quantum analogues of the Bell inequalities. The case of two spatially separated domains*, Journal of Soviet Mathematics **36** (1987) 557–570 &lbrack;[doi:10.1007/BF01663472](https://doi.org/10.1007/BF01663472)&rbrack;

* [[Boris S. Tsirelson]], *Some results and problems on quantum Bell-type inequalities* Hadronic Journal Supplement **8** 4 (1993) 329-345 &lbrack;[pdf](https://www.tau.ac.il/~tsirel/download/hadron.pdf), [[Tsirelson-QuantumBellType.pdf:file]] [web](https://www.tau.ac.il/~tsirel/download/hadron.html)&rbrack;

  > (but see the erratum [here](https://www.tau.ac.il/~tsirel/Research/bellopalg/main.html))

* Wikipedia, *[Tsirelson's bound](https://en.wikipedia.org/wiki/Tsirelson%27s_bound)*

### In quantum field theory

In the generality of ([[relativistic field theory|relativistic]]) [[quantum field theory]]:

* M. S. Guimaraes, I. Roditi, S. P. Sorella: *Bell's inequality in relativistic Quantum Field Theory* &lbrack;[arXiv:2410.19101](https://arxiv.org/abs/2410.19101)&rbrack;



On Bell inequalities in [[particle physics]] and possible relation to the [[weak gravity conjecture]]:

* Aninda Sinha, Ahmadullah Zahed, *Bell inequalities in 2-2 scattering* &lbrack;[arXiv:2212.10213](https://arxiv.org/abs/2212.10213)&rbrack;

On [[BRST complex|BRST invariant]] Bell inequality in [[gauge field theory]]:

* David Dudal, Philipe De Fabritiis, Marcelo S. Guimaraes, Giovani Peruzzo, Silvio P. Sorella: *BRST invariant formulation of the Bell-CHSH inequality in gauge field theories* &lbrack;[arXiv:2304.01028](https://arxiv.org/abs/2304.01028)&rbrack;



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






