

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

For [[metric spaces]] with their [[metric topology]] it is true that [[sequentially compact metric spaces are equivalently compact metric spaces]]. The analogous statement fails for more general [[topological spaces]]: for them, being [[sequentially compact topological space|sequentially compact]] in general neither implies nor is implied by being [[compact topological space|compact]] (see the counter-examples [here](sequentially+compact+topological+space#Examples)).

But the failure of this equivalence is not due to a deficit in the concept of [[convergence]] but in the concept of [[sequences]] and sub-sequences. If the latter are generalized to [[nets]] and [[sub-nets]] (beware that the definition of sub-nets is slightly non-obvious), then the analogue of the statement remains true in generality: A topological space is [[compact topological space|compact]] precisely if every [[net]] in it has a [[sub-net]] that [[convergence]].


## Statement

+-- {: .num_prop #CompactSpacesEquivalentlyHaveConvergetSubnets}
###### Proposition
**(compact spaces are equivalently those for which every net has a converging subnet)**

Assuming [[excluded middle]] and the [[axiom of choice]], then:

A [[topological space]] $(X,\tau)$ is [[compact topological space|compact]] precisely if every [[net]] in $X$ has a [[sub-net]] that [[convergence|converges]].

=--

We break this up into lemmas \ref{InACompactSpaceEveryNetHasAConvergentSubnet} and \ref{IfEveryNetHasConvergentSubnetThenSpaceIsCompact}:

+-- {: .num_example #InACompactSpaceEveryNetHasAConvergentSubnet}
###### Lemma
**(in a compact space, every net has a convergent subnet)**

Let $(X,\tau)$ be a [[compact topological space]]. Then every net in $X$ has a convergent subnet.

=--

+-- {: .proof}
###### Proof

Let $\nu \colon A \to X$ be a net. We need to show that there is a subnet which converges.

For $a \in A$ consider the [[topological closures]] $Cl(S_a)$ of the sets $S_a$ of elements of the net beyond some fixed index:

$$
  S_a 
    \;\coloneqq\;
  \left\{
    \nu_b  \in X \;\vert\; b \geq a
  \right\}
  \subset X
  \,.
$$

Observe that the set $\{S_a \subset X\}_{a \in A}$ and hence also the set $\{Cl(S_a) \subset X\}_{a \in A}$ has the [[finite intersection property]], by the fact that $A$ is a [[directed set]]. Therefore [this prop. ](finite+intersection+property#CompactnessInTermsOfFiniteIntersectionProperty) implies from the assumption of $X$ being compact that the intersection of _all_ the $Cl(S_a)$ is non-empty, hence that there is an element

$$
  x \in \underset{a \in A}{\cap}  Cl(S_a)
  \,.
$$

In particular every [[neighbourhood]] $U_x$ of $x$ intersects each of the $Cl(S_a)$, and hence also each of the $S_a$. By definition of the $S_a$, this means that for every $a \in A$ there exists $b \geq a$ such that $\nu_b \in U_x$, hence that $x$ is a [[cluster point]] of the net.

We will now produce a [[sub-net]] 

$$
  \array{
     B && \overset{f}{\longrightarrow} && A
     \\
     & \searrow && \swarrow_{\nu}
     \\
     && X
  }
$$


that converges to this cluster point. To this end, we first need to build the domain directed set $B$. Take it to be the sub-directed set of the Cartesian product directed set of $A$ with the directed neighbourhood set $Nbhd_X(x)$ of $x$

$$
  B \subset A_{\leq} \times Nbhd_X(x)_{\supset}
$$

on those pairs such that the element of the net indexed by the first component is is contained in the second component:

$$
  B 
    \;\coloneqq\;
  \left\{
     (a,U_x)  \,\vert \, \nu_a \in U_X
  \right\}
  \,.
$$

It is clear $B$ is a [[preordered set]]. We need to check that it is indeed directed, in that every pair of elements $(a_1, U_1)$, $(a_2, U_2)$ has a common upper bound $(a_{bd}, U_{bd})$. Now since $A$ itself is directed, there is an upper bound $a_3 \geq a_1, a_2$, and since $x$ is a cluster point of the net there is moreover an $a_{bd} \geq a_3 \geq a_1, a_3$ such that $\nu_{a_{bd}} \in U_1 \cap U_2$. Hence with $U_{bd} \coloneqq U_1 \cap U_2$ we have obtained the required pair.

Next take the function $f$ to be given by

$$
  \array{
     B &\overset{f}{\longrightarrow}& A
     \\
     (a, U) &\overset{\phantom{AAA}}{\mapsto}& a
  }
  \,.
$$

This is clearly order preserving, and it is cofinal since it is even a surjection. Hence we have defined a subnet $\nu \circ f$.

It now remains to see that $\nu \circ f$ converges to $x$, hence that for every open neighbourhood $U_x$ of $x$ we may find $(a,U)$ such that for all $(b,V)$ with $a \leq b$ and $U \supset V$ then $\nu(f(b,V)) = \nu(b) \in U_x$.  Now by the nature of $x$ there exists some $a$ with $\nu_a \in U_x$, and hence if we take $U \coloneqq U_x$ then nature of $B$ implies that with $(b, V) \geq (a,U_x)$ then $b \in V \subset U_x$.

=--

+-- {: .num_example #IfEveryNetHasConvergentSubnetThenSpaceIsCompact}
###### Lemma

Assuming [[excluded middle]], then:

Let $(X,\tau)$ be a [[topological space]]. If every [[net]] in $X$ has a [[subnet]] that [[convergence|converges]], then $(X,\tau)$ is a [[compact topological space]].

=--

+-- {: .proof}
###### Proof



By [[excluded middle]] we may equivalently prove the [[contrapositive]]: If $(X,\tau)$ is not compact, then not every net in $X$ has a convergent subnet.

Hence assume that $(X,\tau)$ is not compact. We need to produce a net without a convergent subnet.

Again by [[excluded middle]], then by [this prop.](finite+intersection+property#CompactnessInTermsOfFiniteIntersectionProperty) $(X,\tau)$ not being compact means equivalently that there exists a set $\{C_i \subset X\}_{i \in I}$ of [[closed subsets]] satisfying the [[finite intersection property]], but such that their intersection is empty: $\underset{i \in I}{\cap} C_i = \emptyset$.

Consider then $P_{fin}(I)$, the set of [[finite set|finite]] [[subsets]] of $I$. By the assumption that $\{C_i \subset X\}_{i \in I}$ satisfies the [[finite intersection property]], we may [[axiom of choice|choose]] for each $J \in P_{fin}(I)$ an element

$$
  x_J \in \underset{i \in J \subset I}{\cap} C_i
  \,.
$$



Now $P_{fin}(X)$ regarded as a [[preordered set]] under inclusion of subsets is clearly a [[directed set]], with an upper bound of two finite subsets given by their [[union]]. Therefore we have defined a net

$$
  \array{
     P_{fin}(X)_{\subset} &\overset{\nu}{\longrightarrow}& X
     \\
     J &\overset{\phantom{AAA}}{\mapsto}& x_J
  }
  \,.
$$

We will show that this net has no converging subnet.

Assume on the contrary that there were a subnet

$$
  \array{
     B && \overset{f}{\longrightarrow} && P_{fin}(X)
     \\
     & \searrow && \swarrow_{\nu}
     \\
     && X
  }
$$

which converges to some $x \in X$. 

By the assumption that $\underset{i \in I}{\cap} C_i = \emptyset$, there would exist an $i_x \in I$ such that $x \neq C_{i_x}$, and because $C_i$ is a [[closed subset]], there would exist even an [[open neighbourhood]] $U_x$ of $x$ such that $U_x \cap C_{i_x} = \emptyset$. This would imply that $x_J \neq U_x$ for all $J \supset \{i_x\}$.

Now since the function $f$ defining the subset is cofinal, there would exist $b_1 \in B$ such that $\{i_x\} \subset f(b_1)$. Moreover, by the assumption that the subnet converges, there would also be $b_2 \in B$ such that $\nu_{b_2 \leq \bullet} \in U_x$. Since $B$ is directed, there would then be an upper bound $b \geq b_1, b_2$ of these two elements. This hence satisfies both $\nu_{f(e)} \in U_x$ as well as $\{i_x\} \subset f(b_1) \subset f(b)$. But the latter of these two means that $\nu_{f(b)}$ is not in $U_x$, which is a contradiction to the former. Thus we have a [[proof by contradiction]].

=--

## Related concepts

* [[sequentially compact metric spaces are equivalently compact metric spaces]]

* [[countably compact metric spaces are equivalently compact metric spaces]]

* [[sequentially compact metric spaces are totally bounded]]

* [[Lebesgue number lemma]]

