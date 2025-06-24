
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

A _normed ring_ is a [[ring]] compatibly equipped with a [[norm]] on the underlying [[abelian group]]. 

If this is suitably [[complete topological space|complete]] with respect to the norm, then a normed ring is called a _[[Banach ring]]_. A normed ring which is a [[field]] is, naturally, called a [[normed field]], and if the norm is multiplicative it is also called a [[valued field]].

The [[Berkovich spectrum]] of a normed ring $R$ is the set of multiplicative [[seminorms]] on $R$ that are bounded by the norm on $R$.


## Definition

+-- {: .num_defn #NormedCommutativeRing}
###### Definition

A _normed commutative ring_ is a [[commutative ring]] $R$ equipped with a [[function]]

$$
  {\vert -\vert} \;\colon\; R \longrightarrow \mathbb{R}_{\geq 0}
$$

to the non-negative [[real numbers]] such that for all $f,g \in R$

1. ${\vert f \vert} = 0$ precisely if $f = 0$;

2. $\vert -f\vert = \vert f \vert$

3. ${\vert f + g \vert} \leq {\vert f \vert}+ {\vert g \vert}$ ([[triangle identity]])

4. ${\vert f \cdot g\vert} \leq {\vert f \vert\cdot {\vert g \vert}}$.

=--

(e.g [Ozaki, Kashiwagi & Tsuboi 1953](#OzakiKashiwagiTsuboi53))


+-- {: .num_remark}
###### Remark

One might also define a normed ring to be a [[commutative monoid]] [[internalization|internal]] to the [[monoidal category]] $NGrp$ of [[normed groups]].  If the morphisms in $NGrp$ are taken to be the [[short map|short]] group homomorphisms and the [[projective cross norm]] is used on the tensor product, then this reproduces the definition above.  If (as is often seen) the morphisms are generalized to [[bounded map|bounded]] group homomrophisms, then this generalizes the third clause in def. \ref{NormedCommutativeRing}
to 

* there is $C \in \mathbb{R}_{\gt 0}$ such that for all $f,g \in R$

  $$
    {\vert f \cdot g\vert} \leq C \cdot {\vert f \vert\cdot {\vert g \vert}}
  $$

see e.g. ([Bassat-Kremnitzer 13, remark 6.32](#BassatKremnitzer13))
=--


## Examples

A [[normed field]] is of course in particular a [[normed ring]].

+-- {: .num_example #MatrixRing}
###### Example

For $R$ a normed commutative ring, then for each $n \in \mathbb{N}$ the [[matrix algebra]] $Mat_n(R)$ becomes a normed ring with norm

$$
 {\vert A\vert} \coloneqq max_{1 \leq i,j \leq n}({\vert A_{i,j}\vert})
 \,.
$$

Notice that even if $R$ if the norm on $R$ is multiplicative (is an [[absolute value]]) that on $Mat_n(R)$ is not in general. If $R$ is a [[Banach ring]], then so is $Mat_n(R)$.
=--

(e.g. [Jarden 11](#Jarden11)).


## Related concepts

* [[division ring]]

* [[apartness ring]]

* [[tight apartness ring]]

[[!include analytic geometry ingredients -- table]]


## References

The notion of normed rings originates with:

* [[Israel Gelfand]], *Normierte Ringe*, Rec. Math. [Mat. Sbornik] N.S. **9**(51) 1 (1941) 3–24 &lbrack;[mathnet:6046](https://m.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=sm&paperid=6046&option_lang=eng)&rbrack;

Early further discussion:

* {#OzakiKashiwagiTsuboi53} Shigeo Ozaki, Sadao Kashiwagi, Teruo Tsuboi, *Note on Normed Rings*, Science Reports of the Tokyo Bunrika Daigaku, Section A **4** 98/103 (1953) 277-282 &lbrack;[jstor:43700402](https://www.jstor.org/stable/43700402)&rbrack;




See also:

* {#BoschGüntzerRemmert84} [[Siegfried Bosch]], [[Ulrich Güntzer]], [[Reinhold Remmert]], *[[Non-Archimedean Analysis]] -- A systematic approach to rigid analytic geometry*, Grundlehren der Mathem. Wissen. **261** (1984) &lbrack;  [ISBN:9783540125464](https://link.springer.com/book/9783540125464), [pdf](http://math.arizona.edu/~cais/scans/BGR-Non_Archimedean_Analysis.pdf)&rbrack;

* Naoki Kimura, _A note on normed ring_, Kodai Math. Sem. Rep.
**1** 3-4 (1949) 23-24 &lbrack;[euclid:kmj/1138833472](http://projecteuclid.org/euclid.kmj/1138833472)&rbrack;

* {#Naimark59} [[Mark Naimark]] (translated by Leo Boron):  _Normed Rings_, P. Noordhoff (1959) &lbrack;[ark:/13960/s20rdczxmrt](https://archive.org/details/normedrings0000mana)&rbrack;

* {#Jarden11} M. Jarden, _Normed rings_, chapter 2 of:  _Algebraic patching_, Springer Monographs in Mathematics (2011) &lbrack;[[JardenNormedRings.pdf:file]]&rbrack;

* {#Berkovich09} [[Vladimir Berkovich]], _Non-archimedean analytic spaces_, lectures at the _Advanced School on $p$-adic Analysis and Applications_, ICTP, Trieste, 31 August - 11 September 2009 &lbrack;[pdf](http://www.wisdom.weizmann.ac.il/~vova/Trieste_2009.pdf)&rbrack;

* {#BassatKremnitzer13} [[Oren Ben-Bassat]], [[Kobi Kremnizer]], section 6.5 of _Non-Archimedean analytic geometry as relative algebraic geometry_ ([arXiv:1312.0338](http://arxiv.org/abs/1312.0338))

* ProofWiki, <a href="https://proofwiki.org/wiki/Definition:Norm_(Division_Ring)">Norm (Division ring)</a>

For more see the references at _[[Banach ring]]_.


[[!redirects normed ring]]
[[!redirects normed rings]]
