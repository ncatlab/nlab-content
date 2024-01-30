
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Bayes rule#
* table of contents
{:toc}

## Statement

In [[probability theory]], the __Bayes Rule__ (or _Bayes\'s Law_, _Bayes\' Theorem_, or another permutation) is the statement that the [[conditional probabilities]] $P(H\vert E)$ for an event $H$, assuming an event $E$ is related to the condition probability $P(E\vert H)$ of $E$ assuming $H$, and the plain probabilities $P(H)$ and $P(E)$ for $H$ and $E$ separately, by

$$ 
  P(H|E) \;=\; \frac{P(E|H) P(H)} {P(E)}
  \,.
$$

This follows directly from the defining formula $P(A|B) = P(A \wedge B)/P(B)$ for [[conditional probability]].  The rule may also be written in the expanded form

$$ P(H|E) = \frac{P(E|H) P(H)} {P(E|H) P(H) - P(E|\neg{H}) P(H) + P(E|\neg{H})} ,$$

which additionally uses some of the axioms of probability, or somewhere in between these two forms.

As a theorem, it is quite trivial; the point is in its application as a rule for updating the probability of some hypothesis ($H$) on the basis of some evidence ($E$) (which is key to [[Bayesianism]]), using the _prior_ probability of the hypothesis before the evidence is obtained ($P(H)$) and (in the expanded form) the conditional probabilities of obtaining that evidence in the situation where the hypothesis is true ($P(E|H)$) and in the situation where the hypothesis is false ($P(E|\neg{H})$).  (Ideally, the last two can be determined on a purely theoretical basis, but since the probability of $E$ usually depends on other hypotheses of unknown veracity, the application is not always so simple.)

## Applications

### In quantum physics

In [[quantum mechanics]], the [[collapse of the wavefunction]] may be seen as a generalization of Bayes\'s Rule to [[quantum probability theory]].  This is key to the [[Bayesian interpretation of quantum mechanics]].


[[!redirects Bayes Rule]]
[[!redirects Bayes rule]]
[[!redirects Bayes' Rule]]
[[!redirects Bayes' rule]]
[[!redirects Bayes's Rule]]
[[!redirects Bayes's rule]]

[[!redirects Bayes Law]]
[[!redirects Bayes law]]
[[!redirects Bayes' Law]]
[[!redirects Bayes' law]]
[[!redirects Bayes's Law]]
[[!redirects Bayes's law]]

[[!redirects Bayes Theorem]]
[[!redirects Bayes theorem]]
[[!redirects Bayes' Theorem]]
[[!redirects Bayes' theorem]]
[[!redirects Bayes's Theorem]]
[[!redirects Bayes's theorem]]

[[!redirects Bayes' formula]]
[[!redirects Bayes' formulas]]


[[!redirects Bayes's formula]]
[[!redirects Bayes's formulas]]

