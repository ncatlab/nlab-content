
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contenta
{:toc}

## Idea

Each [[filtered object|filtering]] on an [[object]] in a suitable [[stable (∞,1)-category]] (e.g. a [[stable homotopy type]]) induces a [[spectral sequence]] which under suitable conditions computes the [[homotopy groups]] of this object.

This is a generalization of the traditional [[spectral sequence of a filtered complex]].

## Definition


Let thoughout $\mathcal{C}$ be a [[stable (∞,1)-category]] and let $\pi_\bullet$ be a [[homological functor]] on $\mathcal{C}$ taking values in an [[abelian category]]. A typical example is when $\mathcal{C}$ is equipped with a [[t-structure]] and $\pi_\bullet$ are the corresponding homotopy groups with values in the [[heart of a stable (∞,1)-category|heart]] of the t-structure. 

+-- {: .num_example}
###### Example

For instance 

* $\mathcal{C} = Spec$  the [[stable (∞,1)-category of spectra]] with its canonical t-structure. 

=--

+-- {: .num_defn #GeneralizedFilteredObject}
###### Definition

A _generalized [[filtered object]]_ in $\mathcal{C}$ is
simply a sequential diagram $X \colon (\mathbb{Z}, \lt) \to \mathcal{C}$

$$
  \cdots
  X_{n+1} \to X_n \to X_{n-1} \to \cdots
  \,.
$$

Or rather, the object being filtered is the [[homotopy limit]]

$$
  X \coloneqq \underset{\leftarrow}{\lim}_n X_n
$$

and the sequential diagram exhibits the filtering.

=--

This appears as ([[Higher Algebra|Higher Algebra, def. 1.2.2.9]]).


+-- {: .num_defn #ExactCoupleForFilteredObject}
###### Definition

For a generalized filtered object $X_\bullet$, def. \ref{GeneralizedFilteredObject}, write 

$$
  F_n \coloneqq fib(X_n \to X_{n+1})
$$

for the [[homotopy fiber]] of the $n$th structure map, for all $n \in \mathbb{Z}$, and define an [[exact couple]]

$$
  \array{
    && \pi_\bullet(F_\bullet)
    \\
    & \swarrow && \nwarrow
    \\
    \pi_\bullet(X_\bullet)
    && 
       \stackrel{}{\longrightarrow}
    && 
    \pi_\bullet(X_\bullet)
  }
$$

where the maps are given by the [[long exact sequences of homotopy groups]]

$$
  \cdots
  \to
  \pi_\bullet(X_{n+1})
  \to 
  \pi_\bullet(F_n) \to  \pi_\bullet(X_n) \to \pi_\bullet(X_{n+1}) \to \pi_{\bullet+1}(F_n) \to \cdots
$$

=--

We now have the [[spectral sequence of a filtered stable homotopy type]].

+-- {: .num_prop #FiltrationSpectralSequence}
###### Proposition

Let $\mathcal{C}$ be a [[stable (∞,1)-category]] and let $\pi_\bullet:\mathcal{C}\to\mathcal{A}$ be a homological functor where $\mathcal{A}$ is an [[abelian category]]. 

If $\mathcal{C}$ has [[sequential limits]], if  $X_n \simeq 0$ for all $n \lt n_0$, and if some [[Mittag-Leffler condition]] holds, then the [[spectral sequence]] in $\mathcal{A}$ induced by the [[exact couple]]
of def. \ref{ExactCoupleForFilteredObject} converges to the [[homotopy groups]] of the [[homotopy limit]] $\underset{\leftarrow}{\lim}_n X_n$ of the generalized filted object:

$$
  E^{p,q}_1
  =
  \pi_{p+q} F_{p-1}
  \Rightarrow
  \pi_{p+q} (\underset{\leftarrow}{\lim} X_\bullet) 
$$

=--

This is due to ([[Higher Algebra|Higher Algebra, prop. 1.2.2.14]]). Review is in [Wilson 13, theorem 1.2.1](#Wilson13).

For the traditional statement in the [[category of chain complexes]] see at _[[spectral sequence of a filtered complex]]_.

## Examples

* [[Adams spectral sequence]]

## References

The general theory is set up in section 1.2.2 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_.

A quick exposition is for instance in section 1.2 of

* [[Dylan Wilson]] _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at [2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php) ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-03-21-Dylan-Wilson-ANSS.pdf))
 {#Wilson13}

[[!redirects spectral sequence of a filtered object in a stable (∞,1)-category]]
[[!redirects spectral sequence of a filtered object in a stable (infinity,1)-category]]

[[!redirects filtered stable homotopy type]]
[[!redirects filtered stable homotopy types]]