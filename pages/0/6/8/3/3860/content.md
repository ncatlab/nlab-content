
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A formula for the number of [[fixed points]] of [[continuous map|continuous]] [[endomorphism|endo-maps]] of [[topological spaces]].

## Statement


\begin{definition}
\label{LefschetzNumber}
**(Lefschetz number)**
\linebreak
Given a [[continuous map|continuous]] [[endomorphism]] $f \colon X\to X$ of a [[topological space]], its **Lefschetz number**  is the alternating [[sum]] of the [[traces]] 

$$
  \Lambda_k(X,f)
  \;\coloneqq\;
  \sum_i 
  \,
    (-1)^i 
  \cdot
  Tr 
  \bigg(
    H^i(X ,\, \mathbb{Q})
    \xrightarrow{ f^\ast }
    H^i(X ,\, \mathbb{Q})
  \bigg)
  \,,
$$

of the [[linear map|linear]] [[endomorphisms]] on the [[rational cohomology]] [[cohomology groups|groups]] with [[coefficients]] given by [[pullback in cohomology]] .
\end{definition}

One sometimes also speaks of the _Lefschetz number_ of the induced [[endomorphism]] of the [[chain complex|chain/cochain complexes]], see *[[algebraic Lefschetz formula]]*. 


\begin{proposition}
\label{LefschetzFixedPointTheorem}
**(Lefschetz fixed point theorem)**
\linebreak
If $X$ is a [[compact topological space|compact]] [[polyhedron]] (a finite [[simplicial complex]]) and if the Lefschetz number (Def. \ref{LefschetzNumber}) is non-zero, then $f$ has at least one [[fixed point]]. I
\end{proposition}
The **proof** follows from the existence of 

1. a good cycle map,

1. the [[Künneth formula]],

1. [[Poincaré duality]].

