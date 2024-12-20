
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Two [[generalized homology theories]] $E_\bullet$, $F_\bullet$, hence [[spectra]] $E$, $F$ are called _Bousfield equivalent_ if the [[homology groups]] of both always vanish simultaneously, hence if for every [[homotopy type]]/[[spectrum]] $X$ we have $E_\bullet(X) \simeq 0$ precisely if $F_\bullet(X) \simeq 0$.

## Examples

### Global arithmetic fracture square

There is a Bousfield equivalence 

$$
  S (\mathbb{Q}/\mathbb{Z}) \simeq_{Bousf} \vee_p S \mathbb{F}_p
$$

between the [[Moore spectrum]] of the quotient $\mathbb{Q}/\mathbb{Z}$ and the [[coproduct]] of the Moore spectra of all [[cyclic groups]]/[[finite fields]] of [[prime]] order (e.g. [Strickland 12, MO comment](http://mathoverflow.net/a/91057/381)).

This governs the global [[fracture theorem|arithmetic fracture theorem]] [in stable homotopy theory](fracture+theorem#InStableHomotopyTheory).


### Morava E-theory and Morava K-theory

For all $n$, the $n$th [[Morava E-theory]] $E(n)$ is [[Bousfield equivalence|Bousfield equivalence]] to $E(n-1) \times K(n)$, where the last factor is $n$th [[Morava K-theory]].

([Lurie 10, lect. 23, prop. 1](#LurieLect23))


## References

The concept of Bousfield classes is due to (see at [[Bousfield localization of spectra]])

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_ , Topology vol 18 (1979) ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

and was named such in

* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf)) 

Discussion in the context of [[higher algebra]] is in

* {#LurieLect23} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010; Lecture 23 _The Bousfield Classes of $E(n)$ and $K(n)$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture23.pdf))
 

[[!redirects Bousfield equivalences]]

