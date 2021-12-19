
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

In a [[model category]] fibrations enjoy [[pullback stability]] and cofibrations are stable under [[pushout]], but weak equivalences need not have either property. In a proper model category weak equivalences are also preserved under certain pullbacks and/or certain pushouts.

Put differently, in a proper model category, [[homotopy pullbacks]] and/or pushouts can be computed with less need for [[fibrant replacement|fibrant and/or cofibrant replacement]].



## Definition ##

+-- {: .num_defn}
###### Definition

A [[model category]] is called 

* **right proper** if weak equivalences are preserved by [[pullback]] along fibrations

* **left proper** if weak equivalence are preserved by [[pushout]] along cofibrations

* **proper** if it is both left and right proper.

=--


+-- {: .num_remark}
###### Remark

More in detail this means the following. 
A model category is right proper if for every weak equivalence $f : A \to B$ in $W\subset Mor(C)$ and every fibration $h : C \to B$ the pullback $h^* f : A \times_B C \to C$ in

$$
  \array{
    A \times_C B &\to& A
    \\
    \;\;\downarrow^{\mathrlap{\Rightarrow h^* f \in W}} && \downarrow^{\mathrlap{f \in W}}
    \\
    C &\stackrel{h \in F}{\to}& B
  }
$$

is a weak equivalence.

=--

\begin{remark}
The above definition is the way it is usually phrased, but in fact it is equivalent to a seemingly weaker condition that is sometimes easier to check: for right properness it suffices to assume that weak equivalences are preserved by pullback along fibrations *between fibrant objects*.  That is, in the more explicit version above, we are free to assume that $B$ (hence also $C$) is fibrant; this then implies the more general version without this hypothesis.  See Proposition \ref{FibrationsBetweenFibrantObjectsSuffice} below.
\end{remark}


