
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

> This entry is about the notion of (co)skeleta of [[simplicial sets]]. For the notion of skeleton of a [[category]] see at _[[skeleton]]_.

#Contents#
* table of contents
{:toc}




## Definition


For $\Delta$ the [[simplex category]] write $\Delta_{\leq n}$ for its [[full subcategory]] on the objects $[0], [1], \cdots, [n]$. The inclusion $\Delta|_{\leq n} \hookrightarrow \Delta$ induces a truncation functor

$$
  tr_n : sSet = [\Delta^{op}, Set] \to [\Delta_{\leq n}^{op},Set] = sSet_{\leq n}
$$ 

that takes a [[simplicial set]] and restricts it to its degrees $\leq n$.


This functor has a fully faithful [[left adjoint]], given by left [[Kan extension]]

$$
  sk_n 
  \;\colon\; 
  sSet_{\leq n} \to sSet
$$

called the $n$-**skeleton**

and a fully faithful [[right adjoint]], given by right [[Kan extension]]

$$
  cosk_n 
  \;\colon\; 
  sSet_{\leq n} \to sSet
$$

called the $n$-**coskeleton**.

$$
  ( sk_n \dashv tr_n \dashv cosk_n) \;\;
   \colon
   \;\;
   sSet_{\leq n}
   \stackrel{\overset{sk_n}{\longrightarrow}}{\stackrel{\overset{tr_n}{\longleftarrow}}{\underset{cosk_n}{\longrightarrow}}}
   sSet
  \,.
$$


The $n$-skeleton produces a simplicial set that is freely filled with degenerate simplices above degree $n$. Conversely, the $n$-coskeleton produces a simplicial set having a simplex of degree $m \gt n$ whenever there is a compatible family of $m$-faces.


Write

$$
  \mathbf{sk}_n := sk_n \circ tr_n: sSet \to sSet
$$

and

$$
  \mathbf{cosk}_n := cosk_n \circ tr_n: sSet \to sSet
$$

for the composite functors. Often by slight abuse of notation we suppress the boldface and just write $sk_n : sSet \to sSet$ and $cosk_n : sSet \to sSet$.

these in turn form an [[adjunction]]

$$
  ( \mathbf{sk}_n \dashv \mathbf{cosk}_n)
  \;\;
  :
  \;\;
  sSet
  \stackrel{\leftarrow}{\to}
  sSet
  \,.
$$

So the $k$-coskeleton of a simplicial set $X$ is given by the formula

$$
  \mathbf{cosk}_k X : [n] \mapsto Hom_{sSet}(\mathbf{sk}_k \Delta[n], X)
  \,.
$$


Simplicial sets isomorphic to objects in the image of $cosk_n$ are called **$n$-coskeletal** simplicial sets.


## Properties {#Properties}

### General

+-- {: .num_prop}
###### Proposition


For $X \in $ [[sSet]], the following are equivalent:

* $X$ is $n$-coskeletal; 

* on $X$ the [[adjunction unit]] $X \to \mathbf{cosk}_n(X)$ is an [[isomorphism]];

* the map

  $$
    X_k 
    \;=\; 
    Hom(\Delta[k], X) 
     \stackrel{tr_n}{\to} 
    Hom(tr_n(\Delta[k]), tr_n(X))
  $$

  is a [[bijection]] for all $k \gt n$

* for $k \gt n$ and every morphism $\partial\Delta[k] \to X$ from the [[boundary of a simplex|boundary]] of the $k$-[[simplex]] there exists a _unique_ filler $\Delta[k] \to X$

  $$
    \array{
       \partial \Delta[k] &\to& X
       \\
       \downarrow & \nearrow
       \\
       \Delta[k]
    }
  $$

=--

+-- {: .num_remark}
###### Remark

So in particular if $X$ is an $n$-coskeletal [[Kan complex]], all its [[simplicial homotopy group]]s above degree $(n-1)$ are trivial.

=--

### Compatibility with Kan conditions

