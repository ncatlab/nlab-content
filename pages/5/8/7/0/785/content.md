
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
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

The notion of __[[homotopy pushout]]__ is the [[duality|dual]] concept.

For more details see *[[homotopy limit]]*.

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
   }{\sum} 
   \big(
     f(a) = g(b)
   \big)
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

Notice that a  [[fibrant resolution]] of the [[cospan]] [[diagram]] in the injective [[model structure on functors]] has _both_ morphisms be a fibration. So the first point in Prop. \ref{HomotopyPullbackByOrdinaryPullback} says that (in the special case of pullbacks) something weaker than fibrancy  is sufficient for [[derived functor|deriving]] the [[limit]] functor on cospan diagrams.

This can be explained in model-categorical terms by the fact that the category of [[cospans]] also has a [[Reedy model structure]] in which the fibrant objects are precisely those considered in the first point in Prop. \ref{HomotopyPullbackByOrdinaryPullback}, and that homotopy limits can equally well be computed using this model structure (specifically, the [[adjunction]] $Const \dashv Lim$ is [[Quillen adjunction|Quillen]] with respect to it).

In this spirit one may ask for the largest class of morphisms such that their ordinary pullbacks are already homotopy pullbacks. This is related to the concept of _[[sharp morphisms]]_.

=--

