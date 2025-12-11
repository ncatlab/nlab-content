+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

*Nakayama's lemma* is a family of simple but fundamental results of [[commutative algebra]] which are frequently used to lift information from the [[fiber]] of a [[sheaf]] over a point (as for example a [[coherent sheaf]] over a [[scheme]]) to give information on the [[stalk]] at that point.

## Statement

We first state and prove a pair of fundamental geometric facts (Prop. \ref{GeneralNakayamaLemma}) concerning the relationships between annihilators, supports, and tensor products of modules and then deduce as corollaries two standard formulations (Cor. \ref{FirstSpecialVersion} and Cor. \ref{SecondSpecialVersion}) of "Nakayama's lemma" from which various other instances thereof can in turn be derived (as is done in [Stacks 00DV](https://stacks.math.columbia.edu/tag/00DV)).

As motivation, recall the following general fact:

\begin{proposition}\label{GeneralNakayamaMotivation}
**(motivation)**
\linebreak
Given [[commutative ring]] $R$, [[natural number|natural]] $n$, and $n$-[[tuple]] of [[module|$R$-modules]] $\left( M _ i \right) _ { i \in n }$,

1. for all $i \in n$, one has $supp \left( M _ i \right) \subseteq \mathcal{V} \left( Ann \left( M _ i \right) \right)$.

2. $supp \left( \underset{ i \in n }{ \bigotimes } M _ i \right) \subseteq \bigcap _ { i \in n } supp \left( M _ i \right)$.

(Here $\mathcal{V}$ denotes the [zero locus](https://stacks.math.columbia.edu/tag/00DZ), $supp$ denotes the [support](https://stacks.math.columbia.edu/tag/00L1), and $Ann$ denotes the [annihilator](https://stacks.math.columbia.edu/tag/07T7).
For convenience, we assume the [[ordinal number|Von Neumann convention]] so that, e.g., the quantification "$i \in n$" is equivalent to "$i \in \left\{ 0 , \dots , n-1 \right\}$".)
\end{proposition}

\begin{proof}
As for the first claim,
if $i \in n$ and $\mathfrak{p} \in supp \left( M _ i \right)$,
i.e., if $M _ i \otimes R _ { \mathfrak{p} } \ \,&#x2244;\, \  0$,
then the elements of $R \setminus \mathfrak{p}$ act nontrivially on $M _ i \otimes R _ { \mathfrak{p} }$,
hence nontrivially on $M _ i$,
hence $Ann \left( M _ i \right) \subseteq \mathfrak{p}$.
As for the second claim, recall that $\left( \underset{ i \in n }{ \bigotimes } M _ i \right) \otimes R _ { \mathfrak{p} } \simeq \underset{ i \in n }{ \bigotimes } \left( M _ i \otimes R _ { \mathfrak{p} } \right)$,
hence that if $\mathfrak{p} \in supp \left( \underset{ i \in n }{ \bigotimes } M _ i \right)$,
i.e., if $\left( \underset{ i \in n }{ \bigotimes } M _ i \right) \otimes R _ { \mathfrak{p} } \ \,&#x2244;\, \  0$,
then for all $i \in n$ one must have $M _ i \otimes R _ { \mathfrak{p} } \ \,&#x2244;\, \  0$,
i.e., $\mathfrak{p} \in supp \left( M _ i \right)$.
\end{proof}

Our first, geometric incarnation of Nakayama’s lemma is just the assertion that if the modules in the statement of Prop. \ref{GeneralNakayamaMotivation} are finitely generated, then the inclusions in the same are equalities.

\begin{proposition}\label{GeneralNakayamaLemma}
**("geometric Nakayama")**
\linebreak
Given [[commutative ring]] $R$, [[natural number|natural]] $n$, and $n$-[[tuple]] of [[finitely generated]] $R$-modules $\left( M _ i \right) _ { i \in n }$,

1. for all $i \in n$, one has $supp \left( M _ i \right) = \mathcal{V} \left( Ann \left( M _ i \right) \right)$.

2. $supp \left( \underset{ i \in n }{ \bigotimes } M _ i \right) = \bigcap _ { i \in n } supp \left( M _ i \right)$.

(Here $\mathcal{V}$ denotes the [zero locus](https://stacks.math.columbia.edu/tag/00DZ), $supp$ denotes the [support](https://stacks.math.columbia.edu/tag/00L1), and $Ann$ denotes the [annihilator](https://stacks.math.columbia.edu/tag/07T7).
For convenience, we assume the [[ordinal number|Von Neumann convention]] so that, e.g., the quantification "$i \in n$" is equivalent to "$i \in \left\{ 0 , \dots , n-1 \right\}$".)
\end{proposition}

We give an "element-free" proof below. The two key ideas are that finitely-generated $R$-modules are (precisely) those which can be "built up" inductively from cyclic $R$-modules via extensions and that the relevant properties of the former are sufficiently determined by those of the latter, which are standard and/or easily verified.

\begin{proof}
Recall the following seven basic facts (essentially two "induction principles", three "interaction principles", and two "base cases" of our "induction" up from cyclic modules):

1. The middle term of a short exact sequence is $0$ iff its left and right terms are $0$

2. The middle component of a morphism of short exact sequences is $0$ iff its left and right components are $0$.

3. Given prime $\mathfrak{p} \in Spec (R)$, the functor $N \mapsto N \otimes R _ { \mathfrak{p} }$ is exact.

4. The ($n$-ary) functor of $R$-modules $\left( N _ i \right) _ { i \in n } \mapsto \underset{ i \in n }{ \bigotimes } N _ i$ is right exact in all arguments.

5. Given prime $\mathfrak{p} \in Spec (R)$ and $n$-tuple of $R$-modules $\left( N _ i \right) _ { i \in n }$, one has $\left( \underset{ i \in n }{ \bigotimes } N _ i \right) \otimes R _ { \mathfrak{p} } \simeq \underset{ i \in n }{ \bigotimes } \left( N _ i \otimes R _ { \mathfrak{p} } \right)$.

6. Given prime $\mathfrak{p} \in Spec (R)$ and ideal $J \subseteq R$, one has $\left( R / J \right) \otimes_{R} R _ { \mathfrak{p} } \ \,&#x2244;\, \  0$ iff $\mathfrak{p} \in \mathcal{V} \left( J \right)$.

7. Given $n$-tuple of ideals $\left( J _ i \subseteq R \right) _ { i \in n }$, one has $\underset{ i \in n }{ \bigotimes } \left( R / J _ i \right) \simeq R / \left( \sum _ { i \in n } J _ i \right)$.

The argument goes in four parts:

1.  Suppose we are given $i \in n$.
By the hypothesis that $M _ i$ is finitely generated
there exists natural $d _ i$ such that $M$ is a quotient of $R ^ { d _ i }$.
It follows (by taking the image under said quotient of the standard length-$d _ i$ filtration of $R ^ { d _ i }$)
that $M _ i$ admits a length-$d _ i$ filtration with cyclic cokernels;
denote this filtration and its associated $d _ i$-tuple of short exact sequences as
\[ 0 \ = \ M _ { i , 0 } \ \overset{ \iota _ { i , 0 } }{ \hookrightarrow } \ \dots \ \overset{ \iota _ { i , d _ i - 1 } }{ \hookrightarrow } \ M _ {i , d _ i } \ = \ M _ i \]
and
\[ \left( \ 0 \ \to \ M_{ i , j } \ \overset{ \iota _ { i , j } }{ \hookrightarrow } \ M_{ i , j + 1 } \ \overset{ \pi _ { i , j } }{ \twoheadrightarrow } \ R / I_{ i , j } \ \to \ 0 \ \right)_{ j \in d _ i } \]
with $\left( I _ { i , j } \subseteq R \right) _ { j \in d _ i }$ ideals.
 
2. We now show, given $i \in n$,
that $\mathcal{V} \left( Ann \left( M _ i \right) \right) = \bigcup _ { j \in d _ i } \mathcal{V} \left( I _ { i , j } \right)$.
Applying recalled fact 2, it follows (inductively) that all $f \in Ann \left( M _ i \right)$ act as $0$ on all the $R / I _ { i , j }$,
hence that $Ann \left( M _ i \right) \subseteq \bigcap_{ j \in d _ i } I _ { i , j }$.
Conversely, it’s clear for all $j \in d _ i$ that $I _ { i , j } M _ { i , j + 1 } \subseteq M _ { i , j }$,
from which it follows (reverse inductively) that $\prod _ { j \in d _ i } I _ { i , j } \subseteq Ann \left( M _ i \right)$.
We conclude that $\prod _ { j \in d _ i } I _ { i , j } \subseteq Ann \left( M _ i \right) 
\subseteq \bigcap_{ j \in d _ i } I _ { i , j }$,
whence the (sub)claim.

3. We now show, given $i \in n$ and prime $\mathfrak{p} \in Spec (R)$,
that $M _ i \otimes R _ { \mathfrak{p} } \ \,&#x2244;\, \  0$ iff there exists $j \in d _ i$ such that $\mathfrak{p} \in \mathcal{V} \left( I _ { i , j } \right)$.
Applying recalled fact 3, we have a $d _ i$-tuple of short exact sequences
\[ \left( \ 0 \ \to \ M_{ i , j } \otimes R _ { \mathfrak{p} } \ \overset{ \iota _ { i , j } \otimes 1 _ { R _ { \mathfrak{p} } } }{ \hookrightarrow } \ M_{ i , j + 1 } \otimes R _ { \mathfrak{p} } \ \overset{ \pi _ { i , j } \otimes 1 _ { R _ { \mathfrak{p} } } }{ \twoheadrightarrow } \ R / I_{ i , j } \otimes R _ { \mathfrak{p} } \ \to \ 0 \ \right)_{ j \in d _ i } . \]
Applying recalled fact 1, it follows (inductively) that $M \ \,&#x2244;\, \  0$ iff there exists $j \in d _ i$ such that $\left( R / I _ { i , j } \right) \otimes R _ { \mathfrak{p} } \ \,&#x2244;\, \  0$.
Applying recalled fact 6 this holds iff in turn there exists $j \in d _ i$ such that $\mathfrak{p} \in \mathcal{V} \left( I _ { i , j } \right)$.

4. We now show, given a prime $\mathfrak{p} \in Spec (R)$,
that $\left( \underset{ i \in n }{ \bigotimes } M _ i \right) \otimes R _ { \mathfrak{p} } \ \,&#x2244;\, \  0$
iff for all $i \in n$ there exists $j \in d _ i$ such that $\mathfrak{p} \in \mathcal{V} \left( I _ { i , j } \right)$.
Suppose first that there exists $i _ { nil } \in n$ such that there exists no $j \in d _ { i _ { nil } }$ such that $\mathfrak{p} \in \mathcal{V} \left( I _ { i _ { nil } , j } \right)$.
Applying recalled facts 3 and 6, we obtain a $d _ { i _ { nil } }$-tuple of isomorphisms
\[ \left( \ 0 \ \to \ \ M_{ i _ { nil } , j } \otimes R _ { \mathfrak{p} } \ \overset{ \iota _ { i _ { nil } , j } \otimes 1 _ { R _ { \mathfrak{p} } } }{ \hookrightarrow } \ M_{ i _ { nil } , j + 1 } \otimes R _ { \mathfrak{p} } \ \twoheadrightarrow \ 0 \ \to \ 0 \ \right) _ { j \in d _ { i _ { nil } } } , \]
from which it follows (inductively) that the composite
\[ 0 \overset{ \iota _ { i _ { nil } , d _ { i _ { nil } } - 1 } \circ \dots \circ \iota _ { i _ { nil } , 0 } }{ \to } M _ { i _ { nil } } \otimes R _ { \mathfrak{p} } \]
is an isomorphism.
Applying recalled fact 5, we conclude by the above that $\left(  \underset{ i \in n }{ \bigotimes } M _ i \right) \otimes R _ { \mathfrak{p} } \simeq 0$.
Suppose now instead that for each $i \in n$ there exists maximal $j _ { i , sup } \in d _ i $ such that $\mathfrak{p} \in \mathcal{V} \left( I _ { i , j _ { i , sup } } \right)$.
Applying recalled facts 3, 4, 6, and 7, we obtain an epimorphism
\[ \left( \underset{ i \in n }{ \bigotimes } M _ { i , j _ { i , sup } } \right) \otimes R _ { \mathfrak{p} } \ \overset{ \left( \underset{ i \in n }{ \bigotimes } \pi _ { i , j _ { i , sup } } \right) \otimes 1 _ { R _ { \mathfrak{p} } } }{ \twoheadrightarrow } \ \left( \underset{ i \in n }{ \bigotimes } \left( R / I _ { i , j _ { i , sup } } \right) \right) \otimes R _ { \mathfrak{p} } \ \ \,&#x2244;\, \  \ 0 , \]
hence that $\left( \underset{ i \in n }{ \bigotimes } M _ { i , j _ { i , sup } } \right) \otimes R _ { \mathfrak{p} } \ \,&#x2244;\, \  0$.
Applying recalled facts 3 and 6 (and the maximality of $j _ { i , sup }$), we obtain isomorphisms
\[ \left( \ 0 \ \to \ \ M_{ i , j } \otimes R _ { \mathfrak{p} } \ \overset{ \iota _ { i , j } \otimes 1 _ { R _ { \mathfrak{p} } } }{ \hookrightarrow } \ M_{ i , j + 1 } \otimes R _ { \mathfrak{p} } \ \twoheadrightarrow \ 0 \ \to \ 0 \ \right) _ { \substack{ i \in n \\ j \in \left\{ j _ { i , sup } + 1 , \dots , d _ { i } - 1 \right\} } } , \]
from which it follows (inductively) that the tensored composite
\[ \underset{ i \in n }{ \bigotimes } \left( M _ { i , j _ { i , sup } } \otimes R _ { \mathfrak{p} } \right) \overset{ \underset{ i \in n }{ \bigotimes } \left( \left( \iota _ { i , d _ i - 1 } \otimes 1 _ { R _ { \mathfrak{p} } } \right) \circ \dots \circ \left( \iota _ { i , j _ { i , sup } + 1 }  \otimes 1 _ { R _ { \mathfrak{p} } } \right) \right) }{ \to } \underset{ i \in n }{ \bigotimes } \left( M _ i \otimes R _ { \mathfrak{p} } \right) \]
is an isomorphism.
Applying recalled fact 5 (twice), we conclude by the above that $\left( \underset{ i \in n }{ \bigotimes } M _ i \right) \otimes R _ { \mathfrak{p} } \ \,&#x2244;\, \  0$.

Claims 1 and 2 of Prop. \ref{GeneralNakayamaLemma} are immediate from subarguments 2 and 3 and 2 and 4 above respectively.
\end{proof}

Prop. \ref{GeneralNakayamaLemma} immediately gives the following corollary, which we include for general interest:

\begin{corollary}\label{SupportTensorIntersection}
**(Bounds on the annihilator of a tensor product of finitely generated modules)**
\linebreak
Given commutative ring $R$, natural $n$, and $n$-tuple of finitely generated $R$-modules $\left( M _ i \right) _ { i \in n }$,
\[ \sum _ { i \in n } Ann \left( M _ i \right) \ \subseteq \ Ann \left( \underset{ i \in n }{ \bigotimes } M _ i \right) \ \subseteq \ rad \left( \sum _ { i \in n } Ann \left( M _ i \right) \right) . \]

(Here $Ann$ denotes the [annihilator](https://stacks.math.columbia.edu/tag/07T7) and $rad$ denotes the [[radical]].
For convenience, we assume the [[ordinal number|Von Neumann convention]] so that, e.g., the quantification "$i \in n$" is equivalent to "$i \in \left\{ 0 , \dots , n-1 \right\}$".)
\end{corollary}

\begin{proof}
The left inclusion follows from that each $Ann \left( M _ i \right)$ (manifestly) annihilates $\underset{ i \in n }{ \bigotimes } M _ i$.
The right inclusion follows from that by claims 1 and 2 of Prop. \ref{GeneralNakayamaLemma}
\[
\begin{aligned}
\mathcal{V} \left( Ann \left( \underset{ i \in n }{ \bigotimes } M _ i \right) \right)
& = supp \left( \underset{ i \in n }{ \bigotimes } M _ i \right) \\
& = \bigcap _ { i \in n } supp \left( M _ i \right) \\
& = \bigcap _ { i \in n } \mathcal{V} \left( Ann \left( M _ i \right) \right) \\
& = \mathcal{V} \left( \sum _ { i \in n } Ann \left( M _ i \right) \right) ,
\end{aligned}
\]
hence $rad \left( Ann \left( \underset{ i \in n }{ \bigotimes } M _ i \right) \right)
 = rad \left( \sum _ { i \in n } Ann \left( M _ i \right) \right)$.
\end{proof}

Remark that the finiteness hypotheses in the statements of Prop. \ref{GeneralNakayamaLemma} and Cor. \ref{SupportTensorIntersection} are necessary:

\begin{example}\label{NoInfiniteNakayama}
**(The finitness hypotheses in Prop. \ref{GeneralNakayamaLemma} and Cor. \ref{SupportTensorIntersection} are necessary)**
\linebreak
Viewing $\mathbb{Q} / \mathbb{Z}$ as a $\mathbb{Z}$-module,

- $supp \left( \mathbb{Q} / \mathbb{Z} \right) \subsetneq \mathcal{V} \left( Ann \left( \mathbb{Q} / \mathbb{Z} \right) \right)$,

- $supp \left( \left( \mathbb{Q} / \mathbb{Z} \right) \otimes \left( \mathbb{Q} / \mathbb{Z} \right) \right) \subsetneq supp \left( \mathbb{Q} / \mathbb{Z} \right) \cap supp \left( \mathbb{Q} / \mathbb{Z} \right)$,

- $Ann \left( \left( \mathbb{Q} / \mathbb{Z} \right) \otimes \left( \mathbb{Q} / \mathbb{Z} \right) \right) \supsetneq rad \left( Ann \left( \mathbb{Q} / \mathbb{Z} \right) + Ann \left( \mathbb{Q} / \mathbb{Z} \right) \right)$,

contradicting claims 1 and 2 of Prop. \ref{GeneralNakayamaLemma} and Cor. \ref{SupportTensorIntersection} respectively sans the finiteness hypotheses.
\end{example}

Note likewise that the right inclusion in Cor. \ref{SupportTensorIntersection} can be tight even when the left one isn't:

\begin{example}\label{SupportTensorIntersectionTight}
**(The right bound in Cor. \ref{SupportTensorIntersection} is nontrivially achievable)** 
\linebreak
Let $R = \mathbb{Z} \left[ x _ 0, x _ 1 \right]$, $M _ 0 = R / ( x _ 0 ) \oplus R / ( x _ 1 )$, and $M _ 1 = R / ( x _ 0 - x _ 1 )$.
Then
\[ Ann \left( M _ 0 \right) + Ann \left( M _ 1 \right) \subsetneq Ann \left( M _ 0 \otimes M _ 1 \right) = rad \left( Ann \left( M _ 0 \right) + Ann \left( M _ 1 \right) \right) , \]
viewing $M _ 0$ and $M _ 1$ as $R$-modules.
\end{example}

\begin{proof}
Observe that

- $Ann \left( M _ 0 \right) = ( x _ 0 x_ 1 )$.

- $Ann \left( M _ 1 \right) = ( x _ 0 - x _ 1 )$.

- $Ann \left( M _ 0 \right) + Ann \left( M _ 1 \right) = ( x _ 0 - x _ 1 ) + ( x _ 0 , x_ 1 ) ^ 2$.

- $rad \left( Ann \left( M _ 0 \right) + Ann \left( M _ 1 \right) \right) = ( x _ 0 , x_ 1 )$.

- $M _ 0 \otimes M _ 1 \simeq R / ( x _ 0 , x _ 1 ) \oplus R / ( x _ 0 , x _ 1 )$.

- $Ann \left( M _ 0 \otimes M _ 1 \right) = ( x _ 0 , x_ 1 )$.

The claim follows.
\end{proof}

We now deduce more familiar forms of Nakayama's lemma can as corollaries of the above. Sometimes, as for instance in the [Stacks Project](https://stacks.math.columbia.edu/tag/00DV), wherein all 11(!) other formulations of the lemma are straightforwardly reduced to the following, Nakayama's lemma is stated instead as:

\begin{corollary}\label{FirstSpecialVersion}
**(Nakayama, version 1)** 
\linebreak
Given commutative ring $R$, finitely generated $R$-module $M$, and ideal $I \subseteq R$ such that $I M = M$,
there exists element $f \in R$ such that $f = 1 \ (mod \ I)$ and $f M = 0$.
\end{corollary}
\begin{proof}
From that $I M = M$ it follows that $M \otimes_{R} \left( R / I \right) \simeq 0$,
i.e. that $supp \left( M \otimes_{R} left( R / I \right) = \emptyset$,
hence by claims 1 and 2 of Prop. \ref{GeneralNakayamaLemma}
that $\mathcal{V} \left( Ann \left( M \right) \right)$ is disjoint from $\mathcal{V} \left( I \right)$,
i.e. that $Ann \left( M \right)$ and $I$ are comaximal.
The [Chinese Remainder theorem](https://stacks.math.columbia.edu/tag/00DT) then constructs the desired $f \in R$ such that $f = 1\ (mod\ I)$ and $f = 0\ \left( mod\ Ann \left( M \right) \right)$.
\end{proof}

Alternatively, Nakayama's lemma is often understood as a means by which information about the fiber of a module at a point can be used to characterize that of its stalk at said point:

\begin{corollary}\label{SecondSpecialVersion}
**(Nakayama, version 2)** 
\linebreak
Given [[local ring]] $R$ with maximal ideal $\mathfrak{m} \subseteq R$ and finitely generated $R$-module $M$,
then $M \ \,&#x2244;\, \  0$ iff $M \otimes_R \left( R / \mathfrak{m} \right) \ \,&#x2244;\, \  0$. 
\end{corollary}
\begin{proof}
Observe that $\mathfrak{m} \in supp \left( R / \mathfrak{m} \right)$,
hence by claim 2 of Prop. \ref{GeneralNakayamaLemma}
that $\mathfrak{m} \in supp (M)$ iff $\mathfrak{m} \in supp \left( M \otimes_R \left( R / \mathfrak{m} \right) \right)$.
Conclude by that an $R$-module is (essentially tautologically) $\ \,&#x2244;\, \  0$ iff $\mathfrak{m}$ is in its support.
\end{proof}

## Examples and consequences

\begin{example}
Suppose $R$ is a local ring with maximal ideal $\mathfrak{m} \subseteq R$ and $f \colon N \to M$ is an $R$-module map. The latter gives rise to an exact sequence
\[ N \stackrel{f}{\to} M \stackrel{p}{\to} M / N \to 0 . \]
Tensoring with $R / \mathfrak{m}$ is a right exact functor, so we have an exact sequence
\[ N \otimes_{R} (R / \mathfrak{m}) \stackrel{f \otimes_{R} (R / \mathfrak{m})}{\to} M \otimes_{R} (R / \mathfrak{m}) \stackrel{p \otimes_{R} (R / \mathfrak{m})}{\to} (M / N) \otimes_{R} (R / \mathfrak{m}) \to 0 . \]
Nakayama's lemma says that if $(M / N) \otimes_{R} (R / \mathfrak{m})$, then $M / N \cong 0$. Equivalently, it says that if $f \otimes_{R} (R / \mathfrak{m})$ is epic, then $f$ is epic. In particular, to check whether a finite set of elements $v_{1}, \ldots, v_{n}$ generates $M$, it suffices to check whether the residue classes $v_i \mod \mathfrak{m} M$ generate the vector space $M / \mathfrak{m} M$, which is a linear algebra calculation (as $R / \mathfrak{m}$ is a field). 
\end{example}

\begin{example}
Suppose $R$ is a [[Noetherian ring|Noetherian]] local ring with maximal ideal $\mathfrak{m} \subseteq R$. A typical example is the stalk at a point $p$ of a Noetherian scheme as locally ringed space, and we will write as if we were in that situation. As $R$ is Noetherian, $\mathfrak{m}$ is finitely generated. Suppose $\mathfrak{m} \otimes (R / \mathfrak{m}) \cong \mathfrak{m} / \mathfrak{m}^2$ -- the cotangent space -- is a vector space of dimension $n$. We would like to know whether a collection of functions $f_1, \ldots, f_n$ that vanish at $\mathfrak{m}$ form a local coordinate system. 

For this, it suffices to check whether the differentials $d f_1, \ldots, d f_n$ at $\mathfrak{m}$, belonging to the cotangent space $\mathfrak{m}/\mathfrak{m}^2$, are linearly independent. (For then they span the cotangent space, and one concludes from Nakayama that the $f_i$ generate $\mathfrak{m}$ as an $R$-module, thereby forming a local coordinate system at $\mathfrak{m}$.) In this way, Nakayama's lemma operates as a kind of "inverse function theorem". 
\end{example}

To cement this further, the following statement is offered in [Harris](#Harris) as a corollary of Nakayama's lemma (corollary 14.10, page 179): 

+-- {: .num_prop}
###### Proposition 
**(Inverse Function Theorem)** 
A map between complex projective varieties of dimension $n$ which is a bijection and has injective derivative at every point is an isomorphism. 
=-- 

## References

* [[Stacks Project]]: [07RC](https://stacks.math.columbia.edu/tag/07RC)

* Wikipedia: *[Nakayama lemma](https://en.wikipedia.org/wiki/Nakayama%27s_lemma)*

category: algebra


[[!redirects Nakayama lemma]]

