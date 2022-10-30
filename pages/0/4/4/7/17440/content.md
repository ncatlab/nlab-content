
> This entry is about the classical Adams spectral sequence only. For more general discussion see at _[[Adams spectral sequence]]_.

> under construction

#Contents#
* table of contents
{:toc}

## Idea

The _classical Adams spectral sequence_ ([Adams 58](#Adams58)) is a type of [[spectral sequences]] used for computations  in [[stable homotopy theory]]. It computes the [[homotopy groups of spheres]] at prime 2 from   [[homology]]/[[cohomology]], as [[modules]]/[[comodules]] over its [[Steenrod operations]]. The Adams spectral sequence may be seen as a variant of the [[Serre spectral sequence]] obtained by replacing a single fibration by an "[[Adams resolution]]". 

The original _clasical Adams spectral sequenc_ for [[ordinary cohomology]] is further refined by the _[[Adams-Novikov spectral sequence]]_ ([Novikov 67](#Novikov67)) by replacing [[ordinary cohomology]] modulo $p$ by [[complex cobordism cohomology theory]] or [[Brown-Peterson theory]] or the like. 

Generally, for $E$ a suitable [[E-infinity algebra]] there is a corresponding _$E$-[[Adams spectral sequence]]_ whose second page is given by $E$-[[generalized cohomology]] and which arises as the [[spectral sequence of a simplicial stable homotopy type]] of the [[cosimplicial object|cosimplicial]] object which is the [[Cech nerve]]/[[Sweedler coring]]/[[Amitsur complex]] of $E$. As such the Adams spectral sequence is an analog in [[stable homotopy theory]] of the [[Bousfield-Kan spectral sequence|Bousfield-Kan]] [[homotopy spectral sequence]] in unstable [[homotopy theory]].


### Via iterated Hurewicz theorem and Serre spectral sequence
 {#MotivationFromHurewiczTheoremAndSerreSpectralSequence}

The classical Adams spectral sequence may be motivated from the strategy to 
compute [[homotopy groups]] from [[cohomology groups]] by subsequently applying the [[Hurewicz theorem]] to compute the lowest-degree non-trivial homotopy group from the corresponding [[cohomology group]], then co-killing that by forming its [[homotopy fiber]], finally applying the [[Serre spectral sequence]] to  identify the next lowest non-trivial cohomology group of that fiber, and then iterating this process. The Adams spectral sequence arises when in this kind of strategy instead of co-killing only the lowest lying [[cohomology group]], one at a time, one co-kills _all_ nontrivial cohomology groups, then forms the corresponding [[homotopy fiber]] and so on.

This was apparently historically the way that [[John Adams]] indeed proceeded from [[Jean-Pierre Serre]]'s approach and this is still a good motivation for the whole construction. A nice exposition is in  ([Wilson 13, 1.1](#Wilson13)).

We now say this again in more detail.

Given $n \in \mathbb{N}$, consider the probem of computing the [[homotopy groups of spheres|homotopy groups]] $\pi_k(S^n) \;mod \;2$ of the [[n-sphere]] $S^n$. For $k \leq n$ this is clear: first for $k \lt n$ they all vanish, and second for $k = n$ we have, by the very nature of [[Eilenberg-MacLane spaces]] $K(\mathbb{Z}_2, n)$, that the [[ordinary cohomology]] is

$$
  H^n(S^n, \mathbb{Z}_2) \simeq [S^n, K(\mathbb{Z}_2,n)] \simeq \pi_n(K(\mathbb{Z}_2,n)) \simeq \mathbb{Z}_2
$$

so that by the [[Hurewicz theorem]] it follows that also

$$
  \pi_n(S^n) \;mod\;2 \;\simeq \mathbb{Z}_2
  \,.
$$

The [[Hurewicz theorem]] does not say anything beyond the first non-vanishing cohomology group, but so to apply it again we can move up one step in the [[Whitehead tower]] of $S^n$ and hence consider the [[homotopy fiber]]

$$
  \array{
     F_1
     \\
     \downarrow
     \\
     S^n &\stackrel{c_1}{\longrightarrow}& K(\mathbb{Z}_2,n)
  }
$$

of the generator $[c_1] = 1 \in \pi_n(S^n) \simeq \mathbb{Z}_2$.

To apply the [[Hurewicz theorem]] to that fiber we need to know its lowest non-trivial [[cohomology group]] again, and this is computed via the [[Serre spectral sequence]] applied to this [[fiber sequence]]. 

From here on the process repeats, and one moves higher through the [[Whitehead tower]] of $S^n$


$$
  \array{
     \vdots
     \\
     \downarrow
     \\
     F_1 &\stackrel{c_2}{\longrightarrow}& K(\mathbb{Z}_2, n+1)
     \\
     \downarrow
     \\
     S^n &\stackrel{c_1}{\longrightarrow}& K(\mathbb{Z}_2,n)
  }
  \,.
$$

The Adams spectral sequence arises from this strategy by co-killing not just the first non-trivial [[cohomology group]] at each stage, but _all_ nontrivial cohomology groups at a given stage.

This is done in [[stable homotopy theory]], so let now $X$ be a [[spectrum]] (for instance the [[sphere spectrum]] $X = \mathbb{S}$ if we still with the computation of the [[stable homotopy groups of spheres]]). Write $H \mathbb{F}_2$ for the [[Eilenberg-MacLane spectrum]] for [[ordinary cohomology]] with [[coefficients]] in $\mathbb{Z}_2$, so that an element in [[cohomology]]

$$
  [c] \in H^n(X) 
$$

is represented by the [[homotopy class]] of a [[homomorphism]] of [[spectra]] of the form

$$
  c \;\colon\;  X \longrightarrow \Sigma^n H\mathbb{F}_2
$$

(a [[cocycle]]), where "$\Sigma$" denotes [[suspension]], as usual.

If $X$ is a [[spectrum]] of [[finite type]] then there is a [[finite]] $I$ of non-trivial cohomology classes like this, and a choice of [[cocycles]] $c_i$ for each of them gives a single map

$$
  f_0 
    \coloneqq 
   (c_i)_I \;\colon\; 
   X \longrightarrow K_0 \coloneqq \bigvee_{i \in I} \Sigma^{n_i}H \mathbb{F}_2
$$

into a [[generalized Eilenberg-MacLane spectrum]]. As before, this map classifies its [[homotopy fiber]]

$$
  \array{
    F_1
    \\
    \downarrow
    \\
     X &\stackrel{f_0}{\longrightarrow}& K_0
  }
$$

which may be thought of as encoding all information about $X$ beyond its [[cohomology groups]]. Iterating this process gives the corresponding analog of the [[Whitehead tower]], called the _[[Adams resolution]]_ of $X$:

$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    F_2 &\stackrel{f_2}{\longrightarrow}& K_2
    \\
    \downarrow
    \\
    F_1 &\stackrel{f_1}{\longrightarrow}& K_1
    \\
    \downarrow
    \\
     X &\stackrel{f_0}{\longrightarrow}& K_0
  }
  \,.
$$

The _Adams spectral sequence_ is that induced by the [[exact couple]] obtained by applying $\pi_\bullet$ to this [[Adams resolution]].

We now say this more in detail.

The [[long exact sequences of homotopy groups]] for all the [[homotopy fibers]] in this diagram arrange into a diagram of the form

$$
  \array{
    \vdots
    \\
    \downarrow & \nwarrow
    \\
    \pi_\bullet(F_2) &\stackrel{\pi_\bullet(f_2)}{\longrightarrow}& \pi_\bullet(K_2)
    \\
    \downarrow & \nwarrow^{\mathrlap{\partial_2}}
    \\
    \pi_\bullet(F_1) &\stackrel{\pi_\bullet(f_1)}{\longrightarrow}& \pi_\bullet(K_1)
    \\
    \downarrow & \nwarrow^{\mathrlap{\partial_1}}
    \\
    \pi_\bullet(X) &\stackrel{\pi_\bullet(f_0)}{\longrightarrow}& \pi_\bullet(K_0)
  }
  \,,
$$

where the diagonal maps are the [[connecting homomorphisms]] and hence decrease degree in $\pi_\bullet$ by one.
The idea now is to compute the [[homotopy groups]] of $X$ from the decomposed information in this diagram as follows.

First, by construction the homotopy groups $\pi_\bullet(K_s)$ are known, therefore we can identify elements 

$$
  \sigma \in \pi_\bullet(X)
$$

if they come from elements 

$$
  \sigma_s \in \pi_\bullet(X_s)
$$

whose image 

$$
  \pi_\bullet(f_s)(\sigma_s) \in \pi_\bullet(K_s)
$$

we understand. So the task is to understand the image of $\pi_\bullet(f_s)$ in $\pi_\bullet(K_s)$, for each $s$.

By [[exact sequence|exactness]] an element $\kappa_s \in \pi_\bullet(K_s)$ is in this image if its image 

$$
  \rho_{s+1} \coloneqq \partial(\kappa_s) \in \pi_{\bullet-1}(X_{s+1})
$$

vanishes. Now, by construction of the resolution, "evidence" for this is that $f_{s+1}(\partial(\kappa_s)) \in \pi_{\bullet-1}(K_{s+1})$ vanishes, which in turn by [[exact sequence|exactness]] means equivalently that $\partial(\kappa_s)$ is the image of an element  $\rho_{s+2} \in  \pi_{\bullet-1}(X_{s+2}) \to \pi_{\bullet-1}(X_{s+1})$. Now again "evidence" for $\rho_{s+2}$ to vanish is that its image $f_{s+2}(\rho(s+2))$ vanishes, which again means that it comes from an element $\rho_{s+3} \in  \pi_{\bullet-1}(X_{s+3}) \to \pi_{\bullet-1}(X_{s+2})$.

Proceeding by [[induction]] this way, we find that accumulated "evidence" in homotopy groups of $K_\bullet$ for an element $\kappa_s$ to represent an element in $\pi_\bullet(X)$ is that its differential $\partial \kappa_s$ factors through all the $\pi_{\bullet-1}(X_{s+k}) \to \pi_{\bullet-1}(X_s)$. This in turn means that it factors through the [[inverse limit]] $\underset{\leftarrow}{\lim}_s \pi_{\bullet-1}(X_s)$.
Such an element $\kappa_s$ with 

$$
  \partial \kappa_s \in \underset{\leftarrow}{\lim}_s \pi_{\bullet-1}(X_s) \to \pi_{\bullet-1}(X_{s+1})
$$

is called a _permanent cycle_.

In good cases, the [[Adams resolution]] is indeed a [[resolution]] which means that  the [[inverse limit]] $\underset{\leftarrow}{\lim}_s X_s $ is in fact [[contractible]]. This means that all the "evidence" accumulated in a permanent cycle is indeed sufficient evidence to prove the existence of an element $\sigma_s \in \pi_\bullet(X_s)$ and hence of an element $\sigma \in \pi_\bullet(X)$.


A trivial way for this to be the case is that the original $\sigma_s$ is itself in the image under $\partial$ of some element, in which case $\kappa_s = 0$ already all by itself. These elements are called _eventual boundaries_. Therefore if the Adams resolution is indeed a resolution, then the quotient group

$$
  \frac{permanent\;cycles}{eventual\;boundaries}
$$

gives elements in $\pi_\bullet(S)$, and this quotient is what the Adams spectral sequence computes.


## Properties

### Generators in low range

For the moment see at _[[May spectral sequence]]_.


### Further

$h_j$ is a permanent cycle in the Adams spectral sequence if $\mathbb{R}^{(2^j)}$ admits the structure of a real [[division algebra]]

Adams: ...

$$
  d_2(h_{j+1}) = h_0 h_j^2
$$


Mahowald-Tangora: $h_4^2$ is a permanent cycle

Barratt-Jones-Mahowald: $h_5^2$ is a permanent cycle

Hill-Hopkins-Ravenel: for $j \gt 7$ then $h_j^2$ is not a permanent cycle.

## Related concepts

* [[May spectral sequence]], [[Curtis algorithm]]

* [[Adams-Novikov spectral sequence]]

## References

The original article is

* {#Adams58} [[Frank Adams]], _On the structure and applications of the Steenrod algebra_, Comm. Math. Helv. 32 (1958), 180&#8211;214.

Textbook accounts proceeding in the [[coalgebra]] picture include

* [[Doug Ravenel]], chapter 3 of _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986/2003

* {#Kochman96} [[Stanley Kochman]], chapter 5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

Further review includes

* [[John McCleary]], chapter 9 of _A User's Guide to Spectral Sequences_, Cambridge University Press (1985, 2001)

* {#Bruner09} [[Robert Bruner]], _An Adams spectral sequence primer_, 2009 ([pdf](http://www.math.wayne.edu/~rrb/papers/adams.pdf))

* {#Rognes12} [[John Rognes]], _The Adams spectral sequence_ (following [Bruner 09](#Bruner09)), 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

and

* [[Alexander Kupers]], _An introduction to the Adams spectral sequence_ (following [Rognes 12](#Rognes12)) ([pdf](http://math.stanford.edu/~kupers/adamsss.pdf))

* Paolo Masulli, _Stable homotopy and the Adams spectral sequence_ ([pdf](http://www.math.ku.dk/~jg/students/masulli.msproject.2011.pdf))

* [pdf](http://www.math.harvard.edu/~sia/notes/classical_topology_adams.pdf)

