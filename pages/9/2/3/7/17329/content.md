# Contents
* table of contents
{: toc}

## Introduction

We give a proof that [[groupoid | groupoids]] model [[homotopy 1-type | homotopy 1-types]]. More precisely, we construct a Quillen equivalence between a model structure on the category of groupoids, and a certain model structure on the category of cubical sets.

## Preliminaries

+-- {: .num_note}
###### Notation

We make use throughout of the notation of [[category of cubes]], [[cubical set]], [[cubical truncation, skeleton, and co-skeleton]], and [[fundamental groupoid of a cubical set and the cubical nerve of a groupoid]]. 

=--

## One direction of the equivalence

+-- {: .num_prop #PropositionPi1NToIdIsNatIso}
###### Proposition

The adjunction natural transformation $\epsilon : \Pi^{\leq 2}_{1} \circ N^{\leq 2} \rightarrow id$ is a natural isomorphism.

=--

+-- {: .proof}
###### Proof

Let $\mathcal{A}$ be a groupoid. Let $r(\mathcal{A}) : \mathcal{A} \rightarrow \Pi^{\leq 2}_{1} \circ N^{\leq 2}$ be the functor defined as follows.

1) On objects it is the identity.

2) To an arrow $f : a_{0} \rightarrow a_{1}$ of $\mathcal{A}$, we associate the arrow   

$$
   \array{
      a_{0}  &  \overset{f}{\rightarrow} & a_{1} \overset{id}{\leftarrow} & a_{1} 
   }
$$

of $\Pi^{\leq 2}_{1} \circ N^{\leq 2}(\mathcal{A})$.

Because of 1 b) ii) of [Notation 3](fundamental+groupoid+of+a+cubical+set+and+the+cubical+nerve+of+a+groupoid#NotationFundamentalGroupoid) of [[fundamental groupoid of a cubical set and the cubical nerve of a groupoid]], the following diagram of commutative squares illustrates that $r(g \circ f) = r(g) \circ r(f)$, where $f : a_{0} \rightarrow a_{1}$ and $g : a_{1} \rightarrow a_{2}$ are arrows of $\mathcal{A}$. 

$$
   \array{
      a_{0}         & \overset{f}{\rightarrow}          & a_{1}        & \overset{id}{\rightarrow} & a_{1}        & \overset{g}{\rightarrow}   & a_{2}         & \overset{id}{\leftarrow} & a_{2} \\
      id \downarrow &                                   & \downarrow g &                           & \downarrow g &                            & \downarrow id &                          & \downarrow id \\
      a_{0}         & \underset{g \circ f}{\rightarrow} & a_{2}        & \underset{id}{\leftarrow} & a_{2}        & \underset{id}{\rightarrow} & a_{2}         & \underset{id}{\leftarrow} & a_{2}
   }
$$

That $r(id) = id$ follows immediately from 1 b) i) of [Notation 3](fundamental+groupoid+of+a+cubical+set+and+the+cubical+nerve+of+a+groupoid#NotationFundamentalGroupoid) of [[fundamental groupoid of a cubical set and the cubical nerve of a groupoid]].

It is clear that $\epsilon(\mathcal{A}) \circ r(\mathcal{A})$ is $id(\mathcal{A})$.

Moreover, because of 1 b) ii) of [Notation 3](fundamental+groupoid+of+a+cubical+set+and+the+cubical+nerve+of+a+groupoid#NotationFundamentalGroupoid) of [[fundamental groupoid of a cubical set and the cubical nerve of a groupoid]], the following diagram of commutative squares illustrates that $r(\mathcal{A}) \circ \epsilon(\mathcal{A})$ is $id(\mathcal{A})$. 

$$
   \array{
      a_{0}         & \overset{f_{1}}{\rightarrow} & a_{1}        & \overset{g_{1}}{\leftarrow} & a_{2}        & \cdots & a_{2n-2}     & \overset{f_{n}}{\rightarrow} & a_{2n-1}              & \overset{g_{n}}{\leftarrow} & a_{2n} \\
      id \downarrow &                              & \downarrow A &                              & \downarrow B &        & \downarrow C &                              & \downarrow g_{n}^{-1} &                             & \downarrow id \\
      a_{0}         & \underset{D}{\rightarrow}    & a_{2n}       & \underset{id}{\leftarrow} & a_{2n}          & \cdots & a_{2n}       & \underset{id}{\rightarrow} & a_{2n}                  & \underset{id}{\leftarrow}   & a_{2n}
   }
$$

Here 

$$
   \array{
      a_{0}  &  \overset{f_{1}}{\rightarrow} & a_{1} \overset{g_{1}}{\leftarrow} & a_{2} & \cdots & a_{2n-2} & \overset{f_{n}}{\rightarrow} & a_{2n-1} \overset{g_{n}}{\leftarrow} & a_{2n}
   }
$$

is any zig-zag of arrows of $\mathcal{A}$, and the arrows A, B, C, and D are given as follows.

A) $g_{n}^{-1} \circ f_{n} \circ \cdots g_{2}^{-1} \circ f_{2} \circ g_{1}^{-1}$

B) $g_{n}^{-1} \circ f_{n} \circ \cdots g_{2}^{-1} \circ f_{2}$

C) $g_{n}^{-1} \circ f_{n}$

D) $g_{n}^{-1} \circ f_{n} \circ \cdots g_{2}^{-1} \circ f_{2} \circ g_{1}^{-1} \circ f_{1}$

We also make use of 1 b) i) of [Notation 3](fundamental+groupoid+of+a+cubical+set+and+the+cubical+nerve+of+a+groupoid#NotationFundamentalGroupoid) of [[fundamental groupoid of a cubical set and the cubical nerve of a groupoid]] in identifying 

$$
    \array{a_{0} & \underset{D}{\rightarrow} & a_{2n} & \underset{id}{\leftarrow} & a_{2n} & \cdots & a_{2n} & \underset{id}{\rightarrow} & x_{2n} & \underset{id}{\leftarrow} & a_{2n}}
$$

with 

$$
    \array{a_{0} & \underset{D}{\rightarrow} & a_{2n} & \underset{id}{\leftarrow} a_{2n}}
$$

as required.
 
=--

+-- {: .num_cor}
###### Corollary

The adjunction natural transformation $\Pi_{1} \circ N \rightarrow id$ is a natural isomorphism.

=--

+-- {: .proof}
###### Proof

Since $tr_{2}$ is fully faithful, the adjunction natural transformation $id \rightarrow tr_{2} cosk_{2}$ is a natural isomorphism. The corollary follows from this and Proposition \ref{PropositionPi1NToIdIsNatIso}.

=--

## Other direction of the equivalence

To be written.