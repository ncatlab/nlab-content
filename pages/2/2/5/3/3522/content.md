

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Goodwillie calculus
+--{: .hide}
[[!include Goodwillie calculus - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Goodwillie calculus is an [[(∞,1)-category theory|(∞,1)-]][[categorification]] of [[differential calculus]], where [[smooth functions]] between [[Cartesian spaces]] are replaced by [[topological functors]] between [[categories]] of [[pointed topological spaces]].
 
### As an approximation to stabilization of a functor

The operation of [[stabilization]] that sends an [[(∞,1)-category]] $C$ to the [[stable (∞,1)-category]] $Stab(C)$ does not in general extend to a functor.

We may think of this operation as the analog of _linearizing_ a space. Turning an [[(∞,1)-functor]] $F \colon C \to D$ into a functor $Stab(C) \to Stab(D)$ is not unlike performing a first order [[Taylor expansion]] of a function, whence one speaks here of [[Goodwillie-Taylor towers]].

This is what Goodwillie calculus studies.

Let $F: \mathcal{C} \to \mathcal{D}$ (where $\mathcal{C}$ and $\mathcal{D}$ are each either $Top_*$, the category of [[pointed topological spaces]], or $Spec$, the category of [[spectra]]) be a pointed homotopy functor. Associate with $F$ a sequence of spectra, called the derivatives of $F$, denoted by $\partial_1 F, \partial_2 F,\cdots, \partial_n F, \cdots$, or, collectively, by $\partial_* F$. For each $n$ the spectrum $\partial_n F$ has a natural [[action]] of the [[symmetric group]] $\Sigma_n$. Thus, $\partial_\bullet F$ is a [[symmetric sequence]] of spectra.

The Goodwillie-derivatives of $F$ contain substantial information about the homotopy type of $F$. We can form a sequence of 'approximations' to $F$ together with natural transformations forming a *[[Goodwillie-Taylor tower]]*. This tower takes the form

$$
F \to \cdots \to P_n F \to P_{n-1} F \to \cdots\to P_0 F
$$

with $P_n F$ being the universal *n-excisive* approximation to $F$. (A functor is [[n-excisive (∞,1)-functor|n-excisive]] if it takes any $n + 1$-dimensional cube with homotopy pushout squares for faces to a homotopy cartesian cube.) For '[[analytic (∞,1)-functors]]' $F$, this tower converges for sufficiently highly connected $X$, that is

$$
F(X) \simeq \underset{n}{holim} P_n F(X).
$$

The fibre $D_n F$ of the map $P_n F \to P_{n-1} F$ is an *n-homogeneous* functor in an appropriate sense, and is determined by $\partial_n F$, via the following formula. If $F$ takes values in $Spec$ then

$$
D_n F(X) \simeq (\partial_n F \wedge X^{\wedge n})_{h \Sigma_n}.
$$

If $F$ takes values in $Top_*$ then one needs to prefix the right hand side with $\Omega^{\infty}$. (Arone & Ching)


### Analogy between homotopy theory and calculus {#Analogy}

Here is an overview of the relation between [[homotopy theory]]/[[∞-groupoid]] theory and [[algebraic approaches to differential calculus|differential calculus]] that is the starting point for Goodwillie calculus. 

> based on a message by [[André Joyal]] to the Category Theory Mailing list, May 12, 2010

Write $k[ [x] ]$ for the [[ring]] of [[formal power series]] in one
variable over a [[field]] $k$. The ring $k[ [x] ]$ bears some resemblances
with the category of [[pointed object|pointed]] [[homotopy type]]s (= pointed spaces up to [[weak homotopy equivalence]]s). The category of pointed
homotopy types is a ring (the product is the [[smash product]]
and the sum is the [[wedge sum]]).


The following dictionary indicates what the correspondence between the two subjects is.

* $k$ $\stackrel{\text{corresponds to}}{\mapsto}$ the category of [[pointed set]]s;

* $k[ [x] ]$ 
  $\mapsto$ 
  the category of pointed [[homotopy type]]s;

* $x$ $\mapsto$ the pointed circle;

* the augmentation $(k[ [x] ] \to k)$ 
  $\mapsto$ 
  the [[homotopy group|connected components functor]] 
  $\pi_0$ :  pointed homotopy types $\to$ pointed sets

* the augmentation ideal $J$
  $\mapsto$
  the [[subcategory]] of pointed [[connected]] spaces;

* the $n+1$ power of the augmentation ideal 
  $J^{n+1}$
  $\mapsto$
  the subcategory of pointed $n$-[[connected]] spaces;

* the product of an element in $J^{n+1}$ 
  with an element of $J^{m+1}$ is an element of 
  $J^{n+m+2}$
  $\mapsto$
  the [[smash product]] of an $n$-[[connected]] space 
  with a $m$-connected space is $(n+m+1)$-connected;

* multiplication by $x$ $\mapsto$ the [[suspension]] functor.

* division by $x$ $\mapsto$ the [[loop space]] functor;

  Notice here the difference: the loop functor is 
  [[right adjoint]] to the suspension functor, not its [[inverse]]. 
  Moreover, the loop space of a space has a special structure 
  (it is a [[group object in an (infinity,1)-category|group]]).

* the ideal $J=x k[ [x] ]$ is [[isomorphism|isomorphic]] 
  to $k[ [x] ]$ via division by $x$
  $\mapsto$
  similarly, the category of pointed connected spaces is equivalent 
  to the category of topological groups via the loop space 
  functor (it is actually an [[Quillen equivalence]] 
  of [[model categories]]).

* More generally, the ideal $J^{n+1}$ is isomorphic to 
  $k[ [x] ]$ via division by $x^{n+1}$.
  $\mapsto$
  similarly, the category of $n$-connected spaces is 
  equivalent to the category of $(n+1)$-fold 
  [[topological group]]s 
  (it is actually an [[Quillen equivalence]] of 
  [[model categories]]) via the $(n+1)$-fold loop space functor.

* the quotient ring $k[ [x] ]/J^{n+1}$ $\mapsto$
  the category of $n$-truncated homotopy types 
  (=[[homotopy n-type]]s)

* The sequence of approximations of a 
  formal power series $f(x)=a_0+a_1x+ \cdots $

  $a_0$

  $a_0+a_1 x$

  $a_0+a_1 x + a_2 x^2$

  $\cdots$

  $\mapsto$

  the [[Postnikov tower]] of a pointed homotopy type $X$:

  $[\pi_0(X)]$

  $[\pi_0(X); \pi_1(X)]$

  $[\pi_0(X); \pi_1(X); \pi_2(X)]$

  $\cdots$

  Here, $\pi_0(X)$ is the set of connected components of 
  $X$, $[\pi_0(X); \pi_1(X)]$ is the [[fundamental groupoid]] 
  of $X$,
  $[\pi_0(X); \pi_1(X); \pi_2(X)]$
  is the fundamental 2-groupoid of $X$, etc.


* The differences between $f(x)$ and its successives approximations

  $$
   \begin{aligned}
     R_0 = f(x)-a_0  &= a_1 x+a_2 x^2+a_3 x^3+ \cdots
     \\
     R_1 = f(x)-(a_0+a_1 x) &= a_2 x^2 + a_3 x^3 + a_4 x^4+ \cdots
     \\
     R_2 = f(x)-(a_0+a_1x+a_2x^2) &= a_3 x^3 + a_4 x^4 + a_5 x^5 +\cdots
   \end{aligned}
  $$

  $\mapsto$
  
  the [[Whitehead tower]] of $X$,

  $C_0=[0;\pi_1(X), \pi_2(X), \pi_3(X), \cdots]$

  $C_1=[0;0, \pi_2(X), \pi_3(X), \cdots]$

  $C_2=[0;0, 0, \pi_3(X), \cdots]$

  Here, $C_0$ is the connected component of $X$ at the base point,
  $C_1$ is the [[universal cover]] of $X$ constructed by from 
  paths starting at the base point,
  $C_2$ is the universal 2-cover of $X$ 
  constructed from paths starting the base point, etc.

* Division by $x$ is shifting down the coefficients of a 
  power series.

  If $f(x)=a_1 x+a_2 x^2 + \cdots$, 
  then $f(x)/x= a_1+a_2 x+ \cdots $

  Similarly, the loop space functor is shifting down 
  the homotopy groups
  of a pointed space: 

  if $X=[a_0,a_1,a_2,...]$ then $\Omega(X)=[a_1,a_2,....]$.

  Unfortunately, the [[suspension]] functor does not shift 
  up the [[homotopy group]]s of a space. It is however shifting 
  the first $2n$ homotopy groups of an $n$-connected space $X$ 
  $(n \geq 1)$ by the
  [[Freudenthal suspension theorem]]

  For example, if $X=[0;0,a_2, a_3,...]$ then 
  $\Sigma X=[0;0,0,a_2,a_3...]$,
  and if $X=[0;0,0, a_3, a_4, a_5,...]$ then 
  $\Sigma X=[0;0,0, 0, a_3, a_4, a_5,...]$.

  In other words, the canonical map $X \to \Omega X$
  is a $2n$-equivalence if $X$ is $n$-[[connected]] 
  $(n \geq 1)$.
  If $X[2n]$ denotes the $2n$-type of $X$ 
  (the $2n$-[[truncated|truncation]] of $X$),
  then we have a [[homotopy equivalence]]

  $X[2n]  \to \Omega \Sigma X[2n] \simeq \Omega \Sigma X[2n+1]$.


...

From a blog [discussion](http://golem.ph.utexas.edu/category/2008/12/smooth_structures_in_ottawa.html#c020698)

[Arone Kankaanrinta 95](#AroneKankaanrinta95) write

>The Goodwillie tower of the identity...is a tower of functors and natural transformations, which starts with stable homotopy and converges to unstable homotopy. (p. 1)

>...the Goodwillie tower is an inverse to stable homotopy in the same way as logarithm is an inverse to exponential. (p. 1)

>It is the point of this paper that the Goodwillie tower is the homotopy theoretic analog of logarithmic expansion, rather than of Taylor series. (p. 6)

What's going on, they say, is like finding a function of the form $a^{x - 1}$ which best approximates $x$. This is when $a = e$.

The functor from spaces to spaces which sends $X$ to the [[infinite loop space]] underlying its [[suspension spectrum]]

$$
\Omega^{\infty}\Sigma^{\infty} X = colim \Omega^n \Sigma^n X
$$

sends coproducts to products and is supposed to be like $e^{x - 1}$.
(The "$-1$" comes about from issues to do with basepoints.)

A homogeneous linear functor is defined to be one sending coproducts to products, so it is like an [[exponential map|exponential]].  Compared to an exponential, the [[identity functor]] is like a [[logarithm]], so it has a non-trivial Taylor series.

>...our point of view is that stable homotopy is analogous to the function $e^{x - 1}$ rather than to a linear function, and the Goodwillie tower is an infinite product, rather than an infinite sum, namely it is analogous to the product

$$
e^{x - 1} \cdot e^{-\frac{(x - 1)^2}{2}} \cdot e^{\frac{(x - 1)^3}{3}} \ldots = e^{ln(1 + (x - 1))} = x. 
$$

>(p. 2)

Gregory Arone in an MO [answer](http://mathoverflow.net/questions/32071/is-the-dual-notion-of-a-presheaf-useful)

>Covariant functors from the category of pointed sets to the category of pointed topological spaces are sometimes called $\Gamma$-spaces, and they have been important in algebraic topology. One reason is that $\Gamma$-[[Gamma-space|spaces]] model infinite loop spaces (and therefore connective spectra) and are very helpful for understanding stable homotopy theory.

>$\Gamma$-spaces also serve as a model for particularly well-behaved covariant functors from the category of pointed topological spaces to itself. Of course, these functors play an important role in topology as well. I like to think of Goodwillie's Calculus of Homotopy Functors (and also of Michael Weiss's Orthogonal Calculus) as a kind of "sheaf theory for covariant functors". In these theories, covariant functors are analogous to presheaves and linear functors are analogous to sheaves (The definition of a linear functor is essentially a homotopy-invariant version of the definition of a sheaf). The process of approximating a general functor by a linear one is analogous to sheafification, and so forth. These theories provide methods for studying certain types of functors, but of course they also tell you something about the category of spaces itself.

Eric Finster's research statement

>One tantalizing aspect of the Goodwillie calculus is that it suggests the possibility of thinking geometrically about the global structure of homotopy theory. In this interpretation, the category of spectra plays the role of the tangent space to the category of spaces at the one-point space. Moreover, the identity functor from spaces to spaces is not linear...and one can interpret this as saying that spaces have some kind of non-trivial curvature.

However, Goodwillie remarks in the [report](#OWR2004) (p. 905) on a Oberwolfach meeting.:

>Rhetorical question: If the first derivative of the identity is the identity matrix, why is the second derivative not zero? Answer: Some of the terminology of homotopy calculus works better for functors from spaces to spectra than for functors from spaces to spaces. Specifically, since "linearity" means taking pushout squares to pullback squares, the identity functor is not linear and the composition of two linear functors is not linear.

>Attempted cryptic remark: Unlike the category of spectra, where pushouts are the same as pullbacks, the category of spaces may be thought of has having nonzero curvature.

>Correction: After the talk Boekstedt asked about that remark. We discussed the matter at length and found more than one connection on the category of spaces, but none that was not flat. In fact curvature is the wrong thing to look for. There are in some sense exactly two tangent connections on the category of spaces (or should we say on any model category?). Both are  flat and torsion-free. There is a map between them, so it is meaningful to subtract them. As is well-known in differential geometry, the difference between two connections is a 1-form with values in endomorphisms (whereas the curvature is a 2-form with values in endomorphisms). Thus there is a way of discussing the discrepancy between pushouts and pullbacks in the language of differential geometry, but it is a tensor field of a different type from what I had guessed.

This is from the [report](#OWR2004) (p. 905) on a Oberwolfach meeting. The table on p. 900 also makes comparisons to differential geometry.

Chris Schommer-Pries

>Any linear functor from spaces to spaces is a generalized cohomology theory. More precisely, there is a model category on the functors from spaces to spaces called the model category of W-spaces. Really I should be using pointed spaces here. This model category is one of the standard models for the category spectra and so the fibrant objects can be thought of as the (co)homology theories. The fibrant objects are precisely those functors which are linear in Goodwillie's sense. The example $S P^{\infty}$ corresponds to ordinary cohomology (well there is a $\pi_0$ issue, but let's ignore that). In general evaluating the linear functor $E$ on a space $X$ gives you a space which should be thought of as the smash product of $E$ and $X$.

>So now why should spectra/cohomology theories be thought of as linear functors? Well if you think of spectra as analogous to abelian groups, then applying a spectrum to a space (i.e. smashing with it) is a linearization of that space.

>Following this analogy, if we now have any old functor from space to spaces we can take its fibrant replacement in $W$-spaces. This is a linear functor which is the best approximation to the original functor. So it is like taking a derivative of a function. Goodwillie's insight was to extend this analogy to encompass the rudiments of calculus. There is in fact  a whole series of model categories on functors from spaces to spaces where the fibrant objects are Goodwillie's polynomial functors of degree $n$.

See also Eric Finster's blog post [Thoughts on the Goodwillie Calculus](https://web.archive.org/web/20121114044441/https://curiousreasoning.wordpress.com/2010/08/02/thoughts-on-the-goodwillie-calculus/)

## Properties

### $\infty$-Toposes of polynomial $(\infty, 1)$-functors

For each $n$, the collection of [[n-excisive (∞,1)-functors]] from bare [[homotopy types]] to bare homotopy types is an [[(infinity,1)-topos]], the _[jet topos](jet+category#JetToposes)_.


due to ( [Joyal 08, 35.5](#Joyal08), with [[Georg Biedermann]]) See also at _[[tangent (infinity,1)-category]]_, and [[Charles Rezk]], appears as ([Lurie, remark 6.1.1.11](#HigherAlg)).

## Examples

### Goodwillie derivatives of the identity functor

The Goodwillie derivatives of the [[identity functor]] on  [[pointed topological spaces]], form an [[operad]] in [[spectra]] ([Ching 05](#Ching05)).

See at _[[Goodwillie derivatives of the identity functor]]_ 

### Goodwillie derivatives of exponential modality
 {#GoodwillieDerivativeOfExponentialModality}

The ([[(infinity,1)-functor|$\infty$-]])functor

$$
  \Sigma^\infty \circ \Omega^\infty
  \;\colon\;
  Spectra \to Spectra
$$

[induced](monad#RelationBetweenAdjunctionsAndMonads) from the [[stabilization]]-[[adjoint (infinity,1)-functor|adjunction]] is (see [there](!-modality#RealizationInLinearHomotopyTypeTheory)) the [[exponential modality]] in [[linear homotopy type theory]] (or rather the un-pointed version is). Indeed, in Goodwillie calculus it behaves like an [[exponential function]] ("minus 1"), for instance in that 

* all its higher [[Goodwillie derivatives]] are the [[unit object|unit]] [[sphere spectrum]], and

* on [[suspension spectra]] $\mathbb{X} \equiv \Sigma^\infty_+ X$ we have

  $$
    \Sigma^\infty \Omega^\infty \mathbb{X}
    \;\simeq\;
    \underset{n \geq 1}{\oplus}
    \mathbb{X}^{\wedge n} \sslash Sym(n)
    \,.
  $$

([Arone & Ching 2019, Exp. 2.6](#AroneChing19), using [Ahearn & Kuhn 2002, Cor. 1.3](#AhearnKuhn02))



### Goodwillie derivatives of mapping spaces

See at _[[stable splitting of mapping spaces]]_.



## Related concepts

* [[Goodwillie spectral sequence]]

* [[Goodwillie-differentiable (∞,1)-category]]

* [[excisive (∞,1)-functor]], [[n-excisive (∞,1)-functor]]

* [[Taylor tower]]

* [[Goodwillie differentiation]], [[Goodwillie chain rule]]

* [[Goodwillie derivative of the identity functor]]

* [[tangent (∞,1)-category]], [[tangent cohesion]]

* [[jet (∞,1)-category]]

* [[orthogonal calculus]]

* [[Weiss topology]]

* [[manifold calculus]]

## References

The original articles:

* {#Goodwillie90} [[Tom Goodwillie]], _The differential calculus of homotopy functors_, Proceedings of the International Congress of Mathematicians in Kyoto 1990, Vol. I, Math. Soc. Japan, 1991, pp. 621–6 ([article pdf](https://math.mit.edu/juvitop/old/notes/2009_Fall/goodwillie-icm.pdf), [full proceedings Vol I pdf](https://www.mathunion.org/fileadmin/ICM/Proceedings/ICM1990.2/ICM1990.2.ocr.pdf), [[GoodwillieICM1990.pdf:file]])

* [[Thomas Goodwillie]], _Calculus. I. The first derivative of pseudoisotopy theory_, K-Theory __4__ (1990), no. 1, 1-27 ([doi:10.1007/BF00534191](http://dx.doi.org/10.1007/BF00534191), MR:1076523)

* [[Thomas Goodwillie]], _Calculus. II. Analytic functors_, K-Theory __5__ (1991/92), no. 4, 295-332 ([doi:10.1007/BF00535644](http://dx.doi.org/10.1007/BF00535644), MR:1162445)

* [[Thomas Goodwillie]], _Calculus. III. Taylor series_, Geom. Topol. 7 (2003), 645--711 ([euclid:gt/1513883319](https://projecteuclid.org/euclid.gt/1513883319) [doi:10.2140/gt.2003.7.645](http://dx.doi.org/10.2140/gt.2003.7.645), [arXiv:math/0310481](http://arxiv.org/abs/math/0310481))


* {#OWR2004} The Goodwillie Calculus of Functors. Workshop Oberwolfach Report 17 (2004) &lbrack;[doi:10.4171/OWR/2004/17](https://doi.org/10.14760/OWR-2004-17)&rbrack;


Surveys and introductions:

* [[Brian Munson]], _Introduction to the manifold calculus of Goodwillie-Weiss_,  Morfismos, Vol . 14, No. 1, 2010, pp. 1-60 ([arXiv:1005.1698](https://arxiv.org/abs/1005.1698))

* {#MunsonVolic15} [[Brian Munson]], [[Ismar Volic]], Section 10 of: _Cubical homotopy theory_, Cambridge University Press, 2015  ([pdf](http://palmer.wellesley.edu/~ivolic/pdf/Papers/CubicalHomotopyTheory.pdf), [doi:10.1017/CBO9781139343329](https://doi.org/10.1017/CBO9781139343329))

* [[Michael Ching]], [[Nicholas Kuhn]], [[Victor Turchin]], _[Functor Calculus and Operads](http://www.birs.ca/events/2011/5-day-workshops/11w5058)_, BANFF Workshop 2011

* [[Gregory Arone]], [[Michael Ching]] _[Talbot Workshop 2012: Calculus of Functors](https://math.mit.edu/events/talbot/index.php?year=2012)_ ([Talk schedule](https://math.mit.edu/events/talbot/2012/2012TalbotTalks.pdf), [Notes](https://math.mit.edu/events/talbot/index.php?year=2012&sub=talks))

* {#AroneChing19} [[Gregory Arone]], [[Michael Ching]], *Goodwillie Calculus*, in: *[[Handbook of Homotopy Theory]]* Taylor & Francis (2019) &lbrack;[arXiv:1902.00803](https://arxiv.org/abs/1902.00803),[doi:10.1201/9781351251624](https://doi.org/10.1201/9781351251624)&rbrack;


A [[model category]] presentation for [[n-excisive functors]]:

* [[Georg Biedermann]], [[Boris Chorny]], Oliver R&#246;ndigs, _Calculus of functors and model categories_, Adv. Math., __214__, n. 1 (2007) 92--115, [doi](http://dx.doi.org/10.1016/j.aim.2006.10.009), [math.AT/0601221](http://arxiv.org/abs/math/0601221)

* [[Gregory Arone]], [[Michael Ching]], _Operads And Chain Rules For The Calculus Of Functors_, [arXiv:0902.0399](https://arxiv.org/abs/0902.0399)

* [AroneMahowald 98](#AroneMahowald98)

* {#AroneKankaanrinta95} [[Gregory Arone]], Marja Kankaanrinta,  _The Goodwillie tower of the identity is a logarithm_, 1995 ([[Arone95.pdf:file]], [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.53.8306))


See also:

* {#AhearnKuhn02} [[Stephen T. Ahearn]], [[Nicholas J. Kuhn]], *Product and other fine structure in polynomial resolutions of mapping spaces*, Algebr. Geom. Topol. **2** (2002) 591-647 &lbrack;[arXiv:math/0109041](https://arxiv.org/abs/math/0109041), [doi:10.2140/agt.2002.2.591](https://doi.org/10.2140/agt.2002.2.591)&rbrack;


* Andrew Mauer-Oats, _Algebraic Goodwillie calculus and a cotriple model for the remainder_, Trans. Amer. Math. Soc. __358__  (2006),  no. 5, 1869--1895 [journal](http://www.ams.org/tran/2006-358-05/S0002-9947-05-03936-X/home.html), [math.AT/0212095](http://arxiv.org/abs/math/0212095)

* [[David Barnes]], [[Rosona Eldred]], *Capturing Goodwillie's Derivative*, Journal of Pure and Applied Algebra
**220** 1 (2016) 197-222 &lbrack;[arXiv:1406.0424](https://arxiv.org/abs/1406.0424), [doi:10.1016/j.jpaa.2015.06.006](https://doi.org/10.1016/j.jpaa.2015.06.006)&rbrack;

Discussion in the context of [[chromatic homotopy theory]]:

* {#AroneMahowald98} [[Greg Arone]], [[Mark Mahowald]], _The Goodwillie tower of the identity functor and the unstable periodic homotopy of spheres_, Inventiones mathematicae, February 1999, Volume 135, Issue 3, pp 743-788 ([pdf](http://hopf.math.purdue.edu/Arone-Mahowald/ArMahowald.pdf), [doi:10.1007/s002220050300](https://doi.org/10.1007/s002220050300))

* [[Nicholas Kuhn]], _Goodwillie towers and chromatic homotopy: an overview_,   Proceedings of the Nishida Fest (Kinosaki 2003),  245--279, Geom. Topol. Monogr., 10, Geom. Topol. Publ., Coventry, 2007 ([arXiv:math/0410342](https://arxiv.org/abs/math/0410342), [doi:10.2140/gtm.2007.10.245](http://dx.doi.org/10.2140/gtm.2007.10.245))


Discussion via [[(∞,1)-categories]] and [[stable (∞,1)-categories]]:

* [[Jacob Lurie]], _[[(∞,2)-Categories and the Goodwillie Calculus]]_, [section 5](http://www.math.harvard.edu/~lurie/papers/GoodwillieI.pdf#page=159)

This is now section 7 of 

* {#HigherAlg} [[Jacob Lurie]], _[[Higher Algebra]]_

See also

* Luis Pereira, _A general context for Goodwillie Calculus_ ([arXiv:1301.2832](http://arxiv.org/abs/1301.2832))

* {#Joyal08} [[André Joyal]], _Notes on Logoi_, 2008 ([pdf](http://www.math.uchicago.edu/~may/IMA/JOYAL/Joyal.pdf))
  

Generalization from [[(infinity,1)-categories]] to [[(infinity,n)-categories]] and relation to [[rational homotopy theory]] is discussed in 

* [[Gijs Heuts]], _Goodwillie approximations to higher categories_ ([arXiv:1510.03304](http://arxiv.org/abs/1510.03304))


Relation to [[chromatic homotopy theory]] is discussed in 

* [[Greg Arone]], [[Mark Mahowald]], _The Goodwillie tower of the identity functor and the unstable periodic homotopy of spheres_, Inventiones mathematicae, 1999, Volume 135, Issue 3, pp 743-788 ([pdf](http://hopf.math.purdue.edu/Arone-Mahowald/ArMahowald.pdf))

* [[Nicholas Kuhn]], _Goodwillie towers and chromatic homotopy: an overview_, Geom. Topol. Monogr. 10 (2007) 245-279 ([arXiv:math/0410342](http://arxiv.org/abs/math/0410342))

On the relation to [[configuration space (mathematics)|configuration spaces]]:

* {#Ching05} [[Michael Ching]], _Bar constructions for topological operads and the Goodwillie derivatives of the identity_, Geom. Topol. 9 (2005) 833-934 ([arXiv:math/0501429](https://arxiv.org/abs/math/0501429))

* {#Ching05b} [[Michael Ching]], _Calculus of Functors and Configuration Spaces_, Conference on Pure and Applied Topology Isle of Skye, Scotland, 21-25 June, 2005 ([pdf](https://www3.amherst.edu/~mching/Work/skye.pdf))

Discussion in terms of [[spectral Mackey functors]]

* {#Glasman15} [[Saul Glasman]], _Stratified categories, geometric fixed points and a generalized Arone-Ching theorem_ ([arXiv:1507.01976](https://arxiv.org/abs/1507.01976), [talk notes pdf](http://www-users.math.umn.edu/~sglasman/strattalk.pdf))

* {#Glasman16} [[Saul Glasman]], _Goodwillie calculus and Mackey functors_  ([arXiv:1610.03127](https://arxiv.org/abs/1610.03127))

Discussion in an [[equivariant]] setting is in

* Emanuele Dotto, _Higher Equivariant Excision_, ([arXiv:1507.01909](https://arxiv.org/abs/1507.01909))


[[!redirects Goodwillie derivative]]
[[!redirects Goodwillie derivatives]]

[[!redirects Goodwillie calculus of functors]]

