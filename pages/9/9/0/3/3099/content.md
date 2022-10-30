
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **(combinatorial) species** is a [[presheaf]] or [[higher category theory|higher categorical]] presheaf on the [[groupoid]] [[core]]([[FinSet]]).


## Definition


### 1-categorical

The [[category]] of **species**, $Species := PSh(core(FinSet))$, is the [[category of presheaves]] on the [[groupoid]] $\mathbb{P} := core(FinSet)$ of [[finite sets]] and [[bijections]], the [[core]] of [[FinSet]]: 

$$
  \hat \mathbb{P} := PSh(core(FinSet))
  \,.
$$

For more, see [[structure type]].

### 2-categorical

A **2-species** (usually called a [[stuff type]]) is a [[2-presheaf]] on [[core]]([[FinSet]]), i.e. a [[pseudofunctor]]

$$
  core(FinSet) \to Grpd
$$

to the [[2-category]] [[Grpd]].

### $(\infty,1)$-categorical

Generally, an **$\infty$-species** or **homotopical species** is an [[(∞,1)-presheaf]] on $core(FinSet)$, i.e. an [[(∞,1)-functor]]

$$
  core(FinSet)^{op} \to \infty Grpd
$$

to the [[(∞,1)-category]] [[∞Grpd]].

The [[(∞,1)-category]] of $\infty$-species is the [[(∞,1)-category of (∞,1)-presheaves]]

$$
  \infty Species := PSh_{(\infty,1)}(core(FinSet))
  \,,
$$

### Operations on species

There are in fact 5 important monoidal structures on the category of species.  For a discussion of all five, you'll currently have to read about [[Schur functors]], where these operations are discussed in the context of $Fin\Vect$-valued species, i.e. $Fin\Vect$-valued presheaves on the groupoid of finite sets.  But here are two:

#### Sum

The **sum** $A + B$ of two species $A$, $B$ is their [[coproduct]] $A \coprod B$. Since [[colimit]]s of [[presheaves]] are computed objectwise, we have

$$
  (A + B)_n \simeq A_n \coprod B_n
  \,.
$$

#### Product

The category $core(FinSet)$ becomes a [[monoidal category]] under disjoint union of finite sets. This monoidal structure $(core(FinSet), \coprod)$ induces canonically the [[Day convolution]] monoidal structure on $Species := PSh(core(FinSet))$.

For $A$ and $B$ two combinatorial species, their product is given by the [[coend]]

$$
  (A \otimes B)_n
  \simeq
  \int^{n \in FinSet}  A_k \times B_l \times Hom_{core(FinSet)}(n,k+l)
  \simeq
  \coprod_{k+l = n} \prod_{\frac{(k+l)!}{k! + l!}} (A_k \times B_l)
  \,.
$$

## Cardinality

Under [[groupoid cardinality]] 

$$
  {|-|} : \infty Grpd_{tame} \to \mathbb{R}
$$

every (tame) [[∞-groupoid]] is mapped to a [[real number]]

$$
  X \mapsto {|X|} := \sum_{[x] \in \pi_0(X)}\prod_{i = 1}^{\infty} (\pi_i(X,x)^{(-1)^{i}})
  \,.
$$

A species $\mathbf{X}$ assigns an [[∞-groupoid]] $\mathbf{X}_n$ to each [[natural number]] $n \in \mathbb{Z}$. Therefore under [[groupoid cardinality]] we may naturally think of a tame species as mapping to a [[power series]]

$$
  \mathbf{X} \mapsto {|\mathbf{X}|}
  :=
  \sum_{n = 0}^{\infty} \frac{1}{n!} {|\mathbf{X}_n|} z^n
  \in 
  \mathbb{R}[ [ z ] ]
  \,.
$$

This cardinality operation maps the above addition and multiplication of combinatorial species to addition and multiplication of [[power series]].

That [[coproduct]] of species maps to sum of their cardinalities is trivial. That [[Day convolution]] of species maps under cardinality to the product of their cardinality series depends a little bit more subtly on the combinatorial prefactors:

$$
  {| A \otimes B |}
  =
  {|A|} \cdot {|B|}
  =
  \sum_{n=0}^\infty 
   \frac{1}{n!}
   \sum_{k+l = n} \frac{n!}{k! l!} 
   {|A_k|} \cdot {|B_l|}
  \,.
$$

## Variants

If in the definition of combinatorial species the  domain [[core]]([[FinSet]]) is replaced with [[FinVect]] and also the presheaves are take with values in [[FinVect]] then one obtains the notion of  **[[Schur functor]]**.

## In Homotopy Type Theory

Let $FinSet$ be the type of finite sets.  A species is a type $X :
Type$ equipped with an arrow into $Finset$:

$$
  Species \coloneqq \sum_{X : Type} (X \to FinSet)
$$

To obtain a generating function from $f : X \to FinSet$, we decategorify by
0-truncating $FinSet$, making it equivalent to $\mathbb{N}$:

