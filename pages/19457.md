
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _enriched adjunction_ is the generalization of that of [[adjoint functors]] ([[adjunctions]] in [[Cat]]) from [[category theory]] to [[enriched category theory]].

## Definition

+-- {: .num_defn}
###### Definition
**(enriched adjunction)**

For $\mathcal{V}$ a [[closed monoidal category|closed]] [[symmetric monoidal category]] with all [[limits]] and [[colimits]], let $\mathcal{C}$, $\mathcal{D}$ be two $\mathcal{V}$-[[enriched categories]]. Then an _[[adjoint pair]] of $\mathcal{V}$-[[enriched functors]]_ or _enriched adjunction_ 

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

is a [[pair]] of $\mathcal{V}$-[[enriched functors]], as shown, such that there is a $\mathcal{V}$-[[enriched natural isomorphism]] between [[enriched hom-functors]] of the form

$$
  \mathcal{C}(L(-),-)
  \;\simeq\;
  \mathcal{D}(-,R(-))
  \,.
$$

=--

(e.g. [Borceux 94, Def. 6.7.1](#Borceux94))

The 2-functor $\mathcal{V}$-$Cat \rightarrow {Cat}$ that sends an enriched category to its underlying ordinary category sends an enriched adjunction to an ordinary adjunction.

## Examples

* An adjunction enriched over truth values is a [[Galois connection]].

## Related concepts

* [[enriched Quillen adjunction]]

  * [[simplicial Quillen adjunction]]

* [[monoidal adjunction]]

## References


* [[Max Kelly]], section 1.11 of _Basic Concepts of Enriched Category Theory_, Cambridge University Press, Lecture Notes in Mathematics 64, 1982,  Republished in: Reprints in Theory and Applications of Categories, No. 10 (2005) pp. 1-136 ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))


* {#Borceux94} [[Francis Borceux]], Vol 2, def. 6.2.4 of _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)

[[!redirects enriched adjunctions]]


[[!redirects enriched adjoint]]
[[!redirects enriched adjoints]]