(see [Milne, section 25](#Milne)).

\begin{remark}
The Lefschetz formula holds more generally in [[Weil cohomology]] theories (by definition) and hence notably in [[ℓ-adic cohomology|ℓ-adic]] [[étale cohomology]]. This fact serves to prove the [[Weil conjectures]].
\end{remark}



## Examples

\begin{example}
**(Euler characteristic)**
\linebreak
For $f = id$ is the [[identity]] map, the Lefschetz number (Def. \ref{LefschetzNumber}) reduces to the _[[Euler characteristic]]_ of $X$ (see [this Def.](Euler+characteristic#EulerCharOfTopSpace)):
$$
  \Lambda(X,\,id) \,=\, \chi(X)
  \,.
$$ 
\end{example}


\begin{example}
\label{ForContractibleCompactPolyhedra}
**(fixed point theorem for [[contractible topological space|contractible]] [[polyhedra]])**
\linebreak
If $X$ is compact polyhedron which is [[contractible topological space|contractible]] then all its [[cohomology groups]] in [[positive number|positive]] degree vanish, $H^{\geq 1}(X; k) \,=\, 0$, while $H^0(X; k) \,=\, k$.  This implies that the Lefschetz number (Def. \ref{LefschetzNumber}) of every endo-map $f$ is $\Lambda(X,f) \,=\, 1$.

Therefore, for contactible compact polyhedral $X$ the Lefschetz fixed point theorem (Prop. \ref{LefschetzFixedPointTheorem}) says that every map $f \colon X\to X$ has a fixed point.

In the further special case that $X = D^n$ is a [[disk]]/[[ball]], this is also the statement of [[Brouwer's fixed point theorem]].
\end{example}

\begin{example}\label{FixedPointTheoremForHomeomorphismsOfnSpheres}
**(fixed point theorem for [[homeomorphisms]] of [[n-spheres]])**
\linebreak
 For $n \in \mathbb{N}$, the [[n-sphere]] has [[ordinary cohomology]], in particular, [[rational cohomology]], concentrated in degrees 0 and $n$:
$$
  H^k(S^n;\, \mathbb{Q})
  \;\simeq\;
  \left\{
  \array{
    \mathbb{Q} &\vert& k \in \{0,n\}
    \\
    0 &\vert& \text{otherwise}
  }
  \right.
  \,.
$$

Any map $f \,\colon\, S^n \to S^n$ necessarily induces the [[identity]] on $H^0(S^n;\mathbb{Q})$ and is multiplication by the [[degree of a continuous function|degree]] $d(f)$ on $H^n(S^n; \mathbb{Q})$.

Therefore the Lefschetz number of $f$ (Def. \ref{LefschetzNumber}) is 
$$
  \Lambda(S^n, f)
  \;=\;
  1 + (-1)^n d(f)
$$
and so the Lefschetz fixed point theorem (Prop. \ref{LefschetzFixedPointTheorem}) in this case implies that sufficient conditions for $f$ to have a fixed point is that 

* $f$ is not a [[homeomorphism]] (its degree is different from $\pm 1$);

* $f$ is a [[homeomorphism]] and

  $$
    d(f) \,=\, (-1)^n
    \,.
  $$

The last case means equivalently that a [[homeomorphism]] $f \,\colon\, S^n \to S^n$ is guaranteed to have a fixed point if

* $n$ is [[even number|even]] and $f$ preserves [[orientation]];

or

* $n$ is [[odd number|odd]] and $f$ reverses [[orientation]].

This plays a role in the classification of [[free action|free]] [[transformation group]] [[actions]] on [[n-spheres]], see at *[[group actions on spheres]]* the section *[Free actions by finite groups](group+actions+on+spheres#FreeActionsByFiniteGroupsAndSphericalSpaceForms)*.

For example, the [[antipode|antipodal]] reflection action of [[cyclic group of order two|$\mathbb{Z}/2$]] on $S^n$ is orientation reversing for even $n$ and orientation preserving for odd $n$ and hence always has vanishing Lefschetz number. Indeed, this action is manifestly fixed-point free. But the Lefschetz fixed point theorem implies that this is the only case, in that there can be *no* orientation-preserving free action of $\mathbb{Z}/2$ on an even-dimensional sphere, and no orientation-reversing free action of $\mathbb{Z}/2$ on an odd-dimensional sphere.
\end{example}



## Related concepts

* [[Brouwer's fixed point theorem]]

* [[Atiyah-Bott fixed point formula]]

* [[Reidemeister trace]]

* [[Weil conjecture]]

* [[Grothendieck-Lefschetz trace formula]]


## References

### For ordinary cohomology

The original article is

* [[Solomon Lefschetz]], _On the fixed point formula_, Ann. of Math. (2), **38**  (1937) 819&#8211;822 ([jstor:1968838](https://www.jstor.org/stable/1968838))

Review:

* Edgar Lin, *An overview and proof of the Lefschetz fixed-point theorem* ([pdf](http://math.uchicago.edu/~may/REU2019/REUPapers/Lin,Edgar.pdf), [[Lin_LefschetzFixedPointTheorem.pdf:file]])

* {#eom} Online Springer Enc. of Math. ([[eom]]): [Lefschetz number](http://eom.springer.de/l/l057990.htm) (Rudyak), [Lefschetz formula](http://eom.springer.de/L/l057980.htm) (Iskovskikh)
 

In [[equivariant cohomology]]:

* [[Minhyong Kim]], _A Lefschetz trace formula for equivariant cohomology_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 28 no. 6 (1995), p. 669-688 ([numdam:ASENS_1995_4_28_6_669_0](http://www.numdam.org/item?id=ASENS_1995_4_28_6_669_0), [MR97d:55012](http://www.ams.org/mathscinet-getitem?mr=97d:55012))


### For &#233;tale cohomology

For [[étale cohomology]] of [[schemes]]:

* [[James Milne]], section 25 of _[[Lectures on Étale Cohomology]]_

For [[algebraic stacks]]:

* [[Kai Behrend]], _The Lefschetz trace formula for algebraic stacks_, 	Invent. Math. **112**, 1 (1993), 127-149 ([doi:10.1007/BF01232427](http://dx.doi.org/10.1007/BF01232427))

[[!redirects Lefschetz number]]
[[!redirects Lefschetz formula]]
[[!redirects Lefschetz numbers]]

[[!redirects Lefschetz fixed point theorem]]

[[!redirects Lefschetz fixed point formula]]
[[!redirects Lefschetz fixed-point formula]]