<div class="rightHandSide toc">
[[!include higher algebra - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

$L_\infty$-algebras are a [[vertical categorification]] of Lie algebras: in an $L_\infty$-algebra the Jacobi identity is allowed to hold (only) up to higher coherent homotopy. 

From another perspective: an $L_\infty$-algebra is a [[Lie ∞-algebroid]] with a single object.

## Definition ##

### Original definition in terms of lots of brackets ###

Originally $L_\infty$-algebras were defined as follows:

an $L_\infty$-algebra is an $\mathbb{N}_+$-[[graded vector space]] $\mathfrak{g} = V$ together with for each $n \in \mathbb{N}_+$ a list of skew linear maps

$$
  l_n(\cdots) := [-,-, \cdots, -] : V^{\wedge n} \to V
$$

of degree -1, that satisfy a generalized Jacobi identity of the form

$$
  \sum_{i+j = n} \sum_{unshuffles \sigma}
  \pm l_i (l_j (v_{\sigma(1)}, \cdots, v_{\sigma(j)}
   , v_{\sigma(j+1) , \cdots , v_{\sigma(n)}}
  ) )
  = 0
  \,,
$$

for all elements $(v_i) \in V^{\otimes n}$, 
where the sign "$\pm$" depends on the signature of the un[[shuffle]] permutation $\sigma$.

Notably for $n = 4$ this says that the binary bracket $l_2 = [-,-]$, the trinary bracket $l_3 = [-,-,-]$ and the unary "bracket" $l_1$ are related by

$$
  [[v_1,v_2],v_3] \pm  
  [[v_2,v_3],v_1]
  \pm 
  [[v_3,v_1],v_2]
  =
  l_1 ([v_1, v_2, v_3])
  \,.
$$

> (Exercise for the reader: put in the right signs, depending on the degree of the $v_i$).

If the right hand side were 0, this would be the Jacobi identity of an ordinary [[Lie algebra]] (or [[super Lie algebra]], rather). So the image under $l_1$ of the trinary bracket $[-,-,-]$ in the $L_\infty$-algebra is a measure for how the ordinary Jacobi identity _fails_ in an $L_\infty$-algebra.

But the point is that it does not _just_ fail: it fails by the speccific homtopy expressed by $l_3$, and this homotopy itself is _coherent_, in that it satisfies suitable relatoins itself, obtained by evaluating the above sum expression for $n \gt 4$.

### Reformulation in terms of semifree differential coalgebra ###

A little later it was realized that the above huge sum expressions can very neatly be equivalently encoded as follows:

An **$L_\infty$-algebra** is 

* an $\mathbb{N}_+$-graded vector space $\mathfrak{g}$;

* equipped with a differential $D : \vee^\bullet \mathfrak{g} \to \vee^\bullet \mathfrak{g}$ of degree $-1$ on the [[free graded co-commutative coalgebra]] over $\mathfrak{g}$ that squares to 0

$$
  D^2 = 0
  \,.
$$

Here the free graded co-commutative co-algebra $\vee^\bullet \mathfrak{g}$ is, as a vector space, the same as the graded [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g}$ whose elements we write as 

$$
  3 t_1 \vee t_2 + t_3 + t_3 \vee t_4 \vee t_5
$$

etc (where the $\vee$ is just a funny way to write the wedge $\wedge$, in order to remind us that:...)

but throught of as equipped with the standard coproduct

$$
  \Delta (v_1 \vee v_2 \cdots \vee v_n)
  \propto \sum_i \pm (v_1 \vee \cdots \vee v_i) \otimes (v_{i+1} \vee \cdots \vee v_n)
$$

> (work out or see the references for the signs and prefacors).

Since this is a _free_ graded co-commutative coalgebra, one can see that any differential 

$$
  D : \vee^\bullet \mathfrak{g} \to \vee^\bullet \mathfrak{g}
$$

on it is fixed by its value "on cogenerators" (a statement that is maybe unfamiliar, but simply the straightforward dual of the more familar statement to which we come below, that differentials on free graded algebras are fixed by their action on generators) which means that we can decompose $D$ as

$$
  D = D_1 +  D_2 + D_3 + \cdots
  \,,
$$

where each $D_i$ acts as $l_i$ when evaluated on a homogeneous element of the form $t_1 \vee \cdots \vee t_n$ and is then uniquely extended to all of $\vee^\bullet \mathfrak{g}$ by extending it as a _coderivation_ on a coalgebra.

For instance $D_2$ acts on homogeneous elements of word lenght 3 as

$$
  D_3(t_1 \vee t_2 \vee t_3) = 
  [t_1, t_2]\vee t_3 \pm permutations
  \,.
$$

> exercise for the reader: spell this all out more in detail with all the signs and everyrthing. Possibly by looking it up in the references given below.

Using this, one checks that the simple condition that $D$ squares to 0 is precisely equivalent to the infinite tower of generalized Jacobi identities:


$$
  (D^2 = 0)
  \Leftrightarrow
  \left(
    \forall n : 
  \sum_{i+j = n} \sum_{unshuffles \sigma}
  \pm l_i (l_j (v_{\sigma(1)}, \cdots, v_{\sigma(j)}
   , v_{\sigma(j+1) , \cdots , v_{\sigma(n)}}
  ) )
  = 0
  \right)
  \,.
$$


### Reformulation in terms of semifree differential algebra ###

The reformulation of an $L_\infty$-algebra as simply a semi-co-free graded-co-commutative coalgebra $(\vee^\bullet \mathfrak{g}, D)$ is a useful repackaging of the original definition, but the coalgebraic aspect tends to be not only unfamiliar, but also a bit inconvenient. At least when the graded vector space $\mathfrak{g}$ is degreewise finite dimensional, we can simply pass to its degreewise dual graded vector space $\mathfrak{g}^*$. Its [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g}^*$ is then naturally equipped with an ordinary differential $d = D^*$ which acts on $\omega \in \wedge^\bullet \mathfrak{g}^*$ as

$$
  (d \omega) (t_1 \vee \cdots \vee t_n) =
  \pm \omega(D(t_1 \vee \cdots \vee t_n))
  \,.
$$

When the grading-dust has settled one finds that with 

$$
  \wedge^\bullet \mathfrak{g}^* =
  k \oplus \mathfrak{g}^*_1 \oplus (\mathfrak{g}^*_1 \wedge \mathfrak{g}^*_1 \oplus \mathfrak{g}^*_2) \oplus \cdots
$$

with the ground field in degree 0, the degree 1-elements of $\mathfrak{g}^*$ in degree 1, etc, that $d$ is of degree +1 and of course squares to 0

$$
  d^2 = 0
  \,.
$$

This means that we have a [[semifree dga]]

$$
  CE(\mathfrak{g}) := (\wedge^\bullet \mathfrak{g}^*, d)
  \,.
$$

In the case that $\mathfrak{g}$ happens to be an ordinary [[Lie algebra]], this is the ordinary [[Chevalley-Eilenberg algebra]] of this Lie algebra. Hence we should generally call $CE(\mathfrak{g})$ the [[Chevalley-Eilenberg algebra]]
of the $L_\infty$-algebra $\mathfrak{g}$.

One observes that this construction is bijective: every (degreewise finite dimensional) cochain [[semifree dga]] generated in positive degree comes from a (degreewise finite dimensional) $L_\infty$-algebra this way.

This means that we may just as well _define_ a (degreewise finite dimensional) $L_\infty$-algebra as an object in the [[opposite category]] of (degreewise finite dimensional) commutative [[dg-algebra]]s that are [[semifree dga]]s and generated in positive degree.

And this turns out to be one of the most useful perspectives on $L_\infty$-algebras.

In particular, if we simply drop the condition that the dg-algebra be generated in positive degree and allow it to be generated in non-negative degree, we have the notion of the (Chevalley-Eilenberg algebra of) an [[L-infinity-algebroid]]. 







## Special cases and generalizations ##

* An $L_\infty$-algebra for which $V$ is concentrated in the first $n$ degree is a **Lie $n$-algebra** (sometimes also: "$L_n$-algebra").

* The skew-symmetry of the Lie bracket is retained strictly in $L_\infty$-algebras. It is expected that weakening this, too, yields a more general [[vertical categorification]] of Lie algebras. For $n=2$ this has been worked out by Dmitry Roytenberg: [On weak Lie 2-algebras](http://arxiv.org/abs/0712.3461).

* The [[horizontal categorification]] of $L_\infty$-algebras are $L_\infty$-[[Lie infinity-algebroid|algebroid]]s.

* An $L_\infty$-algebra with only $D_n$ non-vanishing is called an **[[n-Lie algebra]]** -- to be distinguished from a _Lie $n$-algebra_ ! However, in large parts of the literature $n$-Lie algebras are considered for which $D_n$ is _not_ of the required homogeneous degree in the grading, or in which no grading is considered in the first place. Such $n$-Lie algebras are not special examples of $L_\infty$-algebras, then. For more see [[n-Lie algebra]].


## References ##

The original references are:

* T. Lada and J. Stasheff,  _Introduction to sh Lie algebras for physicists_, Int. J. Theo. Phys. 32 (1993), 1087--1103. ([arXiv](http://arxiv.org/abs/hep-th/9209099))

* Tom Lada, Martin Markl, _Strongly homotopy Lie algebras_ ([arXiv](http://arxiv.org/abs/hep-th/9406095))

A quick web entry is:

* Marilyn Daily, [$L_\infty$-structures](http://www.aei.mpg.de/~md/hl.html).

See also for instance section 3.1 of:

Alberto S. Cattaneo, Florian Sch&auml;tz, _Equivalences of higher derived brackets_ ([arXiv](http://arxiv.org/abs/0704.1403))

The standard reference for Lie 2-algebras is:

* [[John Baez]] and Alissa Crans, _Higher-dimensional dlgebra VI: Lie 2-algebras_, [TAC](http://www.tac.mta.ca/tac/volumes/12/14/12-14abs.html) 12, (2004), 492--528. ([arXiv](http://arxiv.org/abs/math/0307263))

For more general 'weak Lie 2-algebras', see:

* Dmitry Roytenberg, _On weak Lie 2-algebras_,  ([arXiv](http://arxiv.org/abs/0712.3461))


[[!redirects L-infinity-algebras]]
[[!redirects Lie infinity-algebra]]
[[!redirects L-infinity algebra]]
[[!redirects Lie infinity-algebras]]
[[!redirects L-infinity algebras]]
[[!redirects L-∞ algebra]]
[[!redirects L-∞ algebras]]
[[!redirects L-∞-algebra]]
[[!redirects L-∞-algebras]]

[[!redirects Lie n-algebra]]
[[!redirects L-n-algebra]]
[[!redirects L-n algebra]]
[[!redirects Lie n-algebras]]
[[!redirects L-n-algebras]]
[[!redirects L-n algebras]]