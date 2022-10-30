
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+-- {: .hide}
[[!include model category theory - contents]]
=--
=--
=--




# Contents
* table of contents
{: toc}


## Idea 

A **homotopy pullback** is a special kind of [[homotopy limit]]: the appropriate notion of [[pullback]] in the context of [[homotopy theory]]. Homotopy pullbacks model the [[limit in quasi-categories|quasi-category pullbacks]] in the [[(infinity,1)-category]] that is [[presentable (infinity,1)-category|presented]] by a given [[homotopical category]].  Since pullbacks are also called fiber products, homotopy pullbacks are also called **homotopy fiber products**.

A __homotopy pushout__ is the [[duality|dual]] concept.

For more details see [[homotopy limit]].

In the context of [[homotopy type theory]] a homotopy pullback is the [[categorical semantics|interpretation]] of the space of solutions to an [[equation]].

## Definition 

### In category theory

As with all homotopy limits, there is both a _local_ and a _global_ notion of homotopy pullback.

The _global_ definition says that the homotopy pullback of a [[co-span|cospan]] $X \to Z \leftarrow Y$ in a [[category with weak equivalences]] $C$ is its image under the right [[derived functor]] of the [[base change]] functor $pb: C^{\to \leftarrow} \to C$.

The _local_ definition says that the homotopy pullback of $X \to Z \leftarrow Y$ in a category with a notion of [[homotopy]] consists of a square
$$
  \array{
   P & \to& Y
   \\
    \downarrow && \downarrow
   \\
   X &\to& Z
  }
$$
that [[commutative square|commutes]] up to [[homotopy]], and such that for any other square
$$
  \array{
   T & \to& Y
   \\
    \downarrow && \downarrow
   \\
   X &\to& Z
  }
$$
that commutes up to homotopy, there exists a morphism $T\to P$, unique up to homotopy, making the two triangles commute up to homotopy, and similarly for homotopies and higher homotopies.  In other words, there is an equivalence
$$Map(T,P) \simeq HoSq(T,X\to Z\leftarrow Y)$$
between the space of maps $T\to P$ and the space of homotopy commutative squares with vertex $T$.

In good situations, such as when $X,Y,Z$ are [[fibrant object|fibrant]] in a [[model category]], the two constructions agree up to weak equivalence.

Note that in both cases, there is a canonical map from the actual pullback $X\times_Z Y$ to the homotopy pullback $X\times_Z^h Y$.  In the global case this comes by the definition of a derived functor; in the local case it comes because a commutative square is, in particular, a homotopy commutative one.