+-- {: .num_prop #CoskeletonPreservesKanComplexes}
###### Proposition

The coskeleton operations $\mathbf{cosk}_n$ preserve [[Kan complexes]].

More generally, $\mathbf{cosk}_n$ preserves those [[Kan fibrations]] between [[Kan complexes]] whose [[codomains]] have [[trivial group|trivial]] [[homotopy group]] $\pi_n$.

=--

([Dwyer & Kan 1984, p. 141 (4 of 9)](#DwyerKan84), proofs are spelled out by [Low 2013](#Low13), [Deflorin 2019, Lemma 10.12](#Deflorin19))


### Truncation and Postnikov towers {#Truncation}

+-- {: .num_prop}
###### Proposition

For each $n \in \mathbb{N}$, the [[unit of an adjunction|unit of the adjunction]]

$$
  X \longrightarrow \mathbf{cosk}_n(X)
$$

induces an [[isomorphism]] on all [[simplicial homotopy groups]] in degree $\lt n$.

=--


It follows from the above that for $X$ a [[Kan complex]], the sequence

$$
  X = \underset{\leftarrow}{\lim}\, cosk_n X \to \cdots \to cosk_{n+1} X \to cosk_{n} X \to \cdots \to *
$$

is a [[Postnikov tower]] for $X$.

See also the discussion in [Dwyer & Kan 1984, p. 140, 141](#DwyerKan84). 

For the interpretation of this in terms of  [[(n,1)-topos]]es inside the [[(∞,1)-topos]] [[∞Grpd]] see [[n-truncated object in an (∞,1)-category]], example <a href="http://ncatlab.org/nlab/show/n-truncated+object+of+an+(infinity%2C1)-category#InInfGrpd">In ∞Grpd and Top</a>.


## Examples
 {#Examples}

\begin{example}
\label{CoskeletalityOfSimplicialNervesOfCategories}
**(coskeletality of simplicial nerves of categories)**
\linebreak
The [[simplicial nerve]] of a [[category]] (i.e. of a [[1-category]]) is a [[coskeleton|2-coskeletal]] [[simplicial set]] ([this Prop.](nerve#NerveOfACategoryIsTwoCoskeletal)): The unique filler of the [[boundary of a simplex|boundary of an $n \geq 3$-simplex]] encodes the [[associativity]]-condition on [[n-tuple|$n$-tuples]] of composable morphisms.

Of course there is more to a category than its associativity condition, and hence the converse fails: Not every [[coskeleton|2-coskeletal]] [[simplicial set]] is the [[nerve of a category]]. For example the [[boundary of a simplex|boundary of the 2-simplex]], $\partial \Delta^2$, is 2-coskeletal but not the nerve of a category, since it is missing a [[composition]] of the edges $0 \to 1 \to 2$, namely it is missing a filler of this [[inner horn]].

In fact, a [[simplicial set]] is the [[nerve]] of a [[category]] iff it has *unique* [[inner horn|inner $n$-horn]]-fillers for $n \geq 2$ (e.g. [this Prop.](nerve#sSetIsNerveOfCategoryIffAllInnerHornsHaveUniqueFillers)).
But [[coskeleton|2-coskeletality]] already implies that all $k \geq 4$-horns have unique filler (first uniquely fill the missing $k-1$-face then the interior $k$)-cell. Together this implies that:

A [[simplicial set]] is the [[nerve]] of a [[category]] iff

1. it is [[coskeleton|2-coskeletal]],

1. all *[[inner horn|inner]]* 2- and 3-[[horns]] have unique fillers (encoding [[composition]] and [[associativity]]).

Similarly for [[groupoids]] (by [this Prop.](nerve#sSetIsNerveOfGroupoidIffAllHornsHaveUniqueFillers)):

A [[simplicial set]] is the [[nerve]] of a [[groupoid]] iff

1. it is [[coskeleton|2-coskeletal]],

1. all 2- and 3-[[horns]] have unique fillers.

For better or worse, such a simplicial set has at times also been called a *[[1-hypergroupoid]]*, pointing to the fact that this is the first non-trivial stage in a pattern that recognizes $n+1$-coskeletal [[Kan complexes]] with unique horn fillers as models for [[n-groupoids|$n$-groupoids]] 

Notice that a [[Kan complex]] which is [[coskeleton|2-coskeletal]] but with possibly non-unique 2-horn fillers is still a [[homotopy 1-type]] and may still be called a *[[1-groupoid]]* in the sense of [[homotopy theory]], but need not be the [[nerve]] of a [[groupoid]]. It may be thought of as a [[bigroupoid]] (2-[[hypergroupoid]]) which happens to be just a [[homotopy 1-type]].
\end{example}

Accordingly, essentially by definition:

* A [[Kan complex]] that is $(n+1)$-coskeletal is equivalent to (the [[nerve]] of) an [[n-groupoid|$n$-groupoid]].

Also:

* A 0-coskeletal simplicial set $X$ is (-1)-[[truncated]] and hence either empty or a [[contractible]] [[Kan complex]] , $X \stackrel{\simeq}{\to} *$ that is the [[nerve]] $X = N(C)$ of a [[groupoid]] $C$ that has a [[equivalence of categories]] $C \simeq *$.


## Related concepts

* [[Postnikov tower]], [[Whitehead tower]]

* [[Eilenberg subcomplex]]

* [[adjoint modality]]

* [[hypergroupoid]]

## References


* [[Peter May]], Section II.8 of: _Simplicial objects in algebraic topology_, The University of Chicago Press 1967 ([djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu), [ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html))

* {#DwyerKan84} [[William Dwyer]], [[Dan Kan]], Section 1.2 (vi) of: *An obstruction theory for diagrams of simplicial sets*, Indagationes Mathematicae (Proceedings) **87** 2 (1984) 139-146 &lbrack;<a href="https://doi.org/10.1016/1385-7258(84)90015-5">doi:10.1016/1385-7258(84)90015-5</a>&rbrack;

* [[Paul Goerss]], [[J. F. Jardine]], Section VI.3 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999)  Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4))

Also:

* {#Low13} [[Zhen Lin]], [Math.SE:a/597990](http://math.stackexchange.com/a/597990/58526)

* {#Deflorin19} Gian Deflorin, Section 10.2 of: *The Homotopy Hypothesis*, Zurich 2019 ([2019](http://user.math.uzh.ch/cattaneo/deflorin.pdf), [[Deflorin_HomotopyHypothesis.pdf:file]])

The [[level of a topos]]-structure of simplicial (co-)skeleta is discussed in

* {#KRRZ10} C. Kennett, [[Emily Riehl|E. Riehl]], M. Roy, M. Zaks, _Levels in the toposes of simplicial sets and cubical sets_ , JPAA **215** no.5 (2011) pp.949-961. ([arXiv:1003.5944](http://arxiv.org/abs/1003.5944))


[[!redirects coskeletal]]
[[!redirects coskeleton]]
[[!redirects simplicial coskeleton]]

[[!redirects coskeleta]]
[[!redirects skeleta]]

[[!redirects coskeletons]]
[[!redirects skeletons]]

[[!redirects simplicial skeleta]]

[[!redirects n-skeleton]]
[[!redirects n-skeleta]]

[[!redirects cellular skeleton]]
[[!redirects cellular skeleta]]
