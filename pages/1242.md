
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

An **exact sequence** may be defined in a [[semi-abelian category]], and more generally in a [[homological category]]. It is a [[sequential diagram]] in which the [[image]] of each [[morphism]] is equal to the [[kernel]] of the next morphism.


## Definition
 {#Definition}


### Definition in additive categories
Let $\mathcal{A}$ be an [[additive category]] (often assumed to be an [[abelian category]], for instance $\mathcal{A} = R$[[Mod]] for $R$ some [[ring]]).

+-- {: .num_defn #ExactSequence}
###### Definition

An **exact sequence** in $\mathcal{A}$ is a [[chain complex]] $C_\bullet$ in $\mathcal{A}$ with vanishing [[chain homology]] in each degree:

$$
  \forall n \in \mathbb{N} . H_n(C) = 0 
  \,.
$$

=--

+-- {: .num_defn #ShortExactSequence}
###### Definition

A **short exact sequence** is an exact sequence, def. \ref{ExactSequence} of the form

$$
  \cdots \to 0 \to 0 \to A \to B \to C \to 0 \to 0 \to \cdots
  \,.
$$

One usually writes this just "$0 \to A \to B \to C \to 0$" or even just "$A \to B \to C$".

=--

+-- {: .num_remark }
###### Remark

A general exact sequence is sometimes called a **long exact sequence**, to distinguish from the special case of a short exact sequence.

=--


+-- {: .num_prop #CharacterizationByMonoEpi}
###### Proposition

Explicitly, a sequence of morphisms 

$$ 
  0 \to A \stackrel{i}\to B \stackrel{p}\to C  \to 0
$$

is short exact, def. \ref{ShortExactSequence}, precisely if

1. $i$ is a [[monomorphism]],

1. $p$ is an [[epimorphism]], 

1. and the [[image]] of $i$ equals the [[kernel]] of $p$  (equivalently, the [[coimage]] of $p$ equals the [[cokernel]] of $i$).

=--

+-- {: .proof}
###### Proof

The third condition is the definition of exactness at $B$. So we need to show that the first two conditions are equivalent to exactness at $A$ and at $C$.

This is easy to see by looking at elements when $\mathcal{A} \simeq R$[[Mod]], for some ring $R$ (and the general case can be reduced to this one using one of the [embedding theorems](abelian%20category#EmbeddingTheorems)):

The sequence being exact at

$$
  0 \to A \to B
$$

means, since the [[image]] of $0 \to A$ is just the element $0 \in A$, that the [[kernel]] of $A \to B$ consists of just this element. But since $A \to B$ is a [[group homomorphism]], this means equivalently that $A \to B$ is an [[injection]]. 

Dually, the sequence being exact at

$$
  B \to C \to 0
$$

means, since the [[kernel]] of $C \to 0$ is all of $C$, that also the [[image]] of $B \to C$ is all of $C$, hence equivalently that $B \to C$ is a [[surjection]].

=--

+-- {: .num_defn }
###### Definition

A **[[split exact sequence]]** is a short exact sequence as above in which $i$ is a [[split monomorphism]], or (equivalently) in which $p$ is a [[split epimorphism]].  

=--

In this case, $B$ may be decomposed as the [[biproduct]] $A \oplus C$ (with $i$ and $p$ the usual biproduct inclusion and projection); this sense in which $B$ is 'split' into $A$ and $C$ is the origin of the general terms 'split (mono/epi)morphism'.

### Definition in pointed sets
It is also helpful to consider a similar notion in the case of a [[pointed set]].

+-- {: .num_defn}
###### Definition
In the category $Set_*$ of [[pointed sets]], a sequence
$$
\array{
  (A, a) & \overset{f}{\to} & (B, b) & \overset{g}{\to} & (C, c)
}
$$
is said to be **exact** at $(B, b)$ if $im f = g^{-1}(c)$.

For [[concrete category|concrete]] pointed categories (ie. a category $\mathcal{C}$ with a faithful functor $F: \mathcal{C} \to Set_*$), a sequence is exact if the image under $F$ is exact.
=--

In the case of (abelian) categories like $Ab$ and $R-Mod$, the two notions of exactness coincide if we pick the point of each group/module to be $0$. Such a general notion is useful in cases such as the [[long exact sequence of homotopy groups]] where the homotopy "groups" for small $n$ are just pointed sets without a group structure.

## Properties

### Computing terms in an exact sequence

A typical use of a long exact sequence, notably of the [[homology long exact sequence]], is that it allows to determine some of its entries in terms of others.

The characterization of short exact sequences in prop. \ref{CharacterizationByMonoEpi} is one example for this: whenever in a long exact sequence one entry vanishes as in $\cdot \to 0 \to C_n \to \cdot$ or $\cdot \to C_n \to 0 \to \cdots$, it follows that the _next_ morphism out of or into the vanishing entry is a [[monomorphism]] or [[epimorphism]], respectively.

In particular: 

+-- {: .num_prop }
###### Proposition

If part of an exact sequence looks like

$$
  \cdots \to 0 \to C_{n+1} \stackrel{\partial_n}{\to} C_n \to 0 \to \cdots
  \,,
$$

then $\partial_n$ is an [[isomorphism]] and hence 

$$
  C_{n+1} \simeq C_n
  \,.
$$

=--


### Exactness and quasi-isomorphisms
 {#ExactnessAndQuasiIsomorphisms}

+-- {: .num_prop }
###### Proposition

A chain complex $C_\bullet$ is exact (is a long exact sequence), precisely if the unique [[chain map]] from the [[initial object]], the 0-complex

  $$
    0 \to C_\bullet
  $$

is a [[quasi-isomorphism]].

=--

### Short exact sequences and quotients
 {#SESAndQuotients}

The following are some basic lemmas that show how given a short exact sequence one obtains new short exact sequences from forming [[quotients]]/[[cokernels]] (see [Wise](#Wise)). 

Let $\mathcal{A}$ be an [[abelian category]]. 

+-- {: .num_lemma}
###### Lemma

For

$$
  A \to B \to C \to 0
$$

an exact sequence in $\mathcal{A}$ and for $X \to B$ any morphism in $\mathcal{A}$, also

$$
  A \to B/X \to C/X \to 0
$$

is a short exact sequence.


=--

+-- {: .proof}
###### Proof

We have an exact sequence of complexes of length 2

$$
  \array{
    0 &\to& X &\stackrel{id}{\to}& X &\to& 0
    \\
    \downarrow & & \downarrow & & \downarrow & & \downarrow
    \\
    A &\to& B &\to& C &\to& 0
  }
$$

and the exact sequence to be demonstrated is degreewise the [[cokernel]] of this sequence. So the statement reduces to the fact that forming cokernels is a [[right exact functor]].

=--

+-- {: .num_lemma}
###### Lemma

For

$$
  0 \to A \to B \to C
$$

an exact sequence and $X \to A$ any morphism, also 

$$
  0 \to A/X \to B/X  \to C
$$

is exact.

=--


## Examples

### Specific examples
 {#SpecificExamples}


+-- {: .num_example #MultiplicationAndCyclicGroup}
###### Example

Let $\mathcal{A} = \mathbb{Z}$[[Mod]] $\simeq$ [[Ab]]. For $n \in \mathbb{N}$ with $n \geq 1$ let $\mathbb{Z} \stackrel{\cdot n}{\to} \mathbb{Z}$ be the [[linear map]]/[[homomorphism]] of [[abelian groups]] which acts by the ordinary multiplication of [[integers]] by $n$. This is clearly an [[injection]]. The [[cokernel]] of this morphism is the projection to the [[quotient group]], which is the [[cyclic group]] $\mathbb{Z}_n \coloneqq \mathbb{Z}/n\mathbb{Z}$. Hence we have a short exact sequence

$$
  0 \to \mathbb{Z} \stackrel{\cdot n}{\to} \mathbb{Z}
  \to \mathbb{Z}_n
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The [[connecting homomorphism]] of the [[long exact sequence in homology]] induced from short exact sequences of the form in example \ref{MultiplicationAndCyclicGroup} is called a _[[Bockstein homomorphism]]_.

=--

+-- {: .num_example }
###### Example

* [[exponential exact sequence]]

* [[Kummer sequence]]

* [[Artin-Schreier sequence]]

* [[Kummer-Artin-Schreier-Witt exact sequence]]

=--


### Classes of examples

* [[short exact sequence of vector bundles]]

* [[long exact sequence of homotopy groups]]

* [[long exact sequence in homology]]/[[long exact sequence in homology|in cohomology]]

  * [[long exact sequence in chain homology]]

  * [[long exact sequence in generalized homology]]

* [[Serre long exact sequence]]


## Related concepts

* [[splicing of short exact sequences]]

* [[exact functor]]

* [[exact sequence of Hopf algebras]]


## References

A standard introduction is for instance in section 1.1 of

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_

The quotient lemmas from [above](#SESAndQuotients) are discussed in

* [[Jonathan Wise]], _The Snake Lemma_ ([pdf](http://math.stanford.edu/~jonathan/papers/snake.pdf))
 {#Wise}

in the context of the [[salamander lemma]] and the [[snake lemma]].

[[!redirects exact sequences]]

[[!redirects long exact sequence]]
[[!redirects short exact sequence]]


[[!redirects long exact sequences]]
[[!redirects short exact sequences]]
