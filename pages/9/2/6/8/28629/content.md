

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

\tableofcontents


## Idea

The *Riesz formula* expresses the [[projection operator|projection]] onto the part of a [[linear operator]] that belongs to an isolated piece of its [[spectrum of an operator|spectrum]] as a [[contour integral]] of the [[resolvent]] around that piece of the spectrum. The operator so defined is called the *Riesz projection* or *Riesz projector*.

This is the special case of the [[holomorphic functional calculus]] applied to a [[locally constant function]] which is $1$ around the selected part of the spectrum and $0$ around the rest.


## Definition

Let $A$ be a [[bounded linear operator]] on a complex [[Banach space]] $\mathcal{X}$, and suppose that its spectrum decomposes into two [[disjoint subset|disjoint]] [[closed subsets]]:
$$
  \sigma(A) 
  \;=\; 
  \sigma_\ast \,\sqcup\, \sigma_\perp
  \,.
$$
Let $\Gamma \subset \mathbb{C} \setminus \sigma(A)$ be a positively oriented [[contour]] (or finite union of contours) which encircles $\sigma_\ast$ but not $\sigma_\perp$. Then the *Riesz projection* onto $\sigma_\ast$ is
$$
  P_{\sigma_\ast}
  \;\coloneqq\;
  \frac{1}{2\pi \mathrm{i}}
  \oint_\Gamma
  (z - A)^{-1}
  \, \mathrm{d}z
  \,.
$$

(Authors using the convention $R(z) = (A - z)^{-1}$ for the resolvent have a minus sign in front of the integral.)


## Properties

+-- {: .num_prop #BasicProperties}
###### Proposition
**(basic properties)**

In the situation of the above Definition:

1. $P_{\sigma_\ast}$ does not depend on the choice of contour $\Gamma$, by the [[Cauchy integral theorem]].

1. $P_{\sigma_\ast}$ is [[idempotent]], $P_{\sigma_\ast}^2 = P_{\sigma_\ast}$, and [[commutator|commutes]] with $A$.

1. The [[direct sum]] decomposition $\mathcal{X} = \mathrm{im}(P_{\sigma_\ast}) \oplus \mathrm{ker}(P_{\sigma_\ast})$ is into closed $A$-[[invariant subspaces]], and the spectra of the corresponding restrictions of $A$ are
   $$
     \sigma\big(A\vert_{\mathrm{im}(P_{\sigma_\ast})}\big) \;=\; \sigma_\ast
     \,,
     \;\;\;\;\;
     \sigma\big(A\vert_{\mathrm{ker}(P_{\sigma_\ast})}\big) \;=\; \sigma_\perp
     \,.
   $$

1. If $\sigma_\ast = \{\lambda\}$ is an isolated [[eigenvalue]] and $P_{\sigma_\ast}$ has finite rank, then $\mathrm{im}(P_{\sigma_\ast})$ is the [[generalized eigenspace]] of $\lambda$.

=--

+-- {: .num_prop #SelfAdjointCase}
###### Proposition
**(self-adjoint case)**

If $\mathcal{X}$ is a [[Hilbert space]] and $A$ is [[self-adjoint operator|self-adjoint]] (or just [[normal operator|normal]]), then $P_{\sigma_\ast}$ is an [[orthogonal projection]], and it coincides with the [[spectral projection]] $\mathbb{1}_{\sigma_\ast}(A)$ obtained from the [[Borel functional calculus]] of the [[spectral theorem]].

=--

+-- {: .num_prop #SmoothDependence}
###### Proposition
**(smooth dependence on parameters)**

If $s \mapsto A(s)$ is a $C^k$ family of bounded operators (in the operator norm) such that the spectral splitting persists with a contour $\Gamma(s)$ which may be chosen to depend continuously on $s$, then $s \mapsto P_{\sigma_\ast(s)}$ is also $C^k$, and the rank of $P_{\sigma_\ast(s)}$ is locally constant in $s$.

=--

This is a key ingredient in the [[quantum adiabatic theorem]].

All of the above generalizes to [[closed operator|closed]] [[unbounded operators]] $A$, as long as $\sigma_\ast$ is [[bounded subset|bounded]] (e.g. [Kato 1966, §III.6.4](#Kato66)).


## Related concepts

* [[functional calculus]], [[holomorphic functional calculus]]

* [[resolvent]]

* [[spectral theorem]]

* [[quantum adiabatic theorem]]


## References

* [[Frigyes Riesz]], Béla Szőkefalvi-Nagy: *Leçons d'analyse fonctionnelle*, Akadémiai Kiadó (1952); English transl.: *Functional Analysis*, Ungar (1955), reprinted by Dover (1990)

* Nelson Dunford, Jacob T. Schwartz: §VII.3 of: *Linear Operators, Part I: General Theory*, Wiley (1958) \[<a href="https://edu.fjfi.cvut.cz/studijni-materialy/Ing/4.%20ro%C4%8Dn%C3%ADk/KFA/Nelson%20James%20Dunford,%20Jacob%20T.%20Schwartz%20-%20Linear%20Operators.%20Part%20I_%20General%20Theory%20.%20Part1-John%20Wiley%20_%20Sons%20Inc%20(1958).pdf">pdf</a>\]

* {#Kato66} [[Tosio Kato]]: §III.6.4 of: *Perturbation Theory for Linear Operators*, Grundlehren der mathematischen Wissenschaften **132**, Springer (1966, 2nd ed. 1976, reprinted 1995) &lbrack;[doi:10.1007/978-3-642-66282-9](https://doi.org/10.1007/978-3-642-66282-9)&rbrack;

[[!redirects Riesz projections]]

[[!redirects Riesz formula]]
[[!redirects Riesz formulas]]

[[!redirects Riesz projector]]
[[!redirects Riesz projectors]]
[[!redirects Riesz projection formula]]