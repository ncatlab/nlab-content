
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

The operations on an [[H-space]] $X$ (such as a [[topological group]] or a  [[loop space]]) equip its [[homology]] with the [[mathematical structure|structure]] of  [[ring]]. At least for [[ordinary homology]] this is known as the _[[Pontrjagin ring]]_ $H_*(X)$ of $X$.

## Properties

### Relation to Whitehead product
 {#RelationToWhiteheadProduct}

Under the [[Hurewicz homomorphism]], the [[commutator]] of the Pontrjagin product on homology is the [[Whitehead product]] on [[homotopy groups]] of a [[based loop space]]. 

This is due to [Samelson (1953)](#Samelson53) and for higher Whitehead brackets due to [Arkowitz (1971)](#Arkowitz71). 

In fact, in [[characteristic zero]] the [[Pontrjagin ring]] structure on [[connected topological space|connected]] [[based loop spaces]] $\Omega X$ is identified via the [[Hurewicz homomorphism]] with the [[universal enveloping algebra]] (see [there](universal+enveloping+algebra#ForSuperLieAlgebras)) of the [[Whitehead bracket super Lie algebra]] of $X$ &lbrack;[Milnor & Moore (1965) Appendix](#MilnorMoore65); [Whitehead (1978) Thm. X.7.10](#Whitehead78); [Félix, Halperin & Thomas 2000, Thm. 16.13](#FélixHalperinThomas00)&rbrack;. Moreover, in this case the [[underlying]] [[ordinary cohomology]] ([[universal coefficient theorem|hence]] the [[ordinary homology]]) [[vector space]] may be read off from any [[Sullivan model]] of $X$ (by the proposition [here](Sullivan+model+of+loop+space#SullivanModelForBasedLoopSpace)).


For the following examples we use these notational conventions:

* $\mathbb{K}$ denotes a [[field]] of [[characteristic zero]],

* a subscript on a generator denotes its degree,

* $\mathbb{K}\langle\cdots \rangle$ denotes the [[graded vector space|graded]] $\mathbb{K}$-[[vector space]] [[linear span|spanned]] by the [[linear basis]] of generators listed inside the angular brackets;

* $\mathbb{K}[\cdots]$ denotes the [[underlying]] [[vector space]] of the free [[graded-commutative algebra]] on the set of generators listed inside the square brackets;

* $T(-)$ denotes the graded [[tensor algebra]] on a given [[graded vector space]],

* the [[semifree dgc-algebra]] on a given set $\{\cdots\}$ of generators subject to differential relations we denote, with slight abuse of notation, by

  $$
    \mathbb{K}[\cdots]\big/
    \left(
      \begin{array}{c}
        \mathrm{d}(-) = \ldots
        \\
        \vdots
      \end{array}
    \right)
  $$

\begin{example}
\label{RationalPontrAlgOfLoopsOfSpheresAndCPn}
**(rational Pontrjagin algebra of loops of spheres and $\mathbb{C}P^n$s)**
\linebreak
The [[Sullivan model of spheres|Sullivan model of]] the [[2-sphere]] is
$$
  CE(\mathfrak{l} S^2)
  \;\simeq\;
  \mathbb{Q}\big[
    \omega_2, \omega_3
  \big]\big/
  \left(
  \begin{array}{l}
    \mathrm{d} \omega_2 \,=\, 0
    \\
    \mathrm{d} \omega_3 
      \,=\, 
    \tfrac{1}{2} \omega_2 \wedge \omega_2
  \end{array}
  \right)
  \,.
$$
From this it follows (since [[the co-binary Sullivan differential is the dual Whitehead product]])
that the binary [[Whitehead brackets|Whitehead]] [[super Lie brackets]] of $S^2$ are:
$$
  \begin{array}{l}
    [v_1, v_1] = v_2
    \\
    [v_2, v_2] = 0
    \\
    [v_1, v_2] = 0
  \end{array}
$$

The rational Pontrjagin ring of $\Omega S^2$ is the [[universal enveloping algebra]] of this [[super Lie algebra]], hence:
$$
  H_\bullet\big(
    \Omega S^2
    ;\,
    \mathbb{K}
  \big)
  \;\simeq\;
  T\big(
    \mathbb{K}\langle v_1, v_2\rangle
  \big)
  \big/
  \left(
    \begin{array}{l}
      2 v_1^2 - v_2
      \\
      v_1 v_2 - v_2 v_1 
    \end{array}
  \right)
  \mathrlap{\,.}
$$ 
Therefore the [[underlying]] [[graded vector space|graded]] $\mathbb{K}$-[[vector space]] of the Pontrjagin ring of $\Omega S^2$ is 
$\mathbb{K}[v_1, v_2]$ but the product of the $v_1$ is deformed from $v_1 \cdot v_1 = 0$ to $v_1 \cdot v_1 = \tfrac{1}{2}v_2$.

Similarly, the rational Pontrjagin algebra of the loop space of the [[4-sphere]] is 
$$
  H_\bullet\big(
    \Omega S^4
    ;\,
    \mathbb{K}
  \big)
  \;\simeq\;
  T\big( \mathbb{K}\langle v_3, v_6\rangle \big)
  \big/
  \left(
    \begin{array}{l}
      2 v_3^2 - v_6
      \\
      v_3 v_6 - v_6 v_3 
    \end{array}
  \right)
$$
whose [[underlying]] $\mathbb{K}$-[[vector space]] is $\mathbb{K}[v_3, v_6]$ but with the product of the $v_3$ deformed from $v_3 \cdot v_3 = 0$ to $v_3 \cdot v_3 = \tfrac{1}{2}v_6$.

On the other hand, the differential of the [[Sullivan model of complex projective space|Sullivan model of]] [[complex projective space]] $\mathbb{C}P^n$ for $n \geq 2$ has vanishing co-binary part, so that
$$
  H_\bullet\big(
    \Omega \mathbb{C}P^{n \geq 2}
    ;\,
    \mathbb{K}
  \big)
  \;\simeq\;
  T\big( \mathbb{K}\langle v_2, v_{2n}\rangle \big)
  \big/
  \left(
    \begin{array}{l}
      2 v_1^2
      \\
      v_1 v_{2n} - v_{2n} v_1
    \end{array}
  \right)
  \;\simeq\;
  \mathbb{K}[v_1, v_{2n}]
$$ 
is just a plain graded-commutative algebra. 

For $n = \infty$ (ie. for the [[classifying space]] $\mathbb{C}P^\infty \simeq$[[BU(n)|$B U(1)$]]) this becomes
$$
  H_\bullet\big(
    \Omega \mathbb{C}P^{\infty}
    ;\,
    \mathbb{K}
  \big)
  \;\simeq\;
  T\big( \mathbb{K}\langle v_2\rangle \big)
  \big/
  \big(
      2 v_1^2
  \big)
  \;\simeq\;
  \mathbb{K}[v_1]
  \mathrlap{\,,}
$$ 
reflecting the fact that $\Omega \, \mathbb{C}P^\infty \,\simeq\, \Omega B U(1)\,\simeq\, S^1$.
\end{example}




### Homological group completion

The homological version of 
the _[[group completion theorem]]_ relates the [[Pontrjagin ring]] of a [[topological monoid]] $A$ to that of its [[group completion]] $\Omega B A$.

### Relation to quantum cohomology
 {#RelationToQuantumCohomology}

The homology Pontrjagin product of certain [[compact Lie groups]] is identified with the [[quantum cohomology]] of corresponding [[flag varieties]] (see references [below](#ReferencesOnQuantumCohomologyAsPontrjaginRings)).


## Related concepts

* [[homology of loop spaces]]



## References

### General

The concept and the terminology "Pontryagin-multiplication" is due to

* [[Raoul Bott]], [[Hans Samelson]], *On the Pontryagin product in spaces of paths*, Commentarii Mathematici Helvetici **27** (1953) 320–337 &lbrack;[doi:10.1007/BF02564566](https://doi.org/10.1007/BF02564566)&rbrack;

who name it in honor of the analogous product operation on the homology of [[compact Lie groups]] due to:

* [[Lev Pontrjagin]], *Homologies in compact Lie groups*, Rec. Math. [Mat. Sbornik] N. S. **6** (**48**) 3 (1939) 389–422 &lbrack;[mathnet:5835](http://m.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=sm&paperid=5835&option_lang=eng)&rbrack;

see also:

* [[Hans Samelson]], §3 in: *Beitr&auml;ge Zur Topologie der Gruppen-Mannigfaltigkeiten*, Annals of Mathematics, Second Series, **42** 5 (1941) 1091-1137 &lbrack;[jsotr:1970463](https://www.jstor.org/stable/1970463)&rbrack;

Proof that the [[commutator]] of the Pontrjagin product is the [[Whitehead product]], under the [[Hurewicz homomorphism]]:

* {#Samelson53} [[Hans Samelson]], *A Connection Between the Whitehead and the Pontryagin Product*, American Journal of Mathematics **75** 4 (1953) 744–752  &lbrack;[doi:10.2307/2372549](https://doi.org/10.2307/2372549)&rbrack;

and in [[characteristic zero]]:

* {#MilnorMoore65} [[John Milnor]], [[John Moore]], Appendix (pp. 262) of: _On the structure of Hopf algebras_, Annals of Math. __81__ (1965) 211-264 &lbrack;[doi:10.2307/1970615](https://doi.org/10.2307/1970615), [pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/milnor-moore-ann-math-1965.pdf)&rbrack;

* {#FélixHalperinThomas00} [[Yves Félix]], [[Stephen Halperin]], [[Jean-Claude Thomas]], Thm. 16.13 in: _Rational Homotopy Theory_, Graduate Texts in Mathematics **205** Springer (2000) &lbrack;[doi:10.1007/978-1-4613-0105-9](https://link.springer.com/book/10.1007/978-1-4613-0105-9)&rbrack;

and slightly beyond

* {#Halperin92} [[Stephen Halperin]], *Universal enveloping algebras and loop space homology*, Journal of Pure and Applied Algebra **83** 3 (1992) 237-282 \[<a href="https://doi.org/10.1016/0022-4049(92)90046-I">doi:10.1016/0022-4049(92)90046-I</a>\]

* [[Jonathan A. Scott]], _Algebraic Structure in the Loop Space Homology Bockstein Spectral Sequence_,  Transactions of the American Mathematical Society **354** 8 (2002) 3075-3084 &lbrack;[jstor:3073034](https://www.jstor.org/stable/3073034)&rbrack;

and for higher Whitehead brackets:

* {#Arkowitz71} [[Martin Arkowitz]], *Whitehead Products as Images of Pontrjagin Products*, Transactions of the American Mathematical Society, **158** 2 (1971) 453-463 &lbrack;[doi:10.2307/1995917](https://doi.org/10.2307/1995917)&rbrack;

and full lifting of the theorem [Milnor & Moore, 1965 (Appendix)](#MilnorMoore65), equipping the rational Pontrjagin algebra with [[A-infinity algebra|$A_\infty$-algebra]] structure and identifying it with the universal envelope of the [[Whitehead L-infinity algebra]]:

* [[José M. Moreno-Fernández]], Thm. 4.1 in: *The Milnor-Moore theorem for $L_\infty$-algebras in rational homotopy theory*, Mathematische Zeitschrift **300** (2022) 2147–2165  &lbrack;[arXiv:1904.12530](https://arxiv.org/abs/1904.12530), [doi:10.1007/s00209-021-02838-z](https://doi.org/10.1007/s00209-021-02838-z)&rbrack;

Refinement to algebra structure on the [[singular chain complex]] (Adams-Hilton model):

* [[John F. Adams]], [[Peter J. Hilton]], *On the chain algebra of a loop space*, Commentarii Mathematici Helvetici **30** (1956) 305–330 &lbrack;[doi:10.1007/BF02564350](https://doi.org/10.1007/BF02564350)&rbrack;

reviewed and further developed in:

* [[Kathryn Hess]], [[Paul-Eugène Parent]], [[Jonathan Scott]], [[Andrew Tonks]], *A canonical enriched Adams-Hilton model for simplicial sets*, Advances in Mathematics **207** 2 (2006) 847-875 &lbrack;[doi:10.1016/j.aim.2006.01.013](https://doi.org/10.1016/j.aim.2006.01.013), [arXiv:math/0408216](https://arxiv.org/abs/math/0408216)&rbrack;

More on the Pontrjagin rings of the [[classical Lie groups]]:

* [[Ichiro Yokota]], *On the homology of classical Lie groups*, J. Inst. Polytech. Osaka City Univ. Ser. A **8** 2 (1957) 93-120 &lbrack;[euclid:ojm/1353054814](https://projecteuclid.org/journals/osaka-journal-of-mathematics/volume-8/issue-2/On-the-homology-of-classical-Lie-groups/ojm/1353054814.full)&rbrack;

reviewed in:

* [[Inna Zakharevich]], pp. 35 of: *Stable homotopy*, Section 11 of: *[K-theory and characteristic classes](https://pi.math.cornell.edu/~zakh/6530/)*, lecture notes (2017) &lbrack;[pdf](https://pi.math.cornell.edu/~zakh/6530/sec11.pdf), [[Zakharevich-StableHomotopy.pdf:file]]&rbrack;


Further early discussion:

* [[Raoul Bott]], *The space of loops on a Lie group*, Michigan Math. J. **5** 1 (1958) 35-61 &lbrack;[doi:10.1307/mmj/1028998010](https://projecteuclid.org/journals/michigan-mathematical-journal/volume-5/issue-1/The-space-of-loops-on-a-Lie-group/10.1307/mmj/1028998010.full)&rbrack;

  > (for loop spaces of [[Lie groups]])


* [[William Browder]], *Homology and Homotopy of H-Spaces*, Proceedings of the National Academy of Sciences of the United States of America **46** 4 (1960) 543-545 &lbrack;[jstor:70867](https://www.jstor.org/stable/70867)&rbrack;

* [[William Browder]], p. 36 of: *Torsion in H-Spaces*, Annals of Mathematics, Second Series **74** 1 (1961) 24-51  &lbrack;[jstor:1970305](https://www.jstor.org/stable/1970305)&rbrack;

* [[William Browder]], *Homology Rings of Groups*, American Journal of Mathematics **90** 1 (1968) &lbrack;[jstor:2373440](https://www.jstor.org/stable/2373440)&rbrack;

On the effect on Pontrjagin rings of [[group completion]] of [[topological monoids]]:

* [[Michael Barratt]], [[Stewart Priddy]], *On the homology of non-connected monoids and their associated groups*, Commentarii Mathematici Helvetici, **47** 1 (1972) 1–14 &lbrack;[doi:10.1007/BF02566785](https://link.springer.com/article/10.1007/BF02566785), [eudml:139496](https://eudml.org/doc/139496)&rbrack;

* [[Dusa McDuff]], [[Graeme Segal]]: *Homology fibrations and the “group-completion” theorem*, Inventiones mathematicae **31** (1976) 279-284 &lbrack;[doi:10.1007/BF01403148](https://doi.org/10.1007/BF01403148)&rbrack;




Pontrjagin rings in the context of [[string topology]]:

* [[Moira Chas]], [[Dennis Sullivan]], §3 in: *String Topology* &lbrack;[arXiv:math/9911159](https://arxiv.org/abs/math/9911159)&rbrack;

* [[Ralph L. Cohen]], [[John D. S. Jones]], Jun Yan, pp. 15 of: *The loop homology algebra of spheres and projective spaces*, in *Categorical Decomposition Techniques in Algebraic Topology*, Progress in Mathematics **215**, Birkhäuser (2003) &lbrack;[arXiv:math/0210353](https://arxiv.org/abs/math/0210353), [doi:10.1007/978-3-0348-7863-0_5](https://doi.org/10.1007/978-3-0348-7863-0_5)&rbrack;


* Gwénaël Massuyeau, [[Vladimir Turaev]], *Brackets in the Pontryagin algebras of manifolds*, Mém. Soc. Math. France **154** (2017) &lbrack;[arXiv:1308.5131](https://arxiv.org/abs/1308.5131)&rbrack;



Textbook accounts:


* {#Whitehead78} [[George W. Whitehead]], p. 98 in: *Elements of Homotopy Theory*, Springer (1978) &lbrack;[doi:10.1007/978-1-4612-6318-0](https://link.springer.com/book/10.1007/978-1-4612-6318-0)&rbrack;


* {#Hatcher02} [[Allen Hatcher]], §3.C, pp. 287 in: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

Lecture notes

* [[Tyrone Cutler]], §3 in: *The Bott-Samelson Theorem* (2020) &lbrack;[pdf](https://www.math.uni-bielefeld.de/~tcutler/pdf/Week%2011%20-%20The%20Bott-Samelson%20Theorem.pdf)&rbrack;

See also

* Wikipedia, _[Pontryagin product](https://en.wikipedia.org/wiki/Pontryagin_product)_

Relating the Pontrjagin algebra on [[loop groups]] of [[compact Lie groups]] to their [[Langlands dual groups]]:

* [[Zhiwei Yun]], [[Xinwen Zhu]], *Integral homology of loop groups via Langlands dual groups*, Represent. Theory **15** (2011) 347-369 &lbrack;[arXiv:0909.5487](https://arxiv.org/abs/0909.5487), [doi:10.1090/S1088-4165-2011-00399-X](https://doi.org/10.1090/S1088-4165-2011-00399-X)&rbrack;



Computation of the Pontryagin products for (loop spaces of) [[flag manifolds]]:

* Jelena Grbic, Svjetlana Terzic, *The integral Pontrjagin homology of the based loop space on a flag manifold*, Osaka J. Math. **47** (2010) 439-460 &lbrack;[arXiv:math/0702113](https://arxiv.org/abs/math/0702113)





[[!include quantum cohomology as Pontrjagin rings -- references]]






[[!redirects Pontrjagin rings]]

[[!redirects Pontryagin ring]]
[[!redirects Pontryagin rings]]
[[!redirects Pontrjagin ring]]
[[!redirects Pontrjagin rings]]

[[!redirects Pontryagin product]]
[[!redirects Pontryagin products]]
[[!redirects Pontrjagin product]]
[[!redirects Pontrjagin products]]

[[!redirects Pontryagin multiplication]]
[[!redirects Pontryagin multiplications]]

[[!redirects Pontryagin-multiplication]]
[[!redirects Pontryagin-multiplications]]

[[!redirects Pontryagin algebra]]
[[!redirects Pontryagin algebras]]
[[!redirects Pontrjagin algebra]]
[[!redirects Pontrjagin algebras]]

[[!redirects Pontryagin homology algebra]]
[[!redirects Pontryagin homology algebras]]
[[!redirects Pontrjagin homology algebra]]
[[!redirects Pontrjagin homology algebras]]



[[!redirects Peterson isomorphism]]
[[!redirects Peterson isomorphisms]]

[[!redirects Adams-Hilton model]]
[[!redirects Adams-Hilton models]]


