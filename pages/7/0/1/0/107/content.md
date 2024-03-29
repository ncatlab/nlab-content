
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

[[Carlos Simpson]] conjectured, in the context of [[semi-strict infinity-categories]] that every [[weak omega-category]] is [[equivalence|equivalent]] to one that is a [[strict omega-category]] except for the units.

## Statement

In 

* {#Simpson98} [[Carlos Simpson]], _Homotopy types of strict 3-groupoids_ ([arXiv:9810059](http://arxiv.org/abs/math/9810059))

it was conjectured ([page 27](http://arxiv.org/PS_cache/math/pdf/9810/9810059v1.pdf#page=27)) that

**Simpson's Conjecture:** _Every weak $\infty$-[[infinity-category|category]] is equivalent to an $\infty$-category in which [[strict omega-category|composition and exchange laws are strict]] and only the unit laws are allowed to hold weakly._ 

For weak unit laws in $\infty$-categories see

* Joachim Kock,  _Weak identity arrows in higher categories_ ([arXiv](http://arxiv.org/abs/math.CT/0507116))

In 

* {#JoyalKock06} [[Andre Joyal]], Kock, _Weak units and homotopy 3-types_ ([arXiv](http://arxiv.org/abs/math.CT/0602084))

Simpson's conjecture is proven up to the case of 3-categories with a single object.

## Remarks

One expects several alternative such [[semi-strict infinity-category|semi-strictification]] statements. Eugenia Cheng and Nick Gurski write the following at the end of their paper:

+--{style="font-size: 90%; margin-left:2em;"}
Finally we consider the question of eliminating the distinguished invertible 
elements by using a stricter form of $n$-category. Generalising from the previous 
sections, we see that we do not need to restrict all the way to strict $n$-categories 
&#8211; a semistrict version will suffice. One form of semistrictness has everything strict 
except interchange (cf. Gray-categories and see Crans 2000b, Crans 2000a); another has everything strict except units (Koch 2005, Simpson 1998). These have both been proposed 
as solutions to the coherence problem for $n$-categories. 

However, there are other possible "shades" of semistrictness and the above 
notions do not appear to be right for the present purposes. Instead, we need a 
form of semistrict $n$-category in which the units and interchange for $(n-1)$-cells 
are strict, but everything else can be weak. This is to eliminate the constraint 
$n$-cells that become distinguished invertible elements in our $n$-degenerate situation; 
we expect that as in the case $n = 2$ the associator is automatically forced to be the 
identity. 

**Hypothesis 5.3. Semistrictness**
Let $n \ge 3$. Then an $n$-degenerate semistrict $n$-category in the above sense is precisely a commutative monoid. 
=--
E. Cheng and N. Gurski's,  _The periodic table of $n$-categories for low dimensions I_ ([arXiv](http://arxiv.org/abs/0708.1178))


## History
 {#History}

The conjecture was initially triggered by the claim in 

* {#KapranovVoevodsky91} [[Mikhail Kapranov]],  [[Vladimir Voevodsky]],  _$\infty$-Groupoids and homotopy types_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 32 no. 1 (1991), p. 29-46  ([Numdam](http://www.numdam.org/item?id=CTGDC_1991__32_1_29_0))

that "[[semi-strict infinity-category|semi-strict infinity-groupoids]]", in which only the [[inverses]] could be weak and everything else strict, model all [[homotopy types]] (hence solve the [[homotopy hypothesis]])

In ([Simpson 98](#Simpson98)) it was pointed out that this seems to be wrong for the [[homotopy type]] of the [[sphere|2-sphere]].

The issue, however, is quite subtle, as highlighted by Voevodsky [here](http://ncatlab.org/nlab/show/homotopy+type+theory#VoevodskyIASTalk2014))

(For instance  Corollary 5.2 in ([Simpson 98](#Simpson98)) leaves open the possibility that the [[geometric realization]] in  ([Kapranov-Voevodsky 91](#KapranovVoevodsky91)) is essentially surjective, only that the homotopy groups of the resulting space could not be read off from the groupoid in the obvious way. 

Examining [KV 91](#KapranovVoevodsky91)'s motivation, Simpson noticed a singularity at the origin of [[Moore paths]], which led him to conjecture that weakening invertibility and units (while keeping strict associativity and interchange) would be enough to get at all homotopy types. Specifically, he writes on p. 27

> I think that the argument of (K. and V.) (which is unclear on the question of identity elements) actually serves to prove the above statement. I have called the above statement a "conjecture" because I haven't checked this.


[[!redirects Simpson conjecture]]
[[!redirects Simpson's conjecture]]
[[!redirects Simpson's conjecture]]
[[!redirects Simpson\'s conjecture]]
[[!redirects Simpson's conjecture]]
[[!redirects Simpson's conjecture]]