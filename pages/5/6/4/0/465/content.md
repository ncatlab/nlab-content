
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _regular epimorphism_ is a [[morphism]] $c\to d$ in a [[category]] which behaves in the way that a [[covering]] is expected to behave, in the sense that "$d$ is the union of the parts of $c$, identified with each other in some specified way".

In a category with [[pullbacks]], regular epimorphisms are the same as [[effective epimorphisms]] and [[strict epimorphisms]].  Every regular epimorphism is an [[epimorphism]], and every [[split epimorphism]] is regular, but the converses frequently fail.

## Definition 

\begin{definition}
\label{RegularEpimorphism}
A **regular epimorphism** is a [[morphism]] $f \colon c \to d$ (in a given [[category]]) that is the [[coequalizer]] of _some_ [[parallel pair]] of morphisms, i.e. if there exists _some_ [[colimit]] diagram of the form
$$ 
  a 
    \;\rightrightarrows\; 
  c 
    \xrightarrow{\;f\;} 
  d. 
$$
\end{definition}

\begin{remark}
The [[formal duality|dual]] concept to Def. \ref{RegularEpimorphism} is that of *[[regular monomorphism]]*.
\end{remark}

## Properties

### Epimorphy

Although Def. \ref{RegularEpimorphism} does not state it explicitly, it is true (and easy to prove) that:

\begin{proposition}
Every regular epimorphism (Def. \ref{RegularEpimorphism}) is an [[epimorphism]].  
\end{proposition}
In fact, every regular epimorphism is a [[strong epimorphism]], hence an [[extremal epimorphism]].  In particular, this implies that a regular epimorphism which is also a [[monomorphism]] must in fact be an [[isomorphism]].

Frequently (such as in a [[regular category]]), every strong or extremal epimorphism is regular.  Moreover, in a regular category, every regular epimorphism is [[pullback-stability|pullback-stable]], and therefore a [[descent morphism]].  If the category is moreover [[exact category|exact]], or has stable [[reflexive coequalizers]], then every regular epimorphism is an [[effective descent morphism]].

On the other hand, every [[split epimorphism]] is regular, but the converse holds only rarely (it is an [[internalization|internal]] form of the [[axiom of choice]]).


### Effective epimorphisms

Def. \ref{RegularEpimorphism} refers only to *some* parallel pair, but often there is a canonical choice: the [[kernel pair]] of the morphism in question:

