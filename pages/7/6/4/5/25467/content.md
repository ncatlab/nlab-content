
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

Suppose we have a [[fibered category]] $p \colon \mathcal{E} \to \mathcal{B}$, whose objects we think as [[categories with families|type families]] (living in the fibers of $\mathcal{E}$) indexed by [[contexts]] (living in $\mathcal{B}$).

A **definable collection** of objects of the total category $\mathcal{E}$ corresponds, intuitively, to the extension of a 'meta-property' of the types which we can use to single out subcontexts by means of a generalized '[[comprehension category|comprehension]]'.

The archetypal example is given by 'truth'. Suppose $p$ has [[fibred terminal objects]], i.e. over each context $B:\mathcal{B}$, there is a 'unit type' $1_B : \mathcal{E}_B$, terminal in the fiber.
Then the collection $\{1_B : \mathcal{E} \mid B: \mathcal{B}\}$ is an extensive definition of the meta-property of 'being true' (or better: being inhabited).

Once we have a definable collection $\mathcal{P}$, and given an object $X: \mathcal{E}_B$, we can ask: which members of the 'family' $X$ 'satisfy' $P$? This question is answered by a subobject $\{b:B \mid X_b : \mathcal{P}\} \rightarrowtail B : \mathcal{B}$.

In a sense, a definable collection is a very weak notion of [[coreflective subcategory|coreflective subfibration]] (i.e. a fibred coreflective subcategory).

## Definition

We follow the exposition in [(Jacobs '99)](#Jacobs).
Fix a [[Grothendieck fibration|fibration]] $p:\mathcal{E} \to \mathcal{B}$.

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

* {#Jacobs} [[Bart Jacobs]], _Categorical Logic and Type Theory_, Studies in Logic and the Foundations of Mathematics, 141. North-Holland Publishing Co., Amsterdam, 1999. xviii+760 pp. ISBN: 0-444-50170-3 ([pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)) ([contents](http://www.cs.ru.nl/B.Jacobs/CLT/bookinfo.html))