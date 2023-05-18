
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

The concept of _pushout product_ is a natural kind of pairing operation on [[morphisms]] in [[categories]] equipped with a pairing operation on [[objects]] (e.g. a [[tensor product]]) and having [[pushouts]]. It sends two morphisms to the universal morphism out of the [[pushout]] of the [[span]]-diagram they form by pairing their [[domain]] objects. Regarding arrows in a category as diagrams with domain the [[interval category]], and giving the interval category the natural monoidal product, this is a kind of [[Day convolution]] [[tensor product]] with the natural [[copower|copowering]] over [[Set]] replacing a tensor in the [[end|coend]].


## Definition
 {#Definition}

Consider

* three [[categories]] $\mathcal{E}_i$, $i \in \{1,2,3\}$
 
  (often taken to be the same),

* a [[functor]]  $\otimes \colon \mathcal{E}_1 \times \mathcal{E}_2 \to \mathcal{E}_3$ out of the [[product category]] 

  (often being the [[tensor product]] on a [[monoidal category]] or the [[tensoring]] of an [[enriched category]] over its [[cosmos]]). 

Assume that $\mathcal{E}_3$ has all [[pushouts]].

+-- {: .num_defn}
###### Definition

Given a [[pair]] of [[morphisms]] 

* $f \colon A \to B$ in $\mathcal{E}_1$ 

* $g \colon X \to Y$ in $\mathcal{E}_2$, 

their **pushout product** is the [[morphism]] in $\mathcal{E}_3$

$$
  f \Box g 
  \;\;\colon\;\;
  A \otimes Y 
    \overset
      {A \otimes X}
      {\amalg} 
  B \otimes X
  \longrightarrow
  B \otimes Y
$$

out of the [[pushout]] of the two morphisms, which is induced by the [[universal property]] of the pushout by the following [[commuting diagram]] (induced, in turn, from the [[functor|functoriality]] of the [[tensor product]] as a functor on a [[product category]]):

$$
  \array{
    A \otimes X 
    &\overset{f \otimes id_X}{\longrightarrow}& 
    B \otimes X
    \\
    \mathllap{{}^{id_A \otimes g}}\Big\downarrow 
    && 
    \Big\downarrow\mathrlap{{}^{id_B \otimes g}}
    \\
    A \otimes Y 
    &\underset{f \otimes id_Y}{\longrightarrow}& 
    B \otimes Y
    \mathrlap{\,.}
  }
$$

\begin{tikzcd}[
 row sep=40pt,
 column sep=20pt
]
  A \otimes X 
  \ar[rr, "{ f \otimes \mathrm{id}_X }"{description}]
  \ar[dd, "{ \mathrm{id}_A \otimes g }"{description}]
  \ar[dr, phantom, "{ \scalebox{.6}{(po)} }"{pos=.8}]
  && 
  B \otimes X
  \ar[dd, "{ \mathrm{id}_B \otimes g }"{description}]
  \ar[dl]
  \\
  &   
  A \otimes Y 
    \overset
      {A \otimes X}
      {\sqcup} 
  B \otimes X
  \ar[dr, dashed, "{ f \,\Box\, g }"{sloped, description}]
  \\
  A \otimes Y
  \ar[rr, "{ f \otimes \mathrm{id}_Y }"{description}]
  \ar[ur]
  &&
  B \otimes Y
\end{tikzcd}


=--

## Properties
 {#Properties}

For $\mathcal{C}$ any [[category]] and $K\subset Mor(\mathcal{C})$ any [[class]] of its morphisms, write $K Inj$ for the $K$-[[injective morphisms]] and $K Cof \coloneqq  (K Inj)Proj$ for the $K Inj$-[[projective morphisms]]. 

+-- {: .num_prop #PushoutProductOfCofClassIsCofClassOfPushoutProduct}
###### Proposition

Let $\mathcal{C}$ be a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] with [[finite limits]] and [[finite colimits]], and let $I_1, I_2\subset Mor(\mathcal{C})$ be two [[classes]] of its morphisms. 

Then under [[pushout product]] $\Box$:

$$
  (I_1 Cof) \Box (I_2 Cof)
  \subset 
  (I_1 \Box I_2) Cof
  \,.
$$

=--

([Hovey-Shipley-Smith 00](#HoveyShipleySmith00))

+-- {: .proof}
###### Proof

By a little [[Joyal-Tierney calculus]].

=--

\begin{remark}\label{PushoutProductAxiomInCofibrantlyGeneratedModelCategories}
In the context of [[monoidal model category]] theory, prop. \ref{PushoutProductOfCofClassIsCofClassOfPushoutProduct} implies that for checking the [[pushout-product axiom]] in the case of [[cofibrantly generated model categories]] it is sufficient to check it on [[generating cofibrations]].
\end{remark}


## Examples
 {#Examples}

\begin{example}\label{InjectionsOfSets}
**(Cartesian pushout-products of sets)**
\linebreak
  Pushout-products of monomorphisms ([[injections]]) in [[Set]], with respect to the [[Cartesian product]]

$$
  \times 
    \;\colon\; 
  Set \times Set 
    \longrightarrow 
  Set
$$

are again injections. The following graphics illustrates this for [[interval]]-subsets of the [[plane]]:

<img src="/nlab/files/PushoutProductOfInjections-230425.jpg" width="300">

Generally, given a [[pair]] of [[maps]] of [[sets]] consider their [[epi-mono factorization]] through their [[images]]

$$
  \array{
    f 
      \,\colon\, 
    X 
      &\overset{\phantom{---}}{\twoheadrightarrow}& 
    im(f) 
      &\overset{\phantom{---}}{\hookrightarrow}& 
    X'
    \\
    g 
      \,\colon\, 
    Y 
      &\overset{\phantom{---}}{\twoheadrightarrow}& 
    im(g)
      &\overset{\phantom{---}}{\hookrightarrow}& 
    Y'
  }
$$





\end{example}

+-- {: .num_example #PushoutProductOfSpheresInclusionsIntoDisks}
###### Example

For $n \in \mathbb{N}$, let

$$
  i_n \;\colon\; S^{n-1}\hookrightarrow D^n
$$

be the canonical [[sphere]] inclusions in [[Top]] (the generating cofibrations of the [[classical model structure on topological spaces]]). Their pushout product (with respect to [[Cartesian product]] of topological spaces) is given by addition of indices:

$$
  i_{n_1} \Box i_{n_2} \simeq i_{n_1 + n_2}
  \,.
$$

Let moreover

$$
  j_n \coloneqq (id,\delta_0) \;\colon\; D^n \hookrightarrow D^n \times I
  \,.
$$

Then 

$$
  i_{n_1}\Box j_{n_2} \simeq j_{n_1 + n_2}
  \,.
$$

=--

+-- {: .proof}
###### Proof

To see this, it is profitable to model [[n-disks]] and [[n-spheres]], up to [[homeomorphism]], as n-cubes and their boundaries.

To see the idea of the proof, consider the situation in low dimensions, where one readily sees that

$$
  i_1 \Box i_1
  \;\colon\;
    (\; = \;\cup\; \vert\vert\;) 
    \hookrightarrow
    \Box
$$

and

$$
  i_1 \Box j_0
  \;\colon\;
    (\; = \;\cup\; \vert \; ) 
    \hookrightarrow
    \Box
  \,.
$$

Generally, $D^n$ may be represented as the space of $n$-tuples of elements in $[0,1]$, and $S^n$ as the suspace of tuples for which at least one of the coordinates is equal to 0 or to 1.

Accordingly $S^{n_1} \times D^{n_2} $ is the spaces of $(n_1+n_2)$-tuples, such that one of the first $n_1$ coordinates is equal to 0 or 1, and hence

$$
  S^{n_1} \times D^{n_2} \cup D^{n_1} \times S^{n_2} \simeq S^{n_1 + n_2}
  \,.
$$

And of course it is clear that $D^{n_1} \times D^{n_2} \simeq D^{n_1 + n_2}$. This shows the first case.

For the second, use that $S^{n_1} \times D^{n_2} \times I$ is contractible to $S^{n_1} \times D^{n_2}$ in $D^{n_1} \times D^{n_2} \times I$, and that $S^{n_1} \times D^{n_2}$ is a subspace of $D^{n_1} \times D^{n_2}$.

=--

+-- {: .num_remark}
###### Remark

The relations in example \ref{PushoutProductOfSpheresInclusionsIntoDisks} are the key in proving that the [[classical model structure on topological spaces]] (on [[compactly generated topological spaces]]) is an [[enriched model category]] over itself. See there at _[topological enrichment](classical+model+structure+on+topological+spaces#TopologicalEnrichment)_ for more.

=--



## Related concepts

* [[pullback power]] -- the dual concept

* [[pushout-product axiom]]

* [[Joyal-Tierney calculus]]


## References

Pushout-products are prominently discussed in the context of [[monoidal model category]]-theory (where they appear in a *[[pushout-product axiom]]*), and here a key motivation are constructions of [[symmetric monoidal smash products of spectra]]. See for instance:

* {#HoveyShipleySmith00} [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208 ([arXiv:math/9801077](http://arxiv.org/abs/math/9801077))


[[!redirects pushout product]]
[[!redirects pushout-products]]
[[!redirects pushout products]]