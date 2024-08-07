# Contents
* table of contents
{: toc}

## Truncation

We make use of the notation introduced in [[category of cubes]] and [[cubical set]].

+-- {: .num_defn}
###### Notation

Let $n \geq 0$ be an integer. We denote by $\square_{n}$ the full sub-category of $\square$ whose objects are $I^{0}$, $I^{1}$, $\ldots$, $I^{n}$.

=--

+-- {: .num_defn}
###### Terminology

We refer to $\square_{n}$ as the _$n$-truncated category of cubes_.

=--

+-- {: .num_defn}
###### Notation

Let $n \geq 0$ be an integer. The inclusion functor $i_{n} : \square_{n} \rightarrow \square$ canonically determines a functor $i_{n}^{*} : \mathsf{Set}^{\square^{op}} \rightarrow \mathsf{Set}^{\square_{n}^{op}}$. We shall denote this functor by $tr_{n}$.

=--

+-- {: .num_defn}
###### Terminology

We refer to $tr_{n}$ as the _$n$-truncation_ functor.

=--

+-- {: .num_defn}
###### Definition

Let $n \geq 0$ be an integer. The _category of $n$-truncated cubical sets is the free co-completion of $\square_{n}$. 

=--

+-- {: .num_defn}
###### Remark

The free co-completion of a small category can be constructed as the category of [[presheaf | presheaves]] presheaves of sets on this category. Thus we can also think of the category of $n$-truncated cubical sets as the category of presheaves of sets on $\square_{n}$.

=--

+-- {: .num_defn}
###### Notation

We denote the category of $n$-truncated cubical sets by $\mathsf{Set}^{\square_{n}^{op}}$.

=--

+-- {: .num_defn}
###### Definition

An _$n$-truncated cubical set_ is an object of $\mathsf{Set}^{\square_{n}^{op}}$.

=--

+-- {: .num_defn}
###### Remark

When we think of the category of $n$-truncated cubical sets as the category of presheaves of sets on $\square_{n}$, we consequently think of an $n$-truncated cubical set as a presheaf of sets on $\square_{n}$.

=--

+-- {: .num_defn}
###### Definition

A _morphism of $n$-truncated cubical sets_ is an arrow of $\mathsf{Set}^{\square_{n}^{op}}$.

=--

+-- {: .num_defn}
###### Terminology

Let $X$ be an $n$-truncated cubical set. Let $0 \leq m \geq n$ be an integer. By an _$m$-cube_ of $X$, we shall mean an $m$-cube of $sk_{n}(X)$, where $sk_{n}$ is $n$-skeleton functor defined in Notation \ref{NotationNSkeleton}.

=--


## Skeleton

+-- {: .num_defn #NotationNSkeleton}
###### Notation

Let $n \geq 0$ be an integer. By [[Kan extension | left Kan extension]], the functor $tr_{n} : \mathsf{Set}^{\square^{op}} \rightarrow \mathsf{Set}^{\square_{n}^{op}}$ admits a [[adjoint functor | left adjoint]] $i_{!} : \mathsf{Set}^{\square_{n}^{op}} \rightarrow \mathsf{Set}^{\square^{op}}$. We shall denote this functor by $sk_{n}$.

=--

+-- {: .num_defn}
###### Terminology

We refer to $sk_{n}$ as the _$n$-skeleton_ functor.

=--

## Co-skeleton

+-- {: .num_defn}
###### Notation

Let $n \geq 0$ be an integer. By [[Kan extension | right Kan extension]], the functor $tr_{n} : \mathsf{Set}^{\square^{op}} \rightarrow \mathsf{Set}^{\square_{n}^{op}}$ admits a [[adjoint functor | right adjoint]] $i_{*} : \mathsf{Set}^{\square_{n}^{op}} \rightarrow \mathsf{Set}^{\square^{op}}$. We shall denote this functor by $cosk_{n}$.

=--

+-- {: .num_defn}
###### Terminology

We refer to $cosk_{n}$ as the _$n$-coskeleton_ functor.

=--