+-- {: .num_remark #NeedForThreeFibrantObjects}
###### Remark

In the first point of Prop. \ref{HomotopyPullbackByOrdinaryPullback} it is indeed necessary that all three objects are fibrant. As a ([[counterexample|counter-]])[[example]] consider the 
pullback of $\Lambda_1^2 \to \Delta^2$ along $d_1 \colon \Delta^1 \to \Delta^2$ in [[SimplicialSets]]: This is not a homotopy pullback with respect to the [[Joyal model structure]], even though the latter morphism is a fibration between fibrant objects. 

=--


Due to prop. \ref{HomotopyPullbackByOrdinaryPullback} one typically computes homotopy pullbacks of a diagram by first forming a [[resolution]] of one of the two morphisms by a fibration and then forming an ordinary pullback. 

+-- {: .num_cor #HomotopyPullbackByFactorizationLemma}
###### Corollary

If in $A \stackrel{f}{\to} C \stackrel{g}{\leftarrow} B$ 
all three objects are [[fibrant objects]], then
the homotopy pullback of this diagram is presented by the ordinary [[pullback]]

$$
  \array{
     A\times_C^h B & \longrightarrow & C^I \times_C B
    \\
    \big\downarrow && \big\downarrow 
    \\
     A & \underset{f}{\longrightarrow} & C
  }
  \,.
$$

or, equivalently up to [[isomorphism]], as the ordinary [[pullback]]

\[
  \label{HomotopyPullbackAsFiberProductWithPaths}
  \array{
    A\times_C^h B 
      & \longrightarrow & 
    C^I
    \\
    \big\downarrow && \big\downarrow 
    \\
    A\times B 
    & 
    \underset{(f,g)}{\longrightarrow} 
    & 
    C\times C
  }
  \,.
\]

=--

See also at _[[Mayer-Vietoris sequence]]_ ([this proposition](Mayer-Vietoris+sequence#SequenceFromDiagonal)) and at *[[homotopy equalizer]]* ([this section](homotopy+equalizer#RelationToHomotopyPullbacks)).

\begin{proof}
Since the objects are already fibrant, prop. \ref{HomotopyPullbackByOrdinaryPullback} implies that it is sufficient to replace one of the morphisms by a fibrant resolution.
Such a resolution is provided by the [[factorization lemma]]: by [Lemma 3](factorization+lemma#FibrantResolution), $B \to C$ admits a canonical fibrant resolution
  $$ C^I \times_C B \twoheadrightarrow C $$
where $C \stackrel{\simeq}{\to} C^I \to C \times C$ is a [[path space object]] for $C$ (for instance, when $C$ is a [[closed monoidal homotopical category]] then this can be taken to be the [[internal hom]] with an [[interval object]] $I$).
\end{proof}

+-- {: .num_remark #HomotopyFiberSequenceOfHomotopyPullback}
###### Remark

Incidentally, when $A,B,C$ are [[pointed topological spaces]] and $A \longrightarrow C$ and $B \longrightarrow C$ are pointed maps, then
(eq:HomotopyPullbackAsFiberProductWithPaths) implies that the homotopy fiber product $A \times_C^h B$ sits in a [[homotopy fiber sequence]] of the form
$$
  \Omega C 
  \longrightarrow
  A \times^h_C B
  \longrightarrow
  A \times B
  \,.
$$

This is because the following outer rectangle is a (homotopy) pullback exhibiting the [[based loop space]] of $C$:

$$
  \array{
    \Omega C
    &\longrightarrow&
    A\times_C^h B 
      & \longrightarrow & 
    C^I
    \\
    \big\downarrow 
    &&
    \big\downarrow 
    && 
    \big\downarrow 
    \\
    \ast
    &\longrightarrow&
    A\times B 
    & 
    \underset{(f,g)}{\longrightarrow} 
    & 
    C\times C
    \mathrlap{\,,}
  }
$$

which implies the claim by the [[pasting law]] for (homotopy) pullbacks.

=--

\begin{remark}
The homotopy pullback constructed in the way of Corollary \ref{HomotopyPullbackByFactorizationLemma} is an example of a _strict homotopy limit_, as mentioned at *[[homotopy limit]].*  In such a case, one can say that an arbitrary homotopy-commutative square

$$
  \array{
   W &\longrightarrow& Y
   \\
   \big\downarrow && \big\downarrow
   \\
   X &\longrightarrow& Z
  }
$$

is a homotopy pullback square if the induced morphism from $W$ to the strict homotopy pullback is a [[weak equivalence]].
\end{remark}


A useful class of examples of this is implied by the following:

+-- {: .num_prop }
###### Proposition

Let $\mathcal{C}$ be a category of [[simplicial presheaves]] over some [[site]] equipped with a _local_ injective [[model structure on simplicial presheaves]] with respect to that site.

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
  A \times_C^h B 
  \;\simeq\; 
  \Big\{ 
    a \colon A
    ,\, 
    b \colon B 
    \;\big\vert\; 
    \big(
      f(a) = g(b)
    \big)
  \Big\}
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

1. the square is a [[homotopy pushout]] square;

1. the induced morphism on the homotopy fiber over the [[zero object]] 0 is a weak equivalence

   $$
      hfib_0(f) \stackrel{\simeq}{\longrightarrow} hfib_0(g)
      \,.
   $$

=--

A proof in terms of [[stable model categories]] including the third item is spelled out for instance in ([Hovey 07, remark 7.1.12](#Hovey07)). (Beware: this is not in the original volume from 1999, but is in the version "reprinted with corrections" from 2007.) A proof in terms of [[stable (∞,1)-categories]] is in ([[Higher Algebra|Lurie HA, prop. 1.1.3.4 (2) & lemma 1.2.4.14]]).


### Pasting law

* [[pasting law]]

## Examples

### Fiber sequences 

Of particular interest are consecutive homotopy pullbacks of point inclusions. These give rise to [[fiber sequence]]s and [[loop space object]]s.

## Related concepts

* [[equation]]

* [[homotopy limit]], [[(∞,1)-limit]]

* [[homotopy pushout type]]


[[!include notions of pullback -- contents]]



## References

### General

See also the references at _[[homotopy limit]]_ .

Homotopy pullbacks are at least mentioned in almost any textbook on [[homotopy theory]].

Dedicated textbook introductions:

* [[Jeffrey Strom]], *Homotopy Pullback Squares*, §7.3 in: *Modern classical homotopy theory*, Graduate Studies in Mathematics **127**, American Mathematical Society (2011) &lbrack;[doi:10.1090/gsm/127](http://www.ams.org/books/gsm/127/)&rbrack;

* [[Martin Arkowitz]], *Homotopy Pushouts and Pullbacks*, §6 in: *Introduction to Homotopy Theory*, Springer (2011) &lbrack;[doi:10.1007/978-1-4419-7329-0](https://doi.org/10.1007/978-1-4419-7329-0)&rbrack;

* [[Peter May]], [[Kate Ponto]], *Some basic homotopy limits*: §2.2 in: _[[More concise algebraic topology]]_,   University of Chicago Press (2012) &lbrack;[ISBN:9780226511795](https://press.uchicago.edu/ucp/books/book/chicago/M/bo12322308.html), [pdf](https://www.math.uchicago.edu/~may/TEAK/KateBookFinal.pdf)&rbrack;

Lecture notes:

* [[Cary Malkiewich]]: *Fibration Sequences and Pullback Squares* (2021) &lbrack;[pdf](https://people.math.binghamton.edu/malkiewich//fibration_sequences.pdf), [[Malkiewich-FibrationSequences.pdf:file]]&rbrack;


Exposition in [[model category]]-theory:

* [[Urs Schreiber]], *[Homotopy Pullbacks](Introduction+to+Homotopy+Theory#HomotopyPullbacks)*, section in: *[[Introduction to Homotopy Theory]]*



Fairly comprehensive general resources:

* {#Hovey07} [[Mark Hovey]], _Model categories_, Mathematical Surveys and Monographs, vol 63, 1999,reprinted 2007

* {#Lurie} [[Jacob Lurie]], appendix of _[[Higher Topos Theory]]_
  
See also:

* {#CPS05} [[Wojciech Chacholski]], Wolfgang Pitsch, and [[Jerome Scherer]], _Homotopy pullback squares up to localization_, in [[Dominique Arlettaz]], [[Kathryn Hess]] (eds.) _An Alpine Anthology of Homotopy Theory_ ([arXiv:math/0501250](http://arxiv.org/abs/math/0501250), [pdf](http://sma.epfl.ch/~jscherer/articles/hopullbacks2.pdf), [doi:10.1090/conm/399](http://dx.doi.org/10.1090/conm/399))

* [[Alisa Govzmann]], [[Damjan Pištalo]], [[Norbert Poncin]], *Indeterminacies and models of homotopy limits* &lbrack;[arXiv:2109.12395](https://arxiv.org/abs/2109.12395)&rbrack;

 

### In terms of homotopy type theory
 {#ReferencesForHoTT}

Discussion of homotopy pullbacks in [[homotopy type theory]]:

* [[Univalent Foundations Project]], Exc. 2.11 in: *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Egbert Rijke]], *Homotopy pullbacks* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/pullback.pdf)&rbrack;, Lecture 10 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;



[[!redirects homotopy pullback]]
[[!redirects homotopy pullbacks]]


[[!redirects homotopy fiber product]]
[[!redirects homotopy fiber products]]

[[!redirects homotopy cofiber product]]
[[!redirects homotopy cofiber products]]


[[!redirects homotopy base change]]
[[!redirects homotopy base changes]]