## Examples 
 {#Examples}


### Left proper model categories

* by cor. \ref{AllObjectsFibrantImpliesRightProper}, every model category in which all objects are cofibrant is left proper;

  this includes notably

  * the [[classical model structure on simplicial sets]]

  * the [[model structure for quasi-categories]]

  and many model structures derived from these, such as 

  * the injective global [[model structure on simplicial presheaves]] over any (simplicial) category;

* the left [[Bousfield localization]] of every left proper [[combinatorial model category]] at a set of morphisms is again left proper.

  So in particular also the _local_ injective model structures on
  simplicial presheaves over a [[site]] are left proper.  

### Non-left proper model categories

A class of model structures which tends to be _not_ left proper are model structures on categories of not-necessarily commutative algebras. 

For instance 

* the standard model structure on [[simplicial object|simplicial]] [[associative unital algebra]]s (weak equivalences and fibrations are those of the underlying simplicial sets) is  _not_  left proper (see [Rezk2000, example 2.11](http://arxiv.org/PS_cache/math/pdf/0003/0003065v1.pdf#page=5))

But it is [[Quillen equivalence|Quillen equivalent]] to a model structure that _is_ left proper. This is discussed [below](#ProperEquivModels).


### Right proper model categories ###

* by cor. \ref{AllObjectsFibrantImpliesRightProper} every model category in which each object is fibrant is right proper.

  This includes for instance the standard [[Quillen model structure on topological spaces]]. 

* The [[classical model structure on simplicial sets]] is (automatically left proper, since all objects are cofibrant, but also) right proper, even though not all objects are fibrant.  See [there](classical+model+structure+on+simplicial+sets#Properness).


### Non-right proper model categories

* "Non-algebraic" models for higher categories (other than higher groupoids) are generally not right proper.  For example, the [[model structure for complete Segal spaces]] and the [[model structure for quasi-categories]] are not right proper (see [mathoverflow](http://mathoverflow.net/questions/40938/is-the-model-category-of-complete-segal-spaces-right-proper)).


### Proper model categories ###

Model categories which are both left and right proper include

* [[Top]]: [[classical model structure on topological spaces]] ([prop.](classical+model+structure+on+topological+spaces#Properness))

* [[sSet]]: [[classical model structure on simplicial sets]] ([here](classical+model+structure+on+simplicial+sets#Properness))

* The _global_ [[model structure on simplicial presheaves]] and any local such model structure over a site with [[point of a topos|enough points]] and weak equivalences the [[stalk]]wise weak equivalences.

* {#ModelStructureOnChainComplexesIsProper} The standard [[model structures on chain complexes]] (see [there](model+structure+on+chain+complexes#Properness)).

* The projective [[model structure on differential graded-commutative algebras]] (unbounded). See [this MO discussion](http://mathoverflow.net/q/204414/381).


### Proper Quillen equivalent model structures {#ProperEquivModels}

While some model categories fail to be proper, often there is a [[Quillen equivalence|Quillen equivalent]] one that does enjoy properness.

+-- {: .num_theorem}
###### Theorem

Every model category whose acyclic cofibrations are [[monomorphism]]s is Quillen equivalent to its [[model structure on algebraic fibrant objects]].
In this all objects are fibrant, so that it is right proper.

=--

([Nikolaus 10, theorem 2.18](#Nikolaus10))





+-- {: .num_theorem}
###### Theorem

Let $T$ be a simplicial (possibly multi-colored) [[theory]], and let $T Alg$ be the corresponding category of simplicial T-algebras. This carries a model category structure where the fibrations and weak equivalences are those of the underlying simplicial sets in the [[classical model structure on simplicial sets]]. 

Then there exists a morphism of simplicial theories $T \to S$ such that

1. the induced [[adjunction]] $S Alg \stackrel{\to}{\leftarrow} T Alg$ is a [[Quillen equivalence]];

1. $S Alg$ is a proper [[simplicial model category]]. 


=--


This is the content of ([Rezk 02](#Rezk02))





## Properties 

### General

The following says that left/right properness holds _locally_ in every model category, namely between cofibrant/fibrant objects.

+-- {: .num_prop #GoodPullbacksAndPushouts}
###### Proposition

Given a [[model category]],

1. every [[pushout]] of a [[weak equivalence]] between [[cofibrant objects]] along a [[cofibration]] is again a weak equivalence;

1. every [[pullback]] of a [[weak equivalence]] between [[fibrant objects]] along a [[fibration]] is again a weak equivalence.

=--

A proof is spelled out in ([Hirschhorn, prop. 13.1.2](#Hirschhorn)), there attributed to ([Reedy](#Reedy)).

This gives a large class of examples of left/right proper model categories:

+-- {: .num_cor #AllObjectsFibrantImpliesRightProper}
###### Corollary

A model category in which all objects are cofibrant is left proper.

A model category in which all objects are fibrant is right proper.

=--

See in the list of [Examples](#Examples) below for concrete examples.

Notice that the prop. \ref{GoodPullbacksAndPushouts} applies only (in the right proper case, for concreteness) to pullbacks of fibrations along weak equivalences in which *all three* objects are fibrant, since a fibration with fibrant codomain also has fibrant domain.  The definition of right proper, on the other hand, states this property in the case when *none* of the objects are assumed to be fibrant.

One might consider as an "in-between" assumption the situation when only the common codomain of the fibration and the weak equivalence (hence also the domain of the fibration) are fibrant; but it turns out that this apparently-weaker assumption is sufficient to imply full right properness.  This can be found, for instance, as Lemma 9.4 of [Bousfield 2001](#Bousfield01).

+-- {: .num_prop #FibrationsBetweenFibrantObjectsSuffice}
###### Proposition
Suppose that in some model category, if $X\to Y$ is a fibration and $Z\to Y$ a weak equivalence, with $Y$ (hence also $X$) fibrant, then the pullback $X\times_Y Z \to X$ is a weak equivalence.  Then the model category is right proper, i.e. the same statement is true without the assumption that $Y$ is fibrant.
=--
+-- {: .proof}
###### Proof
Suppose given $X\to Y\leftarrow Z$ where $X\to Y$ is a fibration and $Z\to Y$ a weak equivalence.  Choose a fibrant replacement $Y\to R Y$, and factor $X\to Y \to R Y$ as a weak equivalence $X\to R X$ followed by a fibration $R X \to R Y$.  The assumption now applies to the cospan $R X \to R Y \leftarrow Y$, so that the map $R X \times_{R Y} Y \to R X$ is a weak equivalence.  By 2-out-of-3, the induced map $X \to R X \times_{R Y} Y$ is also a weak equivalence.

Now by [[Ken Brown's lemma]], the pullback functor along $Z\to Y$ preserves weak equivalences between fibrant objects, and in particular preserves this weak equivalence $X \to R X \times_{R Y} Y$.  Thus, the induced map $X\times_Y Z \to R X \times_{R Y} Z$ is a weak equivalence.  However, $R X \times_{R Y} Z \to R X$ is a weak equivalence by the assumption, so by 2-out-of-3, the map $X\times_Y Z \to X$ is also a weak equivalence, as desired.
=--


### Homotopy (co)limits in proper model categories ###
 {#HomotopyLimits}

+-- {: .num_prop #PullbackAlongFibrationsAreHomotopyPullbacks}
###### Proposition


In a left proper model category, ordinary [[pushouts]] along cofibrations are [[homotopy pushouts]].

Dually, in a right proper model category, ordinary [[pullbacks]] along fibrations are [[homotopy pullbacks]].

=--

+-- {: .proof}
###### Proof

This is stated for instance in [[Higher Topos Theory|HTT, prop A.2.4.4]] or in prop. 1.19 in
[Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf). We follow the proof given in this latter reference.

We demonstrate the first statement, the second is its direct formal dual.

So consider a [[pushout]] diagram

$$
  \array{
    K &\to& Y
    \\
    \downarrow^{\mathrlap{\in cof}} && \downarrow
    \\
    L &\to& X
  }
$$

in a left proper model category, where the morphism $K \to L$ is a cofibration, as indicated. We need to exhibit a weak equivalence $X' \stackrel{}{\to} X$ from an object $X'$ that is manifestly a [[homotopy pushout]] of $L \leftarrow K \to Y$.

The standard procedure to produce this $X'$ is to pass to a weakly equivalent diagram with the property that all objects are cofibrant and one of the morphisms is a cofibration. The ordinary pushout of that diagram is well known to be the [[homotopy pushout]], as described there.

So pick a cofibrant replacement $\emptyset \hookrightarrow K' \stackrel{\simeq}{\to}$ of $K$ and factor $K' \to K \to Y$ as a cofibration followed by a weak equivalence
$K' \hookrightarrow Y' \stackrel{\simeq}{\to} Y$ and similarly factor $K' \to K \to L$ as $K' \hookrightarrow L' \stackrel{\simeq}{\to} L$

This yields a weak equivalence of  diagrams

$$
  \array{
    Y &\stackrel{\simeq}{\leftarrow}& Y'
    \\
    \uparrow && \uparrow^{\mathrlap{\in cof}}
    \\
    K &\stackrel{\simeq}{\leftarrow}& K'
    \\
    \downarrow^{\mathrlap{\in cof}}
     && \downarrow^{\mathrlap{\in cof}}
    \\
    L &\stackrel{\simeq}{\leftarrow}& L'    
  }
  \,,
$$

where now the diagram on the right is cofibrant as a diagram, so that its ordinary pushout

$$
  X' \coloneqq L' \coprod_{K'} Y'
$$

is a homotopy colimit of the original diagram. To obtain the weak equivalence from there to $X$, first form the further pushouts

$$
  \array{
    K &&&\to&&& Y
    \\
    & \nwarrow^{\mathrlap{\in W}} 
     &&&& \nearrow_{\mathrlap{\simeq}} & 
    \\
    && K' &\to& Y' &&  
    \\
    \downarrow^{\mathrlap{\in cof}} 
    && \downarrow^{\mathrlap{\in cof}} 
     && \downarrow^{\mathrlap{\in cof}} && \downarrow
    \\
    && L' &\to& X' && 
    \\
    & {}^{\mathllap{\in W}}
    \swarrow &&&& \searrow^{\mathrlap{\simeq}} & 
    \\
    L'' \coloneqq K \coprod_{K'} L 
    &&&\to&&& 
    L'' \coprod_{K} Y
    \\
    \downarrow^{\mathrlap{\in W}} &&&&&&  \downarrow
    \\
    L &&&\to&&& X
  }
  \,,
$$

where the total outer diagram is the original pushout diagram. Here the cofibrations are as indicated by the above factorization and by their stability under pushouts, and the weak equivalences are as indicated by the above factorization and by the left properness of the model category. The weak equivalence $L'' \stackrel{\simeq}{\to} L$ is by the [[category with weak equivalences|2-out-of-3 property]].

This establishes in particular a weak equivalence

$$
  X' \stackrel{\simeq}{\to} L'' \coprod_K Y
  \,.
$$

It remains to get a weak equivalence further to $X$.
For that, take the two outer squares from the above

$$
  \array{
    K &\to& Y
    \\
    \downarrow^{\mathrlap{\in cof}} && \downarrow
    \\
    L'' &\to& L'' \coprod_{K'} Y
    \\
    \downarrow^{\mathrlap{\in W}} && \downarrow
    \\
    L &\to& X
  }
  \,.
$$

Notice that the top square is a pushout by construction, and the total one by assumption.  Therefore by the [[pasting law]], also the lower square is a pushout.

Then factor $K \to Y$ as a cofibration followed by a weak equivalence $K \hookrightarrow Z \stackrel{\simeq}{\to} Y$
and push that factorization through the double diagram, to obtain

$$
  \array{
    K &\stackrel{\in cof}{\to}& Z &\stackrel{\in W}{\to}& Y
    \\
    \downarrow^{\mathrlap{\in \cof}} 
    && \downarrow^{\mathrlap{\in cof}} && \downarrow
    \\
    L'' &\stackrel{\in cof}{\to}& 
    L'' \coprod_{K} Z
    &\stackrel{\in W}{\to}&
    L'' \coprod_{K'} Y
    \\
    \downarrow^{\mathrlap{\in W}} && 
    \downarrow^{\mathrlap{\in W}}
    && \downarrow
    \\
    L & \to& L \coprod_K Z &\stackrel{\in W}{\to}& X
  }
  \,.
$$

Again by the behaviour of pushouts under pasting, every single square and composite rectangle in this diagram is a pushout. Using this, the cofibration and weak equivalence properties from before push through the diagram as indicated. This finally yields the desired weak equivalence

$$
  L'' \coprod_{K'} Y \stackrel{\simeq}{\to}
  X
$$

by [[category with weak equivalences|2-out-of-3]].

=--

If we had allowed ourselved to assume in addition that $K$ itself is already cofibrant, then the above statement has a much simpler proof, which we list just for fun, too.

+-- {: .proof}
###### Proof of prop. \ref{PullbackAlongFibrationsAreHomotopyPullbacks} assuming that the domain of the cofibration is cofibrant 


Let $A \hookrightarrow B$ be a cofibration with $A$ cofibrant and let $A \to C$ be any other morphism. Factor this morphism as
$A \hookrightarrow C' \stackrel{\simeq}{\to} C$ by a cofibration
followed by an acyclic fibration. This give a weak equivalence
of pushout diagrams

$$
  \array{
    C' &\stackrel{\simeq}{\to}& C
    \\
    \uparrow && \uparrow
    \\
    A &\stackrel{=}{\to}& A
    \\
    \downarrow && \downarrow
    \\
    B &\stackrel{=}{\to}& B
  }
  \,.
$$

In the diagram on the left all objects are cofibrant and one morphism is a cofibration,
hence this is a cofibrant diagram and its ordinary colimit is the homotopy colimit.
Using that [[pushout]] diagrams compose to pushout diagrams, that cofibrations are preserved under pushout and that in a left proper model category weak equivalences
are preserved under pushout along cofibrations, we find a weak equiovalence
$hocolim \stackrel{\simeq}{\to} B \coprod_A C$

$$
  \array{
    A &\stackrel{\in cof}{\to}& C' &\stackrel{\in W \cap fib}{\to}& C
    \\
    \downarrow^{\mathrlap{\in cof}} &&
    \downarrow^{\mathrlap{\in cof}} &&
    \downarrow^{\mathrlap{\in cof}}
    \\
    B &\to& hocolim &\stackrel{\in W}{\to}&
    B \coprod_A C
  }
  \,.
$$

The proof for the second statement is the precise formal dual.

=--

+-- {: .num_prop}
###### Proposition

A model category is [[right proper model category|right proper]] if and only if every fibration is a [[sharp map]].

=--

([Rezk 98](#Rezk98))





### Slice categories
 {#SliceCategories}

For any model category $M$, and any morphism $f \colon A\to B$, the 
[[base change]] of [[slice categories]] along $f$
$$ 
  \Sigma_f 
    \;\colon\; 
  M/A 
    \rightleftarrows 
  M/B 
   \;\colon\; 
  f^* $$
is a [[Quillen adjunction]] between [[slice model categories]] ([this Prop.](slice+model+structure#LeftBaseChangeQuillenAdjunction)).  

If this adjunction is a [[Quillen equivalence]], then $f$ must be a [[weak equivalence]].  In general, the converse can be proven only if $A$ and $B$ are fibrant.

\begin{proposition}\label{ViaSliceCategories}
The following are equivalent:

1. $M$ is right proper.

1. If $f$ is any weak equivalence in $M$, then $\Sigma_f \dashv f^*$ is a Quillen equivalence.

\end{proposition}

This is due to [Rezk 02, Prop. 2.5](#Rezk02).

\begin{remark}
The statement of Prop. \ref{ViaSliceCategories} may be read as saying $M$ is right proper iff all [[slice model categories]] have the "correct" Quillen equivalence type.

Since whether or not a Quillen adjunction is a Quillen equivalence depends only on the classes of weak equivalences, not the fibrations and cofibrations, it follows that being right proper is really a property of a [[homotopical category]].  In particular, if one model structure is right proper, then so is any other model structure on the same category with the same weak equivalences.
\end{remark}


### Local cartesian closure

Since most well-behaved model categories are equivalent to a model category in which all objects are fibrant --- namely, the model category of [[algebraically fibrant objects]] --- they are in particular equivalent to one which is right proper.  Thus, right properness by itself is not a property of an $(\infty,1)$-category, only of a particular presentation of it via a model category.

However, if a [[Cisinski model category]] is right proper, then the $(\infty,1)$-category which it presents must be [[locally cartesian closed (∞,1)-category|locally cartesian closed]].  Conversely, any locally cartesian closed (∞,1)-category has a presentation by a right proper Cisinski model category; see [[locally cartesian closed (∞,1)-category]] for the proof.


## Related pages

* [[semi-left-exact left Bousfield localization]]


## References ##

The concept originates in 

* {#BousfieldFriedlander78} [[Aldridge Bousfield]], [[Eric Friedlander]], def. 1.1.6 in _Homotopy theory of $\Gamma$-spaces, spectra, and bisimplicial sets_, Springer Lecture Notes in Math., Vol. 658, Springer, Berlin, 1978, pp. 80-130. ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/bousfield-friedlander.pdf))

The usefulness of right properness for constructions of [[homotopy category|homotopy categories]] is discussed in

* [[Rick Jardine]], _Cocycle categories_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0605/0605198v1.pdf))


The general theory can be found in 

* {#Hirschhorn} [[Philip Hirschhorn]], chapter 13 of _Model Categories and Their Localizations_, 2003 ([AMS](http://www.ams.org/bookstore?fn=20&arg1=whatsnew&item=SURV-99), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))
 

also in 

* {#Reedy} [[Chris Reedy]], _Homotopy theory of model categories_ ([pdf](http://www-math.mit.edu/~psh/reedy.pdf))

Proposition \ref{FibrationsBetweenFibrantObjectsSuffice} can be found in

* {#Bousfield01} [[Aldridge Bousfield]], *On the telescopic homotopy theory of spaces*, Trans. Amer. Math. Soc. 353 (2001), 2391-2426, [web with fulltext](https://www.ams.org/journals/tran/2001-353-06/S0002-9947-00-02649-0/)

See also:

* {#Rezk98} [[Charles Rezk]], _Fibrations and homotopy colimits of simplicial sheaves_ ([arXiv:9811038](http://arxiv.org/abs/math/9811038))
 
* {#Rezk02} [[Charles Rezk]], _Every homotopy theory of simplicial algebras admits a proper model_, Topology and its Applications, Volume 119, Issue 1, 2002, Pages 65-94, (<a href="https://doi.org/10.1016/S0166-8641(01)00057-8">doi:10.1016/S0166-8641(01)00057-8</a>, [arXiv:math/0003065](http://arxiv.org/abs/math/0003065))

* {#Nikolaus10} [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv:1003.1342](http://arxiv.org/abs/1003.1342))

Examples of nonproper model structures can be found in:

* [[Simon Henry]], _Counter-example to the existence of left Bousfield localization of combinatorial model category_ [MathOverflow](https://mathoverflow.net/questions/325383/counter-example-to-the-existence-of-left-bousfield-localization-of-combinatorial)

* [[Simon Henry]], _Examples of non-proper model structure_,
[MathOverflow](https://mathoverflow.net/questions/339084/examples-of-non-proper-model-structure)

[[!redirects proper model categories]]

[[!redirects right proper model category]]
[[!redirects right proper model categories]]

[[!redirects left proper model category]]
[[!redirects left proper model categories]]

[[!redirects left proper]]
[[!redirects right proper]]
[[!redirects left properness]]
[[!redirects right properness]]