$$
  f \circ card : X \to FinSet \to {\|FinSet\|_{0}} \simeq \mathbb{N}
$$

The generating function of the species is then

$$
  {|X|}(z) 
  \coloneqq 
    \sum_{n=0}^{\infty} {\big| fib_{f \circ card}(n) \big|}\,  z^{n}
  =
  \sum_{n=0}^{\infty} {\big| fib_{f}(Fin(n)) \big|}\, \frac{z^{n}}{n!}
$$

where $Fin(n)$ is a type with exactly $n$ elements.

If $\Phi : FinSet \to Type$ is a family of types, then we obtain the species

$$
  pr_{1} : \bigg(\sum_{A : FinSet} \Phi(A)\bigg) \to FinSet
$$

with generating function

$$
  {|\Phi|}(z)
  =
  \sum_{n=0}^{\infty} {|\Phi(Fin(n))|} \frac{z^{n}}{n!}
$$

So, if $\Phi$ is a [[stuff, structure, property|stuff, structure, or property]]
on finite sets, then we immediately know something about its generating function, considered as an exponential generating function:

* If $\Phi(A)$ is contractible for all $A$, then $\Phi(Fin(n)) = 1$, so its generating function is $e^{z}$.

* If $\Phi(A)$ is a family of mere propositions, then every coefficient is either $0$ or $1$, according to whether $A$ can be equipped with a $\Phi$-structure or not
    
* If $\Phi(A)$ is a family of sets (i.e., a [[structure type]]), then every coefficient is an element of $\mathbb{N}$.
    
* If $\Phi(A)$ has a higher homotopy level (i.e., is a [[stuff type]]), then the coefficients are in $[0, \infty)$.

Since any species $f : X \to Type$ is equal to

$$
  pr_{1} : \bigg(\sum_{x:X}fib_{f}(x)\bigg) \to Type
$$

every species is equal to one obtained from a stuff type.

### Operations on species

