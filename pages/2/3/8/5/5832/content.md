
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

As surjections permit the transfer of logical properties, Barr's theorem has the following important consequence:

> If a statement in [[geometric logic]] is deducible from a [[geometric theory]] using classical [[logic]] and the [[axiom of choice]], then it is also
deducible from it in [[constructive mathematics]]. 

The proof of Barr's theorem itself, however, is highly non-constructive. 

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

## Related entries

* [[Deligne completeness theorem]]
* [[Boolean topos]]

## References

* [[Michael Barr|M. Barr]], _Toposes without points_ , JPAA **5** (1974) pp.265-280. ([preprint](http://www.math.mcgill.ca/barr/papers/top.no.pt.pdf)) doi:[10.1016/0022-4049(74)90037-1](http://dx.doi.org/10.1016/0022-4049(74%2990037-1)

Extensive discussion of the context of Barr's theorem is in chapter 7 of:

* [[P. T. Johnstone]], _Topos Theory_ , Academic Press New York 1977 (Dover reprint 2014).

For a discussion of the importance of this theorem in constructive algebra see

* [[Gavin Wraith]], _Intuitionistic algebra: some recent developments in topos theory_  In Proceedings
of the International Congress of Mathematicians (Helsinki, 1978), pages 331&#8211;337, Helsinki, 1980. Acad. Sci. Fennica. ([pdf](http://www.mathunion.org/ICM/ICM1978.1/Main/icm1978.1.0331.0338.ocr.pdf))
 {#Wraith}

For proof-theoretic approaches to Barr's theorem see

* Sara Negri, _Contraction-free sequent calculi for geometric theories with an
application to Barr's theorem_ , Archive for Mathematical Logic **42** (2003) pp.389&#8211;401.

For the connection with the Boolean-valued completeness theorem see

* R. Goldblatt, _Topoi - The Categorical Analysis of Logic_ , North-Holland 1982&#178;. (Dover reprint)

* R. Mansfield, _The Completeness Theorem for Infinitary Logic_ , JSL **37** no.1 (1972) pp.31-34.

* [[Michael Makkai]], [[Gonzalo E. Reyes]], _First-order Categorical Logic_ , LNM **611** Springer Heidelberg 1977.

See also the following MO discussion: ([link](http://mathoverflow.net/questions/98729/topos-without-point-from-the-point-of-view-of-logic))