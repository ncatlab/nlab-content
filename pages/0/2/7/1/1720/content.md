
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
* automatic table of contents goes here
{:toc}

## Idea ##

In a [[model category]] fibrations enjoy [[pullback stability]] and cofibrations are stable under [[pushout]], but weak equivalences need not have either property. In a proper model category weak equivalences are also preserved under certain pullbacks and/or certain pushouts.



## Definition ##

A [[model category]] is called 

* **right proper** if weak equivalences are preserved by [[pullback]] along fibrations

* **left proper** if weak equivalence are preserved by [[pushout]] along cofibrations

* **proper** if it is both left and right proper.


So a model category is right proper if for every weak equivalence $f : A \to B$ in $W\subset Mor(C)$ and every fibration $h : C \to B$ the pullback $h^* f : A \times_B C \to C$ in

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

## Examples ##


### Left proper model categories

* every model category in which all objects are cofibrant is left proper;

  this includes notably

  * the standard [[model structure on simplicial sets]]

  * the [[model structure for quasi-categories]]

  * the [[model structure on simplicially enriched categories]]

  and many model structures derived from these, such as 

  * the injective global [[model structure on simplicial presheaves]]
    over any small (simplicial) category;

* the left [[Bousfield localization]] of every left proper [[combinatorial model category]] at a set of morphisms is again left proper.

  So in particular also the _local_ injective model structures on
  simplicial presheaves over a [[site]] are left proper.  

### Non-left proper model categories

A class of model structures which tends to be _not_ left proper are model structures on categories of not-necessarily commutative algebras. 

For instance 

* the standard model structure on [[simplicial object|simplicial]] _[[associative unital algebra]]s (weak equivalences and fibrations are those of the underlying simplicial sets) is  _not_  left proper (see [Rezk2000, example 2.11](http://arxiv.org/PS_cache/math/pdf/0003/0003065v1.pdf#page=5))

But it is [[Quillen equivalence|Quillen equivalent]] to a model structure that _is_ left proper. This is discussed [below](#ProperEquivModels).


### Right proper model categories ###

* every model category in which eaxch object is fibrant is right proper.

  This includes for instance the standard [[model structure on topological spaces]]. 


### Proper model categories ###

Model categories which are both left and right proper include

* [[Top]]: [[model structure on topological spaces]]

* [[sSet]]: [[model structure on simplicial sets]]

All [[model category|model categories]] that model aspects of [[∞-stack]]s and hence of [[cohomology]] are right proper: 

* [[model structure on simplicial presheaves]]

* [[model structure on presheaves of spectra]] 

  for presheaves over the point this restricts to:

  * [[model structure on spectra]]


### Proper Quillen equivalent model structures {#ProperEquivModels}

While some model categories fail to be proper, often there is a [[Quillen equivalence|Quillen equivalent]] one that does enjoy properness.

+-- {: .un_theorem}
###### Theorem

Every model category whose acyclic cofibrations are [[monomorphism]]s is Quillen equivalent to its [[model structure on algebraic fibrant objects]].
In this all objects are fibrant, so that it is right proper.

=--

+-- {: .proof}
###### Proof

This is theorem 2.18 in

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))

=--



+-- {: .un_theorem}
###### Theorem

Let $T$ be a simplicial (possibly multi-colored) [[theory]], and let $T Alg$ be the corresponding category of simplicial T-algebras. This carries a model category structure where the fibrations and weak equivalences are those of the underlying simplicial sets in the standard [[model structure on simplicial sets]]. 

Then there exists a morphism of siplicial theories $T \to S$ such that

1. the induced [[adjunction]] $S Alg \stackrel{\to}{\leftarrow} T Alg$ is a [[Quillen equivalence]];

1. $S Alg$ is a proper [[simplicial model category]]. 


=--

+-- {: .proof}
###### Proof

This is the content of 

* [[Charles Rezk]], _Every homotopy theory of simplicial algebras admits a proper model_ ([math/0003065](http://arxiv.org/abs/math/0003065))

=--




## Properties ##


### Homotopy (co)limits in proper model categories ###

+-- {: .un_lemma }
###### Lemma


In a left proper model category, ordinary [[pushout]]s along cofibrations are [[homotopy pushout]]s.

Dually, in a right proper model category, ordinary [[pullback]]s along fibrations are [[homotopy pullback]]s.


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
  X' := L' \coprod_{K'} Y'
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
    L'':= K \coprod_{K'} L 
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

Notice that the top square is a pushout by construction, and the total one by assumption.  Therefore by the general theorem about pastings of [[pushout]]s, also the lower square is a pushout.

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
###### Proof of the above assuming that the domain of the cofibration is cofibrant 


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





## References ##


The usefulness of right properness for constructions of [[homotopy category|homotopy categories]] is discussed in

* J. Jardine, _Cocycle categories_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0605/0605198v1.pdf))

[[!redirects proper model categories]]
[[!redirects right proper model category]]
[[!redirects left proper model category]]