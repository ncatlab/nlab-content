[[!redirects fundamental groupoid of a cubical set]]
[[!redirects cubical nerve of a groupoid]]
# Contents
* table of contents
{: toc}

## Introduction

We construct an adjunction between the category of [[groupoid | groupoids]] and the category of [[cubical set | cubical sets]], the left adjoint of which is the _fundamental groupoid_ of a cubical set, and the right adjoint of which is the (cubical) _nerve_ of a groupoid.

## Preliminaries

+-- {: .num_defn}
###### Notation

We denote the category of [[groupoid | groupoids]] by $\mathsf{Grpd}$.

=--

+-- {: .num_defn}
###### Notation

We make use throughout of the notation of [[category of cubes]], [[cubical set]], and [[cubical truncation, skeleton, and co-skeleton]]. 

=--

## Fundamental groupoid for 2-truncated cubical sets

+-- {: .num_defn #NotationFundamentalGroupoid}
###### Notation

We denote by $\Pi^{\leq 2}_{1} : \mathsf{Set}^{\square_{\leq 2}^{op}} \rightarrow \mathsf{Grpd}$ the functor defined as follows.

1) To a 2-truncated cubical set $X$, we associate the groupoid $\Pi^{\leq 2}_{1}(X)$ defined as follows.

a) The objects of $\Pi^{\leq 2}_{1}(X)$ are the 0-cubes of $X$.

b) The arrows of $\Pi^{\leq 2}_{1}(X)$ are zig-zags of 1-cubes of $X$ up to the notion of equivalence defined below, where by a zig-zag of 1-cubes of $X$ we mean, for some integer $n \geq 0$, a set of 1-cubes of $X$ whose faces match up as follows. 

$$
   \array{
      x_{0} & \overset{f_{1}}{\rightarrow} & x_{1} \overset{g_{1}}{\leftarrow} & x_{2} & \cdots & x_{2n-2} & \overset{f_{n}}{\rightarrow} & x_{2n-1} \overset{g_{n}}{\leftarrow} & x_{2n}
   }
$$

We identify a pair of zig-zags if one can be obtained from the other by a sequence of the following manipulations.

i) We may remove or add a pair of arrows (anywhere in the zig-zag) of the form 

$$
   \array{
      x_{0} & \overset{f}{\rightarrow} & x_{1} & \overset{f}{\leftarrow} & x_{0}
   }
$$

or of the following form.

$$
   \array{
      x_{0} & \overset{f}{\leftarrow} & x_{1} & \overset{f}{\rightarrow} & x_{0}
   }
$$  

ii) We may replace an entire zig-zag  

$$
   \array{
      x_{0} & \overset{f_{1}}{\rightarrow} & x_{1} \overset{g_{1}}{\leftarrow} & x_{2} & \cdots & x_{2n-2} & \overset{f_{n}}{\rightarrow} & x_{2n-1} \overset{g_{n}}{\leftarrow} & x_{2n}
   }
$$

with a zig-zag 

$$
   \array{
      x'_{0} & \overset{f'_{1}}{\rightarrow} & x'_{1} \overset{g'_{1}}{\leftarrow} & x'_{2} & \cdots & x'_{2n-2} & \overset{f'_{n}}{\rightarrow} & x'_{2n-1} \overset{g'_{n}}{\leftarrow} & x'_{2n}
   }
$$

if there is, for every $1 \leq i \leq n$, a 2-cube of $X$ whose horizontal 1-cubes are as follows

$$
   \array{
      x_{2i-2}   & \overset{f_{i}}{\to}   & x'_{2i-1} \\
      \downarrow &                        & \downarrow \\
      x'_{2i-2}  & \underset{f'_{i}}{\to} & x'_{2i-1}
   }
$$

and there is, for every $1 \leq i \leq n$, a 2-cube of $X$ whose horizontal 1-cubes are as follows.

$$
   \array{
      x_{2i-1}   & \overset{g_{i}}{\leftarrow}   & x'_{2i} \\
      \downarrow &                        & \downarrow \\
      x'_{2i-1}  & \underset{g'_{i}}{\leftarrow} & x'_{2i}
   }
$$

c) The source of a zig-zag as at the beginning of b) is $x_{0}$, and the target is $x_{2n}$.

d) Composition of arrows is given by concatenation of zig-zags (it is immediately verified that this is well-defined with respect to the equivalence relation of b)).

