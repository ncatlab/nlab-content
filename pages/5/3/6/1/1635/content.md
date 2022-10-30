
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

Simplicial homotopy groups are the basic invariants of [[simplicial sets]]/[[Kan complexes]] in [[simplicial homotopy theory]].
 
Given that a [[Kan complex]] is a special [[simplicial set]] that [[homotopy hypothesis|behaves like]] a combinatorial model for a [[topological space]], the _simplicial homotopy groups_ of a  Kan complex are accordingly the combinatorial analog of the [[homotopy groups]] of [[topological spaces]]: instead of being maps from topological [[spheres]] modulo maps from topological disks, they are maps from the [[boundary of a simplex]] modulo those from the [[simplex]] itself. 

Accordingly, the definition of the discussion of simplicial homotopy groups is essentially literally the same as that of [[homotopy groups]] of topological spaces.  One technical difference is for instance that the definition of the group structure is slightly more non-immediate for simplicial homotopy groups than for topological homotopy groups (see below).



## Definition

Recall the classical [[model structure on simplicial sets]]. Let $X$ be a fibrant simplicial set, i.e. a [[Kan complex]].  

+-- {: .num_defn #UnderlyingSetsOfSimplicialHomotopyGroups}
###### Definition 

For $X$ a [[Kan complex]], then its **0th homotopy group** (or **set of [[connected components]]**) is the set of [[equivalence classes]] of vertices modulo the [[equivalence relation]] $X_1 \stackrel{(d_1,d_0)}{\longrightarrow} X_0 \times X_0$

$$
  \pi_0(X) \colon X_0/X_1
  \,.
$$

For $x \in X_0$ a vertex and for $n \in \mathbb{N}$, $n \geq 1$, then the underlying [[set]]  of the **$n$th homotopy group** of $X$ at $x$ -- denoted $\pi_n(X,x)$ -- is, the set of [[equivalence classes]] $[\alpha]$ of morphisms

$$
  \alpha \colon \Delta^n \to X
$$ 
 
from the simplicial $n$-[[simplex]] $\Delta^n$ to $X$, such that these take the [[boundary of a simplex|boundary of the simplex]] to $x$, i.e. such that they fit into a [[commuting diagram]] in [[sSet]] of the form
 
$$
  \array{
     \partial \Delta[n] & \longrightarrow &  \Delta[0]
     \\
     \downarrow && \downarrow^{\mathrlap{x}}
     \\
     \Delta[n] &\stackrel{\alpha}{\longrightarrow}& X
   }
  \,,
$$


where two such maps $\alpha, \alpha'$ are taken to be equivalent is they are related by a [[simplicial homotopy]] $\eta$

$$
  \array{
     \Delta[n]
     \\
     \downarrow^{i_0} & \searrow^{\alpha}
     \\
     \Delta[n] \times \Delta[1]
     &\stackrel{\eta}{\longrightarrow}&
     X
     \\
     \uparrow^{i_1} & \nearrow_{\alpha'}
     \\
     \Delta[n]
  }
$$

that fixes the boundary in that it fits into a [[commuting diagram]] in [[sSet]] of the form

$$
  \array{
     \partial \Delta[n] \times \Delta[1]
     & \longrightarrow &
     \Delta[0]
     \\
     \downarrow && \downarrow^{\mathrlap{x}}
     \\
     \Delta[n]  \times \Delta[1]
     &\stackrel{\eta}{\longrightarrow}&
     X
  }
  \,.
$$

=--

These sets are taken to be equipped with the following group structure.

+-- {: .num_defn #ProductOnSimplicialHomotopyGroups}
###### Definition 
  
For $X$ a [[Kan complex]], for $x\in X_0$, for $n \geq 1$ and for  $f,g \colon \Delta[n] \to X$ two representatives of $\pi_n(X,x)$ as in def. \ref{UnderlyingSetsOfSimplicialHomotopyGroups}, consider the following $n$-simplices in $X_n$:

$$
  v_i 
  \coloneqq
  \left\{
    \array{
      s_0 \circ s_0 \circ \cdots \circ s_0 (x) & for \; 0 \leq i \leq  n-2
      \\
      f & for \; i = n-1
      \\
      g & for \; i = n+1
    }
  \right.
$$

This corresponds to a morphism $\Lambda^{n+1}[n] \to X$ from a [[horn]] of the $(n+1)$-[[simplex]] into $X$. By the [[Kan complex]] property of $X$ this morphism has an [[extension]] $\theta$ through the $(n+1)$-[[simplex]] $\Delta[n]$

$$
  \array{
     \Lambda^{n+1}[n] & \longrightarrow & X
     \\
     \downarrow & \nearrow_{\mathrlap{\theta}}
     \\
     \Delta[n+1]
  }
$$

From the [[simplicial identities]] one finds that the boundary of the $n$-simplex arising as the $n$th boundary piece $d_n \theta$ of $\theta$ is constant on $x$

$$
  d_i d_{n} \theta = d_{n-1} d_i \theta = x
$$

So $d_n \theta$ represents an element in $\pi_n(X,x)$ and we define a product operation on $\pi_n(X,x)$ by

$$
  [f]\cdot [g] \coloneqq [d_n \theta]
  \,.
$$

=--

(e.g. [Goerss-Jardine 96, p. 26](#GoerssJardine96))

+-- {: .num_remark}
###### Remark 

All the degenerate $n$-simplices $v_{0 \leq i \leq n-2}$ in def. \ref{ProductOnSimplicialHomotopyGroups} are just there so that the gluing of the two $n$-cells $f$ and $g$ to each other can be regarded as forming the boundary of an $(n+1)$-simplex except for one face. By the Kan extension property that missing face exists, namely $d_n \theta$.  This is a choice of gluing composite of $f$ with $g$.

=--

+-- {: .num_lemma}
###### Lemma

The product on homotopy group elements in def. \ref{ProductOnSimplicialHomotopyGroups} is
well defined, in that it is independent of the
choice of representatives $f$, $g$ and of the extension $\theta$.

=--

e.g. ([Goerss-Jardine 96, lemma 7.1](#GoerssJardine96))


+-- {: .num_lemma}
###### Lemma

The product operation in def. \ref{ProductOnSimplicialHomotopyGroups} yields a [[group]] structure on $\pi_n(X,x)$, which is [[abelian group|abelian]] for $n \geq 2$.

=--

e.g. ([Goerss-Jardine 96, theorem 7.2](#GoerssJardine96))

Finally:

+-- {: .num_defn }
###### Definition

The simplicial homotopy groups of any [[simplicial set]], not necessarily [[Kan complex|Kan]], are those of any of its [[Kan fibrant replacements]] according to def. \ref{UnderlyingSetsOfSimplicialHomotopyGroups}.

=-- 

+-- {: .num_remark}
###### Remark 

The first homotopy group, $\pi_1(X,x)$, is also called the _[[fundamental group]]_ of $X$. 

=--



## Properties

### Relation to topological homotopy groups

The simplicial homotopy groups of a Kan complex coincide with the homotopy groups of its [[geometric realization]], see e.g. ([Goerss-Jardine 96, page 60](#GoerssJardine96)).


### Relation to homotopy equivalence

A morphism of simplicial sets which induces an [[isomorphism]] on all simplicial homotopy groups is called a [[weak homotopy equivalence]]. If it goes between [[Kan complexes]] then it is actually a [[homotopy equivalence]].


### Relation to chain homology groups of associated Moore complexes

Another way to get the group structure on the homotopy groups of a Kan complex, $X$, is via its [[Dwyer-Kan loop groupoid]] and the [[Moore complex]]. This gives a [[simplicial groupoid|simplicially enriched groupoid]] $G(X)$, or if we restricted to the pointed case, and just look at the loops at the base vertex, a [[simplicial group]]. (We will assume for the sake of simplicity that $X$ is _reduced_, that is to say, $X_0$ is a singleton, and thus that $G(X)$ is a simplicial group.)

The construction of $G(X)$ is then given by  the free group functor on the various levels, shifted by 1, and with a twist in the zeroth face map (see [[Dwyer-Kan loop groupoid]] and simplify to the reduced case.) 


+-- {: .num_prop}
###### Proposition

There is an isomorphism between $\pi_n(X)$ as defined above and $H_{n-1}(N G(X))$, the $(n-1)$th homology group of the [[Moore complex]] of the simplicial group, $G(X)$.

=--

### Long exact sequences of a Kan fibration

For $f \colon X \longrightarrow Y$ a [[Kan fibration]], for $x\in X_0$ any vertex, for $y \coloneqq f(x) \in Y$ its image and $F_x \coloneqq f^{-1}(y)$ the [[fiber]] at that point, then the induced [[homomorphism]] of simplicial homotopy groups form a [[long exact sequence of homotopy groups]]

$$
  \cdots
  \to
  \pi_{n+1}(Y,y)
  \stackrel{}{\longrightarrow}
  \pi_n(F,x)
  \stackrel{}{\longrightarrow}
  \pi_n(X,x)
  \stackrel{}{\longrightarrow}
  \pi_n(Y,y)
  \stackrel{}{\longrightarrow}
  \pi_{n-1}(F,x)
  \to
  \cdots
$$

$$
  \cdots 
  \to
  \pi_1(F,x) \longrightarrow
  \pi_0(F) \stackrel{}{\longrightarrow} \pi_0(X) \longrightarrow \pi_0(Y)
$$

i.e. a [[long exact sequence]] of [[groups]] ending in a long exact sequence of [[pointed sets]].

(e.g. [Goerss-Jardine 96, lemma 7.3](#GoerssJardine96))


## Examples 

+-- {: .num_lemma }
###### Lemma

Let $C$ be a [[groupoid]] and $\mathcal{N}(C)$ its [[nerve]].

Then 

* $\pi_0 \mathcal{N}(C,c)$ is the set of isomorphism classes of $C$ with the class of $c$ as base point

* $\pi_1 \mathcal{N}(C,c)$ is the [[automorphism group]] $Aut_C(c)$ of $c$

* $\pi_{n \geq 2} \mathcal{N}(C,c)$ is trivial

=--

In particular a [[functor]]
$f : C \to D$ of [[groupoids]] is a [[equivalence of categories]] if under the nerve it induces a weak equivalence $\mathcal{N}(f) : \mathcal{N}(C) \to \mathcal{N}(D)$ of [[Kan complexes]]:

* that $\pi_0 \mathcal{N}(f,c) : \pi_0(C,c) \to \pi_0(D,f(c))$ is an isomorphism implies that $f$ is an [[essentially surjective functor]] and is implied by $f$\'s being a [[full functor]];
* that $\pi_1 \mathcal{N}(f,c) : \pi_1(C,c) \to \pi_1(D,f(c))$ is an isomorphism is equivalent to $f$\'s being a [[full and faithful functor]].


## References

Textbook accounts include

* {#GoerssJardine96} [[Paul Goerss]], [[Rick Jardine]], chapter I, section 7 of _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1996)


Originally homotopy groups of simplicial sets had been defined in terms of the ordinary [[homotopy groups]] of the [[topological spaces]] [[geometric realization|realizing]] them. Apparently the first or one of the first discussions of the purely combinatorial definition is 

* {#Kan58} [[Dan Kan]], _A combinatorial definition of homotopy groups_, Annals of Mathematics Second Series, Vol. 67, No. 2 (Mar., 1958), pp. 282-312 ([jstor](http://www.jstor.org/stable/1970006?seq=8))

[[!redirects simplicial homotopy groups]]