\begin{prop}
\label{MorphismsWithKernelPairsAreRegularIffEffective}
A morphism having a [[kernel pair]] (such as any morphism in a category with [[pullbacks]]) is a regular epimorphism (Def. \ref{RegularEpimorphism}) if and only if it is the [[coequalizer]] of its kernel pair.  
\end{prop}
E.g. [Borceux 1994, Prop. 2.5.7](#Borceux94), [Taylor 1999, Lemma 5.6.6](#Taylor99).
This also follows from the theory of [[generalized kernels]].  

\begin{definition}
\label{EffectiveEpimorphism}
A regular epimorphism 
that satisfies the following two conditions (which are equivalent, by Prop. \ref{MorphismsWithKernelPairsAreRegularIffEffective}) 

1. it has a [[kernel pair]], 

1. it is the [[coequalizer]] of its kernel pair

is called an _[[effective epimorphism]]_.
\end{definition}


### Pullbacks and pushouts


\begin{proposition}
\label{InRegularCategoryRegularEpisAreStableUnderPullback}
In a [[regular category]], [[regular epimorphisms]] are [[preserved limit|preserved]] by [[pullback]].
\end{proposition}
This is by definition of "[[regular category]]".

\begin{proposition}
\label{InRegularCategoryEffectiveEpisAreStableUnderPullback}
**(in regular category pullback preserves effective epimorphisms)**
\linebreak
  In a [[regular category]], [[effective epimorphisms]] (Def. \ref{EffectiveEpimorphism}) are preserved by [[pullback]]:

Given a [[commuting diagram]] of the form

\begin{tikzcd}
  R'
  \ar[d, shift left=4pt]
  \ar[d, shift right=4pt]
  \ar[r]
  \ar[dr, phantom, "\mbox{\tiny(pb)}"]
  &
  R
  \ar[d, shift left=4pt]
  \ar[d, shift right=4pt]
  \\
  X'
  \ar[d, ->>]
  \ar[r]
  \ar[dr, phantom, "\mbox{\tiny(pb)}"]
  &
  X
  \ar[d, ->>]
  \\
  Y'
  \ar[r]
  &
  Y
\end{tikzcd}

where 

* the right vertical column is both a [[kernel pair]] and a [[coequalizer]], hence the kernel pair of a regular epimorphism,

* all parallel squares are [[pullbacks]]

then also the left vertical column is both a kernel pair and a coequalizer, hence the kernel pair of a regular epimorphism.
\end{proposition}
\begin{proof}
  The left column is again a kernel pair since [[limits commute with limits]] and the left bottom vertical morphism is again a regular epimorphism, by Prop. \ref{InRegularCategoryRegularEpisAreStableUnderPullback}.

Therefore the left vertical column is also a coequalizer by Prop. \ref{MorphismsWithKernelPairsAreRegularIffEffective} and hence an effective epimorphism by Def. \ref{EffectiveEpimorphism}.
\end{proof}



+-- {: .num_prop #PullbackSquareOfRegularEpisIsPushout}
###### Proposition

In a [[regular category]], if in a [[pullback]] [[diagram]] 

$$
  \array{
     & \swarrow & \searrow
     \\
     & \searrow & \swarrow
  }
$$

the two bottom morphisms are regular epis (hence by prop. \ref{InRegularCategoryRegularEpisAreStableUnderPullback} all four morphisms are), then the diagram is also a [[pushout]].

=--

(e.g. [Johnstone, section A, prop. 1.4.3](#Johnstone))

+-- {: .num_prop} 
###### Proposition 
In a regular category $C$, regular epimorphisms and [[strong epimorphisms]] (= [[extremal epimorphisms]] since $C$ admits pullbacks) coincide; hence regular epimorphisms are closed under composition. 
=-- 

(See [Johnstone, A.1.3.4](#Johnstone).) 

+-- {: .num_remark} 
###### Remark 
Regular epimorphisms are not generally closed under composition. [Taylor 1999 p. 289](#Taylor99) gives the following example in [[Cat]]. Let $\mathbb{2}$ be the [[interval category]]; then the coequalizer of the two object inclusions $1 \rightrightarrows \mathbb{2}$ is a regular epi $\mathbb{2} \to B\mathbb{N}$ (the codomain is the additive monoid $\mathbb{N}$ made into a 1-object category; the epi sends the non-identity arrow of $\mathbb{2}$ to $1 \in \mathbb{N}$). There is an evident regular epi $e: \mathbb{N} \to \mathbb{Z}/3$ of monoids. But the composite 

$$\mathbb{2} \to B\mathbb{N} \stackrel{B e}{\to} B\mathbb{Z}/3$$ 

is not a regular epi in $Cat$. A very similar example is found at [Bednarczyk et al.](#Bed), Example 4.4. 
=--

## Examples

* In [[Set|the category of sets]], every epimorphism is regular. Thus, it can be hard to know, when generalising concepts from $\Set$ to other categories, what kind of epimorphism to use.  Frequently, regular epimorphisms are a good choice.  In particular, one may define a [[projective object]] (and hence the [[axiom of choice]]) using regular epimorphisms.

* More generally, in every [[Grothendieck topos]] every epimorphism is regular (and in fact [[effective epimorphism|effective]], see there).

* In [[Grp|the category of groups]], every epimorphism is regular. A number of proofs can be found in the literature; one proof that avoids case analysis is given [here](http://ncatlab.org/toddtrimble/published/epimorphisms+in+the+category+of+groups). 

* In the category of [[monoid]]s, the inclusion $\mathbb{N}\hookrightarrow\mathbb{Z}$ is an epimorphism, even though it is far from a [[surjection]].  But in this or any other [[algebraic category]] (a category of models of an [[algebraic theory]]), the morphisms whose underlying function is surjective are precisely the regular epimorphisms.  Thus $\mathbb{N}\hookrightarrow\mathbb{Z}$ is not a regular epimorphism. 

* Similarly, in the category of rings, not every epimorphism is regular, as shown by the example $\mathbb{Z} \hookrightarrow \mathbb{Q}$. 

* In [[Diff]], the category of smooth (paracompact) manifolds, regular epimorphisms are not as useful as in other settings. As any [[split epimorphism]] is regular, and split epimorphisms are badly behaved in $\Diff$ (for example, pullbacks of split epis do not necessarily exist), the usual procedure is to consider the smallest class of arrows inside regular epis of which all pullbacks exist, namely the surjective [[submersions]]. In the setting of [[differentiable stacks]] and [[Lie groupoids]] it is surjective submersions that play the role of regular epimorphisms.

## Related pages

* The page [[epimorphism]] has a list of many types of epimorphism and their relationships.

* The dual concept is [[regular monomorphism]].  In particular, in the presence of pullbacks, [[effective epimorphisms]] and [[strict epimorphisms]] are the same as regular ones.

* In higher category theory:

  * [[regular epimorphism in an (∞,1)-category]]

## References

Textbook accounts:

* [[Jiri Adamek|Ji&#345;í Adámek]], [[Horst Herrlich]], [[George Strecker]], Def. 7.71 in: *[[Abstract and Concrete Categories -- The Joy of Cats]]* John Wiley and Sons, New York (1990) reprinted as: Reprints in Theory and Applications of Categories **17** (2006) 1-507 ([tac:tr17](http://www.tac.mta.ca/tac/reprints/articles/17/tr17abs.html), [book webpage](http://katmat.math.uni-bremen.de/acc/), [pdf](http://katmat.math.uni-bremen.de/acc/acc.pdf))

* {#Borceux94} [[Francis Borceux]], Def. 4.3.1 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) ([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))

Exposition and examples:

* [[Qiaochu Yuan]], *[Regular and effective monomorphisms and epimorphisms](https://qchu.wordpress.com/2012/11/03/regular-and-effective-monomorphisms-and-epimorphisms/)*, 2012

See also:

* {#Johnstone} [[Peter Johnstone]], Section A of: _[[Sketches of an Elephant]]_ 

* {#Bed} Marek A. Bednarczyk, Andrzej M. Borzyszkowski, and Wieslaw Pawlowski, *Generalized congruences &#8211; epimorphisms in $\mathcal{C}a t$*, Theory and Applications of Categories [electronic only] 5 (1999), 266-280 ([dml:120226](https://eudml.org/doc/120226?lang=fr&limit=5))

* {#Taylor99} [[Paul Taylor]], *[[Practical Foundations of Mathematics]]*, Cambridge Studies in Advanced Mathematics 59, Cambridge University Press 1999 ([webpage](http://www.paultaylor.eu/~pt/prafm/index.html))



[[!redirects regular epimorphisms]]
[[!redirects regular epi]]
[[!redirects regular epis]]
[[!redirects regular epic]]
[[!redirects regular epics]]