### In homotopy type theory
 {#InHomotopyTypeTheory}

In [[homotopy type theory]] the homotopy pullback of a [[term]] of [[function type]] 

$$
  f : A \to C
$$

along a term of function type

$$
  g : B \to C
$$

is given formally by precisely the same formula that would also define the ordinary [[fiber product]] of functions of sets, namely by 

$$
  \left\{
     a : A, b : B \;\; | \;\; f(a) = g(b)
  \right\}
  \,.
$$

Spelled out, this is the [[dependent sum]] 

$$
  \underset{
    \array{
      {a \colon A}  
      \\
      {b\colon B}
    }
   }{\sum} (f(a)= g(b))
$$


over the [[dependent type|dependent]] [[identity type]] over the [[evaluation]] of $f$ and $g$.


What in classical logic is interpreted as the set of pairs $(a,b)$ such that $f(a)$ and $g(b)$ are equal here becomes the restriction of a [[mapping cocylinder]].


Formal proof that this is the homotopy pullback in homotopy type theory is in ([Brunerie](#Brunerie)). Proof in the [[categorical semantics of homotopy type theory]] is [below](#ConstructionInHomotopyTypeTheory).


## Concrete constructions
  {#ConcreteConstructions}

We discuss various concrete constructions by ordinary [[pullbacks]] and ordinary [[limits]] such that under some sufficient conditions these compute homotopy pullbacks, up to weak equivalence.

### General
 {#ConstructionsGeneral}

+-- {: .num_prop #HomotopyPullbackByOrdinaryPullback}
###### Proposition

Let $A \to C \leftarrow B$ be a [[diagram]] in some [[model category]]. Then sufficient conditions for the ordinary (1-categorical) [[pullback]] $A \times_C B$ to present the homotopy pullback of the diagram are

* one of the two morphisms is a [[fibration]] and all three objects are [[fibrant objects]];

* one of the two morphisms is a [[fibration]] and the model category is [[right proper model category|right proper]].

=--

Both statements are classical. They are reviewed for instance as [Lurie, prop. A.2.4.4](#Lurie). The proof of the second statement is spelled out [here](proper+model+category#HomotopyLimits).

+-- {: .num_remark }
###### Remark

Notice that a fibrant [[resolution]] of the diagram in the injective [[model structure on functors]] has _both_ morphisms be a fibration. So the first point in prop. \ref{HomotopyPullbackByOrdinaryPullback} says that (in the special case of pullbacks) something weaker than this is sufficient for computing the [[homotopy limit]] of the diagram.

This can be explained in model-categorical terms by the fact that the category of [[cospans]] also has a [[Reedy model structure]] in which the fibrant objects are precisely those considered in the first point above, and that homotopy limits can equally well be computed using this model structure (specifically, the [[adjunction]] $Const \dashv Lim$ is [[Quillen adjunction|Quillen]] with respect to it).

In this spirit one may ask for the largest class of morphisms such that their ordinary pullbacks are already homotopy pullbacks. This is related to the concept of _[[sharp morphisms]]_.

=--



Due to prop. \ref{HomotopyPullbackByOrdinaryPullback} one typically computes homotopy pullbacks of a diagram by first forming a [[resolution]] of one of the two morphisms by a fibration and then forming an ordinary pullback. 

+-- {: .num_cor #HomotopyPullbackByFactorizationLemma}
###### Corollary

If in $A \stackrel{f}{\to} C \stackrel{g}{\leftarrow} B$ 
all three objects are [[fibrant objects]], then
the homotopy pullback of this diagram is presented by the ordinary [[pullback]]

$$
  \array{
     A\times_C^h B & \to & C^I \times_C B
    \\
    \downarrow && \downarrow 
    \\
     A & \stackrel{f}{\to} & C
  }
  \,.
$$

or, equivalently up to [[isomorphism]], as the ordinary [[pullback]]

$$
  \array{
     A\times_C^h B & \to & C^I
    \\
    \downarrow && \downarrow 
    \\
     A\times B & \stackrel{(f,g)}{\to} & C\times C
  }
  \,.
$$

=--

See also at _[[Mayer-Vietoris sequence]]_ [this proposition](Mayer-Vietoris+sequence#SequenceFromDiagonal).

+-- {: .proof}
###### Proof
Since the objects are already fibrant, prop. \ref{HomotopyPullbackByOrdinaryPullback} implies that it is sufficient to replace one of the morphisms by a fibrant resolution.
Such a resolution is provided by the [[factorization lemma]]: by [Lemma 3](factorization+lemma#FibrantResolution), $B \to C$ admits a canonical fibrant resolution
  $$ C^I \times_C B \twoheadrightarrow C $$
where $C \stackrel{\simeq}{\to} C^I \to C \times C$ is a [[path space object]] for $C$ (for instance, when $C$ is a [[closed monoidal homotopical category]] then this can be taken to be the [[internal hom]] with an [[interval object]] $I$).
=--

The homotopy pullback constructed in this way is an example of a _strict homotopy limit_, as mentioned at [[homotopy limit]].  In such a case, one can say that an arbitrary homotopy-commutative square

$$
  \array{
   W & \to& Y
   \\
    \downarrow && \downarrow
   \\
   X &\to& Z
  }
$$

is a homotopy pullback square if the induced morphism from $W$ to the strict homotopy pullback is a [[weak equivalence]].


A useful class of examples of this is implied by the following:

+-- {: .num_prop }
###### Proposition

Let $\mathcal{C}$ be a category of [[simplicial presheaves]] over some [[site]]
equipped with a _local_ injective [[model structure on simplicial presheaves]] with respect to that site.

Then an ordinary pullback of $A \to C \leftarrow B$ in $\mathcal{C}$ is a homotopy pullback already when one of the two morphisms is an objectwise [[Kan fibration]].

=--

+-- {: .proof}
###### Proof

The _global_ projective [[model structure on simplicial presheaves]] is [[right proper model category|right proper]]. So by prop. \ref{HomotopyPullbackByOrdinaryPullback} the ordinary pullback in question presents the homotopy pullback in the global structure. By the discussion at [[homotopy limit]] and [[Bousfield localization of model categories]], this presents the [[(∞,1)-pullback]] of the diagram of [[(∞,1)-presheaves]], and the fibrant replacement of that pullback in the _local_ model structure presents the [[(∞,1)-sheafification]] of this [[(∞,1)-presheaf]]. This is (essentially by definition, see [[(∞,1)-topos]]) a [[left exact functor|left exact]] [[(∞,1)-functor]] and hence preserves finite [[(∞,1)-limits]]. 

=--



### In homotopy type theory
 {#ConstructionInHomotopyTypeTheory}


If we unwind the [[categorical semantics]] of the [above definition](#InHomotopyTypeTheory) 

$$
  A \times_C^h B \simeq \{ a : A, b : B | (f(a) = g(b)) \}
$$

of the homotopy pullback in [[homotopy type theory]], we re-obtain the 
[above prescription](#ConstructionsGeneral) for how to construct homotopy pullbacks.

So let the ambient category be a suitable [[type-theoretic model category]].

+-- {: .num_example}
###### Example

The type $ a : A, b : B \vdash (f(a) = g(b))$ is obtained by [[substitution]] from the [[identity type]] of $C$. By the discussion there, the [[categorical semantics]] of substitution is given by [[pullback]] of the fibrations that interpret the [[dependent types]], and so this is interpreted as the pullback $[a : A, b : B \vdash (f(a) = g(b))] \coloneqq (f,g)^* C^I$ of the [[path space object]] of $C$:

$$
  \array{
    [a : A, b : B \vdash (f(a) = g(b))]
    &\to&
    [Id C]
    \\
    \downarrow && \downarrow
    \\
    [a : A , b : B]
    &\stackrel{(f,g)}{\to}&
    [c_1 : C , c_2 : C]
  }
  \;\;
   = 
  \;\;
  \array{
    (f,g)^* C^I &\to& C^I
    \\
    \downarrow && \downarrow
    \\
    A \times B
    &
    \stackrel{(f,g)}{\to}
    &
    C \times C
  }
  \,.
$$

Forming the [[dependent sum]] over $a : A, b : B$ is simply interpreted as regarding the resulting object $(f,g)^* C^I$ as an object in $\mathcal{C} \simeq \mathcal{C}_{/*}$ instead of as an object in the [[slice category]] $\mathcal{C}_{/ A \times B}$.

Since by assumption on the categorical interpretation of a type, all objects here are fibrant, this coincides with the expression of the homotopy pullback from corollary \ref{HomotopyPullbackByFactorizationLemma} above.

=--


+-- {: .num_example}
###### Example

Specifically, let $f \colon A \longrightarrow B$ be a [[function]], then the [[categorical semantics]] for the expression

$$
  \underset{b \colon B}{\sum} fib(f,b)
  =
  \underset{b \colon B}{\sum} \underset{a \colon A}{\sum} (f(a) = b)
$$

is the canonical [[fibration]] replacement of $f$ as it appears notably in the [[factorization lemma]]

$$
  \array{
    A \times_B B^I &\longrightarrow& B^I
    \\
    \downarrow && \downarrow
    \\
    A \times B
    &\stackrel{(f, Id)}{\longrightarrow}&
    B \times B
  }
  \,.
$$

=--


## Properties

### Fiber-wise characterization
 {#HomotopyFiberCharacterization}


+-- {: .num_prop #FiberwiseCharacterizationInInfinityGrpds}
###### Proposition

In plain [[homotopy types]] (i.e. in [[∞-groupoids]], in the [[classical model structure on simplicial sets]] etc.) the following holds:

a [[diagram]] 

$$
  \array{
    A &\stackrel{f}{\longrightarrow}& B
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    C &\stackrel{g}{\longrightarrow}& D
  }
$$

is a homotopy pullback diagram precisely if it induces a [[weak equivalence]] on all [[homotopy fibers]]

$$
  \array{
    hfib_b(f) &\longrightarrow& A &\stackrel{f}{\longrightarrow}& B
    \\
    \downarrow^{\mathrlap{\simeq}}  && \downarrow && \downarrow^{\mathrlap{p}}
    \\
    hfib_{p(b)}(g) &\longrightarrow& C &\stackrel{g}{\longrightarrow}& D
  }
$$

for all elements $b \in B$.

=--

 (e.g. [CPS 05, 5.2](#CPS05), [MO](http://mathoverflow.net/a/192303/381))

+-- {: .num_remark }
###### Remark

For the analog of prop. \ref{FiberwiseCharacterizationInInfinityGrpds} to hold in [[(∞,1)-categories]] more general than [[∞-groupoids]] one would need either "enough [[global elements]]" of the object $B$ to detect all homotopy fibers, or else one would need a suitable "[[internal logic|internal]]" formulation of the statement. 

=--

On the other hand in [[stable homotopy theory]] the statement holds generally:

+-- {: .num_prop #FiberwiseRecognitionInStableCase}
###### Proposition

For $\mathcal{C}$ a [[stable model category]], then for a diagram

$$
  \array{
    A &\stackrel{f}{\longrightarrow}& B
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    C &\stackrel{g}{\longrightarrow}& D
  }
$$

the following are equivalent

1. the square is a homotopy pullback square;

1. the square is a [[homotopy pushout]] squre;

1. the induced morphism on the homotopy fiber over the [[zero object]] 0 is a weak equivalence

   $$
      hfib_0(f) \stackrel{\simeq}{\longrightarrow} hfib_0(g)
      \,.
   $$

=--

A proof in terms of [[stable model categories]] including the third item is spelled out for instance in ([Hovey 07, remark 7.1.12](#Hovey07)). (Beware: this is not in the original volume from 1999, but is in the version "reprinted with corrections" from 2007.) A proof in terms of [[stable (∞,1)-categories]] of the first two items is in ([[Higher Algebra|Lurie HA, prop. 1.1.3.4 (2)]]).


### Pasting law

* [[pasting law]]

## Examples

### Fiber sequences 

Of particular interest are consecutive homotopy pullbacks of point inclusions. These give rise to [[fiber sequence]]s and [[loop space object]]s.

## Related concepts

* [[equation]]

* [[homotopy limit]], [[(∞,1)-limit]]


[[!include notions of pullback -- contents]]


## References

### General

See the references at _[[homotopy limit]]_ .

Fairly comprehensive resources are

* {#Hovey07} [[Mark Hovey]], _Model categories_, Mathematical Surveys and Monographs, vol 63, 1999,reprinted 2007

* {#Lurie} [[Jacob Lurie]], appendix of _[[Higher Topos Theory]]_
  
See also

* {#CPS05} [[Wojciech Chacholski]], Wolfgang Pitsch, and [[Jerome Scherer]], _Homotopy pullback squares up to localization_, in [[Dominique Arlettaz]], [[Kathryn Hess]] (eds.) _An Alpine Anthology of Homotopy Theory_ ([arXiv:math/0501250](http://arxiv.org/abs/math/0501250), [pdf](http://sma.epfl.ch/~jscherer/articles/hopullbacks2.pdf), [doi:10.1090/conm/399](http://dx.doi.org/10.1090/conm/399))

 

### In terms of homotopy type theory
 {#ReferencesForHoTT}

A proposal for a formalization of homotopy pushouts by [[higher inductive types]] in [[homotopy type theory]] has been given in

* [[Mike Shulman]], _Homotopy Type Theory VI_ ([blog post](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_vi.html))

A [[homotopy type theory|HoTT]]-[[Coq]]-coding of homotopy pullbacks and pushouts is in 

* [[Guillaume Brunerie]], _[HoTT/Coq/Limits/Pullbacks.v](https://github.com/guillaumebrunerie/HoTT/blob/master/Coq/Limits/Pullbacks.v)_
 {#Brunerie}

[[!redirects homotopy pullback]]
[[!redirects homotopy pullbacks]]

[[!redirects homotopy pushout]]
[[!redirects homotopy pushouts]]

[[!redirects homotopy fiber product]]
[[!redirects homotopy fiber products]]

[[!redirects homotopy cofiber product]]
[[!redirects homotopy cofiber products]]


[[!redirects homotopy co-fiber product]]
[[!redirects homotopy co-fiber products]]