e) The identity arrow on an object $x$ of $\Pi^{\leq 2}_{1}(X)$ is the zig-zag with $n = 0$ consisting simply of $x$.

f) The inverse of an arrow 

$$
   \array{
      x_{0} & \overset{f_{1}}{\rightarrow} & x_{1} \overset{g_{1}}{\leftarrow} & x_{2} & \cdots & x_{2n-2} & \overset{f_{n}}{\rightarrow} & x_{2n-1} \overset{g_{n}}{\leftarrow} & x_{2n}
   }
$$

of $\Pi_{1}(X)$ is the following arrow (it is immediately verified that this is well-defined with respect to the equivalence relation of b)).

$$
   \array{
      x_{2n} & \overset{g_{n}}{\rightarrow} & x_{2n-1} \overset{f_{n}}{\leftarrow} & x_{2n-2} & \cdots & x_{2} & \overset{g_{1}}{\rightarrow} & x_{1} \overset{f_{1}}{\leftarrow} & x_{0}
   }
$$

2) To a morphism of 2-truncated cubical sets $F : X \rightarrow Y$, we associate the functor $\Pi^{\leq 2}_{1}(F) : \Pi^{\leq 2}_{1}(X) \rightarrow \Pi^{\leq 2}_{1}(Y)$ defined as follows.

a) On objects, $\Pi^{\leq 2}_{1}(F)$ is the same as $F$.

b) To a zig-zag as follows 

$$
   \array{
      x_{0}  &  \overset{f_{1}}{\rightarrow} & x_{1} \overset{g_{1}}{\leftarrow} & x_{2} & \cdots & x_{2n-2} & \overset{f_{n}}{\rightarrow} & x_{2n-1} \overset{g_{n}}{\leftarrow} & x_{2n}
   }
$$

we associate the following zig-zag. 

$$
   \array{
      F(x_{0}) &  \overset{F(f_{1})}{\rightarrow} & F(x_{1}) \overset{F(g_{1})}{\leftarrow} & F(x_{2}) & \cdots & F(x_{2n-2}) & \overset{F(f_{n})}{\rightarrow} & F(x_{2n-1}) \overset{F(g_{n})}{\leftarrow} & F(x_{2n})
   }
$$

It is immediately verified that this is well-defined with respect to the equivalence relation of 1) b).

=--

+-- {: .num_defn}
###### Terminology

We refer to $\Pi^{\leq 2}_{1} : \mathsf{Set}^{\square_{\leq 2}^{op}} \rightarrow \mathsf{Grpd}$ as the _fundamental groupoid_ functor for 2-truncated cubical sets.

=--

## 2-truncated nerve functor

+-- {: .num_defn}
###### Notation

We denote by $N^{\leq 2} : \mathsf{Grpd} \rightarrow \mathsf{Set}^{\square_{\leq 2}^{op}}$ the functor defined as follows.

1) To a groupoid $\mathcal{A}$, we associate the 2-truncated cubical set $N^{\leq 2}(\mathcal{A})$ defined as follows.

a) The 0-cubes of $N^{\leq 2}(\mathcal{A})$ are the objects of $\mathcal{A}$.

b) The 1-cubes $f : a_{0} \rightarrow a_{1}$ of $N^{\leq 2}(\mathcal{A})$ are the arrows $f$ of $\mathcal{A}$ with source $a_{0}$ and target $a_{1}$.

c) The 2-cubes 

$$
   \array{
      a_{0}            & \overset{f_{0}}{\to}  & a_{1} \\
      f_{2} \downarrow & \sigma                & \downarrow f_{1} \\
      a_{2}            & \underset{f_{3}}{\to} & a_{3}
   }
$$

of $N^{\leq 2}(\mathcal{A})$ are the commutative squares $\sigma$ of $\mathcal{A}$ whose boundary looks the same as this.

d) The degenerate 1-cubes of $N^{\leq 2}(\mathcal{A})$ are the identity arrows of $\mathcal{A}$.

e) The degenerate 2-cubes of $N^{\leq 2}(\mathcal{A})$ are the commutative squares of $\Pi^{\leq 2}_{1}(\mathcal{A})$ which look as follows

$$
   \array{
      x_{0}         & \overset{f}{\to}  & x_{1} \\
      id \downarrow & \sigma            & \downarrow id \\
      x_{0}         & \underset{f}{\to} & x_{1}
   }
$$

or as follows.

