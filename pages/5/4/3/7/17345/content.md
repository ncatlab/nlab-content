[[!redirects Introduction to Stable homotopy theory -- I]]
[[!redirects Introduction to Stable homotopy theory -- I]]

{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

***

This page is an introduction to [[spectral sequences]]. We motivate [[spectral sequences of filtered complexes]]
from the computation of [[cellular cohomology]] via stratum-wise [[relative cohomology]]. In the end
we generalize to [[spectral sequences of filtered spectra]].

$\,$

For background on [[homological algebra]] see at _[[schreiber:Introduction to Homological algebra]]_.

For background on [[stable homotopy theory]] see at _[[Introduction to Stable homotopy theory]]_.

For application to [[complex oriented cohomology]] see at _[[Introduction to Cobordism and Complex Oriented Cohomology]]_.

For application to the [[Adams spectral sequence]] see _[[Introduction to Stable homotopy theory -- 2|Introduction to Adams spectral sequences]]_.


***

$\,$

#Contents#
* table of contents
{:toc}



In _[[Introduction to Stable homotopy theory -- 1|Introduction to Stable homotopy theory]]_ we have set up the concept of [[spectra]] $X$ and their [[stable homotopy groups]] $\pi_\bullet(X)$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGroups)). More generally for $X$ and $Y$ two spectra then there is the graded stable homotopy group $[X,Y]_\bullet$ of homotopy classes of maps bewteen them ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory)). These may be thought of as [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology]] groups ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-1#ForASpectrumXGeneralizedECohomology)). Moreover, in _[[Introduction to Stable homotopy theory -- 1-2|part 1.2]]_ we discussed the [[symmetric monoidal smash product of spectra]] $X \wedge Y$. The stable homotopy groups of such a smash product spectrum may be thought of as [[generalized homology]] groups ([rmk.](Introduction+to+Stable+homotopy+theory+--+1-2#EMHomology)).

These stable homotopy and generalized (co-)homology groups are the fundamental invariants in [[algebraic topology]]. In general they are as rich and interesting as they are hard to compute, as famously witnessed by the [[stable homotopy groups of spheres]], some of which we compute in [[Introduction to Stable homotopy theory -- 2|part 2]].


In general the only practicable way to carry out such computations is by doing them along a decomposition of the given spectrum into a "sequence of stages" of sorts. The concept of _[[spectral sequence]]_ is what formalizes this idea.

(Here the re-occurence of the root "spectr-" it is a historical coincidence, but a lucky one.)

Here we give an expository introduction to the concept of spectral sequences, building up in detail to the spectral sequence of a filtered complex.

We put these spectral sequences to use in

* _[[Introduction to Stable homotopy theory -- 2|part 2 -- Adams spectral sequences]].

* _[[Introduction to Stable homotopy theory -- S|part S -- Complex oriented cohomology theory]]_


