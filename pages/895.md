
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _cofibration category_ is a [[category]] equipped with a sub-[[class]] of its [[morphisms]] which behave like [[cofibrations]].

The notion of _cofibration category_ was introduced by [[Hans-Joachim Baues]] (see references below) as a variant of the category of cofibrant objects, (for which, see [[category of fibrant objects]] and dualise). The axioms are substantially weaker than [[model category|those of  a Quillen model category]], but add one axiom to [[category of fibrant objects|those of K. S. Brown]].

 In the first chapter of his book *Algebraic Homotopy* (see below), [[Hans-Joachim Baues|Baues]] suggests two criteria for an axiom system:

1. _The axioms should be sufficiently strong to permit the basic constructions of homotopy theory._

1. _The axioms should be as weak (and as simple) as possible, so that the constructions of homotopy theory are available in as many contexts as possible._

Baues also introduces the notion of a [[I-category]] being a category with a natural cylinder functor satisfying a set of good properties.

One should distinguish cofibration categories from the Waldhausen's notion of a "category with cofibrations and weak equivalences", nowdays called [[Waldhausen category]].

## Definition

A *cofibration category* is a category $C$ with two classes of morphisms, $\mathit{cof}$ of
_cofibrations_ and $w.e.$ of _weak equivalences_.
These are to satisfy:

C 1) Isomorphisms are both cofibrations and weak equivalences.  If

$$A\stackrel{f}{\rightarrow} B \stackrel{g}{\rightarrow} C$$ 
are composable morphisms in $C$, then if two of $f$, $g$, $g \circ f$ are in  $w.e.$, so is the
third; if $f$, $g \in \mathit{cof}$ then $g \circ f\in \mathit{cof}$.

C2) Pushout axiom:

Given $B\rightarrow A$ in $\mathit{cof}$ and any $f : B\rightarrow Y$, the pushout


$$
  \array{
    B &\stackrel{f}{\rightarrow}& Y
    \\
    \downarrow_i
    &&
    \downarrow^{\bar{i}}
    \\
   A &\stackrel{\bar{f}}{\to}&  A \cup_B Y   
  }
$$

exists and $\bar{i}$ is in $\mathit{cof}$; if $f$ is in $w.e.$, so is $\bar{f}$; if $i$ is also in $w.e.$, so is $\bar{i}$.

C3) Factorisation axiom:

Given $B\stackrel{f}{\rightarrow} Y$, there is a factorisation 

$$
  \array{
B&\stackrel{f}{\longrightarrow}&Y\\
\stackrel{i}{\searrow}&&\stackrel{g}{\nearrow}\\
&A&
}$$

with $i \in \mathit{cof}$, $g\in w.e.$

C4) Axiom on fibrant models:

Using the terminology: "$f$ is a _trivial cofibration_" to mean "$f\in
\mathit{cof} \cap w.e.$", and "$RX$ is _fibrant_" to mean "Given any trivial
cofibration $i: RX \stackrel{\simeq}{\rightarrow}Q$, there is a retraction $r :
Q \rightarrow RX$, $r \circ i = Id_{RX}$", the axiom states:

Given $X\in C$, there is trivial cofibration $X\rightarrow RX$ with $RX$ fibrant.

## Examples

* If $C$ has a model category structure then the full subcategory of  cofibrant objects forms a cofibration category.

## Related concepts

* [[fibration category]]

* [[category of cofibrant objects]]

## References

* [[H. J. Baues]], _Algebraic homotopy_, Cambridge studies in advanced mathematics 15,  Cambridge University Press, (1989).

* [[Karol Szumiło]], Homotopy theory of cofibration categories. Homology Homotopy Appl. 18 (2016), no. 2, 345–357.
[doi](https://doi.org/10.4310/HHA.2016.v18.n2.a19)

* [[Karol Szumiło]], Homotopy theory of cocomplete quasicategories. Algebr. Geom. Topol. 17 (2017), no. 2, 765–791.
[doi](https://doi.org/10.2140/agt.2017.17.765)

* [[Krzysztof Kapulkin]], [[Karol Szumiło]], Quasicategories of frames of cofibration categories. Appl. Categ. Structures 25 (2017), no. 3, 323–347.
[doi](https://doi.org/10.1007/s10485-015-9422-y)

* [[Karol Szumiło]], Frames in cofibration categories. J. Homotopy Relat. Struct. 12 (2017), no. 3, 577–616.
[doi](https://doi.org/10.1007/s40062-016-0139-x)

* [[Markus Land]], [[Thomas Nikolaus]], [[Karol Szumiło]], Localization of cofibration categories and groupoid C∗-algebras. Algebr. Geom. Topol. 17 (2017), no. 5, 3007–3020.
[doi](https://doi.org/10.2140/agt.2017.17.3007)

[[!redirects cofibration categories]]

[[!redirects category with cofibrations]]
