
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

**Barr's theorem** was originally conjectured by [[William Lawvere]] as an infinitary generalization of the [[Deligne completeness theorem]] for [[coherent toposes]] which can be expressed as the existence of a surjection $\mathcal{S}/K\to\mathcal{E}$ for a coherent topos $\mathcal{E}$ with set of points $K$. General toposes $\mathcal{E}$ may fail to have [[enough points]] but [[Michael Barr]] showed that a surjection from a suitable [[Boolean topos]] still exists.

## Statement

+-- {: .num_theorem}
###### Theorem

If $\mathcal{E}$ is a [[Grothendieck topos]], then there is a  [[surjective geometric morphism]]

$$
  \mathcal{F} \to \mathcal{E}
$$

where $\mathcal{F}$ satisfies the [[axiom of choice]].

=--

## Remark

[[Deligne completeness theorem|Deligne's completeness theorem]] says that a coherent Grothendieck topos has enough points in $Set$ and this corresponds to the G&#246;del-Henkin completeness theorem for first-order theories. Similarly, Barr's theorem can interpreted as saying that a Grothendieck topos has sufficient _Boolean-valued_ points and is in turn closely related to Mansfield's **Boolean-valued completeness theorem** for infinitary first-order theories.

## Constructive proof and classical detour

Let $\mathbb{T}$ be a [[geometric theory]] and $U_\mathbb{T}$ its [[classifying topos|universal model]]. Recall that $U_\mathbb{T}$ represents deducibility in geometric logic in the sense that a geometric sequent $ \sigma$ is deducible from $\mathbb{T}$ precisely iff $U_\mathbb{T}\models \sigma $.

Suppose that $M=f^*(U_\mathbb{T})$ is a $\mathbb{T}$-model in a topos $\mathcal{E}$ where $f:\mathcal{E}\to Set[U_\mathbb{T}]$ is a [[surjective geometric morphism]] to the [[classifying topos]] of $\mathbb{T}$ and let $ (\varphi \vdash_{\vec{x}} \psi) $ be a geometric sequent such that $M\models (\varphi \vdash_{\vec{x}} \psi) $. Now by the definition of the satisfaction relation, this is the same as to say that the monomorphism $\{\vec{x}.\varphi\wedge\psi\}_M\hookrightarrow\{\vec{x}.\varphi\}_M$ is an isomorphism but, $f$ being surjective, $f^*$ is [[conservative functor|conservative]] whence $U_\mathbb{T}\models (\varphi \vdash_{\vec{x}} \psi) $ and, accordingly, $(\varphi \vdash_{\vec{x}} \psi)$ is deducible from $\mathbb{T}$ in geometric logic.

This together with the existence of a Boolean cover assured by Barr's theorem implies the following important

+-- {: .num_theorem}
###### Corollary

Let $\mathbb{T}$ be a [[geometric theory]] and $\sigma$ a geometric sequent that holds in all $\mathbb{T}$-models in Boolean toposes. Then $\sigma$ is deducible from $\mathbb{T}$ in geometric logic.

=--


In other words, if a statement in [[geometric logic]] is deducible from a [[geometric theory]] using classical [[logic]] and the [[axiom of choice]], then it is also deducible from it in [[constructive mathematics]]. While the construction in the proof Barr's theorem is constructive, the proof that it results in a topos where the axiom of choice holds depends on an application of Zorn's Lemma in the base topos (of sets, say); see Theorems 5.39 and 7.57 of Johnstone's _Topos Theory_. Hence the result does not directly help in finding such constructive replacements for classical proofs of geometric statements. 


## Related entries

* [[Deligne completeness theorem]]

* [[Boolean topos]]

## Link

* MO discussion on topos without points: _[Topos Without point, from the point of view of logic.](http://mathoverflow.net/questions/98729/topos-without-point-from-the-point-of-view-of-logic)_

## References

* [[Michael Barr|M. Barr]], _Toposes without points_ , JPAA **5** (1974) pp.265-280. ([preprint](http://www.math.mcgill.ca/barr/papers/top.no.pt.pdf)) doi:[10.1016/0022-4049(74)90037-1](http://dx.doi.org/10.1016/0022-4049(74%2990037-1)

Extensive discussion of the context of Barr's theorem is in chapter 7 of:

* [[P. T. Johnstone]], _Topos Theory_ , Academic Press New York 1977 (Dover reprint 2014).

A proof sketch and a survey of its model-theoretic context is in

* [[Gonzalo Reyes|Gonzalo E. Reyes]], _Sheaves and concepts: A model-theoretic interpretation of Grothendieck topoi_ , Cah. Top. Diff. G&#233;o. **Cat. XVIII** no.2 (1977) pp.405-437. ([numdam](http://www.numdam.org/item?id=CTGDC_1977__18_2_105_0))

For a discussion of the importance of the corollary in constructive algebra see also

* [[Gavin Wraith]], _Intuitionistic algebra: some recent developments in topos theory_  In: Proceedings of the International Congress of Mathematicians (Helsinki, 1978), pages 331&#8211;337, Helsinki, 1980. Acad. Sci. Fennica. ([pdf](http://www.mathunion.org/ICM/ICM1978.1/Main/icm1978.1.0331.0338.ocr.pdf))
 {#Wraith}

For proof-theoretic approaches to Barr's theorem see

* Sara Negri, _Contraction-free sequent calculi for geometric theories with an
application to Barr's theorem_ , Archive for Mathematical Logic **42** (2003) pp.389&#8211;401.

For the connection with the Boolean-valued completeness theorem see also

* R. Goldblatt, _Topoi - The Categorical Analysis of Logic_ , North-Holland 1982&#178;. (Dover reprint New York 2006; [project euclid](http://projecteuclid.org/euclid.bia/1403013939))

* R. Mansfield, _The Completeness Theorem for Infinitary Logic_ , JSL **37** no.1 (1972) pp.31-34.

* [[Michael Makkai]], [[Gonzalo E. Reyes]], _First-order Categorical Logic_ , LNM **611** Springer Heidelberg 1977.