## For filtered complexes
 {#SpectralSequencesForFilteredChainComplexes}

We begin with recalling basics of [[ordinary cohomology|ordinary]] _[[relative homology]]_ and then seamlessly derive the notion of _[[spectral sequences]]_ from that as the natural way of computing the ordinary cohomology of a [[CW-complex]] stagewise from the relative cohomology of its [[simplicial skeleton|skeleta]]. This is meant as motivation and warmup. What we are mostly going to use further below are spectral sequences induced by [[filtered spectra]], this we turn to [next](#SpectralSequencesForFilteredSpectra).





### Ordinary homology

Let $X$ be a [[topological space]] and $A \hookrightarrow X$ a [[topological subspace]]. Write $C_\bullet(X)$ for the [[chain complex]] of [[singular homology]] on $X$ and $C_\bullet(A) \hookrightarrow C_\bullet(X)$ for the [[chain map]] induced by the subspace inclusion.

+-- {: .num_defn #RelativeSingularHomology}
###### Definition

The (degreewise) [[cokernel]] of this inclusion, hence the [[quotient]] $C_\bullet(X)/C_\bullet(A)$ of $C_\bullet(X)$ by the [[image]] of $C_\bullet(A)$ under the inclusion, is the **chain complex of $A$-relative singular chains**.

* A [[boundary]] in this quotient is called an **$A$-relative singular boundary**,

* a [[cycle]] is called an **$A$-relative singular cycle**.

* The [[chain homology]] of the quotient is the **$A$-relative singular homology of $X$**

  $$
    H_n(X , A)\coloneqq H_n(C_\bullet(X)/C_\bullet(A))
    \,.
  $$

=--

+-- {: .num_remark}
###### Remark

This means that a singular $(n+1)$-chain $c \in C_{n+1}(X)$ is an $A$-relative cycle precisely if its [[boundary]] $\partial c \in C_{n}(X)$ is, while not necessarily 0, contained in the $n$-chains of $A$: $\partial c \in C_n(A) \hookrightarrow C_n(X)$. So the boundary vanishes possibly only "up to contributions coming from $A$".

=--

We record two evident but important classes of [[long exact sequences]] that relative homology groups sit in:

+-- {: .num_prop #RelativeHomologyLongExactSequence}
###### Proposition

Let $A \stackrel{i}{\hookrightarrow} X$ be a [[topological subspace]] inclusion. The corresponding
relative singular homology, def. \ref{RelativeSingularHomology}, sits in a [[long exact sequence]] of the form

$$
  \cdots
  \to
  H_n(A)
   \stackrel{H_n(i)}{\to}
  H_n(X)
  \to
  H_n(X, A)
   \stackrel{\delta_{n-1}}{\to}
  H_{n-1}(A)
   \stackrel{H_{n-1}(i)}{\to}
  H_{n-1}(X)
  \to
  H_{n-1}(X, A)
  \to
  \cdots
  \,.
$$

The [[connecting homomorphism]] $\delta_{n} \colon H_{n+1}(X, A) \to H_n(A)$ sends an element $[c] \in H_{n+1}(X, A)$ represented by an $A$-relative cycle $c \in C_{n+1}(X)$, to the class represented by the [[boundary]] $\partial^X c \in C_n(A) \hookrightarrow C_n(X)$.

=--

+-- {: .proof}
###### Proof

This is the _[[homology long exact sequence]]_, induced by the defining [[short exact sequence]] $0 \to C_\bullet(A) \stackrel{i}{\hookrightarrow} C_\bullet(X) \to coker(i)  \simeq C_\bullet(X)/C_\bullet(A)  \to 0$ of chain complexes.

=--

+-- {: .num_prop #RelativeTripleHomologyLongExactSequence}
###### Proposition

Let $B \hookrightarrow A \hookrightarrow X$ be a sequence of two [[topological subspace]] inclusions. Then there is a [[long exact sequence]] of [[relative singular homology]] groups of the form

$$
  \cdots \to H_n(A , B) \to H_n(X , B) \to H_n(X , A ) \to H_{n-1}(A , B) \to \cdots
  \,.
$$

=--

+-- {: .proof}
###### Proof

Observe that we have a [[short exact sequence]] of chain complexes, def. \ref{ShortExactSequenceOfChainComplexes}

$$
  0 \to C_\bullet(A)/C_\bullet(B) \to C_\bullet(X)/C_\bullet(B) \to C_\bullet(X)/C_\bullet(A) \to 0
  \,.
$$

The corresponding [[homology long exact sequence]], prop. \ref{HomologyLongExactSequence}, is the long exact sequence in question.

=--

We look at some concrete fundamental examples in a moment. But first it is useful to make explicit the following general sub-notion of relative homology.

Let $X$ still be a given [[topological space]].

+-- {: .num_defn}
###### Definition

The **[[augmentation]] map** for the [[singular homology]] of $X$ is the [[homomorphism]] of [[abelian groups]]

$$
  \epsilon \colon C_0(X) \to \mathbb{Z}
$$

which adds up all the coefficients of all 0-chains:

$$
  \epsilon \colon \colon \sum_{i} n_i \sigma_i \mapsto \sum_i n_i
  \,.
$$

Since the [[boundary]] of a 1-chain is in the [[kernel]] of this map, by example \ref{BasicExamplesOfChainBoundaries}, it constitutes a [[chain map]]

$$
  \epsilon \colon C_\bullet(X) \to \mathbb{Z}
  \,,
$$

where now $\mathbb{Z}$ is regarded as a chain complex concentrated in degree 0.

=--

+-- {: .num_defn #ReducedSingularChainComplex}
###### Definition

The **reduced singular chain complex** $\tilde C_\bullet(X)$ of $X$ is the [[kernel]] of the augmentation map, the chain complex sitting in the [[short exact sequence]]

$$
  0 \to \tilde C_\bullet(C) \to C_\bullet(X) \stackrel{\epsilon}{\to} \mathbb{Z} \to 0
  \,.
$$

The **reduced singular homology** $\tilde H_\bullet(X)$ of $X$ is the [[chain homology]] of the reduced singular chain complex

$$
  \tilde H_\bullet(X) \coloneqq H_\bullet(\tilde C_\bullet(X))
  \,.
$$

=--

Equivalently:

+-- {: .num_defn}
###### Definition

The **reduced singular homology** of $X$, denoted $\tilde H_\bullet(X)$, is the [[chain homology]] of the [[augmentation|augmented]] chain complex

$$
  \cdots \to C_2(X) \stackrel{\partial_1}{\to} C_1(X) \stackrel{\partial_0}{\to} C_0(X) \stackrel{\epsilon}{\to}
  \mathbb{Z} \to 0
  \,.
$$

=--

Let $X$ be a [[topological space]], $H_\bullet(X)$ its [[singular homology]] and $\tilde H_\bullet(X)$ its reduced singular homology, def. \ref{ReducedSingularChainComplex}.

+-- {: .num_prop #RelationBetweenReducedSingularAndSingular}
###### Proposition

For $n \in \mathbb{N}$ there is an [[isomorphism]]

$$
  H_n(X)
  \simeq
  \left\{
    \array{
      \tilde H_n(X) & for \; n \geq 1
      \\
      \tilde H_0(X) \oplus \mathbb{Z} & for\; n = 0
    }
  \right.
$$

=--

+-- {: .proof}
###### Proof

The [[nLab:homology long exact sequence]], prop. \ref{HomologyLongExactSequence}, of the defining short exact sequence $\tilde C_\bullet(C) \to C_\bullet(X) \stackrel{\epsilon}{\to} \mathbb{Z}$ is, since $\mathbb{Z}$ here is concentrated in degree 0, of the form

$$
  \cdots \to \tilde H_n(X) \to H_n(X) \to 0 \to \cdots \to
  0 \to
  \cdots \to \tilde H_1(X) \to H_1(X) \to 0 \to
  \tilde H_0(X) \to H_0(X) \stackrel{\epsilon}{\to}  \mathbb{Z} \to 0
  \,.
$$

Here [[nLab:exact sequence|exactness]] says that all the morphisms $\tilde H_n(X) \to H_n(X)$ for positive $n$ are [[nLab:isomorphisms]]. Moreover, since $\mathbb{Z}$ is a [[nLab:free abelian group]], hence a [[nLab:projective object]], the remaining [[nLab:short exact sequence]]

$$
  0 \to \tilde H_0(X) \to H_0(X) \to \mathbb{Z} \to 0
$$

is [[nLab:split exact sequence|split]], by prop. \ref{SplittingLemma}, and hence $H_0(X) \simeq \tilde H_0(X) \oplus \mathbb{Z}$.

=--

+-- {: .num_prop}
###### Proposition

For $X = *$ the [[nLab:point]], the morphism

$$
  H_0(\epsilon) \colon H_0(X) \to \mathbb{Z}
$$

is an [[nLab:isomorphism]]. Accordingly the reduced homology of the point vanishes in every degree:

$$
  \tilde H_\bullet(*) \simeq 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion in section [2)](#SimplicialHomology) we have that

$$
  H_n(*) \simeq
  \left\{
    \array{
       \mathbb{Z} & for \; n = 0
       \\
       0 & otherwise
    }
  \right.
  \,.
$$

Moreover, it is clear that $\epsilon \colon C_0(*) \to \mathbb{Z}$ is the [[nLab:identity]] map.

=--

Now we can discuss the relation between reduced homology and relative homology.

+-- {: .num_prop}
###### Proposition

For $X$ an [[inhabited set|inhabited]] [[topological space]], its [[reduced singular homology]], def. \ref{ReducedSingularChainComplex}, coincides with its [[relative singular homology]] relative to any base point $x \colon * \to X$:

$$
  \tilde H_\bullet(X)
  \simeq
   H_\bullet(X,*)
  \,.
$$


=--

+-- {: .proof}
###### Proof

Consider the sequence of [[nLab:topological subspace]] inclusions

$$
  \emptyset \hookrightarrow * \stackrel{x}{\hookrightarrow} X
  \,.
$$

By prop. \ref{RelativeTripleHomologyLongExactSequence} this induces a [[nLab:long exact sequence]] of the form

$$
  \cdots
  \to
  H_{n+1}(*) \to H_{n+1}(X) \to H_{n+1}(X,*)
  \to
  H_n(*) \to H_n(X) \to H_n(X,*)
  \to
  \cdots
  \to
  H_1(X) \to H_1(X,*) \to  H_0(*) \stackrel{H_0(x)}{\to}  H_0(X) \to H_n(X,*)
  \to 0
  \,.
$$

Here in positive degrees we have $H_n(*) \simeq 0$ and therefore [[nLab:exact sequence|exactness]] gives [[nLab:isomorphisms]]

$$
  H_n(X) \stackrel{\simeq}{\to} H_n(X,*)\;\; \forall_{n \geq 1}
$$

and hence with prop. \ref{RelationBetweenReducedSingularAndSingular} isomorphisms

$$
  \tilde H_n(X) \stackrel{\simeq}{\to} H_n(X,*)\;\; \forall_{n \geq 1}
  \,.
$$

It remains to deal with the case in degree 0. To that end, observe that $H_0(x) \colon H_0(*) \to H_0(X)$ is a [[nLab:monomorphism]]: for this notice that we have a [[nLab:commuting diagram]]

$$
  \array{
     H_0(*) &\stackrel{id}{\to}& H_0(*)
     \\
     {}^{\mathllap{H_0(x)}}\downarrow &{}^{\mathllap{H_0(f)}}\nearrow& \downarrow^{\mathrlap{H_0(\epsilon)}}_\simeq
     \\
     H_0(X) &\stackrel{H_0(\epsilon)}{\to}& \mathbb{Z}
  }
  \,,
$$

where $f \colon X \to *$ is the terminal map.
That the outer square commutes means that $H_0(\epsilon) \circ H_0(x) = H_0(\epsilon)$ and hence the composite on the left is an [[nLab:isomorphism]]. This implies that $H_0(x)$ is an injection.

Therefore we have a [[nLab:short exact sequence]] as shown in the top of this diagram

$$
  \array{
    0 &\to& H_0(*) &\stackrel{H_0(x)}{\hookrightarrow}&
    H_0(X) &\stackrel{}{\to}& H_0(X,*)
    &\to&
    0
    \\
    && & {}_{\mathllap{\simeq}}\searrow & \downarrow^{\mathrlap{H_0(\epsilon)}} &
   \\
   && && \mathbb{Z}
  }
  \,.
$$

Using this we finally compute

$$
  \begin{aligned}
    \tilde H_0(X)
    & \coloneqq
    ker H_0(\epsilon)
    \\
    & \simeq coker( H_0(x) )
    \\
    & \simeq H_0(X,*)
  \end{aligned}
  \,.
$$

=--

With this understanding of homology _relative to a point_ in hand, we can now characterize relative homology more generally.
From its definition in def. \ref{RelativeSingularHomology}, it is plausible that the relative homology group $H_n(X,A)$ provides information about the quotient topological space $X/A$. This is indeed true under mild conditions:

+-- {: .num_defn #GoodPair}
###### Definition

A [[nLab:topological subspace]] inclusion $A \hookrightarrow X$ is called a **good pair** if

1. $A$ is [[nLab:closed subset|closed]] inside $X$;

1. $A$ has an [[nLab:neighbourhood]] $A \hookrightarrow U \hookrightarrow X$ such that $A \hookrightarrow U$ has a [[nLab:deformation retract]].

=--

+-- {: .num_prop #HomologyOfQuotientSpace}
###### Proposition

If $A \hookrightarrow X$ is a [[nLab:topological subspace]] inclusion which is _good_ in the sense of def. \ref{GoodPair}, then the $A$-relative singular homology of $X$ coincides with the [[reduced singular homology]], def. \ref{ReducedSingularChainComplex}, of the [[quotient space]] $X/A$:

$$
  H_n(X/A)
  \simeq
  \tilde H_n(X , A)
 \,.
$$

=--

The proof of this is spelled out at _[Relative homology -- relation to quotient topological spaces](relative%20homology#RelationToQuotientTopologicalSpaces)_. It needs the proof of the _[Excision property](http://ncatlab.org/nlab/show/relative%20homology#Excision)_ of relative homology. While important, here we will not further dwell on this. The interested reader can find more information behind the above links.




### Cellular homology

With the general definition of relative homology in hand, we now consider the basic _cells_ such that _[[nLab:cell complexes]]_ built from such cells have tractable relative homology groups. Actually, up to [[nLab:weak homotopy equivalence]], _every_ [[nLab:Hausdorff topological space]] is given by such a [[nLab:cell complex]] and hence its relative homology, then called _[[nLab:cellular homology]]_, is a good tool for computing singular homology rather generally.

+-- {: .num_defn }
###### Definition

For $n \in \mathbb{N}$ write

* $D^n \hookrightarrow \mathbb{R}^n \in $ [[nLab:Top]] for the standard $n$-[[nLab:disk]];

* $S^{n-1} \hookrightarrow \mathbb{R}^{n} \in $ [[nLab:Top]] for the standard $(n-1)$-[[nLab:sphere]];

  (notice that the 0-sphere is the disjoint union of _two points_, $S^0 = * \coprod *$, and by definition the $(-1)$-sphere is the [[nLab:empty set]])


* $S^{-1} \hookrightarrow D^{n}$ for the [[nLab:continuous function]] that includes the $(n-1)$-sphere as the [[nLab:boundary]] of the $n$-disk.

=--


+-- {: .num_example }
###### Example

The [[nLab:reduced singular homology]] of the $n$-[[nLab:sphere]] $S^{n}$  equals the $S^{n-1}$-relative homology of the $n$-[[nLab:disk]] with respect to the canonical [[nLab:boundary]] inclusion $S^{n-1} \hookrightarrow D^n$: for all $n \in \mathbb{N}$

$$
  \tilde H_\bullet(S^n) \simeq H_\bullet(D^n, S^{n-1})
 \,.
$$

=--

+-- {: .proof}
###### Proof

The $n$-[[nLab:sphere]] is [[nLab:homeomorphism|homeomorphic]] to the $n$-[[nLab:disk]] with its entire [[nLab:boundary]] identified with a point:

$$
  S^n \simeq D^n/S^{n-1}
  \,.
$$

Moreover the boundary inclusion is a _good pair_ in the sense of def. \ref{GoodPair}. Therefore the example follows with prop. \ref{HomologyOfQuotientSpace}.

=--


When forming [[nLab:cell complexes]] from disks, then each relative dimension will be a [[nLab:wedge sum]] of disks:


+-- {: .num_defn #WedgeSum}
###### Definition

For $\{x_i \colon * \to X_i\}_i$ a [[nLab:set]] of [[nLab:pointed topological spaces]], their _[[nLab:wedge sum]]_ $\vee_i X_i$ is the result of identifying all base points in their [[nLab:disjoint union]], hence the quotient

$$
  \left(
   \coprod_i X_i
  \right)/
  \left(
    \coprod_i *
  \right)
  \,.
$$

=--

+-- {: .num_example }
###### Example

The wedge sum of two pointed [[nLab:circles]] is the "figure 8"-topological space.

=--

+-- {: .num_prop #ReducedHomologyRespectsWedgeSum}
###### Proposition

Let $\{* \to X_i\}_i$ be a set of [[nLab:pointed topological spaces]]. Write $\vee_i X_i \in Top$ for their [[nLab:wedge sum]] and write
$\iota_i \colon X_i \to \vee_i X_i$ for the canonical inclusion functions.


Then for each $n \in \mathbb{N}$ the homomorphism

$$
  (\tilde H_n(\iota_i))_i \colon \oplus_i \tilde H_n(X_i) \to \tilde H_n(\vee_i X_i)
$$

is an [[nLab:isomorphism]].

=--


+-- {: .proof}
###### Proof

By prop. \ref{HomologyOfQuotientSpace} the reduced homology of the wedge sum is equivalently the relative homology of the disjoint union of spaces relative to their disjoint union of basepoints

$$
  \tilde H_n(\vee_i X_i)
  \simeq
  H_n(\coprod_i X_i, \coprod_i *)
  \,.
$$

The relative homology preserves these coproducts (sends them to [[nLab:direct sums]]) and so

$$
  H_n(\coprod_i X_i, \coprod_i *)
  \simeq
  \oplus_i H_n(X_i, *)
  \,.
$$

=--

The following defines topological spaces which are inductively built by gluing disks to each other.

+-- {: .num_defn #CWComplex}
###### Definition

A **[[nLab:CW complex]] of [[nLab:dimension]] $(-1)$** is the [[nLab:empty set|empty]] [[nLab:topological space]].

By [[nLab:induction]], for $n \in \mathbb{N}$ a **[[nLab:CW complex]] of [[nLab:dimension]] $n$** is a [[nLab:topological space]] $X_{n}$ obtained from

1. a $CW$-complex $X_{n-1}$ of dimension $n-1$;

1. an index set $Cell(X)_n \in Set$;

1. a set of [[nLab:continuous maps]] (the **attaching maps**) $\{ f_i \colon S^{n-1} \to X_{n-1}\}_{i \in Cell(X)_n}$

as the [[nLab:pushout]]

$$
  X_n
   \simeq
  \left(
    \coprod_{j \in Cell(X)_n} D^n
  \right)
   \underset{j \in Cell(X)_n S^{n-1}}{\coprod}
   X_n
$$

in

$$
  \array{
    \coprod_{j \in Cell(X)_{n}} S^{n-1} &\stackrel{(f_j)}{\to}& X_{n-1}
    \\
    \downarrow && \downarrow
    \\
    \coprod_{j \in Cell(X)_{n}} D^{n} &\to& X_{n}
  }
  \,,
$$

hence as the topological space obtained from $X_{n-1}$ by gluing in $n$-disks $D^n$ for each $j \in Cell(X)_n$ along the given boundary inclusion $f_j \colon S^{n-1} \to X_{n-1}$.

By this construction, an $n$-dimensional CW-complex is canonically a _[[nLab:filtered topological space]]_, hence a sequence of [[nLab:topological subspace]] inclusions of the form

$$
  \emptyset \hookrightarrow X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X_{n-1} \hookrightarrow X_n
$$

which are the right vertical morphisms in the above pushout diagrams.

A general **[[nLab:CW complex]]** $X$ then is a [[nLab:topological space]] which is the limiting space of a possibly infinite such sequence, hence a topological space given as the [[nLab:sequential colimit]] over a [[nLab:tower]] [[nLab:diagram]] each of whose morphisms is such a filter inclusion

$$
  \emptyset \hookrightarrow X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X
  \,.
$$

=--

The following basic facts about the [[nLab:singular homology]] of [[nLab:CW complexes]] are important.



Now we can state a variant of singular homology adapted to CW complexes which admits a more systematic way of computing its homology groups. First we observe the following.

+-- {: .num_prop #SkeletalRelativeSingularHomologyOfCW}
###### Proposition

The [[nLab:relative singular homology]], def. \ref{RelativeSingularHomology}, of the filtering degrees of a [[nLab:CW complex]] $X$, def. \ref{CWComplex}, is

$$
  H_n(X_k , X_{k-1})
  \simeq
  \left\{
    \array{
       \mathbb{Z}[Cells(X)_n] & if\; k = n
       \\
       0 & otherwise
    }
  \right.
  \,,
$$

where $\mathbb{Z}[Cells(X)_n]$ denotes the [[nLab:free abelian group]] on the set of $n$-cells.


=--

+-- {: .proof}
###### Proof

The inclusion $X_{k-1} \hookrightarrow X_k$ is a _good pair_ in the sense of def. \ref{GoodPair}. The quotient $X_k/X_{k-1}$ is by definition of CW-complexes a [[nLab:wedge sum]], def. \ref{WedgeSum}, of $k$-[[nLab:spheres]], one for each element in $Cell(X)_k$. Therefore by prop. \ref{HomologyOfQuotientSpace} we have an isomorphism $H_n(X_k , X_{k-1}) \simeq \tilde H_n( X_k / X_{k-1})$ with the [[nLab:reduced homology]] of this wedge sum. The statement then follows by the respect of reduced homology for wedge sums, prop. \ref{ReducedHomologyRespectsWedgeSum}.

=--

+-- {: .num_prop #SingularHomologyOfCWComples}
###### Proposition

For $X$ a [[nLab:CW complex]] with skeletal filtration $\{X_n\}_n$ as above, and with $k,n \in \mathbb{N}$ we have for the [[nLab:singular homology]] of $X$ that

$$
  (k \gt n) \Rightarrow (H_k(X_n) \simeq 0)
  \,.
$$

In particular if $X$ is a CW-complex of finite [[nLab:dimension]] $dim X$ (the maximum degree of cells), then

$$
  (k \gt dim X) \Rightarrow (H_k(X) \simeq 0).
$$

Moreover, for $k \lt n$ the inclusion

$$
  H_k(X_n) \stackrel{\simeq}{\to} H_k(X)
$$

is an [[nLab:isomorphism]] and for $k = n$ we have an isomorphism

$$
  image(H_n(X_n) \to H_n(X)) \simeq H_n(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the [[nLab:long exact sequence]] in [[nLab:relative homology]], prop. \ref{RelativeHomologyLongExactSequence} we have an [[nLab:exact sequence]] of the form

$$
  H_{k+1}(X_n , X_{n-1})
  \to
  H_k(X_{n-1})
  \to
  H_k(X_n)
  \to
  H_k(X_n, X_{n-1})
  \,.
$$

Now by prop. \ref{SkeletalRelativeSingularHomologyOfCW} the leftmost and rightmost homology groups here vanish when $k \neq n$ and $k \neq n-1$ and hence exactness implies that

$$
  H_k(X_{n-1})
  \stackrel{\simeq}{\to}
  H_k(X_n)
$$

is an [[nLab:isomorphism]] for $k \neq n,n-1$. This implies the first claims by [[nLab:induction]] on $n$.

Finally for the last claim use that the above exact sequence gives

$$
  H_{n-1+1}(X_n , X_{n-1})
  \to
  H_{n-1}(X_{n-1})
  \to
  H_{n-1}(X_n)
  \to
  0
$$

and hence that with the above the map $H_{n-1}(X_{n-1}) \to H_{n-1}(X)$ is surjective.

=--

We may now discuss the _[[cellular homology]]_ of a [[CW complex]].

+-- {: .num_defn #CellularChainComplex}
###### Definition

For $X$ a [[nLab:CW-complex]], def. \ref{CWComplex}, its
**cellular chain complex** $H_\bullet^{CW}(X) \in Ch_\bullet$ is the [[nLab:chain complex]] such that for $n \in \mathbb{N}$

* the [[nLab:abelian group]] of [[nLab:chains]] is the [[nLab:relative singular homology]] group, def. \ref{RelativeSingularHomology}, of $X_n \hookrightarrow X$ relative to $X_{n-1} \hookrightarrow X$:

  $$
    H_n^{CW}(X) \coloneqq H_n(X_n, X_{n-1})
    \,,
  $$

* {#DifferentialInCellularHomology} the [[nLab:differential]] $\partial^{CW}_{n+1} \colon H_{n+1}^{CW}(X) \to H_n^{CW}(X)$ is the [[nLab:composition]]

  $$
    \partial^{CW}_n
    \colon
    H_{n+1}(X_{n+1}, X_n)
     \stackrel{\partial_n}{\to}
    H_n(X_n)
     \stackrel{i_n}{\to}
    H_n(X_n, X_{n-1})
    \,,
  $$

  where $\partial_n$ is the [[nLab:boundary]] map of the [[nLab:singular chain complex]] and where $i_n$ is the morphism on [[nLab:relative homology]] induced from the canonical inclusion of pairs $(X_n, \emptyset) \to (X_n, X_{n-1})$.

=--

+-- {: .num_prop}
###### Proposition

The composition $\partial^{CW}_{n} \circ \partial^{CW}_{n+1}$ of two differentials in def. \ref{CellularChainComplex} is indeed zero, hence $H^{CW}_\bullet(X)$ is indeed a [[nLab:chain complex]].

=--

+-- {: .proof}
###### Proof

On representative singular [[nLab:chains]] the morphism $i_n$ acts as the identity and hence $\partial^{CW}_{n} \circ \partial^{CW}_{n+1}$ acts as the double singular boundary, $\partial_{n} \circ \partial_{n+1} = 0$.

=--

+-- {: .num_remark}
###### Remark

This means that

* a **cellular $n$-chain** is a singular $n$-chain required to sit in filtering degree $n$, hence in $X_n \hookrightarrow X$;

* a **cellular $n$-cycle** is a singular $n$-chain whose singular boundary is not necessarily 0, but is contained in filtering degree $(n-2)$, hence in $X_{n-2} \hookrightarrow X$.

* a **cellular $n$-boundary** is a singular $n$-chain which is the boundary of a singular $(n+1)$-chain coming from filtering degree $(n+1)$.

=--

This kind of situation -- chains that are cycles only up to lower filtering degree and boundaries that come from specified higher filtering degree -- has an evident generalization to higher relative filtering degrees. And in this greater generality the concept is of great practical relevance. Therefore before discussing cellular homology further now, we consider this more general "higher-order relative homology" that it suggests (namely the formalism of [[nLab:spectral sequences]]). After establishing a few fundamental facts about that we will come back in prop. \ref{SpectralSequenceOfCWComplex} below to analyse the above cellular situation using this conceptual tool.

In theorem \ref{CelluarEquivalentToSingularFromSpectralSequence} we conclude that cellular homology and singular homology agree of [[CW-complexes]] agres.

First we abstract the structure on chain complexes that in the above example was induced by the CW-complex structure on the [[singular chain complex]].





### Filtered chain complexes

+-- {: .num_defn #FilteredChainComplex}
###### Definition

The structure of a **[[filtered chain complex]]** in a [[chain complex]] $C_\bullet$ is a sequence of [[chain map]] inclusions

$$
  \cdots
  \hookrightarrow
  F_{p-1}C_\bullet \hookrightarrow F_p C_\bullet \hookrightarrow
  \cdots
  \hookrightarrow
  C_\bullet
  \,.
$$

The **[[associated graded]] complex** of a filtered chain complex, denoted $G_\bullet C_\bullet$, is the collection of [[quotient]] chain complexes

$$
  G_p C_\bullet \coloneqq F_p C_\bullet / F_{p-1} C_\bullet
  \,.
$$

We say that element of $G_p C_\bullet$ are _in filtering degree_ $p$.

=--

+-- {: .num_remark}
###### Remark

In more detail this means that

1. $[\cdots \stackrel{\partial_{n}}{\to} C_n \stackrel{\partial_{n-1}}{\to} C_{n-1} \to \cdots]$ is a [[chain complex]], hence $\{C_n\}$ are [[objects]] in $\mathcal{A}$ ($R$-[[nLab:modules]]) and $\{\partial_n\}$ are [[nLab:morphisms]] (module [[nLab:homomorphisms]]) with $\partial_{n+1} \circ \partial_{n} = 0$;

1. For each $n \in \mathbb{Z}$ there is a [[nLab:filtered object|filtering]] $F_\bullet C_n$ on $C_n$ and all these filterings are compatible with the [[nLab:differentials]] in that

   $$
     \partial(F_p C_n) \subset F_p C_{n-1}
   $$

1. The grading associated to the filtering is such that the $p$-graded elements are those in the [[nLab:quotient]]

   $$
     G_p C_n \coloneqq \frac{F_p C_n}{ F_{p-1} C_n}
     \,.
   $$

   Since the differentials respect the grading we have chain complexes $G_p C_\bullet$ in each filtering degree $p$.

=--

Hence elements in a filtered chain complex are **[[nLab:bigraded object|bi-graded]]**: they carry a degree as elements of $C_\bullet$ as usual, but now they also carry a filtering degree: for $p,q \in \mathbb{Z}$ we therefore also write

$$
  C_{p,q} \coloneqq F_p C_{p+q}
$$

and call this the collection of **$(p,q)$-chains** in the filtered chain complex.

Accordingly we have $(p,q)$-cycles and -boundaries. But for these we may furthermore refine to a notion where also the filtering degree of the boundaries is constrained:


+-- {: .num_defn #AlmostChainsCyclesBoundaries}
###### Definition

Let $F_\bullet C_\bullet$ be a [[nLab:filtered chain complex]].  Its [[nLab:associated graded]] chain complex is the set of chain complexes

$$
  G_p C_\bullet \coloneqq F_p C_\bullet / F_{p-1} C_\bullet
$$

for all $p$.

Then for $r, p, q \in \mathbb{Z}$ we say that

1. $G_p C_{p+q}$ is the module of ***$(p,q)$-[[nLab:chains]]*** or of ***$(p+q)$-chains in filtering degree $p$***;

1. the module

   $$
     \begin{aligned} Z^r_{p,q}  & \coloneqq \left\{ c \in G_p C_{p+q} | \partial c = 0 \, mod F_{p-r} C_{\bullet} \right\} \\ & =  \left\{ c \in F_p C_{p+q} | \partial(c) \in F_{p-r} C_{p+q-1} \right\}/ F_{p-1}C_{p+q} \end{aligned}
   $$

   is the module of ***$r$-almost $(p,q)$-[[nLab:cycles]]*** (the $(p+q)$-chains whose differential vanishes modulo terms of filtering degree $p-r$);


1. $B^{r}_{p,q} \coloneqq \partial(F_{p+r-1} C_{p+q+1}) \,,$

   is the module of **$r$-almost $(p,q)$-[[nLab:boundaries]]**.

=--

Similarly we set

$$
  Z^\infty_{p,q} \coloneqq \{c \in F_p C_{p + q} | \partial c = 0 \}/F_{p-1}C_{p+q}
  =
  Z(G_p C_{p+q})
$$

$$
  B^\infty_{p,q} \coloneqq \partial( F_p C_{p+q+1} )
  \,.
$$

From this definition we immediately have that the differentials $\partial \colon C_{p+q} \to C_{p+q-1}$ restrict to the $r$-almost cycles as follows:

+-- {: .num_prop #DifferentialsOnAlmostChains}
###### Proposition

The [[nLab:differentials]] of $C_\bullet$ restrict on $r$-almost cycles to homomorphisms of the form

$$
  \partial^r
   \colon
  Z^r_{p,q}
  \to
  Z^r_{p-r, q+r-1}
  \,.
$$

These are still [[nLab:differentials]]: $\partial^2 = 0$.

=--


+-- {: .proof}
###### Proof

By the very definition of $Z^r_{p,q}$ it consists of elements in filtering degree $p$ on which $\partial$ decreases the filtering degree to $p-r$. Also by definition of differential on a chain complex, $\partial$ decreases the actual degree $p+q$ by one. This explains that $\partial$ restricted to $Z^r_{p,q}$ lands in $Z^\bullet_{p-r,q+r-1}$.
Now the image constists indeed of actual boundaries, not just $r$-almost boundaries. But since actual boundaries are in particular $r$-almost boundaries, we may take the [[nLab:codomain]] to be $Z^r_{p-r,q+r-1}$.

=--

As before, we will in general index these differentials by their [[nLab:codomain]] and hence write in more detail

$$
  \partial^r_{p,q}
   \colon
  Z^r_{p,q}
  \to
  Z^r_{p-r, q+r-1}
  \,.
$$


+-- {: .num_prop }
###### Proposition

We have a sequence of canonical inclusions

$$
  B^0_{p,q}
  \hookrightarrow
  B^1_{p,q}
  \hookrightarrow
  \cdots
  B^\infty_{p,q}
  \hookrightarrow
  Z^\infty_{p,q}
  \hookrightarrow
  \cdots
  \hookrightarrow
  Z^1_{p,q}
  \hookrightarrow
  Z^0_{p,q}
  \,.
$$

=--

The following observation is elementary, and yet this is what drives the theory of [[nLab:spectral sequences]], as it shows that almost cycles may be computed iteratively by homological means themselves.

+-- {: .num_prop #KernelsInsideAlmostCycles}
###### Proposition

The $(r+1)$-almost cycles are the $\partial^r$-[[nLab:kernel]] inside the $r$-almost cycles:

$$
  Z^{r+1}_{p,q}
  \simeq
  ker( Z^r_{p,q} \stackrel{\partial^r}{\to} Z^r_{p-r, q+r-1} )
  \,.
$$

=--


+-- {: .proof}
###### Proof

An element $c \in F_p C_{p+q}$ represents

1. an element in $Z^r_{p,q}$ if $\partial c \in F_{p-r} C_{p+q-1}$

1. an element in $Z^{r+1}_{p,q}$ if even $\partial c \in F_{p-r-1} C_{p+q-1} \hookrightarrow F_{p-r} C_{p+q-1}$.

The second condition is equivalent to $\partial c$ representing the 0-element in the quotient $F_{p-r}C_{p+q-1}/ F_{p-r-1}C_{p+q-1}$. But this is in turn equivalent to $\partial c$ being 0 in $Z^r_{p-r,q+r-1} \subset F_{p-r} C_{p+q-1} / F_{p-r-1} C_{p+q-1}$.

=--

With a definition of almost-cycles and almost-boundaries, of course we are now interested in the corresponding homology groups:

+-- {: .num_defn #ExplicitForm}
###### Definition

For $r, p, q \in \mathbb{Z}$ define the **$r$-almost $(p,q)$-[[nLab:chain homology]]** of the filtered complex to be the [[nLab:quotient]] of the $r$-almost $(p,q)$-cycles by the $r$-almost $(p,q)$-boundaries, def. \ref{AlmostChainsCyclesBoundaries}:

$$
  \begin{aligned}
    E^r_{p,q}
    & \coloneqq
    \frac{Z^r_{p,q}}{B^r_{p,q}}
    \\
    & =
  \frac{
    \left\{
     x \in F_p C_{p+q} \,|\, \partial x \in F_{p-r} C_{p+q-1}
    \right\}
  }
  {
    \partial( F_{p+r-1} C_{p+q+1} ) \oplus F_{p-1} C_{p+q}
  }
  \end{aligned}
$$

By prop. \ref{DifferentialsOnAlmostChains} the differentials of $C_\bullet$ restrict on the $r$-almost homology groups to maps

$$
  \partial^r : E^r_{p,q} \to E^r_{p-r, q+r - 1}
  \,.
$$


=--

The central property of these $r$-almost homology groups now is their following iterative homological characterization.


+-- {: .num_prop #ExplicitDefIsIndeedSpectralSequ}
###### Proposition

With definition \ref{ExplicitForm} we have that
$E^{r+1}_{\bullet, \bullet}$ is the $\partial^r$-[[nLab:chain homology]] of $E^r_{\bullet, \bullet}$:

$$
  E^{r+1}_{p,q}
  =
 \frac{
    ker(\partial^r : E^r_{p,q} \to E^r_{p-r, q+r-1})
  }{
    im( \partial^r : E^r_{p+r, q-r+1} \to E^r_{p,q} )
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{KernelsInsideAlmostCycles}.

=--

This structure on the collection of $r$-almost cycles of a filtered chain complex thus obtained is called a _[[nLab:spectral sequence]]_:

+-- {: .num_defn #SpectralSequence}
###### Definition

A **homology spectral sequence** of $R$-[[nLab:modules]] is

1. a set $\{E_{p,q}^r\}_{p,q,r \in \mathbb{Z}}$ of $R$-modules;

1. a set $\{ \partial^r_{p,q} \colon E_{p,q}^{r} \to E^r_{p-r, q+r-1} \}_{r,p,q \in \mathbb{Z}}$ of [[nLab:homomorphisms]]

such that

1. the $\partial^r$s are [[nLab:differentials]]: $\forall_{p,q,r}  (\partial^r_{p-r,q+r-1} \circ \partial^r_{p,q} = 0)$;

1. the modules $E^{r+1}_{p,q}$ are the $\partial^r$-[[nLab:homology]] of the modules in relative degree $r$:

   $$
     \forall_{r,p,q}
     \left(
       E^{r+1}_{p,q} \simeq \frac{ker(\partial^r_{p-r,q+r-1})}{im(\partial^r_{p, q})}
      \right)
     \,.
   $$

One says that $E^r_{\bullet,\bullet}$ is the **$r$-page** of the spectral sequence.

=--

Since this turns out to be a useful structure to make explicit, as the above motivation should already indicate, one introduces the following terminology and basic facts to talk about spectral sequences.


+-- {: .num_defn #LimitTerm}
###### Definition

Let $\{E^r_{p,q}\}_{r,p,q}$ be a [[nLab:spectral sequence]], def. \ref{SpectralSequence}, such that for each $p,q$ there is $r(p,q)$ such that for all $r \geq r(p,q)$ we have

$$
  E^{r \geq r(p,q)}_{p,q} \simeq E^{r(p,q)}_{p,q}
  \,.
$$

Then one says that

1. the [[nLab:bigraded object]]

   $$
     E^\infty
      \coloneqq
     \{E^\infty_{p,q}\}_{p,q} \coloneqq \{ E^{r(p,q)}_{p,q} \}_{p,q}
   $$

   is the **limit term** of the spectral sequence;

*  the spectral sequence **abuts** to $E^\infty$.

=--

+-- {: .num_example #Degeneration}
###### Example

If for a spectral sequence there is $r_s$ such that all [[nLab:differentials]] on pages after $r_s$ vanish, $\partial^{r \geq r_s} = 0$, then $\{E^{r_s}\}_{p,q}$ is a limit term for the spectral sequence. One says in this cases that the spectral sequence **degenerates** at $r_s$.

=--

+-- {: .proof}
###### Proof

By the defining relation

$$
  E^{r+1}_{p,q} \simeq ker(\partial^r_{p-r,q+r-1})/im(\partial^r_{p,q}) = E^r_{pq}
$$

the spectral sequence becomes constant in $r$ from $r_s$ on if all the differentials vanish, so that $ker(\partial^r_{p,q}) = E^r_{p,q}$ for all $p,q$.

=--


+-- {: .num_example #Collaps}
###### Example

If for a [[nLab:spectral sequence]] $\{E^r_{p,q}\}_{r,p,q}$ there is $r_s \geq 2$ such that the $r_s$th page is concentrated in a single row or a single column, then the spectral sequence degenerates on this pages, example \ref{Degeneration}, hence this page is a limit term, def. \ref{LimitTerm}. One says in this case that the spectral sequence **collapses** on this page.

=--

+-- {: .proof}
###### Proof

For $r \geq 2$ the [[nLab:differentials]] of the spectral sequence

$$
  \partial^r \colon E^r_{p,q} \to E^r_{p-r, q+r-1}
$$

have [[nLab:domain]] and [[nLab:codomain]] necessarily in different rows an columns (while for $r = 1$ both are in the same row and for $r = 0$ both coincide). Therefore if all but one row or column vanish, then all these differentials vanish.

=--


+-- {: .num_defn #Convergence}
###### Definition

A [[nLab:spectral sequence]] $\{E^r_{p,q}\}_{r,p,q}$ is said to **converge** to a [[nLab:graded object]] $H_\bullet$ with [[nLab:filtered chain complex|filtering]] $F_\bullet H_\bullet$, traditionally denoted

$$
  E^r_{p,q} \Rightarrow H_\bullet
  \,,
$$

if the [[nLab:associated graded]] complex $\{G_p H_{p+q}\}_{p,q} \coloneqq \{F_p H_{p+q} / F_{p-1} H_{p+q}\}$ of $H$ is the limit term of $E$, def. \ref{LimitTerm}:

$$
  E^\infty_{p,q} \simeq G_p H_{p+q} \;\;\;\;\;\;\; \forall_{p,q}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

In practice spectral sequences are often referred to via their first non-trivial page, often also the page at which it collapses, def. \ref{Collaps}, often already the second page. Then one tends to use notation such as

$$
  E^2_{p,q} \Rightarrow H_\bullet
$$

to be read as "There is a spectral sequence whose second page is as shown on the left and which converges to a filtered object as shown on the right."

=--

+-- {: .num_defn #BoundedSpectralSequence}
###### Definition

A spectral sequence $\{E^r_{p,q}\}$ is called a **bounded spectral sequence** if for all $n,r \in \mathbb{Z}$ the number of non-vanishing terms of total degree $n$, hence of the form $E^r_{k,n-k}$, is finite.

=--

+-- {: .num_defn #QuadrantSpectralSequence}
###### Definition

A [[nLab:spectral sequence]] $\{E^r_{p,q}\}$ is called

* a **first quadrant spectral sequence** if all terms except possibly for $p,q \geq 0$ vanish;

* a **third quadrant spectral sequence** if all terms except possibly for $p,q \leq 0$ vanish.

Such spectral sequences are bounded, def. \ref{BoundedSpectralSequence}.

=--



+-- {: .num_prop #BoundedSpectralSequenceHasLimitTerm}
###### Proposition

A bounded spectral sequence, def. \ref{BoundedSpectralSequence}, has a limit term, def. \ref{LimitTerm}.

=--

+-- {: .proof}
###### Proof

First notice that if a spectral sequence has at most $N$ non-vanishing terms of total degree $n$ on page $r$, then all the following pages have at most at these positions non-vanishing terms, too, since these are the homologies of the previous terms.

Therefore for a bounded spectral sequence for each $n$ there is $L(n) \in \mathbb{Z}$ such that $E^r_{p,n-p} = 0$ for all $p \leq L(n)$ and all $r$. Similarly there is $T(n) \in \mathbb{Z}$ such $E^r_{n-q,q} = 0$ for all $q \leq T(n)$ and all $r$.

We claim then that the limit term of the bounded spectral sequence is in position $(p,q)$ given by the value $E^r_{p,q}$ for

$$
  r \gt max(  p-L(p+q-1), q + 1 - L(p+q+1) )
  \,.
$$

This is because for such $r$ we have

1. $E^r_{p-r, q+r-1} = 0$ because $p-r \lt L(p+q-1)$, and hence the [[nLab:kernel]] $ker(\partial^r_{p-r,q+r-1}) = 0$ vanishes;

1. $E^r_{p+r, q-r+1} = 0$ because $q-r + 1 \lt T(p+q+1)$, and hence the [[nLab:image]] $im(\partial^r_{p,q}) = 0$ vanishes.

Therefore

$$
  \begin{aligned}
    E^{r+1}_{p,q}
    &=
    ker(\partial^r_{p-r,q+r-1})/im(\partial^r_{p,q})
    \\
    & \simeq E^r_{p,q}/0
    \\
    & \simeq E^r_{p,q}
  \end{aligned}
  \,.
$$

=--

The central statement about the notion of the spectral sequence of a filtered chain complex then is the following proposition. It says that the iterative computation of higher order relative homology indeed in the limit computes the genuine homology.

+-- {: .num_defn #FilteringOnHomology}
###### Definition

For $F_\bullet C_\bullet$ a [[nLab:filtered complex]], write for $p \in \mathbb{Z}$

$$
  F_p H_\bullet(C)
   \coloneqq
  image( H_\bullet(F_p C) \to H_\bullet(C) )
  \,.
$$

This defines a [[nLab:filtered object|filtering]] $F_\bullet H_\bullet(C)$ of the homology, regarded as a graded object.

=--


+-- {: .num_prop #ConvergingToGenuineHomology}
###### Proposition

If the [[spectral sequence of a filtered complex]] $F_\bullet C_\bullet$ of prop. \ref{ExplicitDefIsIndeedSpectralSequ} has a limit term, def. \ref{LimitTerm} then it converges, def. \ref{Convergence}, to the chain homology of $C_\bullet$

$$
  E^r_{p,q} \Rightarrow H_{p+q}(C_\bullet)
  \,,
$$

i.e. for sufficiently large $r$ we have

$$
  E^r_{p,q} \simeq G_p H_{p+q}(C)
  \,,
$$

where on the right we have the [[nLab:associated graded object]] of the filtering of def. \ref{FilteringOnHomology}.

=--

+-- {: .proof}
###### Proof

By assumption, there is for each $p,q$ an $r(p,q)$ such that for all $r \geq r(p,q)$ the $r$-almost cycles and $r$-almost boundaries, def. \ref{AlmostChainsCyclesBoundaries}, in $F_p C_{p+q}$ are the ordinary [[nLab:cycles]] and [[nLab:boundaries]]. Therefore for $r \geq r(p,q)$ def. \ref{ExplicitForm} gives $E^r_{p,q} \simeq G_p H_{p+q}(C)$.


=--

This says what these spectral sequences are converging to. For computations it is also important to know how they start out for low $r$. We can generally characterize $E^r_{p,q}$ for very low values of $r$ simply as follows:

+-- {: .num_prop #SpectralSequencePagesForLowr}
###### Proposition

We have

* $E^0_{p,q} = G_p C_{p+q} = F_p C_{p+q} / F_{p-1} C_{p+q}$

  is the [[nLab:associated graded|associated p-graded]] piece of $C_{p+q}$;

* $E^1_{p,q} = H_{p+q}(G_p C_\bullet)$

=--

+-- {: .proof}
###### Proof

For $r = 0$ def. \ref{ExplicitForm} restricts to

$$
  E^0_{p,q} = \frac{ F_p C_{p+q}}{F_{p-1} C_{p+q}} = G_p C_{p+q}
$$

because for $c \in F_p C_{p+q}$ we automatically also have $\partial c \in F_p C_{p+q}$ since the differential respects the filtering degree by assumption.

For $r = 1$ def. \ref{ExplicitForm} gives

$$
  E^1_{p,q} = \frac{\{c \in G_p C_{p+q} | \partial c = 0 \in G_p C_{p+q}\} }{\partial(F_p C_{p+q})} = H_{p+q} (G_p C_\bullet)
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

There is, in general, a decisive difference between the homology of the associated graded complex $H_{p+q}(G_p C_\bullet)$ and the associated graded piece of the genuine homology $G_p H_{p+q}(C_\bullet)$: in the former the differentials of cycles are required to vanish only up to terms in lower degree, but in the latter they are required to vanish genuinely. The latter expression is instead the value of the spectral sequence for $r \to \infty$, see prop. \ref{ConvergingToGenuineHomology} below.

=--





### Comparing cellular and singular homology

These general facts now allow us, as a first simple example for the application of [[nLab:spectral sequences]] to see transparently that the [[cellular homology]] of a CW complex, def. \ref{CellularChainComplex}, coincides with its genuine [[singular homology]].

First notice that of course the structure of a [[nLab:CW-complex]] on a [[nLab:topological space]] $X$, def. \ref{CWComplex} naturally induces on its [[nLab:singular simplicial complex]] $C_\bullet(X)$ the structure of a [[nLab:filtered chain complex]], def. \ref{FilteredChainComplex}:


+-- {: .num_defn #SpectralSequenceOfSingularChainsInCWComplex}
###### Definition

For $X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X$ a
[[nLab:CW complex]], and $p \in \mathbb{N}$, write

$$
  F_p C_\bullet(X) \coloneqq C_\bullet(X_p)
$$

for the [[nLab:singular chain complex]] of $X_p \hookrightarrow X$. The given  [[nLab:topological subspace]] inclusions $X_p \hookrightarrow X_{p+1}$ induce [[nLab:chain map]] inclusions $F_p C_\bullet(X) \hookrightarrow F_{p+1} C_\bullet(X)$ and these equip the singular chain complex $C_\bullet(X)$ of $X$ with the structure of a bounded [[nLab:filtered chain complex]]

$$
  0
  \hookrightarrow
  F_0 C_\bullet(X)
  \hookrightarrow
  F_1 C_\bullet(X)
  \hookrightarrow
  F_2 C_\bullet(X)
  \hookrightarrow
  \cdots
  \hookrightarrow
  F_\infty C_\bullet(X)
  \coloneqq
  C_\bullet(X)
  \,.
$$

(If $X$ is of finite [[nLab:dimension]] $dim X$ then this is a bounded filtration.)

Write $\{E^r_{p,q}(X)\}$ for the [[nLab:spectral sequence of a filtered complex]] corresponding to this filtering.

=--

+-- {: .num_prop #SpectralSequenceOfCWComplex}
###### Proposition

The spectral sequence $\{E^r_{p,q}(X)\}$ of singular chains in a [[nLab:CW complex]] $X$, def. \ref{SpectralSequenceOfSingularChainsInCWComplex} converges, def. \ref{Convergence}, to the [[nLab:singular homology]] of $X$:

$$
  E^r_{p,q}(X) \Rightarrow H_\bullet(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The spectral sequence $\{E^r_{p,q}(X)\}$ is clearly a first-quadrant spectral sequence, def. \ref{QuadrantSpectralSequence}. Therefore it is a bounded spectral sequence, def. \ref{BoundedSpectralSequence} and hence has a limit term, def. \ref{BoundedSpectralSequenceHasLimitTerm}. So the statement follows with prop. \ref{ConvergingToGenuineHomology}.

=--


We now identify the low-degree pages of $\{E^r_{p,q}(X)\}$ with structures in singular homology theory.

+-- {: .num_prop #PagesInTheSpectralSequenceOfTheFilteredSingularComplex}
###### Proposition

* $r = 0$ -- $E^0_{p,q}(X) \simeq C_{p+q}(X_p)/C_{p+q}(X_{p-1})$ is the group of $X_{p-1}$-[[nLab:relative homology|relative (p+q)-chains]], def. \ref{RelativeSingularHomology}, in $X_p$;

* $r = 1$ -- $E^1_{p,q}(X) \simeq H_{p+q}(X_p, X_{p-1})$ is the $X_{p-1}$-[[nLab:relative singular homology]], def. \ref{RelativeSingularHomology}, of $X_p$;

* $r = 2$ -- $E^2_{p,q}(X) \simeq \left\{ \array{ H_p^{CW}(X) & for\; q = 0 \\ 0 & otherwise }  \right.$

* $r = \infty$ -- $E^\infty_{p,q}(X) \simeq F_p H_{p+q}(X) / F_{p-1} H_{p+q}(X) $.

=--

+-- {: .proof}
###### Proof

By straightforward and immediate analysis of the definitions.

=--

As a result of these general considerations we now obtain the promised isomorphism between the cellular homology and the singular homology of a CW-complex $X$:

+-- {: .num_theorem #CelluarEquivalentToSingularFromSpectralSequence}
###### Theorem

For $X \in $ [[Top]] a [[CW complex]], def. \ref{CWComplex}, its [[cellular homology]], def. \ref{CellularChainComplex} $H^{CW}_\bullet(X)$ coincides with its [[singular homology]] $H_\bullet(X)$:

$$
  H^{CW}_\bullet(X) \simeq H_\bullet(X)
 \,.
$$

=--

+-- {: .proof}
###### Proof

By the third item of prop. \ref{PagesInTheSpectralSequenceOfTheFilteredSingularComplex} the $(r = 2)$-page of the spectral sequence $\{E^r_{p,q}(X)\}$ is concentrated in the $(q = 0)$-row and hence it collapses there, def. \ref{Collaps}. Accordingly we have

$$
  E^\infty_{p,q}(X) \simeq E^2_{p,q}(X)
$$

for all $p,q$. By the third and fourth item of prop. \ref{PagesInTheSpectralSequenceOfTheFilteredSingularComplex} this non-trivial only for $q = 0$ and there it is equivalently

$$
  G_p H_{p}(X) \simeq H^{CW}_p(X)
  \,.
$$

Finally observe that $G_p H_p(X) \simeq H_p(X)$ by the definition of the filtering on the homology, def. \ref{FilteringOnHomology}, and using prop. \ref{SingularHomologyOfCWComples}.


=--





## For filtered spectra
 {#SpectralSequencesForFilteredSpectra}

+-- {: .num_defn #FilteredSpectrum}
###### Definition

A [[filtered spectrum]] is a [[spectrum]] $X$ equipped with a sequence $X_\bullet \colon (\mathbb{N}, \gt) \longrightarrow Spectra$  of spectra of the form

$$
  \cdots
   \longrightarrow
  X_3
    \stackrel{f_2}{\longrightarrow}
  X_2
    \stackrel{f_1}{\longrightarrow}
  X_1 \stackrel{f_0}{\longrightarrow} X_0 = X
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

More generally a [[filtered object in an (infinity,1)-category|filtering]] on an object $X$ in (stable or not) [[homotopy theory]] is a $\mathbb{Z}$-graded sequence $X_\bullet $ such that $X$ is the [[homotopy colimit]]  $X\simeq \underset{\longrightarrow}{\lim} X_\bullet$. But for the present purpose we stick with the simpler special case of def. \ref{FilteredSpectrum}.

=--


+-- {: .num_remark}
###### Remark

There is _no_ condition on the [[morphisms]] in def. \ref{FilteredSpectrum}. In particular, they are _not_ required to be [[n-monomorphisms]] or [[n-epimorphisms]] for any $n$.

On the other hand, while they are also not explicitly required to have a presentation by [[cofibrations]] or [[fibrations]], this follows automatically: by the existence of [[model structures for spectra]], every filtering on a spectrum is equivalent to one in which all morphisms are represented by [[cofibrations]] or by [[fibrations]].

This means that we may think of a filtration on a spectrum $X$ in the sense of def. \ref{FilteredSpectrum} as equivalently being a [[tower of fibrations]] over $X$.

=--

The following remark \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum} unravels the structure encoded in a filtration on a spectrum, and motivates the concepts of [[exact couples]] and their [[spectral sequences]] from these.


+-- {: .num_remark #UnrolledExactCoupleOfAFiltrationOnASpectrum}
###### Remark

Given a [[filtered spectrum]] as in def. \ref{FilteredSpectrum},
write $A_k$ for the [[homotopy cofiber]] of its $k$th stage, such as to obtain the diagram

$$
  \array{
   \cdots
     &\stackrel{}{\longrightarrow}&
   X_3
     &\stackrel{f_2}{\longrightarrow}&
   X_2
     &\stackrel{f_2}{\longrightarrow} &
   X_1
     &\stackrel{f_1}{\longrightarrow}&
   X
   \\
   && \downarrow && \downarrow && \downarrow && \downarrow
   \\
   && A_3 && A_2 && A_1 && A_0
  }
$$

where each stage

$$
 \array{
   X_{k+1} &\stackrel{f_k}{\longrightarrow}& X_k
   \\
   && \downarrow^{\mathrlap{cofib(f_k)}}
   \\
   && A_k
 }
$$

is a [[homotopy fiber sequence]].

To break this down into invariants, apply the [[stable homotopy groups]]-[[functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+1#StableHomotopyGroups)). This yields a diagram of $\mathbb{Z}$-[[graded abelian groups]] of the form

$$
  \array{
   \cdots
     &\stackrel{}{\longrightarrow}&
   \pi_\bullet(X_3)
     &\stackrel{\pi_\bullet(f_2)}{\longrightarrow}&
   \pi_\bullet(X_2)
     &\stackrel{\pi_\bullet(f_2)}{\longrightarrow} &
   \pi_\bullet(X_1)
     &\stackrel{\pi_\bullet(f_1)}{\longrightarrow}&
   \pi_\bullet(X_0)
   \\
   && \downarrow && \downarrow && \downarrow && \downarrow
   \\
   && \pi_\bullet(A_3) && \pi_\bullet(A_2) && \pi_\bullet(A_1) && \pi_\bullet(A_0)
  }
  \,.
$$

Each hook at stage $k$ extends to a [[long exact sequence of homotopy groups]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1#HomotopyCofiberSequencesAreHomotopyFiberSequencesInSpectra)) via [[connecting homomorphisms]] $\delta_\bullet^k$

$$
  \cdots
    \to
  \pi_{\bullet+1}(A_k)
    \stackrel{\delta_{\bullet+1}^k}{\longrightarrow}
  \pi_\bullet(X_{k+1})
    \stackrel{\pi_\bullet(f_k)}{\longrightarrow}
  \pi_\bullet(X_k)
    \stackrel{}{\longrightarrow}
  \pi_\bullet(A_k)
   \stackrel{\delta_\bullet^k}{\longrightarrow}
  \pi_{\bullet-1}(X_{k+1})
  \to
  \cdots
  \,.
$$

If we understand the [[connecting homomorphism]]

$$
  \delta_k \colon \pi_\bullet(A_k) \longrightarrow \pi_\bullet(X_{k+1})
$$

as a morphism of degree -1, then all this information fits into one diagram of the form

$$
  \array{
   \cdots
     &\stackrel{}{\longrightarrow}&
   \pi_\bullet(X_3)
     &\stackrel{\pi_\bullet(f_2)}{\longrightarrow}&
   \pi_\bullet(X_2)
     &\stackrel{\pi_\bullet(f_2)}{\longrightarrow} &
   \pi_\bullet(X_1)
     &\stackrel{\pi_\bullet(f_1)}{\longrightarrow}&
   \pi_\bullet(X_0)
   \\
   &&
   \downarrow &{}_{\mathllap{\delta_2}}\nwarrow &
   \downarrow &{}_{\mathllap{\delta_1}}\nwarrow &
   \downarrow &{}_{\mathllap{\delta_0}}\nwarrow
   & \downarrow
   \\
   && \pi_\bullet(A_3) && \pi_\bullet(A_2) && \pi_\bullet(A_1) && \pi_\bullet(A_0)
  }
  \,,
$$

where each triangle is a rolled-up incarnation of a [[long exact sequence of homotopy groups]] (and in particular is _not_ a commuting diagram!).

If we furthermore consider the [[bigraded object|bigraded]] [[abelian groups]] $\pi_\bullet(X_\bullet)$ and $\pi_\bullet(A_\bullet)$, then this information may further be rolled-up to a single diagram of the form

$$
  \array{
     \pi_\bullet(X_\bullet)
       & \stackrel{\pi_\bullet(f_\bullet)}{\longrightarrow} &
     \pi_\bullet(X_\bullet)
     \\
       & {}_{\mathllap{\delta}}\nwarrow
       & \downarrow^{\mathrlap{\pi_\bullet(cofib(f_\bullet))}}
     \\
     &&
     \pi_\bullet(A_\bullet)
  }
$$

where the morphisms $\pi_\bullet(f_\bullet)$, $\pi_\bullet(cofib(f_\bullet))$ and $\delta$ have bi-degree $(0,-1)$, $(0,0)$ and $(-1,1)$, respectively.

Here it is convenient to shift the bigrading, equivalently, by setting

$$
  \mathcal{D}^{s,t} \coloneqq \pi_{t-s}(X_s)
$$

$$
  \mathcal{E}^{s,t} \coloneqq \pi_{t-s}(A_s)
  \,,
$$

because then $t$ counts the cycles of going around the triangles:

$$
  \cdots
   \to
  \mathcal{D}^{s+1,t+1}
    \stackrel{\pi_{t-s}(f_s)}{\longrightarrow}
  \mathcal{D}^{s,t}
    \stackrel{\pi_{t-s}(cofib(f_s))}{\longrightarrow}
  \mathcal{E}^{s,t}
    \stackrel{\delta_s}{\longrightarrow}
  \mathcal{D}^{s+1,t}
    \to
  \cdots
$$

Data of this form is called an _[[exact couple]]_, def. \ref{ExactCouple} below.


=--


+-- {: .num_defn #UnrolledExactCouple}
###### Definition

An _unrolled [[exact couple]]_ (of Adams-type) is a diagram of [[abelian groups]] of the form

$$
  \array{
     \cdots
       &\stackrel{}{\longrightarrow}&
     \mathcal{D}^{3,\bullet}
       &\stackrel{i_2}{\longrightarrow}&
     \mathcal{D}^{2,\bullet}
       &\stackrel{i_1}{\longrightarrow} &
     \mathcal{D}^{1,\bullet}
       &\stackrel{i_0}{\longrightarrow}&
     \mathcal{D}^{0,\bullet}
     \\
     &&
     \downarrow^{\mathrlap{}}  &{}_{\mathllap{k_2}}\nwarrow &
     {}^{\mathllap{j_2}}\downarrow &{}_{\mathllap{k_1}}\nwarrow &
     {}^{\mathllap{j_1}}\downarrow &{}_{\mathllap{k_0}}\nwarrow
     & {}_{\mathllap{j_0}}\downarrow
     \\
     && \mathcal{E}^{3,\bullet} && \mathcal{E}^{2,\bullet}
     && \mathcal{E}^{1,\bullet} && \mathcal{E}^{0,\bullet}
   }
$$

such that each triangle is a rolled-up [[long exact sequence]] of [[abelian groups]] of the form

$$
  \cdots
   \to
  \mathcal{D}^{s+1,t+1}
    \stackrel{i_s}{\longrightarrow}
  \mathcal{D}^{s,t}
    \stackrel{j_s}{\longrightarrow}
  \mathcal{E}^{s,t}
    \stackrel{k_s}{\longrightarrow}
  \mathcal{D}^{s+1,t}
    \to
  \cdots
  \,.
$$


=--

The collection of this "un-rolled" data into a single diagram of [[abelian groups]] is called the corresponding _[[exact couple]]_.


+-- {: .num_defn #ExactCouple}
###### Definition

An _[[exact couple]]_ is a [[diagram]] (non-commuting) of [[abelian groups]] of the form

$$
  \array{
    \mathcal{D}
    &\stackrel{i}{\longrightarrow}&
    \mathcal{D}
    \\
    & {}_{\mathllap{k}}\nwarrow & \downarrow^{\mathrlap{j}}
    \\
    && \mathcal{E}
  }
  \,,
$$

such that this is [[exact sequence]] exact in each position, hence such that the [[kernel]] of every [[morphism]] is the [[image]] of the preceding one.

=--


The concept of exact couple so far just collects the sequences of long exact sequences given by a filtration. Next we turn to extracting information from this sequence of sequences.

+-- {: .num_remark #Observingd1}
###### Remark

The sequence of long exact sequences in remark \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum} is inter-locking, in that every $\pi_{t-s}(X_s)$ appears in _two_ of them, and thus we can string them all together:

$$
  \array{
    && & \searrow && \nearrow
    \\
    && && \pi_{t-s-1}(X_{s+1})
    \\
    && & {}^{\mathllap{\delta_{t-s}^s}}\nearrow
    && \searrow^{\mathrlap{\pi_{t-s-1}(cofib(f_{s+1}))}}
    && && && \nearrow
    \\
    && \pi_{t-s}(A_s) && \underset{def: \;\;d_1^{s,t}}{\longrightarrow} && \pi_{t-s-1}(A_{s+1})
    && \stackrel{def: \; d_1^{s+1,t}}{\longrightarrow} && \pi_{t-s-2}(A_{s+2})
    \\
    & \nearrow && && && {}_{\mathllap{\delta_{t-s-1}^{s+1}}}\searrow
    && \nearrow_{\mathrlap{\pi_{t-s-2}(cofib(f_{s+2}))}}
    \\
    && && && && \pi_{t-s-2}(X_{s+2})
    \\
    && && && & \nearrow && \searrow
  }
$$

This gives rise to the horizontal composites $d_1^{s,t}$, as show above, and by the fact that the diagonal sequences are long exact, these are differentials: $d_1^2 = 0$, hence give a [[chain complex]]:

$$
  \array{
    \cdots & \stackrel{}{\longrightarrow}
    && \pi_{t-s}(A_s) && \overset{d_1^{s,t}}{\longrightarrow} && \pi_{t-s-1}(A_{s+1})
    && \stackrel{d_1^{s+1,t}}{\longrightarrow} && \pi_{t-s-2}(A_{s+2})
    &&\longrightarrow & \cdots
  }
  \,.
$$

We read off from the interlocking long exact sequences what these differentials _mean_: an element $c \in \pi_{t-s}(A_s)$ lifts to an element $\hat c \in \pi_{t-s-1}(X_{s+2})$ precisely if $d_1 c = 0$:

$$
  \array{
    &\hat c \in & \pi_{t-s-1}(X_{s+2})
    \\
    && & \searrow^{\mathrlap{\pi_{t-s-1}(f_{s+1})}}
    \\
    && && \pi_{t-s-1}(X_{s+1})
    \\
    && & {}^{\mathllap{\delta_{t-s}^s}}\nearrow
    && \searrow^{\mathrlap{\pi_{t-s-1}(cofib(f_{s+1}))}}
    \\
    & c \in  & \pi_{t-s}(A_s) && \underset{d_1^{s,t}}{\longrightarrow} && \pi_{t-s-1}(A_{s+1})
  }
$$

This means that the [[cochain cohomology]] of the complex $(\pi_{\bullet}(A_\bullet), d_1)$ produces elements of $\pi_\bullet(X_\bullet)$ and hence of $\pi_\bullet(X)$.

In order to organize this observation, notice that in terms of the exact couple of remark \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum}, the differential

$$
  d_1^{s,t}  \;\coloneqq \; \pi_{t-s-1}(cofib(f_{s+1})) \circ \delta_{t-s}^s
$$

is a component of the composite

$$
  d \coloneqq j \circ k
  \,.
$$


=--

Some terminology:

+-- {: .num_defn #PageOfAnExactCouple}
###### Definition

Given an exact couple, def. \ref{ExactCouple},

$$
  \array{
    \mathcal{D}^{\bullet,\bullet}
    &\stackrel{i}{\longrightarrow}&
    \mathcal{D}^{\bullet,\bullet}
    \\
    & {}_{\mathllap{k}}\nwarrow & \downarrow^{\mathrlap{j}}
    \\
    && \mathcal{E}^{\bullet,\bullet}
  }
$$

its _page_ is the [[chain complex]]

$$
  (E^{\bullet,\bullet}, d \coloneqq j \circ  k)
  \,.
$$

=--

+-- {: .num_defn #DerivedExactCouple}
###### Definition

Given an exact couple, def. \ref{ExactCouple}, then the induced _derived exact couple_ is the diagram

$$
  \array{
    \widetilde {\mathcal{D}}
    &\stackrel{\tilde i}{\longrightarrow}&
    \widetilde {\mathcal{D}}
    \\
    & {}_{\mathllap{\tilde k}}\nwarrow & \downarrow^{\mathrlap{\tilde j}}
    \\
    && \widetilde{\mathcal{E}}
  }
$$

with

1. $\tilde{\mathcal{E}} \coloneqq ker(d)/im(d)$;

1. $\tilde {\mathcal{D}} \coloneqq im(i)$;

1. $\tilde i \coloneqq i|_{im(i)}$;

1. $\tilde j \coloneqq j \circ i^{-1}$;

1. $\tilde k \coloneqq k|_{ker(d)}$.


=--

+-- {: .num_prop #DerivedExactCoupleIsExactCouple}
###### Proposition

A derived exact couple, def. \ref{DerivedExactCouple},
is again an exact couple, def. \ref{ExactCouple}.

=--

+-- {: .num_defn}
###### Definition

Given an exact couple, def. \ref{ExactCouple},
then the induced [[spectral sequence]], def. \ref{SpectralSequence}, is the sequence of pages, def. \ref{PageOfAnExactCouple}, of the induced sequence of derived exact couples, def. \ref{DerivedExactCouple}, prop. \ref{DerivedExactCoupleIsExactCouple}.

=--


+-- {: .num_example #AdamsTypeSpectralSequenceOfATower}
###### Example

Consider a [[filtered spectrum]], def. \ref{FilteredSpectrum},

$$
  \array{
   \cdots
     &\stackrel{}{\longrightarrow}&
   X_3
     &\stackrel{f_2}{\longrightarrow}&
   X_2
     &\stackrel{f_2}{\longrightarrow} &
   X_1
     &\stackrel{f_1}{\longrightarrow}&
   X
   \\
   && \downarrow && \downarrow && \downarrow && \downarrow
   \\
   && A_3 && A_2 && A_1 && A_0
  }
$$

and its induced [[exact couple]] of [[stable homotopy groups]], from remark \ref{UnrolledExactCoupleOfAFiltrationOnASpectrum}

$$
  \array{
    \mathcal{D} &\stackrel{i}{\longrightarrow}& \mathcal{D}
    \\
    &{}_{\mathllap{k}}\nwarrow& \downarrow^{\mathrlap{j}}
    \\
    && \mathcal{E}
  }
  \;\;\;\;\;\,\;\;\;\;\;\;
  \array{
    \mathcal{D} &\stackrel{(-1,-1)}{\longrightarrow}& \mathcal{D}
    \\
    &{}_{\mathllap{(1,0)}}\nwarrow& \downarrow^{\mathrlap{(0,0)}}
    \\
    && \mathcal{E}
  }
$$

with bigrading as shown on the right.

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/adamstypedifferentials.jpg" width="360" >
</div>

As we pass to derived exact couples, by def. \ref{DerivedExactCouple},
the bidegree of $i$ and $k$ is preserved, but that of $j$ increases by $(1,1)$ in each step, since

$$
  deg(\tilde j) = deg( j \circ i^{-1}) = deg(j) + (1,1)
  \,.
$$


Therefore the induced [[spectral sequence]] has differentials of the form

$$
  d_r \;\colon\; \mathcal{E}_r^{s,t} \longrightarrow \mathcal{E}_r^{s+r, t+r-1}
  \,.
$$

This is also called the Adams-type _[[spectral sequence of a tower of fibrations|spectral sequence of the tower of fibrations]]_ $X_{n+1} \to X_n$.

=--

This we discuss in detail in _[[Introduction to Stable homotopy theory -- 2|part 2 -- Adams spectral sequences]]_.



## References
 {#References}

A gentle exposition of the general idea of spectral sequences is in

* [[John McCleary]], _A User's Guide to Spectral Sequences_, Cambridge University Press (1985, 2001)

A concise account streamlined for our purposes is in section 2 of

* {#Rognes12} [[John Rognes]], _The Adams spectral sequence_ (following [Bruner](classical+Adams+spectral+sequence#Bruner09)), 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

