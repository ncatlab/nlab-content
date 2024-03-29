## Idea


In ([Jacobs 12](#Jacobs)) the approach to categorical logic where the substrate carrying the logical notions are [[Heyting algebras]] of [[subobjects]] in a [[topos]] is replaced by a new one where the substrate is [[effect algebra of predicates]] in [[extensive categories]].

## Predicates

Let $C$ be a category with coproducts (written $+$). A **predicate** is a map $X\stackrel{p}{\to} X+X$ such that $[id_X,id_X]\circ p=id_X$.

A predicate is hence in particular a [[nLab:coalgebra for an endofunctor|coalgebra]] for the $C$-endofunctor  $X\mapsto X+X$.

If we denote the coproduct inclusions by $k_1:X\to X+X$ and $k_2:X\to X+X$, then their coproduct $[k_2,k_1]:X+X\to X+X$ is the swap map (which is a self-inverse equivalence).

For a predicate $p$ the **orthocomplement of $p$** is defined to be the composite $p^\perp:=[k_2,k_1]\circ p$. We have $(p^\perp)^\perp\simeq p$.

## Effect algebra of predicates
+-- {: .un_lemma}
###### Lemma
In a extensive category we have the following diagrams involving coproducts and pullbacks:

(...lots of diagrams...)
=--

+-- {: .un_cor}
###### Corollary
Predicates with the operations defined by (...) assemble to an effect algebra called **the effect algebra of predicates**.
=--

## Examples

+-- {: .un_remark}
###### Examples

If $X\in Set$ is a set and $p:X\to X+X$ is a predicate on $X$, then $p(x)=k_1 x$ or $p(x)=k_2 x$.

In particular we can identify $p$ with a subset $U=\{x|p(x)=k_1 x\}\subseteq X$. Then $\neg U=\{x|p(x)=k_2 x\}=\{x|p^\perp(x)=k_1 x\}$

=--

+-- {: .proof}
###### Proof
In $Set$ we have [[nLab:disjoint coproduct|disjoint coproducts]] such that in our case we have
$$\array{
0&\to &X\\
\downarrow&&\downarrow^{k_2}\\
X&\stackrel{k_1}{\to}&X+X
}$$
is a pushout square as well as a pullback square. And in $Set$ we have [[nLab:universal colimit|universal coproducts]] such that in our case we have $X+X\simeq X$. Now if we assume $[id_X,id_X]\circ p\simeq id_X$ the couniversal property of the coproduct implies that $p$ factors through $k_1$ and $k_2$ followed by an equivalence.

A category having disjoint- and universal coproducts is called an [[nLab:extensive category]].
=--

Further examples are listed at

* [[nLab:coalgebra of the real interval]]

* some of the examples at [[nLab:coalgebra for an endofunctor]]

## References

* [[Bart Jacobs]], _New Directions in Categorical Logic, for Classical, Probabilistic and Quantum Logic_, (2012) ([arXiv:1205.3940 ](http://arxiv.org/abs/1205.3940))
 {#Jacobs}
