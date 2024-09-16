
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Exceptional structures
+-- {: .hide}
[[!include exceptional structures -- contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[Lie group]] called $E_8$ is the largest-dimensional one of the five [[exceptional Lie groups]].

## Properties

### As part of the ADE pattern

[[!include ADE -- table]]

### Homotopy groups

The first nontrivial [[homotopy group]] of the [[topological space]] underlying $E_8$ is

$$
  \pi_3(E_8) \simeq \mathbb{Z}
$$

as for any compact Lie group. Then the next nontrivial homotopy group is

$$
  \pi_{15}(E_8) \simeq \mathbb{Z}
  \,.
$$

This means that all the way up to the 15 [[coskeleton]] the group $E_8$ looks, [[homotopy theory|homotopy theoretically]] like the [[Eilenberg-MacLane space]] $K(\mathbb{Z},3) \simeq B^3 \mathbb{Z} \simeq B^2 U(1) \simeq B \mathbb{C}P^\infty$.

### Subgroups
  {#Subgroups}

The [[subgroup]] of the [[exceptional Lie group]] [[E8]] which corresponds to the [[Lie algebra]]-inclusion $\mathfrak{so}(16) \hookrightarrow \mathfrak{e}_8$ is the [[semi-spin group]] [[SemiSpin(16)]]

$$
  SemiSpin(16)
  \;\subset\;
  E_8
$$

On the other hand, the [[special orthogonal group]] $SO(16)$ is _not_ a [[subgroup]] of $E_8$ (e.g. [McInnes 99a, p. 11](SemiSpin16#McInnes99a)).

Under the inclusion of the maximal compact subgroup, the [[fundamental representation]] of $E_{8(8)}$ [[branching rule|branches]] as 

\begin{tikzcd}[sep=0pt]
  \mathrm{SemiSpin}(16)
  \ar[rr, "{ \iota }"]
  &&
  E_{8(8)}
  \\
  \mathbf{120}
  \oplus
  \mathbf{128}
  &\rotatebox{180}{$\longmapsto$}&
  \mathbf{248}
\end{tikzcd}

(e.g. [Hohm & Samtleben 2014 p 4](#HohmSamtleben14))


### Invariant polynomials

By the above discussion of homotopy groups, it follows (by [[Chern-Weil theory]]) that the first [[invariant polynomials]] on the [[Lie algebra]] $\mathfrak{e}_8$ are the quadratic [[Killing form]] and then next an octic polynomial. That is described in ([Cederwall-Palmkvist](#CederwallPalmkvist)).


### As U-duality of 3d SuGra

$E_8$ is the [[U-duality]] group (see there) of [[11-dimensional supergravity]] [[KK-compactification|compactified]] to 3 dimensions.

[[!include U-duality -- table]]


## Related entries

The group $E_8$ plays a role in some exceptional [[differential geometry]]/[[differential cohomology]]. See for instance

* [[exceptional generalized geometry]], [[supergravity C-field]], [[Hořava-Witten theory]], [[heterotic string theory]]

* [[G₂]], [[F₄]],

  [[E₆]], [[E₇]],  **E₈**, [[E₉]], [[E₁₀]], [[E₁₁]], $\cdots$


## References
 {#References}

### General

Surveys:

* [[Skip Garibaldi]], _$E_8$, the most exceptional group_ ([arXiv:1605.01721](https://arxiv.org/abs/1605.01721))

* Wikipedia, _[E₈](http://en.wikipedia.org/wiki/E8_%28mathematics%29)_

An introductory survey with an eye towards the relation to the [[octonions]] is given in [section 4.6](http://math.ucr.edu/home/baez/octonions/node19.html) of 

* [[John Baez]], _The Octonions_ ([web](http://math.ucr.edu/home/baez/octonions/octonions.html)) 

### Homotopy groups
 {#HomotopyGroupsReferences}

The lower [[homotopy groups]] of $E_8$ are a classical result due to

* [[Raoul Bott]] and H. Samelson, _Application of the theory of Morse to symmetric spaces_ , Amer.
J. Math., 80 (1958), 964-1029.

The higher homotopy groups are discussed in 

* Hideyuki Kachi, _Homotopy groups of compact Lie groups $E_6$, $E_7$ and $E_8$_ Nagoya Math. J. Volume 32 (1968), 109-139. ([project EUCLID](http://projecteuclid.org/euclid.nmj/1118797372))

See also

* [[André Henriques]], [MO comment](http://mathoverflow.net/questions/52286/how-are-the-classifying-space-of-e-8-and-k-mathbbz-4-related/52321#52321) 

### Invariant polynomials

The octic [[invariant polynomial]] of $E_8$ is discussed in 

* [[Martin Cederwall]], Jakob Palmkvist, _The octic $E_8$ invariant_ J.Math.Phys.48:073505 (2007) ([arXiv:hep-th/0702024](http://arxiv.org/abs/hep-th/0702024))
{#CederwallPalmkvist}

### More

On [[string bordism]] of the [[classifying space]] of $E_8$:

* [[Michael Hill]], *The $String$  bordism of $B E_8$ and $B E_8 \times B E_8$ through dimension 14*, Ill. J. Math. **53** 1 (2009) 183-196 &lbrack;[doi:10.1215/ijm/1264170845](https://projecteuclid.org/journals/illinois-journal-of-mathematics/volume-53/issue-1/The-string-bordism-of-BE_8-and-BE_8times-BE_8-through-dimension/10.1215/ijm/1264170845.full)&rbrack;

On $E_8$-[[exceptional field theory]]-formulation of [[D=11 supergravity]]:

* {#HohmSamtleben14} [[Olaf Hohm]], [[Henning Samtleben]]: _Exceptional Field Theory III: [[E8|$E_{8(8)}$]]_, Phys. Rev. D **90** 066002 (2014) &lbrack;[arXiv:1406.3348](http://arxiv.org/abs/1406.3348), [doi:10.1103/PhysRevD.90.066002](https://doi.org/10.1103/PhysRevD.90.066002)&rbrack;

[[!redirects E8]]
