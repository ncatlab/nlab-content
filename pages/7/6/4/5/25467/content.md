
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fibred category theory
+-- {: .hide}
[[!include fibred category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Suppose we have a [[fibered category]] $p \colon \mathcal{E} \to \mathcal{B}$, whose objects we think as [[categories with families|type families]] (living in the fibers of $\mathcal{E}$) indexed by [[contexts]] (living in $\mathcal{B}$, cf. the [[categorical semantics of dependent types]]).

A **definable collection** of objects of the total category $\mathcal{E}$ corresponds, intuitively, to the extension of a 'meta-property' of the types which we can use to single out subcontexts by means of a generalized '[[comprehension category|comprehension]]'.

{#ArchetypicalExample} The archetypal example is given by '[[truth]]': Suppose $p$ has [[fibred terminal objects]], i.e. over each [[context]] $B \colon \mathcal{B}$, there is a '[[unit type]]' $1_B \colon \mathcal{E}_B$ which is [[terminal object|terminal]] in the fiber.
Then the collection $\{1_B \colon \mathcal{E} \mid B \colon \mathcal{B}\}$ is an extensive definition of the meta-property of 'being true' (or better: being [[inhabited type|inhabited]]).

Once we have a definable collection $\mathcal{P}$, and given an object $X: \mathcal{E}_B$, we can ask: which members of the 'family' $X$ 'satisfy' $P$? This question is answered by a subobject $\{b:B \mid X_b : \mathcal{P}\} \rightarrowtail B : \mathcal{B}$.

In a sense, a definable collection is a very weak notion of [[coreflective subcategory|coreflective subfibration]] (i.e. a fibred coreflective subcategory).

## Definition

We follow the exposition in [(Jacobs '99)](#Jacobs).
Fix a [[Grothendieck fibration|fibration]] $p:\mathcal{E} \to \mathcal{B}$.

### Of collections of objects

\begin{definition}

Let $\mathcal{P}$ be a collection of object in $\mathcal{E}$, and denote by $\mathcal{P}_B$ the subcollection of those objects in $\mathcal{P}$ over a chosen $B:\mathcal{B}$.

1. We say $\mathcal{P}$ is **closed under substitution** if for each map $u:J \to I$ in $\mathcal{B}$ and $P : \mathcal{P}_I$, $u^*P : \mathcal{P}_J$.

2. We say $\mathcal{P}$ is **definable** if it is closed under substitution and, for each object $X: \mathcal{E}$, there is an object $\{X\}_{\mathcal{P}} : \mathcal{P}$ and  a [[cartesian morphism]] $i_X : \{X\}_{\mathcal{P}} \to X$ which is universal among cartesian morphisms into $X$ from an object in $\mathcal{P}$.

\end{definition}

The constructor $\{-\}_{\mathcal{P}}$ is the generalized comprehension we were mentioning above.
Indeed, we have the following characterization:

\begin{lemma} *(Lemma 9.6.2 in [(Jacobs '99)](#Jacobs))*

Let $\mathcal{P}$ be a collection closed under substitution.
Then the following our equivalent:

1. $\mathcal{P}$ is definable
2. For each object $X: \mathcal{E}_B$ the [[presheaf]] on $\mathcal{B}$ defined as
   \[
      J \mapsto \{u : J \to I \mid u^*X : \mathcal{P}\}
   \]
   is representable.

\end{lemma}
\begin{proof}
  The idea is that $\{X\}_P$ is the representing object for the presheaf object of (2).
\end{proof}

### Of collections of functors
\begin{definition}
Let $\mathcal{C}$ be a category, that we think of as trivially fibred $!_{\mathcal{C}} : \mathcal{C} \to 1$. A collection of fibred functors $\{(I_a, f_a) : !_{\mathcal{C}} \to p\}_{a:A}$ (where $A$ is a [[class]]) is definable iff it is definable as a collection of object of the [[exponent fibration]] $p^{!_{\mathcal{C}}}$.
\end{definition}

Recall the exponent fibration $p^{!_{\mathcal{C}}}$ is a fibration over $\mathcal{B}$ whose fiber over $I:\mathcal{B}$ is given by functors $\mathcal{C} \to \mathcal{E}_I$ and whose reindexing is given by post-composition with the reindexing functors of $p$. See [[exponent fibration]] for more details.

\begin{remark}
Clearly this definition generalizes the previous one since collections of objects of $\mathcal{E}$ are given by collections of functors out of $\mathcal{C}$.
\end{remark}

### Of collections of vertical morphisms
\begin{definition}
A collection of [[vertical morphisms]] of $\mathcal{E}$ is definable iff it is definable as collection of functors out of the arrow category $\downarrow$.
\end{definition}

### Of subfibrations
\begin{definition}
A [[subfibration]] $p': \mathcal{E}' \to \mathcal{B}$ of $p$ is definable iff its collection of objects and vertical morphisms are both definable.
\end{definition}

## Examples

\begin{example}
If $p$ has a fibred terminal objects, then their collection is definable if and only if the functor $1: \mathcal{B} \to \mathcal{E}$ has a right adjoint $\{-\}:\mathcal{E} \to \mathcal{B}$.
\end{example}

\begin{example}
For $p : \mathrm{Fam}(\mathcal{C}) \to \mathbf{Set}$ a fibration of families (a family over $I:\mathbf{Set}$ is a n $I$-indexed family of objects of $\mathcal{C}$), definable collection are those determined by a choice of objects of $\mathcal{C}$ (Lemma 9.6.4 in in [(Jacobs '99)](#Jacobs)).
\end{example}

## See also

* [[fibred category]]

* [[comprehension category]]

* [[axiom of comprehension]]

## References

Definability is introduced on p.35 ('Short annotated glossary') of

* {#Benabou85} [[Jean Bénabou]], _Fibered categories and the foundations of naive category theory_, Journal of Symbolic Logic, **50**(1) (1985) pp10-37. doi:[10.2307/2273784](https://doi.org/10.2307/2273784), ([JSTOR](http://www.jstor.org/stable/2273784))

A modern and more traditional account is given in Section 9.6 of

* {#Jacobs} [[Bart Jacobs]], *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf), [webpage](http://www.cs.ru.nl/B.Jacobs/CLT/bookinfo.html)&rbrack;

