
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

By the general discussion at _[[equivariant K-theory]]_, given a suitable [[topological group]] $G$ with an [[action]] on a [[topological space]] $X$ there is a canonical map

$$
  K_G(X) \to K_G^{Bor}(X) \simeq K_G(X \times E G) \simeq K(X \!\sslash\! G)
$$

from the [[equivariant K-theory]] of $X$ to the ordinary [[topological K-theory]] of the [[homotopy quotient]] ([[Borel construction]]).

While this map is never an [[isomorphism]] unless $G$ is the [[trivial group]], the _Atiyah-Segal completion theorem_ says that this map exhibits $K(X \!\sslash\! G)$ as the [[formal completion]] of the [[cohomology ring]] $K_G(X)$ at the [[augmentation ideal]] of the [[representation ring]] of $G$ (hence, regarded as a [[ring of functions]], the restriction to an [[infinitesimal neighbourhood]] of the base point).

See also at _[formal completion -- Examples -- Atiyah-Segal theorem](completion+of+a+ring#AtiyahSegalTheorem)_.

The analog stable for [[stable cohomotopy]] is the _[[Segal-Carlsson completion theorem]]_:

[[!include Segal completion -- table]]

## Consequences

In the case where $X=*$ (i.e. a point), we have that $K_G(*) \simeq R(G)$ and $K(*//G)=KU^0(B G)$, thus we conclude that

$$
  KU^0(BG) \simeq R(G)\hat{_I}
$$

where $I$ is the [[augmentation ideal]] of the [[representation ring]] of $G$.

## Examples and applications
 {#ExamplesAndApplications}

\begin{example}\label{ComplexTopologicalKTheoryOfBS1}
**(complex topological K-theory of $B S^1$)** \linebreak

The [[complex topological K-theory]] of the [[classifying space]]
[[BU(n)|$B S^1$]] of the [[circle group]] is the [[power series ring]]:
$$
  KU^0
  \big(
    B S^1
  \big)
  \;\simeq\;
  \mathbb{Z}
  [ [ c_1^{KU} ] ]
  \,,
$$
where $c_1^{K U}$ is any [[complex oriented cohomology theory|complex orientation]] of [[KU]] (see [this Prop](complex+oriented+cohomology+theory#CohomologyRingOfBU1)).

On the other hand, the [[representation ring]] of the [[circle group]] is (see [this Example](representation+ring#RepresentationRingOfUnitaryGroups))

$$
  R_{\mathbb{C}}(S^1) \;\simeq\; \mathbb{Z}[x, x^{-1}]
  \,.
$$

Here $x$ is the class of the 1-dimensional [[irrep]] $U(1) \hookrightarrow \mathbb{C}$, the [[augmentation ideal]] is clearly generated by $c \coloneqq x - 1$. The corresponding completion is again 

$$
  \begin{aligned}
    \big(
      R_{\mathbb{C}}(S^1)
    \big)\hat{_{(c)}}
    &
    \;\simeq\;
    \mathbb{Z}[x, x^{-1}][ [ c ] ] / (c - x + 1) 
    \\
    & 
    \;\simeq\;
    \mathbb{Z}[ [ c ] ][ (1 + c)^{-1} ]
    \\
    & 
    \;\simeq\;
    \mathbb{Z}[ [ c ] ]
    \,,
  \end{aligned}
$$

where the first step is [this example](completion+of+a+ring#CompletionOfNoetherianRingByPowerSeries) and the third step observes that $1 + c$ is invertible in the $c$-power series ring (by [this Prop.](power+series#InvertibleElements)).

(e.g. [Buchholtz 08, Sec. 8.2](#Buchholtz08), also [Math.SE:a/3282578](https://math.stackexchange.com/a/3282578/58526))

\end{example}

compare also [Greenlees 1994, p. 74](https://www.sciencedirect.com/science/article/pii/002240499490006X)


## Related theorems

* [[Baum-Connes conjecture]], [[Green-Julg theorem]]

* As explained in _[[Equivariant stable homotopy theory]]_, there is a related characterization of the [[K-homology]] of $B G$ as a [[localization]].


## References

The original articles:

* [[Michael Atiyah]], _Characters and cohomology of finite groups_, Publications Mathématiques de l'IHÉS, Volume 9 (1961) , p. 23-64 ([numdam:PMIHES_1961__9__23_0]( http://www.numdam.org/item?id=PMIHES_1961__9__23_0))

* [[Michael Atiyah]], [[Friedrich Hirzebruch]], _Vector bundle and homogeneous spaces_, Proc. Sympos. Pure Math., Vol. III, American Mathematical Society, Providence, R.I., 1961, 3, 7–38 ([[AtiyahHirzebruch61.pdf:file]])

* [[Michael Atiyah]], [[Graeme Segal]], _Equivariant $K$-theory and completion_,  J. Differential Geom. Volume 3, Number 1-2 (1969), 1-18. ([euclid:jdg/1214428815](http://projecteuclid.org/euclid.jdg/1214428815))

Review and survey:

* {#Buchholtz08} [[Ulrik Buchholtz]], _The Atiyah-Segal completion theorem_, Master Thesis 2008 ([pdf](http://www.math.ku.dk/~jg/students/buchholtz.ms.2008.pdf), [[Buchholtz_AtiyahSegalCompletion.pdf:file]])

* Wikipedia, _[Atiyah-Segal completion theorem](http://en.wikipedia.org/wiki/Atiyah%E2%80%93Segal_completion_theorem)_


[[!redirects Atiyah-Segal completion]]
[[!redirects Atiyah-Segal completions]]
