
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[topology]], the "shrinking lemma" (lemma \ref{PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained} below) states that on a [[normal topological space]] the patches of every [[locally finite cover]] may be replaced by smaller patches which still cover the space, but such that their [[topological closures]] are contained in the original patches. 

If there is more than a [[countable set]] of elements in the original cover, then this conclusion requires [[excluded middle]] and [[Zorn's lemma]], hence the [[axiom of choice]].

The shrinking lemma is needed in the proof that [[ paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]].

## Statement

+-- {: .num_lemma #PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained}
###### Lemma
**(shrinking lemma for locally finite covers)**

Assuming the [[axiom of choice]] then:

Let $X$ be a [[topological space]] which is [[normal topological space|normal]] and let $\{U_i \subset X\}_{i \in I}$ be a [[locally finite cover|locally finite]] [[open cover]].

Then there exists another open cover $\{V_i \subset X\}_{i \in I}$ such that the [[topological closure]] $Cl(V_i)$ of its elements is contained in the original patches:

$$
  \underset{i \in I}{\forall}
  \left(
     V_i \subset Cl(V_i) \subset U_i
  \right)
  \,.
$$

=--

We now **prove** this in  increasing generality, first for  binary open covers (lemma \ref{ShrinkingLemmaForBinaryCover} below), then for finite covers (lemma \ref{ShrinkinglemmaForFiniteCovers}), then for locally finite countable covers (lemma \ref{ShrinkingLemmaForLocallyFiniteCountableCovers}), and finally for general locally finite covers (lemma \ref{PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained}, proof [below](#PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained)). It is only the last statement that needs the [[axiom of choice]].

+-- {: .num_lemma #ShrinkingLemmaForBinaryCover}
###### Lemma
**(shrinking lemma for binary covers)**

Let $(X,\tau)$ be a [[normal topological space]] and let $\{U_i \subset X\}_{i \in \{1,2\}}$ an [[open cover]] by two [[open subsets]].

Then there exists an open set $V_1 \subset X$ whose [[topological closure]] is contained in $U_1$

$$
  V_1 \subset Cl(V_1) \subset U_1
$$

and such that $\{V_1,U_2\}$ is still an open cover of $X$. 

=--

+-- {: .proof}
###### Proof

Since $U_1 \cup U_2 = X$ it follows (by [[de Morgan's law]]) that their [[complements]] $X \backslash U_i$ are [[disjoint subset|disjoint]] [[closed subsets]]. Hence by normality of $(X,\tau)$ there exist disjoint open subsets 

$$
  V_1 \supset X \backslash U_2
  \phantom{AAA}
  V_2 \supset X \backslash U_1
  \,.
$$

By their disjointness, we have the following inclusions:

$$
  V_1 \subset X \backslash V_2 \subset U_1
  \,.
$$

In particular, since $X \backslash V_2$ is closed, this means that $Cl(V_1) \subset X \backslash V_2$.

Hence it only remains to observe that $V_1 \cup U_2 = X$, by definition of $V_1$.


=--

+-- {: .num_lemma #ShrinkinglemmaForFiniteCovers}
###### Lemma
**(shrinking lemma for finite covers)**

Let $(X,\tau)$ be a [[normal topological space]], and let $\{U_i \subset X\}_{i \in \{1, \cdots, n\}}$ be an [[open cover]] with a [[finite number]] $n \in \mathbb{N}$ of patches. Then there exists another open cover $\{V_i \subset X\}_{i \in I}$ such that $Cl(V_i) \subset U_i$ for all $i \in I$.

=--


+-- {: .proof}
###### Proof

By [[induction]] using lemma \ref{ShrinkingLemmaForBinaryCover}.

To begin with, consider $\{ U_1, \underoverset{i = 2}{n}{\cup} U_i\}$. This is a binary open cover, and hence lemma \ref{ShrinkingLemmaForBinaryCover} gives an open subset $V_1 \subset X$ with $V_1 \subset Cl(V_1) \subset U_1$ such that $\{V_1, \underoverset{i = 2}{n}{\cup} U_i\}$ is still an open cover, and accordingly so is

$$
  \{ V_1  \} \cup \left\{ U_i \right\}_{i \in \{2, \cdots, n\}}
  \,.
$$

Similarly we next find an open subset $V_2 \subset X$ with $V_2 \subset Cl(V_2) \subset U_2$ and such that

$$
  \{ V_1, ,V_2  \} \cup \left\{ U_i \right\}_{i \in \{3, \cdots, n\}}
$$
 
is an open cover. After $n$ such steps we are left with an open cover $\{V_i \subset X\}_{i \in \{1, \cdots, n\}}$ as required.

=--

+-- {: .num_remark}
###### Remark

Beware that the [[induction]] in lemma \ref{ShrinkinglemmaForFiniteCovers} does _not_ give the statement for infinite [[countable covers]]. The issue is that it is not guaranteed that $\underset{i \in \mathbb{N}}{\cup} V_i$ is a cover. 

And in fact, assuming the [[axiom of choice]], then there exists a  counter-example of a countable cover on a normal spaces for which the shrinking lemma fails (a [[Dowker space]] due to [Beslagic 85](#Beslagic85)).

=--

This issue is evaded if we consider [[locally finite covers]]:

+-- {: .num_lemma #ShrinkingLemmaForLocallyFiniteCountableCovers}
###### Lemma
**(shrinking lemma for locally finite countable covers)**

Let $(X,\tau)$ be a [[normal topological space]] and $\{U_i \subset X\}_{i \in \mathbb{N}}$ a [[locally finite cover|locally finite]] [[countable cover]]. Then there exists [[open subsets]] $V_i \subset X$ for $i \in \mathbb{N}$ such that $V_i \subset Cl(V_i) \subset U_i$ and such that $\{V_i \subset X\}_{i \in \mathbb{N}}$ is still a cover.

=--

+-- {: .proof}
###### Proof

As in the proof of lemma \ref{ShrinkinglemmaForFiniteCovers}, there exist $V_i$ for $i \in \mathbb{N}$ such that $V_i \subset Cl(V_i) \subset U_i$ and such that for every finite number, hence every $n \in \mathbb{N}$, then 

$$
  \underoverset{i = 0}{n}{\cup} V_i \cup
  \underoverset{i = n+1}{\infty}{\cup} U_i
  \;=\; X\,.
$$ 

Now the extra assumption that $\{U_i \subset X\}_{i \in I}$ is [[locally finite cover|locally finite]] implies that every $x \in X$ is contained in only finitely many of the  $U_i$, hence that for every $x \in X$ there exists $n_x \in \mathbb{N}$ such that

$$
  x \notin \underoverset{i = n_x+1}{\infty}{\cup} U_i
  \,.
$$

This implies that for each $x$

$$
  x \in \underoverset{i = 0}{n_x}{\cup} V_i 
  \subset \underset{i \in \mathbb{N}}{\cup} V_i
$$

hence that $\{V_i \subset X\}_{i \in \mathbb{N}}$ is indeed a cover of $X$.

=--

We now invoke [[Zorn's lemma]] to generalize the shrinking lemma for finitely many patches (lemma \ref{ShrinkinglemmaForFiniteCovers}) to arbitrary sets of patches:

+-- {: .proof}
###### Proof
of the general shrinking lemma \ref{PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained}

Let $\{U_i \subset X\}_{i \in I}$ be the given locally finite cover of the normal space $(X,\tau)$. Consider the set $S$ of [[pairs]] $(J, \mathcal{V})$ consisting of

1. a [[subset]] $J \subset I$;

1. an $I$-indexed set of open subsets $\mathcal{V} = \{V_i \subset X\}_{i \in I}$

with the property that 

1. $(i \in J \subset I) \Rightarrow ( Cl(V_i) \subset U_i )$;

1. $(i \in I \backslash J) \Rightarrow ( V_i = U_i )$.

1. $\{V_i \subset X\}_{i \in I}$ is an open cover of $X$.

Equip the set $S$ with a [[partial order]] by setting

$$
  \left(
    (J_1, \mathcal{V})
    \leq
    (J_2, \mathcal{W})
  \right)
    \Leftrightarrow
  \left(
    \left(
      J_1 \subset J_2
    \right)
    \,\text{and}\,
    \left(
      \underset{i \in J_1}{\forall}
      \left(
         V_i = W_i
      \right)
    \right)
  \right)  
  \,.
$$

By definition, an element of $S$ with $J = I$ is an open cover of the required form.

We claim now that a [[maximal element]] $(J, \mathcal{V})$ of $(S,\leq)$ has $J = I$.

For assume on the contrary that there were $i \in I \backslash J$. Then we could apply the construction in lemma \ref{ShrinkingLemmaForBinaryCover} to replace that single $V_i$ with a smaller open subset $V'_i$ to obtain $\mathcal{V}'$ such that $Cl(V'_i) \subset V_i$ and such that $\mathcal{V}'$ is still an open cover. But that would mean that $(J,\mathcal{V}) \lt (J \cup \{i\}, \mathcal{V}')$, contradicting the assumption that $(J,\mathcal{V})$ is maximal. This [[proof by contradiction|proves by contradiction]] that a maximal element of $(S,\leq)$ has $J = I$ and hence is an open cover as required.

We are reduced now to showing that a maximal element of $(S,\leq)$ exists. To achieve this we invoke [[Zorn's lemma]]. Hence we have to check that every [[chain]] in $(S,\leq)$, hence every [[total order|totally ordered]] [[subset]] has an [[upper bound]].

So let $T \subset S$ be a [[total order|totally ordered]] subset. Consider the union of all the index sets appearing in the pairs in this subset:

$$
  K
    \;\coloneqq\;
  \underset{(J,\mathcal{V}) \in T  }{\cup} J
  \,.
$$

Now define open subsets $W_i$ for $i \in K$ picking any $(J,\mathcal{V})$ in $T$ with $i \in J$ and setting

$$
  W_i \coloneqq V_i \phantom{AAA} i \in K
  \,.  
$$

This is independent of the choice of $(J,\mathcal{V})$, hence well defined, by the assumption that $(T,\leq)$ is totally ordered.

Moreover, for $i \in I\backslash K$ define

$$
  W_i \coloneqq U_i  \phantom{AAA} i \in I \backslash K
  \,.
$$

We claim now that $\{W_i \subset X\}_{i \in I}$ thus defined is a cover of $X$. Take an arbitrary point $x \in X$. If $x \in U_i$ for some $i \notin K$, we have $U_i = W_i$ and therefore $x$ is in $\underset{i \in I}{\cup} W_i$. Otherwise, combining with the assumption that $\{U_i \subset X\}_{i \in I}$ is locally finite, the set $J_x$ of indices $i \in I$ such that $x \in U_i$ is finite and $J_x \subset K$. Since $(T,\leq)$ is a total order, it must contain an element $(J, \mathcal{V})$ such that $J_x \subset J$.  And since that $\mathcal{V}$ is a cover and $x$ cannot belong to any $U_i$ with $i$ outside of $J_x$, it must be that $x \in \underset{i \in J_x}{\cup} V_i \subset \underset{i \in J}{\cup} V_i$, and hence $x$ is in $\underset{i \in I}{\cup} W_i$.

This shows that $(K,\mathcal{W})$ is indeed an element of $S$. It is clear by construction that it is an upper bound for $(T ,\leq )$. Hence we have shown that every [[chain]] in $(S,\leq)$ has an upper bound, and so Zorn's lemma implies the claim.


=--

## References

The above account follows

* [[Matt Rosenzweig]], _[General shrinking lemma for normal spaces](https://matthewhr.wordpress.com/2014/06/11/general-shrinking-lemma-for-normal-spaces/)_

The example (a [[Dowker space]]) of a normal space with a (not locally-finite) countable cover to which the shrinking lemma does not apply is given in

* {#Beslagic85} Amer Beslagic, _A Dowker product_, Transactions of the AMS, vol 292, number 2 (1985) ([pdf](http://www.ams.org/journals/tran/1985-292-02/S0002-9947-1985-0808735-X/S0002-9947-1985-0808735-X.pdf))



