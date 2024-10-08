
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Knot theory
+-- {: .hide}
[[!include knot theory - contents]]
=--
=--
=--

# The HOMFLY-PT Polynomial
* tic
{: toc}

## Idea

The HOMFLY-PT polynomial is a [[knot]] and [[link]] [[knot invariants|invariant]].  Confusingly, there are several variants depending on exactly which relationships are used to define it.  All are related by simple substitutions.


## Definition

To compute the HOMFLY-PT polynomial, one starts from an [[oriented link diagram]] and uses the following rules:

1. $P$ is an isotopy invariant (thus, unchanged by [[Reidemeister moves]]).
1. $P(\text{unknot}) = 1$
1. Let $L_+$, $L_-$, and $L_0$ be links which are the same except for one part where they differ according to the diagrams below.  Then, depending on the choice of variables:

   1. $l \cdot P(L_+) + l^{-1} \cdot P(L_-) + m \cdot P(L_0) = 0$.
   1. $a \cdot P(L_+) - a^{-1} \cdot P(L_-) = z \cdot P(L_0)$.  (Sometimes $\nu$ is used instead of $a$)
   1. $\alpha^{-1} \cdot P(L_+) - \alpha \cdot P(L_-) = z \cdot P(L_0)$.
   1. Using *three* variables: $x \cdot P(L_+) + y \cdot P(L_-) + z \cdot P(L_0) = 0$.

   $$
   \begin{array}{ccc}
   \begin{svg}[[!include SVG skein positive crossing]]\end{svg} &
   \begin{svg}[[!include SVG skein negative crossing]]\end{svg} &
   \begin{svg}[[!include SVG skein no crossing]]\end{svg} \\
   L_+ & L_- & L_0
   \end{array}
   $$

From the rules, one can read off the relationships between the different formulations:

1. $y = \alpha = a^{-1}$
1. $x = - \alpha^{-1} = -a$
1. $a = - i l$, $l = i a$
1. $z = i m$, $m = - i z$.


## Properties

The HOMFLY polynomial generalises both the [[Jones polynomial]] and the [[Alexander polynomial]] (equivalently, the [[Conway polynomial]]).

* To get the [[Jones polynomial]], make one of the following substitutions:

  1. $a = q^{-1}$ and $z = q^{1/2} - q^{-1/2}$
  1. $\alpha = q$ and $z = q^{1/2} - q^{-1/2}$
  1. $l = i q^{-1}$ and $m = i (q^{-1/2} - q^{1/2})$

* To get the [[Conway polynomial]], make one of the following substitutions:

  1. $a = 1$
  1. $\alpha = 1$
  1. $l = i$, $m = -i z$

* To get the [[Alexander polynomial]], make one of the following substitutions:

  1. $a = 1$, $z = q^{1/2} - q^{-1/2}$
  1. $\alpha = 1$, $z = q^{1/2} - q^{-1/2}$
  1. $l = i$, $m = i (q^{-1/2} - q^{1/2})$


## Related entries

* [[Shum's theorem]]


## References

See the [wikipedia page](http://en.wikipedia.org/wiki/HOMFLY_polynomial) for the origin of the name.

Some fairly elementary discussion of the HOMFLY polynomial is given in introductory texts such as 

* [[N. D. Gilbert]] and [[T. Porter]], Knots and Surfaces, Oxford U.P., 1994.

The original work was published as 

*   [[P. Freyd]], [[D. Yetter]], J.  Hoste,  W.B.R. Lickorish, K. Millett, and [[A. Ocneanu]]. (1985). _A New Polynomial Invariant of Knots and Links_ Bulletin of the American Mathematical Society 12 (2): 239&#8211;246.

More recent work includes:

* A.Mironov, A.Morozov, An.Morozov, _Character expansion for HOMFLY polynomials. I. Integrability and difference equations_, [arxiv/1112.5754](http://arxiv.org/abs/1112.5754)
* Hugh Morton, Peter Samuelson, _The HOMFLYPT skein algebra of the torus and the elliptic Hall algebra_, [arxiv/1410.0859](http://arxiv.org/abs/1410.0859)
 

category: knot theory

[[!redirects HOMFLY-PT polynomial]]
[[!redirects homfly-pt polynomial]]
[[!redirects HOMFLY polynomial]]
[[!redirects homfly polynomial]]
[[!redirects HOMFLY-PT]]
[[!redirects homfly-pt]]
[[!redirects HOMFLY]]
[[!redirects homfly]]
