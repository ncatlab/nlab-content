
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


# Contents 
* Table of contents 
{: toc}

##Idea

Cellular homology is a very efficient tool for computing the [[ordinary homology|ordinary]] [[homology groups]] of [[topological spaces]] which are [[CW complexes]], based on the [[relative singular homology]] of their [[cell complex]]-decomposition and using [[degree of a continuous function|degree]]-computations.

Hence cellular homology uses the combinatorial structure of a CW-complex to define, first a [[chain complex]] of _celluar chains_ and then the corresponding [[chain homology]]. The resulting _cellular homology_ of a CW-complex is [[isomorphism|isomorphic]] to its [[singular homology]], hence to its [[ordinary homology]] as a topological space, and hence provides an efficient method for computing the latter.

## Definition 

### CW-Complex

For definiteness and to fix notation which we need in the following, we recall the definition of _[[CW-complex]]_. The actual definition of cellular homology is [below](#CellularHomology).

For $n \in \mathbb{N}$ write

* $S^n \in $ [[Top]] for the standard $n$-[[sphere]];

* $D^n \in $ [[Top]] for the standard $n$-[[disk]];

* $S^n \hookrightarrow D^{n+1}$ for the [[continuous function]] that includes the $n$-sphere as the [[boundary]] of the $(n+1)$-disk.

Write furthermore $S^{-1} \coloneqq \emptyset$ for the [[empty set|empty]] topological space and think of $S^{-1} \to D^0 \simeq *$ as the boundary inclusion of the (-1)-sphere into the 0-disk, which is the [[point]].

+-- {: .num_defn #CWComplex} 
###### Definition

A **[[CW complex]] of [[dimension]] $(-1)$** is the [[empty set|empty]] [[topological space]].

By [[induction]], for $n \in \mathbb{N}$ a **[[CW complex]] of [[dimension]] $n$** is a [[topological space]] $X_{n}$ obtained from

1. a $CW$-complex $X_{n-1}$ of dimension $n-1$;

1. an index set $Cell(X)_n \in Set$;

1. a set of [[continuous maps]] (the **attaching maps**) $\{ f_i \colon S^{n-1} \to X_{n-1}\}_{i \in Cell(X)_n}$

as the [[pushout]] $X_n \simeq \coprod_{j \in Cell(X)_n} D^n \coprod_{j \in Cell(X)_n S^{n-1}} X_n$

$$
  \array{
    \coprod_{j \in Cell(X)_{n}} S^{n-1} &\stackrel{(f_j)}{\to}& X_{n-1}
    \\
    \downarrow && \downarrow
    \\
    \coprod_{j \in Cell(X)_{n}} D^{n} &\to& X_{n} 
  }
  \,.
$$ 

By this construction an $n$-dimensional CW-complex is canonical a [[filtered topological space]] with filter inclusion maps

$$
  \emptyset \hookrightarrow X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X_{n-1} \hookrightarrow X_n
$$

the right vertical morphisms in these pushout diagrams. 

A general **[[CW complex]]** $X$ is a [[topological space]] given as the [[sequential colimit]] over a [[tower]] [[diagram]] each of whose morphisms is such a filter inclusion 

$$
  \emptyset \hookrightarrow X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X
  \,.
$$

=--

For the following a CW-complex is all this data: the chosen [[filtered topological space|filtering]] with the chosen attaching maps. 


### Cellular homology
 {#CellularHomology}

We define "[[ordinary homology|ordinary]]" cellular homology with [[coefficients]] in the [[group]] $\mathbb{Z}$ of [[integers]]. The analogous definition for other [[coefficients]] is immediate.


+-- {: .num_defn #CellularChainComplex} 
###### Definition

For $X$ a [[CW-complex]], def. \ref{CWComplex}, its
**cellular chain complex** $H_\bullet^{CW}(X) \in Ch_\bullet$ is the [[chain complex]] such that for $n \in \mathbb{N}$

* the [[abelian group]] of [[chains]] is the [[relative singular homology]] group of $X_n \hookrightarrow X$ relative to $X_{n-1} \hookrightarrow X$:

  $$
    H_n^{CW}(X) \coloneqq H_n(X_n, X_{n-1})
    \,,
  $$

* the [[differential]] $\partial^{CW}_{n+1} \colon H_{n+1}^{CW}(X) \to H_n^{CW}(X)$ is the [[composition]]

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

  where $\partial_n$ is the [[boundary]] map of the [[singular chain complex]] and where $i_n$ is the morphism on [[relative homology]] induced from the canonical inclusion of pairs $(X_n, \emptyset) \to (X_n, X_{n-1})$. 

=--

+-- {: .num_prop} 
###### Proposition 

The composition $\partial^{CW}_{n} \circ \partial^{CW}_{n+1}$ of two differentials in def. \ref{CellularChainComplex} is indeed zero, hence $H^{CW}_\bullet(X)$ is indeed a [[chain complex]].

=-- 

+-- {: .proof}
###### Proof

On representative singular [[chains]] the morphism $i_n$ acts as the identity and hence $\partial^{CW}_{n} \circ \partial^{CW}_{n+1}$ acts as the double singular boundary, $\partial_{n} \circ \partial_{n+1} = 0$.

=--

+-- {: .num_remark} 
###### Remark

By the discussion at _[Relative homology - Relation to reduced homology of quotient spaces](relative%20homology#RelationToQuotientTopologicalSpaces)_ the relative homology group $H_n(X_n, X_{n-1})$ is isomorphic to the the [[reduced homology]] $\tilde H_n(X_n/X_{n-1})$ of $X_n/X_{n-1}$.

This implies in particular that 

* a **cellular $n$-chain** is a singular $n$-chain required to sit in filtering degree $n$, hence in $X_n \hookrightarrow X$;

* a **cellular $n$-cycle** is a singular $n$-chain whose singular boundary is not necessarily 0, but is contained in filtering degree $(n-2)$, hence in $X_{n-2} \hookrightarrow X$.

=--

## Properties

### Cellular chains

+-- {: .num_prop} 
###### Proposition 

For every $n \in \mathbb{N}$ we have an [[isomorphism]]

$$
  H^{CW}_n(X)
  \coloneqq
  H_n(X_n, X_{n-1}) 
  \simeq
  \mathbb{Z}(Cell(X)_n)
$$

that the group of cellular $n$-chains with the [[free abelian group]] whose set of [[basis]] elements is the set of $n$-[[disks]] attached to $X_{n-1}$ to yield $X_n$. 

=-- 

This is discussed at _[Relative homology - Homology of CW-complexes](relative%20homology#RelativeHomologyOfCWComplexes)_.


+-- {: .num_remark} 
###### Remark

Thus, each cellular differential $\partial^{CW}_n$ can be described as a [[matrix]] $M$ with [[integer]] entries $M_{i j}$. Here an index $j$ refers to the attaching map $f_j \colon S^n \to X_n$ for the $j^{th}$ disk $D^{n+1}$. The integer entry $M_{i j}$ corresponds to a map 

$$\mathbb{Z} \cong H_{n+1}(D^{n+1}, S^n) \to H_n(S^n) \to H_n(D^n, S^{n-1}) \cong H_n(S^n) \cong \mathbb{Z}$$ 

and is computed as the [[degree of a continuous function]]

$$S^n \stackrel{f_j}{\to} X_n \to X_n/(X_n - D^n) \cong D^n/S^{n-1} \cong S^n$$ 

where the inclusion $X_n - D^n \hookrightarrow X_n$ corresponds to the attaching map for the $i^{th}$ disk $D^n$. 

=--

### Relation to singular homology

+-- {: .num_theorem} 
###### Theorem 

For $X$ a [[CW-complex]], its cellular homology $H^{CW}_\bullet(X)$ agrees with its [[singular homology]] $H_\bullet(X)$:

$$
  H^{CW}_\bullet(X)
  \simeq
  H_\bullet(X)
  \,.
$$

=-- 

This appears for instance as ([Hatcher, theorem 2.35](#Hatcher)). A proof is below as the proof of cor. \ref{CelluarEquivalentToSingularFromSpectralSequence}.

### Relation to the spectral sequence of the filtered singular complex
 {#RelationToSpectralSequenceOfFilteredSingularComplex}

The structure of a [[CW-complex]] on a [[topological space]] $X$, def. \ref{CWComplex} naturally induces on its [[singular simplicial complex]] $C_\bullet(X)$ the structure of a [[filtered chain complex]]:


+-- {: .num_defn } 
###### Definition

For $X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X$ a [[CW complex]], and $p \in \mathbb{N}$, write

$$
  F_p C_\bullet(X) \coloneqq C_\bullet(X_p)
$$

for the [[singular chain complex]] of $X_p \hookrightarrow X$. The given  [[topological subspace]] inclusions $X_p \hookrightarrow X_{p+1}$ induce [[chain map]] inclusions $F_p C_\bullet(X) \hookrightarrow F_{p+1} C_\bullet(X)$ and these equip the singular chain complex $C_\bullet(X)$ of $X$ with the structure of a bounded [[filtered chain complex]]

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

(If $X$ is of finite [[dimension]] $dim X$ then this is a bounded filtration.)

Write $\{E^r_{p,q}(X)\}$ for the [[spectral sequence of a filtered complex]] corresponding to this filtering.

=--

We identify various of the pages of this spectral sequences with structures in singular homology theory.

+-- {: .num_prop #PagesInTheSpectralSequenceOfTheFilteredSingularComplex} 
###### Proposition

* $r = 0$ -- $E^0_{p,q}(X) \simeq C_{p+q}(X_p)/C_{p+q}(X_{p-1})$ is the group of $X_{p-1}$-[[relative homology|relative (p+q)-chains]] in $X_p$;

* $r = 1$ -- $E^1_{p,q}(X) \simeq H_{p+q}(X_p, X_{p-1})$ is the $X_{p-1}$-[[relative singular homology]] of $X_p$;

* $r = 2$ -- $E^2_{p,q}(X) \simeq \left\{ \array{ H_p^{CW}(X) & for\; q = 0 \\ 0 & otherwise }  \right.$

* $r = \infty$ -- $E^\infty_{p,q}(X) \simeq F_p H_{p+q}(X) / F_{p-1} H_{p+q}(X) $.

=--

+-- {: .proof}
###### Proof

(...)

=--

This now directly implies the isomorphism between the cellular homology and the singular homology of a CW-complex $X$:

+-- {: .num_cor #CelluarEquivalentToSingularFromSpectralSequence} 
###### Corollary

$$ 
  H^{CW}_\bullet(X) \simeq H_\bullet(X)
$$

=--

+-- {: .proof}
###### Proof

By the third item of prop. \ref{PagesInTheSpectralSequenceOfTheFilteredSingularComplex} the $(r = 2)$-page of the spectral sequence $\{E^r_{p,q}(X)\}$ is concentrated in the $(q = 0)$-row. This implies that all [[differentials]] for $r \gt 2$ vanish, since their domain and codomain groups necessarily have different values of $q$. Accordingly we have 

$$
  E^\infty_{p,q}(X) \simeq E^2_{p,q}(X)
$$

for all $p,q$. By the third and fourth item of prop. \ref{PagesInTheSpectralSequenceOfTheFilteredSingularComplex} this is equivalently

$$
  G_p H_{p}(X) \simeq H^{CW}_p(X)
  \,.
$$

Finally observe that $G_p H_p(X) \simeq H_p(X)$ by the definition of the filtering on the homology as $F_p H_p(X) \coloneq image(H_p(X_p) \to H_p(X))$ and by standard properties of singular homology of [[CW complexes]] discusses at _[CW complex -- singular homology](CW+complex#SingularHomology)_.


## Software

There are convenient software implementations for large-scale computations of cellular homology: one may use [LinBox](http://www.linalg.org), [CHomP](http://chomp.rutgers.edu) or [Perseus](http://www.sas.upenn.edu/~vnanda/perseus).
=--


## Related concepts

* [[ordinary homology]]

* [[singular homology]], [[Čech homology]]



## References


[[!include cohomology -- early references]]




### General

A standard textbook account is from p. 139 on in 

*  [[Allen Hatcher]], _[Algebraic topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_, Cambridge Univ. Press 2002, 

Lecture notes include

* Lisa Jeffrey, _Homology of CW-complexes and Cellular homology_ ([pdf](http://www.math.toronto.edu/~mat1300/oldnotes/cellular-homology.pdf))

Formulation in [[homotopy type theory]]:

* [[Ulrik Buchholtz]], [[Favonia|Kuen-Bang Hou (Favonia)]], _[[Cellular Cohomology in Homotopy Type Theory]]_, Logical Methods in Computer Science, **16** 2 (2020) ([arXiv:1802.02191](https://arxiv.org/abs/1802.02191), [lmcs:6518](https://lmcs.episciences.org/6518)) 

* [[Axel Ljungström]]: *More cellular (co)homology in HoTT*, [talk at](CQTS#LjungströmApr2024) *[Running HoTT 2024](CQTS#RunningHoTT2024)*, [[CQTS]]@NYUAD (April 2024) &lbrack;video: [kt](https://cdnapisec.kaltura.com/html5/html5lib/v2.73.2/mwEmbedFrame.php/p/1674401/uiconf_id/23435151/entry_id/1_r5x4tca9?wid=_1674401&iframeembed=true&playerId=kaltura_player&entry_id=1_r5x4tca9)&rbrack;



[[!redirects cellular chain complex]]

[[!redirects cellular cohomology]]

[[!redirects cellular cochain complex]]


[[!redirects cellular]]

