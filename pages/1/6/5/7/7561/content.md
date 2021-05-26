
# Solenoids
* table of contents
{: toc}

## Idea

A simple example of a solenoid is the dyadic solenoid.  This is the [[codirected limit|inverse limit]] of the inverse sequence, $(X(n),p_n)$, in which each $X(n)$ is a copy of the [[circle]] $S^1$ and each 'structure map' $p_n\colon X(n) \to X(n-1)$ is given by the squaring map on the circle, that is $e^{i\theta}\mapsto e^{2i\theta}$ (viewing $S^1$ as the unit circle in the [[complex plane]]).

We will restrict attention, for the moment, to the class of solenoids defined by inverse sequences of circles:


## General definition

Let $P = (r_1,\ldots, r_n,\ldots)$ be a sequence of [[prime numbers]].  The _$P$-adic-solenoid_ is the space,

$S_P = Lim (X(n),p_n,\mathbb{N})$

where for each $n$, $X(n)= S^1$ and (considering $S^1$ as the unit circle in $\mathbb{C}$), $p_n(z) = z^{r_n}$.

The $P$-adic solenoid is a [[compact space|compact]], [[connected space|connected]] [[topological group]].


## Solenoids and shape

In [[shape theory]], the solenoids provide good examples of _non-stable spaces_. If one takes the [[Čech fundamental group]] of $S_P$, then it is the limit of the inverse sequence of the [[fundamental groups]] of the $X(n)$ together with the induced homomorphisms. It thus is trivial as it contains all integers that are divisible by all the primes in the sequence, and that an infinite number of times! The Strong Shape fundamental group of $S_P$ is not trivial as it involves the first derived functor $Lim^{(1)}$ of the inverse sequence of groups as well.

## Related concepts

* [[decimal number#solenoid]]

## References

For solenoids in many settings, see the [Wikipedia page](http://en.wikipedia.org/wiki/Solenoid_%28mathematics%29), which also has some very neat graphics!

For solenoids and shape, references include:

* [[K. Borsuk]], _Theory of Shape_, Monografie Matematyczne Tom 59,Warszawa 1975.

and

* [[Jean-Marc Cordier|J.-M. Cordier]] and [[Tim Porter|T. Porter]], (1989), Shape Theory: Categorical Methods of Approximation, Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008).

The subject is treated in others of the sources listed under [[shape theory]].


[[!redirects solenoid]]
[[!redirects solenoids]]
[[!redirects p-adic solenoid]]
[[!redirects p-adic solenoids]]
