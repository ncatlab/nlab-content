\tableofcontents

## Definition

Recall that a [[filter]] $F$ on a [[lattice]] $L$ is called __[[prime filter|prime]]__ if $\bot \notin F$ and, whenever $x \vee y \in F$, then $x \in F$ or $y \in F$.  In other words, for every [[finite set|finite index set]] $I$, $x_k \in F$ for some $k$ whenever $\bigvee_{i\colon I} x_i \in F$.

We now generalise from finitary [[joins]] to arbitrary joins:  A filter $F$ on a [[complete lattice]] $L$ is __completely prime__ if, for any index set $I$ whatsoever, $x_k \in F$ for some $k$ whenever $\bigvee_{i\colon I} x_i \in F$.  Equivalently, a completely prime filter is given by a simultaneous [[suplattice]] and lattice [[homomorphism]] from $L$ to the lattice $TV$ of [[truth values]] (which is classically the [[boolean domain]] $\mathbb{2}$).

In particular, if $L$ is a [[frame]], then a completely prime filter of $L$ is given by a frame homomorphism from $L$ to $TV$.  Thinking of $L$ as a [[locale]], this is the same as a [[point of a locale|point]] of $L$.

## Related concepts

* [[locale]]

* [[locale of real numbers]]

* [[countably prime filter]]

* [[point of a locale]]

## References

* [[Ming Ng]], *Adelic Geometry via Topos Theory*, PhD thesis ([pdf](https://puzzledoyster.github.io/publications/FINALSUBMISSION.pdf))

[[!redirects completely prime filter]]
[[!redirects completely prime filters]]
