
> This entry needs to be merged with *[[Bell's inequalities]]*. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Bell's theorem_ is the collective name for a family of results, all showing the impossibility of a Local Realistic ([[hidden variable]]) [[interpretation of quantum mechanics]].  As such, it is a form of a [[no-go theorem]] and is related to

* the [[Kochen-Specker theorem]] and

* [[Gleason's theorem]].

### Statement

(...)

### Quantum mechanical violations

The original derivation of Bell's inequalities involved the use of a [[Stern-Gerlach device]] that measures spin along an axis.  Suppose $\sigma_{1}$ and $\sigma_{2}$ are spins.  The result, _A_, of measuring $\sigma_{1}\cdot\vec{a}$ is then interpreted as being entirely determined by $\vec{a}$ and $\lambda$.  Likewise for _B_ and $\sigma_{2}\cdot\vec{b}$.  It is also important to remember that the result _B_ does not depend on $\vec{a}$ and likewise _A_ does not depend on $\vec{b}$.

For a singlet state (that is a state with total spin of zero), the quantum mechanical expectation value of measurements along two different axes (see the Wigner derivation below for a more intuitive explanation of the physical nature of this) is

\[
  \langle\sigma_{1}\cdot\vec{a},\sigma_{2}\cdot\vec{b}\rangle = - \vec{a}\cdot\vec{b}.
\]

In theory this ought to equal $P(\vec{a},\vec{b})$ but in practice it does not.  It is important to remember that we are using _classical_ reasoning throughout our derivations of the various forms of Bell's inequalities.

The setup envisioned here consists of pairs of spin-1/2 particles produced in singlet states that then each pass through separate Stern-Gerlach (SG) devices.  Since they are in singlet states, if we measured the first particle of a pair to be aligned with a given axis, say $\vec{a}$, then the second should be measured to be anti-aligned with that same axis, giving a total spin of zero.

In practice we are dealing with _beams_ of particles and thus we can never be absolutely certain that correlated pairs are measured simultaneously and so we ultimately are making statistical predictions.  Nevertheless, in a given sample consisting of a large-enough number of randomly distributed spin-1/2 particles, we can be certain that, for example, a definite number are aligned with an axis $\vec{a}$ while a definite number are aligned with an axis $\vec{b}$.

Now take an individual particle and suppose that, for this particle, if we measured $\sigma\cdot\vec{a}$ we would obtain a +1 with certainty (meaning it is aligned with $\vec{a}$) but if we instead chose to measure $\sigma\cdot\vec{b}$ we would obtain a -1 with certainty (meaning it is anti-aligned with $\vec{b}$).  Notationally we refer to such a particle as belonging to type $(\vec{a}+,\vec{b}-)$.  Clearly for a given pair of particles in a singlet state, if particle 1 is of type $(\vec{a}+,\vec{b}-)$, then particle 2 must be of type $(\vec{a}-,\vec{b}+)$.

### Locality

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

### Wigner's derivation

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
N_{3} + N_{4} \le (N_{3} + N_{7}) + (N_{4} + N_{2}).
\]

Now let $P(\vec{a}+;\vec{b}+)$ be the probability that, in a random selection, _A_ finds particle 1 to be $\vec{a}+$ and _B_ finds particle 2 to be $\vec{b}+$.  In terms of populations, we have

\[
  P(\vec{a}+;\vec{b}+) = \frac{(N_{3} + N_{4})}{\sum_{i}^{8}N_{i}}.
\]

Similarly we have

\[
  P(\vec{a}+;\vec{c}+) = \frac{(N_{2} + N_{4})}{\sum_{i}^{8}N_{i}}
\]

and

\[
  P(\vec{c}+;\vec{b}+) = \frac{(N_{3} + N_{7})}{\sum_{i}^{8}N_{i}}.
\]

The positivity condition (9) then becomes

\[
P(\vec{a}+;\vec{b}+) \le P(\vec{a}+;\vec{c}+) + P(\vec{c}+;\vec{b}+).
\]

This is Wigner's form of Bell's inequality.

### Violations and geometry

As we mentioned before, we have used purely classical reasoning to derive the two forms of Bell's inequality that we have thusfar encountered.  Recall that the context within which the above were derived was the Stern-Gerlach experiment are we are measuring along axes of the magnetic field.  As such, there are angles between these various axes.  Thus the quantum mechanically-derived probabilities corresponding to (10), (11), and (12) are

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

respectively.  Bell's inequality, (13), then becomes

\[
  \frac{1}{2}sin^{2}\left(\frac{\theta_{ab}}{2}\right) \le \frac{1}{2}sin^{2}\left(\frac{\theta_{ac}}{2}\right) + \frac{1}{2}sin^{2}\left(\frac{\theta_{cb}}{2}\right).
\]

From a geometric point of view, this inequality is not always possible.  For example, suppose, for simplicity that $\vec{a}$, $\vec{b}$, and $\vec{c}$ lie in a plane and suppose that $\vec{c}$ bisects $\vec{a}$ and $\vec{b}$, i.e.

$$
\array{
  \theta_{ab} = 2\theta & \text{ and } & \theta_{ac}=\theta_{cb}=\theta.
}
$$

Then (14) is violated for $0 \lt \theta \lt \frac{\pi}{2}$.  For example, if $\theta = \frac{\pi}{4}$, (14) would become $0.500 \le 0.292$ which is absurd!

## Related concepts


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

The original paper outlining [[Bell's theorem]] is

* J. S. Bell, _On the Einstein Podolsky Rosen Paradox_ , Physics, [pdf](http://www.drchinese.com/David/Bell_Compact.pdf).

A detailed discussion is found here:

* Stanford Encyclopedia of Philosophy, _Bell's theorem_ ([url](http://plato.stanford.edu/entries/bell-theorem/))

[[!redirects Bell theorem]]
[[!redirects Bell's theorems]]