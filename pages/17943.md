
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[topological homotopy theory]], the _fundamental theorem of covering spaces_ says that for a sufficiently well-behaved [[topological space]] $X$, the [[functor]] which sends a [[covering space]] of $X$ to the [[Set]]-[[action]] ([[permutation representation]]) of the [[fundamental groupoid]] of $X$ on the [[fibers]] of $E$ is an [[equivalence of categories]]. 

This is a basic instance of the general principle of [[Galois theory]]. 

It follows in particular that for [[connected topological space|connected]] $X$ then the [[automorphism group]] of the [[universal covering space]] of $X$ coincides with the [[fundamental group]] $\pi_1(X,x)$ itself (for any basepoint $x$). This often yields a convenient means to determine the [[fundamental group]] of $X$ in the first place.

This is closely related to the [[(∞,1)-Grothendieck construction]]; the equivalence $\infty Grpd_{/X} \simeq \infty Grpd^X$ restricts to an equivalence between the subcategories of bundles $Y \to X$ with discrete fibers and of set-valued functors on $X$. Observe in particular that $Set^{\Pi_1(X)} \simeq Set^X$.


## Statement

+-- {: .num_theorem #FundamentalTheoremOfCoveringSpaces}
###### Theorem
**(fundamental theorem of covering spaces)**

Let $X$ be a [[locally path-connected topological space|locally path-connected]] and [[semi-locally simply-connected topological space]]. Then the operations on 

1. extracting the [[monodromy]] $Fib_{E}$ of a [[covering space]] $E$ over $X$

1. [[reconstructing a covering space from monodromy]] $Rec(\rho)$

constitute an [[equivalence of categories]]

$$
  Cov(X)
    \underoverset
      {\underset{Fib}{\longrightarrow}}
      {\overset{Rec}{\longleftarrow}}
      {\simeq}
  Set^{\Pi_1(X)}
$$


between the [[category of covering spaces]], and the category  of [[permutation representation|permutation]] [[groupoid representations]] of the [[fundamental groupoid]] of $X$.

=--

+-- {: .proof}
###### Proof

With the standard definitions of the two functors, both are in fact inverse [[isomorphisms]] of categories instead of just [[equivalences of categories]] (meaning that the required [[natural isomorphisms]] from the composites of the two functors to the [[identity functor]] are componentwise [[equalities]]), which establishes the claim right away. For definiteness, we make this explicit:

Given $\rho \in Set^{\Pi_1(X)}$ a [[permutation representation]],
we need to exhibit a [[natural isomorphism]] of permutation representations.

$$
  \eta_{\rho} 
    \;\colon\; 
  \rho \longrightarrow Fib(Rec(\rho))
$$

First consider what the right hand side is like:
By [this def.](reconstruction+of+covering+spaces+from+monodromy#ElementaryReconstructionCoveringSpace) of $Rec$ and [this def.](monodromy#CoveringSpaceMonodromy) of $Fib$ we have for every $x \in X$ an actual equality

$$
  Fib(Rec(\rho))(x) = \rho(x)
  \,.
$$

To similarly understand the value of $Fib(Rec(\rho))$ on morphisms $[\gamma] \in \Pi_1(X)$, let $\gamma \colon [0,1] \to X$ be a representing [[path]] in $X$. As in the proof of the path lifting lemma for covering spaces ([this lemma](covering+space#CoveringSpacePathLifting)) we find a [[finite number]] of paths $\{\gamma_i\}_{i \in \{1,n\}}$ such that 

1. regarded as morphisms $[\gamma_i]$ in $\Pi_1(X)$ they [[composition|compose]] to $[\gamma]$:

   $$
     [\gamma] = [\gamma_n] \circ \cdots \circ [\gamma_2] \circ [\gamma_1]
   $$

1. each $\gamma_i$ factors through an open subset $U_i \subset X$ over which $Rec(\rho)$ trivializes.

Hence by [[functor|functoriality]] of $Fib(Rec(\rho))$ it is sufficient to understand its value on these paths $\gamma_i$. But on these we have again by direct unwinding of the definitions that

$$
  Fib(Rec(\rho))([\gamma_i]) = \rho([\gamma_i])
  \,.
$$

This means that if we take

$$
  \eta_\rho(x) \colon \rho(x) \overset{=}{\longrightarrow} Fib(Rec(\rho))
$$

to be the above identification, then this is a [[natural transformation]] and hence in a particular a natural isomorphism, as required.

It remains to see that these morphisms $\eta_\rho$ are themselves natural in $\rho$, hence that for each morphism $\phi \colon \rho \to \rho'$ the diagram


$$
  \array{
    \rho &\overset{\phi}{\longrightarrow}& \rho'
    \\
    {}^{\mathllap{eta_\rho}}\downarrow 
      && 
    \downarrow^{\mathrlap{\eta_{\rho'}}}
    \\
    Fib(Rec(\rho))
    &\underset{Fib(Rec(\phi))}{\longrightarrow}&
    Fib(Rec(\rho'))
  }
$$

commutes as a diagram in $Rep(\Pi_1(X), Set)$. Since these morphisms are themselves groupoid homotopies (natural isomorphisms) this is the case precisely if for all $x \in X$ the corresponding component diagram commutes. But by the above this is 


$$
  \array{
    \rho(x) &\overset{\phi(x)}{\longrightarrow}& \rho'(x)
    \\
    {}^{\mathllap{=}}\downarrow && \downarrow^{\mathrlap{=}}
    \\
    Fib(Rec(\rho))(x)
    &\underset{Fib(Rec(\phi))(x) }{\longrightarrow}&
    Fib(Rec(\rho'))(x)
  }
$$

and hence this means that the top and bottom horizontal morphism are in fact equal. Direct unwinding of the definitions shows that this is indeed the case.


Conversely, given $E \in Cov(X)$ a covering space, we need to exhibit a natural isomorphism of covering spaces of the form

$$
  \epsilon_E 
    \;\colon\;
  Rec(Fib(E)) \longrightarrow E
  \,.
$$

Again by [this def.](reconstruction+of+covering+spaces+from+monodromy#ElementaryReconstructionCoveringSpace) of $Rec$ and [this def.](monodromy#CoveringSpaceMonodromy) of $Fib$  the underlying set of $Rec(Fib(E))$ is actually equal to that of $E$, hence it is sufficient to check that this [[identity function]] on underlying sets is a [[homeomorphism]] of [[topological spaces]].

By the assumption that $X$ is [[locally path-connected topological space|locally path-connected]] and [[semi-locally simply connected topological space|semi-locally simply connected]], it is sufficient to check for $U\subset X$ an open path-connected subset and $x \in X$ a point with the property that $\pi_1(U,x) \to \pi_1(X,x)$ lands is constant on the trivial element, that the open subsets of $E$ of the form $U \times \{\hat x\} \subset p^{-1}(U)$ form a basis for the topology of $Rec(Fib(E))$. But this is the case by definition of $Rec$. 

It remains to see that $\epsilon_E$ is itself natural in $E$. But as for the converse direction, since the components of $\epsilon_E$ are in fact equalities, this follows by direct unwinding of the definitions.

This establishes an equivalence as required. In fact this is an [[adjoint equivalence]].



=--


## Applications

* [[fundamental group of the circle is the integers]]

## In homotopy type theory

In [[homotopy type theory]], the fundamental theorem of covering spaces is really just a special case of the [[universal property]] of [[n-truncation modality|$1$-truncation]]. 

Indeed, in HoTT a covering space over a [[type]] $X$ is usually defined as a [[dependent type]] $C \colon X \to \mathsf{Sets}$. We can get the more familiar bundle definition of a covering space by taking the [[dependent sum type]] $\sum_{x \colon X} C(x)$, which comes equipped with a canonical projection $\operatorname{proj}_1 \colon \sum_{x \colon X} C(x) \to X$.

Since $\mathsf{Sets}$ is a $1$-type, then by the universal property of 1-truncation we have an equivalence:

$$
  \big(
    \Vert X \Vert_1 \to \mathsf{Sets}
  \big) 
  \;\simeq\; 
  \big(
    X \to \mathsf{Sets}
  \big)
  \,.
$$
Since the 1-truncation $\Vert X \Vert_1$ is the [[fundamental groupoid]] of $X$, this really is the fundamental theorem of covering spaces.

\linebreak

{#InCohesiveHomotopyTypeTheory}
Or rather, more faithful to the traditional concepts in topology, it is the [[shape modality]] $\esh$ in [[cohesive homotopy type theory]]
which  turns a [[geometric homotopy type]] into $X$ its [[fundamental infinity-groupoid|fundamental $\infty$-groupoid]] $\esh X$ (see at *[[shape via cohesive path ∞-groupoid]]*) truncating to the actual [[fundamental groupoid]] $\Vert \esh X \Vert_1$.

Then the [[adjunction]] between the [[shape modality]] and the [[flat modality]] $\flat$ says that 

$$
  \big(
    \esh X \to \mathsf{Sets}
  \big) 
  \;\simeq\; 
  \big(
    X \to \flat \mathsf{Sets}
  \big)
  \,,
$$

or, equivalently, that

$$
  \big(
    \Vert \esh X \Vert_1 \to \mathsf{Sets}
  \big) 
  \;\simeq\; 
  \big(
    X \to \flat \mathsf{Sets}
  \big)
  \,,
$$


where $\flat Sets$ is the actual classifier for covering spaces in the generality of cohesive (e.g. topological) homotopy types. This reflects the fundamental theorem of covering spaces as traditionally understood in [[topology]].

(This is the topic of [[schreiber:differential cohomology in a cohesive topos|dcct, sec. 3.8.6]], [p. 358](https://arxiv.org/pdf/1310.7930v1.pdf#page=358))

## References

Lecture notes include

* {#Waldhausen} [[Friedhelm Waldhausen]], around p. 122 of  _Topologie_ ([pdf](https://www.math.uni-bielefeld.de/~fw/ein.pdf))

* {#Moller11} [[Jesper Møller]], _The fundamental group and covering spaces_ (2011) ([pdf](http://www.math.ku.dk/~moller/f03/algtop/notes/covering.pdf))


