#Contents#
* table of contents
{:toc}

## Idea

An open subscheme is the analogue of an open subset of a [[topological space]] for schemes. 

## Definition

An __open subscheme__ of a [[scheme]] $(Y,\mathcal{O}_Y)$ is a scheme $(U,\mathcal{O}_Y)$ whose underlying space is the subspace $U$ of $Y$ together with an isomorphism of the structure sheaf $\mathcal{O}_U$ with the restriction $\mathcal{O}_Y|_U$ of the structure sheaf $\mathcal{O}_Y$ to $U$. An isomorphism of a scheme $(X,\mathcal{O}_X)$ and an open subscheme $(U,\mathcal{O}_Y)$ of another scheme $(Y,\mathcal{O}_Y)$ amounts to an [[open immersion of schemes]] $(X,\mathcal{O}_X)\hookrightarrow(Y,\mathcal{O}_Y)$. 

## Open subsets of the underlying topological space of a scheme

Before embarking upon the proof of Proposition \ref{PropositionOpenSubsetAsOpenSubscheme}, we shall need a few preliminaries. Let $A$ be a commutative ring. Let $Spec A$ denote the set of prime ideals of $A$. Given an element $a$ of $A$, we denote by $D_{A}(a)$ the set of [[prime ideal|prime ideals]] of $A$ to which $a$ does not belong. Either by definition, or by a little basic commutative algebra, we have that $\{ D_{A}(a) | a \in A \}$ is a [[topological base|basis]] for the [[Zariski topology]] on $Spec A$. 

An [[affine scheme]] is by definition the locally ringed space $(Spec A, \mathcal{O}_{Spec A})$, where $Spec A$ is the set we have just defined equipped with the Zariski topology, and $\mathcal{O}_{Spec A}$ is a certain sheaf of rings on this space.

A basic result in commutative algebra is that, for any $a \in A$, $(D_{A}(a), \mathcal{O}_{Spec A} | D_{A}(a))$ is an affine scheme, isomorphic to $(Spec A_{a}, \mathcal{O}_{Spec A_{a}})$. Here $A_{a}$ is the [[localisation of a commutative ring at an element | localisation]] of $A$ at $a$. 

+-- {: .num_prop #PropositionOpenSubsetAsOpenSubscheme}
###### Proposition

Let $(X, \mathcal{O}_{X})$ be a scheme, and let $U$ be an open subset of $X$. Then $(U, \mathcal{O}_{X} | U)$, in the same notation as at [[scheme]], is a scheme.

=--

+-- {: .proof}
###### Proof

Let $x \in U$. We must prove that $x$ has an open neighbourhood $W$ in $U$ such that $(W, \mathcal{O}_{U} | W)$ is isomorphic to an [[affine scheme]].  

Immediately from the definition of a scheme, there is an open neighbourhood $N$ of $x$ in $X$ such that $(N, \mathcal{O}_{X} | N)$ is isomorphic to an [[affine scheme]], that is to say, a pair $(Spec A, \mathcal{O}_{Spec A})$ as defined above, for some commutative ring $A$. This isomorphism in particular involves an isomorphism of topological spaces $N \rightarrow Spec A$, which we shall denote by $i$.

Since $\{ D_{A}(a) | a \in A \}$ is a basis for the Zariski topology on $Spec A$, there is some $a \in A$ such that $i(x) \in D_{A}(a)$ and $D_{A}(a) \subset i(N \cap U)$, noting that since $U$ is open in $X$, $N \cap U$ is open in $N$. 

Now, as we have remarked, $(D_{A}(a), \mathcal{O}_{Spec A} | D_{A}(a))$ is isomorphic to an affine scheme. Hence $(i^{-1}(D_{A}(a)), i^{*}(\mathcal{O}_{Spec A} | D_{A}(a)))$ is isomorphic to an affine scheme, where $i^{*}$ is the [[inverse image]] functor from sheaves of commutative rings on $D_{A}(a)$ to sheaves of commutative rings on $i^{-1}(D_{A}(a))$. 

But $i^{*}(\mathcal{O}_{Spec A} | D_{A}(a))$ is isomorphic to $\mathcal{O}_{U} | i^{-1}(D_{A}(a))$. Since $i^{-1}(D_{A}(a)) \subset i^{-1}(i(N \cap U)) = N \cap U \subset U$, we conclude that we can take $W$ to be $i^{-1}(D_{A}(a))$.

=--

category: algebraic geometry
[[!redirects open subschemes]]