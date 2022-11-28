
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Syntomic cohomology_ is the [[abelian sheaf cohomology]] of the _syntomic site_ of a [[scheme]].
It is a $p$-[[p-adic|adic]] analogue of [[Deligne-Beilinson cohomology]].

Syntomic cohomology is closely related to the [[crystalline cohomology]] of that scheme and may be regarded as a [[p-adic numbers|$p$-adic]] [[absolute Hodge cohomology]].

## Construction via Prismatic Cohomology

The syntomic cohomology may also be obtained from [[prismatic cohomology]] ([Bhatt22](#Bhatt22)). Let $R$ be a p-adically complete ring and let $\Delta_{R}$ be its absolute prismatic cohomology. It has an action of the [[Frobenius morphism]] $\phi$. We also have a "Breuil Kisin twist" $\Delta\lbrace 1\rbrace$ and a [[filtration]] $\Fil_{N}^{\bullet}\Delta$ called the _Nygaard filtration_ (see see [Bhatt21](#Bhatt21), section 2). The syntomic cohomology $\mathbb{Z}_{p}(i)$ is then defined to be the [[fiber]]

$$\mathbb{Z}_{p}(i)(R)=\fib(\Fil_{N}^{i}\Delta_{R}\lbrace i\rbrace\xrightarrow{\phi_{i}-1}\Delta_{R}\lbrace i\rbrace)$$

This construction globalizes and may be applied to p-adic [[formal schemes]] instead of just p-adically complete rings (see [Bhatt21](#Bhatt21), Remark 2.14).

## Related

* [[Deligne-Beilinson cohomology]]

* [[p-adic Hodge theory]]

* [[prismatic cohomology]]

## References

The syntomic site was introduced in

* Jean-Marc Fontaine and [[William Messing]], _$p$-Adic periods and $p$-adic etale cohomology_ ([pdf](http://www.ams.org/publications/online-books/conm67-conm67-ch4.pdf))

A construction of syntomic cohomology via [[prismatic cohomology]] is briefly discussed in

* {#Bhatt21} [[Bhargav Bhatt]], _Algebraic Geometry in Mixed Characteristic_ ([arXiv:2112.12010](https://arxiv.org/abs/2112.12010))

* {#Bhatt22} [[Bhargav Bhatt]], _p-adic Hodge Theory and Applications: Connections to Algebraic Topology_ (Day 3 of Simons Lectures) ([YouTube](https://www.youtube.com/watch?v=OUDJZnuy8Jw))

Further developments are in

* Amnon Besser, _Syntomic regulators and $p$-adic integration I: rigid syntomic regulators_ ([pdf](http://www.math.uiuc.edu/K-theory/0298/reg.pdf))

The following shows that, just as [[Deligne-Beilinson cohomology]] may be interpreted as [[absolute Hodge cohomology]], syntomic cohomology may be interpreted as $p$-adic absolute Hodge cohomology.

* [[Frédéric Déglise]], [[Wiesława Nizioł]], _On $p$-adic absolute Hodge cohomology and syntomic coefficients, I_, [arXiv:1508.02567](http://arxiv.org/abs/1508.02567).