$$
   \array{
      x_{0}        & \overset{id}{\to}  & x_{0} \\
      f \downarrow & \sigma             & \downarrow f \\
      x_{1}        & \underset{id}{\to} & x_{1}
   }
$$

2) To a functor $F : \mathcal{A} \rightarrow \mathcal{B}$, we associate the morphism of 2-truncated cubical sets $N^{\leq 2}(F) : N^{\leq 2}(\mathcal{A}) \rightarrow N^{\leq 2}(\mathcal{B})$ defined as follows.

a) On 0-cubes, $N^{\leq 2}(\mathcal{A})$ is the same as $F$.

b) On 1-cubes, $N^{\leq 2}(F)$ is the same as $F$. 

c) On 2-cubes, $N^{\leq 2}(F)$ sends a commutative square 

$$
   \array{
      a_{0}            & \overset{f_{0}}{\to}  & a_{1} \\
      f_{2} \downarrow & \sigma                & \downarrow f_{1} \\
      a_{2}            & \underset{f_{3}}{\to} & a_{3}
   }
$$

of $\mathcal{A}$ to the commutative square 

$$
   \array{
      F(a_{0})            & \overset{F(f_{0})}{\to}  & F(a_{1}) \\
      F(f_{2}) \downarrow & F(\sigma)                & \downarrow F(f_{1}) \\
      F(a_{2})            & \underset{F(f_{3})}{\to} & F(a_{3})
   }
$$

of $\mathcal{A}$.

=--

+-- {: .num_defn}
###### Terminology

We refer to $N^{\leq 2} : \mathsf{Grpd} \rightarrow \mathsf{Set}^{\square_{\leq 2}^{op}}$ as the 2-truncated _nerve_ functor.

=--

## Adjunction between the fundamental groupoid functor for 2-truncated cubical sets and the 2-truncated cubical nerve functor 

+-- {: .num_defn}
###### Notation

We denote by $\epsilon : \Pi^{\leq 2}_{1} \circ N^{\leq 2} \rightarrow id$ the natural transformation which to a groupoid $\mathcal{A}$ associates the functor $\epsilon(\mathcal{A}) : \Pi^{\leq 2}_{1} \circ N^{\leq 2}(\mathcal{A}) \rightarrow \mathcal{A}$ defined as follows.

1) On objects it is the identity.

2) To an arrow of $\Pi^{\leq 2}_{1} \circ N^{\leq 2}(\mathcal{A})$, given by a zig-zag of arrows   

$$
   \array{
      a_{0}  &  \overset{f_{1}}{\rightarrow} & a_{1} \overset{g_{1}}{\leftarrow} & a_{2} & \cdots & a_{2n-2} & \overset{f_{n}}{\rightarrow} & a_{2n-1} \overset{g_{n}}{\leftarrow} & a_{2n}
   }
$$

of $\mathcal{A}$, we associate the arrow of $\mathcal{A}$ given by the composition in $\mathcal{A}$ of the arrows

$$
   \array{
      a_{0}  &  \overset{f_{1}}{\rightarrow} & a_{1} \overset{g_{1}^{-1}}{\rightarrow} & a_{2} & \cdots & a_{2n-2} & \overset{f_{n}}{\rightarrow} & a_{2n-1} \overset{g_{n}^{-1}}{\rightarrow} & a_{2n}
   }
$$

of $\mathcal{A}$. 

It is straightforward to check that this is well-defined with respect to the equivalence relation of 1 b) of Notation 
\ref{NotationFundamentalGroupoid}, and that we indeed have a functor.
 
=--

+-- {: .num_defn}
###### Notation

We denote by $\eta : id \rightarrow N^{\leq 2} \circ \Pi^{\leq 2}_{1}$ the natural transformation which to a 2-truncated cubical set $X$ associates the morphism of 2-truncated cubical sets $\eta(X) : X \rightarrow N^{\leq 2} \circ \Pi^{\leq 2}_{1}(X)$ defined as follows.

1) On objects it is the identity.

2) To a 1-cube $f : x_{0} \rightarrow x_{1}$ of $X$ we associate the following zig-zag of 1-cubes of $X$, where the right arrow is the degeneracy on $x_{1}$.

$$
   \array{
      x_{0}  &  \overset{f}{\rightarrow} & x_{1} \overset{id}{\leftarrow} & x_{1} }
$$

3) To a 2-cube 

$$
   \array{
      x_{0}            & \overset{f_{0}}{\to}  & x_{1} \\
      f_{2} \downarrow & \sigma                & \downarrow f_{1} \\
      x_{2}            & \underset{f_{3}}{\to} & x_{3}
   }