The five monoidal structures mentioned above under [Operations on species](#operations_on_species)
can be represented in HoTT, along with a couple other useful operations.  We
give four of the five monoidal structures here.
For more operations, see ([Dougherty15](#Dougherty15)).  We assume throughout this subsection that $f : X \to \Finset$ and $g : Y \to Finset$ are two species, and $\Phi, \Psi : FinSet \to Type$ are two stuff types.

#### Coproduct

The recursion principle for the coproduct gives the species

$$ \array{
  (f + g) &:& X + Y \to Finset \\
  (f + g) &:& (x, y) \mapsto f(x) + g(y)
}$$

If $X$ and $Y$ are obtained from $\Phi$ and $\Psi$, respectively, then the coproduct is equal to 

$$
  \sum_{A : FinSet} (\Phi(A) + \Psi(A))
$$

The generating function for the coproduct is

$$
  {|X + Y|}(z) = {|X|}(z) + {|Y|}(z)
$$

#### Hadamard product

The Hadamard product of species is

$$ \array{
  \langle X, Y \rangle &:& X \times_{FinSet} Y \to FinSet \\
  \langle X, Y \rangle &:& (x, y, p) \mapsto f(x)
}$$

which for stuff types is equal to

$$ \array{
  \sum_{A : FinSet} (\Phi(A) \times \Psi(A))
}$$

The generating functions are related by

$$
  {|\langle X, Y \rangle|}(z)
  =
  \sum_{n=0}^{\infty} n! X_{n} Y_{n} z^{n}
$$

where $X_{n}$ and $Y_{n}$ are the $n$th coefficients of the functions ${|X|}(z)$ and ${|Y|}(z)$, respectively.

The name "Hadamard product" is used by Aguiar and Mahajan ([Aguiar-Mahajan10](#Aguiar10)) and Bergeron _et al._ ([Bergeron-Labelle-Leroux08](#Bergeron08)).  Baez and Dolan ([Baez-Dolan01](#Baez01)) call it the "inner product" of stuff types, because equipping the category of stuff types with this operation makes it a categorified version of the Hilbert space of a quantum harmonic oscillator.


#### Cauchy product

The Cauchy product of species is

$$ \array{
  (f \cdot g) &:& X \times Y \to FinSet \\
  (f \cdot g) &:& (x, y) \mapsto f(x) + g(y) 
} $$

which for stuff types is equal to

$$
  \sum_{A, U, V : FinSet} \sum_{p : U + V = A} (\Phi(U) \times \Psi(V))
$$

So, $\Phi\Psi$ stuff on a finite set is the stuff of "being chopped in two, with $\Phi$ stuff on one part and $\Psi$ stuff on the other".

The generating function is

$$
  {|X \cdot Y|}(z) = {|X|}(z) \cdot {|Y|}(z)
$$


#### Composition

The composition of two species is

$$ \array{
  (f \tilde{\circ} g) &:& \bigg(\sum_{x:X}(Fin(card(f(x)) \to Y)\bigg) \to FinSet \\
  (f \tilde{\circ} g) &:& (x, P, p) \mapsto \bigoplus_{i=1}^{card(f(x))}g(P(i))
}$$

where $\bigoplus_{i=1}^{n}g(P(i))$ is the $n$-ary direct sum of the finite sets $g(P(i))$.  For stuff types, this amounts to

$$
  \sum_{(A, C : FinSet)}\sum_{(B : Fin(card(C)) \to FinSet)} \bigg(
  (B\vdash_{card(C)}A) \times \Phi(C) \times \prod_{k : Fin(card(C))} \Psi(B(k))
  \bigg)
$$

That is, $\Phi \tilde{\circ} \Psi$ stuff on a finite set is a partition of the set into $card(C)$ subsets, with $\Phi$ stuff on the partition and $\Psi$ stuff on each of the subsets.

The generating function of the composition is

$$
{|X \tilde{\circ} Y|}(z) = {|X|}({|Y|}(z))
$$ 

This species is also called the [[plethysm]] product.



## References

The notion of species goes back to

* [[André Joyal]], _Une th&#233;orie combinatoire des s&#233;ries formelles_ , Advances in Mathematics 42:1-82 (1981) <a href="http://dx.doi.org/10.1016/0001-8708(81)90052-9">doi</a>, [MR84d:05025](http://www.ams.org/mathscinet-getitem?mr=633783)

An expositional discussion can be found at

* [[Todd Trimble]], _Exponential Generating Function and Introduction to Species_ ([blog](http://topologicalmusings.wordpress.com/2009/03/28/number-of-idempotent-endofunctions/)) (scroll down a bit).

See also wikipedia: [combinatorial species](http://en.wikipedia.org/wiki/Combinatorial_species) and 

* Fran&#231;ois Bergeron, Gilbert Labelle, Pierre Leroux, _Th&#233;orie des esp&#232;ces et combinatoire des structures arborescentes_ , LaCIM, Montr&#233;al (1994). English version: [[Combinatorial species and tree-like structures]], Cambridge University Press (1998).
* {#Bergeron08} F. Bergeron, G. Labelle, P. Leroux, _Introduction to the theory of
species of structures_, 2008, [pdf](http://bergeron.math.uqam.ca/Site/bergeron_anglais_files/livre_combinatoire.pdf)
* Fran&#231;ois Bergeron, _Species and variations on the theme of species_, invited talk at [Category Theory and Computer Science '04](http://www.itu.dk/research/theory/ctcs2004/), Copenhagen (2004). Slides ([pdf](http://bergeron.math.uqam.ca/Especes_trans.pdf)).
* G. Labelle, [video](http://www.sms.cam.ac.uk/media/937;jsessionid=9540827CB40AC9F1E61BF944127EBAF4) intro into combinatorial species at Newton Institute, Cambridge 2008
* {#Aguiar10} [[Marcelo Aguiar]], Swapneel Mahajan, _[[Monoidal Functors, Species and Hopf Algebras]]_, With forewords by Kenneth Brown, Stephen Chase, [[André Joyal]]. CRM Monograph Series __29__ Amer. Math. Soc. 2010. lii+784 pp. ([pdf draft](http://www.math.tamu.edu/~maguiar/a.pdf))

An application in computer science: 

* Brent Yorgey, _Random testing and beyond! with combinatorial species_, slides [pdf](http://www.cis.upenn.edu/~byorgey/talks/combtesting-ku-20091124.pdf); _Species and functors and types, oh my_, article, [pdf](http://www.cis.upenn.edu/~byorgey/papers/species-pearl.pdf)

An application in statistical mechanics:

* W. Faris, _Combinatorial species and cluster expansions_, Mosc. Math. J. __10__:4 (2010), 713&#8211;727 [pdf](http://www.ams.org/distribution/mmj/vol10-4-2010/faris.pdf), [MR2791054](http://www.ams.org/mathscinet-getitem?mr=2791054)

An application to Feynman diagrams:

* {#Baez01} [[John Baez]] and [[James Dolan]], From finite sets to Feynman diagrams, in _Mathematics Unlimited - 2001 and Beyond_, vol. 1, eds. Bj&#246;rn Engquist and Wilfried Schmid, Springer, Berlin, 2001, pp. 29-50.  ([arXiv](http://arxiv.org/abs/math.QA/0004133))

Formalization in homotopy type theory:

* {#Dougherty15} [[John Dougherty]], _Species in HoTT_ ([pdf](https://github.com/jdoughertyii/hott-species/blob/master/species.pdf?raw=true)) ([formalization in Coq](https://github.com/jdoughertyii/hott-species))

[[!redirects homotopical species]]
[[!redirects (infinity,1) species]]
[[!redirects ∞-species]]
[[!redirects combinatorial species]]