$$

of $X$ we associate the commutative square in $\Pi^{\leq 2}_{1}(X)$ given as follows.

$$
   \array{
      x_{0}            & \overset{f_{0}}{\to}  & x_{1} & \overset{id}{\leftarrow}  & x_{1} \\
      f_{2} \downarrow &                       &       &                           & \downarrow f_{1} \\
      x_{2}            &                       &       &                           & x_{3} \\
      id    \downarrow &                       &       &                           & \downarrow id \\
      x_{2}            & \underset{f_{3}}{\to} & x_{2} & \underset{id}{\leftarrow} & x_{3} \\       
   }
$$

The following diagram of commutative squares in $\Pi^{\leq 2}_{1}(X)$ illustrates that the above square does indeed commute in $\Pi^{\leq 2}_{1}(X)$.

$$
   \array{
      x_{0}         & \overset{f_{0}}{\rightarrow}  & x_{1}        & \overset{id}{\leftarrow} & x_{1}        & \overset{f_{1}}{\rightarrow}   & x_{2}         & \overset{id}{\leftarrow} & x_{2} \\
      id \downarrow &                               & \downarrow A &                          & \downarrow A &                            & \downarrow id &                          & \downarrow id \\
      x_{0}         & \underset{f_{2}}{\rightarrow} & x_{2}        & \underset{id}{\leftarrow} & x_{2}        & \underset{f_{3}}{\rightarrow} & x_{3}         & \underset{id}{\leftarrow} & x_{3}
   }
$$

Here A is $f_{2} \circ f_{0}^{-1}$. That the square  

 $$
   \array{
      x_{1}        & \overset{f_{1}}{\to}     & x_{3} \\
      A \downarrow &                       & \downarrow id \\
      x_{2}        & \underset{f_{3}}{\to} & x_{3}
   }
$$

commutes follows easily from the commutativity of the square arising from the 2-cube $\sigma$ of $X$ above. 

=--

+-- {: .num_defn #PropositionAdjunctionBetweenPi1TwoTruncAndNTwoTrunc}
###### Proposition

The natural transformations $\eta$ and $\epsilon$ define an adjunction between $\Pi^{\leq 2}_{1}$ and $N^{\leq 2}$.

=--

+-- {: .proof}
###### Proof

Straightforward verification that the triangle identities hold.

=--

## Fundamental groupoid functor

+-- {: .num_defn}
###### Notation

Adopting the notation of [[cubical truncation, skeleton, and co-skeleton]], we denote by $\Pi_{1} : \mathsf{Set}^{\square^{op}} \rightarrow \mathsf{Grpd}$ the functor 

$$
   \array{
      \mathsf{Set}^{\square^{op}} & \overset{tr_{2}}{\rightarrow}  & \mathsf{Set}^{\square_{2}^{op}} & \overset{\Pi_{1}^{\leq 2}}{\rightarrow} & \mathsf{Grpd}.
   }
$$

=--

+-- {: .num_defn}
###### Terminology

We refer to the functor $\Pi_{1} : \mathsf{Set}^{\square^{op}} \rightarrow \mathsf{Grpd}$ as the _fundamental groupoid_ functor.

=--

## Nerve functor

+-- {: .num_defn}
###### Notation

Adopting the notation of [[cubical truncation, skeleton, and co-skeleton]], we denote by $N : \mathsf{Grpd} \rightarrow \mathsf{Set}^{\square^{op}}$ the functor 

$$
   \array{
      \mathsf{Grpd} & \overset{N^{\leq 2}}{\rightarrow} & \mathsf{Set}^{\square_{\leq 2} ^{op}} & \overset{cosk_{2}}{\rightarrow}  & \mathsf{Set}^{\square^{op}}.
   }
$$

=--

+-- {: .num_defn}
###### Terminology

We refer to the functor $N : \mathsf{Set}^{\square^{op}} \rightarrow \mathsf{Grpd}$ as the _nerve_ functor.

=--

## Adjunction between the fundamental groupoid functor and the nerve functor

Since $\Pi^{\leq 2}_{1}$ is left adjoint to $N^{\leq 2}$ by Proposition \ref{#PropositionAdjunctionBetweenPi1TwoTruncAndNTwoTrunc} above, and since $tr_{2}$ is left adjoint to $cosk_{2}$, we have that $\Pi_{1}$ is left adjoint to $N$.